---
title: Improving WiFi speed 
categories:
  - Tech
  - Home
header:
  og_image: /assets/images/blog/home_wireless_network_diagram_networking_wireless.jpg
---

Working from home has become the new normal for many. This means more streaming, video calls,  and other bandwidth intensive activities. For most of us, all this happens over WiFi and puts more strain on the available bandwidth. If you have a lot of smart devices on the same network, this only exacerbates the problem.

TL;DR
----
- Use dual band WiFi - 2.4 Ghz and 5 Ghz
- Use different network name per band
- Keep high priority devices on 5 Ghz 
    - Gaming consoles
    - Work machines
    - Your personal phone 
- Keep everything else on 2 Ghz
    - IoT sensors
    - Smart TVs*
    - Your flatmate's devices*

*Feel free to move some of these to 5 Ghz if the speeds are insufficient for your use case.
{: .notice--primary}

My story
----
I'm a smart home fanatic and there are between **19 to 30 devices** actively connected to my home network at any given time. The number varies depending on who is home and what they are doing. For instance, playing Xbox on the TV - adds 2 additional active devices. The bare minimum are the always on smart devices such as Curtains, Smart Switches, and various servers (3 to be precise) around the house. I noticed that adding all these devices has seriously affected the internet speed and latency on my phone and laptops. At my workspace, I was getting speeds in the range of __30-50 Mbs (Up/Down)__ when my internet package offers a minimum of __150Mbps (Up / Down)__. So, I spent some time to figure out what's really causing this slow down from my side - you know, before just ringing up my Internet provider.

Finding the problem
----
Run a quick speed test by just searching ["speed test" on Google](https://lmgtfy.app/?q=speed+test) or using either [speed test](speedtest.net) or [fast.com](fast.com). Ideally do this in the spot of your house where you commonly use the internet from. If you notice a significant difference from the ISP promised speeds vs your results, read on.

{% include figure image_path="/assets/images/blog/home_wireless_network_diagram_networking_wireless.jpg" alt="diagram of home wifi network" caption="An overview of the home WiFi network." %}

As the figure shows, your internet traffic hops multiple links before reaching the service. What "_Internet speed test_" results tell you is actually the speed of the slowest of these links! If you can find and fix the sluggish link in this network, your speed tests should reflect that accordingly. Obviously, you don't have control over all the links and in fact this post is only about fixing problems in the Wireless network (WiFi). If you have access to a laptop or some device that you can plug-in to the router, do so and run a speed test. This will verify the maximum attainable speed over your wired connection - connecting links 1, 2 & 3. If this speed is not close to your ISP's advertised ones, contact them! The maximum speed you could attain over Wireless network will almost always be at or below this. Rare exceptions are when you are using a very bad ethernet cable to connect your laptop to the router or when the wire between the modem / wall socket is really bad. This concludes the initial debugging to make sure the problem is indeed with your WiFi network (and not your ISP or bad cables throttling you).

How does WiFi work
----
Before we jump ahead to trying out the fixes, a quick lesson on how the WiFi networks work. This is optional of course, but gives you a better sense of the things we will attempt to alleviate the problem. I will start big - with the full electromagnetic spectrum.

{% include figure image_path="/assets/images/blog/electromagnetic-spectrum.jpg" caption="Figure depicting the use of different parts of the full electromagnetic spectrum." %}

The highlighted oval is the part where most of our short range wireless communications such as WiFi, Bluetooth, Zigbee etc work in. WiFi is the one of interest to us. The figure doesn't show it due to lack of space but WiFi is actually two different bands in that crowded space - 2.4 Ghz and 5 Ghz - not to be confused with the cellular 2G, 3G, 4G and 5G networks, which have their own space in the spectrum.

2.4 Ghz WiFi
----
{% include figure image_path="/assets/images/blog/2.4ghz-spectrum.png" caption="Channels of the 2.4 Ghz WiFi" %}

The 2.4 Ghz region of WiFi is further divided into 14 channels as shown above. Each channel is 22 Mhz wide. Devices that communicate in a channel have to share the 22 Mhz bandwidth. When you create a WiFi network, the router picks one of the 14 channels for the network - some routers are smart about how they pick this while other's may do so randomly, or worse, always pick the same channel. All devices that are connected through a channel, __irrespective of the WiFi network__ they are part of, have to share the channel's bandwidth. This means taking turns when sending or receiving data. If there are too many WiFi networks or devices on the same channel, it can seriously slow down the speed - as each device / network gets a smaller time share to use the channel. Another downside of the 2.4 Ghz WiFi specifically is, __the channels overlap!__ This means that devices communicating with each other in 2 overlapping channels (say 1 and 3) can interfere with each other - thus opening possibilities for further degradation of speeds across channels. In fact there are only 4 non-overlapping channels and this is barely enough for urban neighbourhoods where there are typically more than 4 WiFi networks in range at any given spot! To sum up, if your router support only 2.4 Ghz networks, look for which channels your nearby WiFi's are in and pick a channel that is less congested and if possible, of the same colours in the below picture.

{% include figure image_path="/assets/images/blog/2.4ghz-channels-colored.jpg" caption="Channels with same color have the least overlap in a 2.4 Ghz WiFi" %}
 

5 Ghz WiFi
----
{% include figure image_path="/assets/images/blog/5ghz-wifi-channels.png" caption="Channels of the 5 Ghz WiFi" %}

The 5 Ghz region of the WiFi is quite interesting. You have the choice to pick from more channels and within each channel you can also pick from different channel width - 20 Mhz to 160 Mhz. In case you haven't noticed already, these channels are non-overlapping! The actual number of options available to you depend on your region and router model - manufacturers are permitted to support free home WiFis only within certain frequencies - depending on the country. Nevertheless, you should still have more choices than 2.4 Ghz. Since each channel can have a wider band, this should support more data flow than a typical 2.4 Ghz channel. One downside of the 5 Ghz network is range. I would argue that, for smaller urban flats especially, the shorter range is a blessing in disguise! You see shorter ranges for each WiFi network would mean less interfere with your neighbours networks!

{% include figure image_path="/assets/images/blog/2.4-vs-5ghz.png" caption="Summary of differences between the 2.4 Ghz and 5 Ghz WiFi bands" %}

Picking the right band
----
The short answer is, if your router supports dual band, use them both! However, there's more to this. You have 2 options when it comes to running your router with dual bands. In both options, your devices will be making use of a wider spectrum than a single band WiFi setup. However, there are key differences as you will see in the next sections. 

## Same name for both bands
You will use the same name for both your 2.4 Ghz and 5 Ghz networks - there's good chance that your router recommends this option when setting up dual bands. An argument for this setup is that devices that support only 2.4 Ghz (IoT sensors, weighing scales, some smart watches) will always use 2.4 Ghz, while devices that support 2.4 Ghz and 5 Ghz (which is almost all smart-phones and laptops) will dynamically pick the band that is less crowded.

This sounds good in theory. However, in my experience I noticed that a lot of the devices were often packed in the 2.4 Ghz band and my speeds have dropped significantly as a result
{: .notice--warning}

You must use the __same password__ for networks with the __same name__.
{: .notice--danger}


## Different name for each band
You will have 2 different WiFi networks - if following the typical naming pattern, __MyWiFi__ and __MyWiFi 5Ghz__. Now you pick which devices are part of which network. Personally, I recommend putting most of your passive devices in the 2.4 Ghz network and the devices that you use frequently or those that need your best internet speeds on 5 Ghz network. I prefer this setup as it gave me the best results to prioritize some devices while others continue to work silently in the background. At the time of writing this, I have 22 devices our Home network, of which

- 2 connected through Ethernet
- 3 connected through 5 Ghz WiFi
    - My phone
    - Work laptop
    - Xbox
- 17 connected through 2.4 Ghz WiFi

Despite having so many devices on the 2.4 Ghz network, the speeds (revealed later) are sufficient for most day to day tasks, including streaming.
{: .notice--success}


Picking the right channels
----
This is a bit tricky as channels which may seem best at one time may not continue to be so. If your neighbours left it to auto selection in their router setup, their networks may hop between channels based on how their routers see fit. I would recommend trying out the auto selection option in your router and if that doesn't seem to work well for you, read on. If you are an Android user, install [Wifi analyzer](https://play.google.com/store/apps/details?id=com.farproc.wifi.analyzer) to scan across both your WiFi bands and pick a channel that seems best - the app can make these recommendations.

Finishing thoughts
----
I hope this helped you fix your WiFi speeds and you enjoyed all that additional information about WiFi spectrum. Please leave a comment if you need more help on this. Here are my network speeds.

<figure class="half">
    <img src="/assets/images/blog/internet-speed-2.4ghz.png">
    <img src="/assets/images/blog/internet-speed-5ghz.png">
    <figcaption>Internet speed tests over 2.4 and 5 Ghz networks respectively</figcaption>
</figure>   

__Stay safe and stay strong__ 💪😷🧴👐