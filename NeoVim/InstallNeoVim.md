### Install NeoVim
> winget install Neovim.Neovim

### Setup user profile & command aliases
> mkdir .config/powershell

> nvim .config/powershell/user_profile.ps1

Add these alies to `user_profile.ps1` file
```ps1
# Alias
Set-Alias vim nvim
Set-Alias ll ls
Set-Alias g git
Set-Alias grep findstr
Set-Alias tig 'C:\Program Files\Git\usr\bin\tig.exe'
Set-Alias less 'C:\Program Files\Git\usr\bin\less.exe'
```

Set nvim profile, run below command to open `Microsoft.PowerShell_profile.ps1`
>nvim $PROFILE.CurrentUserCurrentHost

Add this to `Microsoft.PowerShell_profile.ps1`
```ps1
. $env:USERPROFILE\.config\powershell\user_profile.ps1
```
Example `Microsoft.PowerShell_profile.ps1`:
```ps1
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\bubbles.omp.json" | Invoke-Expression

. $env:USERPROFILE\.config\powershell\user_profile.ps1
```
Above aliases should now be added. Open another terminal session to make sure they work.
