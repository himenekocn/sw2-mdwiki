# 📦 MenuOptionEventArgs

为菜单选项事件提供事件数据。

**命名空间:** `SwiftlyS2.Shared.Menus`

**类型:** `class`

**继承:** `EventArgs`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Player` | `IPlayer?` | get | 触发此菜单事件的玩家。 |
| `Option` | `IMenuOption?` | get | 与此事件相关的菜单选项，或对于打开或关闭菜单等生命周期事件则为 null。 |

