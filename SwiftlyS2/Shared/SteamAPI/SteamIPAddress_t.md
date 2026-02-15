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
SteamIPAddress_t ip;  
System.Net.IPAddress addr = ip.ToIPAddress();
```

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
SteamIPAddress_t ip = SteamNetworkingUtils.GetLocalIP();  
Console.WriteLine(ip.ToString());
```

### GetIPType

```csharp
ESteamIPType GetIPType()
```

**返回值:** `ESteamIPType`

**用法示例:**
```csharp
SteamIPAddress_t ip;  
ESteamIPType type = ip.GetIPType();
```

### IsSet

```csharp
bool IsSet()
```

**返回值:** `bool`

**用法示例:**
```csharp
SteamIPAddress_t addr;  
bool isSet = addr.IsSet();
```

