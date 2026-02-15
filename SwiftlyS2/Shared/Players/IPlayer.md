# 🔌 IPlayer

**命名空间:** `SwiftlyS2.Shared.Players`

**类型:** `interface`

**继承:** `IEquatable\<IPlayer\>`

## 📝 属性

| 名称 | 类型 | 访问器 | 描述 |
|------|------|--------|------|
| `PlayerID` | `int` | get | Gets the unique identifier for the player. |
| `SessionId` | `ulong` | get | Gets the session ID for the player. |
| `UserID` | `int` | get | Gets the user ID for the player. |
| `Slot` | `int` | get | Gets the slot of the player. Equals to the player ID. |
| `Name` | `string` | get | Gets the name of the player. |
| `IsFakeClient` | `bool` | get | Whether the client is a bot. |
| `IsAuthorized` | `bool` | get | Whether the current user is authorized by Steam. |
| `ConnectedTime` | `uint` | get | Gets the total time, in seconds, that the connection has been active. |
| `SteamID` | `ulong` | get | Gets the unique Steam identifier associated with the user. |
| `UnauthorizedSteamID` | `ulong` | get | Gets the Steam ID that was not verified yet. |
| `IsAlive` | `bool` | get | Gets a value indicating whether the player is currently alive. |
| `Controller` | `CCSPlayerController` | get | Gets the player controller associated with the player. |
| `RequiredController` | `CCSPlayerController` | get | Gets the player controller associated with the player. Requires the controller to be valid. <exception cref="InvalidOperationException">Thrown when the controller is not valid.</exception> |
| `Pawn` | `CBasePlayerPawn?` | get | Gets the pawn associated with the player. |
| `RequiredPawn` | `CBasePlayerPawn` | get | Gets the pawn associated with the player. Requires the pawn to be valid. <exception cref="InvalidOperationException">Thrown when the pawn is not valid.</exception> |
| `PlayerPawn` | `CCSPlayerPawn?` | get | Gets the player pawn associated with the player. |
| `RequiredPlayerPawn` | `CCSPlayerPawn` | get, set | Gets the player pawn associated with the player. Requires the player pawn to be valid. <exception cref="InvalidOperationException">Thrown when the player pawn is not valid.</exception> |
| `PressedButtons` | `GameButtonFlags` | get, set | Gets the set of game buttons that are currently pressed. |
| `IPAddress` | `string` | get, set | Gets the IP address associated with the player. |
| `VoiceFlags` | `VoiceFlagValue` | get, set | Gets or sets the set of flags that specify voice options or features to be applied. |
| `PlayerLanguage` | `Language` | get | Gets the language for the player. |
| `IsFirstSpawn` | `bool` | get | Indicates whether this is the player's first spawn. |
| `IsValid` | `bool` | get | Checks if the player is valid (has controller, is not HLTV, is connected and has pawn). |

