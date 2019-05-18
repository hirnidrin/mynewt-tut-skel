# Mynewt skeleton app


## Overview

This repo contains some of my first Mynewt learning steps. It is a very simple skeleton
app that includes some of the most appealing beginner features / subsystems that come 
for free in Mynewt, like:

* console, RTT
* configuration
* stats
* logging
* watchdog
* firmware: remote / OTA update, signed code

These features are useful in almost any app, so after completion, I hope to have a small skeleton that is useful as a starting point for my further Mynewt endeavours.


## What the app shall do

Basic blinky app, with these bells and whistles:

* Config values stored in flash, read/write using RTT console access
  * ledon [ms] → LED on duration, default = 500
  * ledoff [ms] → LED off duration, default = 500
  * watchdog [s] → watchdog reset timeout, 0 = watchdog off, default = 5
  * restore defaults on factory reset
* Stats stored in flash, read using RTT console access
  * LED blink count since last power-on
  * LED blink count since last factory reset
  * watchdog resets since last factory reset
  * cleared by factory reset
* Buttons
  * 1 - factory reset the target
  * 2 - crash/hang the target, so it comes alive only after power cycle or watchdog
* Logs stored in flash, read using RTT console access
  * persistent until factory reset
  * config changes
  * watchdog resets


## Tutorial sessions

The project consists of several tutorial apps.

1. It all starts with the default blinky app.
2. Clone it and use as base of the next tutorial step.
3. Add one of the new features that I want to learn.
4. Goto 2.

## Requirements

* I have a Nordic nRF52840 dev kit (model pca10056).
* The Mynewt environment is [installed and running](https://mynewt.apache.org/latest/newt/install/newt_linux.html) on my Ubuntu 18.04 box.
* I have successfully compiled and run the [blinky tutorial](https://mynewt.apache.org/latest/tutorials/blinky/blinky.html) on my target board.
* I have read some of the Mynewt doc.



