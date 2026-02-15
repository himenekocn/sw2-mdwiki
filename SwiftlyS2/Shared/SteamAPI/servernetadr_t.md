# 🏗️ servernetadr_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

## ⚙️ 方法

### Init

```csharp
void Init(uint ip, ushort usQueryPort, ushort usConnectionPort)
```

**参数:**

- `ip` (`uint`)
- `usQueryPort` (`ushort`)
- `usConnectionPort` (`ushort`)

**用法示例:**
```csharp
servernetadr_t addr;
addr.Init(0x7F000001, 27015, 27015);
```

### GetIPAndQueryPort

```csharp
netadr_t GetIPAndQueryPort()
```

**返回值:** `netadr_t`

**用法示例:**
```csharp
netadr_t ipAndQueryPort = serverNetAdr.GetIPAndQueryPort();
```

### GetQueryPort

```csharp
ushort GetQueryPort()
```

**返回值:** `ushort`

**用法示例:**
```csharp
ushort port = serverNetAdr.GetQueryPort();
```

### SetQueryPort

```csharp
void SetQueryPort(ushort usPort)
```

**参数:**

- `usPort` (`ushort`)

**用法示例:**
```csharp
servernetadr_t adr;  
adr.SetQueryPort(27015);
```

### GetConnectionPort

```csharp
ushort GetConnectionPort()
```

**返回值:** `ushort`

**用法示例:**
```csharp
ushort port = serverNetAdr.GetConnectionPort();
```

### SetConnectionPort

```csharp
void SetConnectionPort(ushort usPort)
```

**参数:**

- `usPort` (`ushort`)

**用法示例:**
```csharp
servernetadr_t adr;  
adr.SetConnectionPort(27015);
```

### GetIP

```csharp
uint GetIP()
```

**返回值:** `uint`

**用法示例:**
```csharp
uint ip = serverNetAdr.GetIP();
```

### SetIP

```csharp
void SetIP(uint unIP)
```

**参数:**

- `unIP` (`uint`)

**用法示例:**
```csharp
servernetadr_t adr;  
adr.SetIP(0x7F000001);
```

### GetConnectionAddressString

```csharp
string GetConnectionAddressString()
```

**返回值:** `string`

**用法示例:**
```csharp
string addr = serverNetAdr.GetConnectionAddressString();
```

### GetQueryAddressString

```csharp
string GetQueryAddressString()
```

**返回值:** `string`

**用法示例:**
```csharp
string queryAddr = serverNetAdr.GetQueryAddressString();
```

### ToString (静态)

```csharp
string ToString(uint unIP, ushort usPort)
```

**参数:**

- `unIP` (`uint`)
- `usPort` (`ushort`)

**返回值:** `string`

**用法示例:**
```csharp
string addr = servernetadr_t.ToString(0x7F000001, 8080);
```

### Equals

```csharp
bool Equals(object other)
```

**参数:**

- `other` (`object`)

**返回值:** `bool`

### GetHashCode

```csharp
int GetHashCode()
```

**返回值:** `int`

### Equals

```csharp
bool Equals(servernetadr_t other)
```

**参数:**

- `other` (`servernetadr_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(servernetadr_t other)
```

**参数:**

- `other` (`servernetadr_t`)

**返回值:** `int`

**用法示例:**
```csharp
servernetadr_t a = default; servernetadr_t b = default; int result = a.CompareTo(b);
```

