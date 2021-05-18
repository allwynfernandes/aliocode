---
title: "Installing Java on Linux"
date: 2021-05-18T19:59:17+05:30
draft: false
---

## First figure out your why
This afternoon I needed to setup java on my personal computer to run Metabase which is a fantastic open source data visulization/ analytics/ BI tool. You can find out more about my fanboying and curious writing here. Now metabase required that I have java running on my computer. Ironically, I didn't was no basic version of java on my computer (thank you Ubuntu, I guess).

## The obvious options
A quick google search revealed the simple (but not so simple) command I had to run to get java up and running on my machine.
```bash
sudo apt install default-jre
```
But that went no where. I got an error immediately telling me I had some unmet dependencies. They looked something like this:
```bash
E: Package 'default-jre' has no installation candidate
```
then this
```bash
E: Unable to correct problems, you have held broken packages.
```
This went on for a while with different packages and installation methods detailed on Stackoverflow.
I even went as far as downloading the .tar zip file and installing it manually. Needless to say, that didn't work either.

All through this, I just kept thinking to myself, "Life on windows was so much more straightforward" Not simple, straigforward. I like things that are straightforward.
While none of the above techniques worked, I intensified my google search, finally landing up on SDKMAN

## The one true god
Finally, I found my answer on [this](https://stackoverflow.com/questions/52504825/how-to-install-jdk-11-under-ubuntu) StackOverflow post.
An absolutely elegant solution. The idea being: An installation / environment manager for Java (and other SDKs). As one of the comments on SO described it-- "SDKMan is to Java what Anaconda is to Python". Coming from python, this statement instantly put a smile on my face!
So finally, here's the code I used to install Java on my Ubuntu 20.04 machine:

`# First Install SDK Man`
```bash
$ curl -s "https://get.sdkman.io" | bash
$ source "$HOME/.sdkman/bin/sdkman-init.sh"
$ sdk version

```
`# Then install Java`
```bash
$ sdk install java
```
Done! That's it. You have Java on your system now. To verify you can run `java --version`.

And that's how you install Java on your linux computer, the easy, hassle-free and straightforward way.