---
layout: post
title: "Dabbling into Home Servers"
date: 2021-10-13 20:46:00 +0100
categories: tech
--- 
Living in the UK involves certain restrictions on your habitual life, and here I don't mean the temporary shortages that happen at supermarkets and everywhere else these days, or the Brexit border bull****, but rather the risk of "torrenting" things. For that, I set myself up with a little home server in Romania, and another one in the UK, with the goal of downloading in Romania and automatically syncing the data here.

This article is fluid, meaning I aim to change it whenever I change one of the services running on either side. That might not always happen, but oh well. I also aim to use this as a reference for myself, to keep track of what I installed, where.

### Romania Server
- currently a Raspberry Pi 4B.

#### Services:
- Deluge (torrent client)
- Privoxy (HTTP proxy)
- nginx server, with letsencrypt credentials. Generally I aim to expose local services to the internet for remote access through here.
- Pihole. A must. Local IP is likely frozen.
- Plex. I tried out Sonarr + Radarr + Jackett as well, but I wasn't very impressed. Takes a lot of config.
- Syncthing. Nice to get the torrents automatically in the UK.
- frps, the server.

#### Extras and notes:
- This location has an exposed IPv4 address, which I use the router to publish its domain to DNS servers.

### UK Server
- currently a Dell thin client I got for free from work. Goal is to swap these two.

#### Services:
- Pihole
- Photoprism, looks like a great service.
- Plex. Much better performance on the thin client than on the RPi, naturally. Main reason why I want to swap.
- Syncthing
- frpc, the client.