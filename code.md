---
layout: page
title: Code
permalink: /code/
rss: https://github.com/archenoth.atom
---

<style>
  .post-content img{
    float: right;
    margin-left: 100px;
    margin-bottom: 50px;
    max-width: 50%;
  }

  @media only screen and (max-width: 1400px) and (min-width: 600px) {
    .post-content img{
      max-width: 40%;
    }
  }
  @media only screen and (max-width: 600px) {
    .post-content img{
      max-width: 100%;
    }
  }

</style>

I slow down computers in useful ways for a living. Here is a collection of various means by which you can slow down yours too!

## [Pokemon Blue: Oshawott Edition](https://github.com/Archenoth/pokeblue-oshawott)
> what if pokemon blue, but oshawott

![An Oshawott battling against Bulbasaur in Pokemon Blue's first rival battle, running in Mednafen](https://raw.githubusercontent.com/Archenoth/pokeblue-oshawott/master/OshawottBattle.png "Oshawott!")

Using the extremely neat [pret](https://github.com/pret/pokered) disassembly of the original games, I made a modification where you can play the game with an Oshawott starter!

[Oshawott's moveset](https://bulbapedia.bulbagarden.net/wiki/Oshawott_(Pok%C3%A9mon)#Learnset) largely doesn't exist in the Gen 1 Pokemon games, so this is still a bit challenging, though I did give the entire line access to Mega Punch and Mega Kick since the place you can get those can be taught to any starter!

[Here is a video of it in action](https://www.youtube.com/watch?v=g8ttpYLQaw8) if you wanna see what it all looks like~


## [clj-anki](https://github.com/Archenoth/clj-anki)
> A way to make Anki flashcards from silly things! Alternatively a way to extract silly things from Anki flashcards~

A Clojure library to read and write Anki files. It's as simple as running

```clojure
(let [cards ["3 + 4" "7"
             "4 + 5" "9"]
  (anki/notes-to-package! cards "math.apkg"))
```

...and poof! You have a little study deck~

This means you can basically just shove your [soup](https://github.com/mfornos/clojure-soup) output or whatever right into [`notes-to-package!`](https://github.com/Archenoth/clj-anki/blob/master/doc/intro.md#writing) and get a nifty study deck back using any data source you could imagine!


## [wsl_proxy](https://github.com/Archenoth/wsl_proxy)
> So your Windows can accidentally your WSL programs too

![A screenshot of a cmd.exe Window where I rename wsl_proxy to ls.exe, use it to list the folder it's in, hardlink it to cat.exe, and use cat.exe to open a file with a complex set of hard-to-escape characters, link it again to ln.exe, and use that to hardlink the file I catted earlier into the current folder](https://raw.githubusercontent.com/Archenoth/wsl_proxy/master/screenshot.png "wsl_proxy.exe being used to run a bunch of wsl programs in a cmd window")
wsl_proxy is a little program where, if you rename `wsl_proxy.exe` to the name of a command you have in your WSL distro, it will act as if it *is* that program.

So if you rename `wsl_proxy.exe` to `nano.exe`, you will be able to associate it with things in Windows!
