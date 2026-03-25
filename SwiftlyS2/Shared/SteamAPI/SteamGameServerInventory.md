<a id="steamgameserverinventory"></a>

# 📦 SteamGameServerInventory

**命名空间:** `SwiftlyS2.Shared.SteamAPI`

**类型:** `class`

## ⚙️ 方法

### GetResultStatus (静态)

```csharp
EResult GetResultStatus(SteamInventoryResult_t resultHandle)
```

<para> 库存异步结果管理</para> <para> 异步库存查询始终返回一个结果句柄，该句柄可用于 GetResultStatus、GetResultItems 等方法。当异步结果准备就绪（或失败）时，将触发 SteamInventoryResultReady_t 回调。</para> <para> 查询异步库存结果句柄的状态。可能的返回值：</para> <para> k_EResultPending - 进行中</para> <para> k_EResultOK - 已完成，结果已就绪</para> <para> k_EResultExpired - 已完成，结果已就绪，但可能已过时（请参见 DeserializeResult）</para> <para> k_EResultInvalidParam - 错误：无效的 API 调用参数</para> <para> k_EResultServiceUnavailable - 错误：服务暂时不可用，稍后可重试</para> <para> k_EResultLimitExceeded - 错误：操作将超过用户库存限制</para> <para> k_EResultFail - 错误：未知/通用错误

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)

**返回值:** `EResult`

**用法示例:**
```csharp
var status = SteamGameServerInventory.GetResultStatus(resultHandle);
if (status == EResult.k_EResultOK) Console.WriteLine("库存结果已就绪");
```

### GetResultItems (静态)

```csharp
bool GetResultItems(SteamInventoryResult_t resultHandle, SteamItemDetails_t[] pOutItemsArray, ref uint punOutItemsArraySize)
```

<para> 将结果集的内容复制到一个一维数组中。结果集的具体内容取决于所使用的查询。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `pOutItemsArray` (`SteamItemDetails_t[]`)
- `punOutItemsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint itemCount = 0;
bool ok = SteamGameServerInventory.GetResultItems(resultHandle, pOutItemsArray, ref itemCount);
```

### GetResultItemProperty (静态)

```csharp
bool GetResultItemProperty(SteamInventoryResult_t resultHandle, uint unItemIndex, string pchPropertyName, out string pchValueBuffer, ref uint punValueBufferSizeOut)
```

与 GetResultItems 配合使用，可通过 GetResultItemProperty 获取结果集中指定项的动态字符串属性。属性名称始终由 ASCII 字母、数字和/或下划线组成。若将 pchPropertyName 设为 NULL，则返回可用属性名的逗号分隔列表。若 pchValueBuffer 为 NULL，则 *punValueBufferSize 将包含建议的缓冲区大小；否则，该值表示实际复制到 pchValueBuffer 中的字节数。若结果无法完全放入给定缓冲区，可能仅复制部分结果。

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `unItemIndex` (`uint`)
- `pchPropertyName` (`string`)
- `pchValueBuffer` (`out string`)
- `punValueBufferSizeOut` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint valueSize = 0; string value;
SteamGameServerInventory.GetResultItemProperty(resultHandle, 0, "quality", out value, ref valueSize);
```

### GetResultTimestamp (静态)

```csharp
uint GetResultTimestamp(SteamInventoryResult_t resultHandle)
```

<para>返回生成结果时的服务器时间。与</para> <para>IClientUtils::GetServerRealTime() 的返回值进行比较以确定时效性。</para>

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

<para>如果结果属于目标 Steam ID，则返回 true；否则返回 false。在使用 DeserializeResult 时，此方法至关重要，用于验证远程玩家是否伪装成拥有其他用户的库存。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `steamIDExpected` (`CSteamID`)

**返回值:** `bool`

**用法示例:**
```csharp
bool isValid = SteamGameServerInventory.CheckResultSteamID(resultHandle, steamIDExpected);
if (!isValid) return;
```

### DestroyResult (静态)

```csharp
void DestroyResult(SteamInventoryResult_t resultHandle)
```

<para>销毁结果句柄并释放所有关联的内存。</para>

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

<para>库存异步查询</para> <para>捕获当前用户的 Steam 库存的完整状态。</para> <para>完成使用此句柄后，必须调用 DestroyResult。</para> <para>如果库存不可用，则返回 false 并将*pResultHandle 设置为零。</para> <para>注意：对此函数的调用受速率限制影响，若调用过于频繁可能会返回缓存结果。建议在即将展示用户完整库存时，或预期库存可能发生变化时才调用此函数。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool ok = SteamGameServerInventory.GetAllItems(out resultHandle);
```

### GetItemsByID (静态)

```csharp
bool GetItemsByID(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t[] pInstanceIDs, uint unCountInstanceIDs)
```

<para>获取当前用户 Steam 库存中由一组物品实例 ID 指定的子集状态。</para><para>此调用的结果可被序列化并传递给其他玩家，以“证明”当前用户拥有特定物品，同时无需暴露其整个库存。</para><para>例如，您可以调用 GetItemsByID 获取用户当前装备的饰品物品的 ID，将其序列化为缓冲区，然后在加入游戏时将此缓冲区传输给其他玩家。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pInstanceIDs` (`SteamItemInstanceID_t[]`)
- `unCountInstanceIDs` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamItemInstanceID_t[] ids = { itemId1, itemId2 };
SteamGameServerInventory.GetItemsByID(out var result, ids, (uint)ids.Length);
```

### SerializeResult (静态)

```csharp
bool SerializeResult(SteamInventoryResult_t resultHandle, byte[] pOutBuffer, out uint punOutBufferSize)
```

<para>结果序列化与认证</para><para>序列化的结果集包含一个简短的签名，该签名无法伪造，也不能在不同游戏会话中被重放。结果集可在本地客户端进行序列化，通过您的游戏网络传输给其他玩家，并由远程玩家反序列化。这是一种安全的方式，可防止黑客谎称拥有稀有或高价值物品。</para><para>将带有签名字节的結果集序列化到输出缓冲区。若需获取所需大小，可将 NULL 作为输出缓冲区传入，大小将通过 punOutBufferSize 返回。序列化后的结果集大小取决于正在序列化的物品数量。在向其他玩家安全传输物品时，建议先调用"GetItemsByID"以创建最小化的结果集。</para><para>结果集内置时间戳，超过一小时后将被视为“已过期”。有关过期处理详情，请参阅 DeserializeResult。</para>

**参数:**

- `resultHandle` (`SteamInventoryResult_t`)
- `pOutBuffer` (`byte[]`)
- `punOutBufferSize` (`out uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint outSize; SteamGameServerInventory.SerializeResult(resultHandle, null, out outSize);
```

### DeserializeResult (静态)

```csharp
bool DeserializeResult(out SteamInventoryResult_t pOutResultHandle, byte[] pBuffer, uint unBufferSize, bool bRESERVED_MUST_BE_FALSE = false)
```

<para>反序列化结果集并验证签名字节。若 bRequireFullOnlineVerify 标志已设置但 Steam 处于离线模式，则返回 false。</para> <para>否则返回 true，并通过 GetResultStatus() 传递错误代码。</para> <para>bRESERVED_MUST_BE_FALSE 标志保留供将来使用，您的游戏当前不应将其设置为 true。</para> <para>DeserializeResult() 存在一种潜在的软失败模式：在此模式下句柄状态被设置为 k_EResultExpired，但 GetResultItems() 仍可成功执行。</para> <para>“过期”结果可能表示数据已过时——这不仅可能是因为超时（一小时）导致，也可能是因为生成结果集后，其中的某项物品已被交易或消耗。您可以通过比较 GetResultTimestamp() 返回的时间戳与 ISteamUtils::GetServerRealTime() 来获取服务器真实时间，从而判断数据的陈旧程度。您可以选择忽略“过期”结果代码并照常处理，也可以针对持有过期数据的玩家发起挑战，要求其发送更新后的结果集。</para>

**参数:**

- `pOutResultHandle` (`out SteamInventoryResult_t`)
- `pBuffer` (`byte[]`)
- `unBufferSize` (`uint`)
- `bRESERVED_MUST_BE_FALSE` (`bool`) = `false`

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool ok = SteamGameServerInventory.DeserializeResult(out resultHandle, buffer, (uint)buffer.Length, false);
```

### GenerateItems (静态)

```csharp
bool GenerateItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayItemDefs, uint[] punArrayQuantity, uint unArrayLength)
```

<para>库存异步修改</para><para>GenerateItems() 函数用于创建一个或多个物品，随后生成一个带有匹配 nCallbackContext 参数的 SteamInventoryCallback_t 回调通知。此 API 仅适用于原型开发，且仅限属于您游戏发行商组的 Steam 账号使用。</para><para>若 punArrayQuantity 不为 NULL，其长度应与 pArrayItems 保持一致，并用于描述每个待生成物品的数量。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `punArrayQuantity` (`uint[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t result;
SteamGameServerInventory.GenerateItems(out result, itemDefs, quantities, (uint)itemDefs.Length);
```

### GrantPromoItems (静态)

```csharp
bool GrantPromoItems(out SteamInventoryResult_t pResultHandle)
```

GrantPromoItems() 检查用户可能有资格获得的促销物品列表，并授予这些物品（仅限一次）。如果操作成功，结果集中将包含已授予的物品（如有）。如果因用户不符合任何促销条件而未授予任何物品，该情况仍视为操作成功。

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t result;
bool ok = SteamGameServerInventory.GrantPromoItems(out result);
```

### AddPromoItem (静态)

```csharp
bool AddPromoItem(out SteamInventoryResult_t pResultHandle, SteamItemDef_t itemDef)
```

<para>AddPromoItem() / AddPromoItems() 是 GrantPromoItems() 的限制版本。不同于扫描所有符合条件的促销物品，此类方法仅针对单个物品定义或一组物品定义进行检查。若您的游戏拥有用于向用户展示特定促销物品的自定义 UI，此功能将非常有用。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemDef` (`SteamItemDef_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t result;
SteamGameServerInventory.AddPromoItem(out result, itemDef);
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
SteamInventoryResult_t result;
bool ok = SteamGameServerInventory.AddPromoItems(out result, itemDefs, (uint)itemDefs.Length);
```

### ConsumeItem (静态)

```csharp
bool ConsumeItem(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t itemConsume, uint unQuantity)
```

<para>ConsumeItem() 会从库存中永久移除物品，且无法恢复。</para> <para>此操作风险较高——如果您的游戏确实实现了物品移除功能，强烈建议采用高摩擦（high-friction）的用户界面确认流程。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemConsume` (`SteamItemInstanceID_t`)
- `unQuantity` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool success = SteamGameServerInventory.ConsumeItem(out resultHandle, itemConsume, 1);
```

### ExchangeItems (静态)

```csharp
bool ExchangeItems(out SteamInventoryResult_t pResultHandle, SteamItemDef_t[] pArrayGenerate, uint[] punArrayGenerateQuantity, uint unArrayGenerateLength, SteamItemInstanceID_t[] pArrayDestroy, uint[] punArrayDestroyQuantity, uint unArrayDestroyLength)
```

<para>ExchangeItems() 是一个集物品生成与消耗于一体的原子操作。</para><para>该接口可用于实现制作配方、转化逻辑，或支持自分解为其他物品的道具（例如箱子）。</para><para>交换配方在 ItemDef 中定义，并明确列出所需的物品类型及最终生成的物品类型。</para><para>Inventory Service 将以原子方式评估交换配方；若提供的组件不匹配配方要求或数量不足，则交换操作将失败。</para>

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
SteamInventoryResult_t result; SteamGameServerInventory.ExchangeItems(out result, generateDefs, generateQty, (uint)generateDefs.Length, destroyIds, destroyQty, (uint)destroyIds.Length);
```

### TransferItemQuantity (静态)

```csharp
bool TransferItemQuantity(out SteamInventoryResult_t pResultHandle, SteamItemInstanceID_t itemIdSource, uint unQuantity, SteamItemInstanceID_t itemIdDest)
```

<para>TransferItemQuantity() 专用于可堆叠的物品（即数量可大于 1）。该函数可用于将一个堆栈拆分为两个，或将一个堆栈中的部分数量转移到另一个相同物品的堆栈中。若要将单个堆栈拆分为两个，请将 itemIdDest 参数设置为 k_SteamItemInstanceIDInvalid，系统将生成一个新物品。</para>

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `itemIdSource` (`SteamItemInstanceID_t`)
- `unQuantity` (`uint`)
- `itemIdDest` (`SteamItemInstanceID_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
bool ok = SteamGameServerInventory.TransferItemQuantity(out resultHandle, sourceItemId, 1, destItemId);
```

### SendItemDropHeartbeat (静态)

```csharp
void SendItemDropHeartbeat()
```

<para> 限时掉落与游戏时长计数</para><para> 已弃用。调用此方法并非进行正确游戏时长统计所必需。</para>

**用法示例:**
```csharp
SteamGameServerInventory.SendItemDropHeartbeat();
```

### TriggerItemDrop (静态)

```csharp
bool TriggerItemDrop(out SteamInventoryResult_t pResultHandle, SteamItemDef_t dropListDefinition)
```

游玩时长积分必须由游戏消耗并转化为物品掉落。仅当物品定义被标记为“游玩时长物品生成器”时，方可生成该物品。若游玩时长积分不足以生成掉落物，调用将返回空结果集。游戏应在合适的时机调用 TriggerItemDrop，以便用户获得新物品，例如在回合之间或玩家死亡期间。请注意，修改客户端的玩家可能会篡改"dropListDefinition"的值，因此切勿将其用于直接控制稀有度。请查阅您的 Steamworks 配置以设置各个物品定义的游玩时长掉落率。客户端库将对过于频繁的此方法调用进行抑制。

**参数:**

- `pResultHandle` (`out SteamInventoryResult_t`)
- `dropListDefinition` (`SteamItemDef_t`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamInventoryResult_t resultHandle;
SteamGameServerInventory.TriggerItemDrop(out resultHandle, dropListDefinition);
```

### TradeItems (静态)

```csharp
bool TradeItems(out SteamInventoryResult_t pResultHandle, CSteamID steamIDTradePartner, SteamItemInstanceID_t[] pArrayGive, uint[] pArrayGiveQuantity, uint nArrayGiveLength, SteamItemInstanceID_t[] pArrayGet, uint[] pArrayGetQuantity, uint nArrayGetLength)
```

<para>已弃用。不支持此方法。</para>

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
SteamInventoryResult_t result; bool ok = SteamGameServerInventory.TradeItems(out result, steamIDTradePartner, pArrayGive, pArrayGiveQuantity, nArrayGiveLength, pArrayGet, pArrayGetQuantity, nArrayGetLength);
```

### LoadItemDefinitions (静态)

```csharp
bool LoadItemDefinitions()
```

<para>物品定义</para><para>物品定义是将“定义 ID"（1 至 1,000,000 之间的整数）映射到一组字符串属性的机制。其中部分属性是 Steam 社区网站显示物品所必需的；其他属性可由应用程序自行定义。</para><para>这些函数的使用是可选的：如果您的游戏硬编码了数值定义 ID（例如，紫色面具 = 20，蓝色武器模组 = 55），且不允许在不进行客户端补丁的情况下添加新的物品类型，则无需调用 LoadItemDefinitions。</para><para>LoadItemDefinitions 会触发物品定义的自动加载与刷新。每当有新的物品定义可用时（例如，在游戏进行中动态添加新物品类型时），将触发一个 SteamInventoryDefinitionUpdate_t 回调。</para>

**返回值:** `bool`

**用法示例:**
```csharp
bool loaded = SteamGameServerInventory.LoadItemDefinitions();
```

### GetItemDefinitionIDs (静态)

```csharp
bool GetItemDefinitionIDs(SteamItemDef_t[] pItemDefIDs, ref uint punItemDefIDsArraySize)
```

<para> GetItemDefinitionIDs 返回所有已定义的物品定义 ID 集合（这些 ID 通过 Steamworks 配置定义，不一定是连续的整数）。</para><para> 如果 pItemDefIDs 为 null，则调用将返回 true，且 *punItemDefIDsArraySize 将包含后续调用所需的总大小。否则，仅当输出数组空间不足时，调用才会返回 false。</para>

**参数:**

- `pItemDefIDs` (`SteamItemDef_t[]`)
- `punItemDefIDsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = 0; SteamGameServerInventory.GetItemDefinitionIDs(null, ref size);
```

### GetItemDefinitionProperty (静态)

```csharp
bool GetItemDefinitionProperty(SteamItemDef_t iDefinition, string pchPropertyName, out string pchValueBuffer, ref uint punValueBufferSizeOut)
```

GetItemDefinitionProperty 从指定的物品定义中获取一个字符串属性。注意，某些属性（例如"name"）可能是本地化的，并且取决于当前的 Steam 语言设置（参见 ISteamApps::GetCurrentGameLanguage）。属性名称始终由 ASCII 字母、数字和/或下划线组成。若要将可用属性名的逗号分隔列表传递给 pchPropertyName，请传入 NULL 指针。如果 pchValueBuffer 为 NULL，则 *punValueBufferSize 将包含建议的缓冲区大小；否则，它将表示实际复制到 pchValueBuffer 中的字节数。如果结果无法放入给定的缓冲区，可能会复制部分结果。

**参数:**

- `iDefinition` (`SteamItemDef_t`)
- `pchPropertyName` (`string`)
- `pchValueBuffer` (`out string`)
- `punValueBufferSizeOut` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = 256; string value; bool ok = SteamGameServerInventory.GetItemDefinitionProperty((SteamItemDef_t)123, "name", out value, ref size);
```

### RequestEligiblePromoItemDefinitionsIDs (静态)

```csharp
SteamAPICall_t RequestEligiblePromoItemDefinitionsIDs(CSteamID steamID)
```

<para>请求可为指定用户手动授予的“符合条件”促销物品列表。</para><para>这些是类型为“手动”且不会自动授予的促销物品。</para><para>此方法的一个典型用例是每周可用的物品。</para>

**参数:**

- `steamID` (`CSteamID`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerInventory.RequestEligiblePromoItemDefinitionsIDs(steamID);
```

### GetEligiblePromoItemDefinitionIDs (静态)

```csharp
bool GetEligiblePromoItemDefinitionIDs(CSteamID steamID, SteamItemDef_t[] pItemDefIDs, ref uint punItemDefIDsArraySize)
```

在处理 SteamInventoryEligiblePromoItemDefIDs_t 调用结果后，请使用此函数提取用户可通过 AddPromoItems() 调用人工授予的物品定义 ID 列表。

**参数:**

- `steamID` (`CSteamID`)
- `pItemDefIDs` (`SteamItemDef_t[]`)
- `punItemDefIDsArraySize` (`ref uint`)

**返回值:** `bool`

**用法示例:**
```csharp
uint size = 0; var itemDefIDs = Array.Empty<SteamItemDef_t>(); SteamGameServerInventory.GetEligiblePromoItemDefinitionIDs(steamID, itemDefIDs, ref size);
```

### StartPurchase (静态)

```csharp
SteamAPICall_t StartPurchase(SteamItemDef_t[] pArrayItemDefs, uint[] punArrayQuantity, uint unArrayLength)
```

启动给定物品定义的购买流程。如果 Steam 成功初始化交易，将发布回调 SteamInventoryStartPurchaseResult_t。一旦用户授权并完成购买，将发布回调 SteamInventoryResultReady_t。

**参数:**

- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `punArrayQuantity` (`uint[]`)
- `unArrayLength` (`uint`)

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerInventory.StartPurchase(itemDefs, quantities, (uint)itemDefs.Length);
```

### RequestPrices (静态)

```csharp
SteamAPICall_t RequestPrices()
```

<para>请求所有适用物品定义项的当前价格</para>

**返回值:** `SteamAPICall_t`

**用法示例:**
```csharp
SteamAPICall_t call = SteamGameServerInventory.RequestPrices();
```

### GetNumItemsWithPrices (静态)

```csharp
uint GetNumItemsWithPrices()
```

<para>返回具有价格的项目数量。需先调用 RequestPrices()。</para>

**返回值:** `uint`

**用法示例:**
```csharp
uint priceItemCount = SteamGameServerInventory.GetNumItemsWithPrices();
```

### GetItemsWithPrices (静态)

```csharp
bool GetItemsWithPrices(SteamItemDef_t[] pArrayItemDefs, ulong[] pCurrentPrices, ulong[] pBasePrices, uint unArrayLength)
```

<para>返回用户本地货币下的物品定义 ID 及其价格。</para> <para>需先调用 RequestPrices()。</para>

**参数:**

- `pArrayItemDefs` (`SteamItemDef_t[]`)
- `pCurrentPrices` (`ulong[]`)
- `pBasePrices` (`ulong[]`)
- `unArrayLength` (`uint`)

**返回值:** `bool`

**用法示例:**
```csharp
SteamGameServerInventory.GetItemsWithPrices(null, null, null, 0);
```

### GetItemPrice (静态)

```csharp
bool GetItemPrice(SteamItemDef_t iDefinition, out ulong pCurrentPrice, out ulong pBasePrice)
```

<para>获取物品定义 ID 对应的价格。</para> <para>如果该物品定义未存储价格，则返回 false。</para>

**参数:**

- `iDefinition` (`SteamItemDef_t`)
- `pCurrentPrice` (`out ulong`)
- `pBasePrice` (`out ulong`)

**返回值:** `bool`

**用法示例:**
```csharp
ulong currentPrice, basePrice; bool ok = SteamGameServerInventory.GetItemPrice((SteamItemDef_t)1001, out currentPrice, out basePrice);
```

### StartUpdateProperties (静态)

```csharp
SteamInventoryUpdateHandle_t StartUpdateProperties()
```

<para>创建请求以更新物品属性</para>

**返回值:** `SteamInventoryUpdateHandle_t`

**用法示例:**
```csharp
SteamInventoryUpdateHandle_t updateHandle = SteamGameServerInventory.StartUpdateProperties();
```

### RemoveProperty (静态)

```csharp
bool RemoveProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName)
```

移除物品上的该属性

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool removed = SteamGameServerInventory.RemoveProperty(updateHandle, itemId, "rarity");
if (removed) Console.WriteLine("Property removed");
```

### SetProperty (静态)

```csharp
bool SetProperty(SteamInventoryUpdateHandle_t handle, SteamItemInstanceID_t nItemID, string pchPropertyName, string pchPropertyValue)
```

访问器方法用于设置物品的属性

**参数:**

- `handle` (`SteamInventoryUpdateHandle_t`)
- `nItemID` (`SteamItemInstanceID_t`)
- `pchPropertyName` (`string`)
- `pchPropertyValue` (`string`)

**返回值:** `bool`

**用法示例:**
```csharp
bool ok = SteamGameServerInventory.SetProperty(updateHandle, itemId, "Quality", "Rare");
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
bool updated = SteamGameServerInventory.SetProperty(updateHandle, itemId, "CanTrade", true);
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
bool success = SteamGameServerInventory.SetProperty(updateHandle, itemId, "quality", 1L);
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
bool ok = SteamGameServerInventory.SetProperty(updateHandle, itemId, "damage_multiplier", 1.5f);
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
bool ok = SteamGameServerInventory.SubmitUpdateProperties(handle, out result);
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
string token = "item_token"; SteamInventoryResult_t resultHandle; bool ok = SteamGameServerInventory.InspectItem(out resultHandle, token);
```

