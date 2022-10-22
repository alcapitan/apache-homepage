# Apache Default Homepage

This is a default home page made for use with Apache.

## How to add my projects to the homepage ?

The method is archaic, but a modernization could take place.  
In the ```index.html``` file, copy this in the div.available element :   
```
<a href="http://localhost/my-project"> # Put the link of your project here
     <article class="project">
          <div class="icon">
               <img src="icon of your project"> # If it don't have an icon, writes "icons/default_icon.png". It should be a monochrome icon for consistency.
          </div>
          <div class="text">
               <p>Project Name</p>
               <em>Project description</em>
          </div>
     </article>
</a>
```
Then, edit the information according to your project.

## How to install it ?

### Windows

A contribution for the method of installation on Windows would be appreciated.

### Linux (debian-based)

```
sudo apt update && sudo apt install apache2 git
git clone https://github.com/alcapitan/apache-homepage.git
sudo mkdir -p /var/www/apache-homepage
sudo cp -r ./apache-homepage /var/www/apache-homepage
sudo cp /var/www/apache-homepage/apache-website-config-file.conf /etc/apache2/sites-available
sudo su -
cp /var/www/apache-homepage/apache-website-config-file.conf /etc/apache2/sites-available/001-apache-homepage.conf
a2dissite 000-default.conf
a2ensite 001-apache-homepage.conf
exit
```

Then, run a web browser and if you are lucky, this should be work.

