# 📦 NativeVGUI

**命名空间:** `SwiftlyS2.Core.Natives`

**类型:** `class`

## ⚙️ 方法

### RegisterScreenText (静态)

```csharp
ulong RegisterScreenText()
```

**返回值:** `ulong`

### UnregisterScreenText (静态)

```csharp
void UnregisterScreenText(ulong textid)
```

**参数:**

- `textid` (`ulong`)

### ScreenTextCreate (静态)

```csharp
void ScreenTextCreate(ulong textid, Color col, int fontsize, bool drawBackground, bool isMenu)
```

**参数:**

- `textid` (`ulong`)
- `col` (`Color`)
- `fontsize` (`int`)
- `drawBackground` (`bool`)
- `isMenu` (`bool`)

### ScreenTextSetText (静态)

```csharp
void ScreenTextSetText(ulong textid, string text)
```

**参数:**

- `textid` (`ulong`)
- `text` (`string`)

### ScreenTextSetColor (静态)

```csharp
void ScreenTextSetColor(ulong textid, Color col)
```

**参数:**

- `textid` (`ulong`)
- `col` (`Color`)

### ScreenTextSetPosition (静态)

```csharp
void ScreenTextSetPosition(ulong textid, float x, float y)
```

0.0-1.0, where 0.0 is bottom/left, and 1.0 is top/right

**参数:**

- `textid` (`ulong`)
- `x` (`float`)
- `y` (`float`)

