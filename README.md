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

And, as promised my personal [Brewfile](https://github.com/fcarran/DevResources/blob/main/Brewfile).

## The Ultimate Terminal

The default terminal is... fine. But it could be so much better. If you're in the tech world, you're probably already using something different, whether that be Hyper, or the default app. My personal choice is iTerm2 (already installed thanks to the handy dandy Brewfile).

iTerm2 is great on it's own, with it's fancy broadcasting to all panes and ability to [sync](https://shyr.io/blog/sync-iterm2-configs) settings across devices, but the default shell is not. Enter [oh-my-zsh](https://ohmyz.sh)! 

[Freecodecamp](https://www.freecodecamp.org/news/how-to-configure-your-macos-terminal-with-zsh-like-a-pro-c0ab3f3c1156/) has a great guide already on how to set this up, so I'll pick and choose what I ended up using.

And assuming oh-my-zsh is already installed - the terminal should now look a little cleaner. But wait, there's still some more things to do! Like themes, extensions, and icon packs! Luckily, this all gets written to a new hidden file in your directory named .zshrc.

If you've read ahead and taken a peak at my [.zshrc](https://github.com/fcarran/DevResources/blob/main/.zshrc) file, you might have already seen a few of my day to day extensions and aliases (nobody likes to type more keystrokes than they have to).

![aliases](https://github.com/fcarran/DevResources/blob/main/images/Aliases.png "aliases")


Personally, with oh-my-zsh I like using [PowerLevel10K](https://github.com/romkatv/powerlevel10k#oh-my-zsh). Run `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k` and once installed/rebooted the session you'll be walked through a setup wizard. 

Finally, set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`

PL10K comes with some pretty sweet icon sets, problem is you'll need a compatible font in order to view them - but trust me, it's worth it!

Now, my personal favorites should have already been installed via the Brewfile
```
cask "homebrew/cask-fonts/font-hack-nerd-font"
cask "homebrew/cask-fonts/font-meslo-for-powerline"
```

But in the event they aren't then can be installed after the fact, and setup in iTerm's settings like:
![iTermSettings](https://github.com/fcarran/DevResources/blob/main/images/iTerm-Settings.png "settings")

And once this is all set and done, voila! 
![Final](https://github.com/fcarran/DevResources/blob/main/images/iTermFinal.png "final")
