# 🔌 EventInstructorStartLesson

事件 "instructor_start_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorStartLesson\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `HintName` | `string` | get, set | 要开始课程的名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |
| `HintTarget` | `int` | get, set | 提示信息应显示的实体ID。如果控制器目标为空，则留空 <br/> 类型：long |
| `VrMovementType` | `byte` | get, set | 类型：字节 |
| `VrSingleController` | `bool` | get, set | 类型：布尔值 |
| `VrControllerType` | `byte` | get, set | 类型：字节 |

