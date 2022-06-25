### Install
```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
```

### Setup to load on startup
Open the powershell user profile `.ps1` file
```powershell
code $PROFILE
```
Add this and save file
```powershell
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\bubbles.omp.json" | Invoke-Expression
 ```
