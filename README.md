<h1>PicoCTF 2022 #38 ‘Secrets’ HIDDEN WEBSITE DIRECTORIES</h1>

 

<h2>Description</h2>

<img src="https://i.imgur.com/PARyv7i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


What is a Website Directory?

A website directory is a handmade list of websites. Also known as a subject directory, these lists create an organized method for finding websites. It's similar, but not identical, to a search engine.

LET'S BEGIN OUR CTF

As we begin , we are greeted with three web pages

Page 1 - Home Page

<img src="https://i.imgur.com/4Aa2g6R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



Page 2 - About

<img src="https://i.imgur.com/asmPUVq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Page 3 - Contact

<img src="https://i.imgur.com/6nerxMd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


As we see no useful information relating to our CTF challenge , lets go ahead and view the source code using the command “Control + U”

<img src="https://i.imgur.com/aUxq1hH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

While studying the source code , we see a link that seems interesting “<link href="secret/assets/index.css" rel="stylesheet" />” and we click it, it takes us to

<img src="https://i.imgur.com/jgIso9Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Still no useful information to be found. But on a second glance we see the url, and try to go back a little before index to assets.

It returns a 403 Forbidden message , so a dead end.

So now we go back a step more in the url to the secrets

http://saturn.picoctf.net:61481/secret/


A very comic message greets us , so lets check its souce code

<img src="https://i.imgur.com/NnxZvET.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

In the source code a we find a link “<link rel="stylesheet" href="hidden/file.css" /” 
                                           
When we go to the link and further investigate we are greeted by this page 
                                           


<img src="https://i.imgur.com/MLrqGue.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

We further review the source code of this page and find a very interesting link “<input type="hidden" name="db" value="superhidden/xdfgwd.html" />” 

We copy and paste the superhidden/ to the page code (http://saturn.picoctf.net:61481/secret/hidden/superhidden/)
and press ENTER

<img src="https://i.imgur.com/iwlCP23.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

WE DID IT, WE CAPTURED THE FLAG

Thanks For Reading, Have A Good DAY!




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
