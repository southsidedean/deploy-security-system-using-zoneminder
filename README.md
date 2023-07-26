# Deploying a Video Security System Using ZoneMinder on Ubuntu Linux

### Tom Dean: [LinkedIn](https://www.linkedin.com/in/tomdeanjr/)

## Introduction

When we moved into our house five years ago...



In this tutorial, I'm not going to provide a step-by-step guide, because of the many variables, including cameras, house construction and technical concerns.  I will point out the high-level considerations, where I ran into issues and will document any resources I used for the project in this repository.

***Let's go!***

## High-Level Thinking


### Hardware

#### ZoneMinder Server

I started with a **Dell Precision T3500** workstation that I use as a general-purpose server in my lab:

- Ubuntu 22.04
- Single six-core Xeon processor
- Plenty of storage
    - RAID-1 HDD for system: 1TB
    - RAID-1 HDD for data: 3TB
- Dual 1GB network connections
    - Public/General network
    - Private/Data/Application Network
- 24GB of RAM

I experimented with this server for a day, and ran into performance issues.  The server ran out of RAM and went into swap, and I had pretty significant iowaits, which caused significant impact to performance.  I wasn't happy with this setup, so I configured a new instance of ZoneMinder on another more powerful machine in my lab.

I have a **Dell Precision T5500** workstation sitting under my desk, which I recently upgraded:

- Ubuntu 22.04
- Dual six-core Xeons
- Plenty of storage
    - RAID-1 SSD for system: 250GB
    - RAID-1 HDD for data: 6TB
- Dual 1GB network connections
    - Public/General network
    - Private/Data/Application Network
- 72GB of RAM
- Decent GPU, possible future use?

The workstation was already up and running with Ubuntu 22.04, mostly idle, serving as an development server at this point.  Yes, it's kind of old, but it's still a trooper, like me.

#### Security Cameras


### NVR Software: ZoneMinder

I've been researching this project for a couple of years, and had set up ZoneMinder in the past, but never moved to the "installing cameras" part of the project.

***Let's see how we build that!***

## Install ZoneMinder Software


## Perform a Site Survey: Not Optional!


## Cameras: Physical Installation/Wiring


## Configure Cameras on the Network

General Network Considerations:

- Camera IP Addresses
    - Static IP or Reserved DHCP IP Addresses
- DNS: Forward and Reverse
    - Optional, but a good idea if you can
    - Makes setup, configuration and maintenance easier

Once the cameras are on the network...
## Add Cameras to ZoneMinder




![Camera Configuration: General](images/Cam_Configuration_General.png)

![Camera Configuration: Source](images/Cam_Configuration_Source.png)

![Console: Cameras Configured](images/Console.png)


## Add Cameras to Groups (Optional)

![Cameras: Add to Groups](images/Groups.png)


## Define Camera Zones



![Zone Example 1: Partial Zone](images/Zone_Partial_1.png)

![Zone Example 2: Partial Zone](images/Zone_Partial_2.png)

![Zone Example 3: Full Zone](images/Zone_Full_1.png)



## Configure Montage View

![Configure Montage View](images/Montage.png)


***That's it!***

## Summary

In this tutorial, we...

Enjoy!

***Tom Dean***
