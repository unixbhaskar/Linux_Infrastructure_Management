*  *Basic Understanding Of Infrastructure*

Understanding the environment for work is an utmost need for any person to work
on the infrastructure domain.

For instance, whether it is a normal physical infra or based on the cloud. There
is a */need for certain mind shift/* for working in two different environments.

The traditional *Data Center* environment is drastically different than the
*"Virtual Data Center"* environment. Things are different.

I have been to both places. Operating is an undertaking in both places.*Co-lo*
infrastructure was the dominant factor before cloud engulfed them.

In the physical data center, you need to interact with iron boxes, watch out for
the cables, configure the rack console and check for the lights on the front and
back of the server and take some decisions based on that!!.

While in the virtual data center, you are not so fortunate about seeing those,
but the software makes it simulated for those missing parts, sometimes it missed
and sometimes it hits, depending on how the software is configured and which software
it is (there is a plethora of that kind of software available in the market,
open-source and close-source, both).

Because virtualization arrived late (although it was there for a long time and
people ignored it and hardware support was minimal, so never get kick-off) and
things have changed, people get more aware of their capabilities, started to take
advantage of it.

*"Cost-cutting"* is mandatory in any IT organization's portfolio these days and
they reap benefits of it, by opting for virtualization. But, still, some
important and mission-critical thing runs in a physical place. And I love it;
nothing like seeing an iron box in front of you ..so you can view it with your
x-ray eyes and touch it.

Sometimes I feel (absolutely my personal opinion), that the virtual environment
is a little more fragile than the physical one; probably I came from a normal DC
environment to a VDC environment that is why. I didn't mean to say it is inferior
or bad, but it has many more ways to fail than the physical environment.

Anyway, being in infra management, you have to be well conversant with both the
environment. No other go, simple. Period.

Yes, one thing is very clear that you are bound to be leaner on software to manage
the data center because the underlying part i.e hardware and other kinds of the
stuff is taken care of by the provider you are opting for i. e Amazon,
Rackspace, et al.

I had a struggle (and I am not ashamed of it, because it helps me to learn
what ware not on my radar), that while moving to the cloud I had a horrid time,
indeed. I still (sometimes) failed to understand the terminology people are
trying to describe something. Let me give you an instance, where I got confused.

I get into an environment where the cloud is a "mantra" and a team working
exclusively on clouds and I keep hearing from them many times in a day the word
*HA* for building the project they are working on.  I was excited; building HA for
anything is very exciting, indeed. One day I was overly curious and ask one of
them; what is this fuss all about HA? Where is heartbeat (the software) and how it
has been configured? But boy!, what I came to know is that they are simply building
those in two different places and using the feature of AWS auto-scaling.

Kinda disappointed solely because my conventional mind jumps into
building a conventional way of building HA, heck...

I had the good fortune to work for a pretty big and good name IT giant for some
time and I saw it all. I still remember the first day; I went into DC with my
manager, and I was awe-struck to see thousand of the physical boxes in different
shapes (one of the shapes dominating although) and sizes.. oh boy! And the sound
and the chillness of the place!!

Now the downside. I was running some automation scripts which bother some
users; they complained to me "what is your problem?" I was a bit weary at that
time. Also, it was my fault for not taking consent from the person , who looks after
all that,taking the rein on my hand without having all the information is not a
good thing on my part. Anyway, learned the lesson quicker.

Working in 24/7 and 365 days schedule mar lot of your plan and commitment, but
one has to do. Once taken the responsibilities, you just can not bypass it, because
a lot of things might depend on your action. Basically, I meant to say, prepared
for the heads up very frequently and repetitive way and pull your socks all the
time; no respite.

General term: try to segregate the important thing from the masses. You can get
hold of them in time of urgency. Like, you should have information about; where
the DNS servers are located and where the NIS servers are located.You can add a
few more stuff which is absolutely critical for operation.

Last but not the least, but extremely important, you got to work with a bunch of
people like you; so try to mingle with them genuinely and make them feel happy
about you. Because they will be the ones who will save your ass when you will be
in distress.

Next article, I will discuss what /components/ are important to consider for
infrastructure.
