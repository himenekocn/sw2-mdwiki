<a id="takedamageentityparams"></a>

# 🏗️ TakeDamageEntityParams

**命名空间:** `SwiftlyS2.Shared.GameHooks`

**类型:** `struct`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `DamageResult` | `CTakeDamageResult*` | - | 可选的本地伤害结果。当调用者未提供结果对象时，它可能为 null。 |

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Info` | `ref CTakeDamageInfo` | - | 传递到原始函数的伤害信息。修改会写入原生内存。 |
| `DamageResult` | `CTakeDamageResult*` | - | 可选的本地伤害结果。当调用者未提供结果对象时，它可能为 null。 |

