---
title: Server Setup Part 1
description: This guide will show you how to setup and use a CSGO server using the DatHost service
section: guides
layout: ../../layouts/MainLayout.astro
herotext:
  - Since PopFlash is now a paid service you might be wondering how can you setup 10-mans with your friends or even scrim against other teams. Fear not for this guide will show you how to setup up your own server for relatively cheap.
comments: true
image: /content/posts/server-setup-1.png
date: 2020/05/06
---

## Pre requisites

### Enabling the developer console

Pretty basic, we will use the console to execute scripts remotely in the server. If you haven't enabled the console check our [getting started page](/commands/getting-started.html)

### Creating a DatHost account

DatHost is a server rental company that allows you to pay as you go. This means that if you don't use your server at all for a month you wont pay for it.

You get a MYSQL database for free with your CSGO server which come in pretty handy if you want to keep a leader board if you run some 1v1 arenas or a retake plugin.

[Follow this link](http://dathost.net/r/mlivwi) to signup and create your first server.

DISCLAIMER
I am not sponsored by DatHost. I'm just happy with their service and can recommend it due to its ease of use.

If you want to help out and get some free credits use our [signup link](http://dathost.net/r/mlivwi)

## Creating a server

One you're logged into your [DatHost.net](http://dathost.net/r/mlivwi) account. Click on the `Add Server` button and select the CSGO icon.

<img src="/content/resources/server/select-server.png" class="centered" alt="DatHost.net select server type" />

Fill up the form that appears, give your server a name and an address and click the `Rent` button.

## RCON Settings

Rcon allows you to change your csgo game server settings via the in-game Console. Using Rcon, you can issue commands to password your server, change to a certain map, restart the map, pause the game, start your GOTV and even kick or ban a rude player. In order for you to gain Rcon of your server,however, you will need your Rcon / Admin Password.

You can set your RCON user and password in `Control Panel > Your Server > Edit > Basic Settings`

<img src="/content/resources/server/server-settings.png" class="centered" alt="DatHost.net CSGO server settings"/>

## Server Scripts

By default DatHost includes a wide variety of CFG's in you server for you to use.

You can check out all the included CFG's in `Control Panel > Your Server > Edit > Configs`. By default you'll see something similar to:

<img src="/content/resources/server/server-configs.png" class="centered"  alt="DatHost.net CSGO server config"/>

The one we will be using today will be the `esl5on5.cfg` which as you would expect sets up a 5v5 game with ESL's config.

## Running Commands With RCON

Open up CS:GO and open up your console and paste the connect command found in DatHost. For this example the command is `connect csgoconsole.datho.st:27981; password yoursecurepassword`.

Once you're connected to the server we can go on and connect to RCON.

<div class="flex flex-wrap">
<div class="w-full md:w-1/2 md:pr-2 ">

## Connecting to RCON

Open up the console again, and type:

`rcon_password yourrconpassword`

Hit send and if everything worked out we can try the `rcon status` command and we should see something similar to this:

<img src="/content/resources/server/rcon1.png" class="centered" alt="How to RCON in CSGO servers"/>

</div>
<div class="w-full md:w-1/2 md:pl-2 ">

## Running the game script

If we have correctly connected to RCON we can start executing commands on the server. Lets try to load ESL's 5on5 CFG so that we can setup our first PUG.

Open the console and type `rcon exec esl5on5.cfg`. If this works we'll see information being outputted to our console.

<img src="/content/resources/server/rcon3.png" class="centered"  alt="How to run scripts in CSGO servers"/>

</div>
</div>

## Server commands

We've created a page specifically for [server commands](/commands/server.html) that you can check up at any time.

## Wrapping it up

We've seen how to setup a basic server and execute commands remotely on our server. We will cover how to setup more advanced mods like 1v1 arenas, retakes or practicemode in further guides.
