<a id="steamipaddress_t"></a>

# 🏗️ SteamIPAddress_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## ⚙️ 方法

### ToIPAddress

```csharp
System.Net.IPAddress ToIPAddress()
```

**返回值:** `System.Net.IPAddress`

**用法示例:**
```csharp
System.Net.IPAddress ip = steamIPAddress.ToIPAddress();
```

### ToString

```csharp
string ToString()
```

**返回值:** `string`

### GetIPType

```csharp
ESteamIPType GetIPType()
```

**返回值:** `ESteamIPType`

**用法示例:**
```csharp
ESteamIPType type = instance.GetIPType();
```

### IsSet

```csharp
bool IsSet()
```

**返回值:** `bool`

**用法示例:**
```csharp
bool isSet = steamIpAddress.IsSet();
```

