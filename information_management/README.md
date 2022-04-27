#+title: Linux Infrastructure Management Part-III
#+date: 2022-04-28
#+tags: Technical

* *Information Management*

*/"Information Management"/* means keeping the information in an easily accessible
format. Many companies do it different manner. There must be some sort of
uniform way to manage information.

Oh BTW ,in case if you missed the first two parts of this series , here they are :
[[https://unixbhaskar.wordpress.com/2022/04/26/linux-infrastructure-management-part-i/][Part-One]]  and [[https://unixbhaskar.wordpress.com/2022/04/27/linux-infrastructure-management-part-ii/][Part-Two]] .

I am a huge fan of *Wiki* and install one if it is missing from the existing
framework. It will keep the team on the same page like everyone. Wiki can be
maintained in such a fashion that, it would be easy to read and interpret the
information. And not to forgot that during the crucial time the information
should be available at ease.

So, first thing first, installing Wiki is pretty easy as compared to other
things. I have done it, so I am going to share it with you. I like the way
*/DokuWiki/* handle the information ,so that would be my choice. It all depends on
how many people are convenient with it ,so we can opt for it . We need to think
about its maintenance too.The more people know about it the better. You need to
go here [[https://www.dokuwiki.org/dokuwiki][Dokuwiki]] and pull the download from here and follow the instruction on
the same page on the left to install it and manage it.

Having a home grown */Knowledgebase/* is extremely important for the people who
delve with infrastructure. Because ,it helps to make thing quickly
resolvable.And there would a standard place in the infra to look for the
solutions.

I have an inclination to have something /internal/ and necessarily not connected to
internet or need internet to fetch the piece. That means, freely accessible
within the concern and it is very common. Although ,nowadays companies put lots
of docs on the internet for public consumption , but certainly not this kind of
operational stuff. And it might not be useful either, because everyone operate
in different way.

Once you installed the system in place then you are supposed to access the web
UI and adding pages according to the wiki-style and keep it updated. Then, share
the URL to everyone to read it, but allow or restrict only designated people to
update it. Because it might play a huge role to maintain the infrastructure.

For instance, you might have solved a critical problem in the infrastructure,
but you failed to document it in a proper manner then you will be in trouble(
because similar kind of problem come to infra management very often, and if the
gap is more, then chances are high that you might forget that solution..irk), so
not to befall in that trap, a better way to put that solution in the wiki, so in
time it can get fetched from it to resolve the problem in quick time.

Another case, say, you might be doing something very important to the
infrastructure, and probably with a team, and in the team, not everyone has got
the same wavelength(you have to understand it), so it might get screwed up the
quick time by somebody's mistake. Then you might get back to the pristine state
by the look at the road map for that particular project.

Do not trust anyone ..always validate ..where the information coming and how
they are coming and who is providing that! If you do; you have a safe bet. But
still, we falter ...to humans is err.

Okay, we might take advantage of several open-source tool to keep the things in
place and available in time. Like, Trac and other custom have grown KB.

Next, we will discuss problem management related to infrastructure management.
