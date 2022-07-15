---
title: CSGO Grenade Training
description: Throwing good grenades is a must for all good players. Perfection can only be achieved through practice, and practice you shall...
section: guides
layout: ../../layouts/MainLayout.astro
herotext:
  - Throwing good grenades is a must for all good players. Perfection can only be achieved through practice, and practice you shall with this CFG.
image: /content/posts/grenade-training.png
comments: true
date: 2020/05/07
---

## Recommended Binds

Before you get into a server to practice, I recommend that you have this two binds set up in your autoexec.

```
bind "key" "noclip"                       // allows you to fly around the map
bind "key" "sv_rethrow_last_grenade"      // rethrows the last grenade
```

## The configuration file

The file is pretty self explanatory with comments for groups of similar commands.

```
// PRACTICE config
clear

// Enables cheat commands
sv_cheats 1

// No player limit in teams
mp_limitteams 0
mp_autoteambalance 0
mp_roundtime 60
mp_roundtime_defuse 60 // 60 minutes in defusal maps
mp_respawn_on_death_ct 1
mp_respawn_on_death_t 1

// Money and buy zone
mp_maxmoney 60000
mp_startmoney 60000
mp_buytime 9999
mp_buy_anywhere 1

// Disables freezetime
mp_freezetime 0

// Ammo
sv_infinite_ammo 1
ammo_grenade_limit_total 5 // allows to have all nades

// Grenade trajectory visible
sv_grenade_trajectory 1
sv_grenade_trajectory_time 10 // time visible

// Bullet impacts
sv_showimpacts 1
sv_showimpacts_time 10 // time visible

// Giv all grenades
mp_ct_default_grenades "weapon_flashbang weapon_hegrenade weapon_smokegrenade weapon_decoy weapon_incgrenade"
mp_t_default_grenades "weapon_flashbang weapon_hegrenade weapon_smokegrenade weapon_decoy weapon_molotov"

// Setup
bot_kick
mp_warmup_end
mp_restartgame 1

//Write to console
clear
echo ""
echo ""
echo ""
echo "http://csgoconsole.com/resources/training-configs.html"
echo "practice.cfg loaded, GLHF"
echo ""
echo ""
echo ""
```

## Download

You can download the CFG by saving the following file into `C:\Program Files\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg`.

To run the file create an offline game with bots and run `exec practice.cfg` in your console.

<a text="Download File" url="../../practice.cfg" icon="software-download" cssStyles="inline-flex lg"></a>
