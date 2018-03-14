# Flavour CSS

Flavour is a utility, dekstop first scss library made and maintained [@thinkingjuice](https://thinkingjuice.co.uk). The idea is that it is utility first and grew from a natural movement towards using small classes to control simple styles allowing us to iterate on feedback quickly without any unwanted side effects.

Heavy inspiration has been taken from [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/) and [tailwindcss](https://tailwindcss.com/)

**tailwind has a great [write up](https://tailwindcss.com/docs/what-is-tailwind/) on how it works, if you want to know ideas and more I suggest you check it out until a more comprehensive write here has happened**


## History
The approach that this first took started off from seperating our scss into folders of varying complexitity. This was a big thanks to the concept of [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/) by [Harry Roberts (CSS Wizardry)](https://csswizardry.com/), at the time it was great and we still enjoy the structure, it was a significant step over what we had before.

Slowly overtime as a team we started to write smaller and smaller single use classes allowing us to have finer control over how things were displayed. We have now decided to go all in on this utility first approach.

## This just inline css?
You're not wrong to think this. 

In a way it is, however with css you have the power of media queries, written correctly you can control any utility easily at any given breakpoint and this is what we do here. Using prefixes you can easily see and control padding, margin, widths, display properties and more with ease at any time.

## I don't like adding lots of classes to my html/templates
Thats fair enough, if you'd like to get around that then you can make your own components and apply the styles, it's really up to you how you'd like to do it. If you do, we suggest just like tailwind suggest to use the pre-existing utility classes using @extend to generate components based from the utility classes.

## Controlling file size
Since we've generating a big stylesheet of utility classes you can end up with quite a big css file. To get around this we recommend using a css tool to examine your templates and clean your css of all un-used css. Be careful though because these tools won't have any concept of dynamic classes so, you'll need to account for this.

Just like [tailwindcss (controlling filesize)](https://tailwindcss.com/docs/controlling-file-size), we recommend [purgecss](https://github.com/FullHuman/purgecss), this works real nice in webpack/gulp etc. You can find out more with our webpack/gulp setup which will be available soon. This will allow you to whitelist classes and account for the special characters that we use in Flavour CSS.