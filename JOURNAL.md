---
title: "CubeOn"
author: "@valen"
description: "Rubik's cube timer with scramble generation and solve history storage"
created_at: "2025-06-20"
---

### Total time spent: 3h

# June 20: Started project planning

Today I started planning how I'm going to design my project and what components I'll use. I might change them later, but for now I'm looking at using: Seeed Studio XIAO RP2040 or any other RP2040 based board as MCU (could also use bare chip but I'm not sure if it's worth the hassle), 0.96in 128x64 OLED as display, two keyswitches to start and stop the timer, and a Li-Po or Li-Ion battery with a TP4056 charging module (I still need to research a lot about this).

The solve history will be stored on the XIAO's onboard flash, but for now I'm not completely sure how I'd visualize that data since connecting to a PC via USB is a bit cumbersome just to see your solves. I still have to figure that out, I was thinking of making it so you can view your average solve times and past solves from the timer itself but maybe having a way of seeing everything from your phone would be more convenient, I'd probably have to change the MCU for that though.

Tomorrow I'm going to research more about integrating a battery into my project, I'll start with my schematic and now that I'm writing this I'm considering changing the MCU to an ESP32 based board to have a web server so turns out I don't have everything as planned as I thought I did lol

Really excited for tomorrow!! :D didn't add any images since today was mostly planning, design and research

**Time spent this session: 1h**

# June 21: More research and new MCU choice

I was hoping I'd be able to start with my schematic today, but I spent most of the day at my grandparents house and didn't have my laptop on me. What I was able to do from my phone though is a lot of research, and I think with all the information I have now I can finally start doing the schematic and maybe even start the PCB tomorrow.

I've decided that I'm going to be using the XIAO ESP32C3 as the MCU for this project. It only costs $4.90 and it has a built-in battery charging circuit, (I spent quite a lot of time researching how to do it manually with a TP4056 only to find out the xiao handles everything 😭) it supports WiFi so I can sync my solve history with my phone using a web server and it also has more flash storage.

<img src="assets/xiao-bat-connection.png" width=500px>

What I have to figure out now is how I'll wire the 18650 battery holder to the BAT pads on the back of the xiao, since I'm soldering headers to the xiao and the pads on the back are flat, probably meant for SMD soldering. Maybe I could just make a hole on the PCB to be able to access the pads from the back, but they wouldn't be touching the PCB so that would make them harder to reach. I'll figure something out tomorrow

<img src="assets/xiao-back-pads.png" width=500px>

If I take into account all the time I spent researching how to do this it'd probably amount to like 3 or 4 hours, but since it wasn't a whole uninterrupted session and basically I only did some research whenever I had free time let's call it 2 hours.

PS: I love how well documented xiao boards are, not only that but the docs also include a lot of resources like schematics of the board, 3D models, DXF files with dimensions, and a lot of useful stuff

**Time spent this session: 2h**
