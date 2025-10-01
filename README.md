<pre style="font-size:34px">
        ░▀█▀░█▀█░█░█░█▀█░█░█░█▀▄░█░░░█▀▄
        ░░█░░█▀█░░█░░█░█░█▄█░█▀▄░█░░░█░█
        ░░▀░░▀░▀░░▀░░▀▀▀░▀░▀░▀░▀░▀▀▀░▀▀░ 's
                 OMARCHY MAC MENU
*Made with love for omarchy and the omarchy-mac fork*
</pre>

### GALLERY
<div>
  <img src="https://github.com/tayowrld/omarchy-mac-menu/blob/main/assets/1.jpg?raw=true" style="width:48%"/>
  <img src="https://github.com/tayowrld/omarchy-mac-menu/blob/main/assets/2.jpg?raw=true" style="width:48%"/>
  <img src="https://github.com/tayowrld/omarchy-mac-menu/blob/main/assets/3.jpg?raw=true" style="width:67%"/>
</div>


| Tested on                      | Performance |
| ------------------------------ | ----------- |
| MacBook Pro 16 (M1 Max / 32GB) | Fine        |
| MacBook Air (M1 / 8GB)         | Fine        |

### What and why changed?

Walker is a great and flexible piece of software, but not on *aarch64* architecture. The Omarchy menu was originally built under this frontend, which caused bugs such as cancel-loops, visual glitches, performance issues, and limited functionality.

I retranslated calls from the Omarchy backend to the Fuzzel frontend, and this solved most problems, if not all. **The important thing is that this is not an official change and is not supported by Omarchy (or Omarchy aarch64).** You will need to save and keep an Omarchy-menu backup, as it could be overwritten after updating Omarchy.

**I do not recommend you to use this utility. All changes to the original bin files are at your own risk. I can only read your issues and try to fix them.**

<pre>
░█▀▄░█▀▀░█▀█░█▀▀░█▀█░█▀▄░█▀▀░█▀█░█▀▀░▀█▀░█▀▀░█▀▀
░█░█░█▀▀░█▀▀░█▀▀░█░█░█░█░█▀▀░█░█░█░░░░█░░█▀▀░▀▀█
░▀▀░░▀▀▀░▀░░░▀▀▀░▀░▀░▀▀░░▀▀▀░▀░▀░▀▀▀░▀▀▀░▀▀▀░▀▀▀
</pre>


```bash
sudo pacman -S fuzzel
```

* Omarchy must also already be installed. I used this fork and it worked great for me on a Mac: [https://github.com/malik-na/omarchy-mac](https://github.com/malik-na/omarchy-mac)
* For non-Mac systems, it is recommended to use Armarchy or other forks.


<pre>
░█▀█░█░█░▀█▀░█▀█░░░░░█░░░█▀█░▀█▀░▀█▀░█▀█░█▀█
░█▀█░█░█░░█░░█░█░▄▄▄░█░░░█▀█░░█░░░█░░█░█░█░█
░▀░▀░▀▀▀░░▀░░▀▀▀░░░░░▀▀▀░▀░▀░░▀░░▀▀▀░▀▀▀░▀░▀
</pre>


**Requires ```git, rsync```**

```bash
  cd ~
  git clone https://github.com/tayowrld/omarchy-mac-menu/
  cd omarchy-mac-menu
  sh manage-mac-menu.sh
```

It would clone the repository and auto-install all the components.


<pre>
░█▄█░█▀█░█▀█░█░█░░░░░█░░░█▀█░▀█▀░▀█▀░█▀█░█▀█
░█░█░█▀█░█░█░█░█░▄▄▄░█░░░█▀█░░█░░░█░░█░█░█░█
░▀░▀░▀░▀░▀░▀░▀▀▀░░░░░▀▀▀░▀░▀░░▀░░▀▀▀░▀▀▀░▀░▀        
</pre>


* ***IMPORTANT: BACK UP YOUR ORIGINAL OMARCHY-MENU FUZZEL CONFIG (if it exists)***

  You can do this simply by running: (never use sudo here, if you have that habit)

  ```bash
  mv ~/.config/fuzzel/ ~/.config/fuzzel.bak
  cp ~/.local/share/omarchy/bin/ ~/.local/share/omarchy/bin.bak
  ```

* Go to your home directory (or any working directory) and clone this repo:

  ```bash
  cd ~
  git clone https://github.com/tayowrld/omarchy-mac-menu/
  ```

* Enter the folder and copy the files like this:

  ```bash
  cd omarchy-mac-menu
  cp -R ./omarchy/bin/omarchy-* ~/.local/share/omarchy/bin/
  cp -rf fuzzel ~/.config
  ```

* You can now delete the cloned repo (or skip this step):

  ```bash
  cd ..
  rm -rf omarchy-mac-menu
  ```

And you're good to go. Try running `omarchy-menu` in the terminal and check the changes. If it has changed but the SUPER+ALT+SPACE keybind still launches Walker, try rebooting or logging out and back in. If nothing has changed, restore the backups and repeat the steps. If I made a mistake in the manual, open an issue.

### AFTERWORDS

Thank you for your attention. If you encounter any bugs, you can always open an issue and I will fix them. Enhancements and updates are also welcome. Have a good time with Omarchy and its community.
