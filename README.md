# gentoo-change-gdm-background

This script automates the process of setting an image or color in GNOME Display Manager 44 background on Arch/Gentoo Linux

## Warning

*I've let most of the README intact, however I could not test it on Arch. I guess it should behave the same...*
*Feel free to open an issue on any problem*

This script wont work with older versions of GDM because they have a different
way of dealing with gdm settings.

It also won't work if your system is set to a custom gdm3 theme. You will have to reset to the
default configuration of gdm3 before using the script.

This tool was made specifically to work with Arch/Gentoo Linux as it now bundles all configuration files
inside a .gresource file

If you are going to set an image file that has spaces in its file name or folders, remember to
scape them with backslashes.

## Installation (Arch)

First, you will need to install with `pacman -S glib2`
Then, you can download the script with the command below:
```
wget -O arch-change-gdm-background github.com/Loatchi/gentoo-change-gdm-background/raw/master/gentoo-change-gdm-background
```
And set it as an executable with `chmod +x arch-change-gdm-background`

## Installation (Gentoo)

Simply use my overlay:
```
eselect repository enable loatchi
emaint sync -r loatchi
emerge change-gdm-background
```

## Usage

*It will be called `change-gdm-background` but it should work the same either on Gentoo or Arch*

Run the script with root privileges such as `change-gdm-background /path/to/image`.

If you see a message `login image sucessfully changed`, then, when you restart gdm or reboot your
computer, your gdm background should be covered with the image you selected.

You can restore your original gdm theme any time with `change-gdm-background
--restore`.

### Change Color

Now you can change that dull grey color to any color you like. Just type `change-gdm-background \#yourhexcode` and voilá, you changed it. Your color hex format should
be of six characters like \\#407294 or three characters like \\#6ac.

## Credits

Feel free to see the project [gdm-settings](https://github.com/gdm-settings/gdm-settings). I've translated their `44-support` branch patch for this script
to work.

## Donation

You can donate to one of the contributor `thiggy01`: 
    https://ko-fi.com/thiggy01.
    


