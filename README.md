Install [Composer](https://getcomposer.org/download/) by running the below commands

    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    php -r "if (hash_file('SHA384', 'composer-setup.php') === '55d6ead61b29c7bdee5cccfb50076874187bd9f21f65d8991d46ec5cc90518f447387fb9f76ebae1fbbacf329e583e30') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
    php composer-setup.php
    sudo cp composer.phar /usr/local/bin/
    php -r "unlink('composer-setup.php');"
    
Test installation by running.

    composer -v;

You should see a bunch of help info.

    php composer.phar create-project -n thom8/drupal8-vagrant:dev-php7 drupal && cd $_ && vagrant up;
    
This will take a while, you will have to enter your `sudo` password near the beginning.

    sudo pico /etc/hosts

Remove drupal directory

    rm -rf drupal
