# 📦 BaseDatamapFunctionOperator

**命名空间:** `SwiftlyS2.Core.Datamaps`

**类型:** `class`

**继承:** `IDatamapFunctionOperator\<T`

**实现接口:** `K\>
    where T : ISchemaClass\<T\>
    where K : IDatamapFunctionHookContext\<T\>`, `new()`

## 📋 字段

| 名称 | 类型 | 修饰符 | 描述 |
|------|------|--------|------|
| `IsDisposed` | `bool` | - | - |

## ⚙️ 方法

### HookPre

```csharp
void HookPre(Action<K> callback)
```

**参数:**

- `callback` (`Action\<K\>`)

### HookPost

```csharp
void HookPost(Action<K> callback)
```

**参数:**

- `callback` (`Action\<K\>`)

### Invoke

```csharp
void Invoke(T schemaObject)
```

**参数:**

- `schemaObject` (`T`)

### InvokeOriginal

```csharp
void InvokeOriginal(T schemaObject)
```

**参数:**

- `schemaObject` (`T`)

### Dispose

```csharp
void Dispose()
```

