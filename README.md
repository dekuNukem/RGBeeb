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


BBC is 310mm x 230mm, and ATX is 305x244mm. Either it's one hell of a coincidence, or Acorn was so ahead of its time that it predicted ATX form factor **14 years** ahead!

Still in disbelief, I placed a spare BBC motherboard inside a random ATX case, and low and behold, it fits almost perfectly!

!!MEDIA TODO: Photo of motherboard inside the shit PC case, NEW PHOTO better illustrates the point.

The RGB, cassette, serial, composite and RF ports even line up with the I/O window! And there are also space for all the connectors in the back! This is almost too good to be true.

Although in this particular case(!!), the PCI bracket is blocking the analogue and econet port, and 5.25" drives won't fit since is a bit too short.

Which brings us neatly to the question: What case *should* I use?

## Case Selection

Initially, I wanted one of those absolutely obnoxious gaming cases kitted out with RGB peripherals like something straight out of r/pcmasterrace, just for maximum hilarity.

!!MEDIA TODO: Photo of RGB CASE, and a photo from PCMR reddit

So I set out to look for a case that's:

* I can buy brand new

* Full size ATX or larger

* Gaming aesthetics (RGB, Glass panel, etc)

* Has four 5.25" bays for two full-height disk drives

Didn't seem like a tall order, but after sifting through dozens of pages on amazon and newegg, I came to the devastating conclusion such case *simply doesn't exist anymore*.

The main culprit is 5.25" bays. I need 4 of them to hold the two drives, and they are simply extinct from most modern gaming cases. Instead there is just a blank space where it used to be.

Just when I thought modern cases were a dead end, I stumbled upon something I completely missed: **open-frame cases**!

Some of them are basically some scaffolding for mining rigs, but one particular case really caught my eye, the Thermaltake Core P3 TG Snow:

!!MEDIA TODO: screenshots of that case

* I really like its striking yet minimalist design, juxtapose neatly with 1980s technology, and also a nice break from the today's bland "gaming black".

* It puts the motherboard on display front-and-center, instead of having to look through a window into a box in conventional cases. Much less claustrophobic.

* There are lots of space to work with, and everything is modular. PCI bracket blocking the ports? Simply don't install it!

* And most importantly, the mounting holes for water cooling fans are perfect for mounting 5.25" inch drives! I doubt they'll line up but I can always make a bracket.

It's not cheap, but I really see it as the ideal case for this project, so I ordered one.

The clean and minimalist design also changed my mind about the overall aesthetics. Instead of full-on obnoxious RGB blast, now I kind of want something more subtle and tasteful. It's still early, so I'll see what happens.

## Mounting motherboard

I looked up ATX standard, and measured the mounting holes on the BBC motherboard. A simple adapter plate was designed in Inkscape and laser-cut in acrylic.

The case soon arrived, I had the main chassis laid out, installed ATX standoffs, and tried out the adapter plate:

!!MEDIA TODO: Photo of MB mounted on case, nothing else

It works! And already looks pretty good!

I then installed the ATX PSU with RGB fans and modular cables. To my annoyance the RGB fan points downwards, so it is practically invisible with the case standing up. Anyway, at least it's white!

Which brings us neatly to the next question: How are we going to power the motherboard?

## Power to the Beeb

BBC Micro motherboard only requires two voltages: +5V and -5V. The former is all that's needed for the system to work, and the latter is only used for sound and serial communication.

Fortunately, 5V is readily available on a ATX PSU, and -5V can be derived from -12V with a simple 7905 linear regulator. The PSU itself can be turned on or off by shorting the green PWR_ON signal to ground. So nothing particularly difficult here. 

One slight issue is that I want to use the power button on the PC case, which is momentary. That means I can't just hook it up to the PWR_ON pin, because it will only turn on while the button is held down.

I thought about using a simple flip-flop to toggle the PWR_ON signal with button presses, and it rather quickly got out of hand. How about putting it on a PCB? What about button denouncing? I can put the 7905 regulator on there too! Might as well break out all the voltages! A fan header would be useful! What about RGB?

## Enter USB4VC

In the end, I decided to go all out and design a PCB specifically for using **ATX power supply on retro computers**.

I call it ATX4VC, and it covers lots of

* All voltages in one place: +12V, +5V, +3.3V, -5V, -12V

* Fused output on +12V, +5V and +3.3V, using common car fuses.

* Two 4-pin fan headers with PWM speed adjustment

* DS18B20 temperature probe support

* Fan speed: manual or temperature dependent

* Two ARGB headers for fans and light strips, etc.

* 2.5 inch form factor

It went though A LOT of revisions, mostly refining the details and adding new features.

More details and user manual on main article.

Buy one here.

## Did anyone say RGB?

repair, intricate trace designs, would be very attractive to add backlight to the back of the motherboard. luckly the motherboard had no ground pours, making the traces extra visible. did a mockup by taping some RGB light strips, and it looked absolutly amazing.

the light strip had shit adhensives that starts to peel off after a day or two, and i dont really like the hand-soldered look anyway, might as well go all out, so i designed a new PCB adaptor plate with built in RGB backlight.

USB cable to carry power and data

## Keyboards and gamepads

## Motherboard modification

## Floppy drives, mounting and configurations

now to how to mount the drive, there are a bunch of slots on the case, so a simple right angle metal bracket should be sufficient. i went to my local hardware store and bought some mounting brackets, to my surprise they almost fit with out much modification at all, al though i had to drill some holes at the longer side to mount the drive. in the future i probably should have a proper bracket frabricated.


floppy needs cable without twists

one shugart 80-track and one tandon 40-track (from a IBM PC!), should cover everything.

Molex connector just barely long enough.

## putting it all together

