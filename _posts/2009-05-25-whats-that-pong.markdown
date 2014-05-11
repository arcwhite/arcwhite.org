---
author: admin
comments: true
date: 2009-05-25 08:15:36+00:00
layout: post
slug: whats-that-pong
title: What's that Pong!?
wordpress_id: 111
categories:
- Game Dev
- IT
---

_Over the past few weeks, I've been working on some iPhone game development. For a long time I've wanted to get back into game dev (long abandoned after University as something that I didn't have time for) - the iPhone is proving to be a fun platform to work with._

_So here is a brief treatment of my first project, which for the moment goes by the moniker **DotSlashPong**. It's in (working, but early) prototype at the moment, but I'll tell you more about it as development continues - and provide a few screenshots in about a months' time!
_

**Overview**

Pong is an ancient videogame classic. The original game featured a few simple elements - two paddles, a ball bouncing between them. The object of the game was to bounce the ball off your paddle in such a way that your opponent failed to subsequently hit it. If the ball goes off your side of the screen, your opponent scores a point.

Simple. Laughably primitive by today's standards.

DotSlashPong takes that gameplay and tears its face off. The basic gameplay is the same, albeit sped up somewhat to cater for the faster twitchin' reflexes of today's gamer on the go. The paddle is controlled by subtle twisting of the iPhone, using the accelerometers to convert that twisting motion into movement of the paddle. We add a liberal sprinkling of power-ups, some extremely shiny neon graphics, a theme, a subtle whiff of a metagame, and occasional complete breakdown of the expected Pong metaphor.

Then we toss that on the iPhone, liberally apply multiplayer and network connectivity in some unexpected ways, and see what we get.

<!-- more -->

**Theme**

Does Pong need a theme? Not particularly. But for the sake of tying the graphics and various gameplay modes together, we'll fabricate a deliberately flimsy one. The goal will be to hint at the theme for the most part, and let the player(s) supply more of the narrative.

The game itself is a hacking interface - a highly abstracted command and control system for a bunch of programs used to take control of hosts on the intertubes, and defend against other hacker-types doing the same. Most of it is automated, but it needs some human input; input provided in the form of fast twitch responses to highly formulated questions in a 2d game environment! Hooray!

This contrivance allows us to fill our game with all sorts of bright neon computery graphics, 3d objects in the background, dazzling powerup effects and surprising integrations of the game world and the internet (which I'll not yet discuss here).

The players are two hackers, vying for supremacy over each other. Initially connected to a neutral server, the game rolls back and forth across proxy servers until one of the hackers is knocked off the internet, their machine pwned by their opponent.

**Basic Elements**



	
  * Paddles - Represent a player's control over the virtual world / hacking interface. Powerups (and powerdowns) can increase or decrease the size of the paddle, double it, triple it, move it up or down the playing environment, or make viruballs behave strangely as they draw closer ...

	
  * Viruballs - Initially just one, these are viruses sent over the internet, through the server both 'hackers' are currently connected to, where they attempt to infect the other hacker. Bouncing them off the paddle destroys them and instantly launches a counter-virus back at your opponent - which happens to look exactly like a bouncing ball! Powerups and downs can do all sorts of weird things to viruballs...

	
  * Servers - The "level" upon which play takes place. Initially a quiet and unresponsive chat server, the battle soon wages up and down the line of proxy servers each hacker has at their disposal; occasionally triggering antivirus software, or drawing the attention of law enforcement counterintrusion AIs...

	
  * Obstacles - highly privileged processes on the server, which happen to look and behave exactly like solid brick walls. _Usually_ impervious to harm, the viruballs bounce off them - increasing the complexity of their trajectory. Some are positioned to obstruct player paddles. Some of them are null points, which absorb things that hit them...

	
  * Powerups - all sorts of weird and wonderful code lives out there on the Internet. Some of it can be useful - doubling or mutating viruballs, increasing their efficiency (speed) or giving them strange properties. Some of it can be downright harmful, backfiring in horrible and unexpected ways.
Their use should be subtle, but potentially powerful - and highly dependent on the server/level you're in!


**Graphics**

I really wanted to demonstrate this here, but so far I haven't come up with anything satisfactory. Much of my inspiration is drawn from the 'cyberspace' scenes of Ghost in the Shell: Stand Alone Complex, with a liberal smattering of Beat.Trip-Beat sensibilities, and a touch of Geometry Wars. The player should feel like they're using some hyperadvanced computer interface of joy and wonder; the underlying thematic metaphor of 'hacking' should be conveyed by special effects (without getting in the way of gameplay, except where we WANT those effects to become part of the experience directly ...)

**Desirable Features**



	
  * Surprising and Interesting Integration with the Internets (more to be discussed later!)

	
  * Multiplayer - target iPhone OS 3.0 and its delicious ad-hoc networking

	
  * Surprising Gameplay - Mess with the established conventions; give the players ongoing gameplay puzzles and surprises to overcome


**Progress to Date**

We have a prototype working, which effectively demonstrates the most basic gameplay mechanisms and the outlines of the code structure to come.

