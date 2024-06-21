---
title: "How to Fix CH340 USB to Serial Driver 3.8 version issue."
description: "CH340 USB-to-Serial Driver 3.8 version issue. It cause the Arduino IDE prompt \"A device attached to the system is not functioning\" error message."
date: "2024-06-21"
tags: ["Arduino", "CH340"]
draft: false
ShowToc: true
canonicalURL: "https://juanstechblog.blogspot.com/2024/06/how-to-fix-ch340-driver-3-8-issue.html"
ShowCanonicalLink: true
CanonicalLinkText: "Originally published at Juan's Tech Blog(Blogger/Blogspot)"
cover:
    image: esp-01s-and-esp-ch340-usb-programmer.webp
    alt: ESP-01S and ESP USB Programmer with CH340 chip.
    caption: ESP-01S and ESP USB Programmer with CH340 chip.
    relative: true
---


Recently, I started working with the ESP-01S module and CH340 ESP programmer. However, when I tried to upload a new Arduino sketch, I encountered an error:

```shell
A fatal esptool.py error occurred: Cannot configure port, something went wrong. Original message: PermissionError(13, 'A device attached to the system is not functioning.', None, 31)
```
## CH340 Driver Issue and Fix.
After some googling, I discovered that the problem was related to the CH340 USB-to-serial chip driver. The latest CH340 driver, version 3.8, seem to cause the issue. To fix it, I had to uninstall the 3.8 version driver, and install the previous 3.4 version driver.

Here how you can do the same:
1. Go to Device Manager and find __USB-SERIAL CH340__ under **Ports(COM & LPT)**.
2. Right the CH340 device and click **Properties**.
3. The **driver version** is under **Driver** tab.
4. If the version is not right, click the **Uninstall Device**.
5. Download the 3.4 version and install.


## Windows 11 Auto Update Drive, Break the CH340 Driver Again.
Somehow, Windows 11 will automatically update drivers, and this can revert the CH340 driver back to the problematic version 3.8. My temporary fix is to disable automatic driver updates.

1. Press the Windows key and search for **Change device installation settings**.
2. Click on the search result to open the settings.
3. Select **No** radio button.
4. Click **Save Changes**.

Please note that disabling this stops Windows install/update any new and existing device drivers automatically. Make sure you install or update your driver manually.