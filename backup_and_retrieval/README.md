# Backup and Retrieval

It would be of utmost importance to understand the impact of this activity i.e. backup. We used to have specific software related to that (good old days!), and which will run at a specific time (generally midnight) to get the backup of a specified activity. Say, we want to take a backup of some application running on the specific box or we want to take the snapshot of a specific image of the specific box. Nowadays, it is become even easier, with respect to cloud computing space it is just a matter of click!

Likewise, we will get it back i.e. retrieval, when things go wrong or people dependent of specific things get back the old form.

On the GNU/Linux system plethora of backup and retrieval systems available. Not only that even the service or application-specific backup can be done and retrieve with the tools come along built into the software. For instance, what is the most common way to take MySQL(MariaDB) dump by simply running mysqldump on a specific database, you wish to take a dump. Likewise, if you are interested to take backup of any specific LVM thing, then you might consider looking into the LVM snapshot feature. If you are exposed to AWS then those features are just a matter of clicks.

I have seen those big silos box in one of the famous IT organization's DC, probably in older days, other companies had too. Where all the tapes reside and at the end of the day all the tapes have to be a move to off-site, which means a safe place as per the policy. Not only that, but I have also had the experience to see that daily backup in cdrom and put into safe in some off-site (tiny organization). The bigger the infrastructure the bigger plan has to be rolled out for this kind of activity and the window should be large enough.

It's not just about taking backups, it is also essential to validate it before putting into a safe place or off-site. By not doing that, I have had come across a situation where backups had been taken but not verified, and when the bell rings, we found out that those backups got corrupted and we have nowhere to go..o heck. Nowadays I believe all the software responsible to do involve in that kind of job, will build into that feature in it. So, we can breathe easily while retrieval the backup on an emergency.

Okay, as I had worked with a really tiny organization were some costly or proprietary backup tool was a real luxury to have. They did use the built-in tool that comes along with a specific flavor of Linux they were using or get something that is free. Yep, a lot of smart people are there in an open-source world who writes and even smarter ones who build and deploy those.

Different industries work in different ways. I mean they deploy workaround strategy to deal with it. I have been to different industry and I have seen quite a few, none match with others, but they all do the same work with different tools. Even the rsync ran overnight to get the content from one server to another!!

