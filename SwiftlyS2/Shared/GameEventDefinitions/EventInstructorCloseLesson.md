# 🔌 EventInstructorCloseLesson

事件 "instructor_close_lesson"

**命名空间:** `SwiftlyS2.Shared.GameEventDefinitions`

**类型:** `interface`

**继承:** `IGameEvent\<EventInstructorCloseLesson\>`

## 📝 属性

| 名称 | 类型 | 访问方法 | 描述 |
|------|------|--------|------|
| `UserIdController` | `CCSPlayerController` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserIdPawn` | `CCSPlayerPawn` | get | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `UserId` | `int` | get, set | 本课程面向的玩家 <br/> 类型：玩家控制器 |
| `HintName` | `string` | get, set | 要开始课程的名称。必须与 instructor_lesson.txt 匹配 <br/> 类型：字符串 |

