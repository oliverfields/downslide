---
author: Oliver Fields
title: Slides with downslide
slide links: yes
---

# ${title} {: .slides-title }

## By ${author} {: .slides-sub-title }

<p style="text-align: center; background-color: var(--color-fg); color: var(--color-bg); border-radius: .5em;">Navigate with ⬅️ , ➡️ or click</p>

---

# Features

- Markup slides using Markdown
- Key/values defined in optional front matter can be referenced in markdown
- Local images are embedded in slides (share one file)
- Live rebuilding

☝️ Slides made with downslide, see the [markdown](https://github.com/oliverfields/downslide/blob/main/example_slides.md?plain=1).

---

# Basic CLI usage

<pre>
$ downslide slides.md
$ ls
slides.html  slides.md
</pre>

---

# Navigating HTML slides

- Next slide **space, enter or right arrow**, or click right side
- Previous slide **backspace, left arrow**, or click left side


---

# Styling

Recommended starting point is to use the following command and edit **style.css** to taste.

<pre>
$ downslide --dump-default-css > style.css
</pre>

The following command generates slides with your new style.

<pre>
$ downslide --css style.css slides.md
</pre>

---

# Front matter key/values

The following markdown represents a single slide. The title will be **Nice slide**. Note that front matter key names are converted to lower case.

<pre>
--- 
title: Nice slide
--- 

# &dollar;{title}

A slide about slides
</pre>

---

# Embedding images {: style="font-size: 4em;" }

Any images that are referenced relatively in markdown will be automatically embedded in the slide HTML (base64).

<pre>
$ cat my_beach_slides.md
# Slide 1

![Look at that beach](beach.jpg)
$ ls
beach.jpg
my_beach_slides.md
$ downslide my_beach_slides.md
</pre>

