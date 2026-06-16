<a id="igameeventaccessor"></a>

# 🔌 IGameEventAccessor

对原生IGameEvent的通用访问器。

**命名空间:** `SwiftlyS2.Shared.GameEvents`

**类型:** `interface`

**继承:** `INativeHandle`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DontBroadcast` | `bool` | get, set | 当此值为真时，事件将不会广播给客户端。 |

## ⚙️ 方法

### SetBool

```csharp
void SetBool(string key, bool value)
```

在事件负载上设置一个布尔字段。

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

从事件负载中获取一个布尔字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `bool` - 布尔值。

**用法示例:**
```csharp
bool value = eventAccessor.GetBool("is_active");
```

### SetInt32

```csharp
void SetInt32(string key, int value)
```

在事件负载上设置一个整数字段。

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

从事件载荷中获取一个整数字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 整数值。

**用法示例:**
```csharp
int value = eventAccessor.GetInt32("userid");
```

### SetUInt64

```csharp
void SetUInt64(string key, ulong value)
```

在事件负载上设置一个无符号64位整数字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`ulong`) - 无符号64位值。

**用法示例:**
```csharp
eventAccessor.SetUInt64("score", 1000UL);
```

### GetUInt64

```csharp
ulong GetUInt64(string key)
```

从事件负载中获取一个无符号64位整数字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `ulong` - 无符号64位值。

**用法示例:**
```csharp
ulong value = gameEventAccessor.GetUInt64("entity_id");
```

### SetFloat

```csharp
void SetFloat(string key, float value)
```

在事件载荷上设置一个浮点数字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`float`) - 浮点数值。

**用法示例:**
```csharp
gameEventAccessor.SetFloat("damage", 95.5f);
```

### GetFloat

```csharp
float GetFloat(string key)
```

从事件负载中获取一个浮点数字段。

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

在事件负载上设置一个字符串字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`string`) - 字符串值。

**用法示例:**
```csharp
eventAccessor.SetString("reason", "player_disconnect");
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
string value = gameEventAccessor.GetString("player_name");
```

### SetEntity<K>

```csharp
void SetEntity<K>(string key, K value)
```

在事件负载上设置一个实体引用。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`K`) - 实体实例。

**用法示例:**
```csharp
eventAccessor.SetEntity("attacker", player);
```

### GetEntity<K>

```csharp
K GetEntity<K>(string key)
```

从事件负载中获取一个实体引用。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `K` - 实体实例。

**用法示例:**
```csharp
var entity = eventAccessor.GetEntity<CBasePlayer>("userid");
```

### SetEntityIndex

```csharp
void SetEntityIndex(string key, int value)
```

在事件载荷上设置一个实体索引字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`int`) - 实体索引。

**用法示例:**
```csharp
eventAccessor.SetEntityIndex("userid", 1);
```

### GetEntityIndex

```csharp
int GetEntityIndex(string key)
```

从事件负载中获取实体索引字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 实体索引。

**用法示例:**
```csharp
int index = eventAccessor.GetEntityIndex("userid");
```

### SetPlayerSlot

```csharp
void SetPlayerSlot(string key, int value)
```

在事件负载上设置一个玩家槽位字段。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`int`) - 玩家槽位。

**用法示例:**
```csharp
eventAccessor.SetPlayerSlot("player", 1);
```

### GetPlayerSlot

```csharp
int GetPlayerSlot(string key)
```

从事件负载中获取玩家槽位字段。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 玩家槽位。

**用法示例:**
```csharp
int slot = eventAccessor.GetPlayerSlot("userid");
```

### GetPlayerController

```csharp
CCSPlayerController GetPlayerController(string key)
```

获取指定字段引用的玩家控制器。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `CCSPlayerController` - 玩家控制器。

**用法示例:**
```csharp
var player = gameEventAccessor.GetPlayerController("userid");
```

### GetPlayerPawn

```csharp
CCSPlayerPawn GetPlayerPawn(string key)
```

获取指定字段引用的玩家Pawn。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `CCSPlayerPawn` - 玩家棋子。

**用法示例:**
```csharp
var pawn = gameEventAccessor.GetPlayerPawn("userid");
```

### GetPlayer

```csharp
IPlayer? GetPlayer(string key)
```

获取由给定字段引用的玩家。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `IPlayer?` - 玩家.

**用法示例:**
```csharp
IPlayer? player = eventAccessor.GetPlayer("userid");
```

### SetPtr

```csharp
void SetPtr(string key, nint value)
```

在事件负载上设置一个原始指针值。

**参数:**

- `key` (`string`) - 字段名称。
- `value` (`nint`) - 指针值。

**用法示例:**
```csharp
gameEventAccessor.SetPtr("player_ptr", player.Handle);
```

### GetPtr

```csharp
nint GetPtr(string key)
```

从事件负载中获取原始指针值。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `nint` - 指针值。

**用法示例:**
```csharp
nint ptr = gameEventAccessor.GetPtr("entity_ptr");
```

### GetPawnEntityIndex

```csharp
int GetPawnEntityIndex(string key)
```

获取由给定字段引用的棋子实体索引。

**参数:**

- `key` (`string`) - 字段名称。

**返回值:** `int` - 棋子实体索引

**用法示例:**
```csharp
int pawnIndex = gameEventAccessor.GetPawnEntityIndex("player");
```

### IsReliable

```csharp
bool IsReliable()
```

指示事件是否被标记为可靠。

**返回值:** `bool` - 如果可靠则为真。

**用法示例:**
```csharp
bool isReliable = eventAccessor.IsReliable();
```

### IsLocal

```csharp
bool IsLocal()
```

指示事件是否局限于当前服务器/客户端。

**返回值:** `bool` - 如果本地则为真。

**用法示例:**
```csharp
bool isLocal = eventAccessor.IsLocal();
```

