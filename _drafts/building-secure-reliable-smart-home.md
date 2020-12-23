---
title: Building a Smart Home - Secure, Reliable, and Transparent
categories:
  - Home
  - Tech
header:
  teaser: /assets/images/blog/home-assistant-network.png
  og_image: /assets/images/blog/home-assistant-network.png
---
Building a smart home is more easy than ever. Making it reliable, secure and transparent however takes a lot of patience and making good choices of devices, architecture and overall setup. In this post, I will discuss my smart home setup, along with the reasoning for the choices I made. Our house has been running on this setup for over 8 months now with no downtime even during the multiple internet outages in our area.


Home Assistant
----
Talk about the open source software and how customizable it is


Hue Zigbee Network
----
See this image

{% include figure image_path="/assets/images/blog/hue-zigbee-network.png" caption="Phillips hue zigbee mesh network has more connections in the network" %}


Universal Zigbee Network
----
See this image

{% include figure image_path="/assets/images/blog/universal-zigbee-network.png" caption="Universal zigbee mesh network has fewer connections due to more non active devices" %}


WiFi Network
----
See this image

{% include figure image_path="/assets/images/blog/wifi-network.png" caption="WiFi network has all smart devices that need internet and some IoTs that work fully local" %}


Bluetooth Network
----
See this image

{% include figure image_path="/assets/images/blog/bluetooth-network.png" caption="Bluetooth network is made of 2 Raspberry Pis collected data from plant bluetooth sensors" %}


Home assistant network
----
See this image

{% include figure image_path="/assets/images/blog/home-assistant-network.png" caption="Home assistant gathers data from all the other networks over local network created by the router" %}

