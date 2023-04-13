---
layout: post
title:  "Firefox helpful tips"
date:   2023-04-13 14:55:56 -0500
categories: jekyll update
---

Firefox css 

If you are using Firefox 70+ versions on Linux, like me:

1. Go to about:support. And look for the "Profile Directory" button. 2. On the opened directory, create a folder called "chrome" if it doesn't exist. 3. Create a file called userContent.css, and paste in the following contents: ``` @-moz-document url-prefix(about:home), url-prefix(about:newtab) { .click-target-container *, .top-sites-list * { color: #fff !important ; text-shadow: 2px 2px 2px #000 !important ; }

body { background: url(/usr/share/backgrounds/flowers-4564439.jpg) !important ; background-size: cover !important ; } } ``` Save the file and open Firefox (no need to restart at this point).

·	 [replace the url(...) with the image path. Here, in my case I have images in the /usr/share/backgrounds direcotry]

·	 [The `background-size: cover !important  ;` line here means that the image will be resized automatically].

·	 [Everything is self explainatory here]

·	 [IDK how to format codes on support.mozilla.org]. 

4. Open the url about:config, and change the option "toolkit.legacyUserProfileCustomizations.stylesheets" to true.

5. Restart firefox. It should look more awesome now!

echo export MOZ_USE_XINPUT2=1 | sudo tee /etc/profile.d/use-xinput2.sh

gfx.webrender.software

