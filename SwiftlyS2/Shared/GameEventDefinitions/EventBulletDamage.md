# 🔌 EventBulletDamage

事件 "bullet_damage"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventBulletDamage\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `VictimController` | `CCSPlayerController` | get | 受伤的玩家索引 <br/> 类型：玩家控制器与载具 |
| `VictimPawn` | `CCSPlayerPawn` | get | 受伤的玩家索引 <br/> 类型：玩家控制器与载具 |
| `Victim` | `int` | get, set | 受伤的玩家索引 <br/> 类型：玩家控制器与载具 |
| `AttackerController` | `CCSPlayerController` | get | 攻击的玩家索引 <br/> 类型：玩家控制器与游戏体 |
| `AttackerPawn` | `CCSPlayerPawn` | get | 攻击的玩家索引 <br/> 类型：玩家控制器与游戏体 |
| `Attacker` | `int` | get, set | 攻击的玩家索引 <br/> 类型：玩家控制器与游戏体 |
| `Distance` | `float` | get, set | 子弹击中玩家前飞行的距离 <br/> 类型：float |
| `DamageDirX` | `float` | get, set | 子弹的方向向量 <br/> 类型：float |
| `DamageDirY` | `float` | get, set | 子弹的方向向量 <br/> 类型：float |
| `DamageDirZ` | `float` | get, set | 子弹的方向向量 <br/> 类型：float |
| `NumPenetrations` | `byte` | get, set | 穿透的表面数量 <br/> 类型：字节 |
| `NoScope` | `bool` | get, set | 射手是否被瞬狙？<br/>类型：bool |
| `InAir` | `bool` | get, set | 射手是否处于跳跃状态？<br/>类型：布尔值 |
| `ShootAngX` | `float` | get, set | 射击角度 x <br/> 类型：浮点数 |
| `ShootAngY` | `float` | get, set | 射击角度 Y <br/> 类型：浮点数 |
| `ShootAngZ` | `float` | get, set | 射击角度 Z <br/> 类型：浮点数 |
| `AimPunchX` | `float` | get, set | 瞄准偏移 X <br/> 类型：浮点数 |
| `AimPunchY` | `float` | get, set | 瞄准偏移 Y <br/> 类型：浮点数 |
| `AimPunchZ` | `float` | get, set | 瞄准偏移 Z <br/> 类型：浮点数 |
| `AttackTickCount` | `int` | get, set | 攻击节拍 <br/> 类型：int |
| `AttackTickFrac` | `float` | get, set | 攻击分数 <br/> 类型：浮点数 |
| `RenderTickCount` | `int` | get, set | 渲染刻度 <br/> 类型：int |
| `RenderTickFrac` | `float` | get, set | 渲染分数 <br/> 类型：浮点数 |
| `InaccuracyTotal` | `float` | get, set | 总不准确度 <br/> 类型：浮点数 |
| `InaccuracyMove` | `float` | get, set | 移动误差 <br/> 类型：浮点数 |
| `InaccuracyAir` | `float` | get, set | 空气偏差 <br/> 类型：浮点数 |
| `RecoilIndex` | `float` | get, set | 后坐力指数。是的，这确实是一个浮点数。<br/>类型：浮点数 |
| `Type` | `int` | get, set | 延迟补偿类型 <br/> 类型：int |

