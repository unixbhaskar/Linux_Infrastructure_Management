# Basic understanding of Infrastructure

When we start working on something in the infra manage project, we need to understand the environment first to get into the grove.

For instance, whether it is a normal physical infra or based on cloud. There is a requirement of huge mind shift in working in two different environment.

Traditional DC environment is quite different then the "virtual Data Center" environment. Things are quite different.

I have had been to physical data center and virtual data center too. Operating is quite an undertaking in both the places (yep! you guessed it right, my lack of bend of mind) ,but somehow I float by on both the environment without much hassle.

Now in physical data center you need to interact with iron box ,see the cable, configure the rack console and check for the lights on the servers front and back and take some decision based out of that!!

While in the virtual data center you are not so fortunate about seeing those, but the softwares make it simulated for those missing part, sometime it missed and sometime it hits ,depend on how the software configured and which software it is (there are plethora of that kind of available in the market, open and closed both).

Because virtualization arrived late (although it was there for long time and people ignored it and hardware support were minimal, so never get kick off) and we started to take advantage of it.

"Cost cutting" is mandatory (buzzword????) word in any IT organization's portfolio these days and they reap benefit out of virtualization. But, still some important and mission critical thing runs on physical place .And I love it; nothing like seeing an iron box in front of you ..so you can view it with your x-ray eyes and touch it.

Sometime I feel (absolutely my personal opinion) that virtual environment are little bit fragile then the physical one; probably I came from a normal DC environment to VDC environment that is why. I didn't meant to say it is inferior or bad; but it has many more ways to fail then the physical environment.

Anyway, being in infra management you have to be well conversant with both the environment. No other go, simple. Period.

Yes, one thing is very clear that you abound to be more lean on software to manage data center, because the underlying part i.e hardware and other stuffs are taken care by the provider you are opting for i. e Amazon, Rackspace et al.

I had have struggle (and I am not ashamed of it) that while moving to cloud I had horrid time, indeed. I still (sometime) failed to understand the terminology there are trying to describe something. Let me give you an instance, where I got confused.

I get into an environment where cloud is "mantra" and one of team or guy working on two things ,one proxy and second nagios. I keep hearing from the people sitting close to me the HA word for both!! so I was excited; building HA for anything is very exciting, indeed. So, one day I was overly curious and ask one of them what this fuss all about HA; where is heartbeat (the software) and how it has been configured; but boy, what I came to know that they are simply building those in two different place and using the feature of AWS  autoscalling.

I am not sure, what will be the outcome; but my conventional mind jump into building conventional way of building HA, heck..

I had the good fortune to work for pretty big and good name IT giant for sometime and I saw it all. I still remember the first day I went into DC with my manager, and I was awe-struck to see thousand of physical box in different shape (one of the shape dominating although) and size.. boy and the sound and the chillness of the place!!

O did I see those so called "big shots" during yearly downtime? those who refrain show up all the time in the year and sent some chilled and awful emails to the person down the lines, amazing persons those are, heck.

Managing geographically distributed DC or working in it is a daunting task. Specially when you are working in pretty low (o yeah not in that "big shot" role), because lot of things get hide from you. Reason behind exactly two: you are not in the "big shot" level to know everything, forget about accessing and seeing. Second, you have been constantly told "do not assume anything"; how come? I think those who said ,seriously deserve a f***  word .Can't help.

Now the downside. I was running some automation script, and which bother some users; he complained to me "what is your problem"; I was bit weary that time.

Working in 24/7 and 365 days schedule mar lot of your plan and commitment, but has to do. Once taken the responsibilities you just can not bypass it, because lot of thing might depend on your action. So, basically I meant to say  prepared for the heads up very frequent and repetitive way and pull your socks all the time; no respite.

General term try to segregate the important thing from the masses. So you can get hold of them in time of urgency. Like ,you should have know and have enlisted somewhere in your notebook; where the dns servers are and where the NIS servers are.

Last but not the least, you got to work with a team of people like you; so try to mingle with them genuinely and make them feel happy about you. Because they will be the one who will save your arse when you will be in distress.

Okay, enough chit chat; lets fasten your sit belt for the ride.





