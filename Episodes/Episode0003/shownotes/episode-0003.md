# Episode 3 - 11/10

Cold Open: This week, we’re going to Take Control of Windows 11, start working toward a better approach to online photos and video, take a new Niri competitor for a test spin, answer your questions, and see how we did on our homework. It’s time to Take Control of Your Tech

Intro: I fought some real-life tech debt this weekend. 

Lots of good suggestions for the name for the battle against enshittification. I liked a bunch of them (de-shittify, flushing, detoxing, exorcising, etc), but I think the winner came from the one and only Bunnyfiend. Taking control…

Github to follow the actual shownotes that I use, [link in the podcast shownotes](https://github.com/notthatwillsmith/takecontrol). <don’t use while driving> 

Sub plug - 

**Skipping News this week because we’ve got a lot of Taking Control to do here**

<aside>
💡

AD -  Fastmail is an email service for people like you and me. I love it’s one-touch integrations with 1Password and Bitlocker, which lets me easily create single-use email addresses when I sign up for new services. I also love its integrated domain support. You connect your domains to its backend and then spinning up a new address is as easy as a few clicks in your webmail interface. If you want to support the show, try it out free for 30 days. Go to [join.fastmail.com/wil](http://join.fastmail.com/will)l to sign up. There’s no obligation and they don’t even ask for your credit card.  You get a great email host that isn’t spying on you and they throw me a few bucks for everyone who signs up. Thanks Fastmail! 

</aside>

### Dis-Enshittify

- Windows Tips - [https://takecontrol.content.town/blog/unfucking-windows-for-fun-and-profit/](https://takecontrol.content.town/blog/unfucking-windows-for-fun-and-profit/)
    - Talk about defaults mattering, and the ability to change this stuff only impacts a tiny percentage of users. 90+% of people will never do this stuff
        - Also, please subscribe, because I just cut my total addressable audience from 8B people to 80M people
    - Everything was tested on Windows 25H2
    - Also plug the Github and the article - [https://github.com/notthatwillsmith/takecontrol](https://github.com/notthatwillsmith/takecontrol)
    - Fix the Start Menu
        - Turn off the personalization (Settings > Personalization > Start
            - Show recommendation for tips and app recommendations, shortcuts, new apps, and more to off
            - Show account-related notifications to off - upsells and reminders to spend money
        - Limit Start Menu Search to Applications
            - This is my number 1 tip - Open Regedit and go to Computer\HKEY_CURRENT_USER\SOFTWARE\Policies\Microsoft\Windows\Explorer (You may need to create the Explorer key. It wasn’t there on my test PC. You do that by making a new Key in the Windows folder. Add a 32-bit DWORD value tcalled DisableSearchBoxSuggestions and set it’s value to 1. Log out and log back in and Bing will be out of your Start menu
                - If more than just you use this computer, you can do HKEY_LOCAL_MACHINE and the same path to make it a system level change
    - Get rid of the unnecessary software you don’t use
        - Apps - It’s worth diving into the Start Menu and uninstalling all the stuff you’re never going to use (See you in hell Game Assist)
            - If you uninstall One Drive, it stops the Windows Backup prompts, at least on the version of Windows I have.
            - On some versions of Windows, uninstalling Copilot is harder than others. On the current 25H2 version I’m running, uninstalling gets rid of it in most places
            - I get rid of everything but Calculator, Clock, Notepad, Paint, Remote Desktop Connection, Snipping Tool, Sound Recorder, Terminal, and Xbox/Xbox Live
                - There’s other stuff hidden in the System components page, but some of it can’t be removed
                - you should choose the stuff you want to keep. No shame for keeping solitaire or minesweeper
                - There are also often stub apps, like Candy Crush, that are essentially just shortcuts to store links that will auto-download the apps
        - widgets  (MSN news, weather, dynamic lock screen, etc)
            - Disabling the taskbar widgets is in Taskbar settings in the Settings app.  You can get to it quickly by right-clicking the taskbar and selection settings
                - The Weather widget also gives you spam from MS’s news site sometimes
            - The homescreen widgets are sometimes tied to the Windows Spotlight setting for the lock/login screen, so you lose the dynamic wallpapers, news and weather widgets, and other unnecessary crap if you turn them off
                - On my unique version of Windows 11 25H2 I have distinct settings for Widgets, Windows Spotlight, and “Get fun facts, tips, tricks, and more on your lock screen”
                    - Unchecking “Suggest widgets” crashed the Settings app, so Microsoft remains awesome at making Windows
    - Turn off Co-pilot everywhere
        - This is easier than it used to be
            - On current versions, uninstall works, but it will still be in some of the other apps (like Paint and Notepad)
            - It will likely get reinstalled on some future major updates
            - The price of freedom is eternal vigiliance
        - What about the Copilot key
            - Some laptops and keyboards let you rebind it to be a second Windows key/Super key
            - If they don’t, you’re kind of hosed. MS used a weird keycode for it, so it’s not something you can intercept in a fully functional way, even in Linux.
            - Windows Recall is off by default, but you can fully remove it in the Windows Features page
    - Andrew Cunningham’s great Ars Technica guide calls out the Settings > Privacy and Security section [https://arstechnica.com/gadgets/2025/11/what-i-do-to-clean-up-a-clean-install-of-windows-11-23h2-and-edge/](https://arstechnica.com/gadgets/2025/11/what-i-do-to-clean-up-a-clean-install-of-windows-11-23h2-and-edge/)
        - Disable Personalized offers in Recommendations & offers, Show notifications in Settings, Recommendations and offers in settings, and Advertising ID
        - Diagnostics and Feedback - feedback frequency to Never
        - Search - Show search highlights gets rid of web search results in the Search menu (start menu is separate in the versions of Windows I have access to)
            - While you’re in Search, the Enhanced search is pretty good, but you have to tell it where to look, if you save your stuff outside the normal c:/users/username/ tree
        - Another one I love from here is Settings > System > Notifications - expand the additional settings box and uncheck all three boxes there (Show the Windows Welcome experience after updates , suggest ways to get the most of out of Windows, get tips and suggestions when using Windows)
            - If it isn’t in there, try System > Notifications > scroll to the bottom and open Additional Settings
    - Replace your text editor
        - Notepad++ is great
    - Keep your home folders out of One Drive
        - This is easier to do when you install than it is after the fact. When you’re installing, use the OOBE trick (on Windows 11 Home computers) or the “I’m setting up my PC for work or school” trick on Pro machines.
            - The OOBE trick is to hit Shift+F10 at the start of the graphical Windows 11 installer and at that command line, type OOBE\BYPASSNRO. After the PC reboots, you’ll be able to choose “I don’t have internet” at the network setup screen and it will let you create a local account.
        - Once you’ve finished the setup, you can safely connect your Microsoft account and the OS won’t move your crap into the weird OneDrive folders
        - You can move these manually after this has happened, but it has some gnarly downstream impacts, and I usually just recommend that you live with the weird one-drive structure rather than try to force a change
- Things not to do
    - Don’t use the Windows 10 LTS versions
        - These are really built for single-purpose computers, things that power public displays, info kiosks, etc. Things will break over time, they don’t get the same kind of security updates, and they’re just not appropriate for computers that people use on the daily.
    - Don’t run one of those “Windows Cleanup Scripts”
        - Everyone has a different balance between how much control you want to take over your computer and how much of a hassle you’re willing to go through to get that control, and the folks who make these scripts are essentially in an arms race with each other to strip more stuff out.
        - It’s better to think about the things that actually annoy *you* and focus on those than take some random person’s word for what you need to do
        - Also, if you do the work yourself, you know how to fix it and/or replicate it when something breaks and/or you need to move to a new PC or a new Windows install, even if the script you used is no longer available/updated.
    - I don’t like running Windows without a MS account. If you use Windows without using any other MS services, I guess it’s OK, but I use their office suite, Xbox apps, Minecraft, and apps from their store, so it’s too much of an inconvenience for me.
        - Plus you can’t use Windows Hello without a MS account, which has some downstream consequences for your login, biometric and 2 factor login support, and stuff like unlocking your password manager
        - This also applies to those “Fixed” Windows installers. They’re an easy vector for malware and a huge target and have all the same issues as the cleanup scripts
    - Don’t install Windows 11 if your computer doesn’t support Secure Boot or TPM2.0
        - At some point you’ll get stuck on an update that’s no longer supported. Its time to either turn those features on in the UEFI or upgrade your hardware if it doesn’t support them

SEND IN THE THINGS YOU DO TO TAKE CONTROL OF WINDOWS. I’ll run the best ones in an upcoming episode. Plug the email address!

### Taking Control of My Tech Updates

- Umbriel first steps - link to this
    - Replacement compositor (like Niri), built by Noctalia and designed to work well with Noctalia
    - It’s early, but it also seems built for people like me
        - Game tech out of the box - HDR, VRR, and primary gaming monitor support
        - per-workspace modes (scrolling (like Niri), dwindling (like Hyprland), master (unfortunate name, but one main windows + secondary in a stack), stacking (like Windows or MacOS) layouts) -
            - Hey shownotes readers: sorry about this parenthesis nightmare
        - I need to setup workspaces and autolaunches and all that stuff, but it seems promising.
- I’ve been dealing with out of storage issues on my family’s shared Google account for ages, and a big part of the problem is our photos
    - I installed Immich and am in the process of importing everything from Google into the Immich library
        - I want to dedupe, which is explicitly not in Google’s best interests, but also I want to have a local backup of my cloud photos
            - I’m not sure I want to get rid of cloud backup for the photos, but having a second source of truth that’s not tied to a Google account feels wise to me

### Letters

Plug the email address here.

> Been a fan of yours since finding the Brad and Will techpod. I have always been into tech but listening to you and the folks around you made me realize that I don't use tech anymore; it's using me. I sort of knew but having more knowledgeable people backup your own thoughts brings these issues into the open. Thank you.

I have seen a bunch of guides and such on using pfsense/opnsense and your old router for WiFi and lan hub.

Question:

If you're still using your problematic router on your Lan, behind pfsense, with access to the  internet wouldn't you still have that thing leaking info out (like Mac addresses, connected devices, websites accessed...)? Defeating the point of making your own? Or is it that pfsense will block that stuff from leaving your Lan?

I have searched for answers but have found none. Might just be I'm asking the wrong questions

Thanks again, and have a slop free day,

Matt - Cornwall, UK
> 
- Jerry (audio) - getting rid of Roku

> Self-hosted multiplayer games are seemingly nearly extinct.  If I want a multiplayer game that I can host myself to play with friends, without being bombarded with battle passes and other addictive hooks, not to mention retain actual ownership, my options for LAN and direct IP connections are basically Larian's games, some survival crafting games, and <end of list>.  If I want to play a shooter like this, my best options are 20+ year old games on GOG like Red Faction and Star Wars Battlefront II (2005).  What's the best way to send a signal to game studios that this is what it takes to earn a sale from weirdos like us, and to get this feature to return?

Thanks,

Andrew
> 

Plug the email address again! 

<aside>
💡

AD 2 - I absolutely love Fastmail. It was the fastest I’ve ever signed up for a service after starting a trial—I think I switched my free trial to a paid one within about 30 minutes of starting to use it. It’s email that doesn’t spy on you that makes a bunch of the difficult stuff about managing email for your own domains easy. They make it easy to connect as many domains and inboxes as you want to your account. You can create single-use masked email addresses for signups inside 1Password or Bitlocker. 

If you want to support the show, try Fastmail out for free for 30 days. Go to [join.fastmail.com/wil](http://join.fastmail.com/will)l to sign up. There’s no obligation and they don’t even ask for your credit card.  You get a great email host that isn’t spying on you and they throw me a few bucks for everyone who signs up. Thanks Fastmail! 

</aside>

### Homework

- My homework - I finished a couple of things and started another
    - I finally uninstalled Adobe’s apps, which I haven’t used since last fall, but lingered on my Windows partition.
    - [Content.town](http://Content.town) landing page
        - I’ve needed a landing page for the top-level [content.town](http://content.town) domain, so I sat down and jammed out a flat page that looks relatively modern using a local AI model, then hosted it on Github Pages.
        - And yes, Github is a MS product, so it’s not ideal, but the price is right and sometimes the easy answer is the right one.
        - I generated the page using Qwen3.8 running on my local machine. It took me about 20 minutes and the landing page is much more functional than it would be if I did it myself.  (it does stuff like respect the users light/dark mode, has a form for contacting me, etc)
    - What other folks did: I saw a lot of folks talking about organizing their photos, some folks switched their primary email from Google to Fastmail, and I saw more than a few setting up GlanceApp to use as their browser homepage. Some folks moved personal projects off of hosting services that they weren’t using, and removing web search from the Windows Start Menu
- This week’s homework is to do some (or all) of the Windows fixes above. Hop in the Discord, hit me on Bluesky, or drop a comment on the site and share what you’ve done,
- I want to see comments, tell me how doing this made you feel

Sub plug -
