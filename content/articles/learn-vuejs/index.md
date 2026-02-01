+++
title = 'Learn Vuejs'
date = 2025-08-27T18:13:55+01:00
draft = true
summary = ""
showTableOfContents = true

+++

#### The Goal: A Crossword Website


It's easy to spend an age trying to decide what library, language or framework to learn.

I want to make some JS websites and I chose [VueJS](https://vuejs.org).

It's popular so there's lots of [tutorials](https://vuejs.org/tutorial) and [examples](https://vuejs.org/examples).
It can be used from a cdn to 'enhance' some existing html.
It seems to split things up in a way that's familiar to someone with basic html, css and javascript experience. (like me!)


#### Exercise App

I found this tutorial and decided to work my way through it (4h9min!)

https://www.youtube.com/watch?v=JAgeFLJYrUY

What did I learn?

* Setting up with vite
* Components
    * Script
    * Template
    * Styles
* < Slot/>
* Object?.[item]
* @click
* v-if
* v-bind
* props
* passing functions as props

#### TicTacToe Tutorial

https://www.youtube.com/watch?v=sjYxRlwHvsM&t=1234s

What did I learn?

This probably had simpler code and was a shorter tutorial but

* Computed values
* TailwindCSS with a plugin in VS Code 
* if elsif else shorthand {{ cell === 'X' ? 'close' : cell === 'O' ? 'circle' : '' }}
* outputting conditional css classes based on js variables





#### Weather App

https://www.youtube.com/watch?v=JLc-hWsPTUY

I tried chanigng this as I went from XX to composition but I just tied myself in knots.

After a while I couldn't really figure out what the source of my errors was. The API is down?

I'm using the wrong syntax for variables?

So I went looking for an easier example of fetching API data

#### VueJS Examples page

https://vuejs.org/examples/#fetching-data

This grabs a list of commits from a Github url and loops through them. 

Uses some small methods to truncate the commit message and format the dates associated.

It uses nested template tags which are just to signify 'sections' or logical groups of the template.

<!--
{{< figure
    src="abstract.jpg"
    alt="Abstract purple artwork"
    caption="Photo by [Jr Korpa](https://unsplash.com/@jrkorpa) on [Unsplash](https://unsplash.com/)"
    >}}



![Abstract purple artwork](abstract.jpg "Photo by [Jr Korpa](https://unsplash.com/@jrkorpa) on [Unsplash](https://unsplash.com/)")

-->