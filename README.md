# Pimp My Beeb

BBC Micro inside a open-frame ATX PC case 

!!MEDIA TODO: Photo of completed build, big wood tabletop, HDMI monitor, modern wireless mechanical keyboard, mouse, and Xbox Series X gamepad.

!!MEDIA TODO: GIF clip of the machine in action. overview, power up, closeup of animated backlit motherboard, using modern input devices.

## Highlights

* Fully functional BBC Micro inside open-frame ATX PC case

* Animated RGB Backlight

* Working dual full-height 5.25" Floppy Drives

* USB keyboard and gamepad ([via USB4VC](https://github.com/dekuNukem/USB4VC/blob/master/README.md))

* HDMI video out ([via RGB2HDMI](https://github.com/hoglet67/RGBtoHDMI))

* SD card support (TurboMMC)

* Working soft power and reset button

## BBC Micro: (A quick) Introduction

### History and Legacy

* In early 1980s, BBC started the *Computer Literacy Project*, aiming to introduce people to computers and show what they can do.

* **[Acorn Computer](https://en.wikipedia.org/wiki/Acorn_Computers)**'s design won out, and was developed into **[BBC Microcomputer](https://en.wikipedia.org/wiki/BBC_Micro)**, often nicknamed the "**Beeb**".

TAKE MY OWN PHOTO OF BBC MICRO, LOW ANGLE SO THE IT CAN BE CROPPED IS SHORT

* BBC Micro was featured heavily in [TV programmes](https://en.wikipedia.org/wiki/The_Computer_Programme), and became ubiquitous in education environments in UK.

![Alt text](photos/tv.png)

* A common sight in school computer labs, it introduced a whole generation to computing, and inspired many bright minds in related fields.

* Acorn went on to develop the **Acorn RISC Machine**, or [ARM](https://en.wikipedia.org/wiki/ARM_architecture_family) in short (Yes, *that* ARM), which are now found in virtually all smartphones, 32-bit microcontrollers, and even desktop PCs.

![Alt text](photos/arm.png)

* It might be relatively unknown outside UK, but BBC Micro holds a significant place in computer history, as well as nostalgia in many peoples hearts!

### Specifications

### Trivias

## Oh no! You butchered a piece of important computer history!

First of all, all modifications here are **non-destructive and reversible**. So no Beebs were harmed during the creation of this project!

What's more, modifying BBC Micros certainly was not unheard of even back then! One great example is the original [Torch Communicator](https://en.wikipedia.org/wiki/Torch_Computers):

![Alt text](photos/torch.jpeg)

A sleek business machine with integrated display, keyboard, and disk drives, running a version CP/M called CPN. What's not to like?

At this point, eagle-eyed viewers might notice the UI looks suspiciously familiar! The secret is revealed looking inside the case [thanks to this video](https://www.youtube.com/watch?v=pNdYtTvEAQs):

![Alt text](photos/torchinside.png)

Yep, they literally nicked the motherboard from a BBC Micro and built their own computer around it!

Despite the humble root, the Torch Communicator was a fairly advanced machine, having a Z80 co-processor running CP/M with networking capabilities, and it was the [first microcomputer](https://nosher.net/archives/computers/micro_decision_1982-05_002) to be fully approved by British Telecom for connection to the telephone and Telex network, in 1982!

Torch Computer went on to develop their [own machines](https://en.wikipedia.org/wiki/Torch_Computers#Torch_Triple_X) later. But this is a great example of building upon an existing computer to expand its capabilities.

## The FrankenBeeb

Of course, Beeb tinkering did not stop with commercial companies, apparently plenty enterprising users had a go as well!

Here is a machine I picked up locally via ebay:

![Alt text](photos/ebay.png)

It's a Beeb with ... a separate keyboard and hinged case??

The top half of the Beeb was replaced with a flat hinged lid, now resembling a small PC case. And the keyboard is now in its own metal enclosure with ribbon cable (???).

![Alt text](photos/case.png)

The new flat case most likely allows the computer, disk drive and monitor to be stacked on top each other, saving valuable desk space.

A look inside revealed big upgrades, fully kitted out with sidewise expansion card, floppy disc controller, battery backup, a standalone audio jack, and speech synthesis chips. And just look at all the ROMs!

The toggle switch is wired up to a jumper on the sidewise card, most likely for switching ROM banks.

![Alt text](photos/hinge.jpeg)

The disc drive features dual-80 track full height floppy drives, with some notes on the door:

![Alt text](photos/disc.jpeg)

There is no brand name or identifying information on any of the modifications, which led me to assume that the whole thing was home-made or at least from a kit.

Either way, it looks very professionally done, and is a seriously impressive feat of how far people would go to personalize their computers to their exact liking.

I removed the RIFA caps from the PSU, took lots of photos for documentation, cleaned up the PCB, and tested it out. It actually works! Look at the huge list of ROMs:

![Alt text](photos/roms.jpeg)

The disc drive works too! I decided not to risk the original power supply, and used a modern ATX PSU to power the drives. And the Beeb read the discs just fine:

![Alt text](photos/mess2.jpg)

As you can see, it's quite a mess indeed. It was at this point that an idea occurred to me:

***Wouldn't it be nice if all those can go into a single ATX PC case?***

* Everything's in one place, no more separate boxes.

* Juxtaposition of old and new. 40 year old hardware in cutting edge 

* very much in the spirit

## A Happy Coincidence?

That sure sounded like an outrageous idea, but after bit of thinking, I felt that it wasn't completely unrealistic.

* The 5.25" floppy drives are designed to go into 5.25" bays, so no problem there.

* BBC Micro motherboard needs +5V to work, which ATX PSU have.

* It also need -5V for sound and RS423 serial, but it can be easily derived from the -12V rail

So far so good, but what about the motherboard itself? I found a spare and did some measurements.

Imagine my surprise when I found that BBC micro motherboard has **almost identical size** to the full-size ATX specification!

PHOTO OF BEEB MB AND AN ATX MB, MAYBE SVG COMPARISON

![Alt text](photos/atxbbc.png)


BBC is 310mm x 230mm, and ATX is 305x244mm. Either it's one hell of a coincidence, or Acorn was so ahead of its time that it predicted ATX form factor 14 years ahead!

## Full Steam Ahead!

With that shocking revelation, there really isn't any hurdles left at all! I quickly designed an adapter plate. It screws into the case standoffs, and Beeb MB screws into that:

and made one out of hardboard: 

!!MEDIA TODO: Photo of bbc micro motherboard with hard board adapter plate side by side

!!MEDIA TODO: Photo of motherboard inside the shit PC case

I tried it out in my spare junk PC case, and as expected it fits fine! Most of the ports even line up with the I/O window! There are even space for the connectors in the back! Although this particular case is a bit too short, so the 5.25" drives would block the Tube and 1MHz connector.

Which brings us neatly to the question: What case *should* I use?

## Case Selection / a case of ???

Initially I wanted to use one of those absolutely obnoxious gaming cases kitted out with RGB peripherals for maximum hilarity:

!!MEDIA TODO: Photo of RGB CASE

I am NOT a fan of RGB at all, but 


self contained BBC micro with two disk drives inside a ATX case with PSU and working power buttons and LEDs just like a real PC.

mention really dont like RGB gaming builds, i find them obnoxious and pointless. all my pcs are under the desk and i dont look at them when i use them!

at first i wanted a obnoxious RGB esport gaming case just for the shit of it. something like the stuff people show off on pcmasterrace reddit:

!!MEDIA TODO: Photo of obnoxious gaming RGB PC builds

but as it turns out, to the shock and disappoint of dozens of retro computer enthusiasts, almost all modern PC case doesn't have 5.25 inch bay anymore! there is just a blank space there. those who did does not support full height drive anymore as well, as they are optimised for optical drives and have half-height drives that prevent full height drives to be inserted. 

!!MEDIA TODO: screenshots of PC cases on amazon or newegg or uk equivalent?

I want my dual full-height drives, that means four(!) 5.25 inch bays! and its safe to say i wasnt able to find any gaming cases on sale today with that.

I then decided to turn my attention to a little eariler, and got myself a case from early 2000s. A handsome looking aluminum coolermaster full-size case. it has 4 bays and everything i need. its a nice case for a period build but still leaves me a bit cold. the major theme of this build is to contrast the 40 years old computer with modern enclosure, and using a 20 years old case just wasnt going to cut it.

!!MEDIA TODO: Photo of my coolermaster case

then during another scrolling session of looking at PC cases, I stumbled upon something i never thought of: open-frame cases!

!!MEDIA TODO: screenshots of listings of open frame cases

striking design, minimalist and thoroughly modern
lots of space to work with, easier to work on than a cramped regular case
more flexible mounting not having to worry about side of the case and cutting stuff out
more visibility for the motherboard and internals since everything is on display
on-the-nose gaming image? perfect contrast

i looked at several designs, Thermaltake Core P3 TG Snow caught my eye the most:

!!MEDIA TODO: screenshots of Thermaltake Core P3 TG Snow case, go find it on the official website

really like the clean and modern look and customisable design, can be configured to stand up, lay down, or wall mounted. (look at more blurb here), and most importantly, there are slots at the right edge of the case for mounting water cooling radiator fans, which looks perfect for mounting full-height drives! it will probably need some custom bracket fabrication but we'll get to that.

theres a black one as well, i really like the white color, sets it apart from a sea of black boxs. black is so boring!

the clean and minimalist design of the case also changed my aesthetic plan a bit, was originally going to go full-on RGB blast, but now i wanted it to be a bit more subtle?

## Things to consider

Still 

## Mounting motherboard

I looked up ATX motherboard standard and measured the mounting holes on the BBC motherboard, and designed a simple adapter plate in inkscape, and had it cut out in acrylic. Much more ridgid than the hand drilled hardboard.

the case arrived, i had it roughtly assembled, and installed a second hand RGB PSU, to my annoyance the RGB fan points to the bottom so it will be pretty much invisiable, but still, at least its white too!

tried the adaptor plate, works fine and fits snugly.

!!MEDIA TODO: Photo of MB mounted on case, nothing else

Needed to remove tube connectors, write about low-temp alloy desoldering?

## power supply, ATX4VC

Another neat side effect of putting it in a PC case is that I can do away with the old power supply which tends to blow up if the RIFA capacitor is not removed. Modern ATX PSU had all the required voltages. now 

## Did anyone say RGB?

repair, intricate trace designs, would be very attractive to add backlight to the back of the motherboard. luckly the motherboard had no ground pours, making the traces extra visible. did a mockup by taping some RGB light strips, and it looked absolutly amazing.

the light strip had shit adhensives that starts to peel off after a day or two, and i dont really like the hand-soldered look anyway, might as well go all out, so i designed a new PCB adaptor plate with built in RGB backlight.

USB cable to carry power and data

## Floppy drives, mounting and configurations

now to how to mount the drive, there are a bunch of slots on the case, so a simple right angle metal bracket should be sufficient. i went to my local hardware store and bought some mounting brackets, to my surprise they almost fit with out much modification at all, al though i had to drill some holes at the longer side to mount the drive. in the future i probably should have a proper bracket frabricated.


floppy needs cable without twists

one shugart 80-track and one tandon 40-track (from a IBM PC!), should cover everything.

Molex connector just barely long enough.

## putting it all together

