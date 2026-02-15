# 🔌 CEntityIdentity

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CEntityIdentity\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `NameStringableIndex` | `ref int` | get | - |
| `Name` | `string` | get, set | - |
| `DesignerName` | `string` | get, set | - |
| `Flags` | `ref uint` | get | - |
| `WorldGroupId` | `ref uint` | get | - |
| `DataObjectTypes` | `ref uint` | get | - |
| `PathIndex` | `ref ChangeAccessorFieldPathIndex_t` | get | - |
| `Attributes` | `CEntityAttributeTable?` | get | - |
| `Prev` | `CEntityIdentity?` | get | - |
| `Next` | `CEntityIdentity?` | get | - |
| `PrevByClass` | `CEntityIdentity?` | get | - |
| `NextByClass` | `CEntityIdentity?` | get | - |

## ⚙️ 方法

### NameStringableIndexUpdated

```csharp
void NameStringableIndexUpdated()
```

