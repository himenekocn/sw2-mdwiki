# 🔌 IGameEventAccessor

对原生 IGameEvent 的泛型访问器。

**命名空间:** `SwiftlyS2.Shared.GameEvents`

**类型:** `interface`

**继承:** `INativeHandle`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `DontBroadcast` | `bool` | get, set | 当此值为 true 时，事件将不会广播到客户端。 |

## ⚙️ 方法

### SetBool

```csharp
void SetBool(string key, bool value)
```

在事件负载上设置一个布尔字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`bool`) - 布尔值。

**用法示例:**
```csharp
gameEventAccessor.SetBool("isReady", true);
```

### GetBool

```csharp
bool GetBool(string key)
```

从事件负载中获取一个布尔字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `bool` - 布尔值。

**用法示例:**
```csharp
bool isReady = gameEventAccessor.GetBool("isReady");
```

### SetInt32

```csharp
void SetInt32(string key, int value)
```

在事件负载上设置一个整数字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`int`) - 整数类型的值。

**用法示例:**
```csharp
gameEventAccessor.SetInt32("score", 100);
```

### GetInt32

```csharp
int GetInt32(string key)
```

从事件负载中获取一个整数字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `int` - 整数类型的值。

**用法示例:**
```csharp
int score = gameEvent.GetInt32("score");
```

### SetUInt64

```csharp
void SetUInt64(string key, ulong value)
```

在事件负载上设置一个无符号64位整数字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`ulong`) - 无符号64位值。

**用法示例:**
```csharp
gameEventAccessor.SetUInt64("score", 100UL);
```

### GetUInt64

```csharp
ulong GetUInt64(string key)
```

从事件负载中获取一个无符号64位整数字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `ulong` - 无符号64位值。

**用法示例:**
```csharp
ulong score = gameEventAccessor.GetUInt64("score");
```

### SetFloat

```csharp
void SetFloat(string key, float value)
```

在事件负载上设置一个浮点数字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`float`) - 浮点值。

**用法示例:**
```csharp
gameEventAccessor.SetFloat("health", 100f);
```

### GetFloat

```csharp
float GetFloat(string key)
```

从事件负载中获取一个浮点字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `float` - 浮点值。

**用法示例:**
```csharp
float value = gameEventAccessor.GetFloat("health");
```

### SetString

```csharp
void SetString(string key, string value)
```

在事件负载上设置一个字符串字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`string`) - 字符串值。

**用法示例:**
```csharp
gameEventAccessor.SetString("playerName", "Alice");
```

### GetString

```csharp
string GetString(string key)
```

从事件负载中获取一个字符串字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `string` - 字符串值。

**用法示例:**
```csharp
string value = gameEventAccessor.GetString("playerName");
```

### SetEntityIndex

```csharp
void SetEntityIndex(string key, int value)
```

在事件负载上设置一个实体索引字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`int`) - 实体索引。

**用法示例:**
```csharp
gameEventAccessor.SetEntityIndex("killer", 42);
```

### GetEntityIndex

```csharp
int GetEntityIndex(string key)
```

从事件负载中获取实体索引字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `int` - 实体索引。

**用法示例:**
```csharp
int index = gameEventAccessor.GetEntityIndex("player");
```

### SetPlayerSlot

```csharp
void SetPlayerSlot(string key, int value)
```

在事件负载上设置玩家槽位字段。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`int`) - 玩家槽位。

**用法示例:**
```csharp
gameEventAccessor.SetPlayerSlot("slot1", 3);
```

### GetPlayerSlot

```csharp
int GetPlayerSlot(string key)
```

从事件负载中获取玩家槽位字段。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `int` - 玩家槽位。

**用法示例:**
```csharp
int slot = gameEventAccessor.GetPlayerSlot("player_slot");
```

### GetPlayerController

```csharp
CCSPlayerController GetPlayerController(string key)
```

获取由给定字段引用的玩家控制器。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `CCSPlayerController` - 玩家控制器。

**用法示例:**
```csharp
IGameEventAccessor accessor = ...; // 假设已存在实例  
CCSPlayerController controller = accessor.GetPlayerController("player1");
```

### GetPlayerPawn

```csharp
CCSPlayerPawn GetPlayerPawn(string key)
```

获取由给定字段引用的玩家Pawn。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `CCSPlayerPawn` - 玩家Pawn。

**用法示例:**
```csharp
IGameEventAccessor accessor = GameEvents.GetAccessor();  
CCSPlayerPawn pawn = accessor.GetPlayerPawn("player1");
```

### GetPlayer

```csharp
IPlayer? GetPlayer(string key)
```

获取由给定字段引用的玩家。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `IPlayer?` - 玩家。

**用法示例:**
```csharp
IPlayer? player = gameEventAccessor.GetPlayer("player1");
```

### SetPtr

```csharp
void SetPtr(string key, nint value)
```

在事件负载上设置原始指针值。

**参数:**

- `key` (`string`) - 字段名。
- `value` (`nint`) - 指针值。

**用法示例:**
```csharp
gameEventAccessor.SetPtr("playerPointer", (nint)player);
```

### GetPtr

```csharp
nint GetPtr(string key)
```

从事件负载中获取原始指针值。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `nint` - 指针值。

**用法示例:**
```csharp
nint ptr = gameEventAccessor.GetPtr("playerPosition");
```

### GetPawnEntityIndex

```csharp
int GetPawnEntityIndex(string key)
```

获取由给定字段引用的兵卒实体索引。

**参数:**

- `key` (`string`) - 字段名。

**返回值:** `int` - Pawn实体索引。

**用法示例:**
```csharp
int index = gameEventAccessor.GetPawnEntityIndex("pawn1");
```

### IsReliable

```csharp
bool IsReliable()
```

指示事件是否被标记为可靠。

**返回值:** `bool` - 如果可靠，则为 true。

**用法示例:**
```csharp
bool reliable = gameEventAccessor.IsReliable();
```

### IsLocal

```csharp
bool IsLocal()
```

指示事件是否仅限于本服务器/客户端。

**返回值:** `bool` - 如果为本地，则为 true。

**用法示例:**
```csharp
bool isLocal = gameEventAccessor.IsLocal();
```

