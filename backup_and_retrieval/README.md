# Backup and Retrieval

It would be an utmost important to understand the impact of this activity i.e. backup .We used to have specific software related to that(good old days!) ,and which will run at specific time (generally midnight) to get the backup of specified activity.Say, we want to take a backup of some application running on the specific box or we want to take the snapshot of specific image of the specific box.Nowadays ,it is become even easier ,with respect to cloud computing space it is just a matter of click!

Likewise ,we will get it back i.e. retrieval ,when things goes wrong or people dependent of specific thing get back the old form.

On GNU/Linux system plethora of backup and retrieval systems available.Not only that even the service or application specific backup can be done and retrieve with the tool come along built into the software. For instance,what is the most common way to take mysql(mariadb) dump by simply running mysqldump on specific database,you wish to take dump.Likewise,if you are interested to take backup of any specific lvm thing ,then you might consider about look into lvm snapshot feature.If you are exposed to AWS then those features are just a matter of clicks.

I have seen those big silos box in one of the famous IT organization DC,probably in older days other companies had too.Where all the tapes reside and at the end of the day all the tapes has to be move to off-site ,means safe place as per the policy.Not only that,I have had the experience to see that daily backup in cdrom and put into safe in some off-site(tiny organization).The bigger the infrastructure the bigger plan has to be roll out for this kind of activity and the window should be large enough.

It's not just about taking backups,it is also essential to validate it before putting into safe place or off-site.By not doing that ,I have had come across a situation where backups had been taken but not varified,and when the bell rings ,we found out that those backups got corrupted and we have nowhere to go..o heck.Nowadays I believe all the software responsible to do involve in that kind of job,will built into that feature in it.So,we can breathe easy while retrieval the backup on emergency.

Okay,as I had work with really tiny organization where some costly or proprietory backup tool was real luxury to have.They did use the built in tool comes along with specific flavour of linux they were using or get something which is free.Yep,lot of smart people are there in open source world who writes and even smarter one who build and deploy those.

Different industry work different way.I mean they deploy workaround strategy to deal with it.I have been to different industry and I have seen quite a few,none match with other, but they all do the same work with different tools.Even the rsync ran overnight to get the content from one server to another!!
