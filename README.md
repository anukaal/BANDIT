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

Again their is a inhere directory, as in this level we can get the password which is stored in a human readable file so first for getting the ASCII file i write the command "du -h | file ./ "* then bythis we get to know that the human readable file is -file07 so for getting the password I write the command as "cat ./-file07".

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

Then I for another level it was written that the password is in a file data.txt, which contains base64 encoded data so i founded the password by "base64 -d data.txt".

     PASSWORD : IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
     
Level 11 to 12:

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

