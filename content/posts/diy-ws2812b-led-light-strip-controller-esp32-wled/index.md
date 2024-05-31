---
title: "DIY WS2812B Addressable LED Light Strip Controller with ESP32 and WLED."
description: "Guide to Build a WS2812B Addressable LED Light Strip Controller with ESP32 and WLED."
date: "2024-03-19"
tags: ["WLED", "ESP32", "WS2812B", Addressable LED Light Strip]
draft: false
ShowToc: true
cover:
    image: esp32-wled-controls-ws2812b-led-light-strip.webp
    alt: "ESP32 with WLED controls WS2812B addressable LED light strip."
    caption: "ESP32 with WLED controls WS2812B addressable LED light strip."
    relative: true
---

I know a ready-made LED controller is affordable. But I think ESP32 with WLED is more versatile and playable. I can integrate it into my Home Assistant and TV ambient light project later.

Let's get started.

## Video
{{< youtube GwjAe-mXsfs >}}

## Parts Required
- 5M WS2812B 30LED/M LED Light Strip(Get any desire length).
- ESP 32(Any ESP8266/ESP32).
- 5V6A Power Supply.
- DC Jack.
- Breadboard.
- Some Jumper Wires.


## Flash WLED
We will use the easy way, ESP Web Tools, to flash the WLED firmware into ESP32. However, it requires using Google Chrome/Microsoft Edge browser and serial driver for your development board.

![WLED's ESP Web tool install web page](wled-esp-web-tool-install-web-page.webp)

Go to [Install WLED](https://install.wled.me/) page, select the latest version, and click the Install button.

![Select ESP32's series port in WLED ESP web tool](select-esp32-series-port-wled-esp-web-tool.webp)
Select the ESP32's series port.

![Click Install WLED](click-install-wled-wled-esp-web-tool.webp)
Click Install WLED

![Set up ESP32 Wi-Fi connection](set-up-wifi-wled-web-tool.webp)
We can continue wiring up other parts.

After the installation, set up the Wi-Fi connection and log on to the WLED web UI.
![Set up ESP32 Wi-Fi connection](set-up-wifi-wled-web-tool.webp)

Now, we can continue wiring up other parts.

## Wire-up
![WS2812B LED Light Strip with ESP32 Schemetic Diagram](ws2812b-led-light-strip-esp32-schemetic.webp)

| WS2812B    | ESP32       | DC Jack |
| ---------- | ----------- | ------- |
| RX2(GPI16) | RX2(GPIO16) | 
| +5V        | VIN         | +       |
| GND        | GND         | -       |

The WS2812B has two ways to power it; one from the red and white wires or the 3-pin connector. The Power supply plug with the DC jack connects to the WS2812B's red(+) and white(GND) wires. 

ESP32's VIN, RX2(GPIO16), and GND connect with the WS2812B's 3-pin connector.

It's a common recommendation to put a 100 ~ 1000uF capacitor close to the WS2812B's +5V and GND pins. Also, a 220 ~ 470 Ω resistor is added near the WS2812B's data pin. Both addon for protection and signal stability purposes.

## Result

![WS2812B in blends effect with Analogous color palette controlled by ESP32 and WLED](ws2812b-blends-effect-analogous-color-palette-esp32-wled.webp)

WS2812B in blends effect with Analogous color palette controlled by ESP32 and WLED