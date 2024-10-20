<div align="center">
    <h1>Redish Midnight</h1>
    <p>Dark theme for Linux desktops based on <a href="https://github.com/legendlife/Redish" target="_blank">Redish</a>, <a href="https://github.com/vinceliuice/Lavanda-kde" target="_blank">Lavanda</a>, and <a href="https://github.com/folke/tokyonight.nvim">Tokyo Night</a></p>
</div>

- **Distro:** Debian 12
- **Desktop Environment:** Xfce 4.18
- **Window Manager:** Xfwm4
- **Panel:** Xfce4-panel (Centered time using 3 equal-width panels)
- **File Manager:** Thunar
- **Icons:** [Suru++Asprómauros](https://github.com/gusbemacbe/suru-plus-aspromauros), with colors modified to match Redish
- **Cursor:** Adwaita
- **Terminal:** xfce4-terminal with colors modified to match Redish + Tokyo Night
- **Greeter**: LightDM
- **GTK + Window Manager + Greeter Theme:** RedishMidnight - The [Lavanda + Tokyo Night theme](https://github.com/mehedirm6244/Miserable_Xfce/tree/Serenade) from Miserable_Xfce + modified to match Redish colors + styled window buttons in GIMP (.xcf files also uploaded). Only tested on GTK 3.0, behavior may be inconsistent for other versions
- **GRUB Bootloader Theme:** [Xenlism](https://www.pling.com/p/1440862) with settings, colors, and images edited to match Redish - only the Debian version is in this repo, but the modifications here can (probably) be easily copied to Xenlism versions for other distros
- **Fonts:** Noto Mono Regular for terminal + bootloader, Inter everywhere else
- **Wallpaper:** [Window Samurai](https://github.com/legendlife/Redish/blob/main/wallpaper/window-samurai.jpg) from Redish, created by [Crysalis](https://www.instagram.com/curisaris/)
- **IDE**: VSCodium w/ Tokyo Night extension, with settings.json modified to match Redish. Should also work w/ VSCode

### GRUB Bootloader Customization

```bash
$ sudo vim /etc/default/grub

# Add the following lines:
export GRUB_COLOR_NORMAL="red/black"
export GRUB_COLOR_HIGHLIGHT="black/red"
export GRUB_MENU_PICTURE="{YOUR_WALLPAPER_PATH}/window-samurai.jpg"

# In another terminal, use your distro's command to convert font for GRUB (paths and commands below may differ)
# ex. $sudo grub-mkfont -s 11 -o /boot/grub/fonts/NotoMono-Regular.pf2 /usr/share/fonts/truetype/noto/NotoMono-Regular.ttf
export GRUB_FONT="/boot/{YOUR_FONT_PATH}/NotoMono-Regular.pf2"

$ sudo update-grub
```