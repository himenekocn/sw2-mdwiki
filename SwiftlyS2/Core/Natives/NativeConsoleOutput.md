# 📦 NativeConsoleOutput

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### AddConsoleListener (静态)

```csharp
ulong AddConsoleListener(nint callback)
```

callback should receive: string message

**参数:**

- `callback` (`nint`)

**返回值:** `ulong`

### RemoveConsoleListener (静态)

```csharp
void RemoveConsoleListener(ulong listenerId)
```

**参数:**

- `listenerId` (`ulong`)

### IsEnabled (静态)

```csharp
bool IsEnabled()
```

returns whether console filtering is enabled

**返回值:** `bool`

### ToggleFilter (静态)

```csharp
void ToggleFilter()
```

toggles the console filter on/off

### ReloadFilterConfiguration (静态)

```csharp
void ReloadFilterConfiguration()
```

reloads the filter configuration from file

### NeedsFiltering (静态)

```csharp
bool NeedsFiltering(string text)
```

checks if a message needs filtering

**参数:**

- `text` (`string`)

**返回值:** `bool`

### GetCounterText (静态)

```csharp
string GetCounterText()
```

gets the counter text showing how many messages were filtered

**返回值:** `string`

