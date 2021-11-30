# DevResources
A repo filled with stuff needed for a new machine! I'm mainly writing this for future me, but if you happen to be reading this, Hello! 👋

## New Machine Setup
I always end up forgetting or misplacing how/what to install on a new machine, so after picking up one of those shiny new M1 Mac's, I thought "Hey, let's automate the install of all of my stuff!".

Insert `Homebrew Bundle`!

Admittedly, I would have never of heard of this tool had I not listened to Casey Liss on my favorite podcast - [ATP](https://www.caseyliss.com/2019/10/8/brew-bundle).


First things first, installing [Homebrew](https://brew.sh).

With Homebrew installed, the fun begins.

As mentioned above, we'll be using Bundle. Bundle requires what is called a `Brewfile`, that contains apps, packages, etc from your current installation. 
To generate this file, run:

```
brew bundle dump
```

generating a Brewfile (hopefully you ran this from your home dir).

With this newly minted file, you can now run:

```
brew bundle install
```

Be patient! Especially if you're installing something like XCode 😅

Yes, this will require some maintenance/upkeep as you add new apps to the Brewfile, so I'll add it to this repo for safe keeping.

A good habit to get into is to install any available apps you use using this method - even fonts.

UI apps can be searched for using `brew search <appname>`
Apps available from the Mac App Store can be searched for using `mas search <appname>`
Fonts can be searched for in a similar manner, `brew search <font>`

Adding in `tap "buo/cask-upgrade"` will update all of your apps. 

Then to upgrade them, `brew cu`
