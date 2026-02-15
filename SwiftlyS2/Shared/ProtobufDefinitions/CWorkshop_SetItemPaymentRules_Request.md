# 🔌 CWorkshop_SetItemPaymentRules_Request

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CWorkshop_SetItemPaymentRules_Request\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Appid` | `uint` | get, set | - |
| `Gameitemid` | `uint` | get, set | - |
| `AssociatedWorkshopFiles` | `IProtobufRepeatedFieldSubMessageType\<CWorkshop_SetItemPaymentRules_Request_WorkshopItemPaymentRule\>` | get | - |
| `PartnerAccounts` | `IProtobufRepeatedFieldSubMessageType\<CWorkshop_SetItemPaymentRules_Request_PartnerItemPaymentRule\>` | get, set | - |
| `ValidateOnly` | `bool` | get, set | - |
| `MakeWorkshopFilesSubscribable` | `bool` | get, set | - |
| `AssociatedWorkshopFileForDirectPayments` | `CWorkshop_SetItemPaymentRules_Request_WorkshopDirectPaymentRule` | get | - |

