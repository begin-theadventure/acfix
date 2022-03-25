## Make Assasin's Creed: 2, Brotherhood and Unity work.
### About
This makes Assassins Creed 2, Brotherhood and Unity (DLCs) work with the native Linux Steam client. 
We do this by downloading an edited .json file that changes "DLC" to "hidden_DLC" and then using [Steam Metadata Editor](https://github.com/tralph3/Steam-Metadata-Editor) we patch the appinfo.vdf file.

After such procedure the games should launch!
### How to apply
The most convenient way is to use a bash script that'll do everything for you.

[All at once](https://github.com/begin-theadventure/acfix/releases/tag/ACA), 
[Assassin's Creed 2](https://github.com/begin-theadventure/acfix/releases/tag/AC2), 
[Assassin's Creed Brotherhood](https://github.com/begin-theadventure/acfix/releases/tag/ACB), 
[Assassin's Creed Unity](https://github.com/begin-theadventure/acfix/releases/tag/ACU).

Make sure it's executable before using it:

GUI: Properties -> Permissions -> ..

Terminal: chmod +x name

### FAQ
- Game still doesn't work.

Additionaly, you may also need to install [**Steamworks Common Redistributables**](https://steamdb.info/app/228980) from the client or using `steam steam://install/228980`.

- Does this fix work on Steam Deck? 
In short: **YES**.

Steam Metadata Editor is a python application but Steam depends on python so Steam Deck has it installed by default.

I also replaced wget with curl because Steam Deck doesn't have wget.

### How to apply
(_other methods_)

2) Terminal:

Take a look at the scripts (here on GitHub) and just copy the commands.

3) (almost all w/) GUI:

'Save as' [Steam Metadata Editor](https://raw.githubusercontent.com/tralph3/Steam-Metadata-Editor/master/src/steammetadataeditor) to x directory -> make it executable -> download modifications.json -> move to ~/.local/share/Steam-Metadata-Editor/config -> open terminal -> cd x directory -> ./steammetadataeditor -s
