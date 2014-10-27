# Solution Delivary
Well we have look into the problem and how to tackle them,but providing solution to the external and as well internal stakeholders needs different set of jobs.And ultimately that counts a lot about teams performance measured by some "Black Suit" wearing fellow sitting on top.

But from technical stand point of view,we have to make sure everything in place to make the solution will be sustained one.And we might use it in the future(as I mentioned the importance of Wiki et al in chapter 3 information management).We need to organise every solution like it should look like a KB in place.It will save time and headache later  to do something useful later.Certainly help to automate things and make an enhancement lot easier.

So,diffent enterprise approach to the problem solving different way and few of them stand out.The solution should consists of a link to the wiki or whatever or wherever we post the steps and outcome of that perticular problem.Say,the infrastructure having a perenneial problem with httpd and it has been solve with some monumental efforts. That efforts should not go waste ,and should be in a proper format to concerned persons(the black suit wearing ) jerk! I have had habit of almost every thing copied from the terminal(yeah I know better method of doing thing )and at least paste on gedit or some other note taking place..if not another vim .So,later I can sort and filter out the absolutely necessary information out of it( processing of raw data) and put it into wiki or document space.

Solutions should absolutely clear and precise.Having said that I meant,it should have step by step approch whenever prossible.If and only if require should go into the details explaining the cause in small vignette.Yes,you got it right ,need to write clear SOP for all the problem we faced and solved.Those SOP's get exchnaged with guy up in the verticals.But do those guys care about it ?? NOO, they don't .They only care about the matix,and they need that to asses the delivery(oh no!),yep that's the way.

I am just providing a SOP here for reference(yeah I know few folks can write even better)

Under Monitoring Standard:

Software : Nagios

Threshhold : Max and Min value


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

Setting “MaxRequestPerChild”  to a non-zero limit will solve some memory leakage problem..but that has to be supplied judiciously.

Say, What is MPM the server is running and how will serve the content will dictate the term for setting parameters in main config file.

How to find ALL the virtualhost in shared box:

/sbin/httpd -S


How to find ALL the modules at once:

/sbin/httpd -M

How to find the MPM on running server?

/sbin/httpd -V


Tips to overcome bottleneck:

1) It's best to set StartServers and MinSpareServers to high numbers, so that if you get a high load just after the server has been restarted, the fresh servers will be ready to serve requests immediately.

2) MinSpareServers and MaxSpareServers to similar (or even the same) values.

3) Having MaxSpareServers close to MaxClients will completely use all of your resources (if MaxClients has been chosen to take full advantage of the resources) and make sure that at any given moment your system will be capable of responding to requests with the maximum speed (assuming that the number of concurrent requests is not higher than MaxClients—otherwise, some requests will be put on hold).

3) Try to run benchmark with the apache inbuilt tool .It's not sufficent ..but give you enough details to see where it is lagging.

4) Status and Info page should be enabled.


Chekpoints too:

1) Please check the docroot for changes i.e file permission change,modified file ,relocation of file inside docroot.

2) Please check wheater httpd/Apache process is alive or not.

3) The process by tools( top,vmstat)

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
