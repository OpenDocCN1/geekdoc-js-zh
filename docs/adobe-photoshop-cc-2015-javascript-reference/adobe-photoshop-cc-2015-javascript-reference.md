# Adobe Photoshop CC 2015 JavaScript 参考手册











Adobe Photoshop CC 2015 JavaScript 脚本参考


-   复制
73

-   合并
74

-   移除
74


80

81




































removeAll







removeAll





width



























# JavaScript 脚本参考

Adobe Photoshop CC 2015


217


# 1 简介

本参考手册描述了 Adobe® Photoshop® CC 2015® JavaScript™ 类型库中的对象和方法。配套文档 *Photoshop CC 2015 脚本指南* 描述了基本的脚本概念和 Photoshop 对象模型。本文档提供了 Photoshop 对象模型的详细参考信息，以及 JavaScript 特有的功能说明。

Adobe Photoshop CC 2015 使用 ExtendScript，这是 Adobe 对 JavaScript 的扩展实现。有关更多信息，请参阅 [Adobe Photoshop CC 2015 中的 JavaScript 支持](#)。

本书包含以下部分：

-   * 本简介，介绍了 Adobe Photoshop CC 2015 中的脚本支持功能，并列出了自上一版本以来 JavaScript 接口的更改。
- [JavaScript 对象参考](#)，为所有 Photoshop DOM 对象和命令提供了完整的参考。
- [脚本常量](#)，列出了 Photoshop 类型库中使用的所有枚举。

# Adobe Photoshop CC 2015 中的 JavaScript 支持

JavaScript 文件要被 Photoshop 识别为有效的脚本文件，必须使用 `.js` 或 `.jsx` 扩展名。

在 Mac OS 上，使用这两种扩展名的脚本功能没有区别。在 Windows 上，如果从 Photoshop 内部打开脚本文件，使用 `.js` 和 `.jsx` 扩展名没有区别。但是，如果通过双击启动脚本，使用 `.js` 扩展名的脚本将使用 Microsoft JScript 引擎解释，无法启动 Adobe Photoshop CC 2015。对于 Windows，建议使用 `.jsx` 扩展名，因为它会使用 ExtendScript 引擎解释脚本。

所有 Adobe Creative Cloud 应用程序，包括 Adobe Photoshop CC 2015，都使用 ExtendScript，这是 Adobe 对 JavaScript 的扩展实现。ExtendScript 文件以 `.jsx` 扩展名区分。ExtendScript 提供了所有标准 JavaScript 功能，以及额外的功能和实用工具，例如：

-   * 调试环境（ExtendScript Toolkit）
- 本地化实用工具
- 允许您组合脚本并将其定向到特定应用程序的工具
- 平台无关的文件和文件夹表示

许多 JavaScript 对象和方法使用 ExtendScript 中定义的对象，例如 `File` 对象、`Folder` 对象和 `UnitValue` 对象。因此，为脚本文件使用 `.jsx` 扩展名更为可取。

有关这些和附加功能的详细信息，请参阅 *JavaScript 工具指南*。本文档随 Creative Cloud 应用程序安装在以下位置：

-   * 在 Windows 上：
    `C:\Program Files\Adobe\Adobe Utilities\ExtendScript Toolkit CC 2015\SDK`
- 在 Mac OS 上：
    Applications/Utilities/Adobe Utilities/ExtendScript Toolkit CC/SDK

本文档和 ExtendScript Toolkit 的最新版本也可以从 Adobe Developer Center (http://www.adobe.com/devnet/) 下载。

# 执行脚本

Adobe Photoshop CC 2015 界面包含一个脚本菜单（**文件 > 脚本**），可快速便捷地访问您的 JavaScript。脚本可以直接列为菜单项，选择时运行，也可以导航并运行文件系统中的任何 JavaScript。

如果 Adobe Photoshop CC 2015 在脚本执行过程中遇到错误，它会显示错误消息。

# 安装脚本

要将 JavaScript 安装到脚本菜单，请将其放在 Scripts 文件夹（**Photoshop CC 2015/Presets/Scripts**）中。Scripts 文件夹中的脚本名称（不含文件扩展名）将显示在脚本菜单中。脚本菜单中可以安装任意数量的脚本。

在 Adobe Photoshop CC 2015 运行时添加到 Scripts 文件夹的脚本，要到下次启动应用程序时才会出现在脚本菜单中。

Scripts 文件夹及其子文件夹中的所有脚本都会显示在 **文件 > 脚本** 菜单的顶层。添加子文件夹不会为脚本菜单添加层次结构组织。

# 执行其他脚本

**脚本** 菜单末尾的 **浏览** 项（**文件 > 脚本 > 浏览**）允许您执行未安装在 Scripts 文件夹中的脚本。您也可以使用“浏览”来选择在上次启动应用程序后安装在 Scripts 文件夹中的脚本。

选择 **浏览** 将显示一个文件浏览器对话框，允许您选择要执行的脚本文件。浏览对话框中仅显示 .js 或 .jsx 文件。选择脚本文件时，其执行方式与安装的脚本相同。

# 启动脚本

启动时，Adobe Photoshop CC 2015 会执行它在启动文件夹中找到的所有 .jsx 文件。

-   * 在 Windows 上，用于用户定义脚本的启动文件夹是：
    C:\Program Files\Common Files\Adobe\Startup Scripts CC\Adobe Photoshop
- 在 Mac OS 上，用于用户定义脚本的启动文件夹是：
    ~/Library/Application Support/Adobe/Startup Scripts CC/Adobe Photoshop

如果一个脚本打算仅由 Adobe Photoshop CC 2015 执行，它必须包含如下所示的代码：

```javascript
if( BridgeTalk.appName == "photoshop" ) {
    //继续执行脚本
}
```

有关更多详细信息，请参阅 *JavaScript 工具指南*。



## 对象模型用法与命名

JavaScript API 遵循 JavaScript 命名约定，所有类（对象类型）以大写字母开头，并采用混合大小写。在 JavaScript 中，通常使用 `new` 运算符来实例化类：

```
new ClassName();
```

然而，在 Photoshop 对象模型中，通常不需要这样做。主要的对象类型被收集到集合类中；例如，`Document` 对象列表包含在 `Documents` 集合对象中。然后，你可以通过对象层次结构中其容器中的相应集合属性来访问该集合对象。

例如，所有打开的文档集合包含在顶级 `Application` 对象中。你可以通过全局变量 `app` 访问它，或者直接在顶层引用其属性：

```
app.documents[0] // 获取第一个加载的文档
documents[0] // 这是相同的
```

集合属性与集合对象同名，但以小写字母开头。例如，一个 `Document` 包含一个 `LayerSets` 集合，而一个 `LayerSet` 包含一个 `ArtLayers` 集合。要访问集合中的一个 `ArtLayer` 对象：

```
var myLayer = activeDocument.layerSets[0].artLayers[0];
```

如示例所示，集合可以被视为数组，这对迭代很有用。它们还提供方法来创建其包含的对象，以及按名称访问它们：

```
var newLayer = activeDocument.artLayers.add(); // 创建一个新的 ArtLayer 对象
newLayer.name = "My Layer"; // 命名以便后续引用
...
var layerRef = activeDocument.artLayers.getByName("My Layer");
```

某些对象，例如 `app.fonts` 集合中包含的 `Font` 对象，是由应用程序创建的，而不是由你的脚本创建。

你的脚本确实使用 JavaScript `new` 运算符来创建辅助对象，例如那些封装了以特定格式打开或保存文档的一组选项的对象：

```
var opts = new PDFOpenOptions();
opts.page = 10;
app.open(myPDFFile, opts);
```

## 2 JavaScript 对象参考

本章按字母顺序和表格格式介绍了 Photoshop 对象（Adobe® Photoshop® CC 2015 的 JavaScript 类型库）。给出了几个对象模型类的示例代码，以帮助说明对象类的语法和用法。

### 对象描述

每个对象的属性和方法在单独的表格中描述。以下各节描述了这些描述中使用的约定。

### 属性表示法

对象的属性表列出以下内容：

- 每个对象中定义的属性。
- 每个属性的值类型。
  当值类型是常量或另一个对象时，该值是链接到该常量或对象列表的超文本链接。
- 属性的输入状态：只读或读写。
- 解释属性作用的描述。

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **displayDialogs** | [DialogModes](DialogModes) | 读写。应用程序的对话框模式，控制运行脚本时应显示哪些类型的对话框。 |

对于常量，如示例中的 [DialogModes](DialogModes)，点击链接可查看显示允许值的表格。常量由对象表示，允许值是这些对象的属性。以 *ConstantName.VALUE* 的形式指定常量值。例如：

```
app.displayDialogs = DialogModes.ERROR;
```

### 方法表示法

对象的方法表列出以下内容：

- 方法名称。
- 参数列表。
- 参数值类型，位于与每个参数对应的行上。
- 返回值类型。
- 方法功能的描述，以及在需要时对参数的进一步描述。

| 方法 | 参数类型 | 返回值 | 功能说明 |
| :--- | :--- | :--- | :--- |
| **crop** (bounds [, angle] [, width] [, height]) | 4 个 UnitValue 的数组<br>number UnitValue UnitValue | | 裁剪文档。bounds 参数是裁剪后剩余区域的四个坐标的数组，[left, top, right, bottom]。 |

当参数类型或返回值是常量或另一个对象时，该值是链接到该常量或对象列表的超文本链接。

参数可以是必需的或可选的。可选参数在表中用方括号 ([]) 表示。在示例中，第一个参数 *bounds* 是必需的。其余参数都是可选的。

你必须为每个必需参数传递一个值。如果没有要传递的剩余值，可以省略可选参数；但是，如果你希望为任何非最后指定的可选参数使用默认值，请传递 `undefined` 作为占位符。你必须按列出的顺序输入值，以便 JavaScript 编译器知道你输入的是哪个值。

例如，以下仅传递必需参数（使用先前定义的变量作为边界区域）：

```
app.activeDocument.crop( myRegion );
```

以下跳过 *angle* 参数，指定 *width* 值，并省略最后的 *height* 值：

```
var myWidth = new UnitValue( "500 pixels" );
app.executeAction( myRegion,undefined,myWidth );
```

## ActionDescriptor

此对象提供了一种字典式机制，用于以键值对的形式存储数据。它可用于对 Photoshop 的低级访问。用法示例参见第 169 页的“选择示例脚本”。

许多配置文件使用序列化的动作描述符来表示其数据。例如，它用于在 `Application.playbackParameters` 中封装播放选项，并由 `Application.getCustomOptions()` 返回。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `count` | number | 只读。描述符中包含的键数。 |
| `typename` | string | 只读。引用的 `actionDescriptor` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |
| --- | --- | --- | --- |
| `clear()` | | | 清除描述符。 |
| `erase(key)` | number | | 从描述符中删除一个键。 |
| `fromStream(value)` | string | | 从字节流创建描述符；用于从磁盘读取。 |
| `getBoolean(key)` | number | boolean | 获取布尔类型的键值。 |
| `getClass(key)` | number | number | 获取类类型的键值。 |
| `getData(key)` | number | string | 获取原始字节数据作为字符串值。 |
| `getDouble(key)` | number | number | 获取双精度类型的键值。 |
| `getEnumerationType(key)` | number | number | 获取键的枚举类型。 |
| `getEnumerationValue(key)` | number | number | 获取键的枚举值。 |
| `getInteger(key)` | number | number | 获取整数类型的键值。 |
| `getKey(index)` | number | number | 获取第 N 个键的 ID，由索引提供。 |
| **getLargeInteger** (key) | number | number | 获取大整数类型的键值。 |
| **getList** (key) | number | ActionList | 获取列表类型的键值。 |
| **getObjectType** (key) | number | number | 获取对象类型键中对象的类 ID。 |
| **getObjectValue** (key) | number | ActionDescriptor | 获取对象类型的键值。 |
| **getPath** (key) | number | File | 获取文件类型的键值。 |
| **getReference** (key) | number | ActionReference | 获取 ActionReference 类型的键值。 |
| **getString** (key) | number | string | 获取字符串类型的键值。 |
| **getType** (key) | number | DescValueType | 获取键的类型。 |
| **getUnitDoubleType** (key) | number | number | 获取 UnitDouble 类型键的单位类型。 |
| **getUnitDoubleValue** (key) | number | number | 获取 UnitDouble 类型的键值。 |
| **hasKey** (key) | number | boolean | 检查描述符是否包含提供的键。 |
| **isEqual** (otherDesc) | ActionDescriptor | boolean | 确定描述符是否与另一个描述符相同。 |
| **putBoolean** (key, value) | number boolean | | 设置布尔类型键的值。 |
| **putClass** (key, value) | number number | | 设置类类型键的值。 |
| **putData** (key, value) | number string | | 将原始字节数据作为字符串值放入。 |
| **putDouble** (key, value) | number number | | 设置双精度类型键的值。 |
| **putEnumerated** (key, enumType, value) | number number number | | 设置键的枚举类型和值。 |



## ActionList

此对象提供了一种数组式的数据存储机制。它可用于对 Photoshop 进行底层访问。

此对象非常适合存储相同类型的数据。列表中的所有项必须是同一类型。

您可以使用 "put" 方法（例如 `putBoolean()`）来追加新元素，并且可以使用 `clear()` 清空整个列表，但不能以其他方式修改列表。

> **注意：** `ActionList` 对象是 Action Manager 功能的一部分。有关使用 Action Manager 的详细信息，请参阅 *Photoshop CC 2015 脚本指南*。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `count` | `number` | 只读。构成操作的命令数量。 |
| `typename` | `string` | 只读。引用的 `ActionList` 对象的类名。 |

## 方法

除 `clear()` 方法外，您使用此对象的方法来获取列表中特定类型数据的值或设置（放入）值类型。

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `clear()` | | | 清空列表。 |
| `getBoolean(index)` | `number` | `boolean` | 获取布尔类型的列表元素值。 |
| `getClass(index)` | `number` | `number` | 获取类类型的列表元素值。 |
| `getData(index)` | `number` | `string` | 获取原始字节数据作为字符串值。 |
| `getDouble(index)` | `number` | `number` | 获取双精度浮点类型的列表元素值。 |
| `getEnumerationType(index)` | `number` | `number` | 获取列表元素的枚举类型。 |
| `getEnumerationValue(index)` | `number` | `number` | 获取列表元素的枚举值。 |
| `getInteger(index)` | `number` | `number` | 获取整数类型的列表元素值。 |
| `getLargeInteger(index)` | `number` | `number` | 获取长整数类型的列表元素值。 |
| `getList(index)` | `number` | `ActionList` | 获取列表类型的列表元素值。 |
| `getObjectType(index)` | `number` | `number` | 获取对象类型列表元素的类 ID。 |
| `getObjectValue(index)` | `number` | `ActionDescriptor` | 获取对象类型的列表元素值。 |
| `getPath(index)` | `number` | `File` | 获取文件类型的列表元素值。 |
| `getReference(index)` | `number` | `ActionReference` | 获取 ActionReference 类型的列表元素值。 |
| `getString(index)` | `number` | `string` | 获取字符串类型的列表元素值。 |
| `getType(index)` | `number` | `DescValueType` | 获取列表元素的类型。 |
| `getUnitDoubleType(index)` | `number` | `number` | 获取双精度浮点类型列表元素的单位值类型。 |
| `getUnitDoubleValue(index)` | `number` | `number` | 获取双精度浮点类型列表元素的单位值。 |
| `putBoolean(value)` | `boolean` | | 追加一个新值，true 或 false。 |
| `putClass(value)` | `number` | | 追加一个新值，一个类或数据类型。 |
| `putData(value)` | `string` | | 追加一个新值，一个包含原始字节数据的字符串。 |
| `putDouble(value)` | `number` | | 追加一个新值，一个双精度浮点数。 |
| `putEnumerated(enumType, value)` | `number`<br>`number` | | 追加一个新值，一个枚举（常量）值。 |
| `putInteger(value)` | `number` | | 追加一个新值，一个整数。 |
| `putLargeInteger(value)` | `number` | | 追加一个新值，一个长整数。 |
| `putList(value)` | `ActionList` | | 追加一个新值，一个嵌套的操作列表。 |
| `putObject(classID, value)` | `number`<br>`ActionDescriptor` | | 追加一个新值，一个对象。 |
| `putPath(value)` | `File` | | 追加一个新值，一个路径。 |
| `putReference(value)` | `ActionReference` | | 追加一个新值，一个对在脚本中创建的对象的引用。 |
| `putString(value)` | `string` | | 追加一个新值，一个字符串。 |
| `putUnitDouble(classID, value)` | `number`<br>`number` | | 追加一个新值，一个单位/值对。 |

## ActionReference

此对象提供有关操作所引用内容的信息。例如，当引用某个事物的名称时，您可能会使用 keyName。该引用还需要知道您指的是哪个名称。在这种情况下，您可以使用 classDocument 表示文档名称，或使用 classLayer 表示图层名称。它可用于对 Photoshop 进行底层访问。包含与 ActionDescriptor 关联的数据。

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `typename` | `string` | 只读。引用的 Action 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `getContainer()` | | `ActionReference` | 获取包含在此引用中的容器引用。容器引用为引用提供额外的部分。它看起来像另一个引用，但实际上属于同一引用的一部分。 |
| `getDesiredClass()` | | `number` | 获取表示对象类别的数字。 |
| `getEnumeratedType()` | | `number` | 获取枚举类型。 |
| `getEnumeratedValue()` | | `number` | 获取枚举值。 |
| `getForm()` | | `ReferenceFormType` | 获取此操作引用的形式。 |
| `getIdentifier()` | | `number` | 获取形式为标识符的引用的标识符值。 |
| `getIndex()` | | `number` | 获取列表或数组中引用的索引值。 |
| `getName()` | | `string` | 获取引用的名称。 |
| `getOffset()` | | `number` | 获取对象索引值的偏移量。 |
| `getProperty()` | | `number` | 获取属性 ID 值。 |
| `putClass(desiredClass)` | `number` | | 将新的类形式和类类型放入引用。 |
| `putEnumerated(desiredClass, enumType, value)` | `number`<br>`number`<br>`number` | | 将枚举类型和 ID 与引用的所需类一起放入引用。 |
| `putIdentifier(desiredClass, value)` | `number`<br>`number` | | 将新的标识符和值放入引用。 |
| `putIndex(desiredClass, value)` | `number`<br>`number` | | 将新的索引和值放入引用。 |
| `putName(desiredClass, value)` | `number`<br>`string` | | 将新的名称和值放入引用。 |
| `putOffset(desiredClass, value)` | `number`<br>`number` | | 将新的偏移量和值放入引用。 |
| `putProperty(desiredClass, value)` | `number`<br>`number` | | 将新的属性和值放入引用。 |

## Application

Adobe Photoshop CC 2015 应用程序对象，它是对象模型的根，并提供对所有其他对象的访问。此对象提供应用程序范围的信息，例如应用程序默认值和可用字体。它提供了许多重要方法，例如用于打开文件和加载文档的方法。

要访问属性和方法，您可以使用预定义的全局变量 `app`。例如：

```javascript
var docRef = app.documents.add(800, 600, 72, "docRef", NewDocumentMode.RGB);
```

`Application` 对象的属性和方法也可在顶层使用；您可以完全省略对 `Application` 对象的引用。例如：

```javascript
var docRef = documents.add(800, 600, 72, "docRef", NewDocumentMode.RGB);
```

这种用法可能会有些模糊；为清晰起见，建议您使用对 `app` 的显式引用。

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `activeDocument` | `Document` | 读写。最前面的文档。设置此属性等同于在 Adobe Photoshop CC 2015 应用程序中单击一个打开的文档以将其带到屏幕最前面。**提示：** 如果没有打开的文档，访问此属性将引发异常。 |
| `backgroundColor` | `SolidColor` | 读写。文档的默认背景颜色和颜色样式。 |
| `build` | `string` | 只读。应用程序的信息。 |
| `colorSettings` | `string` | 读写。当前颜色设置的名称，通过“编辑” > “颜色设置”选择。 |
| `currentTool` | `string` | 读写。当前所选工具的名称。 |
| `displayDialogs` | `DialogModes` | 读写。应用程序的对话框模式，用于控制运行脚本时应显示哪些类型的对话框。 |
| `documents` | `Documents` | 只读。打开文档的集合。这是访问应用程序中当前打开文档的主要入口点。此数组允许您访问任何打开的文档，或遍历所有打开的文档。 |
| `fonts` | `TextFonts` | 只读。此系统上安装的字体。 |
| `foregroundColor` | `SolidColor` | 读写。默认前景颜色（用于绘制、填充和描边选区）。 |



| 属性 | 值类型 | 说明（续） |
| --- | --- | --- |
| `freeMemory` | 数字 | 只读。Adobe Photoshop CC 2015 可用的未使用内存量。 |
| `locale` | 字符串 | 只读。应用程序的语言区域设置。<br><br>Adobe 区域代码由一个 2 字母的 ISO-639 语言代码和一个可选的 2 字母 ISO 3166 国家/地区代码组成，中间用下划线分隔。区分大小写。例如 `en_US`、`en_UK`、`ja_JP`、`de_DE`、`fr_FR`。 |
| `macintoshFileTypes` | 字符串数组 | 只读。Adobe Photoshop CC 2015 可以打开的文件图像类型列表。 |
| `measurementLog` | MeasurementLog | 已执行测量的日志。 |
| `name` | 字符串 | 只读。应用程序的名称。 |
| `notifiers` | Notifiers | 只读。当前配置的通知器集合（位于 Adobe Photoshop CC 2015 应用程序的脚本事件管理器菜单中）。 |
| `notifiersEnabled` | 布尔值 | 可读写。如果所有通知器均已启用，则为 true。 |
| `path` | File | 只读。Adobe Photoshop CC 2015 应用程序位置的完整路径。 |
| `playbackDisplayDialogs` | DialogModes | 可读写。回放模式的对话框模式，控制在使用动作调板回放录制的动作时显示何种类型的对话框。 |
| `playbackParameters` | ActionDescriptor | 可读写。存储和检索作为录制动作一部分使用的参数。例如，可用于控制回放速度。 |
| `preferences` | Preferences | 只读。应用程序首选项设置（等同于在 Windows 的 Adobe Photoshop CC 2015 应用程序中选择 **编辑 > 首选项**，或在 Mac OS 中选择 Photoshop > 首选项）。 |
| `preferencesFolder` | File | 只读。“首选项”文件夹的完整路径。 |
| `recentFiles` | File 数组 | 只读。“最近使用文件”列表中的文件。 |
| `scriptingBuildDate` | 字符串 | 只读。脚本接口的构建日期。 |
| `scriptingVersion` | 字符串 | 只读。脚本接口的版本。 |
| `systemInformation` | 字符串 | 只读。应用程序和系统的运行时详细信息。 |
| `typename` | 字符串 | 只读。被引用 app 对象的类名。 |
| `version` | 字符串 | 只读。你正在运行的 Adobe Photoshop 应用程序版本。 |
| `windowsFileTypes` | 字符串数组 | 只读。Adobe Photoshop CC 2015 可以打开的文件图像扩展名列表。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |
| :--- | :--- | :--- | :--- |
| `batch` (`inputFiles`, `action`, `from` [, `options`]) | `File 数组`<br>`string`<br>`string`<br>`BatchOptions` | `string` | 运行批处理自动化例程（类似于“文件 > 自动化 > 批处理”命令）。inputFiles 参数指定批处理命令要处理的文件来源。 |
| `beep` () | | | 发出“嘟”的声音。 |
| `bringToFront` () | | | 使 Adobe Photoshop CC 2015 成为活动（最前面的）应用程序。 |
| `changeProgressText` (`progressString`) | `string` | | 更改进度窗口中显示的文本。progressString 参数是要在进度窗口中显示的字符串。 |
| `charIDToTypeID` (`charID`) | `string` | `number` | 将四字符代码（字符 ID）转换为运行时 ID。 |
| `doAction` (`action`, `from`) | `string`<br>`string` | | 从动作调板播放动作。action 参数是动作的名称，from 参数是动作组的名称。 |
| `doForcedProgress` (`progressString`, `javaScriptString`) | `string`<br>`string` | | 带进度条执行任务。强制显示进度条，忽略通常会阻止其不必要显示的启发式规则（例如，在非常短的任务期间）。必须定期调用其他进度 API 来更新进度条并允许取消。progressString 参数是要在进度窗口中显示的字符串，javaScriptString 参数是要执行的字符串。 |
| **doProgress**<br>(progressString, javaScriptString) | string<br>string | | 带进度条执行任务。必须定期调用其他进度 API 来更新进度条并允许取消。<br>`progressString` 参数是要在进度窗口中显示的字符串，`javaScriptString` 参数是要执行的字符串。 |
| **doProgressSegmentTask**<br>(segmentLength, done, total, javaScriptString) | number<br>number<br>number<br>string | boolean | 从进度条的未使用部分划分出一段用于执行子任务。取消时返回 false。当遍历运行时间不等的任务列表时，应使用此方法。<br>`segmentLength` 参数是当前任务的长度，`done` 参数是所有已完成任务的总长度，`total` 参数是所有任务的总长度。`javaScriptString` 参数是要执行的字符串。 |
| **doProgressSubTask**<br>(index, limit, javaScriptString) | number<br>number<br>string | boolean | 从进度条的未使用部分划分出一段用于执行子任务。取消时返回 false。当遍历运行时间相等的任务列表时，应使用此方法。<br>`index` 参数是当前任务的从 0 开始的索引，`limit` 参数是任务总数，`javaScriptString` 参数是要执行的字符串。 |
| **doProgressTask**<br>(taskLength, javaScriptString) | number<br>string | boolean | 从进度条的未使用部分划分出一段用于执行子任务。取消时返回 false。<br>`taskLength` 参数是要划分的未使用进度条的量，范围在 0.0 到 1.0 之间。`javaScriptString` 参数是要执行的字符串。 |
| **eraseCustomOptions**<br>(key) | string | | 从 Photoshop 注册表中删除具有指定 ID 值的用户对象。 |
| **executeAction**<br>(eventID<br>[, descriptor]<br>[, displayDialogs]) | number<br>ActionDescriptor<br>DialogModes | ActionDescriptor | 播放一个 Action Manager 事件。 |
| **executeActionGet**<br>(reference) | ActionReference | ActionDescriptor | 获取有关预定义或录制动作的信息。 |
| **featureEnabled**<br>(name) | string | boolean | 确定由 `name` 指定的功能是否已启用。<br>以下功能支持作为 `name` 的值：<br>"photoshop/extended"<br>"photoshop/standard"<br>"photoshop/trial" |
| **getCustomOptions**<br>(key) | string | ActionDescriptor | 从 Photoshop 注册表中检索 ID 值为 `key` 的用户对象。 |
| **isQuicktimeAvailable**<br>() | | boolean | 如果安装了 Quicktime，则返回 true。 |
| **load**<br>(document) | File | | 从指定位置加载支持文件（相对于 Photoshop 图像文档）。 |
| **makeContactSheet**<br>(inputFiles<br>[, options]) | File 数组<br>ContactSheetOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |
| **makePDFPresentation**<br>(inputFiles,<br>outputFiles<br>[, options]) | File 数组<br>File<br>PresentationOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |
| **makePhotoGallery**<br>(inputFolder,<br>outputFolder<br>[, options]) | File<br>File<br>GalleryOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |
| **makePhotomerge**<br>(inputFiles) | File 数组 | string | 在 Adobe Photoshop CC 2015 中已弃用。请使用提供的脚本：<br>`runphotomergeFromScript = true;`<br>`$.evalFile( app.path +`<br>`"Presets/Scripts/Photomerge.jsx")`<br>`photomerge.createPanorama(` <br>`fileList, displayDialog );`<br>将多个文件合并为一个，需要用户交互。 |
| **makePicturePackage**<br>(inputFiles<br>[, options]) | File 数组<br>PicturePackageOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |



## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| **open**<br>(文档 [, as] [, asSmartObject]) | File 对象或 OpenDocumentType 布尔值 | Document | 打开指定的文档。<br>使用可选参数 `as` 通过 `OpenDocumentType` 中的常量指定文件格式；或者，您可以使用以下对象同时指定文件格式及其打开选项：<br>[CameraRAWOpenOptions](https://example.com)<br>[DICOMOpenOptions](https://example.com)<br>[EPSOpenOptions](https://example.com)<br>[PDFOpenOptions](https://example.com)<br>[PhotoCDOpenOptions](https://example.com)<br>[RawFormatOpenOptions](https://example.com)<br>使用可选参数 `asSmartObject`（默认值：`false`）为打开的文档创建智能对象。<br>请参阅 Application 示例脚本，了解如何在 `open` 方法中使用 File 对象。 |
| **openDialog**<br>() | | File 数组 | 调用 Photoshop 的“打开”对话框，供用户选择文件。<br>返回一个包含对话框中所选文件的 File 对象数组。 |
| **purge**<br>(目标) | PurgeTarget | | 清除一个或多个缓存。 |
| **putCustomOptions**<br>(键, 自定义对象 [, 持久化]) | string ActionDescriptor boolean | | 将自定义设置对象保存到 Photoshop 注册表中。<br>`键` 是自定义设置的唯一标识符。<br>`自定义对象` 是要保存到注册表中的对象。<br>`持久化` 指示脚本执行完毕后对象是否应持久保存。 |
| **refresh**<br>() | | | 在应用程序刷新时暂停脚本。用于减慢执行速度，并在脚本运行时向用户显示结果。请谨慎使用；使用此方法时脚本运行速度会显著变慢。 |
| **refreshFonts**<br>() | | | 强制更新字体列表。 |
| **runMenuItem**<br>(菜单ID) | number | | 根据菜单 ID 运行指定的菜单项。 |
| **showColorPicker**<br>() | | boolean | 如果取消对话框则返回 false，否则返回 true。 |
| **stringIDToTypeID**<br>(字符串ID) | string | number | 将字符串 ID 转换为运行时 ID。 |
| **togglePalettes**<br>() | | | 切换面板可见性。 |
| **toolSupportsBrushes**<br>(工具) | string | boolean | 如果指定工具支持画笔则返回 true，否则返回 false。 |
| **typeIDToCharID**<br>(类型ID) | number | string | 将运行时 ID 转换为字符 ID。 |
| **typeIDToStringID**<br>(类型ID) | number | string | 将运行时 ID 转换为字符串 ID。 |
| **updateProgress**<br>(已完成,<br>总数) | number<br>number | boolean | 更新由 `doProgress` 方法启动的进度条。此方法应用于基于手动的非任务进度更新。取消时返回 false。<br><br>`已完成` 参数是已完成的任务数，`总数` 参数是任务总数。 |

### 应用程序示例脚本

### Application.jsx

此脚本会调用一个警告框，显示应用程序的重要属性，例如版本号、应用程序路径、可用内存量以及打开的文档数量。

当用户按下警告框上的“确定”按钮时，会打开第二个对话框，询问用户是否要将前景色和背景色设置为当前打开文档的颜色。如果没有打开的文档，该脚本会为用户打开一个新文档。

该脚本（在未打开文档时）会产生三个连续的对话框。

```
//创建欢迎消息
// 使用应用程序对象的 name 和 version 属性
// 将应用程序名称和版本附加到欢迎消息中
// 使用 "\r" 插入回车符
// 使用组合运算符 += 将信息附加到消息中
var message = "欢迎使用 " + app.name
message += " 版本 " + app.version + "\r\r"

// 查找 Adobe Photoshop CC 2015 的安装位置
// 并将路径添加到消息中
// 在 path 属性中添加可选参数 fsName
// 以最常用的格式显示文件系统名称
message += "我安装在 " + app.path.fsName + "\r\r"

// 查看 Adobe Photoshop CC 2015 有多少可用内存
message += "您有以下内存量可用于 Adobe Photoshop CC 2015：" +
app.freeMemory + "\r\r"

// 使用 documents 对象的 length 属性
// 查看打开了多少个文档
var documentsOpen = app.documents.length
message += "您当前打开了 " + documentsOpen + " 个文档。\r\r"

// 向用户显示消息
alert(message)

// 对于“是”回答，answer 为 true，对于“否”回答，则为 false
var answer = confirm("是否将前景色和背景色设置为我喜欢的颜色？")

// 设置颜色
if (answer) {
    // 我没有特别喜欢的颜色。你可能想知道我为什么这样问。
    app.foregroundColor.rgb.red = Math.random() * 255
    app.foregroundColor.rgb.green = Math.random() * 255
    app.foregroundColor.rgb.blue = Math.random() * 255
    app.backgroundColor.rgb.red = Math.random() * 255
    app.backgroundColor.rgb.green = Math.random() * 255
    app.backgroundColor.rgb.blue = Math.random() * 255
}

// 打开一个文档
if (app.documents.length == 0) {

    // 使用应用程序路径和到 Samples 文件夹的偏移量
    var sampleDocToOpen = File(app.path + "/Samples/Fish.psd")

    // 组合包含文件名的消息
    message = "是否要我为您打开一个示例？（"
    message += sampleDocToOpen.fsName
    message += "）"

    // 再次询问用户
    answer = confirm(message)

    // 相应地打开文档
    if (answer) {
        open(sampleDocToOpen)
    }
}
```

### PDFPresentation.jsx

此脚本将图像序列呈现为 Adobe PDF 幻灯片放映。

```
// 使用 Samples 文件夹中的所有文件
var inputFolder = new Folder(app.path + "/Samples/")

// 检查是否有可用内容
if (inputFolder != null) {

    // 获取此文件夹中所有 Adobe Photoshop CC 2015
    //（.psd 格式）文件
    var inputFiles = inputFolder.getFiles("*.psd")

    // 输出到桌面
    var outputFile = File("~/Desktop/JavaScriptPresentation.pdf")

    // 有默认设置，但我喜欢自己设置选项
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

## ArtLayer

文档中包含图像视觉元素的对象（相当于 Adobe Photoshop CC 2015 应用程序中的图层）。

通过 `Document.artLayers` 集合访问文档中的图层。您可以通过名称访问图层；例如：

```
var layerRef = app.activeDocument.artLayers.getByName("my layer");
layerRef.allLocked = true;
```

通过父级图层组中的 `LayerSet.artLayers` 集合访问图层组中的图层。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| allLocked | boolean | 读写。设置为 true 可完全锁定此图层的内容和设置。 |
| blendMode | BlendMode | 读写。混合模式。 |
| bounds | UnitValue 数组 | 只读。描述图层边界矩形的坐标数组。 |
| boundsNoEffects | UnitValue 数组 | 只读。描述图层（不包括效果）边界矩形的坐标数组。 |
| fillOpacity | number [0.0..100] | 读写。图层的内部不透明度，以百分比表示。 |
| filterMaskDensity | double | 读写。滤镜蒙版的密度（介于 0.0 到 250.0 之间）。 |
| filterMaskFeather | double | 读写。滤镜蒙版的羽化（介于 0.0 到 250.0 之间）。 |
| grouped | boolean | 读写。如果此图层与其下方的图层编组，则为 true。 |
| isBackgroundLayer | boolean | 读写。如果这是文档的背景图层，则为 true。一个文档只能有一个背景图层。如果没有背景图层，将此属性设置为 true 会使其成为背景图层。 |
| kind | LayerKind | 读写。为一个空图层设置类型（例如“文字图层”）。<br>仅当图层为空且 `isBackgroundLayer` 为 false 时有效。请参阅 `isBackgroundLayer`。<br>您可以使用 `kind` 属性将背景图层转换为普通图层；但是，要将图层转换为背景图层，必须将 `isBackgroundLayer` 设置为 `true`。 |



## 属性

| 属性名 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| layerMaskDensity | double | 读写。图层蒙版的密度（在 0.0 到 100.0 之间） |
| layerMaskFeather | double | 读写。图层蒙版的羽化（在 0.0 到 250.0 之间） |
| linkedLayers | ArtLayer 或 LayerSet 的数组 | 只读。链接到此图层的图层。参见 ArtLayer.link。 |
| name | string | 读写。名称。 |
| opacity | number [0.0..100.0]. | 读写。图层的主不透明度，一个百分比值。 |
| parent | Document | 只读。对象的容器。 |
| pixelsLocked | boolean | 读写。如果图层图像中的像素无法使用画笔工具编辑，则为真。 |
| positionLocked | boolean | 读写。如果图层图像中的像素无法在图层内移动，则为真。 |
| textItem | TextItem | 只读。与图层关联的文本项目。仅当 kind = LayerKind.TEXT 时有效。 |
| transparentPixelsLocked | boolean | 读写。如果编辑被限制在图层的不透明部分，则为真。 |
| typename | string | 只读。引用的 artLayer 对象的类名。 |
| vectorMaskDensity | double | 读写。矢量蒙版的密度（在 0.0 到 250.0 之间） |
| vectorMaskFeather | double | 读写。矢量蒙版的羽化（在 0.0 到 250.0 之间） |
| visible | boolean | 读写。如果图层可见，则为真。 |
| xmpMetadata | xmpMetadata | 读写。图层的元数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |
| :--- | :--- | :--- | :--- |
| **adjustBrightnessContrast**<br>(brightness,<br>contrast) | number<br>number |  | 调整亮度（范围 [-100..100]）和对比度（范围 [-100..100]）。 |
| **adjustColorBalance**<br>([shadows]<br>[, midtones]<br>[, highlights]<br>[, preserveLuminosity]) | number 的数组<br>number 的数组<br>number 的数组<br>boolean |  | 调整图层组件通道的颜色平衡。对于 **shadows**（阴影）、**midtones**（中间调）和 **highlights**（高光），数组必须包含三个值，范围在 [-100..100] 之间，分别表示青色或红色、品红色或绿色、黄色或蓝色，具体取决于文档模式是 CMYK 还是 RGB。<br><br>参见 [Document.mode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/properties/document.html#document-mode "Document.mode")。 |
| **adjustCurves**<br>(curveShape) | number 的二维数组 |  | 使用最多十四个点调整所选通道的色调范围。<br><br>`curveShape` 数组中的每个值都是一个点对，即一个包含 x 和 y 整数值的数组。 |
| **adjustLevels**<br>(inputRangeStart,<br>inputRangeEnd,<br>inputRangeGamma,<br>outputRangeStart,<br>outputRangeEnd) | number [0..253]<br>number [(start + 2)..255]<br>number [0.10..9.99]<br>number [0..253]<br>number [(start + 2)..255] |  | 调整所选通道的色阶。 |
| **applyAddNoise**<br>(amount,<br>distribution,<br>monochromatic) | number [0.1..400]<br>[NoiseDistribution](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/enums/noisedistribution.html "NoiseDistribution")<br>boolean |  | 应用“添加杂色”滤镜。<br><br>`amount` 是一个百分比值。 |
| **applyAverage**<br>() |  |  | 应用“平均值”滤镜。 |
| **applyBlur**<br>() |  |  | 应用“模糊”滤镜。 |
| **applyBlurMore**<br>() |  |  | 应用“进一步模糊”滤镜。 |
| **applyClouds**<br>() |  |  | 应用“云彩”滤镜。 |
| **applyCustomFilter**<br>(characteristics,<br>scale,<br>offset) | number 的数组<br>number<br>number |  | 应用自定义滤镜。<br><br>`characteristics` 数组有 25 个成员。<br><br>具体说明请参见 Adobe Photoshop CC 2015 帮助。 |
| **applyDeInterlace**<br>(eliminateFields,<br>createFields) | EliminateFields<br>CreateFields |  | 应用“逐行”滤镜。 |
| **applyDespeckle**<br>() |  |  | 应用“去斑”滤镜。 |
| **applyDifferenceClouds**<br>() |  |  | 应用“分层云彩”滤镜。 |
| **applyDiffuseGlow**<br>(graininess,<br>glowAmount,<br>clearAmount) | number [0..10]<br>number [0..20]<br>number [0..20] |  | 应用“扩散亮光”滤镜。 |
| **applyDisplace**<br>(horizontalScale,<br>verticalScale,<br>displacement,<br>undefinedareas,<br>displacementMapFiles) | number [-999..999]<br>number [-999..999]<br>DisplacementMapType<br>UndefinedAreas<br>File |  | 使用指定的水平比例和垂直比例、映射类型、未扭曲区域的处理方式以及扭曲图像映射的路径，应用“置换”滤镜。 |
| **applyDustAndScratches**<br>(radius,<br>threshold) | number [1..100]<br>number [0..255] |  | 应用“蒙尘与划痕”滤镜。 |
| **applyGaussianBlur**<br>(radius) | number [0.1..250.0] |  | 在指定半径（以像素为单位）内应用“高斯模糊”滤镜。 |
| **applyGlassEffect**<br>(distortion,<br>smoothness,<br>scaling<br>[, invert]<br>[, texture]<br>[, textureFile]) | number [0..20]<br>number [1..15]<br>number [50..200]<br>boolean<br>TextureType<br>File |  | 应用“玻璃”滤镜。scaling 是一个百分比值。 |
| **applyHighPass**<br>(radius) | number [0.1..250.0] |  | 在指定半径内应用“高反差保留”滤镜。 |
| **applyLensBlur**<br>( [source]<br>[, focalDistance]<br>[, invertDepthMap]<br>[, shape]<br>[, radius]<br>[, bladeCurvature]<br>[, rotation]<br>[, brightness]<br>[, threshold]<br>[, amount]<br>[, distribution]<br>[, monochromatic]<br>) | DepthMapSource<br>number<br>boolean<br>Geometry<br>number<br>number<br>number<br>number<br>number<br>number<br>NoiseDistribution<br>boolean |  | 应用“镜头模糊”滤镜。<br>source：深度图的来源（默认：DepthMapSource.NONE）<br>focalDistance：深度图的模糊焦距（默认：0）。<br>invertDepthMask：如果反转深度图则为真（默认：false）。<br>shape：光圈的形状（默认：Geometry.HEXAGON）<br>radius：光圈的半径（默认：15）。<br>bladeCurvature：光圈的叶片曲率（默认：0）。<br>rotation：光圈的旋转（默认：0）<br>brightness：高光的亮度（默认：0）。<br>threshold：高光的阈值（默认：0）。<br>amount：杂色的数量（默认：0）<br>distribution：杂色的分布值（默认：NoiseDistribution.UNIFORM）。<br>monochromatic：如果杂色为单色则为真（默认：false）。 |
| **applyLensFlare**<br>(brightness,<br>flareCenter,<br>lensType) | number<br>array(UnitValue)<br>LensType |  | 应用“镜头光晕”滤镜，指定亮度（0-300，作为百分比）、光晕中心的 x 和 y 坐标（单位值）以及镜头类型。 |
| **applyMaximum**<br>(radius) | number [1..100] |  | 在指定半径（以像素为单位）内应用“最大值”滤镜。 |
| **applyMedianNoise**<br>(radius) | number [1..100] |  | 在指定半径（以像素为单位）内应用“中间值”滤镜。 |
| **applyMinimum**<br>(radius) | number [1..100] |  | 在指定半径（以像素为单位）内应用“最小值”滤镜（1 - 100）。 |
| **applyMotionBlur**<br>(angle,<br>radius) | number [-360..360]<br>number [1..999] |  | 应用“动感模糊”滤镜。 |
| **applyNTSC**<br>() |  |  | 应用 NTSC 颜色滤镜。 |
| **applyOceanRipple**<br>(size,<br>magnitude) | number [1..15]<br>number [0..20] |  | 应用“海洋波纹”滤镜。 |
| **applyOffset**<br>(horizontal,<br>vertical,<br>undefinedAreas) | UnitValue<br>UnitValue<br>OffsetUndefinedAreas |  | 将图层水平移动和垂直移动指定的数量（最小/最大数量取决于图层大小），在图层的原始位置留下一个未定义区域。 |
| **applyPinch**<br>(amount) | number [-100..100] |  | 应用“挤压”滤镜。*amount* 是一个百分比值。 |
| **applyPolarCoordinates**<br>(conversion) | PolarConversionType |  | 应用“极坐标”滤镜。 |
| **applyRadialBlur**<br>(amount,<br>blurMethod,<br>blurQuality<br>[, blurCenter]) | number [1..100]<br>RadialBlurMethod<br>RadialBlurQuality<br>UnitValue |  | 使用指定的数量应用“径向模糊”滤镜，使用旋转或缩放效果以及指定的质量。参数 *blurCenter* 是位置（单位值）。 |
| **applyRipple**<br>(amount,<br>size) | number [-999..999]<br>RippleSize |  | 以指定的数量在图像中应用“波纹”滤镜，并指定大小。 |
| **applySharpen**<br>() |  |  | 应用“锐化”滤镜。 |
| **applySharpenEdges**<br>() |  |  | 应用“锐化边缘”滤镜。 |
| **applySharpenMore**<br>() |  |  | 应用“进一步锐化”滤镜。 |



### ArtLayer 示例脚本

以下脚本将打开样本文件夹中的所有文件，创建一个多图层文档。每个图层被粘贴到四个象限中的一个，并设置为50%透明度。最后，图层按名称排序。

```
ArtLayer.jsx
```

```
// 保存当前首选项
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// 将 Adobe Photoshop CC 2015 设置为使用像素且不显示任何对话框
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

// 关闭所有打开的文档
while (app.documents.length) {
    app.activeDocument.close()
}

// 创建一个新文档，用于合并所有样本
var mergedDoc = app.documents.add(1000, 1000, 72, "Merged Samples",
    NewDocumentMode.RGB, DocumentFill.TRANSPARENT, 1)

// 使用应用程序路径并附加样本文件夹
var samplesFolder = Folder(app.path + "/Samples/")

// 获取文件夹中的所有文件
var fileList = samplesFolder.getFiles()

// 打开每个文件
for (var i = 0; i < fileList.length; i++) {
    // fileList 包含文件夹和文件，因此只打开文件
    if (fileList[i] instanceof File) {
        open(fileList[i])

        // 使用文档名称作为合并文档中的图层名称
        var docName = app.activeDocument.name

        // 拼合文档以获取所有内容，然后复制
        app.activeDocument.flatten()
        app.activeDocument.selection.selectAll()
        app.activeDocument.selection.copy()

        // 不保存我们所做的任何更改
        app.activeDocument.close(SaveOptions.DONOTSAVECHANGES)

        // 通过在文档上创建随机选择区域来粘贴
        // 方法是将文档划分为四个象限，并通过选择该区域
        // 粘贴到其中一个象限
        var topLeftH = Math.floor(Math.random() * 2)
        var topLeftV = Math.floor(Math.random() * 2)
        var docH = app.activeDocument.width.value / 2
        var docV = app.activeDocument.height.value / 2
        var selRegion = Array(Array(topLeftH * docH, topLeftV * docV),
            Array(topLeftH * docH + docH, topLeftV * docV),
            Array(topLeftH * docH + docH, topLeftV * docV + docV),
            Array(topLeftH * docH, topLeftV * docV + docV),
            Array(topLeftH * docH, topLeftV * docV))
        app.activeDocument.selection.select(selRegion)
        app.activeDocument.paste()

        // 更改图层名称和不透明度
        app.activeDocument.activeLayer.name = docName
        app.activeDocument.activeLayer.fillOpacity = 50
    }
}
```



```
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

## ArtLayers

文档或图层组中 ArtLayer 对象的集合。

通过 Document.artLayers 或 LayerSet.artLayers 集合访问。例如：

```
var layerRef = docRef.artLayers.add()
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。artLayers 集合中的元素数量。 |
| parent | Document | 只读。对象的容器。 |
| typename | string | 只读。引用的 artLayers 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| add () | | ArtLayer | 在文档中创建一个新的艺术图层，并将新对象添加到此集合中。 |
| getByName (name) | string | ArtLayer | 获取 artLayers 集合中具有所提供名称的第一个元素。 |
| removeAll () | | | 从 artLayers 集合中移除所有元素。 |

## BatchOptions

使用 Application.batch() 方法运行批处理操作的选项。

JavaScript 仅支持文件夹作为批处理命令的源。请将批处理源文件夹指定为 Application.batch() 方法的 `inputFiles` 参数。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **destination** | BatchDestinationType | 可读写。处理后文件的目标类型（默认：BatchDestinationType.NODESTINATION）。 |
| **destinationFolder** | Folder | 可读写。处理后文件的文件夹位置。仅当 **destination** = BatchDestinationType.FOLDER 时有效。 |
| **errorFile** | File | 可读写。用于记录遇到错误的文件。要直接在屏幕上显示错误（并在发生错误时停止批处理），请留空。 |
| **fileNaming** | array of FileNamingType | 可读写。文件命名选项列表（最多：6 项）。仅当 **destination** = BatchDestinationType.FOLDER 时有效。 |
| **macintoshCompatible** | boolean | 可读写。True 表示使最终文件名与 Macintosh 兼容（默认：`true`）。仅当 **destination** = BatchDestinationType.FOLDER 时有效。 |
| **overrideOpen** | boolean | 可读写。True 表示覆盖动作中的打开命令（默认：`false`）。 |
| **overrideSave** | boolean | 可读写。True 表示用指定的目标覆盖另存为动作步骤（默认：`false`）。仅当 **destination** = BatchDestinationType.FOLDER 或 SAVEANDCLOSE 时有效。 |
| **startingSerial** | number | 可读写。用于命名文件的起始序号（默认：`1`）。仅当 **destination** = BatchDestinationType.FOLDER 时有效。 |
| **suppressOpen** | boolean | 可读写。True 表示抑制文件打开选项对话框（默认：`false`）。 |
| **suppressProfile** | boolean | 可读写。True 表示抑制颜色配置文件警告（默认：`false`）。 |
| **typename** | string | 只读。引用的 `batchOptions` 对象的类名。 |
| **unixCompatible** | boolean | 可读写。True 表示使最终文件名与 Unix 兼容（默认：`true`）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| **windowsCompatible** | boolean | 可读写。True 表示使最终文件名与 Windows 兼容（默认：`true`）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |

## BitmapConversionOptions

使用 Document.changeMode() 配合 ChangeMode.Bitmap 将图像转换为位图模式的选项。

在将图像转换为位图模式之前，请先将彩色图像转换为灰度。参见 ArtLayer.desaturate() 方法。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **angle** | `number [-180..180]` | 可读写。用于设置单个点方向的角度（以度为单位）。参见 shape。仅当 method = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| **frequency** | `number [1.0..999.99]` | 可读写。要使用的打印机点数（每英寸）。仅当 method = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| **method** | BitmapConversionType | 可读写。要使用的转换方法（默认：`BitmapConversionType.DIFFUSIONDITHER`）。 |
| **patternName** | `string` | 可读写。要使用的图案名称。有关预装的有效图案的信息，请参阅 Adobe Photoshop CC 2015 帮助中的位图转换命令，或在选择位图转换命令后查看“自定义颜色”下拉框中可用的选项。仅当 method = `BitmapConversionType.CUSTOMPATTERN` 时有效。 |
| **resolution** | `number` | 可读写。以像素/英寸为单位的输出分辨率（默认：`72.0`）。 |
| **shape** | BitmapHalfToneType | 可读写。要使用的点形状。仅当 method = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| **typename** | `string` | 只读。引用的 `bitmapConversionOptions` 对象的类名。 |

## BMPSaveOptions

使用 Document.saveAs() 方法将文档保存为 BMP 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alphaChannels | boolean | 可读写。True 表示保存 Alpha 通道。 |
| depth | BMPDepthType | 可读写。每通道的位数。 |
| flipRowOrder | boolean | 可读写。True 表示从上到下写入图像（默认：false）。仅当 osType = OperatingSystem.WINDOWS 时可用。 |
| osType | OperatingSystem | 可读写。目标操作系统。（默认：OperatingSystem.WINDOWS）。 |
| rleCompression | boolean | 可读写。True 表示使用 RLE 压缩。仅当 osType = OperatingSystem.WINDOWS 时可用。 |
| typename | string | 只读。引用的 BMPSaveOptions 对象的类名。 |

## CameraRAWOpenOptions

使用 Application.open 方法打开 Camera RAW 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **bitsPerChannel** | BitsPerChannelType | 可读写。每通道的位数。 |
| **blueHue** | `number [-100..100]` | 可读写。拍摄图像的蓝色色相。 |
| **blueSaturation** | `number [-100..100]` | 可读写。拍摄图像的蓝色饱和度。 |
| **brightness** | `number [0..150]` | 可读写。拍摄图像的亮度。 |
| **chromaticAberrationBY** | `number [-100..100]` | 可读写。拍摄图像的色差 B/Y。 |
| **chromaticAberrationRC** | `number [-100..100]` | 可读写。拍摄图像的色差 R/C。 |
| **colorNoiseReduction** | `number [0..100]` | 可读写。拍摄图像的彩色杂色减少。 |
| **colorSpace** | ColorSpaceType | 可读写。图像的色彩空间。 |
| **contrast** | `number [-50..100]` | 可读写。拍摄图像的对比度。 |
| **exposure** | `number [-4.0..4.0]` | 可读写。拍摄图像的曝光度。 |
| **greenHue** | `number [-100..100]` | 可读写。拍摄图像的绿色色相。 |
| **greenSaturation** | `number [-100..100]` | 可读写。拍摄图像的绿色饱和度。 |
| **luminanceSmoothing** | `number [0..100]` | 可读写。拍摄图像的亮度平滑。 |
| **redHue** | `number [-100..100]` | 可读写。拍摄图像的红色色相。 |
| **redSaturation** | `number [-100..100]` | 可读写。拍摄图像的红色饱和度。 |
| **resolution** | `number [1..999]` | 可读写。文档的分辨率，以像素/英寸为单位。 |
| **saturation** | `number [-100..100]` | 可读写。拍摄图像的饱和度。 |
| **settings** | CameraRAWSettingsType | 可读写。所有 Camera RAW 选项的全局设置。默认：CameraRAWSettingsType.CAMERA。 |
| **shadows** | `number [0..100]` | 可读写。拍摄图像的阴影。 |
| **shadowTint** | `number [-100..100]` | 可读写。拍摄图像的阴影色调。 |
| **sharpness** | `number [0..100]` | 可读写。拍摄图像的锐度。 |
| **size** | CameraRAWSize | 可读写。新文档的大小。 |
| **temperature** | `number [2000..50000]` | 可读写。拍摄图像的色温。 |
```



Adobe Photoshop CC 2015

JavaScript 脚本参考

JavaScript 对象参考 72

| 属性 | 值类型 | 描述（续） |
| :--- | :--- | :--- |
| `tint` | number [-150..150] | 可读写。照片的色调。 |
| `typename` | string | 只读。引用的 cameraRAWOpenOptions 对象的类名。 |
| `vignettingAmount` | number [-100..100] | 可读写。照片的暗角强度。 |
| `vignettingMidpoint` | number [-100..100] | 可读写。照片的暗角中点。 |
| `whiteBalance` | WhiteBalanceType | 可读写。图像的白平衡选项。这些是影响色彩平衡的光照条件。 |

# 通道

关于图像中颜色元素的信息。

通过 [Document.channels](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#Document) 集合访问。你可以通过索引或名称在此列表中访问单个通道对象。例如，以下代码按名称访问活动文档中的一个通道对象并为其分配一个 `opacity` 值：

```
var channelRef = app.activeDocument.channels.getByName("my channel");
channelRef.opacity = 22;
```

通道类似于印刷过程中应用单一颜色的印版。文档的颜色模式决定了默认通道的数量；例如，RGB 文档有三个通道：红、绿和蓝。颜色也可以有一个 Alpha 通道，它以蒙版形式存储选区；或者一个专色通道，它存储专色。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `color` | [SolidColor](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#SolidColor) | 可读写。通道的颜色。<br>当 `kind` = `ChannelType.COMPONENT` 时无效。 |
| `histogram` | array of number | 只读。通道颜色的直方图。该数组包含 256 个成员。<br>当 `kind` = `ChannelType.COMPONENT` 时无效。对于分量通道直方图值，请改用 [Document](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#Document) 对象的 [histogram](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#Document) 属性。 |
| `kind` | [ChannelType](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#ChannelType) | 可读写。通道的类型。 |
| `name` | string | 可读写。通道的名称。 |
| `opacity` | number [0..100] | 可读写。用于 Alpha 通道的不透明度，或用于专色通道的实度。<br>仅当 `kind` = `ChannelType.MASKEDAREA` 或 `SELECTEDAREA` 时有效。 |
| `parent` | [Document](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#Document) | 只读。包含此通道的文档。 |
| `typename` | string | 只读。引用的 `channel` 对象的类名。 |
| `visible` | boolean | 可读写。如果通道可见则为真。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `duplicate ([targetDocument])` | [Document](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#Document) | [Channel](https://www.adobe.com/devnet-docs/photoshop/topicjavascriptref/#Channel) | 复制通道。 |
| **merge**<br>() | | | 将专色通道合并到分量通道中。 |
| **remove**<br>() | | | 删除通道。 |

## 通道集合

文档中 [Channel](#) 对象的集合。

通过 [Document.channels](#) 集合属性访问。例如：

```
var channelRef = app.activeDocument.channels.add()
```

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| length | number | 只读。`channels` 集合中的元素数量。 |
| parent | [Document](#) | 只读。包含此集合的文档。 |
| typename | string | 只读。引用的 `channels` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
|---|---|---|---|
| add() | | [Channel](#) | 创建一个新的通道对象并将其添加到此集合中。 |
| getByName(name) | string | [Channel](#) | 获取 `channels` 集合中具有所提供名称的第一个元素。 |
| removeAll() | | | 从 `channels` 集合中移除所有 Alpha 通道对象。 |

### 通道示例脚本

以下脚本会在没有文件打开时打开一个文件，然后为活动文档中的通道编写一个直方图报告 (histogram.log)。

> **注意：** 此脚本包含一个使用 `break` 语句的 switch 结构。`break` 语句需要一个结尾分号 (;)，如下例所示：

`break;`

### Histogram.jsx

```
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
```

```
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
```

```
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

// if there are no documents open then try to open a sample file
if (app.documents.length == 0) {
    open(File(app.path + "/Samples/Fish.psd"))
}

// get a reference to the working document
var docRef = app.activeDocument
```

```
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
    myChannels[channelIndex].visible = true

    // turn off all the other channels
    for (var secondaryIndex = 0; secondaryIndex < myChannels.length;
         secondaryIndex++) {
        if (channelIndex != secondaryIndex) {
            myChannels[secondaryIndex].visible = false
        }
    }

    // Use the function to dump the histogram
    OutputHistogram(myChannels[channelIndex].histogram,
                    myChannels[channelIndex].name, fileOut)
```



// 关闭输出文件
fileOut.close()
alert("直方图文件已保存至: " + fileOut.fsName)

// 重置活动通道
docRef.activeChannels = myActiveChannels

// 重置应用程序首选项
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.displayDialogs = startDisplayDialogs

// 接受直方图和名称并转储到输出文件的实用函数
function OutputHistogram(inHistogram, inHistogramName, inOutFile) {

    // 查找哪个计数值最大
    // 我将所有内容都缩放到这个数字以进行输出
    var largestCount = 0

    // 一个可重复使用的简单索引器
    var histogramIndex = 0

    // 查看我们总共有多少个样本
    var histogramCount = 0

    // 搜索所有项目并找到最大的单个项目
    for (histogramIndex = 0; histogramIndex < inHistogram.length;
            histogramIndex++) {
        histogramCount += inHistogram[histogramIndex]
        if (inHistogram[histogramIndex] > largestCount)
            largestCount = inHistogram[histogramIndex]
    }

    // 这两个值应该匹配
    if (histogramCount != totalCount) {
        alert("发生了错误！")
    }

    // 查看每个 "X" 代表多少像素
    var pixelsPerX = largestCount / 100

    // 将此数据输出到文件
    inOutFile.write("一个 X = " + pixelsPerX + " 像素。\n")

    // 输出此直方图的名称
    inOutFile.write(inHistogramName + "\n")

    // 遍历所有项目并按以下格式输出
    // 001
    // 002
    for (histogramIndex = 0; histogramIndex < inHistogram.length;
            histogramIndex++) {

        // 此行项目需要额外的 "0" 以保持所有内容对齐
        if (histogramIndex < 10)
            inOutFile.write("0")

        // 此行项目需要额外的 "0" 以保持所有内容对齐
        if (histogramIndex < 100)
            inOutFile.write("0")

        // 将索引输出到文件
        inOutFile.write(histogramIndex)

        // 一些空格使其看起来美观
        inOutFile.write(" ")

        // 计算我需要多少个 X
        var outputX = inHistogram[histogramIndex] / largestCount * 100

        // 输出 X
        for (var a = 0; a < outputX; a++)
            inOutFile.write("X")

        inOutFile.write("\n")
    }

    inOutFile.write("\n")
}

# CMYKColor

定义一种 CMYK 颜色，用于 SolidColor 对象。

另请参阅 GrayColor、HSBColor、LabColor、NoColor、RGBColor。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| black | number [0.0..100.00] | 可读写。黑色值（以百分比表示）。 |
| cyan | number [0.0..100.00] | 可读写。青色值（以百分比表示）。 |
| magenta | number [0.0..100.00] | 可读写。洋红色值（以百分比表示）。 |
| typename | string | 只读。引用的 CMYKColor 对象的类名。 |
| yellow | number [0.0..100.00] | 可读写。黄色值（以百分比表示）。 |

# ColorSampler

文档的颜色取样器。通过 Document.colorSamplers 集合访问。例如：

```
var colorSamplerRef = app.activeDocument.colorSamplers[0];
var currentColor = colorSamplerRef.color;
```

**注意：** 有关颜色取样器的更多信息，请参阅 Adobe Photoshop CC 2015 帮助中的颜色取样器工具。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| **color** | [SolidColor](SolidColor) | 只读。颜色取样器的颜色。 |
| **position** | array of [UnitValue](UnitValue) | 只读。颜色取样器在文档中的位置。数组 (x,y) 表示计数项目的水平和垂直位置。 |
| **parent** | [Document](Document) | 只读。所属文档。 |
| **typename** | string | 只读。引用的 `ColorSampler` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| **move** (position) | array of [UnitValue](UnitValue) | | 将颜色取样器移动到文档中的新位置。`position` 参数 (x,y) 表示移动后的颜色取样器的新水平和垂直位置。 |
| **remove** () | | | 删除 `ColorSampler` 对象。 |

# ColorSamplers

文档中 ColorSampler 对象的集合。通过 Document.colorSamplers 集合属性访问。例如：

```
app.activeDocument.colorSamplers.removeAll()
```

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `length` | number | 只读。`ColorSamplers` 集合中的元素数量。 |
| `parent` | [Document](Document) | 只读。所属文档。 |
| `typename` | string | 只读。引用的 `ColorSamplers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `add` (position) | array of [UnitValue](UnitValue) | [ColorSampler](ColorSampler) | 创建一个新的颜色取样器对象并将其添加到此集合中。`position` 参数 (x,y) 表示移动后的颜色取样器的新水平和垂直位置。 |
| `removeAll` () | | | 从 `ColorSamplers` 集合中移除所有 `ColorSampler` 对象。 |

# ContactSheetOptions

使用 Application.makeContactSheet() 方法创建联系表的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| **acrossFirst** | boolean | 可读写。为 true 则先水平（从左到右，然后从上到下）放置图像（默认值：*true*）。 |
| **bestFit** | boolean | 可读写。为 true 则旋转图像以实现最佳适应（默认值：*false*）。 |
| **caption** | boolean | 可读写。为 true 则使用文件名作为图像的说明文字（默认值：*true*）。 |
| **columnCount** | number [1..100] | 可读写。要包含的列数（默认值：5）。 |
| **flatten** | boolean | 可读写。为 true 则在最终文档中合并所有图层（默认值：*true*）。 |
| **font** | [GalleryFontType](GalleryFontType) | 可读写。用于说明文字的字体（默认值：GalleryFontType.ARIAL）。 |
| **fontSize** | number | 可读写。用于说明文字的字号（默认值：12）。 |
| **height** | number [0..29000] | 可读写。生成文档的高度（以像素为单位）（默认值：720）。 |
| **horizontal** | number | 可读写。图像之间的水平间距（以像素为单位）（默认值：1）。 |
| **mode** | [NewDocumentMode](NewDocumentMode) | 可读写。文档颜色模式（默认值：NewDocumentMode.RGB）。 |
| **resolution** | number [35..1200] | 可读写。文档的分辨率，以每英寸像素数为单位（默认值：72.0）。 |
| **rowCount** | number [1..100] | 可读写。要使用的行数（默认值：6）。 |
| **typename** | string | 只读。引用的 contactSheetOptions 对象的类名。 |
| **useAutoSpacing** | boolean | 可读写。为 true 则自动设置图像间距（默认值：true）。 |
| **vertical** | number [0..29000] | 可读写。图像之间的垂直间距（以像素为单位）（默认值：1）。仅在 useAutoSpacing = *false* 时有效。 |
| **width** | number [100..29000] | 可读写。生成文档的宽度（以像素为单位）（默认值：576）。 |

# CountItem

文档中的计数项目。通过 Document.countItems 集合访问。请参阅 Document.autoCount() 方法。

**注意：** 此功能仅在扩展版中可用。

有关计数项目的更多信息，请参阅 Adobe Photoshop CC 2015 帮助中的计数工具。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| **position** | `array of UnitValue` | 只读。计数项目在文档中的位置。 |
| **parent** | [Document](Document) | 只读。所属文档。 |
| **typename** | `string` | 只读。引用的 `CountItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `remove()` | | | 删除 `CountItem` 对象。 |



## CountItems

文档中的 [CountItem](https://helpx.adobe.com/photoshop/using/counting-tool.html) 对象集合。

通过 [Document.countItems](https://helpx.adobe.com/photoshop/using/counting-tool.html) 集合属性访问。例如：

`app.activeDocument.countItems.removeAll()`

**注意：** 此功能仅在扩展版中可用。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `length` | number | 只读。`CountItems` 集合中的元素数量。 |
| `parent` | [Document](https://helpx.adobe.com/photoshop/using/scripting.html#document) | 只读。包含此集合的文档。 |
| `typename` | string | 只读。被引用的 `CountItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `add(position)` | [UnitValue](https://helpx.adobe.com/photoshop/using/unit-value.html) 数组 | [CountItem](https://helpx.adobe.com/photoshop/using/counting-tool.html) | 创建一个新的计数项对象并将其添加到此集合中。<br>参数 `position` (x, y) 分别表示 `CountItem` 对象的水平和垂直位置。 |
| `getByName(name)` | string | [CountItem](https://helpx.adobe.com/photoshop/using/counting-tool.html) | 获取 `CountItems` 集合中具有指定名称的第一个元素。 |
| `removeAll()` | | | 从 `CountItems` 集合中移除所有 `CountItem` 对象。 |

## DCS1_SaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法将 CMYK 文档保存为 DCS1 格式的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| **dCS** | [DCSType](DCSType) | 可读写。（默认：DCSType.COLORCOMPOSITE）。 |
| **embedColorProfile** | boolean | 可读写。为 true 时在文档中嵌入颜色配置文件。 |
| **encoding** | [SaveEncoding](SaveEncoding) | 可读写。用于文档的编码类型（默认：SaveEncoding.BINARY）。 |
| **halftoneScreen** | boolean | 可读写。为 true 时包含半调网屏（默认：false）。 |
| **interpolation** | boolean | 可读写。为 true 时使用图像插值（默认：false）。 |
| **preview** | [Preview](Preview) | 可读写。预览类型（默认：Preview.MACOSEIGHTBIT）。 |
| **transferFunction** | boolean | 可读写。为 true 时包含用于补偿图像和胶片之间网点扩大的传递函数（默认：false）。 |
| **typename** | string | 只读。被引用的 DCS1_SaveOptions 对象的类名。 |
| **vectorData** | boolean | 可读写。为 true 时包含矢量数据。仅在文档包含矢量数据（未栅格化文本）时有效。 |

## DCS2_SaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法将 CMYK 文档保存为 DCS2 格式的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| dcs | [DCSType](DCSType) | 可读写。要创建的复合文件类型（默认：`DCSType.NOCOMPOSITE`）。 |
| embedColorProfile | boolean | 可读写。为 true 时在文档中嵌入颜色配置文件。 |
| encoding | [SaveEncoding](SaveEncoding) | 可读写。要使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| halftoneScreen | boolean | 可读写。为 true 时包含半调网屏（默认：`false`）。 |
| interpolation | boolean | 可读写。为 true 时使用图像插值（默认：`false`）。 |
| multiFileDCS | boolean | 可读写。为 true 时将颜色通道保存为多个文件或单个文件（默认：`false`）。 |
| preview | [Preview](Preview) | 可读写。预览类型（默认：`Preview.MACOSEIGHTBIT`）。 |
| spotColors | boolean | 可读写。为 true 时保存专色。 |
| transferFunction | boolean | 可读写。为 true 时包含用于补偿图像和胶片之间网点扩大的传递函数（默认：`false`）。 |
| typename | string | 只读。被引用的 DCS2_SaveOptions 对象的类名。 |
| vectorData | boolean | 可读写。为 true 时包含矢量数据。仅在文档包含矢量数据（未栅格化文本）时有效。 |

## DICOMOpenOptions

使用 `Application.open()` 方法打开 DICOM 格式文档的选项。

> **注意：** 此功能仅在扩展版中可用。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| anonymize | boolean | 可读写。为 true 时使患者信息匿名化。 |
| columns | number | 可读写。n-up 配置中的列数。 |
| reverse | boolean | 可读写。为 true 时反转（颠倒）图像。 |
| rows | number | 可读写。n-up 配置中的行数。 |
| showOverlays | boolean | 可读写。为 true 时显示覆盖图。 |
| typename | string | 只读。被引用的 DICOMOpenOptions 对象的类名。 |
| windowLevel | number | 可读写。以 Houndsfield 单位表示的图像对比度。 |
| windowWidth | number | 可读写。以 Houndsfield 单位表示的图像亮度。 |

## Document

脚本中图层和所有其他对象的活动容器对象；文件的基本画布。

- 通过 `Application.activeDocument` 访问当前活动文档的对象。
- 你可以使用 `Application.documents` 集合中的列表访问其他文档，或遍历所有打开的文档。你可以通过索引访问列表中的单个文档，或使用 `Documents.getByName()` 按名称检索它们。
- 使用 `Documents.add()` 方法以编程方式创建文档。

有关示例，请参阅 `Document sample script` 和 `Documents` 集合对象。

**注意：** 在 Adobe Photoshop CC 2015 中，文档也可以称为图像或画布。

- 术语 *图像* 指整个文档及其内容。你可以裁剪或裁切图像。使用 `resizeImage()` 方法调整图像大小。
- 术语 *画布* 指文档在屏幕上占据的空间。你可以旋转或翻转画布。使用 `resizeCanvas()` 方法调整画布大小。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `activeChannels` | `Channel` 数组 | 可读写。选中的通道。 |
| `activeHistoryBrushSource` | `Guide` | 可读写。要与历史记录画笔一起使用的历史记录状态。 |
| `activeHistoryState` | `Guide` | 可读写。选中的 `HistoryState` 对象。 |
| `activeLayer` | `ArtLayer` 或 `LayerSet` | 可读写。选中的图层。 |
| `artLayers` | `ArtLayers` | 只读。图层集合。 |
| `backgroundLayer` | `ArtLayer` | 只读。文档的背景图层。 |
| `bitsPerChannel` | `BitsPerChannelType` | 可读写。每通道位数。 |
| `channels` | `Channels` | 只读。通道集合。 |
| `colorProfileName` | string | 可读写。颜色配置文件的名称。仅在 `colorProfileType` = `ColorProfile.CUSTOM` 或 `WORKING` 时有效。 |
| `colorProfileType` | `ColorProfileType` | 可读写。文档使用的是工作颜色配置文件、自定义配置文件还是没有配置文件。 |
| `colorSamplers` | `ColorSamplers` | 只读。与当前文档关联的颜色取样器。 |
| `componentChannels` | `Channel` 数组 | 只读。构成文档的颜色通道；例如，RGB 文档的红色、绿色和蓝色通道。 |
| `countItems` | [CountItems](https://helpx.adobe.com/photoshop/using/count-tool.html) | 只读。当前的计数项。注意：有关计数项的更多信息，请参阅 Adobe Photoshop CC 2015 关于计数工具的帮助。 |
| `fullName` | [File](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.File.html) | 只读。文档的完整路径名。 |
| `guides` | [Guides](https://helpx.adobe.com/photoshop/using/creating-guides.html) | 只读。参考线集合。 |
| `height` | [UnitValue](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.UnitValue.html) | 只读。文档的高度（单位值）。 |
| `histogram` | number 数组 | 只读。显示复合通道中每个颜色强度级别像素数量的直方图。该数组包含 256 个成员。仅在 [mode](https://helpx.adobe.com/photoshop/using/mode-conversion.html) = DocumentMode.RGB, CMYK 或 INDEXEDCOLOR 时有效。 |
| `historyStates` | [HistoryStates](https://helpx.adobe.com/photoshop/using/history-panel.html) | 只读。历史记录状态集合。 |
| `info` | [DocumentInfo](https://helpx.adobe.com/photoshop/using/document-properties.html) | 只读。关于文档的元数据。 |
| `layerComps` | [LayerComps](https://helpx.adobe.com/photoshop/using/layer-comps.html) | 只读。图层复合集合。 |
| `layers` | [Layers](https://helpx.adobe.com/photoshop/using/layer-basics.html) | 只读。图层集合。 |
| `layerSets` | [LayerSets](https://helpx.adobe.com/photoshop/using/layer-groups.html) | 只读。图层组集合。 |
| `managed` | boolean | 只读。如果文档是工作组文档则为 true。 |
| `measurementScale` | [MeasurementScale](https://helpx.adobe.com/photoshop/using/measuring-tools.html) | 只读。文档的测量比例。注意：测量比例功能仅在扩展版中可用。 |
| `mode` | [DocumentMode](https://helpx.adobe.com/photoshop/using/mode-conversion.html) | 只读。颜色配置文件。 |
| `name` | string | 只读。文档的名称。 |
| `parent` | [Application](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.Application.html) | 只读。包含此文档的应用程序对象。 |
| `path` | [File](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.File.html) | 只读。文档的路径。 |
| `pathItems` | [PathItems](https://helpx.adobe.com/photoshop/using/paths.html) | 只读。路径项集合。 |
| `pixelAspectRatio` | number [0.100..10.000] | 可读写。要使用的（自定义）像素宽高比。 |
| `printSettings` | [DocumentPrintSettings](https://helpx.adobe.com/photoshop/using/printing-photoshop-images.html) | 只读。文档的打印设置。 |



### Document 对象属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `quickMaskMode` | boolean | 读写。如果文档处于快速蒙版模式则为 true。 |
| `resolution` | number | 只读。文档的分辨率（以像素/英寸为单位）。 |
| `saved` | boolean | 只读。如果文档自上次更改后已保存则为 true。 |
| `selection` | [Selection](selection.html) | 只读。文档的选区。 |
| `typename` | string | 只读。Document 对象的类名。 |
| `width` | UnitValue | 只读。文档的宽度（单位值）。 |
| `xmpMetadata` | [xmpMetadata](xmpMetadata.html) | 只读。文档的 XMP 元数据。例如，图像的 Camera RAW 设置存储在此处。 |

### Document 对象方法

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| --- | --- | --- | --- |
| **autoCount**<br>(channel,<br>threshold) | [Channel](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#channel)<br>number | | 统计文档中对象的数量。仅在扩展版中可用。<br><br>为每个被统计的对象创建一个 [CountItem](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#countitem) 对象。<br><br>有关如何设置要计数的对象的更多信息，请参阅 Adobe Photoshop CC 2015 帮助中的计数工具。 |
| **changeMode**<br>(destinationMode<br>[, options]) | [ChangeMode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#changemode)<br>[BitmapConversionOptions](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#bitmapconversionoptions) 或 [IndexedConversionOptions](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#indexedconversionoptions) | | 更改文档的颜色配置文件。 |
| **close**<br>([saving]) | [SaveOptions](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#saveoptions) | | 关闭文档。如果进行了任何更改，脚本将显示一个带有三个选项的警报：保存、不保存、提示保存。可选参数指定警报框中的选择（默认值：`SaveOptionsType.PROMPTTOSAVECHANGES`）。 |
| **convertProfile**<br>(destinationProfile,<br>intent<br>[, blackPointCompensation]<br>[, dither]) | string<br>[Intent](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#intent)<br>boolean<br>boolean | | 更改颜色配置文件。<br><br>`destinationProfile` 参数必须是命名颜色模式的字符串，或者是 `Working RGB`、`Working CMYK`、`Working Gray`、`Lab Color`（表示一个工作颜色空间或 Lab 颜色）。 |
| **crop**<br>(bounds<br>[, angle]<br>[, width]<br>[, height]) | 由 4 个 [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#unitvalue) 组成的数组<br>number<br>[UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#unitvalue)<br>[UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#unitvalue) | | 裁剪文档。`bounds` 参数是裁剪后剩余区域的四个坐标数组 [left, top, right, bottom]。 |
| **duplicate**<br>([name ]<br>[, mergeLayersOnly]<br>) | string<br>boolean | [Document](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#document) | 创建 `document` 对象的副本。<br><br>可选参数 `name` 为复制的文档提供名称。<br><br>可选参数 `mergeLayersOnly` 指示是否仅复制合并的图层。 |
| **exportDocument**<br>(exportIn<br>[, exportAs]<br>[, options]) | File<br>ExportType<br>ExportOptionsIllustrator<br>-或-<br>ExportOptionsSaveForWeb | | 将文档中的路径导出为 Illustrator 文件，或将文档导出为具有 Web 或设备查看优化的文件。<br><br>这等同于选择 **文件 > 导出 > 路径到 Illustrator**，或 **文件 > 存储为 Web 和设备所用格式**。 |
| **flatten**<br>() | | | 拼合文档中的所有图层。 |
| **flipCanvas**<br>(direction) | Direction | | 在指定方向上翻转画布内的图像。 |
| **importAnnotations**<br>(file) | File | | 将注释导入到文档中。 |
| **mergeVisibleLayers**<br>() | | | 拼合文档中所有可见的图层。 |
| **paste**<br>([intoSelection]) | boolean | ArtLayer | 将剪贴板的内容粘贴到文档中。如果可选参数设置为 `true` 且选区处于活动状态，则将内容粘贴到选区中。 |
| **print**<br>([sourceSpace]<br>[, printSpace]<br>[, intent]<br>[blackPointCompensation]) | SourceSpaceType<br>string<br>Intent<br>boolean | | 打印文档。<br>`printSpace` 指定打印机的颜色空间。有效值为 `nothing`（即与源相同）；或 `Working RGB`、`Working CMYK`、`Working Gray`、`Lab Color`（表示一个工作颜色空间或 Lab 颜色）；或指定特定颜色空间的字符串（默认值与源相同）。 |
| **printOneCopy**<br>() | | | 打印文档的一份副本。 |
| **rasterizeAllLayers**<br>() | | | 栅格化所有图层。 |
| **recordMeasurements**<br>([source]<br>[, dataPoints]) | MeasurementSource<br>由字符串组成的数组 | | 记录文档的测量值。 |
| **resizeCanvas**<br>([width]<br>[, height]<br>[, anchor]) | UnitValue<br>UnitValue<br>AnchorPosition | | 更改画布的大小以显示更多或更少的图像，但不更改图像大小。请参阅 `resizeImage`。 |
| **resizeImage**<br>([width]<br>[, height]<br>[, resolution]<br>[, resampleMethod]<br>[, amount]) | UnitValue<br>UnitValue<br>number<br>ResampleMethod<br>number | | 更改图像的大小。<br>**amount** 参数控制使用保留细节时的噪点值量（范围：0 - 100）。 |
| **revealAll**<br>() | | | 扩展文档以显示被裁切的部分。 |
| **rotateCanvas**<br>(angle) | number | | 顺时针方向旋转画布（包括图像）。 |
| **save**<br>() | | | 保存文档。 |
| **saveAs**<br>(saveIn<br>[, options]<br>[, asCopy]<br>[, extensionType]) | File<br>object（见描述）<br>boolean<br>Extension | | 将文档保存为特定格式。<br>通过传递以下对象之一来指定与格式对应的保存选项：<br>BMPSaveOptions<br>DCS1_SaveOptions<br>DCS2_SaveOptions<br>EPSSaveOptions<br>GIFSaveOptions<br>JPEGSaveOptions<br>PDFSaveOptions<br>PhotoshopSaveOptions<br>PICTFileSaveOptions<br>PICTResourceSaveOptions<br>PixarSaveOptions<br>PNGSaveOptions<br>RawSaveOptions<br>SGIRGBSaveOptions<br>TargaSaveOptions<br>TiffSaveOptions |
| **splitChannels**<br>() | | 由 Document 组成的数组 | 将文档通道拆分为单独的图像。 |
| **suspendHistory**<br>(historyString<br>javaScriptString) | string<br>string | | 为整个脚本在历史记录状态中提供一个条目。允许对脚本中采取的所有操作进行一次撤销。<br><br>**historyString** 参数提供用于历史记录状态的字符串。<br><br>**javaScriptString** 参数提供在挂起历史记录时要执行的 JavaScript 代码字符串。 |
| **trap**<br>(width) | number | | 对 CMYK 文档应用陷印。<br>仅当 **docRef.mode** = DocumentMode.CMYK 时有效。 |
| **trim**<br>([top]<br>[, left]<br>[, bottom]<br>[, right]) | TrimType<br>boolean<br>boolean<br>boolean<br>boolean | | 裁剪画布指定边周围的透明区域。所有布尔参数的默认值为 `true`。 |

### Document 示例脚本

以下脚本创建一个文档，其中包含从 Adobe Photoshop CC 2015 示例文件夹中获取的两个图像（一朵向日葵和一只鸭子），并执行以下步骤：

- 确定哪个图像更大。
- 将较小的图像调整大小以匹配较大的图像。
- 创建一个高度为任一图像两倍的新文档，以容纳两个图像。
- 选择文档的一部分并将向日葵粘贴到选区中。
- 反转选区并将鸭子粘贴到文档的下半部分。
- 将向日葵定位在鸭子上方。

```javascript
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs
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
} else {
    app.activeDocument = flowerDoc
    flowerDoc.resizeImage(duckDoc.width, duckDoc.height)
}

// Create a new document twice as high as two files
```



## DocumentPrintSettings

文档的打印设置。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **backgroundColor** | SolidColor | 读写。页面的背景色。 |
| **bleedWidth** | UnitValue | 读写。出血宽度 |
| **caption** | boolean | 读写。打印在 FileInfo 中找到的说明文字。 |
| **centerCropMarks** | boolean | 读写。打印中心裁切标记。 |
| **colorBars** | boolean | 读写。打印色彩校准条。 |
| **copies** | number | 读写。要打印的份数。 |
| **cornerCropMarks** | boolean | 读写。打印边角裁切标记。 |
| **colorHandling** | PrintColorHandling | 只读。颜色处理。 |
| **activePrinter** | string | 读写。当前活动的打印机。 |
| **flip** | boolean | 读写。水平翻转图像。 |
| **hardProof** | boolean | 读写。打印硬打样。 |
| **interpolate** | boolean | 读写。 |
| **labels** | boolean | 读写。打印文档标题。 |
| **mapBlack** | boolean | 读写。映射黑色。 |
| **negative** | boolean | 读写。反转图像颜色。 |
| **renderIntent** | Intent | 读写。当打印空间与源空间不同时的颜色转换意图。 |
| **posX** | UnitValue | 只读。图像在页面上的 x 位置。 |
| **posY** | UnitValue | 只读。图像在页面上的 y 位置。 |
| **printBorder** | UnitValue | 读写。打印边框的宽度。 |
| **printerName** | string | 读写。打印机的名称。 |
| **printSpace** | string | 读写。用于打印机的颜色空间。可以为空（表示与源相同）；'Working RGB'、'Working CMYK'、'Working Gray'、'Lab Color'（表示工作空间之一或 Lab 颜色）；或者一个指定特定颜色空间的字符串（默认为与源相同） |
| **registrationMarks** | boolean | 读写。打印套准标记。 |
| **scale** | number | 只读。图像在页面上的缩放比例。 |
| **vectorData** | boolean | 读写。包含矢量数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| **setPagePosition** (docPosition, posX, posY, scale) | DocPositionStyle UnitValue UnitValue number |  | 设置图像在页面上的位置。 |

## DocumentInfo

关于 `document` 对象的元数据。

通过 [Document.info](https://www.adobe.com/devnet-docs/indesigndocs/JavaScriptRef/#Document.info) 属性访问。例如，以下代码设置 `author`、`caption` 和 `copyrighted` 属性：

```
var docRef = open(fileList[i])
// set the file info
docRef.info.author = "Mr. Adobe programmer"
docRef.info.caption = "Adobe Photo shoot"
docRef.info.copyrighted = CopyrightedType.COPYRIGHTEDWORK
```

这些值可以通过选择 **File > File Info** 进行交互式设置。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `author` | string | 读写。 |
| `authorPosition` | string | 读写。 |
| `caption` | string | 读写。 |
| `captionWriter` | string | 读写。 |
| `category` | string | 读写。 |
| `city` | string | 读写。 |
| `copyrighted` | [CopyrightedType](https://www.adobe.com/devnet-docs/indesigndocs/JavaScriptRef/#CopyrightedType) | 读写。版权状态。 |
| `copyrightNotice` | string | 读写。 |
| `country` | string | 读写。 |
| `creationDate` | string | 读写。 |
| `credit` | string | 读写。 |
| `exif` | array of array [tag data] | 只读。相机数据，包括拍摄图像时使用的相机设置。每个数组成员是一个标签对，即 [tag, tag_data] 的数组；例如 ["camera" "Cannon"]。 |
| `headline` | string | 读写。 |
| `instructions` | string | 读写。 |
| `jobName` | string | 读写。 |
| `keywords` | array of string | 读写。可用于标识文档或其内容的关键词列表。 |
| `ownerUrl` | string | 读写。 |
| `parent` | Document | 只读。info 对象的容器。 |
| `provinceState` | string | 读写。 |
| `source` | string | 读写。 |
| `supplementalCategories` | array of string | 读写。 |
| `title` | string | 读写。 |
| `transmissionReference` | string | 读写。 |
| `typename` | string | 只读。引用的 info 对象的类名。 |
| `urgency` | Urgency | 读写。 |

### DocumentInfo 示例脚本

以下脚本为指定文件夹中的所有文件设置文档信息（元数据），然后将修改后的文件作为低质量 JPEG 图像保存到新文件夹中，而不更改原始文件。

- 要求用户指定包含原始文件的文件夹和 JPEG 图像的输出文件夹，然后检查文件夹是否存在。
- 打开每个文件，并使用 documentInfo 对象属性为其标记以下元数据：
    - author：Adobe programmer
    - caption：Adobe Photo shoot
    - captionWriter：Adobe programmer
    - city：San Jose
    - copyrightNotice：Copyright (c) Adobe programmer Photography
    - copyrighted status：Copyrighted Work
    - country：USA
    - state：CA
- 以低质量设置将新文档保存为 JPEG 格式。

### DocumentInfo.jsx

```
// Save the current preferences
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs
app.displayDialogs = DialogModes.NO

// ask the user for the input and output folders
var inputFolder = Folder.selectDialog("Select a folder to tag")
var outputFolder = Folder.selectDialog("Select a folder for the output files")

// see if we got something interesting from the dialog
if (inputFolder != null && outputFolder != null) {
    // get all the files found in this folder
    var fileList = inputFolder.getFiles()
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

            // change the date to a Adobe Photoshop CC 2015 date format
            // "YYYYMMDD"
            var theDate = new Date()
            // the year is from 1900 ???? 
            var theYear = (theDate.getYear() + 1900).toString()
            // convert the month from 0..12 to 00..12
            var theMonth = theDate.getMonth().toString()
            if (theDate.getMonth() < 10) {
                theMonth = "0" + theMonth
            }
            // convert the day from 0..31 to 00.31
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
}

// Reset the application preferences
app.displayDialogs = startDisplayDialogs
```

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



## 文档

开放的 [Document](https://www.example.com) 对象集合。

可通过 `app` 全局变量或顶层直接访问 [Application.documents](https://www.example.com) 集合属性来获取此列表。例如，以下代码向集合中添加一个新文档：

```
app.documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
--或--
documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | 数字 | 只读。文档集合中的元素数量。 |
| parent | [Application](https://www.example.com) | 只读。所属的应用程序。 |
| typename | 字符串 | 只读。引用的文档对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| add ([宽度][, 高度][, 分辨率][, 名称][, 模式][, 初始填充][, 像素长宽比][, 每通道位数][, 颜色配置文件名称]) | [UnitValue](https://www.example.com) [UnitValue](https://www.example.com) 数字 字符串 [NewDocumentMode](https://www.example.com) [DocumentFill](https://www.example.com) 数字 [0.1..10.00] [BitsPerChannelType](https://www.example.com) 字符串 | [Document](https://www.example.com) | 创建一个新的文档对象并将其添加到此集合中。<br>像素长宽比：默认值为 1.0，即方形长宽比。<br>每通道位数：默认值为 BitsPerChannelType.EIGHT。 |
| getByName (name) | 字符串 | [Document](https://www.example.com) | 获取文档集合中第一个具有所提供名称的元素 |

## EPSOpenOptions

使用 `Application.open()` 方法打开 EPS 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `antiAlias` | 布尔值 | 可读写。为 true 表示使用抗锯齿。 |
| `constrainProportions` | 布尔值 | 可读写。为 true 表示约束图像的比例。 |
| `height` | [UnitValue](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。图像的高度（单位值）。 |
| `mode` | [OpenDocumentMode](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。用作文档模式的颜色配置文件。 |
| `resolution` | 数字 | 可读写。文档的分辨率（像素/英寸）。 |
| `typename` | 字符串 | 只读。引用的 `EPSOpenOptions` 对象的类名。 |
| `width` | [UnitValue](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。图像的宽度（单位值）。 |

## EPSSaveOptions

使用 `Document.saveAs()` 方法将文档另存为 EPS 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `embedColorProfile` | `布尔值` | 可读写。为 true 表示将颜色配置文件嵌入到此文档中。 |
| `encoding` | `SaveEncoding` | 可读写。要使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | `布尔值` | 可读写。为 true 表示包含半调网屏（默认：`false`）。 |
| `interpolation` | `布尔值` | 可读写。为 true 表示使用图像插值（默认：`false`）。 |
| `preview` | `Preview` | 可读写。预览类型。 |
| `psColorManagement` | `布尔值` | 可读写。为 true 表示使用 Postscript 颜色管理（默认：`false`）。 |
| `transferFunction` | `布尔值` | 可读写。为 true 表示包含用于补偿图像和胶片之间网点扩大的传递函数（默认：`false`）。 |
| `transparentWhites` | `布尔值` | 可读写。为 true 表示将白色区域显示为透明。<br><br>仅在 `document.mode = DocumentMode.BITMAP` 时有效。另请参见 `changeMode()`。 |
| `typename` | `字符串` | 只读。引用的 `EPSSaveOptions` 对象的类名。 |
| `vectorData` | `布尔值` | 可读写。为 true 表示包含矢量数据。<br><br>仅当文档包含矢量数据（文本）时有效。 |

## ExportOptionsIllustrator

使用 [Document.exportDocument()](https://example.com/Document.exportDocument) 方法将 [PathItem](https://example.com/PathItem) 对象导出到 Adobe Illustrator® 文件的选项。这些选项是您在选择 **文件 > 导出 > 路径到 Illustrator** 时可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **path** | `IllustratorPathType` | 可读写。要导出的路径类型（默认：`IllustratorPathType.DOCUMENTBOUNDS`）。 |
| **pathName** | `字符串` | 可读写。要导出的路径的名称。仅在 `path` = `IllustratorPathType.NAMEDPATH` 时有效。 |
| **typename** | `字符串` | 只读。引用的 `exportOptionsIllustrator` 对象的类名。 |

## ExportOptionsSaveForWeb

使用 [Document.exportDocument()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法为 Web 或设备优化文档的选项。这些是您在选择 **文件 > 存储为 Web 和设备所用格式** 时可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| **blur** | `数字` | 可读写。对图像应用模糊以减少瑕疵（默认：`0.0`）。 |
| **colorReduction** | [ColorReductionType](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。颜色减少算法（默认：`ColorReductionType.SELECTIVE`）。 |
| **colors** | `数字` | 可读写。调色板中的颜色数量（默认：`256`）。 |
| **dither** | [Dither](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。抖动类型（默认：`Dither.DIFFUSION`）。 |
| **ditherAmount** | `数字` | 可读写。抖动量（默认：`100`）。仅在 [dither](https://www.adobe.com/devnet/photoshop/scripting.html) = `Dither.DIFFUSION` 时有效。 |
| **format** | [SaveDocumentType](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。要使用的文件格式（默认：`SaveDocumentType.COMPU ServerGIF`）。**注意：** 对于此属性，仅支持 `COMPU ServerGIF`、`JPEG`、`PNG-8`、`PNG-24` 和 `BMP`。 |
| **includeProfile** | `布尔值` | 可读写。为 true 表示包含文档的嵌入颜色配置文件（默认：`false`）。 |
| **interlaced** | `布尔值` | 可读写。为 true 表示以多次传递方式下载；渐进式（默认：`false`）。 |
| **lossy** | `数字` | 可读写。允许的有损压缩量（默认：`0`）。 |
| **matteColor** | [RGBColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。用于混合透明像素的颜色。 |
| **optimized** | `布尔值` | 可读写。为 true 表示创建更小但兼容性较低的文件（默认：`true`）。仅在 [format](https://www.adobe.com/devnet/photoshop/scripting.html) = `SaveDocumentType.JPEG` 时有效。 |
| **PNG8** | `布尔值` | 可读写。指示位数；`true` = 8，`false` = 24（默认：`true`）。仅在 [format](https://www.adobe.com/devnet/photoshop/scripting.html) = `SaveDocumentType.PNG` 时有效。 |
| **quality** | `数字 [0..100]` | 可读写。生成图像的质量（百分比）；默认：60。 |
| **transparency** | `布尔值` | 可读写。指示图像的透明区域是否应包含在保存的图像中（默认：`true`）。 |
| **transparencyAmount** | `数字` | 可读写。透明度抖动量（默认：100）。<br><br>仅在 [`transparency`](#) = `true` 时有效。 |
| **transparencyDither** | `Dither` | 可读写。透明度抖动算法（默认：`transparencyDither` = `Dither.NONE`）。 |
| **typename** | `字符串` | 只读。引用的 ExportOptionsSaveForWeb 对象的类名。 |
| **webSnap** | `数字` | 可读写。将相近颜色吸附到 Web 调色板颜色的容差量（默认：0）。 |

## File

## Folder

ExtendScript 定义了 JavaScript 类 `File` 和 `Folder`，以与平台无关的方式封装文件系统引用；请参见第 32 页上的 '[Adobe Photoshop CC 2015 中的 JavaScript 支持](javascript:openLink(32))'。有关这些类的详细参考信息，请参阅 *JavaScript 工具指南*。



# GalleryBannerOptions

GalleryOptions 对象的 bannerOptions 属性的选项。

> **提示：** 你可以通过将 GalleryOptions 属性 `preserveAllMetadata` 设置为 true 来保留这些属性中许多的默认值；这与选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 照片画廊对话框的选项区域中选择 **保留所有元数据** 相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `contactInfo` | `string` | 读写。Web 照片画廊的联系信息。 |
| `date` | `string` | 读写。Web 照片画廊的日期（默认：当前日期）。 |
| `font` | [GalleryFontType](GalleryFontType) | 读写。横幅文本的字体设置（默认：GalleryFontType.ARIAL）。 |
| `fontSize` | `number` [1..7] | 读写。横幅文本的字体大小（默认：3）。 |
| `photographer` | `string` | 读写。Web 照片画廊的摄影师。 |
| `siteName` | `string` | 读写。Web 照片画廊的站点名称（默认：Adobe Web Photo Gallery）。 |
| `typename` | `string` | 只读。引用的 `galleryBannerOptions` 对象的类名。 |

# GalleryCustomColorOptions

GalleryOptions 对象的 `customColorOptions` 属性的选项。

**提示：** 你可以通过将 GalleryOptions 属性 `preserveAllMetadata` 设置为 true 来保留这些属性中许多的默认值；这与选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 照片画廊对话框的选项区域中选择 **保留所有元数据** 相同。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `activeLinkColor` | [RGBColor](RGBColor) | 读写。用于指示活动链接的颜色。 |
| `backgroundColor` | [RGBColor](RGBColor) | 读写。背景颜色。 |
| `bannerColor` | [RGBColor](RGBColor) | 读写。横幅颜色。 |
| `linkColor` | [RGBColor](RGBColor) | 读写。用于指示链接的颜色。 |
| `textColor` | [RGBColor](RGBColor) | 读写。文本颜色。 |
| `typename` | string | 只读。引用的 `galleryCustomColorOptions` 对象的类名。 |
| `visitedLinkColor` | [RGBColor](RGBColor) | 读写。用于指示已访问链接的颜色。 |

# GalleryImagesOptions

GalleryOptions 对象的 imagesOptions 属性的选项。

**提示：** 你可以通过将 GalleryOptions 属性 [preserveAllMetadata](preserveAllMetadata) 设置为 true 来保留这些属性中许多的默认值；这与选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 照片画廊对话框的选项区域中选择 **保留所有元数据** 相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **border** | `number [0..99]` | 读写。分隔图像的边框大小（以像素为单位）（默认：0）。 |
| **caption** | `boolean` | 读写。True 以生成图像说明（默认：`false`）。 |
| **dimension** | `number` | 读写。调整大小后的图像尺寸（以像素为单位）（默认：350）。<br><br>仅当 [resizelImages](resizelImages) = `true` 时有效。 |
| **font** | [GalleryFontType](GalleryFontType) | 读写。用于图像说明的字体（默认：`GalleryFontType.ARIAL`）。 |
| **fontSize** | `number [1..7]` | 读写。图像说明的字体大小（默认：3）。<br><br>仅当 [caption](caption) = `true` 时有效。 |
| **imageQuality** | `number [0..12]` | 读写。JPEG 图像的质量设置（默认：5）。 |
| **includeCopyright** | `boolean` | 读写。True 以在说明中包含版权信息（默认：`false`）。<br><br>仅当 [caption](caption) = `true` 时有效。 |
| **includeCredits** | `boolean` | 读写。True 以在图像说明中包含制作人员名单（默认：`false`）。<br><br>仅当 [caption](caption) = `true` 时有效。 |
| **includeFilename** | `boolean` | 读写。True 以在图像说明中包含文件名（默认：`true`）。<br><br>仅当 [caption](caption) = `true` 时有效。 |
| **includeTitle** | `boolean` | 读写。True 以在图像说明中包含标题（默认：`false`）。<br><br>仅当 [caption](caption) = `true` 时有效。 |
| **numericLinks** | `boolean` | 读写。True 以添加数字链接（默认：`true`）。 |
| `resizeConstraint` | `GalleryConstrainType` | 读写。画廊图像中要约束的图像尺寸（默认：`GalleryConstrainType.CONSTRAINBOTH`）。仅当 `resizeImages` = `true` 时有效。 |
| `resizeImages` | `boolean` | 读写。True 以自动调整图像大小以便放置在画廊页面上（默认：`true`）。 |
| `typename` | `string` | 只读。引用的 `galleryImagesOptions` 对象的类名。 |

# GalleryOptions

Web 照片画廊的选项，使用 Application.makePhotoGallery() 创建。

**提示：** 你可以通过选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 照片画廊对话框的选项区域中选择 **保留所有元数据** 来保留这些属性中许多的默认值。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **addSizeAttributes** | boolean | 读写。True 以添加图像的宽度和高度属性（默认：true）。 |
| **bannerOptions** | GalleryBannerOptions | 读写。与横幅设置相关的选项。 |
| **customColorOptions** | GalleryCustomColorOptions | 读写。与自定义颜色设置相关的选项。 |
| **emailAddress** | string | 读写。要在网页上显示的电子邮件地址。 |
| **imagesOptions** | GalleryImagesOptions | 读写。与图像设置相关的选项。 |
| **includeSubFolders** | boolean | 读写。True 以包含在输入文件夹的子文件夹中找到的所有文件（默认：true）。 |
| **layoutStyle** | string | 读写。用于布局网页的样式（默认：Centered Frame 1 - Basic）。 |
| **preserveAllMetadata** | boolean | 读写。True 以保存元数据（默认：false）。 |
| **securityOptions** | GallerySecurityOptions | 读写。与安全设置相关的选项。 |
| **thumbnailOptions** | GalleryThumbnailOptions | 读写。与缩略图图像设置相关的选项。 |
| **typename** | string | 只读。引用的 galleryOptions 对象的类名。 |
| **useShortExtension** | boolean | 读写。True 以使用简短的网页扩展名 .htm。如果为 false，则使用网页扩展名 .html（默认：true）。 |
| **useUTF8Encoding** | boolean | 读写。True 以使用 UTF-8 编码处理网页（默认：false）。 |

# GallerySecurityOptions

GalleryOptions 对象的 securityOptions 属性的选项。

**提示：** 你可以通过将 GalleryOptions 属性 **preserveAllMetadata** 设置为 true 来保留这些属性中许多的默认值；这与选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 照片画廊对话框的选项区域中选择 **保留所有元数据** 相同。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `content` | [GallerySecurityType](GallerySecurityType) | 读写。Web 照片画廊的安全内容（默认：GallerySecurityType.NONE）。 |
| `font` | [GalleryFontType](GalleryFontType) | 读写。Web 照片画廊的安全字体（默认：GalleryFontType.ARIAL）。 |
| `fontSize` | number [1...72] | 读写。Web 照片画廊的安全字体大小（默认：3）。 |
| `opacity` | number | 读写。网页安全的不透明度（百分比）（默认：100）。 |
| `text` | string | 读写。Web 照片画廊的安全自定义文本。 |
| `textColor` | [GallerySecurityTextColorType](GallerySecurityTextColorType) | 读写。网页安全的文本颜色。 |
| `textPosition` | [GallerySecurityTextPositionType](GallerySecurityTextPositionType) | 读写。Web 照片画廊的安全文本位置（默认：GallerySecurityTextPositionType.CENTERED）。 |
| `textRotate` | [GallerySecurityTextRotateType](GallerySecurityTextRotateType) | 读写。要使用的 Web 照片画廊安全文本方向（默认：GallerySecurityTextRotateType.ZERO）。 |
| `typename` | string | 只读。引用的 gallerySecurityOptions 对象的类名。 |



## GalleryThumbnailOptions

[GalleryOptions](https://example.com) 对象的 [thumbnailOptions](https://example.com) 属性的选项。

> **提示：** 通过将 [GalleryOptions](https://example.com) 属性 [preserveAllMetadata](https://example.com) 设置为 true，你可以为许多这些属性保留默认值；这等同于选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 照片画廊对话框的选项区域选择 **保留所有元数据**。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `border` | `number [0..99]` | 读写。你希望围绕缩略图图像的边框像素量（默认值：0）。 |
| `caption` | `boolean` | 读写。true 表示有标题（默认值：false）。 |
| `columnCount` | `number` | 读写。页面上的列数（默认值：5）。 |
| `dimension` | `number` | 读写。Web 照片画廊缩略图的尺寸，以像素为单位（默认值：75）。 |
| `font` | [GalleryFontType](https://example.com) | 读写。Web 照片画廊的字体（默认值：GalleryFontType.ARIAL）。 |
| `fontSize` | `number [1..7]` | 读写。缩略图图像文本的字体大小（默认值：3）。 |
| `includeCopyright` | `boolean` | 读写。true 表示包含缩略图的版权信息（默认值：false）。 |
| `includeCredits` | `boolean` | 读写。true 表示包含缩略图的致谢信息（默认值：false）。 |
| `includeFilename` | `boolean` | 读写。true 表示包含缩略图的文件名（默认值：false）。 |
| `includeTitle` | `boolean` | 读写。true 表示包含缩略图的标题（默认值：false）。 |
| `rowCount` | `number` | 读写。页面上的行数（默认值：3）。 |
| `size` | [GalleryThumbSizeType](https://example.com) | 读写。缩略图图像的大小（默认值：GalleryThumbSizeType.MEDIUM）。 |
| `typename` | `string` | 只读。引用的 GalleryThumbnailOptions 对象的类名。 |

## GIFSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 GIF 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `colors` | `number` | 读写。调色板颜色数。仅当 `palette` = Palette.LOCALADAPTIVE、LOCALPERCEPTUAL、LOCALSELECTIVE、MACOSPALETTE、UNIFORM、WEBPALETTE 或 WINDOWSPALETTE 时有效。 |
| `dither` | [Dither](https://example.com) | 读写。仿色类型。 |
| `ditherAmount` | `number` [1..100] | 读写。仿色量（默认值：75）。仅当 `dither` = Dither.DIFFUSION 时有效。 |
| `forced` | [ForcedColors](https://example.com) | 读写。要强制加入调色板的颜色类型。 |
| `interlaced` | `boolean` | 读写。true 表示行应交错（默认值：`false`）。 |
| `matte` | [MatteType](https://example.com) | 读写。用于填充图像透明区域相邻的抗锯齿边缘的颜色（默认值：`MatteType.WHITE`）。当 `transparency` = `false` 时，哑光颜色应用于透明区域。 |
| `palette` | [PaletteType](https://example.com) | 读写。要使用的调色板类型（默认值：`Palette.LOCALSELECTIVE`）。 |
| `preserveExactColors` | `boolean` | 读写。true 表示保护图像中在颜色表中有条目的颜色不被仿色。仅当 `dither` = Dither.DIFFUSION 时有效。 |
| `transparency` | `boolean` | 读写。true 表示在转换为 GIF 格式期间保留图像的透明区域。 |
| `typename` | `string` | 只读。引用的 `GIFSaveOptions` 对象的类名。 |

## GrayColor

定义一种灰色，用于 [SolidColor](SolidColor) 对象。

另请参阅 [CMYKColor](CMYKColor)、[HSBColor](HSBColor)、[LabColor](LabColor)、[NoColor](NoColor)、[RGBColor](RGBColor)

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `gray` | `number [0.0..100.0]` | 读写。灰度值（默认值：0.0）。 |
| `typename` | `string` | 只读。引用的 `grayColor` 对象的类名。 |

## Guide

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **direction** | [Direction](https://example.com) | 读写。指示参考线是垂直还是水平。 |
| **coordinate** | [UnitValue](https://example.com) | 读写。参考线距离图像原点的位置。 |

## Guides

打开的 Guide 对象的集合。

通过 Document.guides 集合属性访问此列表，该属性可通过 activeDocument 对象使用。例如，以下代码向集合中添加新的参考线：

```
activeDocument.guides.add (Direction.HORIZONTAL,UnitValue(20,20))
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。guides 集合中的元素数量。 |
| parent | Document | 只读。包含的文档。 |
| typename | string | 只读。引用的 guides 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| add (direction, coordinate) | Direction UnitValue | Guide | 创建一个新的参考线对象并将其添加到此集合。 |
| getByName (name) | string | Guide | 获取 guides 集合中第一个具有所提供名称的元素。 |

## HistoryState

文档的一个自动存储的版本（并添加到 [HistoryStates](https://helpx.adobe.com/photoshop/using/history-states.html) 集合中），每次文档更改时都会保留文档的状态。

通过 [Document.historyStates](https://helpx.adobe.com/photoshop/using/history-states.html) 集合访问。你可以通过名称访问列表中的状态。例如，以下代码在名为“AddLayerMask”的状态对象中分配一个属性值：

```
var stateRef = app.activeDocument.historyState.getByName("AddLayerMask");
stateRef.snapshot = true;
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **name** | `string` | 只读。`HistoryState` 对象的名称。 |
| **parent** | [Document](https://helpx.adobe.com/photoshop/using/scripting.html) | 只读。包含的文档。 |
| **snapshot** | `boolean` | 只读。true 表示历史记录状态是快照。 |
| **typename** | `string` | 只读。引用的 `HistoryState` 对象的类名。 |

## HistoryStates

文档中 [HistoryState](HistoryState) 对象的集合。

通过 [Document.historyStates](Document.historyStates) 集合属性访问。例如，以下代码通过索引访问集合中的一个状态：

```
myState = app.activeDocument.historyStates[7];
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| length | number | 只读。HistoryStates 集合中的元素数量。 |
| parent | [Document](Document) | 只读。包含的文档。 |
| typename | string | 只读。引用的 HistoryStates 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| getByName(name) | string | [HistoryState](HistoryState) | 获取 HistoryStates 集合中第一个具有所提供名称的元素。 |

## HSBColor

定义一种 HSB 颜色，用于 [SolidColor](object) 对象。

另请参阅 [CMYKColor](CMYKColor)、[GrayColor](GrayColor)、[LabColor](LabColor)、[NoColor](NoColor)、[RGBColor](RGBColor)

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **brightness** | `number [0.0...100.0]` | 读写。亮度值。 |
| **hue** | `number [0.0...360.0]` | 读写。色调值。 |
| **saturation** | `number [0.0...100.0]` | 读写。饱和度值。 |
| **typename** | `string` | 只读。引用的 `HSBColor` 对象的类名。 |

## IndexedConversionOptions

使用 [Document.changeMode()](Document.changeMode) 将 RGB 图像转换为索引颜色模型的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `colors` | number | 读写。调色板颜色数。<br><br>仅当 [palette](palette) = Palette.LOCALADAPTIVE、LOCALPERCEPTUAL、LOCALSELECTIVE、MACOSPALETTE、UNIFORM、WEBPALETTE 或 WINDOWSPALETTE 时有效。 |
| `dither` | [Dither](Dither) | 读写。仿色类型。 |
| `ditherAmount` | number [1..100] | 读写。仿色量。<br><br>仅当 [dither](dither) = Dither.DIFFUSION 时有效。 |
| `forced` | [ForcedColors](ForcedColors) | 读写。要强制加入调色板的颜色类型。 |
| `matte` | [MatteType](MatteType) | 读写。用于填充图像透明区域相邻的抗锯齿边缘的颜色（默认值：MatteType.WHITE）。<br><br>当 [transparency](transparency) = false 时，哑光颜色应用于透明区域。 |
| `palette` | [PaletteType](PaletteType) | 读写。调色板类型（默认值：Palette.EXACT）。 |
| `preserveExactColors` | boolean | 读写。true 表示保护图像中在颜色表中有条目的颜色不被仿色。<br><br>仅当 [dither](dither) = Dither.DIFFUSION 时有效。 |
| `transparency` | boolean | 读写。true 表示在转换为 GIF 格式期间保留图像的透明区域。 |
| `typename` | string | 只读。引用的 IndexedConversionOptions 对象的类名。 |



## JPEGSaveOptions

使用 [Document.saveAs()](javascript:void(0)) 方法将文档保存为 JPEG 格式时的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `embedColorProfile` | boolean | 可读写。设为 true 以在文档中嵌入颜色配置文件。 |
| `formatOptions` | [FormatOptions](javascript:void(0)) | 可读写。要使用的下载格式（默认值：FormatOptions.STANDARDBASELINE）。 |
| `matte` | [MatteType](javascript:void(0)) | 可读写。用于填充图像透明区域边缘抗锯齿效果的颜色（默认值：MatteType.WHITE）。当图像的透明度关闭时，哑光颜色会应用于透明区域。 |
| `quality` | number [0..12] | 可读写。要使用的图像质量设置；影响文件大小和压缩率（默认值：3）。 |
| `scans` | number [3..5] | 可读写。在页面上增量显示图像所需的扫描次数（默认值：3）。仅当 `formatOptions` = FormatOptions.PROGRESSIVE 时有效。 |
| `typename` | string | 只读。引用的 JPEGSaveOptions 对象的类名。 |

## LabColor

定义了一种 LAB 颜色，用于 [SolidColor](solidcolor) 对象。

另请参阅 [CMYKColor](cmkycolor)、[GrayColor](graycolor)、[HSBColor](hsbcolor)、[NoColor](nocolor)、[RGBColor](rgbcolor)

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| a | number [-128.0..127.0] | 可读写。a 值。 |
| b | number [-128.0..127.0] | 可读写。b 值。 |
| l | number [0.0..100.0] | 可读写。L 值。 |
| typename | string | 只读。引用的 `LabColor` 对象的类名。 |

## LayerComp

文档中图层状态的快照，可用于查看不同的页面布局或组合。

通过 [Document.layerComps](https://www.adobe.com/devnet/photoshop/scripting.html) 集合访问。你可以通过名称访问一个图层组合。例如，以下代码为名为 `myLayerComp` 的 `LayerComp` 对象设置 `comment` 属性值：

```
var layercompRef = app.activeDocument.layerComps.getByName("myLayerComp");
layercompRef.comment = "View from shoreline";
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| **appearance** | boolean | 可读写。设为 true 以使用图层外观（图层样式）设置。 |
| **comment** | string | 可读写。图层组合的描述。 |
| **name** | string | 可读写。图层组合的名称。 |
| **parent** | [Document](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。所属文档。 |
| **position** | boolean | 可读写。设为 true 以使用图层位置。 |
| **selected** | boolean | 只读。如果图层组合当前被选中，则为 true。 |
| **typename** | string | 只读。引用的 `layerComp` 对象的类名。 |
| **visibility** | boolean | 可读写。设为 true 以使用图层可见性设置。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| **apply**() | | | 将图层组合应用于文档。 |
| **recapture**() | | | 为此图层组合重新捕获当前的图层状态。 |
| **remove**() | | | 删除 `layerComp` 对象。 |
| **resetfromComp**() | | | 将图层组合状态重置为文档状态。 |

## LayerComps

文档中 [LayerComp](LayerComp) 对象的集合。

通过 [Document.layerComps](Document) 集合属性访问。例如：

```
app.activeDocument.layerComps.add("myLayerComp", "View from Shoreline",
    true, true, true);
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **length** | `number` | 只读。`layerComps` 集合中的元素数量。 |
| **parent** | [Document](Document) | 只读。所属文档。 |
| **typename** | `string` | 只读。引用的 `layerComps` **对象**的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| **add** (name, comment, appearance, position, visibility) | `string` `string` `boolean` `boolean` `boolean` | [LayerComp](LayerComp) | 创建一个新的图层组合对象并将其添加到此集合中。 |
| **getByName** (name) | `string` | [LayerComp](LayerComp) | 获取集合中具有提供名称的第一个元素。 |
| **removeAll** () | | | 从 `layerComps` 集合中移除所有成员对象。 |

## Layers

文档中的图层对象集合，包括 `ArtLayer` 和 `LayerSet` 对象。通过 `Document.layers` 或 `LayerSet.layers` 集合属性访问。

例如，此代码使用 `length` 属性统计活动文档中的 `layer` 对象数量，然后在屏幕上显示该数字：

```
var layerNum = app.activeDocument.layers.length
alert(layerNum)
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `length` | number | 只读。`layers` 集合中的元素数量。 |
| `parent` | `Document` 或 `LayerSet` | 只读。所属文档或图层集。 |
| `typename` | string | 只读。引用的 `layers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `getByName` (name) | string | `Layer` | 获取 `layers` 集合中具有提供名称的第一个元素。 |
| `removeAll` () | | | 从集合中移除所有图层。 |

## LayerSet

一组图层对象，可以包括 [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/artlayer/) 对象和其他（嵌套的）LayerSet 对象。单个命令可以操作该组中的所有图层。

通过 [Document.layerSets](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/document/#layersets) 集合访问文档中的顶级图层集。你可以按名称访问图层集。例如，以下代码设置名为 "myLayerSet" 的 `allLocked` 值：

```
var layerSetRef = app.activeDocument.layerSets.getByName("myLayerSet");
layerSetRef.allLocked = true
```

通过父级图层集中的 [LayerSet.layerSets](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layerSet/#layersets) 集合访问嵌套的图层集。例如：

```
app.activeDocument.layerSets[0].layerSets[0];
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **allLocked** | boolean | 可读写。如果此图层集中的图层内容不可编辑，则为 true。 |
| **artLayers** | [ArtLayers](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/artlayers/) | 只读。此图层集中的艺术图层。 |
| **blendMode** | [BlendMode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/blendmode/) | 可读写。图层集使用的混合模式。 |
| **bounds** | [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/unitvalue/) 数组 | 只读。图层集的边界矩形。 |
| **enabledChannels** | [Channel](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/channel/) 数组 | 可读写。为图层集启用的通道；必须是组件通道的列表。请参阅 [Channel.kind](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/channel/#kind)。 |
| **layers** | [Layers](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layers/) | 只读。此图层集中的图层。 |
| **layerSets** | [LayerSets](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layersets/) | 只读。包含在此图层集中的嵌套图层集。 |
| **linkedLayers** | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/artlayer/) 和/或 [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layerSet/) 数组 | 只读。链接到此 `layerSet` 对象的图层。 |
| **name** | string | 可读写。此图层集的名称。 |
| **opacity** | number [0.0..100.0] | 可读写。图层集的主不透明度。 |
| **parent** | [Document](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/document/) 或 [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layerSet/) | 只读。所属文档或图层集。 |
| **typename** | string | 只读。引用的 LayerSet 对象的类名。 |
| **visible** | boolean | 可读写。如果图层集可见，则为 true。 |



## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| --- | --- | --- | --- |
| **duplicate**<br>([relativeObject]<br>[, insertionLocation]) | ArtLayer 或 LayerSet<br>ElementPlacement | LayerSet | 创建对象的副本。 |
| **link**<br>(with) | ArtLayer 或 LayerSet | | 将图层集与另一个图层链接。 |
| **merge**<br>() | | ArtLayer | 合并图层集；返回通过此方法创建的图层的引用。 |
| **move**<br>(relativeObject,<br>insertionLocation) | ArtLayer 或 LayerSet<br>ElementPlacement | | 移动对象。 |
| **remove**<br>() | | | 删除对象。 |
| **resize**<br>([horizontal]<br>[, vertical]<br>[, anchor]) | number<br>number<br>AnchorPosition | | 将图层集中的所有图层调整为指定的尺寸（作为当前尺寸的百分比），并将图层集放置在指定位置。 |
| **rotate**<br>(angle<br>[, anchor]) | number<br>AnchorPosition | | 围绕指定的锚点旋转图层集中的所有图层（默认值：AnchorPosition.MIDDLECENTER）。 |
| **translate**<br>([deltaX]<br>[, deltaY]) | UnitValue<br>UnitValue | | 相对于当前位置移动位置。 |
| **unlink**<br>() | | | 取消图层集的链接。 |

# LayerSets

文档中的 LayerSet 对象集合。

通过 Document.layerSets 集合属性访问文档中的顶级图层集。例如：

```
var layerSetRef = app.activeDocument.layerSets.add()
```

通过父级集中的 LayerSet.layerSets 集合属性访问嵌套图层集。例如：

```
var layerSetRef = app.activeDocument.layerSets.getByName("myParentSet");
var childSet = layerSetRef.layerSets.getByName("myChildSet");
```

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| length | number | 只读。LayerSets 集合中的元素数量。 |
| parent | Document 或 LayerSet | 只读。包含的文档或图层集。 |
| typename | string | 只读。引用的 layerSets 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| --- | --- | --- | --- |
| add() | | LayerSet | 创建新的图层集对象并将其添加到集合中。 |
| getByName(name) | string | LayerSet | 获取集合中第一个具有所提供名称的元素。 |
| removeAll() | | | 从文档中移除所有成员图层集及其包含的任何图层或图层集。 |

### LayerSets 示例脚本

以下脚本创建三个图层集，然后在每个图层集中嵌套第二个图层集，接着在每个嵌套集中创建一个文本图层，显示文本“Layer in *n* Set Inside *n* Set”，其中 *n* 代表集合的序号（第一、第二或第三）。

**注意：** 此脚本使用 ExtendScript $ 调试对象。有关更多详细信息，请参阅 *JavaScript 工具指南*。

```
LayerSets.jsx
$.level = 1

//close all open documents
while (app.documents.length) {
    app.activeDocument.close()
}

// create a working document
var docRef = app.documents.add()

// create an array to hold the layer sets
var myLayerSets = new Array()

// Create an array to hold the text
var textArray = Array("First", "Second", "Third")

//Create an indexer variable
var i = 0

// Create three layer sets at the top level
for (i = 0; i < 3; i++) {
    myLayerSets[i] = new Array()
    myLayerSets[i][0] = docRef.layerSets.add()
}

// Rearrange the layer sets with the first one on top, second next, etc.
myLayerSets[1][0].moveAfter(myLayerSets[0][0])
myLayerSets[2][0].moveAfter(myLayerSets[1][0])

// Create a layer set inside each layer set
for (i = 0; i < 3; i++) {
    myLayerSets[i][0].name = textArray[i] + " Set"
    myLayerSets[i][1] = myLayerSets[i][0].layerSets.add()
    myLayerSets[i][1].name = "Inside " + textArray[i] + " Set"
}

// Create an array to hold the layers
var myLayers = new Array()

// Create a text layer with a description inside each layer set
for (i = 0; i < 3; i++) {
    myLayers[i] = myLayerSets[i][1].artLayers.add()
    myLayers[i].kind = LayerKind.TEXT
    myLayers[i].textItem.contents = "Layer in " + textArray[i] + " Set Inside "
            + textArray[i] + " Set"
    myLayers[i].textItem.position = Array(app.activeDocument.width * i * 0.33,
            app.activeDocument.height * (i + 1) * 0.25)
    myLayers[i].textItem.size = 12
}
```

# MeasurementLog

应用程序的测量日志。通过 Application.measurementLog 属性访问。

**注意：** 此功能仅在扩展版中可用。

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
|---|---|---|---|
| exportMeasurements<br>([file]<br>[, range]<br>[, dataPoints]) | File<br>MeasurementRange<br>string 数组 |  | 将测量结果导出到文件。 |
| deleteMeasurements<br>([range]) | MeasurementRange |  | 从日志中删除测量记录。 |

# MeasurementScale

文档的测量比例。通过 Document.measurementScale 属性访问。例如：

```
app.activeDocument.measurementScale.pixelLength = 25
```

**注意：** 此功能仅在扩展版中可用。

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| pixelLength | number | 读写。此比例等效的像素长度。 |
| logicalLength | number | 读写。此比例等效的逻辑长度。 |
| logicalUnits | string | 读写。此比例的逻辑单位。 |

# NoColor

表示缺失的颜色对象，用于 SolidColor 对象。

另请参阅 CMYKColor、GrayColor、HSBColor、LabColor、RGBColor。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| typename | string | 只读。引用的 noColor 对象的类名。 |

# Notifier

事件处理程序对象，用于告知脚本在特定事件发生时执行指定的代码。必须使用 Application.notifiersEnabled 属性启用通知器。

通过 Application.notifiers 集合访问。

注意：脚本内发生的事件通常不会触发通知器，因为它们发生在“播放脚本”事件内部。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| event | string | 只读。事件标识符，一个四字符代码或唯一字符串。有关四字符代码列表，请参阅附录 A：事件 ID 代码。 |
| eventClass | string | 只读。类标识符，一个四字符代码或唯一字符串。当一个事件适用于多种类型的对象时，使用此属性来区分此通知器适用于哪个对象。例如，创建事件（"Mk  "）可适用于文档（"Dcmn"）、通道（"Chnl"）和其他对象。 |
| eventFile | File | 只读。当事件发生并激活通知器时要执行的文件路径。 |
| parent | Application | 只读。包含的应用程序。 |
| typename | string | 只读。引用对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| remove() | | | 删除此对象。您也可以通过从 Photoshop 首选项文件夹中删除名为“Script Events Manager.xml”的文件，从脚本事件管理器下拉列表中移除 Notifier 对象。有关更多信息，请参阅 Adobe Photoshop CC 2015 帮助。 |



## 通知器

文档中的 [Notifier](https://helpx.adobe.com/photoshop/using/notifier.html) 对象集合。通过 [Application.notifiers](https://helpx.adobe.com/photoshop/using/notifier.html) 集合属性访问。例如：

`var notRef = app.notifiers.add("OnClickGoButton", eventFile)`

必须使用 [Application.notifiersEnabled](https://helpx.adobe.com/photoshop/using/notifier.html) 属性启用通知器。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `length` | `number` | 只读。`notifiers` 集合中的元素数量。 |
| `parent` | [Application](https://helpx.adobe.com/photoshop/using/notifier.html) | 只读。`notifiers` 对象的容器。 |
| `typename` | `string` | 只读。引用的 `notifiers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| --- | --- | --- | --- |
| `add (event, eventFile [, eventClass])` | `string` [File](https://helpx.adobe.com/photoshop/using/notifier.html) `string` | [Notifier](https://helpx.adobe.com/photoshop/using/notifier.html) | 创建一个通知器对象并将其添加到此集合中。`event` 定义事件的类ID：使用一个4字符代码或唯一字符串。参见[附录A：事件ID代码](https://helpx.adobe.com/photoshop/using/notifier.html)。`eventFile` 定义事件发生时执行的脚本文件。当一个事件适用于多种类型的对象时，使用 `eventClass`（一个4字符ID或唯一字符串）来区分此通知器适用于哪个对象。例如，Make事件（"Mk "）适用于文档（"Dcmn"）、通道（"Chnl"）和其他对象。**提示：** 在代码中使用4字符ID代码指定事件或事件类时，请省略单引号。 |
| `removeAll ()` | | | 从 `notifiers` 集合中移除所有成员对象。您也可以通过从Photoshop首选项文件夹中删除名为 `Script Events Manager.xml` 的文件，从脚本事件管理器下拉列表中移除一个 `notifier` 对象。有关更多信息，请参阅 Adobe Photoshop CC 2015 帮助。 |

## 路径项

一个路径或绘图对象，例如形状的轮廓或直线或曲线，它包含定义其几何形状的子路径。

通过 [Document.pathItems](#) 属性中的集合访问。例如，此代码选择一个命名的路径项：

```
var currentPathItem = app.activeDocument.pathItems.getByName("myPath");
currentPathItem.select()
```

通过向 [PathItems.add()](#) 方法传递一组 [SubPathInfo](#) 对象来创建这些对象。此方法为每个 [SubPathInfo](#) 对象创建一个 [SubPathItem](#) 对象，并为所有子路径所表示的路径创建并返回一个新的 [PathItem](#) 对象。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| **kind** | [PathKind](#) | 可读写。类型。 |
| **name** | string | 可读写。名称。 |
| **parent** | [Document](#) | 只读。包含的文档。 |
| **subPathItems** | [SubPathItems](#) | 只读。包含的子路径对象。 |
| **typename** | string | 只读。引用的 `pathItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| --- | --- | --- | --- |
| **deselect** () | | | 取消选择此 `pathItem` 对象。 |
| **duplicate** (name) | string | | 使用新名称复制此 `pathItem` 对象。 |
| **fillPath** ([fillColor] [, mode] [, opacity] [, preserveTransparency] [, feather] [, wholePath] [, antiAlias]) | [SolidColor](#) [ColorBlendMode](#) number [0..100] boolean number [0.0..250.0] boolean boolean | | 填充此路径所包围的区域。`opacity` 是一个百分比值。`feather` 单位为像素。如果 `wholePath` 为 true，则在填充时使用所有子路径（默认值：true）。 |
| **makeClippingPath** ([flatness]) | number [0.2..100] | | 将此路径设为此文档的剪贴路径。`flatness` 告诉 PostScript 打印机如何近似路径中的曲线。 |
| **makeSelection** ([feather] [, antiAlias] [, operation]) | number [0.0..250.0] boolean SelectionType | | 创建一个边框为路径的选区对象。`feather` 单位为像素。 |
| **remove** () | | | 删除此对象。 |
| **select** () | | | 使此对象成为活动或选中的路径项对象。 |
| **strokePath** ([tool] [, simulatePressure]) | ToolType boolean | | 使用指定工具描边路径。 |

### PathItem 示例脚本

以下脚本创建一个包含三段的路径：两条形成 V 形的对角线，以及 V 形上方的一条曲线，使其看起来像一个二维冰淇淋蛋筒。

### Paths.jsx

```
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

// first close all the open documents
while (app.documents.length) {
    app.activeDocument.close()
}

// create a document to work with
var docRef = app.documents.add(5000, 7000, 72, "Simple Line")

//line 1--it's a straight line so the coordinates for anchor, left, and right
//for each point have the same coordinates
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

// line 2
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

//ice cream curve
//it's a curved line, so there are 3 points, not 2
//coordinates for the middle point (lineArray3[1]) are different.
//The left direction is positioned "above" the anchor on the screen.
//The right direction is positioned "below" the anchor
//You can change the coordinates for these points to see
//how the curve works...
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

lineSubPathArray[2] = new SubPathInfo()
lineSubPathArray[2].operation = ShapeOperation.SHAPEXOR
lineSubPathArray[2].closed = false
lineSubPathArray[2].entireSubPath = lineArray3

//create the path item
var myPathItem = docRef.pathItems.add("A Line", lineSubPathArray)

// stroke it so we can see something
myPathItem.strokePath(ToolType.BRUSH)

// Reset the application preferences
preferences.rulerUnits = startRulerUnits
preferences.typeUnits = startTypeUnits
displayDialogs = startDisplayDialogs
```



## PathItems

文档中 [PathItem](PathItem) 对象的集合。
通过 [Document.pathItems](Document.pathItems) 集合属性访问。例如，以下代码使用先前定义的子路径集创建一个新的路径项：

```
app.activeDocument.pathItems.add("myPath", lineSubPathInfoArray);
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。`pathItems` 集合中的 `pathItem` 对象数量。 |
| parent | Document | 只读。`pathItems` 对象的容器。 |
| typename | string | 只读。引用的 `pathItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| add (name, entirePath) | string, array of [SubPathInfo](SubPathInfo) | [PathItem](PathItem) | 创建一个新的路径项对象并将其添加到此集合。为 `entirePath` 中提供的每个 `SubPathInfo` 对象创建一个新的 [SubPathItem](SubPathItem) 对象，并将这些 `SubPathItem` 对象添加到返回的 `PathItem` 的 `subPathItems` 集合中。 |
| getByName (name) | string | [PathItem](PathItem) | 获取 `pathItems` 集合中具有所提供名称的第一个元素。 |
| removeAll () | | | 从 `pathItems` 集合中移除所有 `pathItem` 对象。 |

## PathPoint

表示路径段的锚点和控制柄端点。每个点（锚点、左方向点和右方向点）是一个包含 X 和 Y 位置坐标的数组。

- 使用 `PathPoint` 对象检索有关描述现有路径段的点的信息。属性为只读。通过 `SubPathItem.pathPoints` 属性访问 `PathPoint` 对象。
- 使用 `PathPointInfo` 配合 `PathItems.add()` 创建路径点。属性为可写。

对于直线路段（非曲线），所有三个点的坐标相同。对于曲线段，坐标不同。锚点与左或右方向点之间的差异决定了曲线的弧度。你使用左方向点使曲线“向外”弯曲或使其凸出；你使用右方向点使曲线“向内”弯曲或使其凹陷。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| anchor | `array of number` | 只读。曲线锚点的 X 和 Y 坐标。 |
| kind | `PointKind` | 只读。此点在包含路径段中扮演的角色（角点或平滑点）。 |
| leftDirection | `array of number` | 只读。左方向端点（“入”位置）的位置。 |
| parent | `SubPathItem` | 只读。包含的子路径对象。 |
| rightDirection | `array of number` | 只读。右方向端点（“出”位置）的位置。 |
| typename | `string` | 只读。引用的 `PathPoint` 对象的类名。 |

## PathPointInfo

用于创建 PathPoint，表示路径段的锚点和控制柄端点。每个点（锚点、左方向点和右方向点）是一个包含 X 和 Y 位置坐标的数组。

- 使用 JavaScript new 运算符创建这些对象，并在使用该对象通过 PathItems.add() 创建路径项之前，将它们存储在 SubPathInfo.entireSubPath 属性中。

  请参阅下面的 PathPointInfo 示例脚本。
- 生成的 SubPathItem 对象包含生成的 PathPoint 对象。使用 PathPoint 对象检索有关描述现有路径段的点的信息。属性为只读。

对于直线路段（非曲线），所有三个点的坐标相同。对于曲线段，坐标不同。锚点与左或右方向点之间的差异决定了曲线的弧度。你使用左方向点使曲线“向外”弯曲或使其凸出；你使用右方向点使曲线“向内”弯曲或使其凹陷。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **anchor** | array of number | 读写。曲线锚点的 X 和 Y 坐标。 |
| **kind** | PointKind | 读写。此点在包含路径段中扮演的角色（角点或平滑点）。 |
| **leftDirection** | array of number | 读写。左方向端点（“入”位置）的位置。 |
| **rightDirection** | array of number | 读写。右方向端点（“出”位置）的位置。 |
| **typename** | string | 只读。引用的 PathPointInfo 对象的类名。 |

### PathPointInfo 示例脚本

```
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

    var spi = new SubPathInfo();
    spi.closed = false;
    spi.operation = ShapeOperation.SHAPEXOR;
    spi.entireSubPath = [startPoint, stopPoint];

    var line = doc.pathItems.add("Line", [spi]);
    line.strokePath(ToolType.PENCIL);
    line.remove();
};

drawLine(app.activeDocument, [100,100], [200,200]);
```

## PathPoints

定义子路径的 [PathPoint](https://example.com/PathPoint) 对象集合，保存在 [SubPathItem.pathPoints](https://example.com/SubPathItem.pathPoints) 属性中。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **length** | `number` | 只读。集合中的元素数量。 |
| **parent** | [SubPathItem](https://example.com/SubPathItem) | 只读。包含的子路径对象。 |
| **typename** | `string` | 只读。引用的 PathPoints 对象的类名。 |

## PDFOpenOptions

使用 [Application.open()](https://helpx.adobe.com/photoshop/using/application-object.html) 方法打开通用 Adobe PDF 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `antiAlias` | boolean | 读写。设为 true 以使用抗锯齿。 |
| `bitsPerChannel` | [BitsPerChannelType](https://helpx.adobe.com/photoshop/using/scripting-constants.html) | 读写。每通道的位数。 |
| `constrainProportions` | boolean | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `cropPage` | [CropToType](https://helpx.adobe.com/photoshop/using/scripting-constants.html) | 读写。要使用的裁剪方法。 |
| `height` | [UnitValue](https://helpx.adobe.com/photoshop/using/unit-value-object.html) | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `mode` | [OpenDocumentMode](https://helpx.adobe.com/photoshop/using/scripting-constants.html) | 读写。要使用的颜色模型。 |
| `name` | string | 读写。对象的名称。 |
| `object` | number | 读写。要打开的 3d 对象数量。 |
| `page` | number | 读写。要打开文档的页面或图像，具体取决于 `usePageNumber` 的值。 |
| `resolution` | number | 读写。文档的分辨率（每英寸像素数）。 |
| `suppressWarnings` | boolean | 读写。设为 true 以在打开文档时抑制警告。 |
| `typename` | string | 只读。引用的 `PDFOpenOptions` 对象的类名。 |
| `use3DObjectNumber` | boolean | 读写。如果为 true，则 3d 属性指使用 3d 对象；如果为 false，则使用 `usePageNumber`。 |
| `usePageNumber` | boolean | 读写。当为 true 时，`page` 属性指页码；当为 false 时，指图像编号。 |
| `width` | [UnitValue](https://helpx.adobe.com/photoshop/using/unit-value-object.html) | 在 Adobe Photoshop CC 2015 中已弃用。 |



## PDFSaveOptions

使用 [Document.saveAs()](https://example.com) 方法将文档保存为 Adobe PDF 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为真表示将 Alpha 通道与文件一起保存。 |
| `annotations` | 布尔值 | 读写。为真表示将注释与文件一起保存。 |
| `colorConversion` | 布尔值 | 读写。为真表示将颜色配置文件转换为目标配置文件。 |
| `convertToEightBit` | 布尔值 | 读写。为真表示将 16 位图像转换为 8 位，以更好地兼容其他应用程序。 |
| `description` | 字符串 | 读写。要使用的保存选项的描述。 |
| `destinationProfile` | 字符串 | 读写。最终 RGB 或 CMYK 输出设备的描述，例如显示器或印刷标准。 |
| `downgradeColorProfile` | 布尔值 | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `downSample` | PDFResample | 读写。要使用的降采样方法。 |
| `downSampleSize` | 数字 | 读写。当图像超过每英寸像素数限制时，对其进行降采样的尺寸。 |
| `downSampleSizeLimit` | 数字 | 读写。将降采样或子采样限制为超过每英寸此像素值的图像。 |
| `embedColorProfile` | 布尔值 | 读写。为真表示将颜色配置文件嵌入文档。 |
| `embedFonts` | 布尔值 | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `embedThumbnail` | 布尔值 | 读写。为真表示在 Adobe PDF 文件中包含一个小型预览图像。 |
| `encoding` | PDFEncoding | 读写。要使用的压缩类型（默认：`PDFEncoding.PDFZIP`）。 |
| `interpolation` | 布尔值 | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `jpegQuality` | `number` [0..12] | 读写。生成图像的质量，与压缩量成反比。 <br><br>仅当 `encoding` = PDFEncoding.JPEG 时有效。 |
| `layers` | 布尔值 | 读写。为真表示保存文档的图层。 |
| `optimizeForWeb` | 布尔值 | 读写。为真表示提高 PDF 文件在 Web 服务器上的性能。 |
| `outputCondition` | 字符串 | 读写。一个可选的注释字段，用于插入输出条件的描述。文本存储在 PDF/X 文件中。 |
| `outputConditionID` | 字符串 | 读写。输出条件的标识符。 |
| `PDFCompatibility` | [PDFCompatibility](https://www.adobe.com/devnet-apps/photoshop/cs5/html/ref/#/Properties/PDFSaveOptions/PDFCompatibility) | 读写。要使文档兼容的 PDF 版本。 |
| `PDFStandard` | [PDFStandard](https://www.adobe.com/devnet-apps/photoshop/cs5/html/ref/#/Properties/PDFSaveOptions/PDFStandard) | 读写。要使文档兼容的 PDF 标准。 |
| `preserveEditing` | 布尔值 | 读写。为真表示在 Adobe Photoshop CC 2015 中重新打开 PDF 时，原生 Photoshop 数据保持完整。 |
| `presetFile` | 字符串 | 读写。用于设置的预设文件。 <br><br>**注意：** 此选项会覆盖其他设置。 |
| `profileInclusionPolicy` | 布尔值 | 读写。为真表示显示要包含的配置文件。 |
| `registryName` | 字符串 | 读写。注册输出条件的 URL。 |
| `spotColors` | 布尔值 | 读写。为真表示保存专色。 |
| `tileSize` | 数字 | 读写。压缩选项。 <br><br>仅当 `encoding` = PDFEncoding.JPEG2000 时有效。 |
| `transparency` | 布尔值 | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `typename` | 字符串 | 只读。引用的 `PDFSaveOptions` 对象的类名。 |
| `useOutlines` | 布尔值 | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `vectorData` | `boolean` | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `view` | `boolean` | 读写。为真表示在 Adobe Acrobat 中打开保存的 PDF。 |

## PhotoCDOpenOptions

在 Adobe Photoshop CC 2015 中已弃用。柯达 PhotoCD 现位于 Adobe Photoshop CC 2015 安装 DVD 的 Goodies 文件夹中。

使用 Application.open() 方法打开柯达照片 CD (PCD) 格式文档（包括来自 Pro Photo CD 光盘的高分辨率文件）的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `colorProfileName` | 字符串 | 读写。读取图像时要使用的配置文件。 |
| `colorSpace` | PhotoCDColorSpace | 读写。图像的色彩空间。 |
| `orientation` | Orientation | 读写。图像方向。 |
| `pixelSize` | PhotoCDSize | 读写。图像尺寸。 |
| `resolution` | 数字 | 读写。图像分辨率（每英寸像素数）。 |
| `typename` | 字符串 | 只读。引用的 photoCDOpenOptions 对象的类名。 |

## PhotoshopSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 PSD 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为真表示保存 Alpha 通道。 |
| `annotations` | 布尔值 | 读写。为真表示保存注释。 |
| `embedColorProfile` | 布尔值 | 读写。为真表示将颜色配置文件嵌入文档。 |
| `layers` | 布尔值 | 读写。为真表示保留图层。 |
| `spotColors` | 布尔值 | 读写。为真表示保存专色。 |
| `typename` | 字符串 | 只读。引用的 `photoshopSaveOptions` 对象的类名。 |

## PICTFileSaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法将文档保存为 PICT 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为真表示保存 Alpha 通道。 |
| `compression` | [PICTCompression](PICTCompression) | 读写。要使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | 布尔值 | 读写。为真表示将颜色配置文件嵌入文档。 |
| `resolution` | [PICTBitsPerPixel](PICTBitsPerPixel) | 读写。每像素位数。 |
| `typename` | 字符串 | 只读。引用的 `PICTFileSaveOptions` 对象的类名。 |

## PICTResourceSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法将文档保存为 PICT 资源文件的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为真表示保存 Alpha 通道。 |
| `compression` | [PICTCompression](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。要使用的压缩类型（默认：PICTCompression.NONE）。 |
| `embedColorProfile` | 布尔值 | 读写。为真表示将颜色配置文件嵌入文档。 |
| `name` | 字符串 | 读写。PICT 资源的名称。 |
| `resolution` | [PICTBitsPerPixel](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。每像素位数。 |
| `resourceID` | 数字 | 读写。PICT 资源的 ID（默认：128）。 |
| `typename` | 字符串 | 只读。引用的 PICTResourceSaveOptions 对象的类名。 |

## PicturePackageOptions

使用 `Application.makePicturePackage()` 创建的图片包的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `content` | `PicturePackageTextType` | 读写。内容信息（默认：`PicturePackageTextType.NONE`）。 |
| `flatten` | `boolean` | 读写。如果最终文档中的所有图层都被拼合则为真（默认：`true`）。 |
| `font` | `GalleryFontType` | 读写。用于安全文本的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | `number` | 读写。用于安全文本的字体大小（默认：`12`）。 |
| `layout` | `string` | 读写。用于生成图片包的布局（默认：" (2) 5x7"）。 |
| `mode` | `NewDocumentMode` | 读写。用作文档模式的颜色配置文件（默认：`NewDocumentMode.RGB`）。 |
| `opacity` | `number` | 读写。网页安全不透明度（百分比）（默认：`100`）。 |
| `resolution` | `number` | 读写。文档的分辨率，单位为每英寸像素数（默认：`72.0`）。 |
| `text` | `string` | 读写。图片包的自定义文本。仅当 `content` = `PicturePackageType.USER` 时有效。 |
| `textColor` | `RGBColor` | 读写。用于安全文本的颜色。 |
| `textPosition` | `GallerySecurityTextPositionType` | 读写。安全文本的位置（默认：`GallerySecurityTextPositionType.CENTERED`）。 |
| `textRotate` | `GallerySecurityTextRotateType` | 读写。用于安全文本的方向（默认：`GallerySecurityTextRotateType.ZERO`）。 |
| `typename` | `string` | 只读。引用的 `PicturePackageOptions` 对象的类名。 |



## PixarSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法以 Pixar 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | boolean | 可读写。True 表示保存 Alpha 通道。 |
| `typename` | string | 只读。引用的 `PixarSaveOptions` 对象的类名。 |

## PNGSaveOptions

使用 [Document.saveAs()](http://Document.saveAs()) 方法以 PNG 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **compression** | number [0..9] | 可读写。压缩值（默认：`0`）。 |
| **interlaced** | boolean | 可读写。True 表示交错行（默认：`false`）。 |
| **typename** | string | 只读。引用的 `PNGSaveOptions` 对象的类名。 |

## Preferences

表示 Photoshop 的应用程序首选项。通过 [Application.preferences](https://www.adobe.com/devnet/photoshop/scripting.html) 属性访问此对象。例如：

`app.preferences.rulerUnits = Units.PIXELS`
`app.preferences.typeUnits = TypeUnits.PIXELS`

在此对象中设置值等同于在 Adobe Photoshop CC 2015 应用程序中选择 **编辑 > 首选项**（Windows 中）或 **Photoshop > 首选项**（Mac OS 中）。有关各项设置的说明，请参阅 Adobe Photoshop CC 2015 帮助。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `additionalPluginFolder` | [File](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。附加插件文件夹的路径。<br><br> 仅在 [useAdditionalPluginFolder](https://www.adobe.com/devnet/photoshop/scripting.html) = `true` 时有效。 |
| `appendExtension` | [SaveBehavior](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。在 Windows 中写入文件扩展名的首选策略。 |
| `askBeforeSavingLayeredTIFF` | boolean | 可读写。True 表示在以 TIFF 格式保存文件时，询问用户确认图层保留选项。 |
| `autoUpdateOpenDocuments` | boolean | 可读写。True 表示自动更新打开的文档。 |
| `beepWhenDone` | boolean | 可读写。True 表示在过程完成时发出提示音。 |
| `colorChannelsInColor` | boolean | 可读写。True 表示在通道调板中以彩色显示组件通道。 |
| `colorPicker` | [ColorPicker](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。首选的颜色选择工具。 |
| `columnGutter` | number `[0.1..600.0]` | 可读写。列间距的宽度（以点为单位）。 |
| `columnWidth` | number `[0.1..600.0]` | 可读写。列宽（以点为单位）。 |
| `createFirstSnapshot` | boolean | 可读写。True 表示在创建新文档时自动制作第一个快照。 |
| `dynamicColorSliders` | boolean | 可读写。True 表示颜色调板中显示动态颜色滑块。 |
| `editLogItems` | [EditLogItemsType](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。历史记录日志的首选详细级别。仅在 [useHistoryLog](https://www.adobe.com/devnet/photoshop/scripting.html) = `true` 时有效。 |
| `exportClipboard` | `boolean` | 可读写。True 表示退出 Adobe Photoshop CC 2015 应用程序后，将内容保留在剪贴板上。 |
| `fontPreviewSize` | `FontPreviewType` | 可读写。在文字工具字体菜单中用于字体预览的首选字体大小。 |
| `fullSizePreview` | `boolean` | 可读写。True 表示以全尺寸图像显示图像预览，false 表示显示缩略图（仅限 Mac OS）。 |
| `gamutWarningOpacity` | `number [0..100]` | 可读写。不透明度值（以百分比表示）。 |
| `gridSize` | `GridSize` | 可读写。网格中方块的首选大小。 |
| `gridStyle` | `GridLineStyle` | 可读写。非打印网格线的首选格式样式。 |
| `gridSubDivisions` | `number [1..100]` | 可读写。网格细分数量。 |
| `guideStyle` | `GuideLineStyle` | 可读写。非打印参考线的首选格式样式。 |
| `iconPreview` | `boolean` | 可读写。True 表示使用图标预览（仅限 Mac OS）。 |
| `imageCacheLevels` | `number [1..8]` | 可读写。要保存在缓存中的图像数量。 |
| `imagePreviews` | `SaveBehavior` | 可读写。在 Windows 中写入图像预览的首选策略。 |
| `interpolation` | `ResampleMethod` | 可读写。在图像重新取样或调整大小时，用于为创建的任何新像素分配颜色值的方法。 |
| `keyboardZoomResizesWindows` | `boolean` | 可读写。True 表示使用键盘快捷键缩放时自动调整窗口大小。 |
| `macOSThumbnail` | `boolean` | 可读写。True 表示在保存图像时创建缩略图（仅限 Mac OS）。 |
| `maximizeCompatibility` | `QueryStateType` | 可读写。打开 PSD 文件时，检查是否最大化兼容性的首选策略。 |
| `maxRAMuse` | `number [5..100]` | 可读写。Adobe Photoshop CC 2015 使用的最大可用 RAM 百分比（5 - 100）。 |
| `nonLinearHistory` | `boolean` | 可读写。True 表示允许非线性历史记录。 |
| `numberOfHistoryStates` | `number` | 可读写。要保留的历史记录状态数量。 |
| `otherCursors` | `OtherPaintingCursors` | 可读写。用于某些工具的首选指针类型。 |
| `paintingCursors` | `PaintingCursors` | 可读写。用于某些工具的首选指针类型。 |
| `parent` | `Application` | 可读写。包含的应用程序。 |
| `pixelDoubling` | `boolean` | 可读写。True 表示将分辨率减半（像素大小加倍）以使预览显示更快。 |
| `pointSize` | `PointType` | 可读写。点/派卡大小。 |
| `recentFileListLength` | `number [0..30]` | 可读写。最近文件列表中的项目数。 |
| `rulerUnits` | `Units` | 可读写。脚本系统在接收和返回值时将使用的单位。 |
| `saveLogItems` | `SaveLogItemsType` | 可读写。保存历史记录项目时，历史记录日志数据的首选位置。 |
| `saveLogItemsFile` | `File` | 可读写。首选位置是文件时，历史记录日志文件的路径。 |
| `savePaletteLocations` | `boolean` | 可读写。True 表示使新调板位置成为默认位置。 |
| `showAsianTextOptions` | `boolean` | 可读写。True 表示在段落调板中显示亚洲文字选项。 |
| `showEnglishFontNames` | `boolean` | 可读写。True 表示以英文列出亚洲字体名称。 |
| `showSliceNumber` | `boolean` | 可读写。True 表示在使用切片工具时，在文档窗口中显示切片编号。 |
| `showToolTips` | `boolean` | 可读写。True 表示显示鼠标悬停时的弹出定义。 |
| `smartQuotes` | `boolean` | 可读写。True 表示使用弯引号，false 表示使用直引号。 |
| `textFontSize` | `FontSize` | 可读写。在调板和对话框中使用的小字体的大小。 |
| `typename` | `string` | 只读。引用的 `preferences` 对象的类名。 |
| `typeUnits` | [TypeUnits](https://helpx.adobe.com/photoshop/using/type-units.html) | 可读写。文本字符测量的首选单位。 |
| `useAdditionalPluginFolder` | boolean | 可读写。True 表示使用一个附加文件夹来存储与另一个应用程序兼容的插件。 |
| `useHistoryLog` | boolean | 可读写。True 表示为历史记录状态创建日志文件。 |
| `useLowerCaseExtension` | boolean | 可读写。True 表示对文件扩展名使用小写字母。 |
| `useShiftKeyForToolSwitch` | boolean | 可读写。True 表示启用在一组隐藏工具之间循环切换。 |
| `useVideoAlpha` | boolean | 可读写。True 表示允许 Adobe Photoshop CC 2015 将透明度信息发送到计算机的视频板。（需要硬件支持。） |
| `windowsThumbnail` | boolean | 可读写。True 表示在 Windows 中保存图像时创建缩略图。（需要硬件支持。） |



## PresentationOptions

使用 `Application.makePDFPresentation()` 创建 Adobe PDF 演示文稿的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| autoAdvance | boolean | 读写。设为 true 可在查看演示文稿时自动切换图像（默认值：true）。仅当 presentation = true 时有效。 |
| includeFilename | boolean | 读写。设为 true 可包含图像的文件名（默认值：false）。 |
| interval | number [1..60] | 读写。自动切换视图前的等待时间，单位为秒（默认值：5）。仅当 autoAdvance = true 时有效。 |
| loop | boolean | 读写。设为 true 可在最后一页后重新开始演示（默认值：false）。仅当 autoAdvance = true 时有效。 |
| magnification | MagnificationType | 读写。查看图像时使用的放大类型。 |
| PDFFileOptions | PDFSaveOptions | 读写。创建 PDF 文件时使用的选项。 |
| presentation | boolean | 读写。设为 true 表示输出将是演示文稿（默认值：false）；设为 false 时，输出为多页文档。 |
| transition | TransitionType | 读写。从一张图像过渡到下一张的方法（默认值：TransitionType.NONE）。仅当 autoAdvance = true 时有效。 |
| typename | string | 只读。引用的 PresentationOptions 对象的类名。 |

## RawFormatOpenOptions

使用 `Application.open()` 方法打开 RAW 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **bitsPerChannel** | number | 读写。每个通道的位数。<br><br>唯一有效的值是 `BitsPerChannelType.EIGHT` 或 `BitsPerChannelType.SIXTEEN`。 |
| **byteOrder** | ByteOrder | 读写。读取多字节值的顺序。<br><br>仅当 `bitsPerChannel` = `BitsPerChannelType.SIXTEEN` 时有效。 |
| **channelNumber** | number [1..56] | 读写。图像中的通道数。其值不能超过图像中的通道数。<br><br>当 `bitsPerChannel` = `BitsPerChannelType.SIXTEEN` 时，唯一有效的值是 1、3 或 4。 |
| **headerSize** | number [0..1919999] | 读写。在实际图像信息开始之前，文件中出现的信息字节数；即在文件开头插入的用作占位符的零的数量。 |
| **height** | number | 读写。图像的高度（以像素为单位）。 |
| **interleaveChannels** | boolean | 读写。设为 true 可按顺序存储颜色值。 |
| **retainHeader** | boolean | 读写。设为 true 可在保存时保留标题。<br><br>仅当 `headerSize` 为 1 或更大时有效。 |
| **typename** | string | 只读。引用的 RawFormatOpenOptions 对象的类名。 |
| **width** | number | 读写。图像的宽度（以像素为单位）。 |

## RawSaveOptions

使用 `Document.saveAs()` 方法以 RAW 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alphaChannels | boolean | 读写。设为 true 表示应保存 Alpha 通道。 |
| spotColors | boolean | 读写。设为 true 表示应保存专色。 |
| typename | string | 只读。引用的 RawSaveOptions 对象的类名。 |

## RGBColor

定义 RGB 颜色，用于 [SolidColor](https://example.com) 对象。

另请参阅 [CMYKColor](https://example.com)、[GrayColor](https://example.com)、[HSBColor](https://example.com)、[LabColor](https://example.com)、[NoColor](https://example.com)。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| **blue** | `number [0..255]` | 读写。蓝色值（默认值：255）。 |
| **green** | `number [0..255]` | 读写。绿色值（默认值：255）。 |
| **hexValue** | `string` | 读写。颜色的十六进制表示。 |
| **red** | `number [0..255]` | 读写。红色值（默认值：255）。 |
| **typename** | `string` | 只读。引用的 `RGBColor` 对象的类名。 |

## Selection

文档或图层的选定区域。通过 [Document.selection](Document.selection) 属性访问。例如：
`app.activeDocument.selection.fill(app.foregroundColor)`
许多属性和方法使用 [UnitValue](UnitValue) 类型，该类型将测量值与测量单位相结合。有关此类型的信息，请参阅 *JavaScript 工具指南*。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `bounds` | array of [UnitValue](UnitValue) | 只读。整个选区的边界矩形。 |
| `parent` | [Document](Document) | 只读。对象的容器。 |
| `solid` | boolean | 只读。如果边界矩形是实心的，则为 true。 |
| `typename` | string | 只读。引用的 `selection` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `clear()` | | | 清除选区且不将其复制到剪贴板。 |
| `contract(by)` | [UnitValue](UnitValue) | | 按指定量收缩（减少）选区。 |
| `copy([merge])` | boolean | | 将选区复制到剪贴板。使用可选参数并设为 `true` 时，执行合并复制（选区中的所有可见图层都会被复制）。 |
| `cut()` | | | 清除当前选区并将其复制到剪贴板。 |
| `deselect()` | | | 取消选择当前选区。 |
| `expand(by)` | [UnitValue](UnitValue) | | 按指定量扩展选区。 |
| `feather(by)` | [UnitValue](UnitValue) | | 按指定量羽化选区的边缘。 |

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `fill(filltype[, mode][, opacity][, preserveTransparency])` | `SolidColor`, `ColorBlendMode`, number `[1..100]`, boolean | | 填充选区。<br><br>`opacity` 是百分比值。 |
| `grow(tolerance, antiAlias)` | number, boolean | | 扩展选区以包含所有在指定容差范围内的相邻像素。 |
| `invert()` | | | 反转选区（取消选择选区并选择图层或文档的其余部分）。<br><br>**提示：** 要翻转选区形状，请参阅 [`rotate`](https://extendscript.docsforadobe.dev/scripting-docs/en-us/interface/javascript-tools-guide/objects/selection-resizeboundar.html)。 |
| `load(from[, combination][, inverting])` | `Channel`, `SelectionType`, boolean | | 从指定的通道加载选区。 |
| `makeWorkPath([tolerance])` | number | | 将此选区项设置为本文档的工作路径。 |
| `resize([horizontal][, vertical][, anchor])` | number, number, `AnchorPosition` | | 将选定区域调整为指定的尺寸和锚点位置。 |
| `resizeBoundary([horizontal][, vertical][, anchor])` | number, number, `AnchorPosition` | | 围绕指定的锚点更改选区的尺寸。 |
| `rotate(angle[, anchor])` | number, `AnchorPosition` | | 围绕指定的锚点将选区旋转指定的量。 |
| `rotateBoundary(angle[, anchor])` | number, `AnchorPosition` | | 围绕指定的锚点旋转选区的边界。 |
| `select(region[, type][, feather][, antiAlias])` | array of number, `SelectionType`, number, boolean | | 选择指定的区域。<br><br>`region` 参数是一个包含四个坐标的数组：`[左, 上, 右, 下]`。 |
| `selectAll()` | | | 选择整个图层。 |

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `selectBorder(width)` | UnitValue | | 仅选择选区边框（指定宽度）；后续操作不会影响边框内选定的区域。 |
| `similar(tolerance, antiAlias)` | number, boolean | | 扩展选区以包含整个图像中在容差范围内的像素。 |
| `smooth(radius)` | number | | 清理基于颜色的选区内部或外部遗留的杂散像素（在以像素为单位指定的半径内）。 |
| `store(into[, combination])` | Channel, SelectionType | | 将选区另存为通道。 |
| `stroke(strokeColor, width[, location][, mode][, opacity][, preserveTransparency])` | SolidColor, number, StrokeLocation, ColorBlendMode, number [1..100], boolean | | 对选区边框进行描边。opacity 是百分比值。 |
| `translate([deltaX][, deltaY])` | UnitValue, UnitValue | | 相对于当前位置移动整个选区。 |
| `translateBoundary([deltaX][, deltaY])` | UnitValue, UnitValue | | 相对于当前位置移动选区。 |

### 选区示例脚本

以下脚本通过以下步骤创建棋盘格：

- 创建一个 800 x 800 像素的文档。
- 将整个文档划分为 100 x 100 像素的正方形。
- 选择第一行中的每个其他正方形，然后将选择标准移位以选择下一行中的交替正方形。重复此过程，直到选中文档中的每个其他正方形。
- 用调色板中的前景色填充选中的正方形。
- 反转选区，并用调色板中的背景色填充新选中的正方形。
- 取消选择这些正方形，以移除选择轮廓（“蚂蚁线”）。

### Selection.jsx

```
// 保存当前首选项
var startRulerUnits = app.preferences.rulerUnits
```

var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.displayDialogs = DialogModes.NO

// Close all the open documents
while (app.documents.length) {
    app.activeDocument.close()
}

// Create variables for the 800 pixel board divided in even 100 x 100 squares
var docSize = 800
var cells = 8
var cellSize = docSize / cells

// create a new document
var checkersDoc = app.documents.add(docSize, docSize, 72, "Checkers")

// Create a variable to use for selecting the checker board
// That allows me to shift the selection one square to the right
// on every other row, and then shift back for the rows in between.
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
        // In subsequent iterations, use the EXTEND constant value
        // of the select() method to add to the selection (in the loop’s else clause)
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

// Fill the current selection with the foreground color
checkersDoc.selection.fill(app.foregroundColor)

// Invert the selection
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

## SGIRGBSaveOptions

使用 [Document.saveAs](https://www.adobe.com/devnet/photoshop/scripting.html) 方法以 SGIRGB 格式保存文档的选项。

> **注意：** SGIRGB 格式不会随 Adobe Photoshop CC 2015 自动安装。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `alphaChannels` | 布尔值 | 可读写。为 true 时保存 Alpha 通道。 |
| `spotColors` | 布尔值 | 可读写。为 true 时保存专色。 |
| `typename` | 字符串 | 只读。引用的 `SGIRGBSaveOptions` 对象的类名。 |

## SolidColor

文档中使用的颜色定义。将一种颜色映射到所有可用颜色模型中的等效值。

- 用于 [Application.backgroundColor](https://www.adobe.com/devnet/photoshop/scripting.html) 和 [foregroundColor](https://www.adobe.com/devnet/photoshop/scripting.html) 属性，用于 [Channel.color](https://www.adobe.com/devnet/photoshop/scripting.html)，用于 [ColorSampler.color](https://www.adobe.com/devnet/photoshop/scripting.html)，以及用于 [TextItem.color](https://www.adobe.com/devnet/photoshop/scripting.html)
- 传递给 [PathItem.fillPath()](https://www.adobe.com/devnet/photoshop/scripting.html)、[Selection.fill()](https://www.adobe.com/devnet/photoshop/scripting.html) 和 [Selection.stroke()](https://www.adobe.com/devnet/photoshop/scripting.html)。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| cmyk | [CMYKColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。CMYK 颜色模式。 |
| gray | [GrayColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。灰度颜色模式。 |
| hsb | [HSBColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。HSB 颜色模式。 |
| lab | [LabColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。LAB 颜色模式。 |
| model | [ColorModel](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。颜色模型。 |
| nearestWebColor | [RGBColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 只读。当前颜色最接近的 Web 颜色。 |
| rgb | [RGBColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。RGB 颜色模式。 |
| typename | `string` | 只读。引用的 `SolidColor` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| :--- | :--- | :--- | :--- |
| `isEqual` (color) | [SolidColor](https://www.adobe.com/devnet/photoshop/scripting.html) | `boolean` | 如果 `SolidColor` 对象在视觉上等于指定颜色，则为 true。 |

## SubPathInfo

PathPoint 对象的数组，描述路径的直线或曲线段，用于创建 SubPathItem。

将这些对象的数组传递给 PathItems.add() 方法。此方法为每个 SubPathInfo 对象创建一个 SubPathItem 对象，并为所有子路径表示的路径创建并返回一个新的 PathItem 对象。

- 使用 SubPathInfo 创建子路径；属性可写。
- 使用 SubPathItem 对象检索有关现有子路径的信息。属性为只读。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| closed | 布尔值 | 可读写。为 true 时，路径描述一个封闭区域。 |
| entireSubPath | PathPoint 数组 | 可读写。 |
| operation | ShapeOperation | 可读写。子路径对其他子路径的操作。指定如果目标路径已有选区时如何组合形状。 |
| typename | 字符串 | 只读。引用的 SubPathInfo 对象的类名。 |

## SubPathItem

表示一个子路径；一组子路径构成一个 PathItem。

通过将 SubPathInfo 对象传递给 PathItems.add() 方法来创建这些对象。此方法为每个 SubPathInfo 对象创建一个 SubPathItem 对象，并为所有子路径表示的路径创建并返回一个新的 PathItem 对象。在 PathItem.subPathItems 集合中访问这些对象。

- 使用 SubPathItem 对象检索有关现有子路径的信息。属性为只读。
- 使用 SubPathInfo 创建子路径；属性可写。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| **closed** | `boolean` | 只读。为 true 时，路径已闭合。 |
| **operation** | [ShapeOperation](https://www.adobe.com/devnet/photoshop/scriptingreference/) | 只读。当此对象与另一个 SubPathItem 对象相交时的行为。指定如果目标路径已有选区时如何组合形状。 |
| **parent** | [PathItem](https://www.adobe.com/devnet/photoshop/scriptingreference/) | 只读。对象的容器。 |
| **pathPoints** | [PathPoints](https://www.adobe.com/devnet/photoshop/scriptingreference/) | 只读。PathPoints 集合。 |
| **typename** | `string` | 只读。引用的 SubPathItem 对象的类名。 |



## SubPathItems

构成 PathItem 的 SubPathItem 对象集合。通过 PathItem.subPathItems 集合属性访问此对象。

-   使用 SubPathInfo 创建子路径；其属性可写。
-   使用 SubPathItem 对象检索现有子路径的信息。其属性只读。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| **length** | number | 只读。集合中的元素数量。 |
| **parent** | PathItem | 只读。所属的路径项。 |
| **typename** | string | 只读。引用的 SubPathItems 对象的类名。 |

## TargaSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法以 TGA (Targa) 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | `boolean` | 读写。是否保存 Alpha 通道。 |
| `resolution` | `TargaBitsPerPixel` | 读写。每像素的位数 (默认: `TargaBitsPerPixels.TWENTYFOUR`)。 |
| `rleCompression` | `boolean` | 读写。是否使用 RLE 压缩 (默认: `true`)。 |
| `typename` | `string` | 只读。引用的 `TargaSaveOptions` 对象的类名。 |

## TextFont

描述应用程序可用的字体。通过 [Application.fonts](Application.fonts) 集合访问此对象。例如：

```
var myFont = app.fonts.getByName("ArialMT");
```

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| **family** | `string` | 只读。字体族。 |
| **name** | `string` | 只读。字体名称。 |
| **parent** | [Application](Application) | 只读。所属的应用程序。 |
| **postScriptName** | `string` | 只读。字体的 PostScript 名称。 |
| **style** | `string` | 只读。字体样式。 |
| **typename** | `string` | 只读。引用的 `TextFont` 对象的类名。 |

## TextFonts

计算机上可用字体的集合。字体由 [TextFont](https://example.com) 对象表示。通过 [Application.fonts](https://example.com) 集合属性访问此对象。例如，以下代码显示可用字体的数量：

```
alert(app.fonts.length);
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。集合中的元素数量。 |
| parent | [Application](https://example.com) | 只读。所属的应用程序。 |
| typename | string | 只读。引用的 `TextFonts` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| getByName(name) | string | [TextFont](https://example.com) | 获取 `TextFonts` 集合中具有所提供名称的第一个元素。 |

## TextItem

ArtLayer 对象中 kind 属性为 LayerKind.TEXT 的文本。通过 ArtLayer.textItem 属性访问此对象。例如：

```
myLayers[i].textItem.contents = "Layer in " + textArray[i] + " Set Inside "
```

许多属性使用 UnitValue 类型，该类型将测量值与测量单位相结合。有关此类型的更多信息，请参阅 JavaScript 工具指南。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alternateLigatures | boolean | 读写。是否使用替代连字。**注意：** 替代连字与酌情连字相同。有关更多信息，请参阅 Adobe Photoshop CC 2015 帮助。 |
| antiAliasMethod | AntiAlias | 读写。要使用的抗锯齿方法。 |
| autoKerning | AutoKernType | 读写。要使用的自动字距调整选项。 |
| autoLeadingAmount | number [0.01..5000.00] | 读写。自动（默认）行距所使用的百分比（以点为单位）。仅在 useAutoLeading = true 时有效。 |
| baselineShift | UnitValue | 读写。文本基线偏移中使用的单位值。 |
| capitalization | TextCase | 读写。文本大小写。 |
| color | SolidColor | 读写。文本颜色。 |
| contents | string | 读写。图层中的实际文本。 |
| desiredGlyphScaling | number [50..200] | 读写。缩放文本字符水平大小的所需量。百分比值；在 100 时，字符宽度不缩放。仅在 justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED, 或 Justification.RIGHTJUSTIFIED 时有效。使用时，还需要 minimumGlyphScaling 和 maximumGlyphScaling 值。 |
| desiredLetterScaling | number [100..500] | 读写。字符间的间距量（在 0 时，字符间不添加空格）。等同于段落调板菜单（选择 **Justification**）的 **Justification** 对话框中的 **Letter Spacing**。仅在 `justification` = `Justification.CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFTJUSTIFIED`, 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 [`minimumLetterScaling`](#minimumLetterScaling) 和 [`maximumLetterScaling`](#maximumLetterScaling) 值。 |
| desiredWordScaling | number [0..1000] | 读写。单词间的间距量（百分比）（在 100 时，单词间不添加额外空格）。等同于段落调板菜单（选择 **Justification**）的 **Justification** 对话框中的 **Word Spacing**。仅在 `justification` = `Justification.CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFTJUSTIFIED`, 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 [`minimumWordScaling`](#minimumWordScaling) 和 [`maximumWordScaling`](#maximumWordScaling) 值。 |
| direction | Direction | 读写。文本方向。 |
| fauxBold | boolean | 读写。是否使用伪粗体（默认: *false*）。将此项设置为 true 相当于选择文本并单击字符调板中的 Faux Bold。 |
| fauxItalic | boolean | 读写。是否使用伪斜体（默认: *false*）。将此项设置为 true 相当于选择文本并单击字符调板中的 Faux Italic。 |
| firstLineIndent | UnitValue [-1296..1296] points | 读写。段落首行的缩进量（单位值）。 |
| font | string | 读写。字符的文本字体。使用字体的 PostScript 名称。请参阅 [`TextFont`](#TextFont) 并使用 `postScriptName` 属性。 |
| hangingPunctuation | boolean | 读写。是否使用罗马悬挂标点。 |
| height | UnitValueX | 读写。段落文本边界框的高度（单位值）。仅在 `kind` = `TextType.PARAGRAPHTEXT` 时有效。 |
| horizontalScale | number [0..1000] | 读写。相对于 [`verticalScale`](#verticalScale) 的字符缩放（水平）（百分比值）。 |
| hyphenateAfterFirst | number [1..15] | 读写。允许在自动换行中使用连字符的字母数之后。 |
| hyphenateBeforeLast | number [1..15] | 读写。允许在自动换行中使用连字符的字母数之前。 |
| hyphenateCapitalWords | boolean | 读写。是否允许在大写单词的自动换行中使用连字符。 |
| hyphenateWordsLongerThan | number [2..25] | 读写。单词必须包含的最小字母数，以允许在自动换行中使用连字符。 |
| hyphenation | boolean | 读写。是否在自动换行中使用连字。 |
| hyphenationZone | UnitValue [0..720] pica | 读写。行末将导致单词在非两端对齐文本中断开的距离。 |
| hyphenLimit | number | 读写。可以以连字符结尾的最大连续行数。 |
| justification | Justification | 读写。段落对齐方式。 |
| kind | TextType | 读写。文本换行类型。 |
| language | Language | 读写。要使用的语言。 |
| leading | UnitValue | 读写。行距量。 |
| leftIndent | UnitValue [-1296..1296] points | 读写。文本从左侧缩进的空格量。 |
| ligatures | boolean | 读写。是否使用连字。 |
| maximumGlyphScaling | number [50..200] | 读写。缩放文本字符水平大小的最大量（百分比值；在 100 时，字符宽度不缩放）。仅在 justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED, 或 Justification.RIGHTJUSTIFIED 时有效。使用时，还需要 minimumGlyphScaling 和 desiredGlyphScaling 值。 |



## TiffSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法将文档保存为 TIFF 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alphaChannels | boolean | 读写。为 true 则保存 Alpha 通道。 |
| annotations | boolean | 读写。为 true 则保存注释。 |
| byteOrder | ByteOrder | 读写。文档多字节值的读取顺序（默认值：在 Mac OS 上为 ByteOrder.MACOS，在 Windows 上为 ByteOrder.IBM）。 |
| embedColorProfile | boolean | 读写。为 true 则在文档中嵌入颜色配置文件。 |
| imageCompression | TIFFEncoding | 读写。压缩类型（默认值：TIFFEncoding.NONE）。 |
| interleaveChannels | boolean | 读写。为 true 则图像中的通道将被交错。 |
| jpegQuality | number [0..12] | 读写。生成图像的质量，与 JPEG 压缩量成反比。仅当 imageCompression = TIFFEncoding.JPEG 时有效。 |
| layerCompression | LayerCompression | 读写。保存图层（与保存合成数据相对）时使用的压缩方法。仅当 layers = true 时有效。 |
| layers | boolean | 读写。为 true 则保存图层。 |
| saveImagePyramid | boolean | 读写。为 true 则保留多分辨率信息（默认值：false）。 |
| spotColors | boolean | 读写。为 true 则保存专色。 |
| transparency | boolean | 读写。为 true 则将透明度保存为额外的 Alpha 通道（以便在另一个应用程序中打开文件时使用）。 |
| typename | string | 只读。引用的 TiffSaveOptions 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `convertToShape()` | | | 将文本项目及其包含的图层转换为填充图层，其中文本更改为剪贴路径。 |
| `createPath()` | | | 从实际文本项目（如字母或单词）的轮廓创建剪贴路径。 |

## 属性

| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `maximumLetterScaling` | number [100..500] | 读写。允许在字母之间添加的最大空间量（在 0 时，不添加字母间距）。<br><br>等同于“段落”调色板菜单中“对齐方式”对话框中的 **字距调整**。<br><br>仅当 [`justification`](#) = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED 时有效。<br><br>使用时，还需要 [`minimumLetterScaling`](#) 和 [`desiredLetterScaling`](#) 的值。 |
| `maximumWordScaling` | number [0..1000] | 读写。允许在单词之间添加的最大空间量（百分比值；在 100 时，不在单词之间添加额外空间）。<br><br>等同于“段落”调色板菜单中“对齐方式”对话框中的 **字间距**。<br><br>仅当 [`justification`](#) = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED 时有效。<br><br>使用时，还需要 [`minimumWordScaling`](#) 和 [`desiredWordScaling`](#) 的值。 |
| `minimumGlyphScaling` | number [50..200] | 读写。缩放文本字母水平尺寸的最小量（百分比值；在 100 时，不缩放字符宽度）。<br><br>仅当 [`justification`](#) = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED 时有效。<br><br>使用时，还需要 [`maximumGlyphScaling`](#) 和 [`desiredGlyphScaling`](#) 的值。 |
| `minimumLetterScaling` | `number` [100..500] | 读写。允许在字母之间添加的最小空间量（百分比值；在 0 时，不移除字母间距）。<br><br>等同于“段落”调色板菜单中“对齐方式”对话框中的 **字距调整**。<br><br>仅当 justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED 时有效。<br><br>使用时，还需要 maximumLetterScaling 和 desiredLetterScaling 的值。 |
| `minimumWordScaling` | `number` [0..1000] | 读写。允许在单词之间添加的最小空间量（百分比值；在 100 时，不在单词之间移除额外空间）。<br><br>等同于“段落”调色板菜单中“对齐方式”对话框中的 **字间距**。<br><br>仅当 justification = Justification.CENTERJUSTIFIED、FULLYJUSTIFIED、LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED 时有效。<br><br>使用时，还需要 maximumWordScaling 和 desiredWordScaling 的值。 |
| `noBreak` | `boolean` | 读写。为 true 则禁止此文本中的换行。<br><br>**提示：** 当许多连续字符都设置为 true 时，可以防止自动换行，从而可能导致某些文本在屏幕上不显示。 |
| `oldStyle` | `boolean` | 读写。为 true 则使用旧式字体。 |
| `parent` | ArtLayer | 读写。包含的图层。 |
| `position` | `UnitValue 数组` | 读写。文本的原点位置。数组成员指定 X 和 Y 坐标。<br><br>等同于使用文本工具在文档中单击以创建文本原点。 |
| `rightIndent` | UnitValue [-1296..1296] 点 | 读写。文本从右侧缩进的空间量。 |
| `size` | UnitValue | 读写。字体大小（以 `UnitValue` 表示）。注意：对于 CS3 及更早版本，类型为 `points`。 |
| `spaceAfter` | UnitValue [-1296..1296] 点 | 读写。每个段落之后使用的空间量。 |
| `spaceBefore` | `UnitValue` [-1296..1296] 点 | 读写。每个段落之前使用的空间量。 |
| `strikeThru` | StrikeThruType | 读写。使用的文本删除线选项。 |
| `textComposer` | TextComposer | 读写。用于评估换行并优化指定的断字和对齐选项的组合方法。<br><br>仅当 `kind` = `TextType.PARAGRAPHTEXT` 时有效。 |
| `tracking` | number [-1000..10000] | 读写。多个字符之间的均匀间距量。<br><br>字距调整单位为 1/1000 em 空间。em 空间的宽度相对于当前字体大小。在 1 点字体中，1 em 等于 1 点；在 10 点字体中，1 em 等于 10 点。因此，例如，在 10 点字体中，100 个单位相当于 1 点。 |
| `typename` | string | 只读。引用的 `textItem` 对象的类名。 |
| `underline` | UnderlineType | 读写。文本下划线选项。 |
| `useAutoLeading` | boolean | 读写。为 true 则使用字体内置的行距信息。 |
| `verticalScale` | number [0-1000] | 读写。相对于 horizontalScale 的垂直字符缩放比例（百分比值）。 |
| `warpBend` | number [-100..100] | 读写。弯曲变形百分比。 |
| `warpDirection` | Direction | 读写。弯曲变形方向。 |
| `warpHorizontalDistortion` | number [-100..100] | 读写。弯曲变形的水平失真（百分比值）。 |
| `warpStyle` | WarpStyle | 读写。使用的弯曲变形样式。 |
| `warpVerticalDistortion` | number [-100..100] | 读写。弯曲变形的垂直失真（百分比值）。 |
| `width` | UnitValue | 读写。段落文本的定界框宽度。<br><br>仅当 `kind` = `TextType.PARAGRAPHTEXT` 时有效。 |



## UnitValue

ExtendScript 定义了 JavaScript 类 `UnitValue`，用于表示测量值及其测量单位；详情参见['JavaScript support in Adobe Photoshop CC 2015' 第 32 页]('JavaScript support in Adobe Photoshop CC 2015')。关于这些类的参考细节，请参阅 *JavaScript Tools Guide*。

## xmpMetadata

Camera RAW 图像的 XMP 元数据。

对于 Camera RAW 图像文件，XMP 元数据存储在一个 *sidecar* 文件中，该文件与 RAW 文件位于同一文件夹内，具有相同的基本名称和 XMP 扩展名。

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| `parent` | [Document](https://www.adobe.com/devnet/photoshop/scripting.html) | 只读。包含的文档。 |
| `rawData` | 字符串 | 可读写。包含 XML (RDF) 格式的 XMP 元数据的字符串。有关此格式的详细信息，请参阅 *XMP Specification*。 |
| `typename` | 字符串 | 只读。所引用的 `xmpMetadata` 对象的类名。 |

# Adobe Photoshop CC 2015

### JavaScript 参考指南

#### JavaScript 资源

本节描述了使你的 JavaScript 脚本能够像插件一样运行的 JavaScript 资源。这包括：

- 指定脚本作为命令出现的菜单的能力，
- 一个术语资源，使脚本能够与 Action Manager 一起工作，这允许你的脚本被录制并通过脚本参数自动化，
- 一个类别，用于在菜单内对命令进行排序和分组，
- 以及一个启用字符串，用于指示在给定条件下该命令是启用还是禁用的。
- 字符串必须是有效的 XML 语法。例如，“&”字符将不起作用。在启用信息块中使用 `&amp;` 来表示逻辑“&&”。

#### JavaScript 资源语法

JavaScript 资源具有类似 HTML 的语法，每个 `<tag>` 都有一个对应的关闭标签 `</tag>`。此资源需要出现在注释（`/* ... */`）内，并且应在脚本文件的顶部定义（在文件的前 10,240 个字符内）。

| 标签 | 描述 |
|---|---|
| `<javascriptresource>` | 资源定义标签。 |
| `<name>` | 出现在 Photoshop 菜单中的命令名称。<br>如果资源中未提供此标签，则菜单中命令的名称默认为脚本的名称。 |
| `<menu>` | 命令出现的菜单。如果未提供此标签，命令将出现在 **文件 > 脚本** 菜单中。<br>**注意：** 目前 `<menu>` 唯一支持的值是 `automate`、`filter` 和 `help`。例如，`automate` 会将脚本放入 **文件 > 自动** 菜单中。 |
| `<about>` | 出现在“关于”框中的字符串，用户可以从 **帮助 > 关于插件** 菜单中选择该框。 |
| `<enableinfo>` | 一个布尔表达式，指示菜单中的命令是否启用。请参阅“启用信息语法”部分。<br>**注意：** 如果提供了此标签，则当且仅当至少有一个文档打开，并且布尔表达式计算结果为 true 时，菜单项才启用。如果你希望菜单项始终启用，请不要使用此标签。 |
| `<eventid>` | 一个标识事件的唯一字符串。使用 UUID 将确保你的脚本不会与其他脚本共享此标识符。 |
| `<category>` | 命令在菜单中出现的类别。用于在菜单中分组和排序命令。命令基于 `<category>` 中的字符串按字母顺序放置在菜单中。如果两个命令使用相同的类别，它们将被分组在一起。 |
| `<terminology>` | 使脚本能够与 Action Manager 一起工作的术语词典。请参阅“术语词典”部分。 |

### 基本 JavaScript 资源示例

此示例展示了一个非常基本的 `<javascriptresource>`。使用此资源，可以通过选择 **添加文档** 命令来执行脚本，该命令出现在 **自动** 菜单中。此命令在菜单中是启用的，前提是至少已经打开了一个文档。如果用户从 **关于插件** 菜单请求有关脚本的信息，则会将 `<about>` 标签中包含的字符串显示在对话框中。

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

### 启用信息语法

`<enableinfo>` 标签提供一个布尔表达式，当该表达式被计算时，指示菜单中的命令是否启用。你可以使用此表达式根据文档的各种特性来启用或禁用菜单项。启用信息语法如下：

```
<booleanExpression> :=       <conjunction> { "||" <conjunction> }
<conjunction> :=             <relation> {"&&" <relation> }
<relation> :=                <equality> {<relationOperator><equality>}
<equality> :=                <simpleExpression> {<equalityOperator><simpleExpression>}
<simpleExpression> :=        <term> {<addOperator><term>}
<term> :=                    <factor> {<mulOperator><factor>}
<factor> := <integer> | <intrinsic> | <ident> |
    "(" <booleanExpression> ")" | "(" <simpleExpression> ")" |
    "+" <factor> | "-" <factor> | "!" <factor>

<integer> := digit {digit}

<intrinsic> := <limitFunction> | <dimFunction> | <inFunction>

<limitFunction> := ( "min" | "max") "(" <simpleExpression> ","
    <simpleExpression> { "," <simpleExpression> } ")"

<dimFunction> := "dim" "(" <simpleExpression> "," <simpleExpression> ")"

<ident> := (alpha | "_") {alpha | digit | "_" }

<mulOperator> := "*" | "/"

<addOperator> := "+" | "-"

<equalityOperator> := "==" | "!="

<relationOperator> := "<" | "<=" | ">=" | ">"

<inFunction> := "in" "(" <simpleExpression> {"," <simpleExpression> } ")"
```

运算符优先级如下表所示。运算符按最高优先级在表格顶部列出。

| 运算符 | 描述 |
|---|---|
| `||` | 或 |
| `&&` | 与 |
| `+` `-` | 加法或减法 |
| `*` `/` | 乘法或除法 |
| `<` `<=` `>=` `>` | 小于、小于等于、大于等于、大于 |
| `==` `!=` | 等于或不等于 |
| `(..)` `in()` `max()` `min()` | 函数 |
| 一元 `+` `-` `!` | 一元运算符：增量、减量、非 |

该语法提供了可在 `<enableinfo>` 表达式中使用的变量和常量。下表列出了可用的常量。

| 常量名称 | 描述 |
|---|---|
| `true` | 布尔真 |
| `false` | 布尔假 |
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
| `Gray16Mode` | 灰度模式，每通道 16 位 |
| `RGB48Mode` | RGB 颜色模式，每通道 16 位。 |
| `Lab48Mode` | LAB 模式，每通道 16 位。 |
| `CMYK64Mode` | CMYK 模式，每通道 16 位。 |
| `DeepMultichannelMode` | 深度多通道模式。 |
| `Duotone16Mode` | 双色调模式，16 位深度。 |
| `RGB96Mode` | RGB 颜色模式，每通道 32 位。 |
| `Gray32Mode` | 灰度模式，32 位深度。 |

下表显示了可在 `<enableinfo>` 表达式中使用的变量集。这些变量的值是基于活动文档的属性设置的。

| 变量名称 | 描述 |
| --- | --- |
| `PSHOP_ImageMode` | 活动文档的图像模式。 |
| `PSHOP_ImageDepth` | 活动文档的深度。 |
| `PSHOP_HasLayerMask` | 布尔值，指示是否存在图层蒙版。 |
| `PSHOP_HasSelectionMask` | 布尔值，指示是否存在选区蒙版。 |
| `PSHOP_HasTransparencyMask` | 布尔值，指示是否存在透明度蒙版。 |
| `PSHOP_NumTargetChannels` | 目标通道的数量。 |
| `PSHOP_NumTrueChannels` | 图像通道的数量。 |
| `PSHOP_IsAdjustorSheet` | 布尔值 |
| `PSHOP_IsTargetComposite` | 布尔值，指示通道是否已拼合。 |
| `PSHOP_IsTargetSection` | 布尔值。 |
| `PSHOP_IsTargetVisible` | 布尔值。 |
| `PSHOP_ImageWidth` | 图像的宽度。 |
| `PSHOP_ImageHeight` | 图像的高度。 |
| `PSHOP_TargetProtectFlags` | |



## 启用信息评估中的未定义值

如果任何算术或关系运算包含一个值为未定义的操作数，或一个未定义的变量，则该评估的结果为 `false`。

布尔值的处理方式与 C/C++ 相同，其中非零值为 `true`，零为 `false`，但未定义的值也为 `false`。

## 使用 "in" 函数

`in` 函数（参见 `<inFunction>`）在第一个参数至少等于后续参数之一时返回 `true`。一个典型用法可能是检查活动文档的图像模式是否是一组图像模式中的一种。例如：

```
in(PSHOP_ImageMode, RGBMode, CMYKMode, LabMode)
```

## Action Manager 自动化

要使你的脚本能够记录脚本参数并由其自动化，需要添加两个基本机制：

- 一个*术语字典*，它将脚本的用户界面映射到人类可读的文本，为脚本使用的每个参数提供文本和类型信息。
- 用于在参数来自 Action Manager（而非用户界面）时读取参数信息的代码，以及用于将参数信息写入 Action Manager 的代码。此代码使用 Action Manager 类 `ActionDescriptor`、`ActionList` 和 `ActionReference`。

有关能够记录和由脚本参数自动化的脚本示例，请参见 `Conditional Mode Change.jsx`。此文件可在 Presets/Scripts 文件夹中找到。

## 术语字典

JavaScript 资源提供了一个 `<terminology>` 标签，允许你为脚本提供术语字典。创建术语字典的第一步是检查脚本的用户界面，并为用户界面中的每个元素创建人类可读的字符串。

例如，在“条件模式更改”命令中，用户界面请求一个源模式和一个目标模式。源模式和目标模式都有几个选项。所有这些用户界面元素都需要在术语字典中有条目。

术语字典以 PDF 字典格式创建，包含以下条目，并且必须在 `<javascriptresource>` 中具有以下格式：

```
<terminology><![CDATA[[[
    /Version integer
    /Events <<event dictionary>>
    /Classes <<class dictionary>>
    /Enumerations <<enumeration dictionary>>
>>> ]]></terminology>
```

**注意：** 术语标签中的信息需要包装在 `CDATA` 块中，以便 XML 解析器忽略术语中出现的 "/" 和其他标签。

事件、类和枚举字典的定义如下提供。

/Events 字典包含每个事件的条目：

```
/eventName [                  // Name used in string-based API
    (String event name)     // required
    /direct parameter type  // optional; if omitted, no parameter
    <<                      // optional parameter dictionary
        /parameterName [    // Name used in string-based API
            (String name)   // required
            /parameter type // required
            ]
        ...                 // other parameters
    >>
]
```

/Classes 字典包含每个类的条目：

```
/className [                  // Name used in string-based API
    (ZString class name)    // required
    <<                      // property dictionary
        /propertyName [     // Name used in string-based API
            (String name)   // required
            /property type  // required
            ]
        ...                 // other properties
    >>
]
```

/Enumerations 字典包含每个枚举类型的条目：

```
/enumTypeName                 // Name used in string-based API
    <<
        /enumValue (String name) // required
        ...
    >>
```

## 值类型定义

对于 /parameter type 和 /property type 定义，你可以使用在自己的术语字典中声明的类和枚举类型，可以使用 Photoshop 提供的声明，也可以使用基本值类型。

## 基本值类型

基本值类型如下表所示：

| 名称 | 代码 | 描述 |
| :--- | :--- | :--- |
| typeInteger | 'long' | int32 |
| typeFloat | 'doub' | IEEE 64 位双精度浮点数 |
| typeBoolean | 'bool' | TRUE 或 FALSE。 |
| typeText | 'TEXT' | 任意数量的可读字符块。 |
| typeAlias | 'alis' | Macintosh 文件系统路径。 |
| typePaths | 'Pth ' | Windows 文件系统路径。 |
| typePlatformFilePath | 'alis' 或 'Pth ' | Mac OS 上为 typeAlias，Windows 上为 typePath。 |

## 预定义类类型

Photoshop 提供了许多可在术语字典中使用的预定义类。这些类的一个有用子集如下表所示。在适当的时候使用这些类，但如果有必要，你可以在术语资源中定义新的类。

| 名称 | 代码 | 描述 |
| :--- | :--- | :--- |
| classColor | 'Clr ' | 颜色类的类。 |
| classRGBColor | 'RGBC' | keyRed, keyGreen, keyBlue |
| classCMYKColor | 'CMYC' | keyCyan, keyMagenta, keyYellow, keyBlack。 |
| classUnspecifiedColor | 'UnsC' | 未指定。 |
| classGrayscale | 'Grsc' | keyGray |
| classBookColor | 'BkCl ' | 书籍颜色 |
| classLabColor | 'LbCl ' | keyLuminance, keyA, keyB。 |

## 术语条目的唯一性规则

通常，术语条目的名称在特定类别和范围内必须是唯一的。最好不要不必要地使名称唯一；首选通用术语，并且如果某个事物已有名称，请直接使用它。在考虑术语条目的唯一性时，大小写很重要。

术语条目的唯一性规则是：

- 所有事件名称必须与所有其他事件名称不同。
- 所有类名称必须与所有其他名称不同。
- 所有枚举类型名称必须与所有其他枚举类型名称不同。
- 所有键必须与在同一类或事件中使用的所有其他键不同。
- 所有枚举值必须与在同一枚举类型中的所有其他枚举值不同。
- 一个类、事件、枚举类型、键和枚举值都可以具有相同的名称。

## 术语定义示例

此示例演示了一个新事件的术语定义；该示例使用了 ZStrings。该事件名为 `newAnnot`，接受三个参数：

- `annotType`，一个枚举（`annotType`）
- `at`，一个类（`point`），以及
- `size`，一个类（`annotSizeClass`）。

annotSizeClass 有两个属性：width 和 height，类型均为 floatType。枚举 annotType 有三个值：annotUnknown、annotText 和 annotSound。

```
<terminology><![CDATA[<<<
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

## 脚本常量

本节列出并描述了为 Adobe Photoshop CC 2015 JavaScript 属性和方法定义的枚举。

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **AdjustmentReference** | ABSOLUTE<br>RELATIVE | 解释选择性颜色调整规范的方法：<br><br>`ABSOLUTE` = 占总体的百分比。<br><br>`RELATIVE` = 占现有颜色数量的百分比。<br><br>传递给 `ArtLayer.selectiveColor()`。 |
| **AnchorPosition** | BOTTOMCENTER<br>BOTTOMLEFT<br>BOTTOMRIGHT<br>MIDDLECENTER<br>MIDDLELEFT<br>MIDDLERIGHT<br>TOPCENTER<br>TOPLEFT<br>TOPRIGHT | 变换对象时围绕的点。这是在使用 `ArtLayer`、`LayerSet` 和 `Selection` 中的方法旋转或调整对象大小时，或在使用 `Document.resizeCanvas()` 调整整个画布大小时，不移动的点。 |
| **AntiAlias** | CRISP<br>NONE<br>SHARP<br>SMOOTH<br>STRONG | 通过柔化边缘像素和背景像素之间的颜色过渡来平滑边缘的方法。用于 `TextItem.antiAliasMethod`。 |
| **AutoKernType** | MANUAL<br>METRICS<br>OPTICAL | 字符使用的字距调整类型。用于 `TextItem.autoKerning`。 |
| **BatchDestinationType** | FOLDER<br>NODESTINATION<br>SAVEANDCLOSE | 批处理文件的目标（如果有），在 `Application.batch()` 方法使用的 `BatchOptions` 中指定：<br><br>`FOLDER`：将文件的修改版本保存到新位置（保持原始文件不变）。<br><br>`NODESTINATIONTYPE`：让所有文件保持打开状态。<br><br>`SAVEANDCLOSE`：保存更改并关闭文件。 |

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **BitmapConversionType** | CUSTOMPATTERN, DIFFUSIONDITHER, HALFTHRESHOLD, HALFTONESCREEN, PATTERNDITHER | 指定要转换为位图模式的图像质量。用于 BitmapConversionOptions。 |
| **BitmapHalfToneType** | CROSS, DIAMOND, ELLIPSE, LINE, ROUND, SQUARE | 指定半调网点（油墨沉积）的形状。用于 BitmapConversionOptions。 |
| **BitsPerChannelType** | EIGHT, ONE, SIXTEEN, THIRTYTWO | 每个颜色通道的位数。Document.bitsPerChannel 的值；传递给 Documents.add()。也用于 PDFOpenOptions 和 CameraRAWOpenOptions。 |
| **BlendMode** | COLORBLEND, COLORBURN, COLORDODGE, DARKEN, DIFFERENCE, DISSOLVE, DIVIDE, EXCLUSION, HARDLIGHT, HARDMIX, HUE, LIGHTEN, LINEARBURN, LINEARDODGE, LINEARLIGHT, LUMINOSITY, MULTIPLY, NORMAL, OVERLAY, PASSTHROUGH, PINLIGHT, SATURATION, SCREEN, SOFTLIGHT, SUBTRACT, VIVIDLIGHT | 控制应用滤镜时图像中像素的混合方式。ArtLayer.blendMode 和 LayerSet.blendMode 的值。 |
| **BMPDepthType** | BMP_A1R5G5B5, BMP_A4R4G4B4, BMP_A8R8G8B8, BMP_R5G6B5, BMP_R8G8B8, BMP_X1R5G5B5, BMP_X4R4G4B4, BMP_X8R8G8B8, EIGHT, FOUR, ONE, SIXTEEN, THIRTYTWO, TWENTYFOUR | 每个通道的位数（也称为像素深度或颜色深度）。选择的数字表示 2 的指数。例如，位深为 `EIGHT` 的像素有 2^8，即 256 种可能的颜色值。用于 BMPSaveOptions。 |
| **ByteOrder** | IBM, MACOS | 读取多字节值的平台特定顺序。 |
| **CameraRAWSettingsType** | CAMERA, CUSTOM, SELECTEDIMAGE | 要使用的默认 CameraRaw 设置：相机设置、自定义设置或所选图像的设置。在 CameraRAWOpenOptions 中设置。 |
| **CameraRAWSize** | EXTRALARGE, LARGE, MAXIMUM, MEDIUM, MINIMUM, SMALL | 相机 RAW 尺寸类型选项：`EXTRALARGE=5120 x 4096`，`LARGE=4096 x 2731`，`MAXIMUM=6144 X 4096`，`MEDIUM=3072 x 2048`，`MINIMUM=1536 x 1024`，`SMALL=2048 x 1365`。在 CameraRAWOpenOptions 中设置。 |
| **ChangeMode** | BITMAP, CMYK, GRAYSCALE, INDEXEDCOLOR, LAB, MULTICHANNEL, RGB | 文档的新颜色配置文件或模式，在 Document.changeMode() 中指定。**注意：** 彩色图像在更改为 `BITMAP` 模式之前，必须先更改为 `GRAYSCALE` 模式。 |
| **ChannelType** | COMPONENT, MASKEDAREA, SELECTEDAREA, SPOTCOLOR | 颜色通道的类型：`COMPONENT`：与文档颜色模式相关。`MASKEDAREA`：颜色表示蒙版区域的 Alpha 通道。`SELECTEDAREA`：颜色表示选中区域的 Alpha 通道。`SPOTCOLOR`：用于存储专色的 Alpha 通道。 |
| **ColorBlendMode** | BEHIND, CLEAR, COLOR, COLORBURN, COLORDODGE, DARKEN, DARKERCOLOR, DIFFERENCE, DISSOLVE, EXCLUSION, HARDLIGHT, HARDMIXBLEND, HUE, LIGHTEN, LIGHTERCOLOR, LINEARBURN, LINEARDODGE, LINEARLIGHT, LUMINOSITY, MULTIPLY, NORMAL, OVERLAY, PINLIGHT, SATURATION, SCREEN, SOFTLIGHT, VIVIDLIGHT | 在填充或描边操作中颜色应混合的方式。传递给 `PathItem.fillPath()`、`Selection.fill()`、`Selection.stroke()`。 |
| **ColorModel** | CMYK, GRAYSCALE, HSB, LAB, NONE, RGB | 用于 `SolidColor` 的颜色模型。 |
| **ColorPicker** | ADOBE, APPLE, PLUGIN, WINDOWS | 首选的颜色选择工具，在 `Preferences` 中设置。 |
| **ColorProfileType** | CUSTOM, NONE, WORKING | 用于管理此文档的颜色配置文件类型，在 `Document.colorProfileType` 中设置。 |
| **ColorReductionType** | ADAPTIVE, BLACKWHITE, CUSTOM, GRAYSCALE, MACINTOSH, PERCEPTUAL, RESTRICTIVE, SELECTIVE, WINDOWS | `ExportOptionsSaveForWeb` 的颜色减少算法选项。 |
| **ColorSpaceType** | ADOBERGB, COLORMATCHRGB, PROPHOTORGB, SRGB | 在 `CameraRAWOpenOptions` 中使用的颜色空间类型。 |
| **CopyrightedType** | COPYRIGHTEDWORK, PUBLICDOMAIN, UNMARKED | 文档的版权状态。用于 `DocumentPrintSettings.copyrighted`。 |
| **CreateFields** | DUPLICATION, INTERPOLATION | 用于创建字段的方法。传递给 `ArtLayer.applyDeInterlace()`。 |
| **CropToType** | ARTBOX, BLEEDBOX, BOUNDINGBOX, CROPBOX, MEDIABOX, TRIMBOX | 在 PDF 文档中裁剪页面时使用的样式。在 `PDFOpenOptions.cropPage` 中设置。 |
| **DCSType** | COLORCOMPOSITE, GRAYSCALECOMPOSITE, NOCOMPOSITE | 使用 `DCS1_SaveOptions` 或 `DCS2_SaveOptions` 创建的复合 DCS 文件的类型：`COLORCOMPOSITE`：在 DCS 文件之外创建一个彩色复合文件。`GRAYSCALECOMPOSITE`：在 DCS 文件之外创建一个灰度复合文件。`NOCOMPOSITE`：不创建复合文件。 |
| **DepthMapSource** | IMAGEHIGHLIGHT, LAYERMASK, NONE, TRANSPARENCYCHANNEL | 用于深度贴图的来源。传递给 `ArtLayer.applyLensBlur()`。 |
| **DescValueType** | ALIASTYPE, BOOLEANTYPE, CLASSTYPE, DOUBLETYPE, ENUMERATEDTYPE, INTEGERTYPE, LARGEINTEGERTYPE, LISTTYPE, OBJECTTYPE, RAWTYPE, REFERENCETYPE, STRINGTYPE, UNITDOUBLE | 动作键的值类型，由 `ActionDescriptor.getType()` 和 `ActionList.getType()` 返回。 |
| **DialogModes** | ALL, ERROR, NO | 控制 Photoshop 在运行脚本时显示的对话框类型。 |
| **Direction** | HORIZONTAL, VERTICAL | - 要翻转文档画布的方向，传递给 `Document.flipCanvas()`。- `TextItem.direction` 中文本的方向。- `TextItem.warpDirection` 中文本扭曲的方向。 |



Adobe Photoshop CC 2015 JavaScript 脚本参考 脚本常量 203

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **DisplacementMapType** | STRETCHTOFIT<br>TILE | 描述当图像大小与置换图不匹配时，置换图如何适配图像。传递给 [ArtLayer.applyDisplace()](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| **Dither** | DIFFUSION<br>NOISE<br>NONE<br>PATTERN | 在 [GIFSaveOptions](https://www.adobe.com/devnet/photoshop/scripting.html)、[IndexedConversionOptions](https://www.adobe.com/devnet/photoshop/scripting.html) 和 [ExportOptionsSaveForWeb](https://www.adobe.com/devnet/photoshop/scripting.html) 中使用的仿色类型。 |
| **DocPositionStyle** | PRINTCENTERED<br>USERDEFINED | DocPosition 中使用的定位类型 |
| **DocumentFill** | BACKGROUNDCOLOR<br>TRANSPARENT<br>WHITE | 新文档的填充类型，传递给 [Documents.add()](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| **DocumentMode** | BITMAP<br>CMYK<br>DUOTONE<br>GRAYSCALE<br>INDEXEDCOLOR<br>LAB<br>MULTICHANNEL<br>RGB | 打开文档的颜色模式，即 [Document.mode](https://www.adobe.com/devnet/photoshop/scripting.html)。另请参阅 [Document.changeMode()](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| **EditLogItemsType** | CONCISE<br>DETAILED<br>SESSIONONLY | 历史记录中首选的详细程度，在 [首选项](https://www.adobe.com/devnet/photoshop/scripting.html) 中设置：<br>CONCISE：保存简洁的历史记录日志。<br>DETAILED：保存详细的历史记录日志。<br>SESSIONONLY：仅保存当前会话的历史记录日志。 |
| **ElementPlacement** | INSIDE<br>PLACEATBEGINNING<br>PLACEATEND<br>PLACEBEFORE<br>PLACEAFTER | 对象在图层面板中的位置。<br>**注意**：并非所有值对所有对象类型都有效。请参阅特定对象描述，以确保使用的是有效值。 |
| **EliminateFields** | EVENFIELDS<br>ODDFIELDS | 要消除的场类型。传递给 [ArtLayer.applyDeInterlace()](https://www.adobe.com/devnet/photoshop/scripting.html)。 |
| **ExportType** | ILLUSTRATORPATHS<br>SAVEFORWEB | [Document.exportDocument()](https://www.adobe.com/devnet/photoshop/scripting.html) 的导出类型。<br>这等同于选择 **文件 > 导出 > 路径到 Illustrator**，或 **文件 > 存储为 Web 和设备所用格式**。 |
| **Extension** | LOWERCASE<br>NONE<br>UPPERCASE | 使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 保存时，为文件名添加扩展名的策略和格式。 |

Adobe Photoshop CC 2015 JavaScript 脚本参考 脚本常量 204

| 常量类型 | 值 | 含义 |
|---|---|---|
| **FileNamingType** | `DDMM`<br>`DDMMYY`<br>`DOCUMENTNAMELOWER`<br>`DOCUMENTNAMEMIXED`<br>`DOCUMENTNAMEUPPER`<br>`EXTENSIONLOWER`<br>`EXTENSIONUPPER`<br>`MMDD`<br>`MMDDYY`<br>`SERIALLETTERLOWER`<br>`SERIALLETTERUPPER`<br>`SERIALNUMBER1`<br>`SERIALNUMBER2`<br>`SERIALNUMBER3`<br>`SERIALNUMBER4`<br>`YYDDMM`<br>`YYMMDD`<br>`YYYYMMDD` | 与 [Application.batch()](https://www.indesignjs.com/docs/scripting-scriptui/jsdoc.html#Application.batch) 方法一起使用的 [BatchOptions](https://helpx.adobe.com/photoshop/using/setting-batch-options.html) 的文件命名选项。 |
| **FontPreviewType** | `HUGE`<br>`EXTRALARGE`<br>`LARGE`<br>`MEDIUM`<br>`NONE`<br>`SMALL` | 在文字工具字体菜单中用于字体预览的首选字体大小，在 [首选项](https://helpx.adobe.com/photoshop/using/preference-options.html) 中设置。 |
| **FontSize** | `LARGE`<br>`MEDIUM`<br>`SMALL` | 用于面板和对话框的首选字体大小，在 [首选项](https://helpx.adobe.com/photoshop/using/preference-options.html) 中设置。 |
| **ForcedColors** | `BLACKWHITE`<br>`NONE`<br>`PRIMARIES`<br>`WEB` | 无论使用情况如何，都要包含在颜色表中的颜色类型。用于 [GIFSaveOptions](https://helpx.adobe.com/photoshop/using/saving-gif-images.html) 和 [IndexedConversionOptions](https://helpx.adobe.com/photoshop/using/converting-color-mode-indexed-color.html)。<br><br>`BLACKWHITE`：纯黑和纯白。<br>`NONE`：无<br>`PRIMARIES`：红、绿、蓝、青、洋红、黄、黑和白。<br>`WEB`：216 种 Web 安全颜色。 |
| **FormatOptions** | `OPTIMIZEDBASELINE`<br>`PROGRESSIVE`<br>`STANDARDBASELINE` | 在 [JPEGSaveOptions](https://helpx.adobe.com/photoshop/using/saving-jpeg-images.html) 中保存 JPEG 文件时使用的选项。<br><br>`OPTIMIZEDBASELINE`：优化的颜色和略减小的文件大小。<br>`PROGRESSIVE`：在图像下载时显示一系列逐渐详细的扫描。<br>`STANDARDBASELINE`：大多数 Web 浏览器识别的格式。 |
| **GalleryConstrainType** | `CONSTRAINBOTH`<br>`CONSTRAINHEIGHT`<br>`CONSTRAINWIDTH` | 图像要约束的比例类型。用于 [GalleryImagesOptions](https://helpx.adobe.com/photoshop/using/creating-contact-sheets.html)。 |

## Adobe Photoshop CC 2015 JavaScript 脚本参考 脚本常量 205

| 常量类型 | 值 | 含义 |
|---|---|---|
| **GalleryFontType** | ARIAL, COURIERNEW, HELVETICA, TIMESNEWROMAN | 用于 Web 照片画廊标题和其他文本的字体。用于 GalleryBannerOptions、GalleryImagesOptions 和 GalleryThumbnailOptions。也用于 PicturePackageOptions。 |
| **GallerySecurityTextColorType** | BLACK, CUSTOM, WHITE | 用作防盗威慑措施，显示在画廊图像上的文本颜色。用于 GallerySecurityOptions。 |
| **GallerySecurityTextPositionType** | CENTERED, LOWERLEFT, LOWERRIGHT, UPPERLEFT, UPPERRIGHT | 用作防盗威慑措施，显示在画廊图像上的文本位置。用于 GallerySecurityOptions。也用于 PicturePackageOptions。 |
| **GallerySecurityTextRotateType** | CLOCKWISE45, CLOCKWISE90, COUNTERCLOCKWISE45, COUNTERCLOCKWISE90, ZERO | 用作防盗威慑措施，显示在画廊图像上的文本方向。用于 GallerySecurityOptions。也用于 PicturePackageOptions。 |
| **GallerySecurityType** | CAPTION, COPYRIGHT, CREDIT, CUSTOMTEXT, FILENAME, NONE, TITLE | 用作防盗威慑措施，显示在画廊图像上的文本内容。用于 GallerySecurityOptions。**注意：** 除 CUSTOMTEXT 外，所有类型都从图像的文件信息中提取。 |
| **GalleryThumbSizeType** | CUSTOM, LARGE, MEDIUM, SMALL | Web 照片画廊中缩略图的大小。用于 GalleryThumbnailOptions。 |
| **Geometry** | HEPTAGON, HEXAGON, OCTAGON, PENTAGON, SQUARE, TRIANGLE | 形状的几何选项，例如镜头模糊滤镜中的光圈形状。传递给 ArtLayer.applyLensBlur()。 |
| **GridLineStyle** | DASHED, DOTTED, SOLID | 显示在图像上的非打印网格的首选线条样式，在首选项中设置。 |
| **GridSize** | LARGE, MEDIUM, NONE, SMALL | 网格线间距的首选大小，在首选项中设置。 |

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **GuideLineStyle** | DASHED<br>SOLID | 显示在图像上的非打印参考线的首选线条样式，在 [首选项](Preferences) 中设置。 |
| **IllustratorPathType** | ALLPATHS<br>DOCUMENTBOUNDS<br>NAMEDPATH | 使用 [Document.exportDocument()](Document.exportDocument()) 导出到 Illustrator 文件的路径。 |
| **Intent** | ABSOLUTECOLORIMETRIC<br>PERCEPTUAL<br>RELATIVECOLORIMETRIC<br>SATURATION | 使用 [Document.convertProfile()](Document.convertProfile()) 或 [Document.print()](Document.print()) 从一种颜色空间转换到另一种颜色空间时使用的渲染意图。 |
| **Justification** | CENTER<br>CENTERJUSTIFIED<br>FULLYJUSTIFIED<br>LEFT<br>LEFTJUSTIFIED<br>RIGHT<br>RIGHTJUSTIFIED | 段落文本在边界框内的放置方式。用于 [TextItem.justification](TextItem.justification)。 |
| **Language** | BRAZILIANPORTUGUESE<br>CANADIANFRENCH<br>DANISH<br>DUTCH<br>ENGLISHUK<br>ENGLISHUSA<br>FINNISH<br>FRENCH<br>GERMAN<br>ITALIAN<br>NORWEGIAN<br>NYNORSKNORWEGIAN<br>OLDGERMAN<br>PORTUGUESE<br>SPANISH<br>SWEDISH<br>SWISSGERMAN | 用于文本的语言。用于 [TextItem.language](TextItem.language)。 |
| **LayerCompression** | RLE<br>ZIP | 保存为 TIFF 格式时，图层像素数据的压缩方法。用于 [TiffSaveOptions](TiffSaveOptions)。 |

## 脚本常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| **LayerKind** | `BLACKANDWHITE` `BRIGHTNESSCONTRAST` `CHANNELMIXER` `COLORBALANCE` `CURVES` `EXPOSURE` `GRADIENTFILL` `GRADIENTMAP` `HUESATURATION` `INVERSION` `LEVELS` `NORMAL` `PATTERNFILL` `PHOTOFILTER` `POSTERIZE` `SELECTIVECOLOR` `SMARTOBJECT` `SOLIDFILL` `TEXT` `THRESHOLD` `LAYER3D` `VIBRANCE` `VIDEO` | 图层对象的类型，见 [ArtLayer.kind](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/properties/artlayerprops.html#artlayerprops_kind)。**注意：** 只能从空白图层创建文字图层。 |
| **LensType** | `MOVIEPRIME` `PRIME105` `PRIME35` `ZOOMLENS` | 要使用的镜头类型。传递给 [ArtLayer.applyLensFlare()](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/methods/artlayermethods.html#applylensflare)。 |
| **MagnificationType** | `ACTUALSIZE` `FITPAGE` | 查看图像时使用的缩放类型。用于 [PresentationOptions](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#presentationoptions)。 |
| **MatteType** | `BACKGROUND` `BLACK` `FOREGROUND` `NETSCAPE` `NONE` `SEMIGRAY` `WHITE` | 用于填充与图像透明区域相邻的抗锯齿边缘的颜色。当图像的透明度关闭时，哑光颜色将应用于透明区域。用于 [GIFSaveOptions](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#gifsavemethodoptions)、[IndexedConversionOptions](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#indexedconversionoptions) 和 [JPEGSaveOptions](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#jpegsavemethodoptions)。 |
| **MeasurementRange** | `ALLMEASUREMENTS` `ACTIVEMEASUREMENTS` | 要执行操作的测量范围。传递给 [MeasurementLog](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#measurementlog) 方法。 |
| **MeasurementSource** | `MEASURESELECTION` `MEASURECOUNTTOOL` `MEASURERULERTOOL` | 记录测量的来源。传递给 [Document.recordMeasurements()](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#documentrecordmeasurements)。 |
| **NewDocumentMode** | `BITMAP` `CMYK` `GRAYSCALE` `LAB` `RGB` | 新文档使用的颜色配置文件。传递给 [Documents.add()](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#documentsadd)。也用于 [ContactSheetOptions](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#contactsheetoptions) 和 [PicturePackageOptions](https://www.adobe.com/support/scripting/devscripting/ps/ref/ps_api/DOM/domclasses.html#picturepackageoptions)。 |
| **NoiseDistribution** | `GAUSSIAN` `UNIFORM` | 应用“添加杂色”滤镜时使用的分布方法。传递给 [ArtLayer.applyAddNoise()](https://helpx.adobe.com/photoshop/using/scripting-constants.html)。 |
| **OffsetUndefinedAreas** | `REPEATEDGEPIXELS` `SETTOBACKGROUND` `WRAPAROUND` | 用于填充通过偏移图像或选区留下的空白区域的方法。传递给 [ArtLayer.applyOffset()](https://helpx.adobe.com/photoshop/using/scripting-constants.html)。 |
| **OpenDocumentMode** | `CMYK` `GRAYSCALE` `LAB` `RGB` | 打开 EPS 或 PDF 文档时使用的颜色配置文件。在 [EPSOpenOptions](https://helpx.adobe.com/photoshop/using/scripting-constants.html) 或 [PDFOpenOptions](https://helpx.adobe.com/photoshop/using/scripting-constants.html) 中传递给 `app.open()`。 |
| **OpenDocumentType** | `ALIASPIX` `BMP` `CAMERARAW` `COMPUSERVEGIF` `DICOM` `ELECTRICIMAGE` `EPS` `EPSPICTPREVIEW` `EPSTIFFPREVIEW` `FILMSTRIP` `JPEG` `PCX` `PDF` `PHOTOCD` `PHOTOSHOP` `PHOTOSHOPDCS_1` `PHOTOSHOPDCS_2` `PHOTOSHOPEPS` `PHOTOSHOPPDF` `PICTFILEFORMAT` `PICTRESOURCEFORMAT` `PIXAR` `PNG` `PORTABLEBITMAP` `RAW` `SCITEXCT` `SGIRGB` `SOFTIMAGE` `TARGA` `TIFF` `WAVEFRONTRLA` `WIRELESSBITMAP` | 使用 `app.open()` 打开文档时使用的格式。**注意：** PHOTOCD 已弃用。柯达 PhotoCD 现在可在 Adobe Photoshop CC 2015 安装 DVD 的 Goodies 文件夹中找到。**注意：** DICOM 选项仅适用于扩展版。 |
| **OperatingSystem** | `OS2` `WINDOWS` | [BMPSaveOptions](https://helpx.adobe.com/photoshop/using/scripting-constants.html) 中的目标操作系统。 |
| **Orientation** | `LANDSCAPE` `PORTRAIT` | [PhotoCDOpenOptions](https://helpx.adobe.com/photoshop/using/scripting-constants.html) 的页面方向，在 Photoshop CS3 中已弃用。**注意：** 柯达 PhotoCD 现在可在 Adobe Photoshop CC 2015 安装 DVD 的 Goodies 文件夹中找到。 |
| **OtherPaintingCursors** | `PRECISEOTHER` `STANDARDOTHER` | 以下工具的首选指针：橡皮擦、铅笔、画笔、修复画笔、仿制图章、图案图章、涂抹、模糊、锐化、减淡、加深、海绵。在 [Preferences](Preferences) 中设置。 |
| **PaintingCursors** | `BRUSHSIZE` `PRECISE` `STANDARD` | 以下工具的首选指针：选框、套索、多边形套索、魔棒、裁剪、切片、修补、吸管、钢笔、渐变、直线、油漆桶、磁性套索、磁性钢笔、自由钢笔、测量、颜色取样器。在 [Preferences](Preferences) 中设置。 |
| **PaletteType** | `EXACT` `LOCALADAPTIVE` `LOCALPERCEPTUAL` `LOCALSELECTIVE` `MACOSPALETTE` `MASTERADAPTIVE` `MASTERPERCEPTUAL` `MASTERSELECTIVE` `PREVIOUSPALETTE` `UNIFORM` `WEBPALETTE` `WINDOWSPALETTE` | 在 [GIFSaveOptions](GIFSaveOptions) 和 [IndexedConversionOptions](IndexedConversionOptions) 中使用的调色板类型。 |
| **PathKind** | `CLIPPINGPATH` `NORMALPATH` `TEXTMASK` `VECTORMASK` `WORKPATH` | [PathItem](PathItem) 的类型。 |
| **PDFCompatibility** | `PDF13` `PDF14` `PDF15` `PDF16` `PDF17` | 使文档兼容的 PDF 版本。用于 [PDFSaveOptions](PDFSaveOptions)。 |
| **PDFEncoding** | `JPEG` `JPEG2000HIGH` `JPEG2000LOSSLESS` `JPEG2000LOW` `JPEG2000MED` `JPEG2000MEDHIGH` `JPEG2000MEDLOW` `JPEGHIGH` `JPEGLOW` `JPEGMED` `JPEGMEDHIGH` `JPEGMEDLOW` `NONE` `PDFZIP` `PDFZIP4BIT` | 将文档保存为 PDF 格式时使用的压缩类型。用于 [PDFSaveOptions](PDFSaveOptions)。 |
| **PDFResample** | `NONE` `PDFAVERAGE` `PDFBICUBIC` `PDFSUBSAMPLE` | 要使用的向下采样方法。用于 [PDFSaveOptions](PDFSaveOptions)。 |
| **PDFStandard** | `NONE` `PDFX1A2001` `PDFX1A2003` `PDFX32002` `PDFX32003` `PDFX42008` | 使文档兼容的 PDF 标准。用于 [PDFSaveOptions](PDFSaveOptions)。 |
| **PhotoCDColorSpace** | `LAB16` `LAB8` `RGB16` `RGB8` | [PhotoCDOpenOptions](PhotoCDOpenOptions) 的颜色空间，在 Photoshop CS3 中已弃用。**注意：** 柯达 PhotoCD 现在可在 Adobe Photoshop CC 2015 安装 DVD 的 Goodies 文件夹中找到。 |
| **PhotoCDSize** | `EXTRALARGE` `LARGE` `MAXIMUM` `MEDIUM` `MINIMUM` `SMALL` | [PhotoCDOpenOptions](PhotoCDOpenOptions) 中图像的像素尺寸，在 Photoshop CS3 中已弃用。EXTRALARGE = 1024x1536，LARGE = 512x768，MAXIMUM = 2048x3072，MEDIUM = 256x384，MINIMUM = 64x96，SMALL = 128x192。**注意：** 柯达 PhotoCD 现在可在 Adobe Photoshop CC 2015 安装 DVD 的 Goodies 文件夹中找到。 |
| **PICTBitsPerPixel** | `EIGHT` `FOUR` `SIXTEEN` `THIRTYTWO` `TWO` | 压缩 PICT 文件时使用的每像素位数。用于 [PICTFileSaveOptions](PICTFileSaveOptions) 和 [PICTResourceSaveOptions](PICTResourceSaveOptions)。**注意：** 对于 RGB 图像，使用 16 或 32；对于位图和灰度图像，使用 2、4 或 8。 |
| **PICTCompression** | `JPEGHIGHPICT` `JPEGLOWPICT` `JPEGMAXIMUMPICT` `JPEGMEDIUMPICT` `NONE` | 将图像保存为 PICT 文件时使用的压缩类型。用于 [PICTFileSaveOptions](PICTFileSaveOptions) 和 [PICTResourceSaveOptions](PICTResourceSaveOptions)。 |
| **PicturePackageTextType** | `CAPTION` `COPYRIGHT` `CREDIT` `FILENAME` `NONE` `ORIGIN` `USER` | Picture Package 中文本的功能或含义。用于 [PicturePackageOptions](PicturePackageOptions)。 |



# Adobe Photoshop CC 2015

JavaScript 脚本参考

脚本常量

| 常量类型 | 值 | 含义 |
| --- | --- | --- |
| **PointKind** | `CORNERPOINT`<br>`SMOOTHPOINT` | `PathPoint` 在 `PathItem` 中所扮演的角色。 |
| **PointType** | `POSTSCRIPT`<br>`TRADITIONAL` | 用于字体点数的首选测量单位，在 `Preferences.pointSize` 中设置：<br>`POSTSCRIPT` = 72 点/英寸。<br>`TRADITIONAL` = 72.27 点/英寸。 |
| **PolarConversionType** | `POLARTORECTANGULAR`<br>`RECTANGULARTOPOLAR` | 要使用的极坐标变形方法。传递给 `ArtLayer.applyPolarCoordinates()`。 |
| **Preview** | `EIGHTBITTIFF`<br>`MACOSEIGHTBIT`<br>`MACOSJPEG`<br>`MACOSMONOCHROME`<br>`MONOCHROMETIFF`<br>`NONE` | 在目标应用程序中用作低分辨率预览的图像类型。<br>用于 `DCS1_SaveOptions`、`DCS2_SaveOptions` 和 `EPSSaveOptions`。 |
| **PrintColorHandling** | `PRINTERMANAGED`<br>`PHOTOSHOPMANAGED`<br>`SEPARATIONS` | 用于 ColorHandling 的颜色处理类型。 |
| **PurgeTarget** | `ALLCACHES`<br>`CLIPBOARDCACHE`<br>`HISTORYCACHES`<br>`UNDOCACHES` | `Application.purge()` 操作中要清除的目标缓存。 |
| **QueryStateType** | `ALWAYS`<br>`ASK`<br>`NEVER` | 打开 PSD 文件时，检查是否最大化兼容性的首选策略，在 `Preferences.maximizeCompatibility` 中设置。 |
| **RadialBlurMethod** | `SPIN`<br>`ZOOM` | 要使用的模糊方法。传递给 `ArtLayer.applyRadialBlur()`。 |
| **RadialBlurQuality** | `BEST`<br>`DRAFT`<br>`GOOD` | 模糊图像的平滑度或颗粒度。传递给 `ArtLayer.applyRadialBlur()`。 |
| **RasterizeType** | `ENTIRELAYER`<br>`FILLCONTENT`<br>`LAYERCLIPPINGPATH`<br>`LINKEDLAYERS`<br>`SHAPE`<br>`TEXTCONTENTS` | 使用 `ArtLayer.rasterize()` 栅格化的图层元素。 |
| **ReferenceFormType** | `CLASSTYPE`<br>`ENUMERATED`<br>`IDENTIFIER`<br>`INDEX`<br>`NAME`<br>`OFFSET`<br>`PROPERTY` | `ActionReference` 对象的类型，由 `getForm()` 返回。 |
| **ResampleMethod** | AUTOMATIC<br>BICUBIC<br>BICUBICAUTOMATIC<br>BICUBICSHARPER<br>BICUBICSMOOTHER<br>BILINEAR<br>NEARESTNEIGHBOR<br>NONE<br>PRESERVEDetails | 用于图像插值的方法。传递给 [Document.resizeImage()](https://example.com)，并用作 [Preferences.interpolation](https://example.com) 的值。 |
| **RippleSize** | LARGE<br>MEDIUM<br SMALL | 要使用的波纹大小。传递给 [ArtLayer.applyRipple()](https://example.com)。 |
| **SaveBehavior** | ALWAYSSAVE<br>ASKWHENSAVING<br>NEVERSAVE | 应用程序保存文档时的首选行为。参见 [Preferences.appendExtension](https://example.com) 和 [imagePreviews](https://example.com)。 |
| **SaveDocumentType** | ALIASPIX<br>BMP<br>COMPUVEGIF<br>ELECTRICIMAGE<br>JPEG<br>PCX<br>PHOTOSHOP<br>PHOTOSHOPDCS_1<br>PHOTOSHOPDCS_2<br>PHOTOSHOPEPS<br>PHOTOSHOPPDF<br>PICTFILEFORMAT<br>PICTRESOURCEFORMAT<br>PIXAR<br>PNG<br>PORTABLEBITMAP<br>RAW<br>SCITEXCT<br>SGIRGB<br>SOFTIMAGE<br>TARGA<br>TIFF<br>WAVEFRONTRLA<br>WIRELESSBITMAP | 使用 [Document.exportDocument()](https://example.com) 导出时保存文档的格式。传递给 [ExportOptionsSaveForWeb.format](https://example.com) 以指定要写入的文件类型。导出仅支持以下格式：COMPUSERVEGIF、JPEG、PNG-8、PNG-24 和 BMP。 |
| **SaveEncoding** | ASCII<br>BINARY<br>JPEHIGH<br>JPEGLOW<br>JPEGMAXIMUM<br>JPEGMEDIUM | 使用 [Document.saveAs()](https://example.com) 将文件保存为 DCS 或 EPS 时使用的编码类型。 |
| **SaveLogItemsType** | LOGFILE<br>LOGFILEANDMETADATA<br>METADATA | 历史记录日志数据的首选存储位置，在 [Preferences.saveLogItems](https://example.com) 中设置。 |
| **SaveOptions** | DONOTSAVECHANGES<br>PROMPTTOSAVECHANGES<br>SAVECHANGES | 使用 [Document.close()](https://example.com) 关闭文档时的策略。 |
| **SelectionType** | DIMINISH<br>EXTEND<br>INTERSECT<br>REPLACE | 当选区已存在时的选择行为：<br><br>`DIMINISH`：从已选区域中移除选区。<br><br>`EXTEND`：将选区添加到已选区域。<br><br>`INTERSECT`：使选区仅包含新选区与已选区域的交集区域。<br><br>`REPLACE`：替换选区。<br><br>用于 `PathItem.makeSelection()`、`Selection.load()`、`Selection.select()` 和 `Selection.store()`。 |
| **ShapeOperation** | SHAPEADD<br>SHAPEINTERSECT<br>SHAPESUBTRACT<br>SHAPEXOR | 如果目标路径已有选区，如何组合形状。<br><br>为 `SubPathInfo.operation` 设置，并存储在结果 `SubPathItem` 中。 |
| **SmartBlurMode** | EDGEONLY<br>NORMAL<br>OVERLAYEDGE | 要使用的智能模糊方法：<br><br>`EDGEONLY`、`OVERLAYEDGES`：仅对颜色过渡的边缘应用模糊。<br><br>`NORMAL`：对整个图像应用模糊。<br><br>传递给 `ArtLayer.applySmartBlur()`。 |
| **SmartBlurQuality** | HIGH<br>LOW<br>MEDIUM | 要使用的模糊质量。传递给 `ArtLayer.applySmartBlur()`。 |
| **SourceTypeSpaceType** | DOCUMENT<br>PROOF | 使用 `Document.print()` 打印时源的色彩空间。 |
| **SpherizeMode** | HORIZONTAL<br>NORMAL<br>VERTICAL | 用于变形的曲线（或拉伸形状）。传递给 `ArtLayer.applySpherize()`。 |
| **StrikeThruType** | STRIKEBOX<br>STRIKEHEIGHT<br>STRIKEOFF | 文本中要使用的删除线样式。用于 `TextItem.strikeThru`。 |
| **StrokeLocation** | CENTER<br>INSIDE<br>OUTSIDE | 路径或选区边界描边的位置。传递给 `Selection.stroke()`。 |
| **TargaBitsPerPixels** | SIXTEEN<br>THIRTYTWO<br>TWENTYFOUR | 以 Targa 格式保存图像时使用的分辨率。用于 `TargaSaveOptions`。 |
| **TextCase** | ALLCAPS, NORMAL, SMALLCAPS | 文本中要使用的大写字母样式。用于 `TextItem.capitalization`。 |
| **TextComposer** | ADOBEEVERYLINE, ADOBESINGLELINE | 用于优化指定的连字和对齐选项的组合方法。用于 `TextItem.textComposer`。 |
| **TextType** | PARAGRAPHTEXT, POINTTEXT | 文本类型，用于 `TextItem.kind`。PARAGRAPHTEXT：在边界框内换行的文本。POINTTEXT：不换行的文本。 |
| **TextureType** | BLOCKS, CANVAS, FILE, FROSTED, TINYLENS | 为纹理化器或玻璃滤镜加载的纹理或玻璃表面图像类型。传递给 `ArtLayer.applyGlassEffect()`。 |
| **TIFFEncoding** | JPEG, NONE, TIFFLZW, TIFFZIP | 用于 TIFF 文件的压缩类型。用于 `TiffSaveOptions`。 |
| **ToolType** | ARTHISTORYBRUSH, BACKGROUNDERASER, BLUR, BRUSH, BURN, CLONESTAMP, COLORREPLACEMENTTOOL, DODGE, ERASER, HEALINGBRUSH, HISTORYBRUSH, PATTERNSTAMP, PENCIL, SHARPEN, SMUDGE, SPONGE | 与 `PathItem.strokePath()` 一起使用的工具。 |
| **TransitionType** | BLINDSHORIZONTAL, BLINDSVERTICAL, BOXIN, BOXOUT, DISSOLVE, GLITTERDOWN, GLITTERRIGHT, GLITTERRIGHTDOWN, NONE, RANDOM, SPLITHORIZONTALIN, SPLITHORIZONTALOUT, SPLITVERTICALIN, SPLITVERTICALOUT, WIPEDOWN, WIPELEFT, WIPERIGHT, WIPEUP | PDF 演示文稿中从一个图像过渡到下一个图像的方法。用于 `PresentationOptions`。 |
| **TrimType** | BOTTOMRIGHT<br>TOPLEFT<br>TRANSPARENT | 要修剪的图像周围像素的类型，传递给 [Document.trim()](#)。<br><br>BOTTOMRIGHT = 右下角像素颜色。<br><br>TOPLEFT = 左上角像素颜色。 |
| **TypeUnits** | MM<br>PIXELS<br>POINTS | 文本字符测量的首选单位，在 [Preferences](#) 中设置。 |
| **UndefinedAreas** | REPEATEDGEPIXELS<br>WRAPAROUND | 处理应用“扭曲”类别滤镜后图像中未变形区域或空白区域的方法。传递给 [ArtLayer.applyDisplace()](#)、[applyShear()](#)、[applyWave()](#)。 |
| **UnderlineType** | UNDERLINELEFT<br>UNDERLINEOFF<br>UNDERLINERIGHT | 文本下划线的位置。用于 [TextItem.underline](#)。<br><br>**注意：** UNDERLINELEFT 和 UNDERLINERIGHT 仅在 direction = Direction.VERTICAL 时有效。 |
| **Units** | CM<br>INCHES<br>MM<br>PERCENT<br>PICAS<br>PIXELS<br>POINTS | 字体和标尺增量的首选测量单位，在 [Preferences.rulerUnits](#) 中设置。 |
| **Urgency** | FOUR<br>HIGH<br>LOW<br>NONE<br>NORMAL<br>SEVEN<br>SIX<br>THREE<br>TWO | 文档的编辑紧急状态，在 [DocumentPrintSettings.urgency](#) 中设置。 |
| **WarpStyle** | ARC<br>ARCH<br>ARCLOWER<br>ARCUPPER<br>BULGE<br>FISH<br>FISHEYE<br>FLAG<br>INFLATE<br>NONE<br>RISE<br>SHELLLOWER<br>SHELLUPPER<br>SQUEEZE<br>TWIST<br>WAVE | 文本要使用的变形样式。用于 [TextItem.warpStyle](#)。 |



| 常量类型 | 值 | 含义 |
|---|---|---|
| WaveType | SINE<br>SQUARE<br>TRIANGULAR | 要使用的波形类型。传递给 ArtLayer.applyWave。 |
| WhiteBalanceType | ASSHOT<br>AUTO<br>CLOUDY<br>CUSTOM<br>DAYLIGHT<br>FLASH<br>FLUORESCENT<br>SHADE<br>TUNGSTEN | 影响色彩平衡的光照条件。在 CameraRAWOpenOptions 中设置。 |
| ZigZagType | AROUNDCENTER<br>OUTFROMCENTER<br>PONDRIPPLES | 要使用的锯齿形方法。传递给 ArtLayer.applyZigZag。 |

## 附录 A：事件 ID 代码

下表列出了可与 `notifier` 对象一起使用的事件及其四个字符的 ID 代码或字符串标识符。

**注意：请勿在代码中的四个字符 ID 中包含单引号 ( ' )。** 单引号仅在此表中用于说明不含四个字母的代码中必需空格的位置。但是，长度超过四个字符的字符串标识符在代码中需要使用双引号。

**提示：** 如果在此表中找不到要用于通知的事件，您可以使用 ScriptListener 来确定事件 ID 代码。请参阅 *Photoshop CC 2015 脚本指南* 中“动作管理器”章节的 ScriptListener 文档。

| 事件 | 4 字符 ID 或字符串 |
|---|---|
| 3DTransform | ' TdT ' |
| Average | 'Avrg' |
| ApplyStyle | 'ASty' |
| Assert | 'Asrt' |
| AccentedEdges | 'AccE' |
| Add | 'Add  ' |
| AddNoise | 'AdNs' |
| AddTo | 'AddT' |
| Align | 'Algn' |
| All | 'All  ' |
| AngledStrokes | 'AngS' |
| ApplyImage | 'AppI' |
| BasRelief | 'BsRl' |
| Batch | 'Btch' |
| BatchFromDroplet | 'BtcF' |
| Blur | 'Blr  ' |
| BlurMore | 'BlrM' |
| Border | 'Brdr' |
| Brightness | 'BrgC' |
| CanvasSize | 'CnvS' |
| ChalkCharcoal | 'ChlC' |
| ChannelMixer | 'ChnM' |
| Charcoal | 'Chrc' |
| Chrome | 'Chrm' |
| Clear | 'Cler' |
| Close | 'Cls ' |
| Clouds | 'Clds' |
| ColorBalance | 'ClrB' |
| ColorHalftone | 'ClrH' |
| ColorRange | 'ClrR' |
| ColoredPencil | 'ClrP' |
| ContactSheet | "0B71D221-F8CE-11d2-B21B-0008C75B322C" |
| ConteCrayon | 'CntC' |
| Contract | 'Cntc' |
| ConvertMode | 'CnvM' |
| Copy | 'copy' |
| CopyEffects | 'CpFX' |
| CopyMerged | 'CpyM' |
| CopyToLayer | 'CpTL' |
| Craquelure | 'Crql' |
| CreateDroplet | 'CrtD' |
| Crop | 'Crop' |
| Crosshatch | 'Crsh' |
| Crystallize | 'Crst' |
| Curves | 'Crvs' |
| Custom | 'Cstm' |
| Cut | 'cut ' |
| CutToLayer | 'CtTL' |
| Cutout | 'Ct  ' |
| DarkStrokes | 'DrkS' |
| DeInterlace | 'Dntr' |
| DefinePattern | 'DfnP' |
| Defringe | 'Dfrg' |
| Delete | 'Dlt ' |
| Desaturate | 'Dstt' |
| Deselect | 'Dslc' |
| Despeckle | 'Dspc' |
| DifferenceClouds | 'DrfC' |
| Diffuse | 'Dfs ' |
| DiffuseGlow | 'DfsG' |
| DisableLayerFX | 'dlfx' |
| Displace | 'Dspl' |
| Distribute | 'Dstr' |
| Draw | 'Draw' |
| DryBrush | 'DryB' |
| Duplicate | 'Dplc' |
| DustAndScratches | 'DstS' |
| Emboss | 'Embs' |
| Equalize | 'Eqlz' |
| Exchange | 'Exch' |
| Expand | 'Expn' |
| Export | 'Expr' |
| Jumpto | 'Jpto' |
| ExportTransparentImage | "02879e00-cb66-11d1-bc43-0060b0a13dc4" |
| Extrude | 'Extr' |
| Facet | 'Fct ' |
| Fade | 'Fade' |
| Feather | 'Fthr' |
| Fibers | 'Fbrs' |
| Fill | 'Fl  ' |
| FilmGrain | 'FlmG' |
| Filter | 'Fltr' |
| FindEdges | 'FndE' |
| FitImage | "3caa3434-cb67-11d1-bc43-0060b0a13dc4" |
| FlattenImage | 'FltI' |
| Flip | 'Flip' |
| Fragment | 'Frgm' |
| Fresco | 'Frsc' |
| GaussianBlur | 'GsnB' |
| Get | 'getd' |
| Glass | 'Gls ' |
| GlowingEdges | 'GlwE' |
| Gradient | 'Grdn' |
| GradientMap | 'GrMp' |
| Grain | 'Grn ' |
| GraphicPen | 'GraP' |
| Group | 'GrpL' |
| Grow | 'Grow' |
| HalftoneScreen | 'HlfS' |
| Hide | 'Hd   ' |
| HighPass | 'HghP' |
| HSBHSL | 'HsbP' |
| HueSaturation | 'HStr' |
| ImageSize | 'ImgS' |
| Import | 'Impr' |
| InkOutlines | 'InkO' |
| Intersect | 'Intr' |
| IntersectWith | 'IntW' |
| Inverse | 'Invs' |
| Invert | 'Invr' |
| LensFlare | 'LnsF' |
| Levels | 'Lvls' |
| LightingEffects | 'LghE' |
| Link | 'Lnk ' |
| Make | 'Mk   ' |
| Maximum | 'Mxm ' |
| Median | 'Mdn ' |
| MergeLayers | 'Mrg2' |
| MergeLayersOld | 'MrgL' |
| MergeSpotChannel | 'MSpt' |
| MergeVisible | 'MrgV' |
| Mezzotint | 'Mztn' |
| Minimum | 'Mnm ' |
| ModeChange | "8cba8cd6-cb66-11d1-bc43-0060b0a13dc4" |
| Mosaic | 'Msc ' |
| Mosaic_PLUGIN | 'MscT' |
| MotionBlur | 'MtnB' |
| Move | 'move' |
| NTSCColors | 'NTSC' |
| NeonGlow | 'NGlw' |
| Next | 'Nxt ' |
| NotePaper | 'NtPr' |
| Notify | 'Ntfy' |
| Null | typeNull |
| OceanRipple | 'OcnR' |
| Offset | 'Ofst' |
| Open | 'Opn ' |
| Paint | 'Pnt ' |
| PaintDaubs | 'PntD' |
| PaletteKnife | 'PltK' |
| Paste | 'past' |
| PasteEffects | 'PaFX' |
| PasteInto | 'PstI' |
| PasteOutside | 'PstO' |
| Patchwork | 'Ptch' |
| Photocopy | 'Phtc' |
| PicturePackage | "4C1ABF40-DD82-11d2-B20F-0008C75B322C" |
| Pinch | 'Pnch' |
| Place | 'Plc ' |
| Plaster | 'Plst' |
| PlasticWrap | 'PlsW' |
| Play | 'Ply ' |
| Pointillize | 'Pntl' |
| Polar | 'Plr ' |
| PosterEdges | 'PstE' |
| Posterize | 'Pstr' |
| Previous | 'Prvs' |
| Print | 'Prnt' |
| ProfileToProfile | 'PrfT' |
| Purge | 'Prge' |
| Quit | 'quit' |
| RadialBlur | 'RdlB' |
| Rasterize | 'Rstr' |
| RasterizeTypeSheet | 'RstT' |
| RemoveBlackMatte | 'RmvB' |
| RemoveLayerMask | 'RmvL' |
| RemoveWhiteMatte | 'RmvW' |
| Rename | 'Rnm ' |
| ReplaceColor | 'RplC' |
| Reset | 'Rset' |
| ResizeImage | "1333cf0c-cb67-11d1-bc43-0060b0a13dc4" |
| Reticulation | 'Rtcl' |
| Revert | 'Rvrt' |
| Ripple | 'Rple' |
| Rotate | 'Rtte' |
| RoughPastels | 'RghP' |
| Save | 'save' |
| Select | 'slct' |
| SelectiveColor | 'SlcC' |
| Set | 'setd' |
| SharpenEdges | 'ShrE' |
| Sharpen | 'Shrp' |
| SharpenMore | 'ShrM' |
| Shear | 'Shr ' |
| Show | 'Shw ' |
| Similar | 'Smlr' |
| SmartBlur | 'SmrB' |
| Smooth | 'Smth' |
| SmudgeStick | 'SmdS' |
| Solarize | 'Slrz' |
| Spatter | 'Spt ' |
| Spherize | 'Sphr' |
| SplitChannels | 'SplC' |
| Sponge | 'Spng' |
| SprayedStrokes | 'SprS' |
| StainedGlass | 'StnG' |
| Stamp | 'Stmp' |
| Stop | 'Stop' |
| Stroke | 'Strk' |
| Subtract | 'Sbtr' |
| SubtractFrom | 'SbtF' |
| Sumie | 'Smie' |
| TakeMergedSnapshot | 'TkMr' |
| TakeSnapshot | 'TkSn' |
| TextureFill | 'TxtF' |
| Texturizer | 'Txtz' |
| Threshold | 'Thrs' |
| Tiles | 'Tls ' |
| TornEdges | 'TrnE' |
| TraceContour | 'TrcC' |
| Transform | 'Trnf' |
| Trap | 'Trap' |
| Twirl | 'Twrl' |
| Underpainting | 'Undr' |
| Undo | 'undo' |
| Ungroup | 'Ungr' |
| Unlink | 'Unlk' |
| UnsharpMask | 'UnsM' |
| Variations | 'Vrtn' |
| Wait | 'Wait' |
| WaterPaper | 'WtrP' |
| Watercolor | 'Wtrc' |
| Wave | 'Wave' |
| Wind | 'Wnd  ' |
| ZigZag | 'ZgZg' |
| BackLight | 'BacL' |
| FillFlash | 'FllE' |
| ColorCast | 'ColE' |

## 索引

### A

- 动作管理器 194
- 动作
    - 命令列表 40
    - 描述 43
    - 描述符 37
    - 播放 47
- 活动文档 45
- activePrinter 97
- 添加杂色滤镜
- 调整
    - 亮度 56
    - 颜色 198
    - 色彩平衡 56, 62
    - 对比度 56, 60
    - 曲线 56
    - 高光 63
    - 色阶 56, 60
    - 阴影 63
    - 色温 62
- Adobe Illustrator，将路径导出到 106
- Alpha 通道
    - 定义 73
    - 来自透明度 (TIFF 文档) 187
    - 不透明度 73
    - 保存
        - 在 BMP 文档中 70
        - 在 PDF 文档中 149
        - 在 PICT 文档中 154
        - 在 PICT 资源中 155
        - 在 Pixar 文档中 157
        - 在 PSD 文档中 153
        - 在 RAW 文档中 165
        - 在 SGIRGB 文档中 172
        - 在 Targa 文档中 177
        - 在 TIFF 文档中 187
- 锚点
    - 添加 144
- 注释，导入 93
- 抗锯齿
    - 文本 180
- 应用程序
    - 激活 47
    - 检查功能是否启用 49
    - 默认设置 159
    - 位置 46
    - 首选项 159
- 图层，参见图层
- 亚洲文本 161
- 作者 100
- 自动字距调整 180, 198
- 自动行距 185
- 自动间距，联系表 83
- 可用内存 46
- 平均滤镜 56

### B

- 背景颜色
    - 应用程序 45
    - 画廊 111
- 背景图层 54
- backgroundColor 97
- 基线偏移 180
- 批处理命令 47
- 批处理
    - 目标文件夹 67, 198
    - 指定选项 67
- 嘟嘟声 159
- 位图文档
    - 转换为 199
    - 位深度类型 199
    - 半调类型 199
    - 打开 208
    - 保存 70
- 位图图像
    - 参见位图文档
- 黑白图像 63
- bleedWidth 97
- 混合模式
    - 图层组 130
    - 图层 54
- 模糊滤镜 56
- 模糊滤镜
    - 平均 56
    - 进一步模糊 56
    - 高斯模糊 57
    - 镜头模糊 58
    - 动感模糊 59
    - 径向模糊 59
    - 特殊模糊 60
- 进一步模糊滤镜 56
- BMP 文档
    - 参见位图文档
- 亮度 56
    - 调整 56
    - 均化 61
- 构建版本 45

### C

- 缓存
    - 图像 160
    - 清除 50
- Camera Raw 文档
    - 打开 71
    - 设置 200
    - 大小选项 200



# 画布
- 翻转 93
- 调整大小 93

画布，定义 89

说明文字 97

# 说明文字
- 联系表 83
- 文档 100
- 画廊图像 112
- 画廊缩略图 116
- 图像 100

centerCropMarks 97

changeProgressText 47

# 通道
- 激活 89
- 添加 75
- 调整 56
- Alpha 参见 Alpha 通道
- 创建 75
- 删除 73
- 以彩色显示 159
- 复制 73
- 可见化 73
- 合并 73
- 混合 62
- 分离 94
- 专色 参见专色通道
- 类型 73

# 裁剪路径
- 从路径创建 140
- 从文字创建 186

云彩滤镜 56

CMYKColor 80

色彩平衡，调整 62

拾色器 159

# 颜色配置文件
- 更改 92
- 确定类型 90
- 命名 89

颜色配置文件，参见具体文档格式

# 颜色取样器
- 添加 82
- 创建 82
- 移动 81
- 移除 81

colorBars 97

colorHandling 97

# 颜色
- 活动链接 111
- 调整 198
- 平衡 56
- 通道 73
- CMYK 80
- 自定义设置 114
- 在画廊中 111
- 反相 61
- 修改 63
- 无 136
- 保留（仅限 GIF） 117
- 减少 107

设置 45

纯色对象 173

测试是否相等 173

已访问链接 111

注释，图层复合 127

兼容性，最大化 160

# 复合通道
- 色彩平衡 56
- 定义 73
- 列出 89
- 参见复合通道

复合通道 73

- 参见复合通道

# Compuserve GIF 文档
- 打开 208
- 保存 117

# 联系表
- 说明文字 83
- 列 83
- 尺寸 83
- 制作 49
- 行 83

# 对比度
- 调整 56
- 自动调整 60
- 相机原始设置 71
- 中间调 63

副本 97

版权信息 100

cornerCropMarks 97

# 计数项目
- 添加 85
- 创建 85
- 移除 84

裁剪 92

当前工具名称 45

光标 161

曲线，调整 56

自定义滤镜 56

# D

DCS 1 文档，保存 86

去隔行滤镜 57

去饱和度 61

去斑滤镜 57

# 对话框
- 显示 45

分层云彩滤镜 57

扩散亮光滤镜 57

置换滤镜 57

# 扭曲滤镜
- 扩散亮光 57
- 置换 57
- 玻璃效果 57
- 海洋波纹 59
- 挤压 59
- 极坐标 59
- 水波 59
- 切变 60

# Adobe Photoshop CC 2015
JavaScript 脚本参考

索引 227

- 球面化 60
- 旋转扭曲 60
- 波浪 60
- 水波纹 60

doAction 47

文档格式，参见具体文档格式

DocumentPrintSettings 97

文档 89
- 激活 45
- 添加 103
- 关闭 91
- 代码示例 95
- 颜色配置文件 89
- 颜色取样器 89
- 计数项目 90
- 计数对象 92
- 裁剪 36, 92
- 尺寸 89
- 复制 36, 92
- 导出 93
- 信息 100
- 加载 49
- 受管理 90
- 测量比例 90
- 元数据 90, 100
- 使用 Photoshop 对话框打开 50
- 打开 50
- 为 Web 优化 107
- 打印 93
- 调整大小 93
- 分辨率 91
- 保存 93, 94
- 挂起历史记录 94
- 陷印（CMYK） 94
- 修剪 95

doForcedProgress 47

doProgress 48

doProgressSegmentTask 48

doProgressTask 48

蒙尘与划痕滤镜 57

ExportOptionsIllustrator 106

ExportOptionsSaveForWeb 107

# F

文件扩展名
- 格式 162
- 包含 159
- 脚本文件 32

文件元数据 100

文件
- 合并 49

文件类型
- macOS 46
- Windows 47

填充
- 路径 139
- 选区 168

滤镜，参见具体滤镜名称

翻转 97

Folder 对象 32

字体
- 检测 45
- 确定系列 178
- 确定样式 178

格式，参见具体文档格式

# E

启用信息
- 常量 192
- 语法 191
- 运算符优先级 192
- 变量 193

EPSSaveOptions 105

色调均化 61

事件 ID
- 使用 ScriptListener 查找 217

事件管理器 46

执行脚本 33

exif 100

导出
- 文档 93
- 路径 106
- 到 Illustrator 106
- 到 Web 107

# G

画廊 114
- 背景颜色 111
- 横幅 110
- 说明文字 112
- 颜色选项 111
- 署名 112
- 尺寸 112
- 文件名 112
- 链接颜色 111
- 制作 47, 49
- 元数据 114
- 摄影师 110
- 安全文本 115
- 缩略图图像 116

GalleryBannerOptions 110

GalleryCustomColorOptions 111

GalleryImagesOptions 112, 113

GalleryOptions 114

GallerySecurityOptions 115

GalleryThumbnailOptions 116

高斯模糊滤镜 57

GIF 文档
- 参见 Compuserve GIF 文档

GIFSaveOptions 117

玻璃效果滤镜 57

字形缩放 180–183

GrayColor 118

网格 160

编组图层 54

参考线 160

# JavaScript 脚本参考
# Adobe Photoshop CC 2015

索引 228

# H

- 半调网屏 69
- 悬挂标点 181
- 校样 97
- 高反差保留滤镜 57
- 高光
  - 调整 63
  - 色彩平衡 56
- 直方图
  - 通道 73
- 历史记录日志 162
- 历史记录状态
  - 激活 89
  - 允许非线性 160
  - 默认数量 161
  - 快照 121
  - 挂起 94
- HSBColor 123
- 连字 182

# I

- ID
  - 获取 37
  - PICT 资源 155
  - 属性 43
  - 运行时 47
  - 运行时转字符串 51
  - 字符串转运行时 51
  - 字符串转类型 51
  - 类型转字符 51
- Illustrator
  - 参见 Adobe Illustrator
- 图像
  - 调整大小 94
- 图像金字塔 187
- 图像
  - 位图 69
  - 黑白 63
  - 缓存 160
  - 说明文字 112
  - 定义 89
  - 去饱和度 61
  - 色调均化 61
  - 文件类型 46
  - 来自分离通道 94
  - 反相颜色 61
  - 预览 160
  - 金字塔 187
  - 调整大小 93
  - 在画廊中调整大小 113
  - 缩略图 116
- 索引颜色模型 124
- IndexedConversionOptions 124
- 具体文档格式示例 94
- 安装脚本 33
- 意图 97
- 插值 97
- 插值 160

# J

- JavaScript
  - 支持的功能 32
- JavaScript 资源
  - 启用信息语法 191
  - javascriptresource 语法 190
  - javascriptresource 标签 190
- JPEG
  - 质量 125
- JPEG 文档
  - 质量 125
  - 保存 125
- JPEG 选项
  - 扫描线 125
- JPEGSaveOptions 125
- 对齐 182

# K

- 字距调整 180
- 文本
  - 自动字距调整 198
- 键盘行为 160

# L

- LabColor 126
- 标签 97
- 语言 182
- 图层复合 127
  - 添加 128
  - 应用 127
  - 在文档中 90
- 图层组
  - 添加 132
  - 中的图层 130
  - 复制 131
  - 在文档中 90
  - 中的链接图层 130
  - 链接 131
  - 锁定内容 130
  - 移动 131
  - 嵌套 130
  - 不透明度 130
  - 取消链接 131
- 图层样式，应用 60
- LayerComps 128
- 分层 TIFF 文档，保存 159
- 图层 129
- 图层
  - 添加 66
  - 应用样式 60
  - 背景 54
  - 混合模式 54
  - 边界 54
  - 剪贴板命令 60
  - 复合 127
  - 复制 60
  - 复制 61
  - 拼合 93
  - 编组 54
  - 在文档中 90
  - 反相 61
  - 类型 54
  - 链接 61
  - 锁定内容 54–55
  - 可见化 55
  - 合并 61
  - 合并可见图层 93
  - 移动 62
  - 栅格化 93
  - 栅格化内容 62
  - 移除 66
  - 调整大小 63
  - 旋转 63
  - 在 PDF 文档中保存 149
  - 取消链接 63

LayerSet 130

LayerSets 132

图层组
- 合并 131

行距 182, 185

镜头模糊滤镜
- 应用 58

镜头光晕滤镜 58

字间距 181–184

色阶
- 调整 56
- 自动调整 56

连字 180–182

链接图层 61
- 取消链接 63

链接
- 颜色 111

# N

负片 97

杂色滤镜
- 添加杂色
- 去斑 57
- 蒙尘与划痕 57
- 中间值 58

非线性历史记录 160

通知
- 脚本中的事件 137

通知器
- 添加 138
- 事件 ID 217
- 移除 137

NTSC 滤镜 59

# M

macOS
- 文件类型 46

受管理的文档 90

mapBlack 97

最大化兼容性 160

最大值滤镜 58

中间值滤镜 58

内存 46

合并
- 图层 61
- 可见图层 93

元数据
- 文档 90
- 文档对象 100
- 画廊 114
- xmp 91, 189

方法
- 批处理 47

中间调
- 色彩平衡 56

最小值滤镜 59

动感模糊滤镜 59

# O

海洋波纹滤镜 59

位移滤镜 59

旧版样式字体 184

不透明度
- 通道 73
- 画廊安全文本 115
- 图层填充 54
- 图层组 130
- 图层 55
- 图片包 156

打开选项
- DICOM 格式 88
- EPS 格式 104
- PDF 格式 148
- Photo CD 格式 152
- RAW 格式 71, 164

优化 107

其他滤镜
- 自定义 56
- 高反差保留 57
- 最大值 58
- 最小值 59
- 位移 59

# P

调板 161

粘贴 93

路径 46

路径项目
- 添加 143
- 取消选择 139
- 填充 139
- 从文字创建 186
- 创建选区 140
- 路径点 175
- 选择 140
- 指定路径类型 139
- 描边 140
- 子项目 139
- 子路径信息 174
- 子路径项目 175
- 从选区创建工作路径 168



## 路径点信息
- 锚点 145
- 左方向 145
- 右方向 145

## PNG保存选项 158

## 路径点
- 锚点 144
- 左方向 144
- 右方向 144

## 极坐标滤镜 59

## PathItems 143

## 色调分离 62

## 路径
请参阅路径项。

## PostScript编码 93

## PDF文档
- 打开 148
- 保存 149

## PostScript名称 178

## posX 97

## PDF演示文稿
- 自动前进 163
- 制作 49
- 输出格式 163
- 过渡类型 163

## posY 97

## 首选项 159

## PresentationOptions 163

## 照片光盘，打开 152

## 演示文稿
- 制作 49
- PDF演示文稿

## 照片滤镜 62

## printBorder 97

## 照片画廊
请参阅画廊。

## 打印，文档 93

## 照片合并 49

## printOneCopy 93

## Photoshop文档
- 打开 208
- 保存 153

## printSelected 97

## printSettings 90

## Photoshop文件，最大化兼容性 160

## printSpace 97

## PICT文档
- 打开 208
- 保存 154

## 属性
- measurementLog 46

## PSD文档
- 打开 208
- 保存 153

## PICT资源
- 打开 208
- 保存 155

## 清理 50

# Q

## 图片包
- 内容 156
- 拼合 156
- 制作 49
- 不透明度 156
- 选项 156
- 文本属性 156

## quickMaskMode 91

## 引号样式 161

# R

## 挤压滤镜 59

## 径向模糊滤镜 59

## 栅格化 62

## Pixar文档
- 打开 208
- 保存 157

## 栅格化
- 文档图层 93

## RAW文档
- 打开 164

## PixarSaveOptions 157

## RawSaveOptions 165

## 像素
- 宽高比 90
- 倍增 161
- 均衡化 61
- 插值 160
- 锁定 55
- 单位度量 215

## recentFiles 46

## registrationMarks 97

## 渲染滤镜
- 云彩 56
- 分层云彩 57
- 镜头光晕 58

## renderIntent 97

## 播放选项 46

## 分辨率
- 位图转换 69
- 文档 91

## playbackDisplayDialogs 46

## RGBColor 166

## 插件文件夹
- 附加插件文件夹 162

## 水波滤镜 59

## 旋转 63

## PNG 8文档，保存 107

## 标尺单位 161

# S

## +   缩放 98
## 脚本接口
- 构建日期 46
- 版本 46

## scriptingVersion 46

## 脚本
- 自动化 190, 194
- 在菜单中启用/禁用 190
- 执行 33
- 在菜单中分组 190
- 安装 33
- 启动脚本 33
- 术语词典 194
- 有效文件扩展名 32

## Scripts Events Manager 46

## 选中区域 91

## 选区 167
- 边界 167
- 清除 167
- 复制 167
- 剪切 167
- 取消选择 167
- 羽化 167
- 填充 168
- 从路径生成 140
- 从选区创建工作路径 168
- 调整大小 167, 168
- 旋转 168
- 平滑 169
- 描边 169

## 可选颜色 63

## SGIRGB文档
- 保存 172, 212

## SGIRGBSaveOptions 172, 198

## 阴影
- 调整 63
- 色彩平衡 56

## USM锐化滤镜 59

## 锐化滤镜 59

## 锐化滤镜
- 锐化 59
- 锐化边缘 59
- 进一步锐化 59
- USM锐化 60

## 进一步锐化滤镜 59

## 切变滤镜 60

## 特殊模糊滤镜 60

## 智能引号 161

## 球面化滤镜 60

## 专色通道
- 定义 73
- 合并到复合通道 74
- 不透明度 73

## 保存
- 在DCS 2文档中 87
- 在PDF文档中 150
- 在PSD文档中 153
- 在RAW文档中 165
- 在SGIRGB文档中 172
- 在TIFF文档中 187

## +   spotColors 172

## 启动脚本 33

## 删除线 185

## 描边
- 默认描边颜色 45
- 路径项 140
- 选区 169

## 样式，应用 60

## 子路径项 139

## systemInformation 46

# T

## +   温度 62

## 术语词典
- 定义 194
- 语法 194

## 文本
- 亚洲文本 161
- 自动字距调整 180
- 自动行距 185
- 说明文字 112
- 颜色 185
- 排版器 185
- 内容 180
- 从文本创建工作路径 186
- 格式 185
- 画廊安全 115, 205
- 连字 182
- 在图片包中 156
- 对齐 182
- 语言 182
- 偏移 180
- 方向 181
- 间距 181–184
- 字距微调 185
- 换行 182

## 文本排版器 185

## 文本字体
请参阅字体。

## 文本项
请参阅文本。

## 文本图层
- 添加内容 180
- 创建 54

## 纹理填充滤镜 60

## 纹理滤镜，纹理填充 60

## 阈值 63

## 缩略图
- 116
- Mac OS 160
- Windows 162

## TIFF文档
- 带图层 159
- 保存 187

## togglePalettes 51

## 工具提示 161

## toolSupportsBrushes 51

## 字距微调，文本 185

## 传输信息 100

## 叠印陷印 94

# **U**

## +   - 下划线 185
- 单位
  - 标尺 161
  - 类型 162
- UnitValue对象 32, 188
- USM锐化滤镜 60
- URLs，文档 100
- UTF8编码 114

# **W**

## +   - 变形 185
- 波浪滤镜 60
- Web照片画廊
  - 请参阅画廊。
- webSnap 108
- 宽度 91
- Windows
  - 文件类型 47
- 单词间距 181–184
- 工作路径
  - 指定 209
  - 从选区生成 168
- 换行，文本 182

# **V**

## +   - vectorData 98
- 版本
  - 应用程序 47
  - 脚本接口 46
- 视频Alpha通道 162
- 视频滤镜
  - 逐行 57
  - NTSC 59
- 可见性
  - 通道 73
  - 图层复合 127

# **X**

## +   - XML 189
- xmp元数据 91, 189

# **Z**

## +   - 水波滤镜 60
- 缩放 160
