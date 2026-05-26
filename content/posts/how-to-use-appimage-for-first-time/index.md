---
title: "How to Use AppImage for the First Time"
description: "I like the portability of AppImage, but the initial setup is not beginner-friendly."
summary: "I like the portability of AppImage, but the initial setup is not beginner-friendly."
date: "2025-10-28"
tags: ["Linux", "AppImage"]
---

"It's a portable app in Windows". This was my first impression when I heard about AppImage. 

To try out AppImage, I downloaded LocalSend's AppImage version. I double-clicked it to run and nothing happened...

Maybe my click didn't register? I double-clicked it again. Still, nothing happened.

## Executable Permission

After googling, I found out that I needed to set the permission:
1. Select and right-click the AppImage.
2. Click __Properties__ and __Permissions__ tab
3. Check the __Allow executing file as program__ box.

Then I double-clicked it again and it started to run. 

## AppImage Desktop Integration

Now, I had another question. Why don't I see my app in the menu?

I googled again and found out that I needed to write a `.desktop` file to integrate it. 

For convenient, someone already made [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher) to simplify the process and add useful functions. 

I did it manually, referring to the [Example Desktop Entry File from freedesktop.org](https://specifications.freedesktop.org/desktop-entry-spec/latest/example.html), and wrote a simple `.desktop`. 

``` toml
[Desktop Entry]
Name=LocalSend
Comment=An open-source cross-platform alternative to AirDrop
Version=1.17.0
Type=Application
Categories=Utility;Network;FileTransfer
Exec=/home/juan/Apps/LocalSend/LocalSend-1.17.0-linux-x86-64.AppImage
Icon=/home/juan/Apps/LocalSend/logo-512.png
```

Save the file in `/home/\<user\>/.local/share/applications`. 

Then, it should appear in the menu. 

For more info, please visit [Freedesktop.org Specifications](https://specifications.freedesktop.org/)