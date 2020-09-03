## Installation
1. Put all fonts in the **fonts** folder to */usr/share/fonts/* and refresh font cache \
   `fc-cache -r`
2. Put **slim.conf** into */etc/*
3. Put the **custom** folder to */usr/share/slim/themes/*
4. Create symbolic link for slim background to *~/.wallpaper/slim.png* \
   `sudo ln -s ~/.wallpaper/slim.png /usr/share/slim/themes/custom/background.png`

## Additional configuration
> Edit the **slim.conf** file
- Screenshots \
  `screenshot_cmd      scrot -e 'mv $f /home/username/Pictures/'`
  
Slim requires *~/.xinitrc* to execute WM/DE sessions \
More information is available on the [Arch Wiki](https://wiki.archlinux.org/index.php/SLiM).

<img src="https://i.ibb.co/XDmrFDQ/slim.png" alt="slim" align="center">
<img src="https://i.ibb.co/jR60wvP/slimlock.png" alt="slimlock" align="center">


