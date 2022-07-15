---
title: Network Settings
description: We can configure the rate at which our game client can receive network data in bytes.
section: guides
layout: ../../layouts/MainLayout.astro
herotext:
  - We can configure the rate at which our game client can receive network data in bytes. For most use cases we'll be fine using the max value.
image: /content/posts/network-rates.png
---

## Best network settings

Before you jump into copying and pasting commands into your game, I recommend you to have a read over this post.

- The server simulates the game in discrete time steps called ticks/seconds. So, a tickrate 128 means the server simulates the world every 7,8 milliseconds (128 times by second), a tickrate 64 means every 15 milliseconds. Simulating the world means calculates positions, registering shots, make grenades do their things, etc...
- The only commands that matter for network configuration are: "rate", "cl_updaterate", "cl_cmdrate", "cl_interp", "cl_interp_ratio", "cl_predict", "cl_interpolate" and "cl_lagcompensation".

I recommend you to paste this commands into your `autoexec.cfg`. Learn [how to create your autoexec for csgo](/commands/getting-started.html#creating-an-autoexec).

I also recommend you to read over the article to have a better understanding of what the hell it is you're modifying in the game.

```
//Rate Settings
rate "786432"
cl_cmdrate "128"
cl_updaterate "128"
cl_interp "0"
cl_interpolate "1"
cl_interp_ratio "2"
cl_lagcompensation "1"
cl_predict "1
cl_predictweapons "1"
```

## A note on interpolation

Interpolation is commonly used in FPSs games like CSGO, where having a consistent position for an enemy on time across players is important. Interpolating means that, even if some packets are dropped, you will have smooth movement on the screen.

### Playing on LAN

This setting is good for LAN games or for playing online **if your ping to the server is low.** (less than 50ms)

```
cl_interp_ratio 1
```

### Playing online

If our connection is not as good or we tend to have loss, we should use the following value.

```
cl_interp_ratio 2
```

## A note on lag compensation

Between the representation of the world you have on your monitor and the situation of the world on which the server works, there is a HUGE difference. But, don't panic, the server knows the interpolation (if you don't know what it is, you didn"t read explications on "cl_interp" bad boy) of each players and the ping of each players. So, the server take care of the differences of configuration of each players. If you shoot a guy, you can sometimes have the sensation than your crosshair isn't on him even though you got the frag.

To compute the simulate time from the real time, the server takes care of your ping (the travel time of the date between client and server), and of your interpolation time. So, the only acceptable value for this is `cl_lagcompensation 1` (it means lagcompensation activated).

## A note on tickrate

`cl_updaterate 128` The value of this, 128 for example, means "hey server, I'm a client, send me 128 times/second an update of the world".

`cl_cmdrate 128` The value of this, 128 for example, means "hey server, I will send you 128 times/second an update of my input (mouse, moving, ect...)"

The values of `cl_cmdrate` and `cl_updaterate` **MUST** be the same

## A note on network rates

### How to set the rates

To set the rates, simply type `rate [number` into your console or add it to your autoexec.cfg

You should probably set your rates to the maximum even if your connection speed is not as fast as that of the command.

If we have a slow connection our experience _might_ be slightly improved by setting a value more in line with our speed. Feel free to try them out if you want.

### Table of rates

| connection speed | command               |
| ---------------- | --------------------- |
| 0.5 Mbps         | rate 62500            |
| 1.0 Mbps         | rate 125000           |
| 1.5 Mbps         | rate 187500           |
| 1.57 Mbps        | rate 196608           |
| 2.0 Mbps         | rate 250000           |
| 2.5 Mbps         | rate 312500           |
| 3.0 Mbps         | rate 375000           |
| 3.5 Mbps         | rate 437500           |
| 4.0 Mbps         | rate 500000           |
| 4.5 Mbps         | rate 562500           |
| 5.0 Mbps         | rate 625000           |
| 5.5 Mbps         | rate 687500           |
| 6.0 Mbps         | rate 750000           |
| 6.2 Mbps         | rate 786432 (new Max) |

## Acknowledgement

Thanks to APLIES for writing up [this pastebin](https://pastebin.com/2bBFijFY) which provided a good amount of content for the post.
