<a id="iplugin"></a>

# 🔌 IPlugin

**命名空间:** `SwiftlyS2.Shared.Plugins`

**类型:** `interface`

## ⚙️ 方法

### ConfigureSharedInterface

```csharp
void ConfigureSharedInterface(IInterfaceManager interfaceManager)
```

**参数:**

- `interfaceManager` (`IInterfaceManager`)

**用法示例:**
```csharp
plugin.ConfigureSharedInterface(interfaceManager);
```

### UseSharedInterface

```csharp
void UseSharedInterface(IInterfaceManager interfaceManager)
```

**参数:**

- `interfaceManager` (`IInterfaceManager`)

**用法示例:**
```csharp
plugin.UseSharedInterface(interfaceManager);
```

### OnSharedInterfaceInjected

```csharp
void OnSharedInterfaceInjected(IInterfaceManager interfaceManager)
```

**参数:**

- `interfaceManager` (`IInterfaceManager`)

**用法示例:**
```csharp
plugin.OnSharedInterfaceInjected(interfaceManager);
```

### OnAllPluginsLoaded

```csharp
void OnAllPluginsLoaded()
```

**用法示例:**
```csharp
plugin.OnAllPluginsLoaded();
```

### Load

```csharp
void Load(bool hotReload)
```

**参数:**

- `hotReload` (`bool`)

**用法示例:**
```csharp
plugin.Load(true);
```

### Unload

```csharp
void Unload()
```

**用法示例:**
```csharp
plugin.Unload();
```

