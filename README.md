Command-line installation
To quickly install Composer in the current directory, run the following script in your terminal. To automate the installation, use the guide on installing Composer programmatically.

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
This installer script will simply check some php.ini settings, warn you if they are set incorrectly, and then download the latest composer.phar in the current directory. The 4 lines above will, in order:

Download the installer to the current directory
Verify the installer SHA-384, which you can also cross-check here
Run the installer
Remove the installer
Most likely, you want to put the composer.phar into a directory on your PATH, so you can simply call composer from any directory (Global install), using for example:

sudo mv composer.phar /usr/local/bin/composer
For details, see the instructions on how to install Composer globally.
