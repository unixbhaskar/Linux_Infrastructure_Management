# Information Management

"Information Management" means keeping the information in an easily accessible format. Many company do it different manner. But, most of the good companies do it incorrectly manner. There must be some sort of uniform way to manage information.

I am a huge fan of a Wiki and try to one if it is missing from the existing framework. It will keep the team of projects on the same page for everyone. Wiki can be maintained in such a fashion that, it would be easy to read and interpret the information. And not to forgot that during the crucial time the information should be available at ease.

So, first thing first, installing Wiki is pretty easy as compared to other things. I have had done it, so I am going to share it with you. I have a deal with a wiki called "DokuWiki" and it's pretty easy and fast to set it up and maintain.

You need to go here [https://www.dokuwiki.org/dokuwiki] and pull the download from here and follow the instruction on the same page on the left to install it and manage it.

Otherwise, do it by a script (I did it in that fashion) although the version has changed (and you need to change the below script), like this :

```
#!/bin/bash

# An attempt to automatize packaging DokuWiki for openSUSE

  RELEASE='2009-02-14'
  NEWNAME=$(echo "$RELEASE" | tr '-' '.')
  WORKDIR='/home/bhaskar'
   NO_OF_COMP=5
  WWWDIR="$WORKDIR"

#  mkdir -p "$WORKDIR/dokuwiki/etc/apache2/conf.d"
#  mkdir -p "$WWWDIR"

    # assume the standard download location
    DLFROM='http://www.splitbrain.org/_media/projects/dokuwiki'
    DLFILE="dokuwiki-${RELEASE}.tgz"
    # and get the file
    wget -O "${WWWDIR}/dokuwiki.tgz" "${DLFROM}/${DLFILE}"

     # unpack it
  #   echo "getting into the web space"
  #   cd "$WWWDIR" || exit 17
  #   echo "extracting the file..."
  #   tar -xzf "dokuwiki.tgz"
  #   echo " remove the source..."
  #   rm "dokuwiki.tgz"

      # move it into the right place, create config dirs
   #   echo " Moving it into the right place"
   #   mv "dokuwiki-${RELEASE}" dokuwiki
   #   HTACCESSLIST=$(find "${WWWDIR}/dokuwiki" -name '\.htacc*')
   #   cd "$WORKDIR/dokuwiki/etc" || exit 18
   #   echo " creating an symbolic link for that dir"
   #   ln -s ../srv/www/htdocs/dokuwiki/conf DokuWiki

       # write config for Apache
       # delete .htaccess, move it into Apache's conf
    #   echo " delete htaccess file and move it to apache conf"
    #   cat » 'apache2/conf.d/DokuWiki.conf' ««EOT
    #   Alias /dokuwiki "/srv/www/htdocs/dokuwiki"

# «Directory "/srv/www/htdocs/dokuwiki/"»
#     Options None
#         «IfModule mod_dir.c»
#         DirectoryIndex doku.php index.html index.htm
#     «/IfModule»
#         AllowOverride All
#     Order allow,deny
#         Allow from all
# «/Directory»
#
# EOT
# for SUBDIR in $HTACCESSLIST; do
# RELDIR=${SUBDIR#${WORKDIR}/dokuwiki}
# RELDIR=${RELDIR%/.htacc*}
# echo "«Directory \"$RELDIR\"»" »» 'apache2/conf.d/DokuWiki.conf'
# cat "$SUBDIR" »» 'apache2/conf.d/DokuWiki.conf'
# echo "«/Directory»" »» 'apache2/conf.d/DokuWiki.conf'
# echo " " »» 'apache2/conf.d/DokuWiki.conf'
# rm "$SUBDIR"
# done
# dos2unix -o 'apache2/conf.d/DokuWiki.conf'
#
#
# cd "$WORKDIR" || exit 19
# tar --strip-components=$NO_OF_COMP -cf "dokuwiki-${NEWNAME}.tar" dokuwiki
# gzip "dokuwiki-${NEWNAME}.tar"

``````

That's it!. This will do all the things require to install in the system. Then you are supposed to access the web UI and adding pages according to the wiki-style and keep it updated. Then, share the URL to everyone to read it, but allow or restrict only designated people to update it. Because it might play a huge role to maintain the infrastructure.

For instance, you might have solved a critical problem in the infrastructure, but you failed to document it in a proper manner then you will be in trouble( because similar kind of problem come to infra management very often, and if the gap is more, then chances are high that you might forget that solution..irk), so not to befall in that trap, a better way to put that solution in the wiki, so in time it can get fetched from it to resolve the problem in quick time.

Another case, say, you might be doing something very important to the infrastructure, and probably with a team, and in the team, not everyone has got the same wavelength(you have to understand it), so it might get screwed up the quick time by somebody's mistake. Then you might get back to the pristine state by the look at the road map for that particular project.

Do not trust anyone ..always validate ..where the information coming and how they are coming and who is providing that! If you do; you have a safe bet. But still, we falter ...to humans is err.

Okay, we might take advantage of several open-source tool to keep the things in place and available in time. Like, Trac and other custom have grown KB.

Next, we will discuss problem management related to infrastructure management.

