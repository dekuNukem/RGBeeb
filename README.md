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

More details and user manual on main article.

Buy one here.

It breaks out all the common voltages used in vintage computers (12V, 5V, 3.3V, -5V, -12V) so I can use it to replace the 40 year old power supply with a tendency to blow up.

I also added some convience features such as soft power button and power LED header, 4-pin fan headers with PWM speed control, addressable RGB(ARGB) support, fused outputs, and temperature probe fan curve.

It is also in 2.5 inch bay form factor so it can fit into this PC case, and is smaller0 than most retro computer PSUs, which it aims to replace.

the power button and LED header lets me plug the case header directly into it and control the power of the system.

As such, the ATX4VC will be in charge of controlling the power and RGB lighting in this project.


## Did anyone say RGB?

I did want to involve some RGB in this build, although it's slightly more difficult than usual. on a typical RGB build, the light comes from PSU, Memory, cpu, case, and water cooling fans.

unfortunately, the usual avenue falls a bit short here.

* we do have a RGB PSU, but its fan faces downwards, so not very visible

* nowhere to put RGB ram sticks

* fans are not required for the Beeb, and they aren't very effective in open-frame cases anyway

* I can try light strips, but they tend to be a bit tacky, and hard to conceal in open-frame cases

so all in all, the RGB situation wasn't looking too hot. however, I stumbled upon something much better instead.

while repairing a beeb motherboard, i shined a light from the back to check for solder bridges, the light passed through, beatifully liiminating the delicate and intricate design of all the traces on the circuit board. This is another happy coincidence that they did not use coppor ground planes or internal layers, both of which would block the light.

the idea of adding a RGB backlight behind the entire motherboard immediately came to mind, it would reuiqre a lot of LEDs and possibly a huge circuitboard, but if the result looks good, it's worth the trouble in my book.

Just for mockup, I cut some leftover RGB lightstrips to length and stuck them on the acrylic plate. the adhesives on those cheap strips are incrediably weak, still, they held just long enough so I can see how it looks like, and seeing it for the first time, it was incrediably striking, and I was in awe.

more descriptions? soft defussion, intricate design of the traces, etc.



I went ahead to design a whole new ATX adaptor plate, this time as a whole circuit board with RGB LEDs evenly distributed. I also left a cutout under the keyboard connector, so the cables can exit underneath and not block the backlight. I also used a USB-C connector to carry the ARGB signal, as it is much neater to use the regular USBC cable.

this is the biggest PCB I have ever designed, it is not very complicated, but did took me a while to solder all 168 LEDs by hand. Fortunately, everything lined up fine and it worked on the first revision, it gets blindingly bright when turned all the way up, and the motherboard looks amazing in front ot it, especially after adding different RGB animations. The light difusses nicely around the edge of the board, and the white case really makes the colour pop while remaining a classy and uncluttered wook, i'm exteremly happy with how it turned out. this kind of effects is simply not possible with modern moterhboards.


## USB Keyboards on BBC Micro?

With such a modern case, it's only natural that I want to use this BBC micro just like a real PC with USB keyboard and gamepad.

As if by total coincidence, I happen to have a project for exactly that! what are the odds!

The USB4VC project allows modern USB keyboards, mouse, and gamepads to be used on vintage computers. The modular design supports a wide range of computers with protocol cards. 

At the time of writing, P-cards are availble for IBM PC compatible(ps/2 keyboard/mouse, XT keyboard, serial mouse, 15pin gamepads) and apple macintosh lines. does it need to be this detailed?

Your can read more about the project here.

Anyway, I designed a new protocol card for the BBC Micro, supporting its keyboard and joystick.

the keyboard for BBC micro is a very clever piece of design, it can scan its matrix atonomously without CPU involvment, an interrupt is generated when keypress is detected, only then CPU starts to scan the matrix to see which key is pressed.

That means the timing is very tight once the 6502 starts keyboard query, I actually overclocked the microcontroller to be on the safe side, but in the end it does work rather nicely.

I also had to remap a few buttons since the keyboard layout is different on PC keyboards compared to BBC micro.

I used to on0board DAC for the joystick analog axies, which works fine, although careful calibration is needed to ensure the positiion is centred, as most games dont have calibration themselves.

The prototype p-card works fine with some bodge wires, and those will be fixed in the final version.

 
## Mounting floppy drives

another0 goal of this project is to have real working full-height 5.25" floppy drives in the case. I had two candidates, a 80-track shugart model ??? from the frankenbeeb, and a 40 track Tandon model ??? from a IBM PC XT. With both 40 and 80 tracks, it should cover the majority of floppys I want to read.

I added a ???? floppy controller0 chip and tested out the setup. After some trail and error it seems that for the dual floppy to work, the ribbon cable needs to have NO TWIST, and the drive ID set manually with the on-board jumper. a terminating resistor might also be needed at the last drive on the cable. 

The acorn DFS treats each side of a floppy as different drives, so physical Drive ID 0 will be DFS drive 0 and 2, while drive ID 1 will be drive 1 and 3.

I tested out the setup seperately, and it seemed to work, so now I need to figure out how to mount them on the case.

fortunately the case has plenty of slots near the font for mounting water cooling heatsinks and fans, and looks like a simple metal bracket is all that;s needed.

I went to the local hardware store and bought some angle brackets that looked close enough, I then measured and drilled the holes for the drive. A one-piece solid metal bracket would be preferable, but i wasnt able to find off-the-shelf parts, custom fabrication would have been a lot more expensive.

anyway, the drives mounts fine, however when I line up the faceplate of the drive with the front of the case, the connectors on the back of the motherboard prevents the ribbon cable from being inserted. Still, it;s not a showstopper, I can fix that along with a few other planned modifcations. 

Speaking of which...


## Motherboard modifications

A few modifications were carrid out on the motherboard, mostly for anesstenic reasons. they are completely optional and  entirely reversible, so keep that in mind if you want to try something similar yourslef.

### Power connector

BBC motherboard have power supply posts where the cable plugs into. in total there are three 5V and 3 GND posts, and a single -5V post. All your have to do is feed them the correct voltage.

the simpllist and non-destructive way is just

run wires directly to it from the ATX PSU, but it would creat some clutter0 and block the backlight, so I decided to go a bit further and desolder all the posts and run the cables on the back of the PCB. I used plenty of flux, added some new solder, and heated up the post and pulled it out. I then sucked the solder out of the hole, cleaned it up, and ran power cables to connect all the rails together.

make sure the cable you use is thick enough to carry at least 2A of current, and double check you didn't accidently cross the 5V and GND and short them. also make sure the exposed conductor is not shorting on nearby traces and components.

with the posts removed and new cabling in the back, I can now simply plug it into the terminal blocks on ATX4VC and power the motherboard that way.

### reLOCATING pin headers

As the connectors on the back of the motherboard were blocking the floppy drive, I simply desoldered and replaced them with straight headers. they will still work but takes less space. You The desoldering can be a bit harsh on the PCB, so dont do this unless you run into unavoidable space constrains.

I also desoldered the keyboard pin header and installed it upside down, so the long end is pointing downwards. this way I can connect the keyboard cable from behind through the cutout on the ATX RGB adaptor plate, elinating another item to block the backlight. anything for that clean look!

## Putting it all together

Time to finally put everything together! I gave the motehrbaord another wash to clean off the sticky flux residues, fed the floppy and power cable through the adaptor plate cutout to make sure they dont block backlight. I then mounteed the ATX4VC on the spare 2.5 inch drive bay. It fits nicely, and powers the RGB backlight and USB4VC through two USB-C cables.

the two floppy disk drives now fits perfectly with the header removed, although the power cable is just barely long enough.

I also uesd RGB2HDMI to upscale the video output to HDMI.

the turboMMC makes playing games even easier on BBC micro by booting from SD card with a interaction menu. and 

## conclusion

It;s amazing how quickly a simple idea can get out of hand, I started out just wanting to put a BBC micro mnotherboard into a ATX case, and in the end I developed a new protocol card for USB4VC, a general purpose ATX controller for vintage computers, and a custom RGB backlight plate adaptor. I took this idea and really pushed to see how far I can go.

none of this it toally necessary, it is still a plain old BBC micro with a slight upgrade and some disk drives. but just like the torch computer and the frankenbeeb, the whole ordeal of dragging it kicking and screaming to the 21st centry has made it much more special, and I guess this is what modification is all about.

originality is an important part of retro computing, and many classic machines had been butchered to put newer system in them. 

however, i do find many period modifications rather charming, such as the cursed mac, and I feel that if the process is non-destructive and reversible, i woulnd mind to have a bit of fun, especially with giving a bare motherboard a home instead of having it remain as spare parts.

still, i learned a lot about the history and clever design of this machine, and devloped something that hopefully benefits the community at large. and with everything put together, it looks every bit as good as i imaghined from the beginning.

As for what's next, i might add a torch Z80 card to add CP/M capability next, but to be honest, i spent so much time building this thing, I have't had much time actually enjoying the machine itself, so I guess that's what coming up next.


## putting it all together

