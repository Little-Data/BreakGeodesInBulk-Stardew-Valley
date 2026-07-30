# BreakGeodesInBulk

English | [简体中文](/Readme.zh.md)

Stardew Valley mod to break geodes in bulk, skip/speed up the geode breaking animation.

> [!IMPORTANT]
> Original repo: [BreakGeodesInBulk](https://github.com/jessevang/BreakGeodesInBulk)
>
> Original nexusmods: [Break Geodes In Bulk (No Longer Maintained)](https://www.nexusmods.com/stardewvalley/mods/34257)

# Installation

1. **Install SMAPI** - Download from [smapi.io](https://smapi.io)
2. **Download this mod** - Get the latest release from [GitHub releases](https://github.com/Little-Data/BreakGeodesInBulk-Stardew-Valley/releases)
3. **Extract to Mods folder** - Extract the mod to `Stardew Valley/Mods/BreakGeodesInBulk`

# Configuration

> [!WARNING]
> 如果要在移动设备上使用 **必须开启** 移动端兼容模式，否则游戏崩溃！
> 
> If you want to use it on mobile devices, **you must enable mobile compatibility mode**, or the game will crash!

## In-Game Configuration (Recommended)

1. Install [Generic Mod Config Menu](https://www.nexusmods.com/stardewvalley/mods/5098)
2. Click the gear icon on the title screen
3. Find "BreakGeodesInBulk" in the mod list
4. Configure your preferences through the UI

## Manual Configuration

Edit `config.json` in the mod folder:

```json
{
  "GeodesToBreak": "AllIfInventoryFits",
  "AnimationSpeedMultiplier": 0.3,
  "OverlayOffsetX": 40,
  "OverlayOffsetY": 60,
  "OverlayScale": 1.0,
  "UseMobileGeodeFix": false,
  "DebugMode": false,
  "SkipAnimation": false,
  "PlaySound": true,
  "ShowOverlay": true
}
```

## Configuration Options

| Setting | Description | Default |
|---|---|---|
| `GeodesToBreak` | Geode break mode: break as many as fit in inventory, or all with extras falling on ground | `AllIfInventoryFits` |
| `AnimationSpeedMultiplier` | Animation speed multiplier (0.1 ~ 1.0), ignored when Skip Animation is enabled | `0.3` |
| `SkipAnimation` | Skip the breaking animation, rewards are given instantly | `false` |
| `PlaySound` | Play a break sound when cracking geodes, only applies when Skip Animation is enabled | `true` |
| `ShowOverlay` | Show the x{N} count overlay on the geode spot | `true` |
| `OverlayOffsetX` | Overlay horizontal offset (-500 ~ 500) | `40` |
| `OverlayOffsetY` | Overlay vertical offset (-500 ~ 500) | `60` |
| `OverlayScale` | Overlay font scale (0.1 ~ 2.0) | `1.0` |
| `UseMobileGeodeFix` | Mobile compatibility mode to prevent crashes on Android | `false` |
| `DebugMode` | Enable verbose logging for debugging | `false` |

## Technical Details

### Requirements

- **[SMAPI 4.0.0+](https://smapi.io/)** - Stardew Valley modding framework
- **[Stardew Valley 1.5+](https://store.steampowered.com/app/413150/Stardew_Valley/)** - Base game
- **[.NET 6.0](https://dotnet.microsoft.com/download/dotnet/6.0)** (bundled with the game, required for building the dll)

### Optional Dependencies

- **[Generic Mod Config Menu](https://www.nexusmods.com/stardewvalley/mods/5098)** - For in-game configuration UI

## Development

### Building from Source

Make sure you have Stardew Valley game before building.

Run this command in the directory containing `BreakGeodesInBulk.sln`:

```bash
dotnet build
```

Manually specify the game install directory:

```bash
dotnet build -c Release /p:GamePath="[GamePath]"
```

### Localization

Refer to existing translations in the `i18n` folder and create a new JSON language file.

## Support

- **Report Bugs** - Visit the [GitHub Issues](https://github.com/Little-Data/BreakGeodesInBulk-Stardew-Valley/issues) page
- **Feature Requests** - Submit a feature request on GitHub

## Credits

**Original Author**: [Darkmushu1](https://www.nexusmods.com/profile/Darkmushu1)

Thanks to [ConcernedApe](https://twitter.com/ConcernedApe) for creating Stardew Valley and providing an excellent modding framework. Special thanks to the active modding community for maintaining documentation and development tools.
