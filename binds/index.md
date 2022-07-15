---
title: Binds
description: The CSGO console command bible
sidebarDepth: 2
comments: true
section: commands
layout: ../../layouts/MainLayout.astro
herotext:
  - We have compiled a list of useful binds for you to use in-game. They are ready to be copied and pasted to your autoexec.cfg.
---

## Recommended Binds

### Jump-throw Bind

Throwing complex smokes has never been easier. Press the button whilst holding down left click to perform the jump-throw.

```
bind v "+jump;-attack;-jump"
```

The key `v` is used in this bind.

### Volume Toggle Bind

¿Tired of your teammates shooting a fully-loaded Negev at your head as soon as you spawn?

¿Are you playing FFA and want to listen to music? With this quickbind you can quickly toggle your game volume with a simple button press

```
bindToggle "yourkey" "volume 0.3 0.03"
```

### Grenade Binds

Use the following binds to set specific keys for each grenade. Its handy to have all the grenades bound to something.

```
bind x "use weapon_knife; use weapon_flashbang"
bind c "use weapon_knife; use weapon_smokegrenade"
bind 4 "use weapon_knife; use weapon_molotov;use weapon_incgrenade"
bind 5 "use weapon_knife; use weapon_hegrenade"
```

By using `use weapon_knife` we cancel the throw animation making it faster to pull out a nade.

### Mute chat and radio bind

It comes in pretty handy to have binds for toggling sounds in the game.

Mute the annoying guy that doesn't stop spamming the chat and/or radio commands.

```
bind KEY "ignorerad; ignoremsg;"
```

### Quick Bomb Drop Bind

Dont go alone with the bomb. This helpful bind will drop de bomb without the need of you switching to it and dropping it manually

```
bind b "use weapon_knife; use weapon_c4; drop; slot1"
```

By default `b` is bound to the buy menu. You can add `buymenu` at the end of the bind to use `b` for buying and dropping the bomb.

### Fake Flash Bind

Desperate times require desperate measures. Using your pistol as a fake flash could give you an easy kill when enemies turn around. This bind will switch to your pistol and drop it automatically.

```
bind "t" "use weapon_knife; use weapon_p250; use weapon_hkp2000; use weapon_glock; use weapon_tec9; use weapon_fiveseven; use weapon_deagle; drop"
```

### Jump Duck Bind

This bind will help you getting on top of some objects that require you to jump and crouch.

```
alias +jumpduck "+jump;+duck"
alias -jumpduck "-jump;-duck"
bind alt "+jumpduck"
```

### Smoke Lineup Crosshair

Smoke lineups can get pretty complex and abstract at time. If only your crosshair was as big as your screen to make the lining up easier.

```
bind y "toggle cl_crosshairsize 1 1000"
```

Change the value `1` for your usual crosshair size.

### Remove Blood Bind

Sometimes blood splatter can worsen the visibility of enemies when we're playing a game. With this bind you'll remove all the blood everytime you try to be sneaky by pressing `shift`.

```
bind "SHIFT" "+speed;r_cleardecals"
```

### Switch Hands Bind

Some people like to play with the gun on the left side and some people like it on the right side. Why not both? Quickly change between left and right hand with this bind.

```
bind CapsLock "toggle cl_righthand 0 1;r_cleardecals"
```

Bonus `r_cleardecals` to remove blood splatters on hand switch. ;)

### Mouse Wheel Jump Bind

If you're trying to bunny-hop you already know this bind. Make you player jump when you use your scroll wheel.

```
bind mwheelup "+jump"
bind mwheeldown "+jump"
```

### Change Map Zoom Bind

Change the map zoom level when you need it to show as much of the map as you need at any given time

```
bind mwheelup "+jump"
bind mwheeldown "+jump"
```

### Increase Volume When Shifting Bind

This simple bind increases the volume of the game when you press the shift button. That way it will be easier to listen to sound cues when you are trying to be sneaky.

```
alias +shiftVol "incrementvar volume 0 1 0.5;+speed"
alias -shiftVol "incrementvar volume 0 1 -0.5;-speed"
bind shift +shiftVol
```

### Toggle Net_graph With Scoreboard Bind

A simple script that will toggle the net_graph information with the scoreboard for less distraction while playing.

```
net_graph "1"
net_graphpos "2"
net_graphheight "1"
alias +scorenet "+showscores; net_graph 1"
alias -scorenet "-showscores; net_graph 0"
bind tab "+scorenet"
```

## Suggest a bind

Did we miss a bind? Follow the link below and submit it to CSGOConsole so that everyone can use it.

<a href="https://forms.gle/pZiijbWFpTFUm9gCA">Submit Bind</a>
