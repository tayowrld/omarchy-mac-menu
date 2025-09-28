# Full-featured omarchy menu for aarch64

*Made with love for omarchy and omarchy-mac fork*

| Tested on                           | Results                                  |
| ----------------------------------- | ---------------------------------------- |
| **MacBook Pro 16 (M1 Max \| 32GB)** | Total performance, everything works fine |

### What and why changed?

Walker is a great and elastic software, but not on *aarch64* architecture. Omarchy menu is originally built under this frontend. That caused bugs, like cancel-loop, visual glitches, performance issues and dumb cropped functional.

I've retranslated calls from omarchy backend to fuzzel frontend and this solved most of problems, if not everything. **The important thing it's not official change and not supported by omarchy (so as omarchy aarch64)**. You will need to save and keep the omarchy-menu backup. Also it could be overwritten after updating omarchy.

**I don't afford you to use this utility. All changes in the original bin files are at your own risk. I can only read your issues and try to fix em.**

### DEPENDENCIES

```bash
sudo pacman -S fuzzel

```

- Omarchy also must be already installed. I used this fork and it worked great for me on a mac: https://github.com/malik-na/omarchy-mac
- For non-mac it's recommended to use armarchy or other forks

### MANUAL STEPS

- ***IMPORTANT: COVER YOUR BACKUPS FOR ORIGINAL OMARCHY-MENU FUZZEL CONFIG (if it exists)***

  you can do it simply running this: (never use sudo there, if you got this mania)

  ```bash
  mv ~/.config/fuzzel/ ~/.config/fuzzel.bak
  cp ~/.local/share/omarchy/bin/ ~/.local/share/omarchy/bin.bak
  ```

- Go to Home dir (or git dir) and clone this repo

  ```bash
  cd ~
  git clone https://github.com/tayowrld/omarchy-mac-menu/
  ```

- Get inside and copy files like this

  ```bash
  cd omarchy-mac-menu
  cp -rf omarchy-menu ~/.local/share/omarchy/bin/omarchy-menu
  cp -r fuzzel ~/.config
  ```

- You can now delete the git clone (or skip this step)

  ```
  cd ..
  rm -rf omarchy-mac-menu
  ```

  And you're up to go. Try to run ```omarchy-menu``` using terminal and see changes. If it's changed, but keybind SUPER+ALT+SPACE still shows walker, try to reboot or log out and enter the session again. If nothing changed, try to recover backups and do everything again. If I'm wrong in the manual, pull issue.

### AFTERWORDS

Thank you for your attention. If you got any bugs, you always can open an issue and I'll fix it. The enhancement and update are also greeted. Have a good time with omarchy and it's community.
