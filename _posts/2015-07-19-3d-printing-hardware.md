---
layout: post
title: "3d printing hardware"
description: "overview of hardware that i use to 3d print all the things"
category: printing
tags: [hardware,plastibot,3dprinter,arduino,raspberry-pi]
---
{% include JB/setup %}

Since I started this blog to write (primarily) about 3d printing, it only makes sense that the first post covers my setup. This post will cover the hardware I use. I'll write a separate post that covers the software.

## the printer

Once upon a time, I used my brain for both hardware and software problems, so naturally I thought, instead of buying a ridiculously overpriced printer, I should look into building one. One of my friends recommended that I check out [plastibot][plastibot], and it was an amazing find. I reviewed the [Plastibot Mendel specifications][plastibot-specs] and they seemed right up my alley. I was also amazed to see that the [instructions][plastibot-assembly] for assembling the printer were freely distributed on the interwebs. Luis (the gentleman who runs Plastibot) has also made available all the STL files he uses to print your 3d printer ahead of the weekend course on [github][plastibot-github], and he accepts pull requests!

I signed up for a weekend express course, which is 20 hours split between Saturday and Sunday, and left with a working 3d printer! I wasn't thinking far enough in advance to take pictures as I was assembling the printer, but here's the final product:

![plastibot mendel 3d printer](/assets/images/plastibot-mendel-3d-printer.jpg)

I selected the heated bed so that I could print ABS or PLA (though I primarily print ABS, which is covered further on), and I sprung for the acrylic frame for no good reason other than it looks cool (though a pretty strong case for mitigating the warping that may occur to a plywood frame could be made).


## the controller

The 3d printer controller is the [RepRap Arduino Mega Pololu Shield (RAMPS)][ramps]. It was easy to setup (covered in the final set of assembly instructions on the plastibot site) for the base configuration, and I liked the extensibility of being able to eventually add another extruder head or even hooking up an LCD monitor so as to not use my computer for pushing print instructions to the controller. Naturally I did none of these things, as I went the route of using a raspberry pi to make my 3d printer into a _wireless_ 3d printer, but it was nice to know it was there.


## the interface

Initially, I installed pronterface software on my computer (covered in the software overview) to interface with the RAMPS controller, but decided I didn't like losing my computer for however many hours a print would take. So I looked around and discovered [OctoPi][octopi], a [raspberry pi][raspberry-pi] distribution for 3d printers. I'll cover octopi more in the software overview, but for hardware, I run octopi on the [raspberry pi 2 model b][raspi-two-model-b]. Absolutely worth it:
* Quadcore CPU
* 1GB of RAM
* Expanded GPIO pins
* Micro SD slot (so no more awkward half the SD card hanging off the board!)
* Additional USB ports (this was huge for me since I upgraded from v1 and had 2 USB ports originally)

![raspberry pi 2 model b](/assets/images/raspberry-pi-two-model-b.jpg)

## the plastic

I usually order 3mm ABS plastic filament from [ultimachine][ultimachine]. They were recommended to me while I was building my 3d printer, and I've never had a problem with their plastic. I've also read some [interesting articles on using ABS vs PLA][comparison-abs-vs-pla], but for my applications I'm happy to generally stick with ABS.


## future posts

I'll (eventually) write separate posts for the hardware upgrades I've done. That includes:
* raspberry pi camera module
* lcd + keypad pi plate
* 3d-printed case for raspberry pi 2

and probably some other crap I haven't thought of yet.

[plastibot]: http://www.plastibot.com/
[plastibot-specs]: http://www.plastibot.com/plastibot-mendel-3d-printer/
[plastibot-assembly]: http://www.plastibot.com/assembly-instructions/
[plastibot-github]: https://github.com/plastibot/Plastibot-Mendel
[ramps]: http://reprap.org/wiki/Arduino_Mega_Pololu_Shield
[octopi]: https://github.com/guysoft/OctoPi
[raspberry-pi]: https://www.raspberrypi.org/
[raspi-two-model-b]: https://www.raspberrypi.org/products/raspberry-pi-2-model-b/
[ultimachine]: https://ultimachine.com/
[comparison-abs-vs-pla]: http://www.protoparadigm.com/news-updates/the-difference-between-abs-and-pla-for-3d-printing/
