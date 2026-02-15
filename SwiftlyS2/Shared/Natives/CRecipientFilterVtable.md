# 📦 CRecipientFilterVtable

**命名空间:** `SwiftlyS2.Shared.Natives`

**类型:** `class`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `pCRecipientFilterVTable` | `nint` | static | - |

## ⚙️ 方法

### Destructor (静态)

```csharp
void Destructor(CRecipientFilter* filter)
```

**参数:**

- `filter` (`CRecipientFilter*`)

### GetNetworkBufType (静态)

```csharp
NetChannelBufType_t GetNetworkBufType(CRecipientFilter* filter)
```

**参数:**

- `filter` (`CRecipientFilter*`)

**返回值:** `NetChannelBufType_t`

### IsInitMessage (静态)

```csharp
bool IsInitMessage(CRecipientFilter* filter)
```

**参数:**

- `filter` (`CRecipientFilter*`)

**返回值:** `bool`

### GetRecipients (静态)

```csharp
ulong* GetRecipients(CRecipientFilter* filter)
```

**参数:**

- `filter` (`CRecipientFilter*`)

**返回值:** `ulong*`

### GetPredictedSlotWindows (静态)

```csharp
int* GetPredictedSlotWindows(CRecipientFilter* filter, int* pPlayerSlot)
```

**参数:**

- `filter` (`CRecipientFilter*`)
- `pPlayerSlot` (`int*`)

**返回值:** `int*`

### GetPredictedSlotLinux (静态)

```csharp
int GetPredictedSlotLinux(CRecipientFilter* filter)
```

**参数:**

- `filter` (`CRecipientFilter*`)

**返回值:** `int`

