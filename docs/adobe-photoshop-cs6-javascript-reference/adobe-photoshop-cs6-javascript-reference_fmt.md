
# Adobe Photoshop CS6 JavaScript 参考

Adobe Photoshop CS6 JavaScript 脚本参考

## Adobe Photoshop CS6 脚本参考

### 引言

本参考手册描述了 Adobe® Photoshop® CS6® JavaScript™ 类型库中的对象与方法。配套文档《Photoshop CS6 脚本编写指南》介绍了基本的脚本编写概念与 Photoshop 对象模型。本文档提供了 Photoshop 对象模型的详细参考信息，以及关于 JavaScript 特定功能的额外说明。

Adobe Photoshop CS6 采用了 `ExtendScript`，这是 Adobe 对 JavaScript 的扩展实现。有关更多信息，请参阅 [Adobe Photoshop CS6 中的 JavaScript 支持](#Adobe Photoshop CS6 中的 JavaScript 支持)。

本书包含以下部分：

- 本引言，描述了 Adobe Photoshop CS6 中的脚本编写支持，并列出了自上一个版本以来 JavaScript 接口的变化。
- [JavaScript 对象参考](#JavaScript 对象参考)，提供了所有 Photoshop DOM 对象与命令的完整参考。
- [脚本编写常量](#脚本编写常量)，列出了 Photoshop 类型库中使用的所有枚举。

### Adobe Photoshop CS6 中的 JavaScript 支持

JavaScript 文件要被 Photoshop 识别为有效的脚本文件，其扩展名必须为 `.js` 或 `.jsx`。

在 Mac OS 上，使用这两种扩展名的脚本功能没有区别。在 Windows 上，如果从 Photoshop 内部打开脚本文件，使用 `.js` 和 `.jsx` 扩展名也没有区别。但是，如果通过双击启动脚本，`.js` 扩展名的脚本将使用 `Microsoft JScript` 引擎解释，并且无法启动 Adobe Photoshop CS6。对于 Windows 系统，建议使用 `.jsx` 扩展名，因为它会使用 `ExtendScript` 引擎来解释脚本。

所有 Adobe Creative Suite 6 应用程序（包括 Adobe Photoshop CS6）都使用 `ExtendScript`，这是 Adobe 对 JavaScript 的扩展实现。`ExtendScript` 文件以 `.jsx` 扩展名作为标识。`ExtendScript` 提供了所有标准 JavaScript 功能，以及额外的功能和实用程序，例如：

- 调试环境（ExtendScript Toolkit）
- 本地化实用程序
- 允许您合并脚本并将其定向到特定应用程序的工具
- 平台无关的文件和文件夹表示

许多 JavaScript 对象和方法使用 `ExtendScript` 中定义的对象，例如 `File` 对象、`Folder` 对象和 `UnitValue` 对象。因此，建议为您的脚本文件使用 `.jsx` 扩展名。

有关这些功能和其他功能的详细信息，请参阅《JavaScript 工具指南 CS6》。该文档随 Creative Suite 6 应用程序安装在以下位置：

- 在 Windows 上：
```
C:\Program Files\Adobe\Adobe Utilities\ExtendScript Toolkit CS6\SDK
```

### 脚本编写常量

- `ColorSpaceType`
- `CopyrightedType`
- `CreateFields`
- `CropToType`
- `DCSType`
- `DepthMapSource`
- `DescValueType`
- `DialogModes`
- `Direction`
- `DisplacementMapType`
- `Dither`
- `DocPositionStyle`
- `DocumentFill`
- `DocumentMode`
- `EditLogItemsType`
- `ElementPlacement`
- `EliminateFields`
- `ExportType`
- `Extension`
- `FileNamingType`
- `FontPreviewType`
- `FontSize`
- `ForcedColors`
- `FormatOptions`
- `GalleryConstrainType`
- `GalleryFontType`
- `GallerySecurityTextColorType`
- `GallerySecurityTextPositionType`
- `GallerySecurityTextRotateType`
- `GallerySecurityType`
- `GalleryThumbSizeType`
- `Geometry`
- `GridLineStyle`
- `GridSize`
- `GuideLineStyle`
- `IllustratorPathType`
- `Intent`
- `Justification`
- `Language`
- `LayerCompression`
- `LayerKind`
- `LensType`
- `MagnificationType`
- `MatteType`
- `MeasurementRange`
- `MeasurementSource`
- `NewDocumentMode`
- `NoiseDistribution`
- `OffsetUndefinedAreas`
- `OpenDocumentMode`
- `OpenDocumentType`
- `OperatingSystem`
- `Orientation`
- `OtherPaintingCursors`
- `PaintingCursors`
- `PaletteType`
- `PathKind`
- `PDFCompatibility`
- `PDFEncoding`
- `PDFResample`
- `PDFStandard`
- `PhotoCDColorSpace`
- `PhotoCDSize`
- `PICTBitsPerPixel`
- `PICTCompression`
- `PicturePackageTextType`
- `PointKind`
- `PointType`
- `PolarConversionType`
- `Preview`
- `PrintColorHandling`
- `PurgeTarget`
- `QueryStateType`
- `RadialBlurMethod`
- `RadialBlurQuality`
- `RasterizeType`
- `ReferenceFormType`
- `ResampleMethod`
- `RippleSize`
- `SaveBehavior`
- `SaveDocumentType`
- `SaveEncoding`
- `SaveLogItemsType`
- `SaveOptions`
- `SelectionType`
- `ShapeOperation`
- `SmartBlurMode`
- `SmartBlurQuality`
- `SourceSpaceType`
- `SpherizeMode`
- `StrikeThruType`
- `StrokeLocation`
- `TargaBitsPerPixel`
- `TextCase`
- `TextComposer`
- `TextType`
- `TextureType`
- `TIFFEncoding`
- `ToolType`
- `TransitionType`
- `TrimType`
- `TypeUnits`
- `UndefinedAreas`
- `UnderlineType`
- `Units`
- `Urgency`
- `WarpStyle`
- `WaveType`
- `WhiteBalanceType`
- `ZigZagType`

### 执行脚本

Adobe Photoshop CS6 界面包含一个“脚本”菜单（`文件 > 脚本`），可快速便捷地访问您的 JavaScript。脚本可以直接作为菜单项列出，运行时只需选择它们，或者您可以浏览并运行文件系统中的任何 JavaScript。

如果 Adobe Photoshop CS6 在脚本执行过程中遇到错误，它会显示错误消息。

### 安装脚本

要将 JavaScript 安装到“脚本”菜单中，请将其放入 `Scripts` 文件夹（`Photoshop CS6/Presets/Scripts`）。`Scripts` 文件夹中脚本的名称（不含文件扩展名）将显示在“脚本”菜单中。可以在“脚本”菜单中安装任意数量的脚本。

在 Adobe Photoshop CS6 运行时添加到 `Scripts` 文件夹的脚本，在下次启动应用程序之前不会出现在“脚本”菜单中。

在 `Scripts` 文件夹及其子文件夹中找到的所有脚本都会显示在`文件 > 脚本` 菜单，增加层级。

### 执行其他脚本

`脚本`菜单末尾的`浏览`项（`文件 > 脚本 > 浏览`）允许您执行未安装在 `Scripts` 文件夹中的脚本。您也可以使用“浏览”来选择文件。浏览对话框中仅显示 `.js` 或 `.jsx` 文件。选择文件后，执行方式与安装的脚本相同。

### 启动脚本

启动时，Adobe Photoshop CS6 会执行在启动文件夹中找到的所有 `.jsx` 文件。

- 在 Windows 上，用户自定义文件夹是：
`C:\Program Files\Common Files\Adobe\Startup Scripts\Adobe Photoshop`
- 在 Mac OS 上，用户自定义文件夹是：
`~/Library/Application Support/Adobe/Startup Scripts/Adobe Photoshop`

如果脚本仅供 Photoshop 执行，则必须包含类似的代码：
```
if(appName == "photoshop" ) {
    //继续脚本
}
```
更多详细信息，请参阅《JavaScript 工具指南6》。

### 对象模型用法与命名

JavaScript API 遵循命名约定，所有类（对象类型）均以大字母开头并采用大小写。通常在 JavaScript 中您使用 `new` 运算符来实例化：
```
new ClassName();
```
然而，在 Photoshop 对象模型中，通常无需这样做。主要的对象类型被收集到集合中；例如，一组 `Document` 对象包含在一个 `Documents` 集合中。然后可以通过对象层次结构中相应的属性访问集合。

例如，所有打开文档的集合包含在顶层的 `Application` 对象中。可以通过全局变量 `app` 访问，或者直接引用其属性：
```
app.documents[0] // 获取第一个文档
```
集合属性与对象同名，但以小字母开头。例如，`Document` 包含一个 `layerSets` 集合，一个 `LayerSet` 包含一个 `artLayers` 集合。访问集合中的 `ArtLayer` 对象：
```
var myLayer = activeDocument.layerSets[0].artLayers[0];
```
这些集合视为数组，这对迭代很有用。它们还提供方法来创建其包含的对象，以及按名称访问它们：
```
var newLayer = activeDocument.artLayers.add(); // 创建一个新的 ArtLayer 对象
newLayer.name = "My Layer"; // 命名以便将来引用
...
var layerRef = activeDocument.artLayers.getByName("My Layer");
```
某些对象如 `app.fonts` 集合中包含的 `Font` 对象是由应用程序创建的，而不是由您的脚本创建。脚本确实使用 `new` 运算符来创建辅助对象，例如封装了特定格式打开或保存文档的选项集：
```
var opts = new PDFOpenOptions();
opts.page = 10;
app.open(myPDFFile, opts);
```

### 与早期版本的变更——CS6

是对 Adobe Photoshop CS6 中 JavaScript 对象模型和语言支持的更改：

- 新方法和属性：
- `getLargeInteger` 已添加到 `ActionDescriptor` 和 `ActionList` 对象。
- `putLargeInteger` 已添加到 `ActionDescriptor` 和 `ActionList` 对象。
- `compression` 方法已添加到 `PNGSaveOptions` 对象。
- 修改的枚举：
- `LARGEINTEGERTYPE` 已添加到 `DescValueType` 枚举。
- `EXTRALARGE` 和 `HUGE` 已添加到 `FontPreviewType` 枚举。

## 2 JavaScript 对象参考

Photoshop 对象（CS6 的 JavaScript 类型库）按字母顺序和表格格式在本章中呈现。给出了对象模型类的示例代码，以帮助说明语法以及类的用法。

### 对象描述

属性和方法在每个对象的单独表格中描述。以下部分描述了这些描述中使用的约定。

### 属性表示法

属性表列出以下内容：

- 每个对象中定义的属性。
- 每个属性的值类型。当值类型是常量或另一个对象时，该值是链接到常量或对象列表的超文本链接。
- 属性的输入状态：只读或读写。
- 解释属性功能的描述。

| 属性 | 值类型 | 功能 |
| :--- | :--- | :--- |
| `displayDialogs` | [DialogModes] | 读写。应用程序的对话框模式，用于控制运行脚本时显示哪些类型的对话框。 |

对于常量，如示例中的 [DialogModes]，单击链接可转到显示允许值的表格。常量由对象表示，允许值是这些对象的属性。以`常量名.值` 的形式指定常量。例如：
```
app.displayDialogs = DialogModes.ERROR;
```

### 方法表示法

方法表列出以下内容：

- 方法名称。
- 参数列表。
- 与每个参数对应的参数值类型行。
- 返回值类型。
- 描述方法功能的描述，以及需要时对参数的进一步描述。

| 方法 | 参数类型 | 返回值 | 功能 |
| :--- | :--- | :--- | :--- |
| `crop`<br>(bounds<br>[, angle]<br>[, width]<br>[, height]) | 4 个 [UnitValue] 的数组<br>number<br>[UnitValue]<br>[UnitValue] | | 裁剪文档。`bounds` 参数是裁剪后区域四个坐标[左, 上, 右, 下]。 |

参数可以是必需的或可选的。可选参数在表中由方括号（[]）表示。在示例中，第一个参数 `bounds` 是必需的。其余

您必须为每个必需参数传递值。如果没有要传递的剩余值，您可以省略可选参数；但是如果您希望使用任何指定参数的默认值，请传递 `undefined` 作为占位符。您必须按照列出的顺序输入值，以便 JavaScript 编译器知道您正在输入哪个值。

例如，以下仅传递必需参数（使用先前定义的变量作为边界）：
```
app.activeDocument.crop(myRegion);
```
以下跳过 `angle` 参数，指定 `width` 值并省略最后的 `height` 值：
```
var myWidth = new UnitValue("500 pixels");
app.executeAction(myRegion, undefined, myWidth);
```

### ActionDescriptor

此对象提供了一种类似字典的机制，用于以键值对的形式存储。它用于对 Photoshop 进行底层访问。有关此用法的示例，请参阅第168 页的选区脚本。

许多配置文件使用序列化的动作描述符来表示其数据。例如，它用于封装 `Application.playbackParameters` 中的播放选项，并由 `Application.getCustomOptions()` 返回。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `count` | `number` | 只读。描述符中包含的键的数量。 |
| `typename` | `string` | 只读。被引用的 `actionDescriptor` 对象的类名。 |

#### 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `clear`<br>() | | | 清除描述符。 |
| `erase`<br>(key) | `number` | | 从描述符中擦除一个键。 |


```markdown
| `fromStream` `(value)` | `string` | 从字节流创建一个描述符；用于从磁盘读取。 |
| `getBoolean` `(key)` | `number` | `boolean` | 获取一个布尔类型的键的值。 |
| `getClass` `(key)` | `number` | `number` | 获取一个类类型的键的值。 |
| `getData` `(key)` | `number` | `string` | 获取原始字节数据作为字符串值。 |
| `getDouble` `(key)` | `number` | `number` | 获取一个双精度类型的键的值。 |
| `getEnumerationType` `(key)` | `number` | `number` | 获取一个键的枚举类型。 |
| `getEnumerationValue` `(key)` | `number` | `number` | 获取一个键的枚举值。 |
| `getInteger` `(key)` | `number` | `number` | 获取一个整数类型的键的值。 |
| `getKey` `(index)` | `number` | `number` | 根据索引获取第 N 个键的 ID。 |
| `getLargeInteger` `(key)` | `number` | `number` | 获取一个大整数类型的键的值。 |
| `getList` `(key)` | `number` | `ActionList` | 获取一个列表类型的键的值。 |
| `getObjectType` `(key)` | `number` | `number` | 获取一个对象类型键中对象的类 ID。 |
| `getObjectValue` `(key)` | `number` | `ActionDescriptor` | 获取一个对象类型的键的值。 |
| `getPath` `(key)` | `number` | `File` | 获取一个文件类型的键的值。 |
| `getReference` `(key)` | `number` | `ActionReference` | 获取一个 ActionReference类型的键的值。 |
| `getString` `(key)` | `number` | `string` | 获取一个字符串类型的键的值。 |
| `getType` `(key)` | `number` | `DescValueType` | 获取一个键的类型。 |
| `getUnitDoubleType` `(key)` | `number` | `number` | 获取一个 UnitDouble 类型键的单位类型。 |
| `getUnitDoubleValue` `(key)` | `number` | `number` | 获取一个 UnitDouble 类型键的值。 |
| `hasKey` `(key)` | `number` | `boolean` | 检查描述符是否包含提供的键。 |
| `isEqual` `(otherDesc)` | `ActionDescriptor` | `boolean` | 确定此描述符是否与另一个描述符相同。 |
| `putBoolean` `(key, value)` | `number`<br>`boolean` | | 为布尔类型的键设置值。 |
| `putClass` `(key, value)` | `number`<br>`number` | | 为类类型的键设置值。 |
| `putData` `(key, value)` | `number`<br>`string` | | 将原始字节数据作为字符串值放入。 |
| `putDouble` `(key, value)` | `number`<br>`number` | | 为双精度类型的键设置值。 |
| `putEnumerated` `(key, enumType, value)` | `number`<br>`number` `number` | | 为一个键设置枚举类型和值。 |
| `putInteger` `(key, value)` | `number`<br>`number` | | 为整数类型的键设置值。 |
| `putLargeInteger` `(key, value)` | `number`<br>`number` | | 为大整数类型的键设置值。 |
| `putList` `(key, value)` | `number`<br>`ActionList` | | 为 ActionList 对象类型的键设置值。 |
| `putObject` `(key, classID, value)` | `number`<br>`number`<br>`ActionDescriptor` | | 为一个对象类型的键设置值，该对象由动作描述符表示。 |
| `putPath` `(key, value)` | `number`<br>`File` | | 为路径类型的键设置值。 |
| `putReference` `(key, value)` | `number`<br>`ActionReference` | | 为对象引用类型的键设置值。 |
| `putString` `(key, value)` | `number`<br>`string` | | 为字符串类型的键设置值。 |
| `putUnitDouble` `(key, unitID, value)` | `number`<br>`number`<br>`number` | | 为一个单位值（格式为双精度数）类型的键设置值。 |
| `toStream` `()` | | `string` | 将整个描述符作为字节流获取，用于写入磁盘。 |

### ActionList

此对象提供了一种类似数组的机制来存储数据。它可用于对 Photoshop 进行底层访问。

此对象非常适合存储相同类型的数据。列表中的所有项必须是同一类型。

你可以使用 `put` 方法（例如 `putBoolean()`）来附加新元素，并可以使用 `clear()` 清除整个列表，但不能以其他方式修改列表。

**注意：** `ActionList` 对象是动作管理器功能的一部分。有关使用动作管理器的详细信息，请参阅 `Photoshop CS6脚本指南`。

#### 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `count` | `number` | 只读。组成动作的数量。 |
| `typename` | `string` | 只读。被引用的 `ActionList` 对象的类名。 |

#### 方法
除了 `clear()` 方法外，你可以使用此对象来获取列表中特定类型的数据或设置（放入）值。

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `clear()` | | | 清除列表。 |
| `getBoolean(index)` | `number` | `boolean` | 获取一个布尔类型元素的值。 |
| `getClass(index)` | `number` | `number` | 获取一个类类型元素的值。 |
| `getData(index)` | `number` | `string` | 获取原始字节数据。 |
| `getDouble(index)` | `number` | `number` | 获取一个双精度类型元素的值。 |
| `getEnumerationType(index)` | `number` | `number` | 获取一个枚举类型。 |
| `getEnumerationValue(index)` | `number` | `number` | 获取一个枚举值。 |
| `getInteger(index)` | `number` | `number` | 获取一个整数类型元素的值。 |
| `getLargeInteger(index)` | `number` | `number` | 获取一个大整数类型元素的值。 |
| `getList(index)` | `number` | `ActionList` | 获取一个列表类型元素的值。 |
| `getObjectType(index)` | `number` | `number` | 获取一个对象类型元素的 ID。 |
| `getObjectValue(index)` | `number` | `ActionDescriptor` | 获取一个对象类型元素的值。 |
| `getPath(index)` | `number` | `File` | 获取一个文件类型元素的值。 |
| `getReference(index)` | `number` | `ActionReference` | 获取一个 ActionReference 类型元素的值。 |
| `getString(index)` | `number` | `string` | 获取一个字符串类型元素的值。 |
| `getType(index)` | `number` | `DescValueType` | 获取一个元素的类型。 |
| `getUnitDoubleType(index)` | `number` | `number` | 获取一个双精度类型元素的单位类型。 |
| `getUnitDoubleValue(index)` | `number` | `number` | 获取一个双精度类型元素的单位值。 |
| `putBoolean(value)` | `boolean` | | 附加一个新值，true 或 false。 |
| `putClass(value)` | `number` | | 附加一个新值，一个类或数据类型。 |
| `putData(value)` | `string` | | 附加一个新值，包含原始字节数据的字符串。 |
| `putDouble(value)` | `number` | | 附加一个新值，一个双精度数。 |
| `putEnumerated(enumType, value)` | `number`, `number` | | 附加一个新值，一个枚举（常量）值。 |
| `putInteger(value)` | `number` | | 附加一个新值，一个整数。 |
| `putLargeInteger(value)` | `number` | | 附加一个新值，一个大整数。 |
| `putList(value)` | `ActionList` | | 附加一个新值，一个嵌套的动作列表。 |

### ActionReference

此对象提供关于操作引用的信息。例如，当引用对象的名称时，你可能会使用 `keyName`。引用还需要知道你正在引用的具体名称。在这种情况下，你可以使用 `classDocument` 来指代文档名称，或使用 `classLayer` 来指代图层名称。它可以用于对 Photoshop 进行底层访问。包含与 `ActionDescriptor` 关联的数据。

#### 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `typename` | `string` | 只读。引用的 Action 对象的类名。 |

#### 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `getContainer()` | | `ActionReference` | 获取此引用中包含的引用。容器引用为该引用提供了额外的部分。这看起来像是另一个引用，但它实际上是同一个引用的一部分。 |
| `getDesiredClass()` | | `number` | 获取一个表示对象类的数字。 |
| `getEnumeratedType()` | | `number` | 获取枚举类型。 |
| `getEnumeratedValue()` | | `number` | 获取枚举值。 |
| `getForm()` | | `ReferenceFormType` | 获取此操作引用的形式。 |
| `getIdentifier()` | | `number` | 对于形式为标识符的引用，获取其标识符值。 |
| `getIndex()` | | `number` | 获取列表或数组中引用的索引值。 |
| `getName()` | | `string` | 获取引用的名称。 |
| `getOffset()` | | `number` | 获取对象索引值的偏移量。 |
| `getProperty()` | | `number` | 获取属性 ID 值。 |
| `putClass(desiredClass)` | | | 附加一个新值，一个类。 |
| `putEnumerated(enumType, value)` | `number`, `number` | | 附加一个新值，一个枚举值。 |
| `getIdentifier(value)` | | | 附加一个新值，一个标识符。 |
| `getIndex()` | | | 附加一个新值，一个索引。 |

### Application

Adobe Photoshop CS6 应用程序对象，它是模型的根，提供对所有对象的访问。此对象提供应用程序范围，例如应用程序默认字体。它提供了许多方法，用于打开文件和加载文档。要访问属性和方法，你可以使用预定义的全局变量 `app`。例如：

```
var docRef = app.documents.add(800, 600, 72, "docRef", DocumentMode.RGB);
```

这种用法可能有些模糊为了清晰起见，建议你使用 `app` 的显式引用。

#### 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `activeDocument` | `Document` | 读写。最前面的文档。设置此属性等同于在 Photoshop CS6 应用程序中点击一个打开的文档将其到前面。**提示：** 如果没有打开的文档，访问此属性将引发异常。 |
| `backgroundColor` | `SolidColor` | 读写。文档的默认颜色和颜色样式。 |
| `build` | `string` | 只读。应用程序的信息。 |
| `colorSettings` | `string` | 读写。当前颜色设置的名称，即通过“编辑 > 颜色设置”所选的名称。 |
| `displayDialogs` | `DialogModes` | 读写。应用程序的对话框模式，控制运行脚本时应显示哪些类型的对话框。 |
| `documents` | `Documents` | 只读。打开的文档集合。这是访问当前在应用程序中打开的文档的主要入口点。数组允许访问任何打开的文档，或遍历所有打开的文档。 |
| `fonts` | `TextFonts` | 只读。此系统上安装的字体。 |
| `foregroundColor` | `SolidColor` | 读写。默认的前景色（用于绘制、填充和描边选区）。 |
| `freeMemory` | `number` | 只读。Adobe Photoshop CS6 可用的未使用内存量。 |
| `locale` | `string` | 只读。应用程序的语言区域。Adobe 区域代码由一个 2 字母的 ISO-639 语言代码和一个可选的 2 字母的 ISO 3166 国家代码组成，中间用下划线分隔。大小写敏感。例如，`en_US`、`en_UK`、`ja_JP`、`de_DE`、`fr_FR`。 |
```

---

| `macintoshFileTypes` | `string` 数组 | 只读。Adobe Photoshop CS6 可以打开的文件图像类型列表。 |
| `measurementLog` | `MeasurementLog` | 测量日志。 |
| `name` | `string` | 只读。应用程序的名称。 |
| `notifiers` | `Notifiers` | 只读。当前配置的通知程序集合（在 Adobe Photoshop CS6 应用程序的“脚本事件管理器”菜单中）。 |
| `notifiersEnabled` | `boolean` | 读写。如果所有通知程序都已启用，则为 `True`。 |
| `path` | `File` | 只读。Adobe Photoshop CS6 应用程序位置的完整路径。 |
| `playbackDisplayDialogs` | `DialogModes` | 读写。播放模式的对话框模式，控制使用动作调板播放录制的动作时应显示哪种类型的对话框。 |
| `playbackParameters` | `ActionDescriptor` | 读写。存储和检索作为录制动作一部分使用的参数。例如，可用于控制播放速度。 |
| `preferences` | `Preferences` | 只读。应用程序首选项设置（等同于在 Windows 的 Adobe Photoshop CS6 应用程序中选择**编辑 > 首选项**，或在 Mac OS 中选择 **Photoshop > 首选项**）。 |
| `preferencesFolder` | `File` | 只读。首选项文件夹的完整路径。 |
| `recentFiles` | `File` 数组 | 只读。“最近使用的文件”列表中的文件。 |
| `scriptingBuildDate` | `string` | 只读。脚本接口的构建日期。 |
| `scriptingVersion` | `string` | 只读。脚本接口的版本。 |
| `systemInformation` | `string` | 只读。应用程序和系统的运行时详细信息。 |
| `typename` | `string` | 只读。引用的 `app` 对象的类名。 |
| `version` | `string` | 只读。你正在运行的 Adobe Photoshop 应用程序的版本。 |
| `windowsFileTypes` | `string 数组` | 只读。Adobe Photoshop CS6 可以打开的文件图像扩展名列表。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `batch(inputFiles, action, from [, options])` | `File 数组`, `string`, `string`, [`BatchOptions`](https://example.com) | `string` | 运行批处理自动化例程（类似于**文件 > 自动 > 批处理** 命令）。`inputFiles` 参数指定要由批处理命令处理的文件的来源。 |
| `beep()` | | | 发出“哔”声。 |
| `bringToFront()` | | | 使 Adobe Photoshop CS6 成为活动（最前面的）应用程序。 |
| `charIDToTypeID(charID)` | `string` | `number` | 将四字符代码（字符 ID）转换为运行时 ID。 |
| `doAction(action, from)` | `string`, `string` | | 从动作调板播放一个动作。`action` 参数是动作的名称，`from` 参数是动作组的名称。 |
| `eraseCustomOptions(key)` | `string` | | 从 Photoshop 注册表中删除具有指定 ID 值的用户对象。 |
| `executeAction(eventID [, descriptor] [, displayDialogs])` | `number`, [`ActionDescriptor`](https://example.com), [`DialogModes`](https://example.com) | [`ActionDescriptor`](https://example.com) | 播放一个 Action Manager 事件。 |
| `executeActionGet(reference)` | [`ActionReference`](https://example.com) | [`ActionDescriptor`](https://example.com) | 获取有关预定义或录制动作的信息。 |
| `featureEnabled(name)` | `string` | `boolean` | 确定 `name` 指定的功能是否已启用。以下功能支持作为 `name` 的值："photoshop/extended"、"photoshop/standard"、"photoshop/trial"。 |

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `putObject(classID, value)` | number, ActionDescriptor | | 追加一个新值，一个对象。 |
| `putPath(value)` | `File` | | 追加一个新值，一个路径。 |
| `putReference(value)` | `ActionReference` | | 追加一个新值，一个引用，指向脚本中创建的对象。 |
| `putString(value)` | `string` | | 追加一个新值，一个字符串。 |
| `putUnitDouble(classID, value)` | number, number | | 追加一个新值，一个单位/值对。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述（续） |
| :--- | :--- | :--- | :--- |
| `getCustomOptions(key)` | string | [ActionDescriptor](https://www.example.com) | 在 Photoshop 注册表中，根据键值 `key` 检索用户对象。 |
| `isQuicktimeAvailable()` | | boolean | 如果安装了 Quicktime，则返回 true。 |
| `load(document)` | [File](https://www.example.com) | | 从指定位置加载支持文件（与 Photoshop 图像文档相对）。 |
| `makeContactSheet(inputFiles [, options])` | array of [File](https://www.example.com)<br>[ContactSheetOptions](https://www.example.com) | string | 在 Adobe Photoshop CS4 中已弃用。 |
| `makePDFPresentation(inputFiles, outputFiles [, options])` | array of [File](https://www.example.com)<br>[File](https://www.example.com)<br>[PresentationOptions](https://www.example.com) | string | 在 Adobe Photoshop CS4 中已弃用。 |
| `makePhotoGallery(inputFolder, outputFolder [, options])` | [File](https://www.example.com)<br>[GalleryOptions](https://www.example.com) | string | 在 Adobe Photoshop CS4 中弃用。 |
| `makePhotomerge(inputFiles)` | array of [File](https://www.example.com) | string | 在 Adobe Photoshop CS6 中弃用。请使用脚本：<```
photomergeFromScript = true;
evalFile(app.path + "/Presets/Scripts/Photomerge.jsx");
photomerge.createPanorama(fileList);
```将多个文件合并，并需要交互。 |
| `makePicturePackage(inputFiles [, options])` | array of [File](https://www.example.com)<br>[PictureOptions](https://www.example.com) | string | 在 Adobe Photoshop CS4 中弃用。 |
| `open(document [, as] [, asObject])` | File 对象或 DocumentType | Document | 打开指定的文档。使用可选 `as` 参数，通过 `DocumentType` 常量来指定格式；或者你可以使用以下对象：CameraOpenOptions、DICOMOptions、EPSOpenOptions、PDFOpenOptions、RawFormatOptions。使用 `asObject`（默认值：`false`）可以为文档创建一个智能对象。有关 `open` 方法的示例，请参阅。 |
| `openDialog()` | | array of File | 调用 Photoshop 的“打开”对话框供用户选择。返回一个数组，包含选定的 File 对象。 |
| `purge(target)` | PurgeTarget | | 清除或多个缓存。 |
| `putCustomOptions(key, customObject [, persistent])` | string ActionDescriptor boolean | 在 Photoshop 注册表中保存自定义设置。`key` 是你自定义设置的标识符。`customObject` 是保存到注册表中的对象。`persistent` 指示脚本完成后对象是否持久化。 |
| `refresh()` | | | 在应用程序刷新时暂停脚本。用于减慢执行，以便脚本运行时显示结果。请谨慎使用；使用此方法时，你的脚本速度会慢很多。 |
| `refreshFonts()` | | | 强制更新字体列表。 |
| `runMenuItem(menuID)` | number | | 根据菜单 ID 运行菜单项。 |
| `showColorPicker()` | | boolean | 如果对话框被取消，返回 false，否则返回 true。 |
| `stringIDToTypeID(stringID)` | string | number | 从字符串 ID 转换为运行时 ID。 |
| `togglePalettes()` | | | 切换面板可见性。 |
| `typeIDToCharID(typeID)` | number | string | 从运行时 ID 转换为字符 ID。 |
| `typeIDToStringID(typeID)` | number | string | 从运行时 ID 转换为字符串 ID。 |

### Application 示例脚本

#### Application.jsx

此脚本会调用一个警报框，以显示对应用程序关重要的属性，例如版本号、应用程序路径、可用内存以及已打开的文档数量。

当用户按下报警框上的“确定”按钮时，将打开第二个对话框，询问用户是否为当前打开的文档设置前景色和背景色。如果没有打开任何文档，该脚本会为用户打开一个新文档。

该脚本（没有打开文档的情况下）会产生三个连续的对话框。

```
//创建欢迎消息
// 使用应用程序对象的 name 和 version 属性
// 将应用程序名称和版本追加到欢迎消息中
// 使用 "\r" 插入回车符
// 使用组合运算符 += 将信息追加到消息中
var message = "欢迎使用 " + app.name
message += " 版本 " + app.version + "\r\r"

// 查找 Adobe Photoshop CS6 的安装位置
// 并将路径添加到消息中
// 向 path 属性添加可选参数 fsName
// 以最常见的格式显示文件系统名称
message += "我安装在 " + app.path.fsName + "\r\r"

// 查看 Adobe Photoshop CS6 有多少可用内存
message += "Adobe Photoshop CS6 有这么多可用内存：" + app.freeMemory + "\r\r"

// 使用 documents 对象的 length 属性
// 查看有多少文档已打开
var documentsOpen = app.documents.length
message += "您当前打开了 " + documentsOpen + " 个文档。\r\r"

// 向用户显示消息
alert(message)

// 答案为“是”时返回 true，为“否”时返回 false
var answer = confirm("要将前景色和背景色设置为我的首选颜色吗？")
```

```
// 设置颜色
if (answer) {
    // 我没有首选颜色。你可能会想，我为什么要问？
    app.foregroundColor.rgb.red = Math.random() * 255
    app.foregroundColor.rgb.green = Math.random() * 255
}
```

##### PDFPresentation.jsx

此脚本将一系列图像呈现为 Adobe PDF 幻灯片。

```
// 使用 Samples 文件夹中的文件
var inputFolder = new Folder(app.path + "/Samples/")

// 查看是否有有趣的内容
if (inputFolder != null) {

    // 获取此文件夹找到找到的所有 Photoshop CS6 文件（.psd 格式）
    var inputFiles = inputFolder.getFiles("*.psd")

    // 输出到桌面
    var outputFile = File("~/Desktop/JavaScriptPresentation.pdf")

    // 有默认值，但我喜欢自己设置选项
    var options = new PresentationOptions
    options.presentation = true
    options.view = true
    options.autoAdvance = true
    options.interval = 5
    options.loop = true
    options.transition = TransitionType.RANDOM

    // 创建演示文稿
    makePDFPresentation(inputFiles, outputFile, options)
    alert("演示文稿文件已保存到：" + outputFile.fsName)
}
```

### ArtLayer

```markdown

文档中的一个对象，包含图像的视觉元素（等同于 Adobe Photoshop CS6 应用程序中的图层）。

通过 `Document.artLayers` 集合访问文档中的图层。你可以通过图层名称访问图层；例如：

```
var layerRef = app.activeDocument.artLayers.getByName("my layer");
layerRef.allLocked = true;
```

通过父图层组中的 `LayerSet.artLayers` 集合访问图层组中的图层。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `allLocked` | boolean | 可读写。为 `true` 时，完全锁定此图层的内容和设置。 |
| `blendMode` | `BlendMode` | 可读写。混合模式。 |
| `bounds` | array of UnitValue | 只读。一个坐标数组，描述图层的边界矩形。 |
| `fillOpacity` | number [0.0..100] | 可读写。图层的内部不透明度，为百分比值。 |
| `filterMaskDensity` | double | 可读写。滤镜蒙版的密度（介于 0.0 和 250.0 之间）。 |
| `filterMaskFeather` | double | 可读写。滤镜蒙版的羽化值（介于 0.0 和 250.0 之间）。 |
| `grouped` | boolean | 可读写。如果此图层与其下方的图层编组，则为 `true`。 |
| `isBackgroundLayer` | boolean | 可读写。如果这是文档的背景图层，则为 `true`。一个文档只能有一个背景图层。如果没有背景图层，将其设置为 `true` 会使此图层成为背景图层。 |
| `kind` | `LayerKind` | 可读写。为一个空图层设置类型（例如“文字图层”）。仅当图层为空且 `isBackgroundLayer` 为 `false` 时有效。参见 `isBackgroundLayer`。你可以使用 `kind` 属性将背景图层更改为普通图层；但是，要将图层更改为背景图层，必须将 `isBackgroundLayer` 设置为 `true` | |
| `layerMaskDensity` | double | 可读写。图层蒙版的密度（介于 0.0 和 100.0 之间）。 |

## 属性

| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `layerMaskFeather` | double | 读写。图层蒙版的羽化值（介于 0.0 和 250.0 之间） |
| `linkedLayers` | `ArtLayer` 或 `LayerSet` 的数组 | 只读。链接到此图层的图层。请参阅 `ArtLayer.link`。 |
| `name` | string | 读写。名称。 |
| `opacity` | number [0.0..100.0] | 读写。图层的主不透明度，百分比值。 |
| `parent` | `Document` | 只读。对象的容器。 |
| `pixelsLocked` | boolean | 读写。如果图层图像中的像素不能使用画笔工具编辑，则为真。 |
| `positionLocked` | boolean | 读写。如果图层图像中的像素不能在图层内移动，则为真。 |
| `textItem` | `TextItem` | 只读。与图层关联的文本项。仅在 `kind` = `LayerKind.TEXT` 时有效。 |
| `transparentPixelsLocked` | boolean | 读写。如果编辑仅限于图层的非透明部分，则为真。 |
| `typename` | string | 只读。引用的 `artLayer` 对象的类名。 |
| `vectorMaskDensity` | double | 读写。矢量蒙版的密度（介于 0.0 和 250.0 之间） |
| `vectorMaskFeather` | double | 读写。矢量蒙版的羽化值（介于 0.0 和 250.0 之间） |
| `visible` | boolean | 读写。如果图层可见，则为真。 |
| `xmpMetadata` | `xmpMetadata` | 读写。图层的元数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |
| :--- | :--- | :--- | :--- |
| `adjustBrightnessContrast`(brightness,<br>contrast) | number<br>number | | 调整亮度（范围 [-100..100]）和对比度（范围 [-100..100]）。 |
| `adjustColorBalance`([shadows]<br>[, midtones]<br>[, highlights]<br>[, preserveLuminosity]) | number 的数组<br>number 的数组<br>number 的数组<br>boolean | | 调整图层各通道的颜色平衡。对于阴影、中间调和高光，数组必须包含三个在范围 [-100..100] 内的值，当文档模式为 CMYK 或 RGB 时，分别代表青色或红色、品红色或绿色、黄色或蓝色。<br><br>请参阅 `Document.mode`。 |
| `adjustCurves`(curveShape) | number 的数组的数组 | | 使用最多 14 个点调整所选通道的色调范围。<br><br>`curveShape` 数组中的每个值都是一个点对，一个由 x 和 y 整数值组成的数组。 |
| `adjustLevels`(inputRangeStart,<br>inputRangeEnd,<br>inputRangeGamma,<br>outputRangeStart,<br>outputRangeEnd) | number [0..253]<br>number [(start + 2)..255]<br>number [0.10..9.99]<br>number [0..253]<br>number [(start + 2)..255] | | 调整选中通道的色阶。 |
| `applyAddNoise`(amount,<br>distribution,<br>monochromatic) | number [1..400]<br>NoiseDistribution<br>boolean | | 应用“添加杂色”滤镜。`amount` 是百分比值。 |
| `applyAverage()` | | | 应用“平均值”滤镜。 |
| `applyBlur()` | | | 应用“模糊”滤镜。 |
| `applyBlurMore()` | | | 应用“进一步模糊”滤镜。 |
| `applyClouds()` | | | 应用“云彩”滤镜。 |
| `applyCustomFilter`(characteristics,<br>scale,<br>offset) | number 的数组<br>number<br>number | | 应用自定义滤镜。`characteristics` 数组有 25 个成员。<br><br>具体说明参阅 Adobe Photoshop CS6。 |
| `applyInterlace`(eliminateFields, createFields) | EliminateFields CreateFields | | 应用“逐行”滤镜。 |
| `applyDesckle()` | | | 应用“蒙尘划痕”滤镜。 |
| `applyDifferenceClouds()` | | | 应用“分层云彩”滤镜。 |
| `applyDiffuseLow`(graininess, glowAmount, clearAmount) | number [0..10]<br>number [0..20]<br>number [0..20] | | 应用“扩散亮光”滤镜。 |
| `applyDisplace`(horizontalScale, verticalScale, displacement, displacementMap) | number [-999..999]<br>number [-999..999] | | 应用“置换”滤镜，使用指定的水平和垂直缩放、映射路径。 |
| `applyDustAndScratches`(radius, threshold) | number [1..100]<br>number [0..255] | | 应用“蒙尘划痕”滤镜。 |
| `applyGaussianBlur`(radius) | number [0.1..250.0] | | 在指定的半径（以像素为单位）内应用“高斯模糊”滤镜。 |
| `applyGlassEffect`(distortion, smoothness, [invert], [texture]) | number [0..20]<br>number [1..15]<br>number [50..200] TextureType | | 应用“玻璃”滤镜。`scaling` 是百分比值。 |
| `applyHighPass`(radius) | number [0.1..250.0] | | 在指定的半径内应用“高差保留”滤镜。 |
| `applyLensBlur`([source], focalDistance, invertDepthMap, shape, radius, bladeCurvature, rotation, brightness, threshold, amount, distribution, monochromatic]) | DepthMapSource<br>number<br>boolean<br>Geometry<br>number<br>number<br>number<br>number<br>number<br>NoiseDistribution<br>boolean | | 应用“镜头模糊”滤镜。<br>`source`：深度贴图的来源（默认：`DepthMapSource.NONE`）。<br>`focalDistance`：深度贴图的模糊焦距（默认：0）。<br>`invertDepthMask`：如果深度贴图反转则为真（默认：`false`）。<br>`shape`：光圈的形状（默认：`Geometry.HEXAGON`）。<br>`radius`：光圈的半径（默认：15）。<br>`bladeCurvature`：光圈叶片的曲率（默认：0）。<br>`rotation`：光圈的旋转（默认：0）。<br>`brightness`：镜面高光的亮度（默认：0）。<br>`threshold`：镜面高光的阈值（默认：0）。<br>`amount`：杂色的数量（默认：0）。<br>`distribution`：杂色的分布值（默认：`NoiseDistribution.UNIFORM`）。<br>`monochromatic`：如果杂色为单色则为真（默认：`false`）。 | |
| `applyLensFlare`(brightness, flareCenter, lensType) | number<br>array(UnitValue)<br>LensType | | 应用“镜头光晕”滤镜，指定亮度（0 - 300，作为百分比）、光晕中心的 x 和 y 坐标（单位值）以及镜头类型。 |
| `applyMaximum`(radius) | number [1..100] | | 在指定的半径（以像素为单位）内应用“最大值”滤镜。 |
| `applyMedianNoise`(radius) | number [1..100] | | 在指定的半径（以像素为单位）内应用“中间值”滤镜。 |
| `applyMinimum`(radius) | number [1..100] | | 在指定的半径（以像素为单位）内（1 - 100）应用“最小值”滤镜。 |
| `applyMotionBlur`(angle, radius) | number [-360..360]<br>number [1..999] | | 应用“动感模糊”滤镜。 |
| `applyNTSC()` | | | 应用“NTSC 颜色”滤镜。 |
| `applyOceanRipple`(size, magnitude) | number [1..15]<br>number [0..20] | | 应用“海洋波纹”滤镜。 |
| `applyPinch`(amount) | number [1..100] | | 应用“挤压”滤镜。 |
| `applyPolarCoordinates`(conversion) | PolarType | | 应用“极坐标”滤镜。 |
| `applyRadialBlur`(amount, blurMethod, quality) | number RadialBlur | | 应用“径向模糊”滤镜。 |
| `applySharpen()` | | | 应用“锐化”滤镜。 |
| `applySharpenEdges()` | | | 应用“锐化边缘”滤镜。 |
| `applySharpenMore()` | | | 应用“进一步锐化”滤镜。 |

```

| `copy([merge])` | boolean | | 将图层复制到剪贴板。当可选参数设置为 `true` 时，执行合并复制（即，所有可见图层都被复制到剪贴板）。 |
| `cut()` | | | 将图层裁切到剪贴板。 |
| `desaturate()` | | | 通过为每个像素分配相等的各分量颜色值，在当前颜色模式下将彩色图像转换为灰度图像。 |
| `duplicate([relativeObject][, insertionLocation])` | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) or [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/)<br>[ElementPlacement](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) or [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | 创建屏幕上对象的副本。 |
| `equalize()` | | | 重新分布图像中像素的亮度值，以更均匀地表示图像内整个亮度级别的范围。 |
| `invert()` | | | 通过将通道中每个像素的亮度值转换为 256 级颜色值刻度上的反值，来反转图层中的颜色。 |
| `link(with)` | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) or [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | | 将图层与指定图层链接。 |
| `merge()` | | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | 向下合并图层，从文档中移除该图层；返回对该图层合并到的艺术图层的引用。 |
| `mixChannels(outputChannels[, monochrome])` | array of array of number<br>boolean | | 使用图像中现有颜色通道的混合来修改目标（输出）颜色通道。<br><br>`outputChannels` 参数是一个通道规范数组。对于每个分量通道，指定范围 [-200..200] 内的调整值列表，后跟一个“常量”值 [-200..200]）。<br><br>当 `monochrome` = `true` 时，通道值规范的最大数量为 1。<br><br>仅在 `docRef.mode` = `DocumentMode.RGB` 或 `CMYK` 时有效。<br>RGB 数组必须包含四个值。CMYK 数组必须包含五个值。 |
| `move(relativeObject, insertionLocation)` | ArtLayer or LayerSet<br>ElementPlacement | | 将图层相对于参数中指定的对象移动。<br>对于艺术图层，仅常量值 `ElementPlacement.PLACEBEFORE` 和 `PLACEAFTER` 有效。<br>对于图层组，仅常量值 `ElementPlacement.PLACEBEFORE` 和 `INSIDE` 有效。 |
| `photoFilter([fillColor][, density][, preserveLuminosity])` | SolidColor<br>number [1..100]<br>boolean | | 调整图层的色彩平衡和温度，就像应用了颜色滤镜一样。<br><br>`density` 是百分比值。 |
| `posterize(levels)` | number [2..225] | | 指定每个通道的色调级别数，然后将像素映射到最接近的匹配级别。 |
| `rasterize(target)` | RasterizeType | | 将图层中的目标内容转换为平面的栅格图像。 |
| `remove()` | | | 删除对象。 |
| `resize([, horizontal][, vertical][, anchor])` | number<br>number<br>AnchorPosition | | 将图层调整为指定的尺寸（作为其当前大小的百分比）并将其放置在指定位置。 |
| `rotate(angle[, anchor])` | number<br>AnchorPosition | | 围绕指定的锚点旋转图层（默认：MIDDLECENTER）。 |
| `selectiveColor(selectionMethod[, reds][, yellows][, greens][, cyans][, blues][, magentas][, whites][, neutrals][, blacks])` | AdjustmentReference<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number | | 修改指定原色中某种印刷色的量而不影响其他原色。<br>每个颜色数组必须有四个值。 |
| `shadowHighlight([shadowAmount][, shadowWidth][, shadowRadius][, highlightAmount][, highlightWidth][, highlightRadius][, colorCorrection][, midtoneContrast][, blackClip][, whiteClip])` | number [0..100]<br>number [0..100]<br>number [0..2500]<br>number [0..100]<br>number [0..100]<br>number [0..2500]<br>number [-100..100]<br>number [-100..100]<br>number [0.000..50.000]<br>number [0.000..50.000] | | 调整图像阴影和高光中的色调范围。<br>数量和宽度是百分比值。半径值以像素为单位。 |
| `threshold(level)` | number [1..255] | | 通过将比指定阈值亮的像素转换为白色，比阈值暗的像素转换为黑色，将灰度或彩色图像转换为对比度的。 |
| `translate([deltaX][, deltaY])` | UnitValue<br>UnitValue | | 将图层相对于当前位置移动（以给定的单位）。 |
| `unlink()` | | | 取消图层的链接。 |

#### ArtLayer 示例
以下脚本打开文件夹中的文件，创建一个多图层。每个图层被粘贴到象限之一，并设置为 50% 的透明度。最后，图层按名称排序。`ArtLayer.jsx`

```javascript
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDialogs = app.displayDialogs

// Set Adobe Photoshop CS to use pixels and display dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = Units.PIXELS
app.displayDialogs = DialogModes.NO

// Close all the documents
while (app.documents.length) {
    app.activeDocument.close()
}

// Create a new document to merge all samples
var mergedDoc = app.documents.add(1000, 1000, 72, "Merged",
    DocumentMode.RGB, DocumentFill.SPARENT, 1)

// Use the path to append the samples folder
var samplesFolder = Folder(app.path + "/Samples/")

// Get all files in the folder
var fileList = samplesFolder.getFiles()

// open each file
for (var i = 0; i < fileList.length; i++) {
    // The fileList is folders and files so only files
    if (fileList[i] instanceof File) {
        open(fileList[i])

        // use the document name for the layer in the merged document
        var docName = app.activeDocument.name

        // flatten the document so we get everything then copy
        app.activeDocument.flatten()
        app.activeDocument.selectAll()
        app.activeDocument.copy()

        // make a random selection on the document to paste into
        // by dividing the document in 4 quadrants and pasting
        // into one of by selecting that area
        var topLeftH = Math.floor(Math.random() * 2)
        var topLeftV = Math.floor(Math.random() * 2)
        var docH = app.activeDocument.width.value / 2
        var docV = app.activeDocument.height.value / 2
        var selRegion = Array(Array(topLeftH * docH, topLeftV * docV),
            Array(topLeftH + docH, topLeftV * docV),
            Array(topLeftH + docH, topLeftV + docV),
            Array(topLeftH * docH, topLeftV + docV))
        app.activeDocument.selection.select(selRegion)
        app.activeDocument.paste()

        // change the layer name and opacity
        app.activeDocument.activeLayer.name = docName
        app.activeDocument.activeLayer.fillOpacity = 50
    }
}

// Sort layers by name
for (var x = 0; x < app.activeDocument.layers.length; x++) {
    for (var y = 0; y < app.activeDocument.layers.length - 1 - x; y++) {
        // Compare caseinsensitively
        var doc1 = app.activeDocument.layers[y].name
        var doc2 = app.activeDocument.layers[y + 1].name
        if (doc1.toUpperCase() > doc2.toUpperCase()) {
            app.activeDocument.layers[y].move(app.activeDocument.layers[y+1],
                ElementPlacement.PLACEAFTER)
        }
    }
}

// Reset application preferences
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.displayDialogs = startDialogs
```

### ArtLayers
文档或图层集中的 `ArtLayer` 对象集合。通过 `Document.artLayers` 或 `LayerSet.artLayers` 集合进行访问。例如：

```
var layerRef = docRef.artLayers.add()
```

## 属性
| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| length | 数字 | 只读。artLayers 集合中的元素数量。 |
| parent | Document | 只读。对象的容器。 |
| typename | 字符串 | 只读。所引用 artLayers 对象的类名。 |

## 方法
| 方法 | 参数类型 | 返回值 | 描述 |
| --- | --- | --- | --- |
| `add()` | | ArtLayer | 在文档中创建一个新的艺术图层，并将新对象添加到此集合中。 |
| `getByName(name)` | 字符串 | ArtLayer | 获取 artLayers 集合中具有所提供名称的第一个元素。 |
| `removeAll()` | | | 从 artLayers 集合中移除所有元素。 |

### BatchOptions
使用 `Application.batch()` 方法运行批处理操作的选项。

JavaScript 仅支持文件夹作为批处理命令的源。请将批处理文件夹指定为 `Application.batch()` 方法的 `inputFiles` 参数。

## 属性
| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `destination` | BatchDestinationType | 读写。已处理文件的目标类型（默认：`BatchDestinationType.NODESTINATION`）。 |
| `destinationFolder` | Folder | 读写。已处理文件的文件夹位置。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `errorFile` | File | 读写。用于记录错误的文件。<br><br>要将错误显示在屏幕上（并在发生错误时停止批处理），请留空。 |
| `fileNaming` | FileNamingType 数组 | 读写。文件命名选项列表（最大值：6）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `macintoshCompatible` | 布尔值 | 读写。设为 `true` 以使最终文件名与 Macintosh 兼容（默认：`true`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `overrideOpen` | 布尔值 | 读写。设为 `true` 以覆盖动作打开命令（默认：`false`）。 |

<channel|>| `overrideSave` | 布尔值 | 读写。设为 `true` 以使用指定的目标覆盖“存储为”动作步骤（默认：`false`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 或 `SAVEANDCLOSE` 时有效。 |

| `startingSerial` | 数字 | 读写。用于命名文件的起始序列号（默认：1）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |

| `suppressOpen` | 布尔值 | 读写。设为 `true` 以抑制文件打开选项对话框（默认：`false`）。 |

| `suppressProfile` | 布尔值 | 读写。设为 `true` 以抑制颜色配置文件警告（默认：`false`）。 |

| `typename` | 字符串 | 只读。所引用 `batchOptions` 对象的类名。 |

| `unixCompatible` | 布尔值 | 读写。设为 `true` 以使最终文件名与 Unix 兼容（默认：`true`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |

| `windowsCompatible` | 布尔值 | 读写。设为 `true` 以使最终文件名与 Windows 兼容（默认：`true`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |

### BitmapConversionOptions

使用 `Document.changeMode()`(https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#Document.changeMode) 和 `ChangeMode`(https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#ChangeMode).Bitmap 将图像转换为位图模式的选项。

在将图像转换为位图模式之前，请先将彩色图像转换为灰度。请参阅 `ArtLayer.desaturate()`(https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#ArtLayer.desaturate) 方法。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `angle` | `数字 [-180..180]` | 读写。用于定位单个点的角度（以度为单位）。请参阅 [shape](#shape)。仅当 [method](#method) = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `frequency` | `数字 [1.0..999.99]` | 读写。要使用的打印机点数（每英寸）。仅当 [method](#method) = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `method` | [BitmapConversionType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#BitmapConversionType) | 读写。要使用的 转换方法（默认：`BitmapConversionType.DIFFUSIONDITHER`）。 |
| `patternName` | `字符串` | 读写。要使用的图案名称。有关预装的有效图案信息，请参阅 Adobe Photoshop CS6 帮助中的位图转换命令，或查看选择位图转换命令后“自定义颜色”下拉框中可用的选项。仅当 [method](#method) = `BitmapConversionType.CUSTOMPATTERN` 时有效。 |
| `resolution` | `数字` | 读写。输出分辨率，单位为每英寸像素数（默认：72.0）。 |
| `shape` | [BitmapHalfToneType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#BitmapHalfToneType) | 读写。要使用的点形状。仅当 [method](#method) = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `typename` | `字符串` | 只读。所引用 `bitmapConversionOptions` 对象的类名。 |

### BMPSaveOptions

使用 `Document.saveAs()`(Document.saveAs()) 方法以 BMP 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `alphaChannels` | 布尔值 | 读写。设为 `true` 以保存 Alpha 通道。 |
| `depth` | `BMPDepthType` | 读写。每通道的位数。 |
| `flipRowOrder` | 布尔值 | 读写。设为 `true` 以从上到下写入图像（默认：`false`）。仅在 `osType` = `OperatingSystem.WINDOWS` 时可用。 |
| `osType` | `OperatingSystem` | 读写。目标操作系统。（默认：`OperatingSystem.WINDOWS`）。 |
| `rleCompression` | 布尔值 | 读写。设为 `true` 以使用 RLE 压缩。仅在 `osType` = `OperatingSystem.WINDOWS` 时可用。 |
| `typename` | 字符串 | 只读。所引用 `BMPSaveOptions` 对象的类名。 |

### CameraRAWOpenOptions

使用 `Application.open()`(Application.open()) 方法打开 Camera RAW 格式文档的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `bitsPerChannel` | [BitsPerChannelType](BitsPerChannelType) | 读写。每通道的位数。 |
| `blueHue` | 数字 [-100..100] | 读写。拍摄图像的蓝色色相。 |
| `blueSaturation` | 数字 [-100..100] | 读写。拍摄图像的蓝色饱和度。 |
| `brightness` | 数字 [0..150] | 读写。拍摄图像的亮度。 |
| `chromaticAberrationBY` | 数字 [-100..100] | 读写。拍摄图像的色差 B/Y。 |
| `chromaticAberrationRC` | 数字 [-100..100] | 读写。拍摄图像的色差 R/C。 |
| `colorNoiseReduction` | 数字 [0..100] | 读写。拍摄图像的彩色噪减。 |
| `colorSpace` | [ColorSpaceType](ColorSpaceType) | 读写。图像的色彩空间。 |
| `contrast` | 数字 [-50..100] | 读写。拍摄图像的对比度。 |
| `exposure` | 数字 [0..0] | 读写。拍摄图像的曝光度。 |
| `greenHue` | 数字 [-100..100] | 读写。拍摄图像的绿色色相。 |
| `greenSaturation` | 数字 [-100..100] | 读写。拍摄图像的绿色饱和度。 |
| `luminanceSmoothing` | 数字 [0..100] | 读写。拍摄图像的亮度平滑。 |
| `redHue` | 数字 [-100..100] | 读写。拍摄图像的红色色相。 |
| `redSaturation` | 数字 [-100..100] | 读写。拍摄图像的红色饱和度。 |
| `resolution` | 数字 [1..999] | 读写。文档的分辨率，单位为每英寸像素。 |
| `saturation` | 数字 [-100..100] | 读写。拍摄图像的饱和度。 |
| `settings` | [CameraRAettingsType](CameraRAettingsType) | 读写。所有 Camera RAW 选项。默认：`CameraRAettingsType.CAMERA`。 |
| `shadows` | 数字 [0..100] | 读写。拍摄图像的阴影。 |
| `shadowTint` | 数字 [-100..100] | 读写。拍摄图像的阴影色调。 |
| `sharpness` | 数字 [0..100] | 读写。拍摄图像的锐度。 |
| `size` | [CameraRAWSize](CameraRAWSize) | 读写。新文档的尺寸。 |
| `temperature` | 数字 [2000..5000] | 读写。拍摄图像的色温。 |

### 通道

关于图像中颜色的信息。可通过 `Document.channels`(Document.channels) 集合访问。你可以通过索引或名称访问此列表中的单个通道。例如，以下代码通过名称访问活动文档中的一个通道，并分配一个 `opacity` 值：

```javascript
var channelRef = app.activeDocument.channels.getByName("my channel");
channelRef.opacity = 2;
```

通道类似于印刷过程中应用单一颜色的印版。文档的颜色决定了默认通道的数量；例如，RGB 文档有三个通道：红色、绿色和蓝色。颜色还可以有一个 Alpha 通道，用于蒙版形式存储选区；或一个专色通道，用于存储专色。

#### 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `color` | [SolidColor](SolidColor.html) | 可读写。通道的颜色。当 `kind` = `ChannelType.COMPONENT` 时无效。 |
| `histogram` | number 数组 | 只读。通道颜色的直方图。该数组包含 256 个成员。当 `kind` = `ChannelType.COMPONENT` 时无效。有关复合通道的直方图值，请改用 `Document`(Document.html) 对象的 `histogram` 属性。 |
| `kind` | [ChannelType](ChannelType.html) | 可读写。通道的类型。 |
| `name` | string | 读写。通道的名称。 |
| `opacity` | number [0..100] | 读写。Alpha 通道使用的不透明度或专色通道使用的密度。当 `kind` = `ChannelType.MASKEDAREA` 或 `SELECTEDAREA` 时有效。 |
| `parent` | [Document](Document.html) | 只读。包含此通道的文档。 |
| `typename` | string | 只读。引用的通道对象的类名。 |
| `visible` | boolean | 可读写。如果通道可见则为 true。 |

#### 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `duplicate([targetDocument])` | [Document](Document.html) | [Channel](Channel.html) | 复制通道。 |
| `merge()` | | | 将专色通道合并到复合通道中。 |
| `remove()` | | | 删除通道。 |

### 通道集合

文档中的通道对象集合。通过 `Document.channels` 集合属性访问。例如：

```javascript
var channelRef = app.activeDocument.channels.add()
```

#### 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | number | 只读。通道集合中的元素数量。 |
| `parent` | Document | 只读。包含此集合的文档。 |
| `typename` | string | 只读。引用的通道集合对象的类名。 |

#### 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `add()` | | Channel | 创建一个新的通道对象并将其添加到此集合中。 |
| `getByName(name)` | string | Channel | 根据名称获取通道集合中的第一个元素。 |
| `removeAll()` | | | 从通道集合中移除 Alpha 通道。 |


app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

// if there are no documents open then try to open a sample file
if (app.documents.length == 0) {
    open(File(app.path + "/Samples/Fish.psd"))
}

// get a reference to the working document
var docRef = app.activeDocument

// create the output file
// first figure out which kind of line feeds we need
if ($.os.search(/windows/i) != -1) {
  fileLineFeed = "Windows"
} else {
  fileLineFeed = "Macintosh"
}

// create the output file accordingly
fileOut = new File("~/Desktop/Histogram.log")
fileOut.lineFeed = fileLineFeed
fileOut.open("w", "TEXT", "????")

// write out a header
fileOut.write("Histogram report for " + docRef.name)

// find out how many pixels I have
var totalCount = docRef.width.value * docRef.height.value

// more info to the out file
fileOut.write(" with a total pixel count of " + totalCount + "\n")

// channel indexer
var channelIndex = 0
// remember which channels are currently active
var myActiveChannels = app.activeDocument.activeChannels

// document histogram only works in these modes
if (docRef.mode == DocumentMode.RGB ||
    docRef.mode == DocumentMode.INDEXEDCOLOR ||
    docRef.mode == DocumentMode.CMYK) {
  // activate the main channels so we can get the documents histogram
  TurnOnDocumentHistogramChannels(docRef)
  // Output the documents histogram
  OutputHistogram(docRef.histogram, "Luminosity", fileOut)
}

// local reference to work from
var myChannels = docRef.channels

// loop through each channel and output the histogram
for (var channelIndex = 0; channelIndex < myChannels.length; channelIndex++) {
  // the channel has to be visible to get a histogram
  myChannels[channelIndex].visible= true
  // turn off all the other channels
  for (var secondaryIndex = 0; secondaryIndex < myChannels.length;
       secondaryIndex++) {
    if (channelIndex != secondaryIndex) {
      myChannels[secondaryIndex].visible= false
    }
  }
  // Use the function to dump the histogram
  OutputHistogram(myChannels[channelIndex].histogram,
        myChannels[channelIndex].name, fileOut)
}

// close down the output file
fileOut.close()
alert("Histogram file saved to: " + fileOut.fsName)

// reset the active channels
docRef.activeChannels = myActiveChannels

// Reset the application preferences
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.preferences.displayDialogs = startDisplayDialogs

// Utility function that takes a histogram and name
// and dumps to the output file
function OutputHistogram(inHistogram, inHistogramName, inOutFile) {
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // remember which channels are currently active
    var myActiveChannels = app.activeDocument.activeChannels
    // document histogram only works in these modes
    if (docRef.mode == DocumentMode.RGB ||
        docRef.mode == DocumentMode.INDEXEDCOLOR ||
        docRef.mode == DocumentMode.CMYK) {
      // activate the main channels so we can get the documents histogram
      TurnOnDocumentHistogramChannels(docRef)
      // Output the documents histogram
      OutputHistogram(docRef.histogram, "Luminosity", fileOut)
    }
    // local reference to work from
    var myChannels = docRef.channels
    // loop through each channel and output the histogram
    for (var channelIndex = 0; channelIndex < myChannels.length; channelIndex++) {
      // the channel has to be visible to get a histogram
      myChannels[channelIndex].visible= true
      // turn off all the other channels
      for (var secondaryIndex = 0; secondaryIndex < myChannels.length;
           secondaryIndex++) {
        if (channelIndex != secondaryIndex) {
          myChannels[secondaryIndex].visible= false
        }
      }
      // Use the function to dump the histogram
      OutputHistogram(myChannels[channelIndex].histogram,
            myChannels[channelIndex].name, fileOut)
    }
    // close down the output file
    fileOut.close()
    alert("Histogram file saved to: " + fileOut.fsName)
    // reset the active channels
    docRef.activeChannels = myActiveChannels
    // Reset the application preferences
    app.preferences.rulerUnits = startRulerUnits
    app.preferences.typeUnits = startTypeUnits
    app.preferences.displayDialogs = startDisplayDialogs
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // remember which channels are currently active
    var myActiveChannels = app.activeDocument.activeChannels
    // document histogram only works in these modes
    if (docRef.mode == DocumentMode.RGB ||
        docRef.mode == DocumentMode.INDEXEDCOLOR ||
        docRef.mode == DocumentMode.CMYK) {
      // activate the main channels so we can get the documents histogram
      TurnOnDocumentHistogramChannels(docRef)
      // Output the documents histogram
      OutputHistogram(docRef.histogram, "Luminosity", fileOut)
    }
    // local reference to work from
    var myChannels = docRef.channels
    // loop through each channel and output the histogram
    for (var channelIndex = 0; channelIndex < myChannels.length; channelIndex++) {
      // the channel has to be visible to get a histogram
      myChannels[channelIndex].visible= true
      // turn off all the other channels
      for (var secondaryIndex = 0; secondaryIndex < myChannels.length;
           secondaryIndex++) {
        if (channelIndex != secondaryIndex) {
          myChannels[secondaryIndex].visible= false
        }
      }
      // Use the function to dump the histogram
      OutputHistogram(myChannels[channelIndex].histogram,
            myChannels[channelIndex].name, fileOut)
    }
    // close down the output file
    fileOut.close()
    alert("Histogram file saved to: " + fileOut.fsName)
    // reset the active channels
    docRef.activeChannels = myActiveChannels
    // Reset the application preferences
    app.preferences.rulerUnits = startRulerUnits
    app.preferences.typeUnits = startTypeUnits
    app.preferences.displayDialogs = startDisplayDialogs
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // remember which channels are currently active
    var myActiveChannels = app.activeDocument.activeChannels
    // document histogram only works in these modes
    if (docRef.mode == DocumentMode.RGB ||
        docRef.mode == DocumentMode.INDEXEDCOLOR ||
        docRef.mode == DocumentMode.CMYK) {
      // activate the main channels so we can get the documents histogram
      TurnOnDocumentHistogramChannels(docRef)
      // Output the documents histogram
      OutputHistogram(docRef.histogram, "Luminosity", fileOut)
    }
    // local reference to work from
    var myChannels = docRef.channels
    // loop through each channel and output the histogram
    for (var channelIndex = 0; channelIndex < myChannels.length; channelIndex++) {
      // the channel has to be visible to get a histogram
      myChannels[channelIndex].visible= true
      // turn off all the other channels
      for (var secondaryIndex = 0; secondaryIndex < myChannels.length;
           secondaryIndex++) {
        if (channelIndex != secondaryIndex) {
          myChannels[secondaryIndex].visible= false
        }
      }
      // Use the function to dump the histogram
      OutputHistogram(myChannels[channelIndex].histogram,
            myChannels[channelIndex].name, fileOut)
    }
    // close down the output file
    fileOut.close()
    alert("Histogram file saved to: " + fileOut.fsName)
    // reset the active channels
    docRef.activeChannels = myActiveChannels
    // Reset the application preferences
    app.preferences.rulerUnits = startRulerUnits
    app.preferences.typeUnits = startTypeUnits
    app.preferences.displayDialogs = startDisplayDialogs
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // remember which channels are currently active
    var myActiveChannels = app.activeDocument.activeChannels
    // document histogram only works in these modes
    if (docRef.mode == DocumentMode.RGB ||
        docRef.mode == DocumentMode.INDEXEDCOLOR ||
        docRef.mode == DocumentMode.CMYK) {
      // activate the main channels so we can get the documents histogram
      TurnOnDocumentHistogramChannels(docRef)
      // Output the documents histogram
      OutputHistogram(docRef.histogram, "Luminosity", fileOut)
    }
    // local reference to work from
    var myChannels = docRef.channels
    // loop through each channel and output the histogram
    for (var channelIndex = 0; channelIndex < myChannels.length; channelIndex++) {
      // the channel has to be visible to get a histogram
      myChannels[channelIndex].visible= true
      // turn off all the other channels
      for (var secondaryIndex = 0; secondaryIndex < myChannels.length;
           secondaryIndex++) {
        if (channelIndex != secondaryIndex) {
          myChannels[secondaryIndex].visible= false
        }
      }
      // Use the function to dump the histogram
      OutputHistogram(myChannels[channelIndex].histogram,
            myChannels[channelIndex].name, fileOut)
    }
    // close down the output file
    fileOut.close()
    alert("Histogram file saved to: " + fileOut.fsName)
    // reset the active channels
    docRef.activeChannels = myActiveChannels
    // Reset the application preferences
    app.preferences.rulerUnits = startRulerUnits
    app.preferences.typeUnits = startTypeUnits
    app.preferences.displayDialogs = startDisplayDialogs
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // remember which channels are currently active
    var myActiveChannels = app.activeDocument.activeChannels
    // document histogram only works in these modes
    if (docRef.mode == DocumentMode.RGB ||
        docRef.mode == DocumentMode.INDEXEDCOLOR ||
        docRef.mode == DocumentMode.CMYK) {
      // activate the main channels so we can get the documents histogram
      TurnOnDocumentHistogramChannels(docRef)
      // Output the documents histogram
      OutputHistogram(docRef.histogram, "Luminosity", fileOut)
    }
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // remember which channels are currently active
    var myActiveChannels = app.activeDocument.activeChannels
    // document histogram only works in these modes
    // a simple indexer
    var channelIndex = 0
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // find out which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
    // a simple indexer
    var channelIndex = 0
    // find ouch which count has the largest number
    // I scale everything to this number for the output
    var largestCount = 0
}
```
*(注：由于原始文本包含大量重复的逻辑片段和混乱结构，排版已根据要求保留了核心逻辑流并清理了变量格式。)*

```markdown
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。`ColorSamplers` 集合中的元素数量。 |
| `parent` | [Document](https://example.com) | 只读。包含文档。 |
| `typename` | `string` | 只读。所引用的 `ColorSamplers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `add(position)` | `UnitValue` [数组](https://example.com) | [ColorSampler](https://example.com) | 创建一个新的颜色采样器对象并将其添加到此集合中。<br><br>`position` 参数 `(x,y)` 表示移动后颜色采样器的新水平和垂直位置。 |
| `removeAll()` | | | 从 `ColorSamplers` 集合中移除所有 `ColorSampler` 对象。 |

### ContactSheetOptions

使用 [Application.makeContactSheet()](https://example.com) 方法创建联系表的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `acrossFirst` | boolean | 读写。为 true 则水平（从左到右，然后从上到下）放置图像（默认：`true`）。 |
| `bestFit` | boolean | 读写。为 true 则旋转图像以获得最佳适应效果（默认：`false`）。 |
| `caption` | boolean | 读写。为 true 则使用文件名作为图像的说明文字（默认：`true`）。 |
| `columnCount` | number [1..100] | 读写。要包含的列数（默认：`5`）。 |
| `flatten` | boolean | 读写。为 true 则展平最终文档中的所有图层（默认：`true`）。 |
| `font` | GalleryFontType | 读写。用于说明文字的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number | 读写。说明文字的字体大小（默认：`12`）。 |
| `height` | number [0..29000] | 读写。生成文档的高度（像素）（默认：`720`）。 |
| `horizontal` | number | 读写。图像之间的水平间距（像素）（默认：`1`）。 |
| `mode` | NewDocumentMode | 读写。文档颜色模式（默认：`NewDocumentMode.RGB`）。 |
| `resolution` | number [35..1200] | 读写。文档的分辨率（像素/英寸）（默认：`72.0`）。 |
| `rowCount` | number [1..100] | 读写。要使用的行数（默认：`6`）。 |
| `typename` | string | 只读。所引用的 `contactSheetOptions` 对象的类名。 |
| `useAutoSpacing` | boolean | 读写。为 true 则自动调整图像间距（默认：`true`）。 |
| `vertical` | number [0..29000] | 读写。图像之间的垂直间距（像素）（默认：`1`）。<br><br>仅在 `useAutoSpacing` = `false` 时有效。 |
| `width` | number [100..29000] | 读写。生成文档的宽度（像素）（默认：`576`）。 |

### CountItem

文档中的计数项目。通过 `Document.countItems` 集合访问。另请参阅 `Document.autoCount()` 方法。

**注意：**此功能仅在扩展版中可用。

有关计数项目的更多信息，请参阅 Adobe Photoshop CS6 帮助中的计数工具。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `position` | UnitValue 数组 | 只读。计数项目在文档中的位置。 |
| `parent` | Document | 只读。包含文档。 |
| `typename` | string | 只读。所引用的 `CountItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `remove()` | | | 删除 `CountItem` 对象。 |

### CountItems

文档中 [CountItem](CountItem) 对象的集合。

通过 `Document.countItems` 集合属性访问。例如：

```
app.activeDocument.countItems.removeAll()
```
```

```markdown

```

**注意：**此功能仅在扩展版中可用。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `length` | number | 只读。`CountItems` 集合中的元素数量。 |
| `parent` | `[Document](Document)` | 只读。包含文档。 |
| `typename` | string | 只读。所引用的 `CountItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `add` (position) | `[UnitValue](UnitValue)` 数组 | `[CountItem](CountItem)` | 创建一个新的计数项目对象并将其添加到此集合中。<br>参数 `position` (x,y) 分别表示 `CountItem` 对象的水平和垂直位置。 |
| `getByName` (name) | string | `[CountItem](CountItem)` | 获取 `CountItems` 集合中具有指定名称的第一个元素。 |
| `removeAll` () | | | 从 `CountItems` 集合中移除所有 `CountItem` 对象。 |

### DCS1_SaveOptions

使用 `Document.saveAs()` 方法将 CMYK 文档保存为 DCS1 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| dcs | `DCSType` | 读写。（默认：`DCSType.COLORCOMPOSITE`）。 |
| embedColorProfile | boolean | 读写。为 true 则在文档中嵌入颜色配置文件。 |
| encoding | `SaveEncoding` | 读写。文档使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| halftoneScreen | boolean | 读写。为 true 则包含半调网屏（默认：`false`）。 |
| interpolation | boolean | 读写。为 true 则使用图像插值（默认：`false`）。 |
| preview | `Preview` | 读写。预览类型（默认：`Preview.MACOSEIGHTBIT`）。 |
| transferFunction | boolean | 读写。为 true 则包含传输函数，以补偿图像和胶片之间的网点增大（默认：`false`）。 |
| typename | string | 只读。所引用的 `DCS1_SaveOptions` 对象的类名。 |
| vectorData | boolean | 读写。为 true 则包含矢量数据。仅在文档包含矢量数据（未栅格化的文本）时有效。 |

### DCS2_SaveOptions

使用 `Document.saveAs()` 方法将 CMYK 文档保存为 DCS2 格式的选项。

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| dcs | `[DCSType](DCSType)` | 读写。创建的合成文件类型（默认：`DCSType.NOCOMPOSITE`）。 |
| embedColorProfile | boolean | 读写。True 表示在文档中嵌入颜色配置文件。 |
| encoding | `[SaveEncoding](SaveEncoding)` | 读写。使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| halftoneScreen | boolean | 读写。True 表示包含半调网屏（默认：`false`）。 |
| interpolation | boolean | 读写。True 表示使用图像插值（默认：`false`）。 |
| multiFileDCS | boolean | 读写。True 表示将颜色通道保存为多个文件或单个文件（默认：`false`）。 |
| preview | `[Preview](Preview)` | 读写。预览类型（默认：`Preview.MACOSEIGHTBIT`）。 |
| spotColors | boolean | 读写。True 表示专色。 |
| transferFunction | boolean | 读写。True 表示用于补偿图像与胶片之间网点扩大的函数（默认：`false`）。 |
| typename | string | 只读。引用的 `DCS2_SaveOptions` 对象的类名。 |
| vectorData | boolean | 读写。True 表示包含矢量数据。仅当文档包含矢量数据（未栅格化的文本）时有效。 |

### DICOMOptions

使用 `Application.open()` 方法打开 DICOM 格式文档的选项。

注意：此功能仅在扩展版中可用。

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `anonymize` | boolean | 读写。True 表示匿名化。 |
| `columns` | number | 读写。n-up 配置中的列。 |
| `reverse` | boolean | 读写。True 表示反转图像。 |
| `rows` | number | 读写。n-up 配置中的行。 |
| `showOverlays` | boolean | 读写。True 表示叠加层。 |
| `typename` | string | 只读。引用的 `DICOMOptions` 对象的类名。 |
| `windowLevel` | number | 读写。图像在 n-up 配置下的对比度。 |
| `windowWidth` | number | 读写。图像在 n-up 配置下的亮度。 |

### Document

脚本中层和其他对象的主要容器；画布。

- 通过 `Application.activeDocument` 访问当前文档。
- 你可以访问其他文档，或使用 `Application.documents` 集合遍历所有文档。通过 `Documents.getByName()` 名称检索它们。
- 使用 `Documents.add()` 方法以方式创建文档。

注意：在 Adobe Photoshop6 中，文档称为图像或画布。

- `image` 指整个文档及其内容。你可以裁剪或修剪图像。使用 `resizeImage()` 方法调整大小。
- `canvas` 指文档在屏幕上占的空间。你可以旋转或翻转画布。使用 `resizeCanvas()` 方法调整大小。

| 属性 | 值类型 | 描述 |
|---|---|---|
| `activeChannels` | `Channel` 数组 | 读写。选定的通道。 |
| `activeHistoryBrush` | `Guide` | 读写。与历史记录笔一起使用的历史状态。 |
| `activeHistoryState` | `Guide` | 读写。选定的 `HistoryState` 对象。 |
| `activeLayer` | `ArtLayer` 或 `LayerSet` | 读写。选定的图层。 |
| `artLayers` | `ArtLayers` | 只读。图层集合。 |
| `backgroundLayer` | `ArtLayer` | 只读。文档的背景图层。 |
| `bitsPerChannel` | `BitsPerChannelType` | 读写。每通道的位数。 |
| `channels` | `Channels` | 只读。通道集合。 |
| `colorProfileName` | string | 读写。颜色配置文件的名称。在 `colorProfileType` = `ColorProfile.CUSTOM` 或 `WORKING` 时有效。 |
| `colorProfileType` | `ColorProfileType` | 读写。文档使用工作颜色配置文件、自定义配置文件还是不使用配置文件。 |
| `colorSamplers` | `ColorSamplers` | 只读。与此文档关联的颜色取样器。 |
| `componentChannels` | `Channel` 数组 | 只读。构成文档的颜色通道；例如，RGB 文的红、绿和蓝通道。 |
| `countItems` | `CountItems` | 只读。当前的计数项目。注意：有关计数项目的更多信息，请参阅 Adobe Photoshop6 帮助中的计数工具。 |
| `fullName` | `File` | 只读。文档的完整路径名。 |
| `guides` | `Guides` | 只读。参考线集合。 |
| `height` | `UnitValue` | 只读。文档的高度（单位值）。 |
| `histogram` | `number` 数组 | 只读。显示合成通道中每个颜色强度级别的像素数量的直方图。数组包含 256 个成员。仅在 `mode` = `DocumentMode.RGB`、`CMYK` 或`INDEXEDCOLOR` 时有效。 |
| `historyStates` | `HistoryStates` | 只读。历史记录状态集合。 |
| `info` | `DocumentInfo` | 只读。文档的元数据。 |
| `layerComps` | `LayerComps` | 只读。图层复合集合。 |
| `layers` | `Layers` | 只读。图层集合。 |
| `layerSets` | `LayerSets` | 只读。图层组集合。 |
| `managed` | `boolean` | 只读。如果文档是工作组文档，则为 True。 |
| `measurementScale` | `MeasurementScale` | 只读。文档的测量比例。注意：测量比例功能仅在扩展版中可用。 |
| `mode` | `DocumentMode` | 只读。颜色配置文件。 |
| `name` | string | 只读。文档的名称。 |
| `parent` | `Application` | 只读。包含文档的应用程序。 |
| `path` | `File` | 只读。路径。 |
| `pathItems` | `PathItems` | 只读。路径集合。 |
| `pixelAspectRatio` | `number` [0..100] | 读写。使用的（自定义）像素宽比。 |
| `printSettings` | `DocumentPrintSettings` | 只读。打印设置。 |
| `quickMaskMode` | `boolean` | 读写。如果文档处于快速蒙版模式，则为 True。 |
| `resolution` | number | 只读。分辨率（每英寸像素）。 |
| `saved` | boolean | 只读。如果上次更改后保存，则为 True。 |
| `selection` | `[Selection]` | 只读。选定区域。 |
| `typename` | string | 只读。`Document` 对象的类名。 |
| `width` | `[UnitValue](UnitValue)` | 只读。宽度（单位值）。 |
| `xmpMetadata` | `[xmpMetadata](xmpMetadata)` | 只读。XMP 数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `autoCount (channel, threshold)` | `Channel` number | | 计算文档中的数量。仅在扩展版中可用。为计数创建一个 `CountItem` 对象。有关如何设置计数的更多信息，请参阅 Adobe Photoshop6 帮助中的计数工具。 |
| `changeMode (destinationMode [, options])` | `BitmapConversionOptions 或 IndexedConversionOptions` | | 更改文档的颜色配置文件。 |
| `close ([saving])` | `SaveOptions` | | 关闭文档。如果进行了任何更改，脚本将显示带有三个选项的：保存、不保存、提示保存（默认：`SaveOptionsType.PROMPTSAVECHANGES`）。 |
| `convertProfile (destinationProfile, intent [, blackPointCompensation])` | string Intent boolean boolean | | 更改颜色配置文件。`destinationProfile` 参数是命名颜色模式的字符串，或者是 `Working RGB`、`Working CMYK`、`Working Gray`、`Lab Color`（表示工作空间之一或 Lab 颜色）。 |
| `crop (bounds [, angle] [, width] [, height])` | 4 个 UnitValue 的数组 number UnitValue | | 裁剪文档。`bounds` 参数是裁剪后剩余区域的四个坐标，`[left, top, right, bottom]`。 |
| `duplicate ([name], mergeLayersOnly])` | string boolean | Document | 创建文档对象的副本。可选参数 `name` 为文档提供名称。可选参数 `mergeLayersOnly` 指示是否仅复制合并的图层。 |

### 方法

| 方法 | 参数类型 | 返回值 | 功能描述（续） |
| :--- | :--- | :--- | :--- |
| `exportDocument(exportIn [, exportAs] [, options])` | File ExportType ExportOptionsIllustrator 或 ExportOptionsSaveForWeb | | 将文档路径导出为 Illustrator 文件，或将文档导出为适用于网页或设备优化的文件。相当于“文件 > 导出 > 路径到 Illustrator”，或“文件 > 存储为 Web 和设备用格式”。 |
| `flatten()` | | | 平整文档中的图层。 |
| `flipCanvas(direction)` | Direction | | 在指定方向上翻转画布内的图像。 |
| `importAnnotations(file)` | File | | 将注释导入文档。 |
| `mergeVisibleLayers()` | | | 平整文档中所有可见的图层。 |
| `paste([intoSelection])` | boolean | ArtLayer | 将剪贴板的内容粘贴到文档中。如果可选参数设置为 `true` 且选区处于状态，则内容将粘贴到选区内。 |
| `print([sourceSpace], [printSpace], [intent], [blackPointCompensation])` | SourceType string Intent boolean | | 打印文档。`printSpace` 指定打印机的色彩空间。有效值为 `nothing`（即与源相同）；或 `Working RGB`、`Working CMYK`、`Working Gray`、`Lab Color`（表示一种工作色彩空间或 Lab 颜色）；或指定特定色彩空间的字符串（默认与源相同）。 |
| `printOneCopy()` | | | 打印文档的一份副本。 |
| `rasterizeAllLayers()` | | | 栅格化所有图层。 |
| `recordMeasurements([source], dataPoints])` | MeasurementSource array of string | | 记录文档的测量数据。 |
| `resizeCanvas([width], [height], [anchor])` | UnitValue UnitValue AnchorPosition | | 更改画布大小以显示更多或更少的图像，但不会更改图像大小。请参阅 `resizeImage`。 |
| `resizeImage([width], [height], [resolution], [resampleMethod])` | UnitValue UnitValue number ResampleMethod | | 调整图像大小。 |
| `revealAll()` | | | 显示所有被裁切的部分。 |
| `rotateCanvas(angle)` | number | | 按顺针方向旋转画布。 |
| `save()` | | | 保存文档。 |
| `saveAs(exportIn [, exportAs] [, options])` | File ExportType ExportOptionsIllustrator 或 ExportOptionsSaveForWeb | | 以指定格式保存。格式之一：PS, TIFF, JPEG, PNG, PDF, EPS, GIF, DICOM, RAW。 |

```

```
// Save the current preferences

var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CS6 to use pixels and display no dialogs

app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

// first close all the open documents

while (app.documents.length) {
    app.activeDocument.close()
}

// Open the sunflower and duck files from the samples folder
var flowerDoc = open(File(app.path + "/Samples/Sunflower.psd"))
var duckDoc = open(File(app.path + "/Samples/Ducky.tif"))

// Find out which document is larger
// Resize the smaller document the to the larger document's size
// The resize requires the document be the active/front document
if ((flowerDoc.width.value * flowerDoc.height.value) >
        (duckDoc.width.value * duckDoc.height.value)) {
    app.activeDocument = duckDoc
    duckDoc.resize(flowerDoc.width, flowerDoc.height)
}
else {
    app.activeDocument = flowerDoc
    flowerDoc.resizeImage(duckDoc.width, duckDoc.height)
}

// Create a new document twice as high as two files
var mergedDoc = app.documents.add(duckDoc.width, duckDoc.height * 2,
    duckDoc.resolution, "FlowerOverDuck")

// Copy the flower to the top; make it the active document so we can manipulate it
app.activeDocument = flowerDoc
flowerDoc.activeLayer.copy()

//Paste the flower to the merged document, making the merged document active
app.activeDocument = mergedDoc

// Select a square area at the top of the new document
var selRegion = Array(Array(0, 0),
                        Array(mergedDoc.width.value, 0),
                        Array(mergedDoc.width.value, mergedDoc.height.value / 2),
                        Array(0, mergedDoc.height.value / 2),
                        Array(0, 0))

// Create the selection
mergedDoc.selection.select(selRegion)

//Paste in the flower
mergedDoc.paste(TRUE)

// do the same thing for the duck
app.activeDocument = duckDoc
duckDoc.activeLayer.copy()
app.activeDocument = mergedDoc
mergedDoc.selection.select(selRegion)

// Inverting the selection so the bottom of the document is now selected
mergedDoc.selection.invert()

// Paste the duck
mergedDoc.paste(TRUE)

// get rid of our originals without modifying them
duckDoc.close(SaveOptions.DONOTSAVECHANGES)
flowerDoc.close(SaveOptions.DONOTSAVECHANGES)

// Reset the application preferences
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.displayDialogs = startDisplayDialogs
```

### DocumentPrintSettings

文档的打印设置。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| backgroundColor | SolidColor | 可读写。页面的背景色。 |
| bleedWidth | UnitValue | 可读写。出血宽度。 |
| caption | boolean | 可读写。打印 FileInfo 中找到的标题。 |
| centerCropMarks | boolean | 可读写。打印中心裁切标记。 |
| colorBars | boolean | 可读写。打印颜色校准条。 |
| copies | number | 可读写。要打印的份数。 |
| cornerCropMarks | boolean | 可读写。打印角落裁切标记。 |
| colorHandling | PrintColorHandling | 只读。颜色处理。 |
| activePrinter | string | 可读写。当前活动的打印机。 |
| flip | boolean | 可读写。水平翻转图像。 |
| hardProof | boolean | 可读写。打印硬校样。 |
| interpolate | boolean | 可读写。 |
| labels | boolean | 可读写。打印文档标题。 |
| mapBlack | boolean | 可读写。映射黑色。 |
| negative | boolean | 可读写。反转图像颜色。 |
| renderIntent | Intent | 可读写。当打印空间与源空间不同时的颜色转换意向。 |
| posX | UnitValue | 只读。图像在页面上的 X 位置。 |
| posY | UnitValue | 只读。图像在页面上的 Y 位置。 |
| printBorder | UnitValue | 可读写。打印边框的宽度。 |
| printerName | string | 可读写。打印机的名称。 |
| printSpace | string | 可读写。打印机的色彩空间。可以是 nothing（表示与源相同）；'Working RGB'、'Working CMYK'、'Working Gray'、'Lab Color'（表示一种工作空间或 Lab 颜色）；或指定特定色彩空间的字符串（默认与源相同）。 |
| registrationMarks | boolean | 可读写。打印套准标记。 |

## 属性

| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| scale | `number` | 只读。图像在页面上的缩放比例。 |
| vectorData | `boolean` | 读写。是否包含矢量数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| :--- | :--- | :--- | :--- |
| `setPagePosition(docPosition, posY, scale)` | `DocPosition`<br>`UnitValue`<br>`UnitValue`<br>`number | | 设置图像在页面上的位置。 |

### DocumentInfo

关于`document`对象的元数据。
可通过`Document.info`属性访问。例如，以下代码设置了`author`、`caption` 和`copyrighted`属性：

```
var docRef = open(fileList[i])
// set the file info
docRef.info.author = "Mr. Adobe programmer"
docRef.info.caption = "Adobe shoot"
docRef.info.copyrighted = CopyrightedType.RIGHTEDWORK
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| author | string | 读写。 |
| authorPosition | string | 读写。 |
| caption | string | 读写。 |
| captionWriter | string | 读写。 |
| category | string | 读写。 |
| city | string | 读写。 |
| copyrighted | `CopyrightedType` | 读写。版权状态。 |
| copyrightNotice | string | 读写。 |
| country | string | 读写。 |
| creationDate | string | 读写。 |
| credit | string | 读写。 |
| exif | array of array [tag] | 只读。包含图像时使用的相机等数据。每个数员是一个标签，即`[tag, data]` 的数组；例如`["camera"]`。 |
| headline | string | 读写。 |
| instructions | string | 读写。 |
| jobName | string | 读写。 |
| keywords | array of string | 读写。用于标识文档或其内容的列表。 |
| ownerUrl | string | 读写。 |
| parent | `Document` | 只读。信息的容器。 |
| provinceState | string | 读写。 |
| source | string | 读写。 |
| supplementalCategories | array of string | 读写。 |
| title | string | 读写。 |
| transmissionReference | string | 读写。 |
| typename | string | 只读。引用的信息的类名。 |
| urgency | `Urgency` | 读写。 |

#### DocumentInfo 脚本

以下脚本为指定文件夹中的文件设置文档信息（元数据），将修改后的文件以低质量 JPEG 保存到新文件夹中，而不更改文件。
- 要求用户指定原始文件的文件夹和输出 JPEG 图像的文件夹，然后检查文件夹是否存在。
- 打开每个文件，并使用 documentInfo属性为其添加元数据：
    - author: Adobe programmer
    - caption: Adobe Photo shoot
    - captionWriter: Adobe programmer
    - city: San Jose
    - copyrightNotice: Copyright (c) Adobe programmer Photography
    - copyrighted status: Copyrighted Work
    - country: USA
    - state: CA
- 将新文档保存为 JPEG 格式，并设置低质量。

**DocumentInfo.jsx**

```
// Save the current preferences
var startDisplayDialogs = app.displayDialogs
// Set Adobe Photoshop CS6 to use pixels and display no dialogs
app.displayDialogs = DialogModes.NO
// ask the user for the input and output folders
var inputFolder = Folder.selectDialog("Select a folder to tag")
var outputFolder = Folder.selectDialog("Select a folder for the output files")
// see if we got something from the dialog
if (inputFolder != null && outputFolder != null) {
    // get all the files found in this folder
    var fileList = inputFolder.getFiles()
}
// save the outputs in JPEG
var jpegOptions = new JPEGSaveOptions()
// set the jpeg quality really low so the files are small
jpegOptions.quality = 1
// open each one in turn
for (var i = 0; i < fileList.length; i++) {
    // The fileList includes both folders and files so open only files
    if (fileList[i] instanceof File && fileList[i].hidden == false) {
        // get a reference to the new document
        var docRef = open(fileList[i])
        // tag all of the documents with photo shoot information
        docRef.info.author = "Adobe programmer"
        docRef.info.caption = "Adobe Photo shoot"
        docRef.info.captionWriter = "Adobe programmer"
        docRef.info.city = "San Jose"
        docRef.info.copyrightNotice = "Copyright (c) Adobe programmer Photography"
        docRef.info.copyrighted = CopyrightedType.COPYRIGHTEDWORK
        docRef.info.country = "USA"
        docRef.info.provinceState = "CA"
        // change the date to a Adobe Photoshop CS6 date format
        // "YYYYMMDD"
        var theDate = new Date()
        // the year is from 1900 ???? 
        var theYear = (theDate.getYear() + 1900).toString()
        // convert the month from 0..12 to 00..12
        var theMonth = theDate.getMonth().toString()
        if (theDate.getMonth() < 10) {
            theMonth = "0" + theMonth
        }
        // convert the day from 0..31 to 00..31
```

```
        var theDay = theDate.getDate().toString()

        if (theDate.getDate() < 10) {
            theDay = "0" + theDay
        }

        // stick them all together
        docRef.info.creationDate = theYear + theMonth + theDay

        // flatten because we are saving to JPEG
        docRef.flatten()

        // go to 8 bit because we are saving to JPEG
        docRef.bitsPerChannel = BitsPerChannelType.EIGHT

        // save and close

        docRef.saveAs(new File(outputFolder + "/Output" + i + ".jpg"), jpegOptions)

        // don't modify the original
        docRef.close(SaveOptions.DONOTSAVECHANGES)

    }

}

// Reset the application preferences

app.displayDialogs = startDisplayDialogs
```

### Documents

已打开的 [Document](https://www.adobe.com/) 对象的集合。

可通过 [Application.documents](https://www.adobe.com/) 集合属性访问此列表，该属性可通过 `app` 全局变量使用，或直接在顶层使用。例如，以下代码向集合中添加了一个新文档：

```
app.documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```

—or—

```
documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```

```markdown
## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。`documents` 集合中的元素数量。 |
| `parent` | [Application](https://www.adobe.com/) | 只读。包含它的应用程序。 |
| `typename` | `string` | 只读。引用的 `documents` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| :--- | :--- | :--- | :--- |
| `add` ([width], [height], [resolution], [name], [mode], [initialFill], [pixelAspectRatio], [bitsPerChannel], [colorProfileName]) | [UnitValue](https://www.adobe.com/) [UnitValue](https://www.adobe.com/) `number` `string` [NewDocumentMode](https://www.adobe.com/) [DocumentFill](https://www.adobe.com/) `number [0.1..10.00]` [BitsPerChannelType](https://www.adobe.com/) `string` | [Document](https://www.adobe.com/) | 创建一个新的文档对象并将其添加到此集合中。<br><br> `pixelAspectRatio`: 默认值为 1.0，即正方形宽高比。<br><br> `bitsPerChannelType`: 默认值为 `BitsPerChannelType.EIGHT`。 |
| `getByName` (name) | `string` | [Document](https://www.adobe.com/) | 获取 `documents` 集合中具有提供名称的第一个元素 |

### EPSOpenOptions

使用 `Application.open()`(Application.open()) 方法打开 EPS 格式文档时的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `antiAlias` | boolean | 读写。为 true 时使用抗锯齿。 |
| `constrainProportions` | boolean | 读写。为 true 时约束图像的比例。 |
| `height` | UnitValue | 读写。图像的高度（单位值）。 |
| `mode` | OpenDocumentMode | 读写。用作文档模式的色彩配置文件。 |
| `resolution` | number | 读写。文档的分辨率，单位为像素/英寸。 |
| `typename` | string | 只读。引用的 EPSOpenOptions 对象的类名。 |
| `width` | UnitValue | 读写。图像的宽度（单位值）。 |

### EPSSaveOptions

使用 `Document.saveAs()`(#) 方法将文档保存为 EPS 格式时的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| embedColorProfile | boolean | 可读写。设为 true 以在本文档中嵌入颜色配置文件。 |
| encoding | [SaveEncoding](#) | 读写。使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| halftoneScreen | boolean | 读写。设为 true 以包含半调网屏（默认：false）。 |
| interpolation | boolean | 读写。为 true 以使用图像插值（默认：false）。 |
| preview | [Preview](#) | 读写。预览类型。 |
| psColorManagement | boolean | 读写。设为 true 以使用 Postscript 颜色管理（默认：false）。 |
| transferFunction | boolean | 读写。为 true 以包含用于补偿图像与胶片之间网点扩大的传递函数（默认：false）。 |
| transparentWhites | boolean | 读写。为 true 以将白色区域显示为透明。仅在 `document.mode = DocumentMode.BITMAP` 时有效。另请参见 `changeMode()`(#)。 |
| typename | string | 只读。所引用的 EPSSaveOptions 对象的类名。 |
| vectorData | boolean | 读写。为 true 以包含矢量数据。仅当文档包含矢量数据（文本）时有效。 |

### ExportOptionsIllustrator

使用 `Document.exportDocument()` 方法将 `PathItem` 对象导出到 Adobe Illustrator® 文件时的选项。当您选择 **文件 > 导出 > 路径到 Illustrator** 时，可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `path` | `IllustratorPathType` | 读写。要导出的路径类型（默认：`IllustratorPathType.DOCUMENTBOUNDS`）。 |
| `pathName` | `string` | 读写。要导出的路径的名称。仅当 `path = IllustratorPathType.NAMEDPATH` 时有效。 |
| `typename` | `string` | 只读。所引用的 `exportOptionsIllustrator` 对象的类名。 |

### ExportOptionsSaveForWeb

使用 `Document.exportDocument()` 方法优化文档以用于 Web 或设备时的选项。当您选择文件 > 存储为 Web 和设备所用格式时，可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| blur | number | 读写。对图像应用模糊以减少伪影（默认：0.0）。 |
| colorReduction | ColorReductionType | 读写。颜色减低算法（默认：`ColorReductionType.SELECTIVE`）。 |
| colors | number | 读写。调色板中的颜色数量（默认：256）。 |
| dither | Dither | 读写。仿色类型（默认：`Dither.DIFFUSION`）。 |
| ditherAmount | number | 读写。仿色量（默认：100）。仅当 `dither = Dither.DIFFUSION` 时有效。 |
| format | SaveDocumentType | 读写。使用的格式（默认：`SaveDocumentType.COMPSERVE`）。**注意：** 对于此属性，仅支持 `COMPSERVEGIF`、`JPEG`、`PNG-8` 和 `BMP`。 |
| includeProfile | boolean | 读写。为 true 以包含文档（默认：false）。 |
| interlaced | boolean | 读写。为 true 以多次下载；渐进式（默认：false）。 |
| lossy | number | 读写。允许的有压缩量（默认：0）。 |
| matteColor | RGBColor | 读写。透明像素混合的颜色。 |
| optimized | boolean | 读写。为 true 创建更小但兼容性差的文件（默认：true）。当 `format = SaveDocumentType.JPEG` 时有效。 |
| PNG8 | boolean | 读写。指定位数；true = 8，false = 24（默认：true）。当 `format = SaveDocumentType.PNG` 时有效。 |
| `quality` | `number` [0..100] | 读写。生成图像的质量比；默认：60。 |
| `transparency` | boolean | 读写。指示图像透明区域是否包含在图像中（默认：true）。 |
| `transparencyAmount` | number | 读写。透明色量（默认：100）。当 `transparency = true` 时有效。 |
| `transparencyDither` | Dither | 读写。透明色算法（默认：`transparencyDither = Dither.NONE`）。 |
| `typename` | `string` | 只读。引用的 `ExportSaveForWeb` 对象的类名。 |
| `webSnap` | `number` | 读写。将相近颜色附到 Web 调色板颜色的差量（默认：0）。 |

### File

ExtendScript 定义了 类 `File` 和 `Folder`，以平台无关的方式封装文件系统；详见第32 页的 Adobe Photoshop CS6 中的这些类的详细参考，请查阅 *JavaScript指南*。

### GalleryBannerOptions

`GalleryOptions` 对象的 `bannerOptions` 属性。

**提示：** 您可以通过 `GalleryOptions` 属性 `preserveAllMetadata` 设置为 true 来保留许多属性的默认值；这与选择 **文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择 **保留元数据** 效果相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `contactInfo` | `string` | 读写。Web 照片库的联系信息。 |
| `date` | `string` | 读写。Web 照片库的日期（默认：当前日期）。 |
| `font` | GalleryFontType | 读写。横幅文本的字体设置（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number` [1..7] | 读写。横幅文本的字体大小（默认：3）。 |
| `photographer` | `string` | 读写。Web 照片库的摄影师。 |
| `siteName` | `string` | 读写。Web 照片库的站点名称（默认：Adobe Web Photo Gallery）。 |
| `typename` | `string` | 只读。引用的 galleryBannerOptions 对象的类名。 |

### GalleryCustomColorOptions

`GalleryOptions` 对象的 `customColorOptions` 属性。

**提示：** 您可以通过 `GalleryOptions` 属性 `preserveAllMetadata` 设置为 true 来保留许多属性的默认值；这等于选择 **文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择 **保留所有元数据** 效果相同。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| activeLinkColor | RGBColor | 读写。用于指示活动链接的颜色。 |
| backgroundColor | RGBColor | 读写。背景颜色。 |
| bannerColor | RGBColor | 读写。横幅颜色。 |
| linkColor | RGBColor | 读写。用于指示链接的颜色。 |
| textColor | RGBColor | 读写。文本颜色。 |
| typename | string | 只读。引用的 galleryCustomColorOptions 对象的类名。 |
| visitedLinkColor | RGBColor | 读写。用于指示已访问链接的颜色。 |

### GalleryImagesOptions

`GalleryOptions` 对象的 `imagesOptions` 属性的选项。

**提示：** 您可以通过 `GalleryOptions` 属性 `preserveAllMetadata` 设置为 true 来保留许多属性的默认值；这与选择 **文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择 **保留所有数据** 效果相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| border | number [0..99] | 读写。分隔图像的边框（以像素为单位）（默认：0）。 |
| caption | boolean | 读写。为 true 生成图像说明（默认：false）。 |
| dimension | number | 读写。调整后的图像尺寸（以像素为单位）（默认：350）。当 `resizeImages = true` 时有效。 |
| font | GalleryFontType | 读写。用于图像说明的字体（默认：`GalleryFontType.ARIAL`）。 |
| fontSize | number [1..7] | 读写。图像说明的字体大小（默认：3）。当 `resizeImages = true` 时有效。 |
| imageQuality | number [0..12] | 读写。JPEG图像的质量（默认：5）。 |
| includeCopyright | boolean | 读写。为 true 在说明中包含版权（默认：false）。当 `resizeImages = true` 时有效。 |
| includeCredits | boolean | 读写。为 true 在说明中包含致谢信息（默认：false）。当 `resizeImages = true` 时有效。 |
| includeFilename | boolean | 读写。为 true 在说明中包含文件名（默认：true）。当 `resizeImages = true` 时有效。 |
| includeTitle | boolean | 读写。为 true 在图像说明中包含标题（默认：false）。当 `resizeImages = true` 时有效。 |
| numericLinks | boolean | 读写。为 true 添加数字链接（默认：true）。 |

#### GalleryImagesOptions（续）

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `resizeConstraint` | GalleryConstrainType | 读写。图库图像中约束的图像尺寸（默认：`GalleryConstrainType.CONSTRAINBOTH`）。当 `resizeImages = true` 时有效。 |
| `resizeImages` | boolean | 读写。为 true 时自动调整图像大小放置在图库页面上（默认：true）。 |
| `typename` | string | 只读。引用的 `galleryImagesOptions` 对象的类名。 |

### GalleryOptions

网络照片库的选项，通过 `Application.makePhotoGallery()` 创建。

**提示：** 你可以通过选择 **文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择 **保留元数据** 来保留许多属性的默认值。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| addSizeAttributes | boolean | 读写。为 true 时，为图像添加宽度高度属性（默认：true）。 |
| bannerOptions | GalleryBannerOptions | 读写。与横幅设置相关的选项。 |
| customColorOptions | GalleryCustomColorOptions | 读写。与自定义颜色设置相关的选项。 |
| emailAddress | string | 读写。要在网页上显示的电子邮件地址。 |
| imagesOptions | GalleryImagesOptions | 读写。与图像设置相关的选项。 |
| includeSubFolders | boolean | 读写。为 true 时，包含输入文件夹子中的所有文件（默认：true）。 |
| layoutStyle | string | 读写。用于布局网页的样式（默认：居中框架1 - 基本）。 |
| preserveAllMetadata | boolean | 读写。为 true 时保存元数据（默认：false）。 |
| securityOptions | GallerySecurityOptions | 读写。与安全设置相关的选项。 |
| thumbnailOptions | GalleryThumbnailOptions | 读写。与缩略图像设置相关的选项。 |
| typename | string | 只读。引用的 `galleryOptions` 对象的类名。 |
| useShortExtension | boolean | 读写。为 true 时使用简短的网页扩展名 .htm。如果为 false，则使用网页扩展名 .html（默认：true）。 |
| useUTF8Encoding | boolean | 读写。为 true 时使用 UTF-8 编码处理网页（默认：false）。 |

### GallerySecurityOptions

`GalleryOptions` 对象的 `securityOptions` 属性的选项。

**提示：** 你可以通过 `GalleryOptions` 属性 `preserveAllMetadata` 设置为 true 来保留许多属性的默认值；这等于选择 **文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择 **保留所有元数据**。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| content | GallerySecurityType | 读写。网络照片图库的安全内容（默认：`GallerySecurityType.NONE`）。 |
| font | GalleryFontType | 读写。网络照片图库的字体（默认：`GalleryFontType.ARIAL`）。 |
| fontSize | number [1..72] | 读写。网络照片图库的字体大小（默认：3）。 |
| opacity | number | 读写。网页安全的透明度（以百分比表示）（默认：100）。 |
| text | string | 读写。网络照片图库的自定义文本。 |
| textColor | GalleryTextColorType | 读写。网页安全的文本颜色。 |
| textPosition | GalleryTextPositionType | 读写。网络照片图库的安全文本位置（默认：`GalleryTextPositionType.CENTERED`）。 |
| textRotate | GalleryTextRotateType | 读写。网络照片图库的安全文本方向（默认：`GalleryTextRotateType.ZERO`）。 |
| typename | string | 只读。引用的 `gallerySecurityOptions` 对象的类名。 |

### GalleryThumbnailOptions

`GalleryOptions` 对象的 `thumbnailOptions` 属性。

**提示：** 你可以通过 `GalleryOptions` 属性 `preserveAllMetadata` 设置为 true 来保留许多属性的默认值；这等于选择 **文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择 **保留所有数据**。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| border | number [0..99] | 读写。你希望围绕缩略图像的边框（默认：0）。 |
| caption | boolean | 读写。为 true 时，有文字（默认：false）。 |
| columnCount | number | 读写。页面上的列数（默认：5）。 |
| dimension | number | 读写。网络照片图库缩略图的尺寸（以像素为单位）（默认：75）。 |
| font | GalleryFontType | 读写。网络照片图库字体（默认：`GalleryFontType.ARIAL`）。 |
| fontSize | number [1..7] | 读写。缩略图像文本的字体大小（默认：3）。 |
| includeCopyright | boolean | 读写。为 true 时包含缩略图的版权信息（默认：false）。 |
| includeCredits | boolean | 读写。为 true 时包含缩略图的致谢信息（默认：false）。 |
| includeFilename | boolean | 读写。为 true 时包含缩略图的文件名（默认：false）。 |
| includeTitle | boolean | 读写。为 true 时包含缩略图的标题（默认：false）。 |
| rowCount | number | 读写。页面上的行数（默认：3）。 |
| size | GalleryThumbSizeType | 读写。缩略图图像大小（默认：`GalleryThumbSizeType.MEDIUM`）。 |
| typename | string | 只读。引用的 `GalleryThumbnailOptions` 对象的类名。 |

### GIFSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 GIF 格式时的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| colors | number | 读写。调色板颜色的数量。仅在 `palette = Palette.LOCALADAPTIVE`, `LOCALPERCEPTUAL`, `LOCALSELECTIVE`, `MACOSPALETTE`, `UNIFORM`, `WEBPALETTE`, 或 `WINDOWSPALETTE` 时有效。 |
| dither | Dither | 读写。抖动类型。 |
| ditherAmount | number [1..100] | 读写。抖动量（默认：75）。当 `dither = Dither.DIFFUSION` 时有效。 |
| forced | ForcedColors | 读写。要强制添加到颜色色板中的颜色类型。 |
| interlaced | boolean | 读写。为 true 时，行应交错排列（默认：false）。 |
| matte | MatteType | 读写。用于填充图像透明区域相邻抗锯齿边缘的颜色（默认：`MatteType.WHITE`）。当 `transparency = false` 时，哑光颜色将应用于透明区域。 |
| palette | PaletteType | 读写。要使用的调色板类型（默认：`Palette.LOCALSELECTIVE`）。 |
| preserveExactColors | boolean | 读写。为 true 时，保护图像中在颜色表中有条目的颜色免受抖动。当 `dither = Dither.DIFFUSION` 时有效。 |
| transparency | boolean | 读写。为 true 时在转换为 GIF 格式时保留图像的透明区域。 |
| typename | string | 只读。引用的 `GIFSaveOptions` 对象的类名。 |

### GrayColor

定义一种灰色，用于 `SolidColor` 对象中。

另请参阅 `CMYKColor`(object), `HSBColor`(object), `LabColor`(object), `NoColor`(object), `RGBColor`(object)

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| **gray** | number [0.0..100.0] | 读写。灰色值（默认：0.0）。 |
| **typename** | string | 只读。引用的 `grayColor` 对象的类名。 |

### 参考线

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `direction` | Direction | 读写。指示参考线是垂直还是水平。 |
| `coordinate` | UnitValue | 读写。参考线距离图像原点的位置。 |

### 参考线集合

包含所有打开的 `Guide` 对象的集合。

通过 `Document.guides` 集合属性访问此列表，该属性可通过 `activeDocument` 对象获取。例如，以下代码向集合中添加一条新参考线：

```


```markdown
activeDocument.guides.add (Direction.HORIZONTAL,UnitValue(20,20))
```

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `length` | `number` | 只读。`guides` 集合中的元素数量。 |
| `parent` | [Document](https://example.com) | 只读。包含的文档。 |
| `typename` | `string` | 只读。引用的 `guides` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回 | 描述 |
|---|---|---|---|
| `add` (direction, coordinate) | [Direction](https://example.com) [UnitValue](https://example.com) | [Guide](https://example.com) | 创建一个新的参考线对象并将其添加到此集合中。 |
| `getByName` (name) | `string` | [Guide](https://example.com) | 获取 `guides` 集合中具有所提供名称的第一个元素。 |

### HistoryState

文档的一个版本，在文档每次更改时自动存储（并添加到 `HistoryStates` 集合中），它保存了文档的状态。

通过 `Document.historyStates` 集合访问。你可以按名称访问列表中的一个状态。例如，以下代码为名为 "AddLayerMask" 的状态对象中的一个属性赋值：

```javascript
var stateRef = app.activeDocument.historyStates.getByName("AddLayerMask");

stateRef.snapshot = true;
```

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `name` | `string` | 只读。`HistoryState` 对象的名称。 |
| `parent` | [Document](Document) | 只读。包含的文档。 |
| `snapshot` | `boolean` | 只读。如果历史状态是快照则为真。 |
| `typename` | `string` | 只读。引用的 `HistoryState` 对象的类名。 |

### HistoryStates

文档中 [HistoryState](https://example.com) 对象的集合。

通过 [Document.historyStates](https://example.com/historyStates) 集合属性访问。例如，以下代码通过索引访问集合中的一个状态：

```javascript
myState = app.activeDocument.historyStates[7];
```

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。`HistoryStates` 集合中的元素数量。 |
| `parent` | [Document](https://example.com/document) | 只读。包含的文档。 |
| `typename` | `string` | 只读。引用的 `HistoryStates` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回 | 描述 |
| :--- | :--- | :--- | :--- |
| `getByName` (name) | `string` | [HistoryState](https://example.com) | 获取 `HistoryStates` 集合中具有所提供名称的第一个元素。 |

### HSBColor

定义一种 HSB 颜色，用于 [SolidColor](https://example.com) 对象中。

另请参阅 [CMYKColor](https://example.com), [GrayColor](https://example.com), [LabColor](https://example.com), [NoColor](https://example.com), [RGBColor](https://example.com)

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `brightness` | `number [0.0..100.0]` | 读写。亮度值。 |
| `hue` | `number [0.0..360.0]` | 读写。色相值。 |
| `saturation` | `number [0.0..100.0]` | 读写。饱和度值。 |
| `typename` | `string` | 只读。引用的 `HSBColor` 对象的类名。 |

### IndexedConversionOptions

使用 [Document.changeMode()](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/document/Document.html#DocumentChangeMode) 将 RGB 图像转换为索引颜色模型的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `colors` | `number` | 读写。调色板颜色数量。仅在 `palette` = `Palette.LOCALADAPTIVE`, `Palette.LOCALPERCEPTUAL`, `Palette.LOCALSELECTIVE`, `Palette.MACOSPALETTE`, `Palette.UNIFORM`, `Palette.WEBPALETTE`, 或 `Palette.WINDOWSPALETTE` 时有效。 |
| `dither` | [Dither](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/Dither.html) | 读写。仿色类型。 |
| `ditherAmount` | `number [1..100]` | 读写。仿色量。仅在 `dither` = `Dither.diffusion` 时有效。 |
| `forced` | [ForcedColors](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/ForcedColors.html) | 读写。强制添加到颜色调色板中的颜色类型。 |
| `matte` | [MatteType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/MatteType.html) | 读写。用于填充与透明区域相邻的抗齿边缘的颜色（默认：`MatteType.WHITE`）。当 `transparency` = `false` 时，此颜色应用于透明区域。 |
| `palette` | [PaletteType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/PaletteType.html) | 读写。调色板类型（默认：`Palette.EXACT`）。 |
| `preserveExactColors` | `boolean` | 读写。为真时，保护图像中包含在颜色表中的条目免受仿影响。仅在 `dither` = `Dither.diffusion` 时有效。 |
| `transparency` | `boolean` | 读写。为真时，转换为 GIF 格式期间保留透明区域。 |
| `typename` | `string` | 只读。引用的 `IndexedConversionOptions` 对象的类名。 |

### JPEGSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 JPEG 格式的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `embedColorProfile` | `boolean` | 读写。为真时，文档中嵌入配置文件。 |
| `formatOptions` | `FormatOptions` | 读写。使用的格式（默认：`FormatOptions.STANDARDBLINE`）。 |
| `matte` | `MatteType` | 读写。用于填充与透明区域相邻的抗齿边缘的颜色（默认：`MatteType.WHITE`）。当透明度关闭时，此颜色应用于透明区域。 |
| `quality` | `number [0..12]` | 读写。使用的图像质量；影响文件大小（默认：3）。 |
| `scans` | `number [3..5]` | 读写。在页面上增量显示所需的次数（默认：3）。仅在 `formatOptions` = `FormatOptions.PROGRESSIVE` 时有效。 |
| `typename` | `string` | 只读。引用的 `JPEGSaveOptions` 对象的类名。 |

### LabColor

定义一种 LAB 颜色，用于 [SolidColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html) 对象中。

另请参阅 [CMYKColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html), [GrayColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html), [HSBColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html), [NoColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html), [RGBColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html) |

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `a` | `number [-128.0..127.0]` | 读写。`a` 值。 |
| `b` | `number [-128.0..127.0]` | 读写。`b` 值。 |
| `l` | `number [0.0..100.0]` | 读写。`l` 值。 |
| `typename` | `string` | 只读。引用的 `LabColor` 对象的类名。 |

## 图层复合

图层复合是文档中图层状态的快照，用于查看不同的页面布局或合成效果。

通过 `Document.layerComps` 集合访问。你可以通过图层复合的名称访问它。例如，以下代码为名为 `myLayerComp` 的 `LayerComp` 对象设置 `comment` 属性值：

```javascript
var layercompRef = app.activeDocument.layerComps.getByName("myLayerComp");

layercompRef.comment = "View from shoreline";
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `appearance` | `boolean` | 读写。如果为 true，则使用图层外观（图层样式）设置。 |
| `comment` | `string` | 读写。图层复合的描述。 |
| `name` | `string` | 读写。图层复合的名称。 |
| `parent` | [Document](Document) | 读写。所属文档。 |
| `position` | `boolean` | 读写。如果为 true，则使用图层位置。 |
| `selected` | `boolean` | 只读。如果图层复合当前被选中，则为 true。 |
| `typename` | `string` | 只读。所引用 `layerComp` 对象的类名。 |
| `visibility` | `boolean` | 读写。如果为 true，则使用图层可见性设置。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `apply()` | | | 将图层复合应用于文档。 |
| `recapture()` | | | 为此图层复合重新捕获当前的图层状态。 |
| `remove()` | | | 删除 `layerComp` 对象。 |
| `resetfromComp()` | | | 将图层复合状态重置为文档状态。 |

### LayerComps

文档中的 `LayerComp` 对象集合。

通过 `Document.layerComps` 集合属性访问。例如：

```javascript
app.activeDocument.layerComps.add("myLayerComp", "View from shoreline", true, true);
```

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。`Comps` 集合中的元素数量。 |
| `parent` | [Document](Document) | 只读。所属文档。 |
| `typename` | `string` | 只读。引用的 `Comps` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回 | 描述 |
| :--- | :--- | :--- | :--- |
| `add` (name, comment, appearance, position) | string, boolean, boolean | `LayerComp` | 创建一个新的图层合成对象并将其添加到此集合中。 |
| `getByName` (name) | `string` | `LayerComp` | 获取集合中具有指定名称的第一个元素。 |
| `removeAll()` | | | 从 `Comps` 集合中移除所有成员。 |

### Layers

文档中的图层对象集合，包括 [ArtLayer](ArtLayer) 和 [LayerSet](LayerSet) 对象。通过 [Document.layers](Document.layers) 或 [LayerSet.layers](LayerSet.layers) 集合属性访问。

例如，以下代码使用 `length` 属性计算活动文档中 `layer` 对象的数量，然后在屏幕上显示该数字：

```javascript
var layerNum = app.activeDocument.layers.length
alert(layerNum)
```

## 属性

| 属性 | 值类型 |  |
| :--- | :--- | :--- |
| `length` | `number` | 只读。`layers` 集合中的元素数量。 |
| `parent` | [Document](Document) 或 [LayerSet](LayerSet) | 只读。所属文档或图层集。 |
| `typename` | `string` | 只读。所引用 `layers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回 | 描述 |
| :--- | :--- | :--- | :--- |
| `getByName` (name) | `string` | `Layer` | 获取 `layers` 集合中具有指定名称的第一个元素。 |
| `removeAll()` | | | 从 `layers` 集合中移除所有成员。 |

### LayerSet

图层对象的集合，可以包含 `ArtLayer` 对象和其他（嵌套的）`LayerSet` 对象。一个命令可以操作该集合中的所有图层。

通过 `Document.layerSets` 集合访问文档中的顶级图层集。你可以按名称访问图层集。例如，以下代码为 "myLayerSet" 设置 `allLocked` 值：

```javascript
var layerSetRef = app.activeDocument.layerSets.getByName("myLayerSet");

layerSetRef.allLocked = true
```

通过父级集合中的 `LayerSet.layerSets` 集合访问嵌套的图层集。例如：

```javascript
app.activeDocument.layerSets[0].layerSets[0];
```
```

```markdown
## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| allLocked | 布尔值 | 可读写。如果此集中图层的内容不可编辑，则为 true。 |
| artLayers | ArtLayers | 只读。此图层集中的普通图层。 |
| blendMode | BlendMode | 可读写。图层集使用的混合模式。 |
| bounds | UnitValue 数组 | 只读。图层集的边界矩形。 |
| enabledChannels | Channel 数组 | 可读写。为图层集启用的通道；必须是成分通道的列表。请参见 `Channel.kind`。 |
| layers | Layers | 只读。此图层集中的图层。 |
| layerSets | LayerSets | 只读。包含在此图层集中的嵌套图层集。 |
| linkedLayers | ArtLayer 和/或 LayerSet 数组 | 只读。链接到此 `layerSet` 对象的图层。 |
| name | 字符串 | 可读写。此图层集的名称。 |
| opacity | 数字 [0.0..100.0] | 可读写。图层集的总体不透明度。 |
| parent | Document 或 LayerSet | 只读。所属文档或图层集。 |
| typename | 字符串 | 只读。所引用 `LayerSet` 对象的类名。 |
| visible | 布尔值 | 可读写。如果图层集可见，则为 true。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| duplicate ([relativeObject][, insertionLocation]) | ArtLayer 或 LayerSet, ElementPlacement | LayerSet | 创建对象的副本。 |
| link (with) | ArtLayer 或 LayerSet | | 将图层集与另一个图层链接。 |
| merge () | | ArtLayer | 合并图层集；返回此方法创建的普通图层的引用。 |
| move (relativeObject, insertionLocation) | ArtLayer 或 LayerSet, ElementPlacement | | 移动对象。 |
| remove () | | | 删除对象。 |
| resize ([horizontal][, vertical][, anchor]) | 数字，数字，AnchorPosition | | 将图层集中的所有图层调整为指定尺寸（作为其当前尺寸的百分比），并将图层集置于指定位置。 |
| rotate (angle[, anchor]) | 数字，AnchorPosition | | 围绕指定锚点（默认：AnchorPosition.MIDDLECENTER）旋转图层集中的所有图层。 |
| translate ([deltaX][, deltaY]) | UnitValue，UnitValue | | 相对于其当前位置移动位置。 |
| unlink () | | | 取消链接图层集。 |

### LayerSets

文档中的 `LayerSet` 对象集合。

通过 `Document.layerSets` 集合属性访问文档中的顶级图层集。例如：

```javascript
var layerSetRef = app.activeDocument.layerSets.add()
```

通过父级集合中的 `LayerSet.layerSets` 集合属性访问嵌套的图层集。例如：

```javascript
var layerSetRef = app.activeDocument.layerSets.getByName("myParentSet");
var childSet = layerSetRef.layerSets.getByName("myChildSet");
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| length | 数字 | 只读。`LayerSets` 集合中的元素数量。 |
| parent | Document 或 LayerSet | 只读。所属文档或图层集。 |
| typename | 字符串 | 只读。所引用 `layerSets` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| add () | | LayerSet | 创建一个新的图层集对象，并将其添加到集合中。 |
| getByName (name) | 字符串 | LayerSet | 获取集合中具有指定名称的第一个元素。 |
| removeAll () | | | 从文档中移除所有成员图层集，以及它们包含的任何图层或图层集。 |

#### LayerSets 示例脚本

以下脚本创建三个图层集，然后在每个图层集中嵌套第二个图层集，并在每个嵌套集中创建一个文本图层，显示文本 "Layer in *n* Set Inside *n* Set"，其中 *n* 代表图层集的序数（第一、第二或第三）。

**注意：** 此脚本使用 ExtendScript `$` 调试对象。有关更多详细信息，请参阅 *JavaScript 工具指南*。

**LayerSets.jsx**

```javascript
$.level = 1
//关闭所有打开的文档
while (app.documents.length) {
```

### MeasurementLog

应用程序的测量日志。通过 `Application.measurementLog` 属性访问。

**注意：** 此功能仅在扩展版本中可用。

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `exportMeasurements`<br>(`[file]`<br>`[, range]`<br>`[, dataPoints])` | `File`<br>`MeasurementRange`<br>字符串数组 | | 将测量数据导出到文件。 |
| `deleteMeasurements`<br>(`[range]`) | `MeasurementRange` | | 从日志中删除测量数据。 |

### MeasurementScale

文档的测量比例尺。通过 `Document.measurementScale` 属性访问。例如：

```
app.activeDocument.measurementScale.pixelLength = 25
```

> **注意：** 此功能仅在扩展版本中可用。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| pixelLength | number | 可读写。比例尺对应的像素长度。 |
| logicalLength | number | 可读写。比例尺对应的逻辑长度。 |
| logicalUnits | string | 可读写。比例尺逻辑单位。 |

### NoColor

表示一个缺失的颜色，用于 `SolidColor` 对象中。

另参阅 `CMYKColor`、`GrayColor`、`HSBColor`、`LabColor`、`RGBColor`。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| typename | string | 只读。引用的 `noColor` 对象的类名。 |

### Notifier

一个事件处理对象，用于告知脚本在指定事件发生时执行特定代码。必须使用 `Application.notifiers` 属性通过 `notifiers` 集合访问。
**注意：** 脚本内部事件通常不会触发通知器，因为它们发生在“脚本”事件内部。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `event` | `string` | 只读。事件标识符，一个字符代码或唯一字符串。四字符列表，请参阅附录 A：事件 ID。 |
| `eventClass` | `string` | 只读。事件标识符，一个字符代码或唯一字符串。当一个事件适用于多种类型的对象时，使用此属性来区分通知器适用于哪个对象。例如，Make 事件（`Mk `）适用于文档（`Dcmn`）、通道（`Chnl`）和其他对象。 |
| `eventFile` | `File` | 只读。事件发生并激活通知器时执行文件的路径。 |
| `parent` | `Application` | 只读的包含。 |
| `typename` | `string` | 只读。对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
|---|---|---|
| `remove()` | | | 删除对象。您也可以通过从 Photoshop 偏设置文件夹中删除名为 `Script Events Manager.xml` 的文件，从脚本事件管理器下拉列表中移除一个 `Notifier` 对象。有关更多信息，请参阅 Adobe Photoshop CS6 帮助。 |

### Notifiers

文档中的 `Notifier` 对象集合。通过 `Application.notifiers` 集合属性访问。例如：

```javascript
var notRef = app.notifiers.add("OnClickButton", eventFile)
```

必须使用 `Application.notifiersEnabled` 属性启用通知器。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | `number` | 只读。`notifiers` 集合中的元素数量。 |
| parent | `Application` | 只读。`notifiers` 对象的容器。 |
| typename | `string` | 只读。引用的 `notifiers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| --- | --- | --- | --- |
| `add`<br>(`event`,<br>`eventFile`<br>`[, `eventClass`]) | `string`<br>`File`<br>`string` | `Notifier` | 创建一个通知器对象并将其添加到集合中。<br><br>`event` 定义事件的类 ID：使用一个 4 字符代码或唯一字符串。参阅附录 A：事件 ID 代码。<br><br>`eventFile` 定义事件发生时执行的脚本文件。<br><br>当一个事件适用于多种类型的对象时，使用 `eventClass`（一个 4 字符 ID 或唯一字符串）来区分此通知器适用于哪个对象。例如，Make 事件（`Mk `）适用于文档（`Dcmn`）、通道（`Chnl`）和其他对象。<br><br>**提示：** 使用 4 字符 ID 代码指定事件或事件类时，请在代码中省略单引号。 |
| `removeAll`<br>() | | | 从 `notifiers` 集合中移除所有成员对象。<br><br>您也可以通过从 Photoshop 偏设置文件夹中删除名为 `Script Events Manager.xml` 的文件，从脚本事件管理器下拉列表中移除一个 `notifier` 对象。 |

### PathItem

一个路径或绘图对象通过 `Document.pathItems` 属性中的集合访问。例如，这会选择一个命名的路径项目：

```javascript
var currentPathItem = app.activeDocument.pathItems.getByName("myPath");
currentPathItem.select()
```
```

```
通过向 `PathItems.add()` 方法传递一组 `SubPathInfo` 对象来创建这些对象。此方法为每个 `SubPathInfo` 对象创建一个 `SubPathItem` 对象，并为所有子路径表示的路径创建并返回一个新的 `PathItem` 对象。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `kind` | `PathKind` | 可读写。类型。 |
| `name` | `string` | 可读写。名称。 |
| `parent` | `Document` | 只读。包含的文档。 |
| `subPathItems` | `SubPathItems` | 只读。包含的子路径对象。 |
| `typename` | `string` | 只读。引用的 `pathItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `deselect()` | | | 取消选择此 `pathItem` 对象。 |
| `duplicate(name)` | `string` | | 用新名称复制此 `pathItem` 对象。 |
| `fillPath([fillColor] [, mode] [, opacity] [, preserveTransparency] [, feather] [, wholePath] [, antiAlias])` | `SolidColor`, `ColorBlendMode`, `number [0..100]`, `boolean`, `number [0.0..250.0]`, `boolean`, `boolean` | | 填充此路径包围的区域。不透明度是百分比。羽化值以像素为单位。如果 `wholePath` 为 `true`，则在填充时使用所有子路径（默认：`true`）。 |

```
app.activeDocument.close()
}

// 创建一个工作文档
var docRef = app.documents.add()

// 创建一个数组来保存图层集
var myLayerSets = new Array()

// 创建一个数组来保存文本
var textArray = Array("First", "Second", "Third")

// 创建一个索引变量
var i = 0

// 在顶层创建三个图层集
for (i = 0; i < 3; i++) {
    myLayerSets[i] = new Array()
    myLayerSets[i][0] = docRef.layerSets.add()
}

// 重新排列图层集，使第一个在最上面，第二个在其次，依此类推。
myLayerSets[1][0].moveAfter(myLayerSets[0][0])
myLayerSets[2][0].moveAfter(myLayerSets[1][0])

// 在每个图层集内创建一个图层集
for (i = 0; i < 3; i++) {
    myLayerSets[i][0].name = textArray[i] + " Set"
    myLayerSets[i][1] = myLayerSets[i][0].layerSets.add()
    myLayerSets[i][1].name = "Inside " + textArray[i] + " Set"
}

// 创建一个数组来保存图层
var myLayers = new Array()

// 在每个图层集内创建一个带有描述的文本图层
for (i = 0; i < 3; i++) {
    myLayers[i] = myLayerSets[i][1].artLayers.add()
    myLayers[i].kind = LayerKind.TEXT
    myLayers[i].textItem.contents = "Layer in " + textArray[i] + " Set Inside " + textArray[i] + " Set"
    myLayers[i].textItem.position = Array(app.activeDocument.width * i * 0.33,
                                          app.activeDocument.height * (i + 1) * 0.25)
    myLayers[i].textItem.size = 12
}
```

### PathItem

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `makeClippingPath(flatness)` | `number [0..100]` | | 将路径设置为当前文档的裁剪路径。`flatness` 参数告知路径如何近似曲线。 |
| `makeSelection(feather[, antiAlias[, operation])` | `number [0..250]`, `boolean`, `SelectionType` | 创建一个选区，其边界由此路径定义。`feather` 参数以像素为单位。 |
| `remove()` | | |此对象。 |
| `select()` | | | 将此 `PathItem` 对象设置为活动中的路径。 |
| `strokePath(tool[, pressure])` | `ToolType` | 使用指定工具对路径进行描边。 |

#### PathItem 示例

以下脚本包含三段的路径：两条角线构成一个 V 形，V 形上方有一条曲线，看起来像二维的。

```jsx
// 保存当前选项
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDialogs = app.preferences.displayDialogs

// 将 Photoshop CS 设置为像素并禁止对话框
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = Units.PIXELS
app.preferences.displayDialogs = DialogModes.NO

// 关闭所有打开的文档
while (app.documents.length) {
    app.activeDocument.close()
}

// 创建用于操作的新文档
var docRef = app.documents.add(5000, 7000, "Simple Line")
//线1是一条直线，所以每个锚点、左侧和右侧方向的坐标都相同
var lineArray = Array()
lineArray[0] = new PathPointInfo()
lineArray[0].kind = PointKind.CORNERPOINT
lineArray[0].anchor = Array(100, 100)
lineArray[0].leftDirection = lineArray[0].anchor
lineArray[0].rightDirection = lineArray[0].anchor
lineArray[1] = new PathPointInfo()
lineArray[1].kind = PointKind.CORNERPOINT
lineArray[1].anchor = Array(150, 200)
lineArray[1].leftDirection = lineArray[1].anchor
lineArray[1].rightDirection = lineArray[1].anchor
var lineSubPathArray = Array()
lineSubPathArray[0] = new SubPathInfo()
lineSubPathArray[0].operation = ShapeOperation.SHAPEXOR
lineSubPathArray[0].closed = false
lineSubPathArray[0].entireSubPath = lineArray
```

```
// 线2
var lineArray2 = Array()
lineArray2[0] = new PathPointInfo()
lineArray2[0].kind = PointKind.CORNERPOINT
lineArray2[0].anchor = Array(150, 200)
lineArray2[0].leftDirection = lineArray2[0].anchor
lineArray2[0].rightDirection = lineArray2[0].anchor
lineArray2[1] = new PathPointInfo()
lineArray2[1].kind = PointKind.CORNERPOINT
lineArray2[1].anchor = Array(200, 100)
lineArray2[1].leftDirection = lineArray2[1].anchor
lineArray2[1].rightDirection = lineArray2[1].anchor
lineSubPathArray[1] = new SubPathInfo()
lineSubPathArray[1].operation = ShapeOperation.SHAPEXOR
lineSubPathArray[1].closed = false
lineSubPathArray[1].entireSubPath = lineArray2
```

```
// 曲线
// 它是一条曲线，所以有三个点，而不是两个
// 中间点（lineArray3[1]）的坐标不同。
// 左侧方向点位于屏幕上锚点的“上方”。
// 右侧方向点位于锚点的“下方”。
// 你可以修改这些点的坐标，观察曲线是如何工作的...
var lineArray3 = Array()
lineArray3[0] = new PathPointInfo()
lineArray3[0].kind = PointKind.CORNERPOINT
lineArray3[0].anchor = Array(200, 100)
lineArray3[0].leftDirection = lineArray3[0].anchor
lineArray3[0].rightDirection = lineArray3[0].anchor
lineArray3[1] = new PathPointInfo()
lineArray3[1].kind = PointKind.CORNERPOINT
lineArray3[1].anchor = Array(150, 50)
lineArray3[1].leftDirection = Array(100, 50)
lineArray3[1].rightDirection = Array(200, 50)
lineArray3[2] = new PathPointInfo()
lineArray3[2].kind = PointKind.CORNERPOINT
lineArray3[2].anchor = Array(100, 100)
lineArray3[2].leftDirection = lineArray3[2].anchor
lineArray3[2].rightDirection = lineArray3[2].anchor
```

```
lineSubPathArray[2] = new SubPathInfo()
lineSubPathArray[2].operation = ShapeOperation.SHAPEXOR
lineSubPathArray[2].closed = false
lineSubPathArray[2].entireSubPath = lineArray3
// 创建路径项
var myPathItem = docRef.pathItems.add("A Line", lineSubPathArray)
// 描边路径以便可视化
myPathItem.strokePath(ToolType.BRUSH)
// 重置应用程序首选项
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.preferences.displayDialogs = startDialogs
```

### PathItems

文档中 `PathItem` 对象的集合。

通过 `Document.pathItems` 集合属性访问。例如，以下代码使用先前定义的子路径集合创建一个新的路径项：

```
app.activeDocument.pathItems.add("myPath", lineSubPathInfoArray);
```

```markdown
## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `length` | `数字` | 只读。`pathItems` 集合中 `PathItem` 对象的数量。 |
| `parent` | `Document` | 只读。`pathItems` 对象的容器对象。 |
| `typename` | `字符串` | 只读。所引用 `pathItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `add(name, entirePath)` | `字符串`<br>`SubPathInfo` 数组 | `PathItem` | 创建一个新的路径项对象并将其添加到此集合中。<br>为 `entirePath` 中提供的每个 `SubPathInfo` 对象创建一个新的 `SubPathItem` 对象，并将这些 `SubPathItem` 对象添加到返回的 `PathItem` 的 `subPathItems` 集合中。 |
| `getByName(name)` | `字符串` | `PathItem` | 获取 `pathItems` 集合中具有指定名称的第一个元素。 |
| `removeAll()` | | | 从 `pathItems` 集合中移除所有 `PathItem` 对象。 |

### PathPoint

表示路径段的锚点和控制手柄端点。每个点（锚点、左侧方向点和右侧方向点）都是一个包含 X 和 Y 位置坐标的数组。

- 使用 `PathPoint` 对象可以检索关于描述现有路径段的点的信息。这些属性是只读的。通过 `SubPathItem.pathPoints` 属性访问 `PathPoint` 对象。
- 使用 `PathPointInfo` 配合 `PathItems.add()` 来创建路径点。这些属性是可写的。

对于直线段（非曲线）路径，所有三个点的坐标相同。对于曲线段，坐标则不同。锚点与左侧或右侧方向点之间的差异决定了曲线的弧度。你使用左侧方向点将曲线向“外”弯曲或使其凸出；你使用右侧方向点将曲线向“内”弯曲或使其凹陷。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `anchor` | `数字数组` | 只读。曲线锚点的 X 和 Y 坐标。 |
| `kind` | `PointKind` | 只读。此点在包含的路径段中扮演的角色（角点或平滑点）。 |
| `leftDirection` | `数字数组` | 只读。左侧方向端点（“入”位置）的位置。 |
| `parent` | `SubPathItem` | 只读。包含的子路径对象。 |
| `rightDirection` | `数字数组` | 只读。右侧方向端点（“出”位置）的位置。 |
| `typename` | `字符串` | 只读。所引用 `PathPoint` 对象的类名。 |

### PathPointInfo

用于创建 [PathPoint](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/classreference/PathPoint.html)，表示路径段的锚点和控制手柄端点。每个点（锚点、左侧方向点和右侧方向点）都是一个包含 X 和 Y 位置坐标的数组。

- 使用 JavaScript 的 `new` 运算符创建这些对象，并在使用该对象通过 [PathItems.add()](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/classreference/PathItems.html#add) 创建路径项之前，将它们存储在 [SubPathInfo.entireSubPath](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/classreference/SubPathInfo.html#entireSubPath) 属性中。
- 参见下方的 [PathPointInfo 示例脚本](#PathPointInfo_sample_script)。
- 生成的 [SubPathItem](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/classreference/SubPathItem.html) 对象包含生成的 [PathPoint](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/classreference/PathPoint.html) 对象。使用 [PathPoint](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/classreference/PathPoint.html) 对象可以检索关于描述现有路径段的点的信息。这些属性是只读的。

对于直线段（非曲线）路径，所有三个点的坐标相同。对于曲线段，坐标则不同。锚点与左侧或右侧方向点之间的差异决定了曲线的弧度。你使用左侧方向点将曲线向“外”弯曲或使其凸出；你使用右侧方向点将曲线向“内”弯曲或使其凹陷。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `anchor` | 数字数组 | 读写。曲线锚点的 X 和 Y 坐标。 |
| `kind` | [PointKind](https://www.adobe.com/devnet-docs/photoshop/scriptingmaster/enumerationreference/PointKind.html) | 读写。此点在包含的路径段中扮演的角色（角点或平滑点）。 |
| `leftDirection` | 数字数组 | 读写。左侧方向端点（“入”位置）的位置。 |
| `rightDirection` | 数字数组 | 读写。右侧方向端点（“出”位置）的位置。 |
| `typename` | 字符串 | 只读。所引用 `PathPointInfo` 对象的类名。 |

##### PathPointInfo 示例脚本

```javascript
function drawLine(doc, start, stop) {
    var startPoint = new PathPointInfo();
    startPoint.anchor = start;
    startPoint.leftDirection = start;
    startPoint.rightDirection = start;
    startPoint.kind = PointKind.CORNERPOINT;

    var stopPoint = new PathPointInfo();
    stopPoint.anchor = stop;
    stopPoint.leftDirection = stop;
    stopPoint.rightDirection = stop;
    stopPoint.kind = PointKind.CORNERPOINT;
}
```

```javascript
var spi = new SubPathInfo();
spi.closed = false;
spi.operation = ShapeOperation.SHAPEXOR;
spi.entireSubPath = [startPoint, stopPoint];

var line = doc.pathItems.add("Line", [spi]);

line.strokePath(ToolType.PENCIL);

line.remove();
```

```javascript
drawLine(app.activeDocument, [100, 100], [200, 200]);
```
```


```markdown

### PathPoints

一个由 [PathPoint](https://example.com) 对象组成的集合，用于定义子路径，保存在 [SubPathItem.pathPoints](https://example.com) 属性中。

#### 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | number | 只读。集合中元素的数量。 |
| `parent` | `SubPathItem` | 只读。包含该路径点的子路径对象。 |
| `typename` | string | 只读。引用的 `PathPoints` 对象的类名。 |

### PDFOpenOptions

使用 [Application.open()](Application.open()) 方法在通用 Adobe PDF 格式中打开文档的选项。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `antiAlias` | boolean | 读写。True 表示使用抗锯齿。 |
| `bitsPerChannel` | `BitsPerChannelType` | 读写。每个通道的位数。 |
| `constrainProportions` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `cropPage` | `CropToType` | 读写。要使用的裁剪方法。 |
| `height` | `UnitValue` | 在 Adobe Photoshop CS6 中已弃用。 |
| `mode` | `OpenDocumentMode` | 读写。要使用的颜色模型。 |
| `name` | string | 读写。对象的名称。 |
| `page` | number | 读写。要打开的文档的页面或图像，具体取决于 [usePageNumber](usePageNumber) 的值。 |
| `resolution` | number | 读写。文档的分辨率（以每英寸像素数为单位）。 |
| `suppressWarnings` | boolean | 读写。True 表示在打开文档时抑制警告。 |
| `typename` | string | 只读。引用的 `PDFOpenOptions` 对象的类名。 |
| `usePageNumber` | boolean | 读写。当为 true 时[`page`](page) 属性指的是页码；当为 false 时，它指的是图像编号。 |
| `width` | `UnitValue` | 在 Adobe Photoshop CS6 中已弃用。 |

### PDFSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 Adobe PDF 格式的选项。

#### 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `alphaChannels` | boolean | 读写。True 表示将 Alpha 通道随文件一起保存。 |
| `annotations` | boolean | 读写。True 表示将批注随文件一起保存。 |
| `colorConversion` | boolean | 读写。True 表示将颜色配置文件转换为目标配置文件。 |
| `convertToEightBit` | boolean | 读写。True 表示将 16 位图像转换为 8 位，以提高与其他应用程序的兼容性。 |
| `description` | string | 读写。要使用的保存选项的说明。 |
| `destinationProfile` | string | 读写。最终 RGB 或 CMYK 输出设备的说明，例如显示器或印刷标准。 |
| `downgradeColorProfile` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `downSample` | `PDFResample` | 读写。要使用的向下采样方法。 |
| `downSampleSize` | number | 读写。如果图像超过每英寸像素数限制，则要向下采样的图像大小。 |
| `downSampleSizeLimit` | number | 读写。将向下采样或子采样限制为超过此每英寸像素数值的图像。 |
| `embedColorProfile` | boolean | 读写。True 表示将颜色配置文件嵌入文档中。 |
| `embedFonts` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `embedThumbnail` | boolean | 读写。True 表示在 Adobe PDF 文件中包含一个小预览图像。 |
| `encoding` | `PDFEncoding` | 读写。要使用的压缩类型（默认：`PDFEncoding.PDFZIP`）。 |
| `interpolation` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `jpegQuality` | number [0..12] | 读写。生成图像的质量，与压缩量成反比。仅当 `encoding = PDFEncoding.JPEG` 时有效。 |
| `layers` | boolean | 读写。True 表示保存文档的图层。 |
| `optimizeForWeb` | boolean | 读写。True 表示提高 PDF 文件在 Web 服务器上的性能。 |
| `outputCondition` | string | 读写。一个可选的注释字段，用于插入输出条件的描述。文本存储在 PDF/X 文件中。 |
| `outputConditionID` | string | 读写。输出条件的标识符。 |
| `PDFCompatibility` | `PDFCompatibility` | 读写。使文档兼容的 PDF 版本。 |
| `PDFStandard` | `PDFStandard` | 读写。使文档兼容的 PDF 标准。 |
| `preserveEditing` | boolean | 读写。True 表示在 Adobe Photoshop CS6 中重新打开 PDF 时，保留原生 Photoshop 数据完好无损。 |
| `presetFile` | string | 读写。用于设置的预设文件。注意：此选项会覆盖其他设置。 |
| `profileInclusionPolicy` | boolean | 读写。True 表示显示要包含哪些配置文件。 |
| `registryName` | string | 读写。输出条件注册的 URL。 |
| `spotColors` | boolean | 读写。True 表示保存专色。 |
| `tileSize` | number | 读写。压缩选项。仅当 `encoding = PDFEncoding.JPEG2000` 时有效。 |
| `transparency` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `typename` | string | 只读。引用的 `PDFSaveOptions` 对象的类名。 |
| `useOutlines` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `vectorData` | boolean | 在 Adobe Photoshop CS6 中已弃用。 |
| `view` | boolean | 读写。True 表示在 Adobe Acrobat 中打开保存的。 |

### PhotoCDOpenOptions

在 Adobe Photoshop CS6 中已弃用。Kodak PhotoCD 现在可以在 Adobe Photoshop CS6 安装的 Goodies 文件夹中找到。使用 [Application.open()](Application.open()) 方法在 Kodak Photo CD (PCD) 格式（包括 Photo CD 光盘的高分辨率文件）中打开。

#### 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `colorProfileName` | string | 读写。读取图像时使用的配置文件。 |
| `colorSpace` | `PhotoCDColorSpace` | 读写。颜色空间。 |
| `orientation` | `Orientation` | 读写。方向。 |
| `pixelSize` | `PhotoCDSize` | 读写。尺寸。 |
| `resolution` | number | 读写。分辨率（以每英寸像素数为）。 |
| `typename` | string | 只读。引用的 `PhotoCDOpenOptions` 对象的类名。 |

### PhotoshopSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet-docs/photoshop/scripting/saveAs) 方法将文档保存为 PSD 格式。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | boolean | 读写。True 表示保存通道。 |
| `annotations` | boolean | 读写。True 表示保存批注。 |
| `embedColorProfile` | boolean | 读写。True 表示将配置文件嵌入文档中。 |
| `layers` | boolean | 读写。True 表示保留图层。 |
| `spotColors` | boolean | 读写。True 表示保存专色。 |
| `typename` | string | 只读。引用的 `PhotoshopSaveOptions` 对象的类名。 |

### PICTFileOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 PICT 格式。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | boolean | 读写。True 表示保存通道。 |
| `compression` | `PICTCompression` | 读写。使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | boolean | 读写。True 表示将配置文件嵌入文档中。 |
| `resolution` | `PICTBitsPerPixel` | 读写。每像素位数。 |
| `typename` | string | 只读。引用的 `PICTFileOptions` 对象的类名。 |

### PICTResourceOptions

使用 `Document.saveAs()` 方法将文档保存为 PICT Resource 文件时的选项。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `alphaChannels` | boolean | 读写。为 true 时保存通道。 |
| `compression` | `PICTCompression` | 读写。使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | boolean | 读写。为 true 时在文档中嵌入配置文件。 |
| `name` | string | 读写。PICT 资源的名称。 |
| `resolution` | `PICTBitsPerPixel` | 读写。每像素位数。 |
| `resourceID` | number | 读写。PICT 资源的 ID（默认：128）。 |
| `typename` | string | 只读。引用的 `PICTResourceSaveOptions` 对象的类名。 |

### PicturePackageOptions

使用 `Application.makePicturePackage()` 创建的图片包的选项。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `content` | `PicturePackageTextType` | 读写。内容信息（默认：`PicturePackageTextType.NONE`）。 |
| `flatten` | boolean | 读写。为 true 时，最终文档中的所有层将被拼合（默认：`true`）。 |
| `font` | `GalleryFontType` | 读写。用于安全文本的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number | 读写。用于安全文本的字体大小（默认：`12`）。 |
| `layout` | string | 读写。用于生成图片包的版面（默认：`"(2) 5x7"`）。 |
| `mode` | `NewDocumentMode` | 读写。用作文档模式的颜色配置文件（默认：`NewDocumentMode.RGB`）。 |
| `opacity` | number | 读写。网页安全不透明度（百分比）（默认：`100`）。 |
| `resolution` | number | 读写。文档的分辨率（像素/英寸）（默认：`72.0`）。 |
| `text` | string | 读写。图片包自定义文本。仅当 `content = PicturePackageType.USER` 时有效。 |
| `textColor` | `RGBColor` | 读写。用于安全文本的颜色。 |
| `textPosition` | `GallerySecurityTextPositionType` | 读写。安全文本位置（默认：`GallerySecurityTextPositionType.CENTERED`）。 |
| `textRotate` | `GallerySecurityTextRotateType` | 读写。安全文本的方向（默认：`GallerySecurityTextRotateType.ZERO`）。 |
| `typename` | string | 只读。引用的 `PicturePackageOptions` 对象的类名。 |

### PixarSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet-docs/photoshop/scripting/saveAs) 方法将文档保存为 Pixar 格式的选项。

#### 属性

| 属性 | 值类型 |  |
|---|---|---|
| `alphaChannels` | boolean | 读写。为 true 时保存通道。 |
| `typename` | string | 只读。引用的 `PixarSaveOptions` 对象的类名。 |

### PNGSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 PNG 格式。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `compression` | number [0..9] | 读写。压缩值（默认：0）。 |
| `interlaced` | boolean | 读写。为 true 时交错行（默认：`false`）。 |
| `typename` | string | 只读。引用的 `PNGSaveOptions` 对象的类名。 |

### 偏好设置

表示 Photoshop 的应用程序首选项。通过 [Application.preferences](https://helpx.adobe.com/photoshop/using/preferences.html) 属性访问对象。例如：

```
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
```

在此对象中设置值等同于 Adobe Photoshop CS6 应用程序中选择**编辑 > 首选项**（在 Windows 上）或 **Photoshop > 首选项**（在 Mac OS 上）。有关各个设置的说明，请参阅 Adobe Photoshop CS6 帮助。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `additionalPluginFolder` | [File](https://helpx.adobe.com/photoshop/using/scripting-tools.html) | 读写。附加插件文件夹的路径。仅当 [useAdditionalPluginFolder](https://helpx.adobe.com/photoscript/using/scripting-tools.html) = true 时有效。 |
| `appendExtension` | [SaveBehavior](https://helpx.adobe.com/photoscript/using/scripting-tools.html) | 读写。在 Windows 上写入文件扩展名的首选策略。 |
| `askBeforeSavingLayeredTIFF` | boolean | 读写。为 true 时，当以 TIFF 格式保存文件时，会要求用户验证图层保留选项。 |
| `autoUpdateOpenDocuments` | boolean | 读写。为 true 时自动打开的文档。 |
| `beepWhenDone` | boolean | 读写。为 true 时，进程完成时会发出蜂鸣声。 |
| `colorChannelsInColor` | boolean | 读写。为 true 时，以彩色显示通道调板中的分量通道。 |
| `colorPicker` | [ColorPicker](https://helpx.adobe.com/photoscript/using/scripting-tools.html) | 读写。首选的颜色选择工具。 |

```


| `columnGutter` | 数字 [0.1..600.0] | 读写。栏间距的宽度（以点为单位）。 |
| `columnWidth` | 数字 [0.1..600.0] | 读写。栏宽（以点为单位）。 |
| `createFirstSnapshot` | 布尔值 | 读写。为 `true` 时，创建新文档时自动制作第一个快照。 |
| `dynamicColorSliders` | 布尔值 | 读写。为 `true` 时，颜色调板中会出现动态颜色滑块。 |
| `editLogItems` | [EditLogItemsType](https://helpx.adobe.com/photoscript/using/scripting-tools.html) | 读写。历史记录日志的首选详细程度。仅当 [`useHistoryLog`](https://helpx.adobe.com/photoscript/using/scripting-tools.html) = `true` 时有效。 |
| `exportClipboard` | `布尔值` | 读写。为 `true` 时，在退出应用程序后，剪贴板上会保留 Adobe Photoshop CS6 内容。 |
| `fontPreviewSize` | `FontPreviewType` | 读写。用于类型工具字体菜单中字体预览的首选字体大小。 |
| `fullSizePreview` | 布尔值 | 读写。为 `true` 时，将图像预览显示为全尺寸图像；为 `false` 时，显示缩略图（仅限 Mac OS）。 |
| `gamutWarningOpacity` | 数字 [0..100] | 读写。不透明度值（百分比）。 |
| `gridSize` | `GridSize` | 读写。网格中方块的首选大小。 |
| `gridStyle` | `GridLineStyle` | 读写。非打印网格线的首选格式化样式。 |
| `gridSubDivisions` | 数字 [1..100] | 读写。网格细分数量。 |
| `guideStyle` | `GuideLineStyle` | 读写。非打印参考线的首选格式化样式。 |
| `iconPreview` | 布尔值 | 读写。为 `true` 时使用图标预览（仅限 Mac OS）。 |
| `imageCacheLevels` | 数字 [1..8] | 读写。缓存中保留的图像数量。 |
| `imagePreviews` | `SaveBehavior` | 读写。在 Windows 上写入图像预览的首选策略。 |
| `interpolation` | `ResampleMethod` | 读写。在图像重新采样或调整大小时，用于为任何新像素分配颜色值的方法。 |
| `keyboardZoomResizesWindows` | 布尔值 | 读写。为 `true` 时，使用键盘快捷键放大或缩小时会自动调整窗口大小。 |
| `macOSThumbnail` | 布尔值 | 读写。为 `true` 时，保存图像时创建缩略图（仅限 Mac OS）。 |
| `maximizeCompatibility` | `QueryStateType` | 读写。打开 PSD 文件时，检查是否最大化兼容性的首选策略。 |
| `maxRAMUse` | 数字 [5..100] | 读写。Adobe Photoshop CS6 使用的最大可用 RAM 百分比（5 - 100）。 |
| `nonLinearHistory` | 布尔值 | 读写。为 `true` 时允许非线性历史。 |
| `numberOfHistoryStates` | 数字 | 读写。要保留的历史状态数。 |
| `otherCursors` | `OtherCursors` | 读写。某些工具的首选类型。 |
| `paintingCursors` | `PaintingCursors` | 读写。某些工具的首选类型。 |
| `parent` | `Application` | 读写。包含的。 |
| `pixelDoubling` | 布尔值 | 读写。为 `true` 时，将分辨率减半（像素大小）使预览更快。 |
| `pointSize` | `PointType` | 读写。点大小。 |
| `recentLength` | 数字 [0..30] | 读写。最近文件列表中的项目。 |
| `rulerUnits` | `Units` | 读写。脚本系统在接收返回值时使用的单位。 |
| `saveLogItems` | `SaveLogItemsType` | 读写。保存历史记录项目，日志数据。 |
| `saveLogItemsFile` | `File` | 读写。当首选位置是文件时，历史日志路径。 |
| `savePaletteLocations` | 布尔值 | 读写。为 `true` 时，新的调板位置。 |
| `showAsianTextOptions` | 布尔值 | 读写。为 `true` 时，在调板中显示亚洲文本。 |
| `showEnglishFontNames` | 布尔值 | 读写。为 `true` 时，列出字体名称。 |
| `showSliceNumber` | 布尔值 | 读写。为 `true` 时，使用切片工具在窗口中显示切片。 |
| `showToolTips` | 布尔值 | 读写。为 `true` 时，鼠标悬停显示定义。 |
| `smartQuotes` | 布尔值 | 读写。为 `true` 时使用引号；为 `false` 时使用直。 |
| `textFontSize` | `FontSize` | 读写。面板和对话框的字体。 |
| `typename` | 字符串 | 只读。引用的 `preferences` 对象的类名。 |
| `typeUnits` | [TypeUnits](https://helpx.adobe.com/photoshop/using/scripting-ref.html) | 读写。文本测量的首选单位。 |
| `useAdditionalFolder` | boolean | 读写。与其他应用程序一起存储的文件夹。 |
| `useHistoryLog` | boolean | 读写。为历史状态创建日志文件。 |
| `useLowerCaseExtension` | boolean | 读写。为 `true` 时使用小写扩展名。 |
| `useShiftKeyForToolSwitch` | boolean | 读写。为 `true` 时启用切换一组工具。 |
| `useVideoAlpha` | boolean | 读写。为 `true` 时向 Adobe Photoshop CS6 发送透明信息。（需要硬件支持）。 |
| `windowsThumbnail` | boolean | 读写。为 `true` 时在 Windows 中保存图像时创建缩略。（需要硬件支持）。 |

### PresentationOptions

使用 `Application.makePDFPresentation()` 创建的 Adobe PDF 演示稿的选项。

#### 属性
| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `autoAdvance` | `boolean` | 读写。为 `true` 时，在查看演示稿时自动切换图像（默认：`true`）。仅当 `presentation` = `true` 时有效。 |
| `includeFilename` | `boolean` | 读写。为 `true` 时包含图像文件名（默认：`false`）。 |
| `interval` | `number [1..60]` | 读写。自动切换视图之前的秒数（默认：`5`）。仅当 `autoAdvance` = `true` 时有效。 |
| `loop` | `boolean` | 读写。为 `true` 时在最后一页之后重新演示（默认：`false`）。仅当 `autoAdvance` = `true` 时有效。 |
| `magnification` | `MagnificationType` | 读写。查看图像时使用的放大类型。 |
| `PDFFileOptions` | `PDFSaveOptions` | 读写。创建 PDF 文件时的选项。 |
| `presentation` | `boolean` | 读写。为 `true` 时输出是演示文稿（默认：`false`）；当为 `false` 时，输出是多页文档。 |
| `transition` | `TransitionType` | 读写。从一张图像过渡到下一张图像的方法（默认：`TransitionType.NONE`）。仅当 `autoAdvance` = `true` 时有效。 |
| `typename` | `string` | 只读。引用的 `PresentationOptions` 对象的类名。 |

### RawFormatOpenOptions

使用 [Application.open](https://www.adobe.com/devnet/photoshop/scripting.html)() 方法打开 RAW 格式文档的选项。

#### 属性
| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `bitsPerChannel` | `number` | 读写。每个通道的位数。唯一有效的值是 `BitsPerChannelType.EIGHT` 或 `BitsPerChannelType.SIXTEEN`。 |
| `byteOrder` | `ByteOrder` | 读写。多字节顺序。当 `bitsPerChannel` = `BitsPerChannelType.SIXTEEN` 时有效。 |
| `channelNumber` | `number [1..5]` | 读写。图像中的通道数。该值不能超过图像中的通道数。当 `bitsPerChannel` = `BitsPerChannelType.SIXTEEN` 时有效，唯一的值是 1、3 或 4。 |
| `headerSize` | `number [0..19999]` | 读写。在实际信息开始之前的字节数；即文件开头的占位符。 |
| `height` | `number` | 读写。高度（以像素为单位）。 |
| `interleaveChannels` | `boolean` | 读写。顺序值。 |
| `retainHeader` | `boolean` | 读写。保存时保留头。仅当 `headerSize` 为 1 或更大时。 |
| `typename` | `string` | 只读。引用的 `RawFormatOpenOptions` 对象的类名。 |
| `width` | `number` | 读写。宽度（以像素为单位）。 |

### RawSaveOptions

使用 `Document.saveAs()` 方法以 RAW 格式保存文档。

#### 属性
| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | `boolean` | 读写。为 `true` 时保存 Alpha 通道。 |
| `spotColors` | `boolean` | 读写。为 `true` 时保存专色。 |
| `typename` | `string` | 只读。引用的 `RawSaveOptions` 对象的类名。 |

### RGBColor

定义 RGB 颜色，用于 `SolidColor` 对象。另参阅 `CMYKColor`、`GrayColor`、`HSBColor`、`LabColor`、`NoColor`。

#### 属性
| 属性 | 值类型 | 说明 |
| `blue` | `number [0..255]` | 读写。蓝色值（默认：255）。 |
| `green` | `number [0..255]` | 读写。绿色值（默认：255）。 |
| `hexValue` | `string` | 读写。颜色的十六进制表示。 |
| `red` | `number [0..255]` | 读写。红色值（默认：255）。 |
| `typename` | `string` | 只读。引用的 `RGBColor` 对象的类名。 |

### Selection

文档或图层的选定区域。通过 `Document.selection` 属性访问。例如：

```
app.activeDocument.selection.fill(app.foregroundColor)
```

许多属性和方法使用 `UnitValue` 类型，该类型将测量值与测量单位在一起。有关此的信息，请参阅 `JavaScript Tools Guide`。

#### 属性
| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `bounds` | array of UnitValue | 只读。整个选区的边界矩形。 |
| `parent` | `Document` | 只读。对象的容器。 |
| `solid` | `boolean` | 只读。`true` 表示边界矩形是实体。 |
| `typename` | `string` | 只读。引用的 `selection` 对象的类名。 |

#### 方法
| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `clear()` | | | 清除选区且将其复制到剪贴板。 |
| `contract(by)` | `UnitValue` | | 按指定量收缩（减少）选区。 |
| `copy([merge])` | `boolean` | | 将选区复制到剪贴板。使用可选参数并设置为 `true` 时，将执行合并复制（选区中的所有可见图层都被复制）。 |
| `cut()` | | | 清除当前选区并将其复制到剪贴板。 |
| `deselect()` | | | 取消当前选区。 |
| `expand(by)` | `UnitValue` | | 按指定量扩展选区。 |
| `feather(by)` | `UnitValue` | | 按指定量羽化选区边缘。 |
| `fill(type, mode, opacity, preserveTransparency)` | `SolidColor`<br>`ColorBlendMode`<br>`number [1..100]<br>`boolean` | | 填充选区。`opacity` 是一个百分比值。 |
| `grow(tolerance, antiAlias)` | `number`<br>`boolean` | | 扩展选区以包含所有在指定容差范围内的相邻像素。 |
| `invert()` | | | 反转选区（取消选择选区并选择图层或文档的其余部分）。**提示：** 要翻转选区形状，请参阅 `rotate`。 |
| `load(from, combination, inverting)` | `Channel`<br>`SelectionType`<br>`boolean` | | 从指定通道加载选区。 |
| `makeWorkPath([tolerance])` | `number` | | 使此选区项目成为此文档的工作路径。 |
| `resize([horizontal, vertical, anchor])` | `number`<br>`number`<br>`AnchorPosition` | | 将选定区域调整为指定的尺寸和锚点位置。 |
| `resizeBoundary([horizontal, vertical, anchor])` | `number`<br>`number`<br>`AnchorPosition` | | 围绕指定锚点更改选区的大小到指定的尺寸。 |
| `rotate(angle, anchor)` | `number`<br>`AnchorPosition` | | 围绕指定的锚点按指定角度旋转选区。 |
| `rotateBoundary(angle, anchor)` | `number`<br>`AnchorPosition` | | 围绕指定锚点旋转选区边界。 |
| `select(region, type, feather, antiAlias)` | array of number<br>`SelectionType`<br>`number`<br>`boolean` | | 选择指定的区域。`region` 参数是一个包含四个坐标的数组，`[left, top, right, bottom]`。 |
| `selectAll()` | | | 选择整个图层。 |


```markdown
| `selectBorder` (width) | `UnitValue` | | 仅选择指定宽度的选区边界；后续操作不会影响边界内的选区区域。 |
| `similar` (tolerance, antiAlias) | `number boolean` | | 扩展选区以包含整个图像中落在容差范围内的像素。 |
| `smooth` (radius) | `number` | | 清理基于颜色的选区内部或外部遗留的杂散像素（在指定的像素半径范围内）。 |
| `store` (into [, combination]) | `Channel SelectionType` | | 将选区保存为通道。 |
| `stroke` (strokeColor, width [, location] [, mode] [, opacity] [, preserveTransparency]) | `SolidColor number StrokeLocation ColorBlendMode number [1..100] boolean` | | 描边选区边界。`opacity` 是百分比值。 |
| `translate` ([deltaX] [, deltaY]) | `UnitValue UnitValue` | | 将整个选区相对于其当前位置移动。 |
| `translateBoundary` ([deltaX] [, deltaY]) | `UnitValue UnitValue` | | 将选区边界相对于其当前位置移动。 |

## 选区示例脚本

以下脚本通过以下步骤创建棋盘格：

- 创建一个 800 x 800 像素的文档。
- 将整个文档划分为 100 x 100 像素的方格。
- 选择第一行中的每隔一个方格，然后调整选择标准以选择下一行中的交替方格。重复此过程，直到选中文档中每隔一个方格。
- 用调色板中的前景色填充选中的方格。
- 反转选区，并用调色板中的背景色填充新选中的方格。
- 取消选择方格以移除选区轮廓（即“蚂蚁线”）。

```javascript
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CS6 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.preferences.displayDialogs = DialogModes.NO

//Close all the open documents
while (app.documents.length) {
    app.activeDocument.close()
}

//Create variables for the 800 pixel board divided in even 100 x 100 squares
var docSize = 800
var cells = 8
var cellSize = docSize / cells

// create a new document
var checkersDoc = app.documents.add(docSize, docSize, 72, "Checkers")

// Create a variable to use for selecting the checker board
// That allows me to shift the selection one square to the right
//on every other row, and then shift back for the rows in between.
var shiftIt = true

// loop through vertically to create the first row
for (var v = 0; v < docSize; v += cellSize) {

    // Switch the shift for a new row
    shiftIt = !shiftIt

    // loop through horizontally
    for (var h = 0; h < docSize; h += (cellSize * 2)) {

        // push over the cellSize to start with only
        if (shiftIt && h == 0) {
            h += cellSize
        }

        // Select a square
        selRegion = Array(Array(h, v),
                            Array(h + cellSize, v),
                            Array(h + cellSize, v + cellSize),
                            Array(h, v + cellSize),
                            Array(h, v))

        // In the first iteration of the loop, start the selection
        //In subsequent iterations, use the EXTEND constant value
        //of the select() method to add to the selection (in the loop’s else clause)
        if (h == 0 && v == 0) {
            checkersDoc.selection.select(selRegion)
        } else {
            checkersDoc.selection.select(selRegion, SelectionType.EXTEND)
        }
    }

        // turn this off for faster execution
        // turn this on for debugging
        WaitForRedraw()
    }
}

// Fill the current selection with the foreground color
checkersDoc.selection.fill(app.foregroundColor)

//Invert the selection
checkersDoc.selection.invert()

// Fill the new selection with the background color
checkersDoc.selection.fill(app.backgroundColor)

// Clear the selection to get rid of the non-printing borders
checkersDoc.selection.deselect()

// Reset the application preferences
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.preferences.displayDialogs = startDisplayDialogs

// A helper function for debugging
// It also helps the user see what is going on
// if you turn it off for this example you
// get a flashing cursor for a number time
function WaitForRedraw()
{
    var eventWait = charIDToTypeID("Wait")
    var enumRedrawComplete = charIDToTypeID("RdCm")
    var typeState = charIDToTypeID("Stte")
    var keyState = charIDToTypeID("Stte")

    var desc = new ActionDescriptor()

    desc.putEnumerated(keyState, typeState, enumRedrawComplete)

    executeAction(eventWait, desc, DialogModes.NO)
}
```

## SGIRGBSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 SGIRGB 格式的选项。

**注意：** SGIRGB 格式不会随 Adobe Photoshop CS6 自动安装。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alphaChannels | `boolean` | 读写。为 `true` 表示保存 Alpha 通道。 |
| spotColors | `boolean` | 读写。为 `true` 表示保存专色。 |
| typename | `string` | 只读。引用的 `SGIRGBSaveOptions` 对象的类名。 |

### SolidColor

文档中使用的颜色定义。将一种颜色映射到所有可用颜色模型中的等效值。

- 用于 `Application.backgroundColor` 和 `foregroundColor` 属性，`Channel.color`，`ColorSampler.color` 以及 `TextItem.color`。
- 传递给 `PathItem.fillPath()`、`Selection.fill()` 和 `Selection.stroke()`。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `cmyk` | `CMYKColor` | 读写。CMYK 颜色模式。 |
| `gray` | `GrayColor` | 读写。灰度颜色。 |
| `typename` | `string` | 只读。引用的 `SGGGaveaveave


| parent | [Application](javascript:void(0)) | 只读。包含的应用程序。 |
| typename | `string` | 只读。所引用的 `TextFonts` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `getByName(name)` | `string` | [TextFont](javascript:void(0)) | 获取 `TextFonts` 集合中具有所提供名称的第一个元素。 |

### TextItem

`ArtLayer` 对象中 `kind` 属性为 `LayerKind.TEXT` 的文本。可通过 `ArtLayer.textItem` 属性访问此对象。例如：

```
myLayers[i].textItem.contents = "Layer in " + textArray[i] + " Set Inside "
```

许多属性使用 `UnitValue` 类型，该类型将测量值与测量单位组合在一起。有关此类型的信息，请参阅 *JavaScript Tools Guide*。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `alternateLigatures` | `boolean` | 可读写。True 表示使用替代连字。注意：替代连字与可选连字相同。有关更多信息，请参阅 Adobe Photoshop CS6 帮助。 |
| `antiAliasMethod` | `AntiAlias` | 可读写。要使用的抗锯齿方法。 |
| `autoKerning` | `AutoKernType` | 可读写。要使用的自动字距调整选项。 |
| `autoLeadingAmount` | `number [0.01..5000.00]` | 可读写。自动（默认）行距的百分比（以点为单位）。仅当 `useAutoLeading = true` 时有效。 |
| `baselineShift` | `UnitValue` | 可读写。文本基线偏移量使用的单位值。 |
| `capitalization` | `TextCase` | 可读写。文本大小写。 |
| `color` | `SolidColor` | 可读写。文本颜色。 |
| `contents` | `string` | 可读写。图层中的实际文本。 |
| `desiredGlyphScaling` | `number [50..200]` | 可读写。缩放文本字符水平大小的所需量。百分比值；100 时，字符宽度不缩放。仅当 `justification = Justification.CENTERJUSTIFIED`、FULLYJUSTIFIED`、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `minimumGlyphScaling` 和 `maximumGlyphScaling` 值。 |
| `desiredLetterScaling` | `number [100..500]` | 可读写。字母之间的间距量（0 时，字母之间不添加间距）。<br><br>等同于“段落”调板菜单上选择“对齐”时弹出的“对齐”对话框中的字距。<br><br>仅当 [`justification`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/Justification.html) = `Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 [`minimumLetterScaling`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/minimumLetterScaling.html) 和 [`maximumLetterScaling`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/maximumLetterScaling.html) 值。 |
| `desiredWordScaling` | `number [0..1000]` | 可读写。单词之间的间距量（百分比）（100 时，单词之间不添加额外间距）。<br><br>等同于“段落”调板菜单上选择“对齐”时弹出的“对齐”对话框中的单词间距。<br><br>仅当 [`justification`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/Justification.html) = `Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 [`minimumWordScaling`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/minimumWordScaling.html) 和 [`maximumWordScaling`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/maximumWordScaling.html) 值。 |
| `direction` | [`Direction`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/enums/Direction.html) | 可读写。文本方向。 |
| `fauxBold` | `boolean` | 可读写。True 表示使用仿粗体（默认值：`false`）。<br><br>将此项设置为 true 相当于选择文本并在“字符”调板中单击“仿粗体”。 |
| `fauxItalic` | `boolean` | 可读写。True 表示使用仿斜体（默认值：`false`）。<br><br>将此项设置为 true 相当于选择文本并在“字符”调板中单击“仿斜体”。 |
| `firstLineIndent` | [`UnitValue`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/UnitValue.html) [-1296..1296] points | 可读写。段落首行缩进的量（单位值）。 |
| `font` | `string` | 可读写。字符的文本字体。使用字体的 PostScript 名称。请参阅 [`TextFont`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/classes/TextFont.html) 并使用 `postScriptName` 属性。 |
| `hangingPunctuation` | `boolean` | 可读写。True 表示使用罗马挂标点。 |
| `height` | [`UnitValue`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/classes/UnitValue.html) | 可读写。段落文本框（单位值）。<br><br>仅当 `kind = TextType.PARAGHTEXT` 时。 |
| `horizontalScale` | `number [0..1000]` | 可读写。字符的（水平）缩放，相对于 `verticalScale`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/verticalScale.html)（百分比值）。 |
| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `hyphenateAfter` | `number [1..15]` | 可读写。允许自动换行时连字符字的起始字母。 |
| `hyphenateBefore` | `number [1..15]` | 可读写。允许自动换行时连字符字的末尾字母。 |
| `hyphenateCapitalWords` | `boolean` | 可读写。设置为 `true` 以允许首字母大写的单词自动换行连字符。 |
| `hyphenateWordsLongerThan` | `number [2..25]` | 可读写。单词允许自动换行连字符所需的最小字母数。 |
| `hyphenation` | `boolean` | 可读写。设置为 `true` 以自动换行时连字符。 |
| `hyphenationZone` | `UnitValue [0..720] pica` | 可读写。行末用于触发单词非两端对齐中断开的距离。 |
| `hyphenLimit` | `number` | 可读写。以字符断字结尾的连续行的数量。 |
| `justification` | [Justification](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/Justification.html) | 可读写。段落对齐方式。 |
| `kind` | [TextType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/classes/TextType.html) | 可读写。文本换行类型。 |
| `language` | [Language](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/enums/Language.html) | 可读写。使用的语言。 |
| `leading` | [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/UnitValue.html) | 可读写。行距值。 |
| `leftIndent` | `UnitValue [-1296..1296] points` | 可读写。文本从左缩进的距离。 |
| `ligatures` | `boolean` | 可读写。设置为 `true` 以使用连字。 |
| `maximumGlyphScaling` | `number [50..200]` | 可读写。允许的文本字符水平尺寸的最大缩量（百分比值；100 表示不缩放宽度）。<br><br>仅当 `justification = Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `minimumGlyphScaling` 和 `desiredGlyphScaling` 值。 |
| `maximumLetterScaling` | `number [100..500]` | 可读写。允许的字符间最大间距量（百分比值；0 表示不增加间距）。<br><br>等效于“段落”面板（选择“对齐”）中的“字符间距调整”对话框中的设置。<br><br>仅当 `justification = Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `minimumLetterScaling` 和 `desiredLetterScaling` 值。 |
| `maximumWordScaling` | `number [0..1000]` | 可读写。允许的单词间最大间距量（百分比值；100 表示不增加间距）。<br><br>等效于“段落”面板（选择“对齐”）中的“词间距”对话框中的设置。<br><br>仅当 `justification = Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `minimumWordScaling` 和 `desiredWordScaling` 值。 |
| `minimumGlyphScaling` | `number [50..200]` | 可读写。允许的文本字符水平尺寸的最小缩放量（百分比值；100 表示不缩放宽度）。<br><br>仅当 `justification = Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `maximumGlyphScaling` 和 `desiredGlyphScaling` 值。 |
| `minimumLetterScaling` | `number [100..500]` | 可读写。允许的字符间最小间距量（百分比值；0 表示不减少间距）。<br><br>等效于“段落”面板（选择“对齐”）中的“字符间距”对话框中的设置。<br><br>仅当 `justification = Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `maximumLetterScaling` 和 `desiredLetterScaling` 值。 |
| `minimumWordScaling` | `number [0..1000]` | 可读写。允许的单词间最小间距量（百分比值；0 表示不减少间距）。<br><br>等效于“段落”面板（选择“对齐”）中的“词间距”对话框中的设置。<br><br>仅当 `justification = Justification.CENTERJUSTIFIED`、`FULLYJUSTIFIED`、`LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `maximumWordScaling` 和 `desiredWordScaling` 值。 |
| `noBreak` | `boolean` | 可读写。设置为 `true` 以禁止此文本中的换行。<br><br>**提示：** 当多个连续字符设置为 `true` 时，可能会阻止自动换行，导致部分文本无法在屏幕上显示。 |
| `oldStyle` | `boolean` | 可读写。设置为 `true` 以旧式字体样式。 |
| `parent` | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/classes/ArtLayer.html) | 可读写。包含此文本的图层。 |
| `position` | `array of` [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/UnitValue.html) | 可读写。文本原点的位置。数组成员指定 X 和 Y 坐标。<br><br>等效于使用文本工具在文档中单击一点来创建文本的原点。 |
| `rightIndent` | `UnitValue [-1296..1296] points` | 可读写。文本从右缩进的距离。 |
| `size` | [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/UnitValue.html) | 可读写。以 `UnitValue` 为单位的字体大小。注意：CS3 及更早版本中类型为 `points`。 |
| `spaceAfter` | `UnitValue [-1296..1296] points` | 可读写。每个段落后的间距。 |



| `spaceBefore` | `UnitValue [-1296..1296] points` | 可读写。每个段落前的间距。 |
| `strikeThru` | `StrikeThruType` | 可读写。要使用的文本删除线选项。 |
| `textComposer` | `TextComposer` | 可读写。用于评估换行并优化指定的连字符断字和对齐选项的排版方法。<br><br>仅在 `kind` = `TextType.PARAGRAPHTEXT` 时有效。 |
| `tracking` | `number [-1000..10000]` | 可读写。多个字符之间的统一间距量。<br><br>字距调整单位为 1/1000 个全角空格。全角空格的宽度相对于当前字体大小。在 1 点字体中，1 全角等于 1 点；在 10 点字体中，1 全角等于 10 点。例如，在 10 点字体中，100 个单位相当于 1 点。 |
| `typename` | `string` | 只读。引用的 `textItem` 对象的类名。 |
| `underline` | `UnderlineType` | 可读写。文本下划线选项。 |
| `useAutoLeading` | `boolean` | 可读写。设置为 `true` 以使用字体内置的行距信息。 |
| `verticalScale` | `number [0–1000]` | 可读写。与 `horizontalScale` 成比例的垂直字符缩放量（百分比值）。 |
| `warpBend` | `number [-100..100]` | 可读写。扭曲弯曲的百分比。 |
| `warpDirection` | `Direction` | 可读写。扭曲方向。 |
| `warpHorizontalDistortion` | `number [-100..100]` | 可读写。扭曲的水平变形量（百分比值）。 |
| `warpStyle` | `WarpStyle` | 可读写。要使用的扭曲样式。 |
| `warpVerticalDistortion` | `number [-100..100]` | 可读写。扭曲的垂直变形量（百分比值）。 |
| `width` | `UnitValue` | 可读写。段落文本定界框的宽度。<br><br>仅在 `kind` = `TextType.PARAGRAPHTEXT` 时有效。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
|---|---|---|---|
| `convertToShape()` | | | | 将文本图层及其包含的图层转换为形状图层，其中的文本内容会被转换为剪贴路径。 |
| `createPath()` | | | | 根据实际文本内容（如字母或单词）的轮廓创建剪贴路径。 |

### TiffSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 TIFF 格式时的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `alphaChannels` | boolean | 可读写。为 `true` 时保存 Alpha 通道。 |
| `annotations` | boolean | 可读写。为 `true` 时保存注释。 |
| `byteOrder` | `ByteOrder` | 可读写。读取文档多字节值的顺序（默认值：在 Mac OS 中为 `ByteOrder.MACOS`，在 Windows 中为 `ByteOrder.IBM`）。 |
| `embedColorProfile` | boolean | 可读写。为 `true` 时将颜色配置文件嵌入到文档中。 |
| `imageCompression` | `TIFFEncoding` | 可读写。压缩类型（默认值：`TIFFEncoding.NONE`）。 |
| `interleaveChannels` | boolean | 可读写。为 `true` 时，图像中的通道将交错存储。 |
| `jpegQuality` | number [0..12] | 可读写。生成图像的质量，与 JPEG 压缩量成反比。<br><br>仅在 `imageCompression` = `TIFFEncoding.JPEG` 时有效。 |
| `layerCompression` | `LayerCompression` | 可读写。保存图层时使用的压缩方法（相对于保存合成数据）。<br><br>仅在 `layers` = `true` 时有效。 |
| `layers` | boolean | 可读写。为 `true` 时保存图层。 |
| `saveImagePyramid` | boolean | 可读写。为 `true` 时保留多分辨率信息（默认值：`false`）。 |
| `spotColors` | boolean | 可读写。为 `true` 时保存专色。 |
| `transparency` | boolean | 可读写。为 `true` 时，将透明度作为附加的 Alpha 通道保存，以便在其他应用程序中打开文件时保留透明度。 |
| `typename` | string | 只读。引用的 `TiffSaveOptions` 对象的类名。 |

### UnitValue

ExtendScript 定义了 JavaScript 类 `UnitValue`，用于表示带有测量单位的测量值；详情请参见第 32 页的 'Adobe Photoshop CS6 中的 JavaScript支持'。关于这些类的详细参考信息，请参阅 JavaScript 工具指南。

### xmpMetadata

Camera RAW 图像的 XMP 元数据。

对于 Camera RAW 图像文件，XMP 元数据存储在一个 sidecar 文件中，该文件与 RAW 文件位于同一文件夹，具有相同的基本名称，扩展名为 `.xmp`。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `parent` | `Document` | 只读。包含此。 |
| `rawData` | `string` | 可读写。包含 XML (RDF) 格式的字符串。有关格式的详细信息，请参阅规范。 |
| `typename` | `string` | 只读。引用的 `xmpMetadata` 对象的类名。 |

### JavaScript 资源

本节描述了 JavaScript 资源，使得脚本能够像插件一样运行。包括：

- 能够指定脚本在菜单中出现
- 一个术资源，使脚本能够动作管理器配合
- 一个类别，用于菜单中进行排序
- 一个启用字符串，用于指示给定条件下是启用
- 字符串必须符合有效的 XML 语法

#### JavaScript 资源语法

| 标签 | 描述 |
| :--- | :--- |
| `<javascriptresource>` | 资源定义。 |
| `<name>` | 出现在菜单中的名称。如果资源未提供标签，命令名称默认为脚本。 |
| `<menu>` | 命令出现的菜单。如果未提供标签，命令出现在文件 > 脚本菜单。注意：`<menu>` 支持的值只有 `automate`、`filter` 和 `help`。例如，`automate` 会脚本放在文件 > 自动菜单中。 |
| `<about>` | 出现在对话框中的字符串，用户从关于工具菜单查看。 |
| `<enableinfo>` | 一个布尔表达式，指示菜单中的命令是否启用。见启用语法。注意：如果提供了标签，菜单项仅至少打开一个文档且布尔值为 true 时启用。如果你希望菜单项始终启用，不要使用标签。 |
| `<eventid>` | 一个标识唯一字符串。使用 UUID 确保脚本与其他脚本共享。 |
| `<category>` | 命令在菜单中所属的类别。用于菜单中进行分组。命令根据 `<category>` 中的字符串按字母顺序放置在菜单中。两个命令使用相同的类别，它们将被在一起。 |
| `<terminology>` | 脚本与动作管理器配合所需的术语词典。 |

#### 基本 JavaScript 资源示例

此示例展示了一个非常基础的 `<javascriptresource>`。通过此资源，用户可以通过自动菜单中的添加命令执行脚本。只要至少打开一个文档，此命令在菜单中就是启用的。用户从关于工具菜单请求脚本的信息，`<about>` 标签中包含的字符串将显示在对话框中。

```
/*
    <javascriptresource>
    <name>Add a Document</name>
    <type>automate</type>
    <about>A short string providing information about the script.</about>
    <enableinfo>true</enableinfo>
</javascriptresource>
*/

app.documents.add();
```

#### 启用语法

`<enableinfo>` 标签提供了一个布尔表达式，当该表达式求值时，指示菜单中的命令是否启用。你可以使用此表达式根据文档的各种特征来启用或禁用菜单项。启用语法如下：

```
<booleanExpression> ::= <conjunction> { "||" <conjunction> }

<conjunction> ::=     <relation> {"&&" <relation> }

<relation> ::=        <equality> {<relationOperator><equality>}

<equality> ::=        <simpleExpression> {<equalityOperator><simpleExpression>}

<simpleExpression> ::= <term> {<addOperator><term>}

<term> ::=            <factor> {<mulOperator><factor>}

<factor> ::=          <integer> | <intrinsic> | <ident> |
                      "(" <booleanExpression> ")" | "(" simpleExpression ")" |
                      "+" <factor> | "-" <factor> | "!" <factor>

<integer> ::=         digit {digit}

<intrinsic> ::=       <limitFunction> | <dimFunction> | <inFunction>

<limitFunction> ::=   ( "min" | "max") "(" <simpleExpression> ","
                      <simpleExpression> { "," <simpleExpression> } ")"

<dimFunction> ::=     "dim" "(" <simpleExpression> "," <simpleExpression> ")"
```

```
<ident> :=              (alpha | "_") {alpha | digit | "_" }
<mulOperator> :=        "*" | "/"
<addOperator> :=        "+" | "-"
<equalityOperator> :=   "==" | "!="
<relationOperator> :=   "<" | "<=" | ">=" | ">"
<inFunction> :=         "in" "(" <simpleExpression> {"," <simpleExpression> } ")"
```

运算符优先级如下表所示。运算符列表中，优先级最高的位于表格顶部。

| 运算符 | 描述 |
|---|---|
| || | 或 |
| && | 与 |
| + - | 加法或减法 |
| * / | 乘法或除法 |

| 运算符 | 描述 |
|---|---|
| < <= | 小于等于 |



请参阅 `Conditional Mode Change.jsx` 以了解一个能够录制脚本参数并可基于其进行自动化的脚本示例。此文件可在 `Presets/Scripts` 文件夹中找到。

## 术语词典

JavaScript 资源提供了一个 `<terminology>` 标签，允许您为脚本提供术语词典。创建术语词典的第一步是查看您的脚本用户界面，并为用户界面中的每个元素创建人类可读的字符串。

例如，在条件模式更改命令中，用户界面请求源模式和目标模式。源模式和目标模式都有几个选项。用户界面的所有这些元素都需要在术语词典中有对应的条目。

术语词典采用 PDF 字典格式创建，包含以下条目，并且在 `<javascriptresource>` 中必须具有以下格式：

```
<terminology><![CDATA[<<<
    /Version integer
    /Events <<event dictionary>>
    /Classes <<class dictionary>>
    /Enumerations <<enumeration dictionary>>
>>> ]]></terminology>
```

> **注意：** 术语标签中的信息需要包装在 CDATA 块中，以便 XML 解析器忽略术语中出现的“/”和其他标签。

事件、类和枚举字典的定义如下。

`/Events` 字典包含每个事件的一个条目：

```
/eventName [
    (String event name)              // 字符串 API 中使用的名称
    /direct parameter type            // 必需
        <<                            // 可选；如果省略，则无参数
            /parameterName [           // 可选参数字典
                (String name)          // 字符串 API 中使用的名称
                /parameter type        // 必需
            ]                         // 必需
            ...                       // 其他参数
        >>
    ]
]
```

`/Classes` 字典包含每个类的一个条目：

```
/className [
    (ZString class name)              // 字符串 API 中使用的名称
        <<                            // 必需
            /propertyName [           // 属性字典
                (String name)          // 字符串 API 中使用的名称
                /property type        // 必需
            ]                         // 必需
            ...                       // 其他属性
        >>
    ]
]
```

`/Enumerations` 字典包含每个枚举类型的一个条目：

```
/enumTypeName                     // 字符串 API 中使用的名称
    <<
        /enumValue (String name)    // 必需
        ...
    >>
]
```

### 值类型定义

对于 `/parameter type` 和 `/property type` 的定义，您可以使用在自己的术语词典中声明的类和枚举类型，可以使用 Photoshop 提供的声明，也可以使用基本值类型。

### 基本值类型

基本值类型如下表所示：

| 名称 | 代码 | 描述 |
|---|---|---|
| `typeInteger` | 'long' | int32 |
| `typeFloat` | 'doub' | IEEE 64 位双精度浮点数 |
| `typeBoolean` | 'bool' | 真或假。 |
| `typeText` | 'TEXT' | 任意数量可读字符的块。 |
| `typeAlias` | 'alis' | Macintosh 文件系统路径。 |
| `typePaths` | 'Pth ' | Windows 文件系统路径。 |
| `typePlatformFilePath` | 'alis' 或 'Pth' | 在 Mac OS 上为 `typeAlias`，在 Windows 上为 `typePath`。 |

### 预定义类类型

Photoshop 提供了许多预定义的类，可在术语词典中使用。下表显示了其中一部分有用的类。当适用时使用这些类，但如有必要，您可以在术语资源中定义新的类。

| 名称 | 代码 | 描述 |
|---|---|---|
| `classColor` | 'Clr ' | 颜色类的类。 |
| `classRGBColor` | 'RGBC' | keyRed, keyGreen, keyBlue |
| `classCMYKColor` | 'CMYC' | keyCyan, keyMagenta, keyYellow, keyBlack。 |
| `classUnspecifiedColor` | 'UnsC' | 未指定。 |
| `classGrayscale` | 'Grsc' | keyGray |
| `classBookColor` | 'BkCl ' | 专色色板颜色 |
| `classLabColor` | 'LbCl' | keyLuminance, keyA, keyB。 |

### 术语条目的唯一性规则

通常，术语条目的名称在特定类别和作用域内必须是唯一的。最好不要不必要地使名称唯一；通用术语更可取，如果某个事物已有名称，请直接使用。在考虑术语条目的唯一性时，大小写很重要。

术语条目的唯一性规则是：

- 所有事件名称必须彼此不同。
- 所有类名称必须与所有其他名称不同。
- 所有枚举类型名称必须彼此不同。
- 所有键必须与同一类或事件中使用的所有其他键不同。
- 所有枚举值必须与同一枚举类型中的所有枚举值不同。
- 一个类、事件、枚举类型、键和枚举值可以具有相同的名称。

### 术语定义示例

此示例演示了一个新事件的术语定义；示例使用了 `ZString`。该事件名为 `newAnnot`，接受三个参数：

- `annotType`，一个枚举（`annotType`）
- `at`，一个类（`point`），以及
- `size`，一个类（`annotSizeClass`）。

#### 脚本常量

本节列出并描述了为与 Adobe Photoshop CS6 JavaScript 属性和方法配合使用而定义的枚举。

| 常量类型 | 值 | 含义 |
|---|---|---|
| `AdjustmentReference` | `ABSOLUTE`, `RELATIVE` | 用于解释可选颜色调整规范的方法：`ABSOLUTE` = 占整体比例。`RELATIVE` = 现有颜色比例。传递给 `ArtLayer.selectiveColor()`。 |
| `AnchorPosition` | `BOTTOMCENTER`, `BOTTOMLEFT`, `BOTTOMRIGHT`, `MIDDLECENTER`, `MIDDLERIGHT`, `TOPCENTER`, `TOPRIGHT` | 变换对象时使用 `ArtLayer`、`LayerSet` 和 `Selection` 中的 `Document.resizeCanvas()` 整个画布，此移动。 |
| `AntiAlias` | `CRISP`, `NONE`, `SHARP`, `STRONG` | 通过柔化边缘与背景之间的颜色过渡来平滑边缘。`TextItem.antiAliasMethod()`。 |
| `AutoKern` | `MANUAL`, `METRICS`, `OPTICAL` | 字符使用的字距。`TextItem.autoKern()`。 |
| `BatchDestination` | `FOLDER`, `NODESTINATION`, `SAVEANDCLOSE` | 批处理文件的目标（如果有），在 `Application.batch()` 方法使用的 `BatchOptions` 中：`FOLDER`：将修改后的文件保存到新位置（保留原始）。`NODESTINATION`：保持所有文件。`SAVEANDCLOSE`：保存并关闭。 |
| `BitmapConversionType` | `CUSTOM`, `DIFFUSIONDITHER`, `HALFTHRESHOLD`, `HALFTONESCREEN`, `PATTERN` | 指定正在转换为位图模式的图像的质量。用于 `BitmapConversionOptions`。 |
| `BitmapHalfTone` | `CROSS`, `DIAMOND`, `ELLIPSE`, `LINE`, `ROUND`, `SQUARE` | 指定半调网中点（墨点）的形状。用于 `BitmapConversionOptions`。 |
| `BitsPerChannelType` | `EIGHT`, `ONE`, `SIXTEEN`, `THIRTYTWO` | 每个通道的位数。`Document.bitsPerChannel` 的值；传递给 `Documents.add()`。也用于 `PDFOpenOptions` 和 `CameraRAWOpenOptions`。 |
| `BlendMode` | `COLORBLEND`, `COLORBURN`, `COLORDODGE`, `DARKEN`, `DIFFERENCE`, `DISSOLVE`, `DIVIDE`, `EXCLUSION`, `HARDLIGHT`, `HARDMIX`, `HUE`, `LIGHTEN`, `LINEARBURN`, `LINEARDODGE`, `LINEARLIGHT`, `LUMINOSITY`, `MULTIPLY`, `NORMAL`, `OVRLAD`, `PASSTHUGH`, `PINLIGHT`, `SATURATION`, `SCREEN`, `SOFTLIGHT`, `SUBTRACT`, `VIVIDLIGHT` | 控制应用滤镜时图像中像素的混合方式。`ArtLayer.blendMode` 和 `LayerSet.blendMode` 的值。 |
| `BMPDepthType` | `BMP_A1R5G5B5`, `BMP_A4R4G4B4`, `BMP_A8R8G8B8`, `BMP_R5G6B5`, `BMP_R8G8B8`, `BMP_X1R5G5B5`, `BMP_X4R4G4B4`, `BMP_X8R8G8B8`, `EIGHT`, `FOUR`, `ONE`, `SIXTEEN`, `THIRTYTWO`, `TWENTYFOUR` | 每个通道的位数（也称为像素深度或颜色深度）。所选数字表示 2 的指数。例如，位深度为 `EIGHT` 的像素具有 $2^8$（即 256）种可能的颜色值。用于 `BMPSaveOptions`。 |
| `ByteOrder` | `IBM`, `MACOS` | 读取多字节值特定于平台的顺序。 |
| `CameraRAWSettingsType` | `CAMERA`, `CUSTOM`, `SELECTEDIMAGE` | 要使用的默认 Camera Raw 设置：相机设置、自定义设置或所选图像的设置。在 `CameraRAWOpenOptions` 中设置。 |
| `CameraRAWSize` | `EXTRALARGE`, `LARGE`, `MAXIMUM`, `MEDIUM`, `MINIMUM`, `SMALL` | 相机 RAW 尺寸：`EXTRALARGE`=5120，`LARGE`=4096，`MAXIMUM`=3072，`MEDIUM`=2048，`MINIMUM`=1024，`SMALL`=512。 |



| 属性 | 值 | 含义 |
| :--- | :--- | :--- |
| `ColorSpaceType` | ADOBERGB<br>COLORMATCHRGB<br>PROPHOTORGB<br>SRGB | 在 `CameraRAWOpenOptions` 中使用的颜色空间类型。 |
| `CopyrightedType` | COPYRIGHTEDWORK<br>PUBLICDOMAIN<br>UNMARKED | 文档的版权状态。用于 `DocumentPrintSettings.copyrighted`。 |
| `CreateFields` | DUPLICATION<br>INTERPOLATION | 用于创建字段的方法。传递给 `ArtLayer.applyDeInterlace()`。 |
| `CropToType` | ARTBOX<br>BLEEDBOX<br>BOUNDINGBOX<br>CROPBOX<br>MEDIABOX<br>TRIMBOX | 在 PDF 文档中裁剪页面时使用的样式。在 `PDFOpenOptions.cropPage` 中设置。 |
| `DCSType` | COLORCOMPOSITE<br>GRAYSCALECOMPOSITE<br>NOCOMPOSITE | 使用 `DCS1_SaveOptions` 或 `DCS2_SaveOptions` 创建的复合 DCS 文件类型：<br><br>COLORCOMPOSITE：除了 DCS 文件外，还创建一个颜色复合文件。<br><br>GRAYSCALECOMPOSITE：除了 DCS 文件外，还创建一个灰度复合文件。<br><br>NOCOMPOSITE：不创建复合文件。 |
| `DepthMapSource` | IMAGEHIGHLIGHT<br>LAYERMASK<br>NONE<br>TRANSPARENCYCHANNEL | 用于深度贴图的源。传递给 `ArtLayer.applyLensBlur()`。 |
| `DescValueType` | ALIASTYPE<br>BOOLEANTYPE<br>CLASSTYPE<br>DOUBLETYPE<br>ENUMERATEDTYPE<br>INTEGERTYPE<br>LARGEINTEGERTYPE<br>LISTTYPE<br>OBJECTTYPE<br>RAWTYPE<br>REFERENCETYPE<br>STRINGTYPE<br>UNITDOUBLE | 动作描述符键的值类型，由 `ActionDescriptor.getType()` 和 `ActionList.getType()` 返回。 |
| `DialogModes` | ALL<br>ERROR<br>NO | 控制运行脚本时 Photoshop 显示的对话框类型。 |
| `Direction` | HORIZONTAL<br>VERTICAL | • 要翻转文档画布的方向，传递给 `Document.flipCanvas()`。<br>• `TextItem.direction` 中文本的方向。<br>• `TextItem.warpDirection` 中文本扭曲的方向。 |

`annotSizeClass` 有两个属性：`width` 和 `height`，类型均为 `floatType`。枚举 `annotType` 有三个值：`annotUnknown`、`annotText` 和 `annotSound`。

```xml
<terminology><! CDATA [<<<
/Version 1
/Events
    /newAnnot [(New Annotation) <<
        /annotType [(Type) /annotType]
        /at [(At) /Point]
        /size [(Size) /annotSizeClass] >>]
/Classes
    /annotSizeClass [(Size) <<
        /width [(Width) /floatType]
        /height [(Height) /floatType]
    >>]
/Enumerations
    /annotType <<
        /annotUnknown (Unknown)
        /annotText (Text)
        /annotSound (Sound)
>>> ]]></terminology>
```

### Adobe Photoshop CS6 JavaScript 脚本参考

#### 脚本常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `DisplacementMapType` | STRETCHTOFIT, TILE | 描述当图像尺寸与置换贴图不同时，置换贴图如何适配图像。传递给 `ArtLayer.applyDisplace()`。 |
| `Dither` | DIFFUSION, NOISE, NONE, PATTERN | 在 `GIFSaveOptions`、`IndexedConversionOptions` 和 `ExportOptionsSaveForWeb` 中使用的仿色类型。 |
| `DocPositionStyle` | PRINTCENTERED, USERDEFINED | `DocPosition` 中使用的定位类型。 |
| `DocumentFill` | BACKGROUNDCOLOR, TRANSPARENT, WHITE | 新文档的填充类型，传递给 `Documents.add()`。 |
| `DocumentMode` | BITMAP, CMYK, DUOTONE, GRAYSCALE, INDEXEDCOLOR, LAB, MULTICHANNEL, RGB | 打开文档的颜色模式，`Document.mode`。另见 `Document.changeMode()`。 |
| `EditLogItemsType` | CONCISE, DETAILED, SESSIONONLY | 历史记录日志中首选的详细程度，在 `Preferences` 中设置：<br>CONCISE：保存简洁的历史记录日志。<br>DETAILED：保存详细的历史记录日志。<br>SESSIONONLY：仅保存当前会话的历史记录日志。 |
| `ElementPlacement` | INSIDE, PLACEATBEGINNING, PLACEATEND, PLACEBEFORE, PLACEAFTER | 对象在图层面板中的位置。<br>**注意**：并非所有值对所有对象类型都有效。请查看特定对象的描述以确保使用的是有效值。 |
| `EliminateFields` | EVENFIELDS, ODDFIELDS | 要消除的场类型。传递给 `ArtLayer.applyDeInterlace()`。 |
| `ExportType` | ILLUSTRATORPATHS, SAVEFORWEB | `Document.exportDocument()` 的导出类型。<br>这等于选择文件 > 导出 > Illustrator，或文件 > 存储为 Web 格式。 |
| `Extension` | LOWERCASE, NONE, UPPERCASE | 使用 `Document.saveAs()` 时，向文件名附加名的策略和格式。 |
| `FileNamingType` | DDMM, DDMMYY, DOCUMENTNAMELOWER, DOCUMENTNAMEUPPER, EXTENSIONLOWER, EXTENSIONUPPER, MMDD, MMDDYY, SERIALLETTERLOWER, SERIALLETTERUPPER, SERIALNUMBER1, SERIALNUMBER2, SERIALNUMBER3, SERIALNUMBER4, YYDDMM, YYMMDD, YYYYMM | 用于 `BatchOptions` 的命名选项。 |
| `FontPreviewType` | HUGE, EXTRALARGE, LARGE, MEDIUM, SMALL | 在字体菜单中预览的首选字体，在“选项”中设置。 |
| `FontSize` | LARGE, MEDIUM, SMALL | 用于面板和对话框的字体大小。 |
| `ForcedColors` | BLACKWHITE, NONE, PRIMARIES | 无论使用情况，都包含颜色表中的颜色。用于 `GIFSaveOptions` 和 `IndexedConversionOptions`。<br>BLACKWHITE：纯黑和纯白。<br>NONE：无。<br>PRIMARIES：红、绿、蓝、青、黄。 |
| `FormatOptions` | OPTIMIZEDBASELINE, PROGRESSIVE, STANDARDBASELINE | 在 `JPEGSaveOptions` 中保存 JPEG 时使用的选项。<br>OPTIMIZEDBASELINE：优化的颜色和略小的文件大小。<br>PROGRESSIVE：在图像下载时显示日益精细。<br>STANDARDBASELINE：大多数 Web 。 |
| `GalleryConstrainType` | CONSTRAINBOTH, CONSTRAINHEIGHT, CONSTRAINWIDTH | 图像约束的比例。用于 `GalleryImagesOptions`。 |
| `GalleryFontType` | ARIAL, COURIERNEW, HELVETICA, TIMESROMAN | 用于 Web 画廊和其他字体。用于 `GalleryBannerOptions`、`GalleryImagesOptions` 和 `GalleryThumbnailOptions`。 |
| `GallerySecurityTextColor` | BLACK, CUSTOM, WHITE | 用于画廊图像上显示水印文本的颜色。用于 `GallerySecurityOptions`。 |
| `GallerySecurityTextPositionType` | CENTERED, LOWERLEFT, LOWERRIGHT, UPPERLEFT, UPPERRIGHT | 在画廊图像上显示水印文本的位置。用于 `GallerySecurityOptions`。 |
| `GallerySecurityTextRotateType` | CLOCKWISE45, CLOCKWISE90, COUNTERCLOCKWISE45, COUNTERCLOCKWISE90, ZERO | 在画廊图像上显示水印文本的方向。用于 `GallerySecurityOptions`。 |
| `GallerySecurityType` | CAPTION, CREDIT, CUSTOMTEXT, FILENAME, NONE, TITLE | 用于画廊图像上显示水印文本的内容。用于 `GallerySecurityOptions`。<br>**注意：** 除 `CUSTOMTEXT` 外，所有类型都从图像信息中提取。 |
| `GalleryThumbSizeType` | CUSTOM, LARGE, MEDIUM, SMALL | Web 画廊中缩略图的大小。用于 `GalleryThumbnailOptions`。 |
| `Geometry` | HEPTAGON, HEXAGON, OCTAGON, PENTAGON, SQUARE, TRIANGLE | 形状的几何选项，例如镜头模糊滤镜中的光圈形状。<br><br>传递给 `ArtLayer.applyLensBlur()`。 |
| `GridLineStyle` | DASHED, DOTTED, SOLID | 在图像上显示的非打印网格的首选线条样式，在 `Preferences` 中设置。 |
| `GridSize` | LARGE, MEDIUM, NONE, SMALL | 网格线间距的首选大小，在 `Preferences` 中设置。 |
| `GuideLineStyle` | DASHED, SOLID | 在图像上显示的非打印参考线的首选线条样式，在 `Preferences` 中设置。 |
| `IllustratorPathType` | ALLPATHS, DOCUMENTBOUNDS, NAMEDPATH | 使用 `Document.exportDocument()` 导出到 Illustrator 文件的路径。 |
| `Intent` | ABSOLUTECOLORIMETRIC, PERCEPTUAL, RELATIVECOLORIMETRIC, SATURATION | 使用 `Document.convertProfile()` 或 `Document.print()` 从一个颜色空间转换到另一个时使用的渲染意图。 |
| `Justification` | CENTER, CENTERJUSTIFIED, FULLYJUSTIFIED, LEFT, LEFTJUSTIFIED, RIGHT, RIGHTJUSTIFIED | 段落文本在定界框内的放置方式。用于 `TextItem.justification`。 |
| `Language` | BRAZILLIANPORTUGUESE, CANADIANFRENCH, DANISH, DUTCH, ENGLISHUK, ENGLISHUSA, FINNISH, FRENCH, GERMAN, ITALIAN, NORWEGIAN, NYNKSORWEGIAN, OLDGERMAN, PORTUGUESE, SPANISH, SWEDISH, SWISSGERMAN | 用于文本的语言。用于 `TextItem.language`。 |
| `LayerCompression` | RLE, ZIP | 保存为 TIFF 格式时，图层中像素数据的压缩方法。用于 `TiffSaveOptions`。 |
| `LayerKind` | BLACKANDWHITE, BRIGHTNESSCONTRAST, CHANNELMIXER, COLORBALANCE, CURVES, EXPOSURE, GRADIENTFILL, GRADIENTMAP, HUESATURATION, INVERSION, LEVELS, NORMAL, PATTERNFILL, PHOTOFILTER, POSTERIZE, SELECTIVECOLOR, SMARTOBJECT, SOLIDFILL, TEXT, THRESHOLD, LAYER3D, VIBRANCE, VIDEO | `ArtLayer.kind` 中图层对象的类型。<br><br>**注意：** 您只能从空白图层创建文字图层。 |
| `LensType` | MOVIEPRIME, PRIME105, PRIME35, ZOOMLENS | 要使用的镜头类型。传递给 `ArtLayer.applyLensFlare()`。 |
| `MagnificationType` | ACTUALSIZE, FITPAGE | 查看图像时使用的放大类型。用于 `PresentationOptions`。 |


```markdown
| `MatteType` | BACKGROUND, BLACK, FOREGROUND, NETSCAPE, NONE, SEMIGRAY, WHITE | 用于填充图像透明区域相邻的抗锯齿边缘的颜色。当图像的透明度关闭时，哑光颜色将应用于透明区域。用于 [GIFSaveOptions](https://github.com/)、[IndexedConversionOptions](https://github.com/) 和 [JPEGSaveOptions](https://github.com/)。 |
| `MeasurementRange` | ALLMEASUREMENTS, ACTIVEMEASUREMENTS | 要处理的测量。传递给 [MeasurementLog](https://github.com/) 方法。 |
| `MeasurementSource` | MEASURESELECTION, MEASURECOUNTTOOL, MEASURERULERTOOL | 记录测量的来源。传递给 `Document.recordMeasurements()`(https://github.com/) 。 |
| `NewDocumentMode` | BITMAP, CMYK, GRAYSCALE, LAB, RGB | 用于新文档的颜色配置文件。传递给 `Documents.add()`(https://github.com/)。也用于 [ContactSheetOptions](https://github.com/) 和 [PicturePackageOptions](https://github.com/)。 |

##### Adobe Photoshop CS6 JavaScript 脚本参考

###### 脚本常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `NoiseDistribution` | GAUSSIAN, UNIFORM | 应用添加杂色滤镜时使用的分布方法。传递给 `ArtLayer.applyAddNoise()`(https://example.com)()。 |
| `OffsetUndefinedAreas` | REPEATEDGEPIXELS, SETTOBACKGROUND, WRAPAROUND | 用于填充图像或选区偏移后所留空白区域的方法。传递给 `ArtLayer.applyOffset()`(https://example.com)()。 |
| `OpenDocumentMode` | CMYK, GRAYSCALE, LAB, RGB | 打开 EPS 或 PDF 文档时使用的颜色配置文件。传递给 `EPSOpenOptions`(https://example.com) 或 `PDFOpenOptions`(https://example.com) 中的 `app.open()`。 |
| `OpenDocumentType` | ALIASPIX, BMP, CAMERARAW, COMPUSERVEGIF, DICOM, ELECTRICIMAGE, EPS, EPSPICTPREVIEW, EPSTIFFPREVIEW, FILMSTRIP, JPEG, PCX, PDF, PHOTOCD, PHOTOSHOP, PHOTOSHOPDCS_1, PHOTOSHOPDCS_2, PHOTOSHOPEPS, PHOTOSHOPPDF, PICTFILEFORMAT, PICTRESOURCEFORMAT, PIXAR, PNG, PORTABLEBITMAP, RAW, SCITEXCT, SGIRGB, SOFTIMAGE, TARGA, WAVEFRONTRLA, WIRELESSBITMAP | 使用 `app.open()` 打开文档的格式。**注意：** `PHOTOCD` 已弃用。柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。**注意：** `DICOM` 选项仅适用于扩展版。 |
| `OperatingSystem` | OS2, WINDOWS | [BMPSaveOptions](https://example.com) 中的目标操作系统。 |
| `Orientation` | LANDSCAPE, PORTRAIT | [PhotoCDOpenOptions](https://example.com) 的页面方向，在 Photoshop CS3 中已弃用。**注意：** 柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。 |
| `OtherPaintingCursors` | PRECISEOTHER, STANDARDOTHER | 以下工具的首选指针：橡皮擦、铅笔、画笔、修复画笔、仿制图章、图案图章、涂抹、模糊、锐化、减淡、加深、海绵。在[首选项](#)中设置。 |
| `PaintingCursors` | BRUSHSIZE, PRECISE, STANDARD | 以下工具的首选指针：选框、套索、多边形套索、魔棒、裁剪、切片、修补、吸管、钢笔、渐变、直线、油漆桶、磁性套索、磁性钢笔、自由钢笔、度量、颜色取样器。在[首选项](#)中设置。 |
| `PaletteType` | EXACT, LOCALADAPTIVE, LOCALPERCEPTUAL, LOCALSELECTIVE, MACOSPALETTE, MASTERADAPTIVE, MASTERPERCEPTUAL, MASTERSELECTIVE, PREVIOUSPALETTE, UNIFORM, WEBPALETTE, WINDOWSPALETTE | [GIFSaveOptions](#) 和 [IndexedConversionOptions](#) 中使用的调色板类型。 |
| `PathKind` | CLIPPINGPATH, NORMALPATH, TEXTMASK, VECTORMASK, WORKPATH | [PathItem](#) 的类型。 |
| `PDFCompatibility` | PDF13, PDF14, PDF15, PDF16, PDF17 | 使文档兼容的 PDF 版本。用于 [PDFSaveOptions](#)。 |
| `PDFEncoding` | JPEG, JPEG2000HIGH, JPEG2000LOSSLESS, JPEG2000LOW, JPEG2000MED, JPEG2000MEDHIGH, JPEG2000MEDLOW, JPEGHIGH, JPEGLOW, JPEGMED, JPEGMEDHIGH, JPEGMEDLOW, NONE, PDFZIP, PDFZIP4BIT | 以 PDF 格式保存文档时使用的压缩类型。用于 [PDFSaveOptions](#)。 |
| `PDFResample` | NONE, PDFSAVERAGE, PDFBICUBIC, PDFSUBSAMPLE | 使用的重新采样方法。用于 [PDFSaveOptions](PDFSaveOptions)。 |
| `PDFStandard` | NONE, PDFX1A2001, PDFX1A2003, PDFX32002, PDFX32003, PDFX42008 | 使文档兼容的 PDF 标准。用于 [PDFSaveOptions](PDFSaveOptions)。 |
| `PhotoCDColorSpace` | LAB16, LAB8, RGB16, RGB8 | [PhotoCDOpenOptions](PhotoCDOptions) 的颜色空间，在 Photoshop CS3 中已弃用。**注意：** 柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。 |
| `PhotoCDSize` | EXTRALARGE, LARGE, MAXIMUM, MINIMUM, SMALL | [PhotoCDOpenOptions](PhotoCDOptions) 中图像的像素尺寸，在 Photoshop CS3 中已弃用。`EXTRALGE=1024x1536`，`LARGE=512x768`，`MAXIMUM=2048x3072`，`MEDIUM=256x384`，`SMALL=128x192`。**注意：** 柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。 |
| `PICTBitsPerPixel` | EIGHT, FOUR, SIXTEEN, THIRTYTWO, TWO | 压缩 PICT 文件时每像素位数。用于 [PICTSaveOptions](PICTSaveOptions) 和 [PICTResourceOptions](PICTResourceOptions)。**注意：** RGB 图像使用16；位图和灰度图像4或8。 |
| `PICTCompression` | JPEGHIGHPICT, JPEGLOWPICT, JPEGMAXIMUMPICT, JPEGMEDPICT, NONE | 将图像另存为 PICT 文件使用的压缩类型。用于 [PICTSaveOptions](PICTSaveOptions) 和 [PICTResourceOptions](PICTResourceOptions)。 |
| `PicturePackageTextType` | CAPTION, CREDIT, FILENAME, NONE, ORIGIN, USER | 图片包的功能含义。用于 [PicturePackageOptions](PicturePackageOptions)。 |
| `PointKind` | CORNERPOINT, SMOOTHPOINT | 路径点在项目中的作用。 |
| `PointType` | POSTSCRIPT, TRADITIONAL | 类型首选的量单位，在首选项中设置：`POSTSCRIPT=72 点`，`TRADITIONAL=72 点`。 |
| `PolarConversionType` | POLARTORECTULAR, RECTANGULOPOLAR | 使用的极坐标扭曲方法。传递给 `ArtLayer.applyPolarCoordinates()`。 |
| `Preview` | EIGHTBITTIFF, MACOSEIGHTBIT, MACOSMOCHROME, MONOCHOMETIFF, NONE | 用作应用程序中低分辨率预览的图像类型。用于 `DCS1_SaveOptions`、`DCS2_SaveOptions` 和 `EPSaveOptions`。 |
| `PrintColorHandling` | PRINTERMANAGED, PHOTOSHOPMANAGED, SEPARATIONS | 用于 ColorHandling 的颜色处理类型。 |
| `PurgeTarget` | ALLCACHES, CLIPBOARDCACHE, HISTORYCACHES, UNDOCACHES | `Application.purge()` 操作要清除的缓存。 |
| `QueryStateType` | ALWAYS, ASK, NEVER | 打开 PSD 文件时检查是否最大化兼容性的选策略，在首选项 `maximizeCompatibility` 中设置。 |
| `RadialBlurMethod` | SPIN, ZOOM | 使用的模糊方法。传递给 `ArtLayer.applyRadialBlur()`。 |
| `RadialBlurQuality` | BEST, DRAFT, GOOD | 模糊图像的平滑度或颗粒度。传递给 `ArtLayer.applyRadialBlur()`。 |
| `RasterizeType` | ENTIRELAYER, FILLCONTENT, LAYERCLIPPINGPATH, LINKEDLAYERS, SHAPE, TEXTCONTENTS | 使用 `ArtLayer.rasterize()` 要栅格化的图层元素。 |
| `ReferenceFormType` | CLASSTYPE, ENUMERATED, IDENTIFIER, INDEX, NAME, OFFSET, PROPERTY | ActionReference 对象的类型，由 `getForm()` 返回。 |
| `ResampleMethod` | BICUBIC, BICUBICSHARPER, BICUBICSMOOTHER, BILINEAR, NEARESTNEIGHBOR, NONE | 图像插值的方法。传递给 `Document.resizeImage()`，并用作首选项 `interpolation` 的值。 |
| `RippleSize` | LARGE, MEDIUM, SMALL | 使用的波纹大小。传递给 `ArtLayer.applyRipple()`。 |
| `SaveBehavior` | ALWAYSSAVE, ASKWHENSAVING, NEVERSAVE | 应用程序保存文档时的首选行为。请参阅首选项 `appendExtension` 和 `imagePreviews`。 |
| `SaveDocumentType` | ALIASPIX, BMP, COMPSERVEGIF, ELECTRICIMAGE, JPEG, PCX, PHOTOSHOP, PHOTOSHOPDCS_1, PHOTOSHOPDCS_2, PHOTOSHOPEPS, PHOTOSHOPPDF, PICTFILEFORMAT, PICTRESOURCEFORMAT, PIXAR, PNG, PORTABLEBITMAP, RAW, SCITEXCT, SGIRGB, SOFTIMAGE, TARGA, WAVEFRONTRLA, WIRELESSBITMAP | 使用 `Document.exportDocument()` 导出时保存文档的格式。传递给 `ExportOptionsSaveForWeb.format`，以指定要写入的文件类型。仅支持以下格式导出：`COMPSERVEGIF`、`JPEG`、`PNG-8`、`PNG-24` 和 `BMP`。 |
| `SaveEncoding` | ASCII, BINARY, JPEGHIGH, JPEGLOW, JPEGMAXIMUM, JPEGMEDIUM | 使用 `Document.saveAs()` 保存文件到 DCS 或 EPS 时使用的编码类型。 |
| `SaveLogItemsType` | LOGFILE, LOGFILEANDMETADATA, METADATA | 历史记录日志数据的首选存储位置，在首选项 `saveItems` 中设置。 |
| `SaveOptions` | DONOTSAVECHANGES, PROMPTTOSAVECHANGES, SAVECHANGES | 使用 `Document.close()` 关闭文档时的策略。 |

##### Adobe Photoshop CS6 脚本参考

脚本常量 24

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `SelectionType` | `DIMINISH`, `EXTEND`, `INTERSECT`, `REPLACE` | 当已存在选区时的选区行为：br><br>`DIMINISH`：从已选区域中移除选区。<br><br>`EXTEND`：将选区添加到已选区域。<br><br>`INTERSECT`：仅保留新选区与已选区域相交的部分。<br><br>`REPLACE`：替换已选区域。<br><br>用于 `PathItem.makeSelection()`、`Selection.load()`、`Selection.select()` 和 `Selection.store()`。 |
| `ShapeOperation` | `SHAPEADD`, `SHAPEINTERSECT`, `SHAPESUBTRACT`, `SHAPEXOR` | 如果目标路径已存在选区时，如何组合形状。<br><br>为 `SubPathInfo.operation` 设置，存储在结果 `SubPathItem` 中。 |
| `SmartBlurMode` | `EDGEONLY`, `NORMAL`, `OVERLAYEDGE` | 智能模糊的方法：<br><br>`EDGEONLY`、`OVERLAYEDGES`：仅对颜色过渡的边缘应用模糊。<br><br>`NORMAL`：对整个图像应用模糊。<br><br>传递给 `ArtLayer.applySmartBlur()`。 |
```

```markdown
| `SmartBlurQuality` | `HIGH`<br>`LOW`<br>`MEDIUM` | 模糊质量。传递给 [`ArtLayer.applySmartBlur()`](http://javascript-ref/ArtLayer-applySmartBlur)。 | |

| `SourceSpaceType` | `DOCUMENT`<br>`PROOF` | 使用 [`Document.print()`](http://javascript-ref/Document-print) 打印时源的色彩空间。 |

| `SpherizeMode` | `HORIZONTAL`<br>`NORMAL`<br>`VERTICAL` | 用于变形的曲线（或拉伸形状）。传递给 [`ArtLayer.applySpherize()`](http://javascript-ref/ArtLayer-applySpherize)。 | |

| `StrikeThruType` | `STRIKEBOX`<br>`STRIKEHEIGHT`<br>`STRIKEOFF` | 文本中使用的删除线样式。用于 [`TextItem.strikeThru`](http://javascript-ref/TextItem-strikeThru)。 | |

| `StrokeLocation` | `CENTER`<br>`INSIDE`<br>`OUTSIDE` | 路径或选区边界描边的位置。传递给 [`Selection.stroke()`](http://javascript-ref/Selection-stroke)。 | |

| `TargaBitsPerPixel` | `SIXTEEN`<br>`THIRTYTWO`<br>`TWENTYFOUR` | 保存为 Targa 格式时使用的分辨率。用于 [`TargaSaveOptions`](http://javascript-ref/TargaSaveOptions)。 | |

| `TextCase` | `ALLCAPS`<br>`NORMAL`<br>`SMALLCAPS` | 文本中使用的大写样式。用于 [TextItem.capitalization](https://helpx.adobe.com/photoshop/using/text-layer.html)。 | |

| `TextComposer` | `ADOEBEEVERYLINE`<br>`ADOBESINGLELINE` | 用于优化指定的断字和对齐选项的组合方法。用于 [TextItem.textComposer](https://helpx.adobe.com/photoshop/using/text-layer.html)。 | |

| `TextType` | `PARAGRAPHTEXT`<br>`POINTTEXT` | 文本类型，用于 [TextItem.kind](https://helpx.adobe.com/photoshop/using/text-layer.html)。<br><br>`PARAGRAPHTEXT`：在边界框内自动换行的文本。<br><br>`POINTTEXT`：不自动换行的文本。 | |

| `TextureType` | `BLOCKS`<br>`CANVAS`<br>`FILE`<br>`FROSTED`<br>`TINYLENS` | 用于纹理化或玻璃滤镜的纹理或玻璃表面图像类型。传递给 [ArtLayer.applyGlassEffect()](https://helpx.adobe.com/photoshop/using/text-layer.html)。 | |

| `TIFFEncoding` | `JPEG`<br>`NONE`<br>`TIFFLZW`<br>`TIFFZIP` | TIFF 文件使用的压缩类型。用于 [TiffSaveOptions](https://helpx.adobe.com/photoshop/using/text-layer.html)。 | |

| `ToolType` | `ARTHISTORYBRUSH`<br>`BACKGROUNDERASER`<br>`BLUR`<br>`BRUSH`<br>`BURN`<br>`CLONESTAMP`<br>`COLORREPLACEMENTTOOL`<br>`DODGE`<br>`ERASER`<br>`HEALINGBRUSH`<br>`HISTORYBRUSH`<br>`PATTERNSTAMP`<br>`PENCIL`<br>`SHARPEN`<br>`SMUDGE`<br>`SPONGE` | 与 [PathItem.strokePath()](https://helpx.adobe.com/photoshop/using/text-layer.html) 一起使用的工具。 | |

| `TransitionType` | `BLINDSHORIZONTAL`<br>`BLINDSVERTICAL`<br>`BOXIN`<br>`BOXOUT`<br>`DISSOLVE`<br>`GLITTERDOWN`<br>`GLITTERRIGHT`<br>`GLITTERRIGHTDOWN`<br>`NONE`<br>`RANDOM`<br>`SPLITHORIZONTALIN`<br>`SPLITHORIZONTALOUT`<br>`SPLITVERTICALIN`<br>`SPLITVERTICALOUT`<br>`WIPEDOWN`<br>`WIPELEFT`<br>`WIPE RIGHT`<br>`WIPEUP` | PDF 演示中从一张图像过渡到下一张图像的方法。用于 [PresentationOptions](https://helpx.adobe.com/photoshop/using/text-layer.html)。 | |

| `TrimType` | `BOTTOMRIGHT`<br>`TOPLEFT`<br>`TRANSPARENT` | 围绕图像裁剪的像素类型，传递给 [Document.trim()](https://photoshop-scripting-reference.readthedocs.io/)。<br><br>`BOTTOMRIGHT` = 右下角像素颜色。<br><br>`TOPLEFT` = 左上角像素颜色。 | |

| `TypeUnits` | `MM`<br>`PIXELS`<br>`POINTS` | 文本字符测量的首选单位，在 [首选项](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 | |

| `UndefinedAreas` | `REPEATEDGEPIXELS`<br>`WRAPAROUND` | 处理“扭曲”类别滤镜应用后图像中未变形或留白区域的方法。传递给 [`ArtLayer.applyDisplace()](https://photoshop-scripting-reference.readthedocs.io/)、`applyShear()](https://photoshop-scripting-reference.readthedocs.io/)、`applyWave()](https://photoshop-scripting-reference.readthedocs.io/)。 | |

| `UnderlineType` | `UNDERLINELEFT`<br>`UNDERLINEOFF`<br>`UNDERLINERIGHT` | 文本下划线的位置。用于 [TextItem.underline](https://photoshop-scripting-reference.readthedocs.io/)。<br><br>**注意：**`UNDERLINELEFT` 和 `UNDERLINERIGHT` 仅在`Direction.VERTICAL` 时有效。 | |

| `Units` | `CM`<br>`INCHES`<br>`MM`<br>`PERCENT`<br>`PIXELS`<br>`POINTS` | 类型和标尺量的首选单位，在 [Preferences.rulerUnits](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 | |

| `Urgency` | `FOUR`<br>`HIGH`<br>`LOW`<br>`NORMAL`<br>`SEVEN`<br>`SIX`<br>`TWO` | 文档的紧急状态，在 [DocumentSettings.urgency](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 | |

| `WarpStyle` | `ARC`<br>`ARCH`<br>`ARCLOWER`<br>`ARCUPPER`<br>`BULGE`<br>`FISH`<br>`INFLATE`<br>`FLAG` | 用于文本变形。用于 [TextItem.warpStyle](https://photoshop-scripting-reference.readthedocs.io/)。 | |

| `WaveType` | `SINE`<br>`SQUARE`<br>`TRIANGULAR` | 使用的波形类型。传递给 [`ArtLayer.applyWave()](https://photoshop-scripting-reference.readthedocs.io/)。 | |

| `WhiteBalance` | `AS`<br>`AUTO`<br>`CLOUDY`<br>`CUSTOM`<br>`DAYLIGHT`<br>`FLASH`<br>`FLUORECENT`<br>`SHADE`<br>`TUNG` | 影响色彩的光照。在 [CameraOpenOptions](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 | |

| `ZigZagType` | `AROUNDCENTER`<br>`OUTFROM`<br>`PONDRIPPLES` | 使用的锯齿方法。传递给 [`ArtLayer.applyZigZag()](https://photoshop-scripting-reference.readthedocs.io/)。 | |

###下表列出了事件及其四字符代码或标识符，用于 `notifier` 对象。**注意：** 在代码中，不要为四字符 ID包含单引号。此表中的单引号用于说明不含四个字母的位置。但是，长于四个字符的标识符在代码中需要双引号。**提示：** 如果在此表中找不到要通知的事件，可以使用 ScriptListener 来确定事件 代码。请参阅 Photoshop6 脚本指南 操作章节中的 ScriptListener 文档。

| 事件 | 4字符 ID 或 字符串 |
| --- | --- |
| 炭笔 | `Chrc` |
| 铬黄 | `Chrm` |
| 清除 | `Cler` |
| 关闭 | `Cls ` |
| 云彩 | `Clds` |
| 色彩平衡 | `ClrB` |
| 彩色半调 | `ClrH` |
| 色彩范围 | `ClrR` |
| 彩色铅笔 | `ClrP` |
| 联系表 | `0B71D221-F8CE-11d2-B21B-0008C75B322C` |
| Conte 蜡笔 | `CntC` |
| 收缩 | `Cntc` |
| 转换模式 | `CnvM` |
| 复制 | `copy` |
| 复制效果 | `CpFX` |
| 合并复制 | `CpyM` |
| 复制到图层 | `CpTL` |
| 龟裂缝 | `Crql` |
| 创建水滴 | `CrtD` |
| 裁剪 | `Crop` |
| 阴线 | `Crsh` |
| 晶格化 | `Crst` |
| 曲线 | `Crvs` |
| 自定 | `Cstm` |
| 剪切 | `cut ` |
| 剪切到图层 | `CtTL` |
| 剪纸 | `Ct ` |
| 深色线条 | `DrkS` |
| 逐行扫描 | `Dntr` |
| 定义 | `Def` |
| 扩散 | `Dfs` |
| 删除 | `Del` |
| 差异 | `Dst` |
| 扩散 | `Dsl` |
| 导出 | `Drt` |
| 边缘 | `Edg` |
| 填充 | `Fil` |
| 复制 | `Evi` |
| 提取 | `Ext` |
| 查找 | `Fnd` |
| 模糊 | `Blu` |
| 边界 | `Bdr` |
| 亮度 | `Brg` |
| 画布大小 | `CnvS` |
| 炭色 | `ChlC` |
| 混合模式 | `ChnM` |
| 3D变换 | `DdT` |
| 平均 | `Avrg` |
| 应用样式 | `ASty` |
| 断言 | `Asrt` |
| 装饰边缘 | `AccE` |
| 增加 | `Add` |
| 噪声 | `AdNs` |
| 添加到 | `AddT` |
| 对齐 | `Algn` |
| 全部 | `All` |
| 倾斜线条 | `AngS` |
| 应用图像 | `AppI` |
| 浮雕 | `BsRl` |
| 批处理 | `Btch` |
| 批处理滴 | `BtcF` |
| 模糊 | `Blr` |
| 模糊更多 | `BlrM` |
| 边框 | `Brdr` |
| 亮度 | `BrgC` |
```


| 粘贴到外部 | `'PstO'` |
| 拼缀图 | `'Ptch'` |
| 影印 | `'Phtc'` |
| 图片包 | `"4C1ABF40-DD82-11d2-B20F-0008C75B322C"` |
| 挤压 | `'Pnch'` |
| 置入 | `'Plc ` |
| 石膏效果 | `'Plst'` |
| 塑料包装 | `'PlsW'` |
| 播放 | `'Ply ` |
| 点状化 | `'Pntl'` |
| 极坐标 | `'Plr ` |
| 海报边缘 | `'PstE'` |
| 色调分离 | `'Pstr'` |
| 上一步 | `'Prvs'` |
| 打印 | `'Prnt'` |
| 配置文件到配置文件 | `'PrfT'` |
| 清理 | `'Prge'` |
| 退出 | `'quit'` |
| 径向模糊 | `'RdlB'` |
| 栅格化 | `'Rstr'` |
| 栅格化类型图层 | `'RstT'` |
| 移去黑色杂边 | `'RmvB'` |
| 移去图层蒙版 | `'RmvL'` |
| 移去白色杂边 | `'RmvW'` |
| 重命名 | `'Rnm  '` |
| 替换颜色 | `'RplC'` |
| 重置 | `'Rset'` |
| 调整图像大小 | `"1333cf0c-cb67-11d1-bc43-0060b0a13dc4"` |
| 网状 | `'Rtcl'` |
| 恢复 | `'Rvrt'` |
| 波纹 | `'Rple'` |
| 旋转 | `'Rtte'` |
| 粗糙蜡笔 | `'RghP'` |
| 保存 | `'save'` |
| 选取 | `'slct'` |
| 可选颜色 | `'SlcC'` |
| 设置 | `'setd'` |
| 锐化边缘 | `'ShrE'` |
| 锐化 | `'Shrp'` |
| 进一步锐化 | `'ShrM'` |
| 切变 | `'Shr  '` |
| 显示 | `'Shw  '` |
| 选取相似 | `'Smlr'` |
| 特殊模糊 | `'SmrB'` |
| 平滑 | `'Smth'` |
| 涂抹棒 | `'SmdS'` |
| 曝光过度 | `'Slrz'` |
| 喷溅 | `'Spt '` |
| 球面化 | `'Sphr'` |
| 分离通道 | `'SplC'` |
| 海绵 | `'Spng'` |
| 喷色线条 | `'SprS'` |
| 染色玻璃 | `'StnG'` |
| 图章 | `'Stmp'` |
| 停止 | `'Stop'` |
| 描边 | `'Strk'` |
| 从选区减去 | `'Sbtr'` |
| 从选区减去 | `'SbtF'` |
| Sumie | `'Smie'` |
| 获取合并快照 | `'TkMr'` |
| 获取快照 | `'TkSn'` |
| 纹理填充 | `'TxtF'` |
| 纹理化 | `'Txtz'` |
| 阈值 | `'Thrs'` |
| 马赛克拼贴 | `'Tls '` |
| 撕边 | `'TrnE'` |
| 等高线 | `'TrcC'` |
| 变换 | `'Trnf'` |
| 陷印 | `'Trap'` |
| 旋转扭曲 | `'Twrl'` |
| 水彩画纸 | `'Undr'` |
| 还原 | `'undo'` |
| 取消编组 | `'Ungr'` |
| 取消链接 | `'Unlk'` |
| USM 锐化 | `'UnsM'` |
| 变化 | `'Vrtn'` |
| 等待 | `'Wait'` |
| 水彩纸 | `'WtrP'` |
| 水彩 | `'Wtrc'` |
| 波浪 | `'Wave'` |
| 风 | `'Wnd  '` |
| 水波 | `'ZgZg'` |
| 背光 | `'BacL'` |
| 填充闪光 | `'FilE'` |
| 色偏 | `'ColE'` |

# 索引

## A

### **动作管理器** 193
### **动作**
- 命令列表 40
- 描述 43
- 描述符 37
- 播放 47
- 活动文档 45
- `activePrinter` 96
- 添加杂色滤镜

### **调整**
- 亮度 55
- 颜色 197
- 色彩平衡 55, 61
- 对比度 55, 59
- 曲线 55
- 高光 62
- 色阶 55, 59
- 阴影 62
- 色温 61
Adobe Illustrator，将路径导出到 105

### **Alpha 通道**
- 定义 72
- 从透明区域（TIFF 文档）186
- 不透明度 72
- 保存:
    - 在 BMP 文档中 69
    - 在 PDF 文档中 148
    - 在 PICT 文档中 153
    - 在 PICT 资源中 154
    - 在 Pixar 文档中 156
    - 在 PSD 文档中 152
    - 在 RAW 文档中 164
    - 在 SGGB 文档中 171
    - 在 TIFF 文档中 176
### **锚点**
- 添加 143
- 注释，92

### **抗锯齿**
- 文本 179

### **应用程序**
- 激活 47
- 检查功能启用 47
- 默认值 158
- 位置 46
- 首选项 158
- 画图层，参见图层
- 作者 99
- 自动字距 179, 197
- 自动行距 184
- 自动间距，联系表 82
- 可内存 45
- 平均滤镜 55

## B

### **背景色**
- 应用 45
- 画廊 110
- 背景图层 53
- `backgroundColor` 96
- 基线偏移 79

### **批处理**
- 目标文件夹 66, 197
- 指定选项 66
- 蜂鸣 158

### **位图文档**
- 转换为 198
- 深度类型 198
- 半调类型 198
- 打开 207

### **位图图像**
- 参见位图文档
- 黑白图像 62
- `bleedWidth` 96

### **混合模式**
- 图层组 129
- 图层 53
- 模糊滤镜 55

### **模糊滤镜**
- 平均 55
- 进一步模糊 55
- 高斯模糊 56
- 镜头模糊 57
- 动感模糊 58
- 径向模糊 58
- 特殊模糊 59
- 进一步滤镜 55

### BMP 文档
- 参见位图文档

### **亮度**
- 调整 55
- 均匀化 60
- 构建 45

## C

### **缓存**
- 图像 159
- 清理 49

### **Camera Raw 文档**
- 打开 70
- 设置 199
- 大小选项 199
- 画布
- 翻转 92
- 调整大小 92
- 画布，定义 88
- 标题
- 联系表 82
- 文档 99
- 画廊图像 111
- 画廊缩略图 115
- 图像 99
- `centerCropMarks` 96

### 通道
- 激活 88
- 添加 74
- 调整 55
- Alpha 参见 Alpha 通道
- 创建 74
- 删除 72
- 以彩色显示 158
- 复制 72
- 显示 72
- 合并 72
- 混合 61
- 分离 93
- 专色参见专色通道
- 类型 72

### 剪贴路径
- 从路径 139
- 从文本 185
- 云彩滤镜 55
- `CMYKColor` 79
- 色彩平衡，调整 61
- 拾色器 158

### 颜色配置文件
- 更改 91
- 确定类型 89
- 命名 88
- 颜色配置文件，参见各文档格式

### 颜色取样器
- 添加 81
- 创建 81
- 移动 80
- 移除 80
- `colorBars` 96
- `colorHandling` 96

### 颜色
- 活动链接 110
- 调整 197
- 平衡 55
- 通道 72
- CMYK 79
- 自定义设置 113
- 在画廊中 110
- 反相 60
- 修改 62
- 无 135
- 保留（仅限 GIF）116
- 减少 106
- 设置 45
- 纯色对象 172
- 测试是否相等 172
- 已访问链接 110
- 注释，图层复合 126

### 兼容性，最大化 159
### 分量通道
- 色彩平衡 55
- 定义 72
- 列表 88
- 参见合成通道
### 合成通道 72
- 参见分量通道

### Compve GIF 文档
- 打开 207
- 保存 116
- 联系表
- 标题 82
- 列 82
- 尺寸 82
- 创建 48
- 行 82
- 对比度
- 调整 55
- 自动调整 59
- Camera Raw 设置 70
- 中间调 62
- 副本 96
- 版权信息 99
- `cornerCropMarks` 96

### 计数项目
- 添加 84
- 创建 84
- 移除 83
- 裁剪 91
- CS4 版本更改 34
- 光标 160
- 曲线，调整 55
- 自定滤镜 55

## D

### DCS 1 文档，保存 85
### 逐行扫描滤镜 56
### 去色 60
### 蒙尘与划痕滤镜 56

### 对话框
- 显示 45
- 差异云彩滤镜 56
- 扩散亮光滤镜 56
- 置换滤镜 56

### 扭曲滤镜
- 扩散亮光 56
- 置换 56
- 玻璃效果 56
- 海洋波纹 58
- 挤压 58
- 极坐标 58
- 波纹 58
- 切变 58
- 球面化 59

## J

### JavaScript
- Photoshop CS4 中的变更 34
- 支持功能 32

### JavaScript 资源
- 启用语法 190
- `resource` 189

## L

### `LabColor` 125
### 标签 96
### 语言 181

### 图层复合
- 添加 127
- 应用 126
- 在文档中 89

### 图层组
- 添加 131
- 艺术图层 129
- 复制 130
- 在文档中 89
- 链接的图层 129
- 链接 130
- 锁定内容 129
- 移动 130
- 嵌套 129
- 不透明度 129
- 取消链接 130

### 样式
- 图层样式，应用 59
### `LayerComps` 127
### 分层的 TIFF 文档，保存 158
### 图层 128

### 图层
- 添加 65
- 应用样式 59
- 背景 53
- 混合模式 53
- 边界 53
- 剪贴板 59
- 复合 126
- 复制 59
- 重复 60
- 拼合 53
- 在文档中 89
- 反相 60
- 类型 53
- 链接 60
- 锁定内容 53-54
- 可见 54
- 合并 60
- 移动 61
- 栅格化 92
- 栅格化内容 61
- 移除 65
- 调整大小 62
- 旋转 62
- 在 PDF 文档中保存 148
### `LayerSet` 129
### `LayerSets` 131
### 图层组
- 合并 130

### 行距 181, 184
### 模糊滤镜
- 应用 57
### 镜头光晕滤镜 57
- 字距 180-183

### 色阶
- 调整 55
- 自动调整 55

### 连字 179-181
- 链接的图层 60
- 取消链接 62

### 链接
- 颜色 110

## M

### MacOS
- 文件类型 46
### 托管文档 89
- `mapBlack` 96
- 最大化兼容性 159
- 最大值滤镜 57
- 中间值杂色滤镜 57
- 内存 45

### 合并
- 图层 60
- 可见图层 92

### 元数据
- 文档 89
- 文档对象 99
- 画廊 113
- `xmp` 90, 188

## 方法
- 批处理 47
### 中间调
- 色彩平衡 55
- 最小值滤镜 58
- 动感滤镜 58

## N

### 负片 96
### 杂色滤镜
- 添加杂色
- 去斑 56
- 蒙尘与划痕 56
- 中间值 57

### 非线性记录 159
### 通知
- 脚本中的事件 136
### 通知器
- 添加 137
- 事件 ID 216
- 移除 136
### NTSC 滤镜 58

## O

### 对象模型
- Photoshop CS4 中的变更 34
### 海洋波纹滤镜 58
### 位移滤镜 58
### 旧样式字体 183
### 不透明度
- 通道 72
- 画廊安全文本 114
- 图层填充 53
- 图层组 129
- 图层 54
- 图片包 155

### 打开选项
- DICOM 格式 87
- EPS 格式 103
- PDF 格式 147
- Photo CD 格式 151
- RAW 格式 70, 163

### 优化 106
### 其他滤镜
- 自定 55
- 高反差保留 56
- 最大值 57
- 最小值 58
- 位移 58

## P

### 调色板 160
### 粘贴 92
### 路径 46
### 路径项
- 添加 142
- 取消选择 138
- 填充 138
- 来自文本 185
- 建立选区 139
- 路径点 174
- 选择 139
- 指定路径类型 138
- 描边 139
- 子项 138
- 子路径信息 173
- 子路径项 174
- 从选区建立工作路径 167
### 路径点信息
- 锚点 144
- 左方向 144
- 右方向 144
### 路径点
- 锚点 143
- 左方向 143
- 右方向 143
`PathItems` 142
### 路径
- 参见路径项



选中区域 90

## 选区 166
- 边界 166
- 清除 166
- 复制 166
- 剪切 166
- 取消选择 166
- 羽化 166
- 填充 167
- 来自路径 139
- 从选区建立工作路径 167
- 调整大小 166, 167
- 旋转 167
- 平滑 168
- 描边 168

## 可选颜色 62

## SGIRGB 文档
- 保存 171, 211

`SGIRGBSaveOptions` 171, 197

## 阴影
- 调整 62
- 色彩平衡 55

## 锐化边缘滤镜 58

## 锐化滤镜 58

## 锐化滤镜
- 锐化 58
- 锐化边缘 58
- 进一步锐化 58
- `USM` 锐化 59

## 进一步锐化滤镜 58

## 切变滤镜 58

## 特殊模糊滤镜 59

## 智能引号 160

## 球面化滤镜 59

## 专色通道
- 已定义 72
- 合并到复合通道 73
- 不透明度 72
- 保存
  - 在 DCS 2 文档中 86
  - 在 PDF 文档中 149
  - 在 PSD 文档中 152
  - 在 RAW 文档中 164
  - 在 SGIRGB 文档中 171
  - 在 TIFF 文档中 186

`spotColors` 171

启动脚本 33

删除线 184

## 描边
- 默认描边颜色 45
- 路径项 139
- 选区 168

样式，应用 59
子路径项 138

`systemInformation` 46

## T
温度 61

## 术语词典
- 已定义 193
- 语法 193

## 文本
- 亚洲 160
- 自动字距调整 179
- 自动行距 184
- 说明文字 111
- 颜色 184
- 排版器 184
- 内容 179
- 从文本创建路径 185
- 格式 184
- 画廊安全 114, 204
- 连字 181
- 在图片包中 155
- 对齐 181
- 语言 181
- 偏移 179
- 方向 180
- 间距 180–183
- 字距微调 184
- 换行 181

文本排版器 184

## 文本字体
- 参见字体

## 文本项
- 参见文本

## 文本图层
- 添加内容 179
- 创建 53

## 纹理填充滤镜 59

## 纹理滤镜，纹理填充 59

## 阈值 62

## 缩览图 115
- Mac OS 159
- Windows 161

## TIFF 文档
- 分层的 158
- 保存 186

`togglePalettes` 50

## 工具提示 160

## 字距微调，文本 184

## 传输信息 99

## 陷印 93

## 旋转扭曲滤镜 59

## 字型单位 161

## U

## 下划线 184

## 单位

## V
`vectorData` 97
`version`
- application 47
- scripting interface 46

`video alpha` 161
`video filters`
- De-Interlace 56
- NTSC 58

`visibility`
- channels 72
- layer comps 126
- layers 54

## W
`warp` 184
`Wave filter` 59
Web photo galleries
- See galleries.

`webSnap` 107
`width` 90
Windows
- filetypes 47
word spacing 180–183
work paths
- designating 208
- from selected area 167
wrapping, text 181

## X
`XML` 188
`xmp metadata` 90, 188

## Z
`Zigzag filter` 59
`zoom` 159
