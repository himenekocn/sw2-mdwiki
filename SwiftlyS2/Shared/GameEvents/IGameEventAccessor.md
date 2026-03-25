# 🔌 IGameEventAccessor

一个用于访问原生 IGameEvent 的通用访问器。

**命名空间:** `SwiftlyS2.Shared.GameEvents`

**类型:** `interface`

**继承:** `INativeHandle`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DontBroadcast` | `bool` | get, set | 当为 true 时，事件将不会向客户端广播。 |

## ⚙️ 方法

### SetBool

```csharp
void SetBool(string key, bool value)
```

设置事件负载中的布尔字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`bool`) - 布尔值。

**用法示例:**
```csharp
gameEventAccessor.SetBool("is_active", true);
```

### GetBool

```csharp
bool GetBool(string key)
```

从事件负载中获取布尔字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `bool` - 布尔值。

**用法示例:**
```csharp
bool isActive = eventAccessor.GetBool("is_active");
```

### SetInt32

```csharp
void SetInt32(string key, int value)
```

在事件载荷上设置一个整型字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`int`) - 整数值。

**用法示例:**
```csharp
eventAccessor.SetInt32("score", 100);
```

### GetInt32

```csharp
int GetInt32(string key)
```

从事件负载中获取整数字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 整数值。

**用法示例:**
```csharp
int score = gameEventAccessor.GetInt32("score");
```

### SetUInt64

```csharp
void SetUInt64(string key, ulong value)
```

设置事件负载中的无符号 64 位整数字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`ulong`) - 无符号 64 位数值。

**用法示例:**
```csharp
accessor.SetUInt64("score", 1000UL);
```

### GetUInt64

```csharp
ulong GetUInt64(string key)
```

从事件负载中获取一个无符号 64 位整数字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `ulong` - 无符号 64 位数值。

**用法示例:**
```csharp
ulong value = eventAccessor.GetUInt64("player_id");
```

### SetFloat

```csharp
void SetFloat(string key, float value)
```

在事件负载上设置一个浮点数字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`float`) - 浮点数值。

**用法示例:**
```csharp
eventAccessor.SetFloat("damage", 12.5f);
```

### GetFloat

```csharp
float GetFloat(string key)
```

从事件载荷中获取浮点数字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `float` - 浮点数值。

**用法示例:**
```csharp
float value = gameEventAccessor.GetFloat("damage");
```

### SetString

```csharp
void SetString(string key, string value)
```

在事件负载中设置字符串字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`string`) - 字符串值。

**用法示例:**
```csharp
gameEventAccessor.SetString("reason", "player_disconnect");
```

### GetString

```csharp
string GetString(string key)
```

从事件负载中获取字符串字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `string` - 字符串值。

**用法示例:**
```csharp
string value = eventAccessor.GetString("message");
```

### SetEntity<K>

```csharp
void SetEntity<K>(string key, K value)
```

在事件负载中设置实体引用。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`K`) - 实体实例。

**用法示例:**
```csharp
gameEventAccessor.SetEntity("attacker", player);
```

### GetEntity<K>

```csharp
K GetEntity<K>(string key)
```

从事件负载中获取实体引用。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `K` - 实体实例。

**用法示例:**
```csharp
var player = gameEventAccessor.GetEntity<CCSPlayerController>("userid");
```

### SetEntityIndex

```csharp
void SetEntityIndex(string key, int value)
```

在事件负载中设置实体索引字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`int`) - 实体索引。

**用法示例:**
```csharp
gameEventAccessor.SetEntityIndex("userid", 5);
```

### GetEntityIndex

```csharp
int GetEntityIndex(string key)
```

从事件载荷中获取实体索引字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 实体索引。

**用法示例:**
```csharp
int entityIndex = gameEventAccessor.GetEntityIndex("userid");
```

### SetPlayerSlot

```csharp
void SetPlayerSlot(string key, int value)
```

在事件负载中设置玩家槽位字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`int`) - 玩家槽位。

**用法示例:**
```csharp
gameEventAccessor.SetPlayerSlot("userid", 5);
```

### GetPlayerSlot

```csharp
int GetPlayerSlot(string key)
```

从事件负载中获取玩家槽字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 玩家槽位。

**用法示例:**
```csharp
int slot = accessor.GetPlayerSlot("userid");
```

### GetPlayerController

```csharp
CCSPlayerController GetPlayerController(string key)
```

获取由给定字段引用的玩家控制器。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `CCSPlayerController` - 玩家控制器。

**用法示例:**
```csharp
var controller = accessor.GetPlayerController("Player1");
```

### GetPlayerPawn

```csharp
CCSPlayerPawn GetPlayerPawn(string key)
```

获取由给定字段引用的玩家Pawn。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `CCSPlayerPawn` - 玩家模型。

**用法示例:**
```csharp
CCSPlayerPawn pawn = gameEventAccessor.GetPlayerPawn("userid");
```

### GetPlayer

```csharp
IPlayer? GetPlayer(string key)
```

获取由给定字段引用的玩家。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `IPlayer?` - 玩家。

**用法示例:**
```csharp
IPlayer? player = accessor.GetPlayer("userid");
```

### SetPtr

```csharp
void SetPtr(string key, nint value)
```

在事件负载中设置原始指针值。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`nint`) - 指针值。

**用法示例:**
```csharp
accessor.SetPtr("entity_ptr", entityHandle);
```

### GetPtr

```csharp
nint GetPtr(string key)
```

从事件载荷中获取原始指针值。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `nint` - 指针值。

**用法示例:**
```csharp
nint ptr = eventAccessor.GetPtr("entity_pointer");
```

### GetPawnEntityIndex

```csharp
int GetPawnEntityIndex(string key)
```

获取由给定字段引用的棋子实体索引。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - Pawn 实体索引。

**用法示例:**
```csharp
int pawnIndex = gameEventAccessor.GetPawnEntityIndex("player_pawn");
```

### IsReliable

```csharp
bool IsReliable()
```

指示该事件是否被标记为可靠。

**返回值:** `bool` - 若为可靠数据则为真。

**用法示例:**
```csharp
bool isReliable = gameEventAccessor.IsReliable();
```

### IsLocal

```csharp
bool IsLocal()
```

指示该事件是否仅针对此服务器/客户端。

**返回值:** `bool` - 当为本地时返回 true。

**用法示例:**
```csharp
bool isLocal = gameEventAccessor.IsLocal();
```

