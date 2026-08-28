
# JavaScript 自动化：更多实用且有趣的脚本

![](img/cover.jpeg)

# 前言

在本书系列的第一本回顾计算机“脚本化”历史时，我对 Python 的提及寥寥无几，我希望在本系列的第三作中弥补这一遗憾。

## Python 作为一种脚本语言

Python 是一种高级解释型编程语言，以其简单、可读性和多功能性著称。作为一种脚本语言，Python 在自动化任务、处理系统管理和集成软件组件方面表现出色。以下是 Python 成为脚本理想选择的概述：

### Python 的核心特性

1. **易于学习和使用**：
   - Python 的语法清晰直观，初学者也能上手。它的代码易于阅读和编写，降低了学习曲线并提高了生产力。

2. **解释型语言**：
   - Python 是一种解释型语言，意味着代码按行执行，允许即时反馈和快速开发周期。这一特性使得调试和测试脚本更加高效。

3. **跨平台兼容性**：
   - Python 脚本可以在包括 Windows、macOS 和 Linux 在内的各种操作系统上运行，无需修改。这种跨平台的特性确保了 Python 脚本具有高度的可移植性。

4. **丰富的标准库**：
   - Python 拥有全面的标准库，为各种任务（如文件处理、系统操作、互联网协议和数据处理）提供了许多模块和函数。这一丰富的库减少了从零开始编写代码的需求。

5. **庞大且活跃的社区**：
   - Python 拥有庞大且活跃的用户社区，贡献了大量的第三方模块和包。这个生态系统支持从 Web 开发、数据分析到机器学习和自动化的各种应用。

6. **集成能力**：
   - Python 可以轻松与其他语言和工具集成，使其成为多环境中脚本编写的通用选择。它可以与 `C/C++`、`Java` 以及其他编程语言交互，以及各种 API 和 Web 服务。

7. **自动化与脚本**：
   - Python 广泛用于自动化重复任务，如文件操作、数据提取和批量处理。它用极少代码编写复杂工作流的能力使其成为系统管理员和开发者的强大工具。

8. **面向对象与函数式编程**：
   - Python 支持面向对象和函数式编程范式。这种灵活性允许开发者根据特定需求选择最佳方法，增强了代码的可重用性和维护性。

### Python 脚本的应用

- **系统管理**：自动化例行任务、管理系统配置和监控系统健康。
- **网络爬虫**：从网站提取数据以进行分析或与其他系统集成。
- **数据分析**：使用 `pandas` 和 `NumPy` 等库处理和分析大型数据集。
- **Web 开发**：使用 `Django` 和 `Flask` 等框架构建 Web 应用。
- **软件测试自动化**：编写测试脚本以自动化应用程序的测试。
- **任务自动化**：自动化工作流，例如文件的批量处理、发送电子邮件和与 API 交互。

Python 简单性、多功能性和强大库的结合使其成为脚本的极佳选择。无论你是寻求自动化小任务的初学者，还是构建复杂自动化脚本的资深开发者，Python 都能提供高效完成工作所需的工具和支持。

## SwiftUI - 未来之？

这并不是科学的论断，更像是一种思考。我花了一些时间研究 `SwiftUI`，在某些方面我认为它可能主宰一切。

# 在脚本编辑器中使用 OpenAI API 生成 JXA 代码

在本章中，我们将探索将 JavaScript for Automation (JXA) 与 OpenAI API 集成的实用示例。目标是创建一个与 OpenAI 强大的 `GPT-3.5` 模型交互的自动化脚本，通过先进的 AI 洞察增强 Mac 用户的脚本能力。

## 准备工作

我们首先初始化 JXA 环境并设置必要的应用程序。脚本利用 `Script Editor` (`se`) 应用程序进行脚本的执行和操作，并结合当前应用上下文（`app`）利用标准脚本插件。

```javascript
const se = Application("Script Editor");
const app = Application.currentApplication();
app.includeStandardAdditions = true;
```

## 定义用户交互

我们脚本的核心在于 `getPresetsText` 函数，该函数旨在向用户显示包含预设选项的对话框。这些预设从代码重写到注释生成，反映了用户可能想要自动化的典型脚本任务。

```javascript
function getPresetsText() {
  // 预设选项数组
  const presets = [
    "1 - Rewrite this code to be more efficient",
    "2 - Continue this code",
    "3 - Write a function with this code",
    "4 - Write comments for this code"
  ];

  // 显示对话框并捕获用户输入
  const response = app.displayDialog(presets.join('\n'), {
    defaultAnswer: '4'
  });

  // 解析用户的选择并返回对应的预设文本
  const inputNumber = parseInt(response.textReturned);
  return presets[inputNumber - 1] || "Invalid input";
}
```

## 准备用于提交的代码

为了确保代码适用于 OpenAI API 处理，我们实现了一个 `cleanString` 函数。该函数通过将换行符和制表符替换为空格来整理字符串，使其更适合 API 传输。

```javascript
function cleanString(inputString) {
  return inputString.replace(/[\n\t]/g, ' ');
}
```

## 处理用户选择

脚本随后检查用户是否在脚本编辑器（Script Editor）中选择了任何文本。如果没有，它会提示用户输入想要生成的代码类型。如果有选中，它将使用 `getPresetsText` 函数确定用户的意图，并为 API 交互准备选中的文本。

## 构建 API 请求

准备好的文本将进行编码以确保安全传输，并整合到 `curl` 命令中，格式化为 JSON 负载。该命令旨在与 OpenAI 的 GPT-3.5 模型交互，发送一个包含用户意图以及选中或输入代码的请求。

```javascript
const command = `curl https://api.openai.com/v1/chat/completions ...`;
```

## 错误处理与响应处理

脚本执行 `curl` 命令并解析来自 OpenAI API 的 JSON 响应。它能够优雅地处理潜在错误，确保脚本运行的健壮性。收到的响应（可能包含 AI 生成的代码或注释）将被插入脚本编辑器，完成集成循环。

```javascript
try {
  // 执行并解析 API 响应
  const jsonObj = app.doShellScript(command);
  const obj = JSON.parse(jsonObj);

  // 将 AI 生成的内容插入脚本编辑器
  const thisMessage = obj.choices[0].message.content + '\n\n';
  se.documents[1].selection.contents = thisMessage;
} catch (error) {
  // 错误处理
  console.error("An error occurred: ", error);
}
```

此示例展示了 JXA 与 OpenAI API 的无缝集成，演示了 Mac 自动化脚本如何通过 AI 驱动的能力得到提升。通过这种集成，用户可以直接在 Mac 上利用 GPT-3.5 的力量来自动化、增强甚至生成新的 JavaScript 代码。

# 通过 GPT 进行 Mp4 音频转录

该脚本旨在自动化涉及视频文件转换和音频转录的任务序列，使用了 Apple 的 JavaScript 自动化（JXA）以及 FFmpeg 和 OpenAI API 等外部工具。以下是脚本的逐步说明，并带有解释每个部分的注释：

### 1. 初始化 JXA 对象

```javascript
app = Application.currentApplication()
app.includeStandardAdditions = true
```

- 初始化当前脚本的 `Application` 对象并包含标准脚本扩展，允许使用对话框、文件选择对话框等。

### 2. 转义特殊字符的函数

```javascript
function escapeCharacters(str) {
  return str.replace(/~/g, '\\~').replace(/&/g, '\\&');
}
```

- 定义函数 `escapeCharacters` 用于转义字符串中的特殊字符（`~` 和 `&`）。这对于清理将用于 shell 命令的文件路径或字符串非常有用。

### 3. 文件选择对话框

```javascript
filePath = app.chooseFile({withPrompt:"Choose an MP4 or M4v Movie file"})
inFile = filePath.toString()
```

- 打开文件对话框，要求用户选择一个 MP4 或 M4v 电影文件。选中的文件路径被转换为字符串。

### 4. 提取文件名并准备输出路径

```javascript
filePathParts = inFile.split('/')
fileName = filePathParts[filePathParts.length-1].split('.')
outFile = `/users/homefolder/${fileName[0]}.mp3`
```

- 将选中的文件路径拆分（以 `/` 分隔），提取文件名，并在用户目录下准备一个带有 `.mp3` 扩展名的输出文件路径。

### 5. 用于提取音频的 FFmpeg 命令

```javascript
command = `/usr/local/bin/ffmpeg -i ${inFile} ${outFile}`
response = app.doShellScript(command)
```

- 构建命令使用 FFmpeg 从选定的视频文件中提取音频并将其保存为 MP3 文件。使用 `doShellScript` 执行该命令。

### 6. 显示对话框并等待用户

```javascript
holder = app.displayDialog("Wait")
```

- 显示带有“Wait”消息的对话框。这可能是为了在继续之前等待用户确认的占位符。这里可以根据典型的处理速度设计一个计时，推延迟转录直到 ffmpeg 完成其工作。

### 7. 检查用户响应并继续

```javascript
if (holder.buttonReturned === "OK"){
  // API 调用和转录逻辑
} else {
  app.displayAlert("No")
}
```

- 检查用户是否在对话框中点击了“OK”。如果没有，则显示带有“No”消息的警告。

### 8. 用于转录的 API 调用

```javascript
command = "curl --request POST --url https://api.openai.com/v1/audio/transcriptions " +
"--header 'Authorization: Bearer $OPEN-API-KEY' " +
"--header 'Content-Type: multipart/form-data' " +
"--form file=@" + outFile + " --form model=whisper-1";

try {
  jsonObj = app.doShellScript(command);
  obj = JSON.parse(jsonObj);
  console.log(obj.text)
} catch (error) {
  console.log("An error occurred: " + error);
}

app.setTheClipboardTo(obj.text)
```

- 构建 `curl` 命令向 OpenAI 音频转录 API 发送 POST 请求，使用生成的 MP3 文件。
- 脚本尝试执行命令、解析 JSON 响应并将转录打印到控制台。
- 如果成功，转录将被复制到剪贴板。如果发生错误，则记录错误信息。

此脚本要求用户已安装 FFmpeg 可以在 `/usr/local/bin/ffmpeg` 访问，并假设 OpenAI API 令牌直接在脚本中或通过其他方式提供。脚本未对文件选择或 FFmpeg 命令执行进行错误检查，因此假设这些操作是成功的。此外，API 令牌必须包含在脚本中，以便转录 API 调用能够正常工作。

# 使用自定义 GPT 为 Pages 文档创建索引的脚本

```javascript
// 来自 Pages 的源文本
pages = Application("Pages")

// 转换为 Safari Web 应用
gpt = Application("ChatGPT")

// 用于按键的系统事件
var se = Application('System Events')

// 提供剪贴板访问
app = Application.currentApplication()
app.includeStandardAdditions = true

// 前台 Pages 文档
doc = pages.documents[0]

// 预提示 (Pre-prompt)
pageContent = "Index the following text using the page number provided: "

// 起页
startingPage = 3

// 将十页循环到索引内容中
for (i=startingPage;i<startingPage+2;i++){
  pageNum = i+1 // 获取页码
  currentPage = doc.pages[i].bodyText() // 获取每页的正文
  // 编译预提示、页面内容、页码
  pageContent = pageContent + currentPage + " " + pageNum
}

// 将数据放入剪贴板
app.setTheClipboardTo(pageContent)

// 激活 GPT 应用
gpt.activate()
delay(1)

// 确保输入文本框获得焦点
se.keyCode(53, { using: ["shift down"] });
delay(1)

// 粘贴到 ChatGPT 你可以使用位于 https://chat.openai.com/g/g-Fv9AmeZvV-index-master 的自定义 GPT "Index Master"
se.keystroke("v", { using: ["command down"] })
delay(1)

// 按回车键
se.keyCode(76)
```

/ 一旦 ChatGPT 返回索引，可以使用 Shift-command-down 进行复制。在此系统中，不同的部分将以不同的格式返回。这是聊天回复具有不确定性的一部分。文本将需要被编译和重新格式化。 /

此脚本集成了用于自动化的 JavaScript (JXA)，用于 Mac 上的不同应用程序之间执行一系列任务，特别针对 Pages、运行 ChatGPT 网页版版本的 Safari，并利用系统事件（System Events）进行自动化。

以下是该脚本执行内容的逐步说明：

1. **访问 Pages 应用程序**：脚本通过创建一个对象来与 Pages 应用程序交互，允许其对 Pages 文档进行操作并检索数据。
2. **作为 Safari 网页应用访问 ChatGPT**：随后，它设置一个对象，通过在 Safari 中打开的网页应用版本与 ChatGPT 交互，表示有意将数据发送到 ChatGPT 进行处理。
3. **用于按键模拟的系统事件**：通过创建 `System Events` 对象，脚本可以模拟键盘输入，这种方法通常用于自动化处理脚本环境中没有直接 API 支持的交互。
4. **剪贴板访问**：它准备让当前应用程序（脚本本身）包含标准添加项，这对于与系统剪贴板交互以复制和粘贴数据是必要的。
5. **从 Pages 文档检索内容**：脚本访问 Pages 中打开的第一个文档，并开始循环从指定的起始页读取正文文本，此处假设起始页为第三页（`startingPage = 3`），并持续两页。它将这些内容与递增的页码合并成单个字符串，并在前面加上自定义消息（`"使用提供的页码对文本进行索引："`）。
6. **将数据复制到剪贴板**：编译后的字符串（现在包含了指定页面的文本及其相应的页码）被复制到剪贴板。
7. **激活 ChatGPT 网页应用**：脚本切换焦点到 Safari 网页应用版本的 ChatGPT，准备输入复制的文本。
8. **用于输入的按键**：它模拟快捷键以确保输入区域获得焦点，然后通过模拟 `CMD+V`（粘贴）操作将剪贴板内容粘贴到 ChatGPT 输入字段。
9. **提交查询**：最后，脚本模拟按下回车键将查询提交给 ChatGPT。

一旦 ChatGPT 处理了提交的文本，用户将手动处理响应。“Index Master”是一个专为文档索引设计的自定义 ChatGPT 模型。

这种自动化可以是大型文档管理工作流的一部分，通过 ChatGPT 的处理能力实现 Pages 文档文本索引的自动化。该脚本巧妙地使用 JXA 弥合了应用程序与网络服务之间的差距，展示了 macOS 上自动化的多功能性。

# 从 JXA 调用 Python 脚本以接口 OpenAI API

此脚本由两个部分组成：用于 macOS 的 JXA（用于自动化的 JavaScript）代码段和一个 Python 脚本。让我们对每个部分进行注释以便说明。

### JXA 代码说明

1. **初始化**：
```
app = Application.currentApplication()
app.includeStandardAdditions = true
```
- `Application.currentApplication()` 初始化当前脚本以使用 macOS 的脚本功能。
- `app.includeStandardAdditions = true` 启用使用显示对话框、运行 shell 脚本等标准命令。

2. **显示对话框**：
```
response = app.displayDialog("Prompt?", {defaultAnswer: 'a cat in shades of blue'})
```
- `app.displayDialog` 向用户显示一个对话框。在这里，它问了一个问题（“Prompt?”）并提供了一个默认答案（“蓝色调的猫”）。

3. **获取用户输入**：
```
parameter = response.textReturned
```
- `response.textReturned` 从对话框获取用户输入的文本。

4. **准备 Shell 命令**：
```
command = "/usr/local/bin/python ~/openaiapi/inp.py '" + parameter + "'"
```
- 构建一个运行位于 `~/openaiapi/inp.py` 的 Python 脚本的命令。用户的输入（`parameter`）将作为参数传递给该脚本。

5. **执行 Shell 命令**：
```
theTry = app.doShellScript(command)
```
- `app.doShellScript` 在 shell 中执行构建的命令。

6. **打开 URL**：
```
app.openLocation(theTry)
```
- `app.openLocation` 打开一个 URL。在这里，预计 Python 脚本返回一个 URL 作为输出，然后将其打开。

### Python 代码说明

1. **导入**：
```python
from openai import OpenAI
import webbrowser
import sys
```
- 导入必要的模块：用于与 OpenAI API 交互的 `openai`，用于打开 URL 的 `webbrowser` 以及用于处理命令行参数的 `sys`。

2. **初始化 OpenAI 客户端**：
```python
client = OpenAI(api_key='OPEN-AI KEY)
```
- 使用特定的 API key 初始化 OpenAI 客户端。

3. **命令行参数处理**：
```python
if len(sys.argv) > 1:
    parameter = sys.argv[1]
else:
    parameter = "A cat in a hat"  # 如果未提供参数的默认值
```
- 检查是否提供了命令行参数（来自 JXA 脚本）。如果没有，则使用默认值。

4. **图像生成请求**：
```python
response = client.images.generate(
    model="dall-e-3",
    prompt=parameter,
    size="1024x1024",
    quality="standard",
    n=1,
)
```
- 调用 OpenAI 的 DALL-E 3 模型，根据提供的提示词（`parameter`）生成图像。指定图像大小、质量和图像数量（在此情况下为 1）。

5. **检索图像 URL**：
```python
image_url = response.data[0].url
```
- 从响应中提取生成图像的 URL。

6. **在网页浏览器中打开图像**：
```python
webbrowser.open(image_url)
```
- 在默认网页浏览器中打开图像 URL。

### 整体流程

- JXA 脚本提示用户输入，带输入作为参数运行 Python 脚本，并期望返回 URL。
- Python 脚本使用 OpenAI API 根据输入生成图像，并在网页浏览器中打开生成的图像。

使用名为 "JXA Helper" 的自定义 GPT

![](img/image_rsrc16X.jpg)

# 查询 Google Gemini API

```javascript
app = Application.currentApplication()
app.includeStandardAdditions = true
bebe = Library('bebe')
prompt = "make list of ways to research javescript language"
command = `curl -H 'Content-Type: application/json' -d '{"contents":[{"parts":[{"text":"${prompt}"}]}]}' -X POST https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=API-KEY`
try {
    jsonObj = app.doShellScript(command)
    obj = JSON.parse(jsonObj)
    geminiText = obj.candidates[0].content.parts[0].text
} catch (error) {
    response = app.displayAlert(error.message, {
        message: error.message,
        as: 'critical'
    })
}
bebe.newBBDocWithText ('JSON',geminiText)
```

脚本与外部 API 交互，解析响应，然后使用库创建一个新文档。以下是该脚本执行内容的逐步说明：

1. **初始化应用程序对象**：它通过创建当前应用程序的实例（`Application.currentApplication()`）并启用标准 OS 添加项，如显示警报或运行 shell 脚本（`app.includeStandardAdditions = true`）。
2. **导入库**：导入一个名为 'bebe' 的库（`Library('bebe')`）。该库在脚本后部分用于创建新文档，表明它提供了某些文档管理功能。
3. **准备 API 调用**：设置变量 `prompt`，文本为“make list of ways to research javascript language”（列出研究 javascript 语言的方法）。这是将发送到外部服务的数据。
4. **CURL 命令构建**：构建一个 `curl` 命令，向 `https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent` 发送 POST 请求，并带有 JSON 负载（payload）。该负载包含 `prompt` 变量的内容。该命令结构用于向 API（由占位符 `API-Key` 标识）发送 JSON 请求。
5. **执行并处理 API 响应**：
   - Try 块：使用 `app.doShellScript(command)` 方法执行 `curl` 命令，并将 JSON 响应捕获在 `jsonObj` 中。
   - 使用 `JSON.parse(jsonObj)` 将 `jsonObj` 字符串解析为对象（`obj`）。
   - 从解析的对象中提取特定的文本（`geminiText`），这似乎是 API 响应 prompt 返回的主要内容。
6. **错误处理**：如果在执行 `curl` 命令或处理 JSON 响应时发生错误，它将捕获错误并使用 `app.displayAlert` 显示带有错误信息的警告框。
7. **'bebe' 库的使用**：使用 'bebe' 库创建一个新文档（`bebe.newBBDocWithText ('JSON',geminiText)`），使用从 API 响应中提取的文本。

此脚本本质上自动化了向外部生成语言模型 API 发送 prompt、接收响应并使用响应通过自定义库创建新文档的过程。

# 为照片中的选定图片添加关键词

```javascript
// JXA 脚本，用于为 macOS 照片应用中的选定照片添加关键词并可选地更新说明

// 初始化照片应用并包含用于对话框和警告的标准扩展
const Photos = Application('Photos');
Photos.includeStandardAdditions = true;
Photos.activate(); // 将照片应用带到前台

// 获取当前选择的照片
const selection = Photos.selection();

// 检查是否至少选择了一张照片
if (selection.length < 1) {
  Photos.displayAlert("未选择照片", {
    message: "运行脚本之前必须选择一张照片。",
    as: "warning"
  });
} else {
  // 提示用户输入关键词
  const keywordsToAdd = userInput("请输入用逗号分隔的关键词:", "keys").split(",");

  // 遍历每张选定的照片
  selection.forEach(photo => {
    // 获取现有关键词并与新关键词合并
    const existingKeywords = photo.keywords();
    const combinedKeywords = keywordsToAdd.concat(existingKeywords);

    // 更新照片的关键词
    photo.keywords = combinedKeywords;

    // 询问用户是否也更新说明
    const captionChoice = Photos.displayDialog('关键词已添加。您是否也想更新说明？', {
      buttons: ["取消", "也更新说明", "仅关键词"],
      defaultButton: "仅关键词"
    });

    // 根据用户的选择处理说明更新
    if (captionChoice.buttonReturned === "也更新说明") {
      const newCaption = userInput("请输入说明:", "cap");
      photo.description = newCaption; // 更新照片的说明
    }
  });
}

// 向用户显示对话框并返回输入的函数
function userInput(prompt, type) {
  const response = Photos.displayDialog(prompt, {
    defaultAnswer: "",
    buttons: ["确定"],
    defaultButton: "确定"
  });
  return response.textReturned; // 返回用户的输入文本
}
```

此 JavaScript 自动化（JXA）脚本旨在增强 macOS 照片应用中选定照片的元数据。它通过向每张选定照片添加用户指定的关键词来实现，并提供了更新照片说明的选项。脚本遵循结构化方法来实现目标，确保了直观且高效的用户体验。

以下是脚本功能的详细说明：

1. **初始化并聚焦照片应用**：脚本首先初始化与照片应用的连接，并包含用于对话框和警告的标准扩展。然后它将照片应用带到前台，确保其准备好与用户交互。
2. **选择验证**：它检查用户是否在照片应用中至少选择了一张照片。如果没有选择照片，将显示警告框，提示用户在运行脚本之前选择照片。
3. **关键词输入**：脚本提示用户输入要添加到选定照片的关键词。用户在对话框中输入这些关键词，并用逗号分隔。
4. **使用关键词更新照片（可选更新说明）**：
   - 对于每张选定的照片，脚本获取任何现有关键词并将其与用户提供的新关键词合并。
   - 然后，使用此合并后的关键词列表更新选定的照片。
   - 更新关键词后，脚本询问用户是否也想更新选定照片的说明。
   - 如果用户选择更新说明，将弹出一个对话框，允许用户输入新说明。该说明随后将应用到照片。
   - 如果用户选择不更新说明或选择取消，脚本将在不修改照片说明的情况下继续。
5. **通过对话框进行用户交互**：脚本在输入和确认步骤中使用了对话框，增强了交互性。这包括输入关键词、决定是否更新说明以及输入说明本身。

此脚本简化了在照片应用中增强照片元数据的过程，使用户能够更有效地组织和注释他们的照片集。通过自动化添加关键词和更新说明的选项，它节省了时间并确保了照片元数据的一致性。

# 显示文件的 Spotlight 信息

```javascript
// 选择文件将显示所有非空的 Spotlight 信息并放入 TextEdit 文档
app = Application.currentApplication()
app.includeStandardAdditions = true
file = app.chooseFile({withPrompt:"选择一个文件以获取 kMDItem 信息"})
thePath = Path(file)
info = app.doShellScript("mdls '" + file + "'")
kMDinfo = ""
elements = info.split('\r')
elements.forEach(element => {
  if(!element.includes('null')){
    kMDinfo = kMDinfo + element + '\n'
  }
})
textedit = Application("TextEdit")
document = textedit.make({new: "document"})
document.text = kMDinfo
document.text.color = [256, 40421, 398]
```

此脚本允许用户在 Mac 上选择一个文件，然后检索并显示该文件所有可用的 Spotlight 元数据，排除任何空值的元数据值。以下是脚本执行步骤的详细说明：

1. 它使用标准扩展初始化当前应用程序，使其可以使用系统对话框和 shell 脚本。
2. 用户被提示选择一个文件。脚本随后捕获所选文件的路径。
3. 它带有所选文件的路径执行 shell 命令（`mdls`）以检索其元数据。`mdls` 命令用于列出 macOS 中文件的元数据属性。
4. 脚本处理 `mdls` 命令的输出，按换行符（`\r`）分割。
5. 它随后遍历元数据信息的每一行。如果某一行不包含字符串 'null'（表示该元数据属性有值），则将其添加到字符串变量中，并用换行符进行分隔。
6. 在过滤掉空值后，脚本在 TextEdit 中创建一个新文档。
7. 它将文档的文本设置为过滤后的元数据信息。
8. 最后，它将文档中的文本颜色设置为特定的颜色值。

总结来说，该脚本旨在提供一种用户友好的方法，使用 Spotlight 的 `mdls` 命令查看 macOS 上任何文件的非空元数据，并将结果显示在新的 TextEdit 文档中。

## 将 Numbers 表格数据转换为 JSON

以下是该脚本执行步骤的逐步拆解：

- **加载 bebe 库**：脚本首先加载 `bebe` 库，假设该库提供了处理文件的功能。
- **访问 Numbers 应用程序和活动表格**：脚本访问 `Numbers` 应用程序，并获取第一个文档中活动工作表中的第一个表格。该表格存储了要转换为 JSON 的数据。
- **确定行数和列数**：脚本计算表格的行数和列数，以了解需要处理的数据范围。
- **获取列标题**：脚本遍历表格的第一行（假设为表头行），并收集每个单元格的值。这些值将用作 JSON 对象的键（key）。
- **将表格行转换为 JSON 对象**：对于表格中的每一行，脚本都会创建一个新对象（`rowObj`）。然后，它遍历行中的每个单元格，使用列标题作为键，单元格的值作为值。每个完成的 `rowObj` 代表表格中的行，并添加到 `sheetArray` 中。
- **将数组转换为 JSON**：一旦处理完所有行，使用 `JSON.stringify` 将 `sheetArray` 转换为 JSON 字符串。该字符串（`jText`）代表 JSON 格式的整个表格。
- **创建包含 JSON 内容的新文档**：最后，脚本使用 `bebe` 库创建一个名为 "Json File" 的新文档，其中包含 JSON 字符串。

最终结果是一个 JSON 文件，它镜像了 Numbers 中原始表格的结构，每行都表示数组中的一个对象，每个列标题都作为对象中对应值的键。

```javascript
bebe = Library("bebe")
numbersApp = Application('Numbers');
frontTable = numbersApp.documents[0].activeSheet().tables[0];
theRows = frontTable.rowCount();
theCols = frontTable.columnCount();
sheetArray = [];

// 获取列标题
columnHeadings = [];
for (j = 0; j < theCols; j++) {
  columnHeadings.push(frontTable.rows[0].cells[j].value());
}

// 使用列标题作为键将行转换为对象
for (i = 0; i < theRows; i++) {
  rowObj = {};
  for (j = 0; j < theCols; j++) {
    key = columnHeadings[j];
    value = frontTable.rows[i].cells[j].value();
    rowObj[key] = value;
  }
  sheetArray.push(rowObj);
}

jText = JSON.stringify(sheetArray, null, 2);

// 假设 bebe 是处理文件的库
bebe.newBBDocWithText("Json File", jText);
```

## 使用名为 "JXA Helper" 的自定义 GPT

**网站**：https://chat.openai.com/g/g-yKtWFdI87-jxa-helper

**提示词**：编写一个 JXA 脚本，从 Numbers 中获取 A1-H16 单元格，并根据行创建一系列 Keynote 幻灯片，然后编写演示文脚本。

编写一个 JXA（JavaScript for Automation）脚本来从 Numbers 表格检索数据，并使用这些数据创建 Keynote 幻灯片，最后起草演示脚本，涉及几个步骤。以下是你可以完成此任务的基本大纲。请记住，此脚本假设你有一个在 A1-H16 单元格中有数据的 Numbers 文档，并且使用 Keynote 根据这些数据创建幻灯片。

```javascript
// 定义一个从 Numbers 获取数据的函数
function getDataFromNumbers() {
  const Numbers = Application('Numbers');
  Numbers.activate();
  const doc = Numbers.documents[0]; // 假设文档已打开且是第一个
  const sheet = doc.sheets[0]; // 假设数据在第一个工作表中
  const table = sheet.tables[0]; // 假设数据在第一个表格中
  // 范围 A1-H16
  const range = table.ranges['A1:H16'];
  const data = range.cells.value();
  return data;
}

// 定义一个创建 Keynote 幻灯片的函数
function createKeynoteSlides(data) {
  const Keynote = Application('Keynote');
  Keynote.activate();
  const doc = Keynote.documents[0]; // 假设文档已打开且是第一个
  data.forEach((row, index) => {
    const slide = Keynote.Slide({body: row.join(' ')}); // 将行数据合并为字符串作为幻灯片正文
    doc.slides.push(slide);
  });
}

// 定义一个数据生成演示脚本的函数
function generatePresentationScript(data) {
  let script = "演示脚本:\n\n";
  data.forEach((row, index) => {
    script += `幻灯片 ${index + 1}: ${row.join(', ')}\n\n`;
  });
  return script;
}

// 协调工作流的主函数
function main() {
  const data = getDataFromNumbers();
  createKeynoteSlides(data);
  const presentationScript = generatePresentationScript(data);
  console.log(presentationScript);
}

// 执行主函数
main();
```

此脚本执行以下操作：

1. 从 Numbers 表格检索数据（A1-H16），位于第一个工作表的第一个表格中。
2. 根据该数据创建 Keynote 幻灯片。
3. 然后起草演示脚本。

请确保在运行此脚本之前，已打开了包含对应数据的 Numbers 文档。

## 从 Filemaker 调用 Google 的 API

```javascript
app = Application.currentApplication()
app.includeAdditions = true
fm = Application("Filemaker")
se = Application("System Events")
db = fm.layouts['Picture List']
len = db.records().length
for(i=0;i<len;i++){
  rawText = db.records[i].cells[1]()
  rawText = rawText.replaceAll("'", "")
  rawText = rawText.replaceAll('\n','')
  rawText = rawText.replaceAll('','')
  rawText = rawText.replaceAll(':','')
  prompt = "为以下内容写一份 250 字的事实简介：" + rawText
  command = `curl -H 'Content-Type: application/json' -d '{"contents":[{"parts":[{"text":"${prompt}"}]}]}' -X POST https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=API-KEY`
  try {
    jsonObj = app.doShellScript("/usr/local/bin/bash; " + command)
    obj = JSON.parse(jsonObj)
    googleText = obj.candidates[0].content.parts[0].text
  } catch (error) {
    response = app.displayAlert(error.message, {
      message: error.message,
      as: 'critical'
    })
  }
  delay(5)
  db.records[i].cells[2] = googleText
}
```

4. **确定记录数量**：它计算'Picture List' 布局中存在的记录（艺术家）总数。

5. **遍历每条记录**：
- 对于每个记录，它从当前记录的第一个单元格中（假设单元格是数据库布局中的列）检索存储的艺术家名称。
- 通过移除特定的字符（`'`、`\n`、`"`、`:`）来清理艺术家名称，这些字符可能会导致随后的 API 请求出现问题。

6. **准备并发送 API 请求**：
- 通过将清理后的艺术家名称附加到预定义的请求文本（"Write a factual 250-word profile of the following blues artist: "）来构建提示词（prompt）。
- 使用 `curl` 构建一个命令将此提示词发送到外部 API（通过其 URL 识别并在请求中包含 API 密钥）。预计 API 将根据提示词生成内容。
- 在 bash shell 中执行该命令并捕获 JSON 响应。

7. **处理 API 响应**：
- 解析 JSON 响应以提取生成的内容。
- 如果发生错误（例如网络问题、API 错误），则显示带有错误消息的警报。

8. **更新数据库记录**：
- 使用生成的内容更新当前记录的第二个单元格。
- 在继续更新下一条记录之前包含 5 秒的延迟，可能是为了避免过载 API 或遇到速率限制。

9. **重复**：对'Picture List' 布局中的每条记录重复此过程，从而有效地在数据库中填充生成的数据。

此脚本自动化了数据库中艺术家简介的生成和更新，展示了数据库操作、外部 API 请求和错误处理在自动化脚本中的集成。

# 将页面从 Safari 传输到 Google Chrome

```javascript
Safari = Application('Safari')
Chrome = Application('Google Chrome')
myUrl = Safari.windows[0].currentTab.url()
Chrome.activate()
newWindow = Chrome.Window().make();
newWindow.tabs.push(Chrome.Tab({url: myUrl }));
```

此脚本旨在使用 JavaScript 自动化（JXA）与 Mac 上的 Safari 和 Google Chrome 浏览器交互。以下是其操作的逐步拆解：

1. **初始化 Safari 和 Chrome 的应用对象**：脚本首先为 Safari (`Application('Safari')`）和 Google Chrome (`Application('Google Chrome')`）创建应用对象。这些对象允许脚本控制并与每个浏览器交互。
2. **从 Safari 获取当前 URL**：然后使用 `Safari.windows[0].currentTab.url()` 获取 Safari 前台窗口当前标签页的 URL。这假设 Safari 正在运行并且至少有一个打开的活动标签页。
3. **激活 Google Chrome**：脚本激活 Google Chrome 将其置于顶层，使其成为屏幕上的活动应用程序。
4. **在 Chrome 中创建新窗口**：使用 `Chrome.Window().make();` 在 Google Chrome 中创建一个新窗口。此命令有效地打开了一个新的 Chrome 窗口。
5. **在 Chrome 中打开 Safari 的 URL**：最后，脚本在新创建的 Chrome 窗口中创建一个标签页，将其 URL 设置为之前从 Safari 当前标签页获取的 URL。这是通过 `newWindow.tabs.push(Chrome.Tab({url: myUrl }));` 实现的。

此脚本将 Safari 当前活动标签页的 URL 传输到 Google Chrome 新窗口的新标签页中，有效地跨浏览器复制标签。这对于需要使用多个浏览器并在它们之间移动会话或特定页面的用户特别有用。

对于那些大部分时间使用 Safari，但偶尔使用 Google Chrome 访问整个 Safari 生态系统之外网站的人来说，这非常方便。我设置了可以在 Microsoft Edge 之间发送 URL 的脚本，以便在我出于某种原因使用该浏览器时。

# 从长播放列表中提取 AI 选取的较短播放列表

Apple Music 允许创建包含数千首歌曲的超级播放列表。当你拥有一个包含数千首歌曲的播放列表时，能够生成多少个特定长度的独特播放列表是非常惊人的。最棒的部分是将超级播放列表设置为随机播放，每次都能获得独特的列表。但较大的脚本可以作为歌曲池。此脚本使用 AI 根据预设标准挑选歌曲。

此脚本是一个复杂的自动化工具，旨在简化 macOS 上 Music 应用程序中的播放列表管理。利用 JavaScript 自动化（JXA）的力量，脚本集成了多个 macOS 应用程序和功能，通过自动化与播放列表策划相关的重复任务来提高用户效率。

脚本首先初始化关键 macOS 应用程序：Music、ChatGPT、System Events 和当前应用程序。这种设置确保了脚本能够与这些应用程序无缝交互，利用它们的全部功能。标准组件的引入进一步扩展了脚本的功能，允许进行更复杂的操作。

脚本的一个主要功能是能够验证 Music 应用程序中是否存在指定的播放列表。此初始检查确保脚本在正确的数据集上运行，防止错误并提高可靠性。如果未找到指定的播放列表，脚本将记录相应的错误消息并停止后续执行，为用户提供清晰的反馈。

一旦确认了播放列表，脚本将继续提取轨道信息。它系统地收集播放列表中的歌曲名称，并将这些数据格式化为 CSV 字符串。这一步为后续处理准备了轨道信息，确保数据结构化以便于操作和分析。

然后，脚本为 ChatGPT 构建了一个详细的提示词，要求它从提供的列表中选择 25 首最有趣的歌曲。该提示词被复制到剪贴板，并激活 ChatGPT 处理请求。通过一系列模拟按键操作，脚本与 ChatGPT 交互，粘贴提示词、发送请求并检索响应。这种对 ChatGPT 的创新用法凸显了脚本将高级 AI 工具纳入决策过程的能力。

收到 ChatGPT 的响应后，脚本将处理歌曲列表，精炼数据以移除任何不必要的元素。它记录最终的歌曲列表，为被选中的项目提供透明视图。随后，脚本会在 Music 应用程序中创建一个新的播放列表，并进行命名以反映其来源，并将选中的歌曲复制到此新播放列表中。此功能展示了脚本不仅能够策划，还能有效地组织和管理音乐收藏。

本质上，此脚本体现了 JavaScript 自动化与 macOS 应用程序之间强大的协同作用。通过自动化复杂的播放列表管理过程，它节省了精力，让用户能够专注于享受音乐，而不是被行政任务所困。ChatGPT 的集成进一步增强了它的实用性，展示了利用 AI 进行实际日常应用的前瞻性方法。

## 如何在 macOS 上为 ChatGPT 网站创建 Web 应用以供脚本使用

### 使用 Web 应用的好处

- **独立功能**：Web App 的功能与 Safari 独立运行。它不会与 Safari 共享浏览历史、Cookies、网站数据或设置，确保你在 Web App 中的活动仅在该内部进行。
- **简洁界面**：Web App 具有极简主义风格的工具栏，仅包含后退、前进和分享按钮。这提供了一个干净且专注的用户界面。
- **可自定义**：你可以为 Web App 分配任何名称或图标，使其易于从 `Dock` 中被识别和访问。
- **通知**：如果网站支持通知，Web App 在 `Dock` 中的图标可以显示未读通知的数字。
- **类 App 行为**：Web App 的运行方式与其他任何其他 macOS 应用程序相同。你可以将其添加为登录项，这样它就会在你登录时自动打开。

## 创建 Web App 的步骤

1. **确保兼容性**：
   - 确保你的 macOS 版本为 `Sonoma` 或更高版本。
2. **在 Safari 中打开网页**：
   - 启动 `Safari` 并导航到 `ChatGPT` 网站。
3. **添加到 Dock**：
   - 从 `Safari` 菜单栏中，选择`文件` > `添加到 Dock`。
   - 或者，点击 `Safari` 工具栏中的`分享` 按钮，然后选择`添加到 Dock`。
4. **命名 Web App**：
   - 为你的 Web App 输入所需的名称（例如，“ChatGPT”）。
   - 点击`添加`。Web App 将保存到你用户目录下的 `应用程序` 文件夹中。
5. **访问 Web App**：
   - 现在你可以像打开其他应用程序一样，从 `Dock`、`启动台` 或 `Spotlight` 打开 Web App。

通过遵循这些步骤，你为 `ChatGPT` 网站创建了一个专用的 Web App。该 Web App 随后可以在你的自动化脚本中使用，确保为与 `ChatGPT` 的交互提供专门定制的流畅且隔离的浏览体验。

```javascript
music = Application('Music')
gpt = Application('ChatGPT')
gpt.includeStandardAdditions = true
se = Application('System Events')
app = Application.currentApplication()
app.includeStandardAdditions = true
prePrompt = ""
theLists = ["Ultimate Blues Collection Collection"]
existingPlaylist = music.playlists.whose({ name: theLists[0] })[0]

// Ensure the playlist exists
if (!existingPlaylist) {
console.log("Playlist not found: " + existingPlaylistName);
throw new Error("Playlist not found: " + existingPlaylistName);
}

for(i=0;i<theLists.length;i++){
  currentPlaylist = theLists[i]
  trackNames = []
  csvText = ''
  // Data
  theTracks = music.userPlaylists[currentPlaylist].tracks()
  len = theTracks.length
  theTracks.forEach(getName)
  tlen = trackNames.length
  trackNames.forEach(makeCsv)
}

prePrompt = "Pick out the 25 most interesting sogs from the provided list and produce a list in the format of a return-delimited list as code using \r: "
prompt = prePrompt + csvText
app.setTheClipboardTo(prompt)
gpt.activate()
// se.keystroke("o", { using: ["shift down","command down"] })
delay(2)
se.keyCode(53, { using: ["shift down"] })
delay(2)
se.keystroke("v", { using: ["command down"] })
se.keyCode(76)
delay(3)
gpt.displayDialog('Send to IDE', {buttons: ["Cancel", "Proceed"], defaultButton: "Proceed", withTitle: "Playlist Process", withIcon: "note", givingUpAfter: 60 })
delay(2)
se.keystroke("c", { using: ["shift down","command down"] })
content = app.theClipboard()
finalTracks = content.split("\r")
// Remove the first item: the apostrophes and plain text
finalTracks.shift()
// Remove the last item: the apostrophes
finalTracks.pop();
console.log(finalTracks.toString())
newPlaylist = music.Playlist().make()
newPlaylist.name = "Extracted from " + theLists[0]
newPlaylist.description = "This playlist is extracted from " + theLists[0]
delay(2)
for(j=0;j<finalTracks.length;j++){
  songName = finalTracks[j]
  console.log(songName + " ")
  console = existingPlaylist.tracks.whose({ name: songName })[0]
  delay(2)
  music.duplicate(song, { to: newPlaylist })
}

function getName(tr){
  trackNames.push(tr.name() + '\n')
}

function makeCsv(item){
  csvText += item
}
```

## 脚本逐步说明

1. **初始化应用程序**：
   - 脚本首先初始化 `Music` 应用程序、`ChatGPT` 应用程序、`System Events` 以及当前应用程序。它还为这些应用程序启用标准添加以扩展其功能。
2. **验证播放列表是否存在**：
   - 脚本检查 `Music` 应用中是否存在指定的播放列表。如果未找到播放列表，它将记录错误消息并停止后续执行。
3. **提取轨道信息**：
   - 脚本从指定的播放列表中检索所有曲目的名称。它将这些歌曲名称存储在列表中并将其格式化为 CSV 字符串，为后续处理准备数据。
4. **准备 ChatGPT 提示词 (Prompt)**：
   - 创建了一个详细的提示词，要求 `ChatGPT` 从提供的列表中选出 25 首最有趣的歌曲。该提示词被复制到剪贴板。
5. **激活 ChatGPT**：
   - 脚本激活 `ChatGPT` 并模拟按键粘贴提示词，发送请求。
6. **处理 ChatGPT 响应**：
   - 脚本处理来自 `ChatGPT` 的响应，提取轨道列表并清理不必要元素。
7. **创建新播放列表**：
   - 在 `Music` 应用中创建一个新的播放列表，其名称反映了来源。
8. **复制所选轨道**：
   - 脚本将 `ChatGPT` 选择的轨道复制到新创建的播放列表中。它遍历所选轨道列表，在现有的播放列表中查找每个曲目。
9. **记录并显示信息**：
   - 在整个过程中，脚本会记录相关信息并在需要时显示对话框，以让用户了解其进度以及任何需要确认的操作。

通过遵循这些步骤，该脚本自动化了策划和组织音乐播放列表的任务，结合了 macOS 自动化工具和通过 `ChatGPT` 进行 AI 驱动选择的力量。

# 客户支持

我想为 `BBEdit` 编写一个用于查找和替换的 JXA (JavaScript for Automation) 脚本。我在构思翻译方面有相当的经验，做得越多就越好。但不知为何，我无法在 JXA 脚本中让查找或替换方法工作。无论我如何调整语法，只能得到错误和异常结果。正如往常一样，还有其他方法。

首先，我可以使用效果良好的 AppleScript。这是一个清理网页抓取文本的脚本：

```
tell application "BBEdit"
  replace "\\." using "" searching in selection of text 1 of text document 1 options {search mode:grep, starting at top:true}
  replace "\\-" using "" searching in selection of text 1 of text document 1 options {search mode:grep, starting at top:true}
  replace "'" using "" searching in selection of text 1 of text document 1 options {search mode:grep, starting at top:true}
  replace "é" using "e" searching in selection of text 1 of text document 1 options {search mode:grep, starting at top:true}
  replace "ú" using "u" searching in selection of text 1 of text document 1 options {search mode:grep, starting at top:true}
  replace "\\n" using "," searching in selection of text 1 of text document 1 options {starting at top:true, case sensitive:true}
  replace " " using "" searching in selection of text 1 of text document 1 options {starting at top:true, case sensitive:true}
end tell
```

其次，我可以在 JXA 脚本中使用 `doShellScript` 来调用此脚本以执行替换：

```javascript
app = Application.currentApplication();
app.includeStandardAdditions = true;
result = app.doShellScript("osascript /users/scripts/removecaret.scpt")
```

第三，我可以使用一个 JavaScript 函数来替换文本。这虽然行得通，但 BBEdit 一直是我使用 grep 时的首选：

```javascript
app = Application.currentApplication();
app.includeStandardAdditions = true;
se = Application('System Events')
bb = Application('BBEdit')
bodyText = bb.documents[0].text()
changedText = grepFindAndReplace(bodyText, 'Read.+\n', '')

function grepFindAndReplace(inputString, searchPattern, replaceWith) {
  const regex = new RegExp(searchPattern, 'g');
  const outputString = inputString.replace(regex, replaceWith);
  return outputString;
}

bb.documents[0].text = changedText
```

我的答案是第三点。因为 BBEdit Applescript 将其处理的各种文本组识别为 JavaScript 可以很好地处理的结构化文本类型，从而能够读取、处理并写入到多个可能的位置。

正则表达式是用于匹配字符串中字符组合的模式。在 JavaScript 中，正则表达式也是对象。这些模式用于 `RegExp` 的 `exec()` 和 `test()` 方法，以及 `String` 的 `match()`、`matchAll()`、`replace()`、`replaceAll()`、`search()` 和 `split()` 方法。

# 在 JXA 中使用 JavaScript 正则实现的威力

JavaScript for Automation (JXA)将 JavaScript 强大且多功能的特性引入了 macOS 任务的自动化中。在其许多强大的功能中，JavaScript 的正则表达式（regex）实现是文本处理和操作中一个特别有力的工具。在 JXA 中利用 JavaScript 的正则能力可以显著增强你自动化复杂工作流的能力。具体方法如下：

## 高效的文本解析与匹配

正则表达式提供了一种简洁且强大的手段来搜索、匹配和操作文本。通过 JXA 中的 JavaScript 正则实现，你可以快速识别字符串中的模式、提取特定数据并用最少的代码转换文本。这对于处理日志文件、从结构化文本中提取数据或验证输入格式等任务特别有用。

## 高级字符串操作

JavaScript 的正则函数（如 `match()`、`replace()`、`search()` 和 `split()`）能够实现复杂的字符串操作。例如，你可以：

- 从文本块中提取电子邮件地址。
- 将电话号码格式化为统一样式。
- 根据复杂的分隔符将文本拆分为数组。
- 查找并替换模式，例如纠正拼写错误或更新文件内容的路径。

## 动态且灵活的自动化

JavaScript 中的正则表达式高度动态，可以在运行时构建或修改。这允许创建灵活的自动化脚本以适应不同的输入格式或不断变化的需求。通过编程构建正则模式，你的 JXA 脚本可以处理更广泛的任务，而无需不断更新。

## 与 macOS 应用程序集成

JXA 与 macOS 应用程序和系统组件交互的能力意味着你可以直接在自动化工作流中使用正则驱动的文本操作。例如，你可以：

- 根据正则匹配在 Mail 中自动过滤电子邮件。
- 处理并重新格式 Numbers 或 Excel 表格中的数据。
- 从 Safari 中的网页或文档中提取并转换内容。

## 无缝错误处理与验证

正则表达式在验证输入和确保数据完整性方面非常出色。在 JXA 中，你可以使用正则在进一步处理数据之前强制模式（如有效的电子邮件格式或 URL 结构）。这减少了错误并确保你的自动化脚本一致且正确地处理数据。

## 实用示例：

这是一个简单的 JXA 脚本，使用正则从给定文本中提取所有电子邮件地址：

```javascript
function extractEmails(text) {
  // 定义匹配电子邮件地址的正则模式
  var emailPattern = /\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,7}\b/g;
  // 使用 match() 找到所有匹配项
  var matches = text.match(emailPattern);
  // 返回电子邮件地址数组
  return matches || [];
}

// 示例
var sampleText = "Please contact us at support@example.com or sales@example.org for more information.";
var emails = extractEmails(sampleText);
console.log(emails); // 输出: ["support@example.com", "sales@example.org"]
```

在 JXA 中利用 JavaScript 的正则实现使你能够创建极高效、灵活且强大的自动化脚本。无论你是处理文本文件、爬取网页内容还是验证输入数据，正则都提供了所需的工具来轻松处理复杂的文本操作任务。通过将这些能力集成到你的 JXA 工作流中，你可以简化 macOS 自动化流程，并开启生产力和精确度的新境界。

# 快捷指令

# 生成 QR 代码

1. **从共享表接收更多输入**：此操作被设置为接收来自共享表的输入。如果没有提供输入，它将继续执行下一个操作。这可能是快捷指令接收要转换为 QR 代码 URL 的起点。
2. **从快捷指令输入获取 URL**：此操作从快捷指令接收的输入中提取 URL。如果用户选择了包含 URL 的文本或文件并分享到快捷指令，此操作可确保仅取 URL 作为下一步的输入。

3. **从 URL 生成 QR 代码**：此操作获取上一步提取的 URL 并生成对应的 QR 代码图像。这是快捷指令的核心功能。
4. **将 QR 代码保存到最近**：最后，此操作将生成的 QR 代码图像保存到用户照片应用中的“最近”专辑中。

### 快捷指令描述：

此快捷指令旨在通过共享表接收用户的 URL 并将其转换为 QR 代码。然后，该 QR 代码会被保存到照片应用的“最近”相册中方便访问。这个快捷指令可以以视觉化格式共享 URL，这种格式可以被手机或其他带有相机和 QR 代码扫描功能的设备扫描。这是一种无需专用应用即可生成 QR 代码的简单高效的方法。

# 选择照片提取文本到备忘录

1. **请求文本**：快捷指令提示用户输入文本作为笔记的名称。给用户的提示信息是“Make a name for note”（为笔记命名）。
2. **创建笔记**：快捷指令在名为“Biz”的文件夹或账户中，使用提供的输入（上一步输入的名称）创建一个新笔记。
3. **选择照片**：提示用户选择照片。
4. **从照片中提取文本**：快捷指令使用 OCR（光学字符识别）技术从选定照片中提取文本。
5. **追加**：将提取的文本追加到之前创建的笔记中。

### 快捷指令描述：

此快捷指令旨在从一个或多个选定的照片中提取文本并将文本保存到笔记中。用户首先为笔记命名，然后选择照片。文本将从这些图像中识别并编译到“Biz”文件夹或账户内新建的笔记中。这对于快速将物理文档或图像中的文本捕获并整理成数字格式，以便日后访问和参考非常有用。

# 创建带有更改问题的测验

图片概述了一个名为“Monarchy Quiz”的 macOS 快捷指令。该快捷指令似乎是一个简单的测验应用程序，询问关于君主（特别是爱德华一世）的问题并显示答案。

以下是该快捷指令工作原理的逐步说明：

1. 快捷指令包含一个格式化的 JSON 数组文本块，数组中的每个对象包含一个类别（“Edward I”）、一个子类别（如“Biography”或“Reign”）、一个问题和一个答案。
2. 随后，快捷指令从此 JSON 格式的文本中提取出一个字典。
3. 它进入一个重复循环，遍历字典中的每个项目。
4. 对于每个项目（每对问题和回答对），它会从当前重复项中获取键 `'category'` 的值（尽管这一步在后续操作中似乎没有进一步的用途）。
5. 然后，它从重复项中获取键 `'question'` 的值。
6. 随后，通过 `'Show alert'` 动作向用户显示问题。
7. 之后，它从重复项中获取键 `'answer'` 的值。
8. 该答案也会通过 `'Show alert'` 动作显示给用户。
9. 在处理字典中的所有项目后，循环结束。

如何使用该快捷指令：
- 运行“Monarchy Quiz”快捷指令。
- 阅读弹窗中显示的问题并思考你的答案。
- 关闭问题弹窗，在下一个弹窗中查看正确答案。
- 对测验中的每个问题重复此过程，直到所有问题都回答完毕。

此快捷指令是一种向用户展示一系列问题和答案的简单方法，可能用于教育或娱乐目的。

# 使用 AI 创建播放列表图像

Apple Music 最近的一次更新包含了一个意想不到的惊喜。过去，当创建一个新的播放列表时，使用前四张专辑的封面图来创建播放列表的“封面”。用户可以通过包含所需封面的四首歌曲放在列表开头来控制所使用的封面图。但这次更新完全取消了这个功能，并提供了一些特别难看的预制图像作为选择，除非选择从文件或照片库中添加图像。在创建新播放列表后这样做非常麻烦，因此我使用了快捷指令通过两种方式来简化它。首先是使用 OpenArt.ai 网站创建图像。

用法：

# 使用 OpenArt.ai 创建播放列表图像

图片显示了一个名为“Use AI To Get Playlist Art”的 macOS 快捷指令。该快捷指令旨在帮助你为特定风格的音乐播放列表创建艺术。其工作原理如下：

1. 快捷指令开始，如果没有来自共享表的直接输入，则继续接收输入。
2. 使用 `Dictionary` 动作定义一个样式列表，可以通过选择这些样式来确定你想创建的艺术类型。提供的选项包括用于漫画风格的“Comic”、“新艺术（Art Nouveau）”、“哥特（Gothic）”、“Picasso（毕加索，可能是指代更抽象的风格）”、“California”、“Sixties（六十年代）”和“Movie”。你也可以向此字典中添加更多样式。
3. `'Choose from Dictionary'` 动作允许你选择这些样式中的一种。
4. 随后，快捷指令会提示输入文本，可能是为了接收关于艺术更具体的细节或偏好。
5. 从字典中选定的项目（所选样式）和提供的输入文本合并成单个文本块。
6. 该文本块被复制到剪贴板。
7. 创建一个指向 `https://www.openart.ai/create` 的 URL。
8. 快捷指令打开此 URL，包含样式和任何额外输入的合并文本块可以在此处使用 AI 生成播放列表封面。

如何使用该快捷指令：
- 运行快捷指令并从预定义列表中选择样式。
- 在提示时输入任何额外细节。
- 快捷指令将合并后的文本复制到你的剪贴板，并导航到 openart.ai 网站，你可以在那里使用复制的文本指示 AI 生成所选风格的播放列表封面。

# 使用 Google 查找播放列表图像

其次，使用 Google 搜索适合作为播放列表封面的图像。在播放列表界面，点击三个点获取共享表。选择快捷指令名称。如果正在播放歌曲，快捷指令将立即使用 `Current Song` 的 `Album name`、`Song Title` 和 `Artist` 作为搜索词，否则它将提供音频输入以语音提供搜索词。

以下是所示每个步骤的分解和描述：

1. 快捷指令开始从共享表接收图像和其他输入。如果没有输入，它将继续。
2. 它从 Apple Music 获取 `'Current Song'` 详情。
3. 使用 `'Current Song'` 的详情获取 `'Album'`、`'Artist'`、`'Lyrics'` 和 `'Title'`。
4. `'If'` 条件检查歌曲的 `'Title'` 是否有效。
   - 如果 `'Title'` 有值，构建一个文本命令来寻找与歌曲的 `'Artist'`、`'Album'` 和 `'Title'` 相关的图像。
   - 然后对文本进行 URL 编码，并将此 URL 编码文本保存到名为 `'Choice'` 的变量。
5. 如果 `'Title'` 没有值，快捷指令允许你口述文本，然后进行 URL 编码并保存到 `'Choice'` 变量中。
6. `'If'` 条件结束后，快捷指令使用 `'Choice'` 变量构建 Google 搜索 URL，以寻找与输入或口述信息相关的图像。
7. 最后，打开构建的 URL。

要使用此快捷指令，你可以在 Apple Music 中选择一首歌，将其共享到此快捷指令，然后它将帮助你在线寻找相关图像，可能用于创建播放列表封面或类似的目的。

```
