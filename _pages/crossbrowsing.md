---
title: Cross-browsing, resolutions and devices
---

# Cross-browsing

Cross-browser compatibility is the ability of a website or web application to function across different browsers and degrade gracefully when browser features are absent or lacking.

## Tools for crossbrowsing

{%include components/tag-default.html %}
Our main tool to test websites and apps in different browsers and devices is [Browser Stack](https://www.browserstack.com/).

### From where to start?

Take a look at the global browser usage stats:

- [W3C - Browser Statistics](https://www.w3schools.com/browsers/default.asp): Quick look at most used browser and his release version
- [Global Web Stats](https://www.w3counter.com/globalstats.php): It offers rankings on most popular browsers but also devices, platforms and resolutions
- [Browser Market Share Worldwide](https://gs.statcounter.com/browser-market-share): Focused stats on country and device 

Refer to the project GA dashboard traffic stats (browsers, resolutions, devices).

#### Browsers

At SIRIS, we follow standard, beyond the popular browsers and their minimun release version coverage, it is recommended to ask [Can I use it?](https://caniuse.com/) when integrating code.

#### Resolutions

Follow the standard [Media queries for standard devices](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/), check the stats and configure the CSS mediaqueries

#### Devices & OS

Linked to browsers and resolutions testing on most popular "real" devices and platforms with [Browser Stack](https://www.browserstack.com/)