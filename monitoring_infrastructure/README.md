* *Monitoring Infrastructure*

Building the infrastructure is fine, but we need to monitor it constantly for
its status and its health. So, we can take a decision on the basis of that
report. And sometimes we will introduce some strategy to make a decision upon
the status we received. Many enterprises deploy different kinds of tools to
measure those statuses and take the decision out of those reports. But, at least
a few of them generate or are prone to produce some false alarms and reports
based on that. So, we need to eliminate those "false positives" from the actual
reports to streamline the decision-making process.

In case, if you have missed those previous parts, here they are :

[Part-One](https://unixbhaskar.wordpress.com/2022/04/26/linux-infrastructure-management-part-i/)

[Part-Two](https://unixbhaskar.wordpress.com/2022/04/27/linux-infrastructure-management-part-ii/)

[Part-Three](https://unixbhaskar.wordpress.com/2022/04/28/linux-infrastructure-management-part-iii/)

[Part-Four](https://unixbhaskar.wordpress.com/2022/04/29/linux-infrastructure-management-part-iv/)

[Part-Five](https://unixbhaskar.wordpress.com/2022/04/30/linux-infrastructure-management-part-v/)

[Part-Six](https://unixbhaskar.wordpress.com/2022/05/01/linux-infrastructure-management-part-vi/)

[Part-Seven](https://unixbhaskar.wordpress.com/2022/05/02/linux-infrastructure-management-part-vii/)

Let's get our discussion absolutely to the point, by which I mean, let us talk
about some tools, which are deployed across the enterprises. As I believe and
use and advocate using free and open-source software everywhere, plus I am more
accustomed to that pattern of open source; you can expect lots of suggestions
based on the information and hands-on things. As a side effect, these people
have to have a clear-cut idea of customizing the software according to their
infrastructure's needs. Now, how do you arrest the "false positives"??  There
are methods available to distinguish the actual positive from the false one. One
has to be keen enough to find the details and specifications aware, so it will
be an easy thing to deduce the fact from the result.

Now, what to monitor? I have had been an environment where I saw people monitor
everything (seeing those I conclude that they just don't understand what they
need to know), and in some environment, where everything is very precious, which
means they know; what exactly needed. In the second case, you are better off by
eliminating lots of unnecessary noise. Knowing what you need is a big step, in
every aspect of life. Likewise, in enterprise infrastructure monitoring; things
to be monitored should very precisely be described and documented.

There is no hide-and-seek for my liking; I like Nagios a lot. Why? Partly
because of its flexible nature and easy customization and modularity. Of course,
great community support behind it. And I did lots of hands-on stuff with it for
one of my engagements with a corporation. By which I came to know a lot of
intricacies of its working and liking and disliking. But as I said earlier that
some tools are prone to false alarms, and unfortunately Nagios is one of them. I
personally, tried to figure it out by doing lots of checking by hand; because I
was exposed to it, just to make sure that the result I am seeing is correct and
coming from the right places.

[[https://www.nagios.org/][*Nagios*]] can be built from scratch as per the requirement at hand. I did it, by
compiling it from the source,and refraining from getting it by the package
manager of the particular OS. By doing so, I came to know how I can fine-tune my
build(like every other open-source software build). But, going by the package
manager route gives you an OS-dependent way of deploying it, which is sometimes
beneficial for the infrastructure, but a less flexible one. It's up to you, how
you go about the job.

Let me get fair enough to other monitoring tools too. They are as good as
Nagios, yep few of them; not all. Plus the overhead of configuring those tools
requires you to invest a great deal of precious time to get it right. Am I
sounding too lean towards Nagios?? Might be, but I can tell, [[https://www.cacti.net/][/Cacti]]/ is a
wonderful tool, I had struggled a lot to get it going, but in the end, it was
all satisfactory.

But in the end, you have to have some sort of understanding of /[[https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol][SNMP]]/ because the
underlying protocol will be that for infrastructure monitoring. Understanding
the *OID* and *MIB* does help greatly to decide what to do with the monitoring.

This concludes our take on Linux Infrastructure Management, but a lot more
desired to be left . Before I leave you ,let me share some of the books which
enhance my understanding of infrastructure personnel.

*Bibliography:*

[Check Out Books](https://www.goodreads.com/review/list/47198624-bhaskar-chowdhury?ref=nav_mybooks&shelf=read)

Also, uncountable /PDFs/ and notes from various journals, research papers, which I
have consulted and tried to understand.
