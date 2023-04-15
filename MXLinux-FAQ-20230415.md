MX logo
# FAQs


## Table of Contents
1. [General](#general)
2. [Obtaining and Installing an ISO](#obtaining-and-installing-an-iso)	
3. [Configuration and Customization](#configuration-and-customization)	
4. [Security](#security)	
5. [System](#system)	


## General

### Is MX Linux a rolling distro?
No. When the Debian base changes (about every 2 years), then reinstalling is needed for continued reliable use. It is not difficult to reinstall when a new version becomes available. 

- To keep your existing packages, there is a handy app called “User Installed Packages” that makes it easy to restore packages (if the packages are still available) you had installed and retained after your original installation.

- Settings are important as well. If possible, the easiest method to retain your settings is to select “Reuse the Home directory” during the new installation. Otherwise, you should make a separate backup of the Home directory and manually transfer any settings you want to keep (e.g. browser or email) to the new installation.

Details in Users Manual, Section 1.6.

### What’s the MX release cycle?
As of MX-19 and forward, major version changes happen with Debian stable major updates, with a number of “point releases” in between that will come through the standard update channels for existing users.

### What’s the best way to upgrade from one version of MX to another?
Instructions for migration of different MX versions can be found on the “Migration” page of the MX Community website. https://mxlinux.org/migration/

### How long will a version of MX be supported?
A chart is located here: Previous Releases https://mxlinux.org/previous-releases/
Lots of other distros are dropping their 32-bit versions. What about MX?
MX has no plans to discontinue 32-bit releases.

### Does MX Linux release other official versions?
Three options exist: Xfce (flagship), KDE and Fluxbox. There are many Community respins available, however: see the list on the Forum https://forum.mxlinux.org/viewtopic.php?f=100&t=48617&hilit=respins

### Can I use Flatpaks, Snaps and Appimages?
Stand-alone packages are different in that they are essentially independent from the particular OS and do not need to be installed. For details, consult these pages:

- Appimages	https://mxlinux.org/wiki/applications/appimages/

- Flatpaks	https://mxlinux.org/wiki/applications/flatpaks/

- Snaps	https://mxlinux.org/wiki/applications/snap-packages-and-mx-linux/

### Does MX have any social media presence?
MX has very active social media communities: https://mxlinux.org/wiki/other/mx-linux-social-media/

## Obtaining and Installing an ISO

### Why does my installation stop at 94%?
The installation is waiting for you to fill in the information being requested on the screen. Press “Next” to go through all information screens.

### Can I buy a USB with MX Linux already installed?
Unfortunately, that option is no longer possible since the company providing that service has gone out of business.

### Can I install MX Linux on a computer that has Windows?
If the machine already has Windows 8 or later installed, then special steps must be taken to deal with the presence of (U)EFI [https://en.wikipedia.org/wiki/UEFI] and its best known feature, “Secure Boot.” Most users are urged to turn off Secure Boot by entering the BIOS as the machine starts to boot. The exact procedure to disable Secure Boot varies by manufacturer. If you have problems, check the links to videos and documents in the Users Manual, Section 2.4.1 or seek advice on the Forum.

### There is no install icon on the desktop, so what do I do?
That happens sometimes, especially with personal snapshots. Press F4 to get a terminal, and enter
  
```
minstall-pkexec
```

## Configuration and Customization

### I hate the panel on the side! How can I move it somewhere where I want it?
The MX Tweak tool makes moving the panel to your preferred position very easy.

### How can I install the codecs needed for multimedia?
Most codecs are already installed. Use MX Codecs Installer to bring in a few legacy formats as well as DVD playback support.

### I don’t like Xfce. How can I install a different desktop?
A number of different desktops are available in the MX Package Installer under the category “Window Managers” and can be installed easily.

### Can I use apps from another desktop on Xfce?
Applications from Window Managers other than Xfce that are in the default repos can be installed. Very often, they will bring in other applications and libraries that are dependencies of the application. In some cases full functionality of the installed application may not be achieved and will require some research on how to enable that functionality. The appearance of the installed application may not be consistent with the Xfce default theme, especially since the upgrade to Xfce 4.14.

### The window borders are too thin, and I can’t easily resize windows. Is there a way to do that?
Use Alt-F8 to grab the lower-right window corner and drag to the size you want. Alternatively, select a theme (Settings > Appearance) with larger borders.

### How can I add a button to the Panel for one-click logout/shutdown/restart?
Right-click the Action Buttons icon at the top of the panel > Properties and uncheck everything except what you want to see. You can leave confirmation unchecked for even faster functionality.

## Security

### Is MX secure? How can I check my system?
You can check the status of the kernel in use by running spectre-meltdown-checker in a root terminal. You will need to install the package from the default Debian Repositories with Synaptic or the MX Package Installer. Patched kernels are available with status descriptions in the MX Package Installer > Manage Popular packages under the Kernels category.

### Can I use Ubuntu Personal Package Archive aka PPAs?
Ubuntu is not Debian, so installing PPAs will likely cause problems. See this article for details.	https://mxlinux.org/wiki/system/add-ppa-repository/

Solution: Go to the request forum for your MX version, under Community Repository (CR), and ask our Packaging Devs if the PPA can be be ported or updated for our own repository.

## System

### What’s the deal with MX and systemd? Why are there still systemd packages installed? 
Systemd [https://mxlinux.org/wiki/system/systemd/] is included in order to allow some important applications to run, but it is not enabled by default. For more information see the Users Manual Section 1.7 and the Wiki article. https://mxlinux.org/wiki/system/systemd-overview

### How can I fix random login problems using Network Manager?
This is usually due to a known bug, see this Wiki article. https://mxlinux.org/wiki/hardware/network-manager/

### Is there a way that I can boot into systemd by default?
Yes. Boot into systemd by clicking on the line “Advanced options” on the opening screen (known as GRUB), then launch MX Boot options and check the box to “Enable saving last boot choice.”

### Which package manager should I use?
There are three graphical package managers:

- MX Package Installer (MXPI) for one-click installation/removal of popular apps, as well
as apps in the Debian Stable, MX Test Repo, Debian Backports and the Flatpaks repo.

- Synaptic Package Manager, a tool for a whole range of actions with Debian packages.

- KDE plasma uses Discover in lieu of Synaptic.

For details about these as well as command-line utilities, consult the Users Manual, Section 5.

### How will I know when updates are available?
The icon in the Notification Area will change color. Click on it to see the new packages.

v. 20230321	- includes revisions by FullScale4Me 
