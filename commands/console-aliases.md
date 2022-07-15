---
title: CSGO Console Aliases
section: commands
description: Console aliases are a way of creating shortcuts for commands that we tend to use a lot.
image: assets/posts/rcon3.png
comments: true
layout: ../../layouts/MainLayout.astro
herotext:
  - Have you ever thought to yourself that the commands "quit", "retry", or "disconnect" take too long to type?
  - Then a console alias is everything you ever wanted.
---

## What is a CS:GO Console Alias

An alias is a console command that invokes other commands.

Aliases are only active in the game session they were initiated on, so they are not stored in your games settings once you close the game.

If you have an alias you want to be persistent across restarts, you'll need to set the alias in your [autoexec.cfg](/commands/getting-started.html) file.

## My Aliases

This are my recommended aliases.

```
alias "q" "quit"
alias "d" "disconnect"
alias "rr" "retry"
alias "rs" "mp_restartgame 1"
alias "exe" "exec autoexec"
alias "c" "clear"
```

## Making your own

The alias command is pretty self-explanatory `alias "your short command" "the actual command"`

You can bind aliases to your CFG files so instead of using `exec nadeTraining` we can use `nade`

```
alias "nade" "exec nadeTraining"
alias "getNades" "give weapon_incgrenade;give weapon_molotov;give weapon_hegrenade;give weapon_flashbang;give weapon_smokegrenade;"
```
