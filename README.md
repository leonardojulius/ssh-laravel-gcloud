# ssh-laravel-gcloud

1.Create Compute Engine Instance
2.Generate ssh-keygen -t rsa  -C "username on SSH terminal"
  -prompt for the file name " Will be save at home folder"
  -local ssh file on terminal "cat file.pub"
  -copy then proceed to 3.
3.after being generated add on Compute Engine SSH click enable

on visual studio code ssh config 

Host Connection Name
    HostName Ip.Address.com
    User userNameCanbeFoundSShTermanilCloud
    IdentityFile ~/.ssh/file(private not public)
    
Now Connect
    
    Error 500 internal Server
    
    sudo chmod -R 755 laravel_blog(project Name)
    sudo chmod -R o+w laravel_blog/storage
    

Create the .env file and also run :

php artisan key:generate

This worked for me after pulling a git project.

After creating .env file and generating the key, run the code below:

php artisan cache:clear 
php artisan config:clear


    
    
Apache .htaccess public access


cd /etc/apache2/mods-enabled/

If it does not exist execute the following excerpt:

sudo a2enmod rewrite

Otherwise, change the Apache configuration file to consolidate use of the "friendly URL".

sudo nano /etc/apache2/apache2.conf

Find the following code inside the editor:

<Directory /var/www/> 
   Options Indexes FollowSymLinks
   AllowOverride None
   Require all granted
</Directory> 

Change to:

<Directory /var/www/> 
    Options Indexes FollowSymLinks
    AllowOverride All
    Require all granted
</Directory>

////

htaccess

<IfModule mod_rewrite.c>
    <IfModule mod_negotiation.c>
        Options -MultiViews
    </IfModule>

    RewriteEngine On

    RewriteCond %{REQUEST_FILENAME} -d [OR]
    RewriteCond %{REQUEST_FILENAME} -f
    RewriteRule ^ ^$1 [N]

    RewriteCond %{REQUEST_URI} (\.\w+$) [NC]
    RewriteRule ^(.*)$ public/$1 

    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^ server.php
</IfModule>

