# Episode 5 - 11/24

### Cold Open

On this week’s episode, I’m going to talk about streaming GTA 6 to your Steam Deck (or other PC), the big November update to CachyOS, and I’ve got a special guest in my Dual Boot Diaries co-host Adam Patrick Murray joining the show. 

### Intro

- Fixing the kiddos laptop
- Playing GTA on the Steam Deck and Steam Machine using Chiaki-ng
- Link to Chiaki (PS5 Streaming App) and Greenlight (Xbox Streaming App)

### News

- Big CachyOS update landed - [https://www.cachyos.org/blog/2611-november-release/](https://www.cachyos.org/blog/2611-november-release/)
    - New package manager - I spent some time wtih it, and quite like it. They provide a curated list of packages, with lots of good stuff.
        - AUR, Flatpak support, and it does support appimages now. If you install the appimage from a github link, it will update them too, apparently.
    - EACv2 and scripts to help you set it up. Most users will want to reboot to that kernel when you’re using it, because you can’t use DKMS modules with it (my bluetooth radio and AIO interface both use DKMS modules, as an example)
    - CachyOS Recovery is a self-contained image that will give you the tools you need to rollback a broken cachy install without needing a live CD
        - This is a great addition. It’s one of the big differences between Linux and Windows.
        - You’ll need more space in your boot partition to accommodate it, but it’s only about 70MB
- Niri lead uses Fedora Silverblue (immutable Fedora) for Niri dev (RocketLobster)
    - [https://bxt.rs/blog/using-fedora-silverblue-for-compositor-development/](https://bxt.rs/blog/using-fedora-silverblue-for-compositor-development/)
- Bugmenot bites the dust:
    - Puzzle on the “We’ve closed” page [https://web.archive.org/web/20261116003357/https://bugmenot.com/](https://web.archive.org/web/20261116003357/https://bugmenot.com/)
- Microsoft Bought Wunderlist, Turned it into To-Do, and is now killing To-Do, leaving people’s data stranded
    - Last I looked, you could hook it up to a number of other services.
    - I’m never using another Microsoft service again if I can help it
    - [https://www.windowslatest.com/2026/11/19/microsoft-is-killing-to-do-and-telling-you-to-choose-another-app-after-it-reportedly-paid-up-to-200-million-for-wunderlist-and-killed-it-for-to-do/](https://www.windowslatest.com/2026/11/19/microsoft-is-killing-to-do-and-telling-you-to-choose-another-app-after-it-reportedly-paid-up-to-200-million-for-wunderlist-and-killed-it-for-to-do/)
- From the small wins lead to big wins category: https://www.canva.com/newsroom/news/ai-controls-canva/
    - “We've heard how important it is to make designs and illustrations created by real people easier to find, and our new Content Control has been designed to give you more choice over what you discover. When enabled, it reduces the amount of AI-generated content appearing in search results and recommendations, bringing more human-made work front and centre.”
    - Firefox finally did this earlier this year, and it was good.
    - AI-assisted tools, like their clipping applet won’t. This helps people avoid getting the AI-generated tag on the stuff they’re creating.
        - Reading between the lines, this says to me that people were avoiding flagged as AI templates in the canva galleries, which seems like a good thing
            - One of Canva’s strengths is that there are a ton of good templates and even entire documents in there that people reuse (teachers reusing worksheets, etc)
    - It’s increasingly difficult to avoid AI-generated work, especially code. Finding the line is tough to impossible. Can I say I don’t use AI if I use the NVIDIA broadcast plugin to clip my background? What about if I make a game using hand-written code in an engine that uses AI code?
    - Vistaprints example - they had an AI cleanup process that ran after the customer approved a print that garbled text for at least one customer.

### Feature / Interview

TALK TO ADAM PATRICK MURRAY

### Linux Journey

- Umbriel
- Learned how to format a USB drive in Linux
    - I used the Gnone Disks app
- Fixed the OBS crash I’ve been having by adding
    
    ```jsx
    __NV_DISABLE_EXPLICIT_SYNC = "1" 
    ```
    
    - to my environment variables. Seems like this fixes the same crash in Niri
- Home Server Update - Old laptop, realized another benefit. I pay roughly 1/3 the rate for power from midnight to 3PM that I do from 3PM to 10PM. So I set up a service that sets the charge threshold to 20% during that 3PM to midnight window
    - Will post the services on the github
    - /etc/systemd/system and you need services and timers

### Questions

- Updates on dotfile syncs from Take Control members (SirCadian and bewareofthelaopard)
    - Chez Moi: [https://www.chezmoi.io/](https://www.chezmoi.io/)
    - STOW: [https://www.gnu.org/software/stow/](https://www.gnu.org/software/stow/)
        - I’ll add these to the topic list for a future episode
- Q in the Discord from jkrauska: What do people use for cross platform video calls?   For work I've had to use Zoom, Hangouts, Teams (!), etc.   For my wife and kids I use Facetime.  My old Dad only has a chromebook, so we tend to use Hangouts.  I really want easy/crossplatform/decent quality easy video calls..  WebRTC  was supposed to make this all lovely and easy -- I'm not sure it has -- or maybe since it's non-corporate no one tech took off..   How do I TAKE CONTROL of my video calls with friends and family cross platform?  Bonus points for being able to project to a TV in some fashion for living-room scale video calls (holidays are coming)
- Burtron Audio Question

### Homework

- Last week’s homework was to try out a new linux distro or two. I didn’t get a ton of reaction to this one, but I ended up putting a stripped down version of Debian on an old digital photo frame, which essentially resuscitated it