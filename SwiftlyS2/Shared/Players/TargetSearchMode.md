<a id="targetsearchmode"></a>

# 📋 TargetSearchMode

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `enum`

## 📋 枚举值

| 名称 | 值 | 描述 |
|------|------|------|
| `None` | `0` | 无特定搜索模式；默认行为。 |
| `Alive` | `1 << 0` | 在搜索结果中包含存活玩家。 |
| `Dead` | `1 << 1` | 在搜索结果中包含已阵亡的玩家。 |
| `NoMultipleTargets` | `1 << 2` | 将搜索限制为仅针对单个目标。 |
| `IncludeSelf` | `1 << 3` | 在搜索结果中包含搜索中的玩家。 |
| `TeamOnly` | `1 << 4` | 在搜索结果中仅包含来自同一队伍的玩家。 |
| `OppositeTeamOnly` | `1 << 5` | 搜索结果中仅包含对方队伍的玩家。 |
| `NoBots` | `1 << 6` | 从搜索结果中排除机器人玩家。 |

