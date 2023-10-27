# Moblododo - A KDE Plasma 5 Theme

This is my personal KDE Plasma 5 theme which is a constant work in progress. All the important bits like splash screens and window decorations are themed. Don't expect anything in here to be perfectly tidy, complete or best practice! ...KDE theming is a messy disjointed biz 🥲...

 - To install on a restricted OS or just to restrict to user, replace `/usr/share/` with `~/.local/share/` in the command paths. It should work for most/all of it.
 - Dirs are named after their destined system locations, so boot.grub = `/boot/grub/`.
 - You don't have to symlink the assets as I've suggested. Instead, you can just copy files to their destinations. If you do this, remember to set ownership on the copied files appropriately.
 - I've only installed and tested on Debian however, it should be good to go on any Debian-based distro with KDE plasma 5.

## Future Plans
 - Install script.
 - Share on the KDE store when it's mature.

## Theme Assets Included

|Asset|Description|
|--|--|
|Aurorae|Window Decorations|
|QtCurve|UI 'widget' styles to change buttons, tabs, toolbars, loading bars etc|
|Wallpapers|Wallpaper images|
|Color-schemes|Plasma theme colour schemes for all UI elements|
|Konsole|Colour schemes for the Konsole terminal|
|GRUB|GRUB menu background|
|Plymouth|Boot splash shown directly after GRUB|
|SDDM|Login/lock screen theme|
|Look and Feel|Plasma Look and Feel sets splash screen after login, plus some buttons etc|
|Desktop Theme|Plasma Desktop Theme sets the appearance of the app launcher, panels and widgets|

## Installation

⚠️ Please don't copy and paste blindly. Inspect and adapt commands for your environment.

#### Download the Repo
Download the repo to your home dir, then install any or all of the components below as you prefer.
```
cd ~/
git clone https://github.com/bigupjeff/moblododo
```

#### Aurorae (.usr.share/aurorae.themes/)
```
sudo ln -s ~/moblododo/usr.share/aurorae.themes/Moblododo-dark/ /usr/share/aurorae/themes/Moblododo-dark
sudo ln -s ~/moblododo/usr.share/aurorae.themes/Moblododo-light/ /usr/share/aurorae/themes/Moblododo-light
```
Set in KDE system settings at *Appearance > Window Decorations*.


#### QtCurve (.usr.share/QtCurve/)
```
sudo ln -s ~/moblododo/usr.share/QtCurve/Moblododo.qtcurve /usr/share/QtCurve/Moblododo.qtcurve
```
Set QtCurve profile in KDE system settings at *Appearance > Application Style > QtCurve*.


#### Wallpapers (.wallpapers/)
Put these wherever you prefer, or navigate to this folder when you set the wallpaper.


#### Colour-schemes (.usr.share/color-schemes/)
```
sudo cp -p ~/moblododo/usr.share/color-schemes/Moblododo.colors /usr/share/color-schemes/Moblododo.colors
sudo chown root:root /usr/share/color-schemes/Moblododo.colors
sudo chmod 775 /usr/share/color-schemes/Moblododo.colors
```
Set colours in KDE system settings at *Appearance > Colours*.


#### Konsole (.usr.share/konsole/)
```
sudo ln -s ~/moblododo/usr.share/konsole/Moblododo-dark.colorscheme /usr/share/konsole/Moblododo-dark.colorscheme
sudo ln -s ~/moblododo/usr.share/konsole/Moblododo-light.colorscheme /usr/share/konsole/Moblododo-light.colorscheme
```
Apply colours in Konsole settings.


#### GRUB (.boot.grub/)
```
sudo ln -s ~/moblododo/boot.grub/moblododo_1920x1200_8bit.png /boot/grub/moblododo_1920x1200_8bit.png
sudo update-grub
```
Note: Image format must be png 256 colours (8bit).


#### Plymouth (.usr.share/plymouth.themes/)
```
sudo cp -p -r ~/moblododo/usr.share/plymouth.themes/moblododo/ /usr/share/plymouth/themes/moblododo
sudo chown -R root:root /usr/share/plymouth/themes/moblododo/
sudo chmod 775 -R /usr/share/plymouth/themes/moblododo/
```
Set theme in KDE system settings at *Appearance > Boot Splash Screen*.


#### SDDM (.usr.share/sddm.themes/)
```
sudo cp -p -r ~/moblododo/usr.share/sddm.themes/moblododo/ /usr/share/sddm/themes/moblododo
sudo chown -R root:root /usr/share/sddm/themes/moblododo/
sudo chmod 775 -R /usr/share/sddm/themes/moblododo/
```
Set SDDM in KDE system settings at *Startup and Shutdown > Login Screen (SDDM)*.
 - symlinks don't work even though it will display in the settings dialog.
 - using the equiv directory in home also doesn't seem to play ball.


#### Look and Feel (.usr.share/plasma.look-and-feel/)
```
sudo ln -s ~/moblododo/usr.share/plasma.look-and-feel/moblododo/ /usr/share/plasma/look-and-feel/moblododo
```
Set theme in KDE system settings at *Appearance > Splash Screen*.


#### Desktop Theme (.usr.share/plasma.look-and-feel/)
```
sudo ln -s ~/moblododo/usr.share/plasma.desktoptheme/moblododo/ /usr/share/plasma/desktoptheme/moblododo
```
Set theme in KDE system settings at *Appearance > Plasma Style*.
