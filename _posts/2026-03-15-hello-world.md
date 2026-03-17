---
layout: post
title: "Hello World -- Alexander"
date: 2026-03-15 07:57:00 +00:00
excerpt: "A small demo post for GitHub Pages with example images and GIFs."
categories: [homelab, hardware]
tags: [servers, networking, os]
image: /assets/images/ExampleSwappyPic.png
---
<!--- Add Basic placement div until user verifies, crappy solution for no routing logic --->
<div id="gate" style="
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: black;
  z-index: 9999;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
">
  <div class="cf-turnstile" data-sitekey="0x4AAAAAACsN4kOnRM01XA2b" data-callback="onVerified"></div>
</div>
  
<!---- Sourced From https://developers.cloudflare.com/turnstile/get-started/client-side-rendering/ https://developers.cloudflare.com/turnstile/get-started/server-side-validation/ ---->
<script
  src="https://challenges.cloudflare.com/turnstile/v0/api.js"
  async
  defer
></script>
<script>
async function onVerified(token) {
  const responseOb = await fetch("https://acsite-worker.aycarter2005.workers.dev/", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ "cf-turnstile-response": token }), //check token 
  });
  const data = await responseOb.json()
  if (data.ok) {
    console.log("Worker Data Resp: ", data)
    document.getElementById("gate").style.visibility = "hidden";
    document.getElementsByClassName("cf-turnstile")[0].style.display = "none"; //most likely not needed
  } else {
      window.location.href = "https://aycftf.github.io"; //ret to homepage
  }
}  
</script>

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
bundle exec jekyll s --baseurl "" -- localhosting
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
