Lab - Output, Download and Uncompress
==========
Follow the instructions line-by-line.  

* Type in the commands as is, but ignore the beginning prompt.  
* Enter, tab, up and down are represented by <ENTER><TAB>,<UP> and <DOWN>.  
* "No output" or "nothing happens" are valid answers to any of the questions.
==========

==========
We're going to be echoing stuff to the console and cleaning it up.
==========

==========
1. Type:

$ echo hello

Copy and paste the output below.
----------echo hello
hello
V217-M11:~ bryan.pierrelouis02$ 



==========
2. Type:

$ echo hello there

Copy and paste the output below.
----------V217-M11:~ bryan.pierrelouis02$ echo hello there
hello there



==========
3. Type:

$ echo good mornin'

Copy and paste the output below.
----------V217-M11:~ bryan.pierrelouis02$ echo good mornin'
> 



==========
4. Uh-oh... we're stuck!

Type [CTRL + C] to get your prompt back.
----------
> 
V217-M11:~ bryan.pierrelouis02$ 



==========
5. Say good mornin' again with quotes!

$ echo "good mornin'"

Copy and paste the output below.
----------V217-M11:~ bryan.pierrelouis02$ echo "good mornin'"
good mornin'
V217-M11:~ bryan.pierrelouis02$ 


==========
6. There are some other symbols that have special meanings if you don't quote them.  For example, > brings up a different prompt.  Try *.

$ echo *

What happens?
----------V217-M11:~ bryan.pierrelouis02$ echo *
Adlm Adobe Applications Creative Cloud Files Desktop Documents Downloads Library Movies Music Pictures Public Sites isus
V217-M11:~ bryan.pierrelouis02$


==========
7. Ok... that's a lot of output.  How do we clean up our screen so that it's empty again?

Write the command that you used below:
---------- clear



==========
We're going to practice downloading files from a web site.  We'll use this practice to download more lab materials!
==========
==========
8. Now let's try downloading a file from a web site.  Type in the URL *exactly* as is: google.com.

$ curl google.com

Copy and paste the output below.
----------<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>



==========
9. And again.  This time, add www to the URL.

$ curl www.google.com

Copy and paste the output below, but not the whole thing!  Just copy up to the part that has the title tags (<title>......</title>).
----------
<!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="en"><head><meta content="Search the world's information, including webpages, images, videos and more. Google has many special features to help you find exactly what you're looking for." name="description"><meta content="noodp" name="robots"><meta content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta content="/images/branding/googleg/1x/googleg_standard_color_128dp.png" itemprop="image"><title>Google</title><script nonce="I5kzb2kLPgiQFyoCRYWRQQ==">(function(){window.

==========
10. That's great, but what if I want to save the file?  What flag/option and option argument would I use to download the page to a file called google.html?  Run it to download the URL www.google.com.

Write the command you used below.  Also copy and paste the output below.
---------- -o



==========
11. Now let's download the lab file for this homework.  First, figure out what directory you're in.

Write the command you used to determine your directory.  Also, copy and paste the output below.
---------- pwd



==========
12. If you're not in your home directory, change to it (use the shortcut).

Write the command that you used to change to your home directory.  If you were already in your home directory, write the command that you *would* have used to change to it!
----------bryan.pierrelouis02$ ~/
-bash: /Users/bryan.pierrelouis02/: is a directory
V217-M14:~ bryan.pierrelouis02$ pwd
/Users/bryan.pierrelouis02
V217-M14:~ bryan.pierrelouis02$ 



==========
13. So... the lab materials are located at this url:

http://entertainmenttechnology.github.io/Tsadok-MTEC1003-fall-2018/labs/02/mtec1002-lab-02.zip

Download the file using curl... to a file called mtec1002-lab-02.zip using the commandline.  

REMEMBER to use the -o flag, and follow it with a .zip extension! 

Use ls to verify that it downloaded.

Write down the command that you used to download the file below.  Additionally, write the output of the command below.
----------/Users/bryan.pierrelouis02/Downloads/mtec1002-lab-02.zip 



==========
14. We learned a command to uncompress a .zip file.  Use it to extract the files and folders from the file you just downloaded.

Write down the command that you used to uncompress the file.
----------



==========
15. Change to the directory that was just created.  List the contents (of the directory that was extracted from the labs .zip file). 

Copy and paste the output below.
---------- I dont remember 



==========
We're going to mess around with archiving and compressing files.  We'll make a directory with a file in it... archive and compress it.... and uncompress it elsewhere.
==========
==========
16. Go back up to your home directory.  Create a directory called stuff.  List the contents of your home directory to prove that the directory was created.

Copy and paste the output below.
---------- mkdir stuff
mkdir: stuff: Permission denied
V217-M14:applications bryan.pierrelouis02$ 



==========
17. Change into the "stuff" directory that you just created.  Run the following command (we haven't learned this exact command yet, but we will in the next lab!) exactly as described below:

$ echo "hi" > hello.txt

List the files in the directory you're currently in (which should be stuff).  

Copy and paste the output below.
---------- echo "hi" > hello.txt
-bash: hello.txt: Permission denied
V217-M14:applications bryan.pierrelouis02$ 



==========
18. Go up one directory back into your home directory.  Run the following commands exactly to create a compressed archive of the stuff folder.

$ tar -cvf stuff.tar stuff

List the files in the directory you're currently in (which should be home).  

Copy and paste the output below.
----------tar -cvf stuff.tar stuff
tar: Failed to open 'stuff.tar'
V217-M14:/ bryan.pierrelouis02$ 



==========
19. Go up one directory back into your home directory.  Run the following commands exactly to create a compressed archive of the stuff folder.

$ tar -cvf stuff.tar stuff

Copy and paste the output below.
----------tar -cvf stuff.tar stuff
tar: Failed to open 'stuff.tar'
V217-M14:/ bryan.pierrelouis02$ 



==========
20. List the files in the directory you're currently in (which should be home).  

Copy and paste the output below. (It should contain stuff.tar)
----------
V217-M14:~ bryan.pierrelouis02$ stuff.tar

==========
21. Now compress it!  Type:

gzip stuff.tar

List your files again.... you should have a new file with a .gz extension.  Copy and paste the output of your this below.
----------
~ bryan.pierrelouis02$ gzip stuff.tar
gzip: can't stat: stuff.tar (stuff.tar): No such file or directory
V217-M14:~ bryan.pierrelouis02$ 



==========
22. Move stuff.tar.gz into the lab directory that we downloaded.  We didn't learn this command yet, so just type in exactly as is:

$ mv stuff.tar.gz mtec1002-lab-02 

MAKE SURE YOU MOVE THE FILE THAT ENDS IN .gz!

Change your directory to mtec1002-lab-02.  

List the files.  Copy and paste the output below (stuff.tar.gz should be there).
----------


==========
23. You should be in the lab directory.  Let's uncompress the file.

$ tar -xvf stuff.tar.gz

List the files.  Copy and paste the output below (the folder, stuff, should be there).
----------


