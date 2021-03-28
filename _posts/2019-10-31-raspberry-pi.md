---
layout: post
title: Raspberry Pi
date: 2019-10-31
---

![](/assets/posts/2019-10-31-raspberry-pi.jpg)

Recently purchased a Raspberry Pi to tinker around with as a small remote server. I wanted to learn a bit about home networking and home labs, even if it is at a tiny scale.

Since the first Raspberry Pi was released in 2012, I've been fascinated. A computer with a footprint the size of a credit card? No way! I've always wanted to get my hands on one to experiment with and see what I could do on a machine with limited hardware. There is also something appealing about the idea of a tiny cluster of Raspberry Pi boards that you can hold in one hand—No one else? Just me? Okay.

Choose to go with the Raspberry Pi 3 Model B+ because it came with a full HDMI port. Although the RP4 is the latest generation, I didn't want to commit to also needing to get another cable for its Micro-HDMI port to connect to my monitor. Also, I've heard that the RP4 had some issues with power because the USB-C connector does not adhere to specifications—so the board was not recognizing some chargers. I didn't want to deal with that headache.

Anyway, the RP3 is a neat little package so far.

## Installation

1. Installed [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) on a MicroSD card.
2. Assembled Raspberry Pi.
3. Installed Raspbian by following on-screen prompts.
4. Ran updates:

```
# Download package list for repositories:
> sudo apt-get update

# Download up-to-date packages from repositories:
> sudo apt-get upgrade

# Distribution upgrades:
> sudo apt-get update
> sudo apt=get dist-upgrade
```

Can also combine commands:

```
sudo apt-get update && sudo apt-get upgrade -y
```

## Remove Default Packages

I had installed Raspbian with desktop and recommended software included, but, in hindsight, I should have just installed Raspbian Lite instead. I wanted a barebones Raspbian to work with, and the Lite version would have saved me the trouble of going through this next step:

```
sudo apt-get purge libreoffice* minecraft-pi woflram-engine -y
```

I removed packages that I wasn't going to use. For some reason, many packages couldn't be removed from the command line, so I had to use the GUI package manager to deal with them.

When installing and updating packages, cache data is kept and gets bigger and bigger. Need to clear the cache:

```
# Clear cache:
> sudo apt-get autoclean

# Remove unused packages:
> sudo apt-get autoremove -y
```

## Enable SSH

First have to enable SSH on the Raspberry Pi:

```
sudo raspi-config
```

Find the SSH configuration settings. Apparently, from what I've read, Raspbian developers move this setting around sometimes through updates. Then, reboot the Pi to make this change permanent:

```
sudo reboot
```

Find the IP address for your Pi on your network:

```
sudo ifconfig
```

Since I use Windows on my primary computer, I had to download [PuTTY](http://www.putty.org/). To clarify, Windows does not have built-in support to execute `.sh` files. PuTTY is one of the numerous third-party SSH clients for Windows. Enter the IP address for the Pi from earlier, then open the connection. This will give you a warning (the first time) and then prompt you for the user (`pi`) and password (`raspberry`).

Now you can remotely connect to your Raspberry Pi.
