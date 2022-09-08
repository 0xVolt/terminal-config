# My terminal configuration
A repository to document the setup of my custom terminal prompt and to share the terminal engine configuration files. Consider this a far less cool .vimrc.

## Steps to setting up `oh-my-posh`
###### In case you *accidentally* brick your computer.
### Prerequisite steps for Windows Terminal
- [ ] Install powershell from the Microsoft store.
- [ ] Change `powershell` to be the default shell in the Windows Terminal app. 
- [ ] Pop open the `settings.json` file.
- [ ] Set the `hidden` field to `true` for Windows Powershell.
- [ ] Bring the bottom profile to the top. 
### Installing `oh-my-posh`
- [ ] Run 
    ```powershell
    winget install JanDeDobbeleer.OhMyPosh -s winget
    ```
- [ ] Restart Windows Terminal
- [ ] Head to Nerd Fonts and download any one of those fonts
- [ ] Drag and drop all of them in the fonts folder
- [ ] Change the font of powershell in the settings

### Creating a default profile for powershell to run
- [ ] Create a new directory in the `Documents` folder named `PowerShell`
- [ ] Run 
    ```powershell
    echo 'test string' > C:\Users\deshi\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
    ```
- [ ] Open the new profile initialised in VSCode
- [ ] Get rid of everything and type 
    ```powershell
    oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/jandedobbeleer.omp.json' | Invoke-Expression
    ```