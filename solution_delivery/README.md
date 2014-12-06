# Solution Delivery
Well we have look into the problem and how to tackle them, but providing solution to the external and as well internal stakeholders needs different set of jobs. And ultimately that counts a lot about teams performance measured by some "Black Suit" wearing fellow sitting on top.

But from technical stand point of view, we have to make sure everything in place to make the solution will be sustained one. And we might use it in the future (as I mentioned the importance of Wiki et al in chapter 3 information management). We need to organize every solution like it should look like a KB in place. It will save time and headache later  to do something useful later. Certainly help to automate things and make an enhancement lot easier.

So, different enterprise approach to the problem solving different way and few of them stand out. The solution should consists of a link to the wiki or whatever or wherever we post the steps and outcome of that particular problem. Say, the infrastructure having a perennial problem with httpd and it has been solve with some monumental efforts. That efforts should not go waste ,and should be in a proper format to concerned persons (the black suit wearing ) jerk! I have had habit of almost every thing copied from the terminal (yeah I know better method of doing thing )and at least paste on gedit or some other note taking place, if not another vim .So, later I can sort and filter out the absolutely necessary information out of it( processing of raw data) and put it into wiki or document space.

Solutions should absolutely clear and precise. Having said that I meant, it should have step by step approach whenever possible. If and only if require should go into the details explaining the cause in small vignette. Yes, you got it right ,need to write clear SOP for all the problem we faced and solved. Those SOP's get exchanged with guy up in the verticals. But do those guys care about it ?? NOOOO, they don't .They only care about the matrix, and they need that to asses the delivery (oh no!), yep that's the way.

I am just providing a SOP here for reference (yeah I know few folks can write even better)

Under Monitoring Standard:

Software : Nagios

Threshold : Max and Min value


Service Under Investigation : Httpd/Apache/Apache2

Restart Procedure :

/sbin/service httpd graceful

/sbin/apachectl  graceful

Changes : With date appended with the original file along with Eng name in the same dir.

Check before Bounce: Run “pmap” on the httpd process to find out the memory maps.And must run “ipcs” to find out the resource map for the httpd process.

If and only required to kill httpd ...please use “ipcrm” to killed out shared resources then go for “restart”.


Resolution Aspects:

1) Config file test for httpd service

A: /usr/sbin/apachectl configtest

2)   Checking log files considered to be a good habit.

  Tailf /var/log/httpd/access_log  and tailf /var/log/httpd/error_log

Alternatively , check for sites specific log in specific domain dir log.

Resolving: High Apache/Httpd Memory Usage
Apache can be a big memory user. Apache runs a number of 'servers' and shares incoming requests among them. The memory used by each server grows, especially when the web page being returned by that server includes PHP or Perl that needs to load in new libraries.It is common for each server process to use as much as 10% of a server's memory.
To reduce the number of servers, you can edit your httpd.conf file.There are three settings to tweak: StartServers, MinSpareServers, and MaxSpareServers.Each can be reduced to a value of 1 or 2 and your server will still respond promptly, even on quite busy sites. Some distros have multiple versions of these settings depending on which process model Apache is using.In this case, the 'prefork' values are the ones that would need to change.
To get a rough idea of how to set the MaxClients directive, it is best to find out how much memory the largest apache thread is using. Then stop apache, check the free memory and divide that amount by the size of the apache thread found earlier. The result will be a rough guideline that can be used to further tune (up/down) the MaxClients directive

Setting “MaxRequestPerChild”  to a non-zero limit will solve some memory leakage problem; but that has to be supplied judiciously.

Say, What is MPM the server is running and how will serve the content will dictate the term for setting parameters in main config file.

How to find ALL the virtual host in shared box:

/sbin/httpd -S


How to find ALL the modules at once:

/sbin/httpd -M

How to find the MPM on running server?

/sbin/httpd -V


Tips to overcome bottleneck:

1) It's best to set StartServers and MinSpareServers to high numbers, so that if you get a high load just after the server has been restarted, the fresh servers will be ready to serve requests immediately.

2) MinSpareServers and MaxSpareServers to similar (or even the same) values.

3) Having MaxSpareServers close to MaxClients will completely use all of your resources (if MaxClients has been chosen to take full advantage of the resources) and make sure that at any given moment your system will be capable of responding to requests with the maximum speed (assuming that the number of concurrent requests is not higher than MaxClients—otherwise, some requests will be put on hold).

3) Try to run benchmark with the apache inbuilt tool .It's not sufficient ..but give you enough details to see where it is lagging.

4) Status and Info page should be enabled.


Checkpoints too:

1) Please check the docroot for changes i.e file permission change, modified file ,relocation of file inside document root.

2) Please check whether httpd/Apache process is alive or not.

3) The process by tools( top, vmstat)

4) Find out the file open by httpd process by using system tool like i,e lsof

5) Check how the user is accessing those file by a tool i.e fuser

6) check the website in concern with some external site i.e  http://www.downforeveryoneorjustme.com/

7) If the site has ssl connection check it by s_client from the cli to make sure it responding properly.

8)Check the website landing page response time with the below script:
```
```

#!/bin/bash
CURL="/usr/bin/curl"
GAWK="/usr/bin/gawk"
echo -n "Please pass the url you want to measure:  "
read url
URL="$url"
result=`$CURL -o /dev/null -s -w %{time_connect}:%{time_starttransfer}:%{time_total} $URL`
echo " Time_Connect     Time_startTransfer   Time_total "
echo $result | $GAWK -F: '{ print    $1"               "$2"                   "$3}'
```

```
I would like to record the failure too!!. So I can get a betting insight about the problem solving. You can capture it several ways in the server itself and then send the file by mail or central location from where you can audit. One of ready tool will be UNIX tool i.e script. It will record everything you typed at the terminal and create a file in the respective user home directory (although you can tweak it). They are many more "Enterprise way of doing that thing ...which I am not to inclined to discuss.

RCA, it is big big buzzword in lesser IT driven company ...I have had worked for them I know how pathetically they wrote those, full of nonsense stories; kinda red herring.

Writing an RCA require lot of insight of the system and need to get the details with proper tool and correct interpretation. It should be invigorating details of the problem cause and reader should get excited to know about the fact. Again ,NO STORIES PLEASE. There are plethora of tools come and inbuilt into linux ,which can assist a great deal. What I am trying to say here is, get minimal dependency on third party tools. The more you are depend on it ,the more get deviated from the fact. Yep, I know those tools can give you some eye candy thing ,which will satisfy the needs of "Black Suit" wearing guy; but that's that, nothing more. You ,practically get a opaque information about the event, by the way, it does need some specific daemon to be run in the box with some arcane business license.

So, I would prefer to fuse in some tool ,while building the server/building the AMI for future work. If it is production base/or public facing ,please for heaven's sake DO NOT INSTALL development library in it. I am just trying to close one more door to the bad guys. When the bad event happen we can capture the thing to the points.

I personally write RCA in plain text form (that is the best way I can describe the problem-solution capture). And the RCA should not be too long or filled with some boring details, but must have some pure technicalities attached to it. Most of the time ,it should be restricted to three paragraph, I believe that is good enough. O yeah, you have to pray hard that the set of people you send the thing should read and read throughly (because you have invested lot of invaluable time in it to figure out properly) ,barred those "Black Suite" wearing fellas ,who only rely on matrix. You should be ready to explain every details that you capture out of the problem state, if someone come back to you with good intention (you can figure that out very quickly..), so the more you understand the problem and the solution you are driving for, the better, and you can convey it to less technical people at ease. Yep, that is thing you need to learn, practice and deliver.

Now, you must have some pure technical documentation writer at your disposal. The RCA you write, is not acceptable to the overall client and those "Black Suite" wearing fellow. The technical documentation person will take your text RCA and put it in the "Enterprise ready" format to send them to those fellas. That is the norm in the corporate. The person, should be well versed or should have enough bend of mind understand what you did, and not try to tweak/alter/break ,then put it in that format in "More" readable format for those "true lazy" fellas. You must have a session with the technical documentation expert after he/she format your RCA in that specified format, just to check nothing got distorted or deviated, what you wanted to deliver. A little bit ITIL knowledge would not harm these activities in both the sides. I am sorry, if I sound pretty "Enterprise thing" in the above. I am solely thinking of the BU infra management. But, in the open source world ,we could done it much more variant way.

Next, we will discuss the importance of automation and software configuration management.



