# Category :
### Web

# Challanges :
[h1t](h1t.hamza.fun)&nbsp;- 50  points (**Easy**) <br>
[cock](cock.hamza.fun)&nbsp;- 100 points (**Easy**) <br>
[job](job.hamza.fun)&nbsp;- 250 points (**Medium**)<br>

# Solution:

## 1- **h1t**

This challenge is fairly easy, and is categorized under **real life** maybe you will not face it in **real life** but in the same style and more difficult, You can review `the fifth chapter` of the book `The web application handbook hackers 2`<br>
<br>
As we see this is the interface to challenge

![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/h1t-1.png "h1t-1")<br>
If we click on secret, It will send a request of type **POST**
<br><br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/h1t-2.png "h1t-2")<br>
If we focus too well, it tells you `If you're admin hit flag button !`, flag Button NOT secret Button <br><br>
Ok, Will send flag button<br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/h1t-3.png "h1t-3")<br>
### Done
<br><br><br>
## 2- **cock**

This somewhat challenge does not come in **real life**, it is just **Like-CTF**, You should be familiar with the basics as at least a web developer, and a little evil

in the First , Noting important in source code challange
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/cock-1.png "cock-1")<br>
i try search in pic about file but not found
ok if you try search about file will find `robots.txt` 
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-2.png "cock-2")<br>
ok if we try enter this path , will can't becase just user-agent `joker99` could be enter to it
But even if we change user-agen, There will be no response, and the simple reason is that there is a trap
<br>![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-3.png "cock-3")<br>
just remove port 200 and change it to 80
<br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-5.png "cock-5")<br><br>
<br><br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-6.png "cock-6")<br><br>
ok if send request will ask us `WWW-Authenticate: Basic`<br>
Ammm ok try any user and pass, but not correct
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-7.png "cock-7")<br><br>
if reload page again will add for head new parameter in cookie
<br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-8.png "cock-8")<br><br>
`Login=False` nice , try change it to `True` &&  **Don't forget change user-agent**
<br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/coke-9.png "cock-9")<br><br>
<br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/cock-10.png "cock-10")<br><br>
### DONE
## 3- **job**

  This challenge is great, and you will face it in real life very dramatically, and also in the challenges of CTF

  There is nothing tempting about this challenge but the picture, I have searched the image (it may have been an important file has been integrated into the picture) but I did not find anything , It is also difficult to search for files and folders by tools like gobuster or dirlister and etc ... , becase the response alwayas `200`<br>

  hmmm, Ok We have tried a lot of possibilities, but to no avail, in fact you as a breakthrough laboratory to solve this problem, and the solution comes through: What is the problem basically?

  In any case, you must guess and imagine all the scenarios that can occur with the web developer and may cause danger to the application

  But before we imagine, we should see the head of requests and responses, Hoping to find something to help us ;)
  
  ![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-1.png "job-1")<br>
  
  userCookie! Ok base64 encode , just decode it
  
  ![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-2.png "job-2")<br>
  
  ![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-3.png "job-3")<br>
  hmmm , Object Serialization , Ok try change value to `admin , flag , Admin , Flag , etc ...` but Nothing :( 
  Actually the topic is bigger than that, as we see we are could get `php object injection` , For This We should see the source of the code, so you can do this
  
  some times bad developers forget close file in correct way or make for file backup
  
  ok let's for search about source code 
  
  Before we go we must remember that it is possible to have the following formulas `-
.
~
.1
.2
.3
.bac
.backup
.bak
.cache
.conf
.cs
.csproj
.dif
.err
.gz
.inc
.ini
.java
.map
.log
.lst
.old
.orig
.part
.rej
.sass-cache
.sav
.save
.save.1
.sublime-project
.sublime-workspace
.swp
.tar
.tar.gz
.temp
.templ
.tmp
.txt
.un~
.vb
.vbproj
.vi
.zip
._
0
s
1
_
2
.dist
~
~1
~bk
..swm
..swn
..swo
..swp`
<br>![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-4.png "job-4")<br><br>
![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-5.png "job-5")<br>
If we do a simple code analysis, we will see that the cookie were calling the `class User`.
Through the analysis we find that we can, we can request class `Flag` instead of `User`
<br>![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-6.png "job-6")<br>
<br>![alt text](https://github.com/AnonDeek/CTF/blob/master/HC-CTF/Web/job-7.png "job-7")<br>
### DONE

Thanks For `Hamza Abdelrahim - @Crypto` for this amazing challanges
