# i3 Window Manager
i3 is a tiling window manager, completely written from scratch. The target platforms are GNU/Linux and BSD operating systems, i3 is primarily targeted at advanced users and developers. 

This tiling window manager is really easy to configure. As you can see their use "config" file. You don't need to knows about some programming languages. Well, let's start with "How to install i3wm?".

# i3wm Installations
The firt we wanna do is to install the window manager and some programs that will allow a better performance.

Debian/Ubuntu:
```bash
sudo apt install i3 rofi picom feh
```
If you have problem to install picom I recommend to see this **[Web Page](https://www.linuxfordevices.com/tutorials/linux/picom)** or the original repository (**[Picom Repo](https://github.com/yshui/picom)**)

Then we have to login on i3wm and create the default config. It's easy to create the config file. 

# Clone the Repository
So, now we have the default config in ```~/.config/i3/``` and we need to do something.

Make a copy of the default configuration.
```bash
mv ~/.config/i3/config config2
```
Go to ```~/.config/i3/```  and clone my repository.
```bash
cd ~/.config/i3/
git clone https://github.com/nxdiegog/Dotfiles/tree/master/i3
```
Then you have to install the font. This font allow to personalize our status bar.
```bash
unzip Ubuntu.zip
sudo mv *.ttf /usr/share/fonts/
# If you want, you can delete "Ubuntu.zip"
```
So now you have my configuration, but you have to do somethings. The first one, you have to clone one repository. If you need more information ***[Click Here](https://github.com/tobi-wan-kenobi/bumblebee-status)***
```bash
git clone git://github.com/tobi-wan-kenobi/bumblebee-status
```
This is to personalize our status bar and allows us to have a better appearance in our desktop environment.

Now you have to move the ```bumblebee-status directory```.
```bash
mv bumblebee-status ~/.config/ -r
```

The last thing you have to do. In the config file you have to modificate something.
```config
# Wallpaper 
exec_always feh --bg-fill /home/user/Pictures/wallpapers/1.jpg
# You have to put the corret path for your wallpaper.
```
#i3 Gaps
i3-gaps is a fork of the i3 window manager that is kept up to date with upstream i3, and adds the feature of allowing you to have visible and configurable gaps between windows. This feature is just eye candy, and may or may not actually aid the user by providing some visible space between windows (at the expense of some screen real estate) to make clearer the distinction between adjacent windows. What cannot be argued though, is that i3-gaps just looks better. Seriously though, it is just regular i3 but with re-sizable gaps between windows that can be turned on or off.

So, here is how to build from source and install i3-gaps on debian:

First install the dependencies:
```bash
sudo apt install meson dh-autoreconf libxcb-keysyms1-dev libpango1.0-dev libxcb-util0-dev xcb libxcb1-dev libxcb-icccm4-dev libyajl-dev libev-dev libxcb-xkb-dev libxcb-cursor-dev libxkbcommon-dev libxcb-xinerama0-dev libxkbcommon-x11-dev libstartup-notification0-dev libxcb-randr0-dev libxcb-xrm0 libxcb-xrm-dev libxcb-shape0 libxcb-shape0-dev
```
Then cd to the directory where you want to download the i3-gaps source code and the run the following commands in the order shown.

```bash
cd .config/
git clone https://github.com/Airblader/i3.git i3-gaps
cd i3-gaps
mkdir -p build && cd build
meson --prefix /usr/local
ninja
sudo ninja install
```

If you want to change the color of the status bar you can see the ``themes.txt`` file. In this file I put some themes that you can use. I recommend you to see
which themes I use because these themes are related to the settings you find in ``themes.txt``. 

And that is! Now you can restart your window manager ```mod+Shift+r``` and you have your new window manager.

![ww](https://user-images.githubusercontent.com/85723755/124371300-940e1a00-dc3d-11eb-8e4c-dac01c24c984.png)




