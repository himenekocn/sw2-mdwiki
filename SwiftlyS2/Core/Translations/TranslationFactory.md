# 📦 TranslationFactory

**命名空间:** `SwiftlyS2.Core.Translations`

**类型:** `class`

## ⚙️ 方法

### Create (静态)

```csharp
TranslationResource Create(string resourceDir)
```

Creates a new <see cref="TranslationResource"/> from the specified resource directory.

**参数:**

- `resourceDir` (`string`) - The directory containing the translation files.

**返回值:** `TranslationResource` - A <see cref="TranslationResource"/> containing the translation files.

### CreateLocalizer (静态)

```csharp
Localizer CreateLocalizer(TranslationResource resource, Language language)
```

**参数:**

- `resource` (`TranslationResource`)
- `language` (`Language`)

**返回值:** `Localizer`

