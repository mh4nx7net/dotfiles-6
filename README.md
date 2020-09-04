<p align="center"><a name="top" href="#octocat-hi-there-thanks-for-visiting"><img height="60%" width="100%" src="https://i.ibb.co/k4PbLjv/dotfiles.png"></a></p>

<p align="center">
<a href="#setup"><img width="120px" style="padding: 0 10px;" src="https://i.ibb.co/b5DYRxb/setup.png"></a>
<a href="https://github.com/owl4ce/dotfiles/wiki/Keybinds"><img width="120px" style="padding: 0 10px;" src="https://i.ibb.co/VVc5S9d/keybinds.png"></a>
<a href="https://github.com/owl4ce/dotfiles/wiki/Gallery"><img width="120px" style="padding: 0 10px;" src="https://i.ibb.co/C1sdMw9/gallery.png"></a>
<a href="#notes"><img width="120px" style="padding: 0 10px;" src="https://i.ibb.co/g75Z25g/notes.png"></a>
</p>

##  
### :octocat: Hi there! Thanks for visiting!

<a href="https://www.youtube.com/watch?v=GRLUOrvEc2s"><img src="https://i.ibb.co/bP2pKyR/thumbnail-400px.png" alt="thumbnail" align="right" width="400px"></a>

This is my personal configuration for my favorite openbox window manager and some applications too.

I hope you understand everything here. :wink:

Here are some details about my setup:
- **WM**                           : [Openbox](http://openbox.org/wiki/Main_Page) :art: 4 changable themes/mode!
- **DM**                           : [SLiM](https://wiki.archlinux.org/index.php/SLiM) :gift: login themes Mac looks like!
- **Shell**                        : [zsh](https://wiki.archlinux.org/index.php/zsh) :wrench: with [oh my zsh](https://github.com/ohmyzsh/ohmyzsh) framework!
- **Terminal**                     : [URxvt](https://wiki.archlinux.org/index.php/Rxvt-unicode), [Termite](https://wiki.archlinux.org/index.php/Termite)
- **Openbox Menu**                 : [obmenu-generator](https://github.com/trizen/obmenu-generator)
- **Panel**                        : [tint2](https://wiki.archlinux.org/index.php/Tint2) :shaved_ice: material icon font!
- **Compositor**                   : [Picom](https://github.com/yshui/picom)
- **Notify Daemon**                : [dunst](https://wiki.archlinux.org/index.php/Dunst) :bookmark: minimalist!
- **Application Launcher**         : [rofi](https://github.com/davatorium/rofi) :rocket: apps & sidebar menu!
- **File Manager**                 : [Thunar](https://wiki.archlinux.org/index.php/Thunar) :milky_way: customized sidebar & icon!
- **Text Editor**                  : [Geany](https://www.geany.org/), nano, vim

## Changelogs
- **New mode**: Minimal (both theme)
- **New wallpapers** (can be [added](./.wallpaper/) by yourself)
- **Major changes**: Reconfigure most of the files

Look in the [gallery](https://github.com/owl4ce/dotfiles/wiki/Gallery) and [video preview](https://www.youtube.com/watch?v=GRLUOrvEc2s) for more details.

## Setup
This is how to install this dotfiles for openbox automated setup.

### Introduction of Linux Rice
Please read [this](https://jie-fang.github.io/blog/basics-of-ricing).

### Installation
#### Dependencies
> **Required** (best result)
- **Debian & Ubuntu** \
  `sudo apt install openbox obconf nitrogen dunst tint2 gsimplecal rofi lxappearance qt5ct qt5-style-plugins lxpolkit xautolock rxvt-unicode xclip scrot thunar thunar-archive-plugin thunar-media-tags-plugin thunar-volman ffmpegthumbnailer tumbler ranger caca-utils highlight atool w3m w3m-img poppler-utils mediainfo geany nano vim viewnior mpd mpc ncmpcpp mpv pavucontrol cava parcellite neofetch htop zsh`
  
  zsh, oh-my-zsh, plugins \
  `chsh -s /usr/bin/zsh` \
  `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"` \
  `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting` \
  `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions` \
  `cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc`
  
  picom \
  `sudo apt install libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libxcb-glx0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev  libpcre2-dev  libevdev-dev uthash-dev libev-dev libx11-xcb-dev` \
  `git submodule update --init --recursive` \
  `meson --buildtype=release . build` \
  `ninja -C build` \
  `ninja -C build install`

  obmenu-generator \
  `sudo su`
  `echo 'deb http://download.opensuse.org/repositories/home:/Head_on_a_Stick:/obmenu-generator/Debian_10/ /' > /etc/apt/sources.list.d/home:Head_on_a_Stick:obmenu-generator.list` \
  `wget -nv https://download.opensuse.org/repositories/home:Head_on_a_Stick:obmenu-generator/Debian_10/Release.key -O Release.key` \
  `apt-key add - < Release.key` \
  `apt update` \
  `apt install obmenu-generator`
  
- **Arch Linux** \
  `yay -S openbox obconf nitrogen dunst tint2 gsimplecal rofi lxappearance qt5ct qt5-styleplugins lxsession xautolock rxvt-unicode-patched xclip scrot thunar thunar-archive-plugin thunar-media-tags-plugin thunar-volman ffmpegthumbnailer tumbler ranger w3m geany nano vim viewnior mpd mpc ncmpcpp mpv pavucontrol cava parcellite neofetch htop picom obmenu-generator zsh networkmanager-dmenu`
  
  zsh, oh-my-zsh, plugins \
  `chsh -s /usr/bin/zsh` \
  `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"` \
  `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting` \
  `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions` \
  `cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc`
  
  
> **Optional**: xfce4-power-manager, audacious, spotify, gimp, *browser*, termite, slim. To install this slim theme read [this](./Others/slim).

#### This dotfiles
- **Most of the files** \
  You can clone with `git clone https://github.com/owl4ce/dotfiles.git` or download it as a zip. After that place it in the home directory or **~**.

- **Icons** \
  `cd ~/.icons/` \
  `tar -Jxvf Capitaine-Cursors.tar.xz && tar -Jxvf Papirus-Custom.tar.xz && tar -Jxvf Papirus-Dark-Custom.tar.xz` \
  `sudo cp -r {Capitaine-Cursors,Papirus-Custom,Papirus-Custom-Dark} /usr/share/icons/` \
  `rm -rf ~/.icons/*.tar.xz`

For refresh the font cache do `fc-cache -r`. \
The [Others](./Others/) folder contains spicetify and slim themes.

#### Some user configuration
- **Default lockscreen**: *~/.config/openbox/lockscreen*
- **Tray**: *~/.config/openbox/tray*

### Detailed environment
Please refer to the [wiki/Detailed-Environment](https://github.com/owl4ce/dotfiles/wiki/Detailed-Environment).

## Notes
### <p align="center">Color Scheme</p>
<p align="center"><a name="top" href="#color-scheme"><img src="https://i.ibb.co/9TDTqsy/color-scheme.png" alt="owl4ce.color-scheme" height="60%" width="100%"></a></p>

### <p align="center">:love_letter:</p>
<p align="center">Please don't underestimate, I've configured them all since April 2020 and have been studying them since October 2019. Awesome open-source. If you support it, star it or make a pull request. Or if there is a problem you can make an issue here.</p><p align="center">Thank you!</p>

## Credits / Thanks
- [Elenapan](https://github.com/elenapan)
- [Adhi Pambudi](https://github.com/addy-dclxvi)
- [Fikri Omar](https://github.com/fikriomar16)
- [Rizqi Nur Assyaufi](https://github.com/bandithijo)
- [Muktazam Hasbi Ashidiqi](https://github.com/reorr)
- [Aditya Shakya](https://github.com/adi1090x)
- Our local linux community [Linuxer Desktop Art](https://web.facebook.com/groups/linuxart) and [r/unixporn](https://www.reddit.com/r/unixporn/).
- Some people in the forum who provide solutions.
- All artists who make pictures, illustrations, and wallpapers. By the way [this](https://drive.google.com/drive/folders/1fFseELgArlOGAAeUY32EO98dAU0ITjJ2?usp=sharing) is my wallpaper collection.
