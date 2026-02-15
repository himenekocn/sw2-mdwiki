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

### GetIPAndQueryPort

```csharp
netadr_t GetIPAndQueryPort()
```

**返回值:** `netadr_t`

### GetQueryPort

```csharp
ushort GetQueryPort()
```

**返回值:** `ushort`

### SetQueryPort

```csharp
void SetQueryPort(ushort usPort)
```

**参数:**

- `usPort` (`ushort`)

### GetConnectionPort

```csharp
ushort GetConnectionPort()
```

**返回值:** `ushort`

### SetConnectionPort

```csharp
void SetConnectionPort(ushort usPort)
```

**参数:**

- `usPort` (`ushort`)

### GetIP

```csharp
uint GetIP()
```

**返回值:** `uint`

### SetIP

```csharp
void SetIP(uint unIP)
```

**参数:**

- `unIP` (`uint`)

### GetConnectionAddressString

```csharp
string GetConnectionAddressString()
```

**返回值:** `string`

### GetQueryAddressString

```csharp
string GetQueryAddressString()
```

**返回值:** `string`

### ToString (静态)

```csharp
string ToString(uint unIP, ushort usPort)
```

**参数:**

- `unIP` (`uint`)
- `usPort` (`ushort`)

**返回值:** `string`

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

