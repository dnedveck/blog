---
layout: post
title: Extrracting chords from songs
date: 2018-06-09
categories: music
---

## Background

So, I've got some songs that I want to learn how to play, but I'm not skilled enough to figure out their chord progression. I tried some online tools, but they were unable to pull from YouTube, and I had to pay if I wanted to upload my own MP3.

Turns out [Sonic Visualizer](https://www.sonicvisualiser.org) exists, and I can use it to extract chords with the Chordino plugin.

## installation and use

I'm using Ubuntu 18.04.

Download and install SonicVizualizer from the [downloads page](https://www.sonicvisualiser.org/download.html).

Find out that you need `librubberband2v5` -- turns out that it's not available for 18.04.

I found a [.deb](http://archive.ubuntu.com/ubuntu/pool/universe/r/rubberband/librubberband2v5_1.8.1-6ubuntu2_amd64.deb) for 17.10 at [reposcope.com](https://reposcope.com/package/librubberband2v5), and I decided to give it a shot to install.

Installed it, then Sonic Visualizer installed. 

Downloaded the Chordino plugin, extracted it, made a `vamp` plugins dir, and copied the .so file to it:

```bash
sudo mkdir /usr/local/lib/vamp

sudo cp nnls-chroma.so /usr/local/lib/vamp
```

Started Sonic Visualizer, loaded in an mp3. On the menu I selected Transform > Analysis by Category > Chordino: Chord Estimate, and went with the defaults on the screen that popped up. It ran for a bit, and generated some chords. 

Nice.

*Thanks to [JHoermann for the video](https://www.youtube.com/watch?v=bQrleXXQmWY) that got me started on this.*
