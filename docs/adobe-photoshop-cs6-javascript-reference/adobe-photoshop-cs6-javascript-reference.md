
# Adobe Photoshop CS6 JavaScript 参考

## Adobe Photoshop CS6 JavaScript 脚本参考

### 引言

本参考手册描述了 Adobe® Photoshop® CS6® JavaScript™ 类型库中的对象与方法。配套文档《Photoshop CS6 脚本编写指南》介绍了基本的脚本编写概念与 Photoshop 对象模型。本文档提供了 Photoshop 对象模型的详细参考信息，以及关于 JavaScript 特定功能的额外说明。

Adobe Photoshop CS6 采用了 ExtendScript，这是 Adobe 对 JavaScript 的扩展实现。有关更多信息，请参阅[Adobe Photoshop CS6 中的 JavaScript 支持](#Adobe Photoshop CS6 中的 JavaScript 支持)。

本书包含以下部分：

- 本引言，描述了 Adobe Photoshop CS6 中的脚本编写支持，并列出了自上一个版本以来 JavaScript 接口的变化。
- [JavaScript 对象参考](#JavaScript 对象参考)，提供了所有 Photoshop DOM 对象与命令的完整参考。
- [脚本编写常量](#脚本编写常量)，列出了 Photoshop 类型库中使用的所有枚举。

#### Adobe Photoshop CS6 中的 JavaScript 支持

JavaScript 文件要被 Photoshop 识别为有效的脚本文件，其扩展名必须为`.js`或`.jsx`。

在 Mac OS 上，使用这两种扩展名的脚本功能没有区别。在 Windows 上，如果从 Photoshop 内部打开脚本文件，使用`.js`和`.jsx`扩展名也没有区别。但是，如果通过双击启动脚本，`.js`扩展名的脚本将使用 Microsoft JScript 引擎解释，并且无法启动 Adobe Photoshop CS6。对于 Windows 系统，建议使用`.jsx`扩展名，因为它会使用 ExtendScript 引擎来解释脚本。

所有 Adobe Creative Suite 6 应用程序（包括 Adobe Photoshop CS6）都使用 ExtendScript，这是 Adobe 对 JavaScript 的扩展实现。ExtendScript 文件以`.jsx`扩展名作为标识。ExtendScript 提供了所有标准 JavaScript 功能，以及额外的功能和实用程序，例如：

- 调试环境（ExtendScript Toolkit）
- 本地化实用程序
- 允许您合并脚本并将其定向到特定应用程序的工具
- 平台无关的文件和文件夹表示

许多 JavaScript 对象和方法使用 ExtendScript 中定义的对象，例如`File`对象、`Folder`对象和`UnitValue`对象。因此，建议为您的脚本文件使用`.jsx`扩展名。

有关这些功能和其他功能的详细信息，请参阅《JavaScript 工具指南 CS6》。该文档随 Creative Suite 6 应用程序安装在以下位置：

- 在 Windows 上：

```
C:\Program Files\Adobe\Adobe Utilities\ExtendScript Toolkit CS6\SDK
```

#### 脚本编写常量

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

#### 执行脚本

Adobe Photoshop CS6 界面包含一个“脚本”菜单（文件 > 脚本），可快速便捷地访问您的 JavaScript。脚本可以直接作为菜单项列出，运行时只需选择它们，或者您可以浏览并运行文件系统中的任何 JavaScript。

如果 Adobe Photoshop CS6 在脚本执行过程中遇到错误，它会显示错误消息。

#### 安装脚本

要将 JavaScript 安装到“脚本”菜单中，请将其放入 Scripts 文件夹（`Photoshop CS6/Presets/Scripts`）。Scripts 文件夹中脚本的名称（不含文件扩展名）将显示在“脚本”菜单中。可以在“脚本”菜单中安装任意数量的脚本。

在 Adobe Photoshop CS6 运行时添加到 Scripts 文件夹的脚本，在下次启动应用程序之前不会出现在“脚本”菜单中。

在 Scripts 文件夹及其子文件夹中找到的所有脚本都会显示在“文件 > 脚本”菜单的顶层。添加子文件夹不会为“脚本”菜单增加层级结构。

#### 执行其他脚本

“脚本”菜单末尾的“浏览”项（“文件 > 脚本 > 浏览”）允许您执行未安装在 Scripts 文件夹中的脚本。您也可以使用“浏览”来选择在应用程序上次启动后安装在 Scripts 文件夹中的脚本。

选择“浏览”会显示一个文件浏览器对话框，允许您选择要执行的脚本文件。浏览对话框中仅显示`.js`或`.jsx`文件。选择脚本文件后，其执行方式与已安装的脚本相同。

#### 启动脚本

启动时，Adobe Photoshop CS6 会执行它在启动文件夹中找到的所有`.jsx`文件。

- 在 Windows 上，用于用户自定义脚本的启动文件夹是：

  `C:\Program Files\Common Files\Adobe\Startup Scripts CS6\Adobe Photoshop`

- 在 Mac OS 上，用于用户自定义脚本的启动文件夹是：

  `~/Library/Application Support/Adobe/Startup Scripts CS6/Adobe Photoshop`

如果脚本仅供 Adobe Photoshop CS6 执行，则必须包含类似以下的代码：

```
if( BridgeTalk.appName == "photoshop" ) {
    //继续执行脚本
}
```

更多详细信息，请参阅《JavaScript 工具指南 CS6》。

#### 对象模型用法与命名

JavaScript API 遵循 JavaScript 命名约定，所有类（对象类型）均以大写字母开头并采用混合大小写。通常，在 JavaScript 中，您使用`new`运算符来实例化类：

```
new ClassName();
```

然而，在 Photoshop 对象模型中，通常无需这样做。主要的对象类型被收集到集合类中；例如，一组`Document`对象包含在一个`Documents`集合对象中。然后，您可以通过对象层次结构中其容器的相应集合属性来访问该集合对象。

例如，所有打开文档的集合包含在顶层的`Application`对象中。您可以通过全局变量`app`访问它，或者直接在顶层引用其属性：

```
app.documents[0] // 获取第一个加载的文档
documents[0] // 这是相同的
```

集合属性与集合对象同名，但以小写字母开头。例如，一个`Document`包含一个`LayerSets`集合，一个`LayerSet`包含一个`ArtLayers`集合。要访问集合中的一个`ArtLayer`对象：

```
var myLayer = activeDocument.layerSets[0].artLayers[0];
```

这些集合，如本例所示，可以视为数组，这对迭代很有用。它们还提供方法来创建其包含的对象，以及按名称访问它们：

```
var newLayer = activeDocument.artLayers.add(); // 创建一个新的 ArtLayer 对象
newLayer.name = "My Layer"; // 命名以供将来引用
...
var layerRef = activeDocument.artLayers.getByName("My Layer");
```

某些对象，如`app.fonts`集合中包含的`Font`对象，是由应用程序创建的，而不是由您的脚本创建。

您的脚本确实使用 JavaScript 的`new`运算符来创建辅助对象，例如那些封装了以特定格式打开或保存文档的选项集的对象：

```
var opts = new PDFOpenOptions();
opts.page = 10;
app.open(myPDFFile, opts);
```

#### 与早期版本的变更——CS6 变更

以下是对 Adobe Photoshop CS6 中 JavaScript 对象模型和语言支持所做的更改：

- 新方法和属性：
  - `getLargeInteger` 已添加到`ActionDescriptor`和`ActionList`对象。
  - `putLargeInteger` 已添加到`ActionDescriptor`和`ActionList`对象。
  - `compression`方法已添加到`PNGSaveOptions`对象。

- 修改的枚举：
  - `LARGEINTEGERTYPE` 已添加到`DescValueType`枚举。
  - `EXTRALARGE`和`HUGE`已添加到`FontPreviewType`枚举。

## JavaScript 对象参考

Photoshop 对象（Adobe® Photoshop® CS6 的 JavaScript 类型库）按字母顺序和表格格式在本章中呈现。给出了几个对象模型类的示例代码，以帮助说明语法以及对象类的用法。

#### 对象描述

对象的属性和方法在每个对象的单独表格中描述。以下部分描述了这些描述中使用的约定。

#### 属性表示法

对象的属性表列出以下内容：

- 在每个对象中定义的属性。
- 每个属性的值类型。当值类型是常量或另一个对象时，该值是链接到该常量或对象列表的超文本链接。
- 属性的输入状态：只读或读写。
- 解释属性功能的描述。

| 属性 | 值类型 | 功能 |
| :--- | :--- | :--- |
| `displayDialogs` | [DialogModes] | 读写。应用程序的对话框模式，用于控制运行脚本时应显示哪些类型的对话框。 |

对于常量，如示例中的[DialogModes]，单击链接可转到显示允许值的表格。常量由对象表示，允许值是这些对象的属性。以“常量名.值”的形式指定常量值。例如：

```
app.displayDialogs = DialogModes.ERROR;
```

#### 方法表示法

对象的方法表列出以下内容：

- 方法名称。
- 参数列表。
- 与每个参数对应的参数值类型行。
- 返回值类型。
- 描述方法功能的描述，以及需要时对参数的进一步描述。

| 方法 | 参数类型 | 返回值 | 功能 |
| :--- | :--- | :--- | :--- |
| `crop()` | 4 个[UnitValue]的数组、`number`、[UnitValue]、[UnitValue] |  | 裁剪文档。`bounds`参数是裁剪后剩余区域的四个坐标数组，[左, 上, 右, 下]。 |

当参数类型或返回值是常量或另一个对象时，该值是链接到该常量或对象列表的超文本链接。

参数可以是必需的或可选的。可选参数在表中由方括号（[]）表示。在示例中，第一个参数`bounds`是必需的。其余参数都是可选的。

您必须为每个必需参数传递值。如果没有要传递的剩余值，您可以省略可选参数；但是，如果您希望使用任何非最后指定的可选参数的默认值，请传递`undefined`作为占位符。您必须按照列出的顺序输入值，以便 JavaScript 编译器知道您正在输入哪个值。

例如，以下仅传递必需参数（使用先前定义的变量作为边界区域）：

```
app.activeDocument.crop( myRegion );
```

以下跳过`angle`参数，指定`width`值，并省略最后的`height`值：

```
var myWidth = new UnitValue( "500 pixels" );
app.executeAction( myRegion, undefined, myWidth );
```

### ActionDescriptor

此对象提供了一种类似字典的机制，用于以键值对的形式存储数据。它可用于对 Photoshop 进行底层访问。有关此用法的示例，请参阅第 168 页的[选区示例脚本](https://example.com)。

许多配置文件使用序列化的动作描述符来表示其数据。例如，它用于封装[Application.playbackParameters](https://example.com)中的播放选项，并由[Application.getCustomOptions()](https://example.com)返回。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `count` | `number` | 只读。描述符中包含的键的数量。 |
| `typename` | `string` | 只读。被引用的`actionDescriptor`对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `clear()` |  |  | 清除描述符。 |
| `erase(key)` | `number` |  | 从描述符中擦除一个键。 |



### ActionDescriptor

此对象提供对动作描述符的底层访问，可用于对 Photoshop 进行底层操作。它包含一组键值对，其中键是数字标识符，值可以是多种类型（如布尔值、整数、字符串、文件路径等）。你可以通过 `put` 系列方法设置值，通过 `get` 系列方法获取值，并使用 `hasKey()` 检查键是否存在。

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `fromStream(value)` | `string` | | 从字节流创建一个描述符；用于从磁盘读取。 |
| `getBoolean(key)` | `number` | `boolean` | 获取一个布尔类型的键的值。 |
| `getClass(key)` | `number` | `number` | 获取一个类类型的键的值。 |
| `getData(key)` | `number` | `string` | 获取原始字节数据作为字符串值。 |
| `getDouble(key)` | `number` | `number` | 获取一个双精度类型的键的值。 |
| `getEnumerationType(key)` | `number` | `number` | 获取一个键的枚举类型。 |
| `getEnumerationValue(key)` | `number` | `number` | 获取一个键的枚举值。 |
| `getInteger(key)` | `number` | `number` | 获取一个整数类型的键的值。 |
| `getKey(index)` | `number` | `number` | 根据索引获取第 N 个键的 ID。 |
| `getLargeInteger(key)` | `number` | `number` | 获取一个大整数类型的键的值。 |
| `getList(key)` | `number` | `ActionList` | 获取一个列表类型的键的值。 |
| `getObjectType(key)` | `number` | `number` | 获取一个对象类型键中对象的类 ID。 |
| `getObjectValue(key)` | `number` | `ActionDescriptor` | 获取一个对象类型的键的值。 |
| `getPath(key)` | `number` | `File` | 获取一个文件类型的键的值。 |
| `getReference(key)` | `number` | `ActionReference` | 获取一个 `ActionReference` 类型的键的值。 |
| `getString(key)` | `number` | `string` | 获取一个字符串类型的键的值。 |
| `getType(key)` | `number` | `DescValueType` | 获取一个键的类型。 |
| `getUnitDoubleType(key)` | `number` | `number` | 获取一个 `UnitDouble` 类型键的单位类型。 |
| `getUnitDoubleValue(key)` | `number` | `number` | 获取一个 `UnitDouble` 类型键的值。 |
| `hasKey(key)` | `number` | `boolean` | 检查描述符是否包含提供的键。 |
| `isEqual(otherDesc)` | `ActionDescriptor` | `boolean` | 确定此描述符是否与另一个描述符相同。 |
| `putBoolean(key, value)` | `number`, `boolean` | | 为布尔类型的键设置值。 |
| `putClass(key, value)` | `number`, `number` | | 为类类型的键设置值。 |
| `putData(key, value)` | `number`, `string` | | 将原始字节数据作为字符串值放入。 |
| `putDouble(key, value)` | `number`, `number` | | 为双精度类型的键设置值。 |
| `putEnumerated(key, enumType, value)` | `number`, `number`, `number` | | 为一个键设置枚举类型和值。 |
| `putInteger(key, value)` | `number`, `number` | | 为整数类型的键设置值。 |
| `putLargeInteger(key, value)` | `number`, `number` | | 为大整数类型的键设置值。 |
| `putList(key, value)` | `number`, `ActionList` | | 为 `ActionList` 对象类型的键设置值。 |
| `putObject(key, classID, value)` | `number`, `number`, `ActionDescriptor` | | 为一个对象类型的键设置值，该对象由动作描述符表示。 |
| `putPath(key, value)` | `number`, `File` | | 为路径类型的键设置值。 |
| `putReference(key, value)` | `number`, `ActionReference` | | 为对象引用类型的键设置值。 |
| `putString(key, value)` | `number`, `string` | | 为字符串类型的键设置值。 |
| `putUnitDouble(key, unitID, value)` | `number`, `number`, `number` | | 为一个单位值（格式为双精度数）类型的键设置值。 |
| `toStream()` | | `string` | 将整个描述符作为字节流获取，用于写入磁盘。 |

### ActionList

此对象提供了一种类似数组的机制来存储数据。它可用于对 Photoshop 进行底层访问。

此对象非常适合存储相同类型的数据。列表中的所有项必须是同一类型。

你可以使用 `put` 方法（例如 `putBoolean()`）来附加新元素，并可以使用 `clear()` 清除整个列表，但不能以其他方式修改列表。

**注意：** `ActionList` 对象是动作管理器功能的一部分。有关使用动作管理器的详细信息，请参阅 *Photoshop CS6 脚本指南*。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `count` | `number` | 只读。组成该动作的命令数量。 |
| `typename` | `string` | 只读。被引用的 `ActionList` 对象的类名。 |

## 方法

除了 `clear()` 方法外，你可以使用此对象的方法来获取列表中特定类型数据的值或设置（放入）值的类型。

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `clear()` | | | 清除列表。 |
| `getBoolean(index)` | `number` | `boolean` | 获取一个布尔类型列表元素的值。 |
| `getClass(index)` | `number` | `number` | 获取一个类类型列表元素的值。 |
| `getData(index)` | `number` | `string` | 获取原始字节数据作为字符串值。 |
| `getDouble(index)` | `number` | `number` | 获取一个双精度类型列表元素的值。 |
| `getEnumerationType(index)` | `number` | `number` | 获取一个列表元素的枚举类型。 |
| `getEnumerationValue(index)` | `number` | `number` | 获取一个列表元素的枚举值。 |
| `getInteger(index)` | `number` | `number` | 获取一个整数类型列表元素的值。 |
| `getLargeInteger(index)` | `number` | `number` | 获取一个大整数类型列表元素的值。 |
| `getList(index)` | `number` | `ActionList` | 获取一个列表类型列表元素的值。 |
| `getObjectType(index)` | `number` | `number` | 获取一个对象类型列表元素的类 ID。 |
| `getObjectValue(index)` | `number` | `ActionDescriptor` | 获取一个对象类型列表元素的值。 |
| `getPath(index)` | `number` | `File` | 获取一个文件类型列表元素的值。 |
| `getReference(index)` | `number` | `ActionReference` | 获取一个 `ActionReference` 类型列表元素的值。 |
| `getString(index)` | `number` | `string` | 获取一个字符串类型列表元素的值。 |
| `getType(index)` | `number` | `DescValueType` | 获取一个列表元素的类型。 |
| `getUnitDoubleType(index)` | `number` | `number` | 获取一个双精度类型列表元素的单位值类型。 |
| `getUnitDoubleValue(index)` | `number` | `number` | 获取一个双精度类型列表元素的单位值。 |
| `putBoolean(value)` | `boolean` | | 附加一个新值，`true` 或 `false`。 |
| `putClass(value)` | `number` | | 附加一个新值，一个类或数据类型。 |
| `putData(value)` | `string` | | 附加一个新值，一个包含原始字节数据的字符串。 |
| `putDouble(value)` | `number` | | 附加一个新值，一个双精度数。 |
| `putEnumerated(enumType, value)` | `number`, `number` | | 附加一个新值，一个枚举（常量）值。 |
| `putInteger(value)` | `number` | | 附加一个新值，一个整数。 |
| `putLargeInteger(value)` | `number` | | 附加一个新值，一个大整数。 |
| `putList(value)` | `ActionList` | | 附加一个新值，一个嵌套的动作列表。 |

### ActionReference

此对象提供关于操作引用的信息。例如，当引用某个对象的名称时，你可能会使用 `keyName`。引用还需要知道你正在引用的具体名称。在这种情况下，你可以使用 `classDocument` 来指代文档名称，或使用 `classLayer` 来指代图层名称。它可以用于对 Photoshop 进行底层访问。包含与 `ActionDescriptor` 关联的数据。

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `typename` | `string` | 只读。引用的 Action 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| --- | --- | --- | --- |
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
| `putClass(desiredClass)` | `number` | | 在引用中放置一个新的类形式和类类型。 |
| `putEnumerated(desiredClass, enumType, value)` | `number`, `number`, `number` | | 将枚举类型和 ID 放入引用中，同时包含引用的所需类。 |
| `putIdentifier(desiredClass, value)` | `number`, `number` | | 在引用中放置一个新的标识符及其值。 |
| `putIndex(desiredClass, value)` | `number`, `number` | | 在引用中放置一个新的索引及其值。 |
| `putName(desiredClass, value)` | `number`, `string` | | 在引用中放置一个新的名称及其值。 |
| `putOffset(desiredClass, value)` | `number`, `number` | | 在引用中放置一个新的偏移量及其值。 |
| `putProperty(desiredClass, value)` | `number`, `number` | | 在引用中放置一个新的属性及其值。 |

### Application

Adobe Photoshop CS6 应用程序对象，它是对象模型的根，提供对所有其他对象的访问。此对象提供应用程序范围的信息，例如应用程序默认设置和可用字体。它提供了许多重要的方法，例如用于打开文件和加载文档的方法。

要访问属性和方法，你可以使用预定义的全局变量 `app`。例如：

```
var docRef = app.documents.add(800, 600, 72, "docRef", NewDocumentMode.RGB);
```

`Application` 对象的属性和方法也可以在顶层使用；你可以完全省略对 `Application` 对象的引用。例如：

```
var docRef = documents.add(800, 600, 72, "docRef", NewDocumentMode.RGB);
```

这种用法可能有些模糊；为了清晰起见，建议你使用对 `app` 的显式引用。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `activeDocument` | `Document` | 读写。最前面的文档。设置此属性等同于在 Adobe Photoshop CS6 应用程序中单击一个打开的文档将其带到屏幕前面。**提示：** 如果没有打开的文档，访问此属性将引发异常。 |
| `backgroundColor` | `SolidColor` | 读写。文档的默认背景颜色和颜色样式。 |
| `build` | `string` | 只读。关于应用程序的信息。 |
| `colorSettings` | `string` | 读写。当前颜色设置的名称，即通过“编辑 > 颜色设置”所选的名称。 |
| `displayDialogs` | `DialogModes` | 读写。应用程序的对话框模式，控制运行脚本时应显示哪些类型的对话框。 |
| `documents` | `Documents` | 只读。打开的文档集合。这是访问当前在应用程序中打开的文档的主要入口点。数组允许你访问任何打开的文档，或遍历所有打开的文档。 |
| `fonts` | `TextFonts` | 只读。此系统上安装的字体。 |
| `foregroundColor` | `SolidColor` | 读写。默认的前景色（用于绘制、填充和描边选区）。 |
| `freeMemory` | `number` | 只读。Adobe Photoshop CS6 可用的未使用内存量。 |
| `locale` | `string` | 只读。应用程序的语言区域。Adobe 区域代码由一个 2 字母的 ISO-639 语言代码和一个可选的 2 字母的 ISO 3166 国家代码组成，中间用下划线分隔。大小写敏感。例如，`en_US`、`en_UK`、`ja_JP`、`de_DE`、`fr_FR`。 |



| `macintoshFileTypes` | `string` 数组 | 只读。Adobe Photoshop CS6 可以打开的文件图像类型列表。 |
|---|---|---|
| `measurementLog` | `MeasurementLog` | 测量日志。 |
| `name` | `string` | 只读。应用程序的名称。 |
| `notifiers` | `Notifiers` | 只读。当前配置的通知程序集合（在 Adobe Photoshop CS6 应用程序的“脚本事件管理器”菜单中）。 |
| `notifiersEnabled` | `boolean` | 读写。如果所有通知程序都已启用，则为 True。 |
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
| `windowsFileTypes` | `string` 数组 | 只读。Adobe Photoshop CS6 可以打开的文件图像扩展名列表。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `batch(inputFiles, action, from [, options])` | `File` 数组、`string`、`string`、[`BatchOptions`](https://example.com) | `string` | 运行批处理自动化例程（类似于 **文件 > 自动 > 批处理** 命令）。`inputFiles` 参数指定要由批处理命令处理的文件的来源。 |
| `beep()` |  |  | 发出“哔”声。 |
| `bringToFront()` |  |  | 使 Adobe Photoshop CS6 成为活动（最前面的）应用程序。 |
| `charIDToTypeID(charID)` | `string` | `number` | 将四字符代码（字符 ID）转换为运行时 ID。 |
| `doAction(action, from)` | `string`、`string` |  | 从动作调板播放一个动作。`action` 参数是动作的名称，`from` 参数是动作组的名称。 |
| `eraseCustomOptions(key)` | `string` |  | 从 Photoshop 注册表中删除具有指定 ID 值的用户对象。 |
| `executeAction(eventID [, descriptor] [, displayDialogs])` | `number`、[`ActionDescriptor`](https://example.com)、[`DialogModes`](https://example.com) | [`ActionDescriptor`](https://example.com) | 播放一个 Action Manager 事件。 |
| `executeActionGet(reference)` | [`ActionReference`](https://example.com) | [`ActionDescriptor`](https://example.com) | 获取有关预定义或录制动作的信息。 |
| `featureEnabled(name)` | `string` | `boolean` | 确定 `name` 指定的功能是否已启用。以下功能支持作为 `name` 的值：`"photoshop/extended"`、`"photoshop/standard"`、`"photoshop/trial"`。 |

| 方法 | 参数类型 | 返回值 | 描述 |
|---|---|---|---|
| `putObject(classID, value)` | `number`、`ActionDescriptor` |  | 追加一个新值，一个对象。 |
| `putPath(value)` | `File` |  | 追加一个新值，一个路径。 |
| `putReference(value)` | `ActionReference` |  | 追加一个新值，一个引用，指向脚本中创建的对象。 |
| `putString(value)` | `string` |  | 追加一个新值，一个字符串。 |
| `putUnitDouble(classID, value)` | `number`、`number` |  | 追加一个新值，一个单位/值对。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述（续） |
| :--- | :--- | :--- | :--- |
| `getCustomOptions(key)` | `string` | [ActionDescriptor](https://www.example.com) | 在 Photoshop 注册表中，根据键值 `key` 检索用户对象。 |
| `isQuicktimeAvailable()` |  | `boolean` | 如果安装了 Quicktime，则返回 `true`。 |
| `load(document)` | [File](https://www.example.com) |  | 从指定位置加载支持文件（与 Photoshop 图像文档相对）。 |
| `makeContactSheet(inputFiles [, options])` | `array of [File](https://www.example.com)`<br>[ContactSheetOptions](https://www.example.com) | `string` | 在 Adobe Photoshop CS4 中已弃用。 |
| `makePDFPresentation(inputFiles, outputFiles [, options])` | `array of [File](https://www.example.com)`<br>[File](https://www.example.com)<br>[PresentationOptions](https://www.example.com) | `string` | 在 Adobe Photoshop CS4 中已弃用。 |
| `makePhotoGallery(inputFolder, outputFolder [, options])` | [File](https://www.example.com)<br>[File](https://www.example.com)<br>[GalleryOptions](https://www.example.com) | `string` | 在 Adobe Photoshop CS4 中已弃用。 |
| `makePhotomerge(inputFiles)` | `array of [File](https://www.example.com)` | `string` | 在 Adobe Photoshop CS6 中已弃用。请使用提供的脚本：<br>`runphotomergeFromScript = true;`<br>`$.evalFile(app.path + "Presets/Scripts/Photomerge.jsx")`<br>`photomerge.createPanorama(fileList, displayDialog);`<br>将多个文件合并为一个，并需要用户交互。 |
| `makePicturePackage(inputFiles [, options])` | `array of [File](https://www.example.com)`<br>[PicturePackageOptions](https://www.example.com) | `string` | 在 Adobe Photoshop CS4 中已弃用。 |
| `open(document [, as] [, asSmartObject])` | `File` 对象或 `OpenDocumentType`、`boolean` | `Document` | 打开指定的文档。<br>使用可选的 `as` 参数，通过 `OpenDocumentType` 中的常量来指定文件格式；或者，你可以使用以下对象来指定文件格式及其打开选项：<br>- `CameraRAWOpenOptions`<br>- `DICOMOpenOptions`<br>- `EPSOpenOptions`<br>- `PDFOpenOptions`<br>- `PhotoCDOpenOptions`<br>- `RawFormatOpenOptions`<br>使用可选参数 `asSmartObject`（默认值：`false`）可以为打开的文档创建一个智能对象。<br>有关在 `open` 方法中使用 `File` 对象的示例，请参阅 [Application 示例脚本](http://)。 |
| `openDialog()` |  | `array of File` | 调用 Photoshop 的“打开”对话框供用户选择文件。<br>返回一个数组，包含在对话框中选定的 `File` 对象。 |
| `purge(target)` | `PurgeTarget` |  | 清除一个或多个缓存。 |
| `putCustomOptions(key, customObject [, persistent])` | `string`、`ActionDescriptor`、`boolean` |  | 在 Photoshop 注册表中保存一个自定义设置对象。<br>`key` 是你自定义设置的唯一标识符。<br>`customObject` 是要保存到注册表中的对象。<br>`persistent` 指示脚本完成后该对象是否应持久化。 |
| `refresh()` |  |  | 在应用程序刷新时暂停脚本。用于减慢执行速度，以便在脚本运行时向用户显示结果。请谨慎使用；使用此方法时，你的脚本运行速度会慢很多。 |
| `refreshFonts()` |  |  | 强制更新字体列表。 |
| `runMenuItem(menuID)` | `number` |  | 根据菜单 ID 运行一个菜单项。 |
| `showColorPicker()` |  | `boolean` | 如果对话框被取消，则返回 `false`，否则返回 `true`。 |
| `stringIDToTypeID(stringID)` | `string` | `number` | 从字符串 ID 转换为运行时 ID。 |
| `togglePalettes()` |  |  | 切换面板可见性。 |
| `typeIDToCharID(typeID)` | `number` | `string` | 从运行时 ID 转换为字符 ID。 |
| `typeIDToStringID(typeID)` | `number` | `string` | 从运行时 ID 转换为字符串 ID。 |

#### Application 示例脚本

##### Application.jsx

此脚本会调用一个警报框，以显示对应用程序至关重要的属性，例如版本号、应用程序路径、可用内存量以及已打开的文档数量。

当用户按下警报框上的“确定”按钮时，将打开第二个对话框，询问用户是否要为当前打开的文档设置前景色和背景色。如果没有打开任何文档，该脚本会为用户打开一个新文档。

该脚本（在没有打开文档的情况下）会产生三个连续的对话框。

```javascript
// 创建欢迎消息
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

```javascript
// 设置颜色
if (answer) {
    // 我没有首选颜色。你可能会想，我为什么要问？
    app.foregroundColor.rgb.red = Math.random() * 255
    app.foregroundColor.rgb.green = Math.random() * 255
    app.foregroundColor.rgb.blue = Math.random() * 255
    app.backgroundColor.rgb.red = Math.random() * 255
    app.backgroundColor.rgb.green = Math.random() * 255
    app.backgroundColor.rgb.blue = Math.random() * 255
}

// 打开一个文档
if (app.documents.length == 0) {

    // 使用应用程序的路径和到 samples 文件夹的偏移量
    var sampleDocToOpen = File(app.path + "/Samples/Fish.psd")

    // 用文件名组成一条消息
    message = "您想让我为您打开一个示例文件吗？("
    message += sampleDocToOpen.fsName
    message += ")"

    // 再次询问用户一个问题
    answer = confirm(message)

    // 相应地打开文档
    if (answer) {
        open(sampleDocToOpen)
    }
}
```

##### PDFPresentation.jsx

此脚本将一系列图像呈现为 Adobe PDF 幻灯片。

```javascript
// 使用 Samples 文件夹中的所有文件
var inputFolder = new Folder(app.path + "/Samples/")

// 查看是否有有趣的内容
if (inputFolder != null) {

    // 获取此文件夹中找到的所有 Adobe Photoshop CS6 文件（.psd 格式）
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



文档中的一个对象，包含图像的视觉元素（等同于 Adobe Photoshop CS6 应用程序中的图层）。

通过 `Document.artLayers` 集合访问文档中的图层。你可以通过图层名称访问图层；例如：

```javascript
var layerRef = app.activeDocument.artLayers.getByName("my layer");
layerRef.allLocked = true;
```

通过父图层组中的 `LayerSet.artLayers` 集合访问图层组中的图层。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `allLocked` | `boolean` | 可读写。为 `true` 时，完全锁定此图层的内容和设置。 |
| `blendMode` | `BlendMode` | 可读写。混合模式。 |
| `bounds` | `array of UnitValue` | 只读。一个坐标数组，描述图层的边界矩形。 |
| `fillOpacity` | `number [0.0..100]` | 可读写。图层的内部不透明度，为百分比值。 |
| `filterMaskDensity` | `double` | 可读写。滤镜蒙版的密度（介于 0.0 和 250.0 之间）。 |
| `filterMaskFeather` | `double` | 可读写。滤镜蒙版的羽化值（介于 0.0 和 250.0 之间）。 |
| `grouped` | `boolean` | 可读写。如果此图层与其下方的图层编组，则为 `true`。 |
| `isBackgroundLayer` | `boolean` | 可读写。如果这是文档的背景图层，则为 `true`。一个文档只能有一个背景图层。如果没有背景图层，将其设置为 `true` 会使此图层成为背景图层。 |
| `kind` | `LayerKind` | 可读写。为一个空图层设置类型（例如“文字图层”）。仅当图层为空且 `isBackgroundLayer` 为 `false` 时有效。参见 `isBackgroundLayer`。你可以使用 `kind` 属性将背景图层更改为普通图层；但是，要将图层更改为背景图层，必须将 `isBackgroundLayer` 设置为 `true`。 |
| `layerMaskDensity` | `double` | 可读写。图层蒙版的密度（介于 0.0 和 100.0 之间）。 |
| `layerMaskFeather` | `double` | 可读写。图层蒙版的羽化值（介于 0.0 和 250.0 之间）。 |
| `linkedLayers` | `ArtLayer` 或 `LayerSet` 的数组 | 只读。链接到此图层的图层。请参阅 `ArtLayer.link`。 |
| `name` | `string` | 读写。名称。 |
| `opacity` | `number [0.0..100.0]` | 读写。图层的主不透明度，百分比值。 |
| `parent` | `Document` | 只读。对象的容器。 |
| `pixelsLocked` | `boolean` | 读写。如果图层图像中的像素不能使用画笔工具编辑，则为真。 |
| `positionLocked` | `boolean` | 读写。如果图层图像中的像素不能在图层内移动，则为真。 |
| `textItem` | `TextItem` | 只读。与图层关联的文本项。仅在 `kind = LayerKind.TEXT` 时有效。 |
| `transparentPixelsLocked` | `boolean` | 读写。如果编辑仅限于图层的非透明部分，则为真。 |
| `typename` | `string` | 只读。引用的 `artLayer` 对象的类名。 |
| `vectorMaskDensity` | `double` | 读写。矢量蒙版的密度（介于 0.0 和 250.0 之间）。 |
| `vectorMaskFeather` | `double` | 读写。矢量蒙版的羽化值（介于 0.0 和 250.0 之间）。 |
| `visible` | `boolean` | 读写。如果图层可见，则为真。 |
| `xmpMetadata` | `xmpMetadata` | 读写。图层的元数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |
| :--- | :--- | :--- | :--- |
| `adjustBrightnessContrast(brightness, contrast)` | `number`<br>`number` |  | 调整亮度（范围 [-100..100]）和对比度（范围 [-100..100]）。 |
| `adjustColorBalance([shadows][, midtones][, highlights][, preserveLuminosity])` | `number` 的数组<br>`number` 的数组<br>`number` 的数组<br>`boolean` |  | 调整图层各通道的颜色平衡。对于阴影、中间调和高光，数组必须包含三个在范围 [-100..100] 内的值，当文档模式为 CMYK 或 RGB 时，分别代表青色或红色、品红色或绿色、黄色或蓝色。<br><br>请参阅 `Document.mode`。 |
| `adjustCurves(curveShape)` | `number` 的数组的数组 |  | 使用最多 14 个点调整所选通道的色调范围。<br><br>`curveShape` 数组中的每个值都是一个点对，一个由 x 和 y 整数值组成的数组。 |
| `adjustLevels(inputRangeStart, inputRangeEnd, inputRangeGamma, outputRangeStart, outputRangeEnd)` | `number [0..253]`<br>`number [(start + 2)..255]`<br>`number [0.10..9.99]`<br>`number [0..253]`<br>`number [(start + 2)..255]` |  | 调整所选通道的色阶。 |
| `applyAddNoise(amount, distribution, monochromatic)` | `number [0.1..400]`<br>`NoiseDistribution`<br>`boolean` |  | 应用“添加杂色”滤镜。`amount` 是百分比值。 |
| `applyAverage()` |  |  | 应用“平均值”滤镜。 |
| `applyBlur()` |  |  | 应用“模糊”滤镜。 |
| `applyBlurMore()` |  |  | 应用“进一步模糊”滤镜。 |
| `applyClouds()` |  |  | 应用“云彩”滤镜。 |
| `applyCustomFilter(characteristics, scale, offset)` | `number` 的数组<br>`number`<br>`number` |  | 应用自定义滤镜。<br>`characteristics` 数组有 25 个成员。<br><br>具体说明请参阅 Adobe Photoshop CS6 帮助。 |
| `applyDeInterlace(eliminateFields, createFields)` | `EliminateFields`<br>`CreateFields` |  | 应用“逐行”滤镜。 |
| `applyDespeckle()` |  |  | 应用“蒙尘与划痕”滤镜。 |
| `applyDifferenceClouds()` |  |  | 应用“分层云彩”滤镜。 |
| `applyDiffuseGlow(graininess, glowAmount, clearAmount)` | `number [0..10]`<br>`number [0..20]`<br>`number [0..20]` |  | 应用“扩散亮光”滤镜。 |
| `applyDisplace(horizontalScale, verticalScale, displacement, undefinedareas, displacementMapFiles)` | `number [-999..999]`<br>`number [-999..999]`<br>`DisplacementMapType`<br>`UndefinedAreas`<br>`File` |  | 应用“置换”滤镜，使用指定的水平和垂直缩放、映射类型、未扭曲区域的处理方式以及扭曲图像映射的路径。 |
| `applyDustAndScratches(radius, threshold)` | `number [1..100]`<br>`number [0..255]` |  | 应用“蒙尘与划痕”滤镜。 |
| `applyGaussianBlur(radius)` | `number [0.1..250.0]` |  | 在指定的半径（以像素为单位）内应用“高斯模糊”滤镜。 |
| `applyGlassEffect(distortion, smoothness, scaling [, invert] [, texture] [, textureFile])` | `number [0..20]`<br>`number [1..15]`<br>`number [50..200]`<br>`boolean`<br>`TextureType`<br>`File` |  | 应用“玻璃”滤镜。`scaling` 是百分比值。 |
| `applyHighPass(radius)` | `number [0.1..250.0]` |  | 在指定的半径内应用“高反差保留”滤镜。 |
| `applyLensBlur([source][, focalDistance][, invertDepthMap][, shape][, radius][, bladeCurvature][, rotation][, brightness][, threshold][, amount][, distribution][, monochromatic])` | `DepthMapSource`<br>`number`<br>`boolean`<br>`Geometry`<br>`number`<br>`number`<br>`number`<br>`number`<br>`number`<br>`number`<br>`NoiseDistribution`<br>`boolean` |  | 应用“镜头模糊”滤镜。<br>`source`：深度贴图的来源（默认：`DepthMapSource.NONE`）。<br>`focalDistance`：深度贴图的模糊焦距（默认：0）。<br>`invertDepthMask`：如果深度贴图反转则为真（默认：`false`）。<br>`shape`：光圈的形状（默认：`Geometry.HEXAGON`）。<br>`radius`：光圈的半径（默认：15）。<br>`bladeCurvature`：光圈叶片的曲率（默认：0）。<br>`rotation`：光圈的旋转（默认：0）。<br>`brightness`：镜面高光的亮度（默认：0）。<br>`threshold`：镜面高光的阈值（默认：0）。<br>`amount`：杂色的数量（默认：0）。<br>`distribution`：杂色的分布值（默认：`NoiseDistribution.UNIFORM`）。<br>`monochromatic`：如果杂色为单色则为真（默认：`false`）。 |
| `applyLensFlare(brightness, flareCenter, lensType)` | `number`<br>`array(UnitValue)`<br>`LensType` |  | 应用“镜头光晕”滤镜，指定亮度（0 - 300，作为百分比）、光晕中心的 x 和 y 坐标（单位值）以及镜头类型。 |
| `applyMaximum(radius)` | `number [1..100]` |  | 在指定的半径（以像素为单位）内应用“最大值”滤镜。 |
| `applyMedianNoise(radius)` | `number [1..100]` |  | 在指定的半径（以像素为单位）内应用“中间值”滤镜。 |
| `applyMinimum(radius)` | `number [1..100]` |  | 在指定的半径（以像素为单位）内（1 - 100）应用“最小值”滤镜。 |
| `applyMotionBlur(angle, radius)` | `number [-360..360]`<br>`number [1..999]` |  | 应用“动感模糊”滤镜。 |
| `applyNTSC()` |  |  | 应用“NTSC 颜色”滤镜。 |
| `applyOceanRipple(size, magnitude)` | `number [1..15]`<br>`number [0..20]` |  | 应用“海洋波纹”滤镜。 |
| `applyOffset(horizontal, vertical, undefinedAreas)` | `UnitValue`<br>`UnitValue`<br>`OffsetUndefinedAreas` |  | 将图层水平移动和垂直移动指定的量（最小/最大量取决于图层大小），在图层的原始位置留下一个未定义区域。 |
| `applyPinch(amount)` | `number [-100..100]` |  | 应用“挤压”滤镜。`amount` 是百分比值。 |
| `applyPolarCoordinates(conversion)` | `PolarConversionType` |  | 应用“极坐标”滤镜。 |
| `applyRadialBlur(amount, blurMethod, blurQuality)` | `number [1..100]`<br>`RadialBlurMethod`<br>`RadialBlurQuality` |  | 以指定的数量应用“径向模糊”滤镜，使用旋转或缩放效果以及指定的质量。 |
| `applyRipple(amount, size)` | `number [-999..999]`<br>`RippleSize` |  | 以指定的数量、在整个图像中以及指定的大小应用“波纹”滤镜。 |
| `applySharpen()` |  |  | 应用“锐化”滤镜。 |
| `applySharpenEdges()` |  |  | 应用“锐化边缘”滤镜。 |
| `applySharpenMore()` |  |  | 应用“进一步锐化”滤镜。 |
| `applyShear(curve, undefinedAreas)` | `number` 的数组的数组<br>`UndefinedAreas` |  | 应用“切变”滤镜。曲线定义了一条包含 [2..255] 个点的曲线。曲线数组中的每个值都是一个点对，一个由 x 和 y 整数值组成的数组。 |

### ArtLayer 方法参考

| 方法 | 参数类型 | 返回值 | 功能说明（续） |
| :--- | :--- | :--- | :--- |
| `applySmartBlur(radius, threshold, blurQuality, mode)` | `number [0.1..100.0]`<br>`number [0.1..100.0]`<br>`[SmartBlurQuality](SmartBlurQuality.md)`<br>`[SmartBlurMode](SmartBlurMode.md)` |  | 应用智能模糊滤镜。 |
| `applySpherize(amount, mode)` | `number [-100..100]`<br>`[SpherizeMode](SpherizeMode.md)` |  | 应用球面化滤镜。`amount` 是百分比值。 |
| `applyStyle(styleName)` | `string` |  | 将指定样式应用到图层。你必须使用图层样式面板中样式列表中的样式。 |
| `applyTextureFill(textureFile)` | `[File](File.md)` |  | 应用纹理填充滤镜。 |
| `applyTwirl(angle)` | `number [-999..999]` |  | 应用旋转扭曲滤镜。 |
| `applyUnSharpMask(amount, radius, threshold)` | `number [1..500]`<br>`number [0.1..250.0]`<br>`number [0..255]` |  | 应用 USM 锐化滤镜。`amount` 是百分比值。 |
| `applyWave(generatorNumber, minimumWavelength, maximumWavelength, minimumAmplitude, maximumAmplitude, horizontalScale, verticalScale, waveType, undefinedAreas, randomSeed)` | `number [1..999]`<br>`number [1..998]`<br>`number [2..min+1]`<br>`number [1..998]`<br>`number [2..min+1]`<br>`number [1..100]`<br>`number [1..100]`<br>`[WaveType](WaveType.md)`<br>`[UndefinedAreas](UndefinedAreas.md)`<br>`number` |  | 应用波浪滤镜。缩放因子是百分比值。 |
| `applyZigZag(amount, ridges, style)` | `number [-100..100]`<br>`number [0..20]`<br>`[ZigZagType](ZigZagType.md)` |  | 应用水波滤镜。 |
| `autoContrast()` |  |  | 自动调整选中通道的对比度。 |
| `autoLevels()` |  |  | 使用自动色阶选项调整选中通道的色阶。 |
| `clear()` |  |  | 裁切图层而不将其移动到剪贴板。 |



| `copy`([merge]) | boolean | | 将图层复制到剪贴板。当可选参数设置为 `true` 时，执行合并复制（即，所有可见图层都被复制到剪贴板）。 |
| `cut`() | | | 将图层裁切到剪贴板。 |
| `desaturate`() | | | 通过为每个像素分配相等的各分量颜色值，在当前颜色模式下将彩色图像转换为灰度图像。 |
| `duplicate`([relativeObject][, insertionLocation]) | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) or [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/)<br>[ElementPlacement](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) or [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | 创建屏幕上对象的副本。 |
| `equalize`() | | | 重新分布图像中像素的亮度值，以更均匀地表示图像内整个亮度级别的范围。 |
| `invert`() | | | 通过将通道中每个像素的亮度值转换为 256 级颜色值刻度上的反值，来反转图层中的颜色。 |
| `link`(with) | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) or [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | | 将图层与指定图层链接。 |
| `merge`() | | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/) | 向下合并图层，从文档中移除该图层；返回对该图层合并到的艺术图层的引用。 |
| `mixChannels`(outputChannels[, monochrome]) | array of array of number<br>boolean | | 使用图像中现有颜色通道的混合来修改目标（输出）颜色通道。<br><br>`outputChannels` 参数是一个通道规范数组。对于每个分量通道，指定范围 [-200..200] 内的调整值列表，后跟一个“常量”值 [-200..200]）。<br><br>当 `monochrome` = `true` 时，通道值规范的最大数量为 1。<br><br>仅在 `docRef.mode` = `DocumentMode.RGB` 或 `CMYK` 时有效。<br>RGB 数组必须包含四个值。CMYK 数组必须包含五个值。 |
| `move`(relativeObject, insertionLocation) | ArtLayer or LayerSet<br>ElementPlacement | | 将图层相对于参数中指定的对象移动。<br>对于艺术图层，仅常量值 `ElementPlacement.PLACEBEFORE` 和 `PLACEAFTER` 有效。<br>对于图层组，仅常量值 `ElementPlacement.PLACEBEFORE` 和 `INSIDE` 有效。 |
| `photoFilter`([fillColor][, density][, preserveLuminosity]) | SolidColor<br>number [1..100]<br>boolean | | 调整图层的色彩平衡和温度，就像应用了颜色滤镜一样。<br><br>`density` 是百分比值。 |
| `posterize`(levels) | number [2..225] | | 指定每个通道的色调级别数，然后将像素映射到最接近的匹配级别。 |
| `rasterize`(target) | RasterizeType | | 将图层中的目标内容转换为平面的栅格图像。 |
| `remove`() | | | 删除对象。 |
| `resize`([, horizontal][, vertical][, anchor]) | number<br>number<br>AnchorPosition | | 将图层调整为指定的尺寸（作为其当前大小的百分比）并将其放置在指定位置。 |
| `rotate`(angle[, anchor]) | number<br>AnchorPosition | | 围绕指定的锚点旋转图层（默认：MIDDLECENTER）。 |
| `selectiveColor`(selectionMethod[, reds][, yellows][, greens][, cyans][, blues][, magentas][, whites][, neutrals][, blacks]) | AdjustmentReference<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number<br>array of number | | 修改指定原色中某种印刷色的量而不影响其他原色。<br>每个颜色数组必须有四个值。 |
| `shadowHighlight`([shadowAmount][, shadowWidth][, shadowRadius][, highlightAmount][, highlightWidth][, highlightRadius][, colorCorrection][, midtoneContrast][, blackClip][, whiteClip]) | number [0..100]<br>number [0..100]<br>number [0..2500]<br>number [0..100]<br>number [0..100]<br>number [0..2500]<br>number [-100..100]<br>number [-100..100]<br>number [0.000..50.000]<br>number [0.000..50.000] | | 调整图像阴影和高光中的色调范围。<br>数量和宽度是百分比值。半径值以像素为单位。 |
| `threshold`(level) | number [1..255] | | 通过将比指定阈值亮的像素转换为白色，比阈值暗的像素转换为黑色，将灰度或彩色图像转换为高对比度的黑白图像。 |
| `translate`([deltaX][, deltaY]) | UnitValue<br>UnitValue | | 将图层相对于其当前位置移动指定的量（以给定的单位）。 |
| `unlink`() | | | 取消图层的链接。 |

#### ArtLayer 示例脚本

以下脚本打开示例文件夹中的所有文件，创建一个多图层文档。每个图层被粘贴到四个象限之一，并设置为 50% 的不透明度。最后，图层按名称排序。

`ArtLayer.jsx`

```javascript
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CS6 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

//Close all the open documents
while (app.documents.length) {
    app.activeDocument.close()
}

// Create a new document to merge all the samples into
var mergedDoc = app.documents.add(1000, 1000, 72, "Merged Samples",
    NewDocumentMode.RGB, DocumentFill.TRANSPARENT, 1)

// Use the path to the application and append the samples folder
var samplesFolder = Folder(app.path + "/Samples/")

//Get all the files in the folder
var fileList = samplesFolder.getFiles()

// open each file
for (var i = 0; i < fileList.length; i++) {
    // The fileList is folders and files so open only files
    if (fileList[i] instanceof File) {
        open(fileList[i])

        // use the document name for the layer name in the merged document
        var docName = app.activeDocument.name

        // flatten the document so we get everything and then copy
        app.activeDocument.flatten()
        app.activeDocument.selection.selectAll()
        app.activeDocument.selection.copy()

        // don't save anything we did
        app.activeDocument.close(SaveOptions.DONOTSAVECHANGES)

        // make a random selection on the document to paste into
        // by dividing the document up in 4 quadrants and pasting
        // into one of them by selecting that area
        var topLeftH = Math.floor(Math.random() * 2)
        var topLeftV = Math.floor(Math.random() * 2)
        var docH = app.activeDocument.width.value / 2
        var docV = app.activeDocument.height.value / 2
        var selRegion = Array(Array(topLeftH * docH, topLeftV * docV),
            Array(topLeftH * docH + docH, topLeftV * docV),
            Array(topLeftH * docH + docH, topLeftV * docV + docV),
            Array(topLeftH * docH, topLeftV * docV + docV))
        app.activeDocument.selection.select(selRegion)
        app.activeDocument.paste()

        // change the layer name and opacity
        app.activeDocument.activeLayer.name = docName
        app.activeDocument.activeLayer.fillOpacity = 50
    }
}
```

```javascript
}

// 按名称对图层进行排序
for (var x = 0; x < app.activeDocument.layers.length; x++) {
    for (var y = 0; y < app.activeDocument.layers.length - 1 - x; y++) {
        // 以不区分大小写的方式进行比较
        var doc1 = app.activeDocument.layers[y].name
        var doc2 = app.activeDocument.layers[y + 1].name
        if (doc1.toUpperCase() > doc2.toUpperCase()) {
            app.activeDocument.layers[y].move(app.activeDocument.layers[y+1],
                ElementPlacement.PLACEAFTER)
        }
    }
}

// 重置应用程序首选项
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.displayDialogs = startDisplayDialogs
```

### ArtLayers

文档或图层集中的 `ArtLayer` 对象集合。

通过 [`Document.artLayers`](http://example.com) 或 [`LayerSet.artLayers`](http://example.com) 集合进行访问。例如：

```javascript
var layerRef = docRef.artLayers.add()
```

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `length` | 数字 | 只读。`artLayers` 集合中的元素数量。 |
| `parent` | Document | 只读。对象的容器。 |
| `typename` | 字符串 | 只读。所引用 `artLayers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| --- | --- | --- | --- |
| `add`() | | ArtLayer | 在文档中创建一个新的艺术图层，并将新对象添加到此集合中。 |
| `getByName`(name) | 字符串 | ArtLayer | 获取 `artLayers` 集合中具有所提供名称的第一个元素。 |
| `removeAll`() | | | 从 `artLayers` 集合中移除所有元素。 |

### BatchOptions

使用 `Application.batch()` 方法运行批处理操作的选项。

JavaScript 仅支持文件夹作为批处理命令的源。请将批处理源文件夹指定为 `Application.batch()` 方法的 `inputFiles` 参数。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `destination` | BatchDestinationType | 读写。已处理文件的目标类型（默认：`BatchDestinationType.NODESTINATION`）。 |
| `destinationFolder` | Folder | 读写。已处理文件的文件夹位置。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `errorFile` | File | 读写。用于记录遇到错误的文件。<br><br>要将错误显示在屏幕上（并在发生错误时停止批处理），请留空。 |
| `fileNaming` | FileNamingType 数组 | 读写。文件命名选项列表（最大值：6）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `macintoshCompatible` | 布尔值 | 读写。设为 `true` 以使最终文件名与 Macintosh 兼容（默认：`true`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `overrideOpen` | 布尔值 | 读写。设为 `true` 以覆盖动作打开命令（默认：`false`）。 |



| `overrideSave` | 布尔值 | 读写。设为 `true` 以使用指定的目标覆盖“存储为”动作步骤（默认：`false`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 或 `SAVEANDCLOSE` 时有效。 |
| `startingSerial` | 数字 | 读写。用于命名文件的起始序列号（默认：`1`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `suppressOpen` | 布尔值 | 读写。设为 `true` 以抑制文件打开选项对话框（默认：`false`）。 |
| `suppressProfile` | 布尔值 | 读写。设为 `true` 以抑制颜色配置文件警告（默认：`false`）。 |
| `typename` | 字符串 | 只读。所引用 `batchOptions` 对象的类名。 |
| `unixCompatible` | 布尔值 | 读写。设为 `true` 以使最终文件名与 Unix 兼容（默认：`true`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `windowsCompatible` | 布尔值 | 读写。设为 `true` 以使最终文件名与 Windows 兼容（默认：`true`）。<br><br>仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |

### BitmapConversionOptions

使用 [Document.changeMode()](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#Document.changeMode) 和 [ChangeMode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#ChangeMode).Bitmap 将图像转换为位图模式的选项。

在将图像转换为位图模式之前，请先将彩色图像转换为灰度。请参阅 [ArtLayer.desaturate()](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#ArtLayer.desaturate) 方法。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `angle` | `数字 [-180..180]` | 读写。用于定位单个点的角度（以度为单位）。请参阅 [shape](#shape)。仅当 [method](#method) = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `frequency` | `数字 [1.0..999.99]` | 读写。要使用的打印机点数（每英寸）。仅当 [method](#method) = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `method` | [BitmapConversionType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#BitmapConversionType) | 读写。要使用的转换方法（默认：`BitmapConversionType.DIFFUSIONDITHER`）。 |
| `patternName` | `字符串` | 读写。要使用的图案名称。有关预装的有效图案信息，请参阅 Adobe Photoshop CS6 帮助中的位图转换命令，或查看选择位图转换命令后“自定义颜色”下拉框中可用的选项。仅当 [method](#method) = `BitmapConversionType.CUSTOMPATTERN` 时有效。 |
| `resolution` | `数字` | 读写。输出分辨率，单位为每英寸像素数（默认：`72.0`）。 |
| `shape` | [BitmapHalfToneType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#BitmapHalfToneType) | 读写。要使用的点形状。仅当 [method](#method) = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `typename` | `字符串` | 只读。所引用 `bitmapConversionOptions` 对象的类名。 |

### BMPSaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法以 BMP 格式保存文档的选项。

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

使用 [Application.open()](Application.open()) 方法打开 Camera RAW 格式文档的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `bitsPerChannel` | [BitsPerChannelType](BitsPerChannelType) | 读写。每通道的位数。 |
| `blueHue` | 数字 `[-100..100]` | 读写。拍摄图像的蓝色色相。 |
| `blueSaturation` | 数字 `[-100..100]` | 读写。拍摄图像的蓝色饱和度。 |
| `brightness` | 数字 `[0..150]` | 读写。拍摄图像的亮度。 |
| `chromaticAberrationBY` | 数字 `[-100..100]` | 读写。拍摄图像的色差 B/Y。 |
| `chromaticAberrationRC` | 数字 `[-100..100]` | 读写。拍摄图像的色差 R/C。 |
| `colorNoiseReduction` | 数字 `[0..100]` | 读写。拍摄图像的彩色噪点消减。 |
| `colorSpace` | [ColorSpaceType](ColorSpaceType) | 读写。图像的色彩空间。 |
| `contrast` | 数字 `[-50..100]` | 读写。拍摄图像的对比度。 |
| `exposure` | 数字 `[-4.0..4.0]` | 读写。拍摄图像的曝光度。 |
| `greenHue` | 数字 `[-100..100]` | 读写。拍摄图像的绿色色相。 |
| `greenSaturation` | 数字 `[-100..100]` | 读写。拍摄图像的绿色饱和度。 |
| `luminanceSmoothing` | 数字 `[0..100]` | 读写。拍摄图像的亮度平滑。 |
| `redHue` | 数字 `[-100..100]` | 读写。拍摄图像的红色色相。 |
| `redSaturation` | 数字 `[-100..100]` | 读写。拍摄图像的红色饱和度。 |
| `resolution` | 数字 `[1..999]` | 读写。文档的分辨率，单位为每英寸像素数。 |
| `saturation` | 数字 `[-100..100]` | 读写。拍摄图像的饱和度。 |
| `settings` | [CameraRAWSettingsType](CameraRAWSettingsType) | 读写。所有 Camera RAW 选项的全局设置。默认：`CameraRAWSettingsType.CAMERA`。 |
| `shadows` | 数字 `[0..100]` | 读写。拍摄图像的阴影。 |
| `shadowTint` | 数字 `[-100..100]` | 读写。拍摄图像的阴影色调。 |
| `sharpness` | 数字 `[0..100]` | 读写。拍摄图像的锐度。 |
| `size` | [CameraRAWSize](CameraRAWSize) | 读写。新文档的尺寸。 |
| `temperature` | 数字 `[2000..50000]` | 读写。拍摄图像的色温。 |

### 通道

关于图像中颜色元素的信息。

可通过 [Document.channels](/ref/model/Document.html#channels) 集合访问。你可以通过索引或名称访问此列表中的单个通道对象。例如，以下代码通过名称访问活动文档中的一个通道对象，并为其分配一个 `opacity` 值：

```javascript
var channelRef = app.activeDocument.channels.getByName("my channel");

channelRef.opacity = 22;
```

通道类似于印刷过程中应用单一颜色的印版。文档的颜色模式决定了默认通道的数量；例如，RGB 文档有三个通道：红色、绿色和蓝色。颜色还可以有一个 Alpha 通道，用于以蒙版形式存储选区；或一个专色通道，用于存储专色。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `color` | [SolidColor](/ref/model/SolidColor.html) | 可读写。通道的颜色。<br><br>当 `kind` = `ChannelType.COMPONENT` 时无效。 |
| `histogram` | `number` 数组 | 只读。通道颜色的直方图。该数组包含 256 个成员。<br><br>当 `kind` = `ChannelType.COMPONENT` 时无效。有关复合通道的直方图值，请改用 [Document](/ref/model/Document.html) 对象的 [histogram](/ref/model/Document.html#histogram) 属性。 |
| `kind` | [ChannelType](/ref/enum/ChannelType.html) | 可读写。通道的类型。 |
| `name` | `string` | 可读写。通道的名称。 |
| `opacity` | `number [0..100]` | 可读写。Alpha 通道使用的不透明度或专色通道使用的密度。<br><br>仅当 `kind` = `ChannelType.MASKEDAREA` 或 `SELECTEDAREA` 时有效。 |
| `parent` | [Document](/ref/model/Document.html) | 只读。包含此通道的文档。 |
| `typename` | `string` | 只读。引用的通道对象的类名。 |
| `visible` | `boolean` | 可读写。如果通道可见则为 `true`。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `duplicate([targetDocument])` | [Document](/ref/model/Document.html) | [Channel](/ref/model/Channel.html) | 复制通道。 |
| `merge()` | | | 将专色通道合并到复合通道中。 |
| `remove()` | | | 删除通道。 |

### 通道集合

文档中的通道对象集合。

通过 `Document.channels` 集合属性访问。例如：

```javascript
var channelRef = app.activeDocument.channels.add();
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。通道集合中的元素数量。 |
| `parent` | `Document` | 只读。包含此集合的文档。 |
| `typename` | `string` | 只读。引用的通道集合对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `add()` | | `Channel` | 创建一个新的通道对象并将其添加到此集合中。 |
| `getByName(name)` | `string` | `Channel` | 根据提供的名称获取通道集合中的第一个元素。 |
| `removeAll()` | | | 从通道集合中移除所有 Alpha 通道对象。 |

#### 通道集合示例脚本

以下脚本在未打开任何文件时打开一个文件，然后为活动文档中的通道写入直方图报告（`histogram.log`）。

**注意：** 此脚本包含一个使用 `break` 语句的 `switch` 结构。`break` 语句需要一个结束分号（`;`），如下例所示：

```javascript
break;
```

**Histogram.jsx**

```javascript
// Function to activate all the channels according to the documents mode

// Takes a document reference for input

function TurnOnDocumentHistogramChannels(inDocument) {

    // see how many channels we need to activate

    var visibleChannelCount = 0

    // based on the mode of the document

    switch (inDocument.mode) {

        case DocumentMode.BITMAP:

        case DocumentMode.GRAYSCALE:

        case DocumentMode.INDEXEDCOLOR:

            visibleChannelCount = 1

            break;

        case DocumentMode.DUOTONE:

            visibleChannelCount = 2

            break;

        case DocumentMode.RGB:

        case DocumentMode.LAB:

            visibleChannelCount = 3

            break;

        case DocumentMode.CMYK:

            visibleChannelCount = 4

            break;

        case DocumentMode.MULTICHANNEL:

        default:

            visibleChannelCount = inDocument.channels.length + 1

            break;

    }

    // now get the channels to activate into a local array

    var aChannelArray = new Array()

    // index for the active channels array

    var aChannelIndex = 0

    for(var channelIndex = 0; channelIndex < inDocument.channels.length;

            channelIndex++) {

        if (channelIndex < visibleChannelCount) {

            aChannelArray[aChannelIndex++] = inDocument.channels[channelIndex]

        }

    }

    // now activate them

    inDocument.activeChannels = aChannelArray

}

// Save the current preferences

var startRulerUnits = app.preferences.rulerUnits

var startTypeUnits = app.preferences.typeUnits

var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CS6 to use pixels and display no dialogs

app.preferences.rulerUnits = Units.PIXELS
```



```javascript
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

if (
    docRef.mode == DocumentMode.RGB ||
    docRef.mode == DocumentMode.INDEXEDCOLOR ||
    docRef.mode == DocumentMode.CMYK
) {
    // activate the main channels so we can get the documents histogram

    TurnOnDocumentHistogramChannels(docRef)

    // Output the documents histogram

    OutputHistogram(docRef.histogram, "Luminosity", fileOut)
}

// local reference to work from

var myChannels = docRef.channels

// loop through each channel and output the histogram

for (
    var channelIndex = 0;
    channelIndex < myChannels.length;
    channelIndex++
) {
    // the channel has to be visible to get a histogram

    myChannels[channelIndex].visible = true

    // turn off all the other channels

    for (
        var secondaryIndex = 0;
        secondaryIndex < myChannels.length;
        secondaryIndex++
    ) {
        if (channelIndex != secondaryIndex) {
            myChannels[secondaryIndex].visible = false
        }
    }

    // Use the function to dump the histogram

    OutputHistogram(
        myChannels[channelIndex].histogram,
        myChannels[channelIndex].name,
        fileOut
    )
}

// close down the output file

fileOut.close()

alert("Histogram file saved to: " + fileOut.fsName)

// reset the active channels

docRef.activeChannels = myActiveChannels

// Reset the application preferences

app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.displayDialogs = startDisplayDialogs

// Utility function that takes a histogram and name

// and dumps to the output file

function OutputHistogram(inHistogram, inHistogramName, inOutFile) {
    // find ouch which count has the largest number

    // I scale everything to this number for the output

    var largestCount = 0

    // a simple indexer I can reuse

    var histogramIndex = 0

    // see how many samples we have total

    var histogramCount = 0

    // search through all and find the largest single item

    for (
        histogramIndex = 0;
        histogramIndex < inHistogram.length;
        histogramIndex++
    ) {
        histogramCount += inHistogram[histogramIndex]

        if (inHistogram[histogramIndex] > largestCount) {
            largestCount = inHistogram[histogramIndex]
        }
    }

    // These should match

    if (histogramCount != totalCount) {
        alert("Something bad is happening!")
    }

    // see how much each "X" is going to count as

    var pixelsPerX = largestCount / 100

    // output this data to the file

    inOutFile.write("One X = " + pixelsPerX + " pixels.\n")

    // output the name of this histogram

    inOutFile.write(inHistogramName + "\n")

    // loop through all the items and output in the following format

    // 001

    // 002

    for (
        histogramIndex = 0;
        histogramIndex < inHistogram.length;
        histogramIndex++
    ) {
        // I need an extra "0" for this line item to keep everything in line

        if (histogramIndex < 10) {
            inOutFile.write("0")
        }

        if (histogramIndex < 100) {
            inOutFile.write("0")
        }

        inOutFile.write(histogramIndex + "\t")

        // calculate the number of Xs to output

        var xCount = Math.round(
            inHistogram[histogramIndex] / pixelsPerX
        )

        // output the Xs

        for (var xIndex = 0; xIndex < xCount; xIndex++) {
            inOutFile.write("X")
        }

        // end the line

        inOutFile.write("\n")
    }
}
```

---

### `cameraRAWOpenOptions` 属性（续）

| 属性 | 值类型 | 说明 |
|---|---|---|
| `tint` | `number [-150..150]` | 可读写。拍摄的色调。 |
| `typename` | `string` | 只读。引用的 `cameraRAWOpenOptions` 对象的类名。 |
| `vignettingAmount` | `number [-100..100]` | 可读写。拍摄的晕影量。 |
| `vignettingMidpoint` | `number [-100..100]` | 可读写。拍摄的晕影中点。 |
| `whiteBalance` | `WhiteBalanceType` | 可读写。图像的白平衡选项。这些是影响色彩平衡的光照条件。 |

```javascript
// 这一行需要额外加一个“0”来保持格式对齐
if (histogramIndex < 100) {
    inOutFile.write("0")
}

// 将索引输出到文件
inOutFile.write(histogramIndex)

// 添加一些空格使其更美观
inOutFile.write(" ")

// 计算需要多少个 X
var outputX = inHistogram[histogramIndex] / largestCount * 100

// 输出 X
for (var a = 0; a < outputX; a++) {
    inOutFile.write("X")
}

inOutFile.write("\n")
}

inOutFile.write("\n")
}
```

### `CMYKColor`

定义 CMYK 颜色，用于 `SolidColor` 对象。

另请参阅 `GrayColor`、`HSBColor`、`LabColor`、`NoColor`、`RGBColor`。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `black` | `number [0.0..100.00]` | 读写。黑色值（百分比）。 |
| `cyan` | `number [0.0..100.00]` | 读写。青色值（百分比）。 |
| `magenta` | `number [0.0..100.00]` | 读写。洋红色值（百分比）。 |
| `typename` | `string` | 只读。所引用的 `CMYKColor` 对象的类名。 |
| `yellow` | `number [0.0..100.00]` | 读写。黄色值（百分比）。 |

### `ColorSampler`

文档的颜色采样器。通过 [`Document.colorSamplers`](https://example.com) 集合访问。例如：

```javascript
var colorSamplerRef = app.activeDocument.colorSamplers[0]
var currentColor = colorSamplerRef.color
```

> **注意：**有关颜色采样器的更多信息，请参阅 Adobe Photoshop CS6 帮助中的颜色采样器工具。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `color` | [`SolidColor`](https://example.com) | 只读。颜色采样器的颜色。 |
| `position` | [`UnitValue`](https://example.com) 数组 | 只读。颜色采样器在文档中的位置。数组 (x,y) 表示计数项目的水平和垂直位置。 |
| `parent` | [`Document`](https://example.com) | 只读。包含文档。 |
| `typename` | `string` | 只读。所引用的 `ColorSampler` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `move(position)` | [`UnitValue`](https://example.com) 数组 |  | 将颜色采样器移动到文档中的新位置。参数 `position (x,y)` 表示移动后颜色采样器的新水平和垂直位置。 |
| `remove()` |  |  | 删除 `ColorSampler` 对象。 |

### `ColorSamplers`

文档中 [`ColorSampler`](https://example.com) 对象的集合。通过 [`Document.colorSamplers`](https://example.com) 集合属性访问。例如：

```javascript
app.activeDocument.colorSamplers.removeAll()
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
| `removeAll()` |  |  | 从 `ColorSamplers` 集合中移除所有 `ColorSampler` 对象。 |

### ContactSheetOptions

使用 [Application.makeContactSheet()](https://example.com) 方法创建联系表的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `acrossFirst` | `boolean` | 读写。为 true 则水平（从左到右，然后从上到下）放置图像（默认：`true`）。 |
| `bestFit` | `boolean` | 读写。为 true 则旋转图像以获得最佳适应效果（默认：`false`）。 |
| `caption` | `boolean` | 读写。为 true 则使用文件名作为图像的说明文字（默认：`true`）。 |
| `columnCount` | `number [1..100]` | 读写。要包含的列数（默认：`5`）。 |
| `flatten` | `boolean` | 读写。为 true 则展平最终文档中的所有图层（默认：`true`）。 |
| `font` | `GalleryFontType` | 读写。用于说明文字的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number` | 读写。说明文字的字体大小（默认：`12`）。 |
| `height` | `number [0..29000]` | 读写。生成文档的高度（像素）（默认：`720`）。 |
| `horizontal` | `number` | 读写。图像之间的水平间距（像素）（默认：`1`）。 |
| `mode` | `NewDocumentMode` | 读写。文档颜色模式（默认：`NewDocumentMode.RGB`）。 |
| `resolution` | `number [35..1200]` | 读写。文档的分辨率（像素/英寸）（默认：`72.0`）。 |
| `rowCount` | `number [1..100]` | 读写。要使用的行数（默认：`6`）。 |
| `typename` | `string` | 只读。所引用的 `contactSheetOptions` 对象的类名。 |
| `useAutoSpacing` | `boolean` | 读写。为 true 则自动调整图像间距（默认：`true`）。 |
| `vertical` | `number [0..29000]` | 读写。图像之间的垂直间距（像素）（默认：`1`）。<br><br>仅在 `useAutoSpacing` = `false` 时有效。 |
| `width` | `number [100..29000]` | 读写。生成文档的宽度（像素）（默认：`576`）。 |

### CountItem

文档中的计数项目。通过 `Document.countItems` 集合访问。另请参阅 `Document.autoCount()` 方法。

**注意：**此功能仅在扩展版中可用。

有关计数项目的更多信息，请参阅 Adobe Photoshop CS6 帮助中的计数工具。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `position` | `UnitValue` 数组 | 只读。计数项目在文档中的位置。 |
| `parent` | `Document` | 只读。包含文档。 |
| `typename` | `string` | 只读。所引用的 `CountItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `remove()` |  |  | 删除 `CountItem` 对象。 |

### CountItems

文档中 [CountItem](CountItem) 对象的集合。

通过 [Document.countItems](Document) 集合属性访问。例如：

```javascript
app.activeDocument.countItems.removeAll()
```




**注意：**此功能仅在扩展版中可用。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `length` | number | 只读。`CountItems` 集合中的元素数量。 |
| `parent` | [Document](Document) | 只读。包含文档。 |
| `typename` | string | 只读。所引用的 `CountItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `add(position)` | [UnitValue](UnitValue) 数组 | [CountItem](CountItem) | 创建一个新的计数项目对象并将其添加到此集合中。<br>参数 `position` (x,y) 分别表示 `CountItem` 对象的水平和垂直位置。 |
| `getByName(name)` | string | [CountItem](CountItem) | 获取 `CountItems` 集合中具有指定名称的第一个元素。 |
| `removeAll()` | | | 从 `CountItems` 集合中移除所有 `CountItem` 对象。 |

## DCS1_SaveOptions

使用 `Document.saveAs()` 方法将 CMYK 文档保存为 DCS1 格式的选项。

### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `dcs` | `DCSType` | 读写。（默认：`DCSType.COLORCOMPOSITE`）。 |
| `embedColorProfile` | boolean | 读写。为 true 则在文档中嵌入颜色配置文件。 |
| `encoding` | `SaveEncoding` | 读写。文档使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | boolean | 读写。为 true 则包含半调网屏（默认：false）。 |
| `interpolation` | boolean | 读写。为 true 则使用图像插值（默认：false）。 |
| `preview` | `Preview` | 读写。预览类型（默认：`Preview.MACOSEIGHTBIT`）。 |
| `transferFunction` | boolean | 读写。为 true 则包含传输函数，以补偿图像和胶片之间的网点增大（默认：false）。 |
| `typename` | string | 只读。所引用的 `DCS1_SaveOptions` 对象的类名。 |
| `vectorData` | boolean | 读写。为 true 则包含矢量数据。仅在文档包含矢量数据（未栅格化的文本）时有效。 |

## DCS2_SaveOptions

使用 `Document.saveAs()` 方法将 CMYK 文档保存为 DCS2 格式的选项。

### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `dcs` | [DCSType](DCSType) | 读写。创建的合成文件类型（默认：`DCSType.NOCOMPOSITE`）。 |
| `embedColorProfile` | boolean | 读写。True 表示在文档中嵌入颜色配置文件。 |
| `encoding` | [SaveEncoding](SaveEncoding) | 读写。使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | boolean | 读写。True 表示包含半调网屏（默认：false）。 |
| `interpolation` | boolean | 读写。True 表示使用图像插值（默认：false）。 |
| `multiFileDCS` | boolean | 读写。True 表示将颜色通道保存为多个文件或单个文件（默认：false）。 |
| `preview` | [Preview](Preview) | 读写。预览类型（默认：`Preview.MACOSEIGHTBIT`）。 |
| `spotColors` | boolean | 读写。True 表示保存专色。 |
| `transferFunction` | boolean | 读写。True 表示包含用于补偿图像与胶片之间网点扩大的传递函数（默认：false）。 |
| `typename` | string | 只读。引用的 `DCS2_SaveOptions` 对象的类名。 |
| `vectorData` | boolean | 读写。True 表示包含矢量数据。仅当文档包含矢量数据（未栅格化的文本）时有效。 |

## DICOMOpenOptions

使用 `Application.open()` 方法打开 DICOM 格式文档的选项。

**注意：**此功能仅在扩展版中可用。

### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `anonymize` | boolean | 读写。True 表示匿名化患者信息。 |
| `columns` | number | 读写。n-up 配置中的列数。 |
| `reverse` | boolean | 读写。True 表示反转（反转）图像。 |
| `rows` | number | 读写。n-up 配置中的行数。 |
| `showOverlays` | boolean | 读写。True 表示显示叠加层。 |
| `typename` | string | 只读。引用的 DICOMOpenOptions 对象的类名。 |
| `windowLevel` | number | 读写。图像在 Houndsfield 单位下的对比度。 |
| `windowWidth` | number | 读写。图像在 Houndsfield 单位下的亮度。 |

## Document

脚本中层和所有其他对象的主要容器对象；文件的基础画布。

- 通过 `Application.activeDocument` 访问当前活动文档的对象。
- 你可以访问其他文档，或使用 `Application.documents` 集合中的列表遍历所有打开的文档。你可以通过索引访问列表中的单个文档，或使用 `Documents.getByName()` 按名称检索它们。
- 使用 `Documents.add()` 方法以编程方式创建文档。

有关示例，请参阅 `Document sample script` 和 `Documents` 集合对象。

**注意：**在 Adobe Photoshop CS6 中，文档也可以称为图像或画布。

- 术语 `image` 指整个文档及其内容。你可以裁剪或修剪图像。使用 `resizeImage()` 方法调整图像大小。
- 术语 `canvas` 指文档在屏幕上所占的空间。你可以旋转或翻转画布。使用 `resizeCanvas()` 方法调整画布大小。

### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `activeChannels` | `Channel` 数组 | 读写。选定的通道。 |
| `activeHistoryBrushSource` | `Guide` | 读写。与历史记录画笔一起使用的历史记录状态。 |
| `activeHistoryState` | `Guide` | 读写。选定的 `HistoryState` 对象。 |
| `activeLayer` | `ArtLayer` 或 `LayerSet` | 读写。选定的图层。 |
| `artLayers` | `ArtLayers` | 只读。图层集合。 |
| `backgroundLayer` | `ArtLayer` | 只读。文档的背景图层。 |
| `bitsPerChannel` | `BitsPerChannelType` | 读写。每通道的位数。 |
| `channels` | `Channels` | 只读。通道集合。 |
| `colorProfileName` | string | 读写。颜色配置文件的名称。仅在 `colorProfileType` = `ColorProfile.CUSTOM` 或 `WORKING` 时有效。 |
| `colorProfileType` | `ColorProfileType` | 读写。文档使用工作颜色配置文件、自定义配置文件还是不使用配置文件。 |
| `colorSamplers` | `ColorSamplers` | 只读。与此文档关联的当前颜色取样器。 |
| `componentChannels` | `Channel` 数组 | 只读。构成文档的颜色通道；例如，RGB 文档的红、绿和蓝通道。 |
| `countItems` | `CountItems` | 只读。当前的计数项目。**注意：**有关计数项目的更多信息，请参阅 Adobe Photoshop CS6 帮助中的计数工具。 |
| `fullName` | `File` | 只读。文档的完整路径名。 |
| `guides` | `Guides` | 只读。参考线集合。 |
| `height` | `UnitValue` | 只读。文档的高度（单位值）。 |
| `histogram` | `number` 数组 | 只读。显示合成通道中每个颜色强度级别的像素数量的直方图。数组包含 256 个成员。仅在 `mode` = `DocumentMode.RGB`、`CMYK` 或 `INDEXEDCOLOR` 时有效。 |
| `historyStates` | `HistoryStates` | 只读。历史记录状态集合。 |
| `info` | `DocumentInfo` | 只读。文档的元数据。 |
| `layerComps` | `LayerComps` | 只读。图层复合集合。 |
| `layers` | `Layers` | 只读。图层集合。 |
| `layerSets` | `LayerSets` | 只读。图层组集合。 |
| `managed` | boolean | 只读。如果文档是工作组文档，则为 True。 |
| `measurementScale` | `MeasurementScale` | 只读。文档的测量比例。**注意：**测量比例功能仅在扩展版中可用。 |
| `mode` | `DocumentMode` | 只读。颜色配置文件。 |
| `name` | string | 只读。文档的名称。 |
| `parent` | `Application` | 只读。包含此文档的应用程序对象。 |
| `path` | `File` | 只读。文档的路径。 |
| `pathItems` | `PathItems` | 只读。路径项目集合。 |
| `pixelAspectRatio` | number [0.100..10.000] | 读写。使用的（自定义）像素长宽比。 |
| `printSettings` | `DocumentPrintSettings` | 只读。文档的打印设置。 |
| `quickMaskMode` | boolean | 读写。如果文档处于快速蒙版模式，则为 True。 |
| `resolution` | number | 只读。文档的分辨率（以每英寸像素数为单位）。 |
| `saved` | boolean | 只读。如果自上次更改后文档已保存，则为 True。 |
| `selection` | [Selection](Selection) | 只读。文档的选定区域。 |
| `typename` | string | 只读。`Document` 对象的类名。 |
| `width` | [UnitValue](UnitValue) | 只读。文档的宽度（单位值）。 |
| `xmpMetadata` | [xmpMetadata](xmpMetadata) | 只读。文档的 XMP 元数据。例如，图像的相机 RAW 设置存储在此处。 |

### 方法

| 方法 | 参数类型 | 返回值 | 描述 |
|---|---|---|---|
| `autoCount(channel, threshold)` | Channel number | | 计算文档中的对象数量。仅在扩展版中可用。<br>为每个计数的对象创建一个 `CountItem` 对象。<br>有关如何设置要计数的对象的更多信息，请参阅 Adobe Photoshop CS6 帮助中的计数工具。 |
| `changeMode(destinationMode [, options])` | ChangeMode BitmapConversionOptions 或 IndexedConversionOptions | | 更改文档的颜色配置文件。 |
| `close([saving])` | SaveOptions | | 关闭文档。如果进行了任何更改，脚本将显示一个带有三个选项的警报：保存、不保存、提示保存。可选参数指定在警报框中的选择（默认：`SaveOptionsType.PROMPTTOSAVECHANGES`）。 |
| `convertProfile(destinationProfile, intent [, blackPointCompensation] [, dither])` | string Intent boolean boolean | | 更改颜色配置文件。<br>`destinationProfile` 参数必须是命名颜色模式的字符串，或者是 Working RGB、Working CMYK、Working Gray、Lab Color（表示工作颜色空间之一或 Lab 颜色）。 |
| `crop(bounds [, angle] [, width] [, height])` | 4 个 UnitValue 的数组 number UnitValue UnitValue | | 裁剪文档。`bounds` 参数是裁剪后剩余区域的四个坐标数组，[left, top, right, bottom]。 |
| `duplicate([name] [, mergeLayersOnly])` | string boolean | Document | 创建文档对象的副本。<br>可选参数 `name` 为副本文档提供名称。<br>可选参数 `mergeLayersOnly` 指示是否仅复制合并的图层。 |

### 文档

| 方法 | 参数类型 | 返回值 | 功能描述（续） |
|---|---|---|---|
| `exportDocument(exportIn [, exportAs] [, options])` | File<br>ExportType<br>ExportOptionsIllustrator<br>-或-<br>ExportOptionsSaveForWeb | | 将文档中的路径导出为 Illustrator 文件，或将文档导出为适用于网页或设备查看优化的文件。<br><br>这相当于选择 **文件 > 导出 > 路径到 Illustrator**，或 **文件 > 存储为 Web 和设备所用格式**。 |
| `flatten()` | | | 平整文档中的所有图层。 |
| `flipCanvas(direction)` | Direction | | 在指定方向上翻转画布内的图像。 |
| `importAnnotations(file)` | File | | 将注释导入文档。 |
| `mergeVisibleLayers()` | | | 平整文档中所有可见的图层。 |
| `paste([intoSelection])` | boolean | ArtLayer | 将剪贴板的内容粘贴到文档中。如果可选参数设置为 `true` 且选区处于活动状态，则内容将粘贴到选区内。 |
| `print([sourceSpace] [, printSpace] [, intent] [, blackPointCompensation])` | SourceType<br>string<br>Intent<br>boolean | | 打印文档。<br><br>`printSpace` 指定打印机的色彩空间。有效值为 `nothing`（即与源相同）；或 Working RGB、Working CMYK、Working Gray、Lab Color（表示一种工作色彩空间或 Lab 颜色）；或指定特定色彩空间的字符串（默认与源相同）。 |
| `printOneCopy()` | | | 打印文档的一份副本。 |
| `rasterizeAllLayers()` | | | 栅格化所有图层。 |
| `recordMeasurements([source] [, dataPoints])` | MeasurementSource<br>array of string | | 记录文档的测量数据。 |
| `resizeCanvas([width] [, height] [, anchor])` | UnitValue<br>UnitValue<br>AnchorPosition | | 更改画布大小以显示更多或更少的图像，但不会更改图像大小。请参阅 `resizeImage()`。 |
| `resizeImage([width] [, height] [, resolution] [, resampleMethod])` | UnitValue<br>UnitValue<br>number<br>ResampleMethod | | 更改图像大小。 |
| `revealAll()` | | | 扩展文档以显示被裁切的部分。 |
| `rotateCanvas(angle)` | number | | 按顺时针方向旋转画布（包括图像）。 |
| `save()` | | | 保存文档。 |
| `saveAs(saveIn [, options] [, asCopy] [, extensionType])` | `File` 对象（见描述）<br>boolean<br>`Extension` | | 以特定格式保存文档。<br>通过传递以下对象之一来指定适用于该格式的保存选项：<br>- `BMPSaveOptions`<br>- `DCS1_SaveOptions`<br>- `DCS2_SaveOptions`<br>- `EPSSaveOptions`<br>- `GIFSaveOptions`<br>- `JPEGSaveOptions`<br>- `PDFSaveOptions`<br>- `PhotoshopSaveOptions`<br>- `PICTFileSaveOptions`<br>- `PICTResourceSaveOptions`<br>- `PixarSaveOptions`<br>- `PNGSaveOptions`<br>- `RawSaveOptions`<br>- `SGIRGBSaveOptions`<br>- `TargaSaveOptions`<br>- `TiffSaveOptions` |
| `splitChannels()` | | array of `Document` | 将文档通道分割为单独的图像。 |
| `suspendHistory(historyString, javaScriptString)` | string<br>string | | 在历史记录状态中为 `javaScriptString` 提供的整个脚本创建一个单独的条目。允许对脚本中执行的所有操作进行一次撤销。<br>`historyString` 参数提供用于历史记录状态的字符串。<br>`javaScriptString` 参数提供要在历史记录暂停期间执行的 JavaScript 代码字符串。 |
| `trap(width)` | number | | 对 CMYK 文档应用陷印。<br>仅在 `docRef.mode` = `DocumentMode.CMYK` 时有效。 |
| `trim([type] [, top] [, left] [, bottom] [, right])` | `TrimType`<br>boolean<br>boolean<br>boolean<br>boolean | | 裁剪画布指定边周围图像的透明区域。<br>所有布尔参数的默认值均为 `true`。 |

#### 文档示例脚本

以下脚本创建一个文档，其中包含从 Adobe Photoshop CS6 Samples 文件夹获取的两张图像（一朵向日葵和一只鸭子），并执行以下步骤：

- 判断哪张图像更大。
- 调整较小图像的大小以匹配较大的图像。
- 创建一个高度为任一图像两倍的合并文档，以容纳两张图像。
- 选择文档的一部分并将向日葵粘贴到选区中。
- 反转选区，并将鸭子粘贴到文档的下半部分。
- 将向日葵定位在鸭子的上方。

##### Document.jsx

```javascript
```



```javascript
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
| `backgroundColor` | `SolidColor` | 可读写。页面的背景色。 |
| `bleedWidth` | `UnitValue` | 可读写。出血宽度。 |
| `caption` | `boolean` | 可读写。打印 FileInfo 中找到的标题。 |
| `centerCropMarks` | `boolean` | 可读写。打印中心裁切标记。 |
| `colorBars` | `boolean` | 可读写。打印颜色校准条。 |
| `copies` | `number` | 可读写。要打印的份数。 |
| `cornerCropMarks` | `boolean` | 可读写。打印角落裁切标记。 |
| `colorHandling` | `PrintColorHandling` | 只读。颜色处理。 |
| `activePrinter` | `string` | 可读写。当前活动的打印机。 |
| `flip` | `boolean` | 可读写。水平翻转图像。 |
| `hardProof` | `boolean` | 可读写。打印硬校样。 |
| `interpolate` | `boolean` | 可读写。 |
| `labels` | `boolean` | 可读写。打印文档标题。 |
| `mapBlack` | `boolean` | 可读写。映射黑色。 |
| `negative` | `boolean` | 可读写。反转图像颜色。 |
| `renderIntent` | `Intent` | 可读写。当打印空间与源空间不同时的颜色转换意向。 |
| `posX` | `UnitValue` | 只读。图像在页面上的 X 位置。 |
| `posY` | `UnitValue` | 只读。图像在页面上的 Y 位置。 |
| `printBorder` | `UnitValue` | 可读写。打印边框的宽度。 |
| `printerName` | `string` | 可读写。打印机的名称。 |
| `printSpace` | `string` | 可读写。打印机的色彩空间。可以是 nothing（表示与源相同）；'Working RGB'、'Working CMYK'、'Working Gray'、'Lab Color'（表示一种工作空间或 Lab 颜色）；或指定特定色彩空间的字符串（默认与源相同）。 |
| `registrationMarks` | `boolean` | 可读写。打印套准标记。 |

## 属性

| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `scale` | `number` | 只读。图像在页面上的缩放比例。 |
| `vectorData` | `boolean` | 读写。是否包含矢量数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| :--- | :--- | :--- | :--- |
| `setPagePosition(docPosition, posX, posY, scale)` | `DocPositionStyle`<br>`UnitValue`<br>`UnitValue`<br>`number` | | 设置图像在页面上的位置。 |

### DocumentInfo

关于 `document` 对象的元数据。

可通过 `Document.info` 属性访问。例如，以下代码设置了 `author`、`caption` 和 `copyrighted` 属性：

这些值可以通过选择**文件 > 文件信息**进行交互式设置。

```javascript
var docRef = open(fileList[i])

// set the file info

docRef.info.author = "Mr. Adobe programmer"

docRef.info.caption = "Adobe Photo shoot"

docRef.info.copyrighted = CopyrightedType.COPYRIGHTEDWORK
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `author` | `string` | 读写。 |
| `authorPosition` | `string` | 读写。 |
| `caption` | `string` | 读写。 |
| `captionWriter` | `string` | 读写。 |
| `category` | `string` | 读写。 |
| `city` | `string` | 读写。 |
| `copyrighted` | `CopyrightedType` | 读写。版权状态。 |
| `copyrightNotice` | `string` | 读写。 |
| `country` | `string` | 读写。 |
| `creationDate` | `string` | 读写。 |
| `credit` | `string` | 读写。 |
| `exif` | `array of array [tag data]` | 只读。包含拍摄图像时使用的相机设置等相机数据。每个数组成员是一个标签对，即 [tag, tag_data] 的数组；例如，["camera" "Cannon"]。 |
| `headline` | `string` | 读写。 |
| `instructions` | `string` | 读写。 |
| `jobName` | `string` | 读写。 |
| `keywords` | `array of string` | 读写。可用于标识文档或其内容的关键字列表。 |
| `ownerUrl` | `string` | 读写。 |
| `parent` | `Document` | 只读。信息对象的容器。 |
| `provinceState` | `string` | 读写。 |
| `source` | `string` | 读写。 |
| `supplementalCategories` | `array of string` | 读写。 |
| `title` | `string` | 读写。 |
| `transmissionReference` | `string` | 读写。 |
| `typename` | `string` | 只读。引用的信息对象的类名。 |
| `urgency` | `Urgency` | 读写。 |

#### DocumentInfo 脚本示例

以下脚本为指定文件夹中的所有文件设置文档信息（元数据），然后将修改后的文件以低质量 JPEG 图像保存到新文件夹中，而不更改原始文件。

- 要求用户指定包含原始文件的文件夹和用于输出 JPEG 图像的文件夹，然后检查文件夹是否存在。
- 打开每个文件，并使用 `documentInfo` 对象属性为其添加以下元数据：
  - `author`: Adobe programmer
  - `caption`: Adobe Photo shoot
  - `captionWriter`: Adobe programmer
  - `city`: San Jose
  - `copyrightNotice`: Copyright (c) Adobe programmer Photography
  - `copyrighted status`: Copyrighted Work
  - `country`: USA
  - `state`: CA
- 将新文档保存为 JPEG 格式，并设置低质量。

**DocumentInfo.jsx**

```javascript
// Save the current preferences

var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CS6 to use pixels and display no dialogs

app.displayDialogs = DialogModes.NO

// ask the user for the input and output folders

var inputFolder = Folder.selectDialog("Select a folder to tag")

var outputFolder = Folder.selectDialog("Select a folder for the output files")

// see if we got something interesting from the dialog

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



```javascript
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

已打开的 [`Document`](https://www.adobe.com/) 对象的集合。

可通过 [`Application.documents`](https://www.adobe.com/) 集合属性访问此列表，该属性可通过 `app` 全局变量使用，或直接在顶层使用。例如，以下代码向集合中添加了一个新文档：

```javascript
app.documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```

或：

```javascript
documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```



## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。`documents` 集合中的元素数量。 |
| `parent` | [Application](https://www.adobe.com/) | 只读。包含它的应用程序。 |
| `typename` | `string` | 只读。引用的 `documents` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| :--- | :--- | :--- | :--- |
| `add` (`[width]`, `[height]`, `[resolution]`, `[name]`, `[mode]`, `[initialFill]`, `[pixelAspectRatio]`, `[bitsPerChannel]`, `[colorProfileName]`) | [UnitValue](https://www.adobe.com/) [UnitValue](https://www.adobe.com/) `number` `string` [NewDocumentMode](https://www.adobe.com/) [DocumentFill](https://www.adobe.com/) `number [0.1..10.00]` [BitsPerChannelType](https://www.adobe.com/) `string` | [Document](https://www.adobe.com/) | 创建一个新的文档对象并将其添加到此集合中。<br><br>`pixelAspectRatio`：默认值为 1.0，即正方形宽高比。<br><br>`bitsPerChannelType`：默认值为 `BitsPerChannelType.EIGHT`。 |
| `getByName` (`name`) | `string` | [Document](https://www.adobe.com/) | 获取 `documents` 集合中具有提供名称的第一个元素 |

### EPSOpenOptions

使用 [Application.open()](Application.open()) 方法打开 EPS 格式文档时的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `antiAlias` | `boolean` | 读写。为 `true` 时使用抗锯齿。 |
| `constrainProportions` | `boolean` | 读写。为 `true` 时约束图像的比例。 |
| `height` | `UnitValue` | 读写。图像的高度（单位值）。 |
| `mode` | `OpenDocumentMode` | 读写。用作文档模式的色彩配置文件。 |
| `resolution` | `number` | 读写。文档的分辨率，单位为像素/英寸。 |
| `typename` | `string` | 只读。引用的 `EPSOpenOptions` 对象的类名。 |
| `width` | `UnitValue` | 读写。图像的宽度（单位值）。 |

### EPSSaveOptions

使用 [Document.saveAs()](#) 方法将文档保存为 EPS 格式时的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `embedColorProfile` | `boolean` | 可读写。设为 `true` 以在本文档中嵌入颜色配置文件。 |
| `encoding` | [SaveEncoding](#) | 可读写。使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | `boolean` | 可读写。设为 `true` 以包含半调网屏（默认：`false`）。 |
| `interpolation` | `boolean` | 可读写。设为 `true` 以使用图像插值（默认：`false`）。 |
| `preview` | [Preview](#) | 可读写。预览类型。 |
| `psColorManagement` | `boolean` | 可读写。设为 `true` 以使用 Postscript 颜色管理（默认：`false`）。 |
| `transferFunction` | `boolean` | 可读写。设为 `true` 以包含用于补偿图像与胶片之间网点扩大的传递函数（默认：`false`）。 |
| `transparentWhites` | `boolean` | 可读写。设为 `true` 以将白色区域显示为透明。仅在 `document.mode = DocumentMode.BITMAP` 时有效。另请参见 [changeMode()](#)。 |
| `typename` | `string` | 只读。所引用的 `EPSSaveOptions` 对象的类名。 |
| `vectorData` | `boolean` | 可读写。设为 `true` 以包含矢量数据。仅当文档包含矢量数据（文本）时有效。 |

### ExportOptionsIllustrator

使用 `Document.exportDocument()` 方法将 `PathItem` 对象导出到 Adobe Illustrator® 文件时的选项。当您选择**文件 > 导出 > 路径到 Illustrator**时，可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `path` | `IllustratorPathType` | 可读写。要导出的路径类型（默认：`IllustratorPathType.DOCUMENTBOUNDS`）。 |
| `pathName` | `string` | 可读写。要导出的路径的名称。仅当 `path = IllustratorPathType.NAMEDPATH` 时有效。 |
| `typename` | `string` | 只读。所引用的 `exportOptionsIllustrator` 对象的类名。 |

### ExportOptionsSaveForWeb

使用 `Document.exportDocument()` 方法优化文档以用于 Web 或设备时的选项。当您选择**文件 > 存储为 Web 和设备所用格式**时，可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `blur` | `number` | 可读写。对图像应用模糊以减少伪影（默认：0.0）。 |
| `colorReduction` | `ColorReductionType` | 可读写。颜色减低算法（默认：`ColorReductionType.SELECTIVE`）。 |
| `colors` | `number` | 可读写。调色板中的颜色数量（默认：256）。 |
| `dither` | `Dither` | 可读写。仿色类型（默认：`Dither.DIFFUSION`）。 |
| `ditherAmount` | `number` | 可读写。仿色量（默认：100）。仅当 `dither = Dither.DIFFUSION` 时有效。 |
| `format` | `SaveDocumentType` | 可读写。使用的文件格式（默认：`SaveDocumentType.COMPSERVEGIF`）。**注意：**对于此属性，仅支持 COMPSERVEGIF、JPEG、PNG-8、PNG-24 和 BMP。 |
| `includeProfile` | `boolean` | 可读写。设为 `true` 以包含文档的嵌入颜色配置文件（默认：`false`）。 |
| `interlaced` | `boolean` | 可读写。设为 `true` 以分多次下载；渐进式（默认：`false`）。 |
| `lossy` | `number` | 可读写。允许的有损压缩量（默认：0）。 |
| `matteColor` | `RGBColor` | 可读写。与透明像素混合的颜色。 |
| `optimized` | `boolean` | 可读写。设为 `true` 以创建更小但兼容性较差的文件（默认：`true`）。仅当 `format = SaveDocumentType.JPEG` 时有效。 |
| `PNG8` | `boolean` | 可读写。指定位数；`true` = 8，`false` = 24（默认：`true`）。仅当 `format = SaveDocumentType.PNG` 时有效。 |
| `quality` | `number [0..100]` | 可读写。生成图像的质量百分比；默认：60。 |
| `transparency` | `boolean` | 可读写。指示图像的透明区域是否应包含在保存的图像中（默认：`true`）。 |
| `transparencyAmount` | `number` | 可读写。透明仿色量（默认：100）。<br>仅当 `transparency = true` 时有效。 |
| `transparencyDither` | `Dither` | 可读写。透明仿色算法（默认：`transparencyDither = Dither.NONE`）。 |
| `typename` | `string` | 只读。所引用的 `ExportOptionsSaveForWeb` 对象的类名。 |
| `webSnap` | `number` | 可读写。将相近颜色吸附到 Web 调色板颜色的容差量（默认：0）。 |

### File

### Folder

ExtendScript 定义了 JavaScript 类 `File` 和 `Folder`，以平台无关的方式封装文件系统引用；详见第 32 页的 [Adobe Photoshop CS6 中的 JavaScript 支持]。有关这些类的详细参考，请参阅 *JavaScript 工具指南*。

### GalleryBannerOptions

[GalleryOptions](GalleryOptions) 对象的 [bannerOptions](bannerOptions) 属性的选项。

**提示：**您可以通过将 [GalleryOptions](GalleryOptions) 属性 [preserveAllMetadata](preserveAllMetadata) 设置为 `true` 来保留许多属性的默认值；这与选择**文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择**保留所有元数据**效果相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `contactInfo` | `string` | 可读写。Web 照片库的联系信息。 |
| `date` | `string` | 可读写。Web 照片库的日期（默认：当前日期）。 |
| `font` | [GalleryFontType](GalleryFontType) | 可读写。横幅文本的字体设置（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number [1..7]` | 可读写。横幅文本的字体大小（默认：3）。 |
| `photographer` | `string` | 可读写。Web 照片库的摄影师。 |
| `siteName` | `string` | 可读写。Web 照片库的站点名称（默认：Adobe Web Photo Gallery）。 |
| `typename` | `string` | 只读。所引用的 `galleryBannerOptions` 对象的类名。 |

### GalleryCustomColorOptions

[GalleryOptions](https://example.com) 对象的 [customColorOptions](https://example.com) 属性的选项。

**提示：**您可以通过将 [GalleryOptions](https://example.com) 属性 [preserveAllMetadata](https://example.com) 设置为 `true` 来保留许多属性的默认值；这与选择**文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择**保留所有元数据**效果相同。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `activeLinkColor` | [RGBColor](https://example.com) | 可读写。用于指示活动链接的颜色。 |
| `backgroundColor` | [RGBColor](https://example.com) | 可读写。背景颜色。 |
| `bannerColor` | [RGBColor](https://example.com) | 可读写。横幅颜色。 |
| `linkColor` | [RGBColor](https://example.com) | 可读写。用于指示链接的颜色。 |
| `textColor` | [RGBColor](https://example.com) | 可读写。文本颜色。 |
| `typename` | `string` | 只读。所引用的 `galleryCustomColorOptions` 对象的类名。 |
| `visitedLinkColor` | [RGBColor](https://example.com) | 可读写。用于指示已访问链接的颜色。 |

### GalleryImagesOptions

[GalleryOptions](https://example.com) 对象的 [imagesOptions](https://example.com) 属性的选项。

**提示：**您可以通过将 [GalleryOptions](https://example.com) 属性 [preserveAllMetadata](https://example.com) 设置为 `true` 来保留许多属性的默认值；这与选择**文件 > 自动 > Web 照片库**，然后在 Web 照片库对话框的选项区域中选择**保留所有元数据**效果相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `border` | `number [0..99]` | 可读写。分隔图像的边框大小（以像素为单位）（默认：0）。 |
| `caption` | `boolean` | 可读写。设为 `true` 以生成图像说明（默认：`false`）。 |
| `dimension` | `number` | 可读写。调整后的图像尺寸（以像素为单位）（默认：350）。仅当 `resizeImages = true` 时有效。 |
| `font` | [GalleryFontType](https://example.com) | 可读写。用于图像说明的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number [1..7]` | 可读写。图像说明的字体大小（默认：3）。仅当 `caption = true` 时有效。 |
| `imageQuality` | `number [0..12]` | 可读写。JPEG 图像的质量设置（默认：5）。 |
| `includeCopyright` | `boolean` | 可读写。设为 `true` 以在说明中包含版权信息（默认：`false`）。仅当 `caption = true` 时有效。 |
| `includeCredits` | `boolean` | 可读写。设为 `true` 以在图像说明中包含致谢信息（默认：`false`）。仅当 `caption = true` 时有效。 |
| `includeFilename` | `boolean` | 可读写。设为 `true` 以在图像说明中包含文件名（默认：`true`）。仅当 `caption = true` 时有效。 |
| `includeTitle` | `boolean` | 可读写。设为 `true` 以在图像说明中包含标题（默认：`false`）。仅当 `caption = true` 时有效。 |
| `numericLinks` | `boolean` | 可读写。设为 `true` 以添加数字链接（默认：`true`）。 |

#### GalleryImagesOptions（续）

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `resizeConstraint` | [GalleryConstrainType](http://www.adobe.com/devnet/photoshop/scriptingreference/#GalleryConstrainType) | 读写。图库图像中要约束的图像尺寸（默认值：`GalleryConstrainType.CONSTRAINBOTH`）。仅在 `resizeImages = true` 时有效。 |
| `resizeImages` | `boolean` | 读写。为 `true` 时，自动调整图像大小以便放置在图库页面上（默认值：`true`）。 |
| `typename` | `string` | 只读。引用的 `galleryImagesOptions` 对象的类名。 |

### GalleryOptions

网络照片图库的选项，通过 [Application.makePhotoGallery()](http://www.adobe.com) 创建。

> **提示：**你可以通过选择**文件 > 自动 > Web 照片图库**，然后在 Web 照片图库对话框的选项区域中选择**保留所有元数据**，来保留许多属性的默认值。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `addSizeAttributes` | `boolean` | 读写。为 `true` 时，为图像添加宽度和高度属性（默认值：`true`）。 |
| `bannerOptions` | `GalleryBannerOptions` | 读写。与横幅设置相关的选项。 |
| `customColorOptions` | `GalleryCustomColorOptions` | 读写。与自定义颜色设置相关的选项。 |
| `emailAddress` | `string` | 读写。要在网页上显示的电子邮件地址。 |
| `imagesOptions` | `GalleryImagesOptions` | 读写。与图像设置相关的选项。 |
| `includeSubFolders` | `boolean` | 读写。为 `true` 时，包含输入文件夹子文件夹中的所有文件（默认值：`true`）。 |
| `layoutStyle` | `string` | 读写。用于布局网页的样式（默认值：*居中框架 1 - 基本*）。 |
| `preserveAllMetadata` | `boolean` | 读写。为 `true` 时，保存元数据（默认值：*false*）。 |
| `securityOptions` | `GallerySecurityOptions` | 读写。与安全设置相关的选项。 |
| `thumbnailOptions` | `GalleryThumbnailOptions` | 读写。与缩略图图像设置相关的选项。 |
| `typename` | `string` | 只读。引用的 `galleryOptions` 对象的类名。 |
| `useShortExtension` | `boolean` | 读写。为 `true` 时，使用简短的网页扩展名 `.htm`。如果为 `false`，则使用网页扩展名 `.html`（默认值：`true`）。 |
| `useUTF8Encoding` | `boolean` | 读写。为 `true` 时，使用 UTF-8 编码处理网页（默认值：`false`）。 |

### GallerySecurityOptions

[GalleryOptions](https://helpx.adobe.com/photoshop/using/scripting-reference.html#galleryoptions) 对象的 [securityOptions](https://helpx.adobe.com/photoshop/using/scripting-reference.html#gallerysecurityoptions) 属性的选项。

> **提示：**你可以通过将 `GalleryOptions` 属性 `preserveAllMetadata` 设置为 `true` 来保留许多属性的默认值；这等同于选择**文件 > 自动 > Web 照片图库**，然后在 Web 照片图库对话框的选项区域中选择**保留所有元数据**。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `content` | [GallerySecurityType](https://helpx.adobe.com/photoshop/using/scripting-reference.html#gallerysecuritytype) | 读写。网络照片图库的安全内容（默认值：`GallerySecurityType.NONE`）。 |
| `font` | [GalleryFontType](https://helpx.adobe.com/photoshop/using/scripting-reference.html#galleryfonttype) | 读写。网络照片图库的安全字体（默认值：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number [1...72]` | 读写。网络照片图库的安全字体大小（默认值：3）。 |
| `opacity` | `number` | 读写。网页安全的不透明度（以百分比表示）（默认值：100）。 |
| `text` | `string` | 读写。网络照片图库的安全自定义文本。 |
| `textColor` | [GallerySecurityTextColorType](https://helpx.adobe.com/photoshop/using/scripting-reference.html#gallerysecuritytextcolortype) | 读写。网页安全文本的颜色。 |
| `textPosition` | [GallerySecurityTextPositionType](https://helpx.adobe.com/photoshop/using/scripting-reference.html#gallerysecuritytextpositiontype) | 读写。网络照片图库的安全文本位置（默认值：`GallerySecurityTextPositionType.CENTERED`）。 |
| `textRotate` | [GallerySecurityTextRotateType](https://helpx.adobe.com/photoshop/using/scripting-reference.html#gallerysecuritytextrotatetype) | 读写。要使用的网络照片图库安全文本方向（默认值：`GallerySecurityTextRotateType.ZERO`）。 |
| `typename` | `string` | 只读。引用的 `gallerySecurityOptions` 对象的类名。 |

### GalleryThumbnailOptions

[GalleryOptions](GalleryOptions) 对象的 [thumbnailOptions](thumbnailOptions) 属性的选项。

> **提示：**你可以通过将 [GalleryOptions](GalleryOptions) 属性 `preserveAllMetadata` 设置为 `true` 来保留许多属性的默认值；这等同于选择**文件 > 自动 > Web 照片图库**，然后在 Web 照片图库对话框的选项区域中选择**保留所有元数据**。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `border` | `number [0..99]` | 读写。你希望围绕缩略图图像的边框像素量（默认值：0）。 |
| `caption` | `boolean` | 读写。为 `true` 时，有说明文字（默认值：`false`）。 |
| `columnCount` | `number` | 读写。页面上的列数（默认值：5）。 |
| `dimension` | `number` | 读写。网络照片图库缩略图的尺寸（以像素为单位）（默认值：75）。 |
| `font` | [GalleryFontType](GalleryFontType) | 读写。网络照片图库字体（默认值：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number [1..7]` | 读写。缩略图图像文本的字体大小（默认值：3）。 |
| `includeCopyright` | `boolean` | 读写。为 `true` 时，包含缩略图的版权信息（默认值：`false`）。 |
| `includeCredits` | `boolean` | 读写。为 `true` 时，包含缩略图的致谢信息（默认值：`false`）。 |
| `includeFilename` | `boolean` | 读写。为 `true` 时，包含缩略图的文件名（默认值：`false`）。 |
| `includeTitle` | `boolean` | 读写。为 `true` 时，包含缩略图的标题（默认值：`false`）。 |
| `rowCount` | `number` | 读写。页面上的行数（默认值：3）。 |
| `size` | [GalleryThumbSizeType](GalleryThumbSizeType) | 读写。缩略图图像大小（默认值：`GalleryThumbSizeType.MEDIUM`）。 |
| `typename` | `string` | 只读。引用的 `GalleryThumbnailOptions` 对象的类名。 |

### GIFSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 GIF 格式时的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `colors` | `number` | 读写。调色板颜色的数量。仅在 `palette = Palette.LOCALADAPTIVE, LOCALPERCEPTUAL, LOCALSELECTIVE, MACOSPALETTE, UNIFORM, WEBPALETTE` 或 `WINDOWSPALETTE` 时有效。 |
| `dither` | `Dither` | 读写。抖动类型。 |
| `ditherAmount` | `number [1..100]` | 读写。抖动量（默认值：75）。仅在 `dither = Dither.DIFFUSION` 时有效。 |
| `forced` | `ForcedColors` | 读写。要强制添加到颜色调色板中的颜色类型。 |
| `interlaced` | `boolean` | 读写。为 `true` 时，行应交错排列（默认值：`false`）。 |
| `matte` | `MatteType` | 读写。用于填充图像透明区域相邻抗锯齿边缘的颜色（默认值：`MatteType.WHITE`）。当 `transparency = false` 时，哑光颜色将应用于透明区域。 |
| `palette` | `PaletteType` | 读写。要使用的调色板类型（默认值：`Palette.LOCALSELECTIVE`）。 |
| `preserveExactColors` | `boolean` | 读写。为 `true` 时，保护图像中在颜色表中有条目的颜色免受抖动。仅在 `dither = Dither.DIFFUSION` 时有效。 |
| `transparency` | `boolean` | 读写。为 `true` 时，在转换为 GIF 格式时保留图像的透明区域。 |
| `typename` | `string` | 只读。引用的 `GIFSaveOptions` 对象的类名。 |

### GrayColor

定义一种灰色，用于 [SolidColor](object) 对象中。

另请参阅 [CMYKColor](object)、[HSBColor](object)、[LabColor](object)、[NoColor](object)、[RGBColor](object)。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `gray` | `number [0.0..100.0]` | 读写。灰色值（默认：0.0）。 |
| `typename` | `string` | 只读。引用的 `grayColor` 对象的类名。 |

### 参考线

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `direction` | [Direction](https://www.example.com) | 读写。指示参考线是垂直还是水平。 |
| `coordinate` | [UnitValue](https://www.example.com) | 读写。参考线距离图像原点的位置。 |

### 参考线集合

包含所有打开的 [Guide](https://example.com) 对象的集合。

通过 [Document.guides](https://example.com) 集合属性访问此列表，该属性可通过 `activeDocument` 对象获取。例如，以下代码向集合中添加一条新参考线：

```javascript
```



`activeDocument.guides.add(Direction.HORIZONTAL, UnitValue(20, 20))`

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `length` | `number` | 只读。`guides` 集合中的元素数量。 |
| `parent` | [Document](https://example.com) | 只读。包含的文档。 |
| `typename` | `string` | 只读。引用的 `guides` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回 | 描述 |
|---|---|---|---|
| `add(direction, coordinate)` | [Direction](https://example.com)、[UnitValue](https://example.com) | [Guide](https://example.com) | 创建一个新的参考线对象并将其添加到此集合中。 |
| `getByName(name)` | `string` | [Guide](https://example.com) | 获取 `guides` 集合中具有所提供名称的第一个元素。 |

### HistoryState

文档的一个版本，在文档每次更改时自动存储（并添加到 `HistoryStates` 集合中），它保存了文档的状态。

通过 `Document.historyStates` 集合访问。你可以按名称访问列表中的一个状态。例如，以下代码为名为 `"AddLayerMask"` 的状态对象中的一个属性赋值：

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
|---|---|---|
| `length` | `number` | 只读。`HistoryStates` 集合中的元素数量。 |
| `parent` | [Document](https://example.com/document) | 只读。包含的文档。 |
| `typename` | `string` | 只读。引用的 `HistoryStates` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回 | 描述 |
|---|---|---|---|
| `getByName(name)` | `string` | [HistoryState](https://example.com) | 获取 `HistoryStates` 集合中具有所提供名称的第一个元素。 |

### HSBColor

定义一种 HSB 颜色，用于 [SolidColor](https://example.com) 对象中。

另请参阅 [CMYKColor](https://example.com)、[GrayColor](https://example.com)、[LabColor](https://example.com)、[NoColor](https://example.com)、[RGBColor](https://example.com)。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `brightness` | `number [0.0..100.0]` | 读写。亮度值。 |
| `hue` | `number [0.0..360.0]` | 读写。色相值。 |
| `saturation` | `number [0.0..100.0]` | 读写。饱和度值。 |
| `typename` | `string` | 只读。引用的 `HSBColor` 对象的类名。 |

### IndexedConversionOptions

使用 [Document.changeMode()](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/document/Document.html#DocumentChangeMode) 将 RGB 图像转换为索引颜色模型的选项。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `colors` | `number` | 读写。调色板颜色数量。仅在 `palette` = `Palette.LOCALADAPTIVE`、`LOCALPERCEPTUAL`、`LOCALSELECTIVE`、`MACOSPALETTE`、`UNIFORM`、`WEBPALETTE` 或 `WINDOWSPALETTE` 时有效。 |
| `dither` | [Dither](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/Dither.html) | 读写。仿色类型。 |
| `ditherAmount` | `number [1..100]` | 读写。仿色量。仅在 `dither` = `Dither.diffusion` 时有效。 |
| `forced` | [ForcedColors](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/ForcedColors.html) | 读写。强制添加到颜色调色板中的颜色类型。 |
| `matte` | [MatteType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/MatteType.html) | 读写。用于填充与图像透明区域相邻的抗锯齿边缘的颜色（默认：`MatteType.WHITE`）。当 `transparency` = `false` 时，消隐颜色将应用于透明区域。 |
| `palette` | [PaletteType](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/properties/indexedconversionoptions/PaletteType.html) | 读写。调色板类型（默认：`Palette.EXACT`）。 |
| `preserveExactColors` | `boolean` | 读写。为真时，保护图像中包含在颜色表中的条目免受仿色影响。仅在 `dither` = `Dither.DIFFUSION` 时有效。 |
| `transparency` | `boolean` | 读写。为真时，在转换为 GIF 格式期间保留图像的透明区域。 |
| `typename` | `string` | 只读。引用的 `IndexedConversionOptions` 对象的类名。 |

### JPEGSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 JPEG 格式的选项。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `embedColorProfile` | `boolean` | 读写。为真时，在文档中嵌入颜色配置文件。 |
| `formatOptions` | `FormatOptions` | 读写。要使用的下载格式（默认：`FormatOptions.STANDARDBASELINE`）。 |
| `matte` | `MatteType` | 读写。用于填充与图像透明区域相邻的抗锯齿边缘的颜色（默认：`MatteType.WHITE`）。当图像的透明度关闭时，消隐颜色将应用于透明区域。 |
| `quality` | `number [0..12]` | 读写。要使用的图像质量设置；影响文件大小和压缩（默认：3）。 |
| `scans` | `number [3..5]` | 读写。在页面上增量显示图像所需的扫描次数（默认：3）。仅在 `formatOptions` = `FormatOptions.PROGRESSIVE` 时有效。 |
| `typename` | `string` | 只读。引用的 `JPEGSaveOptions` 对象的类名。 |

### LabColor

定义一种 LAB 颜色，用于 [SolidColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html) 对象中。

另请参阅 [CMYKColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html)、[GrayColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html)、[HSBColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html)、[NoColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html)、[RGBColor](https://helpx.adobe.com/photoshop/using/default-object-reference.html)。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `a` | `number [-128.0..127.0]` | 读写。a 值。 |
| `b` | `number [-128.0..127.0]` | 读写。b 值。 |
| `l` | `number [0.0..100.0]` | 读写。L 值。 |
| `typename` | `string` | 只读。引用的 `LabColor` 对象的类名。 |

## 图层复合

图层复合是文档中图层状态的快照，可用于查看不同的页面布局或合成效果。

通过 [Document.layerComps](Document.layerComps) 集合访问。你可以通过图层复合的名称来访问它。例如，以下代码为名为 `myLayerComp` 的 `LayerComp` 对象设置 `comment` 属性值：

```javascript
var layercompRef = app.activeDocument.layerComps.getByName("myLayerComp");

layercompRef.comment = "View from shoreline";
```

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `appearance` | 布尔值 | 可读写。如果为 `true`，则使用图层外观（图层样式）设置。 |
| `comment` | 字符串 | 可读写。图层复合的描述。 |
| `name` | 字符串 | 可读写。图层复合的名称。 |
| `parent` | [Document](Document) | 可读写。所属文档。 |
| `position` | 布尔值 | 可读写。如果为 `true`，则使用图层位置。 |
| `selected` | 布尔值 | 只读。如果图层复合当前被选中，则为 `true`。 |
| `typename` | 字符串 | 只读。所引用 `layerComp` 对象的类名。 |
| `visibility` | 布尔值 | 可读写。如果为 `true`，则使用图层可见性设置。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `apply()` |  |  | 将图层复合应用于文档。 |
| `recapture()` |  |  | 为此图层复合重新捕获当前的图层状态。 |
| `remove()` |  |  | 删除 `layerComp` 对象。 |
| `resetfromComp()` |  |  | 将图层复合状态重置为文档状态。 |

### LayerComps

文档中的 `LayerComp` 对象集合。

通过 `Document.layerComps` 集合属性访问。例如：

```javascript
app.activeDocument.layerComps.add("myLayerComp", "View from Shoreline", true, true, true);
```

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `length` | 数字 | 只读。`layerComps` 集合中的元素数量。 |
| `parent` | `Document` | 只读。所属文档。 |
| `typename` | 字符串 | 只读。所引用 `layerComps` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `add(name, comment, appearance, position, visibility)` | 字符串、字符串、布尔值、布尔值、布尔值 | `LayerComp` | 创建一个新的图层合成对象，并将其添加到此集合中。 |
| `getByName(name)` | 字符串 | `LayerComp` | 获取集合中具有指定名称的第一个元素。 |
| `removeAll()` |  |  | 从 `layerComps` 集合中移除所有成员对象。 |

### Layers

文档中的图层对象集合，包括 [ArtLayer](ArtLayer) 和 [LayerSet](LayerSet) 对象。通过 [Document.layers](Document.layers) 或 [LayerSet.layers](LayerSet.layers) 集合属性访问。

例如，以下代码使用 `length` 属性计算活动文档中 `layer` 对象的数量，然后在屏幕上显示该数字：

```javascript
var layerNum = app.activeDocument.layers.length;

alert(layerNum);
```

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `length` | 数字 | 只读。`layers` 集合中的元素数量。 |
| `parent` | [Document](Document) 或 [LayerSet](LayerSet) | 只读。所属文档或图层集。 |
| `typename` | 字符串 | 只读。所引用 `layers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `getByName(name)` | 字符串 | `Layer` | 获取 `layers` 集合中具有指定名称的第一个元素。 |
| `removeAll()` |  |  | 从集合中移除所有图层。 |

### LayerSet

图层对象的集合，可以包含 `ArtLayer` 对象和其他（嵌套的）`LayerSet` 对象。一个命令可以操作该集合中的所有图层。

通过 `Document.layerSets` 集合访问文档中的顶级图层集。你可以按名称访问图层集。例如，以下代码为 `"myLayerSet"` 设置 `allLocked` 值：

```javascript
var layerSetRef = app.activeDocument.layerSets.getByName("myLayerSet");

layerSetRef.allLocked = true;
```

通过父级集合中的 `LayerSet.layerSets` 集合访问嵌套的图层集。例如：

```javascript
app.activeDocument.layerSets[0].layerSets[0];
```




## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `allLocked` | 布尔值 | 可读写。如果此集中图层的内容不可编辑，则为 true。 |
| `artLayers` | `ArtLayers` | 只读。此图层集中的普通图层。 |
| `blendMode` | `BlendMode` | 可读写。图层集使用的混合模式。 |
| `bounds` | `UnitValue` 数组 | 只读。图层集的边界矩形。 |
| `enabledChannels` | `Channel` 数组 | 可读写。为图层集启用的通道；必须是成分通道的列表。请参见 `Channel.kind`。 |
| `layers` | `Layers` | 只读。此图层集中的图层。 |
| `layerSets` | `LayerSets` | 只读。包含在此图层集中的嵌套图层集。 |
| `linkedLayers` | `ArtLayer` 和/或 `LayerSet` 数组 | 只读。链接到此 `layerSet` 对象的图层。 |
| `name` | 字符串 | 可读写。此图层集的名称。 |
| `opacity` | 数字 [0.0..100.0] | 可读写。图层集的总体不透明度。 |
| `parent` | `Document` 或 `LayerSet` | 只读。所属文档或图层集。 |
| `typename` | 字符串 | 只读。所引用 `LayerSet` 对象的类名。 |
| `visible` | 布尔值 | 可读写。如果图层集可见，则为 true。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `duplicate([relativeObject][, insertionLocation])` | `ArtLayer` 或 `LayerSet`，`ElementPlacement` | `LayerSet` | 创建对象的副本。 |
| `link(with)` | `ArtLayer` 或 `LayerSet` |  | 将图层集与另一个图层链接。 |
| `merge()` |  | `ArtLayer` | 合并图层集；返回此方法创建的普通图层的引用。 |
| `move(relativeObject, insertionLocation)` | `ArtLayer` 或 `LayerSet`，`ElementPlacement` |  | 移动对象。 |
| `remove()` |  |  | 删除对象。 |
| `resize([horizontal][, vertical][, anchor])` | 数字，数字，`AnchorPosition` |  | 将图层集中的所有图层调整为指定尺寸（作为其当前尺寸的百分比），并将图层集置于指定位置。 |
| `rotate(angle[, anchor])` | 数字，`AnchorPosition` |  | 围绕指定锚点（默认：`AnchorPosition.MIDDLECENTER`）旋转图层集中的所有图层。 |
| `translate([deltaX][, deltaY])` | `UnitValue`，`UnitValue` |  | 相对于其当前位置移动位置。 |
| `unlink()` |  |  | 取消链接图层集。 |

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
| `length` | 数字 | 只读。`LayerSets` 集合中的元素数量。 |
| `parent` | `Document` 或 `LayerSet` | 只读。所属文档或图层集。 |
| `typename` | 字符串 | 只读。所引用 `layerSets` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `add()` |  | `LayerSet` | 创建一个新的图层集对象，并将其添加到集合中。 |
| `getByName(name)` | 字符串 | `LayerSet` | 获取集合中具有指定名称的第一个元素。 |
| `removeAll()` |  |  | 从文档中移除所有成员图层集，以及它们包含的任何图层或图层集。 |

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
| `exportMeasurements([file][, range][, dataPoints])` | `File`<br>`MeasurementRange`<br>字符串数组 |  | 将测量数据导出到文件。 |
| `deleteMeasurements([range])` | `MeasurementRange` |  | 从日志中删除测量数据。 |

### MeasurementScale

文档的测量比例尺。通过 `Document.measurementScale` 属性访问。例如：

```javascript
app.activeDocument.measurementScale.pixelLength = 25
```

> **注意：** 此功能仅在扩展版本中可用。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `pixelLength` | `number` | 可读写。此比例尺对应的像素长度。 |
| `logicalLength` | `number` | 可读写。此比例尺对应的逻辑长度。 |
| `logicalUnits` | `string` | 可读写。此比例尺的逻辑单位。 |

### NoColor

表示一个缺失的颜色对象，用于 `SolidColor` 对象中。

另请参阅 [`CMYKColor`]、[`GrayColor`]、[`HSBColor`]、[`LabColor`]、[`RGBColor`]。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `typename` | `string` | 只读。引用的 `noColor` 对象的类名。 |

### Notifier

一个事件处理程序对象，用于告知脚本在指定事件发生时执行特定代码。必须使用 `Application.notifiersEnabled` 属性启用通知器。通过 `Application.notifiers` 集合访问。

**注意：** 脚本内部发生的事件通常不会触发通知器，因为它们发生在“播放脚本”事件内部。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `event` | `string` | 只读。事件标识符，一个四字符代码或唯一字符串。<br>四字符代码列表，请参阅[附录 A：事件 ID 代码](https://helpx.adobe.com/photoshop/using/appendix-event-id-codes.html)。 |
| `eventClass` | `string` | 只读。类标识符，一个四字符代码或唯一字符串。<br>当一个事件适用于多种类型的对象时，可使用此属性来区分此通知器适用于哪个对象。例如，Make 事件（"Mk "）可应用于文档（"Dcmn"）、通道（"Chnl"）和其他对象。 |
| `eventFile` | [`File`](https://helpx.adobe.com/photoshop/using/scripting-reference.html#file) | 只读。事件发生并激活通知器时要执行的文件的路径。 |
| `parent` | [`Application`](https://helpx.adobe.com/photoshop/using/scripting-reference.html#application) | 只读。包含的应用程序。 |
| `typename` | `string` | 只读。引用对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
|---|---|---|---|
| `remove()` |  |  | 删除此对象。<br>您也可以通过从 Photoshop 偏好设置文件夹中删除名为 `Script Events Manager.xml` 的文件，从脚本事件管理器下拉列表中移除一个 `Notifier` 对象。有关更多信息，请参阅 Adobe Photoshop CS6 帮助。 |

### Notifiers

文档中的 [`Notifier`](https://helpx.adobe.com/photoshop/using/notifiers.html) 对象集合。通过 [`Application.notifiers`](https://helpx.adobe.com/photoshop/using/notifiers.html) 集合属性访问。例如：

```javascript
var notRef = app.notifiers.add("OnClickGoButton", eventFile)
```

必须使用 [`Application.notifiersEnabled`](https://helpx.adobe.com/photoshop/using/notifiers.html) 属性启用通知器。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `length` | `number` | 只读。`notifiers` 集合中的元素数量。 |
| `parent` | [`Application`](https://helpx.adobe.com/photoshop/using/application.html) | 只读。`notifiers` 对象的容器。 |
| `typename` | `string` | 只读。引用的 `notifiers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| --- | --- | --- | --- |
| `add(event, eventFile[, eventClass])` | `string`<br>[`File`](https://helpx.adobe.com/photoshop/using/file-object.html)<br>`string` | [`Notifier`](https://helpx.adobe.com/photoshop/using/notifier.html) | 创建一个通知器对象并将其添加到此集合中。<br><br>`event` 定义事件的类 ID：使用一个 4 字符代码或唯一字符串。参阅[附录 A：事件 ID 代码](https://helpx.adobe.com/photoshop/using/notifiers.html)。<br><br>`eventFile` 定义事件发生时执行的脚本文件。<br><br>当一个事件适用于多种类型的对象时，使用 `eventClass`（一个 4 字符 ID 或唯一字符串）来区分此通知器适用于哪个对象。例如，Make 事件（`"Mk "`）适用于文档（`"Dcmn"`）、通道（`"Chnl"`）和其他对象。<br><br>**提示：** 使用 4 字符 ID 代码指定事件或事件类时，请在代码中省略单引号。 |
| `removeAll()` |  |  | 从 `notifiers` 集合中移除所有成员对象。<br><br>您也可以通过从 Photoshop 偏好设置文件夹中删除名为 `Script Events Manager.xml` 的文件，从脚本事件管理器下拉列表中移除一个 `notifier` 对象。有关更多信息，请参阅 Adobe Photoshop CS6 帮助。 |

### PathItem

一个路径或绘图对象，例如形状的轮廓或直线或曲线，它包含定义其几何形状的子路径。

通过 `Document.pathItems` 属性中的集合访问。例如，这会选择一个命名的路径项目：

```javascript
var currentPathItem = app.activeDocument.pathItems.getByName("myPath");

currentPathItem.select()
```




通过向`PathItems.add()`方法传递一组`SubPathInfo`对象来创建这些对象。此方法为每个`SubPathInfo`对象创建一个`SubPathItem`对象，并为所有子路径表示的路径创建并返回一个新的`PathItem`对象。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `kind` | `PathKind` | 可读写。类型。 |
| `name` | `string` | 可读写。名称。 |
| `parent` | `Document` | 只读。包含的文档。 |
| `subPathItems` | `SubPathItems` | 只读。包含的子路径对象。 |
| `typename` | `string` | 只读。引用的`pathItem`对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `deselect()` |  |  | 取消选择此`pathItem`对象。 |
| `duplicate(name)` | `string` |  | 用新名称复制此`pathItem`对象。 |
| `fillPath([fillColor] [, mode] [, opacity] [, preserveTransparency] [, feather] [, wholePath] [, antiAlias])` | `SolidColor`, `ColorBlendMode`, `number [0..100]`, `boolean`, `number [0.0..250.0]`, `boolean`, `boolean` |  | 填充此路径包围的区域。不透明度是百分比。羽化值以像素为单位。如果`wholePath`为`true`，则在填充时使用所有子路径（默认：`true`）。 |

```javascript
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
| `makeClippingPath([flatness])` | 数字 `[0.2..100]` |  | 将此路径设置为当前文档的裁剪路径。`flatness`参数告知 PostScript 打印机如何近似路径中的曲线。 |
| `makeSelection([feather] [, antiAlias] [, operation])` | 数字 `[0.0..250.0]`<br>布尔值<br>`SelectionType` |  | 创建一个[选区](https://www.adobe.com/devnet/photoshop/scripting.html)对象，其边界由此路径定义。`feather`参数以像素为单位。 |
| `remove()` |  |  | 删除此对象。 |
| `select()` |  |  | 将此`PathItem`对象设置为当前活动或选中的路径。 |
| `strokePath([tool] [, simulatePressure])` | `ToolType`<br>布尔值 |  | 使用指定工具对路径进行描边。 |

#### PathItem 示例脚本

以下脚本创建一个包含三段的路径：两条对角线构成一个 V 形，V 形上方有一条曲线，使其看起来像一个二维的冰淇淋甜筒。

##### Paths.jsx

```javascript
// 保存当前的首选项设置

var startRulerUnits = app.preferences.rulerUnits

var startTypeUnits = app.preferences.typeUnits

var startDisplayDialogs = app.displayDialogs

// 将 Adobe Photoshop CS6 设置为使用像素单位并禁止显示对话框

app.preferences.rulerUnits = Units.PIXELS

app.preferences.typeUnits = TypeUnits.PIXELS

app.displayDialogs = DialogModes.NO

// 首先关闭所有打开的文档

while (app.documents.length) {

    app.activeDocument.close()

}

// 创建一个用于操作的新文档

var docRef = app.documents.add(5000, 7000, 72, "Simple Line")

//线1--它是一条直线，所以每个点的锚点、左侧方向和右侧方向的坐标都相同

var lineArray = new Array()

lineArray[0] = new PathPointInfo

lineArray[0].kind = PointKind.CORNERPOINT

lineArray[0].anchor = Array(100, 100)

lineArray[0].leftDirection = lineArray[0].anchor

lineArray[0].rightDirection = lineArray[0].anchor

lineArray[1] = new PathPointInfo

lineArray[1].kind = PointKind.CORNERPOINT

lineArray[1].anchor = Array(150, 200)

lineArray[1].leftDirection = lineArray[1].anchor

lineArray[1].rightDirection = lineArray[1].anchor

var lineSubPathArray = new Array()

lineSubPathArray[0] = new SubPathInfo()

lineSubPathArray[0].operation = ShapeOperation.SHAPEXOR

lineSubPathArray[0].closed = false

lineSubPathArray[0].entireSubPath = lineArray
```

```javascript
// 线2

var lineArray2 = new Array()

lineArray2[0] = new PathPointInfo

lineArray2[0].kind = PointKind.CORNERPOINT

lineArray2[0].anchor = Array(150, 200)

lineArray2[0].leftDirection = lineArray2[0].anchor

lineArray2[0].rightDirection = lineArray2[0].anchor

lineArray2[1] = new PathPointInfo

lineArray2[1].kind = PointKind.CORNERPOINT

lineArray2[1].anchor = Array(200, 100)

lineArray2[1].leftDirection = lineArray2[1].anchor

lineArray2[1].rightDirection = lineArray2[1].anchor

lineSubPathArray[1] = new SubPathInfo()

lineSubPathArray[1].operation = ShapeOperation.SHAPEXOR

lineSubPathArray[1].closed = false

lineSubPathArray[1].entireSubPath = lineArray2
```

```javascript
//冰淇淋曲线

//它是一条曲线，所以有三个点，而不是两个

//中间点（lineArray3[1]）的坐标不同。

//左侧方向点位于屏幕上锚点的“上方”。

//右侧方向点位于锚点的“下方”

//你可以修改这些点的坐标，以观察曲线是如何工作的...

var lineArray3 = new Array()

lineArray3[0] = new PathPointInfo

lineArray3[0].kind = PointKind.CORNERPOINT

lineArray3[0].anchor = Array(200, 100)

lineArray3[0].leftDirection = lineArray3[0].anchor

lineArray3[0].rightDirection = lineArray3[0].anchor

lineArray3[1] = new PathPointInfo

lineArray3[1].kind = PointKind.CORNERPOINT

lineArray3[1].anchor = Array(150, 50)

lineArray3[1].leftDirection = Array(100, 50)

lineArray3[1].rightDirection = Array(200, 50)

lineArray3[2] = new PathPointInfo

lineArray3[2].kind = PointKind.CORNERPOINT

lineArray3[2].anchor = Array(100, 100)

lineArray3[2].leftDirection = lineArray3[2].anchor

lineArray3[2].rightDirection = lineArray3[2].anchor
```

```javascript
lineSubPathArray[2] = new SubPathInfo()

lineSubPathArray[2].operation = ShapeOperation.SHAPEXOR

lineSubPathArray[2].closed = false

lineSubPathArray[2].entireSubPath = lineArray3

//创建路径项

var myPathItem = docRef.pathItems.add("A Line", lineSubPathArray)

// 描边路径以便可视化

myPathItem.strokePath(ToolType.BRUSH)

// 重置应用程序首选项

preferences.rulerUnits = startRulerUnits

preferences.typeUnits = startTypeUnits

displayDialogs = startDisplayDialogs
```

### PathItems

文档中`PathItem`对象的集合。

通过`Document.pathItems`集合属性访问。例如，以下代码使用先前定义的子路径集合创建一个新的路径项：

```javascript
app.activeDocument.pathItems.add("myPath", lineSubPathInfoArray);
```




## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `length` | `数字` | 只读。`pathItems` 集合中 `PathItem` 对象的数量。 |
| `parent` | `Document` | 只读。`pathItems` 对象的容器对象。 |
| `typename` | `字符串` | 只读。所引用 `pathItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `add` (`name`, `entirePath`) | `字符串`<br>`SubPathInfo` 数组 | `PathItem` | 创建一个新的路径项对象并将其添加到此集合中。<br>为 `entirePath` 中提供的每个 `SubPathInfo` 对象创建一个新的 `SubPathItem` 对象，并将这些 `SubPathItem` 对象添加到返回的 `PathItem` 的 `subPathItems` 集合中。 |
| `getByName` (`name`) | `字符串` | `PathItem` | 获取 `pathItems` 集合中具有指定名称的第一个元素。 |
| `removeAll`() |  |  | 从 `pathItems` 集合中移除所有 `PathItem` 对象。 |

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
};

drawLine(app.activeDocument, [100, 100], [200, 200]);
```




### PathPoints

一个由 [PathPoint](https://example.com) 对象组成的集合，用于定义子路径，保存在 [SubPathItem.pathPoints](https://example.com) 属性中。

#### 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。集合中元素的数量。 |
| `parent` | `SubPathItem` | 只读。包含该路径点的子路径对象。 |
| `typename` | `string` | 只读。引用的 `PathPoints` 对象的类名。 |

### PDFOpenOptions

使用 [Application.open()](Application.open()) 方法在通用 Adobe PDF 格式中打开文档的选项。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `antiAlias` | `boolean` | 读写。True 表示使用抗锯齿。 |
| `bitsPerChannel` | `BitsPerChannelType` | 读写。每个通道的位数。 |
| `constrainProportions` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `cropPage` | `CropToType` | 读写。要使用的裁剪方法。 |
| `height` | `UnitValue` | 在 Adobe Photoshop CS6 中已弃用。 |
| `mode` | `OpenDocumentMode` | 读写。要使用的颜色模型。 |
| `name` | `string` | 读写。对象的名称。 |
| `page` | `number` | 读写。要打开的文档的页面或图像，具体取决于 `usePageNumber` 的值。 |
| `resolution` | `number` | 读写。文档的分辨率（以每英寸像素数为单位）。 |
| `suppressWarnings` | `boolean` | 读写。True 表示在打开文档时抑制警告。 |
| `typename` | `string` | 只读。引用的 `PDFOpenOptions` 对象的类名。 |
| `usePageNumber` | `boolean` | 读写。当为 true 时，`page` 属性指的是页码；当为 false 时，它指的是图像编号。 |
| `width` | `UnitValue` | 在 Adobe Photoshop CS6 中已弃用。 |

### PDFSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 Adobe PDF 格式的选项。

#### 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `alphaChannels` | `boolean` | 读写。True 表示将 Alpha 通道随文件一起保存。 |
| `annotations` | `boolean` | 读写。True 表示将批注随文件一起保存。 |
| `colorConversion` | `boolean` | 读写。True 表示将颜色配置文件转换为目标配置文件。 |
| `convertToEightBit` | `boolean` | 读写。True 表示将 16 位图像转换为 8 位，以提高与其他应用程序的兼容性。 |
| `description` | `string` | 读写。要使用的保存选项的说明。 |
| `destinationProfile` | `string` | 读写。最终 RGB 或 CMYK 输出设备的说明，例如显示器或印刷标准。 |
| `downgradeColorProfile` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `downSample` | `PDFResample` | 读写。要使用的向下采样方法。 |
| `downSampleSize` | `number` | 读写。如果图像超过每英寸像素数限制，则要向下采样的图像大小。 |
| `downSampleSizeLimit` | `number` | 读写。将向下采样或子采样限制为超过此每英寸像素数值的图像。 |
| `embedColorProfile` | `boolean` | 读写。True 表示将颜色配置文件嵌入文档中。 |
| `embedFonts` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `embedThumbnail` | `boolean` | 读写。True 表示在 Adobe PDF 文件中包含一个小预览图像。 |
| `encoding` | `PDFEncoding` | 读写。要使用的压缩类型（默认：`PDFEncoding.PDFZIP`）。 |
| `interpolation` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `jpegQuality` | `number [0..12]` | 读写。生成图像的质量，与压缩量成反比。仅当 `encoding = PDFEncoding.JPEG` 时有效。 |
| `layers` | `boolean` | 读写。True 表示保存文档的图层。 |
| `optimizeForWeb` | `boolean` | 读写。True 表示提高 PDF 文件在 Web 服务器上的性能。 |
| `outputCondition` | `string` | 读写。一个可选的注释字段，用于插入输出条件的描述。文本存储在 PDF/X 文件中。 |
| `outputConditionID` | `string` | 读写。输出条件的标识符。 |
| `PDFCompatibility` | `PDFCompatibility` | 读写。使文档兼容的 PDF 版本。 |
| `PDFStandard` | `PDFStandard` | 读写。使文档兼容的 PDF 标准。 |
| `preserveEditing` | `boolean` | 读写。True 表示在 Adobe Photoshop CS6 中重新打开 PDF 时，保留原生 Photoshop 数据完好无损。 |
| `presetFile` | `string` | 读写。用于设置的预设文件。注意：此选项会覆盖其他设置。 |
| `profileInclusionPolicy` | `boolean` | 读写。True 表示显示要包含哪些配置文件。 |
| `registryName` | `string` | 读写。输出条件注册的 URL。 |
| `spotColors` | `boolean` | 读写。True 表示保存专色。 |
| `tileSize` | `number` | 读写。压缩选项。仅当 `encoding = PDFEncoding.JPEG2000` 时有效。 |
| `transparency` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `typename` | `string` | 只读。引用的 `PDFSaveOptions` 对象的类名。 |
| `useOutlines` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `vectorData` | `boolean` | 在 Adobe Photoshop CS6 中已弃用。 |
| `view` | `boolean` | 读写。True 表示在 Adobe Acrobat 中打开保存的 PDF。 |

### PhotoCDOpenOptions

在 Adobe Photoshop CS6 中已弃用。Kodak PhotoCD 现在可以在 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中找到。

使用 [Application.open()](Application.open()) 方法在 Kodak Photo CD (PCD) 格式（包括来自 Pro Photo CD 光盘的高分辨率文件）中打开文档的选项。

#### 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `colorProfileName` | `string` | 读写。读取图像时要使用的配置文件。 |
| `colorSpace` | `PhotoCDColorSpace` | 读写。图像的颜色空间。 |
| `orientation` | `Orientation` | 读写。图像方向。 |
| `pixelSize` | `PhotoCDSize` | 读写。图像尺寸。 |
| `resolution` | `number` | 读写。图像分辨率（以每英寸像素数为单位）。 |
| `typename` | `string` | 只读。引用的 `PhotoCDOpenOptions` 对象的类名。 |

### PhotoshopSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#Document.html#saveAs) 方法将文档保存为 PSD 格式的选项。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | `boolean` | 读写。True 表示保存 Alpha 通道。 |
| `annotations` | `boolean` | 读写。True 表示保存批注。 |
| `embedColorProfile` | `boolean` | 读写。True 表示将颜色配置文件嵌入文档中。 |
| `layers` | `boolean` | 读写。True 表示保留图层。 |
| `spotColors` | `boolean` | 读写。True 表示保存专色。 |
| `typename` | `string` | 只读。引用的 `PhotoshopSaveOptions` 对象的类名。 |

### PICTFileSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 PICT 格式的选项。

#### 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | `boolean` | 读写。True 表示保存 Alpha 通道。 |
| `compression` | `PICTCompression` | 读写。要使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | `boolean` | 读写。True 表示将颜色配置文件嵌入文档中。 |
| `resolution` | `PICTBitsPerPixel` | 读写。每像素的位数。 |
| `typename` | `string` | 只读。引用的 `PICTFileSaveOptions` 对象的类名。 |

### PICTResourceSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 PICT Resource 文件时的选项。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为 true 时保存 Alpha 通道。 |
| `compression` | `PICTCompression` | 读写。使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | 布尔值 | 读写。为 true 时在文档中嵌入颜色配置文件。 |
| `name` | 字符串 | 读写。PICT 资源的名称。 |
| `resolution` | `PICTBitsPerPixel` | 读写。每像素位数。 |
| `resourceID` | 数字 | 读写。PICT 资源的 ID（默认：128）。 |
| `typename` | 字符串 | 只读。引用的 `PICTResourceSaveOptions` 对象的类名。 |

### PicturePackageOptions

使用 `Application.makePicturePackage()` 创建的图片包的选项。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `content` | `PicturePackageTextType` | 读写。内容信息（默认：`PicturePackageTextType.NONE`）。 |
| `flatten` | `布尔值` | 读写。为 true 时，最终文档中的所有图层将被拼合（默认：`true`）。 |
| `font` | `GalleryFontType` | 读写。用于安全文本的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `数字` | 读写。用于安全文本的字体大小（默认：`12`）。 |
| `layout` | `字符串` | 读写。用于生成图片包的版面（默认：`"(2) 5x7"`）。 |
| `mode` | `NewDocumentMode` | 读写。用作文档模式的颜色配置文件（默认：`NewDocumentMode.RGB`）。 |
| `opacity` | `数字` | 读写。网页安全不透明度（百分比）（默认：`100`）。 |
| `resolution` | `数字` | 读写。文档的分辨率（像素/英寸）（默认：`72.0`）。 |
| `text` | `字符串` | 读写。图片包自定义文本。仅当 `content = PicturePackageType.USER` 时有效。 |
| `textColor` | `RGBColor` | 读写。用于安全文本的颜色。 |
| `textPosition` | `GallerySecurityTextPositionType` | 读写。安全文本位置（默认：`GallerySecurityTextPositionType.CENTERED`）。 |
| `textRotate` | `GallerySecurityTextRotateType` | 读写。安全文本的方向（默认：`GallerySecurityTextRotateType.ZERO`）。 |
| `typename` | `字符串` | 只读。引用的 `PicturePackageOptions` 对象的类名。 |

### PixarSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法将文档保存为 Pixar 格式时的选项。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `alphaChannels` | `布尔值` | 读写。为 true 时保存 Alpha 通道。 |
| `typename` | `字符串` | 只读。引用的 `PixarSaveOptions` 对象的类名。 |

### PNGSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 PNG 格式时的选项。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `compression` | `数字 [0..9]` | 读写。压缩值（默认：0）。 |
| `interlaced` | `布尔值` | 读写。为 true 时交错行（默认：`false`）。 |
| `typename` | `字符串` | 只读。引用的 `PNGSaveOptions` 对象的类名。 |

### 偏好设置

表示 Photoshop 的应用程序首选项。通过 [Application.preferences](https://helpx.adobe.com/photoshop/using/preferences.html) 属性访问此对象。例如：

```javascript
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
```

在此对象中设置值等同于在 Adobe Photoshop CS6 应用程序中选择**编辑 > 首选项**（在 Windows 上）或 **Photoshop > 首选项**（在 Mac OS 上）。有关各个设置的说明，请参阅 Adobe Photoshop CS6 帮助。

#### 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `additionalPluginFolder` | [File](https://helpx.adobe.com/photoshop/using/scripting-tools.html) | 读写。附加插件文件夹的路径。仅当 [useAdditionalPluginFolder](https://helpx.adobe.com/photoscript/using/scripting-tools.html) = true 时有效。 |
| `appendExtension` | [SaveBehavior](https://helpx.adobe.com/photoscript/using/scripting-tools.html) | 读写。在 Windows 上写入文件扩展名的首选策略。 |
| `askBeforeSavingLayeredTIFF` | 布尔值 | 读写。为 true 时，当以 TIFF 格式保存文件时，会要求用户验证图层保留选项。 |
| `autoUpdateOpenDocuments` | 布尔值 | 读写。为 true 时自动更新打开的文档。 |
| `beepWhenDone` | 布尔值 | 读写。为 true 时，进程完成时会发出蜂鸣声。 |
| `colorChannelsInColor` | 布尔值 | 读写。为 true 时，以彩色显示通道调板中的分量通道。 |
| `colorPicker` | [ColorPicker](https://helpx.adobe.com/photoscript/using/scripting-tools.html) | 读写。首选的颜色选择工具。 |



| `columnGutter` | 数字 [0.1..600.0] | 读写。栏间距的宽度（以点为单位）。 |
| `columnWidth` | 数字 [0.1..600.0] | 读写。栏宽（以点为单位）。 |
| `createFirstSnapshot` | 布尔值 | 读写。为 `true` 时，创建新文档时自动制作第一个快照。 |
| `dynamicColorSliders` | 布尔值 | 读写。为 `true` 时，颜色调板中会出现动态颜色滑块。 |
| `editLogItems` | `EditLogItemsType` | 读写。历史记录日志的首选详细程度。仅当 `useHistoryLog` = `true` 时有效。 |
| `exportClipboard` | `布尔值` | 读写。为 `true` 时，在退出应用程序后，剪贴板上会保留 Adobe Photoshop CS6 内容。 |
| `fontPreviewSize` | `FontPreviewType` | 读写。用于类型工具字体菜单中字体预览的首选字体大小。 |
| `fullSizePreview` | `布尔值` | 读写。为 `true` 时，将图像预览显示为全尺寸图像；为 `false` 时，显示缩略图（仅限 Mac OS）。 |
| `gamutWarningOpacity` | `数字 [0..100]` | 读写。不透明度值（百分比）。 |
| `gridSize` | `GridSize` | 读写。网格中方块的首选大小。 |
| `gridStyle` | `GridLineStyle` | 读写。非打印网格线的首选格式化样式。 |
| `gridSubDivisions` | `数字 [1..100]` | 读写。网格细分数量。 |
| `guideStyle` | `GuideLineStyle` | 读写。非打印参考线的首选格式化样式。 |
| `iconPreview` | `布尔值` | 读写。为 `true` 时使用图标预览（仅限 Mac OS）。 |
| `imageCacheLevels` | `数字 [1..8]` | 读写。缓存中保留的图像数量。 |
| `imagePreviews` | `SaveBehavior` | 读写。在 Windows 上写入图像预览的首选策略。 |
| `interpolation` | `ResampleMethod` | 读写。在图像重新采样或调整大小时，用于为任何新像素分配颜色值的方法。 |
| `keyboardZoomResizesWindows` | `布尔值` | 读写。为 `true` 时，使用键盘快捷键放大或缩小时会自动调整窗口大小。 |
| `macOSThumbnail` | `布尔值` | 读写。为 `true` 时，保存图像时创建缩略图（仅限 Mac OS）。 |
| `maximizeCompatibility` | `QueryStateType` | 读写。打开 PSD 文件时，检查是否最大化兼容性的首选策略。 |
| `maxRAMUse` | `数字 [5..100]` | 读写。Adobe Photoshop CS6 使用的最大可用 RAM 百分比（5 - 100）。 |
| `nonLinearHistory` | `布尔值` | 读写。为 `true` 时允许非线性历史记录。 |
| `numberOfHistoryStates` | 数字 | 读写。要保留的历史记录状态数。 |
| `otherCursors` | `OtherPaintingCursors` | 读写。用于某些工具的首选指针类型。 |
| `paintingCursors` | `PaintingCursors` | 读写。用于某些工具的首选指针类型。 |
| `parent` | `Application` | 读写。包含的应用程序。 |
| `pixelDoubling` | 布尔值 | 读写。为 `true` 时，将分辨率减半（像素大小加倍）以使预览显示更快。 |
| `pointSize` | `PointType` | 读写。点/派卡大小。 |
| `recentFileListLength` | 数字 [0..30] | 读写。最近文件列表中的项目数。 |
| `rulerUnits` | `Units` | 读写。脚本系统在接收和返回值时将使用的单位。 |
| `saveLogItems` | `SaveLogItemsType` | 读写。保存历史记录项目时，历史记录日志数据的首选位置。 |
| `saveLogItemsFile` | `File` | 读写。当首选位置是文件时，历史记录日志文件的路径。 |
| `savePaletteLocations` | 布尔值 | 读写。为 `true` 时，将新的调板位置设为默认位置。 |
| `showAsianTextOptions` | 布尔值 | 读写。为 `true` 时，在段落调板中显示亚洲文本选项。 |
| `showEnglishFontNames` | 布尔值 | 读写。为 `true` 时，以英文列出亚洲字体名称。 |
| `showSliceNumber` | 布尔值 | 读写。为 `true` 时，使用切片工具时在文档窗口中显示切片编号。 |
| `showToolTips` | 布尔值 | 读写。为 `true` 时，鼠标悬停时显示弹出定义。 |
| `smartQuotes` | 布尔值 | 读写。为 `true` 时使用弯引号；为 `false` 时使用直引号。 |
| `textFontSize` | `FontSize` | 读写。用于面板和对话框的小字体大小。 |
| `typename` | 字符串 | 只读。引用的 `preferences` 对象的类名。 |
| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `typeUnits` | `TypeUnits` | 读写。文本字符测量的首选单位。 |
| `useAdditionalPluginFolder` | `boolean` | 读写。`True` 表示使用与其他应用程序一起存储的兼容插件的附加文件夹。 |
| `useHistoryLog` | `boolean` | 读写。`True` 表示为历史记录状态创建日志文件。 |
| `useLowerCaseExtension` | `boolean` | 读写。`True` 表示使用小写文件扩展名。 |
| `useShiftKeyForToolSwitch` | `boolean` | 读写。`True` 表示启用循环切换一组隐藏工具。 |
| `useVideoAlpha` | `boolean` | 读写。`True` 表示启用 Adobe Photoshop CS6 向计算机的视频板发送透明度信息。（需要硬件支持。） |
| `windowsThumbnail` | `boolean` | 读写。`True` 表示在 Windows 中保存图像时创建缩略图。（需要硬件支持。） |

### PresentationOptions

使用 `Application.makePDFPresentation()` 创建的 Adobe PDF 演示文稿的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `autoAdvance` | `boolean` | 读写。`True` 表示在查看演示文稿时自动切换图像（默认：`true`）。<br><br>仅当 `presentation` = `true` 时有效。 |
| `includeFilename` | `boolean` | 读写。`True` 表示包含图像的文件名（默认：`false`）。 |
| `interval` | `number [1..60]` | 读写。自动切换视图之前的秒数（默认：`5`）。<br><br>仅当 `autoAdvance` = `true` 时有效。 |
| `loop` | `boolean` | 读写。`True` 表示在最后一页之后重新开始演示（默认：`false`）。<br><br>仅当 `autoAdvance` = `true` 时有效。 |
| `magnification` | `MagnificationType` | 读写。查看图像时使用的放大类型。 |
| `PDFFileOptions` | `PDFSaveOptions` | 读写。创建 PDF 文件时使用的选项。 |
| `presentation` | `boolean` | 读写。`True` 表示输出将是演示文稿（默认：`false`）；当为 `false` 时，输出是多页文档。 |
| `transition` | `TransitionType` | 读写。从一张图像过渡到下一张图像的方法（默认：`TransitionType.NONE`）。<br><br>仅当 `autoAdvance` = `true` 时有效。 |
| `typename` | `string` | 只读。引用的 `PresentationOptions` 对象的类名。 |

### RawFormatOpenOptions

使用 `Application.open()` 方法打开 RAW 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `bitsPerChannel` | `number` | 读写。每个通道的位数。<br><br>唯一有效的值是 `BitsPerChannelType.EIGHT` 或 `BitsPerChannelType.SIXTEEN`。 |
| `byteOrder` | `ByteOrder` | 读写。读取多字节值的顺序。<br><br>仅当 `bitsPerChannel` = `BitsPerChannelType.SIXTEEN` 时有效。 |
| `channelNumber` | `number` `[1..56]` | 读写。图像中的通道数。该值不能超过图像中的通道数。<br><br>当 `bitsPerChannel` = `BitsPerChannelType.SIXTEEN` 时，唯一有效的值是 1、3 或 4。 |
| `headerSize` | `number` `[0..19199999]` | 读写。在实际图像信息开始之前出现在文件中的信息字节数；即，在文件开头作为占位符插入的零的数量。 |
| `height` | `number` | 读写。图像高度（以像素为单位）。 |
| `interleaveChannels` | `boolean` | 读写。`True` 表示顺序存储颜色值。 |
| `retainHeader` | `boolean` | 读写。`True` 表示在保存时保留标头。<br><br>仅当 `headerSize` 为 1 或更大时有效。 |
| `typename` | `string` | 只读。引用的 `RawFormatOpenOptions` 对象的类名。 |
| `width` | `number` | 读写。图像宽度（以像素为单位）。 |

### RawSaveOptions

使用 `Document.saveAs()` 方法以 RAW 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | `boolean` | 读写。`True` 表示应保存 Alpha 通道。 |
| `spotColors` | `boolean` | 读写。`True` 表示应保存专色。 |
| `typename` | `string` | 只读。引用的 `RawSaveOptions` 对象的类名。 |

### RGBColor

定义 RGB 颜色，用于 `SolidColor` 对象。

另请参阅 `CMYKColor`、`GrayColor`、`HSBColor`、`LabColor`、`NoColor`。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `blue` | `number [0..255]` | 读写。蓝色值（默认：255）。 |
| `green` | `number [0..255]` | 读写。绿色值（默认：255）。 |
| `hexValue` | `string` | 读写。颜色的十六进制表示。 |
| `red` | `number [0..255]` | 读写。红色值（默认：255）。 |
| `typename` | `string` | 只读。引用的 `RGBColor` 对象的类名。 |

### Selection

文档或图层的选定区域。通过 `Document.selection` 属性访问。例如：

`app.activeDocument.selection.fill(app.foregroundColor)`

许多属性和方法使用 `UnitValue` 类型，该类型将测量值与测量单位组合在一起。有关此类型的信息，请参阅 *JavaScript Tools Guide*。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `bounds` | `array of UnitValue` | 只读。整个选区的边界矩形。 |
| `parent` | `Document` | 只读。对象的容器。 |
| `solid` | `boolean` | 只读。`True` 表示边界矩形是实体。 |
| `typename` | `string` | 只读。引用的 `selection` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `clear()` | | | 清除选区且不将其复制到剪贴板。 |
| `contract(by)` | `UnitValue` | | 按指定量收缩（减少）选区。 |
| `copy([merge])` | `boolean` | | 将选区复制到剪贴板。使用可选参数并设置为 `true` 时，将执行合并复制（选区中的所有可见图层都被复制）。 |
| `cut()` | | | 清除当前选区并将其复制到剪贴板。 |
| `deselect()` | | | 取消选择当前选区。 |
| `expand(by)` | `UnitValue` | | 按指定量扩展选区。 |
| `feather(by)` | `UnitValue` | | 按指定量羽化选区边缘。 |
| `fill(filltype [, mode] [, opacity] [, preserveTransparency])` | `SolidColor`<br>`ColorBlendMode`<br>`number [1..100]`<br>`boolean` | | 填充选区。`opacity` 是一个百分比值。 |
| `grow(tolerance, antiAlias)` | `number`<br>`boolean` | | 扩展选区以包含所有在指定容差范围内的相邻像素。 |
| `invert()` | | | 反转选区（取消选择选区并选择图层或文档的其余部分）。<br>**提示：** 要翻转选区形状，请参阅 `rotate`。 |
| `load(from [, combination] [, inverting])` | `Channel`<br>`SelectionType`<br>`boolean` | | 从指定通道加载选区。 |
| `makeWorkPath([tolerance])` | `number` | | 使此选区项目成为此文档的工作路径。 |
| `resize([horizontal] [, vertical] [, anchor])` | `number`<br>`number`<br>`AnchorPosition` | | 将选定区域调整为指定的尺寸和锚点位置。 |
| `resizeBoundary([horizontal] [, vertical] [, anchor])` | `number`<br>`number`<br>`AnchorPosition` | | 围绕指定锚点更改选区的大小到指定的尺寸。 |
| `rotate(angle [, anchor])` | `number`<br>`AnchorPosition` | | 围绕指定的锚点按指定角度旋转选区。 |
| `rotateBoundary(angle [, anchor])` | `number`<br>`AnchorPosition` | | 围绕指定锚点旋转选区边界。 |
| `select(region [, type] [, feather] [, antiAlias])` | `array of number`<br>`SelectionType`<br>`number`<br>`boolean` | | 选择指定的区域。<br>`region` 参数是一个包含四个坐标的数组，`[left, top, right, bottom]`。 |
| `selectAll()` | | | 选择整个图层。 |

#### 方法 | 参数类型 | 返回值 | 功能说明（续） |
| :--- | :--- | :--- | :--- |



| `selectBorder` (width) | `UnitValue` | | 仅选择指定宽度的选区边界；后续操作不会影响边界内的选区区域。 |

| `similar` (tolerance, antiAlias) | `number` `boolean` | | 扩展选区以包含整个图像中落在容差范围内的像素。 |

| `smooth` (radius) | `number` | | 清理基于颜色的选区内部或外部遗留的杂散像素（在指定的像素半径范围内）。 |

| `store` (into [, combination]) | `Channel` `SelectionType` | | 将选区保存为通道。 |

| `stroke` (strokeColor, width [, location] [, mode] [, opacity] [, preserveTransparency]) | `SolidColor` `number` `StrokeLocation` `ColorBlendMode` `number` [1..100] `boolean` | | 描边选区边界。`opacity` 是百分比值。 |

| `translate` ([deltaX] [, deltaY]) | `UnitValue` `UnitValue` | | 将整个选区相对于其当前位置移动。 |

| `translateBoundary` ([deltaX] [, deltaY]) | `UnitValue` `UnitValue` | | 将选区边界相对于其当前位置移动。 |

#### 选区示例脚本

以下脚本通过以下步骤创建棋盘格：

- 创建一个 800 x 800 像素的文档。
- 将整个文档划分为 100 x 100 像素的方格。
- 选择第一行中的每隔一个方格，然后调整选择标准以选择下一行中的交替方格。重复此过程，直到选中文档中每隔一个方格。
- 用调色板中的前景色填充选中的方格。
- 反转选区，并用调色板中的背景色填充新选中的方格。
- 取消选择方格以移除选区轮廓（即“蚂蚁线”）。

```
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CS6 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

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
app.displayDialogs = startDisplayDialogs

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

### `SGIRGBSaveOptions`

使用 `Document.saveAs()` 方法将文档保存为 SGIRGB 格式的选项。

**注意：** SGIRGB 格式不会随 Adobe Photoshop CS6 自动安装。

## 属性

| 属性 | 值类型 | 说明 |

| :--- | :--- | :--- |
| `alphaChannels` | `boolean` | 读写。为 `true` 表示保存 Alpha 通道。 |
| `spotColors` | `boolean` | 读写。为 `true` 表示保存专色。 |
| `typename` | `string` | 只读。引用的 `SGIRGBSaveOptions` 对象的类名。 |

### `SolidColor`

文档中使用的颜色定义。将一种颜色映射到所有可用颜色模型中的等效值。

- 用于 `Application.backgroundColor` 和 `foregroundColor` 属性，`Channel.color`，`ColorSampler.color` 以及 `TextItem.color`。
- 传递给 `PathItem.fillPath()`、`Selection.fill()` 和 `Selection.stroke()`。

## 属性

| 属性 | 值类型 | 说明 |

| :--- | :--- | :--- |
| `cmyk` | `CMYKColor` | 读写。CMYK 颜色模式。 |
| `gray` | `GrayColor` | 读写。灰度颜色模式。 |
| `hsb` | `HSBColor` | 读写。HSB 颜色模式。 |
| `lab` | `LabColor` | 读写。LAB 颜色模式。 |
| `model` | `ColorModel` | 读写。颜色模型。 |
| `nearestWebColor` | `RGBColor` | 只读。与当前颜色最接近的 Web 颜色。 |
| `rgb` | `RGBColor` | 读写。RGB 颜色模式。 |
| `typename` | `string` | 只读。引用的 `SolidColor` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |

| :--- | :--- | :--- | :--- |
| `isEqual` (color) | `SolidColor` | `boolean` | 如果 `SolidColor` 对象在视觉上等于指定的颜色，则为 `true`。 |

### `SubPathInfo`

一个 `PathPoint` 对象数组，描述路径的直线或曲线段，用于创建 `SubPathItem`。

将这些对象的数组传递给 `PathItems.add()` 方法。此方法为每个 `SubPathInfo` 对象创建一个 `SubPathItem` 对象，并为所有子路径表示的路径创建并返回一个新的 `PathItem` 对象。

- 使用 `SubPathInfo` 创建子路径；属性可写。
- 使用 `SubPathItem` 对象检索有关现有子路径的信息。属性为只读。

## 属性

| 属性 | 值类型 | 说明 |

| :--- | :--- | :--- |
| `closed` | `boolean` | 读写。如果路径描述的是一个封闭区域，则为 `true`。 |
| `entireSubPath` | `PathPoint` 数组 | 读写。 |
| `operation` | `ShapeOperation` | 读写。子路径对其他子路径的操作。指定如果目标路径已有选区时如何组合形状。 |
| `typename` | `string` | 只读。引用的 `SubPathInfo` 对象的类名。 |

### `SubPathItem`

表示一个子路径；子路径的集合构成一个 `PathItem`。

通过将 `SubPathInfo` 对象传递给 `PathItems.add()` 方法来创建这些对象。此方法为每个 `SubPathInfo` 对象创建一个 `SubPathItem` 对象，并为所有子路径表示的路径创建并返回一个新的 `PathItem` 对象。在 `PathItem.subPathItems` 集合中访问这些对象。

- 使用 `SubPathItem` 对象检索有关现有子路径的信息。属性为只读。
- 使用 `SubPathInfo` 创建子路径；属性可写。

## 属性

| 属性 | 值类型 | 说明 |

| :--- | :--- | :--- |
| `closed` | `boolean` | 只读。如果路径是封闭的，则为 `true`。 |
| `operation` | `ShapeOperation` | 只读。此对象与另一个 `SubPathItem` 对象相交时的行为。指定如果目标路径已有选区时如何组合形状。 |
| `parent` | `PathItem` | 只读。对象的容器。 |
| `pathPoints` | `PathPoints` | 只读。`PathPoints` 集合。 |
| `typename` | `string` | 只读。引用的 `SubPathItem` 对象的类名。 |

### `SubPathItems`

由构成 `PathItem` 的 `SubPathItem` 对象组成的集合。可通过 `PathItem.subPathItems` 集合属性访问此对象。

- 使用 `SubPathInfo` 创建子路径；其属性为可写。
- 使用 `SubPathItem` 对象检索有关现有子路径的信息。其属性为只读。

## 属性

| 属性 | 值类型 | 描述 |

| :--- | :--- | :--- |
| `length` | `number` | 只读。集合中的元素数量。 |
| `parent` | `PathItem` | 只读。包含的路径项。 |
| `typename` | `string` | 只读。所引用的 `SubPathItems` 对象的类名。 |

### `TargaSaveOptions`

使用 `Document.saveAs()` 方法将文档保存为 TGA (Targa) 格式的选项。

## 属性

| 属性 | 值类型 | 描述 |

| :--- | :--- | :--- |
| `alphaChannels` | `boolean` | 可读写。`True` 表示保存 alpha 通道。 |
| `resolution` | `TargaBitsPerPixels` | 可读写。每像素的位数（默认值：`TargaBitsPerPixels.TWENTYFOUR`）。 |
| `rleCompression` | `boolean` | 可读写。`True` 表示使用 RLE 压缩（默认值：`true`）。 |
| `typename` | `string` | 只读。所引用的 `TargaSaveOptions` 对象的类名。 |

### `TextFont`

描述应用程序可用的字体。可通过 `Application.fonts` 集合访问此对象。例如：

```
var myFont = app.fonts.getByName("ArialMT");
```

## 属性

| 属性 | 值类型 | 描述 |

| :--- | :--- | :--- |
| `family` | `string` | 只读。字体系列。 |
| `name` | `string` | 只读。字体名称。 |
| `parent` | `Application` | 只读。包含的应用程序。 |
| `postScriptName` | `string` | 只读。字体的 PostScript 名称。 |
| `style` | `string` | 只读。字体样式。 |
| `typename` | `string` | 只读。所引用的 `TextFont` 对象的类名。 |

### `TextFonts`

计算机上可用字体的集合。字体由 `TextFont` 对象表示。可通过 `Application.fonts` 集合属性访问此对象。例如，以下代码显示可用字体数量：

```
alert(app.fonts.length);
```

## 属性

| 属性 | 值类型 | 描述 |

| :--- | :--- | :--- |
| `length` | `number` | 只读。集合中的元素数量。 |



| parent | [Application](javascript:void(0)) | 只读。包含的应用程序。 |
| typename | string | 只读。所引用的 `TextFonts` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `getByName(name)` | string | [TextFont](javascript:void(0)) | 获取 `TextFonts` 集合中具有所提供名称的第一个元素。 |

### TextItem

`ArtLayer` 对象中 `kind` 属性为 `LayerKind.TEXT` 的文本。可通过 `ArtLayer.textItem` 属性访问此对象。例如：

```javascript
myLayers[i].textItem.contents = "Layer in " + textArray[i] + " Set Inside "
```

许多属性使用 `UnitValue` 类型，该类型将测量值与测量单位组合在一起。有关此类型的信息，请参阅 *JavaScript Tools Guide*。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `alternateLigatures` | boolean | 可读写。True 表示使用替代连字。注意：替代连字与可选连字相同。有关更多信息，请参阅 Adobe Photoshop CS6 帮助。 |
| `antiAliasMethod` | `AntiAlias` | 可读写。要使用的抗锯齿方法。 |
| `autoKerning` | `AutoKernType` | 可读写。要使用的自动字距调整选项。 |
| `autoLeadingAmount` | `number [0.01..5000.00]` | 可读写。自动（默认）行距的百分比（以点为单位）。仅当 `useAutoLeading = true` 时有效。 |
| `baselineShift` | `UnitValue` | 可读写。文本基线偏移量使用的单位值。 |
| `capitalization` | `TextCase` | 可读写。文本大小写。 |
| `color` | `SolidColor` | 可读写。文本颜色。 |
| `contents` | string | 可读写。图层中的实际文本。 |
| `desiredGlyphScaling` | `number [50..200]` | 可读写。缩放文本字符水平大小的所需量。百分比值；100 时，字符宽度不缩放。仅当 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `minimumGlyphScaling` 和 `maximumGlyphScaling` 值。 |
| `desiredLetterScaling` | `number [100..500]` | 可读写。字母之间的间距量（0 时，字母之间不添加间距）。<br><br>等同于“段落”调板菜单上选择“对齐”时弹出的“对齐”对话框中的字距。<br><br>仅当 [`justification`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/Justification.html) = `Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `minimumLetterScaling` 和 `maximumLetterScaling` 值。 |
| `desiredWordScaling` | `number [0..1000]` | 可读写。单词之间的间距量（百分比）（100 时，单词之间不添加额外间距）。<br><br>等同于“段落”调板菜单上选择“对齐”时弹出的“对齐”对话框中的单词间距。<br><br>仅当 [`justification`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/Justification.html) = `Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要 `minimumWordScaling` 和 `maximumWordScaling` 值。 |
| `direction` | [`Direction`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/enums/Direction.html) | 可读写。文本方向。 |
| `fauxBold` | `boolean` | 可读写。True 表示使用仿粗体（默认值：`false`）。<br><br>将此项设置为 `true` 相当于选择文本并在“字符”调板中单击“仿粗体”。 |
| `fauxItalic` | `boolean` | 可读写。True 表示使用仿斜体（默认值：`false`）。<br><br>将此项设置为 `true` 相当于选择文本并在“字符”调板中单击“仿斜体”。 |
| `firstLineIndent` | [`UnitValue`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/UnitValue.html) `[-1296..1296] points` | 可读写。段落首行缩进的量（单位值）。 |
| `font` | `string` | 可读写。字符的文本字体。使用字体的 PostScript 名称。请参阅 [`TextFont`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/classes/TextFont.html) 并使用 `postScriptName` 属性。 |
| `hangingPunctuation` | `boolean` | 可读写。True 表示使用罗马悬挂标点。 |
| `height` | [`UnitValueX`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/classes/UnitValue.html) | 可读写。段落文本边界框的高度（单位值）。<br><br>仅当 `kind = TextType.PARAGRAPHTEXT` 时有效。 |
| `horizontalScale` | `number [0..1000]` | 可读写。字符的（水平）缩放比例，相对于 [`verticalScale`](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/html/scriptref/properties/verticalScale.html)（百分比值）。 |
| `hyphenateAfterFirst` | `number [1..15]` | 可读写。允许在自动换行时进行连字符断字的起始字母数。 |
| `hyphenateBeforeLast` | `number [1..15]` | 可读写。允许在自动换行时进行连字符断字的末尾字母数。 |
| `hyphenateCapitalWords` | `boolean` | 可读写。设置为 `true` 以允许对首字母大写的单词进行自动换行连字符断字。 |
| `hyphenateWordsLongerThan` | `number [2..25]` | 可读写。单词允许进行自动换行连字符断字所需的最小字母数。 |
| `hyphenation` | `boolean` | 可读写。设置为 `true` 以在自动换行时使用连字符断字。 |
| `hyphenationZone` | `UnitValue [0..720] pica` | 可读写。行末用于触发单词在非两端对齐文本中断开的距离。 |
| `hyphenLimit` | `number` | 可读写。以连字符断字单词结尾的连续行的最大数量。 |
| `justification` | [Justification](https://example.com) | 可读写。段落对齐方式。 |
| `kind` | [TextType](https://example.com) | 可读写。文本换行类型。 |
| `language` | [Language](https://example.com) | 可读写。使用的语言。 |
| `leading` | [UnitValue](https://example.com) | 可读写。行距值。 |
| `leftIndent` | `UnitValue [-1296..1296] points` | 可读写。文本从左缩进的距离。 |
| `ligatures` | `boolean` | 可读写。设置为 `true` 以使用连字。 |
| `maximumGlyphScaling` | `number [50..200]` | 可读写。允许的文本字符水平尺寸的最大缩放量（百分比值；100 表示不缩放字符宽度）。<br><br>仅在 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要提供 `minimumGlyphScaling` 和 `desiredGlyphScaling` 值。 |
| `maximumLetterScaling` | `number [100..500]` | 可读写。允许的字符间最大间距量（百分比值；0 表示不增加字符间距）。<br><br>等效于“段落”面板菜单（选择“对齐”）中的“字符间距调整”对话框中的设置。<br><br>仅在 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要提供 `minimumLetterScaling` 和 `desiredLetterScaling` 值。 |
| `maximumWordScaling` | `number [0..1000]` | 可读写。允许的单词间最大间距量（百分比值；100 表示不增加单词间距）。<br><br>等效于“段落”面板菜单（选择“对齐”）中的“词间距”对话框中的设置。<br><br>仅在 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要提供 `minimumWordScaling` 和 `desiredWordScaling` 值。 |
| `minimumGlyphScaling` | `number [50..200]` | 可读写。允许的文本字符水平尺寸的最小缩放量（百分比值；100 表示不缩放字符宽度）。<br><br>仅在 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要提供 `maximumGlyphScaling` 和 `desiredGlyphScaling` 值。 |
| `minimumLetterScaling` | `number [100..500]` | 可读写。允许的字符间最小间距量（百分比值；0 表示不减少字符间距）。<br><br>等效于“段落”面板菜单（选择“对齐”）中的“字符间距调整”对话框中的设置。<br><br>仅在 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要提供 [`maximumLetterScaling`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) 和 [`desiredLetterScaling`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) 值。 |
| `minimumWordScaling` | `number [0..1000]` | 可读写。允许的单词间最小间距量（百分比值；100 表示不减少单词间距）。<br><br>等效于“段落”面板菜单（选择“对齐”）中的“词间距”对话框中的设置。<br><br>仅在 `justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED` 或 `Justification.RIGHTJUSTIFIED` 时有效。<br><br>使用时，还需要提供 [`maximumWordScaling`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) 和 [`desiredWordScaling`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) 值。 |
| `noBreak` | `boolean` | 可读写。设置为 `true` 以禁止此文本中的换行。<br><br>**提示：** 当为多个连续字符设置为 `true` 时，可能会阻止自动换行，从而导致部分文本无法在屏幕上显示。 |
| `oldStyle` | `boolean` | 可读写。设置为 `true` 以使用旧式字体样式。 |
| `parent` | [`ArtLayer`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) | 可读写。包含此文本的图层。 |
| `position` | `array of` [`UnitValue`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) | 可读写。文本原点的位置。数组成员指定 X 和 Y 坐标。<br><br>等效于使用文本工具在文档中单击一点来创建文本的原点。 |
| `rightIndent` | [`UnitValue`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) `[-1296..1296] points` | 可读写。文本从右缩进的距离。 |
| `size` | [`UnitValue`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) | 可读写。以 `UnitValue` 为单位的字体大小。注意：CS3 及更早版本中类型为 `points`。 |
| `spaceAfter` | [`UnitValue`](https://helpx.adobe.com/photoshop/using/scripting-reference.html) `[-1296..1296] points` | 可读写。每个段落后的间距。 |



| 属性 | 值类型 | 描述 |
|---|---|---|
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
| `convertToShape()` |  |  | 将文本图层及其包含的图层转换为形状图层，其中的文本内容会被转换为剪贴路径。 |
| `createPath()` |  |  | 根据实际文本内容（如字母或单词）的轮廓创建剪贴路径。 |

### TiffSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 TIFF 格式时的选项。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `alphaChannels` | `boolean` | 可读写。为 `true` 时保存 Alpha 通道。 |
| `annotations` | `boolean` | 可读写。为 `true` 时保存注释。 |
| `byteOrder` | `ByteOrder` | 可读写。读取文档多字节值的顺序（默认值：在 Mac OS 中为 `ByteOrder.MACOS`，在 Windows 中为 `ByteOrder.IBM`）。 |
| `embedColorProfile` | `boolean` | 可读写。为 `true` 时将颜色配置文件嵌入到文档中。 |
| `imageCompression` | `TIFFEncoding` | 可读写。压缩类型（默认值：`TIFFEncoding.NONE`）。 |
| `interleaveChannels` | `boolean` | 可读写。为 `true` 时，图像中的通道将交错存储。 |
| `jpegQuality` | `number [0..12]` | 可读写。生成图像的质量，与 JPEG 压缩量成反比。<br><br>仅在 `imageCompression` = `TIFFEncoding.JPEG` 时有效。 |
| `layerCompression` | `LayerCompression` | 可读写。保存图层时使用的压缩方法（相对于保存合成数据）。<br><br>仅在 `layers` = `true` 时有效。 |
| `layers` | `boolean` | 可读写。为 `true` 时保存图层。 |
| `saveImagePyramid` | `boolean` | 可读写。为 `true` 时保留多分辨率信息（默认值：`false`）。 |
| `spotColors` | `boolean` | 可读写。为 `true` 时保存专色。 |
| `transparency` | `boolean` | 可读写。为 `true` 时，将透明度作为附加的 Alpha 通道保存，以便在其他应用程序中打开文件时保留透明度。 |
| `typename` | `string` | 只读。引用的 `TiffSaveOptions` 对象的类名。 |

### UnitValue

ExtendScript 定义了 JavaScript 类 `UnitValue`，用于表示带有测量单位的测量值；详情请参见第 32 页的《Adobe Photoshop CS6 中的 JavaScript 支持》。关于这些类的详细参考信息，请参阅《JavaScript 工具指南》。

### xmpMetadata

Camera RAW 图像的 XMP 元数据。

对于 Camera RAW 图像文件，XMP 元数据存储在一个 `sidecar` 文件中，该文件与 RAW 文件位于同一文件夹，具有相同的基本名称，扩展名为 `.xmp`。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `parent` | `Document` | 只读。包含此元数据的文档。 |
| `rawData` | `string` | 可读写。包含 XML（RDF）格式 XMP 元数据的字符串。有关此格式的详细信息，请参阅《XMP 规范》。 |
| `typename` | `string` | 只读。引用的 `xmpMetadata` 对象的类名。 |

## 3 JavaScript 资源

本节描述了 JavaScript 资源，它使得你的 JavaScript 脚本能够像插件一样运行。这包括：

- 能够指定脚本在菜单中作为命令出现的位置。
- 一个术语资源，使脚本能够与动作管理器配合工作，从而允许你的脚本被录制并通过脚本参数进行自动化。
- 一个类别，用于在菜单中对命令进行排序和分组。
- 一个启用字符串，用于指示在给定条件下命令是启用还是禁用。
- 字符串必须符合有效的 XML 语法。例如，`&` 字符将无法工作。请使用 `&amp;`（例如在 enableinfo 块中使用 `&amp;&amp;` 来表示逻辑与）。

### JavaScript 资源语法

JavaScript 资源具有类似 HTML 的语法，每个 `<tag>` 都有一个对应的结束标签 `</tag>`。此资源需要出现在注释中（`/* ... */`），并应定义在脚本文件的顶部（文件的前 10,240 个字符内）。

| 标签 | 描述 |
|---|---|
| `<javascriptresource>` | 资源定义标签。 |
| `<name>` | 出现在 Photoshop 菜单中的命令名称。如果资源中未提供此标签，菜单中命令的名称将默认为脚本的名称。 |
| `<menu>` | 命令出现的菜单。如果未提供此标签，命令将出现在**文件 > 脚本**菜单中。**注意：**目前 `<menu>` 支持的值只有 `automate`、`filter` 和 `help`。例如，`automate` 会将脚本放在**文件 > 自动**菜单中。 |
| `<about>` | 出现在关于对话框中的字符串，用户可以从**帮助 > 关于增效工具**菜单中选择查看。 |
| `<enableinfo>` | 一个布尔表达式，用于指示菜单中的命令是否启用。详见[启用信息语法](https://example.com)。**注意：**如果提供了此标签，菜单项仅当至少打开一个文档且布尔表达式求值为 `true` 时才启用。如果你希望菜单项始终启用，请不要使用此标签。 |
| `<eventid>` | 一个标识事件的唯一字符串。使用 UUID 可确保你的脚本不会与其他脚本共享此标识符。 |
| `<category>` | 命令在菜单中所属的类别。用于对菜单中的命令进行分组和排序。命令根据 `<category>` 中的字符串按字母顺序放置在菜单中。如果两个命令使用相同的类别，它们将被分组在一起。 |
| `<terminology>` | 脚本与动作管理器配合工作所需的术语词典。详见[术语词典](Terminology dictionary)。 |

### 基本 JavaScript 资源示例

此示例展示了一个非常基础的 `<javascriptresource>`。通过此资源，用户可以通过选择**自动**菜单中的**添加文档**命令来执行脚本。只要至少打开一个文档，此命令在菜单中就是启用的。如果用户从**关于增效工具**菜单请求有关脚本的信息，`<about>` 标签中包含的字符串将显示在对话框中。

```javascript
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

### 启用信息语法

`<enableinfo>` 标签提供了一个布尔表达式，当该表达式被求值时，用于指示菜单中的命令是否启用。你可以使用此表达式根据文档的各种特征来启用或禁用菜单项。启用信息语法如下：

```text
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

```text
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
| `||` | 或 |
| `&&` | 与 |
| `+`、`-` | 加法或减法 |
| `*`、`/` | 乘法或除法 |
| `<`、`<=`、`>=`、`>` | 小于、小于等于、大于等于、大于 |
| `==`、`!=` | 等于，或不等于。 |
| `(..)`、`in()`、`max()`、`min()` | 函数 |
| 一元 `+`、`-`、`!` | 一元运算符：正、负、逻辑非 |

语法提供了可在 `<enableinfo>` 表达式中使用的变量和常量。下表列出了可用的常量。

| 常量名 | 描述 |
|---|---|
| `true` | 布尔真值 |
| `false` | 布尔假值 |
| `BitmapMode` | 位图模式。 |
| `GrayScaleMode` | 灰度模式，8 位深度。 |
| `IndexedMode` | 索引颜色模式。 |
| `RGBMode` | RGB 颜色模式。 |
| `CMYKMode` | CMYK 颜色模式。 |
| `HSLMode` | HSL 颜色模式。 |
| `HSBMode` | HSB 颜色模式 |
| `MultiChannelMode` | 多通道模式。 |
| `DuotoneMode` | 双色调模式。 |
| `LabMode` | Lab 颜色模式。 |

| 常量名称 | 描述 |
|---|---|
| `Gray16Mode` | 灰度模式，每通道 16 位 |
| `RGB48Mode` | RGB 颜色模式，每通道 16 位。 |
| `Lab48Mode` | LAB 模式，每通道 16 位。 |
| `CMYK64Mode` | CMYK 模式，每通道 16 位。 |
| `DeepMultichannelMode` | 深度多通道模式。 |
| `Duotone16Mode` | 双色调模式，16 位深度。 |
| `RGB96Mode` | RGB 颜色模式，每通道 32 位。 |
| `Gray32Mode` | 灰度模式，32 位深度。 |

下表显示了您可以在 `<enableinfo>` 表达式中使用的变量集合。这些变量的值基于活动文档的属性设置。

| 变量名称 | 描述 |
|---|---|
| `PSHOP_ImageMode` | 活动文档的图像模式。 |
| `PSHOP_ImageDepth` | 活动文档的位深度。 |
| `PSHOP_HasLayerMask` | 布尔值，指示是否存在图层蒙版。 |
| `PSHOP_HasSelectionMask` | 布尔值，指示是否存在选区蒙版。 |
| `PSHOP_HasTransparencyMask` | 布尔值，指示是否存在透明度蒙版。 |
| `PSHOP_NumTargetChannels` | 目标通道的数量。 |
| `PSHOP_NumTrueChannels` | 图像通道的数量。 |
| `PSHOP_IsAdjustorSheet` | 布尔值。 |
| `PSHOP_IsTargetComposite` | 布尔值，指示通道是否已合并。 |
| `PSHOP_IsTargetSection` | 布尔值。 |
| `PSHOP_IsTargetVisible` | 布尔值。 |
| `PSHOP_ImageWidth` | 图像的宽度。 |
| `PSHOP_ImageHeight` | 图像的高度。 |
| `PSHOP_TargetProtectFlags` | 目标保护标志。 |

### 在 enable-info 求值中使用未定义值

如果任何算术或关系运算的操作数是未定义的值，或者包含未定义的变量，则该求值的结果为 `false`。

布尔值的处理方式与 C/C++ 相同，非零值为 `true`，零为 `false`，但未定义值也视为 `false`。

### 使用 `in` 函数

`in` 函数（参见 `<inFunction>`）在第一个参数至少等于其后续参数之一时返回 `true`。一个典型的用例是检查活动文档的图像模式是否属于一组图像模式之一。例如：

```javascript
in(PSHOP_ImageMode, RGBMode, CMYKMode, LabMode)
```

### 动作管理器自动化

要使您的脚本能够录制脚本参数并基于它们进行自动化，需要添加两个基本机制：

- 一个术语词典，将您脚本的用户界面映射到人类可读的文本，为脚本使用的每个参数提供文本和类型信息。
- 代码，用于当参数信息来自动作管理器（而非用户界面）时读取参数信息，以及将参数信息写入动作管理器。此代码使用动作管理器的类：`ActionDescriptor`、`ActionList` 和 `ActionReference`。



请参阅 `Conditional Mode Change.jsx`，以了解一个能够录制脚本参数并可基于其进行自动化的脚本示例。此文件可在 `Presets/Scripts` 文件夹中找到。

## 术语词典

JavaScript 资源提供了一个 `<terminology>` 标签，允许您为脚本提供术语词典。创建术语词典的第一步是查看您的脚本用户界面，并为用户界面中的每个元素创建人类可读的字符串。

例如，在条件模式更改命令中，用户界面请求源模式和目标模式。源模式和目标模式都有几个选项。用户界面的所有这些元素都需要在术语词典中有对应的条目。

术语词典采用 PDF 字典格式创建，包含以下条目，并且在 `<javascriptresource>` 中必须具有以下格式：

```xml
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

```text
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

```text
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

```text
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
| `typeInteger` | `'long'` | int32 |
| `typeFloat` | `'doub'` | IEEE 64 位双精度浮点数 |
| `typeBoolean` | `'bool'` | 真或假。 |
| `typeText` | `'TEXT'` | 任意数量可读字符的块。 |
| `typeAlias` | `'alis'` | Macintosh 文件系统路径。 |
| `typePaths` | `'Pth '` | Windows 文件系统路径。 |
| `typePlatformFilePath` | `'alis'` 或 `'Pth'` | 在 Mac OS 上为 `typeAlias`，在 Windows 上为 `typePath`。 |

### 预定义类类型

Photoshop 提供了许多预定义的类，可在术语词典中使用。下表显示了其中一部分有用的类。当适用时使用这些类，但如有必要，您可以在术语资源中定义新的类。

| 名称 | 代码 | 描述 |
|---|---|---|
| `classColor` | `'Clr '` | 颜色类的类。 |
| `classRGBColor` | `'RGBC'` | `keyRed`、`keyGreen`、`keyBlue` |
| `classCMYKColor` | `'CMYC'` | `keyCyan`、`keyMagenta`、`keyYellow`、`keyBlack`。 |
| `classUnspecifiedColor` | `'UnsC'` | 未指定。 |
| `classGrayscale` | `'Grsc'` | `keyGray` |
| `classBookColor` | `'BkCl '` | 专色色板颜色 |
| `classLabColor` | `'LbCl'` | `keyLuminance`、`keyA`、`keyB`。 |

### 术语条目的唯一性规则

通常，术语条目的名称在特定类别和作用域内必须是唯一的。最好不要不必要地使名称唯一；通用术语更可取，如果某个事物已有名称，请直接使用。在考虑术语条目的唯一性时，大小写很重要。

术语条目的唯一性规则是：

- 所有事件名称必须彼此不同。
- 所有类名称必须与所有其他名称不同。
- 所有枚举类型名称必须彼此不同。
- 所有键必须与同一类或事件中使用的所有其他键不同。
- 所有枚举值必须与同一枚举类型中的所有其他枚举值不同。
- 一个类、事件、枚举类型、键和枚举值可以具有相同的名称。

### 术语定义示例

此示例演示了一个新事件的术语定义；示例使用了 `ZString`。该事件名为 `newAnnot`，接受三个参数：

- `annotType`，一个枚举（`annotType`）
- `at`，一个类（`point`）
- `size`，一个类（`annotSizeClass`）

### 脚本常量

本节列出并描述了为与 Adobe Photoshop CS6 JavaScript 属性和方法配合使用而定义的枚举。

| 常量类型 | 值 | 含义 |
|---|---|---|
| `AdjustmentReference` | `ABSOLUTE`、`RELATIVE` | 用于解释可选颜色调整规范的方法：`ABSOLUTE` = 占整体的百分比。`RELATIVE` = 占现有颜色量的百分比。传递给 [`ArtLayer.selectiveColor()`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#ArtLayer.selectiveColor)。 |
| `AnchorPosition` | `BOTTOMCENTER`、`BOTTOMLEFT`、`BOTTOMRIGHT`、`MIDDLECENTER`、`MIDDLELEFT`、`MIDDLERIGHT`、`TOPCENTER`、`TOPLEFT`、`TOPRIGHT` | 变换对象时围绕的点。当使用 [`ArtLayer`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#ArtLayer)、`LayerSet` 和 `Selection` 中的方法旋转或调整对象大小时，或使用 [`Document.resizeCanvas()`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#Document.resizeCanvas) 调整整个画布大小时，此点不会移动。 |
| `AntiAlias` | `CRISP`、`NONE`、`SHARP`、`SMOOTH`、`STRONG` | 通过柔化边缘像素与背景像素之间的颜色过渡来平滑边缘的方法。用于 [`TextItem.antiAliasMethod`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#TextItem.antiAliasMethod)。 |
| `AutoKernType` | `MANUAL`、`METRICS`、`OPTICAL` | 字符使用的字距调整类型。用于 [`TextItem.autoKerning`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#TextItem.autoKerning)。 |
| `BatchDestinationType` | `FOLDER`、`NODESTINATION`、`SAVEANDCLOSE` | 批处理文件的目标位置（如果有），在与 [`Application.batch()`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#Application.batch) 方法配合使用的 [`BatchOptions`](https://www.adobe.com/devnet-docs/photoshop/cs6/scripting/#BatchOptions) 中指定：`FOLDER`：将修改后的文件版本保存到新位置（保留原始文件不变）。`NODESTINATIONTYPE`：保持所有文件打开。`SAVEANDCLOSE`：保存更改并关闭文件。 |
| `BitmapConversionType` | `CUSTOMPATTERN`、`DIFFUSIONDITHER`、`HALFTHRESHOLD`、`HALFTONESCREEN`、`PATTERNDITHER` | 指定正在转换为位图模式的图像的质量。用于 [`BitmapConversionOptions`](BitmapConversionOptions)。 |
| `BitmapHalfToneType` | `CROSS`、`DIAMOND`、`ELLIPSE`、`LINE`、`ROUND`、`SQUARE` | 指定半调网屏中点（墨点）的形状。用于 [`BitmapConversionOptions`](BitmapConversionOptions)。 |
| `BitsPerChannelType` | `EIGHT`、`ONE`、`SIXTEEN`、`THIRTYTWO` | 每个颜色通道的位数。[`Document.bitsPerChannel`](Document.bitsPerChannel) 的值；传递给 [`Documents.add()`](Documents.add())。也用于 [`PDFOpenOptions`](PDFOpenOptions) 和 [`CameraRAWOpenOptions`](CameraRAWOpenOptions)。 |
| `BlendMode` | `COLORBLEND`、`COLORBURN`、`COLORDODGE`、`DARKEN`、`DIFFERENCE`、`DISSOLVE`、`DIVIDE`、`EXCLUSION`、`HARDLIGHT`、`HARDMIX`、`HUE`、`LIGHTEN`、`LINEARBURN`、`LINEARDODGE`、`LINEARLIGHT`、`LUMINOSITY`、`MULTIPLY`、`NORMAL`、`OVRLOAD`、`PASSTHROUGH`、`PINLIGHT`、`SATURATION`、`SCREEN`、`SOFTLIGHT`、`SUBTRACT`、`VIVIDLIGHT` | 控制应用滤镜时图像中像素的混合方式。[`ArtLayer.blendMode`](ArtLayer.blendMode) 和 [`LayerSet.blendMode`](LayerSet.blendMode) 的值。 |
| `BMPDepthType` | `BMP_A1R5G5B5`、`BMP_A4R4G4B4`、`BMP_A8R8G8B8`、`BMP_R5G6B5`、`BMP_R8G8B8`、`BMP_X1R5G5B5`、`BMP_X4R4G4B4`、`BMP_X8R8G8B8`、`EIGHT`、`FOUR`、`ONE`、`SIXTEEN`、`THIRTYTWO`、`TWENTYFOUR` | 每个通道的位数（也称为像素深度或颜色深度）。所选数字表示 2 的指数。例如，位深度为 `EIGHT` 的像素具有 2^8（即 256）种可能的颜色值。用于 [`BMPSaveOptions`](BMPSaveOptions)。 |
| `ByteOrder` | `IBM`、`MACOS` | 读取多字节值时特定于平台的顺序。 |
| `CameraRAWSettingsType` | `CAMERA`、`CUSTOM`、`SELECTEDIMAGE` | 要使用的默认 Camera Raw 设置：相机设置、自定义设置或所选图像的设置。在 [`CameraRAWOpenOptions`](https://www.google.com) 中设置。 |
| `CameraRAWSize` | `EXTRALARGE`、`LARGE`、`MAXIMUM`、`MEDIUM`、`MINIMUM`、`SMALL` | 相机 RAW 尺寸类型选项：<br>`EXTRALARGE` = 5120 x 4096<br>`LARGE` = 4096 x 2731<br>`MAXIMUM` = 6144 X 4096<br>`MEDIUM` = 3072 x 2048<br>`MINIMUM` = 1536 x 1024<br>`SMALL` = 2048 x 1365<br><br>在 [`CameraRAWOpenOptions`](https://www.google.com) 中设置。 |
| `ChangeMode` | `BITMAP`、`CMYK`、`GRAYSCALE`、`INDEXEDCOLOR`、`LAB`、`MULTICHANNEL`、`RGB` | 文档的新颜色配置文件或模式，在 [`Document.changeMode()`](https://www.google.com) 中指定。<br><br>**注意：** 彩色图像必须先更改为 `GRAYSCALE` 模式，然后才能更改为 `BITMAP` 模式。 |
| `ChannelType` | `COMPONENT`、`MASKEDAREA`、`SELECTEDAREA`、`SPOTCOLOR` | 颜色通道的类型：<br><br>`COMPONENT`：与文档颜色模式相关。<br><br>`MASKEDAREA`：颜色表示被遮罩区域的 Alpha 通道。<br><br>`SELECTEDAREA`：颜色表示选中区域的 Alpha 通道。<br><br>`SPOTCOLOR`：用于存储专色的 Alpha 通道。 |
| `ColorBlendMode` | `BEHIND`、`CLEAR`、`COLOR`、`COLORBURN`、`COLORDODGE`、`DARKEN`、`DARKERCOLOR`、`DIFFERENCE`、`DISSOLVE`、`EXCLUSION`、`HARDLIGHT`、`HARDMIXBLEND`、`HUE`、`LIGHTEN`、`LIGHTERCOLOR`、`LINEARBURN`、`LINEARDODGE`、`LINEARLIGHT`、`LUMINOSITY`、`MULTIPLY`、`NORMAL`、`OVERLAY`、`PINLIGHT`、`SATURATION`、`SCREEN`、`SOFTLIGHT`、`VIVIDLIGHT` | 在填充或描边操作中应如何混合颜色。传递给 `PathItem.fillPath()`、`Selection.fill()`、`Selection.stroke()`。 |
| `ColorModel` | `CMYK`、`GRAYSCALE`、`HSB`、`LAB`、`NONE`、`RGB` | 用于 `SolidColor` 的颜色模型。 |
| `ColorPicker` | `ADOBE`、`APPLE`、`PLUGIN`、`WINDOWS` | 首选的颜色选择工具，在首选项中设置。 |
| `ColorProfileType` | `CUSTOM`、`NONE`、`WORKING` | 用于管理此文档的颜色配置文件类型，在 `Document.colorProfileType` 中设置。 |
| `ColorReductionType` | `ADAPTIVE`、`BLACKWHITE`、`CUSTOM`、`GRAYSCALE`、`MACINTOSH`、`PERCEPTUAL`、`RESTRICTIVE`、`SELECTIVE`、`WINDOWS` | `ExportOptionsSaveForWeb` 的颜色减少算法选项。 |



| `ColorSpaceType` | `ADOBERGB`<br>`COLORMATCHRGB`<br>`PROPHOTORGB`<br>`SRGB` | 在 `CameraRAWOpenOptions` 中使用的颜色空间类型。 |
| `CopyrightedType` | `COPYRIGHTEDWORK`<br>`PUBLICDOMAIN`<br>`UNMARKED` | 文档的版权状态。用于 `DocumentPrintSettings.copyrighted`。 |
| `CreateFields` | `DUPLICATION`<br>`INTERPOLATION` | 用于创建字段的方法。传递给 `ArtLayer.applyDeInterlace()`。 |
| `CropToType` | `ARTBOX`<br>`BLEEDBOX`<br>`BOUNDINGBOX`<br>`CROPBOX`<br>`MEDIABOX`<br>`TRIMBOX` | 在 PDF 文档中裁剪页面时使用的样式。在 `PDFOpenOptions.cropPage` 中设置。 |
| `DCSType` | `COLORCOMPOSITE`<br>`GRAYSCALECOMPOSITE`<br>`NOCOMPOSITE` | 使用 `DCS1_SaveOptions` 或 `DCS2_SaveOptions` 创建的复合 DCS 文件类型：<br><br>`COLORCOMPOSITE`：除了 DCS 文件外，还创建一个颜色复合文件。<br><br>`GRAYSCALECOMPOSITE`：除了 DCS 文件外，还创建一个灰度复合文件。<br><br>`NOCOMPOSITE`：不创建复合文件。 |
| `DepthMapSource` | `IMAGEHIGHLIGHT`<br>`LAYERMASK`<br>`NONE`<br>`TRANSPARENCYCHANNEL` | 用于深度贴图的源。传递给 `ArtLayer.applyLensBlur()`。 |
| `DescValueType` | `ALIASTYPE`<br>`BOOLEANTYPE`<br>`CLASSTYPE`<br>`DOUBLETYPE`<br>`ENUMERATEDTYPE`<br>`INTEGERTYPE`<br>`LARGEINTEGERTYPE`<br>`LISTTYPE`<br>`OBJECTTYPE`<br>`RAWTYPE`<br>`REFERENCETYPE`<br>`STRINGTYPE`<br>`UNITDOUBLE` | 动作描述符键的值类型，由 `ActionDescriptor.getType()` 和 `ActionList.getType()` 返回。 |
| `DialogModes` | `ALL`<br>`ERROR`<br>`NO` | 控制运行脚本时 Photoshop 显示的对话框类型。 |
| `Direction` | `HORIZONTAL`<br>`VERTICAL` | • 要翻转文档画布的方向，传递给 `Document.flipCanvas()`。<br>• `TextItem.direction` 中文本的方向。<br>• `TextItem.warpDirection` 中文本扭曲的方向。 |

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

##### Adobe Photoshop CS6 JavaScript 脚本参考

###### 脚本常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `DisplacementMapType` | `STRETCHTOFIT`, `TILE` | 描述当图像尺寸与置换贴图不同时，置换贴图如何适配图像。传递给 [`ArtLayer.applyDisplace()`](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| `Dither` | `DIFFUSION`, `NOISE`, `NONE`, `PATTERN` | 在 [`GIFSaveOptions`](https://www.adobe.com/devnet/photoshop/scripting.html)、[`IndexedConversionOptions`](https://www.adobe.com/devnet/photoshop/scripting.html) 和 [`ExportOptionsSaveForWeb`](https://www.adobe.com/devnet/photoshop/scripting.html) 中使用的仿色类型。 |
| `DocPositionStyle` | `PRINTCENTERED`, `USERDEFINED` | `DocPosition` 中使用的定位类型。 |
| `DocumentFill` | `BACKGROUNDCOLOR`, `TRANSPARENT`, `WHITE` | 新文档的填充类型，传递给 [`Documents.add()`](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| `DocumentMode` | `BITMAP`, `CMYK`, `DUOTONE`, `GRAYSCALE`, `INDEXEDCOLOR`, `LAB`, `MULTICHANNEL`, `RGB` | 打开文档的颜色模式，[`Document.mode`](https://www.adobe.com/devnet/photoshop/scripting.html)。另见 [`Document.changeMode()`](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| `EditLogItemsType` | `CONCISE`, `DETAILED`, `SESSIONONLY` | 历史记录日志中首选的详细程度，在 [`Preferences`](https://www.adobe.com/devnet/photoshop/scripting.html) 中设置：<br>`CONCISE`：保存简洁的历史记录日志。<br>`DETAILED`：保存详细的历史记录日志。<br>`SESSIONONLY`：仅保存当前会话的历史记录日志。 |
| `ElementPlacement` | `INSIDE`, `PLACEATBEGINNING`, `PLACEATEND`, `PLACEBEFORE`, `PLACEAFTER` | 对象在图层面板中的位置。<br>**注意**：并非所有值对所有对象类型都有效。请查看特定对象的描述以确保使用的是有效值。 |
| `EliminateFields` | `EVENFIELDS`, `ODDFIELDS` | 要消除的场类型。传递给 [`ArtLayer.applyDeInterlace()`](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| `ExportType` | `ILLUSTRATORPATHS`, `SAVEFORWEB` | [`Document.exportDocument()`](https://www.adobe.com/devnet/photoshop/scripting.html) 的导出类型。<br>这等同于选择 **文件 > 导出 > 路径到 Illustrator**，或 **文件 > 存储为 Web 和设备所用格式**。 |
| `Extension` | `LOWERCASE`, `NONE`, `UPPERCASE` | 使用 [`Document.saveAs()`](https://www.adobe.com/devnet/photoshop/scripting.html) 保存时，向文件名附加扩展名的策略和格式。 |
| `FileNamingType` | `DDMM`, `DDMMYY`, `DOCUMENTNAMELOWER`, `DOCUMENTNAMEMIXED`, `DOCUMENTNAMEUPPER`, `EXTENSIONLOWER`, `EXTENSIONUPPER`, `MMDD`, `MMDDYY`, `SERIALLETTERLOWER`, `SERIALLETTERUPPER`, `SERIALNUMBER1`, `SERIALNUMBER2`, `SERIALNUMBER3`, `SERIALNUMBER4`, `YYDDMM`, `YYMMDD`, `YYYYMMDD` | 用于 `Application.batch()` 方法的 `BatchOptions` 的文件命名选项。 |
| `FontPreviewType` | `HUGE`, `EXTRALARGE`, `LARGE`, `MEDIUM`, `NONE`, `SMALL` | 在文字工具字体菜单中用于字体预览的首选字体大小，在“首选项”中设置。 |
| `FontSize` | `LARGE`, `MEDIUM`, `SMALL` | 用于面板和对话框的首选字体大小，在“首选项”中设置。 |
| `ForcedColors` | `BLACKWHITE`, `NONE`, `PRIMARIES`, `WEB` | 无论使用情况如何，都包含在颜色表中的颜色类型。用于 `GIFSaveOptions` 和 `IndexedConversionOptions`。<br><br>`BLACKWHITE`：纯黑和纯白。<br><br>`NONE`：无。<br><br>`PRIMARIES`：红、绿、蓝、青、品红、黄、黑和白。<br><br>`WEB`：216 种 Web 安全颜色。 |
| `FormatOptions` | `OPTIMIZEDBASELINE`, `PROGRESSIVE`, `STANDARDBASELINE` | 在 `JPEGSaveOptions` 中保存 JPEG 文件时使用的选项。<br><br>`OPTIMIZEDBASELINE`：优化的颜色和略微减小的文件大小。<br><br>`PROGRESSIVE`：在图像下载时显示一系列日益精细的扫描。<br><br>`STANDARDBASELINE`：大多数 Web 浏览器识别的格式。 |
| `GalleryConstrainType` | `CONSTRAINBOTH`, `CONSTRAINHEIGHT`, `CONSTRAINWIDTH` | 图像要约束的比例类型。用于 `GalleryImagesOptions`。 |
| `GalleryFontType` | `ARIAL`, `COURIERNEW`, `HELVETICA`, `TIMESNEWROMAN` | 用于 Web 照片画廊说明文字和其他文本的字体。用于 [`GalleryBannerOptions`](#)、[`GalleryImagesOptions`](#) 和 [`GalleryThumbnailOptions`](#)。<br><br>也用于 [`PicturePackageOptions`](#)。 |
| `GallerySecurityTextColorType` | `BLACK`, `CUSTOM`, `WHITE` | 用于在画廊图像上显示作为防盗威慑的文本的颜色。用于 [`GallerySecurityOptions`](#)。 |
| `GallerySecurityTextPositionType` | `CENTERED`, `LOWERLEFT`, `LOWERRIGHT`, `UPPERLEFT`, `UPPERRIGHT` | 在画廊图像上显示作为防盗威慑的文本的位置。用于 [`GallerySecurityOptions`](#)。<br><br>也用于 [`PicturePackageOptions`](#)。 |
| `GallerySecurityTextRotateType` | `CLOCKWISE45`, `CLOCKWISE90`, `COUNTERCLOCKWISE45`, `COUNTERCLOCKWISE90`, `ZERO` | 在画廊图像上显示作为防盗威慑的文本的方向。用于 [`GallerySecurityOptions`](#)。<br><br>也用于 [`PicturePackageOptions`](#)。 |
| `GallerySecurityType` | `CAPTION`, `COPYRIGHT`, `CREDIT`, `CUSTOMTEXT`, `FILENAME`, `NONE`, `TITLE` | 用于在画廊图像上显示作为防盗威慑的文本的内容。用于 [`GallerySecurityOptions`](#)。<br><br>**注意：** 除 `CUSTOMTEXT` 外，所有类型都从图像的文件信息中提取。 |
| `GalleryThumbSizeType` | `CUSTOM`, `LARGE`, `MEDIUM`, `SMALL` | Web 照片画廊中缩略图图像的大小。用于 [`GalleryThumbnailOptions`](#)。 |
| `Geometry` | `HEPTAGON`, `HEXAGON`, `OCTAGON`, `PENTAGON`, `SQUARE`, `TRIANGLE` | 形状的几何选项，例如镜头模糊滤镜中的光圈形状。<br><br>传递给 [`ArtLayer.applyLensBlur()`](#)。 |
| `GridLineStyle` | `DASHED`, `DOTTED`, `SOLID` | 在图像上显示的非打印网格的首选线条样式，在 [`Preferences`](#) 中设置。 |
| `GridSize` | `LARGE`, `MEDIUM`, `NONE`, `SMALL` | 网格线间距的首选大小，在 [`Preferences`](#) 中设置。 |
| `GuideLineStyle` | `DASHED`, `SOLID` | 在图像上显示的非打印参考线的首选线条样式，在 [`Preferences`](http://example.com) 中设置。 |
| `IllustratorPathType` | `ALLPATHS`, `DOCUMENTBOUNDS`, `NAMEDPATH` | 使用 [`Document.exportDocument()`](http://example.com) 导出到 Illustrator 文件的路径。 |
| `Intent` | `ABSOLUTECOLORIMETRIC`, `PERCEPTUAL`, `RELATIVECOLORIMETRIC`, `SATURATION` | 使用 [`Document.convertProfile()`](http://example.com) 或 [`Document.print()`](http://example.com) 从一个颜色空间转换到另一个时使用的渲染意图。 |
| `Justification` | `CENTER`, `CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFT`, `LEFTJUSTIFIED`, `RIGHT`, `RIGHTJUSTIFIED` | 段落文本在定界框内的放置方式。用于 [`TextItem.justification`](http://example.com)。 |
| `Language` | `BRAZILLIANPORTUGUESE`, `CANADIANFRENCH`, `DANISH`, `DUTCH`, `ENGLISHUK`, `ENGLISHUSA`, `FINNISH`, `FRENCH`, `GERMAN`, `ITALIAN`, `NORWEGIAN`, `NYNORSKNORWEGIAN`, `OLDGERMAN`, `PORTUGUESE`, `SPANISH`, `SWEDISH`, `SWISSGERMAN` | 用于文本的语言。用于 [`TextItem.language`](http://example.com)。 |
| `LayerCompression` | `RLE`, `ZIP` | 保存为 TIFF 格式时，图层中像素数据的压缩方法。用于 [`TiffSaveOptions`](http://example.com)。 |
| `LayerKind` | `BLACKANDWHITE`, `BRIGHTNESSCONTRAST`, `CHANNELMIXER`, `COLORBALANCE`, `CURVES`, `EXPOSURE`, `GRADIENTFILL`, `GRADIENTMAP`, `HUESATURATION`, `INVERSION`, `LEVELS`, `NORMAL`, `PATTERNFILL`, `PHOTOFILTER`, `POSTERIZE`, `SELECTIVECOLOR`, `SMARTOBJECT`, `SOLIDFILL`, `TEXT`, `THRESHOLD`, `LAYER3D`, `VIBRANCE`, `VIDEO` | [`ArtLayer.kind`](https://github.com/) 中图层对象的类型。<br><br>**注意：** 您只能从空白图层创建文字图层。 |
| `LensType` | `MOVIEPRIME`, `PRIME105`, `PRIME35`, `ZOOMLENS` | 要使用的镜头类型。传递给 [`ArtLayer.applyLensFlare()`](https://github.com/)。 |
| `MagnificationType` | `ACTUALSIZE`, `FITPAGE` | 查看图像时使用的放大类型。用于 [`PresentationOptions`](https://github.com/)。 |



| **MatteType** | `BACKGROUND`, `BLACK`, `FOREGROUND`, `NETSCAPE`, `NONE`, `SEMIGRAY`, `WHITE` | 用于填充图像透明区域相邻的抗锯齿边缘的颜色。当图像的透明度关闭时，哑光颜色将应用于透明区域。<br><br>用于 [`GIFSaveOptions`](https://github.com/)、[`IndexedConversionOptions`](https://github.com/) 和 [`JPEGSaveOptions`](https://github.com/)。 |
| **MeasurementRange** | `ALLMEASUREMENTS`, `ACTIVEMEASUREMENTS` | 要处理的测量。传递给 [`MeasurementLog`](https://github.com/) 方法。 |
| **MeasurementSource** | `MEASURESELECTION`, `MEASURECOUNTTOOL`, `MEASURERULERTOOL` | 记录测量的来源。传递给 [`Document.recordMeasurements()`](https://github.com/)。 |
| **NewDocumentMode** | `BITMAP`, `CMYK`, `GRAYSCALE`, `LAB`, `RGB` | 用于新文档的颜色配置文件。<br><br>传递给 [`Documents.add()`](https://github.com/)。<br><br>也用于 [`ContactSheetOptions`](https://github.com/) 和 [`PicturePackageOptions`](https://github.com/)。 |

##### Adobe Photoshop CS6 JavaScript 脚本参考

###### 脚本常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **NoiseDistribution** | `GAUSSIAN`, `UNIFORM` | 应用添加杂色滤镜时使用的分布方法。传递给 [`ArtLayer.applyAddNoise()`](https://example.com)。 |
| **OffsetUndefinedAreas** | `REPEATEDGEPIXELS`, `SETTOBACKGROUND`, `WRAPAROUND` | 用于填充图像或选区偏移后所留空白区域的方法。传递给 [`ArtLayer.applyOffset()`](https://example.com)。 |
| **OpenDocumentMode** | `CMYK`, `GRAYSCALE`, `LAB`, `RGB` | 打开 EPS 或 PDF 文档时使用的颜色配置文件。传递给 [`EPSOpenOptions`](https://example.com) 或 [`PDFOpenOptions`](https://example.com) 中的 [`app.open()`](https://example.com)。 |
| **OpenDocumentType** | `ALIASPIX`, `BMP`, `CAMERARAW`, `COMPUSERVEGIF`, `DICOM`, `ELECTRICIMAGE`, `EPS`, `EPSPICTPREVIEW`, `EPSTIFFPREVIEW`, `FILMSTRIP`, `JPEG`, `PCX`, `PDF`, `PHOTOCD`, `PHOTOSHOP`, `PHOTOSHOPDCS_1`, `PHOTOSHOPDCS_2`, `PHOTOSHOPEPS`, `PHOTOSHOPPDF`, `PICTFILEFORMAT`, `PICTRESOURCEFORMAT`, `PIXAR`, `PNG`, `PORTABLEBITMAP`, `RAW`, `SCITEXCT`, `SGIRGB`, `SOFTIMAGE`, `TARGA`, `TIFF`, `WAVEFRONTRLA`, `WIRELESSBITMAP` | 使用 [`app.open()`](https://example.com) 打开文档的格式。**注意：** `PHOTOCD` 已弃用。柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。**注意：** `DICOM` 选项仅适用于扩展版。 |
| **OperatingSystem** | `OS2`, `WINDOWS` | [`BMPSaveOptions`](https://example.com) 中的目标操作系统。 |
| **Orientation** | `LANDSCAPE`, `PORTRAIT` | [`PhotoCDOpenOptions`](https://example.com) 的页面方向，在 Photoshop CS3 中已弃用。**注意：** 柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。 |
| **OtherPaintingCursors** | `PRECISEOTHER`, `STANDARDOTHER` | 以下工具的首选指针：橡皮擦、铅笔、画笔、修复画笔、仿制图章、图案图章、涂抹、模糊、锐化、减淡、加深、海绵。在[首选项](#)中设置。 |
| **PaintingCursors** | `BRUSHSIZE`, `PRECISE`, `STANDARD` | 以下工具的首选指针：选框、套索、多边形套索、魔棒、裁剪、切片、修补、吸管、钢笔、渐变、直线、油漆桶、磁性套索、磁性钢笔、自由钢笔、度量、颜色取样器。在[首选项](#)中设置。 |
| **PaletteType** | `EXACT`, `LOCALADAPTIVE`, `LOCALPERCEPTUAL`, `LOCALSELECTIVE`, `MACOSPALETTE`, `MASTERADAPTIVE`, `MASTERPERCEPTUAL`, `MASTERSELECTIVE`, `PREVIOUSPALETTE`, `UNIFORM`, `WEBPALETTE`, `WINDOWSPALETTE` | [`GIFSaveOptions`](#) 和 [`IndexedConversionOptions`](#) 中使用的调色板类型。 |
| **PathKind** | `CLIPPINGPATH`, `NORMALPATH`, `TEXTMASK`, `VECTORMASK`, `WORKPATH` | [`PathItem`](#) 的类型。 |
| **PDFCompatibility** | `PDF13`, `PDF14`, `PDF15`, `PDF16`, `PDF17` | 使文档兼容的 PDF 版本。用于 [`PDFSaveOptions`](#)。 |
| **PDFEncoding** | `JPEG`, `JPEG2000HIGH`, `JPEG2000LOSSLESS`, `JPEG2000LOW`, `JPEG2000MED`, `JPEG2000MEDHIGH`, `JPEG2000MEDLOW`, `JPEGHIGH`, `JPEGLOW`, `JPEGMED`, `JPEGMEDHIGH`, `JPEGMEDLOW`, `NONE`, `PDFZIP`, `PDFZIP4BIT` | 以 PDF 格式保存文档时使用的压缩类型。用于 [`PDFSaveOptions`](#)。 |
| **PDFResample** | `NONE`, `PDFSAVERAGE`, `PDFBICUBIC`, `PDFSUBSAMPLE` | 使用的重新采样方法。用于 [`PDFSaveOptions`](PDFSaveOptions)。 |
| **PDFStandard** | `NONE`, `PDFX1A2001`, `PDFX1A2003`, `PDFX32002`, `PDFX32003`, `PDFX42008` | 使文档兼容的 PDF 标准。用于 [`PDFSaveOptions`](PDFSaveOptions)。 |
| **PhotoCDColorSpace** | `LAB16`, `LAB8`, `RGB16`, `RGB8` | [`PhotoCDOpenOptions`](PhotoCDOpenOptions) 的颜色空间，在 Photoshop CS3 中已弃用。**注意：** 柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。 |
| **PhotoCDSize** | `EXTRALARGE`, `LARGE`, `MAXIMUM`, `MEDIUM`, `MINIMUM`, `SMALL` | [`PhotoCDOpenOptions`](PhotoCDOpenOptions) 中图像的像素尺寸，在 Photoshop CS3 中已弃用。`EXTRALARGE = 1024x1536`，`LARGE = 512x768`，`MAXIMUM = 2048x3072`，`MEDIUM = 256x384`，`MINIMUM = 64x96`，`SMALL = 128x192`。**注意：** 柯达 PhotoCD 现位于 Adobe Photoshop CS6 安装 DVD 的 Goodies 文件夹中。 |
| **PICTBitsPerPixel** | `EIGHT`, `FOUR`, `SIXTEEN`, `THIRTYTWO`, `TWO` | 压缩 PICT 文件时使用的每像素位数。用于 [`PICTFileSaveOptions`](PICTFileSaveOptions) 和 [`PICTResourceSaveOptions`](PICTResourceSaveOptions)。**注意：** RGB 图像使用 16 或 32；位图和灰度图像使用 2、4 或 8。 |
| **PICTCompression** | `JPEGHIGHPICT`, `JPEGLOWPICT`, `JPEGMAXIMUMPICT`, `JPEGMEDIUMPICT`, `NONE` | 将图像另存为 PICT 文件时使用的压缩类型。用于 [`PICTFileSaveOptions`](PICTFileSaveOptions) 和 [`PICTResourceSaveOptions`](PICTResourceSaveOptions)。 |
| **PicturePackageTextType** | `CAPTION`, `COPYRIGHT`, `CREDIT`, `FILENAME`, `NONE`, `ORIGIN`, `USER` | 图片包中文本的功能或含义。用于 [`PicturePackageOptions`](PicturePackageOptions)。 |
| **PointKind** | `CORNERPOINT`, `SMOOTHPOINT` | 路径点在路径项目中的作用。 |
| **PointType** | `POSTSCRIPT`, `TRADITIONAL` | 类型点首选的度量单位，在首选项中设置 `pointSize`：`POSTSCRIPT = 72` 点/英寸，`TRADITIONAL = 72.27` 点/英寸。 |
| **PolarConversionType** | `POLARTORECTANGULAR`, `RECTANGULARTOPOLAR` | 使用的极坐标扭曲方法。传递给 [`ArtLayer.applyPolarCoordinates()`](ArtLayer-applyPolarCoordinates)。 |
| **Preview** | `EIGHTBITTIFF`, `MACOSEIGHTBIT`, `MACOSJPEG`, `MACOSMONOCHROME`, `MONOCHROMETIFF`, `NONE` | 用作目标应用程序中低分辨率预览的图像类型。用于 `DCS1_SaveOptions`、`DCS2_SaveOptions` 和 `EPSSaveOptions`。 |
| **PrintColorHandling** | `PRINTERMANAGED`, `PHOTOSHOPMANAGED`, `SEPARATIONS` | 用于 `ColorHandling` 的颜色处理类型。 |
| **PurgeTarget** | `ALLCACHES`, `CLIPBOARDCACHE`, `HISTORYCACHES`, `UNDOCACHES` | [`Application.purge()`](Application-purge) 操作要清除的缓存。 |
| **QueryStateType** | `ALWAYS`, `ASK`, `NEVER` | 打开 PSD 文件时检查是否最大化兼容性的首选策略，在首选项 `maximizeCompatibility` 中设置。 |
| **RadialBlurMethod** | `SPIN`, `ZOOM` | 使用的模糊方法。传递给 [`ArtLayer.applyRadialBlur()`](ArtLayer-applyRadialBlur)。 |
| **RadialBlurQuality** | `BEST`, `DRAFT`, `GOOD` | 模糊图像的平滑度或颗粒度。传递给 [`ArtLayer.applyRadialBlur()`](ArtLayer-applyRadialBlur)。 |
| **RasterizeType** | `ENTIRELAYER`, `FILLCONTENT`, `LAYERCLIPPINGPATH`, `LINKEDLAYERS`, `SHAPE`, `TEXTCONTENTS` | 使用 [`ArtLayer.rasterize()`](ArtLayer-rasterize) 要栅格化的图层元素。 |
| **ReferenceFormType** | `CLASSTYPE`, `ENUMERATED`, `IDENTIFIER`, `INDEX`, `NAME`, `OFFSET`, `PROPERTY` | `ActionReference` 对象的类型，由 [`getForm()`](getForm) 返回。 |
| **ResampleMethod** | `BICUBIC`, `BICUBICSHARPER`, `BICUBICSMOOTHER`, `BILINEAR`, `NEARESTNEIGHBOR`, `NONE` | 图像插值使用的方法。传递给 [`Document.resizeImage()`](Document-resizeImage)，并用作首选项 `interpolation` 的值。 |
| **RippleSize** | `LARGE`, `MEDIUM`, `SMALL` | 使用的波纹大小。传递给 [`ArtLayer.applyRipple()`](ArtLayer-applyRipple)。 |
| **SaveBehavior** | `ALWAYSSAVE`, `ASKWHENSAVING`, `NEVERSAVE` | 应用程序保存文档时的首选行为。请参阅首选项 `appendExtension` 和 `imagePreviews`。 |
| **SaveDocumentType** | `ALIASPIX`, `BMP`, `COMPSERVEGIF`, `ELECTRICIMAGE`, `JPEG`, `PCX`, `PHOTOSHOP`, `PHOTOSHOPDCS_1`, `PHOTOSHOPDCS_2`, `PHOTOSHOPEPS`, `PHOTOSHOPPDF`, `PICTFILEFORMAT`, `PICTRESOURCEFORMAT`, `PIXAR`, `PNG`, `PORTABLEBITMAP`, `RAW`, `SCITEXCT`, `SGIRGB`, `SOFTIMAGE`, `TARGA`, `TIFF`, `WAVEFRONTRLA`, `WIRELESSBITMAP` | 使用 [`Document.exportDocument()`](Document-exportDocument) 导出时保存文档的格式。传递给 `ExportOptionsSaveForWeb.format`，以指定要写入的文件类型。仅支持以下格式导出：`COMPSERVEGIF`、`JPEG`、`PNG-8`、`PNG-24` 和 `BMP`。 |
| **SaveEncoding** | `ASCII`, `BINARY`, `JPEGHIGH`, `JPEGLOW`, `JPEGMAXIMUM`, `JPEGMEDIUM` | 使用 [`Document.saveAs()`](Document-saveAs) 保存文件到 DCS 或 EPS 时使用的编码类型。 |
| **SaveLogItemsType** | `LOGFILE`, `LOGFILEANDMETADATA`, `METADATA` | 历史记录日志数据的首选存储位置，在首选项 `saveLogItems` 中设置。 |
| **SaveOptions** | `DONOTSAVECHANGES`, `PROMPTTOSAVECHANGES`, `SAVECHANGES` | 使用 [`Document.close()`](Document-close) 关闭文档时的策略。 |

##### Adobe Photoshop CS6 JavaScript 脚本参考

脚本常量 214

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **SelectionType** | `DIMINISH`<br>`EXTEND`<br>`INTERSECT`<br>`REPLACE` | 当已存在选区时的选区行为：<br><br>`DIMINISH`：从已选区域中移除选区。<br><br>`EXTEND`：将选区添加到已选区域。<br><br>`INTERSECT`：仅保留新选区与已选区域相交的部分。<br><br>`REPLACE`：替换已选区域。<br><br>用于 [`PathItem.makeSelection()`](http://javascript-ref/PathItem-makeSelection)、[`Selection.load()`](http://javascript-ref/Selection-load)、[`Selection.select()`](http://javascript-ref/Selection-select) 和 [`Selection.store()`](http://javascript-ref/Selection-store)。 |
| **ShapeOperation** | `SHAPEADD`<br>`SHAPEINTERSECT`<br>`SHAPESUBTRACT`<br>`SHAPEXOR` | 如果目标路径已存在选区时，如何组合形状。<br><br>为 [`SubPathInfo.operation`](http://javascript-ref/SubPathInfo-operation) 设置，存储在结果 [`SubPathItem`](http://javascript-ref/SubPathItem) 中。 |
| **SmartBlurMode** | `EDGEONLY`<br>`NORMAL`<br>`OVERLAYEDGE` | 智能模糊的方法：<br><br>`EDGEONLY`、`OVERLAYEDGES`：仅对颜色过渡的边缘应用模糊。<br><br>`NORMAL`：对整个图像应用模糊。<br><br>传递给 [`ArtLayer.applySmartBlur()`](http://javascript-ref/ArtLayer-applySmartBlur)。 |



| SmartBlurQuality | `HIGH`<br>`LOW`<br>`MEDIUM` | 模糊质量。传递给 [`ArtLayer.applySmartBlur()`](http://javascript-ref/ArtLayer-applySmartBlur)。 |
|---|---|---|
| SourceSpaceType | `DOCUMENT`<br>`PROOF` | 使用 [`Document.print()`](http://javascript-ref/Document-print) 打印时源的色彩空间。 |
| SpherizeMode | `HORIZONTAL`<br>`NORMAL`<br>`VERTICAL` | 用于变形的曲线（或拉伸形状）。传递给 [`ArtLayer.applySpherize()`](http://javascript-ref/ArtLayer-applySpherize)。 |
| StrikeThruType | `STRIKEBOX`<br>`STRIKEHEIGHT`<br>`STRIKEOFF` | 文本中使用的删除线样式。用于 [`TextItem.strikeThru`](http://javascript-ref/TextItem-strikeThru)。 |
| StrokeLocation | `CENTER`<br>`INSIDE`<br>`OUTSIDE` | 路径或选区边界描边的位置。传递给 [`Selection.stroke()`](http://javascript-ref/Selection-stroke)。 |
| TargaBitsPerPixel | `SIXTEEN`<br>`THIRTYTWO`<br>`TWENTYFOUR` | 保存为 Targa 格式时使用的分辨率。用于 [`TargaSaveOptions`](http://javascript-ref/TargaSaveOptions)。 |
| TextCase | `ALLCAPS`<br>`NORMAL`<br>`SMALLCAPS` | 文本中使用的大写样式。用于 [`TextItem.capitalization`](https://helpx.adobe.com/photoshop/using/text-layer.html)。 |
| TextComposer | `ADOEBEEVERYLINE`<br>`ADOBESINGLELINE` | 用于优化指定的断字和对齐选项的组合方法。用于 [`TextItem.textComposer`](https://helpx.adobe.com/photoshop/using/text-layer.html)。 |
| TextType | `PARAGRAPHTEXT`<br>`POINTTEXT` | 文本类型，用于 [`TextItem.kind`](https://helpx.adobe.com/photoshop/using/text-layer.html)。<br><br>`PARAGRAPHTEXT`：在边界框内自动换行的文本。<br><br>`POINTTEXT`：不自动换行的文本。 |
| TextureType | `BLOCKS`<br>`CANVAS`<br>`FILE`<br>`FROSTED`<br>`TINYLENS` | 用于纹理化或玻璃滤镜的纹理或玻璃表面图像类型。传递给 [`ArtLayer.applyGlassEffect()`](https://helpx.adobe.com/photoshop/using/text-layer.html)。 |
| TIFFEncoding | `JPEG`<br>`NONE`<br>`TIFFLZW`<br>`TIFFZIP` | TIFF 文件使用的压缩类型。用于 [`TiffSaveOptions`](https://helpx.adobe.com/photoshop/using/text-layer.html)。 |
| ToolType | `ARTHISTORYBRUSH`<br>`BACKGROUNDERASER`<br>`BLUR`<br>`BRUSH`<br>`BURN`<br>`CLONESTAMP`<br>`COLORREPLACEMENTTOOL`<br>`DODGE`<br>`ERASER`<br>`HEALINGBRUSH`<br>`HISTORYBRUSH`<br>`PATTERNSTAMP`<br>`PENCIL`<br>`SHARPEN`<br>`SMUDGE`<br>`SPONGE` | 与 [`PathItem.strokePath()`](https://helpx.adobe.com/photoshop/using/text-layer.html) 一起使用的工具。 |
| TransitionType | `BLINDSHORIZONTAL`<br>`BLINDSVERTICAL`<br>`BOXIN`<br>`BOXOUT`<br>`DISSOLVE`<br>`GLITTERDOWN`<br>`GLITTERRIGHT`<br>`GLITTERRIGHTDOWN`<br>`NONE`<br>`RANDOM`<br>`SPLITHORIZONTALIN`<br>`SPLITHORIZONTALOUT`<br>`SPLITVERTICALIN`<br>`SPLITVERTICALOUT`<br>`WIPEDOWN`<br>`WIPELEFT`<br>`WIPE RIGHT`<br>`WIPEUP` | PDF 演示中从一张图像过渡到下一张图像的方法。用于 [`PresentationOptions`](https://helpx.adobe.com/photoshop/using/text-layer.html)。 |
| TrimType | `BOTTOMRIGHT`<br>`TOPLEFT`<br>`TRANSPARENT` | 围绕图像裁剪的像素类型，传递给 [`Document.trim()`](https://photoshop-scripting-reference.readthedocs.io/)。<br><br>`BOTTOMRIGHT` = 右下角像素颜色。<br><br>`TOPLEFT` = 左上角像素颜色。 |
| TypeUnits | `MM`<br>`PIXELS`<br>`POINTS` | 文本字符测量的首选单位，在[首选项](https://photoshop-scripting-reference.readthedocs.io/)中设置。 |
| UndefinedAreas | `REPEATEDGEPIXELS`<br>`WRAPAROUND` | 处理“扭曲”类别滤镜应用后图像中未变形或留白区域的方法。传递给 [`ArtLayer.applyDisplace()`](https://photoshop-scripting-reference.readthedocs.io/)、[`applyShear()`](https://photoshop-scripting-reference.readthedocs.io/)、[`applyWave()`](https://photoshop-scripting-reference.readthedocs.io/)。 |
| UnderlineType | `UNDERLINELEFT`<br>`UNDERLINEOFF`<br>`UNDERLINERIGHT` | 文本下划线的位置。用于 [`TextItem.underline`](https://photoshop-scripting-reference.readthedocs.io/)。<br><br>**注意：** `UNDERLINELEFT` 和 `UNDERLINERIGHT` 仅在方向 = `Direction.VERTICAL` 时有效。 |
| Units | `CM`<br>`INCHES`<br>`MM`<br>`PERCENT`<br>`PICAS`<br>`PIXELS`<br>`POINTS` | 类型和标尺增量的首选测量单位，在 [`Preferences.rulerUnits`](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 |
| Urgency | `FOUR`<br>`HIGH`<br>`LOW`<br>`NONE`<br>`NORMAL`<br>`SEVEN`<br>`SIX`<br>`THREE`<br>`TWO` | 文档的编辑紧急状态，在 [`DocumentPrintSettings.urgency`](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 |
| WarpStyle | `ARC`<br>`ARCH`<br>`ARCLOWER`<br>`ARCUPPER`<br>`BULGE`<br>`FISH`<br>`FISHEYE`<br>`FLAG`<br>`INFLATE`<br>`NONE`<br>`RISE`<br>`SHELLLOWER`<br>`SHELLUPPER`<br>`SQUEEZE`<br>`TWIST`<br>`WAVE` | 用于文本的变形样式。用于 [`TextItem.warpStyle`](https://photoshop-scripting-reference.readthedocs.io/)。 |
| WaveType | `SINE`<br>`SQUARE`<br>`TRIANGULAR` | 使用的波形类型。传递给 [`ArtLayer.applyWave()`](https://photoshop-scripting-reference.readthedocs.io/)。 |
| WhiteBalanceType | `ASSHOT`<br>`AUTO`<br>`CLOUDY`<br>`CUSTOM`<br>`DAYLIGHT`<br>`FLASH`<br>`FLUORESCENT`<br>`SHADE`<br>`TUNGSTEN` | 影响色彩平衡的光照条件。在 [`CameraRAWOpenOptions`](https://photoshop-scripting-reference.readthedocs.io/) 中设置。 |
| ZigZagType | `AROUNDCENTER`<br>`OUTFROMCENTER`<br>`PONDRIPPLES` | 使用的锯齿方法。传递给 [`ArtLayer.applyZigZag()`](https://photoshop-scripting-reference.readthedocs.io/)。 |

## 附录 A：事件 ID 代码

下表列出了事件及其四字符 ID 代码或字符串标识符，用于 `notifier` 对象。

**注意：** 在代码中，不要为四字符 ID 包含单引号（`'`）。此表中的单引号用于说明不含四个字母的代码中必需空格的位置。但是，长于四个字符的字符串标识符在代码中需要双引号。

**提示：** 如果在此表中找不到要用于通知的事件，可以使用 ScriptListener 来确定事件 ID 代码。请参阅 *Photoshop CS6 脚本指南* 操作管理器章节中的 ScriptListener 文档。

| 事件 | 4 字符 ID 或字符串 |
|---|---|
| 3DTransform | `' TdT '` |
| Average | `'Avrg'` |
| ApplyStyle | `'ASty'` |
| Assert | `'Asrt'` |
| AccentedEdges | `'AccE'` |
| Add | `'Add  '` |
| AddNoise | `'AdNs'` |
| AddTo | `'AddT'` |
| Align | `'Algn'` |
| All | `'All  '` |
| AngledStrokes | `'AngS'` |
| ApplyImage | `'AppI'` |
| BasRelief | `'BsRl'` |
| Batch | `'Btch'` |
| BatchFromDroplet | `'BtcF'` |
| Blur | `'Blr  '` |
| BlurMore | `'BlrM'` |
| Border | `'Brdr'` |
| Brightness | `'BrgC'` |
| CanvasSize | `'CnvS'` |
| ChalkCharcoal | `'ChlC'` |
| ChannelMixer | `'ChnM'` |

Adobe Photoshop CS6

JavaScript 脚本参考

### 附录 A：事件 ID 代码

| 事件 | 4 字符 ID 或字符串 |
|---|---|
| 炭笔 | `'Chrc'` |
| 铬黄 | `'Chrm'` |
| 清除 | `'Cler'` |
| 关闭 | `'Cls '` |
| 云彩 | `'Clds'` |
| 色彩平衡 | `'ClrB'` |
| 彩色半调 | `'ClrH'` |
| 色彩范围 | `'ClrR'` |
| 彩色铅笔 | `'ClrP'` |
| 联系表 | `"0B71D221-F8CE-11d2-B21B-0008C75B322C"` |
| Conte 蜡笔 | `'CntC'` |
| 收缩 | `'Cntc'` |
| 转换模式 | `'CnvM'` |
| 复制 | `'copy'` |
| 复制效果 | `'CpFX'` |
| 合并复制 | `'CpyM'` |
| 复制到图层 | `'CpTL'` |
| 龟裂缝 | `'Crql'` |
| 创建水滴 | `'CrtD'` |
| 裁剪 | `'Crop'` |
| 阴线 | `'Crsh'` |
| 晶格化 | `'Crst'` |
| 曲线 | `'Crvs'` |
| 自定 | `'Cstm'` |
| 剪切 | `'cut '` |
| 剪切到图层 | `'CtTL'` |
| 剪纸 | `'Ct  '` |
| 深色线条 | `'DrkS'` |
| 逐行扫描 | `'Dntr'` |
| 定义图案 | `'DfnP'` |
| 去边 | `'Dfrg'` |
| 删除 | `'Dlt '` |
| 去色 | `'Dstt'` |
| 取消选择 | `'Dslc'` |
| 蒙尘与划痕 | `'Dspc'` |
| 差异云彩 | `'DrfC'` |
| 扩散 | `'Dfs '` |
| 扩散亮光 | `'DfsG'` |
| 禁用图层效果 | `'dlfx'` |
| 置换 | `'Dspl'` |
| 分布 | `'Dstr'` |
| 绘画 | `'Draw'` |
| 干画笔 | `'DryB'` |
| 复制图层 | `'Dplc'` |
| 粉尘与划痕 | `'DstS'` |
| 浮雕效果 | `'Embs'` |
| 色调均化 | `'Eqlz'` |
| 交换 | `'Exch'` |
| 扩展 | `'Expn'` |
| 导出 | `'Expr'` |
| 跳转到 | `'Jpto'` |
| 导出透明图像 | `"02879e00-cb66-11d1-bc43-0060b0a13dc4"` |
| 凸出 | `'Extr'` |
| 切面 | `'Fct '` |
| 消退 | `'Fade'` |
| 羽化 | `'Fthr'` |
| 纤维 | `'Fbrs'` |
| 填充 | `'Fl  '` |
| 胶片颗粒 | `'FlmG'` |
| 滤镜 | `'Fltr'` |
| 查找边缘 | `'FndE'` |
| 适合图像 | `"3caa3434-cb67-11d1-bc43-0060b0a13dc4"` |
| 拼合图像 | `'FltI'` |
| 翻转 | `'Flip'` |
| 碎片 | `'Frgm'` |
| 壁画 | `'Frsc'` |
| 高斯模糊 | `'GsnB'` |
| 获取 | `'getd'` |
| 玻璃 | `'Gls '` |
| 霓虹灯光 | `'GlwE'` |
| 渐变 | `'Grdn'` |
| 渐变映射 | `'GrMp'` |
| 颗粒 | `'Grn '` |
| 素描钢笔 | `'GraP'` |
| 图层组 | `'GrpL'` |
| 扩大选取 | `'Grow'` |
| 半调图案 | `'HlfS'` |
| 隐藏 | `'Hd  '` |
| 高反差保留 | `'HghP'` |
| HSB/HSL | `'HsbP'` |
| 色相/饱和度 | `'HStr'` |
| 图像大小 | `'ImgS'` |
| 导入 | `'Impr'` |
| 墨水轮廓 | `'InkO'` |
| 交叉 | `'Intr'` |
| 与选区交叉 | `'IntW'` |
| 反选 | `'Invs'` |
| 反相 | `'Invr'` |
| 镜头光晕 | `'LnsF'` |
| 色阶 | `'Lvls'` |
| 光照效果 | `'LghE'` |
| 链接 | `'Lnk '` |
| 制作 | `'Mk  '` |
| 最大值 | `'Mxm '` |
| 中间值 | `'Mdn '` |
| 合并图层 | `'Mrg2'` |
| 合并旧图层 | `'MrgL'` |
| 合并专色通道 | `'MSpt'` |
| 合并可见图层 | `'MrgV'` |
| 铜版雕刻 | `'Mztn'` |
| 最小值 | `'Mnm '` |
| 模式更改 | `"8cba8cd6-cb66-11d1-bc43-0060b0a13dc4"` |
| 马赛克 | `'Msc '` |
| 马赛克插件 | `'MscT'` |
| 动感模糊 | `'MtnB'` |
| 移动 | `'move'` |
| NTSC 颜色 | `'NTSC'` |
| 霓虹灯光 | `'NGlw'` |
| 下一步 | `'Nxt '` |
| 便条纸 | `'NtPr'` |
| 通知 | `'Ntfy'` |
| 空值 | `typeNull` |
| 海洋波纹 | `'OcnR'` |
| 位移 | `'Ofst'` |
| 打开 | `'Opn '` |
| 绘画 | `'Pnt '` |
| 绘画涂抹 | `'PntD'` |
| 调色刀 | `'PltK'` |
| 粘贴 | `'past'` |
| 粘贴效果 | `'PaFX'` |
| 粘贴入 | `'PstI'` |



| 粘贴到外部 | `'PstO'` |
|---|---|
| 拼缀图 | `'Ptch'` |
| 影印 | `'Phtc'` |
| 图片包 | `"4C1ABF40-DD82-11d2-B20F-0008C75B322C"` |
| 挤压 | `'Pnch'` |
| 置入 | `'Plc '` |
| 石膏效果 | `'Plst'` |
| 塑料包装 | `'PlsW'` |
| 播放 | `'Ply '` |
| 点状化 | `'Pntl'` |
| 极坐标 | `'Plr '` |
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

**动作管理器** 193

**动作**

- 命令列表 40
- 描述 43
- 描述符 37
- 播放 47

活动文档 45

`activePrinter` 96

添加杂色滤镜

**调整**

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

**Alpha 通道**

- 定义 72
- 从透明区域（TIFF 文档）186
- 不透明度 72
- 保存
  - 在 BMP 文档中 69
  - 在 PDF 文档中 148
  - 在 PICT 文档中 153
  - 在 PICT 资源中 154
  - 在 Pixar 文档中 156
  - 在 PSD 文档中 152
  - 在 RAW 文档中 164
  - 在 SGIRGB 文档中 171
  - 在 Targa 文档中 176
  - 在 TIFF 文档中 186

**锚点**

- 添加 143

注释，导入 92

**抗锯齿**

- 文本 179

**应用程序**

- 激活 47
- 检查功能是否启用 47
- 默认值 158
- 位置 46
- 首选项 158

画图图层，*参见图层*

亚洲文本 160

作者 99

自动字距调整 179, 197

自动行距 184

自动间距，联系表 82

可用内存 45

平均滤镜 55

## B

**背景色**

- 应用 45
- 画廊 110

背景图层 53

`backgroundColor` 96

基线偏移 179

批处理命令 47

**批处理**

- 目标文件夹 66, 197
- 指定选项 66

蜂鸣声 158

**位图文档**

- 转换为 198
- 深度类型 198
- 半调类型 198
- 打开 207
- 保存 69

**位图图像**

- *参见位图文档*

黑白图像 62

`bleedWidth` 96

**混合模式**

- 图层组 129
- 图层 53

模糊滤镜 55

**模糊滤镜**

- 平均 55
- 进一步模糊 55
- 高斯模糊 56
- 镜头模糊 57
- 动感模糊 58
- 径向模糊 58
- 特殊模糊 59

进一步模糊滤镜 55

BMP 文档

- *参见位图文档*

**亮度** 55

- 调整 55
- 均匀化 60

构建 45

## C

**缓存**

- 图像 159
- 清理 49

**Camera Raw 文档**

- 打开 70
- 设置 199
- 大小选项 199

画布

- 翻转 92
- 调整大小 92

画布，定义 88

标题 96

标题

- 联系表 82
- 文档 99
- 画廊图像 111
- 画廊缩略图 115
- 图像 99

`centerCropMarks` 96

通道

- 激活 88
- 添加 74
- 调整 55
- Alpha *参见 Alpha 通道*
- 创建 74
- 删除 72
- 以彩色显示 158
- 复制 72
- 显示 72
- 合并 72
- 混合 61
- 分离 93
- 专色 *参见专色通道*
- 类型 72

剪贴路径

- 从路径 139
- 从文本 185

云彩滤镜 55

`CMYKColor` 79

色彩平衡，调整 61

拾色器 158

颜色配置文件

- 更改 91
- 确定类型 89
- 命名 88

颜色配置文件，参见各文档格式

颜色取样器

- 添加 81
- 创建 81
- 移动 80
- 移除 80

`colorBars` 96

`colorHandling` 96

颜色

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

注释，图层复合 126

兼容性，最大化 159

分量通道

- 色彩平衡 55
- 定义 72
- 列表 88
- *参见合成通道*

合成通道 72

- *参见分量通道*

Compuserve GIF 文档

- 打开 207
- 保存 116

联系表

- 标题 82
- 列 82
- 尺寸 82
- 创建 48
- 行 82

对比度

- 调整 55
- 自动调整 59
- Camera Raw 设置 70
- 中间调 62

副本 96

版权信息 99

`cornerCropMarks` 96

计数项目

- 添加 84
- 创建 84
- 移除 83

裁剪 91

CS4 版本更改 34

光标 160

曲线，调整 55

自定滤镜 55

## D

DCS 1 文档，保存 85

逐行扫描滤镜 56

去色 60

蒙尘与划痕滤镜 56

对话框

- 显示 45

差异云彩滤镜 56

扩散亮光滤镜 56

置换滤镜 56

扭曲滤镜

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

- JavaScript
  - Photoshop CS4 中的变更 34
  - 支持的功能 32

## JavaScript 资源

- 启用信息语法 190
- `javascriptresource` 语法 189

## L

- `LabColor` 125

标签 96

语言 181

## 图层复合

- 添加 127
- 应用 126
- 在文档中 89

## 图层组

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

图层样式，应用 59

`LayerComps` 127

分层的 TIFF 文档，保存 158

图层 128

## 图层

- 添加 65
- 应用样式 59
- 背景 53
- 混合模式 53
- 边界 53
- 剪贴板命令 59
- 复合 126
- 复制 59
- 重复 60
- 拼合 92
- 编组 53
- 在文档中 89
- 反相 60
- 类型 53
- 链接 60
- 锁定内容 53-54
- 可见 54
- 合并 60
- 合并可见 92
- 移动 61
- 栅格化 92
- 栅格化内容 61
- 移除 65
- 调整大小 62
- 旋转 62
- 在 PDF 文档中保存 148
- 取消链接 62

## `LayerSet` 129

`LayerSets` 131

## 图层组

- 合并 130

## 行距 181, 184

## 镜头模糊滤镜

- 应用 57

## 镜头光晕滤镜 57

字距 180-183

## 色阶

- 调整 55
- 自动调整 55

## 连字 179-181

链接的图层 60

- 取消链接 62

## 链接

- 颜色 110

## M

## MacOS

- 文件类型 46

## 托管文档 89

`mapBlack` 96

最大化兼容性 159

最大值滤镜 57

中间值杂色滤镜 57

内存 45

## 合并

- 图层 60
- 可见图层 92

## 元数据

- 文档 89
- 文档对象 99
- 画廊 113
- `xmp` 90, 188

## 方法

- 批处理 47

## 中间调

- 色彩平衡 55

最小值滤镜 58

动感模糊滤镜 58

## N

## 负片 96

## 杂色滤镜

- 添加杂色
- 去斑 56
- 蒙尘与划痕 56
- 中间值 57

## 非线性历史记录 159

## 通知

- 脚本中的事件 136

## 通知器

- 添加 137
- 事件 ID 216
- 移除 136

NTSC 滤镜 58

## O

## 对象模型

- Photoshop CS4 中的变更 34

## 海洋波纹滤镜 58

## 位移滤镜 58

## 旧样式字体 183

## 不透明度

- 通道 72
- 画廊安全文本 114
- 图层填充 53
- 图层组 129
- 图层 54
- 图片包 155

## 打开选项

- DICOM 格式 87
- EPS 格式 103
- PDF 格式 147
- Photo CD 格式 151
- RAW 格式 70, 163

## 优化 106

## 其他滤镜

- 自定 55
- 高反差保留 56
- 最大值 57
- 最小值 58
- 位移 58

## P

## 调色板 160

## 粘贴 92

## 路径 46

## 路径项

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

## 路径点信息

- 锚点 144
- 左方向 144
- 右方向 144

`PathItems` 142

## 路径

- 参见路径项

## PDF 文档

- 打开 147
- 保存 148

## PDF 演示文稿

- 自动前进 162
- 制作 48
- 输出格式 162
- 过渡类型 162

Photo CD 光盘，打开 151

## 照片滤镜 61

## 照片画廊

- 参见画廊

## 照片合并 48

## Photoshop 文档

- 打开 207
- 保存 152

Photoshop 文件，最大化兼容性 159

## PICT 文档

- 打开 207
- 保存 153

## PICT 资源

- 打开 207
- 保存 154

## 图片包

- 内容 155
- 拼合 155
- 制作 48
- 不透明度 155
- 选项 155
- 文本属性 155

## 挤压滤镜 58

## Pixar 文档

- 打开 207
- 保存 156

`PixarSaveOptions` 156

## 像素

- 长宽比 89
- 倍增 160
- 均衡 60
- 插值 159
- 锁定 54
- 单位度量 214

播放选项 46

`playbackDisplayDialogs` 46

## 增效工具文件夹

- 附加增效工具文件夹 161

## PNG 8 文档，保存 106

## PNG 文档

- 保存 157

`PNGSaveOptions` 157

## 极坐标滤镜 58

## 色调分离 61

## PostScript 编码 92

## PostScript 名称 177

`posX` 96

`posY` 96

## 首选项 158

`PresentationOptions` 162

## 演示文稿

- 制作 48
- PDF 演示文稿

`printBorder` 96

## 打印，文档 92

`printOneCopy` 92

`printSelected` 96

`printSettings` 89

`printSpace` 96

## 属性

- 测量日志 46

## PSD 文档

- 打开 207
- 保存 152

## 清理 49

## Q

`quickMaskMode` 90

## 引号样式 160

## R

## 径向模糊滤镜 58

## 栅格化 61

## 栅格化

- 文档图层 92

## RAW 文档

- 打开 163

`RawSaveOptions` 164

`recentFiles` 46

`registrationMarks` 96

## 渲染滤镜

- 云彩 55
- 分层云彩 56
- 镜头光晕 57

`renderIntent` 96

## 分辨率

- 位图转换 68
- 文档 90

`RGBColor` 165

## 波纹滤镜 58

## 旋转 62

## 标尺单位 160

## `runMenuItem` 49

## S

## 存储为 93

## 已保存 90

## 存储 92

## 存储，参见各文档格式。

## 缩放 97

## 脚本接口

- 构建日期 46
- 版本 46

`scriptingVersion` 46

## 脚本

- 自动化 189, 193
- 在菜单中启用/禁用 189
- 执行 33
- 在菜单中分组 189
- 安装 33
- 启动 33
- 术语词典 193
- 有效文件扩展名 32

Scripts Events Manager 46



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

### 锐化滤镜

- 锐化 58
- 锐化边缘 58
- 进一步锐化 58
- USM 锐化 59

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

参见字体

## 文本项

参见文本

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

- `application` 47
- `scripting interface` 46

`video alpha` 161

`video filters`

- `De-Interlace` 56
- `NTSC` 58

`visibility`

- `channels` 72
- `layer comps` 126
- `layers` 54

## W

`warp` 184

`Wave filter` 59

`Web photo galleries`

- See galleries.

`webSnap` 107

`width` 90

`Windows`

- `filetypes` 47

`word spacing` 180–183

`work paths`

- `designating` 208
- `from selected area` 167

`wrapping, text` 181

## X

`XML` 188

`xmp metadata` 90, 188

## Z

`Zigzag filter` 59

`zoom` 159
