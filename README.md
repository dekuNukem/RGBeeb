# Pimp My Beeb

BBC Micro inside a open-frame ATX PC case 

## What's BBC Micro?

## Oh no! You butchered a piece of computing history!

Non-destructive, all modifications are reversible.

Technically no modification is needed at all, I went quite far for aesthetic reasons.

And even though this kind of shenanigans seems one-off, back then users seemed to go a lot harder when it comes to modding.

The original Torch computer is basically a BBC micro motherboard stuck in a case with a monitor, disk drives, and built-in keyboard with a few extra keys.

Show the photos I took at the computer museum, you can see the BBC micro motherboard mounted to the case.

Of course they went a bit further than that, adding a Z80 co-processor and CP/M capabilities. But the idea stands. (what idea?)

Which leads to another machine i picked up locally via ebay. here are the photos on that listing.

you can see this one went even further, putting the keyboard in its own case, a lid on the case to make it a box, and tons of upgrades! Seriously just look at all the ROMs.

dumb it down a bit for regular readers and main stream tech blog editors.

show the owl case micro too? mention backstory, the sellers father were really good at those.

It also came with a external disk drive with dual 5.25 inch floppies, and I spent some time documenting the whole thing and checked it through. Removed RIFA caps,hooked everything up, i didn't want to risk using the PSU inside the external drive so I hooked up a ATX PSU directly to it. I turned it on and it actually worked! All the ROMs are visible, and it is quite a sight to behold:

which got me thinking, if i want to actually use it like that, wouldnt it be a lot nicer to put everything in the same case, like a ATX PC case?

## Figuring out whats needed, ATX size

That did seem like an outrageous idea, so I did some quite measurements. To my surprise, the size of the BBC micro motherboard is almost identical to the full-size ATX motherboard! BBC is ???mm by ???mm, and ATX is 305x244mm. here is a comparison:

SVG comparison of two board outlines.


adapter plate

for mockup, i used the bbc micro motherboard from the owl BBC, it didnt come with a PSU for some reason, after some testing i think i knew why. this one is in pretty rough shape, quite a few reworks and bodge wires, it works but is very unstable, it had a bad VIA, and then still usually crashes after a few minutes. strongly suspect an intermittent RAM program. still, just for mockup. 

photo of bbc micro motherboard with hard board adapter plate side by side

photo of motherboard inside the shit PC case

tried out out in a 30 quid junk case, it actually fits fine, looks strange though.


## case selection / a case of ???

with that out of the way, it really set things in motion, now i have to pick a PC case and think about the next steps.

self contained BBC micro with two disk drives inside a ATX case with PSU and working power buttons and LEDs just like a real PC.

mention really dont like RGB gaming builds, i find them obnoxious and pointless. all my pcs are under the desk and i dont look at them when i use them!

at first i wanted a obnoxious RGB esport gaming case just for the shit of it, but as it turns out, to the shock and disappoint of dozens of retro computer enthusiasts, almost all modern PC case doesn't have 5.25 inch bay anymore! there is just a blank space there. those who did does not support full height drive anymore as well, as they are optimised for optical drives and have half-height drives that prevent full height drives to be inserted. 

I want my dual full-height drives, that means four(!) 5.25 inch bays! and its safe to say i wasnt able to find any gaming cases on sale today with that.

I then decided to turn my attention to a little eariler, and got myself a case from early 2000s. A handsome looking aluminum coolermaster full-size case. it has 4 bays and everything i need. its a nice case for a period build but still leaves me a bit cold. the major theme of this build is to contrast the 40 years old computer with modern enclosure, and using a 20 years old case just wasnt going to cut it.

then during another scrolling session of looking at PC cases, I stumbled upon something i never thought of: open-frame cases!

striking design, minimalist and thoroughly modern
lots of space to work with, easier to work on than a cramped regular case
more flexible mounting not having to worry about side of the case and cutting stuff out
more visibility for the motherboard and internals since everything is on display
on-the-nose gaming image? perfect contrast

i looked at several designs, Thermaltake Core P3 TG Snow caught my eye the most:

really like the clean and modern look and customisable design, can be configured to stand up, lay down, or wall mounted. (look at more blurb here), and most importantly, there are slots at the right edge of the case for mounting water cooling radiator fans, which looks perfect for mounting full-height drives! it will probably need some custom bracket fabrication but we'll get to that.

theres a black one as well, i really like the white color, sets it apart from a sea of black boxs. black is so boring!

the clean and minimalist design of the case also changed my aesthetic plan a bit, was originally going to go full-on RGB blast, but now i wanted it to be a bit more subtle?

## Custom fabrications 

I looked up ATX motherboard standard and measured the mounting holes on the BBC motherboard, and designed a simple adapter plate in inkscape, and had it cut out in acrylic. Much more ridgid than the hand drilled hardboard.

the case arrived, i had it roughtly assembled, and installed a second hand RGB PSU, to my annoyance the RGB fan points to the bottom so it will be pretty much invisiable, but still, at least its white too!

tried the adaptor plate, works fine and fits snugly.

now to how to mount the drive, there are a bunch of slots on the case, so a simple right angle metal bracket should be sufficient. i went to my local hardware store and bought some mounting brackets, to my surprise they almost fit with out much modification at all, al though i had to drill some holes at the longer side to mount the drive. in the future i probably should have a proper bracket frabricated.

## power supply, ATX4VC



## RGB lighting

repair, intricate trace designs, would be very attractive to add backlight to the back of the motherboard. luckly the motherboard had no ground pours, making the traces extra visible. did a mockup by taping some RGB light strips, and it looked absolutly amazing.

the light strip had shit adhensives that starts to peel off after a day or two, and i dont really like the hand-soldered look anyway, might as well go all out, so i designed a new PCB adaptor plate with built in RGB backlight.

## putting it all together

