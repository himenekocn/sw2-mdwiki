# 📚 Datamaps

**命名空间:** `SwiftlyS2.Shared.Datamaps`

共 6 个定义

## 📋 目录

- 📦 [DatamapHookAttribute](#datamaphookattribute)
- 🔌 [IDatamapFunctionHookContext](#idatamapfunctionhookcontext)
- 🔌 [IDatamapFunctionHookContext&lt;T&gt;](#idatamapfunctionhookcontext-t)
- 🔌 [IDatamapFunctionService](#idatamapfunctionservice)
- 🔌 [IDatamapFunctionService](#idatamapfunctionservice)
- 🔌 [IDatamapService](#idatamapservice)

<a id="datamaphookattribute"></a>

## 📦 DatamapHook

**命名空间:** `SwiftlyS2.Shared.Datamaps`

**类型:** `class`

**用法:** `DatamapHook`

### 🏷️ 属性用法

#### 构造函数

```csharp
[DatamapHook(/* hookMode */)]
```

**参数:**

- `hookMode` (`HookMode`)



---

<a id="idatamapfunctionhookcontext"></a>

## 🔌 IDatamapFunctionHookContext

**命名空间:** `SwiftlyS2.Shared.Datamaps`

**类型:** `interface`



---

<a id="idatamapfunctionhookcontext-t"></a>

## 🔌 IDatamapFunctionHookContext&lt;T&gt;

**命名空间:** `SwiftlyS2.Shared.Datamaps`

**类型:** `interface`

**继承:** `IDatamapFunctionHookContext
    where T : ISchemaClass\<T\>`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `SchemaObject` | `T` | get, set | - |
| `HookResult` | `HookResult` | get, set | - |



---

<a id="idatamapfunctionservice"></a>

## 🔌 IDatamapFunctionService

**命名空间:** `SwiftlyS2.Shared.Datamaps`

**类型:** `interface`



---

<a id="idatamapfunctionservice"></a>

## 🔌 IDatamapFunctionService

**命名空间:** `SwiftlyS2.Shared.Datamaps`

**类型:** `interface`



---

<a id="idatamapservice"></a>

## 🔌 IDatamapService

**命名空间:** `SwiftlyS2.Shared.Datamaps`

**类型:** `interface`

### 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `Functions` | `IDatamapFunctionService` | get | - |



---

