# 📦 MenuOptionEventArgs

Provides event data for menu option events.

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `class`

**继承:** `EventArgs`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Player` | `IPlayer?` | get | The player who triggered this menu event. |
| `Option` | `IMenuOption?` | get | The menu option involved in this event, or null for lifecycle events like opening or closing the menu. |

