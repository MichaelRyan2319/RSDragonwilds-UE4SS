# UE4SS for RuneScape: Dragonwilds

[UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) packaged for RuneScape: Dragonwilds.
Lua mods such as [First Person](https://github.com/MichaelRyan2319/RSDragonwilds-FirstPersonIndoors)
need it to run.

This is unmodified UE4SS v3.0.1-1217 (the `experimental-latest` build). It works
with the game's Unreal Engine 5.6 build (26162923) with no extra setup. The only
changes are to `ue4ss/Mods/mods.txt` and `mods.json`: the built-in example mods
are switched off. Most of them are cheats or developer tools (cheat manager,
console, split screen, line trace, keybinds).

## Install

Download `UE4SS-RSDragonwilds.zip` from the [Releases](../../releases) page and
extract it into the game's Win64 folder. In Steam, right-click RuneScape:
Dragonwilds > Manage > Browse local files, then open
`RSDragonwilds\Binaries\Win64`. `dwmapi.dll` and the `ue4ss` folder should sit
next to `RSDragonwilds-Win64-Shipping.exe`.

The repo contains the same files, laid out the same way.

If your antivirus deletes or blocks `dwmapi.dll`, allow it. UE4SS loads into the
game through that file, and antivirus tools sometimes flag it for that reason.

## Adding mods

Put each mod folder in `ue4ss\Mods\`. A mod loads if its folder contains an
`enabled.txt` file, or if `ue4ss\Mods\mods.txt` has a `ModName : 1` line.

The log is `ue4ss\UE4SS.log`.

## Uninstall

Delete `dwmapi.dll` and the `ue4ss` folder from Win64.

## Licence

UE4SS is made by the UE4SS team and released under the MIT licence (see
`LICENSE`). This repo only redistributes it.
