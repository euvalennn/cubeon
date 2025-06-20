---
title: "CubeOn"
author: "@valen"
description: "Rubik's cube timer with scramble generation and solve history storage"
created_at: "2025-06-20"
---

### Total time spent: 1h

# June 20: Started project planning

Today I started planning how I'm going to design my project and what components I'll use. I might change them later, but for now I'm looking at using: Seeed Studio XIAO RP2040 or any other RP2040 based board as MCU (could also use bare chip but I'm not sure if it's worth the hassle), 0.96in 128x64 OLED as display, two keyswitches to start and stop the timer, and a Li-Po or Li-Ion battery with a TP4056 charging module (I still need to research a lot about this).

The solve history will be stored on the XIAO's onboard flash, but for now I'm not completely sure how I'd visualize that data since connecting to a PC via USB is a bit cumbersome just to see your solves. I still have to figure that out, I was thinking of making it so you can view your average solve times and past solves from the timer itself but maybe having a way of seeing everything from your phone would be more convenient, I'd probably have to change the MCU for that though.

Tomorrow I'm going to research more about integrating a battery into my project, I'll start with my schematic and now that I'm writing this I'm considering changing the MCU to an ESP32 based board to have a web server so turns out I don't have everything as planned as I thought I did lol

Really excited for tomorrow!! :D didn't add any images since today was mostly planning, design and research

**Time spent this session: 1h**
