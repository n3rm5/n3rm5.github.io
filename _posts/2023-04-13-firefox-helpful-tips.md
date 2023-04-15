---
layout: post
title:  "Firefox helpful tips"
date:   2023-04-13 14:55:56 -0500
categories: jekyll update
---

Have you ever wanted to change the default "New Tab" background on Firefox from that awful blinding white or ugly grey? 
Well for the longest time I did aswell, I was too lazy to do my research and I just sat around pretending it was impossible.
I am here to tell you it is not only possible but very easy.

<img src="/assets/img/firefox/firefoxone.png">

**Step 1** Go to your url and type `about:support` click on the `Open Directory` link, 

<img src="/assets/img/firefox/firefoxtwo.png">

**Note:** *If your file manager does not automatically open the link you can copy and paste the path into your file manager*

**Step 2** Create a directory inside your Firefox default-release directory called `chrome` inside of this directory 
create another directory called `img` this is where your source image file will be stored. 

<img src="/assets/img/firefox#3.png">


**Step 3** Go back to the chrome directory and create a `.css` file called `userContent.css` add the following to the file:

{% highlight css linenos %}

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

{% highlight ruby linenos %}
def foo
  puts 'foo'
end
{% endhighlight %}
