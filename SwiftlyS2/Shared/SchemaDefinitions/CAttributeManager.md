# 🔌 CAttributeManager

**命名空间:** `SwiftlyS2.Shared.SchemaDefinitions`

**类型:** `interface`

**继承:** `ISchemaClass\<CAttributeManager\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Providers` | `ref CUtlVector\<CHandle\<CBaseEntity\>\>` | get | - |
| `ReapplyProvisionParity` | `ref int` | get | - |
| `Outer` | `ref CHandle\<CBaseEntity\>` | get | - |
| `PreventLoopback` | `ref bool` | get | - |
| `ProviderType` | `ref attributeprovidertypes_t` | get | - |
| `CachedResults` | `ref CUtlVector\<CAttributeManager__cached_attribute_float_t\>` | get | - |

## ⚙️ 方法

### ReapplyProvisionParityUpdated

```csharp
void ReapplyProvisionParityUpdated()
```

### OuterUpdated

```csharp
void OuterUpdated()
```

### ProviderTypeUpdated

```csharp
void ProviderTypeUpdated()
```

