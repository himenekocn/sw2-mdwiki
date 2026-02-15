# 🔌 CMsgClientWelcome

**命名空间:** `SwiftlyS2.Shared.ProtobufDefinitions`

**类型:** `interface`

**继承:** `ITypedProtobuf\<CMsgClientWelcome\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `Version` | `uint` | get, set | - |
| `GameData` | `byte[]` | get, set | - |
| `OutofdateSubscribedCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscribed\>` | get | - |
| `UptodateSubscribedCaches` | `IProtobufRepeatedFieldSubMessageType\<CMsgSOCacheSubscriptionCheck\>` | get, set | - |
| `Location` | `CMsgClientWelcome_Location` | get, set | - |
| `GameData2` | `byte[]` | get, set | - |
| `Rtime32GcWelcomeTimestamp` | `uint` | get, set | - |
| `Currency` | `uint` | get, set | - |
| `Balance` | `uint` | get, set | - |
| `BalanceUrl` | `string` | get, set | - |
| `TxnCountryCode` | `string` | get, set | - |

