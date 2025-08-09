+++
title = "Starting a Blog"
draft=true
[extra]
toc=true
+++

# So you want to make a blog?

if you want to make a blog, first you need to invent the universe. that is to say, the work around making a blog is part of it. i'm starting this out by simply typing into a KWrite window, with nothing of note - just an idea that this will eventually be a blog post on `xela.zone/blog`.

{{ img(id="kwrite.png" alt="kwrite.png" caption="the very beginnings of this blog post")}}

i guess the first thing to do is consider the process to go from writing a simple markdown file to actually getting it to be HTML with some fancy bells and whistles. that brings us to the first topic of discussion, Static Site Generators. 

## Static Site Generators

i've used some Static Site Generators (SSG from here out) in the past, notably Jekyll, in [robotics](https://github.com/metalknightsFTC/metalknightsFTC.github.io). that was 7 years ago! I wonder what's come and changed the world since then. but first, how about one of the first big SSGs, jekyll

### Jekyll

first and formost, jekyll powers [Github Pages](https://pages.github.com/), a prety easy to use site hosting patform. you don't *need* to use jekyll to use github pages, it *just works* out of the box with jekyll, without any additional effort. as i Don't really care about depending on a nice to have in the form of Jekyll's good intigreation with GH pages, i think i'll skip it for now.


### Hugo

i've used Hugo before too! for the MSBSD Tech Expo, [source code here](https://github.com/xela-zone/expo/) and [deployed here](https://xela-zone.github.io/expo/#/expo/main/). I've actually resurected this from the dead for this post, it being easy enough to change the config file to point to xela-zone instead of the original website. My favorite part of this project was making the randomized booth stuff using javascript to randomly pick form the different booths, havign leaflet to show a 'show floor' map with logos and what not for booths. given i was using this in 2021, the version i was using was 0.79. Hugo is up to version 0.148 now, theres got to be some new features or somthing in there now.

### Zola

[Zola](https://github.com/getzola/zola) is an up and coming SSG based on rust, but it looks pretty well featured. it doesn't support plugins, asserting that all you need is in the one, self hosting binary, But I've never used it before. 

### So... witch one?

as i've become accustomed to since the start of the A.I. Era, i've asked Gemini to compare and contrast the different options above. it's reccomending Zola or Hugo, and mentioning that Zola has a very 'opionated' approach - saying that there's a 'clear "Zola way" to do things'. 

so i'm going to start with zola and go from there. one of the very nice things about this all being 'just a bunch of text documents' is that changing to a different generator or viewer is *incredibly easy*, just port the documents over and it'll mostly just work - this is also why I use Obsidian for large knowlage projects.

# Getting started with Zola

I'll start by making a new project, as described by the [Zola Documentation](https://www.getzola.org/documentation/getting-started/overview/). 

first running `zola init blog` in my home folder, set up the blog folder for me.

{{ img(id="terminal-install-zola.png" alt="terminal screenshot of installing zola using pacman -S zola, followed by setting up the repository.")}}


reading the rest of the guide, i found the 'serve' command, started that up, and learned that 'themes' exist in Zola, so i started browsing those, and found [anemone](https://anemone.pages.dev/). given i understand git submodules, i set that up, with `cd themes`, `git submodule add https://github.com/Speyll/anemone.git`. after copying some `[Extra]` Section vars across, i had a theme! 

<firefox - empty theme>
{{ img(id="firefox-empty-theme.png" caption="well, part of a theme...") }}

 now i needed to write some content for the Home page, somthing plain and simple, introducing the site.... i'll start with a simple Hello World
 making a file at `content/_index.md` let me start editing the content!

 ```md
 +++

+++
Hello world!
```

{{ img(id="firefox-hello-world.png" caption="Hello World!") }}



