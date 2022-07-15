---
title: CSGO Launch Options
description: This guide explores the recommended launch options for CS:GO as well as identifying which options have been recommended not to use by the Devs.
section: commands
comments: true
image: assets/posts/launch-options.png
layout: ../../layouts/MainLayout.astro
herotext:
  - This guide explores the recommended launch options for CS:GO as well as identifying which options have been recommended not to use by the Devs.
---

## What are the launch options

Launch options are parameters that you set for steam games in order to change languages, run autoexecs, etc... Back in the they, these used to have significant impact on your game, but these days that’s no longer the case apart from perhaps ‘-novid’ which basically just turns off the intro of the game.

We need to be careful when copying launch parameters from the internet because old launch parameter which seemed to do magic to your fps back in the day either have no impact or its use has been discouraged by Valve developers.

## Recommended launch options

These are the launch options that we recommend.

```
-tickrate 128 -novid -refresh 144
```

`-tickrate 128` any server you create in-game will be running in 128 ticks.

`-novid` skips the video played when you opens CS:GO.

`-refresh <144/60>` set it to `144` or `60` depending on your screens refresh rate.

`-language english` change `english` for any other language or custom language if you want to run CS:GO in a different language than that of Steam.

`exec autoexec.cfg` if we have [an autoexec file](/commands/getting-started.html#creating-an-autoexec) we want it to run when we open CS:GO

## Other launch options

> ⚠️
>
> **If you are using mobile browser**: Be very careful here!
>
> Some of this commands might make no difference in your game experience, some could give you a couple FPS and others could deduct you another couple of FPS.
>
> Generally, the less launch options you use, the better, but feel free to try them out.

`-console` enables the console and makes it visible when you open the game. Some people like to have it to make sure their autoexec has loaded.

`-high` will launch the game in high-priority mode. This could work for low-end computers. Try it out and if you see no gain, remove it.

`-threads <number of cores/threads>` sets the number of threads of your CPU the game should use. I have not gained FPS with this option but again, feel free to try it out.

`-full / -fullscreen` makes the game run in fullscreen mode. You should set this from the game menu.

`-windowed / -window / -sw / -startwindowed` makes the game run in window mode. You should set this from the game menu.

`-noborder` removes the Windows border if running on window mode.

`-nod3d9ex` used to make alt-tabbing faster. Its enabled by default.

`-autoconfig` resets the custom settings from the game.
