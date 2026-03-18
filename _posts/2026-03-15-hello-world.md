---
layout: post
title: "Hello World -- Alexander"
date: 2026-03-15 07:57:00 +00:00
excerpt: "A small demo post for GitHub Pages with example images and GIFs."
categories: [homelab, hardware]
tags: [servers, networking, os]
image: /assets/images/ExampleSwappyPic.png
---

<!-- Turnstile gate — sourced from Cloudflare docs -->
<div id="gate" style=" position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: black; z-index: 9999; display: flex; flex-direction: column; align-items: center; justify-content: center; ">
  <div
    class="cf-turnstile"
    data-sitekey="0x4AAAAAACsN4kOnRM01XA2b"
    data-callback="onVerified">
  </div>
</div>
function onVerified(token) {
  //fetch backend with token from data-sitekey, then get response, and remove gateway object, hopefully!
  fetch("https://acsite-worker.aycarter2005.workers.dev/", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ token })
  }).then(res => {
    if (res.ok) document.getElementById("gate").remove();
  });
}
//remove again just incase
document.getElementById("gate").remove();


# Alexander Carters First Post?!

This will be my intro text. I can say whatever here hello gello jamie jmaie words words!

## Quick demo

My cool awesome embedded GIF:

![Demo GIF](/assets/images/test2.gif)

Fallback external placeholder GIF:

![Placeholder GIF](https://media1.tenor.com/m/xIT75legP18AAAAd/squirtle-squirtle-squad.gif)

## Features

* Lightweight Jekyll post template
* Examples for images, GIFs and code blocks
* Ready for GitHub Pages
* Cool Stuff like bullet points :0

## Installation (Cool Bash Example where its cool and specified and stuff)

```bash
# clone and serve locally
git clone https://github.com/username/repo.git
cd repo
bundle install
bundle exec jekyll serve
bundle exec jekyll s --baseurl "" -- localhosti
bundle gem new_gem_scaffold
##Bundler then resolves these dependencies, fetches the needed gems from a remote source — https://rubygems.org and installs them into your ruby environment
```

```javascript
console.log("Wow")
```

Basic markdown sample:

```markdown
## Example Section
- Step 1: Do this
- Step 2: Do that
- Step 3: Do even more
```

Center and caption (HTML inside Markdown):

<p align="center">
  <img src="/assets/images/centered.png" alt="Centered image" width="600">
  <br><em>Example: Centered Image!</em>
</p>

## Photo

![img-description](https://static.wikia.nocookie.net/deathnote/images/9/9c/Manga_character_icon_Ryuk.jpg/revision/latest?cb=20170716181140)
<br><em>Insert future guide image here!</em>

## Tips for me in the future (TODO)

- Keep images in /assets/images and reference them with absolute paths.
- Use small GIFs to avoid slow page loads.
- Add alt text for accessibility.

## File structure (suggested)

- _posts/
    - 2026-03-15-HelloWorld.md (markdown)
- assets/
    - images/
        - png 3
        - png 2
        - png 1

<!-- End of post -->
