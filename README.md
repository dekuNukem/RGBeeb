# Pimp My Beeb

How I built the **RGBeeb**, a BBC Micro inside a PC case.

With RGB Backlight, USB inputs, ATX PSU, and working full-height floppy drives.

![Alt text](photos/moneyshot.jpeg)

![Alt text](photos/header.gif)

[Click me for a short video!](https://www.youtube.com/watch?v=R9k7dgKrrnE)

## Highlights

* Fully functional BBC Micro inside open-frame ATX PC case

* Animated RGB Backlight

* Working dual full-height 5.25" Floppy Drives

* USB keyboard and gamepad [by USB4VC](https://github.com/dekuNukem/USB4VC/blob/master/README.md)

* ATX power and RGB control [by ATX4VC](https://github.com/dekuNukem/ATX4VC)

## Questions or comments?

Feel free to ask in my [Discord Chatroom](https://discord.gg/T9uuFudg7j), raise a [Github issue](https://github.com/dekuNukem/RGBeeb/issues), or email `dekunukem` `gmail.com`!

## BBC Micro: (A quick) Introduction

![Alt text](photos/mybeeb.jpeg)

* In early 1980s, British Broadcasting Corporation(BBC) started the *Computer Literacy Project*, aiming to introduce people to computers and show what they can do.

* **[Acorn Computer](https://en.wikipedia.org/wiki/Acorn_Computers)**'s design won out, and was developed into **[BBC Microcomputer](https://en.wikipedia.org/wiki/BBC_Micro)**, often nicknamed the "**Beeb**".

* BBC Micro was featured heavily in [TV programmes](https://en.wikipedia.org/wiki/The_Computer_Programme), and became ubiquitous in education environments in UK.

![Alt text](photos/tv.png)

* A common sight in school computer labs, it introduced a whole generation to computing, and inspired many bright minds.

* Acorn went on to develop the **Acorn RISC Machine**, or [ARM](https://en.wikipedia.org/wiki/ARM_architecture_family) in short (Yes, *that* ARM), which are now found in virtually all smartphones, 32-bit microcontrollers, and even desktop PCs.

![Alt text](photos/arm.png)

* It might be relatively unknown outside UK, but BBC Micro holds a significant place in computer history, as well as nostalgia in many peoples hearts!

### Specifications

The original Beeb featured a 6502 microprocessor running at 2MHz, 32K of ROM, and either 16 or 32K of RAM. Its [BASIC interpreter](https://en.wikipedia.org/wiki/BBC_BASIC) was notably one of the fastest of the era, beating even the original IBM PC!

It was also extremely expandable, with a plethora of ports including RS423, cassette, analogue, Econet, a digital user port, a 1MHz bus connection, and a "Tube" expansion slot.

As a result, the Beeb was surprisingly long-lived, lasting more than 10 years. Numerous [upgrades and coprocessors](https://en.wikipedia.org/wiki/BBC_Micro_expansion_unit#ARM_Evaluation_System) were developed, including Z80, 32016, 80186, or even the very first ARM CPU!

## Oh no! You butchered a piece of computer history!

First of all, all modifications here are **non-destructive and reversible**. So no Beebs were harmed during the creation of this project!

What's more, modifying BBC Micros was not unheard of even back then! One great example is the original [Torch Communicator](https://en.wikipedia.org/wiki/Torch_Computers):

![Alt text](photos/torch.jpeg)

A sleek business machine running CP/M with integrated display, keyboard, and disk drives. What's not to like?

At this point, eagle-eyed viewers might notice the UI looks suspiciously familiar! The secret is revealed looking inside the case [thanks to this video](https://www.youtube.com/watch?v=pNdYtTvEAQs):

![Alt text](photos/torchinside.png)

Yep, they literally nicked the motherboard from a BBC Micro and built their own computer around it!

Despite the humble root, the Torch Communicator was a fairly advanced machine, having a Z80 co-processor running CP/M with networking capabilities, and it was the [first microcomputer](https://nosher.net/archives/computers/micro_decision_1982-05_002) to be fully approved by British Telecom to connect to the telephone and Telex network, in 1982!

Torch Computer went on to develop their [own machines](https://en.wikipedia.org/wiki/Torch_Computers#Torch_Triple_X) later. But this is a great example of building upon an existing computer to expand its capabilities.

## The FrankenBeeb

Of course, Beeb tinkering did not stop at commercial companies, plenty enterprising users had a go as well!

Here are eBay photos of a machine I picked up locally (with authentic 70s carpet):

![Alt text](photos/ebay.png)

It's a Beeb with ... a separate keyboard and boxy case??

The top half of the Beeb was replaced with a flat lid. And the keyboard is in its own metal enclosure with a ribbon cable (???).

![Alt text](photos/case.png)

The new boxy case most likely allow the computer, disk drive and monitor to be stacked on top each other, saving valuable desk space.

A look inside revealed big upgrades, fully kitted out with sidewise expansion card, floppy disc controller, battery backup, a standalone audio jack, and speech synthesis chips. And just look at all the ROMs!

![Alt text](photos/hinge.jpeg)

The disc drive contains dual 80 track full height 5.25" floppy drives, with some notes on the door:

![Alt text](photos/disc.jpeg)

There is no brand name or identifying information anywhere on the modifications, which led me to assume that the whole thing was home-made or at least from a kit.

Either way, it looks very professionally done, and is a seriously impressive feat of how far people would go to personalize their computers to their exact liking.

I removed the RIFA caps from the PSU, took lots of photos for documentation, cleaned up the PCB, and tested it out. It actually works! Look at the huge list of ROMs:

![Alt text](photos/roms.jpeg)

The disc drive works too! I decided not to risk the original power supply, and used a modern ATX PSU to power them. The FrankenBeeb read the discs just fine:

![Alt text](photos/mess2.jpg)

As you can see, it's quite a mess indeed. It was at this point that an idea occurred to me:

***Wouldn't it be nice if all those can go into a single ATX PC case?*** 

This way,

* Everything's in one place, cleaner look.

* Interesting juxtaposition between 40-year-old hardware and modern case.

* Very much in the spirit of wacky modding of the era.

* Honestly, why not?

## A Happy Coincidence?

Obviously, the most important part is mounting the motherboard. So I did some measurements.

Imagine my surprise when it turns out the BBC micro motherboard is **almost identical in size** as full-size ATX!

![Alt text](photos/comp.png)

Either it's one hell of a coincidence, or Acorn was so ahead of its time that it predicted ATX form factor by **14 years**!

Still in disbelief, I placed the BBC motherboard inside a ATX case, lo and behold:

![Alt text](photos/mock.jpeg)

It fits almost perfectly! The RGB, cassette, serial, composite and RF ports line up with the I/O window, and there are space for all the connectors in the back! This is almost too good to be true.

Although in this particular case(!!), the PCI bracket is blocking the analogue and econet port, and the long 5.25" drive doesn't go all the way in.

Which brings us neatly to the next part: What case *should* I use?

## Case Selection

Initially, I wanted one of those absolutely obnoxious gaming cases kitted out with RGB straight out of [r/pcmasterrace](https://old.reddit.com/r/pcmasterrace/), just for maximum hilarity. Something [like this:](https://old.reddit.com/r/gamingpc/comments/jb8w25/just_rgb_everything/
)

![Alt text](photos/pcmr.jpg)

So I went to look for a case that's:

* Available new

* Full size ATX or larger

* Gaming aesthetics (RGB, Glass panel, etc)

* Has 5.25" bays for two full-height disk drives

It didn't seem like a tall order, but after sifting through dozens of pages on amazon and newegg, I came to the devastating conclusion such case ***simply does not exist anymore***.

![Alt text](photos/cases.png)

As you can see, apparently 5.25" bays just isn't a thing anymore! Instead there is a blank space where it used to be, to the horror of *dozens* of retro modding enthusiasts.

(yes I know there's a case with 2 bays right in that photo, but I need 4 for two drives)

-----

Just when I thought modern cases were a lost cause, I stumbled upon something I completely missed: **open-frame cases**!

Some of them are just scaffolding for mining rigs, but one in particular really caught my eye, the [Thermaltake Core P3 TG Snow](https://uk.thermaltake.com/core-p3-snow-edition.html):

![Alt text](photos/p3.png)

* I really like its striking yet minimalist design, juxtapose neatly with the 1980s technology. It's also a nice break from today's rather bland "gaming black" aesthetics.

* It puts the motherboard on display front-and-center, instead of having to look through a window into a box in conventional cases. Less claustrophobic.

* There are lots of space to work with, and everything is modular. PCI bracket blocking the ports? Simply don't install it!

* And most importantly, the slot cutouts near the front edge are perfect for mounting 5.25" inch drives!

The clean and minimalist design also changed my mind about the overall aesthetics. Instead of full-on obnoxious RGB blast, now I want something more subtle and tasteful. It's still early, so I'll see what I can do.

It's not cheap, but I really liked it, so I ordered one.

## ATX Adapter Plate

I looked up ATX standard, and measured the mounting holes on the BBC motherboard. A simple adapter plate was designed in Inkscape and laser-cut in acrylic.

![Alt text](photos/acrylic.png)

The case soon arrived, I had the main chassis laid out and tried out the adapter plate:

![Alt text](photos/testmount.jpeg)

It works! And already looks pretty good! I really like how modular this case is. 

I then installed the ATX power supply. Annoyingly its RGB fan points downwards, so it is practically invisible with the case standing up. But at least it's white!

![Alt text](photos/atxpsu.jpeg)

## Power to the Beeb

BBC Micro motherboard requires two voltages: +5V and -5V. The former powers all the chips, and the latter only for sound and serial communication.

Fortunately, 5V is readily available on a ATX PSU, and -5V can be derived from -12V with a simple 7905 linear regulator. The PSU itself can be controlled by shorting the green PS_ON signal to ground.

The most basic circuit would be something like this:

![Alt text](photos/basiccircuit.png)

One slight issue is that I want to use the power button on the PC case, which is momentary. That means I can't just hook it up to the PS_ON pin, as it will only turn on while the button is held down.

I thought about using a simple flip-flop to toggle the PWR_ON signal with button presses, and it quickly got out of hand. How about putting it on a PCB? What about button debouncing? I can put the 7905 on there too! Might as well break out ALL the voltages! A fan header would be useful! What about RGB?

## Enter ATX4VC

In the end, I decided to go all out and design a controller specifically for using **ATX power supply on retro computers**, amply named **[ATX4VC](https://github.com/dekuNukem/ATX4VC/blob/master/README.md)**:

![Alt text](photos/atx4vc.jpeg)

It combines many convenient features in one place:

* All common voltages: +12V, +5V, +3.3V, -5V, -12V. Fused.

* Power button and power LED headers

* Two 4-pin PWM fan headers

* Two Addressable RGB (ARGB) headers

* USB-C power output

[Click me for learn more / buy one / user manual](https://github.com/dekuNukem/ATX4VC/blob/master/README.md)

Altogether, it's an all-in-one package for replacing old unreliable (and sometime explosive!) power supplies with modern ATX PSUs, with provision for cooling and aesthetic upgrades.

--------

It also fits neatly in a 2.5 inch drive bay, I hooked up the power button and LED headers, as well as a fan, and pressed the button.

![Alt text](photos/fantest.jpeg)

It works! PSU turns on, fan spins and lights up, and voltage rails are live.

We still need to connect it to the motherboard though, which will come later.

## Did anyone say RGB?

I do want to involve some RGB in this build, usually they come from RGB fans, RAM sticks, or light strips, none of which are really suitable here:

* Beeb doesn't need fan cooling, and it's a bit silly to add them just for looks.

* Same with RGB RAM sticks

* I can try light strips, but they tend to be a bit tacky, and hard to conceal in open-frame cases

So all in all, the RGB situation wasn't looking too hot. However, I did find something much better!

----

Ground planes and large copper pours really didn't become popular until late 80s, which means the earlier circuit boards are basically translucent. If you shine a light from behind, it will illuminate the delicate and intricate design of all the traces on the PCB.

And here, I want to expand the idea by **adding RGB backlight behind the entire motherboard**, it would require a lot of LEDs, but if it looks good, it's worth the trouble in my book.

For mockup, I stuck some RGB light strips on the acrylic plate, and hastily wired them together.

![Alt text](photos/mockrgb.jpeg)

Seeing it for the first time, I was in awe.

![Alt text](photos/rgbtest.jpeg)

What a sight to behold! And this is just a solid white, should be even more striking with animations and more colours.

I could have just used that, but it was rather messy, so I designed a whole new custom PCB with evenly distributed RGB LEDs, that also function as the ATX adapter plate. I also left a hole in the middle so cables can exit underneath and not block the light. 

I used **USB-C** to carry the ARGB signal. Often used for charging, it is already designed to carry decent amount of current. A single cable plugs directly into ATX4VC, much cleaner this way.

![Alt text](photos/rgbplate.png)

This is the biggest PCB I have ever designed, it is not very complicated, but did take me a while to solder all 168 LEDs by hand. Fortunately, everything worked on first try, and it gets blindingly bright when turned all the way up!

![Alt text](photos/rgbtable.jpeg)

How does it look like with the motherboard? Well:

![Alt text](photos/rgbcasetest.jpeg)

![Alt text](photos/rgbcloseup.jpeg)

Now **that's** what you call R, G, and B!

## USB on BBC

With power and RGB sorted, what's the next must-have item on a modern PC?

Why yes, **USB keyboard, mouse, and gamepads** of course! With such a modern case, it's only natural that I use it with modern inputs!

As if by total coincidence, I happen to have a project for *exactly that*! What are the odds?

![Alt text](photos/usb.jpeg)

[USB4VC](https://github.com/dekuNukem/USB4VC/blob/master/README.md) let you **use USB keyboard, mouse, and gamepads on retro computers**, as an alternative to rare, expensive, and unreliable proprietary vintage peripherals.

With a modular design, different computers are supported by swapping out **Protocol Cards**.

Naturally, I made one for the Beeb, with connectors for keyboard, joystick, and AMX user port mouse.

![Alt text](photos/pcard.jpeg)

The prototype has a few bodge wires, but they are fixed in the latest revision. And it works!

![Alt text](photos/pcardtest.gif)

Pretty fun using a wireless keyboard and Xbox controller on the Beeb!

And if for some reason you literally can't even be bothered to *type*, you can always let [duckyPad](https://github.com/dekuNukem/duckyPad/blob/master/README.md) do it!

![Alt text](photos/ducktype.gif)

duckyPad is a hot-swap mechanical macropad that helps speed up workflow by automating actions using duckyScript.

![Alt text](photos/duck.jpeg)

Read more about [USB4VC](https://github.com/dekuNukem/USB4VC/blob/master/README.md) and [duckyPad](https://github.com/dekuNukem/duckyPad/blob/master/README.md) if you're interested!

------

Phew! Two plugs in a row! Really pushing it there! 😅

## Here comes the twist

With a flurry of modern upgrades, time to balance it out with some good ol' 5.25" drives!

I wanted to have them from the start, partly for contrast with all the new stuff, and partly because I actually have a huge pile of floppies that I want to explore.

I picked two drives, a 48TPI Tandon TM-100-2A from an OG IBM PC, and a 96TPI Shugart SA460 from the FrankenBeeb.

With both 40 and 80 tracks, it should cover most of the floppies from the era.

![Alt text](photos/both.jpeg)

After some trail and error, I found that the cable needs to have **no twists**, and drive ID set manually with jumper.

I had to manually de-twist my cable by cutting and re-soldering the wires in order, which was a bit annoying, but with that and manually setting the drive ID 0 and 1, both worked!

![Alt text](photos/floppytest.jpeg)

With Intel 8271 disk controller and Acorn DFS, two sides of a floppy appear as two separate drives. So the Shugart is drive 0 and 2, and Tandon is drive 1 and 3. This disk seem to have Elite and some save data on it, very nice!

With the setup working, I now have to figure out how to mount them on the case.

The right side of the case has slots for mounting water cooling radiators, I went to local hardware store and bought some metal brackets that's roughly the size, and cut them to length and drilled holes in them.

![Alt text](photos/bnq.png)

They are fastened into the slot and hold the drives from the bottom. I really wanted something more substantial, like a one-piece metal bracket, but custom fabrication would have been a lot more expensive.

![Alt text](photos/empty.jpeg)

Anyway, I test-mounted the drives, and they look pretty good! The face plates line up with the front of the case.

![Alt text](photos/fit.jpeg)

Everything seemed to be going suspiciously well, but of course, things soon went back to normal when I tried to install the motherboard:

![Alt text](photos/block.jpeg)

The connectors in the back are too long! They are touching the floppy cable, preventing the motherboard from being installed.

Well, it's about time that we do something to it...

## Motherboard modifications

This is the part where I put the motherboard under the knife (well, soldering iron). As mentioned before, all modifications are purely for aesthetic reasons, and are totally **optional and reversible**.

First, I desoldered the Tube, 1MHz, and user port header:

![Alt text](photos/headeroff.png)

That was NOT easy, experience and extra care is needed to not lift any pads or damage the PCB.

Next, out comes the keyboard connector and all 7 power connector blades:

![Alt text](photos/desolder.png)

I then soldered a straight header on the user port, so I can use the excellent MMFS SD card adapter.

(I think I put it in backwards in this photo, make sure to double check!)

![Alt text](photos/userport.png)

I then ran power cables to connect all the rails together, 5V, GND, and -5V.

If making your own, make sure the cable is thick enough to carry at least 2A of current. Double check for shorts between 5V and GND, and the exposed conductor is not touching nearby traces and components.

I also soldered the keyboard header on the back side.

![Alt text](photos/power.jpeg)

## Putting it all together

Time to finally put everything together! 

I fed the floppy and power cable through the hole in the adapter plate, and mounted the motherboard.

![Alt text](photos/back.jpeg)

In the back, I:

* Cable tied the USB4VC in place, and connected the ribbon cable.

* Installed two 9-Pin USB header to USB-A adapters, so USB devices can be plugged in on the front panel.

* Cable tied the speaker near the front of the case.

* Powered USB4VC with a USB-C cable.

![Alt text](photos/caseback.jpeg)

I then connected up ATX4VC:

![Alt text](photos/atx4vc_config.jpeg)

* Power rails on top.

* Two USB-C power output on left, one for USB4VC, one for RGB backlight plate.

* Case power button and power LED on right. Case reset button used to change RGB mode.

* ATX motherboard connector on the bottom.

It controls power, lighting and cooling of the whole system. I really like how clean and integrated this is, much better than a nest of flying wires and components.

I then installed the floppy drives, and gave it a test:

![Alt text](photos/testdone.jpeg)

It still works! This motherboard is an issue 4, I picked it because most chips are socketed (including all RAMs), making it very easy to test and troubleshoot. The solder mask also seems thinner as well, allowing more light to pass through.

I decked it out with optional upgrades for the big day, with disk controller, speech synthesis, ADC, and econet. Annoyingly the econet chip itself is missing, and I'll need to get one.

Anyway, time to install the tempered glass for the money shot:

![Alt text](photos/light.jpeg)

![Alt text](photos/moneyshot.jpeg)

## Conclusion

It's amazing how quickly a simple idea can get out of hand, I started out just wanting to put a BBC Micro motherboard into a PC case, and in the end I developed a new protocol card for [USB4VC](https://github.com/dekuNukem/USB4VC/blob/master/README.md), an [ATX power controller](https://github.com/dekuNukem/ATX4VC/blob/master/README.md) just for retro computers, and a custom RGB backlight plate with 168 LEDs. Go big or go home, right? 😅

None of this is totally necessary, but just like the Torch Communicator and the FrankenBeeb, the whole ordeal of dragging it kicking and screaming into the RGB age made it feel more special, and I guess this is what modification is all about.

Of course, I omitted a lot of less glamorous stuff such as writing and debugging firmwares, waiting for parts, many hardware revisions (ATX4VC had 6!), and fixing up old motherboards themselves. Took me about 3 months from start to finish.

Still, I learned a lot about the history and clever design of this machine, and made something that hopefully benefits the community at large. With everything put together, it looks every bit as good as i imagined from the beginning.

As for what's next, I might add a Torch Z80 card for CP/M capability, but to be honest, I spent so much time building this thing, I haven't had much time actually using it! Guess I'm going to fix that.

## Questions and answers

### I want to build one!

Sure! As usual the project is open-source, and all you really need is the ATX adapter plate, which [can be found here](https://github.com/dekuNukem/RGBeeb/tree/master/plates).

Just give the files to a lase-cut acrylic manufacturer. The rest is up to you! Hopefully reading this article gave you some ideas.

### Can I buy one?

(Mostly) No.

This is a very custom build with parts that can be unreliable and difficult to source, so I'm not inclined to turn it into a business.

I'm not completely closed to the idea of making a few one-offs though, but it would need to be worth my while one way or the other.

[Get in touch](#get-in-touch) if you want to have a discussion or have any questions.

### Is BBC Micro Protocol Card available?

Might be, but not at the moment.

BBC Micro already has built-in keyboard, so I don't see much demand for it. Also the firmware needs a little more polish to meet my public release standards.

So again, [let me know](#get-in-touch) if you want it, I'll update in the Discord channel.

## Other Fun Stuff

I've done a few other fun projects over the years, feel free to check them out:

[duckyPad: Do-It-All Mechanical Macropad](https://github.com/dekuNukem/duckypad/blob/master/README.md): A 15-key mechanical macropad with hot-swap, RGB, and sophisticated multi-line scripting.

[ATX4VC](https://github.com/dekuNukem/ATX4VC/blob/master/README.md): Replace vintage computer power supplies with ATX PSU!

[USB4VC](https://github.com/dekuNukem/USB4VC/blob/master/README.md): USB Inputs on Retro Computers

[Pimp My Microwave](https://github.com/dekuNukem/pimp_my_microwave/blob/master/README.md): Fixing my microwave by grafting an RGB mechanical keyboard

[Daytripper: Hide-my-windows Laser Tripwire](https://github.com/dekuNukem/daytripper/blob/master/README.md): Saves the day while you slack off!

[Bob Rewinder](https://github.com/dekuNukem/bob_cassette_rewinder/blob/master/README.md): Hacking Detergent DRM for 98% Cost Saving

[From Aduino to STM32](https://github.com/dekuNukem/STM32_tutorials/blob/master/README.md): A detailed tutorial to get you started with STM32 development.

[List of all my repos](https://github.com/dekuNukem?tab=repositories)

## Get in touch

Questions or comments? Feel free to ask in official [ATX4VC Chatroom](https://discord.gg/T9uuFudg7j), raise a [Github issue](https://github.com/dekuNukem/RGBeeb/issues), or email `dekunukem` `gmail.com`!


## Extra Trivia

Congrats for reaching the bottom! If you stuck around this long, I can only post a few more interesting stuff!

Remember the FrankenBeeb? I actually got *another* BBC Micro from the same person that's also customized. Take a look:

![Alt text](photos/strange.jpeg)

The owl logo from drilled holes! It looked very professionally done. Spacing is even, drill is clean, and they even deburred every single hole!

![Alt text](photos/holes.jpeg)

I have no idea if this was a one-off DIY job or some kind of send-in modification that people could do. Let me know what you think!

Also, notice the keyboard, some keys are actually from a Torch Communicator!

![Alt text](photos/keys.jpeg)

The blue keys, and the tiny "exact space" key, which I have no idea what it's for. Is regular space bar not exact enough?

--------

Eagle eyed viewers might also notice quite a few different motherboards in the photos. There's a Issue 3, a Issue 7, and two Issue 4s.

I must have like half a dozen Beeb motherboards, and just kept swapping part around to keep them going! I used the Issue 4 board in the end because it has all the optional upgrades.
