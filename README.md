[![Build Status](https://travis-ci.com/jmacdotorg/sweat.svg?branch=master)](https://travis-ci.com/jmacdotorg/sweat)
# Sweat

A chatty, distracting, and flexible workout timer.

# Examples

Run through a seven-minute workout while your computer reads aloud trivia from
Wikipedia, reports on the weather, and tells dumb jokes:

    sweat

Run through a seven-minute workout, but without any of that other stuff:

    sweat --no-entertainment

Run through a seven-minute workout with semi-randomized drills:

    sweat --shuffle

Have the program read news headlines instead of clicking around Wikipedia:

    sweat --newsapi-key=MyNewsApiKey12345

# Description

Sweat is a workout timer that helps distract you from the pain of
exercise by chatting incessantly, using your computer's text-to-speech capabilities to read news headlines, crack
strange old-man jokes, talk about the weather, and still manage to call out
workout prompts when necessary.

Sweat is optimized for the so-called [Seven-Minute Workout (7MW)](https://well.blogs.nytimes.com/2013/05/09/the-scientific-7-minute-workout/), which
leads you through twelve 30-second drills, with 10-second rests in
between. These focus on four types of exercise: aerobic, lower-body,
upper-body, and core. While it has sensible and widely accepted
defaults, you can change or expand its list of drills if you really
want, or adjust how many drills each workout entails, or the timing
involved.

Sweat features a friendly pause function, and a shuffle mode that will
randomize the drills you receive within each type while keeping the types themselves in order,
ensuring you get a varied and balanced workout.

Sweat assumes you already know how to perform the drills it calls out,
and trusts you to get through them in whatever way works best for you.
Sweat will never judge you.

Yes, Sweat is a command-line program. Get your butt off the chair once
in a while and onto the floor, fellow hackers. It's good for you.

## How Sweat is different from other timers

Sweat's major features that most other 7MW timers don't have:

### A speech-centered UI

Sweat guides you through voice alone (with a simple text transcription in its terminal window).

### Chatty entertainment while you struggle

Sweat will (unless you ask it not to) click through a randomly chosen thread of related Wikipedia articles while you work out and read aloud what it finds.
The workout takes priority, so this intentionally distracting chatter will not make you miss any exercise cues.

With a little extra configuration, you can have Sweat instead read you current news headlines from a variety of sources.

Sweat will also tell you the local weather during certain drills, and end by reading aloud the output of the \`fortune\` program (if available).

### Optional drill-shuffling

For variety's sake, you can shuffle the drills out of their standard order. While you still get three rounds of aerobic, lower-body, upper-body, and core drills in that order, Sweat will randomize the order of the three drills within each category.

### Pause between side-switching

Halfway through the side-plank drill, Sweat gives you a few seconds to adjust yourself.
(For some reason, few if any other timers seems to bother with this.)

### No-chair and no-jumping modes

A no-chair mode substitutes other drills when you find yourself in a space (e.g. a hotel room) with no suitably stable chair to exercise with.

A no-jumping mode is also available when you want to avoid stomping around on your downstairs neighbor's ceiling.

### Lots of configuration options

It's a command-line Unixish program, so of course it's far too configurable. Happily, its defaults should fit most needs...

# Installation

**First, make sure you have the `cpanm` program on your machine.** It is likely
available as "cpanminus" in your favorite package manager. (Or install it from
source, through the instructions at [http://cpanmin.us](http://cpanmin.us).)

Then, choose one of the options below.

## Installing the latest release

Run this command:

    cpanm Sweat
    

## Installing from source

Clone this repository locally, and then run these commands:

    cpanm --installdeps .
    perl Build.PL
    perl Build build
    perl Build install    # run under sudo to install at system-level

# Usage

Once installed, you can get a quick-reference guide like this:

    sweat --help

Or far more thorough instructions this way:

    man sweat

# Notes

This is this module's first release (or nearly so). It works for the
author's own use-cases, but it's probably buggy beyond that. Please
report issues at [the module's GitHub
site](https://github.com/jmacdotorg/sweat). Code and documentation
pull requests are very welcome!

# Author

Jason McIntosh (jmac@jmac.org)

# Copyright and licence

This software is Copyright (c) 2019 by Jason McIntosh.

This is free software, licensed under:

    The MIT (X11) License
