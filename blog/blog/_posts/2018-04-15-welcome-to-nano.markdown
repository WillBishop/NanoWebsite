---
layout: post
title:  "Welcome to Nano!⌚" 
date:   2018-04-18 12:00:00 +0930
categories: nano release
---

Wow, what a *loooonnnnggg* time coming. 

I've been working on Nano since before I even had an Apple Watch. Well... that's not *that* long, I got my Apple Watch on December 25th, [the same day I teased Nano for the first time.](https://www.reddit.com/r/AppleWatch/comments/7m0zbt/got_an_s3_for_christmas_i_already_know_strapping/). 

Nano has not been an easy journey and it hasn't come without its dissapointing times. But throughtout the development of Nano, I've learnt so much and met so many amazing people, and I'd like to talk about some of that today.

# The People

Wow, I did not expect to meet so many amazing people while developing Nano. As much as I'd like to list them all by name, I cannot do that on here (though, they are listed in the iOS app!). I would feel bad mentioning some people but not all, so I'll keep this pseudo-anonymous. Without all these people, Nano would not be what it is today.

### The Discord Helper
This person helped me to transform my Discord server from a boring ol' chatroom to a server with lots of chat rooms, ranks, permissions, and more. But they did more than just help me on Discord, they were always willing to test bugs and put fourth new ideas. For that, I thank you.

### The Translators
At launch, Nano will be available in three languages, English, Turkish, and Danish. I want Nano to be able to be used by as many people as possible, and the testers using their own time to help translate Nano truly shows the quality of people I had to help me all along the way.

### The Reporters
I have a bit of a love-hate relationship with these guys (many of which are also part of the translators or Discord groups). On the one hand, getting bug reports is great; It helps me make Nano as stable and feature-rich as can be. On the other hand, however, gee it's annoying! Now don't take me the wrong way, **I am not annoyed at the reporters**, I am annoyed at myself. Bugs are a testament to a developers skill, and no program is without bugs. But I spent countless nights (or very early mornings) fixing these bugs and neglecting my school work, 🤞🏻it pays off!.

# Development

Well Apple sure didn't make this easy, but why should they? I come from an iOS development background (despite never releasing an app), but WatchKit does *some* things better, and *some* things worse.

## The Good
* Tables on WatchKit make a bit more sense for newcomers, but coming from an iOS background, they can be tough to start with. For example, on iOS you can set the number of rows a table has using the `numberOfRowsInSection` delegate method like so 
    ```
    func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return something.count
    }
    ```
    However, on WatchKit, the number of rows is set like this
    ```
    table.setNumberOfRows(something.count, withRowType: "rowType")
    ```
    I actually prefer the second method, as it can be called from anywhere, but the consistency between iOS and watchOS is almost non-existant.
    
## The Bad
Unfortunately, it's a lot easier to find bad things than it is to find good things.
* Storyboard **only**; When you're developing for iOS you have a couple of options to build your User Interface, the two most common are *Storyboards*, and *Programatic-UI*. 

    The difference there is simple, with a *Storyboard* you can design your UI with a drag-and-drop interface, and connect your code to it. This method is incredible useful for beginners (or even experienced devs), but it has its own problems (such as working in a team, *Storyboards* can become bloated and prone to merge errors). A *Programatic-UI* works by building the entire UI in code, a favorite amongst iOS veterans. 
    
    But here's the problem, there is **no** option when developing for watchOS, Apple forced you to use *Storyboards*. Which means that as a developer, if I want to make my Reddit client look good, some trickery has to be at play.

* Poor image-support; Now this is an odd one, and one that I've been working on for months now with little success. On Reddit, images are a **huge** part of what makes up the site. Some pictures are too big or too high-resolution to be viewed on the Apple Watch's small screen. Throughout testing Nano, I had an email I could be reached by (nano@willbish.com), and one of the most common feature requests was image-zoom. Image-zoom is something that *is* a part of WatchKit, just not to us developers. An example of this is `Photos.app` on the Apple Watch, in which you can zoom with the crown and pan around with your finger. I've been trying to replicate this functionality, [but this is the closest I got](https://gyazo.com/3a92fb72b96795bd2338ede6c0e44ee7).

I'm hoping WWDC 2018 brings some more updates to WatchKit so I can further improve Nano.



