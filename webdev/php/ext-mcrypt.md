# MCrypt Extension Enabling

#### 1. Checking Extension Loading

    $ php -m

Check to see if mcrypt extension is listed.

#### 2. Checking php.ini file

    $ php --ini

Check where the command line is loading your php.ini. In this file you can enable the extension.

#### 3. Checking mods-available folder

On earlier versions of Ubuntu (prior to 14.04) when you run sudo apt-get install php5-mcrypt it doesn't actually install the extension into the mods-available. You'll need to symlink it.

    # ln -s /etc/php5/conf.d/mcrypt.ini /etc/php5/mods-available/mcrypt.ini

On all Ubuntu versions you'll need to enable the mod once it's installed.

    # php5enmod mcrypt
    # service apache2 restart
