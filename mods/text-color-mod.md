---
title: Enhanced Text Color Mod
description: The Enhanced Text Color Mod modifies the translation file from Bananagaming to provide a cleaner look to the chat and grenade messages.
image: /content/posts/textcolormod.png
date: 2020/04/20
section: mods
layout: ../../layouts/MainLayout.astro
herotext:
  - The Enhanced Text Color Mod modifies the translation file from Bananagaming to provide a cleaner look to the chat and grenade messages.
---

## About the mod

This version provides some further customization to how the chat messages are displayed as well as modifying some of the colours from the original mod.

You can find the complete file as well as some explanations to the modifications made so that you can extend you custom language if you have one.

## Enhancements

<div style="display:flex;  ">
![CSGO Enhanced Text Color Mod](/content/mods/text-color-mod/textmod_1.png)

![CSGO Enhanced Text Color Mod](/content/mods/text-color-mod/textmod_2.png)

</div>
<div style="display:flex">

![CSGO Enhanced Text Color Mod](/content/mods/text-color-mod/textmod_3.png)

![CSGO Enhanced Text Color Mod](/content/mods/text-color-mod/textmod_5.png)

</div>
### Improved Grenade Messages

The grenade radio messages have been altered to remove the word `(RADIO)` as well as displaying clearyl who threw which grenade and from where did they throw it.

```
"Game_radio"			"%s1 : [ %s2 ]"
"Game_radio_location"	"%s1 : %s3 [ %s2 ]"
```

### Improved Chat Messages

Chat messages from teammates and enemies have also been improved to reduce the amount of text displayed every time an enemy or teammate sends a message.

```
"Cstrike_Chat_CT_Loc"		"[CT] %s1 @ %s3 :  %s2"
"Cstrike_Chat_CT"			"[CT] %s1 :  %s2"
"Cstrike_Chat_T_Loc"		"[T] %s1 @ %s3 :  %s2"
"Cstrike_Chat_T"			"[T] %s1 :  %s2"
"Cstrike_Chat_CT_Dead"		"[CT]*DEAD* %s1 :  %s2"
"Cstrike_Chat_T_Dead"		"[T]*DEAD* %s1 :  %s2"
"Cstrike_Chat_Spec"			"[Spectators] %s1 :  %s2"
```

### Customization

At the end of the language file we will find all the available colors commented out. Each color is encoded in a special character that is display like ``.

If we copy and paste any symbol, all the text after the symbol will take the symbol's colour.

```
// - White
// - Red
// - Team color (may cause player's color dot before symbol)
// - Green
// - Light green
// - Green(money awards)
// - Light red
// - CT color
// - Light blue
// - Violet
// - Light red 2
```

## Download

You can find the modified language file by following [this link](/csgo_bananagaming.txt). Just save the .txt file in your computer and place it in `C:\Program Files\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\resource`

![How to install CSGO text color mod](./text-color-mod/textmod_folder.png#centered)

In order to apply the language file we must add the following launch option to our game `-language bananagaming`.

Images by [Bananagaming](https://bananagaming.tv/textcolormod.php) and [CSGOConsole.com](/)

## Alternative Versions

[Thinkii](https://twitter.com/thinkiiCS) has uploaded an alternative version to the text color mod which shows player names as well as modifying the chat to make remove clutter and make it clearer.

You can see screenshots of his version in [this tweet](https://twitter.com/thinkiiCS/status/1252308450190798848) and the download link is in his [github repo](https://github.com/thinkii/CSGO/blob/master/textmod/csgo_competitivo.txt)

### Acknowledgement

The original modification can be found in [Bananagaming's](https://bananagaming.tv/textcolormod.php) website. Credit to him for creating the mod.

### Comments

<!-- <Disqus/> -->
