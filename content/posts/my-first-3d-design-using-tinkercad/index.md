---
title: "My First 3D Design using TinkerCAD."
description: "I want to learn 3D design to print real things with my 3D printer. So, I started with something simple: designing a case for my DIY human presence sensor using an ESP32 and LD2410."
date: "2025-07-19"
tags: ["3D Design", "3D Printing", "TinkerCAD"]
draft: false
ShowToc: true
cover:
    image: imgs/first-3d-design-using-tinkercad.webp
    alt: "Three blue 3D-printed electronic enclosures are displayed on a black surface. The left and right designs are marked with red Xs, indicating failure, while the center design has a green checkmark, showing success. The left enclosure is broken apart, the right one has poor fitting, and the center one fits components well and is properly assembled. Text at the bottom reads: \"First 3D Design.\""
    caption: "First 3D Design"
    relative: true
---

Since I got my first 3D printer, I want to learn 3D design to make my own model to solve my own problem. 
I don't know how to start. I think I should start with something simple. Simple means easy, right?

![My DIY human presence sensor using ESP32 and LD2410C on a breadboard with a few jumper wires to connect each components](imgs/diy-human-presence-sensor-esp32-ld2410-breadboard.webp)

I have a DIY human presence sensor using an ESP32 and LD2410C. It's in a very raw state. I want to make a simple case for it. So, I started with the most intuitive one, in my opinion, TinkerCAD. It looks like just dragging a few boxes around.

## Video
{{< youtube -818AtI2M_g >}}

## Plan & Build the 3D Design
My plan is simple and straightforward.
The box will hold the ESP32 with a hole for the USB-C port, and the lid will hold the LD2410.

![The case design for DIY human presence sensor](imgs/diy-human-presence-sensor-case-3d-design-tinkercad.webp)

To build it:
- I drag four walls to form a square, then add a wall to the bottom to make it a box.  
- I use an [ESP32 Devkit V1 USB-C model by Flametech6](https://www.tinkercad.com/things/2czhE3tLv53-esp32-devkit-v1-usb-c-vision) to mock up the USB-C position, and a [USB-C cutout model by lowerclasswarfare](https://www.tinkercad.com/things/5EdmwRANlsW-usb-c-cutout) to make the hole.
The hole is there to hold the ESP32 in position.
- I take the LD2410 measurements and make a U-shaped bracket to hold the sensor on the lid.

I export and start printing it. Just a few layers in, I stop immediately. 
![3D moodel case for DIY human presence senor after first few 3D prints](imgs/diy-human-presence-sensor-case-3d-model-first-few-layer-of-printing.webp)

Why is there a gap? 

![A gap found in the slicer from the 3D design case for the DIY human presence sensor](imgs/3d-design-case-diy-human-presence-sensor-slicer.webp)
I check the model... Yup, my bad. I was a bit careless there.

## Fixing the 3D Design Flaw

![The second attempt print for the 3D design model case](imgs/3d-design-model-second-attempt-case-diy-human-presence-sensor-case.webp)

![The second attempt print for the 3D design model lid](imgs/3d-design-model-second-attempt-lid-diy-human-presence-sensor-case.webp)

I fixed it up a bit, but the second attempt was still terrible.  The base of the box has a gap,  the walls aren't connecting properly, and one side of the U-shaped bracket on the lid is just floating. I broke it when I removed it from the 3D printer bed. Also, the lid has no way to snap onto the box.

Therefore, I restructured the 3D model. Instead of building everything by dragging solid shapes one by one, I started using the hole shape function to carve out the model and group them together. This way, I can avoid the wall connection issues. I also added an interference fit, also known as a friction fit, to the lid, hoping it can snap onto the box more securely.

![First attempt prints with the new structure](imgs/new-restructured-3d-design-model-for-diy-human-presence-sensor-version-1.webp)
On the first attempt with the new structure, the box looks good. The ESP32 fits in, and the USB-C cutout is spot on. But the lid? Not great. The U-shaped bracket is too narrow, and the lid can’t push into the box.

![Second attempt prints with the new structure](imgs/new-restructured-3d-design-model-for-diy-human-presence-sensor-lid-only-version-2.webp)
For the second attempt, I only printed the lid, since the box is fine. But still... it didn’t fit. 

![Finally attempt prints with the new structure](imgs/new-restructured-3d-design-model-for-diy-human-presence-sensor-lid-only-version-3.webp)

![Finally attempt prints with the new structure](imgs/new-restructured-3d-design-model-for-diy-human-presence-sensor-final-version.webp)

I adjusted and tried a third time. Finally, it fits\!

It’s obviously not the best model, but it’s usable. I added a hole in the lid, thinking it’d help me pry the lid off. But turns out, it’s not even needed. I can just pry it from the side.

## Future Update for the 3D Model
I probably should’ve added some vents, for heat to escape. I think I’ll make a better version later. For now, this one will sit on my desk.

This won’t be the final form. I want it to hang on the wall. But I don’t know how to make a mount that can adjust angles or rotate. If you have any ideas or resources, drop them in the comments.  