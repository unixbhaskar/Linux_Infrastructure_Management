# Things to consider

We are supposed to know the underlying infrastructure, I meant to say, how the servers are organized as a hardware basis and what is the network connection to those boxes. It seems it's a kinda mandatory thing to know about it to operate an inefficient manner.

Indeed, it plays an important role to know where are those boxes reside, for the cloud-related matter, it's good to know which zone it is in.

We have nowadays so many tools available to tell us the information about the underlying infra. In older days we used to write a script to get the low-level details to automate things,now the scope little less as more and more smart people design and architect tools to take the pain away from ordinary mundane people like us. And it helps immensely to spend your time doing the actual thing, rather wasting time to figure out where it is and how it works (yep to some extents; but still require some investigation and time to get into the gory details); but that is the curiosity part. A sensible infra person is hugely curious and conscious about what he or she is doing.

I, personally refrain from doing anything if I am not at least a major part of it clear to me. Because we all know how bad the "half-knowledge" is. A premature assumption can lead you to nowhere and create havoc. Why get into that situation, when you are open to operate it and abound to provide some result. No, I do not gauge people by the result; it sometimes misleads you. The approach, that will make all the difference in an open system (read GNU/Linux and related systems) will allow us to navigate deep down. Provided you are willing to spend time with it. Okay, let me contradict it by saying that, working in BU doesn't always bring you the luxury of time to get deep into it. I agree. But how about your personal time and knack towards it?? Does it take away by the job you are bound to do? If that is the case , then think about it to get on with it.

We should have an understanding of how the servers are built from the ground up. I mean getting to know the hardware specs i.e how many CPU cores?how much ram? How many NIC? What about the power supply? Which rack it is seated and what label on it? et al.

That information will help immensely. I had been to a situation, where I was asked to put the label on the iron box; for the cloud, you can tag it easily. Not only that, looking at the different light colors on the server panel gives you a hint about what is going on inside; although not necessarily that all the time it will do. You got to take into consideration the specific event you are working on.

Important note, nowadays everyone depends on Google and other search engines; I too benefited from that. But I grew up in a stage and era where the internet was not easily available to my country. I had lean on books (yes hardcover and paperback; I still prefer them!) and peers knowledge (you might be lucky enough to get a proper person to enhance your knowledge; a lot of factors involve it).

Taken the thing to your head by yourself. I did. I do. And it takes time( because I don't have a sharp bend of mind like you have), but once I get into it (which certainly has to interest me..at this age; not anymore to bound to do it situation); but doing it for the sake of love and discovery.

I am not very impressed with when I have seen people with some airy-fairy ideas, talk big and nonsense. Because I have had come across people who do practice that to gain attention but false vanity. How dare I say nonsense? Because, they just don't have any use case with them; putting ideas for the sake of doing it, nor they have any hands-on thing on that; that irks me a lot.

When you are not so lucky to know everything, like working with a cloud operator, you have to take a different route to get things done. And I sometimes get bemused by the fact the way things get done. Oversimplification is a curse in the cloud (or I have some mental block about it; need to figure out that). Lots of misnomer is floating out cloud place and it is very easy to get lost into it.

Why not take some time to read the spec and documentation about it then jump the gun and work on it? I had had stumble block about it. I decided to give it a shot and read through a large chunk of it( only that concern me; YMMV). And I believe I get a hold on a few portions of it solidly; thank god .. I did.

I have a serious problem with me from a long time; I can easily figure out whom to approach and whom not and what to listen and whatnot, most of the time and it not necessarily I had have come out with positive all the time, but most of the time I was benefited out of that approach. Now, how come I distinguish that person? Intuition and gut feeling (again YMMV).But having said that, I am not stuck with a particular method or rule( I hate it like anything), am pretty open to anything fruitful.

I like people who are on my face, and I like to be called an "idiot"; if that doesn't make sense to them whatever I propose or do. Because, by being told idiot or similar kind of thing, two things come out; the person is really caring about you and wanted you to improve (I have seen some skeptic, naysayers; they are just saying it out of their habit, and I can figure it out easily, and give them back what they deserve) and you will get chance to introspect about something you stopped thinking. It helps you to become much more stronger and efficient and respectful to those who care. And it also not allow you to live in an "illusionary bubble" anymore. That's good.

When you maintain stuff in a "low" level. But not mean real low level, but to mean at the hardware level, you are supposed to be good with the vendor. They can bail you out of a lot of hassle. I still remember opening up an IBM X series box and look into it excite me a lot. I was a plain watcher; my expert colleague was doing all the stuff at that time.

Physical networking is of utmost importance to work on the data center. I generally keep a patch cable in my laptop bag most of the time. And I have had seen big network experts with a lot of physical tools in the data center. Blinking light on the ethernet port is crucial. Sometimes, it does blink but you failed to understand why the hell server is not responding to the network query; the real thing needs to check a few more places to confirm.

DO NOT REBOOT the machine for a trivial reason, because it takes servers to boot a little more time (some time really good time) to get it back, because lots of things getting initialized while a server boots. Second, you can fix most of the network software related stuff on the console and bouncing the service. Yep, if you are having hard luck with the physical fault in the network, then chances are dooms for you. You need to get help from the network experts. I mentioned above, a person with lots of physical tools.

OR if you still do; without understanding the impact ..please make sure your CV updated and well circulated.

Everybody knows those facts,who has spend enough in the corporate environment. I personally almost did that kind of mistake once; fortunately, my reporting boss helps me to prohibit that. When you have a rack full of servers and no label on it; that might cause lots of trouble, in my case, it was almost happening for that reason.

Never run any automation script without prior permission of the person who in charge of it. I did. And I was castigated by the people to ruin their job on the machine, heck. Even if you are good enough on something still it requires you to be on top of it get the best out of it. I was not in that case. I made people's life miserable. And the important thing,  I took the lesson in a positive way. I wasn't vigilant or informed enough to do such kind of thing in that environment. It's not about running what you know; it's all about how you run and why you run.

Cover your arse too! People get less chance to get on you. By saying that, whatever you do should have some checkpoints and mail related to that. And perhaps the doc related to that. In case of question raised by some "black suit wearing" person, you can readily refer to that.

Linux...Linux...Linux... All I have had care all throughout my endeavor and cared less other stuff (purely because of lack of bend of mind and time to think about others, but that does not include open-source...).I believe thinking in a singular fashion sometimes helps you to achieve more than think a multi-dimensional way. At least it helps me confined within one domain and helps me to grow. But you can stick to whatever interests you. In this book, I will solely focus on GNU/Linux; because that the thing I am living with for a long time. I love it; I hate it; I embrace it; I proliferate it; I endowed it, the list can go on and on. Whatever I learn using it over a decade and exposed to different environments doing different activities.

O BTW, managing an experience NOC team and DevOps demand a little bit more enhanced version of yourself. I have had learned it hard way; yep indeed. Managing some egoistic human is certainly not fun. Machines are good, they do what I want; but humans are blessed with EGO and that is predominant in most of us, time to time came out. But, for some people it is always the way forward; heck,hey seriously deserve a kick on their arse; sorry no other go.

Okay, "Your manager is always right", is that so?? I don't believe it. The only thing that separates you from your manager is exposed to more information about related matters. He/She might have gained it by some other means then she/he can, but still he/she is ahead of you. Respect them on that count. And make sure you extract out what you need from them. Most of them talk loads of rubbish; so put a filter on their verdict. They bring past events of their story into the present by forgetting that this is now different.

No, I am not saying disrespect them, give them the due they deserve. Moreover, who wants the story; give me your code I will figure it out myself; I don't need your past story. Never say that on their face, react like that! So next time they will be cautious enough to take you on. Am I ranting against the managers?? A big NO. Reread the above paragraph again. I just point out the truth and what you should do. There are lots of good and I mean genuinely good people around, who is manager, it just a tiny bit of luck you need to get bumped onto them. But, alas! You will find the bad one are outnumbered the good one; indeed. Keep your finger crossed for that and stop listening to stories.

Get yourself enough chance to fail. By acquiring more knowledge and work. Please make a mistake and learn from it. Get into a discussion on the IRC channel( to meet some rude guys) and in some forums (where most of the time half-cooked information shared!! Except two places, Gentoo forum, and Arch Linux forum), and I really like those places; people are so explicit and to the point for problem-solving and they expect people come there to be explicit and clear. Am I biased? No, I am not. I personally run 13 different GNU/Linux distribution in my laptop for a long time and I have been to most the forums related to those. I know which is what.

Now, the more information you gather by any means (from your manager or by interacting with knowledgeable colleagues), the more chance you can get over quickly with the obstacle.

Read ,read ,read and practice ..practice ,practice; no substitution for those. I do. I am not going to give a lecture on that. I learned it by that fashion. Investing in good books can benefit you in the long run. I personally have around close to 100 UNIX/Linux books on my shelve (at least went through them twice), not for the sake of collecting books and counting in the league but to explore and know more. Nowadays it's become even more possible and easy.

We are in a field that is constantly changing and progressing. Moreover, it is cognitive science, so the more we armed with knowledge, the more we can thrive. Now, there is a catch. Because of google, everybody becomes experts (I have come across a few; O Hell!), a lot of information is not worth it. You need to identify which is required and which one needs to be discarded. At least I have limited space my gray cell, so I discard a lot, keeping only those which will help me deduce something related I am doing /will be doing very soon. It is certainly not an easy job, doing so needs some sort of concentration , like the way we configure software in the servers. One silly mistake and you are in a position to miss the information for good. Sometime it might be costly to miss those. And we do miss those. After all, we are human. To humans is err.

Cloud...OMG cloud!!!... did I mentioned that I struggled with it initially? Yes, I had a torrid time with the terminology used by the expert cloud infra folks. Okay, somehow now I can get hold on it ...although not completely. Cloud has a magnificent upside and equally has a wonderful downside too. If you are opting for it, then you need to embrace both by your hand.

It will take away the overhead of maintaining the physical data center and related stuff, like cooling, personnel et al. And it can spin up a server in a very quick time, so the downtime goes for a toss.  the cons, you loose little control over the hardware and networking stuff, which sometimes not good. You will be dependent on others to provide you the underlying infra. One predominant misconception in people's heads is that the cloud is cheap. NO, it is not. Period. You got to pay for every little thing, which might accumulate exceed your budget long run.

There are lots of players for the cloud in the market, few of the renowned ones are OpenStack, cloudstack , Eucalyptus, OpenNebula.They offer services according to their strength. But, all of them are basically good. Do not forget AWS, they are the front runner in that space. Most of them support the AWS API to get the inter-operability.

 Gets your hands dirty with it (more on that later) will certainly help you to excel in this field. I don't know I always prefer the CLI way of doing things, probably it stuck with me from the beginning. If and only if necessary then only I can fall back on GUI. O BTW you can use ncurses based UI on the terminal itself. And there are many tools that are available to do the required job. In fact, renowned distributions supply the tui version of GUI, that is a good part. Because we will be working most of the time in a headless environment (headless in server term, no X11 or GUI related stuff installed, security measure). So, get yourself accustomed to the CLI, it certainly helps; moreover, it is much faster than GUI (when invoked, it will bring along a plethora of things along with it, in turn, more time to get work ). Try yourself running a GUI app from the terminal, you can only see what is going on behind the scene. When you operate on a server, you just can not afford that clutter your terminal, if you suppress that too, why bother invoking that, when you have an alternative  available, which is much more lightweight.

Now, when you choose your OS, give it a thought that, are you going for 32bit (almost nobody using it now) and opt for 64bit. The architecture is almost similar to a little tweak. And more space in address bus and data bus. Calling to the system call return faster. There is no visual difference between 32bit and 64bit apart from the naming convention to the /lib directory. But, internally it might play huge, as I mentioned briefly in the above. Moreover, you are giving yourself more chance to embrace with current proceeding in the hardware front, which in turn help the server to take advantage of the underlying technological advancement.

And what more? I think I have given enough details above for the heads up.

Let's get into more technical details in the next chapter.










