# 📦 BasePlugin

**命名空间:** `SwiftlyS2.Shared.Plugins`

**类型:** `class`

**继承:** `IPlugin`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `ReloadMethod` | `PluginReloadMethod` | get, set | - |

## ⚙️ 方法

### ConfigureSharedInterface

```csharp
void ConfigureSharedInterface(IInterfaceManager interfaceManager)
```

**参数:**

- `interfaceManager` (`IInterfaceManager`)

**注意:** 此方法是虚方法，需要在子类中重写 (override)。

### UseSharedInterface

```csharp
void UseSharedInterface(IInterfaceManager interfaceManager)
```

**参数:**

- `interfaceManager` (`IInterfaceManager`)

**注意:** 此方法是虚方法，需要在子类中重写 (override)。

### OnSharedInterfaceInjected

```csharp
void OnSharedInterfaceInjected(IInterfaceManager interfaceManager)
```

**参数:**

- `interfaceManager` (`IInterfaceManager`)

**注意:** 此方法是虚方法，需要在子类中重写 (override)。

### OnAllPluginsLoaded

```csharp
void OnAllPluginsLoaded()
```

**注意:** 此方法是虚方法，需要在子类中重写 (override)。

### Load

```csharp
void Load(bool hotReload)
```

**参数:**

- `hotReload` (`bool`)

**用法示例:**
```csharp
basePlugin.Load(false);
// 或 hotReload = true;
// basePlugin.Load(hotReload);
```

### Unload

```csharp
void Unload()
```

**用法示例:**
```csharp
plugin.Unload();
```

