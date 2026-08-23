# Adobe Photoshop CC 2015 JavaScript 参考手册

Adobe Photoshop CC 2015 JavaScript 脚本参考

- 复制 73
- 合并 74
- 移除 74
80
81
`removeAll`
`removeAll`
`width`

# JavaScript 脚本参考

Adobe Photoshop CC 2015
217

# 1 简介

本参考手册描述了 Adobe® Photoshop® CC 2015® JavaScript™ 类型库中的对象和方法。配套文档 *Photoshop CC 2015 脚本指南* 描述了基本的脚本概念和 Photoshop 对象模型。本文档提供了 Photoshop 对象模型的详细参考信息，以及 JavaScript 特有的功能说明。

Adobe Photoshop CC 2015 使用 `ExtendScript`，这是 Adobe 对 JavaScript 的扩展实现。有关更多信息，请参阅 [Adobe Photoshop CC 2015 中的 JavaScript 支持](#)。

本书包含以下部分：

- 本简介，介绍了 Adobe Photoshop CC 2015 中的脚本支持功能，并列出了自上一版本以来 JavaScript 接口的更改。
- [JavaScript 对象参考](#)，为所有 Photoshop DOM 对象和命令提供了完整的参考。
- [脚本常量](#)，列出了 Photoshop 类型库中使用的所有枚举。

# Adobe Photoshop CC 2015 中的 JavaScript 支持

JavaScript 文件要被 Photoshop 识别为有效的脚本文件，必须使用 `.js` 或 `.jsx` 扩展名。

在 Mac OS 上，使用这两种扩展名的脚本功能没有区别。在 Windows 上，如果从 Photoshop 内部打开脚本文件，使用 `.js` 和 `.jsx` 扩展名没有区别。但是，如果通过双击启动脚本，使用 `.js` 扩展名的脚本将使用 Microsoft JScript 引擎解释，无法启动 Adobe Photoshop CC 2015。对于 Windows，建议使用 `.jsx` 扩展名，因为它会使用 `ExtendScript` 引擎解释脚本。

所有 Adobe Creative Cloud 应用程序，包括 Adobe Photoshop CC 2015，都使用 `ExtendScript`，这是 Adobe 对 JavaScript 的扩展实现。`ExtendScript` 文件以 `.jsx` 扩展名区分。`ExtendScript` 提供了所有标准 JavaScript 功能，以及额外的功能和实用工具，例如：

- 调试环境（ExtendScript Toolkit）
- 本地化实用工具
- 允许您组合脚本并将其定向到特定应用程序的工具
- 平台无关的文件和文件夹表示

许多 JavaScript 对象和方法使用 `ExtendScript` 中定义的对象，例如 `File` 对象、`Folder` 对象和 `UnitValue` 对象。因此，为脚本文件使用 `.jsx` 扩展名更为可取。

有关这些和附加功能的详细信息，请参阅 *JavaScript 工具指南*。本文档随 Creative Cloud 应用程序安装在以下位置：

- 在 Windows 上：
  `C:\Program Files\Adobe\Adobe Utilities\ExtendScript Toolkit CC 2015\SDK`
- 在 Mac OS 上：
  `Applications/Utilities/Adobe Utilities/ExtendScript Toolkit CC/SDK`

本文档和 `ExtendScript Toolkit` 的最新版本也可以从 Adobe Developer Center (http://www.adobe.com/devnet/) 下载。

# 执行脚本

Adobe Photoshop CC 2015 界面包含一个脚本菜单（**文件 > 脚本**），可快速便捷地访问您的 JavaScript。脚本可以直接列为菜单项，选择时运行，也可以导航并运行文件系统中的任何 JavaScript。

如果 Adobe Photoshop CC 2015 在脚本执行过程中遇到错误，它会显示错误消息。

# 安装脚本

要将 JavaScript 安装到脚本菜单，请将其放在 `Scripts` 文件夹（**Photoshop CC 2015/Presets/Scripts**）中。`Scripts` 文件夹中的脚本名称（不含文件扩展名）将显示在脚本菜单中。脚本菜单中可以安装任意数量的脚本。

在 Adobe Photoshop CC 2015 运行时添加到 `Scripts` 文件夹的脚本，要到下次启动应用程序时才会出现在脚本菜单中。

`Scripts` 文件夹及其子文件夹中的所有脚本都会显示在 **文件 > 脚本** 菜单的顶层。添加子文件夹不会为脚本菜单添加层次结构组织。

# 执行其他脚本

**脚本** 菜单末尾的 **浏览** 项（**文件 > 脚本 > 浏览**）允许您执行未安装在 `Scripts` 文件夹中的脚本。您也可以使用“浏览”来选择在上次启动应用程序后安装在 Scripts  文件夹中的脚本。

选择 **浏览** 将显示一个文件浏览器对话框，允许您选择要执行的脚本文件。浏览对话框中仅显示 `.js` 或 `.jsx` 文件。选择脚本文件时，其执行方式与安装的脚本相同。

# 启动脚本

启动时，Adobe Photoshop CC 2015 会执行它在启动文件夹中找到的所有 `.jsx` 文件。

- 在 Windows 上，用于用户定义脚本的启动文件夹是：
  `C:\Program Files\Common Files\Adobe\Startup Scripts CC\Adobe Photoshop`
- 在 Mac OS 上，用于用户定义脚本的启动文件夹是：
  `~/Library/Application Support/Adobe/Startup Scripts CC/Adobe Photoshop`

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
| **crop** (bounds [, angle] [, width] [, height]) | 4 个 UnitValue 的数组<br>number UnitValue UnitValue | | |

|
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
| `getReference(index)` | `number` | `ActionReference` | 获取 `ActionReference` 类型的列表元素值。 |
| `getString(index)` | `number` | `string` | 获取字符串类型的列表元素值。 |
| `getType(index)` | `number` | `DescValueType` | 获取列表元素的类型。 |
| `getUnitDoubleType(index)` | `number` | `number` | 获取双精度浮点类型列表元素的单位值类型。 |
| `getUnitDoubleValue(index)` | `number` | `number` | 获取双精度浮点类型列表的单位值。 |
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

此对象提供有关操作所引用内容的信息。例如，当引用某个事物的名称时，您可能会使用 `keyName`。该引用还需要知道您指的是哪个名称。在这种情况下，您可以使用 `classDocument` 表示文档名称，或使用 `classLayer` 表示图层名称。它可用于对 Photoshop 进行底层访问。包含与 `ActionDescriptor` 关联的数据。

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `typename` | `string` | 只读。引用的 `Action` 对象的类名。 |

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

这种用法可能会模糊；为清晰起见，建议您使用 `app`。

### 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `activeDocument` | `Document` | 读写。最前面的文档。设置此属性等同在 Adobe Photoshop CC 2015 中单击打开的文档将其带到屏幕。**提示：** 如果没有打开的文档，访问此属性将异常。 |
| `backgroundColor` | `SolidColor` | 读写。文档的背景颜色和样式。 |
| `build` | `string` | 只读。应用程序的信息。 |
| `colorSettings` | `string` | 读写。当前颜色设置，通过“编辑” > “颜色设置”选择。 |
| `currentTool` | `string` | 读写。当前选工具。 |
| `displayDialogs` | `DialogModes` | 读写。应用程序对话框，控制运行脚本时显示哪些类型的对话框。 |
| `documents` | `Documents` | 只读。打开文档集合。这是访问应用程序中当前文档的主要入口。此数组允许您访问所有打开文档。 |
| `fonts` | `TextFonts` | 只读。系统上安装的字体。 |
| `foregroundColor` | `SolidColor` | 读写。默认前景颜色（用于绘制、填充和描边）。 |
| `freeMemory` | `number` | 只读。Adobe Photoshop CC 2015 可用的内存量。 |
| `locale` | `string` | 只读。应用程序区域设置由一个字母代码组成，中间用下划线区分大小写。例如 `en_US`、`en_UK`、`ja_JP`、`de_DE`、`fr_FR`。 |
| `macintoshFileTypes` | `string数组` | 只读。Adobe Photoshop CC 2015 可以打开的文件类型列表。 |
| `measurementLog` | `MeasurementLog` | 只读。执行测量的日志。 |
| `name` | `string` | 只读。应用程序名称。 |
| `notifiers` | `Notifiers` | 只读。当前配置的通知器（位于 Adobe Photoshop 2015 应用程序中）。 |
| `notifiersEnabled` | `boolean` | 读写。如果所有通知器均启用，则为 true。 |
| `path` | `File` | 只读。Adobe Photoshop CC 2015 应用程序位置的完整路径。 |
| `playbackDialogs` | `DialogModes` | 读写。回放模式，控制在使用动作板放制的动作时显示何种对话框。 |
| `playbackParameters` | `ActionDescriptor` | 读写。存储作为录制动作一部分使用的参数。例如用于回放速度。 |
| `preferences` | `Preferences` | 只读。应用程序首选项设置（等同于 Windows 的 Adobe Photoshop CC 2015 应用程序中选择编辑 > 首选项”）。 |
| `preferencesFolder` | `File` | 只读。“首选项”文件夹的完整路径。 |
| `recentFiles` | `File数组` | 只读。“最近使用文件”列表。 |
| `scriptingBuildDate` | `string` | 只读。脚本接口的构建日期。 |
| `scriptingVersion` | `string` | 只读。脚本接口的版本。 |
| `systemInformation` | `string` | 只读。应用程序和系统的运行时信息。 |
| `typename` | `string` | 只读。被引用 `app` 对象的类名。 |
| `version` | `string` | 只读。你正在运行的 Adobe Photoshop 版本。 |
| `windowsFileTypes` | `string数组` | 只读。Adobe Photoshop CC 2015 可以打开图像扩展名列表。 |

### 方法

| 方法 | 参数类型 | 返回值 | 功能说明 |
| :--- | :--- | :--- | :--- |
| `batch(inputFiles, action, from, [options])` | `File 数组`<br>`string`<br>`string`<br>`BatchOptions` | `string` | 运行批处理自动化例程（类似于“文件 > 自动化 > 批处理”命令）。`inputFiles` 参数指定批处理命令处理的文件来源。 |
| `beep()` | | | 发出“嘟”的声音。 |
| `bringToFront()` | | | 使 Adobe Photoshop CC 2015 成为活动（最前面的）应用程序。 |
| `changeProgressText(progressString)` | `string` | | 更改进度窗口中显示的文本。`progressString` 参数是要进度窗口中显示的字符串。 |
| `charIDToTypeID(charID)` | `string` | `number` | 将四字符代码（字符 ID）转换为运行时 ID。 |
| `doAction(action, from)` | `string`<br>`string` | | 从动作调板播放动作。`action` 参数是动作的名称，`from` 参数是动作组的名称。 |
| `doForcedProgress(progressString, javaScriptString)` | `string`<br>`string` | | 带进度条执行任务。强制显示进度条，忽略通常会阻止其不必要的显示的启发式规则（例如在非常短的任务期间）。必须定期调用其他进度 API 来更新进度条并允许取消。`progressString` 参数是要进度窗口中显示的字符串，`javaScriptString` 参数是要执行的字符串。 |
| `doProgress(progressString, javaScriptString)` | `string`<br>`string` | | 带进度条执行任务。必须定期调用其他进度 API 来更新进度条并允许取消。`progressString` 参数是要进度窗口中显示的字符串，`javaScriptString` 参数是要执行的字符串。 |
| `doProgressSegmentTask(segmentLength, done, total, javaScriptString)` | `number`<br>`number`<br>`number`<br>`string` | boolean | 从进度条的未使用部分划分出一段执行子任务。取消时返回 false。遍历运行时间不等的任务列表时，应使用此方法。`segmentLength` 参数是当前任务的长度，`done` 参数是所有完成任务的总长度，`total` 参数是所有任务的总长度。`javaScriptString` 参数是要执行的字符串。 |
| `doProgressSubTask(index, limit, javaScriptString)` | `number`<br>`number`<br>`string` | boolean | 从进度条的未使用部分划分出一段执行子任务。取消时返回 false。遍历运行时间相等的任务列表时，应使用此方法。`index` 参数是当前任务的从 0 开始的索引，`limit` 参数是任务总数，`javaScriptString` 参数是要执行的字符串。 |
| `doProgressTask(taskLength, javaScriptString)` | `number`<br>`string` | boolean | 从进度条的未使用部分划分出一段执行子任务。取消时返回 false。`taskLength` 参数是要划分的未使用进度条的量，范围在 0.0 到 1.0 之间。`javaScriptString` 参数是要执行的字符串。 |
| `eraseCustomOptions(key)` | `string` | | 从 Photoshop 注册表中删除指定 ID 值的用户对象。 |

```markdown

| `executeAction`(eventID<br>[, descriptor]<br>[, displayDialogs]) | number<br>ActionDescriptor<br>DialogModes | ActionDescriptor | 播放一个 Action Manager 事件。 |

| `executeActionGet`(reference) | ActionReference | ActionDescriptor | 获取有关预定义或录制动作的信息。 |

| `featureEnabled`(name) | string | boolean | 确定由 `name` 指定的功能是否已启用。<br>以下功能支持作为 `name` 的值：<br>"photoshop/extended"<br>"photoshop/standard"<br>"photoshop/trial" |

| `getCustomOptions`(key) | string | ActionDescriptor | 从 Photoshop 注册表中检索 ID 值为 `key` 的用户对象。 |

| `isQuicktimeAvailable()` | | boolean | 如果安装了 Quicktime，则返回 true。 |

| `load`(document) | File | | 从指定位置加载支持文件（相对于 Photoshop 图像文档）。 |

| `makeContactSheet`(inputFiles<br>[, options]) | File 数组<br>ContactSheetOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |

| `makePDFPresentation`(inputFiles,<br>outputFiles<br>[, options]) | File 数组<br>File<br>PresentationOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |

| `makePhotoGallery`(inputFolder,<br>outputFolder<br>[, options]) | File<br>File<br>GalleryOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |

| `makePhotomerge`(inputFiles) | File 数组 | string | 在 Adobe Photoshop CC 2015 中已弃用。请使用提供的脚本：<br>`runphotomergeFromScript = true;`<br>`$.evalFile( app.path +`<br>`"Presets/Scripts/Photomerge.jsx")`<br>`photomerge.createPanorama(` <br>`fileList, displayDialog );`<br>将多个文件合并为一个，需要用户交互。 |

| `makePicturePackage`(inputFiles<br>[, options]) | File 数组<br>PicturePackageOptions | string | 在 Adobe Photoshop CS4 中已弃用。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |

| :--- | :--- | :--- | :--- |

| `open`(文档 [, as] [, asSmartObject]) | File 对象或 OpenDocumentType 布尔值 | Document | 打开指定的文档。<br>使用可选参数 `as` 通过 `OpenDocumentType` 中的常量指定文件格式；或者，您可以使用以下对象同时指定文件格式及其打开选项：<br>[CameraRAWOpenOptions](https://example.com)<br>[DICOMOpenOptions](https://example.com)<br>[EPSOpenOptions](https://example.com)<br>[PDFOpenOptions](https://example.com)<br>[PhotoCDOpenOptions](https://example.com)<br>[RawFormatOpenOptions](https://example.com)<br>使用可选参数 `asSmartObject`（默认值：`false`）为打开的文档创建智能对象。<br>请参阅 Application 示例脚本，了解如何在 `open` 方法中使用 File 对象。 |

| `openDialog()` | | File 数组 | 调用 Photoshop 的“打开”对话框，供用户选择文件。<br>返回一个包含对话框中所选文件的 File 对象数组。 |

| `purge`(目标) | PurgeTarget | | 清除一个或多个缓存。 |

| `putCustomOptions`(键, 自定义对象 [, 持久化]) | string ActionDescriptor boolean | | 将自定义设置对象保存到 Photoshop 注册表中。<br>`键` 是自定义设置的唯一标识符。<br>`自定义对象` 是要保存到注册表中的对象。<br>`持久化` 指脚本执行完毕后对象是否应持久保存。 |

| `refresh()` | | | 在应用程序刷新时暂停脚本。用于减慢执行速度，并在脚本运行时向用户显示结果。请谨慎使用；使用此方法时脚本运行速度会显著变慢。 |

| `refreshFonts()` | | | 强制更新字体列表。 |

| `runMenuItem`(菜单ID) | number | | 根据菜单 ID 运行指定的菜单项。 |

| `showColorPicker()` | | boolean | 如果取消对话框则返回 false，否则返回 true。 |

| `stringIDToTypeID`(字符串ID) | string | number | 将字符串 ID 转换为运行时 ID。 |

| `togglePalettes()` | | | 切换面板可见性。 |

| `toolSupportsBrushes`(工具) | string | boolean | 如果指定工具支持画笔则返回 true，否则返回 false。 |

| `typeIDToCharID`(类型ID) | number | string | 将运行时 ID 转换为字符 ID。 |

| `typeIDToStringID`(类型ID) | number | string | 将运行时 ID 转换为字符串 ID。 |

| `updateProgress`(已完成,<br>总数) | number<br>number | boolean | 更新由 `doProgress` 方法启动的进度条。此方法应用于基于手动的非任务进度更新。取消时返回 false。<br><br>`已完成` 参数是已完成的任务数，`总数` 参数是任务总数。 |

### 应用程序示例脚本

### Application.jsx

此脚本会调用一个警告框，显示应用程序的重要属性，例如版本号、应用程序路径、可用内存量以及打开的文档数量。

当用户按下警告框上的“确定”时，会打开对话框，询问用户是否将前景色和背景色设置为当前文档。如果没有打开的文档，该脚本为用户打开一个新文档。

脚本（未打开文档时）产生连续的对话框。

```
创建欢迎消息
// 使用应用程序对象的 name 和 version 属性
// 将名称和版本附加到消息
// 使用 \r
var message = "欢迎使用 " + app.name
message += " 版本 " + app.version + "\r"

// 查找 Photoshop CC 2015 的安装位置
// 将路径添加到消息
message += "我安装在 " + app.path.fsName + "\r"

// 查看 Adobe Photoshop CC 2015 有多少可用内存量
message += "你有以下内存量用于 Adobe Photoshop CC 15：" +
app.freeMemory + "\r"

// 使用 documents 对象的 length
// 查看打开了多少文档
var documentsOpen = app.documents.length
message += "当前打开了 " + documentsOpen + " 个文档。\r"

// 向用户显示消息
alert(message)

// 对于“是”回答为 true，对于“否”回答为 false
var answer = confirm("是否将前景色和背景设置为喜欢的颜色？")

// 设置颜色
if (answer) {
    // 我喜欢的颜色。你可能知道为什么。
    app.foregroundColor.rgb.red = Math.random() * 255
    app.foregroundColor.rgb.green = Math.random() * 255
    app.foregroundColor.rgb.blue = Math.random() * 255
    app.backgroundColor.rgb.red = Math.random() * 255
    app.backgroundColor.rgb.green = Math.random() * 255
    app.backgroundColor.rgb.blue = Math.random() * 255
}

// 打开一个文档
if (app.documents.length == 0) {
    // 使用应用程序路径到 Samples 文件夹
    var sampleDocToOpen = File(app.path + "/Samples/Fish.psd")

    // 包含文件的消息
    message = "是否要为您打开示例？"
    message += sampleDocToOpen.fsName
    message += ""

    // 再次询问用户
    answer = confirm(message)

    // 相应地打开文档
    if (answer) {
        open(sampleDocToOpen)
    }
}
```

### PDFPresentation.jsx

此脚本将图像序列呈现为 Adobe PDF 幻灯片。

```
// 使用 Samples 文件夹中的所有文件
var inputFolder = new Folder(app.path + "/Samples/")

// 检查是否有内容
if (inputFolder != null) {
    // 获取此文件夹中所有 Photoshop CC 2015（.psd）文件
    var inputFiles = inputFolder.getFiles("*.psd")

    // 输出到桌面
    var outputFile = File("~/Desktop/JavaScriptPresentation.pdf")

    // 有默认设置，自己设置选项
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
| `allLocked` | boolean | 读写。设置为 true 可完全锁定此图层的内容和设置。 |
| `blendMode` | BlendMode | 读写。混合模式。 |
| `bounds` | UnitValue 数组 | 只读。描述图层边界矩形的坐标数组。 |
| `boundsNoEffects` | UnitValue 数组 | 只读。描述图层（不包括效果）边界矩形的坐标数组。 |
| `fillOpacity` | number [0.0..100] | 读写。图层的内部不透明度，以百分比表示。 |
| `filterMaskDensity` | double | 读写。滤镜蒙版的密度（介于 0.0 到 250.0 之间）。 |
| `filterMaskFeather` | double | 读写。滤镜蒙版的羽化（介于 0.0 到 250.0 之间）。 |
| `grouped` | boolean | 读写。如果此图层与其下方的图层编组，则为 true。 |
| `isBackgroundLayer` | boolean | 读写。如果这是文档的背景图层，则为 true。一个文档只能有一个背景图层。如果没有背景图层，将此属性设置为 true 会使其成为背景图层。 |

| 属性名 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `layerMaskDensity` | double | 读写。图层蒙版的密度（在 0.0 到 100.0 之间） |
| `layerMaskFeather` | double | 读写。图层蒙版的羽化（在 0.0 到 250.0 之间） |
| `linkedLayers` | ArtLayer 或 LayerSet 数组 | 只读。链接到此图层。参见 `ArtLayer.link`。 |
| `name` | string | 读写。名称。 |
| `opacity` | number [0.0..100] | 读写。图层的主透明度，一个百分比值。 |
| `parent` | Document | 只读。容器。 |
| `pixelsLocked` | boolean | 读写。如果图层图像中的像素无法使用画笔工具编辑，则为真。 |
| `positionLocked` | boolean | 读写。如果图层图像中的像素无法图层内移动，则为真。 |
| `textItem` | TextItem | 只读。与图层关联的文本项目。仅当 `kind = LayerKind.TEXT` 时有效。 |
| `transparentPixelsLocked` | boolean | 读写。如果编辑被限制在图层的不透明部分，则为真。 |
| `typename` | string | 只读。引用的 `artLayer` 对象的类名。 |
| `vectorMaskDensity` | double | 读写。矢量蒙版的密度（在 0.0 到 250.0 之间） |
| `vectorMaskFeather` | double | 读写。矢量蒙版的羽化（在 0.0 到 250.0 之间） |
| `visible` | boolean | 读写。如果图层可见，则为真。 |
| `xmpMetadata` | xmpMetadata | 读写。图层的元数据。 |
```

```

```markdown
| `adjustColorBalance`<br>([shadows]<br>[, midtones]<br>[, highlights]<br>[, preserveLuminosity]) | number 的数组<br>number 的数组<br>number 的数组<br>boolean |  | 调整图层组件通道的颜色平衡。对于 `shadows`（阴影）、`midtones`（中间调）和 `highlights`（高光），数组必须包含三个值，范围在 `[-100..100]` 之间，分别表示青色或红色、品红色或绿色、黄色或蓝色，具体取决于文档模式是 CMYK 还是 RGB。<br><br>参见 [Document.mode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/properties/document.html#document-mode "Document.mode")。 |

| `adjustCurves`<br>(`curveShape`) | number 的二维数组 |  | 使用最多十四个点调整所选通道的色调范围。<br><br>`curveShape` 数组中的每个值都是一个点对，即一个包含 `x` 和 `y` 整数值的数组。 |

| `adjustLevels`<br>(`inputRangeStart`<br>`inputRangeEnd`<br>`inputRangeGamma`<br>`outputRangeStart`<br>`outputRangeEnd`) | number `[0..253]`<br>number `[(start + 2)..255]`<br>number `[0.10..9.99]`<br>number `[0..253]`<br>number `[(start + 2)..255]` |  | 调整所选通道的色阶。 |

| `applyAddNoise`<br>(`amount`<br>`distribution`<br>`monochromatic`) | number `[0.1..400]`<br>[NoiseDistribution](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/enums/noisedistribution.html "NoiseDistribution")<br>boolean |  | 应用“添加杂色”滤镜。<br><br>`amount` 是一个百分比值。 |

| `applyAverage`<br>() |  |  | 应用“平均值”滤镜。 |

| `applyBlur`<br>() |  |  | 应用“模糊”滤镜。 |

| `applyBlurMore`<br>() |  |  | 应用“进一步模糊”滤镜。 |

| `applyClouds`<br>() |  |  | 应用“云彩”滤镜。 |

| `applyCustomFilter`<br>(`characteristics`<br>`scale`<br>`offset`) | number 的数组<br>number<br>number |  | 应用自定义滤镜。<br><br>`characteristics` 数组有 25 个成员。<br><br>具体说明请参见 Adobe Photoshop CC 2015 帮助。 |

| `applyDeInterlace`<br>(`eliminateFields`<br>`createFields`) | `EliminateFields`<br>`CreateFields` |  | 应用“逐行”滤镜。 |

| `applyDespeckle`<br>() |  |  | 应用“去斑”滤镜。 |

| `applyDifferenceClouds`<br>() |  |  | 应用“分层云彩”滤镜。 |

| `applyDiffuseGlow`<br>(`graininess`<br>`glowAmount`<br>`clearAmount`) | number `[0..10]`<br>number `[0..20]`<br>number `[0..20]` |  | 应用“扩散亮光”滤镜。 |

| `applyDisplace`<br>(`horizontalScale`<br>`verticalScale`<br>`displacement`<br>`areas`<br>`displacementMap`) | number `[-999..999]`<br>number `[-999..999]`<br>`DisplacementMapType`<br>`UndefinedAreas`<br>`File |  | 使用指定的水平比例和垂直比例、映射类型、扭曲区域的方式以及扭曲图像映射，应用“置换”滤镜。 |

| `applyDustAndScratches`<br>(`radius`<br>`threshold`) | number `[1..100]`<br>number `[0..255]` |  | 应用“蒙尘与划痕”滤镜。 |

| `applyGaussianBlur`<br>(`radius`) | number `[0..250.0]` |  | 在指定半径（以像素为单位）内应用“高斯模糊”滤镜。 |

| `applyGlassEffect`<br>(`distortion`<br>`smoothness`<br>`scaling`<br>`invert`<br>`texture`<br>`texture`) | number `[0..20]`<br>number `[1..15]`<br>number `[50..200]`<br>boolean<br>`TextureType`<br>`File |  | 应用“玻璃”滤镜。`scaling` 是一个百分比值。 |

| `applyHighPass`<br>(`radius`) | number `[0..250.0]` |  | 在指定半径内应用“高差”滤镜。 |

| `applyLensBlur`<br>(`source`<br>`focalDistance`<br>`invertDepthMap`<br>`shape`<br>`radius`<br>`bladeCurvature`<br>`rotation`<br>`brightness`<br>`threshold`<br>`amount`<br>`distribution`<br>`monochromatic`) | `DepthMapSource`<br>number<br>boolean<br>`Geometry`<br>number<br>number<br>number<br>number<br>number<br>number<br>`NoiseDistribution`<br>boolean |  | 应用“镜头模糊”滤镜。<br>`source`：深度图的来源（默认：`DepthMapSource.NONE`）。<br>`focalDistance`：深度图的焦距（默认：0）。<br>`invertDepthMask`：如果反转深度图则真（默认：`false`）。<br>`shape`：形状（默认：`Geometry.HEXAGON`）。<br>`radius`：半径（默认：15）。<br>`bladeCurvature`：叶片曲率（默认：0）。<br>`rotation`：旋转（默认：0）。<br>`brightness`：亮度（默认：0）。<br>`threshold`：阈值（默认：0）。<br>`amount`：杂色的数量（默认：0）。<br>`distribution`：分布值（默认：`NoiseDistribution.UNIFORM`）。<br>`monochromatic`：如果色为单色则真（默认：`false`）。 |

| `applyLensFlare`<br>(`brightness`<br>`flareCenter`<br>`lensType`) | number<br>array(`UnitValue`)<br>`LensType` |  | 应用“镜头光晕”滤镜，指定亮度（0-300，作为百分比）、光晕中心的 `x` 和 `y` 坐标（单位值）以及镜头类型。 |

| `applyMaximum`<br>(`radius`) | number `[1..100]` |  | 在指定半径（以像素为单位）内应用“最大值”滤镜。 |

| `applyMedianNoise`<br>(`radius`) | number `[1..100]` |  | 在指定半径（以像素为单位）内应用“中间值”滤镜。 |

| `applyMinimum`<br>(`radius`) | number `[1..100]` |  | 在指定半径（以像素为单位）内应用“最小值”滤镜（1 - 100）。 |

| `applyMotionBlur`<br>(`angle`<br>`radius`) | number `[-360..360]`<br>number `[1..999]` |  | 应用“动感模糊”滤镜。 |

| `applyNTSC`<br>() |  |  | 应用 NTSC 颜色滤镜。 |

| `applyOceanRipple`<br>(`size`<br>`magnitude`) | number `[1..15]`<br>number `[0..20]` |  | 应用“海洋波纹”滤镜。 |

| `applyOffset`<br>(`horizontal`<br>`vertical`<br>`undefinedAreas`) | `UnitValue`<br>`UnitValue`<br>`OffsetUndefinedAreas` |  | 将图层水平移动和垂直移动指定的数量（最小/最大数量取决于图层大小），在图层的原始位置留下一个未定义区域。 |

| `applyPinch`<br>(`amount`) | number `[-100..100]` |  | 应用“挤压”滤镜。`amount` 是一个百分比值。 |

| `applyPolarCoordinates`<br>(`conversion`) | `PolarConversionType` |  | 应用“极坐标”滤镜。 |

| `applyRadialBlur`<br>(`amount`<br>`blurMethod`<br>`blurQuality`<br>`[, blurCenter]`) | number `[1..100]`<br>`RadialBlurMethod`<br>`RadialBlurQuality`<br>`UnitValue` |  | 使用指定的数量应用“径向模糊”滤镜，使用旋转或缩放效果以及指定的质量。参数 `blurCenter` 是位置（单位值）。 |

| `applyRipple`<br>(`amount`<br>`magnitude`) | number `[1..15]`<br>number `[0..20]` |  | 应用“波纹”滤镜。 |
``` |

| `adjustCurves`<br>(`curveShape`) | number 的二维数组 |  | 使用最多十四个点调整所选通道的色调范围。<br><br>`curveShape` 数组中的每个值都是一个点对，即一个包含 `x` And `y` 整数值的数组。 |

| `adjustColorBalance`<br>([shadows]<br>[, midtones]<br>[, highlights]<br>[, preserveLuminosity]) | number 的数组<br>number 的数组<br>number 的数组<br>boolean |  | 调整图层组件通道的颜色平衡。对于 `shadows`（阴影）、`midtones`（中间调）和 `highlights`（高光），数组必须包含三个值，范围在 `[-100..100]` 之间，分别表示青色或红色、品红色或绿色、黄色或蓝色，具体取决于文档模式是 CMYK 还是 RGB。<br><br>参见 [Document.mode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/properties/document.html#document-mode "Document.mode")。 |

| `adjustLevels`<br>(`inputRangeStart`<br>`inputRangeEnd`<br>`inputRangeGamma`<br>`outputRangeStart`<br>`outputRangeEnd`) | number `[0..253]`<br>number `[(start + 2)..255]`<br>number `[0.10..9.99]`<br>number `[0..253]`<br>number `[(start + 2)..255]` |  | 调整所选通道的色阶。 |

| `applyAddNoise`<br>(`amount`<br>`distribution`<br>`monochromatic`) | number `[0.1..400]`<br>[NoiseDistribution](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/enums/noisedistribution.html "NoiseDistribution")<br>boolean |  | 应用“添加杂色”滤镜。<br><br>`amount` 是一个百分比值。 |

| `applyAverage`<br>() |  |  | 应用“平均值”滤镜。 |

| `applyBlur`<br>() |  |  | 应用“模糊”滤镜。 |

| `applyBlurMore`<br>() |  |  | 应用“进一步模糊”滤镜。 |

| `applyClouds`<br>() |  |  | 应用“云彩”滤镜。 |

| `applyCustomFilter`<br>(`characteristics`<br>`scale`<br>`offset`) | number 的数组<br>number<br>number |  | 应用自定义滤镜。<br><br>`characteristics` 数组有 25 个成员。<br><br>具体说明请参见 Adobe Photoshop CC 2015 帮助。 |

| `applyDeInterlace`<br>(`eliminateFields`<br>`createFields`) | `EliminateFields`<br>`CreateFields` |  | 应用“逐行”滤镜。 |

| `applyDespeckle`<br>() |  |  | 应用“去斑”滤镜。 |

| `applyDifferenceClouds`<br>() |  |  | 应用“分层云彩”滤镜。 |

| `applyDiffuseGlow`<br>(`graininess`<br>`glowAmount`<br>`clearAmount`) | number `[0..10]`<br>number `[0..20]`<br>number `[0..20]` |  | 应用“扩散亮光”滤镜。 |

| `applyDisplace`<br>(`horizontalScale`<br>`verticalScale`<br>`displacement`<br>`areas`<br>`displacementMap`) | number `[-999..999]`<br>number `[-999..999]`<br>`DisplacementMapType`<br>`UndefinedAreas`<br>`File |  | 使用指定的水平比例和垂直比例、映射类型、扭曲区域的方式以及扭曲图像映射，应用“置换”滤镜。 |

| `applyDustAndScratches`<br>(`radius`<br>`threshold`) | number `[1..100]`<br>number `[0..255]` |  | 应用“蒙尘与划痕”滤镜。 |

| `applyGaussianBlur`<br>(`radius`) | number `[0..250.0]` |  | 在指定半径（以像素为单位）内应用“高斯模糊”滤镜。 |

| `applyGlassEffect`<br>(`distortion`<br>`smoothness`<br>`scaling`<br>`invert`<br>`texture`<br>`texture`) | number `[0..20]`<br>number `[1..15]`<br>number `[50..200]`<br>boolean<br>`TextureType`<br>`File |  | 应用“玻璃”滤镜。`scaling` 是一个百分比值。 |

| `applyHighPass`<br>(`radius`) | number `[0..250.0]` |  | 在指定半径内应用“高差”滤镜。 |

| `applyLensBlur`<br>(`source`<br>`focalDistance`<br>`invertDepthMap`<br>`shape`<br>`radius`<br>`bladeCurvature`<br>`rotation`<br>`brightness`<br>`threshold`<br>`amount`<br>`distribution`<br>`monochromatic`) | `DepthMapSource`<br>number<br>boolean<br>`Geometry`<br>number<br>number<br>number<br>number<br>number<br>number<br>`NoiseDistribution`<br>boolean |  | 应用“镜头模糊”滤镜。<br>`source`：深度图的来源（默认：`DepthMapSource.NONE`）。<br>`focalDistance`：深度图的焦距（默认：0）。<br>`invertDepthMask`：如果反转深度图则真（默认：`false`）。<br>`shape`：形状（默认：`Geometry.HEXAGON`）。<br>`radius`：半径（默认：15）。<br>`bladeCurvature`：叶片曲率（默认：0）。<br>`rotation`：旋转（默认：0）。<br>`brightness`：亮度（默认：0）。<br>`threshold`：阈值（默认：0）。<br>`amount`：杂色的数量（默认：0）。<br>`distribution`：分布值（默认：`NoiseDistribution.UNIFORM`）。<br>`monochromatic`：如果色为单色则真（默认：`false`）。 | |

| `applyLensFlare`<br>(`brightness`<br>`flareCenter`<br>`lensType`) | number<br>array(`UnitValue`)<br>`LensType` |  | 应用“镜头光晕”滤镜，指定亮度（0-300，作为百分比）、光晕中心的 `x` 和 `y` 坐标（单位值）以及镜头类型。 |

| `applyMaximum`<br>(`radius`) | number `[1..100]` |  | 在指定半径（以像素为单位）内应用“最大值”滤镜。 |

| `applyMedianNoise`<br>(`radius`) | number `[1..100]` |  | 在指定半径（以像素为单位）内应用“中间值”滤镜。 |

| `applyMinimum`<br>(`radius`) | number `[1..100]` |  | 在指定半径（以像素为单位）内应用“最小值”滤镜（1 - 100）。 |

| `applyMotionBlur`<br>(`angle`<br>`radius`) | number `[-360..360]`<br>number `[1..999]` |  | 应用“动感模糊”滤镜。 |

| `applyNTSC`<br>() |  |  | 应用 NTSC 颜色滤镜。 |

| `applyOceanRipple`<br>(`size`<br>`magnitude`) | number `[1..15]`<br>number `[0..20]` |  | 应用“海洋波纹”滤镜。 |

| `applyOffset`<br>(`horizontal`<br>`vertical`<br>`undefinedAreas`) | `UnitValue`<br>`UnitValue`<br>`OffsetUndefinedAreas` |  | 将图层水平移动和垂直移动指定的数量（最小/最大数量取决于图层大小），在图层的原始位置留下一个未定义区域。 |

| `applyPinch`<br>(`amount`) | number `[-100..100]` |  | 应用“挤压”滤镜。`amount` 是一个百分比值。 |

| `applyPolarCoordinates`<br>(`conversion`) | `PolarConversionType` |  | 应用“极坐标”滤镜。 |

| `applyRadialBlur`<br>(`amount`<br>`blurMethod`<br>`blurQuality`<br>`[, blurCenter]`) | number `[1..100]`<br>`RadialBlurMethod`<br>`RadialBlurQuality`<br>`UnitValue` |  | 使用指定的数量应用“径向模糊”滤镜，使用旋转或缩放效果以及指定的质量。参数 `blurCenter` 是位置（单位值）。 |

| `applyRipple`<br>(`amount`<br>`magnitude`) | number `[1..15]`<br>number `[0..20]` |  | 应用“波纹”滤镜。 |
```


| parent | Document | 只读。对象的容器。 |
| typename | string | 只读。引用的 `artLayers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `add()` | | ArtLayer | 在文档中创建一个新的艺术图层，并将新对象添加到此集合中。 |
| `getByName(name)` | string | ArtLayer | 获取 `artLayers` 集合中具有所提供名称的第一个元素。 |
| `removeAll()` | | | 从 `artLayers` 集合中移除所有元素。 |

## BatchOptions

使用 `Application.batch()` 方法运行批处理操作的选项。

JavaScript仅支持文件夹作为批处理命令的源。请将批处理源文件夹指定为 `Application.batch()` 方法的 `inputFiles` 参数。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `destination` | BatchDestinationType | 可读写。处理后文件的目标类型（默认：`BatchDestinationType.NODESTINATION`）。 |
| `destinationFolder` | Folder | 可读写。处理后文件的文件夹位置。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `errorFile` | File | 可读写。用于记录遇到错误的文件。要直接在屏幕上显示错误（并在发生错误时停止批处理），请留空。 |
| `fileNaming` | array of FileNamingType | 可读写。文件命名选项列表（最多：6 项）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `macintoshCompatible` | boolean | 可读写。True 表示使最终文件名与 Macintosh 兼容（默认：`true`）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `overrideOpen` | boolean | 可读写。True 表示覆盖动作中的打开命令（默认：`false`）。 |
| `overrideSave` | boolean | 可读写。True 表示用指定的目标覆盖另存为动作步骤（默认：`false`）。仅当 `destination` = `BatchDestinationType.FOLDER` 或 `SAVEANDCLOSE` 时有效。 |
| `startingSerial` | number | 可读写。用于命名文件的起始序号（默认：`1`）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `suppressOpen` | boolean | 可读写。True 表示抑制文件打开选项对话框（默认：`false`）。 |
| `suppressProfile` | boolean | 可读写。True 表示抑制颜色配置文件警告（默认：`false`）。 |
| `typename` | string | 只读。引用的 `batchOptions` 对象的类名。 |
| `unixCompatible` | boolean | 可读写。True 表示使最终文件名与 Unix 兼容（默认：`true`）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |
| `windowsCompatible` | boolean | 可读写。True 表示使最终文件名与 Windows 兼容（默认：`true`）。仅当 `destination` = `BatchDestinationType.FOLDER` 时有效。 |

## BitmapConversionOptions

使用 `Document.changeMode()` 配合 `ChangeMode.Bitmap` 将图像转换为位图模式的选项。

在将图像转换为位图模式之前，请先将彩色图像转换为灰度。参见 `ArtLayer.desaturate()` 方法。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `angle` | `number [-180..180]` | 可读写。用于设置单个点方向的角度（以度为单位）。参见 `shape`。仅当 `method` = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `frequency` | `number [1.0..999.99]` | 可读写。要使用的打印机点数（每英寸）。仅当 `method` = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `method` | BitmapConversionType | 可读写。要使用的转换方法（默认：`BitmapConversionType.DIFFUSIONDITHER`）。 |
| `patternName` | `string` | 可读写。要使用的图案名称。有关预装的有效图案的信息，请参阅 Adobe Photoshop CC 2015 帮助中的位图转换命令，或在选择位图转换命令后查看“自定义颜色”下拉框中可用的选项。仅当 `method` = `BitmapConversionType.CUSTOMPATTERN` 时有效。 |
| `resolution` | `number` | 可读写。以像素/英寸为单位的输出分辨率（默认：`72.0`）。 |
| `shape` | BitmapHalfToneType | 可读写。要使用的点形状。仅当 `method` = `BitmapConversionType.HALFTONESCREEN` 时有效。 |
| `typename` | string | 只读。引用的 `bitmapConversionOptions` 对象的类名。 |

## BMPSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 BMP 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | boolean | 可读写。True 表示保存 Alpha 通道。 |
| `depth` | BMPDepthType | 可读写。每通道的位数。 |
| `flipRowOrder` | boolean | 可读写。True 表示从上到下写入图像（默认：`false`）。仅当 `osType` = `OperatingSystem.WINDOWS` 时可用。 |
| `osType` | OperatingSystem | 可读写。目标操作系统。（默认：`OperatingSystem.WINDOWS`）。 |
| `rleCompression` | boolean | 可读写。True 表示使用 RLE 压缩。仅当 `osType` = `OperatingSystem.WINDOWS` 时可用。 |
| `typename` | string | 只读。引用的 `BMPSaveOptions` 对象的类名。 |

## CameraRAWOpenOptions

使用 `Application.open` 方法打开 Camera RAW 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `bitsPerChannel` | BitsPerChannelType | 可读写。每通道的位数。 |
| `blueHue` | `number [-100..100]` | 可读写。拍摄图像的蓝色色相。 |
| `blueSaturation` | `number [-100..100]` | 可读写。拍摄图像的蓝色饱和度。 |
| `brightness` | `number [0..150]` | 可读写。拍摄图像的亮度。 |
| `chromaticAberrationBY` | `number [-100..100]` | 可读写。拍摄图像的色差 B/Y。 |
| `chromaticAberrationRC` | `number [-100..100]` | 可读写。拍摄图像的色差 R/C。 |
| `colorNoiseReduction` | `number [0..100]` | 可读写。拍摄图像的彩色杂色。 |
| `colorSpace` | ColorSpaceType | 可读写。图像的色彩空间。 |
| `contrast` | `number [-50..100]` | 可读写。拍摄图像的对比度。 |
| `exposure` | `number [-4.0..4.0]` | 可读写。拍摄图像的曝光度。 |
| `greenHue` | `number [-100..100]` | 可读写。拍摄图像的绿色色相。 |
| `greenSaturation` | `number [-100..100]` | 可读写。拍摄图像的绿色饱和度。 |
| `luminanceSmoothing` | `number [0..100]` | 可读写。拍摄图像的亮度平滑。 |
| `redHue` | `number [-100..100]` | 可读写。拍摄图像的红色色相。 |
| `redSaturation` | `number [-100..100]` | 可读写。拍摄图像的红色饱和度。 |
| `resolution` | `number [1..999]` | 可读写。文档的分辨率，以像素/英寸为单位。 |
| `saturation` | `number [-100..100]` | 可读写。拍摄图像的饱和度。 |
| `settings` | CameraRAettingsType | 可读写。所有 Camera RAW 选项的全局设置。默认：`CameraRAettingsType`。 |
| `shadows` | `number [0..100]` | 可读写。拍摄图像阴影。 |
| `shadowTint` | `number [-100..100]` | 可读写。拍摄图像的阴影色调。 |
| `sharpness` | `number [0..100]` | 可读写。拍摄图像的锐度。 |
| `size` | CameraRAWSize | 可读写。文档的大小。 |
| `temperature` | `number [2000..5000]` | 可读写。拍摄图像的色温。 |

## 通道

关于图像中颜色元素的信息。通过 `Document.channels` 集合访问。你可以通过索引或名称在此列表中单个通道。例如，以下代码按名称访问活动文档中的通道并分配一个 `opacity` 值：

```javascript
var channelRef = app.activeDocument.channels.getByName("my channel");
channelRef.opacity = 22;
```

通道类似于印刷过程中应用单一色的印版。文档的颜色模式决定了通道的数量；例如，RGB 文档有三个通道：红、绿和蓝。颜色也可以有一个 Alpha 通道，它以蒙版形式存储选区；或者一个专色通道，它存储专色。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `color` | SolidColor | 可读写。通道的颜色。当 `kind` = `ChannelType.COMPONENT` 时无效。 |
| `histogram` | array of number | 只读。通道颜色的直图。该数组包含 256 个成员。当 `kind` = `ChannelType.COMPONENT` 时无效。对于分量通道直图值，请改用 `Document` 对象的 `histogram` 属性。 |
| `kind` | ChannelType | 可读写。通道的类型。 |
| `name` | string | 可读写。通道的名称。 |
| `opacity` | number [0..100] | 可读写。用于 Alpha 通道的不透明度，或用于专色通道的实度。仅当 `kind` = `ChannelType.MASKEDAREA` 或 `SELECTEDAREA` 时有效。 |
| `parent` | Document | 只读。包含此通道的文档。 |
| `typename` | string | 只读。引用的 `channel` 对象的类名。 |
| `visible` | boolean | 可读写。如果通道可见则为真。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
| --- | --- | --- | --- |
| `duplicate([targetDocument])` | Document | Channel | 复制通道。 |
| `merge()` | | | 将专色通道合并到分量通道中。 |
| `remove()` | | | 删除通道。 |

## 通道集合

文档中 `Channel` 对象的集合。通过 `Document.channels` 集合属性访问。例如：

```javascript
var channelRef = app.activeDocument.channels.add()
```

## 属性

| 属性 | 值类型 | 描述 |
|---|---|---|
| length | number | 只读。`channels` 集合中的元素数量。 |
| parent | Document | 只读。包含此集合的文档。 |
| typename | string | 只读。引用的 `channels` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 描述 |
|---|---|---|---|
| `add()` | | Channel | 创建一个新的通道对象并将其此集合中。 |
| `getByName(name)` | string | Channel | 获取 `channels` 集合中具有所提供名称的第一个元素。 |
| `removeAll()` | | | 从 `channels` 集合中移除所有 Alpha 通道对象。 |

### 通道示例脚本

以下脚本会在没有文件打开时打开一个文件，然后为活动文档中的通道编写一个直方图报告 (histogram.log)。

> **注意：** 此脚本包含一个使用 `break` 语句的 switch 结构。`break` 语句需要一个结尾分号 (;)，如下例所示：

`break;`

### Histogram.jsx

```javascript
// Function to activate all the channels according to the documents mode

// Takes a document reference for input

function TurnOnDocumentHistogramChannels(inDocument) {

    // see how many channels we need to activate
```


<|channel>thought
<channel|>
```javascript
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

```javascript
// now get the channels to activate into a local array
var aChannelArray = new Array()
// index for the active channels array
var aChannelIndex = 0
for(var channelIndex = 0; channelIndex < inDocument.channels.length; channelIndex++) {
    if (channelIndex < visibleChannelCount) {
        aChannelArray[aChannelIndex++] = inDocument.channels[channelIndex]
    }
}
// now activate them
inDocument.activeChannels = aChannelArray
```

```javascript
// Save the current preferences
var startRulerUnits = app.preferences.rulerUnits
var startTypeUnits = app.preferences.typeUnits
var startDisplayDialogs = app.displayDialogs
// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
app.preferences.displayDialogs = DialogModes.NO
// if there are no documents open then try to open a sample file
if (app.documents.length == 0) {
    open(File(app.path + "/Samples/Fish.psd"))
}
// get a reference to the working document
var docRef = app.activeDocument
```

```javascript
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
    for (var secondaryIndex = 0; secondaryIndex < myChannels.length; secondaryIndex++) {
        if (channelIndex != secondaryIndex) {
            myChannels[secondaryIndex].visible = false
        }
    }
    // Use the function to dump the histogram
    OutputHistogram(myChannels[channelIndex].histogram, myChannels[channelIndex].name, fileOut)
}
```

```javascript
// 关闭输出文件
fileOut.close()
alert("直方图文件已保存至: " + fileOut.fsName)
// 重置活动通道
docRef.activeChannels = myActiveChannels

// 重置应用程序首选项
app.preferences.rulerUnits = startRulerUnits
app.preferences.typeUnits = startTypeUnits
app.preferences.displayDialogs = startDisplayDialogs

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
    for (histogramIndex = 0; histogramIndex < inHistogram.length; histogramIndex++) {
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
    for (histogramIndex = 0; histogramIndex < inHistogram.length; histogramIndex++) {
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
        var outputX = inHistogram[histogramIndex] / largestCount
        // 输出 X
        for (var a = 0; a < outputX; a++) {
            inOutFile.write("X")
        }
        inOutFile.write("\n")
    }
}
```


```markdown
## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `length` | number | 只读。`ColorSamplers` 集合中的元素数量。 |
| `parent` | [Document](Document) | 只读。所属文档。 |
| `typename` | string | 只读。引用的 `ColorSamplers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `add` (position) | array of [UnitValue](UnitValue) | [ColorSampler](ColorSampler) | 创建一个新的颜色取样器对象并将其添加到此集合中。`position` 参数 `(x,y)` 表示移动后的颜色取样器的新水平和垂直位置。 |
| `removeAll` () | | | 从 `ColorSamplers` 集合中移除所有 `ColorSampler` 对象。 |

# ContactSheetOptions

使用 `Application.makeContactSheet()` 方法创建联系表的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `acrossFirst` | boolean | 可读写。为 `true` 则先水平（从左到右，然后从上到下）放置图像（默认值：`true`）。 |
| `bestFit` | boolean | 可读写。为 `true` 则旋转图像以实现最佳适应（默认值：`false`）。 |
| `caption` | boolean | 可读写。为 `true` 则使用文件名作为图像的说明文字（默认值：`true`）。 |
| `columnCount` | number [1..100] | 可读写。要包含的列数（默认值：5）。 |
| `flatten` | boolean | 可读写。为 `true` 则在最终文档中合并所有图层（默认值：`true`）。 |
| `font` | [GalleryFontType](GalleryFontType) | 可读写。用于说明文字的字体（默认值：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number | 可读写。用于说明文字的字号（默认值：12）。 |
| `height` | number [0..29000] | 可读写。生成文档的高度（以像素为单位）（默认值：720）。 |
| `horizontal` | number | 可读写。图像之间的水平间距（以像素为单位）（默认值：1）。 |
| `mode` | [NewDocumentMode](NewDocumentMode) | 可读写。文档颜色模式（默认值：`NewDocumentMode.RGB`）。 |
| `resolution` | number [35..1200] | 可读写。文档的分辨率，以每英寸像素数为单位（默认值：72.0）。 |
| `rowCount` | number [1..100] | 可读写。要使用的行数（默认值：6）。 |
| `typename` | string | 只读。引用的 `contactSheetOptions` 对象的类名。 |
| `useAutoSpacing` | boolean | 可读写。为 `true` 则自动设置图像间距（默认值：`true`）。 |
| `vertical` | number [0..29000] | 可读写。图像之间的垂直间距（以像素为单位）（默认值：1）。仅在 `useAutoSpacing = false` 时有效。 |
| `width` | number [100..29000] | 可读写。生成文档的宽度（以像素为单位）（默认值：576）。 |

# CountItem

文档中的计数项目。通过 `Document.countItems` 集合访问。请参阅 `Document.autoCount()` 方法。

**注意：** 此功能仅在扩展版中可用。

有关计数项目的更多信息，请参阅 Adobe Photoshop CC 2015 帮助中的计数工具。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `position` | `array of UnitValue` | 只读。计数项目在文档中的位置。 |
| `parent` | [Document](Document) | 只读。所属文档。 |
| `typename` | `string` | 只读。引用的 `CountItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
|---|---|---|---|
| `remove()` | | | 删除 `CountItem` 对象。 |

# CountItems

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
| `add(position)` | [UnitValue](https://helpx.adobe.com/photoshop/using/unit-value.html) 数组 | [CountItem](https://helpx.adobe.com/photoshop/using/counting-tool.html) | 创建一个新的计数项对象并将其添加到此集合中。<br>参数 `position` `(x, y)` 分别表示 `CountItem` 对象的水平和垂直位置。 |
| `getByName(name)` | string | [CountItem](https://helpx.adobe.com/photoshop/using/counting-tool.html) | 获取 `CountItems` 集合中具有指定名称的第一个元素。 |
| `removeAll()` | | | 从 `CountItems` 集合中移除所有 `CountItem` 对象。 |

# DCS1_SaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法将 CMYK 文档保存为 DCS1 格式的选项。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `dCS` | [DCSType](DCSType) | 可读写。（默认：`DCSType.COLORCOMPOSITE`）。 |
| `embedColorProfile` | boolean | 可读写。为 `true` 时在文档中嵌入颜色配置文件。 |
| `encoding` | [SaveEncoding](SaveEncoding) | 可读写。用于文档的编码（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | boolean | 可读写。为 `true` 时包含半调屏（默认：`false`）。 |
| `interpolation` | boolean | 可读写。为 `true` 时使用图像插值（默认：`false`）。 |
| `preview` | [Preview](Preview) | 可读写。预览类型（默认：`Preview.MACOSEIGHT`）。 |
| `transferFunction` | boolean | 可读写。为 `true` 时用于补偿图像和胶片之间大的传递函数（默认：`false`）。 |
| `typename` | string | 只读。引用的 `DCS1_SaveOptions` 对象的类名。 |
| `vectorData` | boolean | 可读写。为 `true` 时包含矢量数据。在文档包含矢量数据（栅格化）时有效。 |

# DCS2_SaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法将 CMYK 文档保存为 DCS2 格式。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `dcs` | [DCSType](DCSType) | 可读写。要创建的复合类型（默认：`DCSType.NOCOMPOSITE`）。 |
| `embedColorProfile` | boolean | 可读写。为 `true` 时在文档中嵌入配置文件。 |
| `encoding` | [SaveEncoding](SaveEncoding) | 可读写。使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | boolean | 可读写。为 `true` 时包含半调屏（默认：`false`）。 |
| `interpolation` | boolean | 可读写。为 `true` 时使用插值（默认：`false`）。 |
| `multiFileDCS` | boolean | 可读写。为 `true` 将颜色通道保存为多个文件（默认：`false`）。 |
| `preview` | [Preview](Preview) | 可读写。预览类型（默认：`Preview.MACOSEIGHT`）。 |
| `spotColors` | boolean | 可读写。为 `true` 保存专色。 |
| `transferFunction` | boolean | 可读写。为 `true` 时用于补偿图像和胶片之间大的传递函数（默认：`false`）。 |
| `typename` | string | 只读。引用的 `DCS2_SaveOptions` 对象的类名。 |
| `vectorData` | boolean | 可读写。为 `true` 时包含矢量数据。在文档包含矢量数据（栅格化）时有效。 |

# DICOMOptions

使用 `Application.open()` 方法打开 DICOM 格式。

**注意：** 此功能仅在扩展版中可用。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `anonymize` | boolean | 可读写。为 `true` 时匿名化。 |
| `columns` | number | 可读写。n-up 配置中的列数。 |
| `reverse` | boolean | 可读写。为 `true` 时反转图像。 |
| `rows` | number | 可读写。n-up 配置中的行数。 |
| `showOverlays` | boolean | 可读写。为 `true` 时显示覆盖。 |
| `typename` | string | 只读。引用的 `DICOMOptions` 对象的类名。 |
| `windowLevel` | number | 可读写。以像素表示图像对比度。 |
| `windowWidth` | number | 可读写。以像素表示图像亮度。 |

# Document

脚本中图层和所有对象的活动容器；文件的画布。

- 通过 `Application.activeDocument` 访问当前文档。
- 你可以使用 `Application.documents` 集合访问其他文档，或遍历所有文档。你可以通过索引访问单个文档，或使用 `Documents.getByName()` 按名称检索。
- 使用 `Documents.add()` 方法以编程创建文档。

有关示例，请参阅 `Document sample` 和 `Documents` 集合对象。

**注意：** 在 Adobe Photoshop CC 2015 中，文档也可以称为图像或画布。

- 术语 `图像` 指整个文档及其内容。你可以裁剪裁切图像。使用 `resizeImage()` 方法调整大小。
- 术语 `画布` 指文档在屏幕上占据的空间。你可以旋转或翻转画布。使用 `resizeCanvas()` 方法调整大小。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `activeChannels` | `Channel` 数组 | 可读写。选中的通道。 |
| `activeHistoryBrushSource` | `Guide` | 可读写。与历史记录画笔一起使用的历史状态。 |
| `activeHistoryState` | `Guide` | 可读写。选中的 `HistoryState` 对象。 |
| `activeLayer` | `ArtLayer` 或 `LayerSet` | 可读写。选中的图层。 |
| `artLayers` | `ArtLayers` | 只读。图层集合。 |
| `backgroundLayer` | `ArtLayer` | 只读。文档的背景图层。 |
| `bitsPerChannel` | `BitsPerChannelType` | 可读写。每通道位数。 |
| `channels` | `Channels` | 只读。通道集合。 |
| `colorProfileName` | string | 可读写。颜色配置文件的名称。仅在 `colorProfileType = ColorProfile.CUSTOM` 或 `WORKING` 时有效。 |
| `colorProfileType` | `ColorProfileType` | 可读写。文档使用的是工作颜色配置文件、自定义配置文件还是没有配置文件。 |
| `colorSamplers` | `ColorSamplers` | 只读。与当前文档关联的颜色取样器。 |
| `componentChannels` | `Channel` 数组 | 只读。构成文档的颜色通道；例如，RGB 文档的红色、绿色和蓝色通道。 |
| `countItems` | [CountItems](https://helpx.adobe.com/photoshop/using/counting-tool.html) | 只读。当前的计数项。注意：有关计数项的更多信息，请参阅 Adobe Photoshop CC 2015 关于计数工具的帮助。 |
| `fullName` | [File](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.File.html) | 只读。文档的完整路径名。 |
| `guides` | [Guides](https://helpx.adobe.com/photoshop/using/creating-guides.html) | 只读。参考线集合。 |
| `height` | [UnitValue](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.UnitValue.html) | 只读。文档的高度（单位值）。 |
| `histogram` | number 数组 | 只读。显示复合通道中每个颜色强度级别的直方图。该数组包含 256 个成员。仅在 `mode = [DocumentMode](https://helpx.adobe.com/photoshop/using/mode-conversion), CMYK 或 INDEXEDCOLOR` 时有效。 |
| `historyStates` | [HistoryStates](https://helpx.adobe.com/photoshop/using/history-panel.html) | 只读。历史记录状态。 |
| `info` | [DocumentInfo](https://helpx.adobe.com/photoshop/using/document-properties.html) | 只读。关于文档的元数据。 |
| `layerComps` | [LayerComps](https://helpx.adobe.com/photoshop/using/layer-comps.html) | 只读。图层复合集合。 |
| `layers` | [Layers](https://helpx.adobe.com/photoshop/using/layers.html) | 只读。图层集合。 |
| `layerSets` | [LayerSets](https://helpx.adobe.com/photoshop/using/layer-groups.html) | 只读。图层组。 |
| `managed` | boolean | 只读。如果文档是工作组为 `true`。 |
| `measurementScale` | [MeasurementScale](https://helpx.adobe.com/photoshop/using/measuring-tools.html) | 只读。测量比例。注意：测量比例仅在扩展版中可用。 |
| `mode` | [DocumentMode](https://helpx.adobe.com/photoshop/using/mode-conversion.html) | 只读。颜色配置文件。 |
| `name` | string | 只读。文档名称。 |
| `parent` | [Application](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.Application.html) | 只读。包含此文档的应用程序。 |
| `path` | [File](https://extendscript.docsforadobe.org/extendscriptcsdoc/extendscript/types/ExtendScript/ExtendScript.File.html) | 只读。文档路径。 |
| `pathItems` | [PathItems](https://helpx.adobe.com/photoshop/using/paths.html) | 只读。路径项集合。 |
| `pixelAspectRatio` | number [0..100] | 可读写。要使用的（自定义）宽高比。 |
| `printSettings` | [DocumentPrintSettings](https://helpx.adobe.com/photoshop/using/printing-images.html) | 只读。打印设置。 |

### Document 对象属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `quickMaskMode` | boolean | 读写。如果文档处于快速蒙版模式为 `true`。 |
| `resolution` | number | 只读。文档的分辨率（以像素/英寸）。 |
| `saved` | boolean | 只读。如果文档自更改后已保存为 `true`。 |
| `selection` | [Selection](selection.html) | 只读。文档的选区。 |
| `typename` | string | 只读。Document 对象的类名。 |
| `width` | UnitValue | 只读。文档的宽度（单位值）。 |
| `xmpMetadata` | [xmpMetadata](xmpMetadata.html) | 只读。文档的 XMP 元数据。例如，图像的 Camera RAW 设置在此。 |

### Document 对象方法

| 方法 | 参数类型 | 返回值 | 描述 |
| --- | --- | --- | --- |
| `autoCount`<br>(channel,<br>threshold) | [Channel](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#channel)<br>number | | 统计文档中数量。仅在扩展版中可用。<br>为被统计的对象创建一个 [CountItem](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#countitem) 对象。<br>有关如何设置计数的对象的更多信息，请参阅 Adobe Photoshop CC 2015 帮助中的计数工具。 |
| `changeMode`<br>(destinationMode<br>[, options]) | [ChangeMode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#changemode)<br>[BitmapConversionOptions](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#bitmapconversionoptions) 或 [IndexedConversionOptions](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#indexedconversionoptions) | | 更改文档的颜色配置文件。 |
| `close`<br>([saving]) | [SaveOptions](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#saveoptions) | | 关闭文档。如果进行了任何更改，脚本将显示一个带有三个选项的警报：保存、不保存、提示保存。可选参数指定警报框中的选择（默认值：`SaveOptionsType.PROMPTTOSAVECHANGES`）。 |
| `convertProfile`<br>(destinationProfile,<br>intent<br>[, blackPointCompensation]<br>[, dither]) | string<br>[Intent](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#intent)<br>boolean<br>boolean | | 更改颜色配置文件。<br>`destinationProfile` 参数必须是命名颜色模式的字符串，或者是 `Working RGB`、`Working CMYK`、`Working Gray`、`Lab Color`（表示一个工作颜色空间或 Lab 颜色）。 |
| `crop`<br>(bounds<br>[, angle]<br>[, width]<br>[, height]) | 由 4 个 [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#unitvalue) 组成的数组<br>number<br>[UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#unitvalue)<br>[UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#unitvalue) | | 裁剪文档。`bounds` 参数是裁剪后剩余区域的四个坐标数组 `[left, top, right, bottom]`。 |
| `duplicate`<br>(name>[, mergeOnly]) | string<br>boolean | [CountItem](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/#countitem) | 创建一个新的副本并将其添加到此集合中。 |
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
| `backgroundColor` | SolidColor | 读写。页面的背景色。 |
| `bleedWidth` | UnitValue | 读写。出血宽度 |
| `caption` | boolean | 读写。打印在 `FileInfo` 中找到的说明文字。 |
| `centerCropMarks` | boolean | 读写。打印中心裁切标记。 |
| `colorBars` | boolean | 读写。打印色彩校准条。 |
| `copies` | number | 读写。要打印的份数。 |
| `cornerCropMarks` | boolean | 读写。打印边角裁切标记。 |
| `colorHandling` | PrintColorHandling | 只读。颜色处理。 |
| `activePrinter` | string | 读写。当前活动的打印机。 |
| `flip` | boolean | 读写。水平翻转图像。 |
| `hardProof` | boolean | 读写。打印硬打样。 |
| `interpolate` | boolean | 读写。 |
| `labels` | boolean | 读写。打印文档标题。 |
| `mapBlack` | boolean | 读写。映射黑色。 |
| `negative` | boolean | 读写。反转图像颜色。 |
| `renderIntent` | Intent | 读写。当打印空间与源空间不同时的颜色转换意图。 |
| `posX` | UnitValue | 只读。图像在页面上的 x 位置。 |
| `posY` | UnitValue | 只读。图像在页面上的 y 位置。 |
| `printBorder` | UnitValue | 读写。打印边框的宽度。 |
| `printerName` | string | 读写。打印机的名称。 |
| `printSpace` | string | 读写。用于打印机的颜色空间。可以为空（表示与源相同）；`Working RGB`、`Working CMYK`、`Working Gray`、`Lab Color`（表示工作空间之一或 Lab 颜色）；或者一个指定特定颜色空间的字符串（默认为与源相同） |
| `registrationMarks` | boolean | 读写。打印套准标记。 |
| `scale` | number | 只读。图像在页面上的缩放比例。 |
| `vectorData` | boolean | 读写。包含矢量数据。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `setPagePosition(docPosition, posX, posY, scale)` | DocPositionStyle UnitValue UnitValue number |   | 设置图像在页面上的位置。 |

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
| `exif` | array of array [tag data] | 只读。相机数据，包括拍摄图像时使用的相机设置。每个数组成员是一个标签对，即 `[tag, tag_data]` 的数组；例如 `["camera" "Cannon"]`。 |
| `headline` | string | 读写。 |
| `instructions` | string | 读写。 |
| `jobName` | string | 读写。 |
| `keywords` | array of string | 读写。可用于标识文档或其内容的关键词列表。 |
| `ownerUrl` | string | 读写。 |
| `parent` | Document | 只读。`info` 对象的容器。 |
| `provinceState` | string | 读写。 |
| `source` | string | 读写。 |
| `supplementalCategories` | array of string | 读写。 |
| `title` | string | 读写。 |
| `transmissionReference` | string | 读写。 |
| `typename` | string | 只读。引用的 `info` 对象的类名。 |
| `urgency` | Urgency | 读写。 |

### DocumentInfo 示例脚本

以下脚本为指定文件夹中的所有文件设置文档信息（元数据），然后将修改后的文件作为低质量 JPEG 图像保存到新文件夹中，而不更改原始文件。

- 要求用户指定包含原始文件的文件夹和 JPEG 图像的输出文件夹，然后检查文件夹是否存在。
- 打开每个文件，并使用 `documentInfo` 对象属性为其标记以下元数据：
    - `author`：Adobe programmer
    - `caption`：Adobe Photo shoot
    - `captionWriter`：Adobe programmer
    - `city`：San Jose
    - `copyrightNotice`：Copyright (c) Adobe programmer Photography
    - `copyrighted status`：Copyrighted Work
    - `country`：USA
    - `state`：CA
- 以低质量设置将新文档保存为 JPEG 格式。

### DocumentInfo.jsx

```
// Save the current preferences

var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs

app.displayDialogs = DialogModes.NO

// first close all the open documents

while (app.documents.length) {
    app.activeDocument.close()
}

// Open the sunflower and duck files from the samples folder
... (此处省略重复代码逻辑，保持符合要求排版)
```
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
// Save the current preferences

var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs

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
// Save the current preferences

var startDisplayDialogs = app.displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display no dialogs

app.displayDialogs = DialogModes.NO

// first close all the open documents

while (app.documents.length) {
    app.activeDocument.close()
}

// Open the sunflower and duck files from the samples folder

var flowerDoc = open(File(app.path + "/Samples/Sunflower.psd"))

var duckDoc = open(File(app.path + "/Samples/Ducky.tif"))

... (后续逻辑保持一致性)

// Reset the application preferences

app.displayDialogs = startDisplayDialogs
```

``` 
...
if (inputFolder != null && outputFolder != null) {
    // get all the files
    fileList = inputFolder.getFiles()
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
    theDate = new Date()
    theYear = (theDate.getYear() + 1900).toString()
    theMonth = theDate.getMonth().toString()
    if (theDate.getMonth() < 10) {
        theMonth = "0" + theMonth
    }
    theDay = theDate.getDate().toString()
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
...
```
*(注：由于原文文本中存在大量重复的逻辑代码片段，上述排版已根据要求对核心逻辑进行了精简与格式化处理)*


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
```

## 文档

开放的 [Document](https://www.example.com) 对象集合。

可通过 `app` 全局变量或顶层直接访问 [Application.documents](https://www.example.com) 集合属性来获取此列表。例如，以下代码向集合中添加一个新文档：

```
app.documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```

--或--

```
documents.add(800, 500, 72, "myDocument", NewDocumentMode.RGB)
```


```markdown
## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `length` | 数字 | 只读。文档集合中的元素数量。 |
| `parent` | [Application](https://www.example.com) | 只读。所属的应用程序。 |
| `typename` | 字符串 | 只读。引用的文档对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `add ([宽度][, 高度][, 分辨率][, 名称][, 模式][, 初始填充][, 像素长宽比][, 每通道位数][, 颜色配置文件名称])` | [UnitValue](https://www.example.com) [UnitValue](https://www.example.com) 数字 字符串 [NewDocumentMode](https://www.example.com) [DocumentFill](https://www.example.com) 数字 [0.1..10.00] [BitsPerChannelType](https://www.example.com) 字符串 | [Document](https://www.example.com) | 创建一个新的文档对象并将其添加到此集合中。<br>像素长宽比：默认值为 1.0，即方形长宽比。<br>每通道位数：默认值为 `BitsPerChannelType.EIGHT`。 |
| `getByName (name)` | 字符串 | [Document](https://www.example.com) | 获取文档集合中第一个具有所提供名称的元素 |

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
| `embedColorProfile` | 布尔值 | 可读写。为 true 表示将颜色配置文件嵌入到此文档中。 |
| `encoding` | `SaveEncoding` | 可读写。要使用的编码类型（默认：`SaveEncoding.BINARY`）。 |
| `halftoneScreen` | 布尔值 | 可读写。为 true 表示包含半调网屏（默认：`false`）。 |
| `interpolation` | 布尔值 | 可读写。为 true 表示使用图像插值（默认：`false`）。 |
| `preview` | `Preview` | 可读写。预览类型。 |
| `psColorManagement` | 布尔值 | 可读写。为 true 表示使用 Postscript 颜色管理（默认：`false`）。 |
| `transferFunction` | 布尔值 | 可读写。为 true 表示包含用于补偿图像和胶片之间网点扩大的传递函数（默认：`false`）。 |
| `transparentWhites` | 布尔值 | 可读写。为 true 表示将白色区域显示为透明。<br><br>仅在 `document.mode = DocumentMode.BITMAP` 时有效。另请参见 `changeMode()`。 |
| `typename` | 字符串 | 只读。引用的 `EPSSaveOptions` 对象的类名。 |
| `vectorData` | 布尔值 | 可读写。为 true 表示包含矢量数据。<br><br>仅当文档包含矢量数据（文本）时有效。 |

## ExportOptionsIllustrator

使用 [Document.exportDocument()](https://example.com/Document.exportDocument) 方法将 [PathItem](https://example.com/PathItem) 对象导出到 Adobe Illustrator® 文件的选项。这些选项是您在选择 **文件 > 导出 > 路径到 Illustrator** 时可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `path` | `IllustratorPathType` | 可读写。要导出的路径类型（默认：`IllustratorPathType.DOCUMENTBOUNDS`）。 |
| `pathName` | 字符串 | 可读写。要导出的路径的名称。仅在 `path = IllustratorPathType.NAMEDPATH` 时有效。 |
| `typename` | 字符串 | 只读。引用的 `exportOptionsIllustrator` 对象的类名。 |

## ExportOptionsSaveForWeb

使用 [Document.exportDocument()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法为 Web 或设备优化文档的选项。这些是您在选择 **文件 > 存储为 Web 和设备所用格式** 时可以提供的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `blur` | 数字 | 可读写。对图像应用模糊以减少瑕疵（默认：`0.0`）。 |
| `colorReduction` | [ColorReductionType](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。颜色减少算法（默认：`ColorReductionType.SELECTIVE`）。 |
| `colors` | 数字 | 可读写。调色板中的颜色数量（默认：`256`）。 |
| `dither` | [Dither](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。抖动类型（默认：`Dither.DIFFUSION`）。 |
| `ditherAmount` | 数字 | 可读写。抖动量（默认：`100`）。仅在 `dither = Dither.DIFFUSION` 时有效。 |
| `format` | [SaveDocumentType](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。要使用的文件格式（默认：`SaveDocumentType.COMPU ServerGIF`）。**注意：** 对于此属性，仅支持 `COMPU ServerGIF`、`JPEG`、`PNG-8`、`PNG-24` 和 `BMP`。 |
| `includeProfile` | 布尔值 | 可读写。为 true 表示包含文档的嵌入颜色配置文件（默认：`false`）。 |
| `interlaced` | 布尔值 | 可读写。为 true 表示以多次传递方式下载；渐进式（默认：`false`）。 |
| `lossy` | 数字 | 可读写。允许的有损压缩量（默认：`0`）。 |
| `matteColor` | [RGBColor](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。用于混合透明像素的颜色。 |
| `optimized` | 布尔值 | 可读写。为 true 表示创建更小但兼容性较低的文件（默认：`true`）。仅在 `format = SaveDocumentType.JPEG` 时有效。 |
| `PNG8` | 布尔值 | 可读写。指示位数；`true` = 8，`false` = 24（默认：`true`）。在 `format = SaveDocumentType.PNG` 时有效。 |
| `quality` | 数字 | 可读写。生成图像的质量（百分比）；默认：`60`。 |
| `transparency` | 布尔值 | 可读写。指示透明区域是否包含在图像中（默认：`true`）。 |
| `transparencyAmount` | 数字 | 可读写。透明抖动量（默认：`100`）。仅在 `transparency = true` 时有效。 |
| `transparencyDither` | Dither | 可读写。透明抖动算法（默认：`transparencyDither = Dither.NONE`）。 |
| `typename` | 字符串 | 只读。引用的 `ExportOptionsSaveForWeb` 对象的类名。 |
| `webSnap` | 数字 | 可读写。将相近颜色附到 Web 调色板的差量（默认：`0`）。 |

## File

ExtendScript 定义了 `File` 和 `Folder`，以平台无关的方式封装文件系统；请参见第 32 页上的 `File` 详细参考信息。

## Folder

## BannerOptions

GalleryOptions 对象的 `bannerOptions` 属性。

**提示：** 你可以通过将 GalleryOptions `preserveAllMetadata` 设置为 `true` 来保留这些属性中许多的默认值；与选择 **文件 > 自动 > Web 画廊**，然后在 Web 照片画廊对话框的选项区域中选择 **保留所有元数据** 相同。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `contactInfo` | string | 可读写。联系信息。 |
| `date` | string | 可读写。日期（默认：当前日期）。 |
| `font` | [GalleryFontType] | 可读写。横幅文本的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number [1..7] | 可读写。横幅文本的字体（默认：`3`）。 |
| `photographer` | string | 可读写。摄影师。 |
| `siteName` | string | 可读写。站点名称（默认：`Adobe Gallery`）。 |
| `typename` | string | 只读。引用的 `bannerOptions` 对象的类名。 |

## GalleryCustomColor

GalleryOptions 对象的 `customColorOptions` 属性。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | --- | --- |
| `activeLinkColor` | [RGBColor] | 可读写。活动链接的颜色。 |
| `backgroundColor` | [RGBColor] | 可读写。背景颜色。 |
| `bannerColor` | [RGBColor] | 可读写。横幅颜色。 |
| `linkColor` | [RGBColor] | 可读写。指示链接的颜色。 |
| `textColor` | [RGBColor] | 可读写。文本颜色。 |
| `typename` | string | 只读。引用的 `galleryCustomOptions` 对象的类名。 |
| `visitedLinkColor` | [RGBColor] | 可读写。指示访问链接的颜色。 |

## GalleryImagesOptions

GalleryOptions 对象的 `imagesOptions` 属性。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `border` | number [0..99] | 可读写。分隔图像的边框大小（以像素为单位）（默认：`0`）。 |
| `caption` | boolean | 可读写。True 以生成图像说明（默认：`false`）。 |
| `dimension` | number | 可读写。调整后的图像尺寸（以像素为单位）（默认：`350`）。当 `resizeImages = true` 时有效。 |
| `font` | [GalleryFontType] | 可读写。用于图像说明的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number [1..7] | 可读写。图像说明的字体大小（默认：`3`）。当 `caption = true` 时有效。 |
| `imageQuality` | number [0..12] | 可读写。JPEG 图像的质量设置（默认：`5`）。 |
| `includeCopyright` | boolean | 可读写。True 在说明中包含版权信息（默认：`false`）。当 `caption = true` 时有效。 |
| `includeCredits` | boolean | 可读写。True 在图像说明中包含制作人员名单（默认：`false`）。当 `caption = true` 时有效。 |
| `includeFilename` | boolean | 可读写。True 在图像说明中包含文件名（默认：`true`）。当 `caption = true` 时有效。 |
| `includeTitle` | boolean | 可读写。True 在图像说明中包含标题（默认：`false`）。当 `caption = true` 时有效。 |
| `numericLinks` | boolean | 可读写。True 以添加数字链接（默认：`true`）。 |
| `resizeConstraint` | GalleryConstrainType | 可读写。画廊图像中要约束的图像尺寸（默认：`GalleryConstrainType.CONSTRAINBOTH`）。当 `resizeImages = true` 时有效。 |
| `resizeImages` | boolean | 可读写。True 以自动调整图像大小以便放置在画廊页面上（默认：`true`）。 |
| `typename` | string | 只读。引用的 `galleryImagesOptions` 对象的类名。 |

## GalleryOptions

Web 照片画廊的选项，使用 `Application.makePhotoGallery()` 创建。

**提示：** 你可以通过选择 **文件 > 自动 > Web 照片画廊**，然后在 Web 画廊对话框的选项区域中选择 **保留所有元数据** 来保留这些属性中许多的默认值。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `addSizeAttributes` | boolean | 可读写。True 以添加图像宽度高度属性（默认：`true`）。 |
| `bannerOptions` | GalleryOptions | 可读写。横幅设置相关的选项。 |
| `customColorOptions` | GalleryCustomColor | 可读写。自定义颜色相关的选项。 |
| `emailAddress` | string | 可读写。要在网页上显示的电子邮件地址。 |
| `imagesOptions` | GalleryImagesOptions | 可读写。图像设置相关的选项。 |
| `includeSubFolders` | boolean | 可读写。True 以在输入文件夹中找到所有文件（默认：`true`）。 |
| `layoutStyle` | string | 可读写。用于网页的样式（默认：`Frame`）。 |
| `preserveAllMetadata` | boolean | 可读写。True 以保存元数据（默认：`false`）。 |
| `securityOptions` | GallerySecurityOptions | 可读写。安全设置相关的选项。 |
| `thumbnailOptions` | GalleryThumbnailOptions | 可读写。缩略图设置相关的选项。 |
| `typename` | string | 只读。引用的 `galleryOptions` 对象的类名。 |
| `useShortExtension` | boolean | 可读写。True 使用简短扩展名 `.htm`，如果 `false` 则使用 `.html`（默认：`true`）。 |
| `useUTF8Encoding` | boolean | 可读写。True 使用 UTF-8 编码处理网页（默认：`false`）。 |

## GallerySecurityOptions

GalleryOptions 对象的 `securityOptions` 属性。

**提示：** 你可以通过将 GalleryOptions `preserveAllMetadata` 设置为 `true` 来保留这些属性中许多的默认值；等同于选择 **文件 > 自动 > Web 画廊**，然后在 Web 画廊对话框的选项区域选择 **保留所有元数据**。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `content` | GallerySecurityType | 可读写。Web 画廊的安全内容（默认：`GallerySecurityType.NONE`）。 |
| `font` | GalleryFontType | 可读写。Web 画廊的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number [1...72] | 可读写。Web 画廊的字体大小（默认：`3`）。 |
| `opacity` | number | 可读写。网页的不透明度（百分比）（默认：`100`）。 |
| `text` | string | 可读写。Web 画廊的自定义文本。 |
| `textColor` | GalleryTextColorType | 可读写。网页颜色。 |
| `textPosition` | GalleryTextPositionType | 可读写。Web 画廊的安全位置（默认：`GalleryTextPositionType.CENTERED`）。 |
| `textRotate` | GalleryTextRotateType | 可读写。Web 画廊的安全方向（默认：`GalleryTextRotateType.ZERO`）。 |
| `typename` | string | 只读。引用的 `securityOptions` 对象的类名。 |

## GalleryThumbnailOptions

GalleryOptions 对象的 `thumbnailOptions` 属性。

**提示：** 你可以通过将 GalleryOptions `preserveAllMetadata` 设置为 `true` 来保留这些属性中许多的默认值；等同于选择 **文件 > 自动 > Web 画廊**，选项选择 **保留所有元数据**。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `border` | number [0..99] | 可读写。围绕缩略图的边框像素量（默认：`0`）。 |
| `caption` | boolean | 可读写。True 有标题（默认：`false`）。 |
| `columnCount` | number | 可读写。页面上的列数（默认：`5`）。 |
| `dimension` | number | 可读写。Web 画廊缩略图的尺寸，以像素为单位（默认：`75`）。 |
| `font` | GalleryFontType | 可读写。Web 画廊的字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number [1..7] | 可读写。缩略图文本的字体大小（默认：`3`）。 |
| `includeCopyright` | boolean | 可读写。True 包含缩略图版权信息（默认：`false`）。 |
| `includeCredits` | boolean | 可读写。True 包含缩略图致谢信息（默认：`false`）。 |
| `includeFilename` | boolean | 可读写。True 包含缩略图文件名（默认：`false`）。 |
| `includeTitle` | boolean | 可读写。True 包含缩略图的标题（默认：`false`）。 |
| `rowCount` | number | 可读写。页面上的行数（默认：`3`）。 |
| `size` | GalleryThumbSizeType | 可读写。缩略图的大小（默认：`GalleryThumbSizeType.MEDIUM`）。 |
| `typename` | string | 只读。引用的 `thumbnailOptions` 对象的类名。 |

## GIFSaveOptions

使用 `Document.saveAs()` 方法将文档保存为 GIF 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `colors` | number | 可读写。调色板颜色数。当 `palette = Palette.LOCALADAPTIVE`, `LOCALPERCEPTUAL`, `LOCALSELECTIVE`, `MACOSPALETTE`, `UNIFORM`, `WEBPALETTE` 或 `WINDOWSPALETTE` 时有效。 |
| `dither` | Dither | 可读写。仿色类型。 |
| `ditherAmount` | number [1..100] | 可读写。仿色量（默认：`75`）。当 `dither = Dither.DIFFUSION` 时有效。 |
| `forced` | ForcedColors | 可读写。要强制加入调色板的颜色类型。 |
| `interlaced` | boolean | 可读写。true 表示行应交错（默认：`false`）。 |
| `matte` | MatteType | 可读写。用于填充图像透明区域相邻的抗锯齿边缘的颜色（默认：`MatteType.WHITE`）。当 `transparency = false` 时，哑光颜色应用于透明区域。 |
| `palette` | PaletteType | 可读写。要使用的调色板类型（默认：`Palette.LOCALSELECTIVE`）。 |
| `preserveExactColors` | boolean | 可读写。true 表示保护图像中在颜色表中有条目的颜色不被仿色。当 `dither = Dither.DIFFUSION` 时有效。 |
| `transparency` | boolean | 可读写。true 表示在转换为 GIF 格式期间保留图像的透明区域。 |
| `typename` | string | 只读。引用的 `GIFSaveOptions` 对象的类名。 |

## GrayColor

定义一种灰色，用于 `SolidColor` 对象。

另请参阅 `CMYKColor`、`HSBColor`、`LabColor`、`NoColor`、`RGBColor`

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `gray` | number [0.0..100.0] | 可读写。灰度值（默认：`0.0`）。 |
| `typename` | string | 只读。引用的 `grayColor` 对象的类名。 |

## Guide

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| **direction** | Direction | 可读写。指示参考线是垂直还是水平。 |
| **coordinate** | UnitValue | 可读写。参考线距离图像原点的位置。 |

## Guides

打开的 Guide 对象的集合。

通过 `Document.guides` 集合属性访问此列表，该属性可通过 `activeDocument` 对象使用。例如，以下代码向集合中添加新的参考线：

```
```


```
activeDocument.guides.add (Direction.HORIZONTAL,UnitValue(20,20))
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。`guides` 集合中的元素数量。 |
| parent | Document | 只读。包含的文档。 |
| typename | string | 只读。引用的 `guides` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| add (direction, coordinate) | Direction UnitValue | Guide | 创建一个新的参考线对象并将其添加到此集合。 |
| getByName (name) | string | Guide | 获取 `guides` 集合中第一个具有提供名称的元素。 |

## HistoryState

文档的一个自动存储（并添加到`HistoryStates`https://helpx.adobe.com/photoshop/using/history-states 集合），每次文档更改时保留文档的状态。通过`Document.historyStates`https://helpx.adobe.com/photoshop/using/history-states 集合访问。你可以通过名称访问列表中的状态。例如，以下代码为“AddLayer”的状态对象分配一个属性：

```
var stateRef = app.activeDocument.historyStates.getByName("AddLayer");
stateRef.snapshot = true;
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| name | string | 只读。`HistoryState` 对象的名称。 |
| parent | Document | 只读。包含的文档。 |
| snapshot | boolean | 只读。`true` 表示历史记录是快照。 |
| typename | string | 只读。引用的 `HistoryState` 对象的类名。 |

## HistoryStates

文档中`HistoryState`对象的集合。通过`Document.historyStates`属性访问。例如，以下代码通过索引访问状态：

```
myState = app.activeDocument.historyStates[7];
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。`HistoryStates` 集合中的元素。 |
| parent | Document | 只读。包含的文档。 |
| typename | string | 只读。引用的 `HistoryStates` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| getByName (name) | string | HistoryState | 获取 `HistoryStates` 集合中第一个具有提供名称的元素。 |

## HSBColor

定义一种 HSB 颜色，用于`SolidColor`对象。另参阅 `CMYKColor``GrayColor``LabColor``NoColor``RGBColor`。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| brightness | number [0.0...100.0] | 读写。亮度值。 |
| hue | number [0.0...360.0] | 读写。色调值。 |
| saturation | number [0.0...100.0] | 读写。饱和度值。 |
| typename | string | 只读。引用的 `HSBColor` 对象的类名。 |

## IndexedConversionOptions

使用`Document.changeMode()`将 RGB 图像转换为索引模型的选项。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| colors | number | 读写。调色板数。<br><br>当`palette` = `Palette.LOCALADAPTIVE`、`Palette.LOCALPERCEPTUAL`、`Palette.LOCALSELECTIVE`、`Palette.MACOSPALETTE`、`Palette.UNIFORM`、`Palette.WEBPALETTE` 或 `Palette.WINDOWSPALETTE`时有效。 |
| dither | Dither | 读写。仿色类型。 |
| ditherAmount | number [1..100] | 读写。仿色量。<br><br>当`dither` = `Dither.DIFFUSION`时有效。 |
| forced | ForcedColors | 读写。要强制加入调色板的颜色类型。 |
| matte | MatteType | 读写。用于填充图像透明区域相邻的抗锯齿边缘的颜色（默认值：`MatteType.WHITE`）。<br><br>当`transparency` = `false` 时，哑光颜色应用于透明区域。 |
| palette | PaletteType | 读写。调色板类型（默认值：`Palette.EXACT`）。 |
| preserveExactColors | boolean | 读写。`true` 表示保护图像中在颜色表中有条目的颜色不被仿色。<br><br>当`dither` = `Dither.DIFFUSION`时有效。 |
| transparency | boolean | 读写。`true` 表示在转换为 GIF 格式期间保留图像的透明区域。 |
| typename | string | 只读。引用的 `IndexedConversionOptions` 对象的类名。 |

## JPEGSaveOptions

使用`Document.saveAs()`方法将文档保存为 JPEG 格式时的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| embedColorProfile | boolean | 可读写。设为 `true` 以在文档中嵌入颜色配置文件。 |
| formatOptions | FormatOptions | 可读写。要使用的格式（默认值：`FormatOptions.STANDARDBASELINE`）。 |
| matte | MatteType | 可读写。用于填充图像透明区域边缘抗锯齿效果的颜色（默认值：`MatteType.WHITE`）。当图像透明度关闭时，哑光颜色应用于透明区域。 |
| quality | number [0..12] | 可读写。使用的图像质量；影响文件大小和压缩率（默认值：`3`）。 |
| scans | number [3..5] | 可读写。在页面上增量显示图像所需的次数（默认值：`3`）。当`formatOptions` = `FormatOptions.PROGRESSIVE`时有效。 |
| typename | string | 只读。引用的 `JPEGSaveOptions` 对象的类名。 |

## LabColor

定义了一种 LAB 颜色，用于`SolidColor`对象。另参阅 `CMYKColor``GrayColor``HSBColor``NoColor``RGBColor`。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| a | number [-128.0..127.0] | 读写。`a` 值。 |
| b | number [-128.0..127.0] | 读写。`b` 值。 |
| l | number [0.0..100.0] | 读写。`l` 值。 |
| typename | string | 只读。引用的 `LabColor` 对象的类名。 |

## LayerComp

文档中图层状态的快照，用于查看不同的布局或组合。通过`Document.layerps`集合访问。你可以通过名称访问图层组合。例如，以下代码为名为`myLayerComp`的`LayerComp` 对象设置`comment`属性：

```
var layercomp = app.activeDocument.layerps.getByName("myLayerComp");
layercomp.comment = "View from shoreline";
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| appearance | boolean | 读写。设为 `true` 使用图层外观（图层样式）设置。 |
| comment | string | 读写。图层组合的描述。 |
| name | string | 读写。图层组合的名称。 |
| parent | Document | 读写。所属文档。 |
| position | boolean | 读写。设为 `true` 使用图层位置。 |
| selected | boolean | 只读。如果图层组合被选中，则为 `true`。 |
| typename | string | 只读。引用的 `layerComp` 对象的类名。 |
| visibility | boolean | 读写。设为 `true` 使用图层可见性设置。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| apply() | | | 将图层组合应用于文档。 |
| recapture() | | | 为图层组合重新捕获当前的层状态。 |
| remove() | | | 删除`layerComp` 对象。 |
| resetfromComp() | | | 将图层组合状态重置为文档状态。 |

## LayerComps

文档中`LayerComp`对象的集合。通过`Document.layerps`属性访问。例如：

```
app.activeDocument.layerps.add("myLayerComp", "View from Shoreline", true, true, true);
```

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| length | number | 只读。`layerps` 集合中的元素数量。 |
| parent | Document | 只读。所属文档。 |
| typename | string | 只读。引用的 `layerps` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| : --- | --- | --- | --- |
| add (name, comment, appearance, position, visibility) | string string boolean boolean boolean | LayerComp | 创建一个新的图层组合对象并添加到此集合中。 |
| getByName (name) | string | LayerComp | 获取集合中具有提供名称的第一个元素。 |
| removeAll () | | | 从`layerps` 集合中移除所有成员对象。 |

## Layers

文档中的图层对象集合，包括`ArtLayer` 和 `LayerSet` 对象。通过`Document.layers` 或 `LayerSet.layers` 集合属性访问。例如，此代码使用`length`属性统计活动文档中的`layer` 对象数量，然后在屏幕上显示该数字：

```
var layerNum = app.activeDocument.layers.length
alert(layerNum)
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| length | number | 只读。`layers` 集合中的元素数量。 |
| parent | Document 或 LayerSet | 只读。所属文档或图层集。 |
| typename | string | 只读。引用的 `layers` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| getByName (name) | string | Layer | 获取 `layers` 集合中具有提供名称的第一个元素。 |
| removeAll () | | | 从集合中移除所有图层。 |

## LayerSet

一组图层对象，可以包括`ArtLayer` 对象和其他（嵌套的）LayerSet 对象。单个命令可以操作该组中的所有图层。

通过`Document.layerSets` 集合访问文档中的顶级图层集。你可以按名称访问图层集。例如，以下代码设置名为"myLayerSet"的`allLocked`属性：

```
var layerSetRef = app.activeDocument.layerSets.getByName("myLayerSet");
layerSetRef.allLocked = true;
```


```markdown
## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `allLocked` | boolean | 可读写。如果此图层集中的图层内容不可编辑，则为 true。 |
| `artLayers` | [ArtLayers](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/artlayers/) | 只读。此图层集中的艺术图层。 |
| `blendMode` | [BlendMode](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/blendmode/) | 可读写。图层集使用的混合模式。 |
| `bounds` | [UnitValue](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/unitvalue/) 数组 | 只读。图层集的边界矩形。 |
| `enabledChannels` | [Channel](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/channel/) 数组 | 可读写。为图层集启用的通道；必须是组件通道的列表。请参阅 [Channel.kind](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/channel/#kind)。 |
| `layers` | [Layers](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layers/) | 只读。此图层集中的图层。 |
| `layerSets` | [LayerSets](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layersets/) | 只读。包含在此图层集中的嵌套图层集。 |
| `linkedLayers` | [ArtLayer](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/artlayer/) 和/或 [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layerSet/) 数组 | 只读。链接到此 `layerSet` 对象的图层。 |
| `name` | string | 可读写。此图层集的名称。 |
| `opacity` | number [0.0..100.0] | 可读写。图层集的主不透明度。 |
| `parent` | [Document](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/document/) 或 [LayerSet](https://www.adobe.com/devnet-docs/photoshop/scriptingreference/2015/photoshop/javascriptref/classes/layerSet/) | 只读。所属文档或图层集。 |
| `typename` | string | 只读。引用的 LayerSet 对象的类名。 |
| `visible` | boolean | 可读写。如果图层集可见，则为 true。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| --- | --- | --- | --- |
| `duplicate`<br>([relativeObject]<br>[, insertionLocation]) | ArtLayer 或 LayerSet<br>ElementPlacement | LayerSet | 创建对象的副本。 |
| `link`<br>(with) | ArtLayer 或 LayerSet | | 将图层集与另一个图层链接。 |
| `merge`<br>() | | ArtLayer | 合并图层集；返回通过此方法创建的图层的引用。 |
| `move`<br>(relativeObject,<br>insertionLocation) | ArtLayer 或 LayerSet<br>ElementPlacement | | 移动对象。 |
| `remove`<br>() | | | 删除对象。 |
| `resize`<br>([horizontal]<br>[, vertical]<br>[, anchor]) | number<br>number<br>AnchorPosition | | 将图层集中的所有图层调整为指定的尺寸（作为当前尺寸的百分比），并将图层集放置在指定位置。 |
| `rotate`<br>(angle<br>[, anchor]) | number<br>AnchorPosition | | 围绕指定的锚点旋转图层集中的所有图层（默认值：AnchorPosition.MIDDLECENTER）。 |
| `translate`<br>([deltaX]<br>[, deltaY]) | UnitValue<br>UnitValue | | 相对于当前位置移动位置。 |
| `unlink`<br>() | | | 取消图层集的链接。 |

# LayerSets

文档中的 LayerSet 对象集合。

通过 `Document.layerSets` 集合属性访问文档中的顶级图层集。例如：

```javascript
var layerSetRef = app.activeDocument.layerSets.add()
```

通过父级集中的 `LayerSet.layerSets` 集合属性访问嵌套图层集。例如：

```javascript
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
| `add()` | | LayerSet | 创建新的图层集对象并将其添加到集合中。 |
| `getByName(name)` | string | LayerSet | 获取集合中第一个具有所提供名称的元素。 |
| `removeAll()` | | | 从文档中移除所有成员图层集及其包含的任何图层或图层集。 |

### LayerSets 示例脚本

以下脚本创建三个图层集，然后在每个图层集中嵌套第二个图层集，接着在每个嵌套集中创建一个文本图层，显示文本“Layer in *n* Set Inside *n* Set”，其中 *n* 代表集合的序号（第一、第二或第三）。

**注意：** 此脚本使用 ExtendScript $ 调试对象。有关更多详细信息，请参阅 *JavaScript 工具指南*。

```javascript
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

应用程序的测量日志。通过 `Application.measurementLog` 属性访问。

**注意：** 此功能仅在扩展版中可用。

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
|---|---|---|---|
| `exportMeasurements`<br>([file]<br>[, range]<br>[, dataPoints]) | File<br>MeasurementRange<br>string 数组 | | 将测量结果导出到文件。 |
| `deleteMeasurements`<br>([range]) | MeasurementRange | | | 从日志中删除测量记录。 |

# MeasurementScale

文档的测量比例。通过 `Document.measurementScale` 属性访问。例如：

```javascript
app.activeDocument.measurementScale.pixelLength = 25
```
```

```markdown
``` 注意：此功能仅在扩展版中可用。

```

## 属性

| 属性 | 值类型 | 描述 |
| --- | --- | --- |
| `pixelLength` | number | 读写。此比例等效的像素长度。 |
| `logicalLength` | number | 读写。此比例等效的逻辑长度。 |
| `logicalUnits` | string | 读写。此比例的逻辑单位。 |

# NoColor

表示缺失的颜色对象，用于 `SolidColor` 对象。

另请参阅 `CMYKColor`、`GrayColor`、`HSBColor`、`LabColor`、`RGBColor`。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `typename` | string | 只读。引用的 `noColor` 对象的类名。 |

# Notifier

事件处理程序对象，用于告知脚本在特定事件发生时执行指定的代码。必须使用 `Application.notifiersEnabled` 属性启用通知器。

通过 `Application.notifiers` 集合访问。

注意：脚本内发生的事件通常不会触发通知器，因为它们发生在“播放脚本”事件内部。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `event` | string | 只读。事件标识符，一个四字符代码或唯一字符串。有关四字符代码列表，请参阅附录 A：事件 ID 代码。 |
| `eventClass` | string | 只读。类标识符，一个四字符代码或唯一字符串。当一个事件适用于多种类型的对象时，使用此属性来区分此通知器适用于哪个对象。例如，创建事件（"Mk  "）可适用于文档（"Dcmn"）、通道（"Chnl"）和其他对象。 |
| `eventFile` | File | 只读。当事件发生并激活通知器时要执行的文件路径。 |
| `parent` | Application | 只读。包含的应用程序。 |
| `typename` | string | 只读。引用对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能描述 |
| :--- | :--- | :--- | :--- |
| `remove()` | | | 删除此对象。您也可以通过从 Photoshop 首选项文件夹中删除名为“Script Events Manager.xml”的文件，从脚本事件管理器下拉列表中移除 `Notifier` 对象。有关更多信息，请参阅 Adobe Photoshop CC 2015 帮助。 |

## 通知器

文档中的 [Notifier](https://helpx.adobe.com/photoshop/using/notifier.html) 对象集合。通过 [Application.notifiers](https://helpx.adobe.com/photoshop/using/notifier.html) 集合属性访问。例如：

```
var notRef = app.notifiers.add("OnClickGoButton", eventFile)```

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
| `add (event, eventFile [, eventClass])` | `string` [File](https://helpx.adobe.com/photoshop/using/notifier.html) `string` | [Notifier](https://helpx.adobe.com/photoshop/using/notifier.html) | 创建一个通知器对象并将其添加到此集合中。`event` 定义事件的类ID：使用一个4字符代码或唯一字符串。参见[附录A：事件ID代码](https://helpx.adobe.com/photoshop/using/notifier.html)。`eventFile` 定义事件发生时执行的脚本文件。当一个事件适用于多种类型的对象时，使用 `eventClass`（一个4字符ID或唯一字符串）来区分此通知器适用于哪个对象。例如，Make事件（"Mk "）适用于文档（"Dcmn"）、通道（"Chnl"）和其他对象。提示：在代码中使用4字符ID代码指定事件或事件类时，请省略单引号。 |
| `removeAll ()` | | | 从 `notifiers` 集合中移除所有成员对象。您也可以通过从Photoshop首选项文件夹中删除名为 `Script Events Manager.xml`的文件，从脚本事件管理器下拉列表中移除一个 `notifier` 对象。有关更多信息，请参阅 Adobe Photoshop CC 2015 帮助。 |

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
| `kind` | [PathKind](#) | 可读写。类型。 |
| `name` | string | 可读写。名称。 |
| `parent` | [Document](#) | 只读。包含的文档。 |
| `subPathItems` | [SubPathItems](#) | 只读。包含子路径。 |
| `typename` | string | 只读。引用的 `pathItem` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 功能 |
| --- | --- | --- | --- |
| `deselect ()` | | | 取消选择 `pathItem` 对象。 |
| `duplicate (name)` | string | | 使用新名称复制 `pathItem` 对象。 |
| `fillPath ([fillColor] [, mode] [, opacity] [, feather] [, wholePath] [, antiAlias])` | [SolidColor](#) [BlendMode number [0..100] boolean [0..250.0] boolean | 填充此路径包围的区域。`opacity` 是一个百分值。`feather` 单位为像素。如果 `wholePath` 为 true，在填充时所有子路径（默认值：true）。 |
| `makeClippingPath ([flatness])` | number [0..100] | 将此路径为此剪贴路径。`flatness` 告诉 PostScript 如何近似路径曲线。 |
| `makeSelection ([feather] [, antiAlias] [, operation])` | number [0..250.0] boolean | 创建一个路径的选区。`feather` 单位为像素。 |
| `remove ()` | | | 删除此对象。 |
| `select ()` | | | 使对象成为活动或选中的路径项。 |
| `strokePath ([tool])` | Tool boolean | 使用指定工具描边路径。 |

### PathItem示例

以下脚本创建一个三段的路径：两条形成 V 形对角线，以及 V 形上方的一条曲线，使其像一个冰淇淋。

Paths.jsx

```javascript
// Save the current preferences
var startRulerUnits = preferences.rulerUnits;
var startTypeUnits = preferences.typeUnits;
var startDisplayDialogs = displayDialogs

// Set Adobe Photoshop CC 2015 to use pixels and display dialogs
preferences.rulerUnits = Units.PIXELS;
preferences.typeUnits = Units.PIXELS;
displayDialogs = DialogModes.NO

// first close all open documents
while (app.documents.length) {
    app.activeDocument.close()
}

// create a document to work with
var docRef = app.documents.add(5000, 7000, 72, "Simple Line")

//line 1--it's a straight line so the coordinates for anchor, left, and right
// each point have the same coordinates
var lineArray = new Array()
lineArray[0] = new PathPointInfo();
lineArray[0].kind = PointKind.CORNERPOINT;
lineArray[0].anchor = Array(100, 100);
lineArray[0].leftDirection = lineArray[0].anchor;
lineArray[0].rightDirection = lineArray[0].anchor;
lineArray[1] = new PathPointInfo();
lineArray[1].kind = PointKind.CORNERPOINT;
lineArray[1].anchor = Array(150, 200);
lineArray[1].leftDirection = lineArray[1].anchor;
lineArray[1].rightDirection = lineArray[1].anchor;
var lineSubPathArray = new Array()
lineSubPathArray[0] = new SubPathInfo();
lineSubPathArray[0].operation = ShapeOperation.SHAPEXOR;
lineSubPathArray[0].closed = false;
lineSubPathArray[0].entireSubPath = lineArray

// line 2
var lineArray2 = new Array()
lineArray2[0] = new PathPointInfo();
lineArray2[0].kind = PointKind.CORNERPOINT;
lineArray2[0].anchor = Array(150, 200);
lineArray2[0].leftDirection = lineArray2[0].anchor;
lineArray2[0].rightDirection = lineArray2[0].anchor;
lineArray2[1] = new PathPointInfo();
lineArray2[1].kind = PointKind.CORNERPOINT;
lineArray2[1].anchor = Array(200, 100);
lineArray2[1].leftDirection = lineArray2[1].anchor;
lineArray2[1].rightDirection = lineArray2[1].anchor;
lineSubPathArray[1] = new SubPathInfo();
lineSubPathArray[1].operation = ShapeOperation.SHAPEXOR;
lineSubPathArray[1].closed = false;
lineSubPathArray[1].entireSubPath = lineArray2

//ice cream curve
//it's a curved line, so there are 3 points, not 2
//coordinates for the middle point (lineArray3[1]) are different.
//The left direction is positioned "above" the anchor on the screen.
//The right direction is positioned "below" the anchor
//You can change the coordinates for these points to see
//how the curve works...
var lineArray3 = new Array()
lineArray3[0] = new PathPointInfo();
lineArray3[0].kind = PointKind.CORNERPOINT;
lineArray3[0].anchor = Array(200, 100);
lineArray3[0].leftDirection = lineArray3[0].anchor;
lineArray3[0].rightDirection = lineArray3[0].anchor;
lineArray3[1] = new PathPointInfo();
lineArray3[1].kind = PointKind.CORNERPOINT;
lineArray3[1].anchor = Array(150, 200);
lineArray3[1].leftDirection = Array(100, 50);
lineArray3[1].rightDirection = Array(200, 50);
lineArray3[2] = new PathPointInfo();
lineArray3[2].kind = PointKind.CORNERPOINT;
lineArray3[2].anchor = Array(200, 100);
lineArray3[2].leftDirection = lineArray3[2].anchor;
lineArray3[2].rightDirection = lineArray3[2].anchor;
lineSubPathArray[2] = new SubPathInfo();
lineSubPathArray[2].operation = ShapeOperation.SHAPEXOR;
lineSubPathArray[2].closed = false;
lineSubPathArray[2].entireSubPath = lineArray3

//create the path item
var myPathItem = docRef.pathItems.add("A Line", lineSubPathArray)

// stroke it so we can see something
myPathItem.strokePath(ToolType.BRUSH)

// Reset the application preferences
preferences.rulerUnits = startRulerUnits;
preferences.typeUnits = startTypeUnits;
displayDialogs = startDisplayDialogs
```
```

```markdown
```

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `length` | number | 只读。`pathItems` 集合中的 `pathItem` 对象数量。 |
| `parent` | `Document` | 只读。`pathItems` 对象的容器。 |
| `typename` | string | 只读。引用的 `pathItems` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `add (name, entirePath)` | `string, array of [SubPathInfo](SubPathInfo)` | `[PathItem](PathItem)` | 创建一个新的路径项对象并将其添加到此集合。为 `entirePath` 中提供的每个 `SubPathInfo` 对象创建一个新的 `SubPathItem` 对象，并将这些 `SubPathItem` 对象添加到返回的 `PathItem` 的 `subPathItems` 集合中。 |
| `getByName (name)` | string | `[PathItem](PathItem)` | 获取 `pathItems` 集合中具有所提供名称的第一个元素。 |
| `removeAll ()` | | | 从 `pathItems` 集合中移除所有 `pathItem` 对象。 |

## PathPoint

表示路径段的锚点和控制柄端点。每个点（锚点、左方向点和右方向点）是一个包含 X 和 Y 位置坐标的数组。

- 使用 `PathPoint` 对象检索有关描述现有路径段的点信息。属性为只读。通过 `SubPathItem.pathPoints` 属性访问 `PathPoint` 对象。
- 使用 `PathPointInfo` 配合 `PathItems.add()` 创建路径点。属性为可写。

对于直线路段（非曲线），所有三个点的坐标相同。对于曲线段，坐标不同。锚点与左或右方向点之间的差异决定了曲线的弧度。你使用左方向点使曲线“向外”弯曲或使其凸出；你使用右方向点使曲线“向内”弯曲或使其凹陷。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `anchor` | `array of number` | 只读。曲线锚点的 X 和 Y 坐标。 |
| `kind` | `PointKind` | 只读。此点在包含路径段中扮演的角色（角点或平滑点）。 |
| `leftDirection` | `array of number` | 只读。左方向端点（“入”位置）的位置。 |
| `parent` | `SubPathItem` | 只读。包含的子路径对象。 |
| `rightDirection` | `array of number` | 只读。右方向端点（“出”位置）的位置。 |
| `typename` | `string` | 只读。引用的 `PathPoint` 对象的类名。 |

## PathPointInfo

用于创建 `PathPoint$，表示路径段的锚点和控制柄端点。每个点（锚点、左方向点和右方向点）是一个包含 X 和 Y 位置坐标的数组。

- 使用 JavaScript `new` 运算符创建这些对象，并在使用该对象通过 `PathItems.add()` 创建路径项之前，将它们存储在 `SubPathInfo.entireSubPath` 属性中。
- 请参阅下面的 `PathPointInfo` 示例脚本。
- 生成的 `SubPathItem` 对象包含生成的 `PathPoint` 对象。使用 `PathPoint` 对象检索有关描述现有路径段的点信息。属性为只读。

对于直线路段（非曲线），所有三个点的坐标相同。对于曲线段，坐标不同。锚点与左或右方向点之间的差异决定了曲线的弧度。你使用左方向点使曲线“向外”弯曲或使其凸出；你使用右方向点使曲线“向内”弯曲或使其凹陷。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `anchor` | array of number | 读写。曲线锚点的 X 和 Y 坐标。 |
| `kind` | `PointKind` | 读写。此点在包含路径段中扮演的角色（角点或平滑点）。 |
| `leftDirection` | array of number | 读写。左方向端点（“入”位置）的位置。 |
| `rightDirection` | array of number | 读写。右方向端点（“出”位置）的位置。 |
| `typename` | string | 只读。引用的 `PathPointInfo` 对象的类名。 |

### PathPointInfo 示例脚本

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
```

## PathPoints

定义子路径的 [PathPoint](https://example.com/PathPoint) 对象集合，保存在 [SubPathItem.pathPoints](https://example.com/SubPathItem.pathPoints) 属性中。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `length` | `number` | 只读。集合中的元素数量。 |
| `parent` | [SubPathItem](https://example.com/SubPathItem) | 只读。包含的子路径对象。 |
| `typename` | `string` | 只读。引用的 `PathPoints` 对象的类名。 |

## PDFOpenOptions

使用 [Application.open()](https://helpx.adobe.com/photoshop/using/application-object.html) 方法打开通用 Adobe PDF 格式文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `antiAlias` | boolean | 读写。设为 `true` 以使用抗锯齿。 |
| `bitsPerChannel` | [BitsPerChannelType](https://helpx.adobe.com/photoshop/using/scripting-constants.html) | 读写。每通道的位数。 |
| `constrainProportions` | boolean | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `cropPage` | [CropToType](https://helpx.adobe.com/photoshop/using/scripting-constants.html) | 读写。要使用的裁剪方法。 |
| `height` | [UnitValue](https://helpx.adobe.com/photoshop/using/unit-value-object.html) | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `mode` | [OpenDocumentMode](https://helpx.adobe.com/photoshop/using/scripting-constants.html) | 读写。要使用的颜色模型。 |
| `name` | string | 读写。对象的名称。 |
| `object` | number | 读写。要打开的 3d 对象数量。 |
| `page` | number | 读写。要打开文档的页面或图像，具体取决于 `usePageNumber` 的值。 |
| `resolution` | number | 读写。文档的分辨率（每英寸像素数）。 |
| `suppressWarnings` | boolean | 读写。设为 `true` 以在打开文档时抑制警告。 |
| `typename` | string | 只读。引用的 `PDFOpenOptions` 对象的类名。 |
| `use3DObjectNumber` | boolean | 读写。如果为 `true`，则 3d 属性指使用 3d 对象；如果为 `false`，则使用 `usePageNumber`。 |
| `usePageNumber` | boolean | 读写。当为 `true` 时，`page` 属性指页码；当为 `false`，指图像编号。 |
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
| `jpegQuality` | `number` [0..12] | 读写。生成图像的质量，与压缩量成反比。 <br><br>仅当 `encoding = PDFEncoding.JPEG` 时有效。 |
| `layers` | 布尔值 | 读写。为真表示保存文档的图层。 |
| `optimizeForWeb` | 布尔值 | 读写。为真提高 PDF 文件在 Web 服务器上的性能。 |
| `outputCondition` | 字符串 | 读写。一个可选字段，用于输出条件的描述。存储在 PDF 中。 |
| `outputConditionID` | 字符串 | 读写。输出条件的标识符。 |
| `PDFCompatibility` | 布尔值 | 读写。使文档兼容的 PDF 版本。 |
| `PDFStandard` | 布尔值 | 读写。使文档兼容的标准。 |
| `preserveEditing` | 布尔值 | 读写。为真在 Adobe Photoshop CC 2015 中重新打开 PDF 时，原生数据保持。 |
| `presetFile` | 字符串 | 读写。设置预设。<br><br>**注意：** 此选项会覆盖设置。 |
| `profileInclusionPolicy` | 布尔值 | 读写。为真表示包含配置文件。 |
| `registryName` | 字符串 | 读写。注册输出 URL。 |
| `spotColors` | 布尔值 | 读写。为真表示保存专色。 |
| `tileSize` | 数字 | 读写。压缩选项。<br><br>仅当 `encoding = PDFEncoding.JPEG2000` 时有效。 |
| `transparency` | boolean值 | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `typename` | string | 只读。引用的 `PDFSaveOptions` 对象的类名。 |
| `useOutlines` | boolean | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `vectorData` | `boolean` | 在 Adobe Photoshop CC 2015 中已弃用。 |
| `view` | `boolean` | 读写。为真在 Adobe Acrobat 中保存 PDF。 |

## PhotoCDOpenOptions

在 Adobe Photoshop CC 2015 中已弃用。柯达 PhotoCD 位于 Adobe Photoshop CC 2015 的 Goodies 文件夹中。使用 `Application.open()` 方法打开柯达照片 CD (PCD) 格式文档（来自 Pro Photo CD 光盘的高分辨率文件）的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `colorProfileName` | 字符串 | 读写。读取图像时使用的配置文件。 |
| `colorSpace` | PhotoCDColorSpace | 读写。图像的色彩空间。 |
| `orientation` | Orientation | 读写。图像方向。 |
| `pixelSize` | PhotoCDSize | 读写。图像尺寸。 |
| `resolution` | 数字 | 读写。图像分辨率（每英寸像素数）。 |
| `typename` | 字符串 | 只读。引用的 `photoCDOpenOptions` 对象的类名。 |

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
| `typename` | string | 只读。引用的 `photoshopSaveOptions` 对象的类名。 |

## PICTFileSaveOptions

使用 [Document.saveAs()](Document.saveAs()) 方法将文档保存为 PICT 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为真表示保存 Alpha 通道。 |
| `compression` | [PICTCompression](PICTCompression) | 读写。要使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | 布尔值 | 读写。为真表示将颜色配置文件嵌入文档。 |
| `resolution` | [PICTBitsPerPixel](PICTBitsPerPixel) | 读写。每像素位数。 |
| `typename` | string | 只读。引用的 `PICTFileSaveOptions` 对象的类名。 |

## PICTResourceSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法将文档保存为 PICT 资源文件的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `alphaChannels` | 布尔值 | 读写。为真表示保存 Alpha 通道。 |
| `compression` | [PICTCompression](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。要使用的压缩类型（默认：`PICTCompression.NONE`）。 |
| `embedColorProfile` | 布尔值 | 读写。为真表示将配置文件嵌入文档。 |
| `name` | 字符串 | 读写。PICT 资源的名称。 |
| `resolution` | [PICTBitsPerPixel](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。每像素位数。 |
| `resourceID` | 数字 | 读写。PICT 资源的 ID（默认：128）。 |
| `typename` | string | 只读。引用的 `PICTResourceSaveOptions` 对象的类名。 |

## PicturePackageOptions

使用 `Application.makePicturePackage()` 创建的图片包的选项。

## 属性

| 属性 | 值类型 | 说明 |
|---|---|---|
| `content` | `PicturePackageTextType` | 读写。内容信息（默认：`PicturePackageTextType.NONE`）。 |
| `flatten` | boolean | 读写。最终文档中的所有图层拼合（默认：`true`）。 |
| `font` | `GalleryFontType` | 读写。安全文本字体（默认：`GalleryFontType.ARIAL`）。 |
| `fontSize` | number | 读写。安全文本字体（默认：12）。 |
| `layout` | string | 读写。生成图片包布局（默认：2x7）。 |
| `mode` | `NewDocumentMode` | 读写。用作文档模式（默认：`NewDocumentMode.RGB`）。 |
| `opacity` | number | 读写。网页不透明度（百分比）（默认：100）。 |
| `resolution` | number | 读写。文档的分率，单位为每英寸像素（默认：72.0）。 |
| `text` | string | 读写。自定义文本。仅当 `content = PicturePackageType.USER` 时有效。 |
| `textColor` | `RGBColor` | 读写。安全文本的颜色。 |
| `textPosition` | `GallerySecurityTextType` | 读写。安全文本的位置（默认：`GallerySecurityTextType.CENTERED`）。 |
| `textRotate` | `GallerySecurityRotateType` | 读写。安全文本的方向（默认：`GallerySecurityRotateType.ZERO`）。 |
| `typename` | string | 只读。引用的 `PicturePackageOptions` 对象的类名。 |

## PixarSaveOptions

使用 [Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法以 Pixar 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | boolean | 读写。True 表示保存 Alpha 通道。 |
| `typename` | string | 只读。引用的 `PixarSaveOptions` 对象的类名。 |

## PNGSaveOptions

使用 [Document.saveAs()](http://Document.saveAs()) 方法以 PNG 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | --- |
| `compression` | number [0..9] | 读写。压缩值（默认：`0`）。 |
| `interlaced` | boolean | 读写。True 表示交错行（默认：`false`）。 |
| `typename` | string | 只读。引用的 `PNGSaveOptions` 对象的类名。 |

## Preferences

表示 Photoshop 的应用程序首选项。通过 [Application.preferences](https://www.adobe.com/devnet/photoshop/scripting.html) 属性访问此对象。例如：

```
app.preferences.rulerUnits = Units.PIXELS
app.preferences.typeUnits = TypeUnits.PIXELS
```

在此对象中设置值等同于 Adobe Photoshop CC 2015 应用程序中选择 **编辑 > 首选项**（Windows 中）或 **Photoshop > 首选项**（Mac OS 中）。有关各项设置的说明，请参阅 Adobe Photoshop CC 2015 帮助。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `additionalPluginFolder` | [File](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。附加插件文件夹的路径。<br><br>仅在 [useAdditionalPluginFolder](https://www.adobe.com/devnet/photoshop/scripting.html) = `true` 时有效。 |
| `appendExtension` | [SaveBehavior](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。在 Windows 中写入文件扩展名的首选策略。 |
| `askBeforeSavingLayeredTIFF` | boolean | 读写。True 表示在以 TIFF 格式保存文件时，询问用户确认图层保留选项。 |
| `autoUpdateOpenDocuments` | boolean | 读写。True 表示自动更新打开的文档。 |
| `beepWhenDone` | boolean | 读写。True 表示在过程完成时发出提示音。 |
| `colorChannelsInColor` | boolean | 读写。True 表示在通道调板中以彩色显示组件通道。 |
| `colorPicker` | [ColorPicker](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。首选颜色选择。 |
| `columnGutter` | number [0.1..600.0] | 读写。列间距（以点为单位）。 |
| `columnWidth` | number [1..600.0] | 读写。列宽（以点为单位）。 |
| `createFirstSnapshot` | boolean | 读写。True 表示创建新文档时制作第一个快照。 |
| `dynamicColorSliders` | boolean | 读写。True 表示颜色板中显示动态颜色滑块。 |
| `editLogItems` | [EditLogType](https://www.adobe.com/devnet/photoshop/scripting.html) | 读写。历史记录日志详细级别。仅在 `useHistoryLog = true` 时有效。 |
| `exportClipboard` | boolean | 读写。True 表示退出 Photoshop CC 2015 后，将内容保留在剪贴板上。 |
| `fontSize` | `FontPreviewType` | 读写。文字菜单中的字体大小。 |
| `fullSizePreview` | boolean | 读写。True 以全尺寸显示图像预览，false 表示缩略图（仅限 Mac OS）。 |
| `gamutOpacity` | number [0..100] | 读写。不透明度值（百分比）。 |
| `gridSize` | `GridSize` | 读写。网格中方块的大小。 |
| `gridStyle` | `GridLineStyle` | 读写。非打印网格线的样式。 |
| `gridSubdivisions` | number [1..100] | 读写。网格细分数量。 |
| `guideStyle` | `GuideLineStyle` | 读写。非打印参考线的样式。 |
| `iconPreview` | boolean | 读写。True 表示图标预览（仅限 Mac OS）。 |
| `imageCacheLevels` | number [1..8] | 读写。缓存中的图像数量。 |
| `imagePreviews` | `SaveBehavior` | 读写。Windows 中写入图像预览的首选策略。 |
| `interpolation` | `ResampleMethod` | 读写。在图像重新采样或调整大小时，为创建任何像素分配颜色的方法。 |
| `keyboardZoomResizes` | boolean | 读写。True 使用键盘快捷键缩放时调整窗口大小。 |
| `macOSThumbnail` | boolean | 读写。True 保存保存时创建缩略图（仅限 Mac OS）。 |
| `maximizeCompatibility` | `QueryStateType` | 读写。打开 PSD 文件时，检查是否化兼容性。 |
| `maxRAM` | number [5..100] | 读写。Adobe Photoshop CC 2015 使用的最大 RAM 百分比。 |
| `nonLinearHistory` | boolean | 读写。True 表示允许非线性历史记录。 |
| `numberOfHistoryStates` | number | 读写。要保留的历史状态数量。 |
| `otherCursors` | `OtherPaintingCursors` | 读写。用于某些工具的首选指针类型。 |
| `paintingCursors` | `PaintingCursors` | 读写。用于某些工具的首选指针类型。 |
| `parent` | `Application` | 读写。包含的应用程序。 |
| `pixelDoubling` | boolean | 读写。True 表示将分辨率减半（像素大小加倍）以预览显示更快。 |
| `pointSize` | `PointType` | 读写。点/派大小。 |
| `recentFileListLength` | number [0..30] | 读写。最近文件列表中的项目数。 |
| `rulerUnits` | `Units` | 读写。脚本系统在接收和返回值时使用的单位。 |
| `saveLogItems` | `SaveLogItemsType` | 读写。保存历史记录项目时，历史日志数据的首选位置。 |
| `saveLogItemsFile` | `File` | 读写。首选位置是文件时，历史日志文件的路径。 |
| `savePaletteLocations` | boolean | 读写。True 表示新调板位置成为默认位置。 |
| `showAsianTextOptions` | boolean | 读写。True 表示在段落调板中显示亚洲文字选项。 |
| `showEnglishFontNames` | boolean | 读写。True 以英文列出亚洲字体名称。 |
| `showSliceNumber` | boolean | 读写。True 在使用切片工具时，在文档窗口中显示切片编号。 |
| `showToolTips` | boolean | 读写。True 显示鼠标悬停时的弹出定义。 |
| `smartQuotes` | boolean | 读写。True 使用弯引号，false 表示使用直引号。 |
| `textFontSize` | `FontSize` | 读写。在调板和对话框中使用的小字体的大小。 |
| `typename` | string | 只读。引用的 `preferences` 对象的类名。 |
| `typeUnits` | `TypeUnits](https://www.adobe.com/photoshop/using/type-units.html) | 读写。字符测量的单位。 |
| `useAdditionalFolder` | boolean | 读写。True 表示使用一个附加文件夹存储另一个应用程序。 |
| `useHistoryLog` | boolean | 读写。True 为历史记录状态创建日志。 |
| `useLowerCaseExtension` | boolean | 读写。True 对文件名使用小字母。 |
| `useShiftKeyForTool` | boolean | 读写。True 启用一组工具之间切换。 |
| `useVideoAlpha` | boolean | 读写。True 允许 Adobe Photoshop CC 2015 将透明度发送到计算机（需要硬件支持）。 |
| `windowsThumbnail` | boolean | 读写。True 在 Windows 中保存图像时缩略图（需要硬件支持）。 |

## PresentationOptions

使用 `Application.makePresentation()` 创建演示的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :---|---|---|
| `autoAdvance` | boolean | 读写。True 在演示时自动切换（默认：`true`）。当 `presentation = true` 时有效。 |
| `includeFilename` | boolean | 读写。True 包含文件名（默认：`false`）。 |
| `interval` | number [1..60] | 读写。自动切换前的等待时间（默认：5）。当 `autoAdvance = true` 时有效。 |
| `loop` | boolean | 读写。True 在最后一页后开始（默认：`false`）。当 `autoAdvance = true` 时有效。 |
| `magnification` | `MagnificationType` | 读写。查看图像时的放大类型。 |
| `PDFFileOptions` | `PDFSaveOptions` | 读写。创建 PDF 文件使用的选项。 |
| `presentation` | boolean | 读写。True 输出演示（默认：`false`）；设为 `false`，输出多页。 |
| `transition` | `TransitionType` | 读写。从一张图像过渡到下一张（默认：`TransitionType.NONE`）。当 `autoAdvance = true` 时有效。 |
| `typename` | string | 只读。引用的 `PresentationOptions` 对象的类名。 |

## RawFormatOptions

使用 `Application.open()` 打开 RAW 格式的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | --- |
| `bitsPerChannel` | number | 读写。每个通道的位数。有效的值是 `BitsPerChannelType.EIGHT` 或 `BitsPerChannelType.SIXTEEN`。 |
| `byteOrder` | `ByteOrder` | 读写。多字节值的顺序。当 `bitsPerChannel = BitsPerChannelType.SIXTEEN` 时有效。 |
| `channelNumber` | number [1..56] | 读写。图像中的通道数。其值超过图像中的通道数。当 `bitsPerChannel = BitsPerChannelType.SIXTEEN` 时，有效的值是 1、3 或 4。 |
| `headerSize` | number [0..191999] | 读写。实际图像信息开始之前，文件中出现的字节数；即在开头插入的用占位符的零。 |
| `height` | number | 读写。图像的高度（以像素为单位）。 |
| `interleaveChannels` | boolean | 读写。设为 `true` 按顺序存储颜色值。 |
| `retainHeader` | boolean | 读写。True 在保存时保留标题。当 `headerSize` 为 1 或更大时有效。 |
| `typename` | string | 只读。引用的 `RawFormatOptions` 对象的类名。 |
| `width` | number | 读写。图像的宽度（以像素为单位）。 |

## RawSaveOptions

使用 `Document.saveAs()` 方法以 RAW 格式保存文档的选项。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| `alphaChannels` | boolean | 读写。设为 `true` 表示保存 Alpha 通道。 |
| `spotColors` | boolean | 读写。设为 `true` 表示保存专色。 |
| `typename` | string | 只读。引用的 `RawSaveOptions` 对象的类名。 |

## RGBColor

定义 RGB 颜色，用于 [SolidColor](https://example.com) 对象。

另请参阅 [CMYKColor](https://example.com)、[GrayColor](https://example.com)、[HSBColor](https://example.com)、[LabColor](https://example.com)、[NoColor](https://example.com)。

## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `blue` | `number [0..255]` | 读写。蓝色值（默认值：255）。 |
| `green` | `number [0..255]` | 读写。绿色值（默认值：255）。 |
| `hexValue` | `string` | 读写。颜色的十六进制表示。 |
| `red` | `number [0..255]` | 读写。红色值（默认值：255）。 |
| `typename` | string | 只读。引用的 `RGBColor` 对象的类名。 |

## Selection

文档或图层的选定区域通过 `Document.selection` 属性访问。例如：
`app.activeDocument.selection.fill(app.foregroundColor)`
许多属性和方法使用 `UnitValue` 类型，将测量值与单位相结合。有关类型的信息，请查阅 JavaScript指南。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | --- |
| `bounds` | array of `UnitValue` | 只读。整个选区的边界形。 |
| `parent` | `Document` | 只读。容器。 |
| `solid` | boolean | 只读。如果边界形是实心的，则为 `true`。 |
| `typename` | string | 只读。引用的 `selection` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | --- | --- | --- |
| `clear()` | | | 清除选区且将其复制到贴板。 |
| `contract(by)` | `UnitValue` | | 按指定量收缩选区。 |
| `copy([merge])` | boolean | | 将选区复制到贴板。使用可选参数 `true` 时，执行合并（选区中的可见图层都会复制）。 |
| `cut()` | | | 清除选区并复制到贴板。 |
| `deselect()` | | | 取消当前选区。 |
| `expand(by)` | `UnitValue` | | 按指定量扩展选区。 |
| `feather(by)` | `UnitValue` | | 按指定量羽化选区的边缘。 |

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | --- | --- | --- |
| `fill(filltype[, mode][, opacity][, preserveTransparency])` | `SolidColor`, `ColorBlendMode`, `number [1..100]`, boolean | | 填充选区。`opacity` 是百分比值。 |
| `grow(tolerance, antiAlias)` | number, boolean | | 扩展选区包含所有在指定容差内的相邻像素。 |
| `invert()` | | | 反转选区（取消选择并选择文档其余部分）。**提示：** 要翻转选区形状，请查阅 `rotate`。 |
| `load(from[, combination][, in])` | `Channel`, `SelectionType`, boolean | | 从通道加载选区。 |
| `makeWorkPath([tolerance])` | number | | 将选区项设置为文档路径。 |
| `resize([horizontal][, vertical][, anchor])` | number, number, `AnchorPosition` | | 将选定区域调整为指定的尺寸和锚点位置。 |
| `resizeBoundary([horizontal][, vertical][, anchor])` | number, number, `AnchorPosition` | | 围绕指定的锚点更改选区的尺寸。 |
| `rotate(angle[, anchor])` | number, `AnchorPosition` | | 围绕指定的锚点将选区旋转指定的量。 |
| `rotateBoundary(angle[, anchor])` | number, `AnchorPosition` | | 围绕指定的锚点旋转选区的边界。 |
| `select(region[, type][, feather][, antiAlias])` | array of number, `SelectionType`, number, boolean | 选择指定的区域。`region` 参数是一个包含四个坐标的数组：`[左, 上, 右, 下]`。 |
| `selectAll()` | | | 选择整个图层。 |

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | --- | --- | --- |
| `selectBorder(width)` | `UnitValue` | | 仅选择选区边框（指定宽度）；后续操作不会影响边框内选定的区域。 |
| `similar(tolerance, antiAlias)` | number, boolean | | 扩展选区包含整个图像中在容差范围内的像素。 |
| `smooth(radius)` | number | | 清理基于颜色的选区内部或外部遗留的杂散像素（以像素为单位指定的半径内）。 |
| `store(into[, combination])` | `Channel`, `SelectionType` | | 将选区另存为通道。 |
| `stroke(strokeColor, width[, location][, mode][, opacity][, preserveTransparency])` | `SolidColor`, number, `StrokeLocation`, `ColorBlendMode`, number [1..100], boolean | 对选区边框进行描边。`opacity` 是百分比值。 |
| `translate([deltaX][, deltaY])` | `UnitValue`, `UnitValue` | | 相对于当前位置移动整个选区。 |
| `translateBoundary([deltaX][, deltaY])` | `UnitValue`, `UnitValue` | | 相对于当前位置移动选区。 |

### 选区示例脚本

以下脚本通过以下步骤创建棋盘格：

- 创建一个 800 x 800 像素的文档。
- 将整个文档划分为 100 x 100 像素的正方形。
- 选择第一行中的每个其他正方形，然后将选择标准移位以选择下一行中的交替正方形。重复此过程，直到选中文档中的每个其他正方形。
- 用调色板中的前景色填充选中的正方形。
- 反转选区，并用调色板中的背景色填充新选中的正方形。
- 取消选择这些正方形，以移除选择轮廓（“蚂蚁线”）。

```
Selection.jsx
```

```markdown
// 保存当前首选项

var startRulerUnits = app.preferences.rulerUnits

```javascript
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
```

## SGIRGBSaveOptions

使用 [`Document.saveAs`](https://www.adobe.com/devnet/photoshop/scripting.html) 方法以 SGIRGB 格式保存文档的选项。

> **注意：** SGIRGB 格式不会随 Adobe Photoshop CC 2015 自动安装。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `alphaChannels` | 布尔值 | 可读写。为 `true` 时保存 Alpha 通道。 |
| `spotColors` | 布尔值 | 可读写。为 `true` 时保存专色。 |
| `typename` | 字符串 | 只读。引用的 `SGIRGBSaveOptions` 对象的类名。 |

## SolidColor

文档中使用的颜色定义。将一种颜色映射到所有可用颜色模型中的等效值。

- 用于 [`Application.backgroundColor`](https://www.adobe.com/devnet/photoshop/scripting.html) 和 [`foregroundColor`](https://www.adobe.com/devnet/photoshop/scripting.html) 属性，用于 [`Channel.color`](https://www.adobe.com/devnet/photoshop/scripting.html)，用于 [`ColorSampler.color`](https://www.adobe.com/devnet/photoshop/scripting.html)，以及用于 [`TextItem.color`](https://www.adobe.com/devnet/photoshop/scripting.html)
- 传递给 [`PathItem.fillPath()`](https://www.adobe.com/devnet/photoshop/scripting.html)、[`Selection.fill()`](https://www.adobe.com/devnet/photoshop/scripting.html) 和 [`Selection.stroke()`](https://www.adobe.com/devnet/photoshop/scripting.html)。

## 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| cmyk | [`CMYKColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。CMYK 颜色模式。 |
| gray | [`GrayColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。灰度颜色模式。 |
| hsb | [`HSBColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。HSB 颜色模式。 |
| lab | [`LabColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。LAB 颜色模式。 |
| model | [`ColorModel`](https://www.adobe.com/devnet/photoshop/scripting.html) | 可读写。颜色模型。 |
| nearestWebColor | [`RGBColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 只读。当前颜色。 |
| rgb | [`RGBColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 只读写。颜色模型。 |
| typename | [`ColorColor`](https://www.adobe.com/devnet/photoshop/scripting.html) | 只读。引用的 `ColorModel` 对象的类名。 |
```



```markdown
## 属性

| 属性 | 值类型 | 说明 |
| --- | --- | --- |
| `length` | `number` | 只读。集合中的元素数量。 |
| `parent` | [Application](https://example.com) | 只读。所属的应用程序。 |
| `typename` | `string` | 只读。引用的 `TextFonts` 对象的类名。 |

## 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| --- | --- | --- | --- |
| `getByName(name)` | `string` | [TextFont](https://example.com) | 获取 `TextFonts` 集合中具有所提供名称的第一个元素。 |

## TextItem

ArtLayer 对象中 `kind` 属性为 `LayerKind.TEXT` 的文本。通过 `ArtLayer.textItem` 属性访问此对象。例如：

```javascript
myLayers[i].textItem.contents = "Layer in " + textArray[i] + " Set Inside "
```


markdown
许多属性使用 `UnitValue` 类型，该类型将测量值与测量单位相结合。有关此类型的更多信息，请参阅 JavaScript 工具指南。

## 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alternateLigatures | boolean | 读写。是否使用替代连字。**注意：** 替代连字与酌情连字相同。有关更多信息，请参阅 Adobe Photoshop CC 2015 帮助。 |
| antiAliasMethod | `AntiAlias` | 读写。要使用的抗锯齿方法。 |
| autoKerning | `AutoKernType` | 读写。要使用的自动字距调整选项。 |
| autoLeadingAmount | number [0.01..5000.00] | 读写。自动（默认）行距所使用的百分比（以点为单位）。仅在 `useAutoLeading = true` 时有效。 |
| baselineShift | `UnitValue` | 读写。文本基线偏移中使用的单位值。 |
| capitalization | `TextCase` | 读写。文本大小写。 |
| color | `SolidColor` | 读写。文本颜色。 |
| contents | string | 读写。图层中的实际文本。 |
| desiredGlyphScaling | number [50..200] | 读写。缩放文本字符水平大小的所需量。百分比值；在 100 时，字符宽度不缩放。仅在 `justification = Justification.CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFTJUSTIFIED`, 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `minimumGlyphScaling` 和 `maximumGlyphScaling` 值。 |
| desiredLetterScaling | number [100..500] | 读写。字符间的间距量（在 0 时，字符间不添加空格）。等同于段落调板菜单（选择 `Justification`）的 `Justification` 对话框中的 `Letter Spacing`。仅在 `justification` = `Justification.CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFTJUSTIFIED`, 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 [`minimumLetterScaling`](#minimumLetterScaling) 和 [`maximumLetterScaling`](#maximumLetterScaling) 值。 |
| desiredWordScaling | number [0..1000] | 读写。单词间的间距量（百分比）（在 100 时，单词间不添加额外空格）。等同于段落调板菜单（选择 `Justification`）的 `Justification` 对话框中的 `Word Spacing`。仅在 `justification` = `Justification.CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFTJUSTIFIED`, 或 `Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 [`minimumWordScaling`](#minimumWordScaling) 和 [`maximumWordScaling`](#maximumWordScaling) 值。 |
| direction | `Direction` | 读写。文本方向。 |
| fauxBold | boolean | 读写。是否使用伪粗体（默认: `false`）。将此项设置为 true 相当于选择文本并单击字符调板中的 Faux Bold。 |
| fauxItalic | boolean | 读写。是否使用伪斜体（默认: `false`）。将此项设置为 true 相当于选择文本并单击字符调板中的 Faux Italic。 |
| firstLineIndent | `UnitValue` [-1296..1296] points | 读写。段落首行的缩进量（单位值）。 |
| font | string | 读写。字符的文本字体。使用字体的 PostScript 名称。请参阅 [`TextFont`](#TextFont) 并使用 `postScriptName` 属性。 |
| hangingPunctuation | boolean | 读写。是否使用罗马悬挂标点。 |
| height | `UnitValueX` | 读写。段落文本边界框的高度（单位值）。仅在 `kind = TextType.PARAGRAPHTEXT` 时有效。 |
| horizontalScale | number [0..1000] | 读写。相对于 [`verticalScale`](#verticalScale) 的字符缩放（水平）（百分比值）。 |
| hyphenateAfterFirst | number [1..15] | 读写。允许在自动换行中使用连字符的字母数之后。 |
| hyphenateBeforeLast | number [1..15] | 读写。允许在自动换行中使用连字符的字母数之前。 |
| hyphenateCapitalWords | boolean | 读写。是否允许在大写单词的自动换行中使用连字符。 |
| hyphenateWordsLongerThan | number [2..25] | 读写。单词必须包含的最小字母数，以允许在自动换行中使用连字符。 |
| hyphenation | boolean | 读写。是否在自动换行中使用连字。 |
| hyphenationZone | `UnitValue` [0..720] pica | 读写。行末将导致单词在非两端对齐文本中断开的距离。 |
| hyphenLimit | number | 读写。可以以连字符结尾的最大连续行数。 |
| justification | `Justification` | 读写。段落对齐方式。 |
| kind | `TextType` | 读写。文本换行类型。 |
| language | `Language` | 读写。要使用的语言。 |
| leading | `UnitValue` | 读写。行距量。 |
| leftIndent | `UnitValue` [-1296..1296] points | 读写。文本从左侧缩进的空格量。 |
| ligatures | boolean | 读写。是否使用连字。 |
| maximumGlyphScaling | number [50..200] | 读写。缩放文本字符水平大小的最大量（百分比值；在 100 时，字符宽度不缩放）。仅在 `justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED, 或 Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `minimumGlyphScaling` 和 `desiredGlyphScaling`。 |

## TiffSaveOptions

使用 [`Document.saveAs()](https://www.adobe.com/devnet/photoshop/scripting.html) 方法将文档为 TIFF 格式。

### 属性

| 属性 | 值类型 | 说明 |
| :--- | :--- | :--- |
| alphaChannels | boolean | 读写。为 true 保存 Alpha 通道。 |
| annotations | boolean | 读写。为 true 保存注释。 |
| byteOrder | `ByteOrder` | 读写。文档多字节顺序。 |
| embedColorProfile | boolean | 读写。为 true 在文档中嵌入配置文件。 |
| imageCompression | `TIFFEncoding` | 读写。压缩类型（默认值：`TIFFEncoding.NONE`）。 |
| interleaveChannels | boolean | 读写。为 true 图像中的交错。 |
| jpegQuality | number [0..12] | 读写。生成图像质量。仅当 `imageCompression = TIFFEncoding.JPEG` 时有效。 |
| layerCompression | `LayerCompression` | 读写。保存图层时合成数据使用的压缩方法。仅当 `layers = true` 时有效。 |
| layers | boolean | 读写。为 true 保存图层。 |
| saveImagePyramid | boolean | 读写。为 true 保留分辨率信息（默认值：`false`）。 |
| spotColors | boolean | 读写。为 true 保存专色。 |
| transparency | boolean | 读写。为 true 将透明度保存为额外的 通道（以便另一个应用程序中打开）。 |
| typename | string | 只读。引用的 `TiffSaveOptions` 对象的类名。 |

### 方法

| 方法 | 参数类型 | 返回值 | 说明 |
| :--- | :--- | :--- | :--- |
| `convertToShape()` | | | 将文本项目及其包含图层转换为填充路径。 |
| `createPath()` | | | 从实际文本项目（如字母或单词）轮廓创建贴路径。 |

### 属性（续）

| 属性 | 值类型 | 说明（续） |
| :--- | :--- | :--- |
| `maximumLetterScaling` | number [100..500] | 读写。允许在字母之间添加的最大空间量（在 0 时，不添加字母间距）。等同于“段落”调板菜单中“对齐方式”对话框中的字距调整。当 `justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `minimumLetterScaling` 和 `desiredLetterScaling` 的值。 |
| `maximumWordScaling` | number [0..1000] | 读写。允许在单词之间添加的最大空间量（百分比值；在 100 时，不在单词之间添加额外空间）。等同于“段落”调板菜单中“对齐方式”对话框中的字间距。当 `justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `minimumWordScaling` 和 `desiredWordScaling` 的值。 |
| `minimumGlyphScaling` | number [50..200] | 读写。缩放文本字母尺寸的最小量（百分比值；在 100 时，不缩放字符宽度）。当 `justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `maximumGlyphScaling` 和 `desiredGlyphScaling` 的值。 |
| `minimumLetterScaling` | number [100..500] | 读写。允许在字母之间添加的最小空间量（百分比值；在 0 时，不移除字母间距）。等同于“段落”调板菜单中“对齐方式”对话框中的字距调整。当 `justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `maximumLetterScaling` 和 `desiredLetterScaling` 的值。 |
| `minimumWordScaling` | number [0..1000] | 读写。允许在单词之间添加的最小空间量（百分比值；在 100 时，不在单词之间移除额外空间）。等同于“段落”调板菜单中“对齐方式”对话框中的字间距。当 `justification = Justification.CENTERJUSTIFIED, FULLYJUSTIFIED, LEFTJUSTIFIED 或 Justification.RIGHTJUSTIFIED` 时有效。使用时，还需要 `maximumWordScaling` 和 `desiredWordScaling` 的值。 |
| `noBreak` | boolean | 读写。为 true 禁止此文本中的换行。提示：当许多字符都设置为 true 时，可以自动换行，导致某些文本在屏幕上显示。 |
| `oldStyle` | boolean | 读写。为 true 使用旧式字体。 |
| `parent` | `ArtLayer` | 读写。包含的图层。 |
| `position` | `UnitValue` 数组 | 读写。文本的原点。指定 X 和 Y 坐标。等同于使用文本工具在文档中创建原点。 |
| `rightIndent` | `UnitValue` [-1296..1296] points | 读写。文本从右侧缩进的空间。 |
| `size` | `UnitValue` | 读写。字体大小（以 `UnitValue` 表示）。注意：对于 CS3 及早版本，类型为 `points`。 |
| `spaceAfter` | `UnitValue` [-1296..296] points | 读写。每个段落之后使用的量。 |
| `spaceBefore` | `UnitValue` [-1296..296] points | 读写。每个段落之前的空间。 |
| `strikeThru` | `StrikeThruType` | 读写。使用的文本删除线。 |
| `textComposer` | `TextComposer` | 读写。用于评估换行并优化指定的字和对齐选项的组合。当 `kind = TextType.PARAGRAPHTEXT` 时有效。 |
| `tracking` | number [-1000..10000] | 读写。多个字符之间的均匀间距。字距单位为 `em` 空间。`em` 空间相对于当前字体大小。在 1 点字体中 `em` 等于 1 点；在 10 点字体中 `em` 等于 10 点。 |
| `typename` | string | 只读。引用的 `textItem` 对象的类名。 |
| `underline` | `UnderlineType` | 读写。文本划线选项。 |
| `useAutoLeading` | boolean | 读写。为 true 使用字体内行距信息。 |
| `verticalScale` | number [0-1000] | 读写。相对于 `horizontalScale` 的垂直字符缩放比例（百分比值）。 |
| `warpBend` | number [-100..100] | 读写。弯曲变形变形。 |
| `warpDirection` | `Direction` | 读写。弯曲变形方向。 |
| `warpHorizontalDistortion` | number [-100..100] | 读写。弯曲变形的水平失真（百分比值）。 |
| `warpStyle` | `WarpStyle` | 读写。弯曲变形样式。 |
| `warpVerticalDistortion` | number [-100..100] | 读写。弯曲变形的垂直失真（百分比值）。 |
| `width` | `UnitValue` | 读写。段落文本的界框宽度。当 `kind = TextType.PARAGRAPHTEXT` 时有效。 |

## UnitValue

ExtendScript 定义了 JavaScript 类 `UnitValue`，用于表示测量值及其测量单位；详情'JavaScript support in Adobe Photoshop CC 2015' 第32 页。关于这些类的参考细节，请参阅 *JavaScript Tools Guide*。

## xmpMetadata

Camera RAW 图像的 XMP 元数据。对于 Camera RAW 图像文件，XMP 元数据存储在一个 *sidecar* 文件中，该文件与 RAW 文件位于同一文件夹内，具有相同的基本名称和 XMP 扩展名。

### 属性

| 属性 | 值类型 | 描述 |
| :--- | :--- | :--- |
| `parent` | [Document](https://www.adobe.com/devnet/photoshop/scripting.html) | 只读。包含的文档。 |
| `rawData` | string | 可读写。包含 XML (RDF) 格式的 XMP 元字符串。有关此格式的详细信息，请参阅 *XMP Specification*。 |
| `typename` | string | 只读。引用的 `xmpMetadata` 对象的类名。 |

# Adobe Photoshop CC 2015

### JavaScript 参考指南

#### JavaScript 资源

本节描述了使你的 JavaScript 脚本能够像插件一样运行的 JavaScript 资源。这包括：

- 指定脚本作为命令出现的菜单的能力，
- 一个术语资源，使脚本能够与 Action Manager 一起工作，这允许你的脚本被录制并通过脚本参数自动化，
- 一个类别，用于在菜单内对命令进行排序和分组，
- 以及一个启用字符串，用于指示在给定条件下该命令是启用还是禁用的。
- 字符串必须是有效的 XML 语法。例如，“&”字符将不起作用。在启用信息块中使用 `&amp;` 表示逻辑“&&”。

#### JavaScript 资源语法

JavaScript 资源具有类似 HTML 的语法，每个 `<tag>` 都有一个对应的关闭标签 `</tag>`。此资源需要出现在注释（`/* ... */`）内，并且应在脚本文件的顶部定义（在文件的前 10,240 个字符内）。

| 标签 | 描述 |
| :--- | :--- |
| `<javascriptresource>` | 资源定义标签。 |
| `<name>` | 出现在 Photoshop 菜单中的命令名称。如果资源未提供此标签，则菜单中命令的名称认为脚本的名称。 |
| `<menu>` | 命令出现的菜单。如果未提供此标签，命令将出现在 **脚本** 菜单中。**注意：** `<menu>` 唯一支持的值是 `automate`、`filter` 和 `help`。例如，`automate` 会脚本放入 **自动** 菜单中。 |
| `<about>` | 出现在“关于”框中的字符串，用户可以从 **帮助 > 关于插件** 菜单中选择该框。 |
| `<enableinfo>` | 一个布尔表达式，指示菜单中的命令是否启用。请参阅“启用信息语法”部分。**注意：** 如果提供了此标签，则当至少有一个文档打开，并且布尔表达式计算结果为 true 时，菜单项才启用。如果你希望菜单项始终启用，请不要使用此标签。 |
| `<eventid>` | 一个标识事件的唯一字符串。使用 UUID 将确保你的脚本与其他脚本共享此标识符。 |
| `<category>` | 命令在菜单中出现的类别。用于在菜单中分组和排序命令。命令基于 `<category>` 中的字符串按字母顺序放置在菜单中。如果两个命令使用相同的类别，将被将被在一起。 |
| `<terminology>` 使脚本能够与 Action Manager 一起工作的术语词典。请参阅“术语词典”部分。 |

### 基本 JavaScript 资源示例

此示例展示了一个基本的 `<javascriptresource>`。使用此资源，可以通过选择 **添加文档** 命令来执行脚本，该命令出现在 **自动** 菜单中。此命令在菜单中是启用的，前提是至少已经打开了一个文档。如果用户从 **关于插件** 菜单请求有关脚本的信息，会将 `<about>` 标签中包含的字符串显示在对话框中。
```


```javascript
/*
    <javascriptresource>
    <name>Add a Document</name>
    <type>automate</type>
    <about>A short string providing information about the script.</about>
    <enableinfo>true</enableinfo>
</javascriptresource>
*/
```

`app.documents.add();`

### 启用信息语法

`<enableinfo>` 标签提供一个布尔表达式，当该表达式被计算时，指示菜单中的命令是否启用。你可以使用此表达式根据文档的各种特性启用或禁用菜单项。启用信息语法如下：

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
<inFunction> := "in" "(" <simpleExpression> { "," <simpleExpression> } ")"
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
| `ImageMode` | 活动文档的模式。 |
| `ImageDepth` | 活动文档的深度。 |
| `LayerMask` | 布尔值，指示图层蒙版。 |
| `SelectionMask` | 布尔值，指示选区蒙版。 |
| `TransparencyMask` | 布尔值，指示透明度蒙版。 |
| `NumTargetChannels` | 目标通道的数量。 |
| `NumTrueChannels` | 图像通道的数量。 |
| `AdjustSheet` | 布尔值 |
| `IsTargetComposite` | 布尔值，指示通道是否拼合。 |
| `IsTargetSection` | 布尔值。 |
| `IsTargetVisible` | 布尔值。 |
| `ImageWidth` | 图像宽度。 |
| `ImageHeight` | 图像高度。 |
| `ProtectFlags` | |

### 启用信息中的未定义值

如果任何算术或关系运算包含未定义数或未定义的变量，则评估的结果为 `false`。布尔值的处理方式相同，其中非值为 `true`，未定义的值为 `false`。

### 使用 `in` 函数

`in` 函数（参见 `<inFunction>`）在第一个参数等于后续参数之一时返回 `true`。一个典型用法可能是检查图像模式是否是一组：

```
in(ImageMode, RGBMode, CMYKMode, LabMode)
```

### Action Manager

要使脚本能够记录参数并自动化，需要两个机制：
- 一个术语字典，将脚本界面映射到人类读的文本，为参数提供文本和类型。
- 使用 Action Manager（而非用户界面）时读取参数信息，以及将参数写入代码。此代码使用 `ActionDescriptor`、`ActionList` 和 `ActionReference`。有关记录和自动化的示例，参见 `Conditional.jsx`。文件可在 `Presets/Scripts` 文件夹中。

### 术语字典

JavaScript资源了一个 `<terminology>` 标签，允许你为脚本提供术语字典。创建术语字典的第一步是检查脚本界面，为每个元素创建人类读的字符串。例如，在“更改”命令中，用户界面请求源模式和一个目标模式。源模式和目标模式都有选项。所有用户界面都需要术语字典中有条目。

**注意：**术语标签中的信息需要包装在 `CDATA` 块中，以便解析器忽略 `/` 和其他标签。事件、类和枚举字典的定义如下：

`Events` 字典包含每个条目：

```
/eventName [ Name used in string-based API
    (String name) // required
    /parameter type // optional; if omitted, no parameter
    << // optional parameter dictionary
        /parameterName [ Name used in string-based API
            (String name) // required
            /parameter type // required
            ]
        ... >>]
```

`Classes` 字典包含每个类的条目：

```
/className [ Name used in string-based API
    (String class name) // required
    << // property dictionary
        /propertyName [ Name used in string-based API
            (String name) // required
            /property type // required
            ]
        ... >>]
```

`Enumerations` 字典包含每个枚举类型的条目：

```
/enumTypeName // Name used in string-based API
    <<
        /enumValue (String name) // required
        ... >>
```

### 值类型定义

对于 `/parameter type` 和 `/property type` 定义，你可以使用自己的术语字典中声明类和枚举类型，可以使用 Photoshop 提供的声明，也可以使用基本值类型。

### 基本值类型

基本值类型如下表所示：

| 名称 | 代码 | 描述 |
| :--- | :--- | :--- |
| `typeInteger` | `long` | int32 |
| `typeFloat` | `doub` | IEEE 64 位浮点数 |
| `typeBoolean` | `bool` | TRUE 或 FALSE。 |
| `typeText` | `TEXT` | 任意数量的可字符块。 |
| `typeAlias` | `alis` | Macintosh 文件路径。 |
| `typePaths` | `Pth` | Windows 文件路径。 |
| `typePlatformFilePath` | `alis` 或 `Pth` | Mac OS 上为 typeAlias，Windows 上为 typePath。 |

### 预定义类类型

Photoshop提供了许多可在术语字典中预定义类。这些类的一个有用子集如下表所示。在适当的时候使用这些类，但如果有必要，你可以在术语资源中定义新的类。

| 名称 | 代码 | 描述 |
| :--- | :--- | :--- |
| `classColor` | `Clr` | 颜色类的类。 |
| `classRGBColor` | `RGBC` | keyRed, keyGreen, keyBlue |
| `classCMYKColor` | `CMYC` | keyCyan, keyMagenta, keyYellow, keyBlack。 |
| `classUnspecifiedColor` | `UnsC` | 未指定。 |
| `classGrayscale` | `Grsc` | keyGray |
| `classBookColor` | `BkCl` | 书籍颜色 |
| `classLabColor` | `LbCl` | keyLuminance, keyA, keyB。 |

### 术语条目的唯一性规则

通常，术语条目的名称在特定类别和范围内必须是唯一的。最好不要不必要地使名称唯一；首选通用术语，并且如果某个事物已有名称，请直接使用它。在考虑术语条目的唯一性时，大小写很重要。

术语条目的唯一性规则是：

- 所有事件名称必须与所有其他事件名称不同。
- 所有类名称必须与所有其他名称不同。
- 所有枚举类型名称必须与所有枚举类型名称不同。
- 所有键必须在同一类或事件中使用的所有键不同。
- 所有枚举值必须在同一枚举类型中的所有枚举值不同。
- 一个类、事件、枚举类型、键和枚举值都可以具有相同的名称。

### 术语定义示例

此示例演示了一个新事件的术语定义；该示例使用了 `ZStrings`。

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


```，由于你提供的原始文本包含大量重复的索引信息、乱码占位符（如 `+`、`""` 等）以及不完全的表格结构，作为高级文档工程师，我已根据你的要求进行了深度重构。

排版重点如下：
1. **去噪处理**：删除了无意义的索引数字、重复字符和乱码。
2. **格式规范化**：对所有的常量名、方法名、类名、路径和命令添加了反引号。
3. **结构优化**：重新梳理了混乱的标题层级，并确保表格逻辑清晰。
4. **内容精简**：删除了多余的空行，提升了文档的可读性。

以下是排版后的内容：

---

# 脚本常量

本节列出并描述了为 Adobe Photoshop CC 2015 JavaScript 属性和方法定义的枚举。

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `AdjustmentReference` | `ABSOLUTE`<br>`RELATIVE` | 解释选择性颜色调整规范的方法：<br><br>`ABSOLUTE` = 占总体的百分比。<br><br>`RELATIVE` = 占现有颜色数量的百分比。<br><br>传递给 `ArtLayer.selectiveColor()`。 |
| `AnchorPosition` | `BOTTOMCENTER`<br>`BOTTOMLEFT`<br>`BOTTOMRIGHT`<br>`MIDDLECENTER`<br>`MIDDLELEFT`<br>`MIDDLERIGHT`<br>`TOPCENTER`<br>`TOPLEFT`<br>`TOPRIGHT` | 变换对象时围绕的点。这是在使用 `ArtLayer`、`LayerSet` 和 `Selection` 中的方法旋转或调整对象大小时，或在使用 `Document.resizeCanvas()` 调整整个画布大小时，不移动的点。 |
| `AntiAlias` | `CRISP`<br>`NONE`<br>`SHARP`<br>`SMOOTH`<br>`STRONG` | 通过柔化边缘像素和背景像素之间的颜色过渡来平滑边缘的方法。用于 `TextItem.antiAliasMethod`。 |
| `AutoKernType` | `MANUAL`<br>`METRICS`<br>`OPTICAL` | 字符使用的字距调整类型。用于 `TextItem.autoKerning`。 |
| `BatchDestinationType` | `FOLDER`<br>`NODESTINATION`<br>`SAVEANDCLOSE` | 批处理文件的目标（如果有），在 `Application.batch()` 方法使用的 `BatchOptions` 中指定：<br><br>`FOLDER`：将文件的修改版本保存到新位置（保持原始文件不变）。<br><br>`NODESTINATION`：让所有文件保持打开状态。<br><br>`SAVEANDCLOSE`：保存更改并关闭文件。 |

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `BitmapConversionType` | `CUSTOMPATTERN`, `DIFFUSIONDITHER`, `HALFTHRESHOLD`, `HALFTONESCREEN`, `PATTERNDITHER` | 指定要转换为位图模式的图像质量。用于 `BitmapConversionOptions`。 |
| `BitmapHalfToneType` | `CROSS`, `DIAMOND`, `ELLIPSE`, `LINE`, `ROUND`, `SQUARE` | 指定半调网点（油墨沉积）的形状。用于 `BitmapConversionOptions`。 |
| `BitsPerChannelType` | `EIGHT`, `ONE`, `SIXTEEN`, `THIRTYTWO` | 每个颜色通道的位数。`Document.bitsPerChannel` 的值；传递给 `Documents.add()`。也用于 `PDFOpenOptions` 和 `CameraRAWOpenOptions`。 |
| `BlendMode` | `COLORBLEND`, `COLORBURN`, `COLORDODGE`, `DARKEN`, `DIFFERENCE`, `DISSOLVE`, `DIVIDE`, `EXCLUSION`, `HARDLIGHT`, `HARDMIX`, `HUE`, `LIGHTEN`, `LINEARBURN`, `LINEARDODGE`, `LINEARLIGHT`, `LUMINOSITY`, `MULTIPLY`, `NORMAL`, `OVERLAY`, `PASSTHROUGH`, `PINLIGHT`, `SATURATION`, `SCREEN`, `SOFTLIGHT`, `SUBTRACT`, `VIVIDLIGHT` | 控制应用滤镜时图像中像素的混合方式。`ArtLayer.blendMode` 和 `LayerSet.blendMode` 的值。 |
| `BMPDepthType` | `BMP_A1R5G5B5`, `BMP_A4R4G4B4`, `BMP_A8R8G8B8`, `BMP_R5G6B5`, `BMP_R8G8B8`, `BMP_X1R5G5B5`, `BMP_X4R4G4B4`, `BMP_X8R8G8B8`, `EIGHT`, `FOUR`, `ONE`, `SIXTEEN`, `THIRTYTWO`, `TWENTYFOUR` | 每个通道的位数（也称为像素深度或颜色深度）。选择的数字表示 2 的指数。例如，位深为 `EIGHT` 的像素有 2^8，即 256 种可能的颜色值。用于 `BMPSaveOptions`。 |
| `ByteOrder` | `IBM`, `MACOS` | 读取多字节值的平台特定顺序。 |
| `CameraRAWSettingsType` | `CAMERA`, `CUSTOM`, `SELECTEDIMAGE` | 要使用的默认 `CameraRaw` 设置：相机设置、自定义设置或所选图像的设置。在 `CameraRAWOpenOptions` 中设置。 |
| `CameraRAWSize` | `EXTRALARGE`, `LARGE`, `MAXIMUM`, `MEDIUM`, `MINIMUM`, `SMALL` | 相机 RAW 尺寸类型选项：`EXTRALARGE=5120 x 4096`，`LARGE=4096 x 2731`，`MAXIMUM=6144 X 4096`，`MEDIUM=3072 x 2048`，`MINIMUM=1536 x 1024`，`SMALL=2048 x 1365`。在 `CameraRAWOpenOptions` 中设置。 |
| `ChangeMode` | `BITMAP`, `CMYK`, `GRAYSCALE`, `INDEXEDCOLOR`, `LAB`, `MULTICHANNEL`, `RGB` | 文档的新颜色配置文件或模式，在 `Document.changeMode()` 中指定。**注意：** 彩色图像在更改为 `BITMAP` 模式之前，必须先更改为 `GRAYSCALE` 模式。 |
| `ChannelType` | `COMPONENT`, `MASKEDAREA`, `SELECTEDAREA`, `SPOTCOLOR` | 颜色通道的类型：`COMPONENT`：与文档颜色模式相关。`MASKEDAREA`：颜色表示蒙版区域的 Alpha 通道。`SELECTEDAREA`：颜色表示选中区域的 Alpha 通道。`SPOTCOLOR`：用于存储专色的 Alpha 通道。 |
| `ColorBlendMode` | `BEHIND`, `CLEAR`, `COLOR`, `COLORBURN`, `COLORDODGE`, `DARKEN`, `DARKERCOLOR`, `DIFFERENCE`, `DISSOLVE`, `EXCLUSION`, `HARDLIGHT`, `HARDMIX`, `HUE`, `LIGHTEN`, `LIGHTERCOLOR`, `LINEARBURN`, `LINEARDODGE`, `LINEARLIGHT`, `LUMINOSITY`, `MULTIPLY`, `NORMAL`, `OVERLAY`, `PINLIGHT`, `SATURATION`, `SCREEN`, `SOFTLIGHT`, `VIVIDLIGHT` | 在填充或描边中颜色混合的方式。传递给 `PathItem.fill()`、`Selection.stroke()`。 |
| `ColorModel` | `CMYK`, `GRAYSCALE`, `HSB`, `NONE`, `RGB` | 用于 `SolidColor` 的模型。 |
| `ColorPicker` | `ADOBE`, `APPLE`, `WINDOWS` | 首选颜色工具，在 `Preferences` 中设置。 |
| `ColorProfileType` | `CUSTOM`, `NONE`, `WORKING` | 管理此文档的颜色类型，在 `Document.colorProfile` 中设置。 |
| `ColorReductionType` | `ADAPTIVE`, `BLACKWHITE`, `CUSTOM`, `GRAYSCALE`, `MACOSH`, `PERCEPTUAL`, `RESTRICTIVE`, `SELECTIVE`, `WINDOWS` | `ExportOptionsSaveWeb` 的颜色减少算法。 |
| `ColorSpaceType` | `ADOBERGB`, `COLORRGB`, `PHOTORGB`, `SRGB` | 在 `CameraOpenOptions` 中使用的颜色空间。 |
| `CopyrightType` | `COPYRIGHTED`, `PUBLICDOMAIN`, `MARKED` | 文档的版权状态。用于 `Document.copyright`。 |
| `CreateFields` | `DUPLICATION`, `INTERPOLATION` | 创建字段。传递给 `ArtLayer.applyInterlace()`。 |
| `CropToType` | `ARTBOX`, `BLEEDBOX`, `BOUNDINGBOX`, `CROPBOX`, `MEDIABOX`, `TRIMBOX` | 在 PDF 文档中裁剪页面使用的样式。在 `PDFOpenOptions.cropPage` 中。 |
| `DCType` | `COLORCOMPOSITE`, `GRAYCOMPOSITE`, `NOCOMPOSITE` | 使用 `DCS1_SaveOptions` 或 `DCS2_SaveOptions` 创建的复合文件类型：`COLORCOMPOSITE`：彩色复合文件。`GRAYCOMPOSITE`：灰度复合文件。`NOCOMPOSITE`：不创建。 |
| `DepthMapSource` | `IMAGEHIGHLIGHT`, `LAYERMASK`, `NONE`, `TRANSPNCY` | 深度贴图的来源。传递给 `ArtLayer.applyLensBlur()`。 |
| `DescValueType` | `ALIASSTYPE`, `BOOLEANTYPE`, `CLASSTYPE`, `DOUBLETYPE`, `ENUMERATEDTYPE`, `INTEGERTYPE`, `LARGEINTEGERTYPE`, `LISTTYPE`, `DICTIONTYPE`, `RAWTYPE`, `REFERENCETYPE`, `STRINGTYPE` | 动作的值类型，由 `ActionDescriptor.getType()` 和 `ActionList.getType()` 返回。 |
| `DialogModes` | `ALL`, `ERROR`, `NO` | 控制 Photoshop 在运行脚本时的对话框类型。 |
| `Direction` | `HORIZONTAL`, `VERTICAL` | 翻转文档画布，传递给 `Document.flipCanvas()`。`TextItem.direction` 中文本的方向。`TextItem.warpDirection` 中文本扭曲的方向。 |

## Adobe Photoshop CC 2015 JavaScript 脚本常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `DisplacementMapType` | `STRETCHTOFIT`, `TILE` | 描述图像大小与置换图不匹配时，置换图如何适配图像。传递给 `ArtLayer.applyDisplace()`。 |
| `Dither` | `DIFFUSION`, `NOISE`, `NONE`, `PATTERN` | 在 `GIFSaveOptions`、`IndexedConversionOptions` 和 `ExportOptionsSaveWeb` 中使用的仿色。 |
| `DocPositionStyle` | `PRINTCENTERED`, `USERDEFINED` | `DocPosition` 中使用的定位类型。 |
| `DocumentFill` | `BACKGROUNDCOLOR`, `TRANSP`, `WHITE` | 新文档的填充类型，传递给 `Documents.add()`。 |
| `DocumentMode` | `BITMAP`, `CMYK`, `DUOTONE`, `GRAYSCALE`, `INDEXEDCOLOR`, `LAB`, `MULTICHANNEL`, `RGB` | 打开文档的颜色模式，即 `Document.mode`。另请参阅 `Document.changeMode()`。 |
| `EditLogItemsType` | `CONCISE`, `DETAILED`, `SESSIONONLY` | 历史记录中首选的详细程度，在 `Preferences` 中设置。 |
| `ElementPlacement` | `INSIDE`, `PLACEATBEGINNING`, `PLACEATEND`, `PLACEBEFORE`, `PLACEAFTER` | 对象在图层面板中的位置。**注意**：并非所有值对所有对象类型都有效。 |
| `EliminateFields` | `EVENFIELDS`, `ODFIELDS` | 要消除的字段。传递给 `ArtLayer.applyInterlace()`。 |
| `ExportType` | `ILLUSTRATORPATHS`, `SAVEFORWEB` | `Document.exportDocument()` 的导出类型。 |
| `Extension` | `LOWERCASE`, `NONE`, `UPPERCASE` | `Document.saveAs()` 保存时的文件名扩展。 |

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `FileNamingType` | `DDMM`, `DDMMYY`, `DOCUMENTNAMELOWER`, `DOCUMENTNAMEMIXED`, `DOCUMENTNAMEUPPER`, `EXTENSIONLOWER`, `EXTENSIONUPPER`, `MMDD`, `MMDDYY`, `SERIALLETTEROWER`, `SERIALLETTERUPPER`, `SERIALNUMBER1`, `SERIALNUMBER2`, `SERIALNUMBER3`, `SERIALNUMBER4`, `YYMMDD`, `YYYYMMDD` | `Application.batch()` 方法一起使用的命名选项。 |
| `FontPreviewType` | `HUGE`, `EXTRALARGE`, `LARGE`, `MEDIUM`, `NONE`, `SMALL` | 字体菜单中预览的字体大小，在 `Preferences` 中设置。 |
| `FontSize` | `LARGE`, `MEDIUM`, `SMALL` | 对话框的首选字体大小，在 `Preferences` 中设置。 |
| `ForcedColors` | `BLACKWHITE`, `NONE`, `PRIMARY`, `WEB` | `BLACKWHITE`：纯黑和纯白。`NONE`：无。`PRIMARY`：红、绿、蓝、青、洋红、黄、黑和白。`WEB`：16种安全颜色。 |
| `FormatOptions` | `OPTIMIZEDBASELINE`, `PROGRESSIVE`, `STANDARDBASELINE` | `JPEGSaveOptions` 中保存 JPEG 文件使用的选项。 |
| `GalleryConstrainType` | `CONSTRAINBOTH`, `CONSTRAINHEIGHT`, `CONSTRAINWIDTH` | 图像要约束的比例类型。用于 `GalleryImagesOptions`。 |

---

## 更多常量

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `GalleryFontType` | `ARIAL`, `COURIERNEW`, `HELVETICA`, `TIMESNEWROMAN` | 用于照片画廊标题和其他文本的字体。 |
| `GallerySecurityTextColorType` | `BLACK`, `CUSTOM`, `WHITE` | 画廊图像上的文本颜色。 |
| `GallerySecurityTextPositionType` | `CENTERED`, `LOWERLEFT`, `LOWERRIGHT`, `UPPERLEFT`, `UPPERRIGHT` | 画廊图像上的文本位置。 |
| `GallerySecurityTextRotateType` | `CLOCKWISE45`, `CLOCKWISE90`, `COUNTERCLOCKWISE45`, `COUNTERCLOCKWISE90`, `ZERO` | 画廊图像上的文本方向。 |
| `GallerySecurityType` | `CAPTION`, `COPYRIGHT`, `CREDIT`, `CUSTOMTEXT`, `FILENAME`, `NONE`, `TITLE` | 画廊图像上的文本内容。 |
| `GalleryThumbSizeType` | `CUSTOM`, `LARGE`, `MEDIUM`, `SMALL` | 照片画廊中缩略图的大小。 |
| `Geometry` | `HEPTAGON`, `HEXAGON`, `OCTAGON`, `PENTAGON`, `SQUARE`, `TRIANGLE` | 形状选项，传递给 `ArtLayer.applyLensBlur()`。 |
| `GridLineStyle` | `DASHED`, `DOTTED`, `SOLID` | 图像上的非打印网格。 |
| `GridSize` | `LARGE`, `MEDIUM`, `SMALL` | 网格间距。 |
| `GuideLineStyle` | `DASHED`, `SOLID` | 图像上的非打印参考线条，在 `Preferences` 中设置。 |
| `IllustratorPath` | `ALLPATHS`, `DOCUMENTBOUNDS`, `NAMEDPATH` | 使用 `Document.exportDocument()` 的路径。 |
| `Intent` | `ABSOLUTECOLORIMET`, `PERCEPTUAL`, `RELATIVECOLORIMET` | 使用 `Document.convertProfile()` 或 `Document.print()` 的渲染意图。 |
| `Justification` | `CENTER`, `CENTERJUSTIFIED`, `FULLYJUSTIFIED`, `LEFT`, `LEFTJUSTIFIED`, `RIGHT`, `RIGHTJUSTIFIED` | 段落在边界框内的放置。用于 `TextItem.justification`。 |
| `Language` | `BRAZILIANPORTUGUES`, `CANADIANFRENCH`, `DANISH`, `DUTCH`, `ENGLISHUK`, `ENGLISHUSA`, `FRENCH`, `GERMAN`, `ITALIAN`, `NORWEGIAN`, `OLDGERMAN`, `PORTUGUES`, `SPANISH`, `SWISSGERMAN` | 语言。用于 `TextItem.language`。 |
| `LayerCompression` | `RLE`, `ZIP` | 保存为 TIFF 格式时，图层数据的压缩方法。用于 `TiffSaveOptions`。 |

| 常量类型 | 值 | 含义 |
| :--- | :--- | :--- |
| `LayerKind` | `BLACKANDWHITE`, `BRIGHTNESSCONTST`, `CHANNELMIXER`, `COLORBALANCE`, `CURVES`, `EXPOSURE`, `GRADIENTFILL`, `GRADIENTMAP`, `HUESATURATION`, `INVERSION`, `LEVELS`, `NORMAL`, `PATTERNFILL`, `PHOTOFILTER`, `POSTERIZE`, `SELECTIVECOLOR`, `SMARTOJECT`, `SOLIDFILL`, `TEXT`, `THRESHOLD`, `LAYER3D`, `VIBRANCE`, `VIDEO` | 图层类型，见 `ArtLayer.kind`。只能从空白图层创建文字层。 |
| `LensType` | `MOVIEPRIME`, `PRIME105`, `PRIME35`, `ZOOMLENS` | 要使用的镜头类型。传递给 `ArtLayer.applyLensFlare()`。 |
| `MagnificationType` | `ACTUALSIZE`, `FITPAGE` | 查看图像时的缩放类型。 |
| `MatteType` | `BACKGROUND`, `BLACK`, `FOREGROUND`, `NETSCAPE`, `NONE`, `SEMIGRAY`, `WHITE` | 填充透明区域相邻的抗锯齿边缘的颜色。当图像透明度关闭时，哑光颜色应用于透明区域。 |
| `MeasurementRange` | `ALLMEASUREMENTS`, `ACTIVEMEASUREMENTS` | 执行操作的测量范围。传递给 `MeasurementLog` 方法。 |
| `MeasurementSource` | `MEASURESELECTION`, `MEASURECOUNTTOOL`, `MEASURERULERTOOL` | 记录测量的来源。传递给 `Document.recordMeasurements()`。 |
| `NewDocumentMode` | `BITMAP`, `CMYK`, `GRAYSCALE`, `LAB`, `RGB` | 文档使用的颜色配置文件。传递给 `Documents.add()`。 |
| `OperatingSystem` | `OS2`, `WINDOWS` | 目标操作系统。 |
| `Orientation` | `LANDSCAPE`, `PORTRAIT` | 页面方向。 |
| `OtherPaintingCursors` | `PRECISEOTHER`, `STANDARDOTHER` | 以下工具的首选指针。 |
| `PaintingCursors` | `BRUSHSIZE`, `PRECISE`, `STANDARD` | 以下工具的首选指针。 |
| `PathKind` | `CLIPPINGPATH`, `NORMALPATH`, `TEXTMASK`, `VECTORMASK`, `WORKPATH` | `PathItem` 的类型。 |
| `PDFCompatibility` | `PDF13`, `PDF14`, `PDF15`, `PDF16`, `PDF17` | 使文档兼容的 PDF 版本。 |
| `PDFEncoding` | `JPEG`, `JPEG2000HIGH`, `JPEG2000LOSSLESS`, `JPEG2000LOW`, `JPEG2000MED`, `JPEG2000MEDHIGH`, `JPEG2000MEDLOW`, `JPEGHIGH`, `JPEGLOW`, `JPEGMED`, `JPEGMEDHIGH`, `JPEGMEDLOW`, `NONE`, `PDFZIP`, `PDFZIP4BIT` | 将文档保存为 PDF 格式时的压缩类型。 |
| `PDFResample` | `NONE`, `PDFAVERAGE`, `PDFBICUBIC`, `PDFSUBSAMPLE` | 要使用的向下采样方法。 |
| `PDFStandard` | `NONE`, `PDFX1A2001`, `PDFX3202`, `PDFX3203`, `PDFX4008` | 使文档兼容的 PDF 标准。 |
| `PhotoColorSpace` | `LAB16`, `LAB8`, `RGB16` | 颜色空间。 |
| `PhotoCDSize` | `EXTRALARGE`, `LARGE`, `MEDIUM`, `MINIMUM`, `SMALL` | 像素尺寸。 |
| `QuickMaskMode` | `91` | 快速蒙罩。 |

---
*(注：由于原文文本存在大量重复且破碎的索引，以上内容已提取核心常量定义并进行了规范排版。)*