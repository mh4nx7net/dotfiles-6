## Installation
1. Put all fonts in the **fonts** folder to */usr/share/fonts/* and refresh font cache.
   ```bash
   fc-cache -r
   ```
2. Put **slim.conf** into */etc/*.
3. Put the **custom** folder to */usr/share/slim/themes/*.
4. Create symbolic link for slim background to *~/.wallpaper/slim.png*.
   ```bash
   sudo ln -s ~/.wallpaper/slim.png /usr/share/slim/themes/custom/background.png
   ```

## Additional configuration
> Edit the **slim.conf** file.
- Screenshots
  ```cfg
  screenshot_cmd      scrot -e 'mv $f /home/username/Pictures/'
  ```

Slim requires *~/.xinitrc* to execute WM/DE sessions. \
More information is available on the [Arch Wiki](https://wiki.archlinux.org/index.php/SLiM).

<img src="https://i.ibb.co/XDmrFDQ/slim.png" alt="slim" align="center">
<img src="https://i.ibb.co/jR60wvP/slimlock.png" alt="slimlock" align="center">

If you want a slim **bluesky** theme it's also available at [bluesky.tar.xz](./bluesky.tar.xz).
<img src="https://i.ibb.co/42S8QXJ/slim-bluesky.png" alt="slimlock" align="center">
