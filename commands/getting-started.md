---
title: Getting Started
comments: true
layout: ../../layouts/MainLayout.astro
section: commands
herotext:
  - To make the most out of CS:GO we will have to enable the developer console in game. We also recommend keeping your settings in a auto executable file so that you can take it with you easily to tournaments.
---

## Enabling the console

The developer console is a part of the UI that allows you to tweak the most of the aspects of the game. From the console you can do anything from changing you crosshair to setting up a server.

Unfortunately the developer console is disabled by default so we will have to manually enable it from the settings menu.

`Settings > Game Settings > Enable Developer Console > Yes`

![How to enable the CSGO developer console](./.assets/devconsole.jpg#thumbnail-lg)

We can then assign a button to open the console by using `bind “anykey” "toggleconsole"` replacing `anykey` for your desired key.

## Creating an autoexec

We will have to create an empty file name `autoexec.cfg` and place that file inside `C:\Program Files\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg`.

![How to create a CSGO autoexec](./.assets/autoexec1.png)

After adding the file we must edit it and add the `host_writeconfig` command at the end of our file such that our settings from the autoexec get written to the game's config file. You can copy and paste the following code to the end of your `autoexec.cfg`.

```
host_writeconfig                    //Store current settings to config.cfg
clear                               //clear the console output

echo "autoexec.cfg loaded, GLHF"    //write to the console
```

In order for the autoexec to be loaded we must add the following launch option to our game: `exec autoexec.cfg`
