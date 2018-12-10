# Installing and configuring a Xubuntu 16.04 virtual machine for Java labs
**NB:** If you use Firefox, always open web pages in Private Windows.

## Installation
1. Create a new Ubuntu VM in VirtualBox
    * RAM: 4096 MB
    * HDD: 20 GB
1. Install Xubuntu 16.04
    * User: ...
    * Password: ...
    * Host: ...

## Installing/uninstalling packages
1. `sudo vi /etc/apt/apt.conf`
    * `APT::Install-Recommends "false";`
    * `APT::Install-Suggests "false";`
1. `sudo apt-get update`
1. `sudo apt-get autoremove --purge unattended-upgrades pidgin* mugshot blue* xfce4-dict thunderbird* gnome-mines gnome-sudoku *burn* xfce4-notes* orage onboard* libreoffice-math simple-scan transmission-* parole gigolo xfce4-mailwatch-plugin xfce4-cpugraph-plugin xfce4-netload-plugin xfce4-weather-plugin gnome-software* xfce4-taskmanager system-config-printer-* firefox-locale-en libopencv-core2.4v5 liblcms2-utils friendly-recovery libasprintf-dev libgettextpo-dev libgettextpo0 liblouis-data python3-requests secureboot-db`
1. `sudo apt-get upgrade`
1. `sudo apt-get install vim`
1. Install VirtualBox add-ons

## File system
1. `rmdir Music Pictures Public Videos`
    * Let's keep `Templates/` as it is shown in the "Go" menu of File Manager

## Configuring updates
1. Software Updater → Settings
    * Automatically check for updates: Never
    * When there are other updates: Display every two weeks
    * Notify me of a new Ubuntu version: Never
1. Main menu → Session and Startup → Application Autostart
    * Disable "Update Notifier"

## For the Java classes
1. `sudo apt-get install openjdk-8-jdk openjdk-8-jre openjdk-8-source`
1. https://www.eclipse.org/downloads/
1. Eclipse IDE for Java Developers
    * Disable all Eclipse plugins

## GUI, Desktop, and Apps
1. Main menu → All Settings → Language Support → Regional Formats → Display numbers, ...
    * Change to "English (United States)"
    * Apply System-Wide
1. Main menu → Right-click → Remove from favourites:
    * Mail reader
    * Help
1. Icons to the Desktop (+ click and "Mark as executable)
    * Firefox
    * Terminal Emulator
    * Eclipse
    * MousePad
1. Quick launchers
    * Firefox
    * Terminal
    * Directory menu
    * MousePad
    * Show Desktop
1. System tray
    * Keyboard layout indicator
1. Customize Firefox

## Restart
1. Restart

## Clean-up
1. Remove VirtualBox shared folders
    * Unmount
    * Remove directory
    * Remove in a VirtualBox menu
1. Clean the history:
    * Remove recent Eclipse workspaces
        * General > Startup and Shutdown > Workspaces
        * `$ECLIPSE/configuration/.setting` (`"RECENT_WORKSPACES="`)
    * Clean recent files in Eclipse workspaces
    * Clean Vim history
        * rm .viminfo
        * See: https://unix.stackexchange.com/questions/204689/how-to-clear-search-and-command-history-in-vim
    * Clean MousePad history
    * Terminal: `/dev/null > ~/.bash_history && history -c && exit`
    * Clean Firefox history (unless you always worked in Private Windows)
    * Main Menu → Recently Used → Clean Recently Used

## Shutdown
1. Shutdown
