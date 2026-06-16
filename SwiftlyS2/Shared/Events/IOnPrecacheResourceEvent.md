<a id="ionprecacheresourceevent"></a>

# 🔌 IOnPrecacheResourceEvent

**命名空间:** `SwiftlyS2.Shared.Events`

**类型:** `interface`

## ⚙️ 方法

### AddItem

```csharp
void AddItem(string path)
```

将资源添加到预缓存列表中。

**参数:**

- `path` (`string`) - 要预缓存资源的路径。

**用法示例:**
```csharp
precacher.AddItem("models/props/de_dust2/barrel.vmdl");
```

