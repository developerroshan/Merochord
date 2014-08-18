Merochord.com
=======================

Introduction
------------
This is simple chord, lyrics and tabs sharing forum. As its name suggests,
its my effort to open source code behind Merochord.com and so anyone is 
welcome to make contribution. 

It is based on ZF2 and uses several other submodules designed by others.

Installation
------------

Using Composer (recommended)
----------------------------
The recommended way to get a working copy of this project is to clone the repository
and use `composer` to install dependencies 

Alternately, clone the repository and manually invoke `composer` using the shipped
`composer.phar`:

    cd my/project/dir
    git clone git://github.com/developerroshan/Merochord.git
    cd ZendSkeletonApplication
    php composer.phar self-update
    php composer.phar install

(The `self-update` directive is to ensure you have an up-to-date `composer.phar`
available.)

Web Server Setup
----------------

### Apache Setup

To setup apache, setup a virtual host to point to the public_html/ directory of the
project and you should be ready to go! It should look something like below:

    <VirtualHost *:80>
        ServerName merochord.localhost
        DocumentRoot /path/to/zf2-tutorial/public
        SetEnv APPLICATION_ENV "development"
        <Directory /path/to/merochord/public_html>
            DirectoryIndex index.php
            AllowOverride All
            Order allow,deny
            Allow from all
        </Directory>
    </VirtualHost>
