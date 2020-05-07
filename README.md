# Project 3: From Portland to Portland

### Overview
* Intro
* Figma
* Images
* Typography
* Mobile-first
* Use of `calc()`

## Intro
This is a project about traveling across the US. It was designed to make full use of skills in responsive web development, as taught in Practicum by Yandex's Web Developer course.

## Figma
Project design specifications were outlines in Figma. [Link to the project on Figma](https://www.figma.com/file/lNsn9aE1Be6bvg9FeAzRXT/Sprint-3-From-Portland-to-Portland-desktop-mobile?node-id=0%3A1)

## Images 
All images were exported directly from Figma file and compressed at [tinypng.com](https://tinypng.com).

## Typography
Font-family is *Inter*, downloaded from [this site](https://rsms.me/inter/).
All text was smoothed, size-adjusted, and rendered for legibility.

## Mobile-first
I used the *mobile-first* approach, setting styles initially for 320px viewport width before applying necessary media queries and calculations for larger screen sizes.

## Use of calc()
Frequented a calculation to keep smooth element scaling relative to viewport width:

```
calc(minsize-v + (maxsize - minsize) * ((100vw - [minwidth-v])/(maxwidth - minwidth)))
```

The *minsize* and *maxsize* above relate to element size and the *midwidth* and *maxwidth* relate to viewport size, with *-v* indicating value denomination in the calculation.

Example: 
```CSS
.intro__subtitle {
  width: calc(720px - 30 * ((100vw - 768px)/256));
  max-width: 690px;
}
```
This formula allowed me to set dynamic measurements that were constantly relative to screen size but also gave me control to meet the breakpoint guidelines in the design spec.
