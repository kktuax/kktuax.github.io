---
layout: post
title: "Introducing YouTuPi, a YouTube (mobile) web frontend for your Raspberry Pi"
tags: [youtube, raspbian, youtupi, raspberry-pi]
---

I've been the proud owner of a [Raspberry Pi](http://www.raspberrypi.org/) for several months now. Since I bought it, I've looking for ways of replacing all the functionalities my old TV-attached laptop had, which basically were: torrent downloader, DLNA server and [YouTube](http://www.youtube.com/) player. This device has a very low power consumption so this would be great news.

My first approach was to install [Raspbmc](http://www.raspbmc.com/) which is an [XBMC](http://xbmc.org/) optimized for this hardware. In spite of  XBMC is a great piece of software, in my case it was quite unresponsive, and made my Raspberry Pi hang several times.

This made me try [Raspbian](http://www.raspbian.org/) which is a very lightweight distribution. As it's based on [Debian](http://www.debian.org/), I installed [Transmission](http://www.transmissionbt.com/) and [MiniDLNA](http://minidlna.sourceforge.net/) with no much trouble using apt-get since they are in the repositories. At this point I was quite happy with the result: I had a torrent daemon I was able to control through its web-interface or even with an [android application](https://play.google.com/store/apps/details?id=com.neogb.rtac), and the downloaded media was played in my DLNA-capable TV.

## The hard part: playing YouTube videos on the TV

![Old TV with youtube]({{ "/assets/img/youtube-topic-page.jpg" | relative_url }})

Since flash has so little performance in linux playing YouTube videos from an internet browser was out of the question. Searching the web I found [YT](http://www.raspberrypi.org/phpBB3/viewtopic.php?t=8157): a command-line application written in python for searching YouTube videos and play them without flash thanks to [youtube-dl](http://rg3.github.com/youtube-dl/). This was pretty cool, but I was looking for a more user-friendly solution. Inspired by YT's approach I wrote YouTuPi which has a web interface that can be used in any modern tablet/phone and allow us to search and create a playlist of YouTube videos.

![Youtupi Screenshot]({{ "/assets/img/youtupi-screenshot.png" | relative_url }})

You can find the installation instructions (and the code itself) in [YouTuPi's GitHub repository](https://github.com/kktuax/youtupi).
