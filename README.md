# wise_fish
Instructions and Scripts for setting up an efficient fish environment

1. Install [fish](http://fish.sh)
  - `sudo apt install fish` (run fish --version after install, if it's not >=2.3 uninstall with `sudo apt remove fish` and then compile from source instead.)
  
2. Install [Fisherman](http://fisherman.sh)
  - `curl -Lo ~/.config/fish/functions/fisher.fish --create-dirs git.io/fisher`
  
3. Set fish as default shell
  - `which fish` to get absolute path to fish executable
  - `cat /etc/shells` - make sure that path from previous command is in output, use `sudo nano /etc/shells` to add it if it doesn't show up
  - `chsh -s <fish_location>`
  
4. Logout and back in or reboot

5. Install useful python-based tools
  - `sudo -H pip install thefuck`
  - `sudo -H pip install virtualfish`
  
6. Install fish plugins with fisherman
  - `fisher z omf/thefuck omf/sudope omf/apt omf/virtualfish`
  
7. Set [VirtualFish](http://https://virtualfish.readthedocs.io) environment variables to enable automatic virtual environment activation, project based commands and global requirements (to ensure certain packages are installed with every new virtual environment)
  - `set -Ux VIRTUALFISH_PLUGINS "auto_activation projects global_requirements"`
  
8. Install prompt [theme](https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md) that will automagically show active virtual environment.  If you want to try a different theme, installing a new one will automatically remove the previous theme, no need to uninstall it first.  The options listed here do not require custom fonts.

  - `fisher omf/theme-cmorrell`  ![theme-cmorrell](https://cloud.githubusercontent.com/assets/21592/4770904/8a58e026-5b89-11e4-927c-42a387b41df0.gif)
  
  - `fisher omf/theme-edan`  ![theme-edan](https://cloud.githubusercontent.com/assets/215282/6199938/f67e6a54-b49a-11e4-800b-587a638cfb86.png)
  
  - `fisher omf/theme-l`  ![theme-l](https://camo.githubusercontent.com/38f7780f0669497d4774def9615febec26a98a34/687474703a2f2f662e636c2e6c792f6974656d732f324a334d30663258316a337534373179303830492f322e706e67)
  
  - `fisher omf/theme-scorphish`
  ---
    ![theme-scorphish](https://cloud.githubusercontent.com/assets/2112697/7443483/01d3dd56-f124-11e4-91c3-72a93fbc0dda.png)
---

## Extra Credit
  - Install additional [oh-my-fish](https://github.com/oh-my-fish) plugins.
  - Install [powerline fonts](https://github.com/powerline/fonts)
  - Configure terminal to use one of the new powerline patched fonts (I recommend _Sauce Code Powerline_ or _Ubuntu Mono Derivative_)
  - Install powerline based theme
    - `fisher omf/theme-agnoster`  ![theme-agnoster](https://camo.githubusercontent.com/dabb1f1504c88e93248b3c3b3f9741c4c611acde/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f313736353230392f3235353337392f34353263363638652d386330622d313165322d386138652d6431643133653537643135662e706e67)
    - `fisher omf/theme-budspencer`  ![theme-budspencer](https://raw.githubusercontent.com/tannhuber/media/master/budspencer_pwd_style.jpg)
