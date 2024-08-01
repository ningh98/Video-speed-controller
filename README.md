# Video-speed-controller

This is a 30-days javascript grinding  
js30 [https://github.com/ningh98/js30]  
28. Video-speed-controller [https://github.com/ningh98/Video-speed-controller]

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)



## Overview

The document creates a simple "Video Speed Scrubber" interface that allows users to adjust the playback speed of a video by moving their mouse over a speed control bar. The interface consists of a video player and a speed control area that dynamically updates the video's playback speed.

### Screenshot

![](./screenshot.png)


### Links

- Live Site URL: [https://ningh98.github.io/Video-speed-controller/]

## My process

### Built with

- HTML
- CSS
- Javascript



### What I learned



```js

  const speed = document.querySelector('.speed')
  const bar = speed.querySelector('.speed-bar')
  const video = document.querySelector('.flex')

  speed.addEventListener('mousemove', function(e){
    const y =e.pageY - this.offsetTop
    const percent = y / this.offsetHeight
    const min = 0.4
    const max = 4
    const height = Math.round(percent * 100) + '%'
    const playbackRate = percent * (max - min) + min
    bar.style.height = height
    bar.textContent = playbackRate.toFixed(2) + 'x'
    video.playbackRate = playbackRate
  })


```
