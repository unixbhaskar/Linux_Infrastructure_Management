 # Basic understanding of Infrastructure

Understanding the environment for work is an utmost need for any person to work on the infrastructure domain.

For instance, whether it is a normal physical infra or based on the cloud. There is a need for a certain mind shift for working in two different environments.

THE traditional DC environment is different than the "virtual Data Center" environment. Things are  different

I have had been to the physical data center and virtual data center too. Operating is an undertaking in both the places (yep! You guessed it right, my lack of bend of mind), but somehow I float by on both the environment without much hassle.

In the physical data center, you need to interact with iron boxes, watch out for the cables, configure the rack console and check for the lights on the front and back of the server and take some decision based out of that!!.

While in the virtual data center, you are not so fortunate about seeing those, but the software makes it simulated for those missing part, sometimes it missed and sometimes it hits, depend on how the software configured and which software it is (there are a plethora of that kind of software available in the market, open and closed both).

Because virtualization arrived late (although it was there for a long time and people ignored it and hardware support was minimal, so never get kick-off) and things have changed, people get more aware of the capabilities, started to take advantage of it.

"Cost-cutting" is mandatory (buzzword????) in any IT organization's portfolio these days and they reap benefit out of it, by opting for virtualization. But, still, some important and mission-critical thing runs on a physical place. And I love it; nothing like seeing an iron box in front of you ..so you can view it with your x-ray eyes and touch it.

Sometimes I feel (absolutely my personal opinion), that the virtual environment is a little bit fragile than the physical one; probably I came from a normal DC environment to VDC environment that is why. I didn't mean to say it is inferior or bad, but it has many more ways to fail than the physical environment.

Anyway, being in infra management, you have to be well conversant with both the environment. No other go, simple. Period.

Yes, one thing is very clear that you bound to be leaner on software to manage the data center because the underlying part i.e hardware and other kinds of stuff are taken care of by the provider you are opting for i. e Amazon, Rackspace, et al.

I had had a struggle (and I am not ashamed of it) that while moving to cloud I had a horrid time, indeed. I still (sometimes) failed to understand the terminology people are trying to describe something. Let me give you an instance, where I got confused.

I get into an environment where the cloud is "mantra" and one of team or guy working on two things, one proxy and second Nagios. I keep hearing from the people sitting close to me the HA word for both!!  I was excited; building HA for anything is very exciting, indeed. One day I was overly curious and ask one of them; what this fuss all about HA? Where is heartbeat (the software) and how it has been configured? But boy!, what I came to know that they are simply building those in two different places and using the feature of AWS auto-scaling.

I am not sure, what will be the outcome; but my conventional mind jumps into building a conventional way of building HA, heck...

I had the good fortune to work for a pretty big and good name IT giant for some time and I saw it all. I still remember the first day; I went into DC with my manager, and I was awe-struck to see thousand of the physical boxes in different shapes (one of the shapes dominating although) and size.. a boy and the sound and the chillness of the place!!

Oh did I see those so-called "big shots" during scheduled downtime? Those who refrain showing up all the time in the year and send some chilled and awful emails to the person down the lines, amazing persons those are, heck.

Managing geographically distributed DC or working in it is a daunting task. Especially when you are working in pretty low (o yeah not in that "big shot" role), because a lot of things get hidden from you. The reason behind exactly two: you are not in the "big shot" level to know everything, forget about accessing and seeing. Second, you have been constantly told "do not assume anything"; how come? I think those who said that seriously deserve a **f**  word. Can't help.

Now the downside. I was running some automation script and which bother some users; they  complained to me "what is your problem?" I was a bit weary at that time.

Working in 24/7 and 365 days schedule mar lot of your plan and commitment, but has to do. Once taken the responsibilities, you just can not bypass it, because a lot of things might depend on your action. Basically, I meant to say,  prepared for the heads up very frequent and repetitive way and pull your socks all the time; no respite.

General term: try to segregate the important thing from the masses. You can get hold of them in time of urgency. Like, you should have information about; where the DNS servers are located and where the NIS servers are located.

Last but not the least, you got to work with a team of people like you; so try to mingle with them genuinely and make them feel happy about you. Because they will be the ones who will save your ass when you will be in distress.

Okay, enough chit chat; let us fasten your seat belt for the ride.




