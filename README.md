#Vagrant PHP Development setup


## Installation
####This setup is based and tested with Ubuntu Precise 64 bit base box, with Vagrant 1.0.5 version (should be working with 1.1)

* Install Vagrant using using the [installation instructions](http://docs.vagrantup.com/v2/installation/index.html)

* If you are on Windows OS install NFS support plugin [more information and detailed installation instructions](https://github.com/GM-Alex/vagrant-winnfsd):
    ```vagrant plugin install vagrant-winnfsd```

* Clone this repository

    ```$ git clone https://github.com/tbergeron/vagrant-php.git```
    
* install git submodules
    ```$ git submodule update --init```

* run vagrant (for the first time it should take up to 10-15 min)
    ```$ vagrant up```
    
* Web server is accessible with http://13.37.13.37 (IP address can be changed in Vagrantfile)

* PhpMyAdmin is accessible with http://13.37.13.37/phpmyadmin

* Vagrant automatically setups database with this setup:

    * Username: developer
    * Password: password
    * Database: developer

## Installed components

* [Nginx](http://nginx.org/en/) using puppet module from [example42](https://github.com/example42/puppet-nginx)
* [MySQL](http://www.mysql.com/) using puppet module from [example42](https://github.com/example42/puppet-mysql)
* [PHP-FPM](http://php-fpm.org/) (PHP 5.4)
* [PhpMyAdmin](http://www.phpmyadmin.net/home_page/index.php)
* [Redis](http://redis.io/)
* [Git](http://git-scm.com/)
* [Composer](http://getcomposer.org) installed globaly (use ```$ composer self-update``` to get the newest version)
* [PEAR](http://pear.php.net/)
* [cURL](http://curl.haxx.se/)
* [Imagic](http://www.imagemagick.org/script/index.php)

## Thanks to

* [example42](https://github.com/example42) - for great nginx\mysql templates
* [caramba1337](https://github.com/caramba1337) - for great ideas
* [kertz](https://github.com/kertz) - for great ideas
* [Markus Fischer](https://github.com/mfn) - for contribution
* [Gustavo Schirmer](https://github.com/hurrycaner) - for contribution

## Hints
####Startup speed
To speed up the startup process use ```$ vagrant up --no-provision``` (thanks to [caramba1337](https://github.com/caramba1337))