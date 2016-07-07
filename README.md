Note: this is in-progress....check back later

#@grow_slow

This is a guide to making your own version of [@grow_slow](http://twitter.com/grow_slow), which tweets a photo of a plant once a day. Of course, you can use this to do whatever you want — **these instructions will cover the technical aspects of using a Raspberry Pi to take a photo with a webcam and tweet it once a day**. This is meant to be useful for people who might not have a lot of experience with coding, or with Raspberry Pi. You can read more about [@grow_slow](http://twitter.com/grow_slow) [here](http://nicole.pizza/grow_slow).

##Things You Need

* Raspberry Pi
* Wifi module (might be included with your Pi)
* USB Webcam
* a plant
* External monitor*
* External keyboard*
* External USB mouse*
* HDMI cable*

*if it's your first time using a Pi, you should use these things, but they're not required

##1. Setting up your Pi

A Raspberry Pi is a tiny computer that can do many things. They're nice because you can just leave them running somewhere in your house, and whatever weird art project you're doing won't rely on your own computer being open or connected.

For our purposes, we will use the Pi to take photos with a webcam and tweet them. 

[Follow this guide](https://www.raspberrypi.org/help/quick-start-guide/) to set up your Pi for the first time, plugging it in to your monitor with your HDMI cable, and also plugging in the keyboard and mouse. Then, [connect your Pi](https://www.raspberrypi.org/documentation/configuration/wireless/) to your wifi network.

### Optional but recommended: SSH

Especially if it's your first time, it's nice and easy to be able to plug your Pi into a monitor and use it that way. However, if you don't want to pull out your keyboard, monitor and mouse every time you want to change something, and more importantly, if your webcam is in an inconvenient place for you to also plug in your monitor, you'll want to set up SSH access.

What SSH allows is for you to control your Raspberry Pi from another computer, which is much more convenient. However, you'll be running things entirely from your [command line](https://en.wikipedia.org/wiki/Command-line_interface) (Terminal on a Mac, or Command Prompt on a PC). If you don't have much or any experience with it, it can be a little confusing, but this can be good practice. If you are comfortable with the command line, it's highly recommended that you set up SSH. [You can follow this guide to do so](https://www.raspberrypi.org/documentation/remote-access/ssh/). 

##2. Setting the date

Now that your Pi is up and running, open the Terminal from the toolbar at the top, or log in via SSH. You should see something that looks like this:

`pi@raspberrypi ~ $`

We're going to set the date so that our Pi is on the right time.

Type this in and press enter:

`date`

You should get something formatted like "Wed 6 Jun 20:11:24 EDT 2016." And if it's correct, then hooray, you don't have to do anything else. If it's not, enter:

`tzselect`

and follow the instructions to set your timezone. Once you've done it you can confirm by entering `date` again and it should be correct.














