---
layout: page
title: Mastodon
---
# cannabisCatsCafe  

> I'm just here for the link, dude  
>[cannabiscats.cafe](https://cannabiscats.cafe)

## Context 

With the #TwitterMigration happening I've seen a lot of interest in Mastodon grow over the last few weeks, so I've decided to take another go at hosting an instance. 

__It's important that the cannabis community move off of the profit driven platforms that have long ostracized them.__

In that spirit I have stacked out some space in the fediverse on the cheap (as is tradition around here) and setup camp.

### The Search
Previously I setup a server on a $5 digital ocean droplet with their "One Click Install"
I quickly discovered that the $5 droplet wasn't going to cut it and quickly lost interest. Digital Ocean agrees and you can't use their Mastodon image on anything under their $12 tier now.

Wih Digital Ocean priced out, and at the time of writing this their image was still v3.5 I wanted 4, baby. I started looking at managed hosting providers, mainly masto.host for their $6 beginner tier, but they still haven't opened reg back up so I said "I'm going solo." 

RaspberryPi is hosting their instance on a pi in the sky (love it) and their provider posted this about needing at least 4 gigs to be comfortable.

<iframe src="https://social.mythic-beasts.com/@beasts/109325844364238020/embed" class="mastodon-embed" style="max-width: 100%; border: 0; height:400px;" width="400" height="400" allowfullscreen="allowfullscreen"></iframe>  

I used that information as a starting place for my search. ~4 gigs of ram and as much storage as I could get. But I knew I didn't want to go that route with mythic beasts.

What I ended up settling on breaks down to less than $10 a month. Not too shabby, and I predict this should sustain me and whatever small community I gather for a while.

## Setup

__Server:__ Renting a VPS from a host in Chicago(spend local) for $7+tax a month. 
* Getting me a single core cpu with 6gb of ram and 50gb of storage on an SSD, running ubuntu 22.04(I'm scared of change, whatever)

__Software:__ Vanilla Mastodon 4
 * Nothing fancy, I was thinking about using hometown but I wanted those v4 features.
 * There were a few gotcha's following mastodon's official documentation but nothing a few DDG searchs couldn't fix  

__Domain:__ [cannabiscats.cafe](https://cannabiscats.cafe) less than $10/year
