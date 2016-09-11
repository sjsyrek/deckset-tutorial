# Deckset Tutorial
## How to use Markdown to make beautiful presentations

Open this file in your [favorite text editor](http://www.vim.org/) and in the [Deckset](http://www.decksetapp.com/) application. I recommend that you view the tutorial using the Plain Jane theme to start with, as not all themes support all styling options. You can switch back and forth between editor and app to see how the Markdown is converted into slides, making experimental adjustments as you see fit. Enjoy.

---

# [fit] Deckset with Markdown
# Tutorial

---

or
# Deckset with Markdown
# [fit] Tutorial

---

or
# [fit] Deckset with Markdown
# [fit] Tutorial

---

# Steven Syrek

># `steven.syrek@gmail.com`

# Steven Syrek

>`steven.syrek@gmail.com`

`steven.syrek@gmail.com`

steven.syrek@gmail.com

---

## Start a new slide with a blank line, three dashes, and another blank line

---

## Smart copy & paste

To copy a slide from Deckset to another document, just ⌘+C it, then ⌘+V it into your editor (it will paste the _Markdown_) or into any application that handles PDFs (it will paste the slide as _PDF_).

---

# You can include inspirational quotes

---

>You miss 100 percent of the shots you never take.
-- Wayne Gretzky

---

Or (this one is inline) quotes that are actually interesting:

> # 'I'm bored' is a useless thing to say. You live in a great, big, vast world that you've seen none percent of. Even the inside of your own mind is endless; it goes on forever, inwardly, do you understand? The fact that you're alive is amazing. So you don't get to be bored.
-- Louis C. K.

---

# [fit] Fit text to the slide like this

---

# You can also include notes for yourself in the Markdown file that won't display on the slide

^ This text will not appear on the slide

---

# Line breaks

Put your line
breaks
wherever
you want

# Also works in <br> headers if you use the `<br>` HTML tag

---

# Emojis

You can use [GitHub style emojis](http://www.emoji-cheat-sheet.com/):

:shit: :rage: :fire: :scream: :-1: :pouting_cat:
:princess: :yum: :sweat_smile: :hamster: :hibiscus: :watermelon:

---

1. Ordered list
1. Use a 1 on every line
1. And they will be given the correct sequence

- Unordered list
* Use any of these three characters
+ And you will get a bulleted list

---

- Nested lists are also possible
    1. indent each item 4 spaces
        - here's another nested list
    1. back to this level
    1. and another item
        1. a numbered list, nested
        1. another nested item
- And back to the top

---

You **embolden** text like this or __like this__
You *emphasize* text like this or _like this_
Or __*do both*__ at the same time
You can also ~~strikethrough~~ text

This is <sub>Subscript text</sub>
This is <sup>Superscript text</sup>

> Center text like this
> # Center headings like this

---

# Normal Heading 1
## Normal Heading 2
### Normal Heading 3
#### Normal Heading 4

---

# *Emphasized Heading 1*
## *Emphasized Heading 2*
### *Emphasized Heading 3*
#### *Emphasized Heading 4*

---

# **Emboldened Heading 1**
## **Emboldened Heading 2**
### **Emboldened Heading 3**
#### **Emboldened Heading 4**

---

# ~~Strikethrough Heading 1~~
## ~~Strikethrough Heading 2~~
### ~~Strikethrough Heading 3~~
#### ~~Strikethrough Heading 4~~

---

You can write code inline by using backticks. For example, if you want to mention in passing that the monadic bind operation in Haskell has the type signature `(>>=) :: forall a b. m a -> (a -> m b) -> m b`.

---

Or you can use code blocks for longer examples, which use triple backticks and support syntax highlighting (as on GitHub):

```hs
instance Functor Maybe where
    fmap _ Nothing      = Nothing
    fmap f (Just a)     = Just (f a)

instance Applicative Maybe where
    pure = Just

    Just f  <*> m       = fmap f m
    Nothing <*> _m      = Nothing

    Just _m1 *> m2      = m2
    Nothing  *> _m2     = Nothing

instance  Monad Maybe where
    (Just x) >>= k      = k x
    Nothing  >>= _      = Nothing

    (>>) = (*>)

    fail _              = Nothing
```

---

Yeah, yeah, I know you want to see JavaScript:

```js
var docCookies = new Proxy(docCookies, {
  get: function (oTarget, sKey) {
    return oTarget[sKey] || oTarget.getItem(sKey) || undefined;
  },
  set: function (oTarget, sKey, vValue) {
    if (sKey in oTarget) { return false; }
    return oTarget.setItem(sKey, vValue);
  },
  deleteProperty: function (oTarget, sKey) {
    if (sKey in oTarget) { return false; }
    return oTarget.removeItem(sKey);
  },
  enumerate: function (oTarget, sKey) {
    return oTarget.keys();
  },
  ownKeys: function (oTarget, sKey) {
    return oTarget.keys();
  },
  has: function (oTarget, sKey) {
    return sKey in oTarget || oTarget.hasItem(sKey);
  },
  defineProperty: function (oTarget, sKey, oDesc) {
    if (oDesc && "value" in oDesc) { oTarget.setItem(sKey, oDesc.value); }
    return oTarget;
  },
  getOwnPropertyDescriptor: function (oTarget, sKey) {
    var vValue = oTarget.getItem(sKey);
    return vValue ? {
      value: vValue,
      writable: true,
      enumerable: true,
      configurable: false
    } : undefined;
  },
});
```

---

# [fit] Images

# Images can appear in a variety of ways.
# First, alone.

---

![](logo.png)

---

# Slide with an image and text overlay, filtered
![](logo.png)

---

# Slide with an image and text overlay, unfiltered
![original](logo.png)

---

![inline](logo.png)

You can use the [inline] modifier to add a caption to your image like this

---

# [fit] ![inline](logo.png)
# Image with a bigger caption...

---

# ...or heading
# [fit] ![inline](logo.png)

---

# You can also have images fill a slide (the default behavior), fit to a slide, scale up or down, align left or right, and appear filtered for a cool special effect (demonstrated on the following slides)

---

![](logo.png)

---

![fit](logo.png)

---

![300%](logo.png)

---

![25%](logo.png)

---

![left](logo.png)

---

![right](logo.png)

---

![filtered](logo.png)

---

>Images used inline scale to fit the size of the surrounding text:

# Heading with inline ![inline](logo.png) image

---

# [fit] Fit ![inline](logo.png) heading

---

>You can also create rows of images (make sure to insert a blank line to create a new paragraph):

![inline](logo.png) ![inline](logo.png) ![inline](logo.png)

---

> Or a grid:

![inline](logo.png)![inline](logo.png)
![inline](logo.png)![inline](logo.png)

---
> Or a grid with space between the lines:

![inline](logo.png)![inline](logo.png)

![inline](logo.png)![inline](logo.png)

---

# Create neat effects by combining these techniques

![fill](logo.png)

![inline](logo.png)![inline](logo.png)![inline](logo.png)

---

![fill inline](logo.png)
![inline](logo.png)![inline](logo.png)![inline](logo.png)

---

![inline](logo.png)![fill inline 300%](logo.png)

---

# You can also embed videos into your presentations (local or from YouTube)

---

![](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# You can inline them, too

![inline](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# Video on the left

![left](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# Video on the right

![right](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# Video fill

![fill](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# Video size by Percentage (50%)

![50%](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# Video size by Percentage (200%)

![200%](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# Combine playback options

![left autoplay mute loop](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

---

# You can have footnotes, too, if you must

This is some text that I would like to footnote[^1].

[^1]: This is the footnote (but do you really need footnotes on your slides?).

---

# Name references for footnotes, if you must

This is a reference to something[^Syrek, 2016].

[^Syrek, 2016]: I'm obviously not a fan of footnotes in slides.

---

# There is also support for math using

$$
\LaTeX
$$

Which, if you know how to use it, you are excited about:

$$
	\begin{matrix}
		\left( 	\frac{1 + x}{2 + y^{2}} \right)^{2} &
		\left[ 	\frac{1 + x}{2 + y^{2}} \right]^{2} &
		\left\{	\frac{1 + x}{2 + y^{2}} \right\}^{2} &
		\left|	\frac{1 + x}{2 + y^{2}} \right|^{2} &
		\left\| \frac{1 + x}{2 + y^{2}} \right\|^{2} &
		\left\backslash \frac{1 + x}{2 + y^{2}} \right\backslash^{2} &
		\left/ 	\frac{1 + x}{2 + y^{2}} \right/^{2} &
		\left< \frac{1 + x}{2 + y^{2}} \right>^{2} &\\
		\left\lfloor \frac{1 + x}{2 + y^{2}} \right\rceil^{2} &
		\left\lceil \frac{1 + x}{2 + y^{2}} \right\rfloor^{2} &
		\left\ulcorner \frac{1 + x}{2 + y^{2}} \right\lrcorner^{2} & % not stretchy
		\left\llcorner \frac{1 + x}{2 + y^{2}} \right\urcorner^{2} & % not stretchy
		\left( 	\frac{1 + x}{2 + y^{2}} \right]^{2} & % mix and match
		\left\uparrow \frac{1 + x}{2 + y^{2}} \right\downarrow^{2} & % weird
		\left\Uparrow \frac{1 + x}{2 + y^{2}} \right\Downarrow^{2} & % weirder
		\left\updownarrow \frac{1 + x}{2 + y^{2}} \right\Updownarrow^{2} &\\ % weirdest
		\left. 	\frac{1 + x}{2 + y^{2}} \right)^{2} & % no left delimiter
		\left( 	\frac{1 + x}{2 + y^{2}} \right.^{2} & % no right delimiter
		\left. 	\frac{1 + x}{2 + y^{2}} \right.^{2} % no delimiters at all
	\end{matrix}
$$

You can also do inline formulas thusly: $$[(a * b) + (c * d)]^{2}$$

---

# You include certain directives at the very top of your file, to affect the entire deck:

- footer: `footer: whatever you want your footer to be`
- numbered slides: `slidenumbers: true`
- auto-fit all text onto slides: `autoscale: true`
- show list bullets one by one: `build-lists: true`

I'm not going to demonstrate this one, because it'll make all the other examples too noisy.

---

# See also the official [cheatsheet](http://www.decksetapp.com/cheatsheet/)
