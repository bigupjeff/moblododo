# Moblododo - A KDE Plasma 5 Theme

This is my personal KDE Plasma 5 theme which is a constant work in progress. All the important bits like splash screens and window decorations are themed. Don't expect anything in here to be perfectly tidy, complete or best practice! ...KDE theming is a messy disjointed biz 🥲...

 - To install on a restricted OS or just to restrict to user, replace `/usr/share/` with `~/.local/share/` in the command paths. It should work for most/all of it.
 - Dirs are named after their destined system locations, so boot.grub = `/boot/grub/`.
 - You don't have to symlink the assets as I've suggested, it just helps me when I'm making changes. Instead you can just copy all files to the destinations instead. If you do this, remember to set ownership on the copied files appropriately.

## Future Plans
 - Write an install script.
 - Share on the KDE store when it's more mature.

## Theme Assets Included

Aurorae         Window Decorations.
QtCurve         UI 'widget' styles to change buttons, tabs, toolbars, loading bars etc.
Wallpapers      Wallpaper images.
Color-schemes   Plasma theme colour schemes for all UI elements.
Konsole         Colour schemes for the Konsole terminal.
GRUB            GRUB menu background.
Plymouth        Boot splash shown directly after GRUB.
SDDM            Login/lock screen theme.
Splash Screen   Plasma Look and Feel theme, currently only contains splash screen shown after login.

#### Aurorae (.usr.share/aurorae.themes/)
Symlink `...moblododo/usr.share/aurorae.themes/Moblododo-dark/` to `/usr/share/aurorae/themes/Moblododo-dark`.
Symlink `...moblododo/usr.share/aurorae.themes/Moblododo-light/` to `/usr/share/aurorae/themes/Moblododo-light`.
 - Set in KDE system settings at *Appearance > Window Decorations*.

#### QtCurve (.usr.share/QtCurve/)
Symlink `...moblododo/usr.share/QtCurve/Moblododo.qtcurve` to `/usr/share/QtCurve/Moblododo.qtcurve`.
 - QTCurve settings found in KDE system settings at *Appearance > Application Style > QtCurve*.
 - If theme doesn't appear, click import to locate and install.
 - Select and apply.

#### Wallpapers (.wallpapers/)
Put these wherever you prefer, or just navigate to the folder when you set the wallpaper.

#### Colour-schemes (.usr.share/color-schemes/)
Copy `...moblododo/usr.share/color-schemes/Moblododo.colors` to `/usr/share/color-schemes/Moblododo.colors`.
Set colours in KDE system settings at *Appearance > Colours*.
 - Alternatively open the colours settings and 'Install from File...' (does the same thing).

#### Konsole (.usr.share/konsole/)
Symlink `...moblododo/usr.share/konsole/Moblododo-dark.colorscheme` to `/usr/share/konsole/Moblododo-dark.colorscheme`.
Symlink `...moblododo/usr.share/konsole/Moblododo-light.colorscheme` to `/usr/share/konsole/Moblododo-light.colorscheme`.
 - Apply colours in Konsole settings.

#### GRUB (.boot.grub/)
Symlink `...moblododo/boot.grub/moblododo_1920x1200_8bit.png` to `/boot/grub/moblododo_1920x1200_8bit.png` then run "sudo update-grub".
 - Image format must be png 256 colours (8bit).

#### Plymouth (.usr.share/plymouth.themes/)
Copy `...moblododo/usr.share/plymouth.themes/moblododo/` to `/usr/share/plymouth/themes/moblododo`.
Set theme in KDE system settings at *Appearance > Boot Splash Screen*.
 - Need to test symlinking

#### SDDM (.usr.share/sddm.themes/)
Copy `...moblododo/usr.share/sddm.themes/moblododo/` to `/usr/share/sddm/themes/moblododo`.
Set theme in KDE system settings at *Startup and Shutdown > Login Screen (SDDM)*.
 - symlinks don't work even though it will display in the settings dialog.
 - using the equiv directory in home also doesn't seem to play ball.

#### Splash Screen (.usr.share/plasma.look-and-feel/)
Symlink `...moblododo/usr.share/plasma.look-and-feel/moblododo/` to `/usr/share/plasma/look-and-feel/moblododo`.
Set theme in KDE system settings at *Appearance > Splash Screen*.
