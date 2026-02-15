# 📦 NativeEvents

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### RegisterOnGameTickCallback (静态)

```csharp
void RegisterOnGameTickCallback(nint callback)
```

bool simulating, bool first, bool last -> void

**参数:**

- `callback` (`nint`)

### RegisterOnClientConnectCallback (静态)

```csharp
void RegisterOnClientConnectCallback(nint callback)
```

int32 playerid -> bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

### RegisterOnClientDisconnectCallback (静态)

```csharp
void RegisterOnClientDisconnectCallback(nint callback)
```

int32 playerid, ENetworkDisconnectReason (int32) reason -> void

**参数:**

- `callback` (`nint`)

### RegisterOnClientKeyStateChangedCallback (静态)

```csharp
void RegisterOnClientKeyStateChangedCallback(nint callback)
```

int32 playerid, string key, bool pressed -> void

**参数:**

- `callback` (`nint`)

### RegisterOnClientProcessUsercmdsCallback (静态)

```csharp
void RegisterOnClientProcessUsercmdsCallback(nint callback)
```

int32 playerid, ptr* usercmds, int numcmds, bool paused, float margin -> void

**参数:**

- `callback` (`nint`)

### RegisterOnClientPutInServerCallback (静态)

```csharp
void RegisterOnClientPutInServerCallback(nint callback)
```

int32 playerid, int32 client_kind (0 -> player, 1 -> bot, 2 -> unknown) -> void

**参数:**

- `callback` (`nint`)

### RegisterOnClientSteamAuthorizeCallback (静态)

```csharp
void RegisterOnClientSteamAuthorizeCallback(nint callback)
```

int32 playerid -> void

**参数:**

- `callback` (`nint`)

### RegisterOnClientSteamAuthorizeFailCallback (静态)

```csharp
void RegisterOnClientSteamAuthorizeFailCallback(nint callback)
```

int32 playerid -> void

**参数:**

- `callback` (`nint`)

### RegisterOnEntityCreatedCallback (静态)

```csharp
void RegisterOnEntityCreatedCallback(nint callback)
```

CEntityInstance* entity

**参数:**

- `callback` (`nint`)

### RegisterOnEntityDeletedCallback (静态)

```csharp
void RegisterOnEntityDeletedCallback(nint callback)
```

CEntityInstance* entity

**参数:**

- `callback` (`nint`)

### RegisterOnEntityParentChangedCallback (静态)

```csharp
void RegisterOnEntityParentChangedCallback(nint callback)
```

CEntityInstance* entity, CEntityInstance* newparent

**参数:**

- `callback` (`nint`)

### RegisterOnEntitySpawnedCallback (静态)

```csharp
void RegisterOnEntitySpawnedCallback(nint callback)
```

CEntityInstance* entity

**参数:**

- `callback` (`nint`)

### RegisterOnMapLoadCallback (静态)

```csharp
void RegisterOnMapLoadCallback(nint callback)
```

string mapname

**参数:**

- `callback` (`nint`)

### RegisterOnMapUnloadCallback (静态)

```csharp
void RegisterOnMapUnloadCallback(nint callback)
```

string mapname

**参数:**

- `callback` (`nint`)

### RegisterOnEntityTakeDamageCallback (静态)

```csharp
void RegisterOnEntityTakeDamageCallback(nint callback)
```

CBaseEntity* entity, CTakeDamageInfo* info -> bool (true -> ignored, false -> supercede)

**参数:**

- `callback` (`nint`)

### RegisterOnPrecacheResourceCallback (静态)

```csharp
void RegisterOnPrecacheResourceCallback(nint callback)
```

IEntityResourceManifest* pResourceManifest

**参数:**

- `callback` (`nint`)

### RegisterOnPreworldUpdateCallback (静态)

```csharp
void RegisterOnPreworldUpdateCallback(nint callback)
```

bool simulating

**参数:**

- `callback` (`nint`)

### RegisterOnStartupServerCallback (静态)

```csharp
void RegisterOnStartupServerCallback(nint callback)
```

void

**参数:**

- `callback` (`nint`)

### RegisterOnClientVoiceCallback (静态)

```csharp
void RegisterOnClientVoiceCallback(nint callback)
```

int32 playerid

**参数:**

- `callback` (`nint`)

