<a id="friendsgroupid_t"></a>

# 🏗️ FriendsGroupID_t

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `struct`

**继承:** `System.IEquatable\<FriendsGroupID_t\>`

**实现接口:** `System.IComparable\<FriendsGroupID_t\>`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `m_FriendsGroupID` | `short` | - | - |

## ⚙️ 方法

### ToString

```csharp
string ToString()
```

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

### short (静态)

```csharp
operator short(FriendsGroupID_t that)
```

**参数:**

- `that` (`FriendsGroupID_t`)

**返回值:** `operator`

**用法示例:**
```csharp
short id = FriendsGroupID_t.short(existingFriendsGroupID);
```

### Equals

```csharp
bool Equals(FriendsGroupID_t other)
```

**参数:**

- `other` (`FriendsGroupID_t`)

**返回值:** `bool`

### CompareTo

```csharp
int CompareTo(FriendsGroupID_t other)
```

**参数:**

- `other` (`FriendsGroupID_t`)

**返回值:** `int`

**用法示例:**
```csharp
int result = myFriendsGroupID.CompareTo(otherFriendsGroupID);
```

