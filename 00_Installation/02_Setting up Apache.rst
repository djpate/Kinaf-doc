Setting up Apache
-----------------

In the newly created project the only directory that Apache needs to have acces to is the public directory.

Make sure that you have enabled the rewrite module

::

    a2enmod rewrite
    /etc/init.d/apache restart
    
Then create a virtual host in order to test Kinaf.

If you dont know how to setup a virtualhost you can follow this little tutorial

Start by adding an alias in your host file

::

    nano /etc/hosts
    
Then edit the line starting with 127.0.0.1 and add myProject.localhost

It should look like this

::

    127.0.0.1 computername myProject.localhost
    
now let's add a vhost to apache

::

    nano /etc/apache2/sites-available/myProject

Here is an example vhost config file

::

    <VirtualHost *:80>
        ServerName myProject.localhost
        DocumentRoot /var/www/myProject/public
    </VirtualHost>
    
Now add the vhost to apache

::

    a2ensite myProject
    /etc/init.d/apache2 restart

Once this is setup you should see a basic Welcome to Kinaf homepage

**Congratulations you are ready to go !**
