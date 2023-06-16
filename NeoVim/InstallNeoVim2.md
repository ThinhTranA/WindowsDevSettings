
### Install neovim with choco
```bash
choco install neovim
```

### Install [vim plug](https://github.com/junegunn/vim-plug) to run Plugin in neovim.
```bash
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
```

### Update local configuration
Open AppData folder  `Win`+`R` , go to either Roaming or Local
```bash
%appdata%
```
Create an `nvim` folder, in this folder create an `init.vim` file.

Or just copy the `init.vim` file here.
