<a id="steamgameserverinventory"></a>

# 📦 SteamGameServerInventory

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetResultStatus (静态)

```csharp
EResult GetResultStatus(SteamInventoryResult_t resultHandle)
```

<para> 库存异步结果管理</para> <para> 异步库存查询始终会输出一个结果句柄，该句柄可用于</para> <para> GetResultStatus、GetResultItems 等。当异步结果准备就绪（或失败）时，将触发</para> <para> SteamInventoryResultReady_t 回调。</para> <para> 查询异步库存结果句柄的状态。可能的值：</para> <para> k_EResultPending - 仍在处理中</para> <para> k_EResultOK - 已完成，结果就绪</para> <para> k_EResultExpired - 已完成，结果就绪，但可能已过期（参见 DeserializeResult）</para> <para> k_EResultInvalidParam - 错误：无效的 API 调用参数</para> <para> k_EResultServiceUnavailable - 错误：服务暂时不可用，可稍后重试</para> <para> k_EResultLimitExceeded - 错误：操作将超出每个用户的库存限制</para> <para> k_EResultFail - 错误：未知/通用错误</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult status = SteamGameServerInventory.GetResultStatus(resultHandle);
```

### GetResultItems (静态)

```csharp
bool GetResultItems(SteamInventoryResult_t resultHandle, SteamItemDetails_t[] pOutItemsArray, ref uint punOutItemsArraySize)
```

<para> 将结果集的内容复制到平面数组中。结果集的</para> <para> 具体内容取决于所使用的查询。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `pOutItemsArray` (`SteamItemDetails_t[]`)
- `punOutItemsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamItemDetails_t[] items = new SteamItemDetails_t[10];
uint count = 10;
bool success = SteamGameServerInventory.GetResultItems(resultHandle, items, ref count);
```

### GetResultItemProperty (静态)

```csharp
bool GetResultItemProperty(SteamInventoryResult_t resultHandle, uint unItemIndex, string pchPropertyName, out string pchValueBuffer, ref uint punValueBufferSizeOut)
```

<para> 结合 GetResultItems 使用时，可通过 GetResultItemProperty 获取结果集中指定项目返回的动态字符串属性。</para>
<para> 属性名称始终由 ASCII 字母、数字和/或下划线组成。</para>
<para> 将 pchPropertyName 参数传递为 NULL 指针可获取以逗号分隔的可用属性名称列表。</para>
<para> 若 pchValueBuffer 为 NULL，则 *punValueBufferSize 将包含建议的缓冲区大小；否则其值为实际复制到 pchValueBuffer 的字节数。若结果数据超出给定缓冲区容量，可能仅复制部分结果。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `unItemIndex` (`uint`)
- `pchPropertyName` (`string`)
- `pchValueBuffer` (`out string`)
- `punValueBufferSizeOut` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bufferSize = 256; string value; SteamGameServerInventory.GetResultItemProperty(resultHandle, 0, "name", out value, ref bufferSize);
```

### GetResultTimestamp (静态)

```csharp
uint GetResultTimestamp(SteamInventoryResult_t resultHandle)
```

<para> 返回生成结果时的服务器时间。将其与</para> <para> IClientUtils::GetServerRealTime() 的值进行比较以确定时效。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**返回值:** `uint`

**用法示例:**
```csharp
uint timestamp = SteamGameServerInventory.GetResultTimestamp(resultHandle);
bool isExpired = (SteamClientUtils.GetServerRealTime() - timestamp) > 300;
```

### CheckResultSteamID (静态)

```csharp
bool CheckResultSteamID(SteamInventoryResult_t resultHandle, CSteamID steamIDExpected)
```

<para> 如果结果属于目标Steam ID则返回True，否则返回False。</para> <para> 在使用DeserializeResult时，此方法至关重要，可用于验证</para> <para> 远程玩家是否未冒充其他用户的库存。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `steamIDExpected` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = SteamGameServerInventory.CheckResultSteamID(resultHandle, remotePlayerSteamID);
```

### DestroyResult (静态)

```csharp
void DestroyResult(SteamInventoryResult_t resultHandle)
```

<para>销毁结果句柄并释放所有关联内存。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle = SteamGameServerInventory.GetResultByIndex(0);
SteamGameServerInventory.DestroyResult(resultHandle);
```

### GetAllItems (静态)

```csharp
bool GetAllItems(out SteamInventoryResult_t pResultHandle)
```

<para> 库存异步查询</para>
<para> 捕获当前用户 Steam 库存的完整状态。</para>
<para> 当您不再需要此句柄时，必须对其调用 DestroyResult。</para>
<para> 如果库存不可用，则返回 false 并将 *pResultHandle 设置为零。</para>
<para> 注意：对此函数的调用受速率限制，若过于频繁调用可能会返回缓存结果。</para>
<para> 建议仅在您即将显示用户的完整库存时，</para>
<para> 或预计库存可能已发生变化时调用此函数。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.GetAllItems(out resultHandle);
```

### GetItemsByID (静态)

```csharp
bool GetItemsByID(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t[] pInstanceIDs, uint unCountInstanceIDs)
```

<para> 捕获当前用户Steam库存子集的状态，</para> <para> 由一组物品实例ID标识。此调用的结果</para> <para> 可被序列化并传递给其他玩家，以"证明"当前</para> <para> 用户拥有特定物品，而无需暴露用户的全部库存。</para> <para> 例如，您可以使用用户当前装备的装饰物品的ID</para> <para> 调用GetItemsByID，并将其序列化到缓冲区中，</para> <para> 然后在加入游戏时将这一缓冲区传输给其他玩家。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pInstanceIDs` (`SteamItemInstanceID_t[]`)
- `unCountInstanceIDs` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamItemInstanceID_t[] ids = new SteamItemInstanceID_t[1] { itemInstanceId };
bool success = SteamGameServerInventory.GetItemsByID(out SteamInventoryResult_t result, ids, 1);
```

### SerializeResult (静态)

```csharp
bool SerializeResult(SteamInventoryResult_t resultHandle, byte[] pOutBuffer, out uint punOutBufferSize)
```

<para>结果序列化与身份验证</para>
<para>序列化结果集包含一个简短签名，该签名无法被伪造</para>
<para>或在不同的游戏会话中重放。结果集可在本地客户端上序列化，</para>
<para>通过您的游戏网络传输给其他玩家，</para>
<para>并由远程玩家反序列化。这是一种防止</para>
<para>黑客谎称拥有稀有/高价值物品的安全方式。</para>
<para>将带有签名字节的结果序列化至输出缓冲区。若输出缓冲区</para>
<para>传入NULL，则通过punOutBufferSize获取所需大小。</para>
<para>序列化结果的大小取决于正在序列化的物品数量。</para>
<para>当安全传输物品给其他玩家时，建议</para>
<para>首先使用"GetItemsByID"创建最小结果集。</para>
<para>结果包含内置时间戳，该时间戳在一小时后将被视为"过期"。</para>
<para>过期处理请参见DeserializeResult。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `pOutBuffer` (`byte[]`)
- `punOutBufferSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bufferSize = 0; SteamGameServerInventory.SerializeResult(resultHandle, null, out bufferSize);
```

### DeserializeResult (静态)

```csharp
bool DeserializeResult(out SteamInventoryResult_t pOutResultHandle, byte[] pBuffer, uint unBufferSize, bool bRESERVED_MUST_BE_FALSE = false)
```

<para> 反序列化结果集并验证签名字节。如果设置了bRequireFullOnlineVerify但Steam以离线模式运行，则返回false。</para> <para> 否则返回true，并通过GetResultStatus传递错误代码。</para> <para> bRESERVED_MUST_BE_FALSE标志保留供将来使用，您的游戏此时不应将其设置为true。</para> <para> DeserializeResult存在一种潜在的软故障模式，即句柄状态被设置为k_EResultExpired。在此模式下，GetResultItems()仍然成功。</para> <para> “过期”结果可能表明数据可能已过时——不仅是因为定时过期（一小时），还因为结果集中的某个物品自结果集生成以来可能已被交易或消耗。您可以将GetResultTimestamp()的时间戳与ISteamUtils::GetServerRealTime()进行比较，以确定数据的陈旧程度。您可以简单地忽略“过期”结果代码并继续正常操作，也可以使用过期数据向玩家发起挑战，要求发送更新的结果集。</para>

**参数:**

- `pOutResultHandle` (`out SteamInventoryResult_t`)
- `pBuffer` (`byte[]`)
- `unBufferSize` (`uint`)
- `bRESERVED_MUST_BE_FALSE` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.DeserializeResult(out resultHandle, buffer, (uint)buffer.Length, false);
```

### GenerateItems (静态)

```csharp
bool GenerateItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayItemDefs, uint[] punArrayQuantity, uint unArrayLength)
```

<para> 库存异步修改</para>  
<para> GenerateItems() 创建一个或多个物品，然后生成一个带有匹配 nCallbackContext 参数的 SteamInventoryCallback_t 通知。此 API 仅用于原型设计——仅限属于您游戏发行商组的 Steam 帐户使用。</para>  
<para> 如果 punArrayQuantity 不为 NULL，则其长度应与 pArrayItems 相同，并应描述每个物品的生成数量。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `punArrayQuantity` (`uint[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle; SteamGameServerInventory.GenerateItems(out resultHandle, new SteamItemDef_t[] { (SteamItemDef_t)1001 }, new uint[] { 1 }, 1);
```

### GrantPromoItems (静态)

```csharp
bool GrantPromoItems(out SteamInventoryResult_t pResultHandle)
```

<para> GrantPromoItems() 检查用户可能符合资格的推广物品列表</para> <para> 并发放这些物品（仅一次）。成功时，结果集将包含已发放的物品，</para> <para> 如果有的话。如果因用户不符合任何推广资格而未发放物品，</para> <para> 这仍被视为成功。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.GrantPromoItems(out resultHandle);
```

### AddPromoItem (静态)

```csharp
bool AddPromoItem(out SteamInventoryResult_t pResultHandle, SteamItemDef_t itemDef)
```

<para>AddPromoItem() / AddPromoItems() 是 GrantPromoItems() 的受限版本。不同于</para> <para>扫描所有符合条件的促销物品，此检查仅限于单个物品</para> <para>定义或一组物品定义。如果您的游戏有自定义用户界面用于</para> <para>向用户展示特定促销物品，这将非常有用。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemDef` (`SteamItemDef_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.AddPromoItem(out resultHandle, new SteamItemDef_t(12345));
```

### AddPromoItems (静态)

```csharp
bool AddPromoItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayItemDefs, uint unArrayLength)
```

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamItemDef_t[] items = new SteamItemDef_t[] { (SteamItemDef_t)123 };
bool success = SteamGameServerInventory.AddPromoItems(out SteamInventoryResult_t result, items, 1);
```

### ConsumeItem (静态)

```csharp
bool ConsumeItem(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t itemConsume, uint unQuantity)
```

<para> ConsumeItem() 会从库存中永久移除物品，这些物品无法被恢复。</para> <para> 此操作非同小可——如果你的游戏实现了物品移除功能，强烈建议采用高摩擦力的UI确认流程。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemConsume` (`SteamItemInstanceID_t`)
- `unQuantity` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.ConsumeItem(out resultHandle, itemId, 1);
```

### ExchangeItems (静态)

```csharp
bool ExchangeItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayGenerate, uint[] punArrayGenerateQuantity, uint unArrayGenerateLength, SteamItemInstanceID_t[] pArrayDestroy, uint[] punArrayDestroyQuantity, uint unArrayDestroyLength)
```

<para> ExchangeItems() 是物品生成与消耗的原子化组合操作。</para> <para> 可用于实现合成配方、转化功能，或可拆解为其他物品的容器类物品（如宝箱）。</para> <para> 兑换配方在 ItemDef 中定义，并明确列出所需物品类型及最终生成的物品类型。</para> <para> 兑换配方由库存服务以原子化方式执行评估；若所提供的材料与配方不符，</para> <para> 或其数量不足，则兑换操作将失败。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pArrayGenerate` (`SteamItemDef_t[]`)
- `punArrayGenerateQuantity` (`uint[]`)
- `unArrayGenerateLength` (`uint`)
- `pArrayDestroy` (`SteamItemInstanceID_t[]`)
- `punArrayDestroyQuantity` (`uint[]`)
- `unArrayDestroyLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t result; SteamGameServerInventory.ExchangeItems(out result, new SteamItemDef_t[] { (SteamItemDef_t)101 }, new uint[] { 1 }, 1, new SteamItemInstanceID_t[] { (SteamItemInstanceID_t)12345 }, new uint[] { 1 }, 1);
```

### TransferItemQuantity (静态)

```csharp
bool TransferItemQuantity(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t itemIdSource, uint unQuantity, SteamItemInstanceID_t itemIdDest)
```

<para> TransferItemQuantity() 适用于“可堆叠”（数量可大于一）的物品。</para> <para> 可用于将一个堆叠拆分为两个，或将数量从一个堆叠转移到另一个相同物品的堆叠中。</para> <para> 若要将一个堆叠拆分为两个，请为 itemIdDest 传入 k_SteamItemInstanceIDInvalid，系统将生成一个新物品。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemIdSource` (`SteamItemInstanceID_t`)
- `unQuantity` (`uint`)
- `itemIdDest` (`SteamItemInstanceID_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
SteamGameServerInventory.TransferItemQuantity(out resultHandle, sourceItemId, 10, destItemId);
```

### SendItemDropHeartbeat (静态)

```csharp
void SendItemDropHeartbeat()
```

<para> 定时掉落与游戏时长积分</para>
<para> 已弃用。正确的游戏时长结算无需调用此方法。</para>

**用法示例:**
```csharp
// 该方法已弃用，无需调用
// SteamGameServerInventory.SendItemDropHeartbeat();
```

### TriggerItemDrop (静态)

```csharp
bool TriggerItemDrop(out SteamInventoryResult_t pResultHandle, SteamItemDef_t dropListDefinition)
```

<para> 游戏时间积分必须被消耗并转化为物品掉落。仅允许生成标记为"游戏时间物品生成器"的物品定义。</para> <para> 若游戏时间积分不足以产生一次掉落，调用将返回空结果集。</para> <para> 游戏应在适当时机（如回合间隙或玩家死亡期间）调用TriggerItemDrop，以便用户接收新物品。</para> <para> 注意：破解客户端的玩家可能篡改"dropListDefinition"的值，因此请勿将其用于直接控制稀有度。</para> <para> 请参阅Steamworks配置，为单个物品定义设置游戏时间掉落率。</para> <para> 客户端库将抑制对该方法的过于频繁的调用。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `dropListDefinition` (`SteamItemDef_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.TriggerItemDrop(out resultHandle, new SteamItemDef_t(12345));
```

### TradeItems (静态)

```csharp
bool TradeItems(out SteamInventoryResult_t pResultHandle, CSteamID steamIDTradePartner, SteamItemInstanceID_t[] pArrayGive, uint[] pArrayGiveQuantity, uint nArrayGiveLength, SteamItemInstanceID_t[] pArrayGet, uint[] pArrayGetQuantity, uint nArrayGetLength)
```

<para> 已弃用。此方法不受支持。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `steamIDTradePartner` (`CSteamID`)
- `pArrayGive` (`SteamItemInstanceID_t[]`)
- `pArrayGiveQuantity` (`uint[]`)
- `nArrayGiveLength` (`uint`)
- `pArrayGet` (`SteamItemInstanceID_t[]`)
- `pArrayGetQuantity` (`uint[]`)
- `nArrayGetLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t result; SteamGameServerInventory.TradeItems(out result, CSteamID.Nil, null, null, 0, null, null, 0);
```

### LoadItemDefinitions (静态)

```csharp
bool LoadItemDefinitions()
```

<para> 物品定义</para> <para> 物品定义是将"定义ID"（1 到 1,000,000 之间的整数）</para> <para> 映射到一组字符串属性。其中部分属性是 Steam 社区网站显示物品所必需的，</para> <para> 其他属性可由应用程序自行定义。</para> <para> 这些函数的使用是可选的；如果您的游戏硬编码了数值型定义 ID（例如，紫色面罩 = 20，</para> <para> 蓝色武器模组 = 55），且不通过客户端补丁就无法添加新物品类型，则无需调用 LoadItemDefinitions。</para> <para> LoadItemDefinitions 会触发物品定义的自动加载与刷新。</para> <para> 每当新的物品定义可用时（例如，在玩家仍在游戏过程中动态添加新物品类型时），</para> <para> 将会触发一个 SteamInventoryDefinitionUpdate_t 回调。</para>

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.LoadItemDefinitions();
```

### GetItemDefinitionIDs (静态)

```csharp
bool GetItemDefinitionIDs(SteamItemDef_t[] pItemDefIDs, ref uint punItemDefIDsArraySize)
```

<para> GetItemDefinitionIDs 返回所有已定义物品定义ID的集合（这些ID通过</para> <para> Steamworks 配置定义，且不一定是连续的整数）。</para> <para> 如果 pItemDefIDs 为空，则调用将返回 true，且 *punItemDefIDsArraySize 将</para> <para> 包含后续调用所需的总大小。否则，仅当输出数组空间不足时，调用才会返回 false。</para>

**参数:**

- `pItemDefIDs` (`SteamItemDef_t[]`)
- `punItemDefIDsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = 0; SteamGameServerInventory.GetItemDefinitionIDs(null, ref size);
var ids = new SteamItemDef_t[size]; SteamGameServerInventory.GetItemDefinitionIDs(ids, ref size);
```

### GetItemDefinitionProperty (静态)

```csharp
bool GetItemDefinitionProperty(SteamItemDef_t iDefinition, string pchPropertyName, out string pchValueBuffer, ref uint punValueBufferSizeOut)
```

<para> GetItemDefinitionProperty 从给定的物品定义中返回一个字符串属性。</para> <para> 请注意，某些属性（例如 "name"）可能是本地化的，具体取决于</para> <para> 当前的 Steam 语言设置（参见 ISteamApps::GetCurrentGameLanguage）。</para> <para> 属性名称始终由 ASCII 字母、数字和/或下划线组成。</para> <para> 将 pchPropertyName 传递为空指针以获取可用属性名称的逗号分隔列表。</para> <para> 如果 pchValueBuffer 为空，*punValueBufferSize 将包含建议的缓冲区大小。</para> <para> 否则，它将为实际复制到 pchValueBuffer 的字节数。</para> <para> 如果结果无法容纳在给定缓冲区中，可能会复制部分结果。</para>

**参数:**

- `iDefinition` (`SteamItemDef_t`)
- `pchPropertyName` (`string`)
- `pchValueBuffer` (`out string`)
- `punValueBufferSizeOut` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = 0; SteamGameServerInventory.GetItemDefinitionProperty(def, "name", out _, ref size);
string value = new string('\0', (int)size); SteamGameServerInventory.GetItemDefinitionProperty(def, "name", out value, ref size);
```

### RequestEligiblePromoItemDefinitionsIDs (静态)

```csharp
SteamAPICall_t RequestEligiblePromoItemDefinitionsIDs(CSteamID steamID)
```

<para> 请求可手动授予给定用户的“符合条件”的促销物品列表。</para> <para> 这些是类型为“手动”的促销物品，不会自动授予。</para> <para> 此功能的一个示例用法是每周可用的物品。</para>

**参数:**

- `steamID` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
CSteamID userSteamID = new CSteamID(76561198000000000);
SteamAPICall_t callHandle = SteamGameServerInventory.RequestEligiblePromoItemDefinitionsIDs(userSteamID);
```

### GetEligiblePromoItemDefinitionIDs (静态)

```csharp
bool GetEligiblePromoItemDefinitionIDs(CSteamID steamID, SteamItemDef_t[] pItemDefIDs, ref uint punItemDefIDsArraySize)
```

<para> 在处理 SteamInventoryEligiblePromoItemDefIDs_t 调用结果后，使用此</para> <para> 函数提取用户可通过 AddPromoItems() 调用手动获取的</para> <para> 物品定义ID列表。</para>

**参数:**

- `steamID` (`CSteamID`)
- `pItemDefIDs` (`SteamItemDef_t[]`)
- `punItemDefIDsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
var itemDefs = new SteamItemDef_t[10]; uint count = 10; bool success = SteamGameServerInventory.GetEligiblePromoItemDefinitionIDs(steamID, itemDefs, ref count);
```

### StartPurchase (静态)

```csharp
SteamAPICall_t StartPurchase(SteamItemDef_t[] pArrayItemDefs, uint[] punArrayQuantity, uint unArrayLength)
```

<para> 为给定的物品定义启动购买流程。若Steam能成功初始化交易，将发布 SteamInventoryStartPurchaseResult_t 回调。</para>
<para> 一旦用户授权并完成购买，将发布 SteamInventoryResultReady_t 回调。</para>

**参数:**

- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `punArrayQuantity` (`uint[]`)
- `unArrayLength` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamItemDef_t[] defs = { new SteamItemDef_t(123) }; uint[] qtys = { 1 }; SteamAPICall_t call = SteamGameServerInventory.StartPurchase(defs, qtys, 1);
```

### RequestPrices (静态)

```csharp
SteamAPICall_t RequestPrices()
```

<para> 请求所有适用物品定义的当前价格</para>

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t callHandle = SteamGameServerInventory.RequestPrices();
```

### GetNumItemsWithPrices (静态)

```csharp
uint GetNumItemsWithPrices()
```

<para> 返回有价格的项目数量。需要先调用 RequestPrices()。</para>

**返回值:** `uint`

**用法示例:**
```csharp
SteamGameServerInventory.RequestPrices();
uint count = SteamGameServerInventory.GetNumItemsWithPrices();
```

### GetItemsWithPrices (静态)

```csharp
bool GetItemsWithPrices(SteamItemDef_t[] pArrayItemDefs, ulong[] pCurrentPrices, ulong[] pBasePrices, uint unArrayLength)
```

<para> 返回物品定义ID及其以用户本地货币计价的价格。</para> <para> 需要先调用RequestPrices()。</para>

**参数:**

- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `pCurrentPrices` (`ulong[]`)
- `pBasePrices` (`ulong[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.RequestPrices();
bool success = SteamGameServerInventory.GetItemsWithPrices(itemDefs, currentPrices, basePrices, (uint)itemDefs.Length);
```

### GetItemPrice (静态)

```csharp
bool GetItemPrice(SteamItemDef_t iDefinition, out ulong pCurrentPrice, out ulong pBasePrice)
```

<para> 获取物品定义ID对应的价格</para> <para> 如果该物品定义未存储价格，则返回false。</para>

**参数:**

- `iDefinition` (`SteamItemDef_t`)
- `pCurrentPrice` (`out ulong`)
- `pBasePrice` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerInventory.GetItemPrice(12345, out ulong currentPrice, out ulong basePrice);
```

### StartUpdateProperties (静态)

```csharp
SteamInventoryUpdateHandle_t StartUpdateProperties()
```

<para> 创建更新物品属性的请求</para>

**返回值:** `SteamInventoryUpdateHandle_t`

**用法示例:**
```csharp
var updateHandle = SteamGameServerInventory.StartUpdateProperties();
```

### RemoveProperty (静态)

```csharp
bool RemoveProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName)
```

<para> 移除物品上的属性</para>

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerInventory.RemoveProperty(updateHandle, itemInstanceId, "custom_attribute");
```

### SetProperty (静态)

```csharp
bool SetProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName, string pchPropertyValue)
```

<para> 用于设置物品属性的访问器方法</para>

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)
- `pchPropertyValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.SetProperty(updateHandle, itemId, "quality", "rare");
```

### SetProperty (静态)

```csharp
bool SetProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName, bool bValue)
```

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)
- `bValue` (`bool`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.SetProperty(updateHandle, itemId, "isEquipped", true);
```

### SetProperty (静态)

```csharp
bool SetProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName, long nValue)
```

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)
- `nValue` (`long`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerInventory.SetProperty(handle, itemInstanceId, "Durability", 100);
```

### SetProperty (静态)

```csharp
bool SetProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName, float flValue)
```

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)
- `flValue` (`float`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.SetProperty(updateHandle, itemInstanceId, "durability", 0.5f);
```

### SubmitUpdateProperties (静态)

```csharp
bool SubmitUpdateProperties(SteamInventoryUpdateHandle_t handle, out SteamInventoryResult_t pResultHandle)
```

<para> 通过句柄提交更新请求</para>

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryUpdateHandle_t handle = default;
bool success = SteamGameServerInventory.SubmitUpdateProperties(handle, out SteamInventoryResult_t resultHandle);
```

### InspectItem (静态)

```csharp
bool InspectItem(out SteamInventoryResult_t pResultHandle, string pchItemToken)
```

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pchItemToken` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.InspectItem(out resultHandle, "item_token_123");
```

