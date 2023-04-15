---
layout: post
title:  "Firefox 'New Tab' background" 
date:   2023-04-13 14:55:56 -0500
categories: jekyll update
---

Have you ever wanted to change the default "New Tab" background on Firefox from that awful blinding white or ugly grey? 
Well for the longest time I did as well, I was too lazy to do my research and I just sat around pretending it was impossible.
I am here to tell you it is not only possible but very easy.
<br/>
<br/>
<br/>
<img src="/assets/img/firefox/firefoxone.png">
<br/>
<br/>
<br/>
**Step 1** Go to your url and type `about:support` click on the `Open Directory` link, 
<br/>
<br/>
<br/>
<img src="/assets/img/firefox/firefoxtwo.png">
<br/>
<br/>
<br/>
**Note:** *If your file manager does not automatically open the link you can copy and paste the path into your file manager*
<br/>
<br/>
<br/>
**Step 2** Create a directory inside your Firefox default-release directory called `chrome` inside of this directory 
create another directory called `img` this is where your source image file will be stored. 
<br/>
<br/>
<br/>
<img src="/assets/img/firefox/firefoxthree.png">
<br/>
<br/>
<br/>
**Step 3** Your image needs to meet certain criteria if it is going to format correctly, you should only use 16:9 images and I 
personally wouldn't go below 1920x1080p. Your filename needs to match up with the `.css` file, as you can see in the next step 
I chose to call the file `yourimagefilenamehere.jpg` however you can call it whatever you like as long as it is the same as the 
`.css` file. Place your image file in the `img` directory.
<br/>
<br/>
<br/>
**Step 4** Go back to the chrome directory and create a `.css` file called `userContent.css` add the following to the file:
<br/>
<br/>
<br/>
{% highlight css %}

@-moz-document url(about:home), url(about:newtab), url(about:privatebrowsing) {
.click-target-container *, .top-sites-list * {
    color: #fff !important ;
    text-shadow: 2px 2px 2px #222 !important ;
}
body::before {
    content: "" ;
    z-index: -1 ;
    position: fixed ;
    top: 0 ;
    left: 0 ;
    background: #f9a no-repeat url(img/yourimagefilenamehere.jpg) center ;
    background-size: cover ;
    width: 100vw ;
    height: 100vh ;
}

{% endhighlight %}
<br/>
<br/>
<br/>
**Step 4** Save the `.css` file and open firefox, navigate to `about:config` find the `toolkit.legacyUserProfileCustomizations.stylesheets`
and change it from `false` to `true`. 
<br/>
<br/>
<br/>
<img src="/assets/img/firefox/firefoxfour.png">
<br/>
<br/>
<br/>
**Step 5** Restart Firefox and enjoy!
<br/>
<br/>
<br/>
<img src="/assets/img/firefox/firefoxfive.png">
