# 🔌 IConVar

**命名空间:** `SwiftlyS2.Shared.Convars`

**类型:** `interface`

**继承:** `IConVar`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Value` | `T` | get, set | The value of the convar. When setting, if the convar can be replicated, it will automatically replicate to all clients. Also, setting value with this method will internally put it into a set queue, Which means that for some special case ( e.g. setting sv_enablebunnyhopping inside a hook ) it won't work, in such cases you should use the SetInternal method instead. |
| `MaxValue` | `T` | get, set | The max value of the convar. <exception cref="InvalidOperationException">Thrown when the convar is not a min/max type or doesn't have a max value.</exception> |
| `MinValue` | `T` | get, set | The min value of the convar. <exception cref="InvalidOperationException">Thrown when the convar is not a min/max type or doesn't have a min value.</exception> |
| `DefaultValue` | `T` | get, set | The default value of the convar. |
| `HasDefaultValue` | `bool` | get | Whether the convar has a default value. |
| `HasMinValue` | `bool` | get | Whether the convar has a min value. |
| `HasMaxValue` | `bool` | get, set | Whether the convar has a max value. |
| `Flags` | `ConvarFlags` | get, set | The flags of the convar. |

