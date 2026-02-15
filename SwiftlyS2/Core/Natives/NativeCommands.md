# 📦 NativeCommands

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### HandleCommandForPlayer (静态)

```csharp
int HandleCommandForPlayer(int playerid, string command)
```

1 -> not silent, 2 -> silent, -1 -> invalid player, 0 -> no command

**参数:**

- `playerid` (`int`)
- `command` (`string`)

**返回值:** `int`

### RegisterCommand (静态)

```csharp
ulong RegisterCommand(string commandName, nint callback, bool registerRaw, string helpText)
```

callback should receive (int32 playerid, string arguments_list (separated by \x01), string commandName, string prefix, bool silent), if registerRaw is false, it will not put "sw_" before the command name

**参数:**

- `commandName` (`string`)
- `callback` (`nint`)
- `registerRaw` (`bool`)
- `helpText` (`string`)

**返回值:** `ulong`

### UnregisterCommand (静态)

```csharp
void UnregisterCommand(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### IsCommandRegistered (静态)

```csharp
bool IsCommandRegistered(string commandName)
```

**参数:**

- `commandName` (`string`)

**返回值:** `bool`

### RegisterAlias (静态)

```csharp
ulong RegisterAlias(string aliasName, string commandName, bool registerRaw)
```

registerRaw behaves the same as on RegisterCommand, for commandName you need to also put the "sw_" prefix if the command is registered without raw mode

**参数:**

- `aliasName` (`string`)
- `commandName` (`string`)
- `registerRaw` (`bool`)

**返回值:** `ulong`

### UnregisterAlias (静态)

```csharp
void UnregisterAlias(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### RegisterClientCommandsListener (静态)

```csharp
ulong RegisterClientCommandsListener(nint callback)
```

callback should receive: int32 playerid, string commandline, return true -> ignored, return false -> supercede

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### UnregisterClientCommandsListener (静态)

```csharp
void UnregisterClientCommandsListener(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

### RegisterClientChatListener (静态)

```csharp
ulong RegisterClientChatListener(nint callback)
```

callback should receive: int32 playerid, string text, bool teamonly, return true -> ignored, return false -> supercede, when superceded it's not gonna send the message

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### UnregisterClientChatListener (静态)

```csharp
void UnregisterClientChatListener(ulong callbackID)
```

**参数:**

- `callbackID` (`ulong`)

