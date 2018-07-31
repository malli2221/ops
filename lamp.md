Lamp setup  :

Lamp setup purpose first we need to install the Apache,Mysql,php setup.

Apache installation :

First update the ubuntu machine after that install the apache2 in the machine, after that set the global server name &quot;/etc/apache2/apache2.conf&quot; in this we have mention the machine ip address, after that restart the apache2 server.using that ip address we will get the apache2 in browser.

![au](https://github.com/malli2221/ops/blob/master/imgt/lamp1.png)

Install mysql :

once install apache after that install the mysql in that machine &quot;apt-get install mysql-server&quot; after that set that user name and password to that mysql server .

Install php:

Once install mysql after that install php in that machine using&quot;apt-get install php libapache2-mod-php php-mcrypt php-mysql&quot; after that edit file &quot;/etc/apache2/mods-enabled/dir.conf&quot; we have to change the

&lt;IfModule mod\_dir.c&gt;

    DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm

&lt;/IfModule&gt;

to

&lt;IfModule mod\_dir.c&gt;

    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm

&lt;/IfModule&gt;

after that go browser using ip address and 192.168.33.70/info.php hit we get the phppage in browser.

![au](https://github.com/malli2221/ops/blob/master/imgt/lamp2.png)

install wordpress:

 First download the wordpress after that enter into the wordpress,

after that create data base in mysql after that create user name and password given full premission to that user.

Enter that wordpress and enter this file &quot;wp-config.php&quot; here we need to set the database name and username and password save that file then using ipaddress and hit into browser we will get that wordpress page in the browser.

![au](https://github.com/malli2221/ops/blob/master/imgt/lamp4.png)
