# myMacBookSetup

Recently I had an issue with my MacBook out of nowhere. Intune Management said that my device was not registered any more. After several tries to get it into the management again I decided to reinstall it from scratch. As I did this I decided to docment all necessary settings to get it up an running again. Here is my result

## Install Apps

I will do most of them using homebrew via the commandline

Microsoft PowerPoint
Company Portal
Microsoft Teams
GarageBand
Microsoft Word
OneDrive
Karabiner-EventViewer
Publer
Microsoft Defender
Safari
Microsoft Edge
Microsoft Excel
Microsoft OneNote
Visual Studio Code
Microsoft Outlook
Shottr

### Homebrew to automate it

I decided to use homebrew for most of the packages.

1. Install homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install packages from a list of apps

Update this list regularly as you install new apps.

```bash
brew install $(cat packages.txt)
```

Here is my baseline [packages.txt](./packages.txt)

### Browser Extensions

As I use Edge as my main browser I don'T need to care about the extensions. They are synced together with bookmarks.

## Configuration Files

Most of your preferences on the Mac and it's applications are stored in *plist* files. I recommend using backups of these to keep your settings even after reinstalling.  
You can find your *plist* files under *~/Library/Preferences/*  
I use timemachine backups with an external SSD to keep the backups up to date.

## Karabiner Elements

I use Karabiner Elements mainly for three reasons

1. Mouse and Trackpad
By default Mouse and Trackpad use the same settings. So if I use "Natural Scrolling" on my trackpad the mouse wheel is in the wrong direction. You can easily revert the mousewheel with Karabiner Elements.
![Picture of the settings for my Mousewheel](./media/karabiner-elements-mousewheel.png)
2. Keyboard Layout
I recently had issues that the keyboard settings changed from ISO to ANSI which lead to flipping some keys like ^° and <>. With these settings I am sure that the external keyboard is not changing my local keyboard.
![Picture of my Keyboard Layout settings in Karabiner Elements](./media/karabiner-elements-keyboard.png)
3. Home and End Key
I like using the *HOME* and *END* keys to jump to the beginning or end of a line. With these settings this wirks with the default keys on a regular keyboard.
You can find the two files here [karabiner-elements](./karabiner-elements/)

## Conclusion

After resetting the device I was back up and running tow hours later.