# Episode 4 - 11/17

### Intro

Hello and welcome! On this week’s show, we’re going to talk about the latest Bazzite and SteamOS releases, CachyOS’s new package manager, how to get started switching to Linux, and how Umbriel has helped me Take Control of My Tech

Show intro. Lots of stuff to get to today, but I want to share a couple of things that happened over the weekend. I went to a friends birthday party. It was 90s themed, and all anyone wanted to talk about was Jensen.

And my daughter broke the hinge on her laptop last week. Describe the fix, describe what I fucked up. Describe the next steps. Curse Lenovo for glueing the screen in place

<aside>
💡

AD #1 - Fastmail 

Fastmail is an email service for people like you and me. I love it’s one-touch integrations with 1Password and Bitlocker, which lets me easily create single-use email addresses when I sign up for new services. I also love its integrated domain support. You connect your domains to its backend and then spinning up a new address is as easy as a few clicks in your webmail interface. If you want to support the show, try it out free for 30 days. Go to [join.fastmail.com/wil](http://join.fastmail.com/will)l to sign up. There’s no obligation and they don’t even ask for your credit card.  You get a great email host that isn’t spying on you and they throw me a few bucks for everyone who signs up. Thanks Fastmail! 

</aside>

### News

- Jensen and the AI market
    - Could this be the franz ferdinand moment that causes the AI house of cards to topple?
- Bazzite is on the EAC v2 train w/ Bazzite 45 - [https://universal-blue.discourse.group/t/bazzite-45-is-here/12702](https://universal-blue.discourse.group/t/bazzite-45-is-here/12702)
    - Secure Boot has issues on the Steam Deck, at least for the moment
    - We talked about it a few weeks ago, but the TLDR is that Epic is using a lot of built-in Linux tech to secure the stack from cheaters, and bazzite should be ready for the rollout when it comes  (Epic Post: [https://onlineservices.epicgames.com/news/introducing-easy-anti-cheat-linux-v2](https://onlineservices.epicgames.com/news/introducing-easy-anti-cheat-linux-v2))
- SteamOS 3.10.0 Preview - [https://steamcommunity.com/games/1675200/announcements/detail/687522235410285334](https://steamcommunity.com/games/1675200/announcements/detail/687522235410285334?snr=2___)
    - Minor update but: Added support for HDMI 2.1 VRR (Variable refresh rate), FRL (fixed rate link), and ALLM (Auto Low Latency Mode)
        - I believe this means that SteamOS has support for the full set of HDMI 2.1 features now
        - This was stuff that the HDMI consortium was holding back from open implementations.
        - Reporting I’ve seen is that this will all be enabled by default with kernel 7.4, but with 7.3, which is what Valve’s shipping here, you need to flip some boot flags.
        - Find a link for this:
- CachyOS is working on a new package manager, which feels weird after shifting everyone to Shelly earlier this year. Includes support for the AUR and Flatpaks (like shelly), but doesn’t have support for AppPkg out of the box. Seems like the beta will be in the next Cachy release

<aside>
💡

AD 2 - I absolutely love Fastmail. It was the fastest I’ve ever signed up for a service after starting a trial—I think I switched my free trial to a paid one within about 30 minutes of starting to use it. It’s email that doesn’t spy on you that makes a bunch of the difficult stuff about managing email for your own domains easy. They make it easy to connect as many domains and inboxes as you want to your account. You can create single-use masked email addresses for signups inside 1Password or Bitlocker. 

If you want to support the show, try Fastmail out for free for 30 days. Go to [join.fastmail.com/wil](http://join.fastmail.com/will)l to sign up. There’s no obligation and they don’t even ask for your credit card.  You get a great email host that isn’t spying on you and they throw me a few bucks for everyone who signs up. Thanks Fastmail! 

</aside>

### Feature - How to Get Started Switching to Linux?

- We talked about this a ton in the early Dual-Boot Diaries days. These days the answer is dual-boot.
    
    <aside>
    💡
    
    - Linux is all about choices.
    </aside>
    
    - It can be a little paralyzing when you start out, but the thing to remember is that once you’re up and running, it’s pretty easy to try other stuff.
- Try some live distros - you can burn a thumbdrive (I love Ventoy for this, but Rufus works great too)
    - Explain Ventoy - Link
    - You’ll likely have to turn Secure Boot off if you have it on (you’ll want to turn it back on before you run a game that requires it (BF6, COD, etc)
- I like CachyOS, Bazzite, Pop!_OS and just plain Fedora are all good
    - For gaming, the first two are recommended
        - I haven’t spent much time with SteamOS on non-Steam hardware, but if you have an AMD card especially, it’s probably worth trying out.
    - Maybe talk about Bazzite vs. Cachy a bit here
- What actually changes in a distro?
    - What’s a distro? It’s just a selection of default (and sometimes custom software options, an updating ethos, and tools (like package managers, etc)
        - it isn’t worth yelling at each other about Distros
        - Update ethoses
            - Rolling vs. stable
            - What’s an immutable distro? see also Bazzite
    - Explain the software stack that makes the GUI work
        - Display Server - This is what draws the windows and handles things like mouse position and whether you’re clicking or not
            - Xorg (old, on the way out) and Wayland (new, but weird in a lot of cases)
        - Display Manager - This is the login screen and launches the different sessions
            - Common ones are GDM, SDDM
        - Window Manager - this controls thinks like window placement, window chrome, stuff like keyboard shortcuts, and even stuff like how the windows tile or don’t
            - you usually don’t need to know this part, unless you run a tiling window manager
        - Desktop Environment - This is the collection of apps and applets that controls how what you usually think of as an operating system. It includes a lot of the stuff you probably think of as the operating system.
            - KDE, Gnome, the main steamdeck UI usews Gamescope and just Steam as the DE
            - Some distros make different distros for each DE, some include the DE choice as part of the install
- The part of all this that matters is the Desktop Environment. KDE Plasma is what the SteamDeck runs for desktop mode
    - The short version is that KDE is more Windows-y (taskbar with a start menu)
        - Common wisdom is that it’s generally a little better for games because they tend to support gaming friendly features more (stuff like VRR and HDR) out of the box
    - Gnome  - more Mac like, with a dock and a persistent menu bar
    - A bunch of other weirder stuff -
        - Pop!OS has Cosmic, designed to be easy for Windows people, with lots of nifty features. It’s still pretty early,
        - Novel computer interfaces: tiling window managers like Niri and Hyprland and Umbriel (and Cosmic) - more on Umbriel in a moment
- Dual-booting
    - Best way to set up your machine to not screw something up.
    - First, back up your drive. You can use the old Windows Backup and Restore tool, or any number of a bazillion other apps. That’s out of scope for this.
    - Then you’re going to shrink the partition that’s got a few hundred gigs free (more if you’re going to do games) using the Windows Disk Utility. Pick the disk, right click, select Shrink volume
        - [https://learn.microsoft.com/en-us/windows-server/storage/disk-management/shrink-a-basic-volume](https://learn.microsoft.com/en-us/windows-server/storage/disk-management/shrink-a-basic-volume)
    - You’re going to start installing your distro of choice (Ventoy again) and depending on what you choose, when you get to the disk setup, you’re going to choose “Use available free space”
        - If you want to save yourself a bit of trouble, you’ll want to make sure your linux boot partition is at least 4GB and is *not* the same as your Windows boot partition. It’s totally OK to have two boot partitions in the modern era. You’ll point your UEFI boot process to the Linux partition, and Linux bootloaders are quite good at handing off to the Windows partition when you select a Windows boot.
            - Doing it this way also reduces the likelihood that a Windows update will bork your Linux boot partition. Windows won’t even know that the linux boot partition exists, so it can’t mess it up.
    - You may also get asked about the boot loader you want to install - I like Limine, but there are a bunch of good options. Grub, Limine, and rEFInd seem to be the most popular for enthusiasts/desktop users.
    - Once your install is done, you’ll pull the thumb drive, reboot the computer, and you should see a boot menu
        - If you still boot to Windows, you may need to change your boot order in your UEFI to point to the Linux boot partition first.
    - You should have a working Windows/Linux dual boot at this point! Congrats!

### My Linux Journey

- This week has been all about Umbriel
    - Umbriel is noctalia’s new Window Manager. It supports multiple tiling layouts + normal floating windows and some other nfity features
    - Ported my Niri config over, which took a few hours one day.
    - I love being able to switch a workspace between multiple tiling layouts. I find myself using the infinite scroll on my main layout still, but I’m using Dwindle (the Hyprland style where all the windows live in the available space on the display) for my Chat workspace.
    - Still not using stacking*
        - I am using stacking on the Scratchpad Workspace\
        - Explain scratchpads - they’re really cool
    - To-Dos
        - Some stuff is still weird - their screenshot configuration just doesn’t work right.
        - I need to go back and make sure all of my normal launching apps are actually launching.
        - OBS bugs
        - I need to test HDR in games.
        - I need to setup screen capture blocking for sensitive apps (mostly my password manager)

<aside>
💡

> Ad #3 Take Control of Your Tech Subscriptions
Plug the Sub - [takecontrol.content.town/subscrib](http://takecontrol.content.town/subsc)e
Ad-free audio podcast feed! 
Access to the community in Discord! 
Early access to episodes (whenever it’s posssible) 
The satisfaction of supporting an independent creator!
> 
</aside>

### Letters

> 
> 
> 
> A fan since the Tested days...
> 
> One thing I can't imagine using Windows without is 'Everything' search. It's increadible, I can get to my files and folders in a flash. I introduced it to my coworkers and the whole office is using it now.
> 
> All the best,
> 
> Alex 🖖
> 

> 
> 
> 
> Nick from Michigan here.
> 
> On my PC, I use VoidTools's amazing Everything app to do my universal search. I always struggled on my MacBook, whose search was better than Windows default but still worse than Everything.
> 
> This week I went searching explicitly for a Mac equivalent for Everything. The solution I came up with was [Cardinal.](https://github.com/cardisoft/cardinal) It was intentionally built to emulate Everything, and so it was immediately easy to use and vastly improved my Mac experience.
> 
> I even installed it via the Terminal and Homebrew. I've traditionally shied away from command line actions, preferring the easier GUI. But this podcast (and the Techpod) has encouraged me to try things that are uncomfortable to expand my knowledge and capabilities.
> 

> TVGM Asks:

Do you have a strategy syncing dotfiles between computers? I use Syncthing for syncing document files like Obsidian's Markdown files between my computers, home server, and phone and it works really well, but dotfiles are a bit more complicated as they're scattered (.local, .config, .var) and there are some things I don't want to sync like configs that contain display settings.

Also, thank you for recommending Niri / Noctalia. It is truly a game-changer for interacting with a desktop environment.
> 

Nate in For Collins - Good uses for my own domain

### Homework

- Last week’s homework is to do some (or all) of the Windows fixes above. Hop in the Discord, hit me on Bluesky, or drop a comment on the site and share what you’ve done,
    - People shared a lot of their tips, and we talked a bunch about LTSC versions of Windows and debloating scripts
    
    Shutup 10++
    [https://www.youtube.com/watch?v=IJSie_3ncc8](https://www.youtube.com/watch?v=IJSie_3ncc8)
    
- I vibe coded a replacement for a service that would have cost me a ton of money to use
    - Podclipr ingests a video feed, generates a transcript, identifies segments that might be interesting (using a local model), let’s me vet them, select the ins and outs, drops caption on, and then uses FFMPEG to render out the clips. I write the titles and copy, hit the post buttons, and they go up when the schedule hits.
    - It’s turned a task that I spent 3-4 hours for every episode into about 30 minutes.
- This week’s homework is to setup a thumbdrive with Ventoy and try some live CDs, then report back in the comments thread for the new episode