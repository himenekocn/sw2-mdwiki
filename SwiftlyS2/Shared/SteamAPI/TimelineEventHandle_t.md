# 🏗️ TimelineEventHandle_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<TimelineEventHandle_t\>`

**实现接口:** `System.IComparable\<TimelineEventHandle_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_TimelineEventHandle` | `ulong` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

**返回值:** `string`

**用法示例:**
```csharp
string result = TimelineEventHandle_t.SomeExistingInstance.ToString();
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

### ulong (静态)

```csharp
operator ulong(TimelineEventHandle_t that)
```

**参数:**

- `that` (`TimelineEventHandle_t`)

**返回值:** `operator`

**用法示例:**
```csharp
TimelineEventHandle_t eventHandle = TimelineEventHandle_t.SomeExistingValue;
ulong id = (ulong)eventHandle;
```

### Equals

```csharp
bool Equals(TimelineEventHandle_t other)
```

**参数:**

- `other` (`TimelineEventHandle_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(TimelineEventHandle_t other)
```

**参数:**

- `other` (`TimelineEventHandle_t`)

**返回值:** `int`

**用法示例:**
```csharp
TimelineEventHandle_t handle1 = TimelineEventHandle_t.Default;  
int result = handle1.CompareTo(handle2);
```

