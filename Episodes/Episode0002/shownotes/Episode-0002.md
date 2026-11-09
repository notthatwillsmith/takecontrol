# Episode 2

Intro - on this week - Linux compatible Fortnite, Bazzite running on jailbroken PS5s, the end of the road for the 486, Chris Person’s Aftermath article about switching to Linux (and me), and a big long list of steps I’ve taken to Take Control of My Tech 

### Housekeeping

[https://aftermath.site/we-must-kill-windows/](https://aftermath.site/we-must-kill-windows/)

Talk about the git repo

https://github.com/notthatwillsmith/takecontrol

https://takeControl.content.town/subscribe - Take Control needs your support! I'm funding this out of pocket and would love to be able to do more stuff, like hire a contributor, fund open source projects I love, and more. Subscribing gets you an ad-free feed, early access to the episode (when possible), access to the Subscriber-only Discord, and more! 

AD -  Fastmail is an email service for people like you and me. I love it’s one-touch integrations with 1Password and Bitlocker, which lets me easily create single-use email addresses when I sign up for new services. I also love its integrated domain support. You connect your domains to its backend and then spinning up a new address is as easy as a few clicks in your webmail interface. If you want to support the show, try it out free for 30 days. Go to [join.fastmail.com/wil](http://join.fastmail.com/will)l to sign up. There’s no obligation and they don’t even ask for your credit card.  You get a great email host that isn’t spying on you and they throw me a few bucks for everyone who signs up. Thanks Fastmail! 

### News

- Epic making Linux-compatible Fortnite anti-cheat. Includes a custom kernel from Cachy. (Not sure how I feel about this).
    - TLDR is that instead of writing a janky kernel module, they seem to be working within the existing Linux ecosystem
    - They have a big list of requirements, but here’s the short version.
        - Basically, you need a signed kernel (w/ modules for the NVIDIA drivers), TPM 2.0 and Secure Boot turned on (and using well-known keys), measured boot running, and IOMMU (Input-output memory management Unit) controls access between DMA-capable hardware and your system RAM. Prevents hardware cards designed for cheating from accessing game RAM. Kexec disabled. Linux Security module BPF
            - Well known keys are from Canonical, Fedora, Universal Blue, Debian, openSUSE, Rockey, Microsoft, Alma Linux
        - Most likely this means you’ll install a special kernel which will have its own boot entry if you want to play Fortnite
            - As someone who played a lot of fortnite for a long time, I’m probably OK
    - [https://onlineservices.epicgames.com/news/introducing-easy-anti-cheat-linux-v2](https://onlineservices.epicgames.com/news/introducing-easy-anti-cheat-linux-v2)
- Bazzite is running on jailbroken PS5s with compatible firmwares, giving PS5 owners access to their steam libraries (firmware 13.60)
    - This firmware was current as of a couple of months ago
    - https://github.com/VivaLaVent/ps5-bazzite-deck
- 486 Support being removed in Linux kernel 7.1 - this is an older story, but…
    - [https://www.xda-developers.com/linux-71-is-here-and-it-kills-i486-support-fixes-steam-deck-audio-and-overhauls-ntfs/](https://www.xda-developers.com/linux-71-is-here-and-it-kills-i486-support-fixes-steam-deck-audio-and-overhauls-ntfs/)
- KDE and Gnome both released new major versions
    - KDE Plasma 6.8 - 10/14 - 30th anniversary of KDE
        - Accessibility options built in, better window styling for non-native apps (like Steam), update to the new Union themeing app,  end support for starting X11 sessions in Plasma, and a bunch more -
            - I love that they made a Union version of the default Breeze theme that looks exactly like the old version.
        - Full notes: [https://kde.org/announcements/plasma/6/6.8.0/](https://kde.org/announcements/plasma/6/6.8.0/)
    - Gnome 51 - 9/16
        - Perf improvements for display under heavy load, removed support for legacy NVIDIA drivers, offline maps and updated public transit info, a big update to the Files app, updated file preview all
        - Full notes: [https://release.gnome.org/51/](https://release.gnome.org/51/)
- What kind of Linux news do you want in this segment? Let me know! [takecontrol@content.town](mailto:takecontrol@content.town)
- 

### Linux Changeover Stuff

- [https://docs.noctalia.dev/noctalia/compositor-settings/niri/](https://docs.noctalia.dev/noctalia/compositor-settings/niri/) (blurred corners, weird blur on the widgets fixed with adjusting my niri config.kdl
- What I’ve done to de-enshittify so far,  a quick rundown
    - Linux, obviously - Cachy, Niri, Noctalia
    - Switch To Fastmail for email
        - Email and calendar there
        - Add a Google account for that email so you can use docs (what happens if you don’t) - free link
    - Search: Google > Kagi
    - Disabling stuff in Windows
    - Phone; turning off all the stuff I don’t use
    - Phone: looking at subs
    - Notification management/pruning
    - Moving accounts off Google oauth
    - Glance app instead of Google News
    - I’m

AD 2 - I absolutely love Fastmail. It was the fastest I’ve ever signed up for a service after starting a trial—I think I switched my free trial to a paid one within about 30 minutes of starting to use it. It’s email that doesn’t spy on you that makes a bunch of the difficult stuff about managing email for your own domains easy. They make it easy to connect as many domains and inboxes as you want to your account. You can create single-use masked email addresses for signups inside 1Password or Bitlocker. 

If you want to support the show, try Fastmail out for free for 30 days. Go to [join.fastmail.com/wil](http://join.fastmail.com/will)l to sign up. There’s no obligation and they don’t even ask for your credit card.  You get a great email host that isn’t spying on you and they throw me a few bucks for everyone who signs up. Thanks Fastmail! 

### Questions

- Curtis - VR on Linux
- James - Getting started, figuring out what you don’t know and don’t need to know vs. what you do need to know
- John from Raleigh - some projects in the past, but thinking about rebuilding a MAME cabinet on Linux
- Jonbobcar - File permissions and song
- Nate - DBD changed my life and REISUB keys
    - To use this, most distros require you to turn it on. I don’t exactly know what the downsides are, it’s generally recommended that you use this rather than long press the power button if your system is in a bad way.
    - I haven’t actually had a machine this broken yet. I’ve typically been able to swap to a text mode console and reboot the machine that way (ctrl+alt+F3-F6 on my machines)
    - I’ll link the Arch wiki page for this in the shownotes
    - [https://wiki.archlinux.org/title/Keyboard_shortcuts#Kernel_(SysRq)](https://wiki.archlinux.org/title/Keyboard_shortcuts#Kernel_(SysRq))

### Homework

- We’re bringing homework back
- This week’s homework is to fix something about your computer that annoys you. Hop in the Discord or the comments on the site, share what you’ve done,
    - Turn off Bing results in your Windows Start Menu
    - Kill Co-pilot in Windows
    - Turn off non-essential notifications on your phone
- I want to see comments, tell me how doing this made you feel
-
