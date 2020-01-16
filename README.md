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

     PASSWORD : bandit2 = UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Level 2 to 3:

Again I exited and recalled the server by above commands just replacing 1 by 2 and then I entered the above accessed password in this then I got a file named as "spaces in this filename" I open this file by "cat spaces\ in\ this\ filename" and I again got the password and then i exited and recalled the server by entering the password.

     PASSWORD : bandit3 = pIwrPrtPN36QITSp3EQaw936yaFoFgAB

Level 3 to 4:

In this level after entering the password there is inhere directory in which there is hidden file so I just used "ls -la" then by this get to know that there is .hidden file so I just opened it by ""cat .hidden" in this way I found the password for the next level.

     PASSWORD : 

Level 4 to 5:

Again their is a inhere directory, as in this level we can get the password which is stored in a human readable file so first for getting the ASCII file i write the command "du -h | file ./ "* then bythis we get to know that the human readable file is -file07 so for getting the password I write the command as "cat ./-file07".
