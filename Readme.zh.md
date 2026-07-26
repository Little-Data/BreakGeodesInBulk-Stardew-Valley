# BreakGeodesInBulk

星露谷物语 mod，批量砸开晶石，跳过/加快砸开晶石动画。

> [!IMPORTANT]
>原仓库:[BreakGeodesInBulk](https://github.com/jessevang/BreakGeodesInBulk)
>
>原 nexusmods:[Break Geodes In Bulk (No Longer Maintained)](https://www.nexusmods.com/stardewvalley/mods/34257)

# 安装

1. **安装 SMAPI** - 从 [smapi.io](https://smapi.io) 下载
2. **下载本模组** - 从 [GitHub release](https://github.com/Little-Data/BreakGeodesInBulk-Stardew-Valley/releases) 获取最新版本
3. **解压到 Mods 文件夹** - 将模组解压到 `Stardew Valley/Mods/BreakGeodesInBulk`

# 配置
## 游戏内配置（推荐）

1. 安装 [Generic Mod Config Menu](https://www.nexusmods.com/stardewvalley/mods/5098)
2. 进入主菜单点击齿轮图标
3. 在模组列表中找到"BreakGeodesInBulk"
4. 通过用户界面配置你的偏好

## 手动配置

编辑模组文件夹中的 `config.json`：

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
## 配置选项

| 设置 | 描述 | 默认值 |
|---|---|---|
| `GeodesToBreak` | 晶球打破模式：背包能装下时适量打破，或全部打碎掉地上 | `AllIfInventoryFits` |
| `AnimationSpeedMultiplier` | 动画速度倍率（0.1 ~ 1.0），跳过动画时忽略 | `0.3` |
| `SkipAnimation` | 跳过砸开动画，立即获得奖励 | `false` |
| `PlaySound` | 播放砸开音效，仅启用跳过动画时生效 | `true` |
| `ShowOverlay` | 在铁砧上显示 x{N} 数量叠加文字 | `true` |
| `OverlayOffsetX` | 叠加文字横向偏移（-500 ~ 500） | `40` |
| `OverlayOffsetY` | 叠加文字纵向偏移（-500 ~ 500） | `60` |
| `OverlayScale` | 叠加文字缩放（0.1 ~ 2.0） | `1.0` |
| `UseMobileGeodeFix` | 移动端兼容模式，防止移动端崩溃 | `false` |
| `DebugMode` | 启用详细日志以帮助调试 | `false` |

## 技术细节

### 需求

- **[SMAPI 4.0.0+](https://smapi.io/)** - 星露谷物语模组框架
- **[星露谷物语 1.5+](https://store.steampowered.com/app/413150/Stardew_Valley/)** - 基础游戏
- **[.NET 6.0](https://dotnet.microsoft.com/download/dotnet/6.0)**（随游戏附带，编译 dll 所需）

### 可选依赖

- **[Generic Mod Config Menu](https://www.nexusmods.com/stardewvalley/mods/5098)** - 用于游戏内配置

## 开发

### 从源码构建

构建前确保你已经有了星露谷游戏本体

在包含 `BreakGeodesInBulk.sln` 的目录中使用：

```bash
dotnet build
```

手动指定游戏安装目录：

```bash
dotnet build -c Release /p:GamePath="[GamePath]"
```

### 本地化翻译

参考 `i18n` 文件夹中已有的翻译，新建一个 json 语言文件。

## 支持

- **报告 Bug** - 访问 [GitHub Issues](https://github.com/Little-Data/BreakGeodesInBulk-Stardew-Valley/issues) 页面
- **建议功能** - 在 GitHub 上提交功能请求

## 鸣谢

**原作者**：[Darkmushu1](https://www.nexusmods.com/profile/Darkmushu1)

感谢 [ConcernedApe](https://twitter.com/ConcernedApe) 创造了星露谷物语并提供了优秀的模组框架。特别感谢活跃的模组社区维护文档和开发工具。