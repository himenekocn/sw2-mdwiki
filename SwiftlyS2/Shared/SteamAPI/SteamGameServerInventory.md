# 📦 SteamGameServerInventory

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetResultStatus (静态)

```csharp
EResult GetResultStatus(SteamInventoryResult_t resultHandle)
```

<para> 库存异步结果管理</para> <para> 异步库存查询总是会输出一个结果句柄，该句柄可用于</para> <para> GetResultStatus、GetResultItems 等方法。当异步结果准备就绪（或失败）时，</para> <para> 将会触发 SteamInventoryResultReady_t 回调。</para> <para> 查询异步库存结果句柄的状态。可能的值有：</para> <para> k_EResultPending - 仍在进行中</para> <para> k_EResultOK - 已完成，结果准备就绪</para> <para> k_EResultExpired - 已完成，结果准备就绪，但可能已过时（请参阅 DeserializeResult）</para> <para> k_EResultInvalidParam - 错误：API 调用参数无效</para> <para> k_EResultServiceUnavailable - 错误：服务暂时不可用，您可以稍后重试</para> <para> k_EResultLimitExceeded - 错误：操作将超出每个用户的库存限制</para> <para> k_EResultFail - 错误：未知/通用错误</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**返回值:** `EResult`

**用法示例:**
```csharp
EResult status = SteamGameServerInventory.GetResultStatus(resultHandle);
if (status == EResult.k_EResultOK) { /* 处理结果 */ }
```

### GetResultItems (静态)

```csharp
bool GetResultItems(SteamInventoryResult_t resultHandle, SteamItemDetails_t[] pOutItemsArray, ref uint punOutItemsArraySize)
```

<para>将结果集中的内容复制到一个扁平数组中。结果集的具体内容取决于所使用的查询。</para> <para></para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `pOutItemsArray` (`SteamItemDetails_t[]`)
- `punOutItemsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint count = 10;
SteamItemDetails_t[] items = new SteamItemDetails_t[count];
bool success = SteamGameServerInventory.GetResultItems(resultHandle, items, ref count);
```

### GetResultItemProperty (静态)

```csharp
bool GetResultItemProperty(SteamInventoryResult_t resultHandle, uint unItemIndex, string pchPropertyName, out string pchValueBuffer, ref uint punValueBufferSizeOut)
```

<para> 结合 GetResultItems 使用，您可以使用 GetResultItemProperty 来检索</para> <para> 结果集中给定项的动态字符串属性。</para> <para> 属性名称始终由 ASCII 字母、数字和/或下划线组成。</para> <para> 若将 NULL 指针传递给 pchPropertyName，则将获取可用</para> <para> 属性名称的逗号分隔列表。</para> <para> 如果 pchValueBuffer 为 NULL，则 *punValueBufferSize 将包含</para> <para> 建议的缓冲区大小。否则，它将是实际复制到 pchValueBuffer 的字节数。</para> <para> 如果结果无法放入给定缓冲区，则可能会复制部分结果。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `unItemIndex` (`uint`)
- `pchPropertyName` (`string`)
- `pchValueBuffer` (`out string`)
- `punValueBufferSizeOut` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
string value;
uint bufferSize = 256;
SteamGameServerInventory.GetResultItemProperty(resultHandle, 0, "propName", out value, ref bufferSize);
```

### GetResultTimestamp (静态)

```csharp
uint GetResultTimestamp(SteamInventoryResult_t resultHandle)
```

<para> 返回生成结果时的服务器时间。可与</para> <para> IClientUtils::GetServerRealTime() 的值进行比较，以确定结果的时效性。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**返回值:** `uint`

**用法示例:**
```csharp
uint timestamp = SteamGameServerInventory.GetResultTimestamp(resultHandle);
```

### CheckResultSteamID (静态)

```csharp
bool CheckResultSteamID(SteamInventoryResult_t resultHandle, CSteamID steamIDExpected)
```

<para>如果结果属于目标Steam ID，则返回true；如果结果不属于，则返回false。在使用DeserializeResult时，这一点很重要，可用于验证远程玩家是否没有冒充其他用户的库存。</para> <para></para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `steamIDExpected` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = SteamGameServerInventory.CheckResultSteamID(resultHandle, new CSteamID(123456789));
```

### DestroyResult (静态)

```csharp
void DestroyResult(SteamInventoryResult_t resultHandle)
```

销毁结果句柄并释放所有关联的内存。

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**用法示例:**
```csharp
SteamGameServerInventory.DestroyResult(resultHandle);
```

### GetAllItems (静态)

```csharp
bool GetAllItems(out SteamInventoryResult_t pResultHandle)
```

<para>库存异步查询</para> <para>捕获当前用户Steam库存的完整状态。</para> <para>使用完毕后，必须调用此句柄上的DestroyResult方法。</para> <para>如果库存不可用，则返回false并将*pResultHandle设置为0。</para> <para>注意：对此函数的调用受速率限制，如果调用过于频繁，可能会返回</para> <para>缓存结果。建议仅在您即将显示用户的完整库存时调用</para> <para>此函数，或者如果您预期库存可能已更改。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.GetAllItems(out var resultHandle);
if (resultHandle != 0) { /* 处理结果 */ }
```

### GetItemsByID (静态)

```csharp
bool GetItemsByID(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t[] pInstanceIDs, uint unCountInstanceIDs)
```

<para> 捕获当前用户Steam库存中一部分物品的状态，</para> <para> 这些物品由一个物品实例ID数组标识。此调用的结果</para> <para> 可以被序列化并传递给其他玩家，以“证明”当前</para> <para> 用户拥有特定物品，而无需暴露用户的整个库存。</para> <para> 例如，你可以使用用户当前装备的装饰物品的ID调用GetItemsByID，</para> <para> 并将其序列化到一个缓冲区，然后在加入游戏时将此缓冲区</para> <para> 传输给其他玩家。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pInstanceIDs` (`SteamItemInstanceID_t[]`)
- `unCountInstanceIDs` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamItemInstanceID_t[] itemIDs = { /* 假设已填充 */ };
bool success = SteamGameServerInventory.GetItemsByID(out var resultHandle, itemIDs, (uint)itemIDs.Length);
```

### SerializeResult (静态)

```csharp
bool SerializeResult(SteamInventoryResult_t resultHandle, byte[] pOutBuffer, out uint punOutBufferSize)
```

<para>结果序列化与身份验证</para> <para>序列化的结果集包含一个无法伪造的短签名</para> <para>或在不同游戏会话中重放。结果集可以在本地客户端序列化，</para> <para>通过游戏网络传输给其他玩家，并由远程玩家反序列化。这是一种</para> <para>防止黑客谎称拥有稀有/高价值物品的安全方式。</para> <para>将带有签名字节的结果集序列化到输出缓冲区。将</para> <para>NULL作为输出缓冲区传入，可通过punOutBufferSize获取所需大小。</para> <para>序列化结果的大小取决于正在序列化的项目数量。在安全地向</para> <para>其他玩家传输物品时，建议先使用"GetItemsByID"创建一个最小的结果集。</para> <para>结果内置时间戳，在一小时后将被视为"过期"。有关过期处理，请参阅DeserializeResult。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `pOutBuffer` (`byte[]`)
- `punOutBufferSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bufferSize = 0;
SteamGameServerInventory.SerializeResult(resultHandle, null, out bufferSize);
```

### DeserializeResult (静态)

```csharp
bool DeserializeResult(out SteamInventoryResult_t pOutResultHandle, byte[] pBuffer, uint unBufferSize, bool bRESERVED_MUST_BE_FALSE = false)
```

<para> 反序列化结果集并验证签名字节。如果 bRequireFullOnlineVerify 为 true 但 Steam 处于离线模式，则返回 false。</para> <para> 否则返回 true，并通过 GetResultStatus 传递错误代码。</para> <para> bRESERVED_MUST_BE_FALSE 标志为保留供将来使用，目前不应由您的游戏设置为 true。</para> <para> DeserializeResult 存在一种潜在的软失败模式，即句柄状态被设置为 k_EResultExpired。在此模式下，GetResultItems() 仍会成功。</para> <para> “已过期”的结果可能表示数据可能已过时 - 不仅是因为超时过期（一小时），还可能是因为结果集中的一项物品自生成以来已被交易或消耗。</para> <para> 您可以比较 GetResultTimestamp() 返回的时间戳与 ISteamUtils::GetServerRealTime() 来确定数据的陈旧程度。</para> <para> 您可以简单地忽略“已过期”的结果代码并继续正常操作，或者您可以要求持有过期数据的玩家发送更新的结果集。</para>

**参数:**

- `pOutResultHandle` (`out SteamInventoryResult_t`)
- `pBuffer` (`byte[]`)
- `unBufferSize` (`uint`)
- `bRESERVED_MUST_BE_FALSE` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerInventory.DeserializeResult(out SteamInventoryResult_t result, buffer, bufferSize, false);
```

### GenerateItems (静态)

```csharp
bool GenerateItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayItemDefs, uint[] punArrayQuantity, uint unArrayLength)
```

<para> 库存异步修改</para> <para> GenerateItems() 方法会创建一个或多个物品，然后生成一个带有匹配的 nCallbackContext 参数的 SteamInventoryCallback_t</para> <para> 通知。此 API 仅用于原型设计 - 仅适用于属于您的游戏发行商组的 Steam 账户。</para> <para> 如果 punArrayQuantity 不为 NULL，则其长度应与 pArrayItems 相同，并应描述要生成的每个物品的数量。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `punArrayQuantity` (`uint[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint[] quantities = { 1, 2 };
SteamItemDef_t[] itemDefs = { (SteamItemDef_t)1001, (SteamItemDef_t)1002 };
SteamGameServerInventory.GenerateItems(out var resultHandle, itemDefs, quantities, 2);
```

### GrantPromoItems (静态)

```csharp
bool GrantPromoItems(out SteamInventoryResult_t pResultHandle)
```

<para> GrantPromoItems() 检查用户可能有资格获得的促销商品列表</para> <para> 并授予这些商品（仅一次）。如果成功，结果集将包含已授予的商品（如果有的话）。</para> <para> 如果由于用户不符合任何促销条件而未授予任何商品，这也被视为成功。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.GrantPromoItems(out var resultHandle);
```

### AddPromoItem (静态)

```csharp
bool AddPromoItem(out SteamInventoryResult_t pResultHandle, SteamItemDef_t itemDef)
```

<para> AddPromoItem() / AddPromoItems() 是 GrantPromoItems() 的受限版本。与扫描所有符合条件的促销物品不同，检查范围被限制为单个物品定义或一组物品定义。如果您的游戏有用于向用户展示特定促销物品的自定义 UI，这会很有用。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemDef` (`SteamItemDef_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerInventory.AddPromoItem(out var resultHandle, (SteamItemDef_t)123);
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
bool result = SteamGameServerInventory.AddPromoItems(out var handle, new SteamItemDef_t[] { 1, 2 }, 2);
```

### ConsumeItem (静态)

```csharp
bool ConsumeItem(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t itemConsume, uint unQuantity)
```

<para> ConsumeItem() 会从物品栏中永久移除物品，且无法恢复。</para> <para> 此操作不适合胆小者——如果你的游戏实现了物品移除功能，强烈建议采用高阻力的 UI 确认流程。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemConsume` (`SteamItemInstanceID_t`)
- `unQuantity` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.ConsumeItem(out var result, itemID, 1);
```

### ExchangeItems (静态)

```csharp
bool ExchangeItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayGenerate, uint[] punArrayGenerateQuantity, uint unArrayGenerateLength, SteamItemInstanceID_t[] pArrayDestroy, uint[] punArrayDestroyQuantity, uint unArrayDestroyLength)
```

<para> ExchangeItems() 是物品生成与消耗的原子性组合操作。</para> <para> 它可用于实现合成配方或转化，或实现物品自身解包为其他物品（例如，一个箱子）。</para> <para> 交换配方在 ItemDef 中定义，并明确列出所需的物品类型和生成的结果类型。</para> <para> 交换配方由库存服务以原子性方式评估；如果提供的组件与配方不匹配，或数量不足，则交换将失败。</para>

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
bool result = SteamGameServerInventory.ExchangeItems(out var resultHandle, new SteamItemDef_t[] { 1 }, new uint[] { 2 }, 1, new SteamItemInstanceID_t[] { }, new uint[] { }, 0);
```

### TransferItemQuantity (静态)

```csharp
bool TransferItemQuantity(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t itemIdSource, uint unQuantity, SteamItemInstanceID_t itemIdDest)
```

<para> TransferItemQuantity() 方法旨在用于处理“可堆叠”物品（即数量可以大于一的物品）。它可用于将一个堆叠拆分为两个，或将一个堆叠中的数量转移到另一个相同物品的堆叠中。若要将一个堆叠拆分为两个，请将 k_SteamItemInstanceIDInvalid 传入 itemIdDest，系统将生成一个新物品。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemIdSource` (`SteamItemInstanceID_t`)
- `unQuantity` (`uint`)
- `itemIdDest` (`SteamItemInstanceID_t`)

**返回值:** `bool`

**用法示例:**
```csharp
bool result = SteamGameServerInventory.TransferItemQuantity(out var resultHandle, itemIdSource, 10u, itemIdDest);
```

### SendItemDropHeartbeat (静态)

```csharp
void SendItemDropHeartbeat()
```

<para> 定时掉落与游戏时长积分</para> <para> 已弃用。调用此方法并非进行游戏时长统计所必需。</para>

**用法示例:**
```csharp
SteamGameServerInventory.SendItemDropHeartbeat();
```

### TriggerItemDrop (静态)

```csharp
bool TriggerItemDrop(out SteamInventoryResult_t pResultHandle, SteamItemDef_t dropListDefinition)
```

<para> 游戏时间积分必须由您的游戏消耗并转化为物品掉落。只有被标记为“游戏时间物品生成器”的物品定义才能被生成。如果掉落所需的游戏时间积分不足，该调用将返回一个空的结果集。</para> <para> 您的游戏应在用户接收新物品的适当时间调用 TriggerItemDrop，例如在回合之间或玩家死亡时。请注意，修改客户端的玩家可能会修改“dropListDefinition”的值，因此不要用它来直接控制稀有度。</para> <para> 请查看您的 Steamworks 配置，以设置各个物品定义的游戏时间掉落率。</para> <para> 客户端库将抑制对此方法的过于频繁的调用。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `dropListDefinition` (`SteamItemDef_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.TriggerItemDrop(out resultHandle, itemDef);
```

### TradeItems (静态)

```csharp
bool TradeItems(out SteamInventoryResult_t pResultHandle, CSteamID steamIDTradePartner, SteamItemInstanceID_t[] pArrayGive, uint[] pArrayGiveQuantity, uint nArrayGiveLength, SteamItemInstanceID_t[] pArrayGet, uint[] pArrayGetQuantity, uint nArrayGetLength)
```

<para> 已废弃。此方法不受支持。</para>

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
// 此方法已废弃，不建议使用；若仍需调用（例如兼容旧逻辑），可按如下方式调用：
bool result = SteamGameServerInventory.TradeItems(out var resultHandle, new CSteamID(0), null, null, 0, null, null, 0);
```

### LoadItemDefinitions (静态)

```csharp
bool LoadItemDefinitions()
```

<para> 物品定义</para> <para> 物品定义是将“定义ID”（介于1到1000000之间的整数）</para> <para> 映射到一组字符串属性。其中一些属性是显示物品</para> <para> 在Steam社区网站上是必需的。其他属性可以由应用程序定义。</para> <para> 使用这些函数是可选的；如果您的游戏硬编码了数字定义ID（例如，紫色面具 = 20，蓝色</para> <para> 武器模组 = 55）并且不允许在不进行客户端更新的情况下添加新物品类型，则没有理由调用LoadItemDefinitions。</para> <para> LoadItemDefinitions会触发物品定义的自动加载和刷新。</para> <para> 每当有新的物品定义可用时（例如，在玩家仍在游戏中时动态添加新</para> <para> 物品类型），将触发一个SteamInventoryDefinitionUpdate_t</para> <para> 回调。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool success = SteamGameServerInventory.LoadItemDefinitions();
```

### GetItemDefinitionIDs (静态)

```csharp
bool GetItemDefinitionIDs(SteamItemDef_t[] pItemDefIDs, ref uint punItemDefIDsArraySize)
```

<para> GetItemDefinitionIDs 返回所有已定义物品定义 ID 的集合（这些 ID 是通过 Steamworks 配置定义的，不一定是连续的整数）。</para> <para> 如果 pItemDefIDs 为 null，则该调用将返回 true，并且 *punItemDefIDsArraySize 将包含后续调用所需的数组总大小。否则，当且仅当输出数组空间不足时，该调用将返回 false。</para>

**参数:**

- `pItemDefIDs` (`SteamItemDef_t[]`)
- `punItemDefIDsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = 0;
SteamGameServerInventory.GetItemDefinitionIDs(null, ref size);
SteamItemDef_t[] defs = new SteamItemDef_t[size];
bool success = SteamGameServerInventory.GetItemDefinitionIDs(defs, ref size);
```

### GetItemDefinitionProperty (静态)

```csharp
bool GetItemDefinitionProperty(SteamItemDef_t iDefinition, string pchPropertyName, out string pchValueBuffer, ref uint punValueBufferSizeOut)
```

<para> GetItemDefinitionProperty 从给定的物品定义中返回一个字符串属性。</para> <para> 请注意，某些属性（例如 "name"）可能是本地化的，并且将取决于当前的 Steam 语言设置（请参阅 ISteamApps::GetCurrentGameLanguage）。</para> <para> 属性名称始终由 ASCII 字母、数字和/或下划线组成。</para> <para> 若要获取可用属性名称的逗号分隔列表，请为 pchPropertyName 传递一个 NULL 指针。</para> <para> 如果 pchValueBuffer 为 NULL，则 *punValueBufferSize 将包含建议的缓冲区大小。否则，它将是实际复制到 pchValueBuffer 的字节数。</para> <para> 如果结果不适合给定的缓冲区，则可能会复制部分结果。</para>

**参数:**

- `iDefinition` (`SteamItemDef_t`)
- `pchPropertyName` (`string`)
- `pchValueBuffer` (`out string`)
- `punValueBufferSizeOut` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint bufferSize = 256;
string value = string.Empty;
bool result = SteamGameServerInventory.GetItemDefinitionProperty(SteamItemDef_t.Invalid, "name", out value, ref bufferSize);
```

### RequestEligiblePromoItemDefinitionsIDs (静态)

```csharp
SteamAPICall_t RequestEligiblePromoItemDefinitionsIDs(CSteamID steamID)
```

<para> 请求可手动授予指定用户的“符合资格”的促销商品列表。这些是类型为“manual”且不会自动授予的促销商品。</para> <para> 此功能的一个使用示例是每周可用的商品。</para>

**参数:**

- `steamID` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamGameServerInventory.RequestEligiblePromoItemDefinitionsIDs(new CSteamID(123456789));
```

### GetEligiblePromoItemDefinitionIDs (静态)

```csharp
bool GetEligiblePromoItemDefinitionIDs(CSteamID steamID, SteamItemDef_t[] pItemDefIDs, ref uint punItemDefIDsArraySize)
```

<para> 在处理完 SteamInventoryEligiblePromoItemDefIDs_t 调用结果后，使用此</para> <para> 函数来提取用户可通过 AddPromoItems() 调用手动授予的物品定义 ID 列表。</para>

**参数:**

- `steamID` (`CSteamID`)
- `pItemDefIDs` (`SteamItemDef_t[]`)
- `punItemDefIDsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint itemDefCount = 0;
SteamGameServerInventory.GetEligiblePromoItemDefinitionIDs(CSteamID.Zero, null, ref itemDefCount);
```

### StartPurchase (静态)

```csharp
SteamAPICall_t StartPurchase(SteamItemDef_t[] pArrayItemDefs, uint[] punArrayQuantity, uint unArrayLength)
```

<para> 为给定的物品定义启动购买流程。如果 Steam 能够初始化交易，将发布回调 SteamInventoryStartPurchaseResult_t。</para> <para> 当购买被用户授权并完成时，将发布回调 SteamInventoryResultReady_t。</para>

**参数:**

- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `punArrayQuantity` (`uint[]`)
- `unArrayLength` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamItemDef_t[] itemDefs = { SteamItemDef_t.Def1, SteamItemDef_t.Def2 };
uint[] quantities = { 1u, 2u };
SteamAPICall_t callId = SteamGameServerInventory.StartPurchase(itemDefs, quantities, (uint)itemDefs.Length);
```

### RequestPrices (静态)

```csharp
SteamAPICall_t RequestPrices()
```

<para> 请求所有适用物品定义的当前价格</para>

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerInventory.RequestPrices();
```

### GetNumItemsWithPrices (静态)

```csharp
uint GetNumItemsWithPrices()
```

<para> 返回具有价格的项的数量。需要先调用 RequestPrices() 方法。</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint count = SteamGameServerInventory.GetNumItemsWithPrices();
```

### GetItemsWithPrices (静态)

```csharp
bool GetItemsWithPrices(SteamItemDef_t[] pArrayItemDefs, ulong[] pCurrentPrices, ulong[] pBasePrices, uint unArrayLength)
```

<para> 返回用户本地货币中的物品定义 ID 及其价格。</para> <para> 需要先调用 RequestPrices()。</para>

**参数:**

- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `pCurrentPrices` (`ulong[]`)
- `pBasePrices` (`ulong[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamItemDef_t[] itemDefs = { (SteamItemDef_t)1, (SteamItemDef_t)2 };
ulong[] currentPrices = new ulong[2];
ulong[] basePrices = new ulong[2];
bool success = SteamGameServerInventory.GetItemsWithPrices(itemDefs, currentPrices, basePrices, 2);
```

### GetItemPrice (静态)

```csharp
bool GetItemPrice(SteamItemDef_t iDefinition, out ulong pCurrentPrice, out ulong pBasePrice)
```

<para>检索指定物品定义ID的价格</para> <para>如果未存储该物品定义的价格，则返回false。</para>

**参数:**

- `iDefinition` (`SteamItemDef_t`)
- `pCurrentPrice` (`out ulong`)
- `pBasePrice` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
ulong currentPrice, basePrice;
bool success = SteamGameServerInventory.GetItemPrice(SteamItemDef_t.Definition1, out currentPrice, out basePrice);
```

### StartUpdateProperties (静态)

```csharp
SteamInventoryUpdateHandle_t StartUpdateProperties()
```

<para> 创建一个用于更新项目属性的请求</para>

**返回值:** `SteamInventoryUpdateHandle_t`

**用法示例:**
```csharp
SteamGameServerInventoryHandle_t handle = SteamGameServerInventory.StartUpdateProperties();
```

### RemoveProperty (静态)

```csharp
bool RemoveProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName)
```

<para> 移除项上的属性</para>

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.RemoveProperty(handle, itemID, "custom_prop");
```

### SetProperty (静态)

```csharp
bool SetProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName, string pchPropertyValue)
```

<para> 用于设置项属性的访问器方法</para>

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)
- `pchPropertyValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.SetProperty(handle, itemID, "quality", "rare");
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
bool result = SteamGameServerInventory.SetProperty(handle, itemID, "propName", true);
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
bool result = SteamGameServerInventory.SetProperty(handle, itemID, "health", 100);
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
bool result = SteamGameServerInventory.SetProperty(handle, itemID, "health", 100f);
```

### SubmitUpdateProperties (静态)

```csharp
bool SubmitUpdateProperties(SteamInventoryUpdateHandle_t handle, out SteamInventoryResult_t pResultHandle)
```

通过句柄提交更新请求

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t result;
bool success = SteamGameServerInventory.SubmitUpdateProperties(handle, out result);
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
bool result = SteamGameServerInventory.InspectItem(out var handle, "item_token_123");
```

