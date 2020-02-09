# Installing-Composer-on-Mac-OSX
Installing Composer Globally on Mac OSX Step by Step Tutorial

In this guide, i'm installing Composer on a machine running Mac OSX

1. Open a terminal and navigate to your user directory, 
```bash
 cd /User/<USER_NAME>/
```

2. Run this command shown below to download Composer. This will create a Phar (PHP Archive) file called composer.phar:
```bash
   curl -sS https://getcomposer.org/installer | php
```

3. Now we move composer.phar file to a directory.
```bash
    sudo mv composer.phar /usr/local/bin/
```

4. If you get the following error (# /usr/local/bin/composer.phar: No such file or directory error on mac).
```bash
    cd /usr/local/
```
```bash
   mkdir bin
```

5. and then go back to the.
```bash
   cd /User/<USER_NAME>/
```

6. Run the following command from terminal.
```bash
   sudo mv composer.phar /usr/local/bin/
```

7. We want to run Composer with having to be root al the time, so we need to change the permissions:
```bash
    sudo chmod 755 /usr/local/bin/composer.phar
```

8. Next, we need to let Bash know where to execute Composer:
```bash
   nano ~/.bash_profile
```

9. Add this line below to bash_profile and save
 
```bash
alias composer="php /usr/local/bin/composer.phar"
```

10. and then run this command:
 ```bash
   source ~/.bash_profile
```
 
11. Finally, run:
```bash
   composer
```
