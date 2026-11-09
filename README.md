# UE4SS for RuneScape: Dragonwilds

[UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) packaged for RuneScape: Dragonwilds.
Lua mods such as [First Person](https://github.com/MichaelRyan2319/RSDragonwilds-FirstPersonIndoors)
need it to run.

This is unmodified UE4SS v3.0.1-1217 (the `experimental-latest` build). It works
with the game's Unreal Engine 5.6 build (26162923) with no extra setup. The only
changes are to `ue4ss/Mods/mods.txt` and `mods.json`: the built-in example mods
are switched off. Most of them are cheats or developer tools (cheat manager,
console, split screen, line trace, keybinds).

## Install with Mod Loader

In [Mod Loader](https://github.com/MichaelRyan2319/ModLoader), add RuneScape:
Dragonwilds, then add the mod `MichaelRyan2319/RSDragonwilds-UE4SS`, before any
Lua mod that needs it. Mod Loader 1.0.1 or later sets the game's mods folder to
its inner `RSDragonwilds` folder (the one with `Binaries` and `Content` in it).
If you added the game with an older version, edit it and choose that folder.

## Install by hand

Download `UE4SS-RSDragonwilds.zip` from the [Releases](../../releases) page. In
Steam, right-click RuneScape: Dragonwilds > Manage > Browse local files, then
open the `RSDragonwilds` folder (the one with `Binaries` and `Content` in it)
and extract the zip there. `dwmapi.dll` and the `ue4ss` folder end up in
`Binaries\Win64`, next to `RSDragonwilds-Win64-Shipping.exe`.

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
