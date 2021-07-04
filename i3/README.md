# i3 Window Manager
i3 is a tiling window manager, completely written from scratch. The target platforms are GNU/Linux and BSD operating systems, i3 is primarily targeted at advanced users and developers. 

This tiling window manager it's really easy to configure. As you can see their use "config" file. You don't need to knows about some programming languages. Well, let's start with "How to install i3wm?".

# i3wm Installations
The firt we wanna do is to install the window manager and some programs that will allow a better performance.

Debian/Ubuntu:
```bash
sudo apt install i3 rofi picom feh
```
If you have problem to install picom I recommend to see this **[Web Page](https://www.linuxfordevices.com/tutorials/linux/picom)** or the original repository.**[Picom Repo](https://github.com/yshui/picom)**

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
Then you have to install the fonts. It's allow to for our status bar.
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
exec_always feh --bg-fill /home/diego/Pictures/wallpapers/1.jpg
# You have to put the corret path for your wallpaper.
```
And that is! Now you can restart your window manager ```mod+Shift+r``` and you have your new window manager.

