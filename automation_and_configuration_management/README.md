* *Automation and Configuration Management*

This is a kinda core part of infrastructure management in any form. Sooner or
later time will come, when you wanted a few things to get done automatically,
without much supervision. Especially when the infrastructure is growing and
complexity arise. We basically want to eliminate things that are redundant to
operate. Because, we need to concentrate on more volatile things within the
infra more closely.

Oh,if you missed earlier parts of this series, here they are:

[Part-One](https://unixbhaskar.wordpress.com/2022/04/26/linux-infrastructure-management-part-i/)

[Part-Two](https://unixbhaskar.wordpress.com/2022/04/27/linux-infrastructure-management-part-ii/)

[Part-Three](https://unixbhaskar.wordpress.com/2022/04/28/linux-infrastructure-management-part-iii/)

[Part-Four](https://unixbhaskar.wordpress.com/2022/04/29/linux-infrastructure-management-part-iv/)

[Part-Five](https://unixbhaskar.wordpress.com/2022/04/30/linux-infrastructure-management-part-v/)

I know the cron job does fine and most of the time is sufficient to get the
thing done, but beyond certain points, we need to consider how to enhance and
get things done in the proper manner. Writing tools to do the job done was the
norm in open system management because it will allow you to do so, a rich set of
inbuilt tools come along with it. I wrote and still do write whenever I got the
chance to enhance. But having said that, the modern SCM (Software Configuration
Managers) are quite smart (and I haven't had a hands-on thing with
cfengine..heck), everything else is modern, even chef. I have done a few things
with puppet and salt. Like both of them. Both have pros and cons, like other
software. And mind you, it does require some steep learning curve, but it will
be all worth it if you spend enough time to get the gory details of it or how it
works internally. Most the shops, even the cloud-based projects are heavily lean
on it, because they understand the importance and flexibility it brings to the
table. You can attend and achieve so many things with minimal fuss and
rigor. While you need to be cautious at times, to monitor it that it is doing
the right job, what was intended. CI (Jenkins et al.) can be your friend.

Puppet is written in ruby and very flexible, purely using OOPS concepts inside
it. The noticeable downside would be the slow nature of work/processing. On the
other hand, Saltstack is written in python, and quite flexible and extensible
too. And performance-wise it will probably beat puppet. That is python's ability
to interpret quickly. Anyway, you can choose whatever is your cup of tea, or the
best bet for the particular environment. Now, a little catch, I should warn you,
you need to be very conversant with those or have personnel at your disposal to
do the job and troubleshoot if something goes wrong (sometimes it will
certainly). So, you have been exposed to the system, or the personnel exposed to
those systems have to have much more insight to get things back on track.

I would propose, designating only those personnel involved in it, those who have
an inclination towards it, but not to someone who wanted things done by it. As I
said earlier it needs a little steep learning curve and an understanding of
internals too. Not everybody has that kind of inclination towards it. You need
to identify the resource from your team, or budget permit hire only those who
are deep into it.

There are plenty of SCM around free and proprietary. To name, Ansible is used in
quite a few places and I heard it is done the job well (Again I do not have
hands-on with it). Anyway, we need to consider the different aspects of the
infrastructure requirement. What the present condition is? How it is operating?
How does it accomplish the work done? Once we get a clear-cut answer for those,
then we can proceed to select the tool. Moreover, we need to evaluate the tool
before we recommend the "Black Suit" wearing a guy . He might come up with
something which might catch us off guard. So, try not to be in that position,
get as many details about the product as possible. It will surely help if you
have some use cases under your sleeves.  And it would be wonderful if we can
make some use cases relate to the present environment with that tool.

People, in general, don't like changes, but we are trying to do a thing that
will change the way the environment operates and perform. And we are trying to
get the best out of it with some more effort. Not necessarily all the time we
come out winner, but we can make an effort that we can be winners most of the
time. The prime effect would be two: one, technology will win, and we get boosts
in our confidence and feel valued, which is a very crucial and important aspect
of infrastructure professionals. I have seen and realized that once you feel
truly valued in some setup, you can do better and help out better with less
conflict and ego. Now, you are in a position to do more and take more
responsibility.

And yes, mentoring the other person next to you, will have long-lasting
effects. I am not sure how that can be done, because different people use
different strategies to get along. To me, I am very open and straight to
everyone, few don't like it, but they come to terms when they spend some time
with me. Yep, that's what I am. I believe being genuine to everyone is key, they
feel confident about you. I have seen a few incompetent to play foul to save
their arse and make thing looks rosy. If you sense it, bust it on them but.

Say, we want to change the configure file of the fleet of the webserver farms,
which consists of 350 servers. Doing that by hand would be ridiculous (assuming
similar kinds of changes has to be made to all the servers) and time-consuming
and error-prone too. So, to eliminate those cons we need to take advantage of
SCM exposed to us. It's just a matter of writing once and running everywhere
thing. This means, you need to define it in one place and agents will in from
the master server/servers to get it to sync in a quick time. Pretty neat and
effortless (thinking in terms of writing a manual script and invoking it). And
likewise, you can withdraw your applied changes in almost no time. So it is a
big-time and effort saver. Most enterprises including cloud premier operators
embrace this kind of SCM to make their fleet of servers get a particular service
at a specific time.

I believe all the SCM providers including puppet and Saltstack has a plethora of
modules available for ready to use. Just get them from the internet and modify
them according to your requirement. Those are all template files and a few of
them are really smart to assume the requirement too (specifically dependency
related). Now, it is making our life easy and more productive. We get more
chances to actually lean on the problem than thinking of something else. It is a
boon to have that kind of software available for infrastructure management. And
you can do many different tasks accomplish with it, with minimal fuss. I believe
the syntax is pretty clear and precise, thanks to the pain taken by those
authors to make life easy for others.

I have seen people in infrastructure management doing automation for the sake of
doing it. Why? There is plenty of reason, notably to show the vertical that they
can do a better job and "quality" jobs; expertise in that skill, in turn, trying
to say "elevate me" kinda statement. Most of those folks get the recipe from the
internet (mostly from an unverified source, how do you verify that?) and plain
modification. I have seen they are not even bothering to see checksum of the
download. If something creeps in, the entire infrastructure will be at
stake. And also the poor practices of doing things (yeah, I know the same result
can be achieved in different ways..), but certainly not the inefficient
way. There must be a proper and efficient way of handling it, for that before
implementing that, a lot of tests have to be made. Most of the time and
infrastructure missing those guidelines. Let me give you an example of this kind
of practice. I was in with a big name, but they are trying to get a foot hole in
IT and got a non-IT client. So, they have hired me to do a certain job. Now,
while in that setup I have seen people use very poor practices on an open
system. Instead of using key-exchange, they are using "sshpass"!!

The biggest problem here, the whole set rarely read the man page, instead, they
heavily rely on google. And they might have seen some unverified blogs and used
that and nobody cross-checked. Now, if they are good enough they might have
gleaned on the man page before doing all the nonsense. Let me give you an
excerpt from the man page itself.

```
SECURITY CONSIDERATIONS

   First and foremost, users of sshpass should realize that ssh's insistence on
   only getting the password interactively is not without reason. It is close to
   impossible to securely store the password, and users of sshpass should
   consider whether ssh's public key authentication provides the same end-user
   experience, while involving less hassle and being more secure.

   The -p option should be considered the least secure of all of sshpass's
   options.  All system users can see the password in the command line with a
   simple "ps" command. Sshpass makes a minimal attempt to hide the password, but
   such attempts are doomed to create race conditions without actually solving
   the problem. Users of sshpass are encouraged to use one of the other password
   passing techniques, which are all more secure.

   In particular, people writing programs that are meant to communicate the
   password programmatically are encouraged to use an anonymous pipe and pass
   the pipe's reading end to sshpass using the -d option.

```

So, you can see the heads upright? Does the environment had got some sort of
binding to some sort of compliance to prohibit key-exchange? No. They just
simply failed to realize the importance of it. See, the little things make a
hell of a lot of difference.

Because I did open source development and install tweaks to many thousands of
software. So, I have the habit of reading the README or DOCUMENTATION file
before I started to do anything with the software. It is always a good habit to
read the important information beforehand and then jump onto it. It's help
certainly. So, getting into that habit needs sometimes spend with it. Nowadays,
most people are so accustomed to search engines,that they forgot the habit of
reading the crucial piece. Because whenever they are in doubt, they just use the
search engine to find the answer, I too do, but in very limited cases, not all
the time.

In the next article, I will discuss backup and retrieval for sustainable
infrastructure.
