# Bandit

The Bandit wargame is aimed at absolute beginners. 
It will teach the basics needed to be able to play other wargames




# I am sharing my experience regarding bandit

I started the bandit server by writing

# "ssh bandit@bandit.labs.overthewire.org -p 2220"

Level 0 to 1:

Then after this it asked me password which was bandit0 then after this I used ls so their I found a readme file by the help of cat I opened it and then I found password for next level(level 1) from here.

     PASSWORD : bandit0

Level 1 to 2:

Then after this I exit it then again i called the server by "ssh bandit1@bandit.labs.overthewire.org -p 2220" by this I opened my level 1 and the entered the above accessed password.Then here also by the help of ls i found a file "-" here so I opened it by the help of cat ~./- and get the password of next level.

     PASSWORD : bandit1 = CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Level 2 to 3:

Again I exited and recalled the server by above commands just replacing 1 by 2 and then I entered the above accessed password in this then I got a file named as "spaces in this filename" I open this file by "cat spaces\ in\ this\ filename" and I again got the password and then i exited and recalled the server by entering the password.

     PASSWORD : bandit2 = UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Level 3 to 4:

In this level after entering the password there is inhere directory in which there is hidden file so I just used "ls -la" then by this get to know that there is .hidden file so I just opened it by ""cat .hidden" in this way I found the password for the next level.

     PASSWORD : bandit3 = pIwrPrtPN36QITSp3EQaw936yaFoFgAB

Level 4 to 5:

Again their is a inhere directory, as in this level we can get the password which is stored in a human readable file so first for getting the ASCII file i write the command "du -h | file ./ "* then by this we get to know that the human readable file is -file07 so for getting the password I write the command as "cat ./-file07".

     PASSWORD : bandit4 = koReBOKuIDDepwhWk7jZC0RTdopnAYKh
     
Level 5 to 6:

And by entering the ls I got a directory named as inhere in which I have to find a file which is human readable and of size 1033 and it is not executable. Then I found that how to acess the file which has 1033c using file -size 1033c. Then I got the file name which has the file size 1033c was showing ./maybehere07/.file2 . Then I opened the file and got the password.
So in this way got level 5 and entered into level 6.

     PASSWORD : DXjZPULLxYr17uwoI01bNLQbtFemEgo7
     
Level 6 to 7:

In this level the password is stored somewhere in the server but we have certain information like it was owned by bandit7 owned by group bandit6 and its size is 33 bytes so by all these informations I write the command "find / -user bandit7 -group bandit6 -size 33c" by this way I found the file and access it by "cat /var/lib/dpkg/info/bandit7.password"

     PASSWORD : HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

Level 7 to 8:

Then I entered "find / -user bandit7 -group bandit6 -size 33c 2>&1 | grep -F -v Permission" this I founded the key for next level.In next level I get to know that their is data.txt file in which the key is on millionth, so for this I entered the command "cat data.txt | grep millionth" and then I got the key for next level.

     PASSWORD : cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Level 8 to 9:

Then in next level I get to know that their is file named as data.txt in which only one line is coming once and the code is in that line so for this I used "sort data.txt | uniq -u" so by this I got the key and entered in the next level.

     PASSWORD : UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
     
Level 9 to 10:

After this in level 9 the password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters so for this used "strings data.txt | grep ==" so I get the key from here.

     PASSWORD : truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
     
Level 10 to 11:

Then I for another level it was written that the password is in a file data.txt, which contains base64 encoded data so i founded the password by **"base64 -d data.txt**".

     PASSWORD : IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
     
Level 11 to 12:

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions . then for solving this level i have to search for ROT13 . then I tried the tr command 
**cat data.txt | tr 'n-za-mN-ZA-M' 'a-zA-Z'** . and I get the password.

     PASSWORD : 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
     
Level 12 to 13:

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. Then it was given that we have to make a directory using **mkdir /tmp/anu and copy that data.txt** file in the new directory.Then Use **xxd command** to convert a hex dump back to its original binary form Then using file command file.data it is showing that a gzip compressed data is there is this file. So then First move this compressed data to data.gz and then decompressed it using **gzip -d data.gz** and after that again see file data then it will showing that the data is in the bzip2 compressed. Then move that data to **data.bz2** and then decompressed using **bzip2 -d data.bz2**. 
by using this method u have do untill the type of the data will not show **ASCII code** . 
After that use cat data then it will show the password.

     PASSWORD : 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
     
Level 13 to 14:

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private **SSH key**🔐  that can be used to log into the next level.
Then using ls command a sshkey.private will display. It is saying that u will get a private ssh key that can be used to login in to the next level.
Using **ssh -i ./sshkey.private bandit14@localhost** , it directly jump in into the bandit 14.
Then for getting password for the next level it is stored in the **cat /etc/bandit_pass/bandit14** .

Level 14 to 15:

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost. Using the previous previous question that the password for the next level is stored in the **/etc/bandit_pass/bandit14** and I get this # 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e .
After that To submit this password for the next level using echo command followed by the above password and nc -v localhost 30000

     PASSWORD : BfMYroe26WYalil77FoDi9qh59eK5xNr
     
Level 15 to 16:

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.
Using **echo BfMYroe26WYalil77FoDi9qh59eK5xNr | openssl s_client -quiet -connect localhost:30001** we can find the password of the next level

     PASSWORD : cluFn7wTiGryunymYOu4RcffSxQluehd
     
 Level 16 to 17:
 
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First use this command  **"nmap -Pn -A localhost -p 31000-32000"** to see who all the ports are listening and who are just returning the file which you are sending and get back as echo.
Then use this command **"echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -quiet -connect localhost:31790"** that it will show Private key after that make a directory and saved in the file .
Using echo and edit the private key and named it as **sshkey.private** and after that to change the permissions  use **chmod 400** and then when I use this **"ssh -i ./sshkey.private bandit17@localhost"** to jump into bandit17 it works. 

     NO PASSWORD REQUIRED , ONLY THE SSH KEY
     
Level 17 to 18:

There are 2 files in the home directory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new 
Use a **diff command** to differentiate the two passwords file and it will show the difference between the passwords of the two files which is passwords.old and passwords.new.

     PASSWORD : kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
     
Level 18 to 19:

The password for the next level is stored in a file readme in the home directory. While getting nto bandit18 using ssh commands it is showing BYEBYE and automatically it is getting out of the bandit because it was given that in the level 17 that if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19.
Then I have solved this using **"ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme"** directly not getting into bandit18.

     PASSWORD : IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
     
Level 19 to 20:

To gain access to the next level, you should use the setuid binary in the homedirectory. setuid is (short for "set user ID" and "set group ID")
While Now I am in level 19 and by seeing what are in the this level , it only shows **bandit20-do** . In this level it has already said that the password for this level can be found in the usual place **/etc/bandit_pass** . So I have use this command **./bandit20-do cat /etc/bandit_pass/bandit20** and I got password for the next level.

     PASSWORD : GbKksEFF4yrVs6il55v6gwY5aVje5f0j
     
Level 20 to 21:

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. So first echo the previous password and followed by the nc command with the localhost and the port number.
using this **echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l localhost -p 12345 &** and then using this **./suconnect 12345** 
Then it will read the previous passwords and give the next level passwords.

    PASSWORD : gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
     
Level 21 to 22:

A program is running automatically at regular intervals from cron, the time-based job scheduler. Then It says that look in **/etc/cron.d/** for the configuration.Then go in this directory  and type ls . U will get a file of cronjob. So I have used **cat cronjob_bandit22** then it is showing that how to access the file that which command is being executed at the back.
**cat /usr/bin/cronjob_bandit22.sh** . Then it shows **/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv**. After that I use this using cat command and after the password is here. 

     PASSWORD : Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI


     

