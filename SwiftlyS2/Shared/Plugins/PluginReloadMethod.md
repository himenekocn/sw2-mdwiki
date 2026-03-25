<a id="pluginreloadmethod"></a>

# 📋 PluginReloadMethod

**命名空间:** `SwiftlyS2.Shared.Plugins`

**类型:** `enum`

## 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `Auto` | `0` | 默认设置。当 DLL 文件更新时，系统将自动重新加载；或者您也可以使用 reload 命令手动执行。 |
| `OnMapChange` | `1` | 当 DLL 文件更新后，不会立即重新加载，需等待新地图开始时才会生效。或者，您也可以随时使用 reload 命令手动重载。 |
| `OnlyByCommand` | `2` | 你只能使用重新装填命令。它不会自动重新装填。 |

