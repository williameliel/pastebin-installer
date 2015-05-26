
#Pastebin WP automated installation process, installs Wordpress with custom directory
Download or Clone, change permissions to execute and run for ultimate WP installation experience.
#Get latest Wordpress
wget http://wordpress.org/latest.tar.gz && tar xfz latest.tar.gz && rm -f latest.tar.gz
#Create custom /wp directory structure
mv wordpress wp
cp -r wp/wp-content content
cd content/themes 
#Copy pastebin theme
git clone https://swnyc.git.beanstalkapp.com/pastebin-2.git pastebin 
cd pastebin 
# get custom wp-config and htaccess & other files to wp root
mv core/index.php  ../../../
mv wp-config.php ../../../
mv local-config.php ../../../
mv .htaccess ../../../
mv manifest.webapp ../../../
mv *.txt ../../../
mv crossdomain.xml ../../../
rm -rf .git* 
echo "-*- Done -*-"