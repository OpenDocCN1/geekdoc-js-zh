# Microsoft Windows 管理员高级 VBScript 高级指南








































# 致谢

我衷心感谢杰弗里，他无疑是任何作者所能期盼的最佳合著者之一。撰写一本书籍可能极其耗费心力且耗时，而一位优秀的合著者确实能大大缓解这种压力。同时，我也要感谢 SAPIEN Technologies 的所有成员：乔纳森、亚历克斯和费迪南德，他们为书籍主要目的之外的工具和技术提供了协助，使整个过程顺利了许多。最后，要向 ScriptingAnswers.com 的所有用户致以热烈的感谢，正是他们对脚本社区的执着与坚定支持，成为推动本书面世的主要动力。

唐·琼斯
内华达州拉斯维加斯

撰写你的第一本书可能是一项艰巨且有时令人畏惧的任务。幸运的是，我有一位出色的写作伙伴。感谢你，唐，在出版这个陌生的新世界里成为如此出色的向导。同时也要感谢 Visory Group 的同事。我真心感激你们给予我的灵活性，让我能够承担像这样的项目。最后，我要特别感谢贝丝、卢卡斯和埃莉。没有我新家庭的爱、支持和理解（“爸爸今晚又要工作吗？”），我绝不可能走到今天。你们是我如此努力工作的理由。

杰弗里·希克斯
纽约州锡拉丘兹

# 引言

在撰写我的第一本脚本著作《*使用 VBScript 和 WMI 管理 Windows*》（Addison-Wesley，2004）时，我旨在开创当时的行业先例：这本书并非为开发者设计，而是专门为 Microsoft Windows 管理员量身打造，这些管理员几乎没有 VBScript 经验，只希望学习足够有效的 VBScript 知识。自该书出版以来，Windows 管理员对 Windows Script Host、VBScript、Windows Management Instrumentation 及其他相关技术的掌握日益娴熟。由于参加会议和访问我网站（*http://www.ScriptingAnswers.com*）的管理员开始提出关于更复杂技术和技巧的问题，现在是时候编写一本涵盖高级主题的书籍了。

在本书中，我出色的合著者杰弗里·希克斯和我尝试涵盖一些我们日常使用的更高级的脚本技巧。我们当然并非假装触及每一个可能被视为“高级”的主题；毕竟，脚本与 Microsoft Windows 本身一样多样且复杂。相反，我们尝试涵盖最有用的高级技术，认识到我们的管理员同行通常像我们一样务实和注重实践。我们也尝试以与我们学习这些技术非常相似的方式来涵盖它们，提供完整的解决方案和逐行解析，以便您不仅能看到最终成果，还能详细了解其工作原理及原因。

个人而言，我很高兴 Windows 现在是一个如此成熟、稳定的产品，使我们有时间和工具通过脚本探索自动化。我也很高兴更多的管理员正在攻克高级主题，这告诉我 Windows 已真正成为企业操作系统，具备了通常与传统企业级操作系统（如 UNIX）相关的复杂性和可脚本化程度。

杰弗里和我都感激您选择本书以进一步深入您的脚本学习。我们当然希望您觉得它有用！尽管如此，我们想简要提醒一句：这确实是一本高级书籍。我们不会花时间解释基本的脚本概念，并假设您已经具备中到高级的脚本技能。我们确实在书的开头涵盖了一些基础知识，但只是为了快速复习您可能不常用到的技巧。

在澄清了这一点后，我祝愿您在脚本编写的努力中一切顺利！

唐·琼斯

## 本书适用对象

本书适用于希望将脚本技能提升到更高水平的 Microsoft Windows 管理员。我们假设读者已具备中级到高级的脚本技能，并正在寻找新的技巧和思路来扩展他们的脚本工具箱。本书也适用于希望将其脚本应用范围扩展到 Microsoft Exchange 2003 和 Microsoft Virtual Server 2005 等产品的脚本管理员。如果您以前从未使用过 VBScript，那么本书绝对不适合您。我们不会在基础知识上花费太多时间，而理解本书内容确实需要这些基础。如果您想要一本更入门级别的书籍，可以考虑唐·琼斯的《*使用 VBScript 和 WMI 管理 Windows*》（Addison-Wesley，2004）或类似书目。

## 本书约定

本书结构相对清晰，没有需要读者特别留意的复杂约定。然而，全书使用了以下读者提示来指出有用信息：

| 读者提示 | 含义 |
| --- | --- |
| 提示 | 提供关于特定任务或功能的有用的内部信息 |
| 注意 | 提醒您补充信息 |
| 警告 | 包含关于可能数据丢失、安全漏洞或其他严重问题的重要信息 |
| 随书光盘 | 标识随书附带光盘中可用的工具或附加信息 |
| 最佳实践 | 标识被公认为行业标准的技术或约定；虽然不遵循这些做法不会导致问题，但遵循它们可以使事情更轻松、更高效。 |

## 系统要求

要使用《面向 Microsoft Windows 管理员的高级 VBScript》随书光盘，您需要配备以下配置的计算机：

- Pentium II（或同等级别）处理器，主频 266 兆赫 (MHz) 或更高。
- CD-ROM 或 DVD-ROM 驱动器。
- Microsoft 鼠标或兼容的指点设备。
- Microsoft Windows Server 2003、Microsoft Windows 2000 或 Microsoft Windows XP。我们假设您已安装最新的服务包，尽管在大多数情况下我们不会涵盖特定于某个服务包的信息（如果涉及，我们会注明）。
- Windows Script Host (WSH) 5.6 版或更高版本。WSH 是 Windows 2000 及更高版本的核心组件，因此除非您采取特殊步骤移除了此软件，否则它应该已经安装。
- 部分脚本——特别是涉及 Microsoft Exchange Server 2003、Microsoft Virtual Server 2005 或 Microsoft Operations Manager 2005 的脚本——需要额外的相应 Microsoft 产品。
- Microsoft Internet Explorer 5.5 或更高版本。
- Adobe Acrobat 或 Acrobat Reader。

## 关于随书光盘

为了为您提供快速、便捷的访问本书所需工具的途径，我们已在随书光盘中包含以下内容：

- 书中介绍的脚本。
- 我们提及的、因过长而不便输入的任何 URL 的链接。
- 一些额外工具（或指向它们的链接）。

请花些时间探索光盘及其包含的所有内容。如果您希望深入探讨本书主题之外的脚本技术，我们邀请您访问唐的网站 http://www.ScriptingAnswers.com。您将找到额外的脚本示例、培训、问答讨论论坛以及更多资源，所有这些都专为 Windows 管理脚本而设计。

## 本书支持

我们已尽一切努力确保本书内容及随书光盘的准确性。Microsoft Press 在以下网站提供其书籍和随书光盘的一般支持信息：

http://www.microsoft.com/learning/support/books

要使用本书的 ISBN 搜索本书和光盘的更正信息，请访问：

http://www.microsoft.com/mspress/support/search.asp

如果您对本书或随书光盘有任何评论、问题或想法，请通过以下任一方式发送给 Microsoft Press：

电子邮件：mspinput@microsoft.com

邮寄地址：
Microsoft Press
收件人：《面向 Microsoft Windows 管理员的高级 VBScript》项目编辑
One Microsoft Way
Redmond, WA 98052

请注意，Microsoft 软件产品支持不通过上述地址提供。



欢迎通过 http://www.ScriptingAnswers.com 联系作者，就本书附带光盘中的脚本提出问题或讨论可能遇到的困难。

# 第一部分
高级 Windows 脚本基础

本部分内容：
- 第 1 章：入门 ..................3
- 第 2 章：脚本安全 .................41

第 1 章

## 入门

**本章内容：**
- 前置知识 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
- 高级脚本目标 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
- 我们不会涵盖的内容 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 36
- 选择合适的工具 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 38
- 脚本技术 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 39
- 小结 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 39

在开始之前，让我们花几分钟回顾一些脚本基础知识。如果没有扎实的 VBScript、Active Directory 服务接口 (ADSI) 和 Windows 管理规范 (WMI) 基础，本书中的许多主题可能会让您感到困惑。我们将介绍在继续学习之前您应该理解的一些脚本基本原理。

任何值得进行的旅程都需要一点准备。在本书中，我们将涵盖大量内容。本章将帮助您做好准备。我们将介绍一些您需要已经熟悉的知识，以便从材料中获得最大收益。我们还将花一些时间复习一些脚本基础知识。如果您是脚本新手，本概述应能帮助您理清思路。

### 前置知识

要充分利用本书，您必须具备脚本技术、术语和经验。熟悉 WshShell 对象和 Microsoft Windows 脚本宿主 (WSH) 中的错误处理将使您的学习过程轻松许多。我们包含了一个快速回顾，但如果其中一些内容对您来说是新的，我们建议浏览 Microsoft TechNet 脚本中心的脚本，并阅读 Microsoft Windows 2000 脚本指南（Microsoft Press）或使用 VBScript 和 WMI 管理 Windows（Addison-Wesley）。至少，您应该从 Microsoft 网站 http://www.microsoft.com/downloads/details.aspx?familyid=01592C48-207D-4BE1-8A76-1C4099D7BBB9&displaylang=en 下载并阅读 Windows 脚本宿主 5.6 文档。

> **光盘说明** 此链接（以及本书中引用的大多数链接）都包含在随附光盘中。请点击 Windows 脚本 5.6 文档。

第一部分：高级 Windows 脚本基础

### 了解 Windows 脚本宿主基础

我们假设您已安装 Microsoft Windows 脚本宿主 5.6。如果不确定，请打开命令提示符并输入 `cscript //logo //?`。您应该会看到类似这样的内容。

```
Microsoft (R) Windows Script Host Version 5.6
Copyright (C) Microsoft Corporation 1996-2001. All rights reserved.

Usage: CScript scriptname.extension [option...] [arguments...]

Options:
//B         Batch mode: Suppresses script errors and prompts from displaying
//D         Enable Active Debugging
//E:engine  Use engine for executing script
//H:CScript Changes the default script host to CScript.exe
//H:WScript Changes the default script host to WScript.exe (default)
//I         Interactive mode (default, opposite of //B)
//Job:xxxx  Execute a WSF job
//Logo      Display logo (default)
//Nologo    Prevent logo display: No banner will be shown at execution time
//S         Save current command line options for this user
//T:nn      Time out in seconds: Maximum time a script is permitted to run
//X         Execute script in debugger
//U         Use Unicode for redirected I/O from the console
```

在接下来的几节中，我们将介绍一些关键的 WSH 元素，这些元素将在本书的脚本中反复出现。

> **注意** 本书中的许多脚本和示例都需要管理员权限，无论是在本地还是远程系统上。我们假设您将以本地或域管理员身份运行任何脚本。在适当的情况下，我们将指出如何以及在何处使用备用凭据。

#### WshShell

*WshShell* 对象为脚本管理员提供了大量功能。您可以使用它通过弹出窗口向用户发送消息、读写注册表、启动其他程序等。让我们快速了解一下这个对象。

##### Popup

*Popup* 方法向用户显示图形消息，包含按钮和图标。使用 *Popup* 方法而不是类似的 *MsgBox* 函数（本章稍后讨论）的一个优点是，您可以配置弹出窗口在指定秒数后自动关闭。当您想向用户显示信息但又不想依赖用户单击确定时，这是理想的选择。清单 1-1 展示了 *Popup* 方法的使用示例。

###### 清单 1-1 WshShell Popup 示例

```vbscript
dim wshShell
set wshShell=CreateObject("wscript.shell")
'title for popup window
strTitle="welcome"

'compose popup message text
strMsg="Thank you for logging in." & vbCrLf
strMsg=strMsg & "It is now " & Now & vbCrLf
strMsg=strMsg & "Have a nice day."

'set time to -1 to never dismiss popup window
wshShell.Popup strMsg,7,strTitle,vbOKOnly+vbInformation
```

> 光盘说明 您可以在本书附带的光盘上找到此脚本以及本章列出的其他脚本。

请注意，我们在弹出参数中使用了一些内置常量，*vbOkOnly* 和 *vbInformation*。这些常量分别显示确定按钮和信息图标。这些相同的常量也用于 *MsgBox* 函数。您可以在 Windows 脚本宿主 5.6 文档中找到有关它们的更多信息。

##### 注册表读取

*WshShell* 对象通常用于读取本地注册表。要读取或操作远程注册表，必须使用 Windows 管理规范 (WMI)。假设执行脚本的用户具有适当的权限，您可以轻松地从注册表读取和写入信息。以下是从本地注册表读取所有者和产品信息的快速示例。

```vbscript
dim objShell
Set objShell=CreateObject("wscript.shell")
strRegisteredUser=objShell.RegRead("HKLM\Software\Microsoft\" & _
    "windows NT\CurrentVersion\RegisteredOwner")
strProduct=objShell.RegRead("HKLM\Software\Microsoft\windows NT\" & _
    "CurrentVersion\ProductName")
WScript.Echo strRegisteredUser & " is running " & strProduct
```

##### 程序启动

您经常需要从主管理脚本中调用另一个脚本或程序。幸运的是，*WshShell* 对象使这成为可能，如清单 1-2 所示。

###### 清单 1-2 WshShell Run 示例

```vbscript
dim objShell
'window style
Const WINDOWHIDDEN=0
Const WINDOWNORMAL=1
Const WINDOWMINIMIZE=2
Const WINDOWMAXIMIZE=3

Set objShell=CreateObject("wscript.shell")

'enter in full path to command or script if not in %Systemroot%
strCommand="Notepad"

objShell.Run strCommand,1,True
'this line won't echo until previous command finishes
wScript.Echo "Script complete"
```

在清单 1-2 中，重要参数是窗口样式和命令是否应在继续执行脚本之前等待。在此示例中，我们为典型的窗口样式设置了常量。（同样，请参阅 Windows 脚本宿主 5.6 文档以了解其他窗口样式。）您可能希望运行程序或脚本并将其对用户隐藏。根据程序或脚本的不同，您可以通过将窗口类型参数设置为 0 来实现。

如果您希望主脚本中的执行等待命令完成，请将 *WaitOnReturn* 变量设置为 TRUE。在清单 1-2 中，显示 *Script Complete* 的代码行将不会执行，直到 *WshShell* 对象启动的命令完成。

另一种执行命令的方法是使用 *Exec* 方法。此技术对于解析命令行工具或实用程序的输出特别有用。通常，您可能会发现自己正在开发一个脚本，该脚本可以使用另一个命令的输出作为报告或参数。清单 1-3 获取 *Dir* 命令的输出（该命令显示所有可执行文件），并对其进行修改，使其仅显示目录名称和文件信息。您必须使用 CScript 从命令提示符运行此脚本。

###### 清单 1-3 WshShell Exec 示例：Dir

```vbscript
Dim objShell,objExec
Set objShell=CreateObject("wscript.shell")
'command to Execute
strCommand="cmd /c DIR c:\*.exe /s"
'text to look for in the output
strFind=".exe"

'create Exec object
Set objExec=objShell.Exec(strCommand)

'parse output and only display lines with
'target text
Do while objExec.StdOut.AtEndOfStream<>True
  strLine=objExec.StdOut.ReadLine
  'parse out lines
  If InStr(strLine,"Directory") Then
    wScript.Echo Trim(strLine)
  ElseIf InStr(strLine,strFind) Then
    wScript.Echo vbTab & strLine
  End If
Loop
```



## 第一章：入门

在运行时，脚本将指定的命令传递给 *WshShell* 对象并执行它。该命令的输出随后被重定向到一个新对象，在我们的脚本中称为 *objExec*。利用这个对象，我们可以借助 *StdOut* 的强大功能，操作那些通常会写入命令提示符窗口的数据。只要命令还在运行，*AtEndOfStream* 属性将为 FALSE。由于我们想从通常很长的输出中显示特定信息，我们将一个变量 *strLine* 设置为 *StdOut* 下一行的值。然后我们可以使用 *InStr* 函数来查找感兴趣的字符串。如果有匹配项，就显示该行。在代码清单 1-3 中，我们希望显示目录名称以及包含文件名的每一行。

> **提示**  使用 *StdOut*，你可以使用 *FileSystemObject* 库中的任何文本流属性，例如 *ReadLine*、*SkipLine* 和 *AtEndOfStream*。

```
代码清单 1-4 WshShell Exec 示例：Nslookup
Dim objShell,objExec
Set objShell=CreateObject("wscript.shell")
'要执行的命令
strCommand="Nslookup www.microsoft.com"

'创建 Exec 对象
Set objExec=objShell.Exec(strCommand)

'跳过包含关于我们 DNS 服务器信息的行
objExec.StdOut.SkipLine
objExec.StdOut.SkipLine

Do While objExec.Stdout.AtEndOfStream<>True
    strLine=objExec.Stdout.ReadLine
    WScript.Echo strLine
Loop
wScript.Quit
```

代码清单 1-4 演示了使用 *Exec* 方法的另一种方式：执行 *Nslookup* 命令。我们的脚本解析出感兴趣的行，即指定名称的 IP 地址，并将其清晰地显示出来。该脚本只是跳过任何 *Nslookup* 输出的前两行，这两行通常包含 DNS 服务器名称和 IP 地址。

> **提示**  虽然不是绝对要求，但你会发现通过命令行使用 CScript 运行利用 *StdOut* 和 *StdIn* 的脚本会更简单、更整洁。例如，如果你通过双击来运行代码清单 1-4 中的脚本，你会看到几个空白的弹出窗口。如果你通过命令行使用 CScript 运行脚本，你会得到更整洁的结果。

# 第一部分：高级 Windows 脚本基础

## WshNetwork

WshNetwork 对象为当前用户暴露了一些基本的网络信息，例如用户名或计算机名。此对象也可用于管理打印机和驱动器映射。让我们通过将其融入代码清单 1-1 的脚本中，快速了解一下此对象的功能。

```
代码清单 1-5 WshNetwork 示例
dim objShell,objNetwork,colDrives
set objShell=CreateObject("wscript.shell")
Set objNetwork=CreateObject("WScript.Network")
'弹出窗口标题
strTitle="Welcome"

'枚举映射的驱动器
strMappedDrives=EnumNetwork()

'枚举映射的打印机
strMappedPrint=EnumPrint()

'组成弹出消息文本
strMsg=objNetwork.UserName & ", thank you for logging in to " &_
objNetwork.ComputerName & vbCrLf & vbcrlf
strMsg=strMsg & strMappedDrives & vbCrLf & vbCrLf
strMsg=strMsg & strMappedPrint & vbCrLf & vbCrLf
strMsg=strMsg & "It is now " & Now & vbCrLf
strMsg=strMsg & "Have a nice day."

'将时间设置为 -1 以永不关闭弹出窗口
objShell.Popup strMsg,10,strTitle,vbOKOnly+vbInformation
wScript.quit

Function EnumNetwork()
On Error Resume Next
    Set colDrives = objNetwork.EnumNetworkDrives

    '如果没有枚举出网络驱动器，则通知用户，否则显示
    '枚举出的驱动器
    If colDrives.Count = 0 Then
        ret="There are no network drives to enumerate."
    Else
        ret = "Current network drive connections: " & vbCrLf
        For i = 0 To colDrives.Count - 1 Step 2
            ret = ret & vbCrLf & colDrives(i) & vbTab & colDrives(i + 1)
        Next
    End If
    EnumNetwork=ret
End Function

Function EnumPrint()
On Error Resume Next
    Set colPrint = objNetwork.EnumPrinterConnections
```

'如果没有枚举出网络打印机，则通知用户，否则显示
'枚举出的打印机
If colPrint.Count = 0 Then
    ret="There are no printers to enumerate."
Else
    ret = "Current Printer connections: " & vbCrLf
    For i = 0 To colPrint.Count - 1 Step 2
        ret = ret & vbCrLf & colPrint(i) & vbTab & colPrint(i + 1)
    Next
End If
EnumPrint=ret
End Function
```

在代码清单 1-5 中，我们自定义了消息以显示用户名、用户登录的计算机以及任何映射的驱动器或打印机。我们还在脚本中创建了一个名为 *objNetwork* 的对象，它是 *WshNetwork* 对象的一个实例。借助 *objNetwork* 对象，我们可以通过调用 *EnumNetwork* 和 *EnumPrint* 函数来构建映射驱动器和打印机的列表。这些函数分别使用 *EnumNetworkDrives* 和 *EnumPrinterConnections* 方法来创建映射网络驱动器和打印机的集合，如下所示。

```
For i = 0 To colPrint.Count - 1 Step 2
    ret = ret & vbCrLf & colPrint(i) & vbTab & colPrint(i + 1)
Next
```

然后该函数遍历该集合并列出映射的网络资源。

回到脚本的主体部分，我们组成消息。我们通过调用 *username* 和 *computername* 属性来个性化消息，如下所示。

```
strMsg=objNetwork.UserName & ", thank you for logging in to " & _
objNetwork.ComputerName & vbCrLf & vbCrLf
```

我们的显示消息唯一增加的其他信息是关于映射驱动器和打印机的信息。用户现在可以看到一条个性化的消息，显示他或她所有的映射驱动器和打印机。消息显示 10 秒后关闭。我们增加了超时值，因为现在比代码清单 1-1 示例中有更多内容需要阅读。

> **注意**  用户名属性是用户的 NT4 风格或 *sAMAccountName* 属性，例如 *jhicks* 或 *donj*。如果你想从 Active Directory 获取用户的全名或显示名称，你必须添加代码，根据 *sAMAccountName* 属性搜索该帐户。

## 错误处理

任何管理脚本都应该具有一定级别的错误处理。即使你开发的脚本只有你自己使用，错误处理也能使它们更容易开发、调试和部署。你当然不需要检查每一个可能发生错误的地方，但你应该识别出那些错误或故障会对你的脚本产生重大负面影响的代码段。例如，如果你正在使用 *FileSystemObject* 创建日志文件，并尝试写入一个用户没有适当权限的驱动器，那么该代码将会失败。最好的方法是提前捕获这类错误，并向用户提供一些有意义的反馈，如代码清单 1-6 所示。

> **注意** 我们讨论的错误处理是 VBScript 特有的。运行我们脚本的引擎 Windows Script Host 是语言无关的。我们本可以用 JScript 编写脚本，并以适合该脚本语言的方式处理错误。

```
代码清单 1-6 错误处理示例：Err
Dim objFSO,objTS
On Error Resume Next
Set objFSO=CreateObject("Scripting.FileSystemObject")
Err.clear
Set objTS=objFSO.CreateTextFile("R:\Logs\auditlog.txt")
If Err.Number<>0 Then
    strMsg="There was an error creating the log file" & vbCrLf
    strMsg=strMsg & "Error #" & Err.Number & " " & Err.Description
    WScript.Echo strMsg
    WScript.Quit
End If
'脚本从这里继续执行
```

在代码清单 1-6 中，我们尝试创建一个日志文件。如果此尝试失败，则没有理由继续执行脚本。在尝试捕获错误信息之前，我们使用了 *Err.Clear* 语句。在像这样简短的脚本中可能没有必要，但在更长、更复杂的脚本中，调用 *Err.Clear* 会清除之前在脚本中发生并被忽略的任何错误。例如，你可能正在根据存储在文本文件中的新用户信息在 Active Directory 中创建用户对象。如果你想填充的用户属性之一是 *telephonenumber*，但并非每个新用户都有此属性，你希望脚本无论如何都能继续执行（因此脚本开头有 *On Error Resume Next*）。但是，当你在脚本中尝试设置此属性时，仍然会引发错误。如果你不调用 *Err.Clear*，下次检查 *Err.Number* 的值时，它可能返回的是上一个错误的值。在代码清单 1-6 中，这是一个极不可能发生的事件——尽管如此，我们希望非常清楚地说明如何以及何时使用 *Err.Clear*。

实际的错误检查是在查看 *Err.Number* 的值。值为 0 表示成功。任何非 0 的值都表示上一个命令存在某种失败或错误。根据脚本试图完成的任务，你可能会获得或多或少的错误信息。至少，我们建议以某种错误消息的形式向用户显示 *Err.Number* 和 *Err.Description* 信息。请记住，并非每个错误都有相应的描述。根据你的脚本的性质和 *Err.Number* 的值，你可能会添加更复杂的错误处理。首先，故意引发用户可能导致的错误，并记下错误编号和描述。然后使用



## *Select Case* 语句

*Select Case* 语句可以采取更复杂的步骤，或根据错误提供更详细的信息，如下所示。

```
Select Case Err.Number
    Case 76
        WScript.Echo "Verify that path is available"
    Case 71
        WScript.Echo "You seem to be attempting to access a drive" & _
        " that isn't ready, like a CD"
    Case 70
        WScript.Echo "You don't seem to have permission to write to" & _
        " that file."
    Case Else
        WScript.echo "Error #" & Err.Number & " " & Err.Description
End Select
```

当然，错误处理不仅仅是 *Err* 对象。你可能在脚本中包含的一些对象拥有自己的错误避免或检测机制。例如，*FileSystemObject* 包含了 *FolderExists*、*DriveExists* 和 *FileExists* 方法。如果目标项存在，这些方法会返回 TRUE，这意味着你可以编写如清单 1-7 所示的代码。

```
清单 1-7 错误处理示例：*FileSystemObject*
On Error Resume Next
Dim objFSO,objTS
strFile="R:\logs\audit.log"
Set objFSO=CreateObject("Scripting.FileSystemObject")
If objFSO.FileExists(strFile) then
    Set objTS=objFSO.OpenTextFile(strFile)
Else
    Wscript.echo "Can't find " & strFile
    Wscript.quit
End if
'script continues
```

## *InputBox*

与传统的脚本（如批处理文件）相比，VBScript 的一大优势是能够向执行脚本的用户询问信息或获取输入。这通常通过 *InputBox* 函数完成，如下所示。

```
Dim objFSO, objTS
strTitle="Select Text File"
strFile=InputBox("What file do you want to open?",strTitle,"C:\boot.ini")
'if value of strFile is blank then either nother was entered
'or Cancel was clicked.  In either case we can't continue
If strFile="" Then WScript.Quit
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objTS=objFSO.OpenTextFile(strFile)
'script continues
```

正如这个简短示例所示，脚本使用 *InputBox* 函数向用户询问文件名。尽管唯一必需的参数是解释用户应输入内容的文本，但如果你包含一个标题和一个默认选项，你的脚本将更友好。提供默认选项的好处是用户能更清楚他们应该使用什么格式。

获得输入后，你应该验证它，正如我们在刚才的代码中所做的那样。如果用户单击“取消”或没有输入任何内容，则没有理由继续，因此脚本会静默退出。根据你寻求的信息类型，你可能希望进行进一步的验证，例如检查输入的长度或大小。或者如清单 1-8 所示，你可以验证值本身。

```
清单 1-8 带菜单的 *InputBox* 示例
On Error Resume Next
strTitle="Option Menu"
strMenu="Please select one of the following choices:" & VbCrLf
strMenu=strMenu & "1 - Banana Cream" & VbCrLf
strMenu=strMenu & "2 - Cherry" & VbCrLf
strMenu=strMenu & "3 - Apple Walnut" & VbCrLf
strMenu=strMenu & "4 - Peach"
rc=InputBox(strMenu,strTitle,1)
If rc="" Then WScript.Quit
Select Case rc
    Case "1"
        WScript.Echo "One slice of Banana Cream, coming up!"
    Case "2"
        WScript.Echo "Sorry, we are all out of cherry."
    Case "3"
        WScript.Echo "Do you want ice cream with that?"
    Case "4"
        WScript.Echo "You get the last piece of Peach."
    Case Else
        WScript.Echo Chr(34) & rc & Chr(34) & _
        " is not a valid choice.  Please try again."
        WScript.quit
End Select
'script continues
```

在清单 1-8 中，我们在 *strMenu* 变量中构建了一个文本字符串。该变量作为 *InputBox* 函数的消息参数传递。假设 *InputBox* 返回的值不为空，我们可以使用 *Select Case* 来确定下一步操作。

尽管我们期望用户输入一个数字，但他或她可能会意外地输入一些非数字字符。通过将 *Case* 语句中的选项用引号括起来，我们将值视为字面文本值。这样，我们就能确保 *Case Else* 中的错误处理代码会生效。如果用户输入除 1、2、3 或 4 之外的任何内容，都会显示错误消息。输入 A（这应该是无效的）会返回 Case 1 的代码。你可以从附带的 CD 中复制清单 1-8 的脚本，自己试一试。

唉，除了使用 HTML 应用程序（HTA）（我们将在本书后面介绍）或使用更高级的编程语言（如 Microsoft Visual Basic 2005）开发自己的输入框（这超出了本书的范围）之外，*InputBox* 函数是我们唯一可用的图形输入选项。

## **MsgBox**

与 *InputBox* 函数密切相关的是，*MsgBox* 函数也以图形对话框的形式向用户显示消息。最简单的形式，你只需要编写 *MsgBox* 函数和要显示的文本。

```
MsgBox "welcome to the company!"
```

这一行显示一个消息框，用户必须单击“确定”才能继续。脚本执行会停止，直到消息框被关闭。回想一下，你可以使用 *WshShell.Popup* 方法设置时间间隔来决定消息显示多长时间。你可以通过将超时值设置为 -1，强制弹出窗口的行为类似于消息框，这要求用户单击按钮才能关闭它。

你可以使用 *MsgBox* 函数来显示信息或获取信息，例如用户是否希望继续处理当前任务。*MsgBox* 函数返回一个由所单击按钮决定的值。你可以创建一个提供“确定”、“是”、“否”或“取消”按钮选项的消息框。

> **注意**  还有其他可用的按钮类型，但这些是你在脚本中最可能使用的。有关更多信息，请参阅 Windows Script Host 5.6 文档。

清单 1-9 显示了一个代码片段，你可以用它来让用户控制脚本。

```
清单 1-9 *MsgBox* 是/否 示例
strMsg="The file already exists.  Do you want to overwrite it?"
strTitle="File Confirm"
rc=MsgBox(strMsg,vbYesNo,strTitle)
If rc=vbYes Then
    Script.Echo "Overwriting file"
    'insert code here
Else
    strNewName=InputBox("Enter a new filename.",_
    strTitle,"c:\logs\newlog.txt")
    'insert code here
End If
'script continues
```

一个 *MsgBox* 函数询问用户是否要覆盖文件，并使用常量 *vbYesNo* 来创建“是”和“否”按钮。我们将一个 *rc* 变量设置为根据用户单击的按钮返回 *MsgBox* 的值。然后，我们可以根据返回的值添加代码。但是，如果用户改变主意，想要中止整个脚本呢？看看清单 1-10。

```
清单 1-10 *MsgBox 是/否/取消 示例*
strMsg="The file already exists.  Do you want to overwrite it?"
strTitle="File Confirm"

rc=MsgBox(strMsg,vbYesNoCancel,strTitle)
'take next steps based on value returned by
'MsgBox function
Select Case rc
  Case vbYes
    WScript.Echo "Overwriting file"
    'insert code here
  Case vbNo
    strNewName=InputBox("Enter a new filename.",_
      strTitle,"c:\logs\newlog.txt")
    'insert code here
  Case vbCancel
    WScript.Echo "Aborting the script"
    WScript.Quit
End Select

'script continues
```

在清单 1-10 中，我们使用 *Select Case* 语句来处理 *MsgBox* 的值。*vbYes* 和 *vbNo* 的代码没有改变。我们所做的只是添加了处理 *vbCancel* 的代码。

> **提示**  你也可以在 *WshShell* 弹出窗口中使用 *vbYesNo*、*vbOKOnly* 和 *vbYesNoCancel* 作为按钮选项。返回的值是一个整数，具体取决于单击了哪个按钮，但使用像 *vbYes* 这样的内置常量更容易。如果你不使用常量，你必须找出常量的等效值并在代码中使用，除非你添加大量注释，否则这可能不那么有意义。使用常量，让你的生活更轻松。

*MsgBox* 函数还有一个特性，也适用于 WshShell 弹出窗口——能够在对话框中添加图标。表 1-1 显示了可用的图标。

**表 1-1  *MsgBox 图标常量***

| VBScript 常量 | 整数值 | 显示的图标 |
| :--- | :--- | :--- |
| *vbCritical* | 16 | 关键消息 |
| *vbQuestion* | 32 | 警告查询 |
| *vbExclamation* | 48 | 警告消息 |
| *vbInformation* | 64 | 信息 |

要包含图标，只需将其与相应的按钮类型一起添加，例如 *vbOkOnly+vbInformation*。看看清单 1-11，它是清单 1-10 中脚本的略微修改版，以使用图标。



清单 1-11 带图标的 MsgBox 示例
strMsg="文件已存在。是否要覆盖它？"
strTitle="文件确认"

rc=MsgBox(strMsg,vbYesNoCancel+vbQuestion,strTitle)
'根据 MsgBox 函数返回的值
'采取下一步操作
Select Case rc
    Case vbYes
        MsgBox "正在覆盖文件",vbOKOnly+vbInformation,strTitle
        '在此插入代码
    Case vbNo
        strNewName=InputBox("请输入新文件名。",_
        strTitle,"c:\logs\newlog.txt")
        '在此插入代码
    Case vbCancel
        MsgBox "正在中止脚本",vbOKOnly+vbCritical,strTitle
        WScript.Quit
End Select

'脚本继续执行

现在，我们的消息框不仅更美观一些，而且还向用户提供了视觉上的确认。你可以在 WshShell 弹出窗口中使用这些图标常量，但遗憾的是，不能在 InputBox 中使用它们。

## 使用 FileSystemObject 库

处理文件和目录是脚本编写人员的一项重要基本技能。你需要能够读取可能包含计算机列表的文本文件，以及创建可能用作脚本审计或跟踪日志的文本文件。FileSystemObject 库非常广泛，我们无法在此一一介绍。我们将重点介绍本书中将贯穿使用的一些概念。

你可以按如下方式打开一个文本文件。

```
strFile="c:\boot.ini"
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objTS=objFSO.OpenTextFile(strFile)
```

仅仅两行代码，我们就打开了 C:\boot.ini。在创建了基本的 Scripting.FileSystemObject 之后，我们创建了一个代表文件内容的文本流对象。文件打开并创建文本流对象后，我们就可以逐行读取文件。这是通过使用 Do...While 循环和 AtEndOfStream 属性来实现的。

```
Do while objTS.AtEndOfStream<>True
Loop
```

只要我们没有到达文本文件的末尾，就会继续循环。现在我们需要读取文件的每一行，并可能对其进行一些处理。方便的是，有一个 *ReadLine* 方法。如果我们只是想读取文件并回显每一行，可以使用类似以下的代码。

```
Do while objTS.AtEndOfStream<>True
    wscript.echo objTS.ReadLine
Loop
```

很可能，你会想对包含在该行中的信息做一些处理。我们倾向于设置一个临时变量来保存该行的内容。这样可以更容易地清理、操作或验证文本字符串。

```
Do while objTS.AtEndOfStream<>True
    r=objTS.ReadLine
    if InStr(r,"XP") then strData=ProcessPC(r)
Loop
```

在这个小片段中，我们搜索读取的行中是否包含 *XP*，如果找到，就将 *strData* 设置为脚本中名为 *ProcessPC()* 的函数返回的值。完成后，我们应该调用 *objTS.Close* 来关闭文本文件，做好清理工作。

在结束 *OpenTextFile* 的介绍之前，我们将简要解释打开文件的不同模式。你可以打开一个文件用于只读、写入或追加。只需将模式指定为 *OpenTextFile* 的参数之一。这通常通过在脚本中定义常量来完成，如以下所示。

```
Const FORREADING=1
Const FORWRITING=2
Const FORAPPENDING=8
strFile="c:\\boot.ini"
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objTS=objFSO.OpenTextFile(strFile,FORREADING)
```

如果你以写入模式打开文件，任何现有数据都会被覆盖。如果你以追加模式打开文件，你写入的任何数据都将添加到文件末尾。如果你以只读模式打开文件，则无法对文件进行任何更改。我们通常使用 *OpenTextFile* 来读取或追加数据。如果需要写入新数据，我们会使用 *CreateTextFile* 方法，如下所示。

```
strFile="c:\\logs\\myaudit.log"
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objTS=CreateTextFile(strFile,TRUE)
objTS.WriteLine "审计日志: " & Now
'脚本继续执行
```

通过添加一个 *CreateTextFile* 参数，代码就很简单了。当此参数设置为 TRUE 时，任何具有该名称的现有文件都将被覆盖。如果你不包含 *CreateTextFile* 参数，现有文件将不会被覆盖，并且除非你添加一些错误处理，否则你的脚本将无法继续执行。但在我们创建了文本文件之后，我们使用 *WriteLine* 方法添加任何我们想要的数据。和之前一样，当我们完成时，需要使用 *objTS.Close* 来关闭文件。

*FileSystemObject* 的另一个常见用途是处理文件夹和文件。清单 1-12 展示了其中的一些技术。

```
清单 1-12 FileSystemObject 文件示例
On Error Resume Next
Dim objFSO,objFldr,objFiles,objTS
strTitle="文件演示"

strDir=InputBox("您想要检查哪个文件夹？",_
strTitle,"c:\files")
If strDir="" Then WScript.quit

Set objFSO=CreateObject("Scripting.FileSystemObject")
If objFSO.FolderExists(strDir) Then
  '打开文件夹
  Set objFldr=objFSO.GetFolder(strDir)

  '通过调用 GetFileName 函数
  '获取日志文件信息
  strFile=GetFileName
  If strFile="" Then
    WScript.Quit
  Else
    '调用验证子程序
    validateFile strFile
  End If
Else
  WScript.Echo "找不到 " & strDir
  WScript.Quit
End If

objTS.WriteLine "文件夹报告: " & strDir
'获取此文件夹中的文件
'objFiles 是一个集合
Set objFiles=objFldr.Files

'初始化计数器
i=0
'设置变量以统计文件夹中的文件总数
t=objFiles.Count
'枚举文件集合
For Each file In objFiles
  '获取文件信息并写入日志文件
  objTS.writeLine file.Name & vbTab & file.size & " 字节" & vbTab & _
  file.DateCreated & vbTab & file.DateLastModified
  i=i+1
  iPer=FormatPercent((i/t))
  WScript.Stdout.writeline(iPer& " 完成")
Next

'关闭文件
objTS.Close
MsgBox "请查看 " & strFile & " 获取结果。",vbOKOnly+vbInformation,strTitle

WScript.Quit
'//////////////////////////////////////////////////
Function GetFileName()
On Error Resume Next

GetFileName=InputBox("您想要创建的审计文件名是什么？",strTitle,"c:\filelog.txt")

End Function
'//////////////////////////////////////////////////
Sub ValidateFile(strFile)
On Error Resume Next
'检查日志文件是否存在，如果存在，
'提示用户是否要覆盖。
If objFSO.FileExists(strFile) Then
    rc=MsgBox(strFile & " 已存在。您是否想要" &
    "覆盖它？",vbYesNoCancel+vbQuestion,strTitle)
    Select Case rc
        Case vbYes
            WScript.Echo "正在覆盖文件 " & strFile
            Err.Clear
            '通过覆盖来创建我们的日志文件
            Set objTS=objFSO.CreateTextFile(strFile,True)
            If Err.Number<>0 Then
                strMsg="创建 " &
                strFile & " 时出错" & VbCrLf & "错误号#" & Err.Number &
                " " & Err.Description
                MsgBox strMsg,vbOKOnly+vbCritical,strTitle
                WScript.Quit
            End If
        Case vbNo
            strFile=GetFileName
            ValidateFile strFile
        Case vbCancel
            WScript.Echo "正在中止脚本"
            WScript.Quit
        End Select
    Else
        '创建我们的日志文件
        Err.Clear
        Set objTS=objFSO.CreateTextFile(strFile)
        If Err.Number<>0 Then
            strMsg="创建 " &
            strFile & " 时出错" & VbCrLf & "错误号#" & Err.Number &
            " " & Err.Description
            MsgBox strMsg,vbOKOnly+vbCritical,strTitle
            WScript.Quit
        End If
    End If
End Sub
```

如果你从本章开头一直读到现在，你会注意到清单 1-12 包含了许多前面提出的建议和技巧，还额外加了一点内容，以奖励你读到了本章的这里。

清单 1-12 检查指定文件夹中的所有文件，并创建一个包含特定文件信息的日志。*FileSystemObject* 的这种常见用法适用于任何本地或映射驱动器，以及通用命名约定（UNC）路径。该脚本首先询问用户要检查的文件夹路径。

```
strDir=InputBox("您想要检查哪个文件夹？",_
strTitle,"c:\files")
```

假设用户输入了内容，我们可以使用 *FolderExists* 方法来验证输入。

```
If objFSO.FolderExists(strDir) Then
    '打开文件夹
    Set objFldr=objFSO.GetFolder(strDir)
...
```

我们需要一个日志文件来保存审计结果，既然我们知道可以继续，就需要创建一个文本文件。回想一下，通常一个函数返回一个值，而子程序是一段模块化的代码，可以根据需要调用。我们需要从用户那里获取日志文件名，所以脚本中有一个名为 *GetFileName* 的函数，它相当于一个 *InputBox* 包装器。

```
Function GetFileName()
    On Error Resume Next
    GetFileName=InputBox("您想要创建的审计文件名是什么？",_
    strTitle,"c:\filelog.txt")
End Function
```

同样，假设用户输入了内容，我们需要验证日志文件。我们调用 *ValidateFile* 子程序，它接受一个文件名作为参数。如果文件已存在，我们询问用户是否要覆盖该文件。

```
If objFSO.FileExists(strFile) Then
    rc=MsgBox(strFile & " 已存在。您是否想要" &_
    "覆盖它？",vbYesNoCancel+vbQuestion,strTitle)
```

根据回答，我们可以创建文本文件并覆盖现有版本，或者提示用户指定新的日志文件名。

```
Select Case rc
    Case vbYes
        wScript.Echo "正在覆盖文件 " & strFile
        Err.Clear
        '通过覆盖来创建我们的日志文件
        Set objTS=objFSO.CreateTextFile(strFile,True)
        If Err.Number<>0 Then
            strMsg="创建 " &_
            strFile & " 时出错" & vbCrLf & "错误号#" & Err.Number &_
```



# 第一部分：高级Windows脚本基础

```
" " & Err.Description
MsgBox strMsg, vbOKOnly + vbCritical, strTitle
WScript.Quit
End If
```
请注意，这里包含了覆盖文件时可能出现问题的错误处理。如果用户点击"否"，我们将再次调用`GetFileName`函数，然后调用`ValidateFile`子程序，本质上是重新运行代码。

```
Case vbNo
strFile = GetFileName
ValidateFile strFile
```
当然，用户可能会厌烦并点击"取消"，在这种情况下，我们只需退出脚本。

```
Case vbCancel
WScript.Echo "正在终止脚本"
WScript.Quit
End Select
```
如果文件不存在，我们创建它并返回脚本的主要部分。再次注意错误处理和`MsgBox`。

```
'创建我们的日志文件
Err.Clear
Set objTS = objFSO.CreateTextFile(strFile)
If Err.Number <> 0 Then
strMsg = "创建 " & _
strFile & " 时出错" & vbCrLf & "错误编号:" & Err.Number & _
" " & Err.Description
MsgBox strMsg, vbOKOnly + vbCritical, strTitle
WScript.Quit
End If
```
现在审计日志已经处理完毕，让我们开始正题，使用`FileSystemObject`来查看文件夹中的文件。我们通过调用`Files`方法创建一个集合对象来代表文件夹中的所有文件。

```
Set objFiles = objFldr.Files
```
我们可以使用`For...Each...Next`循环来枚举这个集合，并将每个文件的信息写入日志。

```
For Each file In objFiles
'获取文件信息并写入日志文件
objTS.WriteLine file.Name & vbTab & file.size & " 字节" & vbTab & _
file.DateCreated & vbTab & file.DateLastModified
i = i + 1
iPer = FormatPercent((i / t))
WScript.StdOut.Writeline(iPer & " 完成")
Next
```
*FileSystemObject*会暴露文件的属性，例如其名称、大小、创建、修改和访问的日期等。这个脚本创建了一个制表符分隔的文件，但也可以轻松地改为逗号分隔值（CSV）日志。

在检查完文件夹中的每个文件后，我们关闭日志文件并向用户显示完成消息。

```
objTS.Close
MsgBox "请查看 " & strFile & " 获取结果。", vbOKOnly + vbInformation, strTitle
```
顺便说一下，当前脚本不会递归处理任何子文件夹。我们将此留作你的练习。但这个脚本还有一个优点——我们添加了代码来向用户提供一些进度反馈。唯一的限制是，你必须使用CScript从命令行运行脚本。

我们的文件集合有一个*Count*属性，可以显示当前文件夹中的文件数量。如果我们知道文件总数和已处理的文件数，我们就可以计算完成的百分比。我们只需要一些变量。

```
'初始化我们的计数器
i = 0
'设置文件夹中文件总数的变量
t = objFiles.Count
```
在*For...Each*循环中，我们递增计数器变量并计算完成百分比。我们使用*FormatPercent*函数来整理计算结果。

```
i = i + 1
iPer = FormatPercent((i / t))
```
剩下要做的就是显示结果。我们决定使用*Wscript*对象的*StdOut*方法直接写入命令提示符窗口。

```
wScript.StdOut.writeline(iPer & " 完成")
```
如果脚本使用WScript运行，此方法将不起作用。必须通过在命令提示符下输入**cscript listing1-12.vbs**来使用CScript运行。完成百分比会在屏幕上滚动，通知用户脚本的进展情况。

我们只回顾了*FileSystemObject*的一些基础知识，这些是你在本书中可能遇到的。如需更多信息，请查看Windows Script Host 5.6文档。

> **最佳实践** 使用*FileSystemObject*时有很多机会出现错误和问题。例如，您可能尝试在不存在的驱动器上创建文本文件，或者在用户没有适当权限的文件夹中创建。或者您可能尝试访问不存在的文件夹或驱动器。当脚本让用户以运行时参数或从*InputBox*中指定文件和文件夹时，此类错误尤其常见。在脚本中实施错误处理和验证非常重要。使用*FileSystemObject*的*DriveExists*、*FolderExists*或*FileExists*方法。在创建新文本文件时检查错误，并添加代码以优雅地处理常见错误。您需要考虑所有可能合理发生的问题，例如将C:\输入为C:，并据此编码。

## 理解数组

一种基本的脚本技术是将数据存储在数组中，然后在脚本中使用该数据。数组可以非常复杂且是多维的，但出于我们的目的，我们保持它们简单和基本。将数组想象成一组桶，每个桶装着一条信息。当我们需要那条信息时，我们从其桶中检索它。每个桶都有一个编号，从0开始。

有几种方法可以将信息放入数组中。一种方法是使用*Array*函数。

```
myArray = Array("Elm", "Maple", "Oak", "walnut", "Hickory", "Pine")
```
当要存储的信息是预先知道的，并且数量相对较少时，这种技术非常有效。为了更动态的方法，我们使用*Split*函数。

```
strText = "Elm,Maple,Oak,walnut,Hickory,Pine"
myArray = Split(strText, ",")
```
*Split*函数接受指定的文本字符串，并将每个元素（在此例中以逗号分隔）拆分为数组的各个桶中。

在将数据放入数组后，如果我们知道桶的编号，就可以直接访问它。因此，如果我们想使用Walnut，我们将引用*myArray(3)*。尽管人类会将*Walnut*视为第四个元素（因为我们通常从1开始计数），但数组从0开始计数。因此，显示数组上限的*UBound(myArray)*函数返回5。如果我们想返回一个人类友好的数组元素计数，我们需要使用*UBound(myArray) + 1*。

要遍历数组中的每个元素，我们可以使用*For...Next*循环，如下所示。

```
For i = 0 To UBound(myArray)
    wScript.Echo myArray(i)
Next
```
通常，我们将数组中的值传递给脚本中其他地方的子程序或函数。我们将在本章后面给你一个示例。

## 字典对象

与数组类似，*Scripting.Dictionary*对象也可用于组织外部数据，但数组将数据从0开始放入桶中，而*Dictionary*对象将数据存储在称为*键*的页中。存储的数据被称为*项*。*Scripting.Dictionary*对象被认为是一个*关联数组*。

使用*Add*方法将数据存储在*Dictionary*对象中。

```
Dim objDict
Set objDict = CreateObject("Scripting.Dictionary")
objDict.Add "a", "Elm"
objDict.Add "b", "Maple"
objDict.Add "c", "Oak"
objDict.Add "d", "Walnut"
objDict.Add "e", "Hickory"
objDict.Add "f", "Pine"
```
要引用单个项，我们需要知道相应的键。以下代码行将返回键*b*或*Maple*的值。

```
wScript.Echo objDict.Item("b")
```
如果我们想枚举字典的键，我们需要使用*Keys*方法，如下所示。

```
objKeys = objDict.Keys
wscript.echo "共有 " & objDict.Count & " 个键"
For x = 0 To objDict.Count - 1
    WScript.Echo objKeys(x)
Next
```
*Count*方法可能会引起一些混淆。当与*Dictionary*对象一起使用时，该方法从1开始计数，在此示例中将返回6。然而，当我们遍历键集合时，我们从0开始计数，这就是为什么我们从0循环到*objDict.Count*值减1。

要获取字典中的所有项，我们使用*Items*方法。

```
objItems = objDict.Items
For x = 0 To objDict.Count - 1
    wScript.Echo objItems(x)
Next
```
那么哪种技术是正确的呢？这取决于您的脚本。如果您有大量数据需要整理和跟踪，*Dictionary*对象可能是可行的方法。有方法可以检查项是否存在、删除单个项以及删除所有项以便重新开始。*Dictionary*对象还使得更容易引用特定元素，因为您可以定义键。在数组中，每个元素都存储为一个编号的桶。



条目，你必须跟踪哪个项目在哪个存储桶中。然而，如果你只是要遍历每个元素并对其执行某些操作，数组稍微更容易管理一些。

你也可以在同一个脚本中同时使用两者。我们偶尔会使用这样的代码，其中 *Dictionary* 对象的值是一个 CSV 字符串，该字符串将被放入数组中进行进一步处理。

```vbscript
Dim objDict,objItems
Set objDict=CreateObject("Scripting.Dictionary")
objDict.Add "user1","John,555-1234,7/7/61"
objDict.Add "user2","Mary,555-1234,12/6/56"
objDict.Add "user3","Mike,555-1234,10/13/76"

wscript.echo "There are " & objDict.Count & " user entries."

objItems=objDict.Items
For x=0 To objDict.Count-1
    tmpArray=Split(objItems(x),",")
    strName=tmpArray(0)
    strPhone=tmpArray(1)
    strBDate=tmpArray(2)
    WScript.Echo "Adding " & strName & "(" & strBdate & ")"
    '在此处插入一些代码
Next
```

简而言之，你应该使用最适合你的技术。

## 理解活动目录服务接口基础

开发用于创建和管理用户及组的脚本是一项非常常见的管理任务。这些类型的脚本必须与目录服务进行交互，无论是 Windows NT 的 SAM 数据库还是活动目录。幸运的是，Microsoft 有一个称为活动目录服务接口的脚本接口。不要被这个名字迷惑。你不需要活动目录才能在你的脚本中使用 ADSI。如果你有一个 Windows NT 4.0 域，你仍然可以使用 ADSI；你只需要一个不同的提供程序。

提供程序负责处理与特定目录服务类型交互的所有繁琐工作。ADSI 有几种目录服务类型，但就我们的目的而言，我们将把回顾范围限制在 WinNT 和 LDAP 提供程序。

-   WinNT 提供程序用于处理旧版 Windows 域或系统。WinNT 提供程序旨在与平面命名空间（如 NT 4.0 域）一起工作。这并不是说你不能在活动目录中使用 WinNT 提供程序——你可以，而且在某些情况下它可能是首选的提供程序。我们将在本章后面给你一个示例。

LDAP 提供程序用于基于轻量级目录访问协议的目录服务，例如活动目录。你不能在 NT 4.0 域中使用 LDAP 提供程序，因为 LDAP 提供程序期望的是像活动目录这样的分层目录服务。

使用活动目录时，当你想以平面方式管理目录时可以使用 WinNT 提供程序，当你需要更分层的方法时可以使用 LDAP 提供程序。考虑这个简短的脚本，你应该使用 CScript 从命令提示符运行它。

```vbscript
Dim objDom,objNetwork
Set objNetwork=CreateObject("WScript.Network")
Set objDom=GetObject("winNT://" & objNetwork.UserDomain)
wScript.Echo "Listing users in " & objDom.name
objDom.Filter=Array("user")
For Each user In objDom
    wScript.Echo user.name
Next
```

假设你的域正在运行活动目录，并且你从域中的一台使用域账户的计算机运行它。此脚本列出域中的所有用户，无论他们位于哪个组织单元中。WinNT 提供程序没有 OU 的概念，它将目录视为一个大存储桶。

> **提示** 如果你发现你的 ADSI 脚本莫名其妙地失败，请检查提供程序。ADSI 提供程序区分大小写。WinNT 有效，但 WINNT 无效。

我们使用 *Filter* 方法仅获取属于 *user* 类或类型的目录对象。然后我们可以使用 *For...Each...Next* 循环遍历列表，并显示对象的名称。顺便说一句，这个名称是用户的 NT 4.0 账户名，也称为 *sAMAccountName*。如果你有活动目录并运行此脚本，你将不会看到像 *Jeffery Hicks* 这样的 Windows 2003 账户名，而是像 *jhicks* 这样的 Windows 2000 之前的名称。要显示用户的通用名，你必须使用 LDAP 提供程序。

> **更多信息** 提供程序使用的对象决定了哪些属性是可用的。有关使用 ADSI 的丰富信息来源可从 MSDN 网站获取，网址为

http://msdn.microsoft.com/library/default.asp?url=/library/en-us/adsi/adsi/active_directory_service_interfaces_adsi.asp

（此链接位于配套 CD 上；点击 *MSDN ADSI*。）我们还建议你下载 ADSI SDK，它不仅包含大量示例代码，还包含非常详尽的文档。你可以从 Microsoft 网站下载该工具包，网址为

http://download.microsoft.com/download/2/9/7/29720925-faa3-477f-a5cd-beef80adac07/adsrtk.msi

（此链接位于配套 CD 上；点击 *ADSI Resource Kit*。）

# 第一部分：高级 Windows 脚本基础

如果我们使用 LDAP 提供程序，我们将必须连接到根命名空间，找到所有组织单元和其他容器，并遍历它们。有查询 LDAP 目录的方法，但它们稍微复杂一些。对于此类事情，WinNT 方法快速、高效且易于理解。

使用 WinNT 提供程序的另一种方法是访问成员服务器和桌面。你可以使用 WinNT 提供程序查询本地用户、组和服务。要连接到远程系统，请使用如下代码。

```vbscript
strServer="File01"
Set objSrv=GetObject("WinNT://" & strServer)
```

这样的代码本质上连接到整个平面命名空间。如果你想连接到命名空间中的特定对象，你可以使用清单 1-13 中所示的代码片段。

### 清单 1-13 WinNT 示例：更改本地管理员密码
```vbscript
strServer="File01"
'为本地管理员账户设置的新密码
strPass="N3wP@ssw0rd"
set objUser=GetObject("WinNT://" & strServer & "/administrator,user")
objUser.SetPassword strPass
objUser.SetInfo
```

此脚本连接到服务器 File01 上的管理员账户。然后它调用 SetPassword 方法来更改管理员密码。

> 重要提示 切勿在脚本中硬编码管理员凭据或密码。清单 1-13 仅用于教育目的，不应按原样在生产环境中使用。此信息应在运行时作为脚本参数传递，或由用户通过提示输入。

我们想在此强调的一种方法是 SetInfo。此方法适用于 WinNT 和 LDAP 提供程序。你可能已经注意到 ADSI 使用 GetObject 方法，而不是 CreateObject。这是因为目录服务已经存在。ADSI 获取目录的副本并将其存储在本地缓存中。你对目录中对象所做的所有更改都保存在本地，直到你调用 SetInfo 才会提交回目录。

> 最佳实践 如果你发现自己正在修改目录对象的许多属性，不要在每次属性更改后都调用 SetInfo。等到完成所有操作后再调用 SetInfo 以一次性提交所有更改。否则，你会造成不必要的网络流量和服务器开销。

要使用 LDAP 提供程序，我们必须通过对象的 *可分辨名称* 连接命名空间。假设我们想在属于 Company.pri 活动目录域的 Employees OU 中创建一个新的用户对象。

```vbscript
Set objDom=GetObject("LDAP://OU=Employees,DC=Company,DC=pri")
```

通过此连接，我们可以使用 *Create* 方法创建新的用户对象。

```vbscript
strUser="Jeffery Hicks"
strSAM="jhicks "
strPass="P@ssw0rd"
Set objuser=objDom.Create("User","CN=" & strUser)
```

在获得新用户的 *sAMAccountName* 之后，我们可以将更改提交到活动目录，此时用户账户基本上就存在了。我们使用 *Put* 方法设置对象属性。

```vbscript
objUser.Put "samAccountname",strSAM
objUser.SetInfo
```

当然，我们不喜欢用户密码为空，因此我们需要调用 *SetPassword* 方法指定用户密码并提交更改。

```vbscript
objUser.SetPassword(strPass)
objUser.SetInfo
```

为什么我们不直接设置密码并只调用一次 *SetInfo*？因为对于尚不存在的对象，你无法调用 *SetPassword* 方法。在我们调用 *SetInfo* 提交新对象之前，它在活动目录中是不存在的。

我们将以清单 1-14 中的脚本结束这个简要回顾，该脚本创建了一个新的用户账户。

### 清单 1-14 ADSI 示例：创建用户
```vbscript
Dim objFSO,objTS
Dim objDom,objUser

Const FORREADING=1

strFile="newusers.csv"
'newusers.csv 的格式
'givenname,sn,password,telephonenumber,upnsuffix
'示例：
'Jeff,Hicks,P@sswordJH,555-1234,@jdhitsolutions.com
'Don,Jones,$cr1pting@nsw3rs,555-1234,@scriptinganswers.com

Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objTS=objFSO.OpenTextFile(strFile,FORREADING)

Set objDom=GetObject("LDAP://OU=Consultants,DC=Company,DC=pri")
```

# 第一部分：高级 Windows 脚本基础

```vbscript
'open text file and process user data on each line
Do while objTS.AtEndofStream<>True
  rline=objTS.readline
  UserArray=Split(rline,",")

  strFirst=UserArray(0)
  strLast=UserArray(1)
  strUser=strFirst & " " & strLast
  strLogon=Left(strFirst,1)&strLast
  strUsername=LCASE(Left(strFirst,1)&strlast)
  strPass=UserArray(2)
  strPhone=UserArray(3)
  strUPN=strUserName & UserArray(4)

'create user object
Set objUser=objDom.Create ("User","cn="&strUser)
objUser.Put "samAccountName",strUserName
objUser.SetInfo

'Now that user object is created, let's set some properties
objuser.Put "givenname",strFirst
objUser.Put "sn",strLast
objUser.Put "displayname",strFirst & " " & strLast
objUser.Put "UserPrincipalName",strUPN
objUser.Put "AccountDisabled",FALSE
objUser.Put "TelephoneNumber",strPhone
objUser.SetPassword(strPass)
objUser.SetInfo

Loop

objTS.Close

wScript.Quit
```

在此脚本中，我们有一个用于处理每个新账户的文本文件。不同用户属性的值由逗号分隔。

```vbscript
strFile="newusers.csv"
'format of newusers.csv
'givenname,sn,password,telephonenumber,upnsuffix
'example:
'Jeff,Hicks,P@sswordJH,555-1234,@jdhitolutions.com
'Don,Jones,$cr1pting@nsw3rs,555-1234,@scriptinganswers.com
```

我们使用 *FileSystemObject* 来打开并读取文件。

```vbscript
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objTS=objFSO.OpenTextFile(strFile,FORREADING)

Set objDom=GetObject("LDAP://OU=Consultants,DC=Company,DC=pri")

'open text file and process user data on each line
Do while objTS.AtEndofStream<>True
rline=objTS.readline
```

你会注意到，我们已经建立了与希望创建用户账户的组织单位 (OU) 的连接。我们使用 Split 函数创建了一个用户数据数组，并根据数据设置了一些变量。

```vbscript
UserArray=Split(rline,",")
    strFirst=UserArray(0)
    strLast=UserArray(1)
    strUser=strFirst & " " & strLast
    strLogon=Left(strFirst,1)&strLast
    strUsername=LCASE(Left(strFirst,1)&strlast)
    strPass=UserArray(2)
    strPhone=UserArray(3)
    strUPN=strUserName & UserArray(4)
```

之后，只需创建用户对象并指定 CN 和 sAMAccountName 即可。

```vbscript
'Create user object
Set objUser=objDom.Create ("User","cn="&strUser)
objUser.Put "samAccountName",strUserName
objUser.SetInfo
```

此时，剩下的就是设置其余的用户属性，并调用 SetInfo 将更改写入 Active Directory。

```vbscript
'Now that user object is created, let's set some properties
objUser.Put "givenname",strFirst
objUser.Put "sn",strLast
objUser.Put "displayname",strFirst & " " & strLast
objUser.Put "UserPrincipalName",strUPN
objUser.Put "AccountDisabled",FALSE
objUser.Put "TelephoneNumber",strPhone
objUser.SetPassword(strPass)
objUser.SetInfo
```

完成此操作后，我们可以循环读取文本文件的下一行，并重复该过程。使用这样的脚本，你可以在读完这句话的时间内，在舒适的办公桌前从头创建一百个完全填充的用户账户。

> **注意** 清单 1-14 中的脚本旨在作为教学辅助工具。你可以将其运行在生产环境中，前提是你添加了一些错误处理逻辑。例如，按照目前的写法，如果你尝试创建一个已存在的用户账户，将会收到错误。我们建议你添加代码来处理这种类型的错误，尤其是因为这是一个非常可预见的错误。

## 理解 Windows Management Instrumentation 基础

管理员需要掌握的更高级的脚本主题之一是如何使用 Windows Management Instrumentation (WMI)。WMI 是 Microsoft 和许多独立软件供应商 (ISV) 用于其管理应用程序和实用程序的技术。你可以使用相同的技术，并根据你的环境完全自定义地开发自己的管理脚本。让我们花几分钟时间回顾一些 WMI 基础知识。我们将在本书后面更详细地探讨 WMI。

### Winmgmts

大多数 WMI 脚本使用 *Winmgmts* 对象连接到 WMI 命名空间，该对象可用于连接到本地或远程 WMI 命名空间。通常，默认命名空间是 root\cimv2，大多数 Windows 管理脚本都连接到此命名空间，但可以使用 WMI 管理控制台进行更改。

考虑以下代码行。

```vbscript
Set objWMI=GetObject("winmgmts://")
```

这将连接到本地计算机上的默认 WMI 命名空间。注意我们像使用 ADSI 一样使用 *GetObject*。要连接到远程系统，只需添加计算机名称即可。

```vbscript
strServer="File01"
set objWMI=GetObject("winmgmts://" & strServer)
```

虽然不是必需的，但指定要连接的命名空间（即使它是默认的）是一个好习惯，因为默认值可能会更改。

```vbscript
set objWMI=GetObject("winmgmts://" & strServer & "\\root\\cimv2")
```

使用这样的代码可以消除关于你正在使用哪个命名空间的任何疑虑，特别是如果有人更改了默认的 WMI 命名空间。在后面的脚本中，当我们连接到不同的命名空间时，我们必须指定一个命名空间；通过现在养成这个习惯，你将使你的脚本更容易理解和调试。

到目前为止，我们所做的只是连接到 WMI 命名空间——我们还没有向它询问任何信息。假设你知道你想了解更多信息的类，例如 *Win32_OperatingSystem*，你可以使用两种技术。第一种是使用 *InstancesOf* 方法。

```vbscript
strServer="File01"
set objWMI=GetObject("winmgmts://" & _
strServer).InstancesOf("win32_OperatingSystem")
```

另一种技术是执行查询。我们将在稍后复习 WMI 查询。

```vbscript
strServer="File01"
strQuery="Select * from win32_OperatingSystem"
set objWMI=GetObject("winmgmts://" & strServer)
set objRef=objWMI.ExecQuery(strQuery)
```

使用这种技术，我们实例化一个新对象来保存查询结果。返回的数据以集合的形式出现，所以我们只需使用 *For...Each...Next* 循环来处理这些信息。

```vbscript
For each item in objRef
    wscript.echo item.Name
    wscript.echo item.RegisteredUser
    wscript.echo item.Organization
Next
```

当然，你需要知道属性的名称。你可以从像 *Managing Windows with VBScript and WMI* (Jones, Don, Addison-Wesley, 2004) 这样的脚本书籍或 MSDN 网站 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/wmisdk/wmi/wmi_reference.asp 获取此信息。

**在随书光盘上** 此链接包含在随附的 CD 上。请点击 *MSDN WMI Reference*。

> **提示** 并非每个类的每个属性在 WMI 中都已填充。WMI 为类信息提供了一个存储库，但由各个供应商决定存储哪些数据。可能会有来自两个供应商的两台服务器，一台可能有某个特定类的信息，而另一台则可能没有。不要假设你的脚本有问题；可能只是没有任何信息。在这种情况下，请使用 WbemTest 和 WMI Tools 等工具来枚举类，以便你可以验证存在哪些信息。

快速学习属性名称的方法是询问。使用此代码代替刚刚显示的代码，以获取所有属性和值的列表。

```vbscript
For each item in objRef
    For Each property in item.Properties_
        WScript.echo property.Name & ": " & Property.Value
    Next
Next
```

### WMI 查询语言 (WQL)

正如我们刚刚演示的，使用查询从 WMI 检索信息非常容易。WMI 有其自己的查询语言和语法，与 SQL 非常相似。出于本基础复习的目的，实际上只有两种类型的 *Select* 查询。第一种是请求某个对象类所有信息的查询。

```vbscript
strQuery="select * from win32_ComputerSystem"
```

第二种查询请求有关指定对象类的信息。它更具选择性，因此你必须知道你要查找什么信息。



# 第一部分：高级 Windows 脚本基础

```
strQuery="Select Manufacturer,Model,Description from win32_ComputerSystem"
```

根据对象类的不同，仅请求您需要使用的信息可能更为高效。当您只需要一两个属性值时使用 `Select *` 查询，会给脚本增加不必要的开销。

您可以通过选择符合特定条件的属性来进一步优化脚本。例如，`Win32_LogicalDisk` 类有一个名为 `DriveType` 的属性。此属性的值指示驱动器是固定的（如 C 盘）、可移动的（如 A 盘），还是其他类型。考虑以下查询，它返回所有固定驱动器的 `DeviceID` 和 `Size` 属性。

```
strQuery="Select DeviceID,Size from win32_LogicalDisk where Drivetype = '3'"
```

根据经验，并且您可以通过使用 Wbemtest 测试查询得知，固定驱动器的值为 "3"。通过将查询限制为特定的驱动器类型，我们可以更快地获得更有用的信息。

## SWbemLocator

`winmgmts` 对象的主要优势之一是易于使用。您只需一两行代码即可建立安全的 WMI 连接。但是，在某些情况下，此对象无法完成任务。通常，当您执行脚本时，WMI 会获取运行该脚本的用户凭据，并在指定计算机上模拟该用户。但如果您想使用替代凭据运行脚本怎么办？您可以使用 `RunAs` 命令，可以使用 Microsoft 的 WMI 脚本应用程序编程接口（API）开发 WMI 脚本，或者可以使用 `SWbemObject`。

使用 `SWbemObject` 比使用 `winmgmts` 需要更多的编码，但它允许您指定替代凭据。您首先需要创建一个 `SWbemLocator` 对象。

```
Set objLoc=CreateObject("wbemScripting.SWbemLocator")
```

此对象有一个 `Security_` 属性，您可以设置它。通常，您可以指定 `ImpersonationLevel`，默认情况下为 3。

```
objLoc.Security_.Impersonation=3
```

在此处，您还可以指定用户可能需要的额外权限，例如远程关闭系统的能力。

```
Const SHUTDOWNREMOTEPRIVILEGE=23
Set objLoc=CreateObject("wbemScripting.SWbemLocator")
objLoc.Security_.Impersonation=3
objLoc.Security_.Privileges.Add SHUTDOWNREMOTEPRIVILEGE
```

接下来，我们连接到服务器，可以是本地服务器，也可以是远程服务器。

```
Set objCon=objLoc.ConnectServer(strServer,"root\cimv2")
```

这行代码适用于本地系统，但如果您要连接到远程系统，则必须指定替代凭据。

```
Set objCon=objLoc.ConnectServer(strServer,"root\cimv2",strUser,strPassword)
```

请记住，对于本地连接，您不能指定替代密码。此连接创建了一个 *SWbemServices* 对象。

现在我们有了到系统的安全连接，就可以执行查询了。

```
strQuery="Select * from Win32_OperatingSystem"
set objRef=objCon.Execquery(strQuery)
```

然后我们可以遍历 *objRef* 中的数据。清单 1-15 说明了如何使用 *SWbemLocator* 对象连接到使用替代凭据的远程系统。

```
清单 1-15 SWbemLocator 示例：获取驱动器信息
Dim objWBEM,objCon,objRef
strServer="FILE01"
strUser="Administrator"
strPassword="$3cret"
strQuery="Select DeviceID,Size,FreeSpace,FileSystem from " &_
"win32_LogicalDisk where DriveType='3'"
Set objWBEM=CreateObject("wbemScripting.SwbemLocator")
set objCon=objWBEM.ConnectServer(strServer,"root\cimv2",strUser,strPassword)

set objRef=objCon.ExecQuery(strQuery)
For Each drive In objRef
    strMsg=strMsg & "Drive " & drive.DeviceID & "(" & drive.FileSystem &_
    ")" & vbCrLf
    strMsg=strMsg & "Size: " & drive.Size & " bytes"  & vbCrLf
    strMsg=strMsg & "Free Space: " & drive.FreeSpace & " bytes" & vbCrLf
    strMsg=strMsg & FormatPercent(drive.FreeSpace/Drive.size) &_
    " Free" & vbCrLf
    strMsg=strMsg & vbCrLf
Next

wScript.Echo strMsg
wScript.Quit
```

这种脚本编写 WMI 的方法为您提供了更精确的控制以及使用替代凭据的能力。如果替代凭据不是必需条件，下一页的清单 1-16 中的脚本完成了与清单 1-15 相同的任务，但使用了 *winmgmts*。

### 清单 1-16 Winmgmts 示例：获取驱动器信息

```
dim objWMI, objRef
'enter any computer name
strServer="FILE01"
strQuery="Select DeviceID,Size,FreeSpace,FileSystem from " & _
"win32_LogicalDisk where drivetype='3'"
set objWMI=GetObject("winmgmts://" & strServer & "\root\cimv2")
set objRef=objWMI.ExecQuery(strQuery)
WScript.Echo "Logical Drive Report for " & strServer
for each drive in objRef
    strMsg=strMsg & "Drive " & drive.DeviceID & "(" & drive.FileSystem & _
    ")" & vbcrlf
    strMsg=strMsg & "Size: " & drive.Size & " bytes" & VbCrLf
    strMsg=strMsg & "Free Space: " & drive.FreeSpace & " bytes" & VbCrLf
    strMsg=strMsg & FormatPercent(drive.FreeSpace/drive.Size) & _
    " Free" & VbCrLf
    strMsg=strMsg & VbCrLf
Next

WScript.Echo strMsg
```

我们将在本书中更深入地探讨 WMI。

> **更多信息**  除了已经提到的书籍和链接，我们还推荐 *Windows Management and Instrumentation* (Matthew Lavy & Ashley Meggitt, New Riders, 2002) 和 *WMI Essentials* (Marcin Policht, SAMS, 2002)。

## 高级脚本编写目标

既然我们已经打好了基础，让我们看看本书的目标。

### 保护脚本安全

如果您认真考虑在企业中将 VBScript 作为管理工具使用，则必须确保其安全性。在第 2 章“脚本安全”中，我们将探讨如何通过使用数字签名和证书来创建更安全的脚本。我们还将回顾如何配置生产环境以安全地运行脚本。

### 创建您自己的脚本组件和库

优秀脚本编写者的一个标志是代码重用的能力。在第 3 章“Windows 脚本文件”中，我们将花一些时间讨论 Windows 脚本文件（`.wsf` 脚本）以及如何构建可重用的脚本库。我们还将在第 4 章“Windows 脚本组件”中向您展示如何创建自己的脚本组件。使用脚本组件向导，您将能够创建自己的 COM 对象。

### 远程运行脚本

尽管有多种方法可以通过脚本远程管理系统，但有时您可能希望脚本在远程系统上本地运行。在第 6 章“远程脚本”中，我们将向您展示使用 *WshController* 对象所需了解的内容，以及如何正确配置您的网络。

### 从 Active Directory 检索信息

您可能了解一些 ADSI 基础知识。我们在第 8 章“高级 ADSI 和 LDAP 脚本”和第 9 章“结合使用 ADO 和 ADSI”中涵盖了一些高级 ADSI 和 LDAP 主题。我们演示如何使用 Microsoft 的 EZADSomatic 和其他免费工具。这些工具有助于快速开发脚本，并且在尝试找出脚本无法正常工作的原因时可能非常宝贵。我们还深入探讨了 LDAP 查询以及使用 ActiveX 数据对象（ADO）的 ADSI 查询的奥秘。

### 操纵存储在数据库中的信息

对于初级脚本管理员来说，处理 CSV 文件是一种非常标准的做法。要将脚本编写提升到新的水平，您必须知道如何编写使用数据库技术的脚本。在第 7 章“数据库脚本”中，我们将回顾各种类型的数据库以及如何连接和操作它们。

### 使用 WMI 事件管理您的 Windows 环境

我们承诺 WMI 将是本书的一个主要主题。在第 11 章“WMI 事件”中，我们将探索 WMI 事件、使用者、过滤器和计时器的世界。我们还将向您展示如何使用事件接收器来密切管理您的系统，并包含大量可在您环境中使用的示例。

### 使用 Windows XP 和 Windows Server 2003 的新 WMI 类

在第 13 章“Windows XP 和 Windows Server 2003 中的高级脚本”中，我们将介绍 Microsoft Windows XP 和 Microsoft Windows Server 2003 中可用的一些新 WMI 类。这些类为您的脚本增添了真正的力量，并开启了新的机会。我们还将介绍有助于处理 DNS、IIS 6.0、打印、配额等的新类。每个新类都将包含一个完整的管理示例。

### 使用脚本管理组策略对象

如果您管理一个 Active Directory 林，那么您很可能正在使用组策略。您的组策略环境可以通过组策略管理控制台使用 VBScript 进行管理。我们在第 14 章“组策略管理脚本”中探讨对象模型，并研究如何使用脚本来备份、复制、还原以及设置权限。



## 管理您的 Exchange 2003 环境

在第15章“Exchange Server 2003 脚本”中，我们继续探索企业级脚本，重点讲解如何管理您的 Exchange 2003 环境。您将学习使用新的 WMI 类、ADSI、协作数据对象（CDO）以及用于 Exchange 管理的协作数据对象（CDOEXM）来开发脚本，以管理服务器、存储组、邮件存储和邮箱。

## 将您的脚本集成到 Microsoft Operations Manager 中

在第16章“Microsoft Operations Manager 2005 脚本”中，我们将探讨 Microsoft Operations Manager 2005（MOM）如何使用 VBScript。我们还将探索一个新的对象模型。接着，我们将了解如何编辑现有的 MOM 脚本，并解释如何从头开始编写新脚本。

## 使用 Internet Explorer 和 HTML 应用程序（HTA）为您的脚本创建可视化界面

厌倦了简单的命令行脚本，或者希望图形化脚本能超越 *MsgBox* 函数提供更多功能？在第5章“HTML 应用程序：具有用户界面的脚本”中，我们将向您展示如何使用 HTA 创建更丰富的脚本。您无需成为 Web 开发人员——我们会提供足够的信息和易于遵循的示例，帮助您将现有脚本转换为 HTA。

## 我们不会涵盖的内容

尽管本书是关于高级脚本主题的，但我们不可能涵盖管理员需要了解的所有内容。不过，我们会为您指明获取更多信息的正确方向。

- **ASP 和 Web 脚本** 我们确信，如果您访问您喜欢的图书销售商，会找到大量关于 ASP 和基于 Web 脚本的书籍。在线方面，以下是一些不错的起点：
    - http://msdn.microsoft.com
    - http://www.15seconds.com
    - http://www.4guysfromrolla.com/
    - http://www.asp.net

- **.NET 编程** 尽管我们的某些脚本看起来像是使用高级语言的复杂编程练习，但它们并非如此。它们是在运行时解释执行的脚本。我们不会花时间使用任何 .NET 技术或任何其他编程语言。

- **Microsoft Office 自动化** 有不少免费可用的脚本，它们使用 Microsoft Word 或 Microsoft Excel 来创建精美的报告或作为数据源。这些脚本使用 Microsoft Office 的 COM 对象，本质上是将 Visual Basic for Applications（VBA）代码转换为独立的 VBScript。这项技术超出了本书的范围。如果您对此主题感兴趣，请在网上搜索“office vbscript”，或访问以下网站：
    http://msdn.microsoft.com/library/default.asp?url=/library/en-us/odc_2003_ta/html/odc_anoffice.asp

    > **随书附赠 CD** 此链接包含在随书附赠的 CD 中。请点击 *MSDN Office Automation*。

## 查找有关 JScript、Perl、Python 和 KiXtart 的信息

当然，VBScript 并不是唯一可用的脚本语言，但我们为本书选择它是因为我们认为它对于初学脚本的人来说最容易学习和阅读。其他脚本语言也有其优势，但 VBScript 是 Microsoft 管理员的主流脚本语言。如果您想了解更多关于其他脚本语言的信息，您可能会对以下网站感兴趣。

- **JScript**
    - http://msdn.microsoft.com/library/default.asp?url=/library/en-us/script56/html/js56jsoriJScript.asp

    > **随书附赠 CD** 此链接包含在随书附赠的 CD 中。请点击 *MSDN Jscript documentation*。

    Windows Script Host 5.6 文档也包含 JScript 参考。

- **Perl**
    - http://www.perl.com
    - http://www.perl.org
    - http://www.activestate.com
    - http://www.perlmonks.org

- **Python**
    - http://www.python.org
    - http://diveintopython.org/
    - http://aspn.activestate.com/ASPN/Python/Cookbook/

- **KiXtart**
    - http://www.kixtart.org
    - http://www.microsoft.com/technet/scriptcenter/scripts/kixtart/default.mspx

    > **随书附赠 CD** 此链接包含在随书附赠的 CD 中。请点击 *Microsoft Technet Script Center - Kix*。

## 工欲善其事，必先利其器

如果您打算专业地进行脚本开发，就应该投资于专业工具。如果您仍然使用记事本作为脚本编辑器，那么您开发脚本花费的时间会超出必要的。在这个阶段，是时候购买一个商业级的脚本编辑器了。

市场上有许多编辑器，每个都有稍有不同的功能集。它们在某种程度上共同拥有的功能是让脚本编写时间更高效。其中一个功能是内联智能感知，它可以在列表中显示对象、方法和属性。只需轻轻一点，您就可以避免输入许多错误。另一个功能是能够插入代码片段或保存的小段代码。一些编辑器附带了代码示例库，通常还允许您添加自己的示例。

商业编辑器通常还包括某种形式的脚本颜色编码。这使得识别脚本结构变得非常容易，并简化了故障排除。说到故障排除，大多数编辑器允许您设置断点和其他调试功能。如果编辑器有内置的调试器，那就更好了。有些编辑器还包括各种脚本生成向导、在线帮助以及指向本地工具（如 RegEdit）的链接。

我们在随书附赠的 CD 上尽可能多地收集了主要脚本编辑器的演示和评估版本。我们鼓励您试用它们，并找到一个满足您需求的。您需要决定哪些功能对您很重要，以及您（或您的老板）愿意花多少钱。但是，即使是一个提供基本颜色编码和行号的免费编辑器，也会使脚本开发和故障排除变得更加容易。

### 脚本技术

我们坚信，要为正确的工作使用正确的工具。使用 Microsoft 技术的一大好处是，通常有不止一种方法可以完成特定任务。例如，您可以在批处理文件中使用 Windows Management Instrumentation 命令行（WMIC）语句获取与在 VBScript 中使用 WMI 几乎相同的信息。同样，可能有一个工具包实用程序可以几乎像您编写的脚本一样好地完成一项工作。是什么让一个工具比另一个更好？

当您需要为某个问题开发解决方案时，在打开脚本编辑器之前需要考虑几件事。例如，谁将使用该解决方案？它将如何使用？这是需要计划在半夜运行，还是由具有域管理员凭据的人员交互式运行？是否存在可能影响您解决方案的环境、管理或安全限制？

您还需要考虑您对可用选项的熟悉程度。如果您可以将一个简单的批处理文件组合在一起，比从头开始编写脚本更容易地运行命令行实用程序，那何必费心编写脚本呢？即使您是一位经验丰富的脚本开发人员，您也需要权衡投入的时间和获得的回报。如果您可以通过使用现有的实用程序和批处理文件更轻松地实现目标，就没有必要投入大量时间编写 VBScript。就这一点而言，即使存在商业替代方案，您也需要权衡成本。开发和测试一个解决方案需要多长时间？在编写脚本时，因为没有做其他任务而损失了多少时间？商业替代方案的成本是多少？

我们坚信，Windows 环境中的脚本开发正在成熟，并且需要超越临时解决方案。开发脚本或自动化解决方案应该与 Visual Basic .NET 项目一样，以同等的专业性和规划性来对待。这意味着要制定业务案例，记录需求，并根据所有情况选择最经济的方法。

工欲善其事，必先利其器。正确的工具是您易于使用的、让您在最短时间内开发出可行解决方案的、并且最具经济效益的工具。

### 总结

本章是 VBScript 以及本书中将要使用的许多脚本技术的复习课程。我们还概述了我们将要涵盖的主题，以及不会涵盖的主题。最后，我们讨论了一些脚本理念。至此，您应该已经准备好将您的脚本提升到一个新的水平。让我们开始吧。



# 第2章
脚本安全

本章内容：
- 脚本编码与解码 41
- 脚本签名与Windows脚本宿主信任策略 43
- 替代凭据 52
- 总结 54

毫无疑问，脚本可能很危险；诸如Melissa和“我爱你”等广为人知的病毒已经证明了这一点。但同样毫无疑问的是，脚本也可以是有用的工具。你如何确保运行的是好的脚本，而避免坏的脚本？Windows脚本宿主安全机制，连同其他安全技术，可以帮助在任何环境中安全地使用脚本。我们将向你展示如何做到这一点。

我们见过许多管理员采取措施来锁定脚本执行。不幸的是，其中许多措施并不有效。例如，简单地删除wscript.exe和cscript.exe并不能保证脚本无法运行。作为Microsoft Windows核心操作系统的一部分，这些文件会被Windows文件保护、特定补丁和更新以及服务包所替换。同样，简单地重新分配脚本文件扩展名——例如.vbs和.wsf——也不能保证脚本安全，因为任何文件扩展名的脚本都可以通过将脚本文件名作为命令行参数传递给wscript.exe或cscript.exe来执行。

```
wscript.exe MyScript.txt
```

最后，这两种技术——以及它们的无数变体——并非旨在保证*安全*的脚本执行，而是旨在完全*限制*脚本执行，从而使你无法使用这个有益的管理工具。然而，有一些技术可以用来使脚本更安全。

## 脚本编码与解码

脚本编码是通过Microsoft脚本编码器实现的，该工具可从Microsoft网站免费下载。

http://www.microsoft.com/downloads/details.aspx?FamilyId=E7877F67-C447-4873-B1B0-21F0626A6329&displaylang=en

> **在CD上** 与本书中引用的大多数链接一样，此链接包含在附带的CD中。点击*下载详情-脚本编码器*。

脚本编码器的目的是防止你的脚本被轻易读取。下面是一个示例脚本。

```
'此处的所有内容将保持明文
'包括文档、注释等
'**开始编码**
'此处之后的内容将被编码
MsgBox "Hello, world!"
```

运行脚本编码器后，脚本将如下所示。

```
'anything here will be left clear-text
'include documentation, comments, etc
'**Start Encode**#@~^QQAAAA==@##&B)XDtk o,COD+.P4+.n,k/,nx1WN[@#@&t/
TAG6~E_+sVKSPSW.s9"J@#@&zxIAAA==^#~@
```

你可能认为这对于某些类型的脚本安全问题来说是一个有价值的工具，例如编写具有硬编码管理员凭据的脚本。例如，这样的脚本可能允许助手重置用户密码，而无需给予他或她执行其他管理任务的能力。然而，这并非完全安全的脚本编写方式，尽早澄清这一误解很重要。

事实是，脚本编码器并非脚本*加密器*。从技术上讲，编码器确实执行了一种加密，它使用了所谓的*对称密钥*。这是一个用于加密和解密密码的单一密钥，但由于Windows脚本宿主的每个副本都内置了相同的密钥，编码器作为安全工具早已变得无用。有许多现成的工具可以将脚本解码回其纯文本版本，从而揭示其中的任何敏感信息。其中一些工具包括：

- http://www.virtualconspiracy.com/index.php?page=scrdec/intro，一个可下载的工具
- http://www.greymagic.com/security/tools/decoder/，一个在线工具，可直接在网页中解码脚本，无需下载
- http://www.password-crackers.com/crack/scrdec.html，这不是免费的；尽管它与免费工具大致相同

我们列出这些网址并非为了奖励这些工具的作者，而是为了提请你注意一个事实：不能依赖脚本编码器来保护安全敏感信息。事实上，这从来都不是脚本编码器的用途。它的初衷是模糊网页中的代码，从而减少（但并非消除）知识产权被盗的可能性。脚本可以轻松解码的事实意味着你*永远不应*将脚本编码器视为安全工具，因为解码器很容易就能揭示你试图保护的敏感信息。

## 脚本签名与Windows脚本宿主信任策略

Windows脚本宿主（WSH）5.6包含一个名为信任策略的新功能。由于WSH 5.6随最新的Windows操作系统版本（包括最新的服务包）一起安装，并且可以免费下载，因此没有理由不利用信任策略来提供更安全的脚本环境。信任策略使用基于证书的高级技术来帮助确定哪些脚本可以信任，哪些不能。

### 理解数字证书和脚本签名

信任策略基于*代码签名*的概念，它使用数字证书唯一地签名一段代码，例如脚本或可执行文件。代码签名过程计算一个*校验和*，这是一个由复杂数学算法创建的唯一值。任何给定的代码段只有一个校验和，并且没有两段代码具有相同的校验和。校验和使用证书的私钥加密，并使用证书的公钥解密。例如，Microsoft为其大部分软件的可执行文件和DLL签名。例如，图2-1显示了应用于Microsoft Excel 2003主可执行文件的签名。

![图 2-1：Excel.exe 的签名](img/4fefd6988ba5d4a92a65127617ca24c2_62_0.png)

**图 2-1** Excel.exe 的签名

要验证签名，Windows使用证书的公钥解密签名。如果解密成功，Windows知道该签名是有效的，因为只有签名者才会拥有创建该签名的私钥。然后Windows计算代码的校验和，并将其与解密签名中的校验和进行比较。如果两者匹配，则代码未被修改。如果两者不匹配，则代码自签名以来已被修改。如果出现这种情况，则该代码被视为*不受信任*。

# 第一部分：高级Windows脚本基础

然而，仅仅拥有正确的签名并不能保证代码被认为是受信任的，因为用于创建数字签名的证书也必须由受信任的证书颁发机构（CA）颁发。图2-2显示了用于签署Excel.exe的证书的详细信息。如你所见，该证书由Microsoft代码签名PCA颁发。

![图 2-2：查看代码签名证书的详细信息](img/4fefd6988ba5d4a92a65127617ca24c2_63_0.png)

**图 2-2** 查看代码签名证书的详细信息

图2-3显示了该证书的认证路径，其中列出了Microsoft根证书颁发机构作为授权此证书的根CA。

![图 2-3：查看代码签名证书的认证路径](img/4fefd6988ba5d4a92a65127617ca24c2_63_1.png)

**图 2-3** 查看代码签名证书的认证路径

### 信任问题

为什么Microsoft根证书颁发机构是受信任的CA？为什么*任何*列出在Internet选项中的CA都是受信任的？通常，这是因为Microsoft在发布Windows时包含了它们，或者因为你已将它们添加为你自己的受信任根CA。但受信任意味着什么？

数字证书的目的是唯一标识证书持有者。就Microsoft而言，该证书代表Microsoft公司。如果Microsoft以外的人获得了Microsoft证书，该人可以冒充Microsoft签署恶意软件，诱使你认为它是安全的。因此，CA的目的是确保*仅*将证书授予适当的个人。当你说你信任某个CA时，你是在说你信任他们在颁发证书之前验证个人或公司身份。

很可能，你根本不知道“证书”对话框中列出的CA中有多少是值得信赖的。为了获得最大安全性，你应该从“受信任的根证书颁发机构”列表中移除任何你不熟悉其业务实践的CA，直到你验证其有关安全性的业务实践令人满意为止。请注意，移除一个或多个CA可能会导致应用程序（如Internet Explorer）中出现警告，因为你可能尝试通过https连接到一个具有由你已移除的CA颁发的证书的网站。但是，如果你不信任该CA，你也不应该信任该https连接。

考虑到许多管理员在这方面的担忧，Microsoft在以下位置发布了一篇知识库文章

http://support.microsoft.com/default.aspx?scid=kb;en-us;293819

该文描述了如何从列表中移除CA。

![Internet 选项 - 受信任的根证书颁发机构](img/4fefd6988ba5d4a92a65127617ca24c2_64_0.png)

> **在CD上** 此链接包含在附带的CD中。点击*如何从受信任的根存储中移除根证书*。

要检查此CA是否在Microsoft Windows 2000、Microsoft Windows XP或Microsoft Windows Server 2003计算机上受信任，请打开“控制面板”，双击“Internet选项”图标，然后单击“内容”选项卡。在“Internet属性”对话框的“根证书颁发机构”选项卡上，单击“发行者”按钮以查看受信任的根证书颁发机构列表，如下一页的图2-4所示。如你所见，Microsoft根证书颁发机构在此列表中，这意味着它——以及它授权或颁发的所有证书，及其从属CA授权或颁发的所有证书——都是受信任的。

因此，因为用于签署Excel.exe的证书最终来自受信任的根CA，并且因为签名完好且正确，所以Excel.exe是受信任的代码。



这种信任的概念对于脚本来说工作方式完全相同。你可以从商业证书颁发机构（CA）或内部CA获取代码签名证书，并使用该证书对脚本进行签名。如果颁发证书的CA是受信任的，并且脚本未被修改，那么脚本就会被信任。

现在你需要一种方法来阻止不受信任的脚本运行，这就是WSH TrustPolicy发挥作用的地方。

## 理解WSH TrustPolicy

WSH TrustPolicy默认处于一种本质上中立的状况，即同时允许受信任和不受信任的脚本运行。但是，你可以通过特定的注册表设置重新配置WSH。主要的可配置部分有两个；一部分为所有用户配置计算机范围的设置，另一部分配置特定用户的偏好设置。

特定用户设置位于HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\Windows Script Host\Settings。在此注册表项下，你可以创建一个主要的REG_DWORD值：

- **TrustPolicy** 将其设置为0以运行受信任和不受信任的脚本，或设置为2仅运行受信任的脚本。如果将此值设置为1，在允许不受信任的脚本运行之前，会提示用户。

计算机范围的设置位于HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\Windows Script Host\Settings，你可以指定几个REG_DWORD值：

- **TrustPolicy** 其配置方式与同名的用户特定值相同。通常，用户特定设置优先于计算机范围设置。
- **IgnoreUserSettings** 如果设置为1，计算机范围的TrustPolicy设置将覆盖任何用户特定设置。默认值为0。
- **SilentTerminate** 如果设置为1，尝试运行不受信任的脚本将不会导致警告消息。如果设置为0（默认值），运行不受信任的脚本（即TrustPolicy设置为2时）将导致警告消息。
- **UseWINSAFER** 此值仅适用于Windows XP及更高版本。如果设置为0（默认值），WSH TrustPolicy将被禁用，转而使用软件限制策略（我们将在本章后面讨论）。将此值设置为1可启用WSH TrustPolicy。

我们通常建议启用WSH TrustPolicy并将其设置为2，对所有用户生效，除非你使用的是更灵活的软件限制策略。

## 在你的环境中配置WSH TrustPolicy

如果你已决定在你的环境中实施WSH TrustPolicy（你为什么不呢？），你可以通过登录脚本或其他实用程序手动进行必要的注册表更改，但组策略（Group Policy）无疑是部署这些设置的最有效方法。清单2-1是一个管理模板（.adm文件），可以导入到组策略对象（GPO）中，以集中配置WSH TrustPolicy。

```
清单2-1 WSH TrustPolicy模板
#if version >= 3
CLASS USER

CATEGORY "Windows Script Host"

    POLICY "Windows Script Host trust policy"
        EXPLAIN "配置Windows Script Host 5.6或更高版本对于未签名或不受信任脚本的行为。这与计算机配置中的Windows Script Host设置交互。在WinXP及更高版本上，此设置仅在关闭WSH软件限制策略时处于活动状态。"
        KEYNAME "Software\Microsoft\Windows Script Host\Settings"
        PART "Allow untrusted scripts" DROPDOWNLIST REQUIRED
            VALUENAME "TrustPolicy"
            ITEMLIST
                NAME "Always" VALUE 0
                NAME "Prompt user" VALUE 1
                NAME "Never" VALUE 2
            END ITEMLIST
        END PART
    END POLICY

END CATEGORY

CLASS MACHINE

CATEGORY "Windows Script Host"

POLICY "Windows Script Host trust policy"
    EXPLAIN "配置Windows Script Host 5.6或更高版本对于未签名或不受信任脚本的行为。这与用户配置中的Windows Script Host设置交互。在WinXP及更高版本上，此设置仅在关闭WSH软件限制策略时处于活动状态。"
    KEYNAME "Software\Microsoft\Windows Script Host\Settings"
    PART "Allow untrusted scripts" DROPDOWNLIST REQUIRED
        VALUENAME "TrustPolicy"
        ITEMLIST
            NAME "Always" VALUE 0
            NAME "Prompt user" VALUE 1
            NAME "Never" VALUE 2
        END ITEMLIST
    END PART
END POLICY

POLICY "Ignore User Configuration settings for WSH security"
    EXPLAIN "启用后，导致计算机配置中WSH信任策略设置覆盖用户配置设置"
    KEYNAME "Software\Microsoft\Windows Script Host\Settings"
    PART "Ignore User Configuration" CHECKBOX
        VALUENAME "IgnoreUserSettings"
        VALUEON 1
        VALUEOFF 0
    END PART
END POLICY

POLICY "Use Software Restriction Policies"
    EXPLAIN "启用后，软件限制策略覆盖WSH信任策略设置"
    KEYNAME "Software\Microsoft\Windows Script Host\Settings"
    PART "Use Software Restriction Policies" CHECKBOX
        VALUENAME "UseWINSAFER"
        VALUEON 1
        VALUEOFF 0
    END PART
END POLICY

POLICY "Warn User"
    EXPLAIN "启用后，当WSH无法执行不受信任的脚本时显示警告"
    KEYNAME "Software\Microsoft\Windows Script Host\Settings"
    PART "Warn user that untrusted scripts won't execute" CHECKBOX
        VALUENAME "silentTerminate"
        VALUEON 0
        VALUEOFF 1
    END PART
END POLICY

END CATEGORY
#endif
```

> **在光盘上** 你也可以在随书附带的光盘上找到这个ADM模板，Wsh.adm。

请注意，WSH TrustPolicy设置并不包含在注册表的\SOFTWARE\Policies部分下，这意味着它们不被视为真正的策略（policy）。相反，Microsoft将它们称为*首选项*（preferences），策略和首选项之间存在一些重要区别：

- 要移除首选项，你必须配置一个GPO，将首选项重新配置为它们的原始默认值。仅删除设置或取消GPO链接不会移除首选项。
- GPO编辑器通常不会显示首选项。右键单击“管理模板”文件夹并单击“属性”可强制GPO编辑器显示它们。

除了这些区别，GPO是在整个企业内部署一致的WSH TrustPolicy设置的绝佳方式。

## 使用数字证书对脚本进行签名

获得代码签名证书并将其安装到你的计算机上后，你就可以开始对脚本进行签名了。通常，你会将证书安装到名为“个人证书”的存储区，这是默认设置。你需要知道证书的名称，该名称在证书安装后会出现在“Internet属性”对话框中。要对脚本进行签名，只需编写一个包含以下内容的VBScript脚本：

```
Set objSigner = CreateObject("Scripting.Signer")
objSigner.SignFile "MyScript.vbs", "MyCert"
```

> **你从哪里获得证书？**
> 有几种方法可以获取代码签名证书，你使用哪种在很大程度上取决于你的具体需求。请记住，任何预期运行你脚本的计算机都必须信任颁发你证书的CA，这将在你从哪里获取证书方面带来一些限制。例如，存在许多工具可以创建*自签名证书*。这些本质上是你自己颁发的证书，意味着你就是CA。然而，没有真正的方法配置计算机信任你作为CA，因此这些证书主要仅用于本地计算机上的测试目的。
> 如果你公司有内部CA，你可能可以从中获取代码签名证书。但是，你需要确保所有计算机都配置为信任该CA。商业CA也是一个选项——VeriSign、Thawte、CyberTrust等——因为大多数Windows计算机已经配置为信任主要的商业CA。商业CA相比内部CA有一个巨大的优势：可移植性。如果你打算在你的环境之外共享签名脚本，可能需要商业CA。这是因为你的内部CA不太可能被你自己网络之外的任何人信任。然而，与你合作的组织很可能信任你相同的商业CA。



# 第一部分：高级 Windows 脚本基础

当然，请将 *MyScript.vbs* 替换为您要签名的脚本的路径和文件名，将 *MyCert* 替换为您用于签名脚本的证书名称。这个简短的脚本可用于签署其他脚本。

已签名的脚本将在文件末尾包含一个特殊的签名块。

```
On Error Resume Next
Dim objSet

If WScript.arguments.count>0 Then
    strSrv=WScript.arguments(0)
Else
    strSrv="LOCALHOST"
End If

Set objSet=GetObject("winmgmts://" & strSrv).InstancesOf("win32_OperatingSystem")
If Err.Number Then
    strErrMsg= "Error connecting to WINMGMTS on " & UCase(strSrv) & vbCrLf
    strErrMsg= strErrMsg & "Error #" & err.number & " [0x" & _
        CStr(Hex(Err.Number)) &"]" & vbCrLf
    If Err.Description <> "" Then
        strErrMsg = strErrMsg & "Error description: " & _
            Err.Description & "." & vbCrLf
    End If
    Err.Clear
    WScript.echo strErrMsg
    WScript.quit
End If

For Each obj In objSet
    currtime=obj.LastBootUptime
Next

curryr=Left(currtime,4)
currmo=Mid(currtime,5,2)
currdy=Mid(currtime,7,2)
currtm=Mid(currtime,9,6)

LastBoot= currmo & "/" & currdy & "/" & curryr & " " & _
    FormatDateTime(Left(currtm,2)&":"&Mid(currtm,3,2)&":"&Right(currtm,2),3)
WScript.echo UCase(strSrv) & " Last Boot: " & LastBoot

Set objSet=Nothing
```

```
' SIG ' Begin signature block
' SIG ' MIID7AYJKoZIhvcNAQcCoIID3TCCA9kCAQExDjAMBggq
' SIG ' hkiG9w0CBQUAMGYGCisGAQQBgjCCAQGwDBWMDIGCisG
' SIG ' AQQBgjcCAR4wJAIBAQQQTvApFpkntU2P5azhDxfrqwIB
' SIG ' AAIBAAlBAAIBAIBADAgMAwGCCqGSIb3DQIFBQAEECJJ
' SIG ' dGPYS4Tpwl/NYibcd/mgggIVMIICETCCAXqgAwIBAgIQ
' SIG ' 3zX2vaM1cZVHykons8ASeTANBgkqhkiG9w0BAQQFADAW
' SIG ' MRQwEgYDVQQDEwtQZXJzb25hbCBJVDAeFw0wNTAxMDEw
' SIG ' NDAwMDBaFw0xMDEwNDEwMDBaMBYXFDASBgNVBAMT
' SIG ' C1BlcnNvbmFsIFElUMIGfMA0GCSqGSIb3DQEBAQUAA4GN
' SIG ' ADCBiQKb0QcSFHjIzN8pBimhQMrnIGCorr+F9uyk2r
' SIG ' n4eb/APZFFGSJ7dAVPwycgbNoys6uR4aWY94x0/f4aA6L
' SIG ' czuxoJbbgTo33/0/Moy2AAuUBk3hDfz11aQ9s9k7Coyu
' SIG ' oYT3di0y4mnm35e+RQ5xD1Nf4s2uLDU6gGFded+6aa7
' SIG ' 9BaMgW1DAQABo2AwXjATBgDNVSUEDDAKBggrBgEFBQ0D
' SIG ' AzBhBgNVHQEEQDA+gBAZXxwZaG1kHAAb42VQv5XmOgRw
' SIG ' FjEUMBIGa1UEAxMLUGVYC29UYWwgSVSCEN819r2jXGv
' SIG ' R8pKJ7PAE1nkwDQYJKoZIhvcNAQEEBQADgYEANIL/6LJ
' SIG ' euOk8a4NdbmVLSSS4tujkf4Chm6TXZzLEQc0CH8iVkaxP
' SIG ' l+9vShoJu16ngYWza2H5mT5OpclF1DmWw1EoZXv2qGiQ
' SIG ' +atTFE0SavB6lPmqjVkFYWmYhP1piL9Qwi4sGENVTDOn
' SIG ' JntdaQJv12tx0LFOA2RVVS37qAsFv18xgFBMIiBPQIB
' SIG ' ATAQMBYXFDASBgNVBAMTClBc1NnvbmFsIEUhDaFDNfa9
' SIG ' oyvx1UfKS1ezWBJ5MAWGCG5Tb3DQIFBQCgBDAqBgor
' SIG ' BgEEAYI3AgEMMQIwADAZBgkqhkiG9w0BCQcxBgEBAGC
' SIG ' BAGCNW1BBDACBgorBgEEAYI3AgELMQIwADAYKKwYBBAGC
' SIG ' NwIBFTAfBgkqhkiG9w0BCQQxFgQlpHci0Yobzitac
' SIG ' Rx2eRjANBgkqhkiG9w0BAQEFAASBgBvyluRHAFTNNN9j
' SIG ' UT3NQAjfAo9Md5kEcLsDiPXIkMtwIoucEJO/f2wZ4iYB
' SIG ' sx6KjU2Fu21ogH2ZhZQFPYtokpJsw3Q15oETYTL65YmI
' SIG ' U7stVz/pp4mIL4TbxlbLFwKGlXth+R+Fi8btGF0aUOsfB
' SIG ' pZwKmYUlKAW0d4HbFNQjMual
' SIG ' End signature block
```

请小心，不要修改此签名块（以行 "' SIG ' Begin signature *block*" 开头的行）或脚本的任何部分。任何修改都会使签名无效。

另一种签名脚本的方法是使用 SAPIEN PrimalScript（*www.primalscript.com*），一个商业脚本编辑器，据我们所知，它是唯一包含内置脚本签名的编辑器。如图 2-5 所示，您可以向 PrimalScript 提供您的证书名称（如果您的证书位于默认存储区，请将存储区名称留空），并且该工具可以在每次保存脚本时对它们进行签名，确保它们之后能够正确运行。您还可以配置 HKEY_LOCAL_USER 版本的 TrustPolicy 值，以便可以使用新签名的脚本测试 TrustPolicy 设置。

![配置 PrimalScript 以签名脚本](img/4fefd6988ba5d4a92a65127617ca24c2_70_0.png)

**图 2-5** 配置 PrimalScript 以签名脚本

## 使用软件限制策略

软件限制策略在 Windows XP 和 Windows Server 2003 中引入，作为一种更好地控制允许在 Windows 环境中运行软件的方法。SRP 通过组策略进行配置和部署，允许管理员定义一组异常来标识各种允许的软件，并指定一条默认安全规则，以阻止所有其他软件执行。SRP 使用数字签名来标识软件，这一点与 WSH TrustPolicy 非常相似，尽管 SRP 也可以使用多种其他方法。最初配置 SRP 可能会很耗时，因为您需要为环境中的每个授权软件识别并定义一个异常。但是，配置完成后，SRP 几乎可以消除恶意软件和其他未经授权的软件，从而在初始时间投入方面带来巨大的回报。

> **注意** 本书不全面讨论 SRP。但是，您可以在 Windows XP 或 Windows Server 2003 文档以及许多优秀的书籍中阅读更多关于 SRP 的信息，包括 *Windows Server 2003 Weekend Crash Course*（Don Jones, 2003, Wiley）和 *Introducing Microsoft Windows Server 2003*（Jerry Honeycutt, 2003, Microsoft）。

## 替代凭据

您会时不时地需要使用替代凭据运行脚本。也许您需要运行管理脚本，但并未使用管理凭据登录；或者您可能正在连接到远程服务，并需要为该服务指定适当的凭据。无论原因如何，脚本提供了多种使用替代凭据的方法。

> **注意** 请记住，安全性并不总是像替代凭据那样简单。例如，任何旨在修改用户配置文件部分内容的脚本通常必须在该用户的安全上下文中运行才能访问配置文件。第 6 章将更详细地介绍这种远程脚本。

### 使用 *RunAs* 命令

RunAs.exe 命令行工具可用于使用替代凭据执行脚本。例如，如果您组织实践最小权限（或访问）原则，并且您使用非管理账户登录计算机，这将非常有用。使用 *RunAs* 将允许您使用必要的管理凭据执行脚本。在命令提示符窗口中，键入 **Runas /?** 以查看该命令的正确语法。

### 使用计划任务凭据

对于必须定期运行的脚本，或者您希望在离开时安排运行的脚本，您可以使用 Windows 任务计划程序。任务计划程序允许您指定脚本在其下运行的替代凭据。

当您需要脚本在另一台计算机上使用替代凭据运行，但没有直接方法实现时，此技术通常可用作变通方法。使用 Schtasks.exe 命令行工具（包含在 Windows Server 2003 中）在远程计算机上创建任务。让任务使用替代凭据并执行任何必要的脚本。在命令提示符窗口中，键入 **Schtasks /create /?** 以查看在远程计算机上创建任务以及为任务指定凭据的正确语法。

### 使用 ADSI 替代凭据

Active Directory 服务接口脚本使用运行脚本的用户的安全上下文。在某些情况下，您可能希望为实际的 ADSI 连接提供替代凭据，例如，当运行脚本的帐户没有权限执行您需要脚本执行的任何任务时。清单 2-2 显示了一个使用替代凭据通过 LDAP 查询连接到 Active Directory 的示例。

```
清单 2-2 ADSI 替代凭据
Const ADS_SECURE_AUTHENTICATION = 1

'specify alternate credentials
strUserDN = "cn=Administrator,cn=Users,dc=company,dc=com"
strPassword = InputBox("Enter password for Administrator@company.com")

'Connect to the domain
Set objRoot = GetObject("LDAP:")
Set objDomain = _
    objRoot.OpenDSObject("LDAP://dc=company,dc=com", _
    strUserDN, strPassword, ADS_SECURE_AUTHENTICATION)
```

**在 CD 上** 您将在随书附带的 CD 上找到此脚本以及本章中列出的其他脚本。

此示例连接到域。当然，您可以指定任何合法的 LDAP 查询来返回任何对象，例如用户、组、组织单位、联系人等。另请注意，此技术适用于 ADSI WinNT 提供程序，该程序允许您为连接到 Microsoft Windows NT 域、独立计算机或域成员计算机指定替代凭据。



### 使用 WMI 替换凭据

在 WMI 查询中使用替换凭据与在 ADSI 查询中类似，如清单 2-3 所示。请注意，如果使用替换凭据，则不能使用 `winmgmts:` 单字符串技术连接到 WMI；必须使用此处所示的基于对象的连接方法。此外，Windows 不允许为本地计算机指定替换凭据。如果为本地连接指定替换凭据，将会出错。

**清单 2-3：WMI 替换凭据**

```
Const wbemImpersonationLevelImpersonate = 3

'specify credentials
strComputer = "server1"
strUser = "Administrator"
strPassword = InputBox("Enter password for " & strUser & _
    " on " & strComputer)

'connect to WMI
Set objSWbemLocator = _
    CreateObject("wbemScripting.SWbemLocator")
objSWbemLocator.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
Set objSWbemServices = _
    objSWbemLocator.ConnectServer(strComputer, _
    "root\cimv2", strUser, strPassword)
```

当然，随后你可以使用 `objSWbemServices` 对象的 `ExecQuery` 方法来执行 WMI 查询。

### 总结

在本章中，我们概述了常见的脚本安全问题。我们讨论了通过使用 WSH TrustPolicy 和 SRP 来使脚本更安全的方法。我们还向您展示了一些在替换凭据下运行脚本的技术，并提供了这些技术可能如何应用的思路。这些技术结合本书中的脚本技术，您将反复使用，因此请务必时常回顾本章，以刷新对这些安全选项的记忆。

# 第二部分
打包您的脚本

本部分包含：
- 第 3 章：Windows 脚本文件 ........................................ 57
- 第 4 章：Windows 脚本组件 .................................. 95
- 第 5 章：HTML 应用程序：带用户界面的脚本 ......... 125

# 第 3 章
Windows 脚本文件

**本章内容：**
- 定义 Windows 脚本文件 ........................................ 57
- 理解 XML ................................................... 58
- 创建脚本作业 .................................................. 63
- 包含其他脚本 ............................................... 63
- 添加资源 ..................................................... 63
- 创建示例和帮助文本 ...................................... 64
- 使用命名参数 ................................................ 65
- 查看运行中的 Windows 脚本文件 ............................... 67
- 将现有脚本转换为 WSF 工具 .......................... 72
- 创建和使用包装器 WSF ..................................... 83
- 总结 .............................................................. 94

VBScript 可以多种方式使用，包括作为 Windows 脚本文件。这些 XML 格式的脚本提供了许多好处和特性，我们将在本章中探讨。

标准的 VBScript 每个文件包含一个脚本，外加支持函数和子程序，因此如果您有许多相关脚本，则必须单独管理它们。如果您有一段经常使用的代码，您可能需要在脚本之间复制和粘贴。Windows 脚本文件使得管理脚本和重用代码更容易，它甚至可以使脚本编写更简单。

## 定义 Windows 脚本文件

Windows 脚本文件是一种标准的 Microsoft Visual Basic 脚本，已按照 XML 结构进行格式化。此 XML 结构定义了脚本的各个部分，并允许您*打包*脚本。每个 WSF 可以有任意数量的脚本，或称*作业*。它们甚至可以使用不同的脚本语言编写。例如，一个 WSF 可以包含一个用 VBScript 编写的脚本，该脚本调用另一个用 JScript 编写的脚本。

XML 格式起初可能看起来令人生畏，但当您获得一些经验后，您会看到所有部分是如何工作的。每个部分由一个*标签*定义，类似于 HTML 标签。标签定义了各种元素。每个元素都有一个开始标签和结束标签。例如，`<comment></comment>` 标签定义了注释元素。每个元素都有一个开始 `<comment>` 标签和一个结束 `</comment>` 标签。标签之间的文本称为*内容*。您可能见过带有许多标签和看似复杂格式的 WSF 脚本。不用担心，大部分 XML 格式不是必需的。您真正需要的只有 `<job>` 和 `<script>` 标签。

```
<job>
<script language="vbscript">
MsgBox "Hello world!"
</script>
</job>
```

由于这是一本高级脚本书，我们将更详细地探讨 WSF 脚本。

### 理解 XML

让我们按照您在 WSF 脚本中会使用的顺序来检查标签。请记住，每个标签必须用相应的结束标签关闭，结束标签包含斜杠 (/) 字符，例如 `<comment>` 和 `</comment>`。在下面的示例中，`<object>` 标签没有内容，因此您可以只使用斜杠和结束尖括号 (`/>`) 来关闭它。

```
<object id="objShell" progid="wScript.Shell"/>
```

WSF 脚本可以配置为使用严格的 XML 格式化。如果以 `<?XML version="1.0" ?>` 标签开头，则指定了脚本解析器应强制执行 XML 规则。（对于脚本目的，没有其他版本，只有版本 1。）强制执行严格的 XML 解析取决于个人偏好，以及在某种程度上，经验。严格执行将确保所有标签格式正确，并防止运行时错误。事实上，执行如此严格，以至于标签区分大小写。如果在 WSF 中输入 `<comment>This is a practice script.</Comment>`，则会在运行时收到关于标签不匹配的错误。

使用严格格式化时，还应将脚本代码放在 CDATA 标签之间，如下所示。

```
<script language="VBScript">
<![CDATA[
On Error Resume Next
MsgBox "<100> Perfect Score!"
]]>
</script>
```

如果未包含此标签，任何看起来像标签的内容，在此例中为文本 `<100>`，都将生成运行时错误。

让我们快速浏览一下这些标签。

#### *package* 标签

此标签是脚本文件中所有作业的包装器。每个文件应只有一个 *package* 标签。如果在脚本中指定了 `<?XML version="1.0" ?>`，则需要此标签，除非 WSF 中只有一个作业。

#### *comment* 标签

如果要添加关于脚本的一些元数据或其他注释，请使用 *comment* 标签。您在脚本开头使用此标签，在 *package* 标签之后。`<comment>` 和 `</comment>` 之间的任何内容都将被视为注释，不会以任何方式处理。标签内容在运行时永远不会显示给用户。查看注释的唯一方法是在文本或脚本编辑器中打开脚本。此外，不要使用此标签为脚本正文添加注释。请使用撇号，就像在任何其他 VBScript 中一样。

> **注意** 您也可以在 `<script>` 标签之外的任何位置使用 `<!--` 和 `-->` 标签来定义注释。

#### *job* 标签

*job* 标签用于将与特定任务相关的所有内容分组，例如 *description*、*example*、*named*、*object* 和 *script*。在单个 WSF 文件中可以有任意数量的 *jobs*，但如果有多个作业，必须设置标签的 *id* 属性。

```
<package>
<job id="Backup">
...
</job>
<job id="Restore">
...
</job>
</package>
```

要执行包含多个作业的 WSF 脚本中的特定作业，必须在 CScript 中使用 //Job 开关。例如，要在命令提示符下运行 ServerJobs.wsf 中的 *Backup* 作业，您需要输入 `cscript serverjobs.wsf //job:Backup`。如果定义了多个作业但未指定要运行哪个，则只有第一个作业会运行。作业不会在脚本中按顺序运行。

#### *runtime* 标签

使用 WSF 格式的好处之一是更丰富的运行时功能，例如命名参数和详细帮助信息。这些功能由包含在 *runtime* 标签集中的标签定义。

```
<runtime>
    <description>...</description>
    <named>...</named>
    <example>...</example>
</runtime>
```

#### *description* 标签

此标签类似于 *comment* 标签，不同之处在于，如果调用了 `wscript.ShowUsage` 方法，则内容将在运行时显示给用户。您可以使用此标签提供脚本的描述、版本信息、联系信息或任何其他您喜欢的内容。您不必提供示例或语法信息；这可以由其他标签处理。标签内容可以是任意长度，但将按照文件中的格式显示。

```
<description>
BigEasy.wsf
--------------------------------------------
This is the first line of my description.
This script will make your life very easy
and make your morning coffee.
</description>
```

如果描述较长，则需要测试脚本并相应调整行长度。

#### *example* 标签

如果调用了 `wscript.ShowUsage` 方法，则 *example* 标签的内容可用于向用户提供语法示例。

```
<example>
    cscript wsfdemo.wsf /dir:directorypath /file:filename
    cscript wsfdemo.wsf /dir:c:\temp /file:c:\results.txt
</example>
```

与 *comment* 标签一样，格式会保留，因此在刚刚显示的代码片段中，在示例命令显示之前会出现一个空行。您需要测试帮助消息以确保格式正确。



### *named* 标签

*named* 标签用于指定运行时参数。如果你的脚本需要一个服务器名称作为参数，你可以使用 *named* 标签来定义这个参数。

```
<named name="server" />
```

在运行时，用户会输入 `cscript myscript.wsf /server:File01` 来执行脚本，其中 `File01` 将作为服务器名称参数。我确信你已经注意到这里没有 `</named>` 结束标签。记住，如果标签没有正文内容，你可以使用单个标签元素，就像这里所做的。

> **注意** 你可能已经注意到，有时运行时参数被指定为 `/server`，就像刚刚展示的示例。其他时候，我们使用了像之前示例中的 `//job` 这样的参数。这是因为 CScript 使用双斜杠 (`//`) 作为其运行时参数的前缀，以便它能区分哪些参数适用于 CScript，哪些参数适用于你的脚本。以下命令是正确的，即使它看起来可能有点奇怪。

`cscript myscript.wsf //job:Backup /server:File01`

> **最佳实践** 顺便提一下，最佳实践是将所有 CScript 选项放在前面，然后才是你脚本的任何参数。

### *object* 标签

*object* 标签用于为你的脚本创建对象，而无需使用 `CreateObject` 方法。一个额外的好处是，当你使用 *object* 标签时，你可以访问对象的类型库。这很有帮助，因为完全访问类型库后，你就可以访问对象的所有常量，而无需定义它们。一个传统的脚本可能包含像这样的代码。

```
Dim objFSO
Const FORREADING=1
Const FORWRITING=2
Const FORAPPENDING=8

set objFSO=CreateObject("Scripting.FileSystemObject")
```

在 WSF 脚本中，这可以用一行代码替换。

```
<object id="objFSO" progid="Scripting.FileSystemObject" reference="TRUE"/>
```

你不需要调用 `CreateObject` 或定义任何常量。你仍然需要知道类型库中的常量名称，但你可以通过搜索互联网、研究相关脚本或使用对象浏览器工具来找到它。顺便说一下，你仍然需要显式地创建任何子对象。例如，基于刚刚展示的 object 标签，你仍然需要在脚本部分编写以下代码。

```
Set objFile=objFSO.OpenTextFile("MyLog.txt", FORAPPENDING)
```

你不能用 object 标签定义 objFile。你也不能将它用于你获取的对象，比如 winmgmts。

让我们更详细地看看 object 标签：

- 每个 object 标签都有一个 id 属性。此属性的值是你希望在脚本中使用的对象变量的名称。在这个例子中，它是 objFSO。
- 每个 object 标签必须有一个已定义的 progid 属性。此值与你在传统 CreateObject 语句中使用的值相同。在我们的例子中，它是 Scripting.FileSystemObject。如果你需要创建一个没有 progid 的对象，请使用对象的 guid 属性。
- reference 属性是可选的，但我们通常将其设置为 TRUE。设置为 TRUE 时，你可以完全访问对象的类型库。启用此属性不会带来性能损失。如果你不将其设置为 TRUE，你必须在脚本中显式定义任何类型库常量。

### script 标签

任何 WSF 文件的主要部分是脚本部分。你可以在每个作业中包含任意多个脚本。如果有多个脚本，它们将按顺序执行。大多数管理员为每个作业使用一个 script 标签，但如果你需要，也可以使用多个作业。

你需要为脚本定义的唯一属性是脚本语言，通常是 VBScript 或 JScript。这是通过 language 属性完成的。你可以在一个作业中使用多种脚本语言。

```
<job id="Main">
<script language="vbscript">
...
</script>
<script language="jscript">
...
</script>
</job>
```

## 创建脚本作业

大多数 WSF 文件包含一个作业和一个脚本元素，尽管多个作业包含多个脚本也没有问题。在刚刚展示的示例中，当执行 *Main* 作业时，脚本将按顺序运行。请记住，在第一个脚本中定义的变量对第二个脚本是可用的，但在第二个脚本中定义的变量对第一个脚本不可用。

要创建一个脚本作业，只需使用一组 *script* 标签，并将你的 VBScript 代码放在它们之间。请记住，如果你使用严格的 XML 解析，你需要将代码放在 `<![CDATA[` 和 `]]>` 标签之间。

```
<script language="vbscript">
<![CDATA[
'你的 vbscript 代码在这里
]]>
</script>
```

## 包含其他脚本

当你创建一个脚本作业时，你不仅限于 WSF 文件本身的代码。你可以创建一个 script 元素，通过 `src` 属性引用一个外部脚本。

```
<script language="VBScript" src="ScriptFunctionLibrary.vbs"/>
```

注意，这里没有结束 `</script>` 标签，因为没有代码主体。你可以根据需要包含任意数量的外部脚本。

```
<script language="VBScript" src="ScriptFunctionLibrary.vbs"/>
<script language="JScript" src="E:\scripts\MathFunctions.js"/>
<script language="VBScript" src="\\file01\scripts\Corporate.vbs"/>
```

如你所见，我们仍然需要定义引用脚本的语言。如果引用文件与 WSF 脚本在同一目录中，`src` 属性可以是脚本名称。如果不是，你必须指定外部脚本的完整路径，就像我们在示例中所做的那样。这是重用现有代码的绝佳方式。创建一个包含常用函数和子过程的 VBScript 文件，并将其包含在你的 WSF 文件中。然后你就可以调用外部文件中的任何函数或子过程，就像它是直接在 WSF 文件中编写的一样。如果你需要修改一个函数或子过程，你可以在一个文件中更改它，所有调用它的 WSF 脚本都会自动使用更新后的代码。

## 添加资源

*resource* 标签的正文用法与传统常量相同，但常量通常包含单个值，而 *resource* 标签可以包含你想要的任意多行信息。该标签的正文也对给定作业中的所有脚本可用。你可以使用此标签来存储脚本版本和联系信息。使用 *getResource* 方法来检索资源值。

```
<job>
<resource id="strAbout">
version 1.0
JDH Information Technology Solutions
http://www.jdhitsolutions.com
</resource>
...
<script language="VBScript">
'如果用户传递 version 作为第一个参数，则显示存储在 resource 标签中的版本信息
If InStr(Lcase(wscript.arguments.item(0)), "version") then
    MsgBox getResource("strAbout")
    wscript.quit
End if
'脚本继续执行
</script>
</job>
```

> **故障排除** *resource* ID 区分大小写，因此如果你的脚本失败，请比较 *resource* ID 与 *getResource* 方法的参数的大小写。

## 创建示例和帮助文本

如前所述，你可以使用 *example* 和 *description* 标签向用户显示有用信息。这些标签的正文在调用 *ShowUsage* 方法时显示。这在验证运行时语法时特别有用。如果用户没有指定正确数量的参数，你可以显示用法信息。假设你的脚本需要四个参数。你可能会使用像这样的代码。

```
If wscript.arguments.count<4 then
    wscript.echo "Missing Parameter"
    wscript.arguments.ShowUsage.
    wscript.quit
End if
```

许多命令行工具有一个 /? 开关来显示帮助信息。你可以在 WSF 文件中使用此开关，而无需添加任何代码。使用 /? 作为运行时参数将自动调用 *ShowUsage* 方法。

## 使用命名参数

WSF 脚本相对于传统脚本的一个优点是易于在运行时传递参数。当然，你可以使用传统脚本传递运行时参数，但处理这些值需要一些额外的编码，特别是当参数超过两三个时。在传统脚本中，运行时参数通常必须按特定顺序传递。例如，一个脚本可能期望第一个参数是服务器名称，第二个是用户名，第三个是密码。如果用户弄乱了这些顺序，脚本很可能会失败。在 WSF 文件中使用命名参数简化了这个过程，并提供了一些我们将在本章后面展示的好处。

`<named>` 标签放在 `<runtime></runtime>` 标签内部。这里有一个例子。

```
<named helpstring="要查询的服务器的 NetBIOS 名称"
 name="server" required="true" type="string"/>
```

你可以在 `named` 标签内设置几个属性。我们将逐一检查它们。

### name 属性

`name` 属性不言自明。在运行时，管理员会输入 `cscript CheckServer.wsf /server:DC01`。然后可以在脚本中使用 `server` 参数的值。也容易使用命名参数的值设置一个内部变量。

```
strServer=wscript.arguments.named("Server")
```

> **故障排除** 如果你需要传递的值包含空格，请将该值用引号括起来。例如，传递为 `/user:Jeff Hicks` 的参数将失败。正确的输入是 `/user: "Jeff Hicks"`。你不能将引号作为命名参数的一部分包含在内。

### helpstring 属性

你为 `helpstring` 属性输入的任何文本将在调用 `ShowUsage` 方法时显示。这提供了一种记录脚本参数的简便方法。这里是一组命名参数。

```
<named helpstring="要查询的服务器名称"
 name="Server" required="true" type="string"/>
<named helpstring="用于备用凭据的用户名"
 name="user" required="false" type="string"/>
<named helpstring="备用凭据密码"
 name="pass" required="false" type="string"/>
<named helpstring="将结果保存到文本文件 (True/False)。默认为 FALSE。" name="Log" required="false" type="boolean"/>
```



### *type* 属性

可选的 *type* 属性同样不言自明。你可以使用 *string*、*Boolean* 或 *simple* 类型的命名值。当你使用 *string* 类型时，参数以 /*命名:值* 的形式输入。*simple* 类型将仅传递命名参数，例如 */Trace*。然后你可以检查此参数是否存在。

```
<named name="Trace" helpstring: "Turn on tracing" type=simple/>
...
If wscript.arguments.named.exists("Trace") then
    wscript.echo "Turning on code tracing"
    'code tracing
End if
...
```

*Boolean* 类型是像加号 (+) 或减号 (-)，或者 true 或 false 这样的值。例如，检查以下参数。

```
<named name="Debug" helpstring: "Turn on debugging" type="Boolean"/>
```

在运行时，用户需要指定 **/debug:+** 或 **/debug:true** 以返回正值。

### *required* 属性

虽然听起来有些奇怪，*required* 是一个可选属性。与你的想法可能相反，将 *required* 设置为 *true* 并不会自动强制执行该要求，甚至不会在参数被省略时通知用户。如果脚本需要该参数，你必须添加代码来验证运行时参数。此属性仅用于显示目的。

让我们再次查看这组命名参数。

```
<named helpstring="The name of the server to query"
    name="Server" required="true" type="string"/>
<named helpstring="The username for alternate credentials"
    name="user" required="false" type="string"/>
<named helpstring="Alternate credentials password"
    name="pass" required="false" type="string"/>
<named helpstring="Save results to a text file (True/False). Default is FALSE." name="Log" required="false" type="boolean"/>
```

只有 *Server* 参数是必需的。当调用 *ShowUsage* 方法时，会显示一行用法信息，其中包含所有参数。可选参数用方括号表示，就像任何其他命令行实用程序一样。

```
usage: osinfo.wsf /Server:value [/user:value] [/pass:value] [/Log[+|-]]
```

## 实际查看 Windows 脚本文件

让我们结合本章开头的 *HelloWorld* 脚本的修改版本，将所有内容整合在一起。清单 3-1 展示了一个基本的 WSF 脚本。

```
清单 3-1 HelloUser.wsf
<?xml version="1.0" ?>
<package>
<comment>Demo WSF File</comment>
<job>
<runtime>
<description>
HelloUser.wsf
--------------------------
This is a sample WSF script

</description>
<example>
cscript hellouser.wsf /user:Username [/date]
</example>
<named name="user" helpstring="Your name" type="string" required="True"/>
<named name="date" helpstring="Use to display current date" type="simple" required="False"/>
</runtime>
<script language="vbscript">
<!--![CDATA[

if wscript.arguments.named.Exists("user") then
    strUser=wscript.arguments.named("user")
else
    wscript.echo "Missing Parameter!"
    wscript.arguments.ShowUsage
    wscript.quit
end if
if wscript.arguments.named.Exists("date") then strMsg=" It is now " & Now
wscript.echo "Hello " & strUser & "." & vbcrLF & strMsg

]]>
</script>
</job>
</package>
```

**随附光盘** 你可以在随附光盘上找到此脚本以及本章列出的其他脚本。

此脚本通过包含 `<?xml version="1.0" ?>` 标签使用了严格的 XML 解析，这要求我们包含 `<![CDATA[` 标签。我们定义了带有 `<description>` 和 `<example>` 标签的 `<runtime>` 标签。当调用 `ShowUsage` 方法时，用户将看到如下用法信息：

```
HelloUser.wsf
------------------------
This is a sample WSF script

Usage: hellouser.wsf /user:value [/date]

Options:

user : Your name
date : Use to display current date

cscript hellouser.wsf /user:Username [/date]
```

命名参数 *date* 是可选的，因此请注意其显示方式。脚本的主体非常简单。我们验证参数以确认已传递用户名；如果未传递，我们显示错误消息并调用 `ShowUsage` 方法。

```
if wscript.arguments.named.Exists("user") then
    strUser=wscript.arguments.named("user")
else
    wscript.echo "Missing Parameter!"
    wscript.arguments.ShowUsage
    wscript.quit
end if
```

我们使用类似的代码行来检查是否传递了 *date* 参数。由于这是一个简单类型的命名参数，我们只检查它的存在性。如果存在，我们设置一个变量。

```
if wscript.arguments.named.Exists("date") then strMsg=" It is now " & Now
```

我们进入脚本的主要部分，并向用户显示个性化的消息。文件最后以闭合标签结束。

```
]]>
</script>
</job>
</package>
```

值得指出的是，你不必自己弄清楚所有的 XML 标签。许多商业脚本编辑器都对 Windows 脚本文件提供了某种支持。其中一些，比如 XLNow 的 OnScript 和 Sapien 的 PrimalScript，包含可以生成 XML 格式脚本的向导。

图 3-1 显示了 PrimalScript WSF 向导的第一个屏幕，我们在其中指定脚本文件的位置。

![图 3-1 指定位置](img/4fefd6988ba5d4a92a65127617ca24c2_88_0.png)

**图 3-1** 指定位置

下一步如图 3-2 所示，是我们指定要添加的所有对象的地方。PrimalScript 提供了一些常见选择，但我们可以添加任何想要的对象。

![图 3-2 添加对象](img/4fefd6988ba5d4a92a65127617ca24c2_88_1.png)

**图 3-2** 添加对象

# 第二部分：打包你的脚本

图 3-3 显示了添加对外部类型库引用的位置。

![图 3-3 添加引用](img/4fefd6988ba5d4a92a65127617ca24c2_89_0.png)

**图 3-3** 添加引用

图 3-4 显示了添加其他脚本的位置。这与在 `script` 标签中使用 `src` 属性相同。

![图 3-4 添加脚本](img/4fefd6988ba5d4a92a65127617ca24c2_89_1.png)

**图 3-4** 添加脚本

图 3-5 是向导的最后一个屏幕。

![图 3-5 完成向导](img/4fefd6988ba5d4a92a65127617ca24c2_90_0.png)

**图 3-5** 完成向导

PrimalScript 将完全让你无需编写任何 XML 代码。编辑器在工作区中显示文件。右窗格用于 VBScript 代码，而左窗格（如图 3-6 所示）是 XML 标签的接口。

![图 3-6 PrimalScript 工作区](img/4fefd6988ba5d4a92a65127617ca24c2_90_1.png)

**图 3-6** PrimalScript 工作区

你可以通过 WSF 的属性来设置标签，例如 example、description 和 named。图 3-7 显示了清单 3-1 中 HelloUser.wsf 文件的命名参数的属性对话框。

![图 3-7 命名参数属性](img/4fefd6988ba5d4a92a65127617ca24c2_91_0.png)

**图 3-7** 命名参数属性

使用合适的编辑器，你可以创建 WSF 文件，而无需接触任何 XML 标签。

## 将现有脚本转换为 WSF 实用程序

希望到现在为止，你已经被使用 WSF 脚本的好处所吸引和激励。你的库中可能有许多脚本，如果它们是 WSF 文件，可能会更容易使用。现在我们将向你展示如何将现有脚本转换为 WSF 脚本。

清单 3-2 包含一个脚本，它查询用户指定计算机上的 WMI 并显示操作系统信息。我们不会详细介绍脚本细节，但我们会向你展示脚本的哪些部分可以转换为 WSF 元素。

```
清单 3-2 OSInfo.vbs
'OSINFO.VBS
'v3.0 July 2004
'USAGE: cscript|wscript OSINFO.VBS
'DESCRIPTION: Using WMI get operating system info for specified computer.
'Includes code to display uptime.
'NOTES: You must have admin rights on the queried system. You will be
'prompted for alternate credentials. But they can't be used on the local
'system.

On Error Resume Next

Dim objLocator,objService,objRet
Dim objShell,objNetwork

Const wbemFlagReturnImmediately=&h10
Const wbemFlagForwardOnly=&h20
```



# 第二部分：打包你的脚本

```
strTitle="操作系统信息"

strQuery="Select CSName,BootDevice,Caption,ServicePackMajorVersion," & _
"FreePhysicalMemory,FreeVirtualMemory,InstallDate,LastBootUpTime," & _
"Status,SystemDevice,TotalVirtualMemorySize,TotalVisibleMemorySize," & _
"Version,WindowsDirectory FROM win32_OperatingSystem"

Set objShell=CreateObject("wScript.Shell")
Set objNetwork=CreateObject("wscript.network")

strSrv=InputBox("您想查询哪台计算机？",strTitle,_
objNetwork.ComputerName)
If strSrv="" Then WScript.Quit

'如果不是本地系统，则提示输入备用凭据
If UCase(strSrv)<>UCase(objNetwork.ComputerName) Then
  strUser=InputBox("输入备用凭据账户，或者留空以使用当前凭据。",strTitle,"")
  '如果为strUser输入了内容，则提示输入密码

  If strUser<>"" Then
    strPass=GetIEPassword()
  End If
End If

'如果计算机可以访问，则获取信息
If TestPing(strSrv) Then
  Set objLocator = CreateObject("wbemScripting.SwbemLocator")
  If Err.Number <>0 Then
    strMsg= "创建定位器对象时发生错误 " & Err.Number & " [0x" & CStr(Hex(Err.Number)) & _
    "]。"

    If Err.Description <> "" Then
      strMsg=strMsg & vbCrLf & "错误描述: " & Err.Description & "。"
    End If
    objShell.Popup strMsg,10,strTitle,vbOKOnly+vbCritical
    WScript.Quit
  End If

  Set objService = objLocator.ConnectServer (strSrv,"root\cimv2",_
  strUser,strPass)
  ObjService.Security_.impersonationlevel = 3

  Set objRet=objService.ExecQuery(strQuery,"WQL",wbemFlagForwardOnly+_ wbemFlagReturnImmediately)
  If Err.Number<>0 Then
    strErrMsg= "在 " & UCase(strSrv) & " 上执行查询时出错" & vbCrLf
    strErrMsg= strErrMsg & "您可能没有有效的凭据。" & vbCrLf
    strErrMsg= strErrMsg & "错误编号 " & Err.Number & " [0x" & _
    CStr(Hex(Err.Number)) &"]" & vbCrLf
    If Err.Description <> "" Then
      strErrMsg = strErrMsg & "错误描述: " & Err.Description & "。"
    End If
    objShell.Popup strErrMsg,10,strTitle,vbOKOnly+vbExclamation
    WScript.Quit
  End If

  For Each item In objRet
    strInfo=item.CSName & vbCrLf
    strInfo=strInfo & item.Caption & " (" & item.Version & ")" & vbCrLf
    strInfo=strInfo & "Service Pack " & item.ServicePackMajorVersion & vbCrLf
    strInfo=strInfo & "Windows 目录: " & item.WindowsDirectory & vbCrLf
    strInfo=strInfo & "启动设备: " & item.BootDevice & vbCrLf
    strInfo=strInfo & "系统设备: " & item.SystemDevice & vbCrLf
    strInfo=strInfo & "物理内存: " & _
      FormatNumber(item.TotalVisibleMemorySize/1024,0) & " MB" & _
      " 总计/" & FormatNumber(item.FreePhysicalMemory/1024,0) & " MB 可用" & _
      " (" & _
      FormatPercent(item.FreePhysicalMemory/item.TotalVisibleMemorySize,0) & _
      ")" & vbCrLf

    strInfo=strInfo & "虚拟内存: " & _
      FormatNumber(item.TotalVirtualMemorySize/1024,0) & " MB" & _
      " 总计/" & FormatNumber(item.FreeVirtualMemory/1024,0) & " MB 可用" & _
      " (" & FormatPercent(item.FreeVirtualMemory/item.TotalVirtualMemorySize,0)_
      & ")" & vbCrLf

    strInfo=strInfo & "安装日期: " & ConvWMITime(item.InstallDate) & _
      vbCrLf
    strInfo=strInfo & "上次启动: " & ConvWMITime(item.LastBootUpTime) & _
      vbCrLf
    iDays=DateDiff("d",ConvWMITime(item.LastBootUpTime),Now)
    iHours=DateDiff("h",ConvWMITime(item.LastBootUpTime),Now)
    iMin=DateDiff("n",ConvWMITime(item.LastBootUpTime),Now)
    iSec=DateDiff("s",ConvWMITime(item.LastBootUpTime),Now)
    strUptime=iDays & " 天 " & (iHours Mod 24) & " 小时 " & _
      (iMin Mod 60) & " 分钟 " & (iSec Mod 60) & " 秒"
    strInfo=strInfo & "运行时间: " & strUptime & vbCrLf
    strInfo=strInfo & "状态: " & item.Status

  Next

  objShell.Popup strInfo,30,strTitle,vbOKOnly+vbInformation
  strMsg="您想将结果保存到文本文件 " & GetCurDir() & _
    UCase(strSrv) & "_OSInfo.txt 中吗？" & vbCrLf & _
    " 任何现有文件将被覆盖。"
  rc=MsgBox(strMsg,vbYesNo+vbQuestion,strTitle)
  If rc=vbYes Then
    Dim objFSO,objFile
    Set objFSO=CreateObject("Scripting.FileSystemObject")
    Set objFile=objFSO.CreateTextFile(UCase(strSrv) & "_OSInfo.txt",True)
    objFile.Write strInfo
    objFile.WriteBlankLines(1)
    objFile.WriteLine "记录于 " & Now
    objFile.Close
    objShell.Popup "结果已保存到 " & strSrv & _
      "_OSInfo.txt",10,strTitle,vbOKOnly+vbInformation
  End If

Else
    strMsg="无法 Ping 通 " & UCase(strSrv) & "。"
    objShell.Popup strMsg,10,strTitle,vbOKOnly+vbExclamation

End If

WScript.Quit
'主脚本结束
'//////////////////////////////////
' 转换 WMI 时间函数
'//////////////////////////////////
On Error Resume Next
Function ConvWMITime(wmiTime)
yr = Left(wmiTime,4)
mo = Mid(wmiTime,5,2)
dy = Mid(wmiTime,7,2)
tm = Mid(wmiTime,9,6)

ConvWMITime = mo&"/"&dy&"/"&yr & " " & FormatDateTime(Left(tm,2) & _
":" & Mid(tm,3,2) & ":" & Right(tm,2),3)

End Function

'//////////////////////////////////
'使用 WMI Ping 目标系统。需要本地安装 XP
' 或 Windows 2003
'//////////////////////////////////
Function TestPing(strName)
On Error Resume Next
'此函数需要 Windows XP 或 2003
Dim cPingResults, oPingResult
strPingQuery="SELECT * FROM win32_PingStatus WHERE Address = '" &_
    strName & "'"

Set cPingResults = GetObject("winmgmts://./root/cimv2").ExecQuery(strPingQuery)
For Each oPingResult In cPingResults
    If oPingResult.StatusCode = 0 Then
        TestPing = True
    Else
        TestPing = False
    End If
Next
End Function

'//////////////////////////////////
'使用 IE 密码提示框
'以安全地获取密码
'//////////////////////////////////
Function GetIEPassword()
Dim ie
On Error Resume Next
Set ie=WScript.CreateObject("internetexplorer.application")
ie.Width=400
ie.Height=150
ie.StatusBar=True
ie.MenuBar=False
ie.ToolBar=False

ie.Navigate ("About:blank")
ie.Visible=True
ie.Document.Title="密码提示"

strHTML=strHTML & "<Font color=RED><B>输入密码: <br>"
& "<input id=pass type=Password></B></Font> &nbsp"
strHTML=strHTML & "<input type=checkbox id=clicked size=1>"
& "完成后点击复选框"

ie.Document.Body.InnerHTML=strHTML

Do While ie.Busy<>False
  WScript.Sleep 100
Loop

'循环直到复选框被选中
  Do While ie.Document.All.clicked.Checked=False
    WScript.Sleep 250
  Loop

GetIEPassword=ie.Document.Body.All.pass.Value

ie.Quit
Set ie=Nothing
End Function

'///////////////////////////////////////////////
'获取脚本当前运行的路径
'///////////////////////////////////////////////
Function GetCurDir()
On Error Resume Next
  GetCurDir=Left(WScript.ScriptFullName,Len(WScript.ScriptFullName)_
  -Len(WScript.ScriptName))
End Function

'文件结束
```

要将此脚本转换为 WSF 脚本，首先创建你知道需要的标签。我们可以在进行过程中填充其余部分。

```
<?xml version="1.0" ?>
<package>
<job>
<script language="vbscript">
<![CDATA[
]]>
</script>
</job>
</package>
```

我们可以做的第一件事是获取脚本开头的注释部分，并将其用作 `<comment>` 标签的内容。

```
<package>
    <comment>
OSINFO.VBS
v3.0 July 2004
Jeffery Hicks
jhicks@jhditsolutions.com http://www.jhditsolutions.com
用法: cscript|wscript WMIOINFO.VBS
描述: 使用 WMI 获取操作系统信息。包含显示运行时间的代码。
注意: 您必须在被查询的系统上拥有管理员权限。您将被提示输入备用凭据。但它们不能在本地系统上使用。
    </comment>
```

接下来，我们可以将注释中的描述和注意事项放入 `<description>` 标签中。这对运行脚本的管理员将是很有用的信息。

```
<description>
使用 WMI 获取操作系统信息。
您必须在被查询的系统上拥有管理员权限。您将被提示输入备用凭据。但它们不能在本地系统上使用。
</description>
```

现有脚本提示用户输入服务器名称。我们可以轻松地将其设为一个命名参数。

```
<named helpstring="要查询的服务器名称"
      name="Server" required="true" type="string"/>
```

因为我们可以传递参数，所以也可以改进原始脚本。让我们请求备用凭据，但不将其设为必填。

```
<named helpstring="备用凭据的用户名"
name="user" required="false" type="string"/>
<named helpstring="备用凭据密码"
      name="pass" required="false" type="string"/>
```

最后，让我们再添加一个将结果保存到文本文件的参数。我们可以使用一个简单的命名参数，但让我们使用一个布尔参数以增加趣味性。

```
<named helpstring="将结果保存到文本文件 (True/False)。
默认为 FALSE。" name="Log" required="false" type="boolean"/>
```



### 使用 `<example>` 标签

原始脚本有一个简单的使用示例，但我们可以用 `<example>` 标签对其进行改进。

```
<example>
示例：
cscript wmiosinfo.wsf /server:FILE01
cscript wmiosinfo.wsf /server:FILE01 /user:Admin /pass:P@ssw0rd
cscript wmiosinfo.wsf /server:FILE01 /user:* /pass:*
cscript wmiosinfo.wsf /server:FILE01 /user:Admin /pass:P@ssw0rd /log:TRUE
cscript wmiosinfo.wsf /?

如果您为 /server、/user 或 /pass 使用 *，将会提示您输入
您无法为本地系统使用替代凭据。
同名的现有日志文件将被覆盖。
</example>
```

在描述和示例之间，用户将获得出色的帮助信息。

### 定义对象和库

现在让我们看看原始脚本中的对象，并思考我们在 WSF 脚本中可能需要什么。我们首先需要添加 *Scripting.FileSystemObject*，因为它不在原始文件中，并且我们将需要它来创建日志文件。其他对象可以通过使用 *object* 标签创建。我们使用与原始脚本中相同的 ID。

```
<object id="objFSO" progid="Scripting.FileSystemObject" reference="true"/>
<object id="objShell" progid="wScript.Shell"/>
<object id="objNetwork" progid="wScript.Network"/>
<object id="objLocator" progid="wbemScripting.SWbemLocator" _ reference="true"/>
```

在原始脚本中，我们必须定义作为 *WbemScripting.SWbemLocator* 对象一部分的常量。然而，在 WSF 脚本中，如果我们将 reference 属性设置为 TRUE，我们就可以完全访问该对象的类型库和所有常量。

原始脚本有几个函数，这些函数也用于其他脚本。我们可以通过构建脚本函数库来为未来的脚本做规划。通过包含此脚本，我们可以完全访问所有函数。

```
<script language="VBScript" src="ScriptFunctionLibrary.vbs"/>
```

### 转换脚本主体

现在我们可以简单地将原始脚本的脚本主体复制并粘贴到新文件中 `<![CDATA[` 之后。

因为我们使用了 *object* 标签，所以可以删除实例化这些对象的代码行。我们也可以删除与 *InputBox* 提示相关的代码行，因为该功能现在通过命名参数处理。

我们必须添加代码来验证参数。

```
if wScript.Arguments.Named.exists("Server") then
  strSrv=wscript.arguments.named("Server")
else
  wscript.echo "未指定服务器参数！"
  wscript.arguments.showusage
  wscript.quit
end if

if wScript.Arguments.Named.exists("user") then _ strUser=WScript.Arguments.Named("user")
if wScript.Arguments.Named.exists("pass") then _ strPass=WScript.Arguments.Named("pass")
if wScript.Arguments.Named.exists("log") then _ blnLog=WScript.Arguments.Named("Log")
```

其余的编辑是增强功能，例如使用替代凭据和记录日志。清单 3.3 显示了更新和转换后的脚本。

#### 清单 3-3 OSInfo.wsf

```
<?xml version="1.0" ?>
<package>
  <comment>
OSINFO.WSF
v3.0 2004年7月
Jeffery Hicks
jhicks@jhditsolutions.com http://www.jhditsolutions.com
用法：cscript|wscript WMIOSINFO.VBS
描述：使用 WMI 获取指定计算机的操作系统信息。
包含显示正常运行时间的代码。
注意：您必须在查询的系统上拥有管理员权限。将会提示您输入替代凭据。但它们不能用于本地系统。
  </comment>
  <job>
    <runtime>
    <description>
使用 WMI 获取操作系统信息。
您必须在查询的系统上拥有管理员权限。将会提示您输入替代凭据。但它们不能用于本地系统。
    </description>
      <named helpstring="要查询的服务器名称"
name="Server" required="true" type="string"/>
      <named helpstring="用于替代凭据的用户"
name="user" required="false" type="string"/>
      <named helpstring="替代凭据的密码。"
required="false" type="string"/>
      <named helpstring="将结果保存到文本文件（真/假）。默认为假。" name="Log" required="false"
type="boolean"/>
<example>
示例：
cscript wmiosinfo.wsf /server:FILE01
cscript wmiosinfo.wsf /server:FILE01 /user:Admin /pass:P@ssw0rd
cscript wmiosinfo.wsf /server:FILE01 /user:* /pass:*
cscript wmiosinfo.wsf /server:FILE01 /user:Admin /pass:P@ssw0rd /log:TRUE
cscript wmiosinfo.wsf /?

如果您为 /server、/user 或 /pass 使用 *，将会提示您输入
您无法为本地系统使用替代凭据。
同名的现有日志文件将被覆盖。
</example>
    </runtime>
    <object id="objFSO" progid="Scripting.FileSystemObject" _
      reference="true"/>
    <object id="objShell" progid="WScript.Shell"/>
    <object id="objNetwork" progid="WScript.Network"/>
    <object id="objLocator" progid="wbemScripting.SWbemLocator" _
      reference="true"/>
    <script language="VBScript" src="ScriptFunctionLibrary.vbs"/>
    <script language="VBScript">
<![CDATA[
On Error Resume Next

If WScript.Arguments.Count<1 Then
    wscript.Arguments.ShowUsage
    WScript.Quit
End If
strTitle="操作系统信息"
'verify user is running Windows XP
If InStr(GetOS,"XP Professional")=False Then
    objShell.Popup "此脚本需要 Windows XP Professional",10,_
    strTitle,vbOKOnly+vbExclamation
    WScript.Quit
End If

strQuery="Select CSName,BootDevice,Caption,ServicePackMajorVersion," & _
"FreePhysicalMemory,FreeVirtualMemory,InstallDate,LastBootUpTime," & _
"Status,SystemDevice,TotalVirtualMemorySize,TotalVisibleMemorySize," & _
"Version,WindowsDirectory FROM Win32_OperatingSystem"

if WScript.Arguments.Named.exists("Server") then
    strSrv=wscript.arguments.named("Server")
else
    wscript.echo "未指定服务器参数！"
    wscript.arguments.showusage
    wscript.quit
end if

if WScript.Arguments.Named.exists("user") then _ strUser=WScript.Arguments.Named("user")
if WScript.Arguments.Named.exists("pass") then _ strPass=WScript.Arguments.Named("pass")
if WScript.Arguments.Named.exists("log") then _ blnLog=WScript.Arguments.Named("Log")

If strSrv="*" Then
    strSrv=InputBox("您想要查询哪台计算机？",strTitle,_
    objNetwork.ComputerName)
    If strSrv="" Then WScript.Quit
End If

'如果 Server 是本地系统，则跳过获取替代凭据
If UCase(strSrv)<>UCase(objNetwork.Computername) Then
    If strUSer="*" Then
        strUser=InputBox("输入替代凭据，或留空以使用当前凭据。",strTitle,"")
    End If

If strPass="*" Then
    strPass=GetIEpassword()
End If
End If

'如果本地系统，则将任何替代凭据设置为空
If UCase(strSrv)=UCase(objNetwork.ComputerName) Then
    strUser=""
    strPass=""
End If

'如果计算机可访问，则获取信息
If TestPing(strSrv) Then
    Set objService = objLocator.ConnectServer (strSrv,"root\cimv2",_
        strUser,strPass)
    objService.Security_.impersonationlevel = 3

    Set objRet=objService.ExecQuery(strQuery,"WQL",wbemForwardOnly+_
        wbemFlagReturnImmediately)
    If Err.Number<>0 Then
        strErrMsg= "在 " & UCase(strSrv) & " 上执行查询时出错" & vbCrLf
        strErrMsg= strErrMsg & "您可能没有有效的凭据。" & vbCrLf
        strErrMsg= strErrMsg & "错误 #" & err.number & " [0x" &_
            CStr(Hex(Err.Number)) &"]" & vbCrLf
        If Err.Description <> "" Then
            strErrMsg = strErrMsg & "错误描述：" & Err.Description & "。"
        End If
        objShell.Popup strErrMsg,10,strTitle,vbOKOnly+vbExclamation
        wscript.quit
    End If

    For each item In objRet
        strInfo=item.CSNAME & vbCrLf
        strInfo=strInfo & item.Caption & " (" & item.version & ")" & vbCrLf
        strInfo=strInfo & "服务包 " & item.ServicePackMajorVersion & vbCrLf
        strInfo=strInfo & "Windows 目录：" & item.WindowsDirectory & vbCrLf
        strInfo=strInfo & "启动设备：" & item.BootDevice & vbCrLf
        strInfo=strInfo & "系统设备：" & item.SystemDevice & vbCrLf
        strInfo=strInfo & "物理内存：" &_
            FormatNumber(item.TotalvisibleMemorySize/1024,0) & "MB" & _
            " 总计/" & FormatNumber(item.FreePhysicalMemory/1024,0) & "MB 可用" & _
            " (" &_
            FormatPercent(item.FreePhysicalMemory/item.TotalvisibleMemorySize,0) &_
            ")" & vbCrLf

        strInfo=strInfo & "虚拟内存：" & _
            FormatNumber(item.TotalVirtualMemorySize/1024,0) & "MB" & _
            " 总计/" & FormatNumber(item.FreeVirtualMemory/1024,0) & "MB 可用" & _
            " (" &FormatPercent(item.FreeVirtualMemory/item.TotalVirtualMemorySize,0)_
            & ")" & vbCrLf

        strInfo=strInfo & "安装日期：" & ConvWMITime(item.InstallDate) &_
            vbCrLf
        strInfo=strInfo & "最后启动：" & ConvWMITime(item.LastBootUpTime) &_
```



# 第二部分：打包你的脚本

```vb
vbCrLf
iDays=DateDiff("d",ConvWMITime(item.LastBootUpTime),Now)
iHours=DateDiff("h",ConvWMITime(item.LastBootUpTime),Now)
iMin=DateDiff("n",ConvWMITime(item.LastBootUpTime),Now)
iSec=DateDiff("s",ConvWMITime(item.LastBootUpTime),Now)
strUptime=iDays & " days " & (iHours Mod 24) & " hours " & _
(iMin Mod 60) & " minutes " & (iSec Mod 60) & " seconds"
strInfo=strInfo & "Uptime: " & strUptime & vbCrLf
strInfo=strInfo & "Status: " & item.Status

Next

objShell.Popup strInfo,30,strTitle,vbOKOnly+vbInformation

If blnLog Then
    Set objFile=objFSO.CreateTextFile(UCase(strSrv) & "_OSInfo.txt",True)
    objFile.Write strInfo
    objFile.WriteBlankLines(1)
    objFile.WriteLine "recorded " & Now
    objFile.Close
    objShell.Popup "Results saved to " & strSrv & _
    "_OSInfo.txt",10,strTitle,vbOKOnly+vbInformation
End If

Else
strMsg="Failed to ping " & UCase(strSrv) & "."
objShell.Popup strMsg,10,strTitle,vbOKOnly+vbExclamation

End If

wscript.quit
'主脚本结束
```

如你所见，只需稍加修改，你就可以将一个现有的脚本转变为一个功能齐全的命令行工具。但如果你更喜欢图形界面呢？

在新的 WSF 脚本中，我们添加了代码，如果传递的参数值是一个通配符（*），则会提示用户输入密码。我们这样做主要是为了使用密码对话框来提高安全性，但也可以使用此技术来显示图形界面。但是，如果用户必须先输入一个通配符字符，那么他们如何获得提示呢？我们使用另一个脚本。

清单 3-4 是一个常规的 VBScript。这个脚本的唯一功能是使用 WScript 启动我们新的 WSF 脚本，并传递命名参数。

#### 清单 3-4 RunOSInfo.vbs
```vb
Dim objShell

strCmd="wscript"
strScript="listing3-3.wsf"
strParams="/server:* /username:* /password:* /log:True"

Set objShell=CreateObject("WScript.Shell")
objShell.Run strCmd & " " & strScript & " " & strParams,1,False

wScript.Quit
```

当管理员双击此脚本时，WSF 脚本会被调用，并使用通配符作为参数值。WSF 脚本会按照其代码执行，并提示用户输入所有必要的值。

```vb
If strSrv="*" Then
    strSrv=InputBox("What computer do you want to query?",strTitle,_
    objNetwork.ComputerName)
    If strSrv="" Then wScript.Quit
End If

'如果服务器是本地系统，则跳过获取备用凭据
If UCase(strSrv)<>UCase(objNetwork.Computername) Then
    If strUSer="*" Then
        strUSer=InputBox("Enter alternate credentials, or leave " &_
        "blank to use the current credentials.",strTitle,"")
    End If

    If strPass="*" Then
        strPass=GetIEpassword()
    End If
End If
```

我们两全其美。我们可以使用命令行工具，或者我们可以将该工具包装在另一个脚本中，并使用图形实用程序。

### 创建和使用包装器 WSF

现在让我们看看如何使用 WSF 文件作为包装器脚本。假设你有一些代码，你想针对一组计算机运行。你可能有一个包含计算机名称的文本文件，或者你可能希望查询一个 Active Directory 组织单元。包装器脚本负责处理获取计算机名称的细节。你所要做的就是插入将针对每台远程机器执行的代码。

清单 3-5 中的脚本使用命名参数来指示是从文本文件、组织单元读取计算机名称，还是使用单个计算机名称。以下是该部分代码。

```xml
<named helpstring="Text file to pull computer names from" name="list" required="false" type="string"/>
<named helpstring="OU to pull computer names from" name="container" required="false" type="string"/>
<named helpstring="Run command against single specified computer" name="computer" required="false" type="string"/>
```

包装器脚本还具有用于详细信息、递归、ping 远程计算机以验证可用性和日志记录的可选命名参数。

```xml
<named helpstring="use for verbose output" name="verbose" required="false" type="simple"/>
<named helpstring="Use with /container to include sub-OUs" name="recurse" required="false" type="simple"/>
<named helpstring="File to log names which can't be reached" name="log" required="false" type="string"/>
<named helpstring="Reduce timeout wait by pinging before connecting" name="ping" required="false" type="simple"/>
```

#### 清单 3-5 MultiComputer Wrapper.wsf
```xml
<?xml version="1.0" ?>
<package>
  <job id="MultiComputer" prompt="no">
    <?job error="false" debug="false" ?>
    <runtime>
      <description>
ScriptingAnswers.com - Windows 管理员在此实现自动化
----------------------------------------------------------------------
此命令所基于的 Shell 脚本由 Don Jones 为 ScriptingAnswers.com 编写，
并提供以下命令行参数：

仅使用以下参数之一：
    /list:filename   : 包含每行一个计算机名称的文本文件
    :容器:ouname : 包含计算机账户的 OU 名称
    /computer:name   : 针对单个指定的计算机运行命令

可选地，使用以下一个或多个参数：
    /verbose         : 显示详细的状态消息
    /recurse         : 与 /container 一起使用以包含子 OU
    /log:filename    : 将无法访问的计算机名称写入指定文件
    /ping            : 在连接前预测试每台计算机的连接性
注意 /ping 参数仅在 Windows XP 及更高版本上可用。
----------------------------------------------------------------------
此命令添加了以下（如果有）命令行参数：
   （无）
----------------------------------------------------------------------
概述（更详细的描述见上文）：
      </description>
      <named helpstring="Text file to pull computer names from" name="list" required="false" type="string"/>
      <named helpstring="OU to pull computer names from" name="container" _
required="false" type="string"/>
      <named helpstring="Use for verbose output" name="verbose" _
required="false" type="simple"/>
      <named helpstring="Use with /container to include sub-OUs" _
name="recurse" required="false" type="simple"/>
      <named helpstring="File to log names which can't be reached" _
name="log" required="false" type="string"/>
      <named helpstring="Reduce timeout wait by pinging before connecting" _
name="ping" required="false" type="simple"/>
      <named helpstring="Run command against single specified computer" _
name="computer" required="false" type="string"/>
    </runtime>
    <object id="fso" progid="Scripting.FileSystemObject"/>
    <script id="MultiComputer" language="VBScript">
'<![CDATA[
'---------------------------------------------------------------
' ScriptingAnswers.com Gold          www.scriptinganswers.com
'            超级多计算机包装器脚本
'                   作者：Don Jones
'---------------------------------------------------------------
'
' 概述
' --------
' 接受来自文件的计算机名称列表，或指定 AD 组织单元中的
' 计算机名称，或单个计算机名称。针对每台计算机执行你的代码。
' 包括将数据记录到文件、查询 WMI 和查询 ADSI 的函数。
' 还有在尝试连接前 ping 计算机的选项，以加快超时速度。
' 设计用于从命令行运行；使用 /? 参数运行命令以获取
' 命令行参数帮助。
'
' 支持
' -------
' 仅在 www.scriptinganswers.com 的论坛中在线提供对此脚本的支持。
' 此脚本并非设计为无需修改即可运行；它是一个“外壳”或“模板”脚本。
'
' 免责声明
' --------
' 此脚本按“原样”提供，不附带任何明示或暗示的保证。
' 作者和 ScriptingAnswers.com 进一步否认所有暗示的保证，
' 包括但不限于对适销性或适用于特定目的的任何暗示保证。
' 因使用或执行此脚本而产生的全部风险由你（此脚本的用户）
' 承担。在任何情况下，作者、ScriptingAnswers.com、Don Jones
' 或 BrainCore Nevada, Inc. 均不对因使用或无法使用此脚本
' 而引起的任何损害（包括但不限于业务利润损失、业务中断、
' 业务信息损失或其他金钱损失）承担责任，即使上述各方已被告
' 知存在此类损害的可能性。
```



# 第二部分：打包你的脚本

```
' 
' 版权所有
' ---------
' 此脚本由上述作者版权所有，
' 并由 ScriptingAnswers.com 在许可下分发。
' 你可以在自己的环境中使用此脚本，
' 并使用它来创建衍生脚本。你可以分发
' 任何衍生脚本，前提是此文本块保持
' 完整且未修改。你不得分发此脚本
' 原样（例如，不作为衍生脚本的一部分）或包含
' 对此脚本中包含的代码进行任何修改。
' 换句话说，你可以将你的代码添加到这个包装
' 脚本中，但你不得删除或修改任何
' 随此外包装脚本发布的代码。你不得
' 分发此包装脚本原样，但你可以分发任何
' 使用此包装脚本创建的脚本。
'
'----------------------------------------------------------------------

'确保我们是从 CScript 运行，而不是 WScript
If LCase(Right(WScript.FullName,11)) <> "cscript.exe" Then
    If MsgBox("This script is designed to work with CScript, but you are" _
    "running it under WScript. " & _
    "This script may produce a large number of dialog boxes when running" _
    "under WScript, which you may find to be inefficient. Do you want to" _
    "continue anyway?",4+256+32,"Script host warning") = 7 Then
        WScript.Echo "Tip: Run \"Cscript //h:cscript\"" from a command-line to" _
        "make CScript the default scripting host."
        WScript.Quit
    End If
End If

'计算参数
Dim iArgs
If WScript.Arguments.Named.exists("computer") Then iArgs = iArgs + 1
If WScript.Arguments.Named.exists("container") Then iArgs = iArgs + 1
If WScript.Arguments.Named.exists("list") Then iArgs = iArgs + 1
If iArgs <> 1 Then
    WScript.Echo "Must specify either /computer, /container, or /list arguments."
    WScript.Echo "May not specify more than one of these arguments."
    WScript.Echo "Run command again with /? argument for assistance."
    WScript.Quit
End If

'如果请求了 ping，确保我们在 XP 或更高版本上
Dim bPingAvailable, oLocalWMI, cwindows, owindows
bPingAvailable = False
Set oLocalWMI = GetObject("winmgmts:\\.\root\cimv2")
Set cwindows = oLocalWMI.ExecQuery("Select BuildNumber from " &_
"win32_OperatingSystem",,48)
For Each owindows In cwindows
    If owindows.BuildNumber >= 2600 Then
        bPingAvailable = True
    End If
Next

'是否请求了 ping？
If WScript.Arguments.Named.Exists("ping") Then
  If bPingAvailable Then
    Verbose "will attempt to ping all connections to improve performance"
  Else
    WScript.Echo "*** /ping not supported prior to windows XP"
  End If
End If

'指定了 /list, /computer, 或 /container：
Dim sName
If WScript.Arguments.Named("list") <> "" Then
  '指定了列表 - 从文件中读取名称
  Dim oFSO, oTS
  Verbose "Reading names from file " & WScript.Arguments.Named("list")
  Set oFSO = WScript.CreateObject("Scripting.FileSystemObject")
  On Error Resume Next
  Set oTS = oFSO.OpenTextFile(WScript.Arguments.Named("list"))
  If Err <> 0 Then
    WScript.Echo "Error opening " & WScript.Arguments.Named("list")
    WScript.Echo Err.Description
    WScript.Quit
  End If
  Do Until oTS.AtEndOfStream
    sName = oTS.ReadLine
    TakeAction sName
  Loop
  oTS.Close

Elseif WScript.Arguments.Named("container") <> "" Then
  '指定了容器 - 从 AD 中读取名称
  Dim oObject, oRoot, oChild
  Verbose "Reading names from AD container " & _
    WScript.Arguments.Named("container")
  On Error Resume Next
  Set oRoot = GetObject("LDAP://rootDSE")
  If Err <> 0 Then
    WScript.Echo "Error connecting to default Active Directory domain"
    WScript.Echo Err.Description
    WScript.Quit
  End If
  Set oObject = GetObject("LDAP://ou=" & WScript.Arguments.Named("container") & "," & oRoot.Get("defaultNamingContext"))
  If Err <> 0 Then
    WScript.Echo "Error opening organizational unit " & _
      WScript.Arguments.Named("container")
    WScript.Echo Err.Description
    WScript.Quit
  End If
  WorkwithOU oObject

Elseif WScript.Arguments.Named("computer") <> "" Then
  '指定了单台计算机
  Verbose "Running command against " & WScript.Arguments.Named("computer")
  TakeAction WScript.Arguments.Named("computer")

End If

'显示输出，以便用户知道脚本已完成
WScript.Echo "Command completed."

' ------------------------------------------------------------------------
' 子过程 WorkwithOU
'
' 遍历组织单位中的子对象；如果提供了 /recurse 参数，
' 则递归调用自身以处理子组织单位
' ------------------------------------------------------------------------
Sub WorkwithOU(oObject)
  For Each oChild In oObject
    Select Case oChild.Class
      Case "computer"
        TakeAction Right(oChild.Name,Len(oChild.Name)-3)
      Case "user"
      Case "organizationalUnit"
        If WScript.Arguments.Named.Exists("recurse") Then
          '递归处理子组织单位
          Verbose "Working In " & oChild.Name
          WorkwithOU oChild
        End If
    End Select
  Next
End Sub

' ------------------------------------------------------------------------
' 子过程 TakeAction
'
' 建立连接并执行特定于命令的代码
' ------------------------------------------------------------------------
Sub TakeAction(sName)

  '详细输出？
  Verbose "Connecting to " & sName

  '连接前 ping？
  If WScript.Arguments.Named.Exists("ping") Then
    If Not TestPing(sName,bPingAvailable) Then
      LogBadConnect(sName)
      Exit Sub
    End If
  End If

' ------------------------------------------------------------------------
'         说明与参考
' ------------------------------------------------------------------------
' sName 包含要处理的当前名称
'
' 如果提供了 /ping 参数，则此时该名称
' 已被验证为可达。
'
' 否则，需要捕获连接错误，
' 并在必要时调用 LogBadConnect(sName) 以记录
' 连接失败。
'
' 要输出状态消息：
'   Verbose "消息"
'
' 要追加到文本文件：
'   LogFile "文件名","文本",False
'
' 要写入新的文本文件，覆盖之前的文件：
'   LogFile "文件名","文本",True
'
' 要查询 WMI（简单查询）：参见示例 1。
' 要查询 ADSI（使用 LDAP 或 WinNT）：参见示例 2。

'-------------------------------------------
'              示例 1
'-------------------------------------------
' 示例 WMI 查询，将提示输入密码：
' 显示指定计算机的操作系统版本号
' 取消注释以下行以尝试。
'
  Dim obj, oItem
  Set obj = QueryWMI(sName,"root/cimv2","Select * from" & _
    " win32_operatingsystem","administrator","")
  If IsObject(obj) Then
    For Each oItem In obj
      WScript.Echo sName & " is at windows build " & oItem.BuildNumber
    Next
  Else
    WScript.Echo "Couldn't get build info for " & sName
  End If

'-------------------------------------------
'              示例 2
'-------------------------------------------
' 示例 ADSI 查询
' 显示指定计算机列表中本地管理员账户的密码
' 使用期限。取消注释以下行以
' 尝试。有关更多详细信息，请参阅下面的函数描述。
'
  Dim obj
  Set obj = QueryADSI(sName,"WinNT://%computer%/Administrator,user","%computer%")
  If IsObject(obj) Then
    WScript.Echo "Administrator password on " & sName & _
      " is " & obj.Get("PasswordAge") & " days old."
  Else
    WScript.Echo "Couldn't get password age from " & sName
  End If

'##################################################
'#        特定于命令的代码放在这里        #
'#-----------------------------------------------#
'#                                              #
'   "你的代码放在这里" - 参见上面的示例
'#                                              #
'#----------------------------------------------#
'#          特定于命令的代码结束          #
'##################################################

End Sub

' ---------------------------------------------------------------
' 子过程 LogBadConnect
'
' 将连接失败记录到日志文件中。如果文件已存在，则追加。
' ---------------------------------------------------------------
Sub LogBadConnect(sName)
If WScript.Arguments.Named.Exists("log") Then
    Dim oLogFSO, oLogFile
    Set oLogFSO = WScript.CreateObject("Scripting.FileSystemObject")
    On Error Resume Next
    Set oLogFile = oLogFSO.OpenTextFile(WScript.Arguments.Named("log"),8,True)
    If Err <> 0 Then
        WScript.Echo " *** Error opening log file to log an unreachable computer"
        WScript.Echo " " & Err.Description
    Else
        oLogFile.WriteLine sName
        oLogFile.Close
        Verbose " Logging " & sName & " as unreachable"
    End If
End If
End Sub

' ---------------------------------------------------------------
' 函数 TestPing
'
' 测试到给定名称或地址的连接性；返回 True 或 False
' ---------------------------------------------------------------
Function TestPing(sName,bPingAvailable)
If Not bPingAvailable Then
    WScript.Echo " Ping functionality not available prior to Windows XP"
    Exit Function
End If
Dim cPingResults, oPingResult
Verbose " Pinging " & sName
Set cPingResults = GetObject("winmgmts://./root/cimv2").ExecQuery_
    ("SELECT * FROM Win32_PingStatus WHERE Address = '" & sName & "'")
    For Each oPingResult In cPingResults
        If oPingResult.StatusCode = 0 Then
            TestPing = True
            Verbose " Success"
        Else
            TestPing = False
            Verbose "  *** FAILED"
        End If
```

90  第二部分： 打包你的脚本

下一个
结束函数

' -----------------------------------------------------------------------
' 过程 Verbose
'
' 若提供了 /verbose 参数，则输出状态消息
' -----------------------------------------------------------------------
Sub Verbose(sMessage)
    If WScript.Arguments.Named.Exists("verbose") Then
        WScript.Echo sMessage
    End If
End Sub

' -----------------------------------------------------------------------
' 过程 LogFile
'
' 将指定文本输出到指定的日志文件。设置 Overwrite=True 可覆盖
' 现有文件，否则文件将被追加。
' 每次调用此过程都会重新访问文件，因此除非在脚本开头，
' 否则不要设置 Overwrite=True。
' -----------------------------------------------------------------------
Sub LogFile(sFile, sText, bOverwrite)
    Dim oFSOOut, oTSOut, iFlag
    If bOverwrite Then
        iFlag = 2
    Else
        iFlag = 8
    End If
    Set oFSOOut = WScript.CreateObject("Scripting.FileSystemObject")
    On Error Resume Next
    Set oTSOut = oFSOOut.OpenTextFile(sFile, iFlag, True)
    If Err <> 0 Then
        WScript.Echo "*** 记录日志到 " & sFile & " 时出错"
        WScript.Echo "    " & Err.Description
    Else
        oTSOut.WriteLine sText
        oTSOut.Close
    End If
End Sub

' -----------------------------------------------------------------------
' 函数 QueryWMI
'
' 执行 WMI 查询并返回结果。用户和密码可以
' 作为空字符串传递以使用当前凭据；仅传递一个空白用户名
' 将提示输入密码
' -----------------------------------------------------------------------
Function QueryWMI(sName, sNamespace, sQuery, sUser, sPassword)
    Dim oWMILocator, oWMIService, cInstances
    On Error Resume Next

    '创建定位器
    Set oWMILocator = CreateObject("WbemScripting.SWbemLocator")

    If sUser = "" Then

        '未指定用户 - 使用当前凭据连接
        Set oWMIService = oWMILocator.ConnectServer(sName, sNamespace)
        If Err <> 0 Then
            WScript.Echo "*** 连接到 " & sName & " 上的 WMI 时出错"
            WScript.Echo "    " & Err.Description
            Set QueryWMI = Nothing
            Exit Function
        End If

    Else

        '指定了用户
        If sUser <> "" And sPassword = "" Then

            '未指定密码 - 需要提示输入密码
            If LCase(Right(WScript.FullName, 11)) = "cscript.exe" Then

                'cscript - 尝试使用 ScriptPW.Password 对象
                Dim oPassword
                Set oPassword = WScript.CreateObject("ScriptPW.Password")
                If Err <> 0 Then
                    WScript.Echo " *** 无法在 Windows XP 之前版本提示输入密码"
                    WScript.Echo "   要么系统上没有 ScriptPW.Password 对象，要么"
                    WScript.Echo "    " & Err.Description
                    WScript.Echo "    将尝试使用空白密码继续"
                Else
                    WScript.Echo "请输入用户 '" & _
                    sUser & "' 在 '" & sName & "' 上的密码。"
                    sPassword = oPassword.GetPassword()
                End If
            Else

                'wscript - 使用 InputBox() 提示
                sPassword = InputBox("请输入用户 '" & _
                sUser & "' 在 '" & sName & "' 上的密码。" & vbCrLf & vbCrLf & _
                "警告：密码将显示在屏幕上。使用 CScript 运行命令以避免此情况。")
            End If
        End If

        '尝试使用提供的凭据连接
        Set oWMIService = _
        oWMILocator.ConnectServer(sName, sNamespace, sUser, sPassword)
        If Err <> 0 Then
            WScript.Echo " *** 连接到 " & sName & " 上的 WMI 时出错"
            WScript.Echo "    " & Err.Description
            Set QueryWMI = Nothing
            Exit Function
        End If
    End If

    '执行查询
    If sQuery <> "" Then
        Set cInstances = oWMIService.ExecQuery(sQuery, , 48)
        If Err <> 0 Then
            WScript.Echo "*** 执行查询时出错"
            WScript.Echo " " & sQuery
            WScript.Echo " " & Err.Description
            Set QueryWMI = Nothing
            Exit Function
        Else
            Set QueryWMI = cInstances
        End If
    Else
        Set QueryWMI = oWMIService
    End If

End Function

' -------------------------------------------------------------------
' 函数 QueryADSI
'
' 执行 ADSI 查询。期望变量 sQuery 包含一个以提供程序 LDAP:// 或
' WinNT:// 开头的完整查询。查询字符串可以包含计算机名称的占位符，
' 例如 "%computer%"。在变量 sPlaceholder 中包含该占位符，
' 以便将其替换为当前计算机名称。例如，
'     sQuery = "WinNT://%computer%/Administrator,user"
'     sPlaceholder = "%computer%"
' 将查询脚本定位的每台计算机，并查询其本地管理员用户账户。
' -------------------------------------------------------------------
Function QueryADSI(sName, sQuery, sPlaceholder)

    Dim oObject
    sQuery = Replace(sQuery, sPlaceholder, sName)
    On Error Resume Next
    Verbose " 正在查询 " & sQuery
    Set oObject = GetObject(sQuery)
    If Err <> 0 Then
        WScript.Echo " *** 执行 ADSI 查询时出错"
        WScript.Echo " " & sQuery
        WScript.Echo " " & Err.Description
        Set QueryADSI = Nothing
    Else
        Set QueryADSI = oObject
    End If

End Function

第二部分：打包你的脚本

脚本处理适当列表中的每台计算机，并设置一个包含当前计算机名称的变量。你在 TakeAction 子例程中插入你的代码。包装器脚本包含几个示例。

    ' WMI 查询示例，将提示输入密码：
    ' 显示指定计算机的操作系统内部版本号
    ' 取消下面几行的注释以尝试它。
    '
    ' Dim obj, oItem
    ' Set obj = QueryWMI(sName,"root/cimv2","select * from " & _
    ' "win32_operatingsystem","administrator","")
    ' If IsObject(obj) Then
    '     For Each oItem In obj
    '         WScript.Echo sName & " 的 Windows 内部版本号为 " & oItem.BuildNumber
    '     Next
    ' Else
    '     WScript.Echo "无法获取 " & sName & " 的内部版本信息"
    ' End If

你会注意到这个 WSF 脚本将其所有函数和子例程都作为脚本的一部分，即使它们本可以被放入包含的库脚本中。然而，每当你包含一个库脚本时，你必须确保被包含的脚本位于适当的目录中。如果你要与组织外的人员共享脚本，这尤其成问题。

但这并不能阻止你添加自己的脚本库。事实上，你可能会发现将你想调用的代码放在一个单独的脚本中，作为一个独立的子例程或函数更容易。在包装器脚本中，你只需要调用你的子例程或函数。

使用 WSF 包装器脚本的优点是，你可以将其用作命令行工具，这使其非常容易设置为计划任务。包装器脚本处理所有的列表处理、错误处理和日志记录。你只需插入你现有的代码。

### 总结

在本章中，我们向你快速介绍了 XML，并演示了 Windows 脚本文件的功能和优点。我们向你展示了一个正在运行的 WSF，并引导你将现有的 VBScript 文件转换为 WSF。这类脚本需要稍长的时间来开发，一开始可能令人望而生畏；但随着一些经验，你将学会在哪里可以利用这种脚本格式。它不是每个问题的正确解决方案，但它是你管理脚本工具箱中的另一个工具。

> **更多信息** 有关更多信息，请访问 Microsoft 网站：http://msdn.microsoft.com/library/default.asp?url=/library/en-us/script56/html/wsorixmlelements.asp（此链接在随附的 CD 上；单击 MSDN XML 元素。）ScriptingAnswers.com 还提供了一个培训视频 *Windows Script Files Unmasked*，详细介绍了这个主题。

# 第 4 章：Windows 脚本组件

**本章内容：**

- 理解 COM 对象、方法和属性
- 理解 Windows 脚本组件
- 使用脚本组件向导
- 使用属性
- 使用方法
- 使用事件
- 使用脚本编辑器创建 Windows 脚本组件
- 查看运行中的 Windows 脚本组件
- 总结

如果你开发了复杂的 VBScript 代码，并希望在其他脚本中使用，将其打包成 Windows 脚本组件是一个好方法。通过将你的代码转换为组件，你可以像使用任何其他 COM 对象一样使用它。Windows 脚本组件以 XML 格式打包，但有一种简单的方法可以生成 XML 骨架，我们将引导你完成。我们还将向你提供 COM 的概述。最后，我们将向你展示一个运行中的 Windows 脚本组件。

像许多开发者一样，你可能有一些复杂的脚本，或者可能只是一些函数，你希望在其他脚本中使用。你可以复制和粘贴，但这只会增加新脚本的长度和复杂性。你可以将你的脚本创建为 Windows 脚本文件并引用外部脚本，但你可能不需要 WSF。一个解决方案是将可重用代码创建为你自己的组件对象模型 (COM) 对象，并在你的脚本中使用这个新对象。你不是像脚本那样运行组件，而是在你的脚本中实例化组件，就像你实例化像 WshShell 这样的对象一样。

## 理解 COM 对象、方法和属性

传统的 COM 编程超出了本书的范围，但我们将对该主题提供一个简要概述，你可能比你意识到的更了解它。

将 COM 对象想象成一个装满编程的黑盒子，用于完成一组相关的任务。我们不需要知道盒子里是什么，只需要知道如何使用它。要使用盒子里的代码，程序员首先为对象分配一个名称，或 progid，以便他可以告诉 WScript 创建，

或者实例化该对象的一个实例。程序员还会分配一个全局唯一标识符（GUID），称为 classid。当对象在计算机上注册时，这些值会存储在注册表中。

接下来，程序员在盒子的外部创建接口来操作内部的代码。当你处理对象的属性或方法时，就会使用这些接口。属性是一个值，例如 Wscript.Network 对象的 Username 属性。有些属性是只读的，但其他属性可以更改。大多数 COM 对象还公开一个方法，该方法调用内部代码来执行任务，例如映射网络驱动器。我们并不关心创建驱动器映射的代码；它可能非常复杂。COM 对象简化了它，并为我们提供了一个简单的方法；例如，MapNetworkDrive。

通常，COM 对象被编译成动态链接库（.dll）文件。此文件必须在计算机上注册后才能使用。注册通常作为应用程序安装的一部分进行，但你可以使用 regsvr32.exe 手动注册文件。在命令提示符窗口中输入 **regsvr32 /?** 以查看有关此实用程序的帮助信息。

> **ActiveX、COM 和 OLE**

当你听说 ActiveX 时，它常常让人联想到 Internet Explorer ActiveX 控件，但这只是一个特定的实现。ActiveX 实际上指的是 Microsoft 所有的应用程序组件编程技术，包括 OLE 和 COM。这些技术允许应用程序共享信息。

OLE（对象链接和嵌入）是一种旧方法。如果你曾经在 Microsoft Word 文档中嵌入 Microsoft Excel 电子表格，那么你使用的就是 OLE。OLE 对象将嵌入的电子表格连接到其应用程序 Microsoft Excel。

COM 在 1990 年代初期推出，是 Microsoft 面向对象编程方法的一部分。COM 对象提供接口和通信机制，程序员可以利用这些来构建更大的应用程序。ActiveX 是 COM 的最新化身。

## 理解 Windows 脚本组件

Windows 脚本组件（WSC）文件是一种可以在 VBScript 或 JScript 脚本中用作 COM 对象的脚本文件类型。脚本组件获取复杂的代码并提供更简单的接口。例如，你可能有一个连接到 SQL 数据库并返回有关特定计算机信息的子程序。使用脚本组件，你可以通过创建 COM 对象并利用该对象的接口来执行代码，从而简化功能。

脚本组件不是真正的 COM 对象，因为它没有编译。它实际上是一个特殊格式的 XML 文件，你可以使用任何文本或脚本编辑器创建和编辑它。WSC 的使用方式类似于 COM 对象，但脚本组件库 Scrobj.dll 完成了将 WSC 转换为标准 COM 接口的所有繁重工作。你不必担心开发复杂的编译 COM 对象；你可以通过使用 WSC 文件来利用 COM 功能。

XML 文件由以下标签组成：

- **package** 标签的用法与在 Windows 脚本文件中基本相同，用作包装标签。如果你只有一个组件，此标签是可选的；如果有多个组件，你的文件将以 **package** 标签开始和结束。
- **component** 标签，类似于 Windows 脚本文件中的 **job** 标签，包含组件的所有元素。你可以在文件中拥有多个组件，但实际上，我们建议每个文件只包含一个组件。此标签有一个 **id** 属性，你应该设置它。

```
<component id="JDHIT.Demo">
```

如果你有多个组件或计划生成类型库，则需要设置此项。我们建议将其设置为与脚本组件的 **progid** 相同。

- **?component** 标签具有 **error** 和 **debug** 标志，可设置为 TRUE 或 FALSE。在生产环境中，包括 WSC 文件在内的 COM 对象会静默运行。但是，在开发过程中，你可能需要使用 **?component** 标签来方便调试和故障排除。如果你将 **error** 设置为 TRUE，则组件文件中生成消息的脚本错误将显示给用户。如果你使用的是脚本调试器，也可以将 **debug** 设置为 TRUE。

```
<?component error="true" debug="false" ?>
```

注意使用问号而不是斜杠字符来关闭标签。在将组件投入生产之前，我们建议将这些标志设置为 FALSE。

- **registration** 标签包含注册组件所需的所有信息。尽管所有标签属性都是可选的，但从实际角度来看，你确实应该定义大部分属性。

```
<registration progid="JDHDemo.WSC"
classid="{443fdeb9-7d32-4331-b289-dd3b8da3d9d5}"
description="JDHDemo" remotable="yes" version="1.00">
</registration>
```

**registration** 标签的属性包括：

- **progid** 属性是你在脚本中创建对象实例时将使用的名称。
- **classid** 属性反映新对象的 GUID。不要随意输入任何数字。你需要使用像 uuidgen.exe 或脚本组件向导这样的工具来生成正确的值。
- **description** 属性用于在注册表中描述你的对象。当你使用 COM 对象浏览器时，可以看到此值。保持此值简短。
- **remotable** 属性是一个布尔标志，决定 COM 对象是否可以通过分布式 COM（DCOM）在远程系统上实例化。在使用对象之前，必须在远程系统上安装并注册该对象。当你创建远程实例时，脚本将对象视为在本地运行。但是，所有属性和方法都从远程系统执行，具体取决于凭据和安全设置。
- **version** 属性用于内部版本信息。此数据存储在注册表中。

**public** 标签用于标识对象公开可用的方法和属性。

```
<public>
  <property name="size">
    <get/>
  </property>
  <property name="modified">
    <get/>
  </property>
  <property name="linecount">
    <get/>
  </property>
  <method name="view">
  </method>
</public>
```

**event** 标签用于定义可以从脚本组件内部调用或触发的事件。事件是脚本运行时发生的某些操作，例如文件大小发生变化。你定义该操作是什么。当检测到该操作时，你触发事件。触发的事件本质上是标记发生了某事。你可以添加代码，根据事件的性质采取进一步步骤。你必须定义 **name** 属性。

```
<event name="sizechanged"/>
```

**script** 标签与 Windows 脚本文件中同名标签的作用相同。此标签的主体包含调用以执行对象属性和方法的所有函数和子程序。脚本代码隐藏在黑匣子中，并通过对象的属性和方法公开。

> **重要** 即使我们谈论代码被“隐藏”，我们也不是指字面上的意思。与传统的编译 COM 对象不同，WSC 文件是纯文本，任何人都可以用文本编辑器查看。不要硬编码管理员凭据、密码或任何其他不希望公开的信息。

- **object** 标签，类似于 WSF 脚本中的同名标签，用于使外部对象全局可用。没有此标签，你将不得不在整个脚本中使用 **CreateObject**。

```
<object id=objFSO progid="Scripting.FileSystemObject"/>
```

- **resource** 标签，类似于 WSF 脚本中的同名标签，用于定义要在整个组件中使用的常量。**id** 属性用于在脚本中标识资源主体。

```
<resource id="version">JDHIT Demo v1.0</resource>
...
<script language="VBScript">
...
Function ShowVersion()
  strVer=getResource("version")
  ShowVersion=MsgBox(strVer,vbOKOnly+vbInformation,"Version")
End Function
...
```

- **comment** 标签在其他脚本元素内使用，以提供注释或文档。

```
<public>
  <comment>
    Get the file size of the specified file. Data returned is in bytes.
  </comment>
  <property name="size">
    <get/>
  </property>
</public>
```

> **最佳实践** 我们鼓励你在整个脚本组件文件中大量使用注释块。你现在可能理解每个属性和方法应该做什么，但明年你可能就记不起来了。此外，注释使其他人更容易理解和排除文件故障。

清单 4-1 是一个 WSC 文件的骨架大纲。

```
**清单 4-1 WSC 骨架**
<?XML version="1.0"?>
<package>
<?component error="true" debug="true"?>

  <comment>
    This skeleton shows how script component elements are
    assembled into a .wsc file.
  </comment>

<component id="MyScriptlet">
  <registration
```



# 第二部分：打包你的脚本

```xml
<reference object="progID"
    progid="progID"
    description="description"
    version="version"
    clsid="{00000000-0000-0000-000000000000}"/>

<reference object="progID">
    <public>
        <property name="propertyname"/>
        <method name="methodname"/>
        <event name="eventname"/>
    </public>
    <script language="VBScript">
        <![CDATA[
        dim propertyname
        Function methodname()
            ' 脚本在此处。
        End Function
        ]]>
    </script>
    <object id="objID" progId="some.object">
        <resource ID="resourceID1">字符串或数字在此处</resource>
        <resource ID="resourceID2">字符串或数字在此处</resource>
    </object>
</reference>
</package>
```

> **随书光盘** 你会在本书附带的光盘上找到此脚本以及本章列出的其他脚本。

请记住，如果你的格式不正确，脚本组件将无法正常工作。幸运的是，Microsoft 提供了一个名为 **脚本组件向导** 的免费工具，它可以创建一个框架供你构建组件。你可以在以下地址下载该向导：

http://www.microsoft.com/downloads/details.aspx?FamilyId=408024ED-FAAD-4835-8E68-773CCC951A6B&displaylang=en

> **随书光盘** 此链接与本书中引用的大多数链接一样，都包含在随书光盘中。请点击 *脚本组件向导*。

你也可以在以下网站搜索信息。

http://msdn.microsoft.com/scripting

## 使用脚本组件向导

脚本组件向导会在用户指定的位置创建一个 WSC 文件。它会提示你输入要公开的属性、方法和事件的名称，然后创建适当的注册信息，包括一个 GUID。

例如，我们将构建一个脚本组件，以便更轻松地处理 Active Directory 中的用户对象。我们需要一个对象，它能够根据 sAMAccountName 获取用户的唯一名称，反之亦然。我们还希望能够通过一行代码设置用户的密码。最后，我们希望获取用户对象创建的日期、最后修改的日期以及它所属的组织单位。我们将使用脚本组件向导来构建一个 XML 骨架。该向导 (scriptwz.exe) 默认安装在 `C:\Program Files\Microsoft Windows Script\Component Wizard`。

在图 4-1 中，向导提示我们输入有关新 WSC 文件的信息。

![](img/4fefd6988ba5d4a92a65127617ca24c2_120_0.png)

在向导的步骤 2 中，如图 4-2（在下一页）所示，我们指定组件特性，例如脚本语言以及是否启用错误检查或调试。

![](img/4fefd6988ba5d4a92a65127617ca24c2_121_0.png)

我们现在定义要公开的属性。我们将指定属性的名称和类型。我们从 Active Directory 返回的值是只读的，因此我们将选择该类型。图 4-3 显示了所有选项。如果你忘记了一个属性，请不要担心。你随时可以编辑文件并在稍后添加相应的 XML 标记。

![](img/4fefd6988ba5d4a92a65127617ca24c2_121_1.png)

在向导的步骤 4 中，如图 4-4 所示，我们定义组件的方法。我们创建一个名为 `getsam` 的方法，该方法接受一个名为 `strDN` 的参数并返回 DN。`getDN` 方法返回传入 DN 的 sam。我们还创建了一个 `changepassword` 方法。

# 第 4 章：Windows 脚本组件

![](img/4fefd6988ba5d4a92a65127617ca24c2_122_0.png)

图 4-4  定义脚本组件方法

如果我们有任何要添加的事件，我们将在向导的步骤 5 上定义它们，如图 4-5 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_122_1.png)

图 4-5  定义脚本组件事件

向导的最后一步，如图 4-6（在下一页）所示，是我们指定内容的摘要。我们可以单击“返回”进行任何更正，或单击“完成”创建 WSC 文件。我们完成的 WSC 壳显示在清单 4-2 中，也在下一页。

## 104  第二部分：打包你的脚本

![](img/4fefd6988ba5d4a92a65127617ca24c2_123_0.png)

图 4-6  完成 Windows 脚本组件向导

```xml
清单 4-2  脚本组件向导壳
<?xml version="1.0"?>
<component>
    <?component error="true" debug="false"?>
    <registration
        description="ADUser"
        progid="ADUser.WSC"
        version="1.00"
        classid="{bbe2f493-434e-472f-b0f3-2f267fa17b62}"
    >
    </registration>
    <public>
        <property name="whencreated">
            <get/>
        </property>
        <property name="whenmodified">
            <get/>
        </property>
        <property name="ou">
            <get/>
        </property>
        <method name="getsam">
            <PARAMETER name="strDN"/>
        </method>
        <method name="getdn">
            <PARAMETER name="strSAM"/>
        </method>
        <method name="changepassword">
            <PARAMETER name="strSAM"/>
            <PARAMETER name="strPassword"/>
            <PARAMETER name="BlnChangeNextLogon"/>
        </method>
    </public>

    <script language="VBScript">
    <![CDATA[
        dim whencreated
        dim whenmodified
        dim ou

        function get_whencreated()
            get_whencreated = whencreated
        end function

        function get_whenmodified()
            get_whenmodified = whenmodified
        end function

        function get_ou()
            get_ou = ou
        end function

        function getsam(strDN)
            getsam = "临时值"
        end function

        function getdn(strSAM)
            getdn = "临时值"
        end function

        function changepassword(strSAM,strPassword,BlnChangeNextLogon)
            changepassword = "临时值"
        end function
    ]]>
    </script>

</component>
```

剩下的就是添加文档注释以及将执行我们函数的 VBScript 代码。

## 处理属性

在 WSC 中，你可以通过两种方式处理属性。首先，你可以定义一个简单的、预设的属性名称，如下所示。

```xml
<property name="user" />
```

在脚本部分，你可以为该属性定义值，前提是你将属性定义为读/写。

```xml
<script language="VBScript">
<![CDATA[
'定义 user 属性
User="Test User 98"
...
</script>
```

处理属性的另一种方式是从函数返回一个值。在清单 4-2 中，属性值由函数计算。

```xml
<property name="whencreated">
    <get/>
</property>
...
function get_whencreated()
    get_whencreated = whencreated
end function
```

脚本组件向导生成了一个大纲。我们需要在函数中开发脚本代码并修改属性标记。对于 *whencreated* 属性，我们将输入一个用户的唯一名称作为参数。我们可以修改属性元素以反映此更改，并使用必要的代码更新函数。

```xml
<property name="whencreated">
    <get/>
</property>
...
Function get_whencreated(strDN)
On Error Resume Next
    Set objUser=GetObject("LDAP://" & strDN)
    If Err.Number<>0 Then
        get_whencreated="未找到"
    Else
        get_whencreated = objUser.whencreated
    End If
End Function
```

我们添加 *strDN* 作为函数的参数。你可能也注意到了 *get* 标记。此标记将该属性标识为只读。要使属性可读/写，请添加 *put* 标记。这些操作 *get* 和 *put* 是处理属性的标准 COM 命令。你会注意到 *whencreated* 属性的关联函数是 *get_whencreated*。这有助于我们记住我们正在读取属性值。

**提示** *get* 标记可以使用一个名为 *internalname* 的属性。你可以使用 *internalname* 属性来指定内部函数的名称。

```xml
<property name="size">
  <get internalname="readsize"/>
</property>
...
Function readsize(strFile)
  '此处是读取文件大小的函数代码
  readsize="某个值"
End function
```

如果你没有指定内部名称，关联函数将使用属性名称。对于较长或更复杂的 WSC 文件，你应该使用内部名称，以便轻松记住特定函数应执行的操作。*property* 标记的 *name* 属性是给用户看的。你可能希望为内部使用使用更简单、更有意义的名称。

## 处理方法

在 WSC 文件中使用方法与处理属性非常相似。通常，方法名称是要执行的函数或子程序的名称。如果你想为函数或子程序使用不同的名称，也可以使用 *internalname* 属性。

```xml
<method name="changepassword">
  <PARAMETER name="strSAM"/>
  <PARAMETER name="strPassword"/>
  <PARAMETER name="BlnChangeNextLogon"/>
</method>
function changepassword(strSAM,strPassword,BlnChangeNextLogon)
  '要运行的代码放在此处
  changepassword = "临时值"
end function
```

此示例中的 *changepassword* 方法需要三个参数。任何使用此对象的人都需要知道参数是什么才能使用该方法。你可以在 WSC 文件中记录此信息，也可以生成类型库。如果你想为你的 WSC 文件生成类型库，则必须为方法添加 *parameter* 标记。

> 类型库
类型库提供有关对象的自动化属性和方法的信息。大多数优秀的脚本编辑器都附带了类型库，COM 对象浏览器使用它们，以便你可以学习如何使用对象。如果你的脚本编辑器提供 Intellisense，则类型库用于使用对象信息填充 Intellisense 下拉菜单。一些脚本编辑器，如 PrimalScript，会在你右键单击组件并单击“生成类型库”时为你生成类型库。你也可以在 Windows 资源管理器中右键单击 WSC 文件，然后单击“生成类型库”。还有其他一些方法；有关更多信息，请参阅 Windows Script Host 文档的 Windows 脚本组件部分。

## 处理事件

根据你的组件类型，你可能希望包含对事件的支持。事件是一种操作，例如窗口关闭，或是状态变更，如文件已保存。在 WSC 文件中，你决定事件是什么以及何时调用它。事件在 `public` 节中定义，与属性和方法一同存在。

```xml
<event name="UserAdded" />
```

你在 WSC 代码中使用 `fireevent` 方法来触发事件。例如，你可能有一个名为 *AddUser* 的方法，并希望在此方法完成时触发 *UserAdded* 事件。

```xml
<method name="adduser" internalname="NewUser">
    <parameter name="strSAM"/>
</method>
<script language="VBScript">
<!CDATA[

function NewUser(strSAM)
    '此处放置创建新用户的代码
    fireEvent "UserAdded"
End function
]]>
</script>
```

WSC 文件除了定义和触发事件外，不会对事件做任何处理。使用该对象的脚本决定（如果有的话）要执行什么操作。为了便于做出此决定，需要在脚本中包含一个连接到事件的接收器（sink）。接收器是一个吸引外部交互的对象，就像厨房水槽吸引水流一样。接收器等待事件发生，当事件发生时，它会被外部源联系。这是 DCOM 编程的一部分，但你无需了解更多细节。当事件触发时，接收器中的代码会被执行。你可能会看到类似这样的代码。

```vbscript
Dim objWSC
Set objWSC=CreateObject("MyObject.wsc","sink_")
objWSC.AddUser("jhicks")
'在此处插入其他代码
wscript.disconnectObject objWSC
wscript.quit
Function sink_UserAdded()
    MsgBox "已添加新用户。"
End function
```

当你实例化对象时，你还定义了一个与事件名称相关联的前缀。这些操作创建了接收器。当事件触发时，相应的函数或子程序中的代码（在本例中为 *sink_UserAdded*）将被执行。事件非常有用，因为它们可以在脚本中的任何时间发生。你可以启动一个长时间运行的过程，运行其他代码，然后等待事件发生。但是，如果在事件触发之前退出脚本，你将永远不知道它是否触发。如果你希望事件代码接收器运行，你需要添加代码以防止脚本在事件发生之前结束。一种方法是创建一个消息框。只要不关闭消息框，脚本就会一直运行。在事件触发后，你可以关闭消息框并退出脚本。

你也可以通过定义一个或多个参数让事件返回信息。

```xml
<event name="UserAdded">
  <parameter name="strSAM"/>
  <parameter name="strDN"/>
</event>
```

当你调用 *fireevent* 时，在那时传递参数。

```vbscript
function NewUser(strSAM)
  '此处放置创建新用户的代码
  '此处定义 strDN 的代码
  fireEvent "UserAdded",strSAM,strDN
End function
```

然后你可以在接收器代码中使用这些信息。

```vbscript
Function sink_UserAdded(strSAM,strDN)
  MsgBox "用户 " & strSAM & " 是 " & strDN & "。"
End function
```

我们的 ADUser.wsc 示例中没有任何事件，但最终完成的文件如清单 4-3 所示。

```xml
清单 4-3 ADUser.wsc
<?xml version="1.0" ?>
<component>
  <?component error="true" debug="false" ?>
  <registration progid="ADUser.WSC"
  classid="{bbe2f493-434e-472f-b0f3-2f267fa17b62}"
  description="ADUser" version="1.00">
  </registration>
  <public>
    <property name="whencreated">
      <get/>
    </property>
    <property name="whenmodified">
      <get/>
    </property>
    <property name="ou">
      <get/>
    </property>
    <method name="getsam">
      <parameter name="strDN"/>
    </method>
    <method name="getdn">
      <parameter name="strSAM"/>
    </method>
    <method name="changepassword">
      <parameter name="strUser"/>
      <parameter name="strPassword"/>
      <parameter name="blnChangeNextLogon"/>
    </method>
  </public>
  <object id="cmd" progid="ADODB.Command" events="true" reference="false"/>
  <object id="conn" progid="ADODB.Connection" events="true" reference="false"/>
  <script language="VBScript">
  <![CDATA[
  dim whencreated
  dim whenmodified
  dim ou

  Function get_whencreated(strDN)
  On Error Resume Next
      Set objUser=GetObject("LDAP://" & strDN)
      If Err.Number<>0 Then
          get_whencreated="未找到"
      Else
          get_whencreated = ObjUser.whencreated
      End If
  end Function

  function get_whenmodified(strDN)
  On Error Resume Next
      Set objUser=GetObject("LDAP://" & strDN)
      If Err.Number<>0 Then
          get_whenmodified="未找到"
      Else
          get_whenmodified = ObjUser.whenchanged
      End If
  end function

  function get_ou(strSAM)
  On Error Resume Next
  strDN=getdn(strSAM)
  Set objUser=GetObject("LDAP://" & strDN)
      If Err.Number<>0 Then
          get_ou="未找到"
          Exit function
      Else
          strParent=objUser.Parent
          set objParent=GetObject(strParent)
          get_ou=objParent.name
      End If

  end function

  function getsam(strDN)
  On Error Resume Next
  Set RootDSE=GetObject("LDAP://RootDSE")
  Set myDomain=GetObject("LDAP://"&RootDSE.get("DefaultNamingContext"))

  strQuery="Select SAMAaccountname,cn,distinguishedname from '" & _
  myDomain.AdsPath & "' where objectcategory='person' AND objectclass=" & _
  "'user'" & " AND distinguishedname='" & strDN & "'"

  set cat=GetObject("GC:")
  for each obj In cat
     set GC=obj
  Next

  conn.Provider="ADSDSOObject"
  conn.Open "Active Directory Provider"
  cmd.ActiveConnection=conn
  cmd.Properties("Page Size") = 100
  cmd.Properties("asynchronous")=True
  cmd.Properties("Timeout") =30
  cmd.Properties("Cache Results") = False
  cmd.CommandText=strQuery

  set RS=cmd.Execute

  Do While not RS.EOF
     GetSAM=rs.Fields("samAccountname")
     rs.movenext
  Loop

  If GetSAM="" Then GetSAM="未找到"

  rs.Close
  conn.Close

  end function

  function getdn(strSAM)
  On Error Resume Next
  Set RootDSE=GetObject("LDAP://RootDSE")
  Set myDomain=GetObject("LDAP://"&RootDSE.get("DefaultNamingContext"))

  strQuery="Select SAMAaccountname,cn,distinguishedname from '" & _
  myDomain.AdsPath & "' where objectcategory='person' AND objectclass=" & _
  "'user'" & " AND SAMAccountName='" & strSAM & "'"

  set cat=GetObject("GC:")
  for each obj In cat
     set GC=obj
  Next

  conn.Provider="ADSDSOObject"
  conn.Open "Active Directory Provider"
  cmd.ActiveConnection=conn
  cmd.Properties("Page Size") = 100
  cmd.Properties("asynchronous")=True
  cmd.Properties("Timeout") =30
  cmd.Properties("Cache Results") = False
  cmd.CommandText=strQuery

  set RS=cmd.Execute

  Do While not RS.EOF
      GetDN=rs.Fields("distinguishedname")
      rs.movenext
  Loop

  If GetDN="" Then GetDN="未找到"

  rs.Close
  conn.Close

  end Function


  function changepassword(strSAM,strPassword,BlnChangeNextLogon)
  '如果成功则返回 TRUE
  On Error Resume Next
  strDN=getdn(strSAM)
  Set objUser=GetObject("LDAP://" & strDN)
  If Err.number<>0 Then
      changepassword=MsgBox("查找用户 " & _
      strSAM & " 失败",vbOKOnly+vbInformation,"更改密码错误")
      changepassword=False
      Exit Function
  else
      objUser.setPassword strPassword
      objUser.SetInfo
      If Err.Number<>0 Then
          strMsg="无法为 " & strSAM & " 设置密码" & VbCrLf & _
          "错误号 " & Err.Number & " " & Err.Description
          MsgBox strMsg,vbOKOnly+vbCritical,"密码失败"
          changepassword=False
          Exit Function
      Else
          If BlnChangeNextLogon then
              objUser.put "pwdLastSet", 0
              objUser.SetInfo
          End If
      changepassword = True
      End If
  End If

  end Function

  ]]>
  </script>
</component>
```

# 第二部分：打包你的脚本

## 使用脚本编辑器创建 Windows 脚本组件

脚本组件向导并非创建 WSC 文件的唯一途径。一些商业脚本编辑器，例如 XLNow 的 OnScript 和 SAPIEN 的 PrimalScript，都包含了它们自己版本的脚本组件向导。这些编辑器也有自己的方法来编辑 WSC 文件。让我们来看看 PrimalScript 4.0 的向导。

图 4-7 显示了向导的第一页，我们在其中定义了脚本位置。

![图 4-7 创建新项目](img/4fefd6988ba5d4a92a65127617ca24c2_132_0.png)

在向导的下一页（如图 4-8 所示），我们填写有关组件的一些常规信息，例如名称、位置和主要脚本语言。

![图 4-8 填写常规信息](img/4fefd6988ba5d4a92a65127617ca24c2_132_1.png)



## 114 第二部分：打包你的脚本

在向导的下一页，系统会提示我们指定要包含的对象，如图 4-9 所示。PrimalScript 提供了一个常用对象列表，你也可以点击“浏览”来添加任何其他已注册的对象。

![](img/4fefd6988ba5d4a92a65127617ca24c2_133_0.png)

图 4-9 添加对象

如果我们想要添加任何引用，可以在向导的下一页进行操作，如图 4-10 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_133_1.png)

图 4-10 添加引用

在向导的下一页，如图 4-11 所示，我们可以添加任何函数库或其他脚本。

![](img/4fefd6988ba5d4a92a65127617ca24c2_134_0.png)

图 4-11 添加文件

向导的最后一页是摘要，如图 4-12 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_134_1.png)

图 4-12 向导摘要

PrimalScript 会在工作区中打开该文件，处理方式与 WSF 脚本非常相似。编辑器会屏蔽所有 XML 代码，只留下主编辑窗格供你编写 VBScript。要添加方法和属性，请在左窗格中右键单击“Interface”，然后单击相应的菜单选项，如图 4-13 所示。

## 116 第二部分：打包你的脚本

![](img/4fefd6988ba5d4a92a65127617ca24c2_135_0.png)

图 4-13 添加方法和属性

在图 4-14 中，我们添加并定义了一个属性。在此示例中，内部名称和外部名称不同。外部名称将用于生成的类型库，因此对用户更友好。我们将对函数使用内部名称。

![](img/4fefd6988ba5d4a92a65127617ca24c2_135_1.png)

图 4-14 添加属性

我们在图 4-15 中遵循类似的过程，为脚本文件添加方法。

![](img/4fefd6988ba5d4a92a65127617ca24c2_135_2.png)

图 4-15 添加方法

在添加了组件的方法、属性和事件之后，你所需要做的就是编写底层代码。完成后，在左窗格中右键单击该组件，并注册该组件。PrimalScript 还会生成一个类型库。现在你的组件已准备就绪，可以使用了。完成的脚本组件代码见清单 4-4。

```
清单 4-4 FilePlus.wsc
<?xml version="1.0" ?>
<package>
    <comment>
        Use this component for easy file operations such as returning
        file size and modified date. Includes functions to return linecount,
        the first X number of lines in the file or the last X number of
        lines in the file. Also a view method to open the file in Notepad.
    </comment>
    <component id="FilePlus">
        <?component error="true" debug="false" ?>
        <registration progid="FilePlus.WSC"
        classid="{DB619F63-768F-4746-BCDC-88F5DA1EBB42}"
        description="FilePlus" remotable="no" version="1.0">
        <script language="VBScript">
    <![CDATA[
            Function Register()
                Dim TypeLib
                Set TypeLib = CreateObject("Scriptlet.TypeLib")
                TypeLib.AddURL "FilePlus.WSC"
                TypeLib.Path = "FilePlus.tlb"
                TypeLib.Doc = "FilePlus"
                TypeLib.Name = "FilePlus.tlb"
                TypeLib.MajorVersion = 1
                TypeLib.MinorVersion = 0
                TypeLib.Write
            End Function

            Function Unregister()

            End Function

    ]]>
        </script>
        </registration>
        <public>
            <property internalname="strFile" name="filename">
                <get/>
                <put/>
            </property>
            <property name="linecount">
                <get/>
            </property>
            <property internalname="readsize" name="size">
                <get/>
            </property>
            <property internalname="readmodified" name="modified">
                <get/>
</property>
		<method name="view">
		</method>
		<method name="head">
			<parameter name="numLines"/>
		</method>
		<method name="tail">
			<parameter name="numLines"/>
		</method>
	</public>
<object id="objFSO" progid="Scripting.FileSystemObject" events="false" reference="TRUE"/>
<object id="objShell" progid="WScript.Shell" events="false" reference="TRUE"/>
<script id="FilePlus" language="VBScript">
<![CDATA[
Dim linecount
dim strFile
Dim readsize
Dim readmodified

strFile = 0
linecount = 0
readsize = 0
readmodified = 0

Function get_strFile()
	get_strFile = strFile
End Function

Function put_strFile(newValue)
	strFile = newValue
End Function

Function view()
On Error Resume Next
'open file in Notepad

If objFSO.FileExists(strFile) Then
	view = objShell.Run("Notepad " & strFile,1,False)
Else
	view=MsgBox("File " & strFile & " not found!",vbOKOnly+vbCritical,"Error!")
End If
End Function

Function get_linecount()
On Error Resume Next
If objFSO.FileExists(strFile) Then
	Set objFile=objFSO.OpenTextFile(strFile,ForReading)
	i=0
	Do While objFile.AtEndOfStream<>True
		objFile.ReadLine
		i=i+1
	Loop
	objFile.Close
get_linecount=i
Else
    get_linecount =0
End If
End Function
```

```
Function get_readsize()
On Error Resume Next
If objFSO.FileExists(strFile) Then
    Set objFile=objFSO.GetFile(strFile)
    get_readsize = objFile.size
Else
    get_readsize=0
End If
    'get_readsize = readsize
End Function
```

```
function get_readmodified()
On Error Resume Next
If objFSO.FileExists(strFile) Then
    Set objFile=objFSO.GetFile(strFile)
    get_readmodified = objFile.DateLastModified
Else
    get_readmodified=0
End If
end function
```

```
function head(numLines)
On Error Resume Next
'Display X number of lines from beginning of file
If objFSO.FileExists(strFile) Then
    Set objFile=objFSO.OpenTextFile(strFile,ForReading)
    i=0
    Do while i<numLines
        strData=strData & objFile.ReadLine & VbCrLf
        i=i+1
    Loop
    objFile.Close
    head = strData
Else
    head=MsgBox("File " & strFile & _
" not found!",vbOKOnly+vbCritical,"Error!")
End If
end Function
```

```
function tail(numLines)
On Error Resume Next
If objFSO.FileExists(strFile) Then
    Set objFile=objFSO.OpenTextFile(strFile,ForReading)
    strText=objFile.ReadAll
    objFile.Close
    tmpArray=Split(strText,VbCrLf)
    icount=get_linecount()
iLimit=iCount-numLines
For x= iLimit To iCount
    strData=strData & tmpArray(x) & vbCrLf
Next
tail = strData
Else
    tail=MsgBox("File " & strFile & _
    " not found!",vbOKOnly+vbCritical,"Error!")
End If

end Function
]]>
        </script>
    </component>
</package>
```

## 实战查看 Windows 脚本组件

我们来逐部分查看 FilePlus 组件并观察其实际运行情况。首先要看的是注释部分，它提供了组件功能的概述。

```
<comment>
Use this component for easy file operations such as returning
file size and modified date. Includes functions to return linecount,
the first X number of lines in the file or the last X number of
lines in the file. Also a view method to open the file in Notepad.
</comment>
```

组件的名称是 FilePlus，它将注册为 FilePlus.WSC。

```
<component id="FilePlus">
<?component error="true" debug="false" ?>
<registration progid="FilePlus.WSC"
classid="{DB619F63-768F-4746-BCDC-88F5DA1EBB42}"
description="FilePlus" remotable="no" version="1.0">
```

该组件有一个名为 *filename* 的读/写属性，以及名为 *linecount*、*size* 和 *modified* 的只读属性。

```
<property internalname="strFile" name="filename">
    <get/>
    <put/>
</property>
<property name="linecount">
    <get/>
</property>
<property internalname="readsize" name="size">
    <get/>
</property>
<property internalname="readmodified" name="modified">
    <get/>
</property>
```

请注意，size 和 modified 定义了内部名称，因为我们希望外部属性名称对用户友好，而内部使用则采用更有意义的名称。

该组件有三个方法：view、head 和 tail。后两个方法需要一个参数，用于指定要返回的文本行数。

```
<method name="view">
</method>
<method name="head">
    <parameter name="numLines"/>
</method>
<method name="tail">
    <parameter name="numLines"/>
</method>
```

由于我们大量依赖 Scripting.FileSystemObject，在组件开头用一个 object 标签来定义它是有意义的。定义之后，我们就不必在每个函数中都定义它了。对于 WshShell 对象，我们也将采用同样的方式。

```
<object id="objFSO" progid="Scripting.FileSystemObject" events="false" reference="TRUE"/>
<object id="objShell" progid="WScript.Shell" events="false" reference="TRUE"/>
```

组件的其余部分是支持这些属性和方法的 VBScript。每个属性和方法都有自己的函数。我们不会详细介绍每个函数，但需要指出的是，外部名称是 filename，而内部名称是更有意义的 strFile。此外，如果你像这里一样复用了 strFile 变量，你无需修改任何内容。

代码完成并注册组件后，就可以在脚本中使用该组件了。清单 4-5 中的脚本是一个简短的示例，演示了如何使用 FilePlus.wsc 组件。

> **注意**  你必须先注册脚本组件才能使用它。可以通过在 Windows 资源管理器中右键单击该组件并单击“注册”来完成。一些脚本编辑器也提供了快捷菜单命令。你也可以通过运行 Regsvr32 mycomponent.wsc 来注册组件。你需要使用文件的完整路径。注册组件后，即可通过注册表访问。如果添加或删除了任何属性、方法或事件，必须先注销该组件并重新注册，更改才能生效。你可以使用 Regsvr32 的 /u 开关来注销组件。语法是 regsvr32 /u mycomponent.wsc。顺便提一下，当修改底层 VBScript 时，你不必注销并重新注册组件，只有当组件结构发生变化时才需要。请记住，必须在计划使用该组件的任何计算机上复制并注册该组件文件。



## 第四章：Windows 脚本组件 123

清单 4-5 FilePlusDemo.vbs
'使用 CSCRIPT
Dim objFP
Set objFP=CreateObject("fileplus.wsc")
objFP.filename=InputBox("您想查看哪个文件？","FilePlus","c:\boot.ini")

strData="属性 for " & objFP.filename & vbCrLf
strData=strData & "修改日期: " & objFP.modified & vbCrLf
strData=strData & "大小: " & objFP.size & " 字节" & vbCrLf

strData=strData & "#行数: " & objFP.linecount

WScript.Echo strData
WScript.Echo String(10,"*")
iHead=CInt(InputBox("您想从头部查看多少行？","FilePlus",5))

'查看文件的前5行
strHead=objFP.head(iHead)
WScript.Echo strHead
WScript.Echo String(10,"*")

iTails=CInt(InputBox("您想从尾部查看多少行？","FilePlus",5))

'查看文件的最后5行
strTail=objFP.tail(iTail)
WScript.Echo strTail

rc=MsgBox("您想查看文件吗？",vbYesNo+vbQuestion,"FilePlus")

'在记事本中打开文件
if rc=vbYes Then objFP.view

WScript.Quit
```

该组件可以像任何其他对象一样使用。我们通过使用 *CreateObject* 方法来实例化一个对象。使用该组件的注册名称作为 *progid*。

```
Set objFP=CreateObject("fileplus.wsc")
```

此对象需要定义一个文件名，才能使所有其他属性和方法工作。在清单 4-5 中，我们使用 *InputBox* 函数将对象的 *filename* 属性设置为一个提示值。

```
objFP.filename=InputBox("您想查看哪个文件？","FilePlus","c:\boot.ini")
```

内部变量 *strFile* 具有相同的值，并将在函数中必要时使用。定义了此变量，我们就可以获取 *size*、*modified* 和 *linecount* 属性并显示结果。

```
strData="属性 for " & objFP.filename & vbCrLf
strData=strData & "修改日期: " & objFP.modified & vbCrLf
strData=strData & "大小: " & objFP.size & " 字节" & vbCrLf
strData=strData & "#行数: " & objFP.linecount
wScript.Echo strData
```

当调用对象的属性时，会调用一个函数来返回一个值。例如，要获取 *modified* 属性，会调用此函数。

```
function get_readmodified()
On Error Resume Next
If objFSO.FileExists(strFile) Then
    Set objFile=objFSO.GetFile(strFile)
    get_readmodified = objFile.DateLastModified
Else
    get_readmodified=0
End If
end function
```

这是另一个我们为内部和外部属性使用不同名称的实例。函数名 *get_readmodified* 反映了我们正在读取一个属性值，尽管实际上我们是使用 VBScript 和文件系统对象来计算该值。此函数本质上是文件系统对象的包装器，它返回文件的 *最后修改日期* 属性。

要使用对象的 *head* 和 *tail* 方法，我们需要一个要读取的行数的值。示例脚本会提示用户。

```
iHead=CInt(InputBox("您想从头部查看多少行" & _
"？","FilePlus",5))
```

因为 *head* 方法返回数据，所以我们将其设置为一个变量并显示结果。

```
strHead=objFP.head(iHead)
wScript.Echo strHead
```

同样的过程也适用于 *tail* 方法。

```
iTail=CInt(InputBox("您想从尾部查看多少行" & _
"？","FilePlus",5))

strTail=objFP.tail(iTail)
wScript.Echo strTail
```

最后一个方法 *view*，如果运行脚本的用户选择，将在记事本中打开文件。

```
rc=MsgBox("您想查看文件吗？",vbYesNo+vbQuestion,"FilePlus")
'在记事本中打开文件
if rc=vbYes Then objFP.view
```

我们也可以定义该方法来获取指定的行数，或者查看整个文件并在弹出窗口、记事本或 Internet Explorer 中显示结果。这就是这种技术的好处——你可以将复杂的代码隐藏在 Windows 脚本组件中。使用该组件的脚本只需处理简单的属性和方法。

### 总结

在本章中，我们向您展示了如何通过创建 Windows 脚本组件来创建自己的 COM 对象。使用 WSC 文件，您可以获取完成特定任务的现有代码并将其打包为组件的一部分。此组件用于您的管理脚本中，简化了脚本开发。我们演示了如何使用 Windows 脚本组件向导，并概述了使用脚本编辑器开发脚本组件的好处。最后，我们向您展示了 WSC 如何运行以及如何在脚本中使用它。Windows 脚本组件需要时间来开发和部署，但它们提供的强大功能、灵活性和易用性使其非常值得付出努力。

# 第五章
HTML 应用程序：具有用户界面的脚本

本章内容：

- 理解 HTML 应用程序 ............................................. 125
- 理解 Internet Explorer 文档对象模型 .............. 129
- 准备您的 HTA ................................................................ 133
- 理解 HTA 要求和基本要素 ........................... 140
- 使用表单和字段 .................................................... 147
- 添加子例程和函数 .............................................. 151
- 查看运行中的 HTA ............................................................. 152
- 总结 ................................................................................ 157

HTML 应用程序 (HTA) 结合了 Web 页面的灵活性和 VBScript 的功能强大性。使用 HTA，您可以构建在很多方面看起来和感觉都像 Windows 应用程序的脚本，而无需学习像 VB.NET 这样的复杂语言或使用像 Microsoft Visual Studio 这样的复杂开发工具。我们将向您展示一种逐步转换的方法，将现有的 VBScript 包装在 HTA 中，将其转换为图形脚本。

普通的 VBScript 在用户界面元素方面提供的不多——*MsgBox* 和 *InputBox* 函数几乎是 VBScript 内在提供的全部，并且这并不算多。有时，您可能希望创建一个包含更强大用户界面元素的脚本，也许为用户提供一种在 Windows 风格对话框中输入数据的方式。您可能希望生成格式化的输出，例如状态报告。许多第三方产品可以为您提供这种灵活性，但 Windows 提供了一个内置选项：HTML 应用程序 (HTA)。

## 理解 HTML 应用程序

HTA 是一种 HTML 页面类型，它将标准的 HTML 元素和格式与 VBScript 结合在一起。HTA 由 Mshta.exe 执行，Mshta.exe 是 Microsoft Windows 操作系统的核心可执行文件。Mshta.exe 实例化 Microsoft Internet Explorer 的 HTML 渲染引擎（即使 Internet Explorer 不是用户的默认 Web 浏览器），并允许 Internet Explorer 显示页面并执行其脚本。这种安排与 Web 页面和常规 Windows 脚本有一些明显的不同。

- 通常的 Internet Explorer 安全模型不适用于 HTA。HTA 可以实例化 ActiveX 控件和其他组件对象模型 (COM) 对象，例如 *FileSystemObject* 对象，而无需向用户显示警告消息。通常，Internet Explorer 只执行位于用户计算机硬盘驱动器上的 HTA。Internet Explorer 在从 Internet 下载 HTA 时会显示警告，因为 HTA 可以绕过 Internet Explorer 中内置的大多数安全功能。这种安全绕过使得 HTA 的行为更像 Windows 应用程序（通常对其能做什么几乎没有限制），而不是 Web 页面。
- 您可以更好地控制窗口的外观。与标准 Web 页面不同（Internet Explorer 通常显示多个工具栏、地址栏、菜单等），您可以决定 HTA 显示哪些元素。为了使 HTA 看起来更像 Windows 应用程序而不是 Web 页面，您可以隐藏所有 Internet Explorer 用户界面元素，例如工具栏和菜单。（这些元素被开发者统称为 *chrome*。）您还可以指定窗口标题栏中出现的文本，是否具有标准的最小化和最大化按钮，甚至是否在标题栏和 Windows 任务栏中显示应用程序图标。
- 因为脚本是由 Mshta.exe 执行而不是 wscript.exe 或 cscript.exe，所以您将无法像在普通 VBScript 中那样直接访问 WScript 对象。换句话说，您将无法使用 *WScript.Echo* 等方法。但是，在 HTA 中，大多数内置的 WScript 属性和方法被更适合图形应用程序的东西所取代。例如，您可以使用 VBScript 的内置 *MsgBox* 语句在 HTA 中显示简单的弹出对话框。

> **注意** 默认情况下，HTA 文件扩展名与 Mshta.exe 关联，这允许 Windows 在您双击 HTA 时自动执行它们。但是，某些企业环境可能会修改或删除此文件扩展名关联，因此当您双击 HTA 时，它们将不会执行。如果是这种情况，您可以手动执行 Mshta.exe，将 HTA 的名称作为命令行参数传递给它。

您可能已经在没有意识到的情况下运行过 HTA，因为它们看起来几乎与“真正的” Windows 应用程序完全一样。例如，Microsoft Scripting Guys 的 Scriptomatic 工具（如图 5-1 所示）就是一个 HTA，但它具有传统 Windows 应用程序的外观和感觉。



### 图 5-1 Scriptomatic 是一个用 VBScript 编写的 HTA。

如果你以前从未运行过 HTA，请下载 Scriptomatic 并尝试一下。你将更好地了解 HTA 的工作原理及其外观。然后，在脚本编辑器（或如果没有脚本编辑器，则使用 Microsoft 记事本）中打开 HTA，查看 VBScript 和 HTML 如何协同工作使 HTA 运行。你可以在以下地址下载 Scriptomatic

http://www.microsoft.com/technet/scriptcenter/tools/scripto2.mspx

> 随书附赠 此链接与本书中引用的大多数链接一样，包含在附赠 CD 的 Links 文件夹中。请点击 *Scriptomatic 2.0*。

以下是关于 Scriptomatic 需要注意的一些具体要点。

- 窗口的标题栏是自定义的。注意窗口的图标不是标准的 Internet Explorer 图标，而是 Mshta.exe 使用的默认图标。作者本可以指定一个自定义图标，但该图标图形必须与 HTA 本身一起分发。
- HTA 只需复制 HTA 文件即可分发。尝试将其复制到另一台计算机并运行，它应该能正常工作。作为网站下载，Scriptomatic 被打包在安装程序中，但这主要是因为一些企业防火墙出于安全原因会阻止下载 HTA 文件。（请记住，HTA 绕过了 Internet Explorer 安全模型。）因为你通常会在内部网（或甚至只是在自己的计算机上）创建和使用 HTA，所以你不需要创建安装程序。

# 第二部分：打包你的脚本

- HTA 使用标准的 Windows 用户界面元素，例如下拉列表框、单选按钮等。这些元素可以在运行时动态更改。注意在你从 WMI Namespace 下拉列表中选择一个项目后，WMI Class 下拉列表如何自行填充。
- HTA 是用 HTML 构建的。例如，整个页面布局包含在一个 HTML 表格中，这就是各个部分之间分隔线的创建方式（它们只是表格边框）。

如果在脚本编辑器中查看 Scriptomatic HTA 让你感到困惑，别担心！这个 HTA 是由大师们编写的，他们几乎以此为生。我们将使用更简单的技术来生成 HTA，并会一步步指导你完成。然而，在开始介绍创建新 HTA 的基础知识之前，我们需要花点时间回顾一些背景材料。

我们之前关于 HTA 绕过了 Internet Explorer 中大多数安全限制的陈述可能看起来令人担忧，但你不应该担心。首先，严格来说，HTA 不是在 Internet Explorer 中运行的。Internet Explorer 实际上由几个不同的部分组成。一部分提供可视的用户界面：窗口的标题栏、工具栏、旋转的 *e* 图标等。另一部分是 HTML 渲染引擎，它解释基于文本的 HTML 指令并创建最终的、完全布局的页面。该引擎在 Internet Explorer 应用程序中被实例化，使两者作为一个单元工作。其他应用程序也实例化渲染引擎——你无疑遇到过一些显示 HTML 的 Microsoft 管理控制台 (MMC) 管理单元。它们使用 Internet Explorer HTML 渲染引擎。HTA 由 Mshta.exe 执行，Mshta.exe 也实例化 Internet Explorer HTML 渲染引擎。Internet Explorer 是否运行 HTA 似乎是一个微小的细节，但它很重要。

从安全角度来看，HTA 通常只有在从本地计算机或从 Internet Explorer 受信任的安全区域中的网站启动时才会在没有警告的情况下执行。从其他网站下载的 HTA 被视为可执行文件，因此 Internet Explorer 会显示相应的警告对话框，并通常提示用户保存而不是直接执行 HTA。许多包含软件过滤功能的商业防火墙会像过滤可执行文件一样过滤 HTA，这是完全合理的，因为这两种应用程序类型可能具有相似的功能和风险。简而言之，你可能应该认为 HTA 在功能和安全风险方面与常规可执行文件相当。Windows 也是这样对待它们的，所以你受到的保护与对抗流氓可执行文件的保护一样多。

## 理解 Internet Explorer 文档对象模型

当你使用 HTA 时，你可以编写与应用程序的 HTML 内容交互并修改它的 VBScript。你可以在 Scriptomatic 中看到这种交互。当你单击按钮或进行选择时，HTA 会通过更改其内容来响应。列表框填充了新的选择，文本框填满了脚本代码，等等——所有这些都是为了响应你与 HTA 交互元素的交互。HTA 中的所有可视元素都由 HTML 代码或标签定义。让我们再次查看 Scriptomatic (version 2) 进行演示。（如果你还没有下载这个方便的工具，请现在下载。）

请注意，用户界面包括标记为 *Run*、*CIMv2* 等的按钮。查看 HTML 代码——如果你没有 HTML 或脚本编辑器，请使用记事本——你会找到以下代码。

```
<tr>
    <td VALIGN=TOP WIDTH=700 COLSPAN=2>
        <table BORDER=0>
            <tr>
                <td><input id=runbutton class="button" type="button" value="Run"
                    name="run_button" onClick="RunScript()"></td>
                <td><input id=cimv2button class="button" type="button" value="CIMv2"
                    name="cimv2_button" onClick="SetNamespaceToCIMV2()"></td>
                <td><input id=wmisourcebutton class="wmibutton" type="button" value="WMI Source"
                    name="wmisource_button" onClick="SetWMIRepository()" title="change computer used for WMI
                    namespace and class information"></td>
                <td><input id=openbutton class="button" type="button" value="Open"
                    name="open_button" onClick="OpenScript()"></td>
                <td><input id=savebutton class="button" type="button" value="Save"
                    name="save_button" onClick="SaveScript()"></td>
                <td><input id=quitbutton class="button" type="button" value="Quit"
                    name="quit_button" onClick="QuitScript()"></td>
            </tr>
        </table>
    </td>
</tr>
```

> 注意 这些长代码行在像记事本、Microsoft FrontPage 或 SAPIEN PrimalScript 这样的编辑器中会看起来好得多，在那里它们不会换行成多行。但是，HTML 不区分换行和未换行的行，所以即使你完全按照本书所示输入它，它仍然可以工作。

看看这六个 `<input>` 标签。每个标签定义一个按钮。按钮标签包含在每个标签的 value 属性中。每个按钮还有一个 *id* 和 *name* 属性，这使得按钮可以被唯一标识。

### 理解 HTML 文档层次结构

在刚刚展示的示例代码中，按钮的标签嵌套在其他几个标签内。（这在 HTML 编辑器中更容易看到。）每个 <input> 标签包含在一个 <td> 标签内，<td> 标签定义了一个表格单元格。<td> 标签嵌套在一个 <tr> 标签内，<tr> 标签定义了一个表格行。<tr> 标签嵌套在一个 <table> 标签内，正如你可能猜到的，<table> 标签定义了一个表格。所有构成页面的标签都包含在一个 <body> 标签内，而 <body> 标签本身又包含在一个顶级 <html> 标签内。所有这些嵌套形成了一个标签层次结构。像 SAPIEN PrimalScript 4 (http://www.primalscript.com) 这样的编辑环境以树视图显示此层次结构，如图 5-2 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_149_0.png)

图 5-2 HTML 标签的层次结构

这个层次结构形成了 Internet Explorer 文档对象模型 (DOM)。DOM 通过定义标签之间的关系，提供了一种以编程方式处理复杂的、层次结构的 HTML 格式文档的方法。在我们的例子中，你可以说每个 <td> 标签都是 <input> 标签的父级；反过来，<input> 标签是 <td> 标签的子级。<td> 标签依次是 <tr> 标签的子级，并且是其他 <td> 标签的同级（意味着它们具有相同的父标签）。如果你将标签视为编程对象——就像你之前处理过的组件对象模型 (COM) 对象——以下几点将是正确的。

- 每个标签都有一个 *parentElement* 属性，它引用该标签的父标签。
- 每个标签都有一个 *children* 集合，它引用任何子标签。
- 每个标签都有一个 *innerHTML* 属性，它引用标签内包含的任何 HTML 文本。例如，<tr> 标签将有一个 *innerHTML* 属性，该属性包含 <tr> 标签之间的所有内容。



### 理解 HTML 事件

除了属性和集合，HTML 标签对象还拥有事件。事件在标签发生任何情况时触发。例如，由 `input type="button"` 定义的按钮标签可被用户点击，因此可以拥有一个 `onClick` 事件。请仔细查看“运行”按钮的 HTML。

```
<input id=runbutton class="button" type="button" value="Run" name="run_button" onClick="RunScript()">
```

此标签定义了一个按钮，并告诉 HTA 在 *onClick* 事件发生时执行 *RunScript* 子程序。你会发现 *RunScript* 子程序位于 HTA 的其他位置——实际上是在第 885 行。HTML 标签还定义了一个*事件处理程序*，这意味着它指定了一个将响应 *onClick* 事件的子程序。

你也可以通过创建一个特殊命名的子程序来定义事件处理程序。例如，Scriptomatic 的作者本可以将“运行”按钮的 HTML 标签创建如下。

```
<input id=runbutton class="button" type="button" value="Run" name="run_button">
```

此示例中未包含事件处理程序。我们指定了一个以默认事件处理程序命名的子程序。HTA 当前使用名为 *RunScript* 的子程序，而这里本可以有一个名为 *runbutton_onClick* 的子程序。该子程序的前几行如下所示。

```
Sub runbutton_onClick
    Const ForReading = 1
    Const ForWriting = 2
    Const PERMISSION_DENIED = &h46
...
```

此事件处理程序的名称来源于按钮的 *id* 属性（*runbutton*）和事件名称（*onClick*）。你可以自行选择使用哪种类型——默认事件处理程序还是特殊命名的。你可能更喜欢 Scriptomatic 中使用的技术，因为它允许你为子程序使用更合理的名称，例如 *RunScript*。或者你可能认为 *runbutton_onClick* 更直观、更容易记住。选择权在你。

### 应用 DOM

至此，你已经学习了如何在 HTA 中引用 HTML 标签（通过使用 *id* 属性），以及如何响应像按钮点击这样的交互事件（通过定义并编写事件处理程序）。本质上，构建 HTA 需要以下几个步骤。

1.  用 HTML 创建图形用户界面。
2.  为脚本需要访问的任何标签分配一个 *id* 属性。
3.  定义事件处理程序以响应用户的操作，例如点击按钮。
4.  编写事件处理程序以执行脚本需要完成的任何任务。

本章剩余部分将更详细地探讨这四个步骤。

## 准备你的 HTA

许多管理员对 HTA 感到沮丧，因为调试起来非常复杂。VBScript 和 HTML 之间的大量交互有时会让人难以找出错误所在。这就是为什么我们强烈建议你在开始使用 HTA 之前，先将大部分功能代码编写为常规的 VBScript 文件。这样做可以让你完全专注于 VBScript，从而更容易调试 HTA 中最复杂的部分。在本节中，我们将通过一个示例为你讲解。

### 使用脚本代替 HTA

我们将从一个简单的脚本开始，该脚本从文件中读取计算机名称（每行一个），使用 Windows 管理工具 (WMI) 连接到每台计算机，然后显示计算机名称、操作系统内部版本号（例如，Microsoft Windows XP 的 2600）以及最新安装的服务包版本号。该脚本如清单 5-1 所示。

```
清单 5-1 服务包清单

Dim objFSO, objTS, strComputer, objWMIService, colItems, objItem
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\computers.txt")
Do Until objTS.AtEndOfStream
    strComputer = objTS.ReadLine
    Set objWMIService = GetObject("winmgmts:\\" & strComputer & _
        "\\root\\cimv2")
    Set colItems = objWMIService.ExecQuery("SELECT * " & _
        "FROM Win32_OperatingSystem")
    For Each objItem In colItems
        WScript.Echo strComputer & ": " & _
            objItem.BuildNumber & ", " & _
            objItem.ServicePackMajorVersion & "." & _
            objItem.ServicePackMinorVersion
    Next
Loop
objTS.Close
```

> 随书光盘 你可以在随书附带的光盘上找到此脚本以及本章列出的其他脚本。

此脚本执行了一个相当常见且实用的功能。我们希望 HTA 具备以下特性。

-   它应提供一个文本框，用于输入计算机名称。它还应提供一个按钮，用于读取现有的计算机名称文件，并将这些名称添加到文本框的当前列表中。
-   它应提供选项以读取每台计算机的多个属性。
-   它应在新的 Internet Explorer 窗口中显示信息，并以 HTML 表格格式排版，以便我们可以保存文件（使用“另存为”命令保存为 HTML 格式），或将数据复制粘贴到 Microsoft Excel 工作簿中。
-   当列表中的某台计算机无法连接时，它应继续处理下一台计算机，而不是崩溃。

提前指定目标有助于澄清 HTA 的设计并发现潜在的问题点。我们的列表中已经有两个潜在的问题点。我们在开始 HTA 工作 *之前* 指定了两个要合并到脚本中的功能更改。其中两个目标与图形 HTA 环境直接相关：提供用于计算机名称的文本框，以及提供用于查询不同属性的选项（可能是复选框）。另外两个目标与 HTA 没有直接关系，因此它们可以立即合并到我们的脚本中。现在，在将脚本添加到 HTA 之前，先将更改合并到脚本中，将使最终的 HTA 更易于调试。

> **提示** 常规脚本比 HTA 更容易调试，很大程度上是因为 HTA 在 HTML 标签方面增加了许多干扰。在将其粘贴到 HTA 之前使你的脚本正常工作，你将从一个已知可用的功能开始。然后你可以专注于 HTML 以使其外观正确。此外，使用脚本调试器可以节省大量时间，因此如果可能，你应该使用它们。许多调试器（例如 Microsoft Script Debugger 或 SAPIEN PrimalScope）在处理纯 VBScript 时比处理 HTA 效果更好。

清单 5-2 是修改后的脚本。我们添加了一些注释以帮助你理解其运作方式。

```
清单 5-2 修订后的服务包清单
Dim objFSO, objTS, strComputer, objWMIService, colItems, objItem, strHTML

'open the text file
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\computers.txt")

'create the starting HTML
strHTML = "<table border=1>" & vbCrLf
strHTML = strHTML & "<tr>" & vbCrLf
strHTML = strHTML & "<td>Computer</td>" & vbCrLf
strHTML = strHTML & "<td>Build</td>" & vbCrLf
strHTML = strHTML & "<td>Service Pack</td>" & vbCrLf
strHTML = strHTML & "</tr>" & vbCrLf

'read through the text file
Do Until objTS.AtEndOfStream

    'add a table row to the HTML
    strHTML = strHTML & "<tr>" & vbCrLf

'get the next computer name
strComputer = objTS.ReadLine

'query the computer
On Error Resume Next
Set objWMIService = GetObject("winmgmts:\\" & strComputer & _
"\\root\\cimv2")
If Err = 0 Then
    'no error connecting - query the info
    Set colItems = objWMIService.ExecQuery("SELECT * " & _
    "FROM Win32_OperatingSystem")

    'build the output HTML cells
    For Each objItem In colItems
        strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
        strHTML = strHTML & "<td>" & objItem.BuildNumber & "</td>" & vbCrLf
        strHTML = strHTML & "<td>" & objItem.ServicePackMajorVersion & _
        "." & objItem.ServicePackMinorVersion & "</td>" & vbCrLf
    Next

    'finish the HTML row
    strHTML = strHTML & "</tr>"
Else
    'error connecting
    strHTML = strHTML & "<tr>" & vbCrLf
    strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
    strHTML = strHTML & "<td>?</td>" & vbCrLf
    strHTML = strHTML & "<td>?</td>" & vbCrLf
    strHTML = strHTML & "</tr>" & vbCrLf
End If
On Error GoTo 0

Loop

'close the text file
objTS.Close

'close the table
strHTML = strHTML & "</table>" & vbCrLf

'display the table
Dim objIE
Set objIE = CreateObject("InternetExplorer.Application")
objIE.Navigate "about:blank"
objIE.Document.body.innerHTML = strHTML
objIE.visible = True
```

下一页的图 5-3 显示了 Internet Explorer 中的最终输出。



## 第五章：HTML 应用程序：带用户界面的脚本

这个脚本可以完全独立运行。由于我们将在本章中频繁使用它，下面将简要介绍其工作原理。第一部分只是实例化 FileSystemObject 库并打开一个文本文件。

```
Dim objFSO, objTS, strComputer, objWMIService, colItems, objItem, strHTML
'open the text file
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\computers.txt")
```

接下来，脚本创建一个变量来保存最终输出。由于我们希望在 Internet Explorer 中显示该输出，因此需要将其格式化为 HTML。脚本首先定义一个 HTML 表格的起始部分，包括一个包含三列标签的标题行。

```
'create the starting HTML
strHTML = "<table border=1>" & vbCrLf
strHTML = strHTML & "<tr>" & vbCrLf
strHTML = strHTML & "<td>Computer</td>" & vbCrLf
strHTML = strHTML & "<td>Build</td>" & vbCrLf
strHTML = strHTML & "<td>Service Pack</td>" & vbCrLf
strHTML = strHTML & "</tr>" & vbCrLf
```

然后，脚本开始逐行读取文本文件。

```
'read through the text file
Do Until objTS.AtEndofStream
```

对于文本文件中的每一行，我们都在 HTML 表格中创建一个新行。此行将保存文本文件中列出的单个计算机的信息。

```
'add a table row to the HTML
strHTML = strHTML & "<tr>" & vbCrLf
```

我们从文本文件中读取下一个计算机名称到一个变量中。

```
'get the next computer name
strComputer = objTS.ReadLine
```

现在，我们指示 WMI 连接到该计算机。请注意，我们通过使用 *On Error Resume Next* 启用了错误检查。这将使脚本即使在 WMI 连接失败时也能继续运行。

```
'query the computer
On Error Resume Next
Set objWMIService = GetObject("winmgmts:\\" & strComputer & _
    "\\root\\cimv2")
```

尝试连接后，我们使用内置的 *Err* 对象检查错误状态。如果为零，则表示没有发生错误，我们已连接到远程计算机上的 WMI。然后我们可以指示 WMI 检索我们想要检查的 WMI 类。

```
If Err = 0 Then
    'no error connecting - query the info
    Set colItems = objWMIService.ExecQuery("SELECT * " & _
        "FROM Win32_OperatingSystem")
```

WMI 查询将返回一个实例集合，因此我们使用 *For Each...Next* 循环来依次枚举每个实例。实际上，由于我们查询的类别，该集合通常只包含一个实例。

```
'build the output HTML cells
For Each objItem In colItems
```

我们希望每台计算机都列在 HTML 表格的一行中，因此我们现在构建该 HTML 并将其添加到 *strHTML* 变量中。

```
strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
strHTML = strHTML & "<td>" & objItem.BuildNumber & "</td>" & vbCrLf
strHTML = strHTML & "<td>" & objItem.ServicePackMajorVersion & _
    "." & objItem.ServicePackMinorVersion & "</td>" & vbCrLf
Next
'finish the HTML row
strHTML = strHTML & "</tr>"
```

这是当 *Err* 对象不等于零时执行的代码，意味着在连接远程计算机上的 WMI 时发生错误。我们仍然在向 *strHTML* 变量添加 HTML 表格行，但我们用问号填充它，以便在最终输出中清楚地显示哪些计算机无法连接。

```
Else
    'error connecting
    strHTML = strHTML & "<tr>" & vbCrLf
    strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
    strHTML = strHTML & "<td>?</td>" & vbCrLf
    strHTML = strHTML & "<td>?</td>" & vbCrLf
    strHTML = strHTML & "</tr>" & vbCrLf
End If
On Error GoTo 0
Loop
```

最后，当我们读取完所有计算机后，我们关闭文本文件并完成表格 HTML。

```
'close the text file
objTS.Close
'close the table
strHTML = strHTML & "</table>" & vbCrLf
```

这是显示表格的代码。我们实例化 Internet Explorer，指示它显示一个空白页面（通过使用 URL *about:blank*），然后将文档 body 的 innerHTML 设置为存储在 *strHTML* 变量中的 HTML 表格。

```
'display the table
Dim objIE
Set objIE = CreateObject("InternetExplorer.Application")
objIE.Navigate "about:blank"
objIE.Document.body.innerHTML = strHTML
objIE.Visible = True
```

亲自试试最终的脚本。创建一个名为 *c:\computers.txt* 的文本文件，并填充一些来自您网络的计算机名称。这些计算机必须运行 Windows 2000 或更高版本，并且您需要是这些计算机上的管理员才能查询它们。

### 为 HTA 准备脚本

HTA 本质上是相当模块化的。请记住，您的脚本提供的功能是内置于事件处理程序中的，每个事件处理程序基本上都是一个独立的子例程。目前，我们的 HTA 可能会有一个标有 *Execute* 的按钮，该按钮的事件处理程序将包含我们迄今为止编写的整个脚本。但是，现有脚本中的一些功能是自包含的，我们可能希望将其分离到自己的子例程中。这样做不会使 HTA 更容易编写，但会使重用独立功能变得更容易，例如，打开 Internet Explorer 并显示输出的脚本部分。清单 5-3 是稍作修改的脚本，现在将 Internet Explorer 处理分离为一个独立的子例程。

```
'清单 5-3 模块化的库存脚本
Dim objFSO, objTS, strComputer, objWMIService, colItems, objItem, strHTML

'open the text file
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\computers.txt")

'create the starting HTML
strHTML = "<table border=1>" & vbCrLf
strHTML = strHTML & "<tr>" & vbCrLf
strHTML = strHTML & "<td>Computer</td>" & vbCrLf
strHTML = strHTML & "<td>Build</td>" & vbCrLf
strHTML = strHTML & "<td>Service Pack</td>" & vbCrLf
strHTML = strHTML & "</tr>" & vbCrLf

'read through the text file
Do Until objTS.AtEndOfStream

    'add a table row to the HTML
    strHTML = strHTML & "<tr>" & vbCrLf

    'get the next computer name
    strComputer = objTS.ReadLine

    'query the computer
    On Error Resume Next
    Set objWMIService = GetObject("winmgmts:\\" & strComputer & _
        "\\root\\cimv2")
    If Err = 0 Then
        'no error connecting - query the info
        Set colItems = objWMIService.ExecQuery("SELECT * " & _
            "FROM Win32_OperatingSystem")

        'build the output HTML cells
        For Each objItem in colItems
            strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
            strHTML = strHTML & "<td>" & objItem.BuildNumber & "</td>" & vbCrLf
            strHTML = strHTML & "<td>" & objItem.ServicePackMajorVersion & _
                "." & objItem.ServicePackMinorVersion & "</td>" & vbCrLf
        Next

        'finish the HTML row
        strHTML = strHTML & "</tr>"
    Else
        'error connecting
        strHTML = strHTML & "<tr>" & vbCrLf
        strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
        strHTML = strHTML & "<td>?</td>" & vbCrLf
        strHTML = strHTML & "<td>?</td>" & vbCrLf
        strHTML = strHTML & "</tr>" & vbCrLf
    End If
    On Error GoTo 0

Loop

'close the text file
objTS.Close

'close the table
strHTML = strHTML & "</table>" & vbCrLf

'display the table
DisplayOutputInIE(strHTML)
```

```
Sub DisplayOutputInIE(strHTML)
    Dim objIE
    Set objIE = CreateObject("InternetExplorer.Application")
    objIE.Navigate "about:blank"
    objIE.Document.body.innerHTML = strHTML
    objIE.Visible = True
End Sub
```

现在，如果我们需要另一个在弹出式 Internet Explorer 窗口中显示信息的 HTA，我们只需复制并粘贴 *DisplayOutputInIE* 子例程即可。它已经过调试并可以工作，因此我们将为自己节省大量时间。

> **最佳实践** 管理脚本——实际上，*VBScript* 这个词本身——经常被许多软件开发者甚至 IT 经理所看不起。这是因为太多管理员在创建脚本时未能遵循基本的最佳实践，从而导致管理员声名狼藉。避免这种污名的一种方法是在脚本中遵循软件开发的行业最佳实践，特别是模块化。一般规则是，如果一段脚本可以在同一脚本或不同脚本中使用多次，则将该片段拆分为自己的函数或子例程。我们不会总是对本书中的脚本这样做，当我们这样做时，我们也不会总是尽可能地模块化。我们为本书做出这个决定是为了帮助保持脚本更清晰、更易于理解。但我们坚信，您应该尽可能地进行模块化。

现在我们可以开始处理 HTA 本身了。在开始处理 HTA 之前，您需要掌握一些基础知识。在接下来的几节中，我们将介绍这些背景材料并提供一些代码片段。我们将在最后一节“*在操作中查看 HTA*”中，将这些不同的知识与我们最初的 VBScript 示例结合，创建最终的、功能性的 HTA。

## 理解 HTA 的要求和基本要素

在接下来的几节中，我们将讨论构建 HTA 的一些基本规则，并介绍在开始使用编辑器之前需要做出的一些设计决策。

> **提示** 我们在接下来的几节中向您展示的许多内容可能很难记住，尤其是 HTML 标签格式。不过，有一些工具可以使这些内容变得更容易。免费的 HTA Helpomatic 是一个 Microsoft 工具，可以为您生成各种 HTML 和 HTA 相关格式的示例。（下载地址：http://www.microsoft.com/technet/scriptcenter/hubs/htas.mspx。此链接包含在 CD 上；单击 *HTA Helpomatic*。）如果您使用商业工具作为开发环境，请联系 Scripting Outpost (http://www.scriptingoutpost.com) 了解他们的 HTA Snippets Pack。这些代码片段集成到 PrimalScript 环境中，允许您将 HTML 和 HTA 元素拖放到脚本中。



### 使用 HTA 标签

只有两件事真正将 HTA 与网页区分开来。首先，HTA 使用文件扩展名 `.hta`。正是这个文件扩展名告知 Windows 在 Mshta.exe 中执行文件，而不是直接在 Internet Explorer 中执行。其次，HTA 包含一个特殊标签，称为 HTA 标签，它告诉 Mshta.exe 关于 HTA 应该如何外观、如何执行等一系列细节。

HTA 标签必须出现在 HTML 页面的 head 标签内。HTML 页面的 head 部分不包含用于显示的常规 HTML 标签；相反，它包含许多其他类型的标签——包括你的 VBScript 代码将存储于其中的标签——这些标签为应用程序提供后台信息和支持功能。完整的 HTA 标签如下所示。

```
<hta:application
    applicationname="MyHTA"
    border="dialog"
    borderstyle="normal"
    caption="My HTML Application"
    contextmenu="false"
    icon="myicon.ico"
    maximizebutton="false"
    minimizebutton="true"
    navigable="false"
    scroll="false"
    selection="false"
    showintaskbar="true"
    singleinstance="true"
    sysmenu="true"
    version="1.0"
    windowstate="normal"
/>
```

其中几乎一切都是可选的。至少，你的 HTA 标签需要包含以下信息。

```
<hta:application />
```

通过使用众多可选属性，你可以显著自定义 HTA 的外观和行为。完整的属性列表如下。

- `applicationname` 属性为你的应用程序分配一个名称。
- `border` 属性决定 HTA 窗口将具有的边框类型。默认是厚边框，包括可调整大小的边缘和右下角的尺寸抓取图形元素。你也可以指定以下内容：
    - `Thin`。一个可调整大小但缺少尺寸抓取元素的边框
    - `None`。无边框
    - `Dialog`。一个固定（不可调整大小）的边框
- `borderstyle` 属性控制窗口边框的外观。默认为 `normal`，但你也可以指定以下内容：
    - `Complex`。一个凸起和凹陷的边框
    - `Raised`。一个凸起的 3D 边框
    - `Static`。一个通常用于不接受用户输入窗口的 3D 边框
    - `Sunken`。一个凹陷的 3D 边框
- `caption` 属性指定 HTA 窗口标题栏中显示的文本。
- `contextmenu` 属性，设置为 `TRUE` 或 `FALSE`，指示右键单击 HTA 是否会显示 Internet Explorer 上下文菜单。因为传统的 Windows 应用程序不会这样做，所以将 `ContextMenu="false"` 设置得更符合 Windows 应用程序的行为。
- `icon` 属性设置将用作应用程序窗口和任务栏图标的 `.ico` 文件的名称。如果省略此项，将使用标准的 Mshta.exe 图标。此属性的一个缺点是无法将图标文件与 HTA 文件捆绑在一起。最好指定一个可通过 UNC（可能在文件服务器上）或 URL（可能在内部网 Web 服务器上）访问的图标文件，而不是本地硬盘上的图标。
- `innerborder` 属性在 HTA 周围显示一个 3D 内边框。将其设置为 `No` 可抑制内边框。默认值为 `Yes`。
- `maximizebutton` 属性，当设置为 `TRUE` 时，显示一个最大化 HTA 窗口的按钮。我们建议将其设置为 `FALSE`，因为 HTA 的布局在全屏显示时通常不如其创建时的任何大小看起来好。
- `minimizebutton` 属性，当设置为 `TRUE` 时，显示一个将 HTA 最小化到任务栏的按钮。将其设置为 `FALSE` 会隐藏该按钮。
- `navigable` 属性，当设置为 `TRUE` 时，指定 HTA 中的任何超链接都将在 HTA 中打开，从而导航离开你的 HTA 内容。我们建议将其设置为 `FALSE`，以便任何超链接都将在新的 Internet Explorer 窗口中打开，同时保持你的 HTA 处于打开状态。
- `scroll` 属性，当设置为 `TRUE` 时，在 HTA 的主区域显示滚动条。将其设置为 `FALSE` 会隐藏滚动条。
- `scrollflat` 属性，当设置为 `TRUE` 时，显示平面或 3D 滚动条。将其设置为 `FALSE` 会隐藏滚动条。
- `selection` 属性，当设置为 `TRUE` 时，允许选择 HTA 中的文本。我们建议将其设置为 `FALSE` 以模仿传统 Windows 应用程序的行为。将其设置为 `FALSE` 不会阻止文本框和其他输入控件中的文本被选择，只会阻止你在 HTA 中创建的静态文本被选择。
- `showintaskbar` 属性，当设置为 `TRUE` 时，允许 HTA 在 Windows 任务栏中显示。将其设置为 `FALSE` 会禁止 HTA 在任务栏中显示。
- `singleinstance` 属性，当设置为 `TRUE` 时，允许一次只运行一个 HTA 副本。如果设置为 `FALSE`，则可以运行多个副本。当设置为 `TRUE` 时，如果用户在 HTA 已经运行时双击 HTA 文件，当前运行的实例将出现在前台，而不是启动新的 HTA 副本。
- `sysmenu` 属性，当设置为 `TRUE` 时，显示系统菜单，通常位于窗口标题栏的左上角。如果你将此项设置为 `FALSE`，最小化、最大化和还原按钮也将被隐藏。
- `version` 属性设置 HTA 的版本号。这可以是任何你喜欢的值。
- `windowstate` 属性指定 HTA 的初始窗口状态。默认值 `normal` 使用 Internet Explorer 指定的默认值。你也可以指定以下内容：
    - `Minimize`。窗口仅在任务栏中显示。但是，如果 `showIn-TaskBar` 属性为 `FALSE`，窗口将不会显示，用户将无法访问它。
    - `Maximize`。窗口将最大化，覆盖整个屏幕。

> **注意** 从技术上讲，`application` 属性也可以有一个值。指定 `hta:application` 等同于 `hta:application="no"`，这将应用默认的 HTA 安全模型。此模型阻止框架内的不受信任内容访问 HTA 或被 HTA 访问。指定 `hta:application="yes"` 可强制所有框架内容受信任。这是一个相当罕见的要求，通常只有在你的 HTA 实现了一个包含来自另一个内部网 Web 服务器内容的框架时才会这样做。由于它太罕见，我们将在本书中不涵盖这种情况。

`HTA` 标签允许你对 HTA 的初始外观和行为进行大量控制。

> **提示** HTA 属性通常可以接受 `true` 或 `yes` 表示真，`false` 或 `no` 表示假。MSDN Library 中的 HTA 文档更倾向于使用 `yes` 和 `no`。

### 调整 HTA 大小

使用 `HTA` 标签无法做到的一件事是指定 HTA 窗口的初始大小。强制 HTA 窗口为特定大小的唯一方法是在运行时执行。`window` 对象的 `onLoad` 事件总是在 HTA 加载时运行，甚至在用户开始与 HTA 交互之前。`window` 对象代表 HTA 运行所在的窗口，你可以控制其 `height`、`width`、`left` 和 `top` 属性来调整其在屏幕上的大小和位置。

```
Sub window_onLoad()
    window.moveTo(10,10)
    window.resizeTo(640,480)
End Sub
```

这将强制窗口将自身定位到距离屏幕左边缘 10 像素、距离屏幕顶部边缘 10 像素的位置，并将自身大小调整为 640 像素宽、480 像素高。此事件处理程序会自动运行；你无需做任何特殊处理，只需将其包含在你的 HTA 中即可。

> **提示** `window_onLoad` 事件也是放置任何用于设置 HTA 的脚本代码的好地方。例如，你可以动态填充列表框、设置选项默认值等。

### 使用 `<div>` 和 `<span>` 标签

在前面的示例中，我们向你展示了用于更改按钮文本标签的代码。这可能不是你会在脚本中经常做的事情。然而，你可能*经常*做的是显示动态消息。例如，在我们的示例中，我们可能希望在脚本运行清单部分时显示诸如 *正在清点计算机* 之类的消息。然后我们可能希望在清单完成后将该消息更改为 *清单完成*。在 HTA 中显示此类动态消息很容易，前提是你在初始布局或设计中为其留出了空间。

Division，即 `<div>` 标签，让你为动态消息留出空间。`<div>` 标签只是定义了一个 HTML 文档区域。因为你可以给 `<div>` 标签一个 `id` 属性，所以你可以从脚本代码中引用它。`<div>` 标签有一个 `innerHTML` 属性，因此你可以控制出现在开始 `<div>` 标签和结束 `<div>` 标签之间的内容。Internet Explorer 也支持一个类似的标签，称为 `<span>`。就编写 HTA 而言，两者之间没有太大区别。存在的任何差异都可以追溯到 Microsoft 和 Netscape 探索扩展 HTML 用途的时代。一家公司想出了 `<div>` 标签；另一家想出了 `<span>` 标签。使用你喜欢的任意一个。两者在显示方式上有一些细微差别：例如，`<div>` 标签会创建换行符。然而，就编写 HTA 而言，你可能不会太注意到这些差异。在 Scriptomatic 代码中，你会在第 1403 行附近注意到两个 `<span>` 标签。

```
<span id="wmi_namespaces"></span>
<span id="wmi_classes"></span>
```



### 使用内联框架

如果你对HTML不太熟悉，内联框架——或者像网络开发人员喜欢称呼的那样，IFrame——可能看起来不太直观。本质上，IFrame定义了一个矩形区域，用于显示网页的内容。图5-4展示了一个正在使用的内联框架，清单5-4则是实现它的HTML代码。

这是主页面。

![](img/4fefd6988ba5d4a92a65127617ca24c2_164_0.png)

这是主页面。

**图5-4** 带有内联框架的页面

请注意，这些元素最初没有内部文本或HTML，因此当HTA首次加载时，它们将完全不可见。然而，它们确实具有`id`属性，允许通过脚本代码进行修改。首次引用`wmi_classes` span是在第194行。

```
wmi_classes.innerHTML = "<div style='\"font-size:8pt;color:red;\"'>Please wait, trying to load WMI Classes in namespace '" & .namespacespulldown.value & " ...</div>"
```

这修改了span的*innerHTML*属性，该属性初始为空。脚本插入了一个`<div>`标签（包含用于显示红色文本的格式）和一条消息。

> **注意** 你会发现许多HTA开发者使用`<span>`标签作为动态文本的占位符，比如这个*请稍候*消息，并使用`<div>`标签来应用格式。这是一种完全可接受的做法，如果你觉得它方便易懂，我们鼓励你使用它。

创建动态消息区域就是这么简单。只需使用带有ID的`<span>`或`<div>`标签定义消息的位置，然后通过修改标签的`innerHTML`属性来显示消息。

# 第二部分：打包你的脚本

```
清单5-4 内联框架
<p>This is the main page.</p>
<p><iframe name="I1" src="http://www.scriptinganswers.com">
Your browser does not support inline frames or is currently configured not to display
inline frames.
</iframe></p>
<p>This is the main page.</p>
```

`<iframe>`标签负责创建内联框架。与其他标签一样，它可以有一个`id`属性（尽管在这个简单的示例中没有），以及一个`src`属性，用于告诉IFrame在内联框架区域内显示什么内容。可以指定其他属性来控制IFrame的大小、是否有滚动条、周围是否有边框等。

你可以将IFrame想象成一个完全包含在你定义的矩形区域内的迷你Internet Explorer浏览器。正如我们之前解释的，你的HTA通常无法访问IFrame的内容，但你可以控制`<iframe>`标签本身，这意味着你可以控制IFrame显示的内容。例如，你可以在HTA中放置以下代码。

```
<p>This is the main page.</p>
<p><iframe id="myiframe" name="I1" src="http://www.scriptinganswers.com">
Your browser does not support inline frames or is currently configured not to display
inline frames.
</iframe></p>
<p>This is the main page.</p>
```

在其他地方，你可能有如下脚本。

```
myiframe.src = "http://www.microsoft.com"
```

这将导致IFrame显示Microsoft.com主页。但是，你的脚本将无法访问Microsoft主页的Internet Explorer DOM，除非你使用我们之前描述的`<hta:application="true">`标签，该标签会禁用跨框架安全预防措施。

> **重要** 禁用跨框架安全意味着你的代码可以访问IFrame的内容，同时也意味着IFrame——以及它可能包含的任何脚本——可以访问你的HTA的内容。如果你打算这样做，请绝对确保你信任加载到IFrame中的任何内容。

内联框架也可用于显示信息。例如，在我们的示例HTA中，我们希望输出显示在弹出窗口中。然而，我们同样可以在HTA中设计一个内联框架，并在那里显示输出。内联框架只是你在HTA中显示信息的另一种选择。

## 处理表单和字段

大多数管理员使用HTA的主要原因之一是为了获得更强大的输入能力。毕竟，VBScript内置的*InputBox*函数——唯一的图形化收集用户输入的方式——有点受限。HTML表单和输入控件（或*字段*）提供了更大的灵活性。

也许最基本的输入控件是文本框，HTML包含三种类型。

- *文本框*是一个简单的单行输入字段。
- *文本区域*是一个用于输入多行文本的框。
- *密码框*在功能上模仿文本框，但会遮盖输入的内容。

文本框和密码框通过使用HTML `<input>`标签实现，而文本区域有其特殊的`<textarea>`标签。它们看起来是这样的。

```
<input type="text" id="txtName">
<input type="password" id="txtPassword">
<textarea id="txtStory"></textarea>
```

请注意，每个都带有一个*id*属性，允许从脚本中引用。

通常，我们认为手动输入HTML标签不是个好主意。市场上有许多优秀的商业所见即所得（WYSIWYG）HTML编辑器，没有理由不使用它们。Microsoft FrontPage是你可能熟悉并能轻松获取的一个。然而，FrontPage的一个问题，至少从HTA的角度来看，是它有点过度设计了。这是FrontPage创建的一段HTML片段。它包含了三种类型的输入控件。

```
<form method="POST" action="--WEBBOT-SELF--">
<!--webbot bot="SaveResults" U-File="fpweb:////private/form_results.csv" S-Format="TEXT/CSV"
S-Label-Fields="TRUE" -->
<p><input type="text" name="T1" size="20"></p>
<p><input type="password" name="T2" size="20"></p>
<p><textarea rows="2" name="S1" cols="20"></textarea></p>
<p><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset"
name="B2"></p>
</form>
```

你需要对这段代码进行一些修改，使其更适合在HTA中使用。只需几个步骤。

1.  删除`<form>`标签。
2.  删除`<!--webbot -->`标签。
3.  为每个输入控件添加一个唯一的*id*属性。为了清晰起见，将*name*属性更改为与*id*属性匹配。
4.  删除Submit或Reset按钮，并为你的应用程序添加常规按钮。

FrontPage或其他WYSIWYG HTML编辑器可以使创建复杂、外观专业的应用程序变得容易得多，所以我们认为值得花点时间去清理它们创建的HTML，使其更适合HTA。实际操作输入控件——在脚本中读取它们的值，以及在运行时修改它们——可能有点复杂。在接下来的几节中，我们将涵盖你需要知道的一切。

### 填充列表框

使用FrontPage（或你使用的任何编辑器）创建下拉列表框（或普通的滚动列表框）很容易。你可以使用编辑器提供的工具向列表框添加选项。但是，在某些情况下，你希望动态地向列表中添加项目。例如，当你选择一个WMI命名空间时，Scriptomatic HTA会确定该命名空间中有哪些类，并将它们添加到下拉列表框中。两种类型的列表框都使用`<select>`标签定义。这是一个带有两个选项的下拉列表。

```
<select size="1" name="lstOptions">
<option>Option 1</option>
<option>Option 2</option>
</select>
```

将其更改为滚动列表框只需改变一件事。

```
<select size="3" name="lstOptions">
<option>Option 1</option>
<option>Option 2</option>
</select>
```

你能看出区别吗？在第二个示例中，列表框的大小为3，使其高度为三行。在第一个选项中，列表框的大小为1，这迫使其成为下拉列表框。选项——即列表中的项目——由`<option>`标签定义，这些标签包含在列表框的`<select>`标签内。`<option>`标签之间的文本会出现在列表框中。你可以指定一个值来代表该选项。如果不指定值，则使用选项的文本作为其值。这是一个例子。

```
<option value="1">Option 1</option>
<option>Option 2</option>
```

要动态地向列表框添加选项，请添加一个新的`<option>`标签。这是一个例子。

```
Dim objOption
Set objOption = document.createElement("OPTION")
objOption.Text = "Option 3"
objOption.Value = "3"
lstOptions.Add(objOption)
```

这将第三个选项添加到我们的列表中，文本为*Option 3*，值为3。



### 创建按钮

我们已经提到过，您不应使用“提交”和“重置”按钮类型。提交按钮旨在将表单内容发送到 Web 服务器进行处理。HTA 通常是自包含的，不依赖于 Web 服务器，因此提交按钮是无用的。重置按钮用于清除表单字段，您可能会觉得这有用，但我们曾误点过几次这些按钮，所以我们建议直接省略它们。

不过，您将需要按钮；事实上，Scriptomatic HTA 就有几个。幸运的是，按钮是最容易创建的 HTML 元素之一。

```
<input type="button" value="OK" name="btnOK">
```

这是直接从 FrontPage 导出的，您会注意到它缺少一个 *id* 属性，您需要添加它。*value* 属性决定了按钮正面显示的标签，而 *type* 属性表明这是一个普通按钮，而不是提交或重置按钮。

### 将按钮连接到脚本

通常，您的 HTA 只在有人点击按钮时才执行操作，因此将按钮连接到脚本非常重要。我们已经简要讨论过事件处理程序——它们是您编写脚本以响应按钮点击的方式。连接事件处理程序有两种主要方法。第一种是简单地使用特殊事件处理程序名称编写一个子例程。

```
Sub btnOK_OnClick()
    'your code goes here
End Sub
```

这需要出现在 `<script language="vbscript">` 标签和 `</script>` 标签之间，而这两个标签又位于 HTA 的 *head* 部分内。此方法通常适用于大多数按钮。然而，您可能希望将多个按钮连接到一个事件处理程序。例如，也许您有两个按钮将执行非常相似的操作。一个简单的方法是按如下方式创建按钮。

```
<input type="button" value="OK" name="btnOK" id="btnOK1" onClick="DoButton">
<input type="button" value="OK" name="btnOK" id="btnOK2" onClick="DoButton">
```

这会将两个按钮的 *onClick* 事件都连接到 *DoButton* 子例程。按如下方式编写该子例程。

```
Sub DoButton()
    Select Case window.event.srcElement.id
        Case "btnOK1"
            'your code for btnOK1 goes here
        Case "btnOK2"
            'your code for btnOK2 goes here
    End Select
End Sub
```

特殊的 *window.event.srcElement* 对象引用了生成上一个事件的任何对象——在本例中，是这两个按钮之一。通过检查对象的 *id* 属性，您可以快速确定点击了哪个按钮，并采取相应的操作。

### 使用复选框和单选按钮

复选框和单选按钮是向 HTA 用户显示选项的有用方式。它们在所见即所得编辑器中很容易创建，也可以使用以下 HTML 手动创建。

```
<input type="checkbox" name="chkCheckbox" value="ON" checked>My Checkbox
<input type="radio" value="Value1" checked name="optButton">My Radio Button 1
<input type="radio" name="optButton" value="Value2">My Radio Button 2
```

请注意以下几点。

-   FrontPage 没有为这些元素添加 *id* 属性，因此您需要手动添加。一如既往，尝试保持 *id* 和 *name* 属性相同，以便于使用。
-   复选框和单选按钮（也称为 *选项按钮*）元素只创建实际的复选框或单选按钮；与元素一起的文本是单独插入的。
-   如果复选框中存在 *checked* 属性，则复选框的默认状态为选中。要使默认状态为未选中，请省略 *checked* 属性。
-   两个单选按钮具有相同的 *name* 属性。这使它们成为同一组的一部分，意味着一次只能选中其中一个。它们还应具有相同的 *id* 属性，以便可以编写脚本。
-   其中一个单选按钮具有 *checked* 属性，这意味着它是默认选中的那个。

在脚本中检查这些元素的值很简单。对于单选按钮，只需访问元素的 *value* 属性。尽管会存在多个具有相同 *id* 属性的元素，但 *value* 属性将对应于用户选择的单选按钮的 *value* 属性。在这个简单的示例中，如果用户选择第二个单选按钮，*optButton.Value* 将等于 *Value2*。

复选框的工作方式类似。当被选中时，它们的 *value* 属性将返回您设置的 *value* 属性值（在本例中为 *ON*）。当未选中时，*value* 属性将包含一个空字符串。您可以像这样检查其值。

```
If chkCheckbox.value = "ON" Then
    'checked
Else
    'not checked
End If
```

### 添加图形

图形很容易添加到 HTA 中。显然，所见即所得编辑器使得插入图像变得容易，但您也可以手动构建 HTML 标签。

```
<img src="mygraphic.gif">
```

默认情况下，图形必须与 HTA 本身包含在同一文件夹中。与引用外部脚本一样，您需要确保将图形与 HTA 一起分发。为了使您的 HTA 更易于分发，您可以将图形放在文件服务器或 Web 服务器上，让 HTA 从中获取。由于这点额外的复杂性，我们尽量减少在 HTA 中使用图形。

### 添加子例程和函数

您所有的脚本代码——事件处理程序以及您编写的任何其他子例程和函数——都必须出现在特殊标签内，这些标签告诉 Windows 您使用的是哪种脚本语言。因此，一个（尚未）包含脚本代码的 HTA 的开头大致如下所示。

```
<html>
<head>
<script language="vbscript">
</script>
<hta:application>
</head>
<body>
```

在 `<body>` 标签之后，您插入创建 HTA 可视界面的 HTML。首先，您指定使用的语言（可以是 VBScript 或 JScript）。JScript 是默认语言，因此如果您不指定 VBScript，将会遇到错误。

其次，您可以使用多个脚本部分。如果您打算将所有代码都包含在 HTA 文件本身中（就像 Scriptomatic 和许多其他 HTA 那样），则不需要多个脚本部分。Scriptomatic HTA 将其所有代码都包含在一个脚本部分中。但是，假设您想包含一个充满标准子例程的文件，这些子例程在几个 HTA 中使用。您可能有一个脚本部分包含特定 HTA 的事件处理程序，第二个脚本部分包含一个包含这些标准子例程的外部文件。

```
<script language="vbscript">
Sub btnOK_onClick()
End Sub

Sub btnCancel_onClick()
End Sub
</script>
<script language="vbscript" src="c:\scripts\standard.vbs" />
```

**最佳实践**：将常用子例程保存在外部文件中是个好主意，因为您对这些子例程所做的任何更改（例如错误修复）都只需要进行一次。如果您养成了将代码复制粘贴到多个 HTA 中的习惯，那么任何更改都必须进行多次，这可能会导致错误、遗漏 HTA 以及其他潜在问题。

第二个脚本部分包含一个名为 C:\Scripts\Standard.vbs 的外部文件。这种技术的一个缺点是您的 HTA 不再是自包含的；为了正常运行，它必须能够访问该外部文件。如果您要分发 HTA，则需要将此额外文件与之一处分发，或者将该外部文件放在可访问的区域，例如文件服务器。

**注意**：包含外部文件并不能防止他人查看您的脚本代码。要运行 HTA，用户必须对 HTA 文件以及 HTA 引用的任何外部脚本具有读取权限。用户可以利用这些读取权限直接打开外部脚本，并随意读取。

### 查看 HTA 运行实例

现在我们将向您展示如何从头开始构建一个 HTA。我们将使用清单 5-3，因为它已经过调试，并且具有我们需要的大部分功能。我们首先使用 FrontPage 等编辑器来设计 HTA 的可视界面。我们希望 HTA 具有一些额外的功能，因此我们可以将这些功能设计到界面中。图 5-5 显示了 FrontPage 中的界面，下一页的清单 5-5 是 HTML。请注意，此 HTML 是直接从 FrontPage 导出的；我们还没有对其进行修改或将其制成 HTA。

![](img/4fefd6988ba5d4a92a65127617ca24c2_171_0.png)



## 第5章：带用户界面的HTML应用程序：脚本

155

### 清单5-5 基础HTML

```html
<html>

<head>
<meta http-equiv="Content-Language" content="en-us">
<meta http-equiv="Content-Type" content="text/html; charset=windows-1252">
<title>Computer Inventory Tool</title>
</head>

<body>

<p align="center"><b>Computer Inventory Tool</b></p>
<form method="POST" action="--WEBBOT-SELF--">
<!--webbot bot="SaveResults" U-File="C:\Documents and Settings\DonJones\My Documents\Customer Files\MSPress\AdvancedScripting\Manuscript and CD\On The CD\Scripts\Chap5\_private\form_results.csv" S-Format="TEXT/CSV" S-Label-Fields="TRUE" -->
<p align="left">Inventory the following computers (one per line):<br>
<textarea rows="4" name="txtComputers" cols="40"></textarea><input type="button" value="Load From File" name="btnLoadFromFile"></p>
<p align="left">Inventory this information:<br>
<input type="checkbox" name="chkServicePack" value="ON">Service pack major version<br>
<input type="checkbox" name="chkBuild" value="ON">Windows build<br>
<input type="checkbox" name="chkVersion" value="ON">Version<br>
<input type="checkbox" name="chkSerialNumber" value="ON">Serial number</p>
<p align="left"><input type="button" value="OK" name="btnOK"></p>
</form>

</body>

</html>
```

现在我们需要将其转换为HTA。除了更改文件名外，我们还将移除FrontPage表单标签、添加一个脚本部分、添加*HTA*标签以及添加*id*属性。清单5-6展示了这些更改。

### 清单5-6 HTA修改

```html
<html>

<head>
<meta http-equiv="Content-Language" content="en-us">
<meta http-equiv="Content-Type" content="text/html; charset=windows-1252">
<title>Computer Inventory Tool</title>
<script language="vbscript">

</script>
<hta:application>
</head>

<body>

<p align="center"><b>Computer Inventory Tool</b></p>
<p align="left">Inventory the following computers (one per line):<br>
<textarea id="txtComputers" rows="4" name="txtComputers" cols="40"></textarea><input type="button" value="Load From File" id="btnLoadFromFile" name="btnLoadFromFile"></p>
<p align="left">Inventory this information:<br>
<input type="checkbox" id="chkServicePack" name="chkServicePack" value="ON">Service pack major version<br>
<input type="checkbox" id="chkBuild" name="chkBuild" value="ON">Windows build<br>
<input type="checkbox" id="chkVersion" name="chkVersion" value="ON">Version<br>
<input type="checkbox" id="chkSerialNumber" name="chkSerialNumber" value="ON">Serial number</p>
<p align="left"><input id="btnOK" type="button" value="OK" name="btnOK"></p>
</body>
</html>
```

> **最佳实践** 注意我们为各种控件类型使用了前缀：复选框用*chk*，按钮用*btn*，等等。这种称为*匈牙利命名法*的命名约定是一种最佳实践，因为它有助于识别脚本中所引用的对象类型。它与用于变量名的命名约定非常相似，例如使用*str*作为包含字符串数据的变量的前缀。

现在我们只需要添加功能。我们只有两个按钮，而且`btnOK`按钮的大部分代码在清单5-3中已经处理好了。我们需要对代码进行以下修改。

-   将`txtComputers`的内容提取到一个字符串数组中，而不是从文本文件中读取名称。
-   根据选中的复选框添加输出。
-   根据选中的复选框添加适当的列标题。
-   为`btnLoadFromFile`添加一个事件处理程序，提示输入文件名，然后将文件内容读取到计算机名称文本区域。

清单5-7是完成的HTA。

### 清单5-7 完成的清单HTA

```html
<html>

<head>
<meta http-equiv="Content-Language" content="en-us">
<meta http-equiv="Content-Type" content="text/html; charset=windows-1252">
<title>Computer Inventory Tool</title>
<script language="vbscript">
Sub btnOK_onClick
    Dim arrComputers, strComputer, objWMIService, colItems, objItem, strHTML

    'get the computer names into a string
    'and split it into an array
    arrComputers = Split(txtComputers.InnerText,vbcrlf)

    'create the starting HTML
    strHTML = "<table border=1>" & vbCrLf
    strHTML = strHTML & "<tr>" & vbCrLf
    strHTML = strHTML & "<td>Computer</td>" & vbCrLf
    if chkBuild.value = "ON" Then
        strHTML = strHTML & "<td>Build</td>" & vbCrLf
    end if
    if chkServicePack.value = "ON" Then
        strHTML = strHTML & "<td>Service Pack</td>" & vbCrLf
    end if
    if chkVersion.value = "ON" Then
        strHTML = strHTML & "<td>Version</td>" & vbCrLf
    end if
    if chkSerialNumber.value = "ON" Then
        strHTML = strHTML & "<td>Serial Number</td>" & vbCrLf
    end if

    'read through the array
    For Each strComputer in arrComputers

        'add a table row to the HTML
        strHTML = strHTML & "<tr>" & vbCrLf

        'query the computer
        On Error Resume Next
        Set objWMIService = GetObject("winmgmts:\\" & strComputer & _
            "\\root\\cimv2")
        If Err = 0 Then
            'no error connecting - query the info
            Set colItems = objWMIService.ExecQuery("SELECT * " & _
                "FROM win32_OperatingSystem")

            'build the output HTML cells
            For Each objItem In colItems
                strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
                if chkBuild.value = "ON" Then
                    strHTML = strHTML & "<td>" & objItem.BuildNumber & "</td>" & vbCrLf
                end if
                if chkServicePack.value = "ON" Then
                    strHTML = strHTML & "<td>" & objItem.ServicePackMajorVersion & "</td>" & vbCrLf
                end if
                if chkVersion.value = "ON" Then
                    strHTML = strHTML & "<td>" & objItem.Version & "</td>" & vbCrLf
                end if
                if chkSerialNumber.value = "ON" Then
                    strHTML = strHTML & "<td>" & objItem.SerialNumber & "</td>" & vbCrLf
                end if
            Next
            'finish the HTML row
            strHTML = strHTML & "</tr>"
        Else
            'error connecting
            strHTML = strHTML & "<tr>" & vbCrLf
            strHTML = strHTML & "<td>" & strComputer & "</td>" & vbCrLf
            strHTML = strHTML & "<td>?</td>" & vbCrLf
            strHTML = strHTML & "</tr>" & vbCrLf
        End If
        On Error GoTo 0

    Next

    'close the table
    strHTML = strHTML & "</table>" & vbCrLf

    'display the table
    DisplayOutputInIE(strHTML)
End Sub

Sub DisplayOutputInIE(strHTML)
    Dim objIE
    Set objIE = CreateObject("InternetExplorer.Application")
    objIE.Navigate "about:blank"
    objIE.Document.body.innerHTML = strHTML
    objIE.Visible = True
End Sub

Sub btnLoadFromFile_onClick()
    Dim objFSO, objTS, strFile
    Set objFSO = CreateObject("Scripting.FileSystemObject")
    strFile = InputBox("Path and filename to load?")
    If objFSO.FileExists(strFile) Then
        Set objTS = objFSO.OpenTextFile(strFile)
        txtComputers.innerText = objTS.ReadAll
        objTS.Close
    Else
        MsgBox("File does not exist.")
    End If
End Sub

</script>
<hta:application>
</head>

<body>

<p align="center"><b>Computer Inventory Tool</b></p>
<p align="left">Inventory the following computers (one per line):<br>
<textarea id="txtComputers" rows="4" name="txtComputers" cols="40"></textarea><input type="button" value="Load From File" id="btnLoadFromFile" name="btnLoadFromFile"></p>
<p align="left">Inventory this information:<br>
<input type="checkbox" id="chkServicePack" name="chkServicePack" value="ON">Service pack major version<br>
<input type="checkbox" id="chkBuild" name="chkBuild" value="ON">Windows build<br>
<input type="checkbox" id="chkVersion" name="chkVersion" value="ON">Version<br>
<input type="checkbox" id="chkSerialNumber" name="chkSerialNumber" value="ON">Serial number</p>
<p align="left"><input id="btnOK" type="button" value="OK" name="btnOK"></p>

</body>
</html>
```

就是这么多！我们的工作之所以变得更容易，是因为我们有一个现成的、已经调试过的脚本，其中包含了我们需要的大部分功能。通过调整该代码的次要部分并将其与在FrontPage中开发的简单HTML页面合并，我们创建了一个完整的HTA。

### 总结

在本章中，你了解到HTA是一种结合了VBScript和HTML格式以创建类似Windows应用程序的脚本类型。我们向你展示了一种方法，可以帮助你将独立的VBScript快速转换为完整的HTA，并解释了帮助你更有效地调试和排查HTA问题的方法。然而，请记住，HTA并非适用于所有情况的完美解决方案。有时，特别是对于你将自己使用的脚本来说，创建一个外观精美的HTA所付出的努力可能不值得。但对于你计划与他人（尤其是技术知识较少的用户）共享的脚本，HTA可以通过集成熟悉的Windows用户界面元素，使脚本变得更加友好易用。

> **更多信息** 在使用HTA时，你会发现官方的HTA文档以及Internet Explorer动态HTML（DHTML）文档都很有用。HTA文档位于：
http://msdn.microsoft.com/library/default.asp?url=/workshop/author/hta/hta_node_entry.asp
（此链接在配套CD上；点击*HTML Applications*。）DHTML文档位于以下网站。
http://msdn.microsoft.com/library/default.asp?url=/workshop/author/dhtml/reference/dhtml_reference_entry.asp
（此链接在配套CD上；点击*HTML and DHTML Reference*。）
因为这些位置可能会更改，你也应该知道如何手动访问这些站点。转到http://msdn.microsoft.com/library，在左侧树中点击Web development，在右侧窗格点击HTML And DHTML或在左侧窗格点击HTML And CSS，然后点击HTML Applications。



# 第三部分

## 高级脚本技术、工具与技术

本部分内容：
第6章：远程脚本 161
第7章：数据库脚本 179
第8章：高级ADSI和LDAP脚本 207
第9章：结合使用ADO和ADSI 245
第10章：高级WMI脚本 261
第11章：WMI事件 285
第12章：利用WMI工具优化脚本 319
第13章：在Windows XP和Windows Server 2003中的高级脚本 353

# 第6章

## 远程脚本

- **本章内容：**
  - 理解远程脚本与安全 162
  - 处理Windows防火墙 170
  - 理解远程脚本对象 171
  - 理解远程脚本方法 172
  - 查看远程脚本的实际应用 175
  - 总结 177

远程脚本主要有两种类型。第一种类型涉及运行一个连接到远程计算机并在该远程计算机上执行任务的脚本。第二种类型涉及将脚本部署到远程计算机，然后在远程计算机上运行这些脚本。本章我们将探讨这两种远程脚本，包括你可能遇到的安全问题和困难，你将使用的技术和方法，以及你可以预期获得的好处。

管理脚本的一个好处是能够编写在其他计算机上执行任务的脚本。Windows管理规范（WMI）和活动目录服务接口（ADSI）可能是目前可用的两种最佳远程脚本技术。例如，WMI可用于编写获取远程计算机信息，甚至修改这些计算机配置的脚本。然而，远程脚本也伴随着一定的困难和挑战，我们将在本章帮助你理解和解决它们。

在开始之前，让我们先明确术语。不幸的是，*远程脚本* 这个术语有点模糊，因为它指的是两种涉及完全不同技术的不同技术。为了避免混淆，我们将创造一些新术语。我们将使用术语 *部署脚本* 来指代那种将脚本从你的计算机物理复制到远程计算机，然后在远程计算机上执行的远程脚本类型。我们将使用术语 *连接脚本* 来指代那些在你的计算机上执行，但连接到远程计算机以在其上执行任务的脚本。这些不是你可能在其他地方遇到的行业标准术语；我们仅在本章中使用这些术语，以帮助清晰区分这两种不同类型的远程脚本。

### 理解远程脚本与安全

随着Microsoft Windows成为一个更安全的操作系统，在远程计算机上执行管理任务的难度变得更加复杂。此外，Windows操作系统的底层架构——包括在同一台计算机上拥有多个用户配置文件的能力——可能会使远程脚本变得有些复杂。任何类型的远程脚本通常都需要你处理几个安全要素。

- 连接
- 身份
- 权限
- 上下文

我们将在本章讨论这些要素中的每一个。但请记住，Windows是一个由许多紧密集成的子系统组成的操作系统。因此，这些安全要素经常相互作用。这种相互作用有时会使远程脚本问题更加难以解决。例如，你可能使用提供连接、特定身份和有效权限的域管理员凭据连接到远程计算机——换句话说，一个安全上下文。但是，通过该连接你有权访问的用户配置文件可能不是你所期望的。例如，如果你试图访问计算机主要用户的配置文件，你的脚本将无法正常工作，因为脚本的安全上下文连接的不是那个用户配置文件。因此，每当调试远程脚本时，重要的是要思考脚本在做什么，以及它在每个安全要素的上下文中遇到了什么。

#### 连接

任何类型远程脚本的第一项任务都是连接到远程计算机。通常，连接问题是由底层网络问题引起的，例如无法将名称解析为IP地址。这些问题任何有经验的管理员都应该能轻松解决。其他连接问题可能是由远程计算机甚至你自己的计算机上的本地防火墙软件引起的。我们将在本章后面讨论防火墙问题。

解决网络和防火墙问题后，下一步是连接到远程计算机上适当的服务和组件。例如，WMI需要连接到远程计算机的Windows管理规范服务。如果该服务未运行，你将无法建立连接，你的脚本将无法正常运行。其他类型的远程脚本可能需要分布式组件对象模型（DCOM）连接。如果无法与远程计算机上的正确DCOM对象建立连接——可能是因为对象未正确安装或注册——你的脚本将无法正常运行。

解决此类连接问题的关键是清楚地理解你尝试执行的脚本任务需要什么类型的连接。

- WMI查询通常需要访问远程计算机的WMI服务。这需要到该服务的远程过程调用（RPC）连接，以及实例化作为Windows一部分安装的某些DCOM对象的能力。
- ADSI查询连接到某种类型的服务。在ADSI的LDAP提供程序的情况下，连接是使用LDAP协议连接到LDAP服务器，例如活动目录。在WinNT提供程序的情况下，ADSI使用RPC协议连接到该服务。
- 对远程计算机文件和文件夹的 *FileSystemObject* 查询需要使用服务器消息块（SMB）的文件共享连接，就像你使用Windows资源管理器连接到远程计算机的文件系统一样。

除了物理连接，可能还需要某种形式的权限。大多数形式的远程脚本涉及两种类型的权限。脚本可能需要的第一种权限是 *连接权限* ——连接到服务或对象并要求其执行任务的权限。第二种权限是 *执行权限* ——执行任务的权限。这两者之间存在细微差别。

例如，假设你在名为Server2的计算机上安装了一个DCOM对象，该对象能够从该计算机的本地安全账户管理器（SAM）中删除用户账户。然后你在Client1上编写一个尝试使用Server2的DCOM对象的脚本。你将遇到的第一个权限问题是你的脚本尝试实例化DCOM对象时。权限由Windows的组件服务安全层管理，可以通过组件服务控制台进行配置。如下一页的图6-1所示，这些权限可以保持其默认设置，也可以自定义。

自定义启动权限允许你查看DCOM可以控制的内容。如下一页的图6-2所示，DCOM可以配置控制 *本地启动* （在本地计算机上运行且需要使用该对象的应用程序）或 *远程启动* （在另一台计算机上运行并尝试远程实例化该对象的应用程序，如你的脚本）的权限。



# 第三部分：高级脚本技术、工具与技术

![图 6-1 为特定 DCOM 对象或应用程序配置安全性](img/4fefd6988ba5d4a92a65127617ca24c2_183_0.png)

图 6-1 为特定 DCOM 对象或应用程序配置安全性

![图 6-2 自定义 DCOM 对象的启动权限](img/4fefd6988ba5d4a92a65127617ca24c2_183_1.png)

图 6-2 自定义 DCOM 对象的启动权限

你可以为激活配置类似的权限。你运行脚本所使用的帐户必须具有远程启动和激活权限。这在独立计算机或非域成员的计算机上可能比较困难，因为你的脚本可能无法提供必要的凭据来获取对该对象的远程启动和激活权限。

你还可以配置权限，以控制 DCOM 对象在启动和激活后的访问。默认情况下，只有本地管理员组可以保证拥有必要的权限，不过你显然可以根据需要重新配置权限。

这些只是在远程计算机上开始工作的必要权限。一旦 DCOM 对象启动并运行，它仍然需要权限来执行你希望它完成的任务。我们将在本章后面讨论执行权限。

#### 身份

你能在远程计算机上执行的任务受到你（或你的脚本）在该远程计算机上 *身份* 的约束。在这种情况下，你可以将你的身份理解为在远程计算机上代表你的用户帐户。你的脚本通常会利用 Windows 传递身份验证和身份信息的能力。例如，当你使用 Windows 资源管理器打开远程计算机上的共享文件夹时，Windows 会使用你登录计算机时使用的帐户对你进行身份验证。如果你使用脚本远程访问计算机上的文件，也会发生相同的过程。脚本使用替代凭据访问文件的唯一方法是使用 `RunAs` 命令。当你使用 `RunAs` 命令时，脚本会在不同的帐户下执行，并使用该帐户连接到共享文件夹。

只有少数几种脚本技术支持在不使用 `RunAs` 的情况下轻松使用替代凭据。例如，WMI 和 ADSI 连接都可以使用替代凭据创建，但这只是例外，而非常规。大多数情况下，用于执行脚本的帐户就是该脚本执行所有连接和任务所使用的帐户。

> **注意** 尽管某些脚本技术（如 WMI 和 ADSI）提供了传递替代凭据的方法，但不要犯将那些凭据直接硬编码到脚本中的错误。相反，应在脚本运行时提示输入这些凭据。正如我们在第 2 章“脚本安全”中讨论的，无法确保硬编码的凭据保持机密，这使其成为一个重大的安全风险。

你的身份如此重要的原因是，远程计算机将根据你的身份授予你权限。换句话说，你的身份控制着你在远程计算机上能做什么。

#### 权限

我们已经讨论了连接到各种脚本相关技术和服务所需的权限。然而，在你连接之后，你将需要适当的权限来执行你的脚本试图执行的任何任务。

Windows 的几乎每个领域都有自己独特的安全层。例如，文件和文件夹利用 NTFS 权限。如果你使用名为 *Jeff* 的域帐户登录到你的计算机，并连接到同一域中远程计算机上的共享文件夹，你将只能访问 Jeff 帐户有权访问的文件和文件夹。这与使用非脚本方式（如 Windows 资源管理器）访问这些文件和文件夹相同。对于脚本没有特殊的权限层；它们受制于与其他人相同的规则。

WMI 有自己的安全层，你可以通过 WMI 控制 MMC 管理单元来管理它。如图 6-3 所示，该管理单元提供了对计算机上安装的每个 WMI 命名空间的访问。

![图 6-3 通过 WMI 控制管理单元管理 WMI 安全性](img/4fefd6988ba5d4a92a65127617ca24c2_185_0.png)

图 6-3 通过 WMI 控制管理单元管理 WMI 安全性

修改命名空间的权限是通过一个类似于 NTFS 权限对话框的对话框完成的。如图 6-4 所示，权限可以应用于执行 WMI 方法、写入全部或部分 WMI 属性、启用帐户、远程启用帐户等等。如灰色复选框所示，命名空间的权限可以从父命名空间或 WMI 根命名空间继承。

![图 6-4 配置安全性](img/4fefd6988ba5d4a92a65127617ca24c2_186_0.png)

图 6-4 配置安全性

ADSI 也处理权限。连接到基于 LDAP 的目录（如 Active Directory）意味着你将处理该目录的权限。通过 WinNT 提供程序连接到独立或成员计算机意味着你将处理该计算机上的本地权限。这些权限通常通过用户权利分配来应用。

与许多其他潜在的脚本问题一样，理解远程脚本安全性的最佳方法是思考如果你在不使用脚本的情况下手动执行任务，安全性将如何工作。例如，如果你想要打开 Active Directory 并删除一个用户帐户，执行此操作需要用户帐户具有哪些权限？你用于登录工作站的帐户是否具有这些权限？如果没有，由同一帐户执行的脚本也不会有权限。

#### 上下文

上下文可能是远程脚本中最令人困惑的方面之一。它涉及身份以及 Windows 是一个多用户操作系统的事实。想想看：如果 Jeff 和 Don 共用一台 Microsoft Windows XP Professional 计算机，他们两人都可以登录，并拥有不同的桌面配置、不同的“我的文档”内容以及保存在注册表中的不同应用程序首选项。所有这些特定于用户的项目都存储在 *用户配置文件* 中，该文件由基于文件系统的配置文件（位于顶级“Documents and Settings”文件夹下的文件夹层次结构）和注册表配置单元（位于注册表中的 HKEY_USERS 下）组成。

假设 Don 编写了一个脚本，将几个文件复制到特殊的“我的文档”文件夹，并修改 HKEY_CURRENT_USER 下的几个注册表项。Don 在他自己未共享的计算机上测试了这个脚本，他在该计算机上使用他通常的域帐户登录。脚本运行正常。然后 Don 稍微修改了脚本，通过连接到 Don 和 Jeff 共用的计算机来远程执行相同的任务。Don 的目标是将几个文件复制到 Jeff 的“我的文档”文件夹，并修改 HKEY_CURRENT_USER 中的注册表项，使它们影响 Jeff 的登录会话。当 Don 运行脚本时，它没有错误地完成，但 Jeff 看不到任何更改。图 6-5 说明了发生了什么。

![图 6-5 远程连接和上下文](img/4fefd6988ba5d4a92a65127617ca24c2_187_0.png)

**图 6-5** 远程连接和上下文

当 Don 在他自己的计算机上运行脚本时，它连接到共享计算机。该脚本使用 Don 的用户帐户进行身份验证，因为那是 Don 用于执行脚本的帐户。当你使用特定帐户登录到计算机时，你的配置文件会加载，因此 Don 的脚本修改了“我的文档”和 HKEY_CURRENT_USER——但它是为 Don 在该计算机上的配置文件修改的，而不是 Jeff 的。如果 Don 从未登录到该计算机，计算机会创建一个新的配置文件，就像任何用户首次登录时一样。Jeff 没有看到脚本所做的任何更改，因为没有一项更改是针对他的配置文件进行的。

此示例说明了管理员遇到的最常见问题之一：试图编写一个修改计算机所谓的“主要用户”配置文件的脚本。Windows 不指定“主要用户”；它只是存储用户帐户和配置文件。用户 A 登录，可以访问用户 A 的配置文件；如果用户 B 登录，他或她可以访问用户 B 的配置文件。很简单，但当你试图远程修改用户的配置文件时，这会令人沮丧。作为管理员，我们通常认为计算机属于单个“主要”用户，当我们想在计算机上执行管理任务时，通常希望以影响该主要用户的方式进行。然而，由于 Windows 不支持



### 使用 Windows 防火墙

Windows 防火墙（在 Microsoft Windows XP Professional Service Pack 2 和 Microsoft Windows Server 2003 Service Pack 1 中引入）为启用了防火墙的计算机提供了高级别的本地安全性。然而，默认情况下，防火墙会阻止大多数传入连接，这使得任何类型的远程管理——包括脚本编写——变得不可能。当然，这并非关闭防火墙的理由；你只需修改它以允许必要的传入连接。

- 对于文件和文件夹访问，请启用文件共享的防火墙例外。
- 对于 WMI 访问，请启用远程管理和 DCOM 连接。
- 对于其他脚本技术，请启用传入 DCOM 连接，可能还需要启用 RPC 连接。

由于 Windows 防火墙的配置和管理可能涉及重大的规划和安全问题，本书将不深入探讨这一主题。请记住，防火墙可以通过 Active Directory 和组策略进行集中配置和管理，这意味着你可以轻松高效地在整个企业中创建、部署和实施 Windows 防火墙策略。

> **更多信息** 有关配置防火墙以与 WMI 和其他远程脚本技术配合使用的更多信息，请参阅位于 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/wmisdk/wmi/connecting_through_windows_firewall.asp 的文章（此链接包含在随附的 CD 中；请点击 *通过 Windows 防火墙连接*。）

### 理解远程脚本对象

到目前为止，我们讨论的内容适用于两种类型的远程脚本。然而，从现在开始，我们将专注于部署脚本。（本书的其余大部分内容，特别是关于 WMI 和 ADSI 的章节，涵盖了连接脚本中使用的技术。）

Windows 脚本宿主 (WSH) 5.6 包含专为远程脚本设计的对象。这些对象将脚本从你的计算机复制到远程计算机，然后在远程计算机上执行它。一些对象可以将脚本错误传回你的计算机，你的原始脚本可以在那里适当地处理这些错误。远程脚本涉及两个脚本。

- *部署脚本*，在你的计算机上运行，将脚本部署到一个或多个远程计算机，并可以处理来自远程计算机的错误。
- *已部署的脚本*，被复制到远程计算机并在其上运行，可以将错误发送回你的计算机。

本质上，一个简单的部署脚本看起来像这样。

```
Dim objController, objRemoteScript
Set objController = CreateObject("wshController")
Set objRemoteScript = objController.CreateScript( _
    "C:\MyScript.vbs", "Client1")
objRemoteScript.Execute
Do While objRemoteScript.Status <> 1
    wScript.Sleep 1000
Loop
MsgBox "Script complete"
```

我们将在以下部分讨论这些对象和方法中的每一个。这里的核心对象是 *WshController*（用于复制脚本）和 *WshRemote*（代表远程脚本并提供控制它的方法——在有限程度上）。

请记住，使用 *WshController* 对象时有两个限制。

- 你必须是远程计算机上的本地管理员。
- 你部署到远程计算机的脚本不得尝试通过使用 *WScript.Echo*、*MsgBox*、*InputBox* 或类似函数与用户界面进行交互。已部署的脚本不会在交互式桌面中运行，因此将无法对对话框做出响应。

### 使用其他类型的远程脚本

*WshController* 对象是 Windows 脚本宿主中唯一专门为远程脚本内置的对象，但这并不意味着它是唯一可用的远程脚本类型。一些第三方制造商已经为远程脚本制作了强大而灵活的技术。例如，iTriopoli 的 AdminScript-Editor (http://www.adminscripteditor.com) 包含 Script Packager，你可以用它将脚本打包成独立的可执行文件并进行部署。SAPIEN PrimalScript (http://www.primalscript.com) 有一个类似的功能，Evolved Script Packager，它提供了极大的部署灵活性。

另一个脚本编辑器 OnScript (http://www.onscript.com) 包含远程脚本管理功能。你可以使用 OnScript 来管理和执行远程计算机上的脚本存储库。脚本将在远程计算机上运行，并将状态信息发送回你的 OnScript 控制台。PrimalScript 集成了一个目的大致相似的功能——远程脚本执行引擎，它为运行远程脚本、监控其状态等提供了增强的灵活性。

由于这些功能中的每一个都与特定的商业产品相关，我们不会在本书中涵盖它们。然而，如果此类远程脚本在你的环境中是一种常见需求，我们建议你查看其中一个或所有这些工具（每个都有试用版），以确定哪个最适合你的需求。

### 理解远程脚本方法

*WshController* 对象没有属性，只有一个方法 *CreateScript*。此方法只接受两个参数：要部署的脚本的完整路径和文件名，以及应将脚本复制到的计算机名称。*CreateScript* 方法复制脚本（远程计算机也必须安装 WSH 5.6），返回一个表示远程脚本的 *WshRemote* 对象，并提供用于处理它的属性和方法。

- *Error* 属性表示一个 *WshRemoteError* 对象，该对象保存有关导致远程脚本意外终止的任何错误的信息。
- *Status* 属性的值可以是 0（表示脚本正在运行）或 1（表示脚本已完成）。
- *Execute* 方法运行远程脚本。当脚本完成时，通常会从计算机中删除它。（在极少数情况下，它可能会被保留，例如在脚本完成之前与远程计算机的连接中断。）
- *Terminate* 方法取消远程脚本。它首先尝试通过发送适当的 *close* 消息来结束脚本，但如果这不起作用，它只是终止远程脚本的进程。

使用 *WshController.CreateScript* 对象创建你的远程脚本，使用 *WshRemote.Execute* 对象运行它，并检查 *WshRemote.Status* 对象以查看脚本何时完成。使用 *WshRemoteError* 对象稍微复杂一些，因为没有状态告诉你是否发生了错误。相反，当错误发生时，会引发一个事件。由于事件不是 VBScript 中通常处理的内容，它们可能看起来很陌生。本质上，处理事件有两个步骤。

1. 创建一个处理该事件的子程序。
2. 指示可能引发该事件的对象使用你的子程序。

例如，要对远程脚本引发的错误做出反应，你可以编写一个简短的子程序来简单地显示远程错误。

```
Sub remote_Error
    Dim objError
    Set objError = objRemote.Error
    WScript.Echo "Error - Line: " & theError.Line & _
        ", Char: " & theError.Character & vbCrLf & _
        "Description: " & theError.Description
    WScript.Quit -1
End Sub
```

你会将这个子程序添加到前面声明了 *objRemote* 对象的脚本中。有了子程序后，你只需告诉 *objRemote* 对象，如果其 *Error* 事件发生，就使用新的 *remote_Error* 子程序。

```
wScript.ConnectObject objRemote, "remote_"
```

此命令告诉 *objRemote* 对象，任何事件都将由名称以 *remote_* 为前缀的子程序处理。换句话说，*Error* 事件将由 *remote_Error* 处理。*objRemote* 对象还有一个 *Start* 事件和一个 *End* 事件，它们将分别由 *remote_Start* 和 *remote_End* 处理。整个脚本作为一个整体，显示在下一页的清单 6-1 中。



### 查看远程脚本的实际操作

清单 6-2 是一个将 `C:\Deployed.vbs` 部署到 `C:\Computers.txt` 中列出的每台计算机的脚本。结果记录到 `C:\Log.txt`。

```
清单 6-2 带有日志记录的远程脚本
Dim objController, objRemoteScript, objFSO
Dim objTSIn, objTSOut, strComputer

'创建对象
Set objController = CreateObject("wshController")
Set objFSO = CreateObject("Scripting.FileSystemObject")

'从文件读取计算机名称
Set objTSIn = objFSO.OpenTextFile("C:\computers.txt")

'打开输出文件用于日志
Set objTSOut = objFSO.CreateTextFile("C:\log.txt", True)

Do Until objTSIn.AtEndOfStream
    '将脚本部署到远程计算机
    strComputer = objTSIn.ReadLine
    objTSOut.WriteLine strComputer & ": 部署时间 " & Now

    Set objRemoteScript = objController.CreateScript( _
        "C:\Deployed.vbs", strComputer)
    WScript.ConnectObject objRemoteScript, "remote_"
    objRemoteScript.Execute

    Do Until objRemoteScript.Status = 1
        WScript.Sleep 1000
    Loop

    objTSOut.WriteLine strComputer & " 完成时间 " & Now
    Set objRemoteScript = Nothing
Loop

objTSIn.Close
objTSOut.Close
WScript.Echo "部署脚本完成。"

Sub remote_Error
    Dim objError
    Set objError = objRemoteScript.Error
    objTSOut.WriteLine strComputer & ": 错误时间 " & Now
    objTSOut.WriteLine "  行号: " & objError.Line & _
        ", 字符位置: " & objError.Character & vbCrLf & _
        "描述: " & objError.Description
    WScript.Quit -1
End Sub
```

让我们逐步分析这个脚本的各个部分，看看它在做什么。脚本首先声明一个 *FileSystemObject* 对象和一个 *WshController* 对象。

```
Dim objController, objRemoteScript, objFSO
Dim objTSIn, objTSout, strComputer

'创建对象
Set objController = CreateObject("WshController")
Set objFSO = CreateObject("Scripting.FileSystemObject")
```

接下来，脚本打开 `C:\Computers.txt`，其中每行列出一个计算机名称。脚本还打开一个文本文件用于输出，我们将在此写入远程脚本的状态信息。

```
'从文件读取计算机名称
Set objTSIn = objFSO.OpenTextFile("C:\computers.txt")

'打开输出文件用于日志
Set objTSOut = objFSO.CreateTextFile("C:\log.txt", True)
```

现在，脚本将读取 `C:\computers.txt` 的每一行，将每个计算机名称输入到变量 *strComputer* 中。

```
Do Until objTSIn.AtEndOfStream

    '将脚本部署到远程计算机
    strComputer = objTSIn.ReadLine
```

请注意，脚本的日志消息包括计算机名称、发生了什么以及日期和时间戳。

```
objTSOut.WriteLine strComputer & ": 部署时间 " & Now
```

现在，脚本创建一个 *WshRemote* 对象，并将该对象的事件连接到事件处理子例程。由于我们不关心 *Start* 或 *End* 事件，因此没有为它们包含子例程。当这些事件触发时，由于没有匹配的子例程，所以不会发生任何事情。

```
Set objRemoteScript = objController.CreateScript( _
    "C:\Deployed.vbs", strComputer)
WScript.ConnectObject objRemoteScript, "remote_"
objRemoteScript.Execute
```

接下来，部署脚本将暂停，直到部署的脚本执行完毕。完成后，我们将写入另一个日志条目，然后释放 *WshRemote* 对象，以便在循环的下一次迭代中重用它。

```
Do Until objRemoteScript.Status = 1
    WScript.Sleep 1000
Loop

objTSOut.WriteLine strComputer & " 完成时间 " & Now

Set objRemoteScript = Nothing

Loop
```

当脚本结束时，我们将关闭文本文件并显示完成消息。

```
objTSIn.Close
objTSOut.Close
WScript.Echo "部署脚本完成。"
```

以下是 WshRemote Error 事件处理程序。它只是将错误信息写入我们的日志文件。

```
Sub remote_Error
    Dim objError
    Set objError = objRemoteScript.Error
    objTSOut.WriteLine strComputer & ": 错误时间 " & Now
    objTSOut.WriteLine "  行号: " & objError.Line & _
        ", 字符位置: " & objError.Character & vbCrLf & _
        "描述: " & objError.Description
    WScript.Quit -1
End Sub
```

这是一个基本的脚本，但可以轻松扩展以执行额外的日志记录或错误处理。

### 总结

在本章中，我们介绍了两种远程脚本：一种是连接到远程计算机执行任务的脚本，另一种是将脚本部署到远程计算机并在那里执行的脚本。我们讨论了远程脚本涉及的安全问题，并解释了底层安全层的工作原理，这将帮助你在遇到远程脚本安全问题时更好地进行分析和故障排除。有了这些信息，你将能够使用本书及其他地方的脚本技术。

# 第 7 章

## 数据库脚本

本章内容：

- 理解 ActiveX Data Objects ........................ 179
- 理解 *Connection* 对象 ........................ 181
- 理解 *Recordset* 对象 ........................ 185
- 理解 *Command* 对象 ........................ 191
- 理解数据库之间的差异 ........ 195
- 理解 SQL ................................................... 197
- 查看 ActiveX Data Objects .............................. 202
- 总结 ..................................................................... 206

从脚本中处理数据库可能看起来是最困难的技术之一。然而，这个主题看起来比实际情况复杂得多，这主要是因为大多数文档都是为专业软件开发人员编写的。我们将为你提供关于数据库脚本编写所需的信息，而不会用不必要的细节来淹没你，这样你就可以快速掌握核心概念，使数据库成为你脚本中不可或缺的一部分。

数据库脚本编写乍一看似乎很难、过于复杂且容易出错。如果你正在编写一个大型的数据库驱动应用程序，所有这些都可能是真的。幸运的是，如果你是一个试图自动化任务和跟踪信息的 Windows 管理员，数据库使用起来可能非常简单。你只需要专注于核心数据库技术，而不会被那些只有专业开发人员才会使用的各种功能所分心。

你可以使用数据库脚本编写来执行任务，例如，创建一个简单的 Microsoft Access 应用程序，用户可以输入有关新帐户的信息。该脚本将从 Access 数据库中读取新帐户信息，并创建必要的帐户。这种自动化有助于将一项相当乏味且容易出错的任务简化为一个简单的、一键操作。

### 理解 ActiveX Data Objects

脚本用于访问数据库的技术称为 ActiveX Data Objects (ADO)。不要将其与 ADO.NET 混淆，ADO.NET 是专属于 Microsoft .NET Framework 的，并且不是设计用于从 VBScript 中使用的。ADO 是 ADO.NET 的稍旧版本，功能同样强大，你的脚本可以轻松访问它。



需要理解的是，ADO并非访问数据的唯一手段。例如，Microsoft Excel和Access都能存储数据，并且都可以通过Microsoft Office内置的组件对象模型（COM）自动化接口进行操作。文本文件是另一种数据存储类型，您无疑已经使用过*FileSystemObject*库来轻松访问它。然而，ADO的伟大之处在于，它可以通过一个单一的、标准化的接口访问*所有*这些数据源——以及许多其他数据源。ADO访问多种数据源的能力在图7-1中得到了说明。您的脚本使用ADO，它提供了一套单一的、标准化的编程接口来访问任何类型的数据库。反过来，ADO将这组接口转换为您正在访问的任何数据源所需的特定接口。换句话说，通过花时间学习ADO，您将能够轻松访问数十种不同类型的数据库，无需额外努力——您不必学习单独的技术来访问SQL Server数据库、Access数据库、文本文件等等。

![](img/4fefd6988ba5d4a92a65127617ca24c2_199_0.png)

不过，在我们继续讨论数据库之前，让我们先定义一下术语。

- *数据库*是一个包含数据的文件或其他存储机制。一台SQL Server计算机可以容纳多个数据库，而一个单独的Access .mdb文件就是一个数据库。
- *表*是数据库内的组织单元；大多数数据库可以包含一个或多个表。表也被称为*实体*，因为它们通常包含关于单一类型对象或实体（如人或计算机）的信息。每个表由以下部分组成：
    - 列（也称为*字段*）包含表所代表实体的属性。例如，在一个包含人员信息的表中，一列可能包含人的姓名或地址。
    - 行（也称为记录）包含关于单个实体的所有信息。例如，在一个包含计算机信息的表中，一行将包含包含该计算机名称、IP地址等的所有列。

Excel文件是可视化此结构的绝佳方式。一个Excel工作簿代表一个数据库，每个工作表或选项卡代表一个表，而行和列则代表记录和字段，如图7-2所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_200_0.png)

**图7-2** 将Excel文件用作数据库

总的来说，使用数据库就像使用Excel工作簿一样简单。然而，在开始使用数据库之前，您首先需要连接到它。

#### 理解 Connection 对象

在ADO中，Connection对象用于表示您的脚本与特定数据库之间的电子连接。Connection对象告诉ADO数据库的位置、如何打开它、使用什么用户名和密码（如果需要）等等。创建一个新的Connection对象很简单。

```
Dim objConn
Set objConn = CreateObject("ADODB.Connection")
```

您调用Connection对象的Open方法，并传入连接数据库所需的信息。大多数管理员开始担心的地方就在这里，因为所谓的连接字符串可能看起来异常复杂。但事实并非如此——我们将在接下来的两节中介绍它们。当您使用完数据库后（例如在脚本结束时），您调用Connection对象的Close方法。

```
objConn.Close
```

这可以确保所有数据库文件被正确关闭，任何服务器连接（例如与SQL Server一起使用的连接）被释放，等等。

182 第三部分：高级脚本技术、工具和技术

##### ODBC DSN 连接

ADO能够进行几种不同类型的连接。一种类型是通过Microsoft的开放数据库连接（ODBC）技术进行的。使用ODBC的主要好处是它为*Connection*对象提供了简便的配置。从技术上讲，这是一种过时的技术（它已被OLE DB取代），但它仍然有效，并且由于您的脚本可能不需要超快的性能，ODBC表现得非常好。

首先，您需要创建一个ODBC数据源名称，或DSN。如果单击“开始”菜单上的“管理工具”，然后单击“数据源(ODBC)”，您将看到现有的DSN列表，如图7-3所示。DSN有两种类型：*用户*DSN，它们在本地计算机上配置，仅供您使用；以及*系统*DSN，它们在本地计算机上配置，可供该计算机的所有用户使用。您可以单击“添加”按钮来创建适当的类型。

![](img/4fefd6988ba5d4a92a65127617ca24c2_201_0.png)

图7-4显示了“创建新数据源”对话框，该对话框在单击“添加”时出现。在其中，您为DSN选择一个驱动程序。选择与您想要访问的数据库类型匹配的驱动程序：Access、Excel、dBase、FoxPro、Oracle、Paradox、文本文件、SQL Server等。

![](img/4fefd6988ba5d4a92a65127617ca24c2_202_0.png)

**图7-4 选择数据库驱动程序**

当您单击“完成”时，将出现另一个特定于所选数据库类型的对话框。例如，图7-5显示了Access数据库的对话框。您必须指定一个DSN，即数据源的名称。对于Access数据库或Excel文件，您还需要指定要连接的文件。

![](img/4fefd6988ba5d4a92a65127617ca24c2_202_1.png)

**图7-5 创建 Access DSN**

对于SQL Server，您必须完成一个简短的向导，它会提示您输入服务器名称、数据库、登录凭据等。下一页的图7-6显示了SQL Server ODBC DSN向导的一个屏幕。

![](img/4fefd6988ba5d4a92a65127617ca24c2_203_0.png)

无论您将连接哪种类型的数据库，完成后您都将拥有一个新的DSN，并且您会知道它的名称。激活DSN就像调用*Connection*对象的*Open*方法并传递DSN一样简单。

```
objConn.Open "MyDSN"
```

以这种方式连接的缺点是，您的脚本现在要求DSN存在于计算机上。换句话说，在您设置好DSN之前，您的脚本在其他计算机上将无法正常运行，这可能有点难以自动部署。但是，对于您只从自己的计算机运行的脚本，DSN是一种方便、易于配置的数据库连接方式。

> **最佳实践** 无论何时在脚本中使用DSN，请务必包含一些注释行，描述DSN连接的内容。这些注释将帮助您或其他管理员将来重新创建DSN。您还应该记录数据库的位置，并简要描述其结构。有了这些注释，脚本所需的一切都将记录在脚本本身中，因此它是自包含的且易于维护。

##### 连接字符串

连接字符串可能看起来令人生畏，但它们提供了比DSN更灵活的连接选项。与DSN不同，连接字符串不需要在运行脚本的计算机上进行任何特殊配置。连接字符串本身包含了*Connection*对象找到数据库所需的一切。另一个优点是连接字符串可以使用更新的OLE DB数据库驱动程序（称为*提供程序*），这将使您环境中的任何开发人员都更满意（您可能不会注意到任何差异）。连接字符串在不同的数据库之间可能有很大差异；以下是最常见的示例。请注意，*斜体*元素是占位符，旨在替换为您自己的信息，例如数据库名称。[方括号]中的信息是可选的；如果您的环境中不需要这些元素，可以省略它们。

- 连接到Microsoft Access的连接字符串是：
  `Provider=Microsoft.Jet.OLEDB.4.0;Data Source=数据库路径和文件名;`

- 连接到Microsoft Excel的连接字符串是：
  `Provider=Microsoft.Jet.OLEDB.4.0;Data Source=数据库路径和文件名;Extended Properties=Excel 8.0;`

- 连接到Microsoft SQL Server的连接字符串是：
  `Provider=SQLOLEDB;Data Source=服务器名称;Initial Catalog=数据库名称; [User ID=用户名;Password=密码]`

- 连接到文本文件（例如CSV，其中第一行包含列名）的连接字符串是：
  `Provider=Microsoft.Jet.OLEDB.4.0;Data Source=数据库路径;Extended Properties=Text;HDR=Yes;FMT=Delimited;`

> **注意** 不要将密码硬编码到脚本中。如果需要在连接字符串中提供密码，请使用*InputBox*函数或其他技术提示输入密码，然后将密码附加到连接字符串中。

使用连接字符串很简单——只需将其作为*Open*方法的参数传递即可。

```
objConn.Open "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\MyDB.mdb;"
```

请注意，当您使用文本文件连接字符串时，您只提供文本文件的*路径*；您将在查询中指定*文件名*，我们接下来将介绍。

#### 理解 Recordset 对象

数据库表只是一组行，或*记录*。因此，*记录集*一词与*表*一词的含义非常相似。在ADO中，*Recordset*对象代表数据库表的全部或部分，当然也是如此。当您从数据库查询信息时，ADO将数据存储在*Recordset*对象中，以便您可以处理它。假设您有一个名为*Users*的数据库表，其中包含名为*UserID*、*UserName*和*UserDescription*的列。您可以像这样查询该表的所有行。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
Set objRS = objConn.Execute("SELECT * From Users")
```



以下是一些关于查询数据库的注意事项。

-   刚刚展示的代码片段假设一个名为 *objConn* 的 *Connection* 对象已经被创建并打开。
-   刚刚展示的代码块中的第二行在技术上是不必要的。*Connection* 对象的 *Execute* 方法返回一个 *ADODB.Recordset* 对象，因此你并不需要明确告诉 VBScript 它即将返回。然而，包含这一行可以使脚本编辑器更容易地为 *Recordset* 对象提供特定的帮助，这就是我们包含它的原因。
-   我们将在本章后面介绍称为结构化查询语言（SQL）的查询语法。但是，现在你需要知道的是，*SELECT * FROM Users* 语句从 Users 表中检索所有行和所有列。

> **最佳实践** 专业的软件开发人员不喜欢像 *SELECT * FROM Users* 这样的语句，因为它性能不佳。开发人员会更倾向于使用 *SELECT UserID,UserName,UserDescription FROM Users* 语句，因为它返回相同的结果，并且明确列出了要检索的列。撇开性能考虑，我们也更喜欢第二种方法，因为它使脚本具有自描述性。该语句清晰地列出了要检索的列名，因此你不必稍后在数据库中费力查找。

##### 仅向前记录集

记录集一次提供对单行或单条记录的访问。它们使用一个内部 *指针* 来跟踪当前行。默认情况下，它们从指针位于第一行开始。你可以使用以下四种语句之一来移动指针。

-   *MoveNext*
-   *MovePrevious*
-   *MoveFirst*
-   *MoveLast*

然而，我们刚刚向你展示的示例——使用 *Connection* 对象的 *Execute* 方法返回一个记录集——返回了一种特殊类型的记录集，称为 *仅向前记录集*。它们性能很快，但只支持 *MoveNext* 语句，这意味着在你移动到下一行之后，就不能再返回了。在许多情况下，例如枚举要添加到 Active Directory 的用户列表，仅向前功能就足够了。

*Recordset* 对象还支持一个名为 *EOF* 的属性，它代表文件结束。当记录集指针定位到最后一行数据之后时，此属性被设置为 TRUE。枚举每一行的一个简单方法是在循环中使用 *EOF* 属性。

```
Do Until objRS.EOF = True
    objRS.MoveNext
Loop
```

当然，仅仅遍历所有记录并不是特别有用——你需要以某种方式访问这些记录内部的数据。你可以通过引用所需的列名来做到这一点。

```
Do Until objRS.EOF = True
    strUser = objRS("UserName")
    strID = objRS("UserID")
    strDesc = objRS("Description")
    objRS.MoveNext
Loop
```

这会将每一行的内容拉入一组字符串变量，然后可以在其他语句中使用这些变量将新用户添加到 Active Directory。

> 提示 不要忘记循环内的 *MoveNext* 语句。没有它，记录集指针永远不会移动，因此它永远不会到达末尾。循环会无限期地继续，或者直到你按 Ctrl+Break 来终止脚本。

当你完成使用记录集时，最好关闭它，释放它之前使用的所有资源。

```
Do Until objRS.EOF = True
    strUser = objRS("UserName")
    strID = objRS("UserID")
    strDesc = objRS("Description")
    objRS.MoveNext
Loop
objRS.Close
```

##### 其他类型的记录集

还有其他几种类型的记录集可供你使用。在仅向前（这是默认值）之后，最有用的类型是 *动态* 记录集。要打开一个动态记录集，你必须显式声明一个新的 *Recordset* 对象并使用其 *Open* 方法。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
objRS.Open "SELECT Column FROM Table", objConn, 2
```

请注意，*Open* 方法需要一个 SQL 语句、一个对已打开的 *Connection* 对象的引用以及数字 2，这表示你想要一个动态记录集。如果你忘记了 2，默认值是 0，它将打开一个仅向前记录集。

# 第三部分：高级脚本技术、工具和技术

> **注意** 并非所有数据库提供程序都支持动态记录集。如果你在尝试打开一个动态记录集时遇到错误，请尝试打开一个仅向前记录集。如果成功，那么你的数据库提供程序就不支持动态记录集。

使用动态记录集，你可以使用 *Recordset* 对象的全套导航方法来向前和向后移动记录集指针。你也可以修改动态记录集。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
objRS.Open "SELECT Birthday FROM Table WHERE [Name] = 'Don''", objConn, 2
objRS("Birthday") = "11/22/71"
objRS.Update
```

> **注意** 有时，数据库提供程序会给你一个动态记录集，但不支持 *Update* 方法。在你尝试并因更新尝试而获得错误之前，你不会知道这种情况。在本章的后面，我们将向你展示添加和更改数据的其他方法。

在刚刚展示的示例中，SQL 语句中添加了一个 *WHERE* 子句，因此返回的行只是 *Name* 列包含值 *Don* 的那些行。查询只选择了一列 *Birthday*，我们可以为该列分配一个新值。调用 *Update* 方法会将更改保存回数据库。请记住，在调用移动记录集指针的语句（如 *MoveNext*）之前调用 *Update* 方法。未能先调用 *Update* 可能会导致你的更改丢失，具体取决于你连接的数据库类型。

> **注意** 请注意 *Name* 列列在方括号内。这是因为 *Name* 这个词在大多数数据库系统中具有特定含义。通过将其括在方括号中，我们可以确保它将被视为列名，而不是其他东西。

你还可以使用动态记录集来添加新记录。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
objRS.Open "SELECT * FROM Table", objConn, 2
objRS.AddNew
objRS.("UserName") = "Don"
objRS("Birthday") = "11/22/71"
objRS.Update
```

这类似于更改数据。你调用 *AddNew* 方法来创建一个新的、空白的记录，并将记录集指针移动到它上面。然后你用数据填充表的列，并调用 *Update* 方法来保存你的更改。

**注意** 许多数据库包含关于允许什么类型数据的内部规则。例如，如果 *Birthday* 列被定义为日期字段，并且你尝试插入一个名字，数据库将拒绝你的更改。该拒绝可能直到你调用 *Update* 方法（即数据保存回数据库时）才会发生。当 *Update* 方法出现故障时，请仔细检查你所做的更改，因为其中一个可能正在引起问题。

另一种不太常见的记录集类型是 *静态* 记录集（它在 *Recordset* 对象的 *Open* 方法中的数字是 1）。它是仅向前和动态记录集类型的组合。你可以使用它在静态记录集中前后移动，但不能进行更改。

### 记录集提示和技巧

有一些方便的提示和技巧可用于处理记录集。首先，*Recordset* 对象有一个 *RecordCount* 属性，你可能认为它会提供记录集内的记录数。不幸的是，记录集在你将指针移动到最后一行之前，不知道有多少条记录。对于仅向前记录集来说，这相当没用，但对于动态记录集，你可以在记录之间前后移动，如下面的代码片段所示。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
objRS.Open "SELECT * FROM Table", objConn, 2
objRS.MoveLast
objRS.MoveFirst
WScript.Echo objRS.RecordCount & " records queried."
```

这通常提供准确的计数（取决于数据库类型），并以记录集指针定位在第一行结束，就像它开始时的位置一样。

你可能想要检查记录集是否完全为空，例如，当你的查询没有返回任何结果时。如果 *Table* 为空时运行以下代码，你将得到一个空的记录集。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
objRS.Open "SELECT * FROM Table", objConn, 2
```

一个简单的方法是检查记录集的 *EOF* 和 *BOF*（文件开始）属性是否为 TRUE。*BOF* 仅在记录集指针定位在第一条记录上时为 TRUE。如果 *BOF* 和 *EOF* 都为 TRUE，则记录集为空。

```
Dim objRS
Set objRS = CreateObject("ADODB.Recordset")
objRS.Open "SELECT * FROM Table", objConn, 2
If objRS.EOF And objRS.BOF Then
    'empty recordset
End If
```

Recordset 对象还有其他一些有用的属性和方法，包括以下内容：

-   `Bookmark` 属性可用于存储任意记录的位置，然后快速返回到该记录。正如你所料，此属性在仅向前（forward-only）的记录集中没有用处，因为记录集无法向后移动到书签位置。要使用书签，请先将记录集定位（通过使用 `MoveFirst`、`MoveNext` 或其他方法）到你想要记住的记录。然后将一个变量赋给 `Bookmark` 属性 (`myVar = objRS.Bookmark`)。稍后要返回书签位置，只需将 `Bookmark` 属性赋给该变量 (`objRS.Bookmark = myVar`)。只要你有唯一的变量来保存每个书签，就可以同时使用多个书签。

-   `State` 属性可用于检查记录集是否已打开。记录集关闭时，`State` 属性为零，打开时为 1。还存在其他状态值——2 表示正在连接，4 表示正在执行查询，8 表示正在获取数据——但它们通常变化很快。

-   `Sort`、`Filter` 和 `MaxRecords` 属性可用于对记录集进行排序、进行过滤以仅访问特定行，以及限制查询返回的行数。然而，在原始 SQL 查询（用于填充记录集）中执行这些操作更为高效。我们将在本章稍后向你展示如何操作。

-   `Find` 方法用于查找匹配的记录。执行类似 `objRS.Find "Column = Value"` 的语句（如果列包含字符串值，则使用 `objRS.Find "Column = 'Value'"`）可立即将记录集指针移动到第一个匹配的列。你还可以执行 `objRS.Find "Column = Value", 5`，这将在开始搜索前跳过 5 行（或你指定的任何其他数字）。执行 `objRS.Find "Column = Value",, -1` 将（在动态或静态记录集中）向后搜索，而不是向前。`Seek` 方法的工作方式类似，但灵活性稍差。

-   `Delete` 方法删除动态记录集中的当前行。

-   `Supports` 方法可用于根据记录集的类型及其数据库提供程序，确定给定记录集的功能。`Supports` 接受一个数字，该数字指定你要检查的功能数量。如果所有指定的功能都受支持，它返回 TRUE，否则返回 FALSE。例如，如果 `objRS` 支持 `AddNew` 方法，则 `objRS.Supports(16778240)` 将返回 TRUE。以下列表提供了大多数可用记录集功能的值。要检查多项功能，可对每项功能调用一次 `Supports`，或使用布尔 `Or` 运算符组合功能（例如，执行 `objRS.Supports(16778240 Or 512)` 以检查对 `AddNew` 和 `MovePrevious` 的支持）。

    -   AddNew = 16778240
    -   Bookmark = 8192
    -   Delete = 16779264
    -   Find = 524288
    -   MovePrevious = 512
    -   Update = 65536

使用记录集可以做更多的事情，但这些是你在编写管理脚本时最常用的技术。

> **提示** 如果你使用的是基于 CD 或 DVD 的 Microsoft MSDN 库（请向你所在组织的开发人员索要旧版本副本），你可以找到完整的 ADO 文档。要浏览目录，请单击“数据访问”，然后单击“参考”，接着单击“ADO”，再单击“ADO 程序员参考”，然后单击“ADO API 参考”，最后单击“ADO 对象和接口”。库的在线版本可在 http://msdn.microsoft.com/library 获取。由于在线库的 URL 和组织方式会不时变化，我们无法保证 ADO 信息将位于同一位置，甚至可能无法使用，但在出版时，要导航到该主题，请单击“Win32 和 COM 开发”，然后单击“数据访问和存储”，接着单击“ADO”，再单击“ADO”，然后单击“ADO 程序员参考”，接着单击“ADO API 参考”，最后单击“ADO 对象和接口”。此位置的当前 URL 是 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/ado270/htm/mdmscadoapireference.asp

（此链接包含在随附的 CD 中；请单击 *ADO API 参考*。）

以下最佳实践适用于通过代码或脚本访问任何数据库。

-   始终在 *SELECT* 语句中指定列列表，并且只指定你计划使用的列。
-   除非你确实需要表中的 *所有* 数据，否则请指定 *WHERE* 子句以帮助减少返回的数据量。
-   动态记录集比仅向前记录集需要更多的计算资源，因此尽可能使用仅向前记录集。

除了动态记录集提供的方法外，还有其他方法可以添加和更改数据——我们将在本章稍后介绍它们。

#### 理解 Command 对象

大多数脚本编写者会忽略 ADO *Command* 对象。事实上，如果你不打算使用基于 SQL Server 的数据库，你可以放心地跳过本节。但是，如果你打算使用 SQL Server（或其他关系数据库管理系统，如 Oracle、Sybase 或 DB2），*Command* 对象可提供更好的性能，并帮助你更好地利用服务器软件内置的功能。

*Command* 对象是一种以允许服务器更高效地执行命令的方式向服务器传递查询的方法。最大的好处体现在你访问存储过程时，存储过程是在服务器上包含和执行的一种特殊类型的脚本。创建存储过程超出了本书的范围，但如果你的服务器上有存储过程，我们鼓励你通过 *Command* 对象使用它们。即使没有存储过程，*Command* 对象在与数据库服务器结合使用时也很有用，因为它允许更高效地执行查询，特别是如果该查询将被执行多次的话。你创建 *Command* 对象的方式与其他数据库对象非常相似。

```
Dim objCmd
Set objCmd = CreateObject("ADODB.Command")
```

要使 *Command* 对象正常工作，必须设置三个必需的属性。

```
objCmd.ActiveConnection = objConn
objCmd.CommandText = "SELECT Column1 FROM Table2"
objCmd.CommandType = 1
```

`objConn` 属性必须表示一个已声明并打开的 *Connection* 对象。然后你可以使用 *Command* 来打开一个 *Recordset* 对象。

```
Set objRS = objCmd.Execute
```

这六行代码向服务器提交查询并返回一个仅向前记录集。但是，如果你要执行存储过程，就不会使用此格式。大多数存储过程是*参数化*的，也就是说，它们接受一个或多个输入参数，甚至可能通过输出参数提供输出——这与命令行实用程序并无不同。在 *Command* 对象中使用存储过程需要一些特殊的设置。首先，将 `CommandText` 属性设置为存储过程的名称，然后将 `CommandType` 属性设置为存储过程对应的适当值。

```
objCmd.ActiveConnection = objConn
objCmd.CommandText = "sp_MyProc"
objCmd.CommandType = 4
```

接下来，你需要添加参数。假设你的存储过程有三个参数：*Parm1*、*Parm2* 和 *Parm3*。*Parm1* 是一个长度为 10 的 SQL Server *varchar* 数据类型，*Parm2* 是一个 SQL Server *bigint* 数据类型，而 *Parm3* 是另一个 *bigint*，它将包含存储过程的输出。

```
objCmd.NamedParameters = True
objCmd.Parameters.Add(objCmd.CreateParameter("Parm1",200,1,10,MyVal1))
objCmd.Parameters.Add(objCmd.CreateParameter("Parm2",20,1,,MyVal2))
objCmd.Parameters.Add(objCmd.CreateParameter("Parm3",20,2,,MyVal3))
```

将 `NamedParameters` 属性设置为 TRUE 允许你以任何顺序添加参数，无论它们在存储过程中的定义顺序如何。ADO 根据你提供的名称来匹配参数。以下是 `CreateParameter` 方法的工作原理。

-   该方法的第一个参数是参数的名称。

第二个参数是参数的数据类型。数据类型的常用值包括以下几种：

-   Bigint = 20
-   Char = 129
-   Currency = 6
-   Date = 7
-   Decimal = 14
-   Single = 4
-   Double = 5
-   Empty = 0
-   Int (integer) = 3
-   Smallint = 2
-   Tinyint = 16
-   Varchar = 200
-   VarWChar (SQL Server nvarchar type) = 202

第三个参数指定参数的方向：1 表示输入，2 表示输出。

第四个参数是可选的，仅对变长数据类型（如 varchar、char 等）是必需的。此参数指定数据字段的长度。在此示例中，Parm1 声明的长度为 10 个字符，因此该长度被传递到 CreateParameter 参数中。如果你不使用此参数——例如，对于任何 int 数据类型都不是必需的——请将其留空，但务必像刚才示例中那样包含额外的逗号。

最后一个参数是你传递给参数的值，或者用于存储输出参数值的变量。

如果难以确定什么应该放在哪里，请尽可能与创建存储过程的开发人员沟通。

> 注意：你可以使用诸如 SQL Server Query Analyzer（在 SQL Server 2000 中）、SQL Management Studio（在 SQL Server 2005 中）或 SQL Express Manager（用于 SQL Server 2005 Express 版）等工具来检查存储过程，并查找其输入和输出参数及数据类型。

清单 7-1 列出了数据库中的所有存储过程及其参数（包括名称、类型、方向等）。此脚本是使用 ADO 的扩展 ADOX 编写的。尽管 ADOX 超出了本书的范围，但这个简短的脚本将使你更容易弄清楚如何使用任何可能可用的存储过程。请注意，未列出系统存储过程（SQL Server 内置的）。另请注意，你需要修改连接字符串以匹配你的环境（服务器名称、数据库名称等）。此连接字符串包含额外的参数以利用 SQL Server 的 Windows 集成安全性。

> **注意** 为了使清单 7-1 正确运行，你必须拥有适当的权限，并且数据库服务器必须支持 ADOX 库。如果你的结果包含过程名称但没有参数，可能是你没有足够的权限，或者你的数据库服务器未配置为通过 ADOX 枚举参数。

#### 清单 7-1 列出存储过程

```vb
Dim objConn
Set objConn = CreateObject("ADODB.Connection")
objConn.ConnectionString = "Provider=SQLOLEDB.1;Integrated " & _
    "Security=SSPI;" & _
    "Persist Security Info=False;Initial " & _
    "Catalog=database-name;Data Source=server-name"
objConn.Open

Dim objCatalog
Set objCatalog = CreateObject("ADOX.Catalog.2.8")
objCatalog.ActiveConnection = objConn

Dim objProcedure, objParameter
Set objProcedure = CreateObject("ADODB.Command")
Set objParameter = CreateObject("ADODB.Parameter")

'show procedure count
objCatalog.Procedures.Refresh
WScript.Echo objCatalog.Procedures.Count & " procedures"
WScript.Echo ""

'set the procedure name
For Each objProcedure In objCatalog.Procedures
    WScript.Echo "Procedure " & objProcedure.Name
    WScript.Echo "Parameters: "
    
    'show parameters
    On Error Resume Next
    For Each objParameter In objProcedure.Parameters
        WScript.Echo " " & objParameter.Name & _
            ", type=" & objParameter.Type & _
            ", direction=" & objParameter.Direction & _
            ", size=" & objParameter.Size
    Next
    On Error GoTo 0
    
    WScript.Echo String(40,"-")
    
    Next
```

> **随书光盘** 你可以在随书附带的光盘上找到此脚本以及本章列出的其他脚本。

### 理解数据库之间的差异

尽管 ADO 为各种数据源提供了相当统一的访问方式，但一些数据源的要求与其他数据源略有不同。为了防止你因为这些不同的要求而陷入困境，我们将尽可能多地解释它们，重点介绍我们在初次使用 ADO 时遇到问题的地方。

#### 文本文件

文本文件的问题在于连接字符串不指定文件。

```sql
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\Data\;Extended
Properties=Text;HDR=Yes;FMT=Delimited;
```

连接字符串仅指定文件所在的*路径*。你在编写查询时指定文件，用文件名替换表名。

```sql
SELECT Column1,Column2 FROM MyTextData.csv
```

文本文件还必须包含列标题。换句话说，文件的第一行必须是每个列的名称。文本文件可以使用逗号、制表符或其他常见字符进行分隔。在逗号分隔值（CSV）文件中，任何包含逗号的值必须在双引号内进一步分隔。

> **提示** 由于文本文件对格式如此挑剔，我们通常发现将现有的 CSV 或其他文本文件加载到 Excel 中，将其另存为 Excel 工作簿，然后直接在该格式中进行处理会更容易。

#### Excel 工作簿

Excel 工作簿使用我们已向你展示的大多数技术。然而，有时会引起问题的一件事是工作表名称，它们在 ADO 中充当表名。例如，如果你有一个名为 *Sheet1* 的工作表，你需要这样编写查询。

```sql
SELECT column1, column2 FROM [$Sheet1]
```

另请注意，Excel 数据库提供程序使用工作表第一行的值作为列名。虽然你也可以使用列标签作为名称，但我们不推荐这种技术。

```sql
SELECT A, B, C FROM [$Sheet1]
```

六个月后当你阅读脚本时，将很难记住 A、B 和 C 应该代表什么。相反，创建能描述列中数据的列名。*UserName*、*UserPassword*、*ComputerName*、*ServicePackVersion* 等都是很好的列名示例，当你几个月后需要处理脚本时，它们将易于理解且清晰。

#### Access 数据库

Access 与其他提供程序最大的区别在于 Access 的日期分隔符。大多数数据库允许你将日期视为字符串。

```sql
SELECT Column1, Column2 FROM Table WHERE DateField = '1/1/2005'
```

但是，Access 要求日期用井号或磅号（#）字符分隔。

```sql
SELECT Column1, Column2 FROM Table WHERE DateField = #1/1/2005#
```

除此之外，你使用 Access 的方式与我们向你展示的其他技术大致相同。

> **提示** 如果你执行查询后脚本返回错误，指示一个或多个参数不正确，请检查列名的拼写。此类错误通常是 Access 告诉你它未识别你指定的某个列名的方式。

> **提示** 无论何时调试查询，一个技巧是直接在 Access 中打开数据库。在那里，你可以创建一个新查询，切换到 SQL 视图，并粘贴你正在调试的任何查询。你可以通过单击运行查询（!）按钮来执行查询，Access 将立即显示任何错误，通常比通过 ADO 获得的错误包含更多详细信息。查询调试完成后，你可以将其移回脚本中。

#### SQL Server 数据库

SQL Server 数据库本质上是 ADO 构建所围绕的标准，因此它们与我们目前向你展示的示例和技术没有任何差异。然而，由于 SQL Server 是一个真正的*后端*数据库，而不仅仅像 Access、Excel 或文本文件那样是一个文件，因此 SQL Server 对某些动态记录集功能的支持较少。使用 SQL Server 时，你也需要更加小心，并理解其他人可能正在使用服务器处理相同或其他数据库中的数据。你应始终指定要检索的列，尽可能少地检索行和列，并使用仅向前或静态记录集（这有助于减少 SQL Server 计算机上的开销）。

> **提示** 与 Access 类似，直接在 SQL Server 中调试查询可能更容易。只需打开 SQL Server 的查询分析器工具（它是 SQL Server 管理工具的一部分，运行需要许可证）。对于 SQL Server 2005，请使用 Management Studio（查询分析器在 SQL Server 2005 之前是独立工具）。在该工具中，您可以创建并执行新查询。与 Access 一样，您将立即获得关于查询中任何问题的详细反馈。查询调试完成后，您可以将其移回脚本中。

### 理解 SQL

SQL 是数据库的通用语言，ADO 是围绕它构建的。虽然可以在不使用 SQL 的情况下使用 ADO，但当与 SQL 语言结合使用时，您将获得 ADO 最强大的功能和最大的灵活性。在接下来的几节中，我们将向您介绍用于查询和更改数据的 SQL 语言，并为您提供用于数据库脚本的完整工具集。

#### 返回结果的查询

最常见的 SQL 查询是 *SELECT* 查询，用于从数据库中检索数据。最简单的 *SELECT* 查询形式是从给定表中检索所有列和行。

```sql
SELECT * FROM MyTable
```

通过指定要查询的列（即使查询表中的所有列），可以提高脚本的性能和可维护性。

```sql
SELECT UserName, UserID, Description FROM MyTable
```

> **最佳实践** SQL 不区分大小写。但通常，SQL 关键字（如 *SELECT* 和 *FROM*）使用全大写，而对象名称（如列名和表名）使用驼峰命名法。

##### WHERE 子句

您可以且应该将查询返回的行限制为仅需要的行。*WHERE* 子句提供过滤机制并限制行数。

```sql
SELECT UserName, UserID, Description
FROM MyTable
WHERE UserName = 'DonJ'
```

WHERE 子句可以包含任何类型的列与值比较，类似于 VBScript 的 If...Then 结构。以下是一些比较示例。

- 字符串比较：
  `WHERE UserName = 'DonJ'`
- 通配符字符串比较：
  `WHERE UserName LIKE 'Don%'`
  这将匹配任何以 Don 开头的字符串。
  `WHERE UserName LIKE '%on%'`
  这将匹配任何包含 on 的字符串。
- 数值比较：
  `WHERE ServicePackVer > 2`
- 列表比较：
  `WHERE ServicePackVer In (1,2,3)`
  这将匹配 ServicePackVer 列包含 1、2 或 3 的任何行。
- 范围比较：
  `WHERE StartDate BETWEEN '1/1/2000' AND '1/1/2001'`
- 多条件比较：
  `WHERE (UserName Is Null) or (UserName = '')`
  这将匹配 UserName 列包含特殊 Null 值或包含空字符串的行。

##### TOP 子句

限制返回行数的另一种方法是使用 TOP 子句。此子句适用于 SQL Server 和 Access，也可与其他数据库提供商配合使用。您可以选择返回特定行数或特定百分比的行。

```sql
SELECT TOP 5 UserName FROM Users
SELECT TOP 5 PERCENT ComputerName FROM Computers
```

当然，TOP 可以与 WHERE 结合以进一步限制查询返回的结果。您还可以添加 ORDER BY 子句按指定列对结果进行排序。当 WHERE 与 TOP 结合时，记录首先被排序，然后执行 TOP 子句，因此您将获得基于排序条件的前若干行。以下是一些使用 TOP 和 ORDER BY 的示例。

```sql
SELECT UserName, UserID FROM Users ORDER BY UserName
SELECT TOP 5 ComputerName FROM Computers ORDER BY InstallDate
SELECT UserName FROM Users ORDER BY DateAdded DESC
```

> **注意** *TOP* 子句的确切工作方式可能非常令人困惑。例如，假设您有一个表包含名为 *Version* 的列。在您的表中，*Version* 列仅包含值 1 或值 2，没有其他值。如果您执行类似 `SELECT TOP 5 Version FROM MyTable` 的查询，查询将返回表中的所有行，因为它将尝试选择 *Version* 列的前 5 个值。由于只有两个可用值，所有行都将符合 *TOP* 子句的条件。这对大多数符合 SQL 的数据库（包括 Access）都适用。某些数据库可能行为不同，并非每个数据库都支持 *TOP* 子句。

##### *ORDER BY* 子句

*ORDER BY* 子句默认按升序排序。在前面的示例中，我们添加了 *DESC* 运算符以强制执行反向（降序）排序，使最大的 *DateAdded* 值（最近的日期）首先出现。

> **注意** 每个数据库提供商支持特定版本和方言的 SQL。我们在此处介绍的技术几乎适用于任何数据库，但您使用的数据库可能具有额外的查询功能。

##### *JOIN* 子句

*JOIN* 子句通过某个相关列连接两个数据库表，生成一组结合了两个连接表数据的查询结果。例如，假设您有一个包含两个表 *Computers* 和 *Hotfixes* 的数据库。Computers 表包含计算机的基本信息，Hotfixes 表包含有关已安装热修补程序的信息。计算机上安装的每个热修补程序在 Hotfixes 表中由单行表示。Computers 表的布局可能如下。

| ComputerID | ComputerName | InstallDate | WindowsVer | ServicePackVer |
|---|---|---|---|---|
| 2 | GS77834 | 1/1/2001 | 5.1 | 2 |
| 3 | RM88167 | 2/14/2001 | 5.1 | 1 |
| 4 | ZW85839 | 3/15/2001 | 5.1 | 2 |

Hotfixes 表可能如下所示。

| HotfixID | ComputerID | HFInstallDate |
|---|---|---|
| 2 | 2 | 4/1/2004 |
| 3 | 2 | 4/13/2004 |
| 4 | 2 | 5/11/2005 |
| 5 | 3 | 4/1/2004 |

*ComputerID* 列链接或连接这些表。通过查询 Hotfixes 表中所有 Computer ID 为 2 的行，您将找到安装在计算机 GS77834 上的所有热修补程序。可以在单个记录集中查询每个表的所有信息。生成的记录集可能如下。

| ComputerID | HotfixID | HFInstallDate | ComputerName | InstallDate | WindowsVer | ServicePackVer |
|---|---|---|---|---|---|---|
| 2 | 2 | 4/1/2004 | GS77834 | 1/1/2001 | 5.1 | 2 |
| 2 | 3 | 4/13/2004 | GS77834 | 1/1/2001 | 5.1 | 2 |
| 2 | 4 | 5/11/2005 | GS77834 | 1/1/2001 | 5.1 | 2 |

以下是创建此记录集的查询。

```sql
SELECT c.ComputerID, c.ComputerName, c.InstallDate, c.WindowsVer, c.ServicePackVer,
hf.HotfixID, hf.HFInstallDate
FROM Computers c INNER JOIN Hotfixes hf
ON c.ComputerID = hf.ComputerID
```

请注意此查询的工作方式。

- 列名以 *c* 或 *hf* 为前缀，指示每列所在的表。请注意，查询的 FROM 部分中的表名被赋予了 *c* 和 *hf* 别名。
- 列别名是必需的，因为表共享一个公共列名：*ComputerID*。别名允许 ADO 确定您所指的列。
- FROM 部分中的 INNER JOIN 子句指定要连接的表。
- ON 子句指定连接两个表的列。
- 您还可以添加 TOP、WHERE 或 ORDER BY 子句以进一步过滤或排序结果集。

包含 *JOIN* 子句的查询可能变得相当复杂，尤其是涉及两个以上表时。我们发现使用像 Microsoft Access 这样提供可视查询构建器的工具来创建这些复杂查询更容易。在 Access 中以图形方式构建查询后，您可以切换到 SQL 视图，将 SQL 查询语法复制到剪贴板，然后将其粘贴到脚本中。

#### 更改数据的查询

我们之前提到，动态记录集方法——Update、Delete 和 AddNew——可用于添加和更改数据。动态记录集方法也可与 *SQL INSERT、UPDATE* 和 *DELETE* 查询一起使用，这些查询更改数据但不会将任何行返回到记录集。您通过使用 *Connection* 或 *Command* 对象的 *Execute* 方法来执行这些查询。但是，与前面的示例不同，您不会将 *Recordset* 对象设置为结果，因为这些查询不返回任何结果。

##### *DELETE* 查询

要删除数据，请在查询中指定表名。此查询将删除 `Users` 表中的所有内容。

```
DELETE FROM Users
```

请注意，查询中未包含列列表；这是不需要的，因为删除的是整行。无法只删除单个列，因此无需指定列列表。大多数情况下，你会添加一个 *WHERE* 子句来限制删除的范围。

```
DELETE FROM Users WHERE UserDeactivated = 1
```

请记住，*DELETE* 查询没有“撤销”功能。记录一旦被删除，就永远消失了，除非你做了备份。

##### *UPDATE* 查询

你使用 *UPDATE* 查询来更改表中现有行的数据。查询的基本形式如下所示。

```
UPDATE MyTable SET Column1 = 'value1', Column2 = 'value2'
WHERE Column = 'value'
```

省略 *WHERE* 子句会导致更改应用于数据库的所有行，因此除非你想修改每一行，否则请务必指定一个有效的 *WHERE* 子句。你可以在 *SET* 部分更改任意数量的列，方法是用逗号分隔每个 *column=value* 对。

##### *INSERT* 查询

你使用 *INSERT* 查询向数据库添加新行。你必须指定要插入行的表、要提供值的列以及这些列的值。查询的基本形式如下所示。

```
INSERT INTO Table (Column1,Column2,Column3)
VALUES ('value1', 'value2', 'value3')
```

> **注意** 注意，字符串值包含在单引号中。数值则不需要。在 SQL Server 和大多数其他数据库系统中，日期值也包含在单引号中。Access 是一个例外，它要求日期值用井号 (#) 括起来。

作为最佳实践，你应该为每一列提供一个值。最常见的 INSERT 查询错误之一就是没有为列提供必需的值。例如，一个数据库可能定义了一个名为 `Description` 的列，并允许该列为 `Null` 或空。在这种情况下，你可以合法地从列列表中省略 `Description`。在其他情况下，数据库可能为列定义了默认值，这意味着如果你不提供值，数据库将为该列提供值。在这种情况下，如果你对默认值满意，你可以从 INSERT 查询中省略该列。在所有其他情况下——当没有默认值，且列不允许空值或 `Null` 值时，你必须在查询中包含该列并为其提供值。

另一个常见错误是提供了不正确的数据类型，例如为只能存储数值数据的列提供了字符串值。如果发生这种情况，你的 INSERT 查询通常会返回一个指示类型不匹配的错误。当然，具体的错误取决于你使用的数据库类型。

### 查看 ActiveX 数据对象

清单 7-2 连接到活动目录中的每台计算机，并查询其当前的服务包版本。然后将这些信息添加到一个 Access 数据库中。请注意，此脚本通过名为 `ServicePackDB` 的 ODBC DSN 连接到数据库，你需要手动创建该 DSN。

在随书附带的 CD 上，包含了一个示例 Access 数据库（具有相应的表）以及清单 7-2。

```
清单 7-2 创建服务包清单
'使用所有 AD 计算机及其当前服务包版本更新 Access 数据库

'注意：请参阅 UpdateDB 子程序；需要预先定义一个 ODBC DSN。

'连接到 AD 的根目录
Dim rootDSE, domainObject
Set rootDSE=GetObject("LDAP://RootDSE")
domainContainer = rootDSE.Get("defaultNamingContext")
Set oDomain = GetObject("LDAP://" & domainContainer)

'从域根目录开始
workwithObject(oDomain)

Sub workwithObject(oContainer)
Dim oADObject
For Each oADObject in oContainer
Select Case oADObject.Class
Case "computer"
    'oADObject 代表一个计算机对象；
    '获取服务包版本并将其记录到数据库
    Dim strComputer
    strComputer = oADObject.cn
    wScript.Echo strComputer
    UpdateDB strComputer, GetSPVer(strComputer)
Case "organizationalUnit" , "container"
    'oADObject 是一个组织单元 (OU) 或容器...
    '遍历其对象
    workwithObject(oADObject)
End select
Next
End Sub

Sub UpdateDB(strComputer, strSPVer)
Dim objConn, objRS, strSQL
Set objConn = CreateObject("ADODB.Connection")
objConn.open "ServicePackDB"

'检查数据库中是否存在该计算机
Set objRS = objConn.Execute("SELECT ComputerName FROM Computers " & _
    "WHERE ComputerName = '" & strComputer & "'")
If objRS.EOF And objRS.BOF Then
    '计算机不在数据库中 = 添加
    strSQL = "INSERT INTO Computers (ComputerName," & _
        "ServicePackVersion,LastCheck) VALUES(" & _
        "'" & strComputer & "', '" & _
        "'" & strSPVer & "', '" & _
        "'#" & FormatDateTime(Now,2) & "#)"
Else
    '计算机在数据库中 = 更新
    strSQL = "UPDATE Computers SET " & _
        "ServicePackVersion = '" & strSPVer & "', " & _
        "LastCheck = #'" & FormatDateTime(Now,2) & "#' " & _
        "WHERE ComputerName = '" & strComputer & "'"
End If
objRS.Close
objConn.Execute strSQL
objConn.Close
End Sub

Function GetSPVer(strComputer)
On Error Resume Next
Dim objWMIService
Dim propValue
Dim objItem
Dim SWBemlocator
Dim colItems
Dim strSPVer
Set SWBemlocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer, _
    "\\root\\CIMV2")
Set colItems = objWMIService.ExecQuery("Select * " & _
"from win32_OperatingSystem",,48)
For Each objItem in colItems
    strSPVer= objItem.ServicePackMajorVersion & "." & _
        objItem.ServicePackMinorVersion
    Next
GetSPVer = strSPVer
End Function
```

让我们更详细地看看这个脚本在做什么。请注意，脚本初始注释行中包含了关于 ODBC DSN 的提醒，这样未来运行脚本的人可以轻松看到他们需要设置的 DSN，脚本才能正常工作。

```
'使用所有 AD 计算机及其当前服务包版本更新 Access 数据库

'注意：请参阅 UpdateDB 子程序；需要预先定义一个 ODBC DSN。
```

脚本继续连接到默认域的根目录。这意味着脚本需要在你想操作的域内的一台计算机上运行。顺便说一句，为了使脚本正常工作，你需要成为该域中每台计算机的本地管理员。理想情况下，你应该以域管理员组成员的身份运行脚本。

```
'连接到 AD 的根目录
Dim rootDSE, domainobject
Set rootDSE=GetObject("LDAP://RootDSE")
domainContainer = rootDSE.Get("defaultNamingContext")
Set oDomain = GetObject("LDAP://" & domainContainer)
```

调用 *WorkWithObject* 子程序，并传递一个对域根目录的引用。

```
'从域根目录开始
workwithobject oDomain
```

该子程序旨在枚举当前容器中的每个对象。一个 *Select...Case* 结构处理 *Computer* 和其他容器对象。对于 *Computer* 对象，使用 *GetSPVer* 函数查询服务包版本，使用 *UpdateDB* 子程序将信息写入数据库。对于容器或组织单元 (OU)，脚本递归调用 *WorkWithObject* 子程序，确保无论目录嵌套多深，每个对象都会被处理。

```
Sub workwithobject(oContainer)
    Dim oADObject
    For Each oADObject in oContainer
        Select Case oADObject.Class
            Case "computer"
                'oADObject 代表一个计算机对象；
                '获取服务包版本并将其记录到数据库
```



## 使用 ADSI 脚本工具

微软的 Scripting Guys 团队创建了一个 HTML 应用程序 (HTA)，旨在让编写 ADSI 脚本变得稍微容易一些。类似于他们广受欢迎的、用于编写 WMI 脚本的 Scriptomatic，ADSI Scriptomatic（也称为 EZ-AD Scriptomatic）会编写基于 LDAP 的脚本，这些脚本能够创建、修改和删除各种类型的 Active Directory 对象。如后页图 8-1 所示，该工具生成的脚本相当简短。

第三部分：高级脚本技术、工具和技术

![](img/4fefd6988ba5d4a92a65127617ca24c2_227_0.png)

图 8-1 使用 ADSI 脚本工具创建用户账户

从第一个下拉列表中选择一个新任务会改变脚本。然而，请注意图 8-2，其中现在显示的任务是删除用户账户，但脚本的变化并不大。

![](img/4fefd6988ba5d4a92a65127617ca24c2_227_1.png)

图 8-2 使用 ADSI 脚本工具删除用户账户

现在将对象类型从用户更改为计算机，你会看到脚本的变化仍然不大。事实上，只有最后几行发生了显著变化，如图 8-3 所示。第二行也发生了变化，但这只是一个字符串变量，在此例中定义了要删除的对象的名称。

![](img/4fefd6988ba5d4a92a65127617ca24c2_228_0.png)

图 8-3 使用 ADSI 脚本工具删除计算机账户

脚本工具代码的大部分是样板代码（无论你要求工具执行什么操作，这部分代码都不会改变），这一事实使得代码更容易在你自己的脚本中重用，从而为你的 ADSI 脚本提供一个良好的开端。

![](img/4fefd6988ba5d4a92a65127617ca24c2_228_1.png)

> **注意** 如果你还没有下载，请在此处下载 Scriptomatic：
> http://www.microsoft.com/technet/scriptcenter/tools/admatic.mspx
> （此链接包含在随附光盘中；点击 ADSI (Active Directory Service Interfaces) Scriptomatic。）

### 连接到域

脚本工具使用一个基本代码块来连接到域。实际上，该代码连接到一个容器，这个容器可以包括域本身、组织单元 (OU) 或类似于 OU 的容器，例如内置的 Users 容器。执行此操作的代码在下一页。



第三部分：高级脚本技术、工具与技术

```vb
strContainer = ""
strName = "EzAdUser"
```

```vb
'***************************************************
'*           连接到容器                               *
'***************************************************
Set objRootDSE = GetObject("LDAP://rootDSE")
If strContainer = "" Then
    Set objContainer = GetObject("LDAP://" & _
        objRootDSE.Get("defaultNamingContext"))
Else
    Set objContainer = GetObject("LDAP://" & strContainer & "," & _
        objRootDSE.Get("defaultNamingContext"))
End If
```

此代码尝试连接到 *strContainer* 变量中指定的位置。默认情况下，该变量是一个空字符串，你可以看到 *If...Else...End If* 结构，它会连接到域的默认命名上下文。但是，如果你用类似 *ou=Sales* 或 *cn=Users*（两者都指定了一个容器）的内容填充该变量，脚本将连接到该容器以检索默认命名上下文。

显然，*strName* 变量应填充你将要使用的对象的名称。在建立与域或容器的连接后，会有一个名为 *objContainer* 的变量代表该容器。你使用该容器对象的方法来创建、删除和修改对象。

### 创建对象

创建对象涉及指示将要存储该对象（通常是组织单位）的容器来创建该对象。容器为此目的有一个 *Create* 方法，你只需指定要创建的对象的类以及新对象将使用的规范名称 (*cn*)。容器将创建该对象并返回其引用。对于大多数 Active Directory 对象，你还需要指定一个安全账户管理器 (SAM) 名称，这通常就是账户名称。你可以使用新对象的 *Put* 方法设置此名称，然后使用其 *SetInfo* 方法将信息保存回目录。以下是用户账户的示例。

```vb
Set objUser = objContainer.Create("user", "cn=" & strName)
objUser.Put "SAMAccountName", strName
objUser.SetInfo
```

计算机账户不需要 SAM 名称。

```vb
Set objComputer = objContainer.Create("computer", "cn=" & strName)
objComputer.SetInfo
```

联系人对象也不需要 SAM 名称。实际上，请注意只有变量名——*objContact*——和传递给 *Create* 方法的类是不同的。变量名甚至不必不同，但这确实使脚本更清晰。即使是组织单位账户也几乎完全相同。

```vb
Set objOrganizationalUnit = objContainer.Create("organizationalUnit", "ou=" & strName)
objOrganizationalUnit.SetInfo
```

组账户的差异更大。除了脚本末尾较长的代码外，开头还添加了常量。创建组的主要代码如下所示。

```vb
Set objGroup = objContainer.Create("group", "cn=" & strName)
objGroup.Put "sAMAccountName", strName
objGroup.Put "groupType", ADS_GROUP_TYPE_GLOBAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
objGroup.SetInfo
```

你的脚本不仅要为组指定 SAM 账户名称，还必须指定正在创建的组的类型。这是通过设置 *groupType* 属性来完成的。脚本开头的常量提供了你的选项。

```vb
ADS_GROUP_TYPE_GLOBAL_GROUP = &h2
ADS_GROUP_TYPE_LOCAL_GROUP = &h4
ADS_GROUP_TYPE_UNIVERSAL_GROUP = &h8
ADS_GROUP_TYPE_SECURITY_ENABLED = &h80000000
```

选择前三个选项之一来创建分发列表（或组）。要创建安全组，请使用布尔 *Or* 运算符并附加 *SECURITY_ENABLED* 常量。刚刚显示的示例是 Scriptomatic 在创建组时生成的默认脚本，它将创建一个新的全局安全组。

### 检索对象信息

使用 Scriptomatic 读取对象会生成相当长的脚本。这是你从该工具获得的最有用的脚本之一，因为它显示了它支持的每个对象类的许多属性。以下是用户脚本中检索对象信息的部分。它假设连接到域的样板代码已经执行。

```vb
WScript.Echo vbCrLf & "** 常规属性页**"
WScript.Echo "** （单值属性） **"
strname = objItem.Get("name")
WScript.Echo "name: " & strname
strgivenName = objItem.Get("givenName")
WScript.Echo "givenName: " & strgivenName
strinitials = objItem.Get("initials")
WScript.Echo "initials: " & strinitials
strsn = objItem.Get("sn")
WScript.Echo "sn: " & strsn
strdisplayName = objItem.Get("displayName")
WScript.Echo "displayName: " & strdisplayName
strdescription = objItem.Get("description")
WScript.Echo "description: " & strdescription
strphysicalDeliveryOfficeName = objItem.Get("physicalDeliveryOfficeName")
WScript.Echo "physicalDeliveryOfficeName: " & strphysicalDeliveryOfficeName
strtelephoneNumber = objItem.Get("telephoneNumber")
WScript.Echo "telephoneNumber: " & strtelephoneNumber
strmail = objItem.Get("mail")
WScript.Echo "mail: " & strmail
strwWWHomePage = objItem.Get("wWWHomePage")
WScript.Echo "wWWHomePage: " & strwWWHomePage

WScript.Echo vbCrLf & "** 常规属性页**"
WScript.Echo "** （多值属性） **"
strotherTelephone = objItem.GetEx("otherTelephone")
WScript.Echo "otherTelephone:"
For Each Item in strotherTelephone
    WScript.Echo vbTab & Item
Next
strurl = objItem.GetEx("url")
WScript.Echo "url:"
For Each Item in strurl
    WScript.Echo vbTab & Item
Next

WScript.Echo vbCrLf & "** 地址属性页**"
WScript.Echo "** （单值属性） **"
strstreetAddress = objItem.Get("streetAddress")
WScript.Echo "streetAddress: " & strstreetAddress
strl = objItem.Get("l")
WScript.Echo "l: " & strl
strst = objItem.Get("st")
WScript.Echo "st: " & strst
strpostalCode = objItem.Get("postalCode")
WScript.Echo "postalCode: " & strpostalCode
strc = objItem.Get("c")
WScript.Echo "c: " & strc

WScript.Echo vbCrLf & "** 地址属性页**"
WScript.Echo "** （多值属性） **"
strpostOfficeBox = objItem.GetEx("postOfficeBox")
WScript.Echo "postOfficeBox:"
For Each Item in strpostOfficeBox
    WScript.Echo vbTab & Item
Next

WScript.Echo vbCrLf & "** 账户属性页**"
WScript.Echo "** （单值属性） **"
struserPrincipalName = objItem.Get("userPrincipalName")
WScript.Echo "userPrincipalName: " & struserPrincipalName
strdc = objItem.Get("dc")
WScript.Echo "dc: " & strdc
strsAMAccountName = objItem.Get("sAMAccountName")
WScript.Echo "sAMAccountName: " & strsAMAccountName
struserworkstations = objItem.Get("userworkstations")
WScript.Echo "userWorkstations: " & struserworkstations
WScript.Echo vbCrLf & "** 账户属性页**"
WScript.Echo "** （userAccountControl 属性） **"
Set objHash = CreateObject("Scripting.Dictionary")
objHash.Add "ADS_UF_SMARTCARD_REQUIRED", &h4000
objHash.Add "ADS_UF_TRUSTED_FOR_DELEGATION", &h80000
objHash.Add "ADS_UF_NOT_DELEGATED", &h100000
objHash.Add "ADS_UF_USE_DES_KEY_ONLY", &h200000
objHash.Add "ADS_UF_DONT_REQUIRE_PREAUTH", &h400000
intuserAccountControl = objItem.Get("userAccountControl")
For Each Key in objHash.Keys
    If objHash(Key) And intuserAccountControl Then
        WScript.Echo Key & " 已启用。"
    Else
        WScript.Echo Key & " 已禁用。"
    End If
Next
If objItem.IsAccountLocked = True Then
    WScript.Echo "ADS_UF_LOCKOUT 已启用"
Else
    WScript.Echo "ADS_UF_LOCKOUT 已禁用"
End If

If Err.Number = -2147467259 Or _
    objItem.AccountExpirationDate = "1/1/1970" Then
    WScript.Echo "账户不过期。"
Else
    WScript.Echo "账户到期于: " & objItem.AccountExpirationDate
End If

WScript.Echo vbCrLf & "** 配置文件属性页**"
WScript.Echo "** （单值属性） **"
strprofilePath = objItem.Get("profilePath")
WScript.Echo "profilePath: " & strprofilePath
strscriptPath = objItem.Get("scriptPath")
WScript.Echo "scriptPath: " & strscriptPath
strhomeDirectory = objItem.Get("homeDirectory")
WScript.Echo "homeDirectory: " & strhomeDirectory
strhomeDrive = objItem.Get("homeDrive")
WScript.Echo "homeDrive: " & strhomeDrive

WScript.Echo vbCrLf & "** 电话属性页**"
WScript.Echo "** （单值属性） **"
strhomePhone = objItem.Get("homePhone")
WScript.Echo "homePhone: " & strhomePhone
strpager = objItem.Get("pager")
WScript.Echo "pager: " & strpager
strmobile = objItem.Get("mobile")
WScript.Echo "mobile: " & strmobile
strfacsimileTelephoneNumber = objItem.Get("facsimileTelephoneNumber")
WScript.Echo "facsimileTelephoneNumber: " & strfacsimileTelephoneNumber
stripPhone = objItem.Get("ipPhone")
WScript.Echo "ipPhone: " & stripPhone
strinfo = objItem.Get("info")
WScript.Echo "info: " & strinfo
```



## 第214页 第三部分：高级脚本技术、工具与技术

```
WScript.Echo VbCrLf & "** 电话属性页**"
WScript.Echo "** (多值属性) **"
strotherHomePhone = objItem.GetEx("otherHomePhone")
WScript.Echo "otherHomePhone:"
For Each Item in strotherHomePhone
    WScript.Echo vbTab & Item
Next
strotherPager = objItem.GetEx("otherPager")
WScript.Echo "otherPager:"
For Each Item in strotherPager
    WScript.Echo vbTab & Item
Next
strotherMobile = objItem.GetEx("otherMobile")
WScript.Echo "otherMobile:"
For Each Item in strotherMobile
    WScript.Echo vbTab & Item
Next
strotherFacsimileTelephoneNumber = objItem.GetEx("otherFacsimileTelephoneNumber")
WScript.Echo "otherFacsimileTelephoneNumber:"
For Each Item in strotherFacsimileTelephoneNumber
    WScript.Echo vbTab & Item
Next
strotherIpPhone = objItem.GetEx("otherIpPhone")
WScript.Echo "otherIpPhone:"
For Each Item in strotherIpPhone
    WScript.Echo vbTab & Item
Next
```

```
WScript.Echo VbCrLf & "** 组织属性页**"
WScript.Echo "** (单值属性) **"
strtitle = objItem.Get("title")
WScript.Echo "title: " & strtitle
strdepartment = objItem.Get("department")
WScript.Echo "department: " & strdepartment
strcompany = objItem.Get("company")
WScript.Echo "company: " & strcompany
strmanager = objItem.Get("manager")
WScript.Echo "manager: " & strmanager
```

```
WScript.Echo VbCrLf & "** 组织属性页**"
WScript.Echo "** (多值属性) **"
strdirectReports = objItem.GetEx("directReports")
WScript.Echo "directReports:"
For Each Item in strdirectReports
    WScript.Echo vbTab & Item
Next
```

```
WScript.Echo VbCrLf & "** 环境属性页**"
WScript.Echo "** (终端服务接口的 ADSI 扩展) **"
WScript.Echo "TerminalServicesInitialProgram: " & _
    objItem.TerminalServicesInitialProgram
WScript.Echo "TerminalServicesWorkDirectory: " & _
    objItem.TerminalServicesWorkDirectory
```

```
WScript.Echo "ConnectClientDrivesAtLogon: " & _
    objItem.ConnectClientDrivesAtLogon
WScript.Echo "ConnectClientPrintersAtLogon: " & _
    objItem.ConnectClientPrintersAtLogon
WScript.Echo "DefaultToMainPrinter: " & _
    objItem.DefaultToMainPrinter
```

```
WScript.Echo vbCrLf & "** 会话属性页**"
WScript.Echo "** (终端服务接口的 ADSI 扩展) **"
WScript.Echo "MaxDisconnectionTime: " & _
    objItem.MaxDisconnectionTime
WScript.Echo "MaxConnectionTime: " & _
    objItem.MaxConnectionTime
WScript.Echo "MaxIdleTime: " & _
    objItem.MaxIdleTime
WScript.Echo "BrokenConnectionAction: " & _
    objItem.BrokenConnectionAction
WScript.Echo "ReconnectionAction: " & _
    objItem.ReconnectionAction
```

```
WScript.Echo vbCrLf & "** 远程控制属性页**"
WScript.Echo "** (终端服务接口的 ADSI 扩展) **"
WScript.Echo "EnableRemoteControl: " & _
    objItem.EnableRemoteControl

Select Case objItem.EnableRemoteControl
    Case 0
        WScript.Echo "远程控制已禁用"
    Case 1
        WScript.Echo "远程控制已启用"
        WScript.Echo "需要用户权限"
        WScript.Echo "与会话交互"
    Case 2
        WScript.Echo "远程控制已启用"
        WScript.Echo "不需要用户权限"
        WScript.Echo "与会话交互"
    Case 3
        WScript.Echo "远程控制已启用"
        WScript.Echo "需要用户权限"
        WScript.Echo "查看会话"
    Case 4
        WScript.Echo "远程控制已启用"
        WScript.Echo "不需要用户权限"
        WScript.Echo "查看会话"
End Select
```

```
WScript.Echo vbCrLf & "** 终端服务配置文件属性页**"
WScript.Echo "** (终端服务接口的 ADSI 扩展) **"
WScript.Echo "TerminalServicesProfilePath: " & _
    objItem.TerminalServicesProfilePath
WScript.Echo "TerminalServicesHomeDirectory: " & _
    objItem.TerminalServicesHomeDirectory
WScript.Echo "TerminalServicesHomeDrive: " & _
    objItem.TerminalServicesHomeDrive
```

```
WScript.Echo "AllowLogon: " & _
    objItem.AllowLogon
```

```
WScript.Echo vbCrLf & "** COM+ 属性页**"
WScript.Echo "** (单值属性) **"
WScript.Echo "msCOM-UserPartitionSetLink: "
WScript.Echo " " & objItem.Get("msCOM-UserPartitionSetLink")
```

```
WScript.Echo vbCrLf & "** 成员属性页**"
WScript.Echo "** (单值属性) **"
strprimaryGroupID = objItem.Get("primaryGroupID")
WScript.Echo "primaryGroupID: " & strprimaryGroupID
```

```
WScript.Echo vbCrLf & "** 成员属性页**"
WScript.Echo "** (多值属性) **"
strmemberOf = objItem.GetEx("memberOf")
WScript.Echo "memberOf:"
For Each Item in strmemberOf
    WScript.Echo vbTab & Item
Next
```

```
WScript.Echo vbCrLf & "** 对象属性页**"
WScript.Echo "** (单值属性) **"
strwhenCreated = objItem.Get("whenCreated")
WScript.Echo "whenCreated: " & strwhenCreated
strwhenChanged = objItem.Get("whenChanged")
WScript.Echo "whenChanged: " & strwhenChanged
```

```
objItem.GetInfoEx Array("canonicalName"), 0
WScript.Echo vbCrLf & "** 对象属性页**"
WScript.Echo "** (多值属性) **"
strcanonicalName = objItem.GetEx("canonicalName")
WScript.Echo "canonicalName:"
For Each Item in strcanonicalName
    WScript.Echo vbTab & Item
Next
```

正如你所见，这里包含了大量有用的信息。你几乎可以看到对象的所有主要属性，以及如何从每个属性中检索信息。研究这段代码是探索可用属性、了解它们的功能以及它们在域中为典型用户包含什么值的好方法。事实上，你可以从 Scriptomatic 中复制并粘贴足够的代码来创建一个自动化创建新用户账户的脚本。例如，添加一些数据库代码，你就可以从 Access 数据库中检索新用户信息。

> **提示** 要更改这些属性中的任何一个，请使用 *Put* 或 *PutEx* 方法，而不是 *Get* 或 *GetEx*。

### 使用其他 ADSI 工具

探索 Active Directory 是扩展脚本技能库的好方法。当你遇到一个不熟悉的属性时，你可以通过查看几个现有用户来检查其值。你还可以将属性名称输入搜索引擎，通常会找到关于如何使用它的示例。（在搜索中添加 VBScript 一词可以获得更多特定于脚本的示例。在接下来的几节中，我们将介绍一些特别有用的工具，用于探索 Active Directory 并使 ADSI 脚本编写更容易。

### 使用 ADSI 软件开发工具包

ADSI 软件开发工具包 (SDK) 可以从 Microsoft 网站免费下载。该 SDK 主要供专业软件开发人员使用，但它包含三个我们发现对编写 ADSI 脚本很有用的工具：ADSVW、ADSCmd 和 ADSIDump。

> **在光盘上** 我们在本书附带的光盘上包含了指向 SDK 的链接。你也可以通过 Microsoft TechNet Script Center（网址为 http://www.microsoft.com/technet/scriptcenter）链接到 SDK。

#### ADSVW

Active Directory 浏览器 (ADSVW) 是一个用于探索 Active Directory 的出色工具。与生成相当通用脚本的 Scriptomatic 不同，你可以使用 ADSVW 来浏览你自己的域，这意味着你可以查看域中对象的样本数据，以了解正在使用的内容。首次启动该工具时，选择 ObjectViewer，如图 8-4 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_236_0.png)

图 8-4 启动 ADSVW

接下来，系统会提示你连接到一个特定的对象，如图 8-5 所示。我们通常更喜欢连接到域的根目录。这样，整个域都可以浏览。为此，在 Enter ADs Path 框中输入 **LDAP:**。请确保取消选中 Use OpenObject 复选框，以连接到客户端计算机的默认域。

![](img/4fefd6988ba5d4a92a65127617ca24c2_237_0.png)

图 8-5 使用 ADSVW 连接到默认域

图 8-6 显示了连接到域的浏览器。请注意，OU 等容器在左侧窗格的树视图中单击之前是不可展开的。在图 8-6 中，选择了一个用户对象。在右侧窗格的属性下拉列表中，我们选择了 *nTSecurityDescriptor* 属性。浏览器识别出这是一个特殊属性，并显示安全描述符详细信息。另请注意，显示了两个按钮——SetPassword 和 ChangePassword，提供了特定于该对象类型的功能。

如果你从域中选择一台计算机，视图会发生变化。在图 8-7 中，我们选择了一个更简单的属性，因此右窗格显示有关该对象的常规信息。由于所讨论的对象是计算机，密码按钮被替换为关机按钮。

ADSVW 的图形界面使得从与开发人员——或像你这样的脚本编写者——相同的视角探索域中的对象并查看其属性变得更加容易。你将看到属性名称、它们的值等等，你甚至可以修改这些属性。事实上，ADSVW 可能是一个很好的开发工具，因为你可以用它来验证你的属性名称、对象类，甚至是你放入属性的值，所有这些都无需在编写脚本之前进行。通过首先测试这些内容，你的脚本遇到问题的可能性会大大降低。



## 第八章：高级 ADSI 和 LDAP 脚本编写

![](img/4fefd6988ba5d4a92a65127617ca24c2_238_0.png)

图 8-6 在 ADSVW 中处理用户

![](img/4fefd6988ba5d4a92a65127617ca24c2_238_1.png)

图 8-7 在 ADSVW 中处理计算机

# 第三部分：高级脚本技术、工具和技术

### ADSCmd

ADSCmd，顾名思义，是一个命令行工具。你可以用它来列出域中的对象，包括那些通常无法通过图形工具获取的对象。ADSCmd 可与任何 ADSI 提供程序一起使用。请记住，ADSI 代表 Active Directory Services Interface，但这并不意味着它专为 Active Directory 设计。事实上，与其将其理解为 *Active Directory Services Interface*，不如将其视为 *Active Directory Services Interface*，这意味着它是一个通用的目录服务接口。（ADSI 在 Active Directory 本身出现之前就已存在。）以下是使用 WinNT 提供程序对笔记本电脑运行 ADSCmd 的示例。

```
adscmd list winNT://Don-laptop
__vmware_user__(User)
Administrator(User)
ASPNET(User)
DonJones(User)
Guest(User)
HelpAssistant(User)
IUSR_DON-LAPTOP(User)
IWAM_DON-LAPTOP(User)
SQLDebugger(User)
SUPPORT_388945a0(User)
testuser(User)
VUSR_DON-LAPTOP(User)
WADM_DON-LAPTOP(User)
Administrators(Group)
Backup Operators(Group)
Guests(Group)
Network Configuration Operators(Group)
Power Users(Group)
Remote Desktop Users(Group)
Users(Group)
Debugger Users(Group)
ESR_Administrator(Group)
ESR_Reporter(Group)
HelpServicesGroup(Group)
VS Developers(Group)
__vmware__(Group)
ACS(Service)
Adobe LM Service(Service)
AdobeVersionCue(Service)
Alerter(Service)
ALG(Service)
AppMgmt(Service)
aspnet_admin(Service)
aspnet_state(Service)
Ati HotKey Poller(Service)
AudioSrv(Service)
BITS(Service)
Browser(Service)
BthServ(Service)
CeEPwrSvc(Service)
CFSvcs(Service)
CiSvc(Service)
ClipSrv(Service)
COMSysApp(Service)
CryptSvc(Service)
DcomLaunch(Service)
Dhcp(Service)
...
W3SVC(Service)
WebClient(Service)
winmgmt(Service)
WmcCds(Service)
WmcCdsLs(Service)
WMDM PMSP Service(Service)
WmdmPmSN(Service)
Wmi(Service)
WmiApSrv(Service)
wscsvc(Service)
wuauserv(Service)
WZCSVC(Service)
xmlprov(Service)
Total Number of Objects enumerated is 143
```

> **注意** 为了保持列表简短，我们截断了中间的一些行，但运行时列出了总共 143 个对象。

你会注意到，除了用户和组，WinNT 提供程序还可以连接到服务。（LDAP 提供程序在与 Active Directory 一起使用时，无法连接到服务。）你可以通过使用 WinNT 提供程序连接到这些服务对象来启动和停止服务（我们将在本章后面演示）。以下是使用 ADSCmd 与 LDAP 提供程序连接到域根目录的示例。

```
adscmd list LDAP://company.pri
    CN=Builtin(builtinDomain)
    CN=Computers(container)
    OU=Depts(organizationalUnit)
    OU=Domain Controllers(organizationalUnit)
    OU=Finance(organizationalUnit)
    CN=ForeignSecurityPrincipals(container)
    OU=Groups(organizationalUnit)
    CN=Infrastructure(infrastructureUpdate)
    CN=LostAndFound(lostAndFound)
    OU=MyOU(organizationalUnit)
    CN=NTDS Quotas(msDS-QuotaContainer)
    CN=Program Data(container)
    CN=System(container)
    CN=Users(container)
Total Number of Objects enumerated is 14
```

请注意，只列出了根目录中的对象——也就是我们查询的目录。如果你想查看特定 OU（如 *MyOU*）中的内容，可以执行以下操作。

```
adscmd list LDAP://dc/OU=MyOU,DC=company,DC=pri
OU=AnotherOU(organizationalUnit)
CN=Computer(computer)
CN=Contact(contact)
CN=Group(group)
CN=InetOrgPerson No idea(inetOrgPerson)
CN=Share(volume)
CN=User(user)
Total Number of objects enumerated is 7
```

ADSCmd 是一个有用的工具，可用于快速确定特定容器中的内容。它也可用于测试旨在检索容器的 LDAP 查询。ADSCmd 还可以检索其他对象。例如，刚刚显示的列表表明 *MyOU* 包含一个名为 *User* 的用户帐户。以下是你检索该用户的方法。

```
adscmd dump LDAP://company.pri/CN=User,OU=MyOU,dc=company,
DC=pri
cn                          : User
instanceType                : 4
nTSecurityDescriptor        : Data type is 9
objectCategory              : CN=Person,CN=Schema,CN=Configuration,DC=compan
y,DC=pri
objectClass                 : top, person, organizationalPerson, user
objectSid                   : Data type is 8209
SAMAccountName              : User
```

*dump* 关键字显示的是对象的属性，而不是其子对象，因为在这种情况下，对象（一个用户）没有子对象。这是在将 LDAP 查询添加到脚本之前进行测试的好方法，或者作为故障排除过程的一部分来测试脚本生成的 LDAP 查询。

### ADSIDump

这个强大的命令行实用程序列出域中的每个对象及其大多数属性。信息输出到文件中以便于查看。以下是 ADSIDump 生成的文件的一部分。（请注意，屏幕上显示的输出不如发送到你指定的输出文件完整。）

```
========================================

    ***  DC=company  ***
    ROOT OBJECT
    Full ADS path: "LDAP://DC=company,dc=pri"
    Class: domainDNS
    Schema: LDAP://schema/domainDNS
    Attributes --------------------------
        dc : (BSTR) "company"
        instanceType : (INT) 5
        nTSecurityDescriptor : (Unknown variant type)
        objectCategory : (BSTR) "CN=Domain-DNS,CN=Schema,CN=Configuration,DC=company,DC=pri"
        objectClass : (ARRAY) [  "top"  "domain"  "domainDNS"]
        auditingPolicy : (Unknown variant type)
        creationTime : (Unknown variant type)
        distinguishedName : (BSTR) "DC=company,DC=pri"
        forceLogoff : (Unknown variant type)
        fSMORoleOwner : (BSTR) "CN=NTDS Settings,CN=DC,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=company,DC=pri"
        gPLink : (BSTR) "[LDAP://CN={31B2F340-016D-11D2-945F-00C04FB984F9},CN=Policies,CN=System,DC=company,DC=pri;0]"
        isCriticalSystemObject : (BOOL) TRUE
        lockoutDuration : (Unknown variant type)
        lockoutObservationWindow : (Unknown variant type)
        lockoutThreshold : (INT) 0
        masteredBy : (BSTR) "CN=NTDS Settings,CN=DC,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=company,DC=pri"
        maxPwdAge : (Unknown variant type)
        minPwdAge : (Unknown variant type)
        minPwdLength : (INT) 7
        modifiedCount : (Unknown variant type)
        modifiedCountAtLastProm : (Unknown variant type)
        ms-DS-MachineAccountQuota : (INT) 10
        msDS-AllUsersTrustQuota : (INT) 1000
        msDS-Behavior-Version : (INT) 0
        msDS-masteredBy : (BSTR) "CN=NTDS Settings,CN=DC,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=company,DC=pri"
        msDS-PerUserTrustQuota : (INT) 1
        msDS-PerUserTrustTombstonesQuota : (INT) 10
        name : (BSTR) "company"
        nextRid : (INT) 1003
        nTMixedDomain : (INT) 1
        objectGUID : (Unknown variant type)
        objectSid : (Unknown variant type)
        pwdHistoryLength : (INT) 24
        pwdProperties : (INT) 1
        rIDManagerReference : (BSTR) "CN=RID Manager$,CN=System,DC=company,DC=pri"
        serverState : (INT) 1
        subRefs : (ARRAY) [  "DC=ForestDnsZones,DC=company,DC=pri"  "DC=DomainDnsZones,DC=company,DC=pri"  "CN=Configuration,DC=company,DC=pri"]
        systemFlags : (INT) -1946157056
        uASCompat : (INT) 1
        uSNChanged : (Unknown variant type)
        uSNCreated : (Unknown variant type)
        wellKnownObjects : (ARRAY) []
        whenChanged : (Unknown variant type)
        whenCreated : (Unknown variant type)
```

这仅仅是域本身；域中的每个对象都以类似的方式被分解。（如果你在大型域中运行 ADSIDump，请准备好等待一段时间让文件生成完成！）。以下是输出的另一部分，这次是针对内置容器。

```
*** CN=Builtin ***
    Child of DC=company
    Full ADS path: "LDAP://CN=Builtin,DC=company,dc=pri"
    Class: builtinDomain
    Schema: LDAP://schema/builtinDomain
    Attributes -----------------
        instanceType : (INT) 4
        nTSecurityDescriptor : (Unknown variant type)
        objectCategory : (BSTR) "CN=Builtin-Domain,CN=Schema,CN=Configuration,DC=company,DC=pri"
        objectClass : (ARRAY) [ "top"  "builtinDomain"]
        cn : (BSTR) "Builtin"
        creationTime : (Unknown variant type)
        distinguishedName : (BSTR) "CN=Builtin,DC=company,DC=pri"
        forceLogoff : (Unknown variant type)
        isCriticalSystemObject : (BOOL) TRUE
        lockoutDuration : (Unknown variant type)
        lockoutObservationWindow : (Unknown variant type)
        lockoutThreshold : (INT) 0
        maxPwdAge : (Unknown variant type)
        minPwdAge : (Unknown variant type)
        minPwdLength : (INT) 0
        modifiedCount : (Unknown variant type)
        modifiedCountAtLastProm : (Unknown variant type)
        name : (BSTR) "Builtin"
        nextRid : (INT) 1000
        objectGUID : (Unknown variant type)
        objectSid : (Unknown variant type)
        pwdHistoryLength : (INT) 0
        pwdProperties : (INT) 0
        serverState : (INT) 1
        showInAdvancedViewOnly : (BOOL) FALSE
        systemFlags : (INT) -1946157056
        uASCompat : (INT) 1
        uSNChanged : (Unknown variant type)
        uSNCreated : (Unknown variant type)
        whenChanged : (Unknown variant type)
        whenCreated : (Unknown variant type)
```

你可以使用此技术获取域中每个对象的引用，以及这些对象的关键属性。此输出文件在编写脚本时可以成为宝贵的参考资料，因为它包含属性名称、来自实际域的示例数据等。请注意，它还列出了每个对象的完整 Active Directory 路径，这有助于你优化 LDAP 查询。以下是内置的 Account Operators 组。

```
*** CN=Account Operators ***
    Child of CN=Builtin
    Full ADS path: "LDAP://CN=Account Operators,CN=Builtin,DC=company,dc=pri"
    Class: group
    Schema: LDAP://schema/group
```



### 使用 PrimalScript 专业版 ADSI 向导

属性 -------------------
cn : (BSTR) "Account Operators"
groupType : (INT) -2147483643
instanceType : (INT) 4
nTSecurityDescriptor : (Unknown variant type)
objectCategory : (BSTR) "CN=Group,CN=Schema,CN=Configuration,DC=company,DC=pri"
objectClass : (ARRAY) { "top" "group"}
objectSid : (Unknown variant type)
sAMAccountName : (BSTR) "Account Operators"
adminCount : (INT) 1
description : (BSTR) "Members can administer domain user and group accounts"
distinguishedName : (BSTR) "CN=Account Operators,CN=Builtin,DC=company,DC=pri"
isCriticalSystemObject : (BOOL) TRUE
name : (BSTR) "Account Operators"
objectGUID : (Unknown variant type)
sAMAccountType : (INT) 536870912
systemFlags : (INT) -1946157056
uSNChanged : (Unknown variant type)
uSNCreated : (Unknown variant type)
whenChanged : (Unknown variant type)
whenCreated : (Unknown variant type)

完整的 Active Directory 路径中包含了连接到此组所需的 LDAP 查询语句。如果 LDAP 查询语句显得复杂或令人生畏，只需从 ADSI-Dump 输出文件中借用它们即可，而无需自己编写。

### 使用 PrimalScript 专业版 ADSI 向导

大多数商业脚本编辑器都包含类似于 ADSI Scriptomatic 的 ADSI 向导。然而，PrimalScript 专业版 (http://www.primalscript.com) 采用了不同的方法，我们喜欢它让 ADSI 脚本编写变得如此简单的方式。您首先要选择想要为其编写脚本的 Active Directory 对象类型，如图 8-8 所示。请注意，对于每种对象类型，该向导都可以生成示例代码，展示如何添加、删除或修改该类型的项。

![](img/4fefd6988ba5d4a92a65127617ca24c2_244_0.png)

**图 8-8** 使用 PrimalScript 专业版 ADSI 向导

该向导会生成一系列新类，这些类代表了您选择的对象类型。这些类受到 PrimalScript 的 PrimalSense 功能的支持（该功能会显示列出类成员的菜单，这种功能通常称为*代码提示*），如图 8-9 所示。我们认为这是一个很棒的功能，因为它能帮助您在编写脚本时无需查阅文档。您无需使用普通的对象变量，而是操作像用户、组等行为的对象，这些对象具有您期望的所有属性和方法。

![](img/4fefd6988ba5d4a92a65127617ca24c2_245_0.png)

**图 8-9** 在 PrimalScript ADSI 向导中使用代码提示

添加新用户非常简单。您只需一行代码即可连接到 ADSI，再用一行代码即可创建一个新用户。这是我们基于 ADSI 向导添加的类编写的代码。

```
Dim objADSI, objADSIUser
Set objADSI = New ADSIConnection
Set objADSIUser = New ADSIUser
objADSI.CreateUser("cn=Users","JHicks")
```

这无疑使编写 ADSI 脚本变得更加容易！

### 编写 Active Directory 查询

编写像这样的基本 LDAP 查询语句很容易。

```
LDAP://CN=Account Operators,CN=Builtin,DC=company,dc=pri
```

但这并不总是使用 LDAP 最有效的方式，有时——特别是当您查询大量对象时——简单的查询语句无法满足您的需求。在接下来的两节中，我们将探讨编写 LDAP 查询语句的一些高级技巧。

#### 使用搜索过滤器

LDAP 查询语言包含过滤功能，可以帮助优化您的搜索。例如，您可以添加过滤器来限制搜索返回的对象类别或分类。

```
(objectCategory=person)
```

此示例仅返回 *objectCategory* 属性为 *person* 的对象。在完整的 LDAP 查询语句中使用它可能如下所示。

```
<LDAP://dc=company,dc=pri>; (objectClass=User)
```

这将返回 *company.pri* 域中的所有用户对象。以这种方式设置搜索过滤器有助于使结果集更小、更易于处理，并且更具针对性。

在 VBScript 中如何使用这些过滤器取决于您如何连接到 ADSI。例如，下面是一个 LDAP 连接，它检索所有对象，然后对其进行过滤，以便仅访问用户对象。

```
Set colUsers = GetObject ("LDAP://CN=Users,DC=company,DC=pri")
colUsers.Filter = Array("user")
```

这种技术的一个缺点是，由于是客户端添加过滤器，因此传输到客户端的数据比必要的要多。在下一章中，我们将使用 ActiveX 数据对象 (ADO) 连接到 Active Directory，那时完整的 LDAP 过滤和搜索将是实现更高效查询的一种选择。

#### 使用数据返回限制

ADSI 的一个棘手之处在于它旨在最小化性能方面的负面影响，这有时会导致它产生不是您预期的结果。例如，如果您尝试执行一个将返回一百万对象的查询，ADSI 会将您限制在大约 1,000 个对象，以免过度消耗您正在查询的计算机资源。如果您不知道此限制生效，绕过此限制可能会令人烦恼且困惑。

处理此限制的最佳方法是通过其 ActiveX 数据对象 (ADO) 提供程序访问 ADSI（这是一个我们将在下一章详细讨论的主题）。例如，假设您想查找用户账户的可分辨名称，但您只知道其 NetBIOS 账户名。首先创建一个 *ADO Connection* 对象和一个 *Command* 对象。

```
Dim objConn,objCmd,objRS
Set objConn=Createobject("ADODB.Connection")
Set objCmd=Createobject("ADODB.Command")
```

接下来，将一个字符串变量设置为 *NotFound*。这将是未找到您指定的用户账户时返回的默认值。

```
strGetDN="NotFound"
```

# 第三部分：高级脚本技术、工具和技术

使用 LDAP 查询语句连接到域根目录并检索域的默认命名上下文。

```
Set objRoot=Getobject("LDAP://RootDSE")
Set objDomain=Getobject("LDAP://" & objRoot.get("DefaultNamingContext"))
```

现在开始查询。从域中选择 *sAMAccountName*、*cn* 和 *distinguishedName* 属性，指定对象类别为 *person*，对象类为 *user*，并且 *sAMAccountName* 包含在变量 *samAccount* 中（该变量必须设置为一个值）。

```
strQuery="Select sAMAccountname,cn,distinguishedname from '" & _
    objDomain.AdsPath & "' where objectCategory='person' " & _
    "AND " & "objectclass='user'" & _
    " AND sAMAccountName='" & samAccount & "'"
```

全局编录 (GC) 包含您所需的所有信息，因此您将连接到一个 GC。此查询连接到 GC，循环将遍历它们。最后，*objGC* 代表一个 GC 服务器。

```
set objCatalog=Getobject("GC:")
for each objItem In objCatalog
    Set objGC=objItem
Next
```

现在您可以通过 ADO 设置与 Active Directory 的连接。

```
objConn.Provider="ADSDSOobject"
objConn.Open "Active Directory Provider"
```

连接打开后，将其分配给一个 *Command* 对象。请注意，*Command* 对象的页面大小属性设置为 100。这是我们一次要获取的最大记录数。我们将 *CommandText* 属性设置为我们的查询语句，该语句存储在 *strQuery* 变量中。

```
objCmd.ActiveConnection=objConn
objCmd.Properties("Page Size") = 100
objCmd.Properties("asynchronous")=True
objCmd.Properties("Timeout") =30
objCmd.Properties("Cache Results") = False
objCmd.CommandText=strQuery
```

现在执行 *Command* 对象，并指定其查询结果放置在 ADO *Recordset* 对象中——放入变量 *objRS*。

```
set objRS=objCmd.Execute
```

遍历记录集直到到达其末尾。当我们传递 100 条记录时，ADO 将自动重新查询接下来的 100 条记录。

```
do while not objRS.EOF
    strGetDN=objRS.Fields("distinguishedname")
    objRS.movenext
Loop
```

完成后，关闭记录集和连接。

```
objRS.Close
objConn.Close
```

这是避免记录查询限制的最简单方法。清单 8-1 是完整的脚本，编写为一个函数，以便可以将其添加到您的脚本中。

```
清单 8-1 避免记录查询限制
Function strGetDN(samAccount)

    '给定 NT4 账户名，查找用户账户的可分辨名称
    On Error Resume Next
    Dim objConn,objCmd,objRS
    Set objConn=CreateObject("ADODB.Connection")
    Set objCmd=CreateObject("ADODB.Command")

    strGetDN="NotFound"

    Set objRoot=GetObject("LDAP://RootDSE")
    Set objDomain=GetObject("LDAP://"& objRoot.get("DefaultNamingContext"))

    strQuery="Select sAMAccountname,cn,distinguishedname from '" & _
        objDomain.AdsPath & "' where objectCategory='person' AND " & _
        "objectclass='user'" & _
        " AND SAMAccountName='" & samAccount & "'"

    set objCatalog=GetObject("GC:")
    for each objItem In objCatalog
        Set objGC=objItem
    Next

    objConn.Provider="ADSDSOObject"
    objConn.Open "Active Directory Provider"
    objCmd.ActiveConnection=objConn
    objCmd.Properties("Page Size") = 100
    objCmd.Properties("asynchronous")=True
    objCmd.Properties("Timeout") =30
    objCmd.Properties("Cache Results") = False
    objCmd.CommandText=strQuery

    set objRS=objCmd.Execute

    do while not objRS.EOF
        strGetDN=objRS.Fields("distinguishedname")
        objRS.movenext
    Loop

    objRS.Close
    objConn.Close

    set objConn=Nothing
    set objCmd=Nothing
    set objRoot=Nothing
```



# 第三部分：高级脚本技术、工具与技术

230

```VBScript
set objCatalog=Nothing
set objRS=Nothing

End Function
```

![img/4fefd6988ba5d4a92a65127617ca24c2_249_0.png](img/4fefd6988ba5d4a92a65127617ca24c2_249_0.png)

> 随书光盘
你可以在本书附带的光盘上找到此脚本以及本章列出的其他脚本。

## 脚本化 WinNT 提供程序

WinNT 提供程序经常被管理员忽视，他们没有意识到 ADSI 的能力不仅限于 Active Directory，或者他们认为 WinNT 提供程序仅适用于 Microsoft Windows NT。没有什么比这更偏离事实的了。

请记住，WinNT 提供程序可以连接到计算机上的服务。其中一个服务是 Server 服务，该服务负责处理所有共享文件夹及其文件。例如，假设你编写了这段连接到服务器 Server 服务的简短代码。

```VBScript
sServerName = InputBox ("Server name to check")
sFilename= InputBox ("Full path and filename of the file on the" & _
    "server (use the local path as if you were " & _
    "at the server console)")
' bind to the server's file service
set oFileService = GetObject("winNT://" & sServerName & _
    "/lanmanserver,fileservice")
```

代码返回服务器名称和文件名。其中还有一个对该服务器 lanmanserver 服务的引用，这只是 Server 服务的另一个名称。此服务维护一个 Resources 集合，该集合中的每个项目代表一个打开的资源，例如一个文件。以下代码遍历每个资源，并检查其路径是否与你指定的文件名匹配。

```VBScript
bFoundNone = True
For Each oResource In oFileService.Resources
    If oResource.Path = sFilename Then
        bFoundNone = False
        WScript.Echo oResource.Path & " is opened by " & oResource.User
    End If
Next
```

如果匹配，将显示打开该文件的用户名称。清单 8-2 显示了整个脚本，包括帮助你理解的注释。

# 第 8 章：高级 ADSI 和 LDAP 脚本

231

### 清单 8-2 查找打开的文件

```VBScript
' first, get the server name we want to work with
sServerName = InputBox ("Server name to check")

' get the local path of the file to check
sFilename= InputBox ("Full path and filename of the file on the" & _
" server (use the local path as if you were " & _
"at the server console)")

' bind to the server's file service
set oFileService = GetObject("WinNT://" & sServerName & _
"/lanmanserver,fileservice")

' scan through the open resources until we
' locate the file we want
bFoundNone = True

' use a FOR...EACH loop to walk through the
' open resources
For Each oResource In oFileService.Resources

does this resource match the one we're looking for?
    If oResource.Path = sFilename Then

' we found the file - show who's got it
        bFoundNone = False
        WScript.Echo oResource.Path & " is opened by " & oResource.User
    End If
Next

' if we didn't find the file open, display a msg
If bFoundNone = True Then
    WScript.Echo "Didn't find that file opened by anyone."
End If
```

请注意，此脚本并非在所有情况下都能运行。我们已在 Microsoft Windows XP 上测试过它，但它可能无法在文件服务器上工作。尽管如此，它仍然是一个有用的例证，说明了即使 Windows NT 大体上已成为过去，WinNT 提供程序仍然具有现实意义。

清单 8-3 从下一页开始，是一个 Windows 脚本文件，设计为命令行工具运行。它将批量更改多台计算机上的任何本地帐户密码（例如本地管理员帐户）。它可以从文本文件中读取计算机列表，或者你可以指定域或组织单元中的计算机帐户。

> 注意
此脚本摘自 Don 的书籍 *Microsoft Windows Administrator's Automation Toolkit*（Microsoft Press, 2005），该书包含八十多个用于自动化 Windows 管理的脚本。此处的列表仅为脚本的代码部分。在本书附带的光盘上，你会找到完整的、XML 格式的 WSF 格式脚本。

232

第三部分：高级脚本技术、工具与技术

### 清单 8-3 更改本地密码

```XML
<?xml version="1.0" ?>
<package>
    <job id="changeLocalPassword" prompt="no">
        <job error="false" debug="false" />
        <runtime>
            <description>
                Changes a local account password on one or more computers.

                Use only one of the following:
                    /list:filename     : text file containing one computer name per line
                    /container:ouname  : name of an OU containing computer accounts
                    /computer:name     : run command against single specified computer

                Other arguments are optional.
            </description>
            <named helpstring="Text file to pull computer names from" name="list" required="false" type="string"/>
            <named helpstring="OU to pull computer names from" name="container" required="false" type="string"/>
            <named helpstring="Run command against single specified computer" name="computer" required="false" type="string"/>
            <named helpstring="Display detailed messages" name="verbose" required="false" type="simple"/>
            <named helpstring="Use with /container to include sub-OUs" name="recurse" required="false" type="simple"/>
            <named helpstring="File to log names which can't be reached" name="log" required="false" type="string"/>
            <named helpstring="Reduce timeout wait by pinging before attempting" name="ping" required="false" type="simple"/>
            <named helpstring="User account to change" name="user" required="true" type="string"/>
            <named helpstring="New password for user account" name="password" required="true" type="string"/>
        </runtime>
        <object id="fso" progid="Scripting.FileSystemObject"/>
        <script id="MultiComputer" language="VBScript">
        <![CDATA[
' -------------------------------------------------------
' change local password
' -------------------------------------------------------
' supported: 2003,XP,2000,NT4

'make sure we're running from CScript, not WScript
If LCase(Right(WScript.FullName,11)) <> "cscript.exe" Then
    If MsgBox("This script is designed to work with CScript, but you are running it " & _
              "under WScript. " & _
              "This script may produce a large number of dialog boxes when running under " & _
              "WScript, which you may " & _
              "find to be inefficient. Do you want to continue anyway?",4+256+32,"Script " & _
              "host warning") = 7 Then
        WScript.Echo "Tip: Run ""Cscript //h:cscript"" from a command-line to " & _
                    "make CScript the default scripting host."
        WScript.Quit
    End If
End If
...
```

# 第 8 章：高级 ADSI 和 LDAP 脚本

233

```VBScript
End If
End If

'count arguments
Dim iArgs
If WScript.Arguments.Named.exists("computer") Then iArgs = iArgs + 1
If WScript.Arguments.Named.exists("container") Then iArgs = iArgs + 1
If WScript.Arguments.Named.exists("list") Then iArgs = iArgs + 1
If iArgs <> 1 Then
    WScript.Echo "Must specify either /computer, /container, or /list arguments."
    WScript.Echo "May not specify more than one of these arguments."
    WScript.Echo "Run command again with /? argument for assistance."
    WScript.Quit
End If

'if ping requested, make sure we're on XP or later
Dim bPingAvailable, oLocalWMI, cwindows, owindows
bPingAvailable = False
Set oLocalWMI = GetObject("winmgmts:\\.\root\cimv2")
Set cwindows = oLocalWMI.ExecQuery("Select BuildNumber from win32_operatingSystem",,48)
For Each owindows In cwindows
    If owindows.BuildNumber >= 2600 Then
        bPingAvailable = True
    End If
Next

'was ping requested?
If WScript.Arguments.Named.Exists("ping") Then
    If bPingAvailable Then
        Verbose "will attempt to ping all connections to improve performance"
    Else
        WScript.Echo "*** /ping not supported prior to Windows XP"
    End If
End If

'check required arguments
If Not WScript.Arguments.Named.Exists("password") Or Not
    WScript.Arguments.Named.Exists("user") Then
    WScript.Echo "One or more required arguments are missing."
    WScript.Arguments.ShowUsage
    WScript.Quit
End If

'either /list, /computer, or /container was specified:
Dim sName
If WScript.Arguments.Named("list") <> "" Then
    'specified list - read names from file
    Dim oFSO, oTS
    Verbose "Reading names from file " & WScript.Arguments.Named("list")
    Set oFSO = WScript.CreateObject("Scripting.FileSystemObject")
    On Error Resume Next
    Set oTS = oFSO.OpenTextFile(WScript.Arguments.Named("list"))
    If Err <> 0 Then
        WScript.Echo "Error opening " & WScript.Arguments.Named("list")
        WScript.Echo Err.Description
```

# 第三部分：高级脚本技术、工具与技术

```
wScript.Quit
End If
Do Until oTS.AtEndOfStream
    sName = oTS.ReadLine
    TakeAction sName
Loop
oTS.Close
Elseif wScript.Arguments.Named("container") <> "" Then
    '指定的容器 - 从活动目录读取名称
    Dim oObject, oRoot, oChild
    Verbose "Reading names from AD container " & wScript.Arguments.Named("container")
    On Error Resume Next
    Set oRoot = GetObject("LDAP://rootDSE")
    If Err <> 0 Then
        WScript.Echo "Error connecting to default Active Directory domain"
        WScript.Echo Err.Description
        WScript.Quit
    End If
    Set oObject = GetObject("LDAP://ou=" & wScript.Arguments.Named("container") & _
    "," & oRoot.Get("defaultNamingContext"))
    If Err <> 0 Then
        WScript.Echo "Error opening organizational unit " & wScript.Arguments.Named("container")
        WScript.Echo Err.Description
        WScript.Quit
    End If
    WorkwithOU oObject
Elseif wScript.Arguments.Named("computer") <> "" Then
    '指定的单台计算机
    Verbose "Running command against " & wScript.Arguments.Named("computer")
    TakeAction wScript.Arguments.Named("computer")
End If
'显示输出，以便用户知道脚本已完成
WScript.Echo "Command completed."
'-------------------------------------------------------------------------
' Sub workwithOU
'
' 遍历组织单元中的子对象；如果提供了 /recurse 参数，
' 则调用自身以处理子组织单元
'-------------------------------------------------------------------------
Sub workwithOU(oObject)
    For Each oChild In oObject
        Select Case oChild.Class
            Case "computer"
                TakeAction Right(oChild.Name,Len(oChild.Name)-3)
            Case "user"
            Case "organizationalUnit"
                If wScript.Arguments.Named.Exists("recurse") Then
                    '递归处理子组织单元
                    Verbose "working In " & oChild.Name
                    workwithOU oChild
                End If
        End Select
    Next
End Sub

'-------------------------------------------------------------
' Sub TakeAction
'
' 建立连接并执行特定于命令的代码
'-------------------------------------------------------------
Sub TakeAction(sName)

'详细输出？
Verbose "Connecting to " & sName

'连接前是否 Ping？
If WScript.Arguments.Named.Exists("ping") Then
    If Not TestPing(sName,bPingAvailable) Then
        LogBadConnect(sName)
        Exit Sub
    End If
End If

'##########################################################
'#             命令代码放置于此处             #
'#----------------------------------------------------#
'#                                              #

Dim oUser
On Error Resume Next
Set oUser = QueryADSI(sName,"WinNT://" & sName & "/" & WScript.Arguments.Named("user") & ",user", "")
If Not IsObject(oUser) Then
    WScript.Echo " *** Couldn't retrieve user from " & sName
Else
    On Error Resume Next
    oUser.setpassword WScript.Arguments.Named("password")
    If Err <> 0 Then
        WScript.Echo " *** Couldn't change password on " & sname
        WScript.Echo " " & Err.Description
    Else
        Verbose " Changed password on " & sName
    End If
End If

'#                                        #
'#----------------------------------------------------#
'#          命令代码结束                  #
'##########################################################

End Sub

' -----------------------------------------------------------------------
' Sub LogBadConnect
'
' 将连接失败记录到日志文件。如果文件已存在，则追加。
' -----------------------------------------------------------------------
Sub LogBadConnect(sName)
    If WScript.arguments.Named.Exists("log") Then
        Dim oLogFSO, oLogFile
        Set oLogFSO = WScript.CreateObject("Scripting.FileSystemObject")
        On Error Resume Next
        Set oLogFile = oLogFSO.OpenTextFile(WScript.Arguments.Named("log"),8,True)
        If Err <> 0 Then
            WScript.Echo " *** Error opening log file to log an unreachable computer"
            WScript.Echo " " & Err.Description
        Else
            oLogFile.WriteLine sName
            oLogFile.Close
            Verbose " Logging " & sName & " as unreachable"
        End If
    End If
End Sub


' -----------------------------------------------------------------------
' Function TestPing
'
' 测试与给定名称或地址的连接；返回 True 或 False
' -----------------------------------------------------------------------
Function TestPing(sName,bPingAvailable)
    If Not bPingAvailable Then
        WScript.Echo " Ping functionality not available prior to windows XP"
        Exit Function
    End If
    Dim cPingResults, oPingResult
    Verbose " Pinging " & sName
    Set cPingResults = GetObject("winmgmts://./root/cimv2").ExecQuery("SELECT * FROM win32_PingStatus WHERE Address = '" & sName & "'")
    For Each oPingResult In cPingResults
        If oPingResult.StatusCode = 0 Then
            TestPing = True
            Verbose " Success"
        Else
            TestPing = False
            Verbose " *** FAILED"
        End If
    Next
End Function


' -----------------------------------------------------------------------
' Sub Verbose
'
' 如果提供了 /verbose 参数，则输出状态消息
' -----------------------------------------------------------------------
Sub Verbose(sMessage)
    If wScript.Arguments.Named.Exists("verbose") Then wScript.Echo sMessage End Sub

' Sub LogFile
'
' 将指定文本输出到指定的日志文件。将 Overwrite 设置为 True 以
' 覆盖现有文件，否则将追加到文件。
' 每次调用此子程序都是对文件的全新操作，因此除非在脚本开头，
' 否则不要将 Overwrite 设置为 True。
' ---------------------------------------------------------------------
Sub LogFile(sFile,sText,bOverwrite)
    Dim oFSOOout,oTSOOut,iFlag
    If bOver Then
        iFlag = 2
    Else
        iFlag = 8
    End If
    Set oFSOOout = WScript.CreateObject("Scripting.FileSystemObject")
    On Error Resume Next
    Set oTSOOut = oFSOOout.OpenTextFile(sFile,iFlag,True)
    If Err <> 0 Then
        wScript.Echo "*** Error logging to " & sFile
        wScript.Echo "    " & Err.Description
    Else
        oTSOOut.writeLine sText
        oTSOOut.Close
    End If
End Sub

' Function QueryWMI
'
' 执行 WMI 查询并返回结果。用户和密码可以
' 传入空字符串以使用当前凭据；仅传递空的用户名
' 将提示输入密码。
' ---------------------------------------------------------------------
Function QueryWMI(sName,sNamespace,sQuery,sUser,sPassword)
    Dim oWMILocator, oWMIService, cInstances
    On Error Resume Next

    '创建定位器
    Set oWMILocator = CreateObject("WbemScripting.SWbemLocator")

    If sUser = "" Then

        '无用户 - 使用当前凭据连接
        Set oWMIService = oWMILocator.ConnectServer(sName,sNamespace)
        If Err <> 0 Then
            wScript.Echo "*** Error connecting to WMI on " & sName
            wScript.Echo "    " & Err.Description
            Set QueryWMI = Nothing
            Exit Function
        End If
    Else
        '指定了用户
        If sUser <> "" And sPassword = "" Then
            '无密码 - 需要提示输入密码
            If LCase(Right(WScript.FullName,11)) = "cscript.exe" Then
                'cscript - 尝试使用 ScriptPW.Password 对象
                Dim oPassword
                Set oPassword = WScript.CreateObject("ScriptPW.Password")
                If Err <> 0 Then
                    WScript.Echo " *** Cannot prompt for password prior to windows XP"
                    WScript.Echo "     Either ScriptPW.Password object not present on system, or"
                    WScript.Echo "     " & Err.Description
                    WScript.Echo "     will try to proceed with blank password"
                Else
                    WScript.Echo "Enter password for user '" & sUser & "' on '" & sName & "'."
                    sPassword = oPassword.GetPassword()
                End If
            Else
                'wscript - 使用 InputBox() 提示
                sPassword = InputBox("Enter password for user '" & sUser & "' on '" & sName & "'." & vbCrLf & vbCrLf & _
                                    "WARNING: Password will echo to the screen. Run command with CScript to avoid this.")
            End If
        End If

        '尝试使用提供的凭据连接
        Set oWMIService = oWMILocator.ConnectServer(sName,sNamespace,sUser,sPassword)
        If Err <> 0 Then
            WScript.Echo " *** Error connecting to WMI on " & sName
            WScript.Echo "     " & Err.Description
            Set QueryWMI = Nothing
            Exit Function
        End If
    End If

    '执行查询
    If sQuery <> "" Then
        Set cInstances = oWMIService.ExecQuery(sQuery,,48)
        If Err <> 0 Then
            WScript.Echo "*** Error executing query " & sQuery
            WScript.Echo "     " & Err.Description
            Set QueryWMI = Nothing
            Exit Function
        Else
            Set QueryWMI = cInstances
        End If
    End If
End Function
```



## 使用脚本管理 Active Directory 安全性

在 Active Directory 中，安全性可能是最难用脚本处理的方面之一，主要因为安全本身就很复杂。受托人是被分配权限的用户和组。自主访问控制列表（DACL）应用于每个 Active Directory 对象。DACL 由一个或多个访问控制项（ACE）组成，每个 ACE 为特定的受托人分配特定的权限。用脚本管理这一切可能相当繁琐。

Active Directory 还包括扩展权限。这些权限并非专门应用于某个属性，而是控制特定操作，例如重置用户密码或以用户身份发送消息的权限。扩展权限作为独立对象存储在 Active Directory 中。要使用这些对象进行脚本编写，首先需要为你将要用到的几个值定义常量。

```
Const ADS_ACEACCESS_TYPE_ACCESS_ALLOWED_OBJECT = &H5
Const ADS_FLAG_OBJECT_TYPE_PRESENT = &H1
Const ADS_RIGHT_DS_CONTROL_ACCESS = &H100
```

接下来，连接到一个特定的用户——即你希望授予权限的用户。在我们的示例中，我们将赋予用户 JHicks 重置 DJones 账户密码的权限。使用标准的 LDAP 查询。

```
Set objUser = GetObject("LDAP://CN=DJones,OU=MIS,DC=company,DC=pri")
```

接下来，你需要找到用户的 *ntSecurityDescriptor* 属性（我们早些时候在本章关于 ADSVW 的讨论中讨论过此属性）。从该安全描述符中，你将检索到一组 DACL。

```
Set objSD = objUser.Get("ntSecurityDescriptor")
Set objDACL = objSD.DiscretionaryACLSet
```

现在，你需要向 DACL 添加一个新的 ACE，赋予 JHicks 所需的权限。首先，创建一个新的 ACE 对象。

```
objAce = CreateObject("AccessControlEntry")
```

然后添加新的受托人。你可以使用旧式的“域\用户名”格式。

```
objAce.Trustee = "company\jhicks"
```

将 ACE 的标志设置为零。这些标志控制诸如继承等方面，而我们当前不配置继承。你将使用之前声明的常量为 ACE 对象赋予*允许*权限。

```
objAce.AceFlags = 0
objAce.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
objAce.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT
```

该 ACE 为对象授予权限，且对象类型已存在于 ACL 中。现在你必须指定是*哪个*对象，这通过使用该对象的全局唯一标识符（GUID）来完成。这标识了 ACL 中的对象类型。

```
objAce.ObjectType = "{00299570-246d-11d0-a768-00aa006e0529}"
```

GUID 很难记住（你可以在脚本中将它们声明为常量以提高可读性），因此这里提供一个列表。

-   更改密码：{ab721a53-1e2f-11d0-9819-00aa0040529b}
-   重置密码：{00299570-246d-11d0-a768-00aa006e0529}
-   以...身份接收：{ab721a56-1e2f-11d0-9819-00aa0040529b}
-   以...身份发送：{ab721a54-1e2f-11d0-9819-00aa0040529b}

我们已经指定了正在授予权限，所以现在需要表明授予了哪些特定权限。由于这是一个扩展权限，只有 CONTROL_ACCESS 权限有意义。

```
objAce.AccessMask = ADS_RIGHT_DS_CONTROL_ACCESS
```

将新的 ACE 添加到 DACL。

```
objDACL.AddAce objAce
```

将修改后的 DACL 添加到安全描述符。

```
objSD.DiscretionaryAcl = objDACL
```

现在，将修改后的安全描述符保存回用户帐户。

```
objUser.Put "ntSecurityDescriptor", Array(objSD)
objUser.SetInfo
```

代码清单 8-4 是完整的脚本。

```
代码清单 8-4 在 Active Directory 中添加扩展权限
Const ADS_ACETYPE_ACCESS_ALLOWED_OBJECT = &H5
Const ADS_FLAG_OBJECT_TYPE_PRESENT = &H1
Const ADS_RIGHT_DS_CONTROL_ACCESS = &H100
Set objuser = GetObject("LDAP://CN=DJones,OU=MIS,DC=company,DC=pri")
Set objSD = objuser.Get("ntSecurityDescriptor")
Set objDACL = objSD.DiscretionaryACLSet
objAce = CreateObject("AccessControlEntry")
objAce.Trustee = "company\jhicks"
objAce.AceFlags = 0
objAce.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
objAce.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT
objAce.ObjectType = "{00299570-246d-11d0-a768-00aa006e0529}"
objAce.AccessMask = ADS_RIGHT_DS_CONTROL_ACCESS
objDACL.AddAce objAce
objSD.DiscretionaryAcl = objDACL
objuser.Put "ntSecurityDescriptor", Array(objSD)
objuser.SetInfo
```

要为整个组织单位（OU）授予权限，而不是在初始 LDAP 查询中检索 DJones 用户帐户，需要检索一个 OU。但是，应用于 OU 的权限必须由其子对象继承，这样权限才能应用于 OU *内*的用户，而不仅仅是 OU 本身。代码清单 8-5 是修改后的脚本，其中的更改以粗斜体标出。

```
代码清单 8-5 向 OU 授予权限
Const ADS_ACETYPE_ACCESS_ALLOWED_OBJECT = &H5
Const ADS_FLAG_OBJECT_TYPE_PRESENT = &H1
Const ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT = &H2
Const ADS_RIGHT_DS_CONTROL_ACCESS = &H100
Const ADS_ACEFLAG_INHERIT_ACE = &H2

Set objOU = GetObject("LDAP://OU=MIS,DC=company,DC=pri")
Set objSD = objOU.Get("ntSecurityDescriptor")
Set objDACL = objSD.DiscretionaryACL
Set objAce = CreateObject("AccessControlEntry")

objAce.Trustee = "company\jhicks"
objAce.AceFlags = ADS_ACEFLAG_INHERIT_ACE
objAce.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
objAce.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT OR _
    ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT
objAce.ObjectType = "{00299570-246d-11d0-a768-00aa006e0529}"
objACE.InheritedObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}"
objAce.AccessMask = ADS_RIGHT_DS_CONTROL_ACCESS
objDACL.AddAce objAce
objSD.DiscretionaryAcl = objDACL
objOU.Put "ntSecurityDescriptor", Array(objSD)
objOU.SetInfo
```

这里只有少数几处更改。首先，我们添加了两个常量来处理继承的权限。接下来，我们将 *AceFlags* 属性设置为表明此 ACE（应用于 OU）应该被继承。*Flags* 属性仍然获得 *OBJECT_TYPE_PRESENT* 标志，表明对象位于 ACE 本身。*INHERITED_OBJECT_TYPE_PRESENT* 标志也被添加。因此，我们需要添加 *InheritedObjectType* 属性，它是用户帐户对象类的 GUID。这不是特定帐户的 GUID，而是用户帐户类本身的 GUID。这意味着权限只会由用户帐户继承，而不会由计算机或 OU 中可能存在的其他任何东西继承。我们在以下网站找到了该 GUID。（向下滚动，单击 *User*，Schema-Id-Guid 将显示在页面顶部附近。）

http://msdn.microsoft.com/library/default.asp?url=/library/en-us/adschema/adschema/classes_all.asp

> **随书附带光盘** 此链接包含在随书附带的光盘中。单击 *Schema Reference (User)*。

> **更多信息** 查看 Scripting Guys 关于使用脚本管理 Active Directory 安全性的文章，网址为 http://www.microsoft.com/technet/scriptcenter/topics/security/propset.mspx（此链接在随书附带的光盘中；单击 *Using Scripts to Manage Active Directory Security*。）

### 总结

在本章中，我们向你展示了探索 Active Directory 和 WinNT 提供程序的新方法。我们涵盖了一些高级脚本技术，包括 Active Directory 安全模型。我们还介绍了使用 WinNT ADSI 提供程序执行各种计算机管理任务的技术。希望这能为你提供一些思路，以便编写基于 ADSI 的脚本，帮助自动化组织中的 Windows 管理。



# 第9章
## ADO 与 ADSI 的结合使用

本章内容：
- 了解用于 ADO 的 ADSI 提供程序……246
- 通过 ADO 连接到 ADSI……247
- 将 Active Directory 视为数据库……248
- 编写 ADSI 查询以检索信息……251
- 编写 ADSI 查询以进行更改……254
- 实际查看 ADO 和 ADSI 的应用……256
- 总结……260

微软的数据库访问技术——ActiveX 数据对象 (ADO)，可用于高效地处理 Active Directory。我们将探讨这种数据库与目录的集成如何工作，以及它如何为你的脚本提供强大的功能。尽管使用两种完全不同的方式——ADO 和活动目录服务接口 (ADSI)——来处理 Active Directory 可能看起来有些奇怪，但你会发现 ADO 有其自身的优缺点，因此非常值得花时间学习如何使用它。

在第8章“高级 ADSI 和 LDAP 脚本”中，我们简要讨论了通过使用 ADO 连接到 ADSI，以此作为克服 ADSI 查询中 1000 条记录限制的一种方法。标准轻量级目录访问协议 (LDAP) 提供程序并非旨在返回大型查询结果集，而 ADO 的设计初衷就是处理拥有数十亿条记录的数据库。ADO 包含一种分页机制，允许以更小、更易于管理的块（称为*页*）来检索大型结果集。为了说明这一概念，我们使用了如下示例中的函数，该函数能够扫描一个非常大的结果集以定位对象的可分辨名称。

```
Function strGetDN(samAccount)
    'Given NT4 account name, find the distinguished name
    On Error Resume Next
    Dim objConn,objCmd,objRS
    Set objConn=CreateObject("ADODB.Connection")
    Set objCmd=CreateObject("ADODB.Command")
    strGetDN="NotFound"
    Set objRoot=Getobject("LDAP://RootDSE")
    Set objDomain=Getobject("LDAP:///"& objRoot.get("DefaultNamingContext"))
    strQuery="Select sAMAccountname,distinguishedname from '" & _
    objDomain.AdsPath & "' where objectCategory='person' AND " & _
    "objectclass='user'" & _
    " AND sAMAccountName='" & samAccount & "'"
    
' ...
```

```
set objCatalog=Getobject("GC:")
for each objItem In objCatalog
    Set objGC=objItem
Next
objConn.Provider="ADSDSOObject"
objConn.Open "Active Directory Provider"
objCmd.ActiveConnection=objConn
objCmd.Properties("Page Size") = 100
objCmd.Properties("asynchronous")=True
objCmd.Properties("Timeout") =30
objCmd.Properties("Cache Results") = False
objCmd.CommandText=strQuery
set objRS=objCmd.Execute
do while not objRS.EOF
    strGetDN=objRS.Fields("distinguishedname")
    objRS.movenext
Loop
objRS.Close
objConn.Close
set objConn=Nothing
set objCmd=Nothing
set objRoot=Nothing
set objCatalog=Nothing
set objRS=Nothing
End Function
```

在本章中，我们将详细研究这个示例，并向你展示 ADO 如何提供对 Active Directory 内部信息的访问。

> **更多信息** 如果你对 ADO 还不熟悉，我们建议你先阅读第7章“数据库脚本”，然后再继续本章。第7章解释了数据库脚本和 ADO 的基本概念，我们将在这些概念的基础上进行讲解。

### 了解用于 ADO 的 ADSI 提供程序

*连接字符串*是告诉 ADO 使用何种类型的数据库以及在哪里找到该数据库的一种方式。例如，以下连接字符串连接到位于 C:\MyDB.mdb 的 Microsoft Access 数据库。

```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\MyDB.mdb;
```

连接字符串的一个关键部分是*提供程序*。在此示例中，提供程序是 *Microsoft.Jet.OLEDB.4.0*，这是 Access 数据库使用的 OLE DB 提供程序。要将 Active Directory 视为数据库，我们需要使用一个允许 ADO 连接到 Active Directory 的提供程序。Microsoft OLE DB Provider for Microsoft Active Directory Service (简称 ADSI 提供程序) 内置于 Microsoft Windows 中。开始使用 ADSI 提供程序的最简单方法是创建一个新的 ADO *Connection* 对象，并在其 *ConnectionString* 属性中传递 ADSI 提供程序的名称 *ADSDSOObject*。

```
Dim objConn
Set objConn = CreateObject("ADODB.Connection")
objConn.ConnectionString = "ADSDSOObject"
objConn.Open
```

这会使用你当前的凭据打开一个到你计算机所属域的连接。注意，我们使用的是 *ConnectionString* 属性，而不是原始示例中使用的 *Provider* 属性。就 ADSI 连接而言，这两个属性在大多数情况下可以互换使用。

ADSI 提供程序——像 ADSI 的其他部分一样——可以连接的不仅仅是 Active Directory。事实上，它可以连接到 Windows NT 目录服务、非微软的 LDAP 目录以及更多其他服务，包括 Novell 目录服务 (NDS)。

### 通过 ADO 连接到 ADSI

尽管我们已经向你展示了如何通过 ADO 连接到 Active Directory，但这可能看起来有些超前，但我们其实没有。ADO 和 ADSI 不仅仅是利用你当前凭据的基本连接。例如，我们向你展示的连接字符串最常见的变体之一允许你为连接指定备用凭据。

```
Dim objConn
Set objConn = CreateObject("ADODB.Connection")
objConn.ConnectionString = "Provider=ADSDSOObject;" & _
    "User ID=MyUserID;Password=MyPassword;"
objConn.Open
```

这可以是一种非常有用的技术，因为它可用于在创建 ADO 连接到 Active Directory 时指定备用凭据。

> **重要提示** 这并不意味着你应该将凭据硬编码到脚本中。正如我们在第2章“脚本安全”中讨论的那样，没有安全的方法可以在脚本中硬编码任何凭据。相反，请使用像 *InputBox* 这样的函数来提示输入备用用户名或密码，将它们存储在变量中，然后在连接字符串中传递这些变量的内容。当然，你也可以始终使用 RunAs 命令行实用工具来运行脚本，该工具允许你输入备用凭据。

你还需要向数据库传递命令或查询，然后处理返回的结果。当数据库是 Active Directory 时，同样的道理也适用。

### 将 Active Directory 视为数据库

让我们构建一个查询发送到 Active Directory。在本章开头的示例中，我们在一个字符串变量中构建了查询。

```
strQuery="Select sAMAccountname,cn,distinguishedname from '" & _
    objDomain.AdsPath & "' where objectCategory='person' AND " & _
    "objectclass='user'" & _
    " AND sAMAccountName='" & samAccount & "'"
```

假设我们的域名为 *company.pri*，并且变量 *samAccount* 包含字符串 *DONJ*，那么这个查询将如下所示。

```
Select sAMAccountname,distinguishedname from
'dc=company,dc=pri' where objectCategory = 'person' AND
objectclass='user' AND sAMAccountName='DONJ'
```

这是一个相当直接的 SQL 查询。它做了以下事情。

- 从符合查询条件的 Active Directory 对象中查询 *sAMAccountName* 和 *distinguishedName* 属性。Active Directory 属性（更正式的叫法是*属性*）替代了你在 Access 或 Microsoft SQL Server 等传统数据库中找到的列。

> **提示** 我们经常需要将单个属性映射到 Active Directory 内的特定复选框、文本框或其他图形元素。Microsoft 在以下地址维护了 GUI 到属性映射的完整列表：
>
> http://msdn.microsoft.com/library/default.asp?url=/library/en-us/ad/ad/mappings_for_the_active_directory_users_and_computers_snap-in.asp
>
> （此链接与本书中引用的大多数链接一样，也包含在随附的 CD 中；单击 *Mappings for the Active Directory Users and Computers Snap-in*。）

- 指定我们要查询的记录来源，即 *company.pri* 域。
- 指定三个查询条件，因此只有满足所有三个条件（因为使用了 *And* 运算符）的对象才会作为查询结果返回。指定的条件如下：
  - *objectCategory* 属性必须包含 *person*。
  - *objectClass* 属性必须包含 *user*。
  - *sAMAccountName* 属性必须包含 *DONJ*。



# 第三部分：高级脚本技术、工具与技术

**提示** 在大多数 SQL 查询中，引号外的内容不区分大小写。属性名 *objectclass* 与 *objectClass* 同样有效。然而，单引号内的值（用于界定字符串字面量）*是*区分大小写的。因此，*user* 必须全部使用小写字母书写，因为这正是 Active Directory 存储该值的方式。

接下来，将查询赋值给 ADO *Command* 对象的 *CommandText* 属性。*Command* 对象还需要连接到已打开的 *Connection* 对象。

```vb
Dim objCmd
Set objCmd = CreateObject("ADODB.Command")
objCmd.ActiveConnection=objConn
objCmd.CommandText=strQuery
```

现在可以执行该命令；执行后将返回一个 ADO *Recordset* 对象。

```vb
Set objRS = objCmd.Execute
```

正如我们在第 7 章所解释的，ADO *Recordset* 对象有多种类型。*Connection* 或 *Command* 对象的 *Execute* 方法返回一个静态的、仅向前滚动的 *Recordset* 对象。在使用 ADSI 时，*Command* 对象的 *Execute* 方法将始终返回静态 *Recordset* 对象。了解静态记录集可用这一事实如何影响 *Recordset* 对象的某些属性是有用的。以下是所有 *Recordset* 对象属性的列表及其在 ADSI 连接中的使用情况。

- *AbsolutePage* 此属性为读/写。
- *AbsolutePosition* 此属性为读/写。
- *ActiveConnection* 此属性为只读。
- *BOF* 此属性为只读。
- *Bookmark* 此属性为读/写。
- *CacheSize* 此属性为读/写。
- *CursorLocation* 此属性必须始终使用 *adUseServer* 常量（这是默认值）。
- *CursorType* 此属性必须始终设置为 *adOpenStatic*（这是默认值）。
- *EditMode* 此属性将始终设置为 *adEditNone*，这意味着您无法直接编辑记录集。
- *EOF* 此属性为只读。
- *Filter* 此属性为读/写。
- *LockType* 此属性为读/写。
- *MarshalOptions* 此属性不受支持。
- *MaxRecords* 此属性为读/写。
- *PageCount* 此属性为只读。
- *PageSize* 此属性为读/写。如果您不设置此属性，如我们原始示例中那样，分页将被禁用，并且对于任何查询，您将最多获得大约 1000 条记录。要启用自动分页，必须设置此属性。
- *RecordCount* 此属性为只读。
- *Source* 此属性为读/写。
- *State* 此属性为只读。
- *Status* 此属性为只读。

可能最重要的要设置的属性是 *PageSize* 属性。我们通过在 *Command* 对象的 *Properties* 集合中指定属性名来设置它。

```vb
objCmd.Properties("Page Size") = 100
```

这将页面大小设置为 100 条记录，并强制 ADO 在导航到当前页面末尾附近时查询下 100 条记录。请记住，您使用标准 ADO 方法——主要是 *MoveNext* 方法——来在记录集中导航。以下是 ADSI 记录集中支持的方法的完整列表。

- *Clone*
- *Close*
- *GetRows*
- *Move*
- *MoveFirst*
- *MoveLast*
- *MoveNext*
- *MovePrevious*
- *NextRecordset*
- *Open*
- *Requery*
- *Resync*
- *Supports*

需要明确的是，以下方法*不可用*。

- *AddNew*
- *Cancel*
- *CancelBatch*
- *CancelUpdate*
- *Delete*
- *Update*
- *UpdateBatch*

注意，不可用的方法都与对记录集进行更改有关。因为只有静态记录集可用，所以不允许进行更改。

您可以探索 Active Directory 架构，以查看各类可用的 Active Directory 属性的完整列表。我们建议使用 Active Directory Schema 控制台来执行此操作。只需打开一个新的 Microsoft 管理控制台 (MMC) 会话并添加 Active Directory Schema 管理单元。

**提示** Active Directory Schema 管理单元默认情况下不可用，因此您需要在首次使用时注册它，以便它出现在可用管理单元列表中。要注册它，请打开命令行窗口并键入 `regsvr32 schmmgmt.dll`（您可能需要使用 System32 文件夹来正确执行此操作）。您应该会看到一个对话框指示注册成功，下次打开 MMC 时，该管理单元应该会被列出。

### 编写 ADSI 查询以检索信息

我们已经解释了如何通过 ADO 使用 SQL 查询来查询 Active Directory。然而，作为 SQL 语法的替代方案，您可以使用一种 ADSI 特有的特殊查询语法。它是一个四部分的查询规范。

```
Root; Filter; Attributes [; Scope]
```

最后一部分 *Scope* 是可选的，这就是为什么它通常用方括号表示。查询的 *Root* 部分是 LDAP 对查询起点的引用。这可能指向全局编录服务器。

```
<GC://dc=company,dc=pri>
```

它也可以是对组织单元 (OU) 的简单 LDAP 引用。

```
<LDAP://ou=Sales,dc=company,dc=pri>
```

查询的 *Filter* 部分限制查询返回的对象类型。您可以指定一个实际上没有任何限制的筛选器，允许检索所有对象。

```
(objectClass=*)
```

筛选器包含在括号中，采用 *attribute=value* 的基本格式。例如，这将仅返回用户对象。

```
(objectCategory=user)
```

这将查询将特定用户作为成员的组。

```
(&(objectCategory=Group)(member=cn=TestUser,ou=it,dc=company,dc=pri))
```

让我们详细看看这个筛选器。注意指定了两个条件：一个用于 *objectCategory*，一个用于 *member*。两者都包含在外层括号中，一个 & 符号（布尔 *And*）表示这两个条件都必须为真才能返回结果。一个竖线字符（位于大多数键盘上的反斜杠键上方）将表示布尔 *Or*，允许满足任一条件的对象包含在查询结果集中。

注意：此筛选器格式是行业标准，在 RFC 1960 中指定。

查询的 *Attributes* 部分是一个逗号分隔的列表，包含您希望查询返回的属性。

```
ADsPath, sn, givenName
```

查询的 *Scope* 部分限制在 Active Directory 树中的查询深度。您可以指定 *Base* 仅搜索指定为基础的对象，*OneLevel* 搜索基础及其下一级，或 *Subtree* 指定基础及其下的所有内容。整个查询可能看起来像这样。

```
<LDAP://dc=company,dc=pri>;(objectClass=*);distinguishedName;subtree
```

这连接到 *company.pri* 域，查询所有对象，仅返回其 *distinguishedName* 属性，并包括域根下的整个树。我们更喜欢在单独的字符串变量中指定查询的四个部分，并将它们连接起来形成整个查询——这使得脚本更易于阅读。

作为示例，我们将从 Active Directory 查询所有用户并显示其向后兼容的 NT 名称以及其 Active Directory 规范名称 (*cn*)。我们首先通过 ADO 连接到 Active Directory，并设置 ADO *Command* 对象。

```vb
Set objCmd = CreateObject("ADODB.Command")
Set objCn = CreateObject("ADODB.Connection")
objCn.Provider = "ADsDSOObject"
objCn.Open "Active Directory Provider"
objCmd.ActiveConnection = objCn
```

接下来我们指定查询的基础部分——对域根的 LDAP 引用。

**提示** 唯一区分大小写的部分是 LDAP、GC 或其他协议或提供程序名称。

```vb
strBase = "<LDAP://dc=company,dc=pri>"
```

我们将筛选器指定为任何 *objectCategory* 为 *person* 且 *objectClass* 为 *user* 的内容。注意 & 符号，它指定两个筛选条件都必须为真。

```vb
strFilter = "(&(objectCategory=person)" & _
"(objectClass=user))"
```

我们将属性指定为 NT 风格的 *sAMAccountName* 和 Active Directory 风格的 *cn*。

```vb
strAttributes = "sAMAccountName,cn"
```

现在我们构建查询并指定范围为 *Subtree*。

```vb
strQuery = strBase & ";" & strFilter & ";" & _
strAttributes & ";subtree"
```

这很容易返回超过 1000 条记录，因此我们设置 *Command* 对象以 100 条为分页块返回结果。

```vb
objCmd.CommandText = strQuery
objCmd.Properties("Page Size") = 100
objCmd.Properties("Timeout") = 30
objCmd.Properties("Cache Results") = False
```

现在我们执行命令以检索记录集。

```vb
Set objRS = objCmd.Execute
```

我们一次一条记录地遍历记录集，显示 *sAMAccountName* 和 *cn*。

```vb
Do Until objRS.EOF
   strName = objRS.Fields("sAMAccountName").Value
   strCN = objRS.Fields("cn").value
   wscript.Echo "NT Name: " & strName & _
   ", AD Name: " & strCN
   objRS.MoveNext
Loop
```

最后，我们在完成后关闭连接。

```vb
objCn.Close
```



### 编写 ADSI 查询以进行修改

你只能使用 ADO 从 Active Directory 中读取信息；不能使用 ADO 对 Active Directory 进行修改。但是，你可以使用 ADO 查询信息，然后使用常规的 ADSI 接口来修改这些信息。下面是一个操作指南。

1.  执行 ADO 查询，将一个或多个结果检索到记录集中。
2.  你可以查询的 *ADsPath* 属性包含每个你检索其信息的 Active Directory 对象的完整 LDAP 路径。
3.  将 *ADsPath* 传递给常规的 *GetObject* 函数以检索 Active Directory 对象。
4.  修改你检索到的信息。

请记住，ADO 检索的不是实际的 Active Directory 对象——它只是检索这些对象的某些属性，这就是你无法真正进行任何修改的原因。要使用 ADO 查询信息并进行修改，你必须分几个步骤来完成。首先，声明一个 ADO *Connection* 对象并打开与 Active Directory 的连接。我们已经向你展示了如何使用 *ConnectionString* 属性和 *Open* 方法来做到这一点；这是一个将连接字符串直接传递给 *Open* 方法的快捷方式。

```
Set objConnection = CreateObject("ADODB.Connection")
objConnection.Open "Provider=ADsDSDSOObject;"
```

其次，编写一个查询并将其传递给 ADO *Command* 对象。务必将 *Command* 对象的 *ActiveConnection* 属性设置为 *Connection* 对象。

```
Set objCommand = CreateObject("ADODB.Command")
objCommand.ActiveConnection = objConnection
objCommand.CommandText = _
    "<LDAP://dc=company,dc=pri>;" & _
    "(&(objectCategory=person)(objectClass=user));" & _
    "ADsPath;subtree"
```

在此示例中，我们正在从 *company.pri* 域中查询所有用户对象。接下来，我们执行 *Command* 对象以返回一个静态（即只读）记录集。

```
Set objRecordSet = objCommand.Execute
```

现在我们可以循环遍历记录集并一次处理一个用户。

```
Do Until objRecordset.EOF
```

我们现在将 *ADsPath* 属性提取到一个字符串变量中。

```
strADsPath = objRecordset.Fields("ADsPath")
```

我们使用常规的 ADSI 查询来检索用户对象。

```
Set objUser = GetObject(strADsPath)
```

我们可以使用 *Put* 方法修改一个或多个属性。我们将修改 *postalCode*。

```
objUser.Put "postalCode", "89123"
```

完成后，*SetInfo* 方法将信息保存回 Active Directory，记录集的 *MoveNext* 方法调出下一个用户帐户。

```
objUser.SetInfo
objRecordset.MoveNext
Loop
```

关闭与 Active Directory 的 ADO 连接。

```
objConnection.Close
```

#### 清单 9-1：查询所有用户

```
Dim objCmd, objCn
Dim strBase, strFilter, strAttributes
Dim strQuery, objRS, strName, strCN
Set objCmd = CreateObject("ADODB.Command")
Set objCn = CreateObject("ADODB.Connection")
objCn.Provider = "ADsDSOObject"
objCn.Open "Active Directory Provider"
objCmd.ActiveConnection = objCn
strBase = "<LDAP://dc=company,dc=pri>"
strFilter = "(&(objectCategory=person)" & _
    "(objectClass=user))"
strAttributes = "sAMAccountName,cn"
strQuery = strBase & ";" & strFilter & ";" & _
    strAttributes & ";subtree"
objCmd.CommandText = strQuery
objCmd.Properties("Page Size") = 100
objCmd.Properties("Timeout") = 30
objCmd.Properties("Cache Results") = False
Set objRS = objCmd.Execute
Do Until objRS.EOF
    strName = objRS.Fields("sAMAccountName").Value
    strCN = objRS.Fields("cn").value
    Wscript.Echo "NT Name: " & strName & _
        ", AD Name: " & strCN
    objRS.MoveNext
Loop
objCn.Close
```

> **注意** 你使用 ADO 查询的记录集是静态的。这意味着它通常不会反映记录集构建之后所做的任何更改。（这有一些例外情况，尤其是在大型结果集中，数据是分页检索的。每一页在检索并发送到你的计算机时都是最新的。）在此示例中，检查 ADO 记录集的 *postalCode* 属性将返回*旧的*属性值，而不是刚刚指定的新值。

#### 清单 9-2：查询与修改

```
Set objConnection = CreateObject("ADODB.Connection")
objConnection.Open "Provider=ADsDSOObject;"
Set objCommand = CreateObject("ADODB.Command")
objCommand.ActiveConnection = objConnection
objCommand.CommandText = _
    "<LDAP://dc=company,dc=pri>;" & _
    "(&(objectCategory=person)(objectClass=user));" & _
    "ADsPath;subtree"
Set objRecordSet = objCommand.Execute
Do Until objRecordset.EOF
    strADsPath = objRecordset.Fields("ADsPath")
    Set objUser = GetObject(strADsPath)
    objUser.Put "postalCode", "89123"
    objUser.SetInfo
    objRecordset.MoveNext
Loop
objConnection.Close
```

### 查看 ADO 和 ADSI 的实际应用

你可以使用 ADO 和 ADSI 来测试组成员身份，包括嵌套组成员身份。此功能在登录脚本中非常有用，例如，用于将驱动器和打印机映射到用户组。但是，ADSI 不包含许多内置方式来检查嵌套组成员身份，因此你必须构建自己的函数。我们构建了一个名为 *IsMember* 的函数。该函数首先检查是否存在名为 *objGroupList* 的 VBScript *Dictionary* 对象，如果不存在，则创建它。请注意，我们跨函数使用 *objGroupList* 变量，因此它必须在函数本身之外进行全局声明，以便在全局范围内可用。

```
Dim strUser, objGroupList, strGroup
Dim objRootDSE, strDNSDomain, objCmd, objCn
Dim strBase, strAttributes
Function IsMember(strGroup)
    If IsEmpty(objGroupList) Then
        Set objGroupList = CreateObject("Scripting.Dictionary")
    End If
```

我们为 Dictionary 对象设置一个比较选项，以帮助确保比较细节（例如大小写差异）无关紧要。例如，我们指定的选项确保字符串 Sample 与字符串 sample 的处理方式相同。

```
objGroupList.CompareMode = vbTextCompare
```

现在我们检索域的 DNS 名称。

```
Set objRootDSE = GetObject("LDAP://RootDSE")
strDNSDomain = objRootDSE.Get("DefaultNamingContext")
```

要搜索 Active Directory，我们创建并打开一个 ADO Connection 对象，并创建一个 ADO Command 对象。我们将 Command 对象连接到 Connection 对象，并指定一个从全局编录服务器查询基础域的基础查询。

```
Set objCmd = CreateObject("ADODB.Command")
Set objCn = CreateObject("ADODB.Connection")
objCn.Provider = "ADsDSOObject"
objCn.Open "Active Directory Provider"
objCmd.ActiveConnection = objCn
strBase = "<GC://" & strDNSDomain & ">"
```

我们想要查询 distinguishedName 属性，因此我们将该属性名放入一个字符串变量中。

```
strAttributes = "distinguishedName"
```

为帮助避免产生巨大的结果集，我们指定设置分页的属性。

```
objCmd.Properties("Page Size") = 100
objCmd.Properties("Timeout") = 30
objCmd.Properties("Cache Results") = False
```

最后，我们调用一个 LoadGroups 函数，将用户所属的所有组加载到我们的 Dictionary 对象中。请注意，我们传递的是用户帐户的可分辨名称。完成后，我们关闭 ADO 连接。请注意，我们对 LoadGroups 的调用传递了筛选条件，因此只返回包含我们用户可分辨名称的组。

```
Call LoadGroups("(member=" & strUser & ")")
objCn.close
End If
```

此时，用户所属的每个组都在 objGroupList Dictionary 对象中。我们使用 Dictionary 对象的 Exists 方法查询我们正在寻找的组是否在列表中。Exists 方法返回 TRUE 或 FALSE 值作为 IsMember 函数的结果。

```
IsMember = objGroupList.Exists(strGroup)
End Function
```

然后我们创建了一个名为 *LoadGroups* 的函数，它首先声明几个变量。

```
Sub LoadGroups(strUserFilter)
    Dim strFilter, strQuery, strDN, objRecordSet
    Dim strNextFilter, blnRecurse
```

构建一个字符串变量来筛选 ADO 查询结果。此筛选器将仅查询具有 *Group* 类别的对象，并且仅查询具有 *member* 属性等于我们用户可分辨名称的组。

```
strFilter = "(&(objectCategory=Group)" & strUserFilter & ")"
```

这是由基础查询、筛选器和属性列表组装成的完整查询。

```
strQuery = strBase & ";" & strFilter & ";" & strAttributes & ";subtree"
```

现在我们将查询文本分配给 *Command* 对象并执行它。结果在 *Recordset* 对象中返回。

```
objCmd.CommandText = strQuery
Set objRecordSet = objCmd.Execute
strNextFilter = "(|"
blnRecurse = False
```

我们遍历记录集中的每个结果，并将组的可分辨名称提取到一个字符串变量中。

```
Do Until objRecordSet.EOF
    strDN = objRecordSet.Fields("DistinguishedName")
```

如果组不在我们的字典中，我们就添加它。因为我们还想包含嵌套组，所以我们将组添加到我们的筛选条件中，并将一个变量设置为 TRUE，表示我们需要递归查询该组的成员身份。

```
If Not objGroupList.Exists(strDN) Then
    objGroupList(strDN) = True
    strNextFilter = strNextFilter & "(member=" & strDN & ")"
    blnRecurse = True
End If
objRecordSet.MoveNext
Loop
```

当我们递归处理嵌套组时，*LoadGroups* 函数会调用自身，因此嵌套组成员身份也会被处理。

```
If blnRecurse = True Then
    strNextFilter = strNextFilter & ")"
    Call LoadGroups(strNextFilter)
End If
End Sub
```



使用此函数时，只需指定用户账户的可分辨名称（DN）和要检查的组。

```vb
' 获取用户对象。
strUser = "cn=TestUser,ou=it,dc=company,dc=pri"

' 指定组 DN 并检查成员资格。
strGroup = "cn=Admins,ou=it,dc=company,dc=pri"
If IsMember(strGroup) Then
  '是成员
Else
  '不是成员
End If
```

清单 9-3 包含完整的脚本，其中包括演示 IsMember 函数用法的代码。

```vb
清单 9-3 测试组成员资格
Dim strUser, objGroupList, strGroup
Dim objRootDSE, strDNSDomain, objCmd, objCn
Dim strBase, strAttributes

' 获取用户对象。
strUser = "cn=TestUser,ou=it,dc=company,dc=pri"

' 指定组 DN 并检查成员资格。
strGroup = "cn=Admins,ou=it,dc=company,dc=pri"
If IsMember(strGroup) Then
  '是成员
Else
  '不是成员
End If

Function IsMember(strGroup)
' 用于测试组成员资格的函数。
' strGroup 是组的可分辨名称。
  If IsEmpty(objGroupList) Then
    Set objGroupList = CreateObject("Scripting.Dictionary")
    objGroupList.CompareMode = vbTextCompare

    ' 获取 DNS 域名。
    Set objRootDSE = GetObject("LDAP://RootDSE")
    strDNSDomain = objRootDSE.Get("DefaultNamingContext")

    ' 搜索 Active Directory。
    Set objCmd = CreateObject("ADODB.Command")
    Set objCn = CreateObject("ADODB.Connection")
    objCn.Provider = "ADSDSOObject"
    objCn.Open "Active Directory Provider"
    objCmd.ActiveConnection = objCn
    strBase = "<GC://" & strDNSDomain & ">"
    strAttributes = "distinguishedName"
    objCmd.Properties("Page Size") = 100
    objCmd.Properties("Timeout") = 30
    objCmd.Properties("Cache Results") = False

    Call LoadGroups("(member=" & strUser & ")")
    objCn.Close
  End If
  IsMember = objGroupList.Exists(strGroup)
End Function

Sub LoadGroups(strMemberFilter)
    Dim strFilter, strQuery, strDN, objRecordSet
    Dim strNextFilter, blnRecurse

    strFilter = "(&(objectCategory=Group)" & strMemberFilter & ")"
    strQuery = strBase & ";" & strFilter & ";" & strAttributes & ";subtree"
    objCmd.CommandText = strQuery
    Set objRecordSet = objCmd.Execute
    strNextFilter = "(|"
    blnRecurse = False

    Do Until objRecordSet.EOF
        strDN = objRecordSet.Fields("DistinguishedName")
        If Not objGroupList.Exists(strDN) Then
            objGroupList(strDN) = True
            strNextFilter = strNextFilter & "(member=" & strDN & ")"
            blnRecurse = True
        End If
        objRecordSet.MoveNext
    Loop
    If blnRecurse = True Then
        strNextFilter = strNextFilter & ")"
        Call LoadGroups(strNextFilter)
    End If
End Sub
```

### 总结

虽然可以直接使用 ADSI 访问 Active Directory，但使用 ADO 具有几个优势。ADO 可以查询更大的结果集，并且它使用的语法一些管理员觉得更容易记住。ADO 用于访问 Active Directory 的语法也很容易适配其他类型的数据库，这使得学习 ADO 的时间非常值得。

# 第 10 章
## 高级 WMI 脚本编写

**本章内容：**

- 理解高级 WQL ………… 262
- 使用查询和*关联*类 ………… 267
- 使用高级 WMI 安全技术 ………… 273
- 查看高级 WMI 脚本实战 ………… 276
- 总结 ………… 283

Windows 管理规范（WMI）是管理脚本的基石；它提供了对配置参数、Windows 功能以及更多内容的惊人访问能力。事实上，过去几年人们对管理脚本兴趣的激增在很大程度上归功于 WMI。然而，大多数管理员只了解 WMI 能做的一小部分。在本章中，我们将探讨 WMI 经常被忽视的高级功能。

WMI 是一项用于 Microsoft Windows 管理的强大技术。像 Scriptomatic 这样的工具以及一些商业脚本编辑器内置的 WMI 向导使得 WMI 更易于使用，并帮助管理员利用该技术的功能。即使是像这个列出本地计算机上所有本地用户账户的简单脚本，也可以成为有价值的管理工具。

```vb
Dim strComputer
Dim objWMIService
Dim propValue
Dim objItem
Dim SWbemLocator
Dim UserName
Dim Password
Dim colItems

strComputer = "."
UserName = ""
Password = ""
Set SWbemLocator = CreateObject("wbemScripting.SWbemLocator")
Set objWMIService = SWbemLocator.ConnectServer(strComputer, "\\root\\CIMV2", UserName, Password)
Set colItems = objWMIService.ExecQuery("Select * from Win32_Account")
For Each objItem in colItems
    wScript.Echo "Caption: " & objItem.Caption
    wScript.Echo "Description: " & objItem.Description
    wScript.Echo "Domain: " & objItem.Domain
    wScript.Echo "InstallDate: " & objItem.InstallDate
    wScript.Echo "LocalAccount: " & objItem.LocalAccount
    WScript.Echo "Name: " & objItem.Name
    WScript.Echo "SID: " & objItem.SID
    WScript.Echo "SIDType: " & objItem.SIDType
    WScript.Echo "Status: " & objItem.Status
Next
```

然而，WMI 的功能远不止基本的配置清点。它可以用于更改配置设置、使远程计算机执行特定操作，甚至响应 Windows 中发生的事件。

### 理解高级 WQL

WMI 使用一种相当复杂的查询语言，其模型基于关系数据库管理系统（如 SQL Server）使用的结构化查询语言（SQL）。这种查询语言称为 WMI 查询语言（WQL），你无疑已经遇到过它。本章开头显示的示例就包含一个简短的 WQL 查询。

```sql
select * from win32_Account
```

大多数 WQL 查询仅由 *Select* 关键字、星号、*From* 关键字和 WMI 类名组成。刚才显示的查询将从指定的类中选择所有可用属性。

#### 选择特定属性

如果你曾经编写过查询一组计算机上整个 WMI 类的脚本，你可能想知道是否有办法加快这个过程。清单 10-1 打开一个名为 C:\Computers.txt 的文本文件，该文件预期包含每行一个计算机名。然后脚本连接到每台计算机，查询 *Win32_OperatingSystem* 类的所有属性，并显示每台计算机的名称和当前服务包版本号。

```vb
清单 10-1 服务包清点
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\computers.txt")
Do Until objTS.AtEndOfStream
    strComputer = objTS.ReadLine
    Set SWBemlocator = CreateObject("WbemScripting.SWbemLocator")
    Set objWMIService = SWBemlocator.ConnectServer(strComputer,"\root\CIMV2")
    Set colItems = _
        objWMIService.ExecQuery("Select ServicePackMajorVersion " & _
        " from win32_OperatingSystem Where Primary = True")
    For Each objItem in colItems
        WScript.Echo strComputer & "="
        WScript.Echo objItem.ServicePackMajorVersion
    Next
Loop
objTS.Close
```

> **在 CD 上** 你可以在本书附带的 CD 上找到此脚本以及本章列出的其他脚本。

> **注意** 清单 10-1 假设每台计算机都可用且 WMI 可以联系到它；它不包含任何如果计算机无法到达时的错误处理。

此脚本查询 Win32_OperatingSystem 类的所有属性，但它只使用其中一个属性 ServicePackMajorVersion。其他大约二十多个属性通过网络传输但未被使用，在运行脚本的计算机和被查询的计算机上都造成了浪费。由于脚本可能连接到数百台计算机，这种轻微的低效可能会累积成严重的减速。一种加速方法是只查询你需要的内容。

```sql
Select ServicePackMajorVersion from win32_OperatingSystem
```

就这么简单。只需指定一个以逗号分隔的要查询的属性列表，你将使你的脚本更高效，因为只有查询的属性需要被组装并通过网络传输。

#### 包含 WHERE 子句

正如查询过多属性会导致你的脚本效率低下一样，查询过多实例也会产生相同的效果。例如，在清单 10-1 中，我们查询 *Win32_OperatingSystem* 类的 *所有* 实例。通常一台计算机只有一个操作系统，因此只会返回该类的一个实例。然而，计算机可能包含多个操作系统（随着虚拟计算变得更加普遍，这种情况更有可能发生），因此该查询理论上可能返回多个实例。如果我们只需要主操作系统的服务包信息，那么我们查询和显示的信息就太多了。在你的 WQL 查询中包含一个 *WHERE* 子句可以纠正这一点。下一页上的清单 10-2 是清单 10-1 的更新版本。

在下一页的清单 10-2 中，*WHERE* 子句将查询限制为 *Primary* 属性值为 TRUE 的那些实例。这个子句——其形式始终为 属性 比较 值，如 *Primary = True*——由远程计算机评估，然后它只返回满足 *WHERE* 子句条件的类实例。



##### 清单 10-2 修订后的服务包清单

```vbscript
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\computers.txt")
Do Until objTS.AtEndOfStream
    strComputer = objTS.ReadLine
    Set SWBemlocator = CreateObject("wbemScripting.SWbemLocator")
    Set objWMIService = SWBemlocator.ConnectServer(strComputer, "\\root\\CIMV2")
    Set colItems = _
        objWMIService.ExecQuery("Select ServicePackMajorVersion " & _
        " from Win32_OperatingSystem WHERE Primary = True")
    For Each objItem in colItems
        WScript.Echo strComputer & "="
        WScript.Echo objItem.ServicePackMajorVersion
    Next
Loop
objTS.Close
```

> **注意** 在比较字符串值时，请务必将比较值用单引号括起来。例如，*WHERE 属性* = '*值*'。数值以及布尔值 TRUE 和 FALSE 则不需要用引号括起来。如果需要包含反斜杠字符（例如在文件路径中），则必须输入双反斜杠。例如，路径 \\Server\\Share 对应的语句是 *WHERE 属性* = '\\\\Server\\Share'。如果不使用双反斜杠，WQL 会将其解释为一种数据分隔符。

假设你想检索所有事件 ID 为 1073741925 的事件日志条目（在我们的系统上，这表示 SQL Server 代理服务已启动）。然后你想列出事件生成的时间。清单 10-3 展示了一种完成此任务的方法。

##### 清单 10-3 事件日志扫描器

```vbscript
strComputer = "."
Set SWBemlocator = CreateObject("wbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer, _
    "\\root\\CIMV2", UserName, Password)
Set colItems = _
    objWMIService.ExecQuery("Select * from Win32_NTLogEvent")
For Each objItem in colItems
    If objItem.EventIdentifier = 1073741925 Then
        WScript.Echo "TimeGenerated: " & objItem.TimeGenerated
        WScript.Echo "TimeWritten: " & objItem.TimeWritten
        WScript.Echo "User: " & objItem.User
    End If
Next
```

在我们包含三个相当满的事件日志的测试系统上，此脚本大约需要三分钟完成。想象一下在十几台服务器上运行它——这将耗费相当长的时间。包含一个 *WHERE* 子句可以限制查询，使其仅返回符合我们需求的事件。这是一个简单的改动，如清单 10-4 所示。这个替代版本的脚本只需几秒钟就能完成——改进效果显著。

##### 清单 10-4 修订后的事件日志扫描器

```vbscript
strComputer = "."
Set SWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWbemLocator.ConnectServer(strComputer, _
    "\\root\\CIMV2", UserName, Password)
Set colItems = _
    objWMIService.ExecQuery("Select * from Win32_NTLogEvent " & _
    "WHERE LogFile = 'Application' AND " & _
    "EventIdentifier = 1073741925", , 48)
For Each objItem in colItems
    WScript.Echo "TimeGenerated: " & objItem.TimeGenerated
    WScript.Echo "TimeWritten: " & objItem.TimeWritten
    WScript.Echo "User: " & objItem.User
Next
```

在这个修改后的版本中，只查询 *EventIdentifier* 值匹配的事件，因此我们的脚本不必遍历所有事件来寻找合适的事件。如果此脚本针对远程计算机运行，它将节省更多时间，因为所有无关事件都不会通过网络传输，然后由我们的脚本处理。

*WHERE* 子句可以包含多个条件。只需使用布尔运算符将条件连接起来。你可以使用括号来指定条件的求值顺序（嵌套最深的条件最先求值）。例如，这里还有另一个修订版本，它将使我们的事件日志扫描器运行得更快一些。

```vbscript
objWMIService.ExecQuery("Select * from Win32_NTLogEvent " & _
    "WHERE LogFile = 'Application' AND " & _
    "EventIdentifier = 1073741925", , 48)
```

我们指定只返回列在 Application 事件日志中且 *EventIdentifier* 值匹配的事件。这允许处理查询的计算机排除除指定日志以外的所有事件日志，因为没有其他事件日志的条目能匹配 *LogFile = 'Application'* 条件。你的 WQL 查询越具体，查询执行得就越快，你的脚本运行得就越高效。

#### 使用 *LIKE* 运算符

如果你不知道在 *WHERE* 子句中包含哪个值，Microsoft Windows XP 和更高版本的 Windows（包括 Microsoft Windows Server 2003）支持一个名为 *LIKE* 的特殊运算符。它可以代替 *WHERE* 子句中的等号（=）或其他比较运算符，并允许你在条件中使用通配符。*LIKE* 运算符执行速度非常快，即使没有特定标准，它也是缩小查询结果集规模的绝佳选择。

例如，假设你想返回已安装软件（即产品）中名称包含 *Microsoft* 单词的列表。使用等号运算符很难做到这一点，因为它需要精确匹配。然而，*LIKE* 运算符可以与通配符字符（%）一起使用。清单 10-5 是一个展示 *LIKE* 运算符实际应用的示例。请注意，通配符字符在搜索词 *Microsoft* 之前和之后都包含，允许检索名称中任何位置包含 *Microsoft* 的产品。也就是说，第一个通配符字符将匹配 *Microsoft* 之前的任意数量字符，第二个通配符字符将匹配 *Microsoft* 之后的任意数量字符。

##### 清单 10-5 通配符查询

```vbscript
strComputer = "."
Set SWBemlocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer, "\\root\\CIMV2")
Set colItems = _
    objWMIService.ExecQuery("select * from win32_Product " & _
    "WHERE Caption LIKE '%Microsoft%'")
For Each objItem in colItems
    WScript.Echo "Caption: " & objItem.Caption
    WScript.Echo "Description: " & objItem.Description
    WScript.Echo "Name: " & objItem.Name
    WScript.Echo
Next
```

> **注意** 此脚本仅适用于已安装可选“已安装应用程序 WMI 提供程序”（包含在 Windows Server 2003 产品 CD 中）的 Windows XP 计算机和 Windows Server 2003 计算机。

我们从这个脚本得到的部分结果如下所示。

Caption: Microsoft IntelliType Pro 5.2
Description: Microsoft IntelliType Pro 5.2
Name: Microsoft IntelliType Pro 5.2

Caption: Microsoft .NET Framework 1.1
Description: Microsoft .NET Framework 1.1
Name: Microsoft .NET Framework 1.1

Caption: Microsoft Visio Viewer 2002
Description: Microsoft Visio Viewer 2002
Name: Microsoft Visio Viewer 2002

Caption: HighMAT Extension to Microsoft Windows XP CD Writing Wizard
Description: HighMAT Extension to Microsoft Windows XP CD Writing Wizard
Name: HighMAT Extension to Microsoft Windows XP CD Writing Wizard

请注意，名称以 *Microsoft* 开头的产品以及名称中间包含 *Microsoft* 单词的产品都被检索到了。

> **注意** 请记住，只有 Windows XP 和更高版本的 Windows 支持 LIKE 运算符。如果在不支持的操作系统上尝试使用它，你会收到错误。还要记住，执行查询的计算机也必须支持 LIKE 运算符。因此，如果你在 Windows XP 计算机上运行脚本，并连接到 Microsoft Windows NT 计算机，则不支持 LIKE 运算符。

LIKE 运算符还使用下划线字符（_）作为通配符。与匹配任意数量字符的 % 通配符不同，下划线仅匹配一个字符。例如，表达式 LIKE '_icrosoft' 将匹配 Microsoft 以及 microsoft 和 dicrosoft，但不会匹配 Microsoft Office 或 Update for Microsoft Office。

理解 LIKE 运算符和 WHERE 子句将帮助你编写更高效、更灵活的 WMI 脚本。

### 使用查询和关联类

WMI 有许多关联类。这些类本身通常不提供信息；相反，它们与两个或更多其他类结合使用。在接下来的两节中，我们将向你展示关联类的工作原理以及如何使用它们。

#### 理解关联

*Win32_DependentService* 类表示各种 Windows 系统服务之间的依赖关系。该类本身有三个属性：

- 前置类，即所依赖的服务。
- 依赖类，即依赖于前置类的服务。
- 依赖类型，其值可以表示未知依赖、其他依赖，或者表示前置服务必须已完成、已启动或已停止。

系统中的每个服务依赖关系都存在一个 *Win32_DependentService* 类的实例。下一页的图 10-1 展示了它与 *Win32_Service* 类之间的这种关系。在图 10-1 中，ServiceB 依赖于 ServiceA。*Win32_DependentService* 类的实例通过将 ServiceB 的 *Win32_Service* 类实例列为依赖项，并将 ServiceA 的 *Win32_Service* 类实例列为前置项来体现这种关系。其他 *Win32_Service* 类的实例——例如 ServiceC——可能存在，并且与 ServiceA 或 ServiceB 没有任何关系。



#### 编写关联查询

*ASSOCIATORS OF* 查询替代了标准的 *SELECT* 查询。这个特殊查询旨在查找给定类的所有*关联*类。继续以 *Win32_DependentService* 类为例，你可能会编写如下查询：

```sql
ASSOCIATORS OF {win32_Service.Name='MSSQLSERVER'}
WHERE AssocClass = win32_DependentService
```

此查询要求返回所有与 *Win32_Service* 实例（其中 *Name* 属性为 *MSSQLSERVER*）相关联的类，特别是那些属于 *Win32_DependentService* 类的关联类。这是一个适合在 Wbemtest 中测试的好查询。

1.  在“开始”菜单的“运行”提示符或命令行提示符中输入 **wbemtest** 来运行 Wbemtest.exe。
2.  单击“连接”，然后在出现的对话框中的“命名空间”文本框中输入 **root\cimv2**。
3.  再次单击“连接”以关闭对话框。
4.  单击“查询”并输入 ASSOCIATORS OF 查询。
5.  单击“应用”以查看结果，如图 10-2 所示。

> 注意：上一个示例中的 ASSOCIATORS OF 查询当然假设你正在运行 Microsoft SQL Server 或 Microsoft SQL Server 桌面引擎（MSDE）的实例。但是，为了进一步探索这个概念，你应该尝试替换其他服务名称，看看查询会返回什么结果。

查询的结果是所有通过 *Win32_DependentService* 与指定的 *Win32_Service* 类（即名称为 MSSQLSERVER 的那个）相关联的 *Win32_Service* 类。当然，此查询仅适用于已安装 Microsoft SQL Server 的系统。查询要求返回所有与特定 *Win32_Service* 实例相关联的类，其中关联由 *Win32_DependentService* 类完成。这个特定查询返回指定的 *Win32_Service* 实例的所有依赖和先决服务。

*Win32_DiskDriveToDiskPartition* 类将 *Win32_DiskDrive* 实例与 *Win32_DiskPartition* 实例相关联。例如，假设你要执行一个简单的 WMI 查询，返回系统上连接的所有磁盘驱动器的标题和设备 ID。你可以从类似以下代码开始：

```vb
ComputerName = "."
Set wmiServices = GetObject ( _
    "winmgmts:{impersonationLevel=Impersonate}!//" _
    & ComputerName)

' Get physical disk drive
Set wmiDiskDrives = wmiServices.ExecQuery ( _
    "SELECT Caption, DeviceID FROM Win32_DiskDrive")
```

*wmiDiskDrives* 变量是一个 *Win32_DiskDrive* 实例的集合，因此你可以使用 *For...Each* 循环来枚举该集合。对于每个 *Win32_DiskDrive* 实例，你可以通过使用 ASSOCIATORS OF 查询来检索与驱动器关联的分区。

```vb
Set wmiDiskPartitions = wmiServices.ExecQuery _
    ("ASSOCIATORS OF {win32_DiskDrive.DeviceID='" _
     & strEscapedDeviceID & "'} WHERE " & _
     "AssocClass = win32_DiskDriveToDiskPartition")
```

这将返回匹配的 *Win32_Partition* 实例的集合，因为 *Win32_DiskDriveToDiskPartition* 将 *Win32_DiskDrive* 与 *Win32_Partition* 关联起来。还有一个 *associator* 类将 *Win32_Partition* 与 *Win32_LogicalDisk* 关联，你可以使用以下查询来检索这些关联的实例。

```vb
Set wmiLogicalDisks = wmiServices.ExecQuery _
    ("ASSOCIATORS OF " _
     & "{win32_DiskPartition.DeviceID='" & _
     wmiDiskPartition.DeviceID & "'} WHERE " & _
     "AssocClass = win32_LogicalDiskToPartition")
```

清单 10-6 使用了这三个查询。它首先列出系统中的每个驱动器盘符，然后列出每个驱动器关联的分区，最后列出每个分区关联的逻辑磁盘。

```vb
清单 10-6 关联查询
ComputerName = "."
Set wmiServices = GetObject ( _
    "winmgmts:{impersonationLevel=Impersonate}//" _
     & ComputerName)

' Get physical disk drive
Set wmiDiskDrives = wmiServices.ExecQuery ( _
    "SELECT Caption, DeviceID FROM win32_DiskDrive")

For Each wmiDiskDrive In wmiDiskDrives
    WScript.Echo "Disk drive Caption: " _
        & wmiDiskDrive.Caption _
        & VbCrLf & "DeviceID: " _
        & " (" & wmiDiskDrive.DeviceID & ")"

    'Backslash in disk drive deviceid
    ' must be escaped by "\\"
    strEscapedDeviceID = Replace( _
        wmiDiskDrive.DeviceID, "\\", "\\\\")

    'Use the disk drive device id to
    ' find associated partition
    Set wmiDiskPartitions = wmiServices.ExecQuery _
        ("ASSOCIATORS OF {Win32_DiskDrive.DeviceID='" _
         & strEscapedDeviceID & "'} WHERE " & _
         "AssocClass = Win32_DiskDriveToDiskPartition")

    For Each wmiDiskPartition In wmiDiskPartitions
        'Use partition device id to find logical disk
        Set wmiLogicalDisks = wmiServices.ExecQuery _
            ("ASSOCIATORS OF " _
            & "{Win32_DiskPartition.DeviceID=''" & _
            wmiDiskPartition.DeviceID & "'} WHERE " & _
            "AssocClass = Win32_LogicalDiskToPartition")

        For Each wmiLogicalDisk In wmiLogicalDisks
            WScript.Echo "Drive letter associated" _
                & " with disk drive = " _
                & wmiDiskDrive.Caption _
                & wmiDiskDrive.DeviceID _
                & vbCrLf & " Partition = " _
                & wmiDiskPartition.DeviceID _
                & vbCrLf & " is " _
                & wmiLogicalDisk.DeviceID
        Next
    Next
Next
```

> **注意** 清单 10-6 改编自 Microsoft MSDN Library Platform SDK 中的一个示例，该库包含 WMI 的开发人员文档。请注意，该脚本可能无法在所有系统上一致工作，因为驱动器到分区的映射并非总是一致。

清单 10-7 是清单 10-6 的一个版本，它不包含 *Win32_LogicalDisk* 关联查询。这更清楚地说明了 *Win32_DiskDrive* 和 *Win32_Partition* 之间的原始关联。

```vb
清单 10-7 修订后的关联查询
ComputerName = "."
Set wmiServices = GetObject ( _
    "winmgmts:{impersonationLevel=Impersonate}!//" _
    & ComputerName)

' Get physical disk drive
Set wmiDiskDrives = wmiServices.ExecQuery ( _
    "SELECT Caption, DeviceID FROM Win32_DiskDrive")

For Each wmiDiskDrive In wmiDiskDrives
    WScript.Echo "Disk drive Caption: " _
        & wmiDiskDrive.Caption _
        & vbCrLf & "DeviceID: " _
        & " (" & wmiDiskDrive.DeviceID & ")"
Next
```

# 第三部分：高级脚本技术、工具和技术

请注意，*ASSOCIATORS OF* 查询的 *WHERE* 子句与 *SELECT* 查询中的 *WHERE* 子句有些不同。在清单 10-7 中，*WHERE* 子句被限制为一些非常具体的值。我们使用了 *AssocClass* 属性，它指示我们希望查询使用的关联类的名称；你几乎总会在 *ASSOCIATORS OF* 查询中使用它。你可以指定的其他一些关键字包括：

-   **ClassDefsOnly** - 此关键字指定查询只返回类定义，而不是实例。请注意，此关键字是单独指定的，而不是作为使用等号或其他比较运算符的比较的一部分。
-   **RequiredAssocQualifier=qualifier** - 此关键字表示返回的实例必须通过包含指定限定符的关联类与源对象关联。例如，以下代码将要求关联类包含名为 *Association* 的限定符。

```sql
ASSOCIATORS OF {win32_LogicalDisk.DeviceID='C:'}
WHERE RequiredAssocQualifier = Association
```

-   **RequiredQualifier=qualifier** - 此关键字指定返回的实例必须包含指定的限定符。例如，以下代码将仅返回包含名为 *Locale* 属性的类。

```sql
ASSOCIATORS OF {win32_LogicalDisk.DeviceID='C:'}
WHERE RequiredQualifier = Locale
```

-   **ResultClass=classname** - 此关键字（不能与 *ClassDefsOnly* 一起使用）允许你指定要检索的类。例如，以下查询将返回 *Win32_Directory*、*Win32_ComputerSystem* 和 *Win32_DiskPartition* 类中的实例。

```sql
ASSOCIATORS OF {win32_LogicalDisk.DeviceID='C:'}
```

但是，以下修订版将仅返回源自通用 *CIM_Directory* 类的 *Win32_Directory* 中的实例。

```sql
ASSOCIATORS OF {win32_LogicalDisk.DeviceID='C:'}
WHERE ResultClass = CIM_Directory
```

这些关键字在查询中使用时，如果使用多个，它们之间不使用逗号分隔。

```sql
ASSOCIATORS OF {win32_LogicalDisk.DeviceID='C:'}
WHERE ClassDefsOnly AssocClass=win32_LogicalDiskToPartition
```

> **注意** 你可以查阅 WMI 文档，查看任何 *Win32_* 类所派生的通用计算机信息模型（CIM）类。



#### 使用引用查询

*REFERENCES OF* 语句也可以用来替代标准的 *SELECT* 查询。使用 *REFERENCES OF* 语句的方式与使用 *ASSOCIATORS OF* 语句类似，但方向相反。*REFERENCES OF* 语句检索所有引用特定源实例的关联实例。与 *ASSOCIATORS OF* 查询一样，它可以在 *WHERE* 子句中使用关键字，尽管可用的关键字更有限：*ClassFedsOnly*、*RequiredQualifier* 和 *ResultClass*。

```
REFERENCES OF {Adapter="AHA-294X"} WHERE Resultclass = AdapterDriver
```

此查询返回与适配器为 AHA-294X 的类关联的所有 *Win32_AdapterDriver* 实例（具有指定的 *ResultClass*）。这是另一个例子。

```
REFERENCES OF {win32_NetworkAdapter.DeviceID="0"}
WHERE resultclass = win32_NetworkAdapterSetting
requiredQualifier = Dynamic
```

此查询返回所有设置为 *Dynamic* 的 *Win32_NetworkAdapterSetting* 类实例，并且这些实例引用设备 ID 为 0 的 *Win32_NetworkAdapter* 实例。

### 使用高级 WMI 安全技术

WMI 对身份验证、身份验证服务（NTLM 或 Kerberos）和模拟（允许远程计算机上的 WMI 服务模拟您的凭据执行查询）具有默认设置。在第 2 章中，我们解释了如何为 WMI 连接提供备用凭据。然而，WMI 为特定类型的 WMI 活动提供了额外的安全选项。要使用这些安全和模拟选项，使用 *SWBemLocator* 对象通常比通过 *winmgmts://* 标识符连接到 WMI 更容易。这是因为 *SWBemLocator* 对象语法通常更易于阅读，尤其是在同时使用多个选项时。一个简单的连接和查询如下所示。

```
strComputer = "."
Set SWBemlocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer,"\\root\\CIMV2")
Set colItems = objWMIService.ExecQuery( _
 "select * from win32_OperatingSystem")
```

然而，在调用 *ExecQuery* 方法之前，您可以修改 *SWBemLocator* 对象的 *Security_* 属性。该属性是一个 *SWbemSecurity* 对象，它有三个属性：*AuthenticationLevel*、*ImpersonationLevel* 和 *Privileges*。

#### 使用 *AuthenticationLevel* 属性

*AuthenticationLevel* 属性确定 WMI 执行的身份验证级别。可用的身份验证级别有：

- **0：默认** 身份验证设置为 Windows 用作其默认值的任何值。
- **1：无** 不使用身份验证。
- **2：连接** 身份验证仅在初始连接期间发生。
- **3：调用** 对每次调用远程计算机都进行身份验证。
- **4：数据包** 对每个发送或接收的数据包进行身份验证。
- **5：数据包完整性** 对每个数据包执行身份验证，并验证数据包的完整性以确保它们未被更改。
- **6：数据包隐私** 对每个数据包执行身份验证；它们经过身份验证、完整性检查和加密，以帮助确保隐私。

请注意，当使用标识符连接到 WMI 时，您也可以指定 *AuthenticationLevel* 属性。

```
Set objInst = GetObject("winMgmts:{ " & _
    "authenticationLevel=pktPrivacy}" & _
    "!root/cimv2:win32_LogicalDisk='c:'")
```

#### 使用 *ImpersonationLevel* 属性

指定模拟级别允许远程 WMI 服务使用您的凭据执行查询。可用的模拟级别有：

- **1：匿名** 不允许模拟您的凭据。WMI 通常无法在此级别下工作。
- **2：标识** 标识您但不允许模拟您的凭据。WMI 通常在此级别下会失败。
- **3：模拟** 允许远程 WMI 服务模拟您的凭据。这是 Windows 2000 及更高版本上的默认设置。
- **4：委托** 允许远程计算机模拟您，并将您的凭据提供给其他服务，这些服务也可以模拟您。这通常是不必要的，并且可能存在安全风险。

请注意，当使用标识符连接到 WMI 时，您也可以指定 *ImpersonationLevel* 属性。

```
Set objInst = GetObject("winMgmts:{ " & _
    "impersonationLevel=Impersonate}" & _
    "!root/cimv2:win32_LogicalDisk='c:'")
```

#### 使用 Privileges 属性

有时，仅拥有使用 WMI 执行任何操作的权限是不够的。出于安全原因，某些安全敏感的特权受到限制，即使您的当前用户账户具有权限。必须专门启用这些特权。

*Privileges* 属性是一个 *SWbemPrivilegeSet* 对象。要添加特权，请使用对象的 *AddAsString* 方法添加特定的特权名称。

```
wmiService.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```

以下是可用的安全特权。其中许多特权在管理脚本中不经常使用，但我们为了完整性列出了所有特权。粗体显示的特权是最常用的。

- SeCreateTokenPrivilege
- SeAssignPrimaryTokenPrivilege
- SeLockMemoryPrivilege
- SeIncreaseQuotaPrivilege
- **SeMachineAccountPrivilege**——创建计算机账户所需
- SeTcbPrivilege
- **SeSecurityPrivilege**——执行诸如清除安全事件日志和其他安全敏感任务等任务所需
- **SeTakeOwnershipPrivilege**——在没有对象特定权限的情况下获取对象所有权所需
- SeLoadDriverPrivilege
- **SeSystemProfilePrivilege**——收集系统配置文件和性能信息所需
- **SeSystemtimePrivilege**——设置系统时间所需
- SeProfileSingleProcessPrivilege
- SeIncreaseBasePriorityPrivilege
- SeCreatePageFilePrivilege
- SePermanentPrivilege
- **SeBackupPrivilege**——执行备份操作所需
- **SeRestorePrivilege**——执行还原操作所需
- **SeShutdownPrivilege**——在本地关闭系统所需
- SeDebugPrivilege
- SeAuditPrivilege
- SeSystemEnvironmentPrivilege
- SeChangeNotifyPrivilege
- SeRemoteShutdownPrivilege——远程关闭系统所需
- SeUndockPrivilege
- SeSyncAgentPrivilege
- SeEnableDelegationPrivilege

> **注意** 使用 Add 方法和 SWbemPermissionSet 对象时，必须使用显示的确切特权字符串。例如，`wmiService.Security_.Privileges.AddAsString "SeDebugPrivilege", True`

请注意，当使用标识符风格的连接时，您也可以指定特权。

```
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```

> **提示** 请注意，在刚刚显示的示例中，特权是 Debug，而不是 SeDebugPrivilege。当使用标识符时，您使用最简单的特权字符串版本。去掉字符串中的 Se 和 Privilege 部分。

### 查看高级 WMI 脚本实战

我们将通过介绍使用 WMI 可以执行的最复杂且最常被请求的任务之一来结束本章：管理文件权限。文件、其自由访问控制列表（DACL）、该 DACL 上的访问控制项（ACE）以及 ACE 上列出的受托者之间的关联可能很复杂。WMI 提供了一些捷径，因此您不必执行半打 ASSOCIATORS OF 查询来获取单个文件的权限，但导航类层次结构仍然可能令人困惑。在我们的示例中，我们将编写一个脚本，该脚本接受文件名或文件夹路径，然后显示与其关联的权限。我们首先提示输入该文件或文件夹名称。请注意，我们正在使用 Replace 方法将任何单反斜杠替换为双反斜杠。这是 WMI 的一个普遍要求，因为它使用反斜杠作为特殊字符。

```
Dim objFileSecuritySetting
Dim strFile
strFile = Replace(InputBox("File path and name?"),"\\","\\\\")
```

接下来，我们查询具有指定 Path 属性的 Win32_LogicalFileSecuritySetting 类实例。请注意，尽管该类的名称中包含 File，但它也适用于文件和文件夹。



# 第三部分：高级脚本技术、工具与技术

> **提示** 存在一个类似的 *Win32_LogicalShareSecuritySetting* 类，用于处理共享文件夹权限。你可以相对容易地修改以下示例，使其适用于共享文件夹而非文件和文件夹。

```
Set objFileSecuritySetting = _
    GetObject("winmgmts:Win32_LogicalFileSecuritySetting.path='" _
    & strFile & "'")
```

现在我们显示返回实例的描述及其 *ControlFlags* 属性。该属性本质上是一组位标志，因此我们编写一系列 *If...Then* 语句来检查特定标志是否开启。

```
'FileSecuritySetting 基础
wScript.Echo objFileSecuritySetting.Description
If objFileSecuritySetting.ControlFlags And 1 Then _
    wScript.Echo " 默认所有者"
If objFileSecuritySetting.ControlFlags And 2 Then _
    wScript.Echo " 默认组"
If objFileSecuritySetting.ControlFlags And 4 Then _
    wScript.Echo " DACL 存在"
If objFileSecuritySetting.ControlFlags And 8 Then _
    wScript.Echo " 默认 DACL"
If objFileSecuritySetting.ControlFlags And 16 Then _
    wScript.Echo " SACL 存在"
If objFileSecuritySetting.ControlFlags And 32 Then _
    wScript.Echo " 默认 SACL"
If objFileSecuritySetting.ControlFlags And 256 Then _
    wScript.Echo " DACL 自动继承请求"
If objFileSecuritySetting.ControlFlags And 512 Then _
    wScript.Echo " SACL 自动继承请求"
If objFileSecuritySetting.ControlFlags And 1024 Then _
    wScript.Echo " DACL 已自动继承"
If objFileSecuritySetting.ControlFlags And 2048 Then _
    wScript.Echo " SACL 已自动继承"
If objFileSecuritySetting.ControlFlags And 4096 Then _
    wScript.Echo " DACL 受保护"
If objFileSecuritySetting.ControlFlags And 8192 Then _
    wScript.Echo " SACL 受保护"
If objFileSecuritySetting.ControlFlags And 32768 Then _
    wScript.Echo " 自相关"
wScript.Echo
```

> **提示** 这是一个展示如何使用 VBScript 布尔运算符的绝佳示例。一个字节中的每一位都有一个值：第一位的值是 1，第二位是 2，依次是 4、8、16、32，依此类推，以 2 的幂次递增。要查看第一位是否开启，请使用 *FlagVariable And 1* 表达式。如果该位开启，将返回 TRUE；如果未开启，则返回 FALSE。类似地，*FlagVariable And 4* 将告诉你第三位是否开启（TRUE）或关闭（FALSE）。

接下来，我们要求安全设置实例返回其自身的安全描述符（DACL）。这是一个 Win32_SecurityDescriptor 类，我们通过使用安全设置的 GetSecurityDescriptor 方法检索它。

```
'安全描述符详情
'操作 win32_SecurityDescriptor 实例
Dim intReturn, objSecDesc
intReturn = objFileSecuritySetting.GetSecurityDescriptor(objSecDesc)
```

DACL 也有一个基于位的标志属性，因此我们遍历每一位以查看哪些是开启的。

```
WScript.Echo "安全描述符："
If objSecDesc.ControlFlags And 1 Then _
    WScript.Echo " 默认所有者"
If objSecDesc.ControlFlags And 2 Then _
    WScript.Echo " 默认组"
If objSecDesc.ControlFlags And 4 Then _
    WScript.Echo " DACL 存在"
If objSecDesc.ControlFlags And 8 Then _
    WScript.Echo " 默认 DACL"
If objSecDesc.ControlFlags And 16 Then _
    WScript.Echo " SACL 存在"
If objSecDesc.ControlFlags And 32 Then _
    WScript.Echo " 默认 SACL"
If objSecDesc.ControlFlags And 256 Then _
    WScript.Echo " DACL 自动继承请求"
If objSecDesc.ControlFlags And 512 Then _
    WScript.Echo " SACL 自动继承请求"
If objSecDesc.ControlFlags And 1024 Then _
    WScript.Echo " DACL 已自动继承"
If objSecDesc.ControlFlags And 2048 Then _
    WScript.Echo " SACL 已自动继承"
If objSecDesc.ControlFlags And 4096 Then _
    WScript.Echo " DACL 受保护"
If objSecDesc.ControlFlags And 8192 Then _
    WScript.Echo " SACL 受保护"
If objSecDesc.ControlFlags And 32768 Then _
    WScript.Echo " 自相关"
WScript.Echo String(25,"-")
```

安全描述符的 DACL 属性提供实际的 DACL，它由一个或多个 ACE 组成。我们将 DACL 赋值给一个变量以便进行操作。

```
Dim objDACL, objTrustee, strAccount
objDACL = objSecDesc.DACL
```

我们现在逐一遍历每个 ACE。

```
'遍历 DACL 上的 ACE
'每个都是一个 win32_ACE 实例
Dim objACE
For Each objACE In objDACL
```

每个 ACE 都有一个受托者（trustee），即分配给它的安全帐户（用户或组）。对于每个受托者，我们显示其域和名称。

```
'获取此 ACE 的受托者 - win32_Trustee 实例
Set objTrustee = objACE.Trustee
strAccount = objTrustee.Domain & "\" & objTrustee.Name
```

然后我们显示 ACE 的类型：*允许、拒绝或审核*。

```
'写入 ACE 类型
Select Case objACE.AceType
    case 0
        WScript.Echo strAccount & _
            " 允许："
    Case 1
        WScript.Echo strAccount & _
            " 拒绝："
    Case 2
        WScript.Echo strAccount & _
            " 审核："
End Select
```

被允许、拒绝或审核的权限存储在另一个位标志中，因此我们再次遍历每一位，并显示分配给该 ACE 的开启位的名称。

```
'写入权限
If objACE.AccessMask And 1 Then _
    WScript.Echo " 文件：列出目录"
If objACE.AccessMask And 2 Then _
    WScript.Echo " 文件：添加文件"
If objACE.AccessMask And 4 Then _
    WScript.Echo " 文件：添加子目录"
If objACE.AccessMask And 8 Then _
    WScript.Echo " 文件：读取扩展属性"
If objACE.AccessMask And 16 Then _
    WScript.Echo " 文件：写入扩展属性"
If objACE.AccessMask And 32 Then _
    WScript.Echo " 文件：遍历"
If objACE.AccessMask And 64 Then _
    WScript.Echo " 文件：删除子项"
If objACE.AccessMask And 128 Then _
    WScript.Echo " 文件：读取属性"
If objACE.AccessMask And 256 Then _
    WScript.Echo " 文件：写入属性"
If objACE.AccessMask And 65536 Then _
    WScript.Echo " 删除"
If objACE.AccessMask And 131072 Then _
    WScript.Echo " 读取控制"
If objACE.AccessMask And 262144 Then _
    WScript.Echo " 写入 DACL"
If objACE.AccessMask And 524288 Then _
    WScript.Echo " 写入所有者"
If objACE.AccessMask And 1048576 Then _
    WScript.Echo " 同步"
```

ACE 还包含描述其继承行为的标志，我们也将其显示出来。

```
'写入标志
If objACE.AceFlags And 1 Then _
    WScript.Echo " (非容器子对象将继承)"
If objACE.AceFlags And 2 Then _
    WScript.Echo " (容器子对象将继承)"
If objACE.AceFlags And 4 Then _
    WScript.Echo " (ACE 不传播继承)"
If objACE.AceFlags And 8 Then _
    WScript.Echo " (仅继承 ACE)"
If objACE.AceFlags And 16 Then _
    WScript.Echo " (已继承的 ACE)"
```

最后，我们在当前 ACE 和下一个 ACE 之间显示一行分隔符。

```
'分隔符
WScript.Echo String(25,"-")
Next
```

清单 10-8 是完整的脚本。

```
清单 10-8 文件权限
Dim objFileSecuritySetting
Dim strFile
strFile = Replace(InputBox("文件路径和名称？"),"\","\\")
Set objFileSecuritySetting = _
    GetObject("winmgmts:Win32_LogicalFileSecuritySetting.path='" _
    & strFile & "'")

'FileSecuritySetting 基础
WScript.Echo objFileSecuritySetting.Description
If objFileSecuritySetting.ControlFlags And 1 Then _
    WScript.Echo " 默认所有者"
If objFileSecuritySetting.ControlFlags And 2 Then _
    WScript.Echo " 默认组"
If objFileSecuritySetting.ControlFlags And 4 Then _
    WScript.Echo " DACL 存在"
If objFileSecuritySetting.ControlFlags And 8 Then _
    WScript.Echo " 默认 DACL"
If objFileSecuritySetting.ControlFlags And 16 Then _
    WScript.Echo " SACL 存在"
If objFileSecuritySetting.ControlFlags And 32 Then _
    WScript.Echo " 默认 SACL"
If objFileSecuritySetting.ControlFlags And 256 Then _
    WScript.Echo " DACL 自动继承请求"
If objFileSecuritySetting.ControlFlags And 512 Then _
    WScript.Echo " SACL 自动继承请求"
If objFileSecuritySetting.ControlFlags And 1024 Then _
    WScript.Echo " DACL 已自动继承"
If objFileSecuritySetting.ControlFlags And 2048 Then _
    WScript.Echo " SACL 已自动继承"
If objFileSecuritySetting.ControlFlags And 4096 Then _
    WScript.Echo " DACL 受保护"
```



## 第10章：高级WMI脚本编写

如果 `objFileSecuritySetting.ControlFlags And 8192`，则 _
    WScript.Echo " SACL 受保护"
如果 `objFileSecuritySetting.ControlFlags And 32768`，则 _
    WScript.Echo " 自相关"
WScript.Echo

'安全描述符详细信息
'使用 win32_SecurityDescriptor 实例
Dim intReturn, objSecDesc
intReturn = objFileSecuritySetting.GetSecurityDescriptor(objSecDesc)
WScript.Echo "安全描述符："
如果 `objSecDesc.ControlFlags And 1`，则 _
    WScript.Echo " 默认所有者"
如果 `objSecDesc.ControlFlags And 2`，则 _
    WScript.Echo " 默认组"
如果 `objSecDesc.ControlFlags And 4`，则 _
    WScript.Echo " DACL 存在"
如果 `objSecDesc.ControlFlags And 8`，则 _
    WScript.Echo " 默认 DACL"
如果 `objSecDesc.ControlFlags And 16`，则 _
    WScript.Echo " SACL 存在"
如果 `objSecDesc.ControlFlags And 32`，则 _
    WScript.Echo " 默认 SACL"
如果 `objSecDesc.ControlFlags And 256`，则 _
    WScript.Echo " DACL 自动继承要求"
如果 `objSecDesc.ControlFlags And 512`，则 _
    WScript.Echo " SACL 自动继承要求"
如果 `objSecDesc.ControlFlags And 1024`，则 _
    WScript.Echo " DACL 已自动继承"
如果 `objSecDesc.ControlFlags And 2048`，则 _
    WScript.Echo " SACL 已自动继承"
如果 `objSecDesc.ControlFlags And 4096`，则 _
    WScript.Echo " DACL 受保护"
如果 `objSecDesc.ControlFlags And 8192`，则 _
    WScript.Echo " SACL 受保护"
如果 `objSecDesc.ControlFlags And 32768`，则 _
    WScript.Echo " 自相关"
WScript.Echo String(25,"-")

dim objDACL, objTrustee, strAccount
objDACL = objSecDesc.DACL

'遍历 DACL 上的 ACE
'每个都是 Win32_ACE 的一个实例
Dim objACE
For Each objACE In objDACL
    '获取此 ACE 的受托方 - win32_Trustee 实例
    Set objTrustee = objACE.Trustee
    strAccount = objTrustee.Domain & "\" & objTrustee.Name
    
    '写入 ACE 类型
    Select Case objACE.AceType
        case 0
            WScript.Echo strAccount & _
                " 允许执行："
        Case 1
            WScript.Echo strAccount & _
            " 拒绝执行："
        Case 2
            WScript.Echo strAccount & _
            " 审计执行："
    End Select

    '写入权限
    如果 `objACE.AccessMask And 1`，则 _
        WScript.Echo " 文件：列出目录"
    如果 `objACE.AccessMask And 2`，则 _
        WScript.Echo " 文件：添加文件"
    如果 `objACE.AccessMask And 4`，则 _
        WScript.Echo " 文件：添加子目录"
    如果 `objACE.AccessMask And 8`，则 _
        WScript.Echo " 文件：读取扩展属性"
    如果 `objACE.AccessMask And 16`，则 _
        WScript.Echo " 文件：写入扩展属性"
    如果 `objACE.AccessMask And 32`，则 _
        WScript.Echo " 文件：遍历"
    如果 `objACE.AccessMask And 64`，则 _
        WScript.Echo " 文件：删除子项"
    如果 `objACE.AccessMask And 128`，则 _
        WScript.Echo " 文件：读取属性"
    如果 `objACE.AccessMask And 256`，则 _
        WScript.Echo " 文件：写入属性"
    如果 `objACE.AccessMask And 65536`，则 _
        WScript.Echo " 删除"
    如果 `objACE.AccessMask And 131072`，则 _
        WScript.Echo " 读取控制"
    如果 `objACE.AccessMask And 262144`，则 _
        WScript.Echo " 写入-DACL"
    如果 `objACE.AccessMask And 524288`，则 _
        WScript.Echo " 写入所有者"
    如果 `objACE.AccessMask And 1048576`，则 _
        WScript.Echo " 同步"

    '写入标志
    如果 `objACE.AceFlags And 1`，则 _
        WScript.Echo " （非容器子对象将继承）"
    如果 `objACE.AceFlags And 2`，则 _
        WScript.Echo " （容器子对象将继承）"
    如果 `objACE.AceFlags And 4`，则 _
        WScript.Echo " （ACE 不传播继承）"
    如果 `objACE.AceFlags And 8`，则 _
        WScript.Echo " （仅继承的 ACE）"
    如果 `objACE.AceFlags And 16`，则 _
        WScript.Echo " （已继承的 ACE）"

    '分隔符
    WScript.Echo String(25,"-")
Next

此技术几乎用于 WMI 中的所有权限。大多数与安全相关的类——包括 *Win32_LogicalFileSecuritySetting* 以及某些 Active Directory 类——都提供 *GetSecurityDescriptor* 方法，该方法可以像我们这里展示的那样使用。还有一个 *SetSecurityDescriptor* 方法，用于更改权限。只需获取安全描述符，对其进行修改，然后将其传递回 *SetSecurityDescriptor* 方法以应用权限更改即可。

> **注意** 仅仅因为你可以用脚本*做*某事，并不一定意味着你*应该*用脚本做那件事。文件权限就是一个很好的例子。尽管 WMI 提供了管理文件权限所需的一切，但使用它来实现此目的比使用命令行工具（如 Cacls.exe 或 Xcacls.exe）要复杂得多，如果你需要自动化其操作，这两种工具同样可以编写脚本。

### 总结

本章我们涵盖了很多内容。你学习了如何使用 *ASSOCIATORS OF* 和 *REFERENCES OF* 语句，以及了解了 WMI 支持的一些高级和灵活的安全技术。你还学习了如何通过使用 *WHERE* 子句和指定查询要返回的属性来细化和限制 WMI 查询结果。最后，你学习了如何处理 WMI 中最棘手的任务之一：管理 NTFS 文件权限。希望本章中的示例能帮助你的 WMI 脚本变得更强大、更高效。

# 第11章
## WMI 事件

- **本章内容：**
    - 理解 WMI 事件..................................... 285
    - 使用通知查询...................................... 288
    - 使用 WMI 工具.............................................. 300
    - 查看 WMI 事件的实际运行情况................................ 308
    - 总结....................................................... 317

在 Windows Management Instrumentation (WMI) 中管理事件是一项重要技能，它将使你的管理脚本更上一层楼。Microsoft Windows 是一个事件驱动的操作系统。通过使用 WMI 和 VBScript，我们可以监控事件并在事件发生时采取行动。我们将向你展示如何创建可作为监控工具使用的 WMI 脚本。

服务器和桌面是动态系统：文件被创建和修改，服务被启动和停止，进程被创建和销毁，事件日志被写入。作为管理员，你可能希望在这些操作发生时执行某些操作。例如，你可能希望检测服务何时启动或停止。程序获知这些操作的方式是通过*事件*。事件是程序可能希望响应的任何有趣操作。操作系统程序员和应用程序开发人员决定定义哪些事件以及它们如何发生。例如，当服务停止时会生成停止事件。当事件发生时，称其已*触发*。我们可以使用 WMI 来监控多种类型的事件。

### 理解 WMI 事件

在 WMI 中，事件是一个 WMI 对象，因此当事件触发时，我们可以使用生成的对象。这个事件对象是一个系统对象，因此以两个下划线 (__) 为前缀。事件对象从 __Event 类派生其基本功能。由于 __Event 类是抽象的，因此事件对象将是 __Event 类的子类。有几种类型的 __Event 类，但从脚本的角度来看，我们最有可能使用 __InstanceOperationEvent 的以下子类。

- __InstanceCreationEvent 在创建某些内容时触发，例如新进程或事件日志条目。
- __InstanceModificationEvent 在修改某些内容时触发，例如文件。
- __InstanceDeletionEvent 在删除某些内容时触发，例如文件。当进程销毁时也会触发此事件。

#### 理解使用者

使用已触发事件信息的对象称为*使用者*。没有事件使用者，事件将被忽略。使用者对象派生自 *EventViewerConsumer* 类，而后者又派生自 __*EventConsumer* 系统类。WMI 包括临时和永久使用者。临时使用者仅在使用者运行时接收事件。例如，监控 WMI 事件的 VBScript 通常被视为临时使用者。一旦脚本终止，事件处理就会结束，即使事件继续触发也是如此。我们将使用临时使用者。

永久使用者是接收特定类型事件的应用程序或组件对象模型 (COM) 对象。开发永久使用者超出了本书的范围，但你可以运行一个名为 eventtriggers.exe 的永久使用者应用程序，该程序适用于 Microsoft Windows XP。你可以使用此使用者监控写入本地或远程系统事件日志的事件。在命令提示符下键入 **eventtriggers /?** 和 **eventtriggers /create /?** 以获取更多信息。

> **提示** 当使用 *eventtriggers /create* 与 /TK 参数时，请记住它将在你提供的用户凭据上下文中运行。如果你未指定任何凭据，该工具将使用系统帐户。当为本地系统创建触发器时，你可以指定当前登录用户的凭据。当你希望在特定事件发生时让用户交互或干预时，这非常有用。

永久事件使用者需要在系统上注册才能接收事件通知。我们指的不是每个远程系统，而是你将监控其事件的系统。这要求你定义一个使用者实例和一个事件过滤器，我们稍后将介绍。在 VBScript 中使用 WMI 事件不需要任何注册。

#### 理解通知查询

通知查询是使用 WMI 查询语言 (WQL) 编写的查询，它指定要监控哪个事件以及返回哪些信息。这些查询被称为通知查询，因为当事件发生时你会收到通知。

```
select * from __InstanceCreationEvent
```

在此通知查询语句中，我们指定监控 __*InstanceCreationEvent* 类型。当任何类型的新实例被创建时，该查询将从 __*InstanceCreationEvent* 系统类返回所有属性。



我们可以创建一个通知查询，但要使其生效，我们需要执行该查询，也称为*订阅*该事件。我们可以同步、半同步或异步地执行通知查询。我们将在本章后续更详细地讨论这些概念。

#### 理解过滤器

过滤器实例用于定义或限制要监视的事件类型。过滤器派生自 `__EventFilter` 系统类。通常，过滤器作为通知查询语句的一部分来定义。

```
Select * from __InstanceCreationEvent WHERE TargetInstance ISA 'Win32_NTLogEvent'
```

在此通知查询语句中，我们返回 `__InstanceCreationEvent` 系统类的所有属性。然而，我们不需要每个实例，只需要一个特定类型，称为 TargetInstance。在此示例中，我们想要获取 `Win32_NTLogEvent` 类实例创建时的所有信息。你可能认为我们需要使用等号 (=) 运算符并构造如下过滤器。

```
TargetInstance='Win32_NTLogEvent'
```

然而，在 WMI 事件的世界里，这行不通，因为我们在比较类实例。相反，WQL 提供了一个不同的运算符：ISA。

```
TargetInstance ISA 'Win32_NTLogEvent'
```

此过滤器表示仅当实例是 *Win32_NTLogEvent* 类型时才执行查询。

#### 理解轮询

要在特定时间检查事件，我们可以创建事件计时器。绝对计时器在指定的日期和时间检查事件。这有一定价值，但在大多数情况下，*轮询*更有用。轮询不是一种定时器事件，但它与定时相关。轮询意味着定期检查某些操作，它通过在 WQL 语句中使用 *WITHIN* 子句来实现。

```
Select * from __InstanceCreationEvent WITHIN 5 where TargetInstance ISA 'CIM_DataFile' AND
TargetInstance.drive='e:' AND TargetInstance.Path='\\temp\\'
```

在此查询中，我们要求 WMI 每五秒钟检查一次 E:\Temp 中是否创建了新文件。

**提示** 当使用 WMI 工具（本章后面讨论）设置轮询间隔时，指定的值以毫秒为单位。在 VBScript 和 WBEMTest 中，该值以秒为单位。

第三部分：高级脚本技术、工具和技术

某些类，例如 CIM_DataFile 和 Win32_Process，要求你使用 WITHIN 子句。如果需要但未使用，你将收到错误消息。

> **最佳实践** 设置轮询间隔既是一门艺术，也是一门科学。如果你每几秒轮询一次，你会获得更多信息，但轮询过于频繁可能会引入大量开销。轮询频率取决于你的查询。由于编写不当的查询可能会严重降低系统性能，请在非生产系统上测试所有轮询查询。测试和经验将有助于确定合适的轮询间隔。

### 使用通知查询

让我们开始整合一些关于 WMI 事件的信息。首先，我们使用 WBEMTest 工具尝试一个通知查询。然后，我们研究一个半同步执行通知查询的脚本。最后，我们研究一个异步执行通知查询的脚本。

### 使用 WBEMTest

让我们使用 WBEMTest 来查看通知查询。我们将在第 12 章更详细地介绍 WBEMTest。启动 WBEMTest，然后单击“启用所有权限”，如图 11-1 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_307_0.png)

**图 11-1** WBEMTest 工具的主屏幕

单击“连接”按钮，并将命名空间更改为 root\cimv2。

![](img/4fefd6988ba5d4a92a65127617ca24c2_308_0.png)

图 11-2 在 WBEMTest 中指定连接信息

再次单击“连接”按钮以重新显示 WBEMTest 主屏幕。注意可用的选项：异步、同步和半同步。我们将在本章后面介绍异步查询。现在，接受默认的半同步方式。

单击“通知查询”按钮。在“查询”对话框中，输入以下内容，如图 11-3 所示：

> Select * from __InstanceCreationEvent WHERE TargetInstance ISA 'Win32_NTLogEvent'

![](img/4fefd6988ba5d4a92a65127617ca24c2_308_1.png)

图 11-3 输入通知查询

单击“应用”以显示“查询结果”对话框，如接下来的图 11-4 所示。

290 第三部分：高级脚本技术、工具和技术

![](img/4fefd6988ba5d4a92a65127617ca24c2_309_0.png)

图 11-4 通知查询的查询结果

在命令提示符窗口中，使用 **net stop** 命令停止一个服务。例如，停止 alerter 服务或其他正在运行的服务。服务停止后，你应该会在“查询结果”对话框中看到一些条目，如图 11-5 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_309_1.png)

图 11-5 当服务停止时检测到的 Win32_NTLogEvent 创建事件

双击列表中的第二个条目。选中“隐藏系统属性”复选框，以便更轻松地查看 __InstanceCreationEvent 的属性。图 11-6 显示了 __InstanceCreationEvent 的详细信息。

![](img/4fefd6988ba5d4a92a65127617ca24c2_310_0.png)

**图 11-6** *__InstanceCreationEvent* 的属性

注意 *TargetInstance* 属性显示为一个嵌入对象。这就是 *Win32_NTEventLog* 对象。双击 *TargetInstance* 以显示“属性编辑器”对话框，然后单击“查看嵌入对象”。你应该会看到 *Win32_NTEventLog* 对象的“对象编辑器”，如图 11-7 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_310_1.png)

**图 11-7** *Win32_NTEventLog* 对象的对象编辑器

在探索 *Win32_NTEventLog* 对象时，你会看到一些熟悉的事件日志属性，例如 Logfile、SourceName、Type 和 Message。探索完成后，关闭或取消所有打开的窗口，然后退出 WBEMTest。

#### 半同步执行通知查询

正如你在 WBEMTest 中看到的，默认的查询方法是半同步，这意味着查询执行后，控制权会很快返回给用户。要在脚本中半同步执行通知查询，需要调用 *ExecNotificationQuery* 方法。

在脚本中使用半同步方法允许查询方法之后的任何代码执行。使用此方法时，我们需要使用一种称为*阻塞*的 WMI 脚本技术。当使用阻塞时，脚本会阻塞（暂停）直到事件发生。当通知查询执行时，查询返回一个 *SWbemEventSource* 对象。*SWbemEventSource* 对象有一个名为 *NextEvent* 的方法。当调用 *NextEvent* 方法时，脚本将阻塞直到下一个事件发生。

```
Set oWMI=GetObject("winmgmts:{(security)}")
strQuery="Select * from __InstanceCreationEvent WHERE TargetInstance " &
"ISA 'win32_NTLogEvent'"
Set oEventSrc=oWMI.ExecNotificationQuery(strQuery)
'开始阻塞
Set NTEvent=oEventSrc.NextEvent()
'事件触发后脚本继续执行
```

在此代码片段中，执行一个通知查询并返回一个 *SWbemEventSource* 对象。当调用 *NextEvent* 方法时，脚本暂停并等待新条目被添加到事件日志中。当事件触发时，它返回一个与查询中 *TargetInstance* 属性对应的对象，在本例中是一个 *Win32_NTLogEvent*。按照目前的编写方式，该代码片段将等待事件发生，然后继续执行并退出脚本。

如果我们想检测更多的事件日志创建事件，可以添加一个循环来持续运行或运行指定次数。要中止脚本，如果你使用的是 CScript.exe，请按 Ctrl+C，或者在任务管理器中结束 WScript.exe 任务。

如果你想等待特定时间长度的事件，可以在 *NextEvent* 方法中指定一个以毫秒为单位的超时参数。

```
Set NTEvent=oEventSrc.NextEvent(60000)
```

此代码片段将等待 60 秒下一个事件，然后超时并继续执行脚本的其余部分。清单 11-1 演示了使用阻塞来等待新条目写入事件日志。

**清单 11-1 为事件阻塞**

```
Dim oWMI,oEventSrc,NTEvent
On Error Resume Next
strComputer="."
strQuery="Select * from __InstanceCreationEvent WHERE TargetInstance " &
"ISA 'win32_NTLogEvent'"
'你需要安全权限来读取任何安全事件
Set oWMI=GetObject("winmgmts:{(security)}!\\"&strComputer)
If Err.number<>0 Then
    strErrMsg= strErrMsg & "Error #" & err.number & " [0x" &
    CStr(Hex(Err.Number)) &"]" & vbCrLf
    If Err.Description <> "" Then
        strErrMsg = strErrMsg & "Error description: " & Err.Description & "."
    End If
    Err.Clear
```



wscript.echo strErrMsg
wscript.quit
End If

Set oEventSrc=oWMI.ExecNotificationQuery(strQuery)

'开始阻塞，并在超时一分钟后退出
Set NTEvent=oEventSrc.NextEvent(60000)
logtime=NTEvent.TargetInstance.TimeGenerated
logyr = left(logtime,4)
logmo = mid(logtime,5,2)
logdy = mid(logtime,7,2)
logtm = mid(logtime,9,6)

strMsg=NTEvent.TargetInstance.ComputerName & vbCrLf

strMsg=strMsg & "Event ID: " & NTEvent.TargetInstance.EventCode &_
"   Source: " & NTEvent.TargetInstance.SourceName & vbTab & logmo & "/" &_
logdy & "/" & logyr & "   [" & FormatDateTime(left(logtm,2) & ":" &_
Mid(logtm,3,2) & ":"&Right(logtm,2),3) & "]" & vbCrLf &
NTEvent.TargetInstance.Message

wscript.echo strMsg

在光盘上
你会在这个脚本以及本章列出的其他脚本，在随书附带的光盘上找到。

此脚本等待下一条条目写入事件日志。因为它可能是一个安全事件，所以我们需要明确地添加安全权限。

```
Set oWMI=GetObject("winmgmts:{(security)}!"&strComputer)
```

如果我们想更具体地选择要监视的事件类型，可以修改查询以按日志文件进行筛选。

```
strQuery="Select * from __InstanceCreationEvent WHERE TargetInstance " &\_
"ISA 'Win32_NTLogEvent' AND TargetInstance.LogFile='Security'"
```

在这个脚本中，我们正在监视任何事件。我们使用 *ExecNotificationQuery* 方法来创建事件订阅。

```
Set oEventSrc=oWMI.ExecNotificationQuery(strQuery)
```

我们必须确保脚本不会结束，否则我们将永远不知道事件何时发生。我们通过调用 *NextEvent* 方法并设置一个超时值为60,000毫秒或1分钟的超时来设置阻塞。

```
'开始阻塞，并在超时一分钟后退出
Set NTEvent=oEventSrc.NextEvent(60000)
```

当事件发生时，脚本继续执行，此时一个 Win32_NTEventlog 对象的实例变得可用。我们可以使用该对象的任何属性来为用户创建消息。在此脚本中，我们报告计算机名称、事件ID、事件源、时间戳和事件消息。

```
strMsg=NTEvent.TargetInstance.ComputerName & vbCrLf
strMsg=strMsg & "Event ID: " & NTEvent.TargetInstance.EventCode & _
" Source: " & NTEvent.TargetInstance.SourceName & vbTab & logmo & "/" & _
logdy & "/" & logyr & " [" & FormatDateTime(left(logtm,2) & ":" & _
Mid(logtm,3,2) & ":"&Right(logtm,2),3) & "]" & vbCrLf & _
NTEvent.TargetInstance.Message
wscript.echo strMsg
```

半同步执行通知查询并使用阻塞技术相当简单，但有一些限制。脚本执行会暂停，直到下一个事件发生。如果你想捕获多个事件，必须构造一个循环。如果你想捕获不同类型的事件，或者你希望脚本更具响应性，则需要异步执行通知查询。

#### 异步执行通知查询

异步调用的脚本和工具具有更好的响应性。要亲自验证，请按照本章前面的 WBEMTest 步骤进行操作，但选择 Asynchronous 选项。WBEMTest 的响应性更好，因为它不需要等待，并且除了等待下一个事件外几乎不做其他任何事情。

要异步执行通知查询，需调用 ExecNotificationQueryAsync 方法。当通知查询被异步执行时，脚本不会阻塞（暂停）等待下一个事件发生。相反，当您订阅的事件发生时，WMI 会调用您的脚本。但是，您的脚本如何知道如何处理这个调用呢？答案在于事件接收器。

### 使用事件接收器

事件接收器，简称接收器，是一个在异步操作完成时被调用的对象。在 WMI 中，接收器通过 WbemScripting.SWbemSink 对象实现。创建和使用接收器并不特别困难。在下面的脚本中，我们创建一个接收器并给它一个名称，传统上这个名称以下划线结尾。你一会儿就会明白为什么。

```
Set SINK = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
```

我们通过使用 ExecNotificationQueryAsync 执行通知查询时，将接收器的名称作为参数传递。

```
strQuery="Select * from __InstanceCreationEvent WHERE " & _
"TargetInstance ISA 'win32_NTLogEvent'"
Set oWMI=GetObject("winmgmts:{(security)}")
oWMI.ExecNotificationQueryAsync SINK, strQuery
```

这会将查询结果链接到接收器——任何返回的信息都将被发送到接收器。但是，脚本如何知道何时有返回信息呢？这是通过使用标准的 COM 事件（如 *OnObjectReady*）来完成的。我们创建一个子程序，该子程序将在指定的 COM 事件发生时被调用。在基于事件的编程中，当您的代码被告知某个事件完成时，这被称为*回调*。

```
'回调子程序
'当我们从异步调用收到返回时，将执行此代码
Sub SINK_OnObjectReady(NTEvent,refContext)

logtime=NTEvent.TargetInstance.TimeGenerated
logyr = Left(logtime,4)
logmo = mid(logtime,5,2)
logdy = mid(logtime,7,2)
logtm = mid(logtime,9,6)

WScript.Echo " Event ID: " & NTEvent.TargetInstance.EventCode & _
" Source: " & NTEvent.TargetInstance.SourceName & vbTab & logmo & _
"/" & logdy & "/" & logyr & " [" & FormatDateTime(left(logtm,2) & _
":"&Mid(logtm,3,2) & ":"&Right(logtm,2),3) & "]" & vbCrLf & _
NTEvent.TargetInstance.message

End Sub
```

在这个子程序中，当 WMI 事件触发时，它也会触发 *OnObjectReady* 事件。该子程序包括接收器的名称 *SINK_* 和 COM 事件 *OnObjectReady*。COM 对象返回 WMI 对象（还记得 WBEMTest 中的嵌入对象吗？）。COM 对象还返回一个上下文引用（目前未使用，但我们为了完整性将其包含在内）。

你可能会最常使用 *OnObjectReady* 事件。你也可能会使用以下事件之一：

- *OnCompleted* 事件在异步调用完成时触发。此事件返回一个整数，指示成功（0）或失败（错误编号），如果调用失败，则返回对 WMI *ERR* 对象的引用。
- *OnProgress* 事件在异步调用返回进度状态消息时触发。并非每个对象或类都支持此事件方法；你必须通过将异步调用的 *iFlags* 参数设置为 *wbemFlagSendStatus* 值，在你的异步查询中请求它。所需的参数是一个描述要完成的总任务数的整数，一个描述当前正在处理的项目的整数，一个描述当前任务状态的字符串，以及上下文引用对象。
- *Cancel* 事件取消接收器以及到异步查询的所有连接。它没有参数。
- *OnObjectPut* 事件在对象异步*放置*或设置值时触发。所需的参数是 WMI 对象和上下文引用对象。

#### 清单 11-2 异步监视事件日志

```
Dim oWMI,oEventSrc,NTEvent,objSINK
strComputer="."
strQuery="Select * from __InstanceCreationEvent WHERE TargetInstance " & _
"ISA 'Win32_NTLogEvent'"

'需要安全权限
Set oWMI=GetObject("winmgmts:{(security)}\\" & strComputer & "\root\cimv2")
Set objSINK = wscript.CreateObject("WbemScripting.SWbemSink","SINK_")

oWMI.ExecNotificationQueryAsync objSINK, strQuery

'脚本必须继续运行足够长的时间以使异步操作完成。
'实现此目的的一种方法是使用消息框。如果你点击确定，
'脚本将在异步操作完成之前结束，它将没有地方显示其结果。
MsgBox "Waiting for an event to happen.  Do NOT press OK until you " & _
"get your results or you won't see anything.",vbOKOnly+vbInformation, _
"WMI Sink Demo"

'取消 SINK，因为我们不再需要它来接收信息。
objSINK.Cancel

wscript.quit

'回调子程序
'当我们从异步调用收到返回时，将执行此代码
Sub SINK_OnObjectReady(NTEvent,refContext)

logtime=NTEvent.TargetInstance.TimeGenerated
logyr = Left(logtime,4)
logmo = mid(logtime,5,2)
logdy = mid(logtime,7,2)
logtm = mid(logtime,9,6)

WScript.Echo " Event ID: " & NTEvent.TargetInstance.EventCode & _
"   Source: " & NTEvent.TargetInstance.SourceName & vbTab & logmo & _
"/" & logdy & "/" & logyr & " [" & FormatDateTime(left(logtm,2) & _
":"&Mid(logtm,3,2) & ":"&Right(logtm,2),3) & "]" & vbCrLf & _
NTEvent.TargetInstance.message
End Sub
```

与半同步查询一样，如果在收到通知之前脚本结束，你将永远收不到通知。你需要一些东西来保持脚本存活——即使像消息框这样简单的东西也可以。此脚本显示一个消息框以保持脚本运行，但有一个缺点。我们很难抗拒点击确定，这就像我们无法忽略响起的电话一样。



# 第三部分：高级脚本技术、工具与技术

如果你的脚本还有其他工作要做，或者希望系统尽可能保持响应，那么异步查询本地系统会很有帮助。当你需要监视多个远程系统时，异步查询也更容易操作。你可以连接到每个远程系统并执行异步通知查询，每个系统都会响应到同一个接收器。

这并不意味着你不能在同一个脚本中设置多个接收器和多个查询。来看看清单11-3中的脚本。这个脚本每30秒检查一次CPU利用率。如果处理器负载超过70%，就会显示一条消息。脚本还会每10秒检查一次是否启动了字符映射程序。当检测到字符映射程序时，脚本就会终止。

```
清单11-3 创建处理器查询
'用法：cscript|wscript wmiprocessorquery.vbs 服务器

Dim CPUSink,ProcSink,objShell
On error Resume Next

If (wscript.arguments.count=0) Then
    strMsg="用法：" & vbCrLf
    strMsg=strMsg & "cscript|wscript processorquery.vbs 服务器" & vbCrLf
    strMsg=strMsg & "示例：cscript processorquery.vbs File02"
    wscript.echo strMsg
    wscript.quit
Else
    strSrv=wscript.arguments(0)
End If

'每30秒检查一次处理器负载是否大于70%。
strCPUQuery="Select * from __InstanceModificationEvent WITHIN 30 WHERE " &
"TargetInstance ISA 'Win32_Processor' AND " &
"TargetInstance.LoadPercentage >70"

'每10秒检查一次是否存在charmap.exe进程
strProcQuery="Select * from __InstanceCreationEvent WITHIN 10 WHERE " &
"TargetInstance ISA 'win32_Process' AND " &
"TargetInstance.Name='charmap.exe'"

Set objShell=CreateObject("Wscript.Shell")
Set CPUSink=wscript.CreateObject("WBemScripting.SWbemSink","CPUSINK_")
Set ProcSink=wscript.CreateObject("WBemScripting.SWbemSink","PROCSINK_")

Set oWMILocal=GetObject("winmgmts://")
oWMILocal.ExecNotificationQueryAsync ProcSink,strProcQuery
If err.number<>0 Then
    objShell.Popup "哎呀！本地创建进程事件接收器时出错。" &
    vbCrLf & "错误编号：" &err.number & vbCrLf &
    "描述（如果可用）：" & vbCrLf & " " & err.description &
    vbCrLf & "来源（如果可用）：" & vbCrLf & " " &
    err.source,-1,"CPU 监视",vbOKOnly+vbCritical
    wscript.quit
Else
Err.Clear
End If

Set oWMIRemote=GetObject("winmgmts://" & strSrv)
If err.number<>0 Then
    objShell.Popup "哎呀！连接到 " & _
        UCASE(strSrv) & " 时出错。" & vbCrLf & "错误编号：" &err.number & vbCrLf & _
        "描述（如果可用）：" & vbCrLf & " " & _
        err.description & vbCrLf & "来源（如果可用）：" & _
        vbCrLf & " " & Err.source,-1,"CPU 监视",vbOKOnly+vbCritical
    wscript.quit
Else
    oWMIRemote.ExecNotificationQueryAsync CPUSink,strCPUQuery
    If err.number<>0 Then
        objShell.Popup "哎呀！为 " & _
            UCASE(strSrv) & " 创建CPU接收器时出错。" & vbCrLf & "错误编号：" &err.number & vbCrLf & _
            "描述（如果可用）：" & vbCrLf & " " & _
            err.description & vbCrLf & "来源（如果可用）：" & _
            vbCrLf & " " & err.source,-1,"CPU 监视",vbOKOnly+vbCritical
        wscript.quit
    Else
        err.Clear
    End If
End If

objShell.popup "启动字符映射程序以停止监视",3,"CPU 监视",0+32

blnLoop=True
'检查触发进程是否已运行，每5秒休眠一次。
while blnLoop
    wscript.sleep 5
wend

objShell.Popup "正在取消监视。你可以继续关闭 " & _
    "触发应用程序。",3,"CPU 监视",vbOKOnly+vbInformation
objShell.AppActivate("字符映射")

CPUSink.Cancel()
ProcSink.Cancel()
wscript.DisconnectObject(CPUSink)
wscript.DisconnectObject(ProcSink)

Set oWMILocal=Nothing
Set oWMIRemote=Nothing
Set CPUSink=Nothing
Set ProcSink=Nothing
wscript.quit

'**************************************************************
Sub CPUSINK_OnObjectReady(objEvent,objContext)
    strSystem=objEvent.Path_.Server
    'wscript.echo "fired " & NOW
    objShell.popup "处理器负载为 " & _
        objEvent.TargetInstance.LoadPercentage & "%" & _
        vbCrLf & NOW,-1,"系统 - " & strSystem,vbOKOnly+vbInformation
End Sub

Sub PROCSINK_OnObjectReady(objEvent,objContext)
' 检测到触发器以关闭此脚本
    blnLoop=False
End Sub

'EOF
```

> **重要提示** 清单11-3中的脚本要求被查询的服务器至少运行Microsoft Windows 2000 SP3。在更旧的版本上运行可能无法工作，并且可能导致内存泄漏。

清单11-3使用了两个异步查询和事件接收器。第一个查询和接收器用于脚本的主体部分，用于监视CPU利用率。

```
'每30秒检查一次处理器负载是否大于70%。
strCPUQuery="Select * from __InstanceModificationEvent WITHIN 30 WHERE " & _
"TargetInstance ISA 'win32_Processor' AND " & _
"TargetInstance.LoadPercentage >70"
```

> **提示** 根据你的系统，要使CPU利用率事件触发，你可能需要降低负载百分比。

第二个查询和接收器用于监视可用于触发脚本终止的进程是否存在。

```
'每10秒检查一次是否存在charmap.exe进程
strProcQuery="Select * from __InstanceCreationEvent WITHIN 10 WHERE " & _
"TargetInstance ISA 'win32_Process' AND " & _
"TargetInstance.Name='charmap.exe'"
```

> **注意** 这个巧妙技术的功劳归于Matthew Lavy和Ashley Meggitt，他们在其优秀著作《Windows Management Instrumentation》（New Riders，2002）中提出了这个方法。

在创建接收器并执行查询后，脚本会执行一个循环，直到*blnLoop*的值为TRUE。

```
blnLoop=True
'检查触发进程是否已运行，每5秒休眠一次。
while blnLoop
    wscript.sleep 5
wend
```

如果检测到charmap.exe进程，进程监视接收器的事件会触发并回调相应的子程序。

```
Sub PROCSINK_OnObjectReady(objEvent, objContext)
    '检测到触发器以关闭此脚本
    blnLoop=False
End Sub
```

*blnLoop*的值被设置为FALSE，这将退出循环并完成脚本。然后我们取消接收器并调用*DisconnectObject*方法。

> **最佳实践** 总是最好取消接收器并调用*DisconnectObject*，特别是在查询远程系统时。VBScript和Windows Script Host在清理方面做得相当好，但自己进行清理并无坏处。

你可以使用任何你想要的程序作为触发器——你甚至可以创建自己的，就像Lavy和Meggitt所做的那样。我们选择字符映射程序是因为它是一个很少使用的程序，但在所有版本的Microsoft Windows中几乎普遍存在。

> **重要提示** 虽然异步查询很有用，但它们并非没有风险。WMI用来连接到接收器的回调机制意味着你的脚本正在等待来自某处的消息。从理论上讲，通过网络拦截COM通信并插入恶意代码是可能的。我们建议将WMI身份验证级别设置为*wbemAuthenticationLevelPktPrivacy*。

### 使用WMI工具

如果你不想创建脚本或者没有时间，你可以使用WMI工具附带的WMI事件注册和WMI事件查看器实用程序。

> **更多信息** 你可以在Microsoft网站下载WMI工具。
http://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=6430F853-1120-48DB-8CC5-F2ABDC3ED314

（此链接在随附CD上；点击*WMI工具*。）

#### 使用WMI事件注册

你可以使用WMI事件注册工具来定义消费者和过滤器对象。当事件触发时，你可以使用WMI事件查看器来查看事件的详细信息。让我们来演练一个事件注册。在这个例子中，我们将设置一个事件注册来检测何时有新文件被添加到C:\downloads文件夹。



要启动 WMI 事件注册，请点击“程序”菜单上的 WMI 事件注册快捷方式。此工具必须在 Internet Explorer 中运行。如果你正在运行安装了 SP2 的 Windows XP，请确保已指定允许被阻止的内容。然后，系统将提示你连接到命名空间 root\CIMV2，如图 11-8 所示。

![图 11-8 在 WMI 事件注册中连接到命名空间](img/4fefd6988ba5d4a92a65127617ca24c2_320_0.png)

如果你想连接到远程计算机，请单击计算机按钮并输入该机器的名称，如图 11-9 所示。请务必将起始命名空间更改为 **root\cimv2**。

![图 11-9 浏览远程计算机上的命名空间](img/4fefd6988ba5d4a92a65127617ca24c2_320_1.png)

默认设置使用当前凭据，如图 11-10 所示。

![图 11-10 连接到 WMI 事件注册时的登录凭据](img/4fefd6988ba5d4a92a65127617ca24c2_320_2.png)

如果你想指定备用凭据，请清除“以当前用户身份登录”复选框。如果你连接到本地系统，该复选框将被禁用，因为只能为远程系统指定备用凭据。如果你单击“选项”按钮，将显示其他身份验证和权限选项，如图 11-11 所示。

![图 11-11 连接到 WMI 事件注册时展开的登录凭据](img/4fefd6988ba5d4a92a65127617ca24c2_321_0.png)

如果你正在异步查询远程系统，我们建议将身份验证级别设置为“数据包隐私”。根据你要查询的对象类，或者如果你要查询安全日志，则必须启用所有权限。在指定连接选项后，WMI 事件注册的起始页将出现，如图 11-12 所示。

![图 11-12 WMI 事件注册的起始页](img/4fefd6988ba5d4a92a65127617ca24c2_321_1.png)

我们已准备好创建事件筛选器和使用者。右键单击 `__EventFilter`，然后单击“新建实例”。此时将出现“编辑新实例属性”对话框，如图 11-13 所示。

![图 11-13 创建新筛选器时的属性对话框](img/4fefd6988ba5d4a92a65127617ca24c2_322_0.png)

在对话框中，设置以下属性。请记住，筛选器实际上就是我们的通知查询。在此查询中，每 30 秒监控一次 `C:\downloads` 文件夹，以查看是否添加了新文件。

- 名称：NewFileAdded
- 查询：Select * from `__InstanceCreationEvent` WITHIN 30 where TargetInstance ISA 'CIM_DATAFILE' AND TargetInstance.drive='C:' AND TargetInstance.Path='\\downloads\\'
- 查询语言：WQL

单击“确定”以创建 *NewFileAdded* 筛选器。你可以随时通过右键单击该筛选器并选择“编辑实例属性”来编辑该实例。

> **提示** 查阅 WMI 工具的帮助文档，以获取更多事件筛选器的示例。

既然我们有了筛选器，就需要一个使用者。在左上方面板的下拉框中，单击“使用者”。可以创建两种类型的使用者：*CmdTriggerConsumer* 和 *EventViewerConsumer*，如图 11-14 所示。

![图 11-14 在 WMI 事件注册中查看使用者](img/4fefd6988ba5d4a92a65127617ca24c2_323_0.png)

右键单击 `EventViewerConsumer`，然后选择“新建实例”以显示如图 11-15 所示的“编辑新实例属性”对话框。

![图 11-15 创建新事件查看器使用者时的属性对话框](img/4fefd6988ba5d4a92a65127617ca24c2_323_1.png)

按如下方式设置这些属性。

- 描述：用于新文件事件的使用者
- 名称：NewFileConsumer
- 严重性：1

由于本地系统将接收事件通知，因此 MachineName 字段留空。单击“确定”以创建 *NewFileConsumer* 使用者。如图 11-16 所示，之前创建的 *NewFileAdded* 筛选器显示在右侧窗格中。现在我们将使用者和筛选器绑定在一起。在我们这样做之前，不会发生事件通知。

![图 11-16 新创建的名为 NewFileConsumer 的使用者](img/4fefd6988ba5d4a92a65127617ca24c2_324_0.png)

要将 *NewFileAdded* 筛选器注册到 *NewFileConsumer* 使用者，请右键单击 *NewFileAdded* 筛选器，然后单击“注册”。你也可以单击菜单栏中的“注册”（绿色对勾）按钮。图 11-16 显示了筛选器注册后的结果。从此以后，我们将拥有一个永久事件使用者，直到我们取消将筛选器注册到使用者。要查看事件，我们将使用 WMI 事件查看器实用程序。

#### 使用 WMI 事件查看器

要启动 WMI 事件查看器，请找到并单击“程序”菜单上的 WMI 事件查看器快捷方式。首次打开 WMI 事件查看器时，你会看到一个空白屏幕，如图 11-17 所示，除非当时正在注册某个事件。

![图 11-17 空白的 WMI 事件查看器](img/4fefd6988ba5d4a92a65127617ca24c2_325_0.png)

> **提示** 你可以通过单击笔形按钮从 WMI 事件查看器启动 WMI 事件注册工具。

在你的 C:\ 驱动器上创建一个名为 *downloads* 的文件夹。向此文件夹中添加一个文件。当检测到新文件时，事件将触发并出现在 WMI 事件查看器中，如图 11-18 所示。

![图 11-18 WMI 事件查看器显示有关检测到的已注册事件的信息](img/4fefd6988ba5d4a92a65127617ca24c2_325_1.png)

出现黄色警告图标是因为我们将在使用者中的严重性设置为 1。如果我们将其设置为 0，则会出现红色严重性图标。将严重性设置为 2 意味着不显示任何图标。要显示事件属性，请双击该事件。如图 11-19 所示，目标实例是一个嵌入对象。

![图 11-19 WMI 事件查看器中事件的属性](img/4fefd6988ba5d4a92a65127617ca24c2_326_0.png)

要显示目标实例的属性，请单击“对象”按钮。图 11-20 显示了添加到下载文件夹中的新文件的 *CIM_DataFile* 属性。

![图 11-20 WMI 事件查看器中事件内嵌入对象的属性](img/4fefd6988ba5d4a92a65127617ca24c2_326_1.png)

使用 WMI 事件注册和 WMI 事件查看器工具是监控事件的好方法，也是脚本开发的有用原型技术。你可以查看返回的对象类型以及属性值，从而更轻松地创建自己的脚本。

> **提示** 你可以根据需要定义任意数量的使用者和筛选器。它们都将显示在 WMI 事件查看器中，这就是为什么良好的使用者描述很重要的原因。

### 实际查看 WMI 事件

让我们通过将到目前为止涵盖的所有内容放入一个完整的脚本中来结束本章。清单 11-4 是一个 WSF 脚本，它监控来自特定日志文件的特定类型事件，并在 Internet Explorer 窗口中显示结果。该脚本读取计算机列表并为每台计算机创建异步查询。

> **注意** 如果你需要复习 WSF 脚本，请回顾第 3 章“Windows 脚本文件”。

```xml
<?xml version="1.0" ?>
<package>
<comment>
!!!!在非生产环境中测试！！！
</comment>
<job id="EventAlert">
  <?job error="false" debug="false" ?>
<runtime>
<description>
EVENTALERT.WSF
监控远程计算机上的事件日志。你可以指定要监控的事件日志（如应用程序或系统）以及事件类型（如错误或警告）。轮询间隔指定检查的频率。

此脚本使用 WMI 异步通知，并会在检测到事件时以弹出窗口的形式显示事件。
</description>
<named helpstring="要监控的计算机列表" name="File" required="true" type="string"/>
<named helpstring="轮询间隔秒数" name="Poll" required="true" type="string"/>
<named helpstring="要监控的日志文件，例如应用程序或安全" name="Log" required="true" type="string"/>
<named helpstring="要监控的事件类型，例如警告或错误" name="Type" required="true" type="string"/>
<named helpstring="备用凭据用户名" name="User" required="false" type="string"/>
<named helpstring="备用凭据密码" name="Password" required="false" type="string"/>
<example>cscript EventAlert.wsf /File:servers.txt /Poll:20 /Log:Application /Type:Error
cscript EventAlert.wsf /File:servers.txt /Poll:60 /Log:System /Type:Warning /User:Admin / Password:P@ssw0rd
</example>
</runtime>
<object id="ie" progid="InternetExplorer.Application" events="true" reference="true"/>
<object id="objFSO" progid="Scripting.FileSystemObject" reference="TRUE"/>
```



## 310 第三部分：高级脚本技术、工具与技术

```xml
<object id="wshShell" progid="WScript.Shell" reference="TRUE"/>
<object id="objLocator" progid="WbemScripting.SWbemLocator" _
reference="TRUE"/>
<object id="objSink" progid="WBemScripting.SWbemSink" events="TRUE" _
reference="TRUE"/>
<object id="objProcSink" progid="WBemScripting.SWbemSink" events="TRUE" _
reference="TRUE"/>
<object id="ie" progid="InternetExplorer.Application" events="true" _
reference="true"/>
<object id="objFSO" progid="Scripting.FileSystemObject" reference="TRUE"/>
<script id="Main" language="VBScript">
<!--CDATA[
On Error Resume Next
If WScript.Arguments.Count<4 Then
    WScript.Arguments.ShowUsage
    WScript.Quit
End If

If WScript.Arguments.Named.Exists("File") Then
    strFile=WScript.Arguments.Named("File")
    If objFSO.FileExists(strFile)<>True Then
        WScript.Echo "Can't find " & strFile
        WScript.Quit
    End If
End If

If WScript.Arguments.Named.Exists("Poll") Then
    iPoll=WScript.Arguments.Named("Poll")
Else
    WScript.Echo "You forgot to specify a polling interval."
    WScript.Arguments.ShowUsage
    WScript.Quit
End If

If WScript.Arguments.Named.Exists("Log") Then
    strLog=WScript.Arguments.Named("Log")
Else
    WScript.Echo "You forgot to specify an event log."
    WScript.Arguments.ShowUsage
    WScript.Quit
End If

If WScript.Arguments.Named.Exists("Type") Then
    strType=WScript.Arguments.Named("Type")
Else
    WScript.Echo "You forgot to specify an event type."
    WScript.Arguments.ShowUsage
    WScript.Quit
End If

If WScript.Arguments.Named.Exists("User") Then
    strUser=WScript.Arguments.Named("User")
End If

If WScript.Arguments.Named.Exists("Password") Then
    strPassword=WScript.Arguments.Named("Password")
End If

strQuery="Select * from __InstanceCreationEvent WITHIN " & iPoll &_
" where TargetInstance ISA " & '"win32_NTLogEvent" AND " &_
"TargetInstance.Logfile='" & strLog & '" AND " &_
"TargetInstance.Type='" & strType & '"'

'check every 10 seconds for existence of charmap.exe process
strProcQuery="Select * from __InstanceCreationEvent WITHIN 10 WHERE " &_
"TargetInstance ISA 'win32_Process' AND " &_
"TargetInstance.Name='charmap.exe'"

'uncomment for debugging
' WScript.Echo strQuery
'wscript.echo "connecting as " & strUser & " " & strPassword

'connect to local system and create
Set objWMILocal=GetObject("winmgmts://")
objWMILocal.ExecNotificationQueryAsync objProcSink,strProcQuery

Dim objFile
Set objFile=objFSO.OpenTextFile(strFile,ForReading)
Do While objFile.AtEndOfStream<>True
strComputer=Trim(objFile.ReadLine)
If TestPing(strComputer,True) Then
'add security privilege if querying security logs
If UCase(strLog)="SECURITY" Then
objLocator.Security_.Privileges.AddAsString "SeSecurityPrivilege",True
End If
Err.Clear
set objWMI=objLocator.ConnectServer(strComputer,"root\cimv2",_
strUser,strPassword)
If Err.Number<>0 Then
WScript.Echo "Failed to connect to " & UCase(strComputer) &_
" [Error #" & Hex(Err.Number) &" " & err.Description & "]"
End If
Err.Clear
objWMI.Security_.authenticationLevel = WbemAuthenticationLevelPktPrivacy
WScript.Echo "Connecting sink to " & strComputer
Err.clear
objWMI.ExecNotificationQueryAsync objSink, strQuery
If Err.Number<>0 Then
WScript.Echo "Asynch Query failed To " & UCase(strComputer) &_
" [Error #" & Hex(Err.Number) & " " & err.Description & "]"
End If
Else
WScript.Echo "Failed to ping " & UCASE(strComputer)
Err.Clear
End If
Loop
objFile.close

strTitle="Monitoring"
ie.width=630
ie.height=530
ie.top=10
ie.left=10
ie.menubar=False
ie.statusbar=False
ie.resizable=True
ie.toolbar=False
ie.navigate ("About:blank")
ie.document.title=strTitle

do while ie.readyState<>4
Loop
ie.visible=True

ie.document.body.innerHTML="<font face=Tahoma Size=1 Color=Blue>" &_
strQuery & "</font><br><HR>"

blnFlag=True

wscript.echo "Monitoring...launch CHARMAP.EXE to end."
blnLoop=True
'Check if trigger process has been run, sleeping every 5 seconds.
while blnLoop
  wscript.sleep 5
wend

wScript.Echo "Cancelling and disconnecting sink"
objSink.Cancel
objProcSink.Cancel
wscript.DisconnectObject(objSINK)
wscript.DisconnectObject(objPROCSINK)
ie.Quit
wScript.Quit

' _____________________________________________________________
'callback subroutines
'this is code to happen when we get a return from the async call
' _____________________________________________________________
Sub objSINK_OnObjectReady(NTEvent,refContext)
On Error Resume Next

'define background color variables to alternate
if blnFLAG then
  strColor="#FFFFFF"
  blnFlag=False
Else
  strColor="#CCFF66"
  blnFlag=True
End If

logtime=NTEvent.TargetInstance.TimeGenerated
logyr = Left(logtime,4)
logmo = Mid(logtime,5,2)
logdy = Mid(logtime,7,2)
logtm = Mid(logtime,9,6)

strMsg=NTEvent.TargetInstance.ComputerName & "  Event ID: " &_
NTEvent.TargetInstance.EventCode &_
" Source: " & NTEvent.TargetInstance.SourceName & vbTab & logmo & _
"/" & logdy & "/" & logyr & " [" & FormatDateTime(left(logtm,2) & _
":"&Mid(logtm,3,2) & ":"&Right(logtm,2),3) & "]" & vbCRLF & _
NTEvent.TargetInstance.message
'you can use a popup if you'd like
' wshShell.Popup strMsg,45,NTEvent.TargetInstance.ComputerName & _
" Event Log Alert",vbOKOnly

ie.document.body.InsertAdjacentHTML "beforeEnd","<Table border=0 " & _
"cellpadding=0 cellspacing=2><TR><TD BgColor=" & strColor & _
"><font face=tahoma size=1>" & strMsg & "</TD></TR>
End Sub

Sub OBJPROCSINK_OnObjectReady(objEvent,objContext)
'trigger has been detected to close out this script
    blnLoop=False
End Sub

' ---------------------------------------------------------------
' Function TestPing
'
' Tests connectivity to a given name or address; returns true or False
' ---------------------------------------------------------------
Function TestPing(sName,bPingAvailable)
On Error Resume Next
If Not bPingAvailable Then
    TestPing=False
    Exit Function
End If
Dim cPingResults, oPingResult
Set cPingResults = GetObject("winmgmts://./root/cimv2")._
ExecQuery("SELECT * FROM Win32_PingStatus WHERE Address = '" & sName & "'")
For Each oPingResult In cPingResults
    If oPingResult.StatusCode = 0 Then
        TestPing = True
        'wscript.echo "  Success"
    Else
        TestPing = False
        'WScript.Echo "  *** FAILED"
    End If
Next
End Function
]]>
</script>
</job>
</package>
```

该脚本接受几个参数，其定义如下。

```xml
<named helpstring="要监视的计算机列表" name="File" required="true" type="string"/>
<named helpstring="轮询间隔的秒数" name="Poll" required="true" type="string"/>
<named helpstring="要监视的日志文件，例如应用程序或安全日志" name="Log" required="true" type="string"/>
<named helpstring="要监视的事件类型，如警告或错误"
name="Type" required="true" type="string"/>
<named helpstring="备用凭据用户名" name="User" required="false" type="string"/>
<named helpstring="备用凭据密码" name="Password" required="false" type="string"/>
```

*用户名*和*密码*参数是可选的。若要使用当前凭据运行脚本，您可以输入类似以下的命令。

```
cscript Listing11-4.wsf /File:servers.txt /Poll:20 /Log:System /Type:Error
```

脚本将连接到 `servers.txt` 中列出的每台服务器，建立异步查询，并每 20 秒检查一次系统日志中是否有任何新的错误条目。脚本将持续运行，直到检测到 `charmap.exe` 进程为止。我们首先定义脚本所需的对象。

```xml
<object id="ie" progid="InternetExplorer.Application" events="true" _ reference="true"/>
<object id="objFSO" progid="Scripting.FileSystemObject" reference="TRUE"/>
<object id="wshShell" progid="WScript.Shell" reference="TRUE"/>
<object id="objLocator" progid="WbemScripting.SWbemLocator" _ reference="TRUE"/>
<object id="objSink" progid="WBemScripting.SwbemSink" events="TRUE" _ reference="TRUE"/>
<object id="objProcSink" progid="WBemScripting.SwbemSink" events="TRUE" _ reference="TRUE"/>
```

我们使用 *WbemScripting.SWbemLocator* 对象，以便可以指定备用凭据。请注意，我们可以通过实例化 *WbemScripting.SWbemSink* 对象在这里定义接收器对象。您不需要将下划线字符作为对象 ID 的一部分，但 *OnObjectReady* 子程序应包含它。

```
Sub OBJPROCSINK_OnObjectReady(objEvent,objContext)
'检测到触发器以终止此脚本
  blnLoop=False
End Sub
```

验证参数并定义变量后，我们定义查询。第一个查询是主要查询，用于监视新事件。

```
strQuery="Select * from __InstanceCreationEvent WITHIN " & iPoll &_
" where TargetInstance ISA 'win32_NTLogEvent' AND " &_
"TargetInstance.Logfile='" & strLog & "' AND " &_
"TargetInstance.Type='" & strType & "'"
```

第二个查询监视触发进程 `charmap.exe` 的创建，该进程将终止脚本。

```
'每 10 秒检查 charmap.exe 进程是否存在
strProcQuery="Select * from __InstanceCreationEvent WITHIN 10 WHERE " &_
"TargetInstance ISA 'win32_Process' AND " &_
"TargetInstance.Name='charmap.exe'"
```



要让此查询工作，我们需要连接到本地机器并建立异步查询。

```
'每隔10秒检查charmap.exe进程是否存在
strProcQuery="Select * from __InstanceCreationEvent WITHIN 10 WHERE " & _
"TargetInstance ISA 'Win32_Process' AND " & _
"TargetInstance.Name='charmap.exe'"
```

你应该已经知道如何打开文本文件并读取行，所以我们不再回顾这段代码。每个计算机名都会被读取并传递给Ping函数以验证网络连接。如果计算机"可Ping通"，我们就可以创建接收器。

如果用户指定了安全日志，我们需要向定位器对象添加安全权限。

```
    If UCase(strLog)="SECURITY" Then
        objLocator.Security_.Privileges.AddAsString "SeSecurityPrivilege",True
    End If
```

脚本连接到远程服务器，将WMI身份验证级别设置为数据包隐私，并执行异步通知查询。为清晰起见，我们已突出显示了这些行。

```
set objWMI=objLocator.ConnectServer(strComputer, "root\cimv2",_
strUser,strPassword)
If Err.Number<>0 Then
    WScript.Echo "Failed to connect to " & UCase(strComputer) & _
    " [Error #" & Hex(Err.Number) &" " & err.Description & "]"
    End If
Err.Clear
objWMI.Security_.authenticationLevel = wbemAuthenticationLevelPktPrivacy
WScript.Echo "Connecting sink to " & strComputer
Err.clear
objWMI.ExecNotificationQueryAsync objSink, strQuery
    If Err.Number<>0 Then
    WScript.Echo "Asynch Query failed To " & UCase(strComputer) & _
    " [Error #" & Hex(Err.Number) & " " & err.Description & "]"
    End If
```

> **最佳实践** 我们在脚本的关键点包含了错误处理。当出现问题时，向用户提供反馈非常重要。

尽管我们是从命令行运行脚本，但拥有一个图形事件查看器会很方便。我们可以通过创建Internet Explorer的新实例、导航到空白页面，然后插入HTML文本来实现这一点。

```
strTitle="Monitoring"
ie.width=630
ie.height=530
ie.top=10
ie.left=10
ie.menubar=False
ie.statusbar=False
ie.resizable=True
ie.toolbar=False
ie.navigate ("About:blank")
ie.document.title=strTitle
```

```
do while ie.ReadyState<>4
Loop
ie.visible=True
```

```
ie.document.body.innerHTML="<font face=Tahoma Size=1 Color=Blue>" &_
strQuery & "</font><br><HR"
```

现在，脚本在运行时每十秒检查一次charmap.exe是否正在运行。如果是，那么相应的接收器中的代码（稍后解释）将执行。为了保持脚本存活，我们有一个简单的循环。

```
wscript.echo "Monitoring...launch CHARMAP.EXE to end."
blnLoop=True
'检查触发进程是否已运行，每5秒休眠一次。
while blnLoop
    wscript.sleep 5
wend
```

当事件触发时，*objSink_OnObjectReady* 子例程被调用。此子例程中的代码获取返回对象的属性并创建一个消息字符串。然后，此字符串被包含在HTML代码中并插入到Internet Explorer窗口中。

```
' _____________________________________________________
'回调子例程
'这是当我们从异步调用获得返回时发生的代码
' _____________________________________________________
Sub objSINK_OnObjectReady(NTEvent,refContext)
On Error Resume Next

'定义背景颜色变量以进行交替
if blnFLAG then
    strColor="#FFFFFF"
    blnFlag=False
Else
    strColor="#CCFF66"
    blnFlag=True
End If

logtime=NTEvent.TargetInstance.TimeGenerated
logyr = Left(logtime,4)
logmo = Mid(logtime,5,2)
logdy = Mid(logtime,7,2)
logtm = Mid(logtime,9,6)

strMsg=NTEvent.TargetInstance.ComputerName & "  Event ID: " &_
    NTEvent.TargetInstance.EventCode & _
"    Source: " & NTEvent.TargetInstance.SourceName & vbTab & logmo & _
"/" & logdy & "/" & logyr & " [" & FormatDateTime(left(logtm,2) &
":"&Mid(logtm,3,2) & ":"&Right(logtm,2),3) & "]" & vbcrlf & _
NTEvent.TargetInstance.message
'如果您愿意，可以使用弹出窗口
' wshShell.Popup strMsg,45,NTEvent.TargetInstance.ComputerName & _
' " Event Log Alert",vbOKOnly

ie.document.body.InsertAdjacentHTML "beforeEnd","<Table border=0 " & _
"Cellpadding=0 cellspacing=2><TR><TD BGCOLOR=" & strColor & _
"><font face=tahoma size=1>" & strMsg & "</TD><TR>"
End Sub
```

第三部分：高级脚本技术、工具和技术

每个条目都编写为一个包含一列和一行的HTML表格。我们添加了一些代码，使表格颜色交替，以便于阅读。图11-21展示了此脚本的结果。

![图11-21 清单11-4中脚本的示例HTML输出](img/4fefd6988ba5d4a92a65127617ca24c2_335_0.png)

要终止脚本，我们启动字符映射表。该进程将被检测到，相应的接收器中的代码将被执行。

```
Sub OBJPROCSINK_OnObjectReady(objEvent,objContext)
'已检测到触发器以关闭此脚本
  blnLoop=False
End Sub
```

在这种情况下，*blnLoop* 变量被设置为FALSE，这将停止 *While* 循环。然后，我们取消并断开接收器，并关闭Internet Explorer。

```
while blnLoop
  wscript.sleep 5
wend

WScript.Echo "Cancelling and disconnecting sink"
objSink.Cancel
objProcSink.cancel
wscript.DisconnectObject(objSINK)
wscript.DisconnectObject(objPROCSINK)

ie.Quit
wScript.Quit
```

EventAlert.wsf脚本结合了我们在本章中涵盖的几乎所有内容。我们有多个异步查询和接收器、一个用于结束脚本的触发器应用程序，以及一个图形事件查看器。

> **注意** 我们经常被问及将脚本作为服务运行的问题，正如你可能想要做的那样。我们不建议这样做。首先，脚本不能包含任何用户交互或反馈，例如消息框甚至wscript.echo命令，因为没有用户可以交互。其次，如果在运行时出现问题，脚本的恢复能力非常有限。然而，我们涵盖的关于WMI事件的几乎所有内容都可以用于在更高级的编程语言（如Microsoft Visual Basic .NET）中开发编译应用程序，在该语言中创建可以作为服务运行的应用程序要容易得多。

你可能希望使用我们一直在讨论的WMI脚本作为监控和管理工具，在桌面上交互式运行。根据你的需求，你可能会发现拥有一个专用的XP桌面用于监控和管理，并使用管理员凭据登录是有益的。只要确保它在物理上是安全的即可。

![图11-22](img/4fefd6988ba5d4a92a65127617ca24c2_336_0.png)

### 总结

WMI事件可以产生强大的结果。我们向你展示了如何筛选或查询不同类型的WMI事件。我们还向你展示了如何使用VBScript、WMI工具和WBEMTest设置事件通知。花些时间使用这些工具，使用CD上的示例脚本，亲自看看哪些信息可以用于你的服务器和桌面。

> **更多信息** 有关WMI事件的更多信息，我们推荐Matthew Lavy和Ashley Meggitt所著的*Windows Management Instrumentation*（New Riders 2002）。有关WMI事件的在线信息，请访问以下网站。

http://msdn.microsoft.com/library/default.asp?url=/library/en-us/wmisdk/wmi/receiving_a_wmi_event.asp

（此链接在附带的CD上；点击*接收WMI事件*。）

# 第12章
使用WMI工具改进脚本

**本章内容：**
将工具用作脚本捷径 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 319
使用Scriptomatic . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 320
使用WMIC . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 325
使用WBEMTest . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 341
使用WMI工具 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 343
比较WMI向导 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 349
总结 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 351

有许多免费可用的工具，如WBEMTest和Scriptomatic，可以大大减少开发管理脚本所需的时间。我们将讨论如何使用各种Windows管理规范（WMI）相关工具来提高你的脚本编写效率。

大多数管理员总是时间紧迫，在午餐前有十几件事情要完成。即使对管理脚本的需求很高，花时间开发脚本通常也是低优先级。幸运的是，通过一些好的工具，开发脚本（即使是复杂的WMI脚本）所需的时间可以显著减少。你甚至可能发现这些应用程序可以成为有价值的诊断和故障排除工具。

## 将工具用作脚本捷径

本章涵盖的工具和实用程序可以通过以下方式减少创建管理脚本所需的时间：

-   你可以生成可以原样使用或用作脚本基础的VBScript代码。
-   你可以了解WMI类、对象和属性，以快速识别脚本所需的信息。
-   你可以测试和调试WMI查询。在你知道查询有效后，将其插入脚本中就很简单了。
-   你可以测试替代凭据和权限。如果你怀疑脚本中存在权限或权限问题，可以使用其中一些工具来验证脚本的安全上下文。



### 使用 Scriptomatic

最受欢迎的脚本工具之一是 Scriptomatic，它由 Microsoft Scripting Guys 免费提供。使用此工具，你可以执行以下操作：

-   浏览 WMI 命名空间
-   浏览 WMI 类
-   连接到远程系统
-   以 VBScript 和其他脚本语言生成脚本代码
-   选择脚本输出的格式
-   保存生成的脚本

即使你的脚本能力有限，只了解 WMI 的基础知识，你也可以在几秒钟内使用 Scriptomatic 创建功能完备的管理脚本。如果你是一位经验丰富的脚本开发人员，Scriptomatic 生成的代码可以作为你自己脚本开发的基础。复制和粘贴代码可以节省时间并减少拼写错误。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_339_0.png)

> **注意** 如果你没有 Scriptomatic 工具，请从 Microsoft 网站下载，地址为
> http://www.microsoft.com/downloads/details.aspx?FamilyID=09dfc342-648b-4119-b7eb-783b0f7d1178&DisplayLang=en
> （此链接位于附带的 CD 上；单击 Scriptomatic v2.0。）

#### 列出类和命名空间

Scriptomatic 的主要功能是枚举 WMI 命名空间和类。找到你想要的 WMI 类后，Scriptomatic 将基于该类生成一个脚本。启动 Scriptomatic 时，它会连接到默认的 WMI 命名空间 `root\cimv2`，如图 12-1 所示。

如图 12-2 所示，当你单击 WMI Class 下拉箭头时，将显示此命名空间中所有可用的对象类。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_340_0.png)

图 12-1 启动 Scriptomatic

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_340_1.png)

图 12-2 显示 WMI 类

你也可以通过单击 WMI Namespace 下拉箭头连接到其他 WMI 命名空间，如下一页的图 12-3 所示。根据系统的不同，你可能会看到列出的其他命名空间。例如，Microsoft Exchange 2003 将具有 `root\MicrosoftExchangeV2` 命名空间。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_341_0.png)

图 12-3 列出 WMI 命名空间

对于大多数管理员来说，`root\cimv2` 中的 Win32 对象是最令人感兴趣的。在图 12-4 中，已在 WMI Class 下拉列表中选择了 `Win32_OperatingSystem` 类，并自动生成了脚本。Scriptomatic 将生成多种编程语言的代码。我们使用了默认的 VBScript。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_341_1.png)

图 12-4 显示 Win32_OperatingSystem 脚本

第 12 章：使用 WMI 工具编写更好的脚本 323

Scriptomatic 还包括处理脚本输出的选项，这本质上是枚举特定类对象所有实例的所有属性和值。选择 Plain Text 选项会将脚本输出发送到一个文本文件，该文件会自动在记事本中打开，如图 12-5 所示。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_342_0.png)

图 12-5 在记事本中显示 Win32_OperatingSystem 脚本

以 HTML 格式输出如图 12-6 所示。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_342_1.png)

图 12-6 在 HTML 中显示 Win32_OperatingSystem 脚本

> **注意** WMI Source 按钮用于连接到远程系统。连接到远程系统后，你可以枚举远程计算机上所有的 WMI 命名空间和对象。这对于探索未在本地安装的 WMI 类非常有用。例如，Exchange 2003 有许多 WMI 类。通过连接到 Exchange 2003 服务器，你可以探索这些类，而无需在本地安装 Exchange 2003。但是，在 Scriptomatic v2.0 中，此功能存在一个错误。当你连接到远程系统时，生成的脚本中的计算机名会更改，但该工具仍然在查询本地 WMI 数据库。Microsoft Scripting Guys 已知此错误，并将在该工具的下一个版本中修复。

#### 生成脚本

当然，你仍然可以直接在工具内编辑脚本。Scriptomatic 的脚本实际上是枚举脚本。也就是说，它们报告指定 WMI 类的已定义属性。这种类型的报告可能构成了大多数管理脚本库的大部分内容。Scriptomatic 可以通过针对计算机列表运行脚本使此操作变得简单。

生成的脚本基本上是一个包装器，默认指向本地计算机。在工具界面的底部，有一个目标计算机窗格。你可以手动输入计算机名列表，然后单击“更新脚本”按钮，将这些名称添加到 `arrComputers` 定义的数组中。或者，如果你单击“从文件加载”按钮，可以指定一个包含你想要使用的所有计算机名的文本文件。目标计算机列表可以用逗号分隔，也可以是一个简单的列表，如图 12-7 所示。

![图片](img/4fefd6988ba5d4a92a65127617ca24c2_343_0.png)

#### 保存脚本

当你得到想要的脚本后，单击“保存”按钮。系统会提示你输入脚本的名称和位置。Scriptomatic 不会做的一件事是，在脚本从 Scriptomatic 本身运行时，添加它用于生成 HTML 页面或文本文件的格式化代码。保存的脚本与你在窗口中看到的完全相同。如果你想将输出保存为 HTML 页面、Microsoft Excel 工作簿或 XML 文件，你必须自己添加该代码。

Scriptomatic 可以创建一个功能完备的 WMI 脚本，在短短一分钟内查询多个远程系统。事实上，你可能会发现使用 Scriptomatic 来运行脚本并处理 HTML 等特殊格式更容易。你可以获取一个生成的脚本，添加计算机列表，并删除所有你不需要的 WMI 属性，或者添加一个 WMI 查询来限制返回的数据量。然后，你可以按照我们刚刚演示的方式保存脚本。当你准备好运行它时，启动 Scriptomatic 并单击“打开”。然后找到你的脚本，单击“确定”。使用 Scriptomatic 执行脚本并生成所需的输出。

### 使用 WMIC

如果你喜欢从命令提示符访问 WMI，那么 WMI 命令行 (WMIC) 就是适合你的工具。WMIC 不像 Scriptomatic 那样是脚本工具。实际上，Microsoft 设计 WMIC 是为了给那些想要利用 WMI 的强大功能而不必编写复杂 VBScript 代码的管理员使用。然而，由于这是一个命令行工具，你仍然可以使用传统的批处理文件对其进行脚本化。我们将在本章后面提供一个示例。

> **注意** WMIC 仅在 Microsoft Windows XP 和 Microsoft Windows Server 2003 上可用。但是，如果目标计算机上安装了 WMI 核心文件，你可以使用它远程连接到 Microsoft Windows 2000 甚至 Microsoft Windows NT 4.0 服务器。

你可以使用 WMIC 执行以下任务：

-   管理本地系统。
-   管理远程系统。
-   管理多个远程系统。
-   使用备用凭据。
-   格式化输出。

与 *NSLookup* 类似，你可以在交互模式或单命令模式下使用 WMIC。但是，在使用 WMIC 之前，必须先安装它。为此，请在命令提示符下键入 **WMIC**，然后按 Enter。WMIC 将在不到一分钟的时间内完成安装和配置，之后将出现 WMIC 命令提示符 **wmic:\root\cli>**。要从命令提示符窗口获取 WMI 帮助，请键入 **/?**。

##### 连接到命名空间

命名空间路径是相对于当前命名空间的。启动 WMIC 时，它会连接到默认的 WMI 命名空间，通常是 `root\cimv2`。但是，你可以通过键入 **/namespace:**<命名空间> 来连接到不同的命名空间。除非你扩展 WMIC（这是一个超出本书范围的主题），否则你可能不需要更改命名空间。我们预计默认配置能满足你 99% 的脚本需求。此外，如果你有扩展 WMIC 的技术专长，那么你很可能也有使用 VBScript 开发脚本的专长。

#### 使用别名

WMIC 初次使用时可能会令人困惑，因为它不使用标准的 *Win32* 类名。相反，WMIC 使用按功能（而非按类名）定义 WMI 类的*别名*。请记住，WMIC 是为可能不知道操作系统（`Win32_OperatingSystem`）的 WMI 类名，但能识别类似 `OS` 这样名称的管理员设计的。在命令提示符下键入 `WMIC /?` 会列出可用的别名。

-   *ALIAS* 访问本地系统上可用的别名
-   *BASEBOARD* 主板（也称为母板或系统板）管理
-   *BIOS* 基本输入/输出服务 (BIOS) 管理
-   *BOOTCONFIG* 启动配置管理
-   *CDROM* CD-ROM 管理
-   *COMPUTERSYSTEM* 计算机系统管理
-   *CPU* CPU 管理
-   *CSPRODUCT* 来自 SMBIOS 的计算机系统产品信息
-   *DATAFILE* 数据文件管理
-   *DCOMAPP* DCOM 应用程序管理
-   *DESKTOP* 用户桌面管理
-   *DESKTOPMONITOR* 桌面监视器管理
-   *DEVICEMEMORYADDRESS* 设备内存地址管理
-   *DISKDRIVE* 物理磁盘驱动器管理
-   *DISKQUOTA* NTFS 卷的磁盘空间使用情况
-   *DMACHANNEL* 直接内存访问 (DMA) 通道管理
-   *ENVIRONMENT* 系统环境设置管理
-   *FSDIR* 文件系统目录项管理
-   *GROUP* 组帐户管理



# 第三部分：高级脚本技术、工具与技术

-   IDECONTROLLER IDE 控制器管理
-   IRQ 中断请求线 (IRQ) 管理
-   JOB 访问使用计划服务计划的任务
-   LOADORDER 管理定义执行依赖关系的系统服务
-   LOGICALDISK 本地存储设备管理
-   LOGON 登录会话
-   MEMCACHE 缓存内存管理
-   MEMLOGICAL 系统内存管理（配置布局和内存可用性）
-   MEMPHYSICAL 计算机系统的物理内存管理
-   NETCLIENT 网络客户端管理
-   NETLOGIN 网络登录信息（特定用户）管理
-   NETPROTOCOL 协议（及其网络特性）管理
-   NETUSE 活动网络连接管理
-   NIC 网络接口控制器 (NIC) 管理
-   NICCONFIG 网络适配器管理
-   NTDOMAIN NT 域管理
-   NTEVENT NT 事件日志中的条目
-   NTEVENTLOG NT 事件日志文件管理
-   ONBOARDDEVICE 管理内置于主板（系统板）的通用适配器设备
-   OS 已安装操作系统管理
-   PAGEFILE 虚拟内存文件交换管理
-   PAGEFILESET 页面文件设置管理
-   PARTITION 物理磁盘分区区域管理
-   PORT I/O 端口管理
-   PORTCONNECTOR 物理连接端口管理
-   PRINTER 打印机设备管理
-   PRINTERCONFIG 打印机设备配置管理
-   PRINTJOB 打印作业管理
-   PROCESS 进程管理
-   PRODUCT 安装包任务管理
-   QFE 快速修复工程
-   QUOTASETTING 卷上磁盘配额的设置信息
-   RECOVEROS 操作系统故障时从内存中收集的信息
-   REGISTRY 计算机系统注册表管理
-   SCSI CONTROLLER SCSI 控制器管理
-   SERVER 服务器信息管理
-   SERVICE 服务应用程序管理
-   SHARE 共享资源管理
-   SOFTWAREELEMENT 管理系统上安装的软件产品的元素
-   SOFTWAREFEATURE 管理 SOFTWAREELEMENT 的软件产品子集
-   SOUNDDEV 声音设备管理
-   STARTUP 管理用户登录计算机系统时自动运行的命令
-   SYSACCOUNT 系统账户管理
-   SYSDRIVER 管理基础服务的系统驱动程序
-   SYSTEMENCLOSURE 物理系统机箱管理
-   SYSTEMSLOT 管理物理连接点，包括端口、插槽和外围设备，以及专有连接点
-   TAPEDRIVE 磁带驱动器管理
-   TEMPERATURE 温度传感器（电子温度计）数据管理
-   TIMEZONE 时区数据管理
-   UPS 不间断电源 (UPS) 管理
-   USERACCOUNT 用户账户管理
-   VOLTAGE 电压传感器（电子电压表）数据管理
-   VOLUMEQUOTASETTING 将磁盘配额设置与特定磁盘卷关联
-   WMISET WMI 服务操作参数管理

具有讽刺意味的是，经验丰富的 WMI 用户更容易被这些别名搞混，因为并非总是清楚别名指的是哪个 Win32 类。表 12-1 列出了每个别名及其对应的 Win32 对象类目标。

##### 表 12-1 别名与目标类

| 别名 | 位置 | 目标类 |
| :--- | :--- | :--- |
| Alias | WHERE FriendlyName = '#' | Select * from Msft_CliAlias |
| BaseBoard | | Select * from Win32_BaseBoard |
| BIOS | | Select * from Win32_BIOS |
| BootConfig | | Select * from Win32_BootConfiguration |
| CDROM | WHERE Drive='#' | Select * from Win32_CDRomDrive |
| ComputerSystem | | Select * from Win32_ComputerSystem |
| CPU | WHERE DeviceID='#' | Select * from WIN32_Processor |
| CSProduct | | Select * from Win32_ComputerSystemProduct |
| DataFile | WHERE Name = '#' | Select * from CIM_DataFile |
| DCOMAPP | WHERE Name='#' | Select * from WIN32_DCOMApplication |
| Desktop | WHERE Name='#' | Select * from WIN32_Desktop |
| DesktopMonitor | WHERE DEVICEID='#' | Select * from WIN32_DesktoPmonitor |
| DeviceMemoryAddress | | Select * from Win32_DeviceMemoryAddress |
| DiskDrive | WHERE Index=# | Select * from Win32_DiskDrive |
| DiskQuota | | Select * from Win32_DiskQuota |
| DMAChannel | WHERE DMAChannel=# | Select * from Win32_DMAChannel |
| Environment | | Select * from Win32_Environment |
| FSDir | WHERE Name='#' | Select * from Win32_Directory |
| Group | | Select * from Win32_Group |
| IDEController | | Select * from Win32_IDEController |
| IRQ | WHERE IRQNumber=# | Select * from Win32_IRQResource |
| Job | WHERE jobid=# | Select * from Win32_ScheduledJob |
| LoadOrder | | Select * from Win32_LoadOrderGroup |
| LogicalDisk | WHERE Name='#' | Select * from Win32_LogicalDisk |
| LOGON | | Select * from Win32_LogonSession |
| Memcache | WHERE DeviceID='#' | Select * from WIN32_Cachememory |
| MemLogical | | Select * from Win32_LogicalMemoryConfiguration |
| MemPhysical | | Select * from Win32_PhysicalMemoryArray |
| NetClient | WHERE Name='#' | Select * from WIN32_NetworkClient |
| NetLogin | WHERE Name='#' | Select * from Win32_NetworkLoginProfile |
| NetProtocol | | Select * from Win32_NetworkProtocol |
| NetUse | WHERE LocalName='#' | Select * from Win32_NetworkConnection |
| NIC | WHERE DeviceID=# | Select * from Win32_NetworkAdapter |
| NICConfig | WHERE Index=# | Select * from Win32_NetworkAdapterConfiguration |
| NTDomain | WHERE DomainName='#' | Select * from Win32_NTDomain |
| NTEvent | | Select * from Win32_NTLogEvent |
| NTEventLog | WHERE LogfileName='#' | Select * from Win32_NTEventlogFile |
| OnBoardDevice | | Select * from Win32_OnBoardDevice |
| OS | | Select * from Win32_OperatingSystem |
| PageFile | | Select * from Win32_PageFileUsage |
| PageFileSet | | Select * from Win32_PageFileSetting |
| Partition | WHERE Index=# | Select * from Win32_DiskPartition |
| Port | | Select * from Win32_PortResource |
| PortConnector | WHERE ExternalReferenceDesignator='#' | Select * from Win32_PortConnector |
| Printer | WHERE Name='#' | Select * from Win32_Printer |
| PrinterConfig | WHERE Name='#' | Select * from Win32_PrinterConfiguration |
| PrintJob | WHERE JobId=# | Select * from Win32_PrintJob |
| Process | WHERE ProcessId='#' | Select * from Win32_Process |
| Product | WHERE Name='#' | Select * from Win32_Product |
| QFE | | Select * from Win32_QuickFixEngineering |
| QuotaSetting | | Select * from Win32_QuotaSetting |
| RecoverOS | | Select * from Win32_OSRecoveryConfiguration |
| Registry | | Select * from Win32_Registry |
| SCSIController | | Select * from Win32_SCSIController |
| Server | | Select * from Win32_PerfRawData_PerfNet_Server |
| Service | WHERE Name='#' | Select * from Win32_Service |
| Share | WHERE Name='#' | Select * from Win32_Share |
| SoftwareElement | | Select * from Win32_SoftwareElement |
| SoftwareFeature | | Select * from Win32_SoftwareFeature |
| SoundDev | WHERE Name='#' | Select * from WIN32_SoundDevice |
| Startup | WHERE Caption='#' | Select * from Win32_StartupCommand |
| SysAccount | WHERE Name='#' | Select * from Win32_SystemAccount |
| SysDriver | WHERE Name='#' | Select * from Win32_SystemDriver |
| SystemEnclosure | | Select * from Win32_SystemEnclosure |
| SystemSlot | | Select * from Win32_SystemSlot |
| TapeDrive | | Select * from Win32_TapeDrive |
| Temperature | | Select * from Win32_TemperatureProbe |
| TimeZone | | Select * from Win32_TimeZone |
| UPS | | Select * from Win32_UninterruptiblePowerSupply |
| UserAccount | | Select * from Win32_UserAccount |
| Voltage | | Select * from Win32_VoltageProbe |
| VolumeQuotaSetting | WHERE Element = # and Setting = # | Select * from Win32_VolumeQuotaSetting |
| WMISet | | Select * from Win32_WMISetting |

要获取有关特定别名的更多信息，请打开命令提示符窗口，然后键入 **wmic <别名> /?**。例如，键入 `wmic share /?` 将显示下一页所示的信息。



第三部分：高级脚本技术、工具和技术

SHARE - 共享资源管理。

提示：别名使用的 BNF 语法。
`(<别名> [WMIObject] | <别名> [<路径位置>] | [<别名>]
<路径位置>) [<动词子句>]。`

用法：

SHARE ASSOC [<格式说明符>]
SHARE CALL <方法名> [<实际参数列表>]
SHARE CREATE <赋值列表>
SHARE DELETE
SHARE GET [<属性列表>] [<获取开关>]
SHARE LIST [<列表格式>] [<列表开关>]

大多数 WMIC 命令遵循 `WMIC <连接选项> <别名> <别名选项> <WMC动词> <WMC动词选项>` 的模式。我们将在本章稍后更详细地介绍 WMIC 语法。

#### 连接到远程系统

你可以通过使用 `/node` 开关来使用 WMIC 连接到远程系统。如果你不指定节点，WMIC 默认为本地系统。你可以这样指定单台计算机。

```
wmic /node:Server03
```

你可以这样指定以逗号分隔的计算机列表。

```
wmic /node:Server03,App01,File02,Print01
```

在一个包含计算机名称的文本文件中，名称可以是逗号分隔的值，也可以是列式列表。

```
wmic /node:@servers.txt
```

WMIC 将针对列表中的每个系统处理你的查询。

#### 传递凭据

如果你想在连接到远程系统时使用其他凭据，可以使用 `/user` 和 `/password` 开关。用户名的值应采用 `域\用户` 的格式。你输入的密码值将被显示出来。没有密码提示的选项。将此功能与前面的示例结合使用将产生以下代码片段。

```
wmic /node:@servers.txt /user:"company\j-admin" /password:P@ssw0rd
```

请注意，我们将用户名放在引号中。如果任何开关的值包含特殊字符（如破折号或斜杠），则必须用引号括起来。如有疑问，请使用引号。

## 第 12 章：使用 WMI 工具进行更好的脚本编写 333

### 使用 *list* 和 *get* 进行查询

当然，WMIC 的全部目的是了解系统。这是通过使用动词 *list* 或 *get* 来实现的。这两个动词都返回指定别名的值，但它们返回的信息以及返回方式通常不同，具体取决于别名的定义方式。例如，这是 `wmic pagefile list` 命令的输出。

```
AllocatedBaseSize CurrentUsage Description InstallDate
Name PeakUsage Status TempPageFile
1535 223 C:\pagefile.sys 20050906105923.788062-240 C:\pagefile.sys 261
```

输出将有换行。这是 `wmic pagefile get` 命令的输出。

```
AllocatedBaseSize Caption CurrentUsage Description
InstallDate Name PeakUsage Status
TempPageFile 1535 C:\pagefile.sys 223
C:\pagefile.sys 20050906105923.788062-240 C:\pagefile.sys 261
```

WMIC 在两个命令中查看的是同一个对象，但呈现的信息略有不同。你使用 *get* 来指定要显示其值的属性。运行命令 `wmic os get caption, csdversion` 将返回以下结果。

```
Caption CSDVersion
Microsoft Windows XP Professional Service Pack 2
```

如果你想了解 *get* 命令将为给定别名返回哪些属性，请键入 **wmic <别名> get /?**。默认是返回所有属性值。

你可以通过键入 **wmic <别名> list /?** 来查找 *list* 命令的相同信息。结果会有所不同，具体取决于你指定的别名。例如，`wmic os list /?` 的帮助输出包括 *Brief*、*Full*、*Free* 等格式选项。输入 `wmic cpu list /?` 会显示 *Brief*、*Config*、*Full* 等格式选项。*get* 和 *list* 的主要区别在于，*get* 动词返回别名的所有属性，而 *list* 动词使用由名称定义的预定义属性列表，例如 *Brief*、*Full*、*Config*、*Free* 或其他适合该别名的名称。

你还可以在 WMIC 命令中使用 WMI *WHERE* 查询。只需将条件子句放在括号中。

```
wmic process where (name="spoolsv.exe") list brief
```

此命令将产生以下输出。

```
HandleCount Name Priority ProcessId ThreadCount WorkingSetSize
180 spoolsv.exe 8 1344 13 6262784
```

*get* 和 *list* 都有一个 `/every` 开关，它将按计划间隔运行查询。你指定的间隔以秒为单位。

```
wmic process where (name="spoolsv.exe") list brief /every:10
```

这将每 10 秒运行一次命令，并将输出显示在屏幕上。你可以按任意键结束命令。你也可以使用 `/repeat` 开关来执行命令，每 x 秒执行一次，执行指定的次数。

```
wmic process where (name="spoolsv.exe") list brief /every:10 /repeat:6
```

#### 格式化输出

如果你在阅读本章时一直在测试 WMIC，你可能已经注意到某些输出很难阅读。幸运的是，有几种选项可以生成更用户友好的输出或报告。如果你使用的是 get 动词，最简单的方法是在命令末尾添加 `/value`。

```
wmic os get /value
```

此命令将生成一个易于阅读的属性和值的列式列表。如果你只想显示某些值，请使用如下命令。

```
wmic os get caption,csdversion,version /value
```

此命令将产生以下类型的输出。

```
Caption=Microsoft Windows XP Professional
CSDVersion=Service Pack 2
version=5.1.2600
```

##### 将输出保存到命令提示符窗口

到目前为止我们运行的所有命令都隐式使用了另一个全局开关 `/output`。此开关决定如何处理输出。默认值是 StdOut，这意味着数据写入命令提示符窗口。如果我们想明确指定，可以这样使用命令。

```
wmic /output:stdout OS get /value
```

##### 将输出保存到剪贴板

还有其他一些格式化选择。请注意以下命令，它使用了 clipboard 值。

```
wmic /output:clipboard OS get /value
```

此命令指定不在屏幕上显示任何内容。但是，我们可以通过打开记事本并粘贴存储在剪贴板上的数据来查看操作的输出。

##### 将输出保存到文件

当然，如果你想省去一步，可以直接将输出发送到文件。你只需在命令中指定文件名即可。

```
wmic /output:"e:\logs\os audit\local.txt" OS get /value
```

显然，你需要将包含空格的任何文件路径用引号括起来。使用 `/output` 时，任何现有文件都将被覆盖。如果你想追加到现有文件，可以使用 `/append` 代替 `/output`。

```
wmic /append:"e:\logs\os audit\local.txt" OS get /value
```

##### 使用 XSL 文件

创建文件只是一半的故事。WMIC 包含许多转换文件（.xsl），你可以用来格式化输出。你可以在 `%SystemRoot%\System32\wbem` 找到这些文件。你可以使用 `/format` 开关指定其中一个文件，生成的输出将根据文件进行格式化。以下 XSL 文件最常用：

- **Textvaluelist** 创建属性及其值的列表。
- **Htable** 创建一个显示属性及其值的水平 HTML 表格。
- **Hform** 创建一个显示属性及其值的垂直 HTML 表格。
- **CSV** 创建一个以逗号分隔的属性及其值的列表。
- **RAWXML** 将输出格式化为 XML。在构建自己的 XSL 文件时，这非常有用，因为 WMIC 原生使用 XML 格式。

这些格式选项可与 list 或 get 一起使用。以下是一些你可能想尝试的示例。

```
wmic cpu list brief /format:textvaluelist
wmic /output:processreport.csv process list brief /format:csv
wmic /output:bios.xml bios get /format:rawxml
wmic /output:osinfo.html os list full /format:hform
wmic /output:test.html process list brief /format:htable
```

下一页的图 12-8 说明了最后一个命令的结果。



##### 创建你自己的 XSL 文件

这个主题超出了本书的范围，但如果你有任何 XML 和 XSL 经验，你可以创建自己的格式化文件。你也可以复制其中一个现有文件，然后根据你的需求进行自定义修改。无论如何，你创建或修改的 XSL 文件必须位于 `%Systemroot%\System32\wbem` 文件夹中。清单 12-1 是一个非常简单的 XSL 文件，我们将其作为演示示例。

```
清单 12-1 演示 XSL 文件
<?xml version="1.0"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:template match="/">
<html>
<body bgcolor="#FFFF99">
<img src="http://www.jdhitsolutions.com/images/JDHITSolutionsBtn.jpg" alt="logo"/>
<xsl:for-each select="COMMAND/REQUEST/COMMANDLINECOMPONENTS">
<h3>COMPUTER SYSTEM - <xsl:value-of select="NODELIST/NODE"/></h3>
<hr/>
<font color="BLUE"><xsl:value-of select="RESULTANTQUERY"/></font>
</xsl:for-each>
<br/><br/><br/>
<table border="1"><tr style="background-color:6666ff;font:10pt Tahoma;">
<xsl:for-each select="COMMAND/REQUEST/COMMANDLINECOMPONENTS/PROPERTIES/PROPERTY">
<th><xsl:value-of select="NAME"/></th>
</xsl:for-each>
</tr>
<xsl:for-each select="COMMAND/RESULTS/CIM/INSTANCE">
<tr style="font:8pt Tahoma;">
<xsl:for-each select="PROPERTY">
<td><xsl:value-of select="VALUE"/></td>
</xsl:for-each>
</tr>
</xsl:for-each>
</table>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

> **随书附赠** 你可以在本书附带的 CD 上找到这个脚本以及本章列出的其他脚本。

要使用此文件，请将其保存到 WBEM 文件夹，并命名为 `basichtml.xsl` 之类的名字。然后运行如下命令：

`wmic /output:computersystem.html OS list full /format:basichtml`

在浏览器中打开 `computersystem.html` 文件即可查看结果。

> **注意** 清单 12-1 中的 XSL 文件是为在单个节点上运行并使用 `list /brief` 的 WMIC 命令设计的。它尚未针对与其他 WMIC 命令和别名的格式兼容性进行充分测试。

### 使用 WMIC 进行脚本编写

由于 WMIC 是一个命令行工具，它可以被合并到批处理文件中。清单 12-2 是一个使用 WMIC 的批处理文件示例。

```
清单 12-2 批处理文件中的 WMIC
@echo off
::SysPeek.bat
::用法- syspeek [computer]

::描述- 为指定计算机建立系统资源使用情况的 HTML 页面。
::默认 HTML 文件名为 computernameInfo.htm，它在你运行脚本的同一目录中创建。如果你未指定
::计算机，脚本将默认为本地主机。

::收集的信息：
::    处理器
::    操作系统
::    页面文件
::    内存
::    逻辑驱动器
::    服务
::    进程

::重要说明- 此脚本使用仅在 Windows XP 和 2003 平台上可用的 WMI 命令行版本。在运行脚本之前，
::你必须安装 WMIC。打开命令提示符并键入 'WMIC'，这将启动安装。完成后，你将获得一个交互式
::提示符 (wmic:\root\cli>)。键入 'exit'。你现在可以运行此脚本。你查询的计算机不需要
::WMIC，但它必须启用 WMI。

::你必须在目标计算机上拥有适当的凭据。你可以指定替代凭据，但你需要使用 /USER 和
::/PASSWORD 全局开关。在命令提示符处运行 wmic /? 以查看帮助屏幕。

::如果你了解 XML，你可以构建自己的格式文件 (.xsl)。
::这些文件位于 %systemroot%\system32\wbem 中。

:Top
::用于输出的脚本版本
set zver=v2.0

if "%1"=="" goto :Local
set zSrv=%1
goto :Main

:Local
set zSrv=%computername%

:Main
echo 正在获取 "%zSrv%" 的系统资源信息

::定义 HTML 输出文件
set zOutput=%zSrv%-Info.htm

::如果文件已存在则删除
if exist %zOutput% del %zOutput% >NUL
::如果错误日志先前存在则删除
if exist %zSrv%-Error.log del %zSrv%-Error.log >NUL

::构建外壳 HTML 文件。非必需，但我想尝试一下。
echo ^<html^> >> %zOutput%
echo ^<body^> >> %zOutput%
echo ^<H3^>^<Font Face=Verdana Color=Blue^>^<P align=Center^>%zSrv%^<BR^>
>>%zOutput%
echo 系统资源信息^</Font^>^</H3^>^</P^> >> %zOutput%
echo ^<HR^> >> %zOutput%
echo ^</html^> >> %zOutput%
echo ^</body^> >> %zOutput%

::验证连接性和 WMI 兼容性
wmic /node:"%zSrv%" os list brief 1>NUL 2>> %zSrv%-Error.log
if errorlevel=0 goto :Gather
echo ^<Font Color=Red^>^<B^> 糟糕！！ ^</P^>^>^> %zOutPut%
echo 无法验证与 "%zSrv%" 的连接性或 WMI 兼容性 ^</P^>
>> %zOutPut%
for /f "tokens=*" %%i in (%zSrv%-Error.log) do @echo %%i ^<br^> ^>^>%zoutPut%
echo ^</Font^>^</B^> ^</P^> >> %zOutPut%
goto :cleanup

:Gather
::开始收集信息。WMIC 命令必须在一行内。
echo 操作系统...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>操作系统^</Font^>
^</H3^>^</B^>^</I^> >> %zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" OS get Caption,Version,
CSDVersion,installDate,LastBootUpTime,Status,windowsDirectory
/format:hform.xsl >NUL

echo 处理器...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>处理器^</Font^>
^</H3^>^</B^>^</I^> >> %zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" cpu get deviceID,name,
addresswidth,currentclockspeed,l2cachesize,loadpercentage
/format:htable.xsl >NUL

echo 内存...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>内存^</Font^>
^</H3^>^</B^>^</I^> >> %zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" memlogical get
AvailableVirtualMemory, TotalVirtualMemory, TotalPhysicalMemory,
TotalPageFileSpace /format:hform.xsl >NUL

echo 页面文件...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>页面文件^</Font^>
^</H3^>^</B^>^</I^> >> %zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" pagefileset get name, initialsize,
maximumsize /format:hform.xsl >NUL
wmic /node:"%zSrv%" /append:"%zOutPut%" pagefile get Caption,
CurrentUsage, PeakUsage, InstallDate /format:hform.xsl >NUL

echo 逻辑驱动器...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>驱动器
信息^</Font^>^</H3^>^</B^>^</I^> >> %zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" logicaldisk where drivetype=3 get
name, size, freespace, compressed, filesystem /format:htable.xsl >NUL

echo 进程...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>进程^</Font^>^</H3^>^</B^>^</I^> >>
%zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" process list brief
/format:"htable.xsl":"sortby=Name" >NUL

echo 服务...
echo ^<Font Color=Green^>^<H3^>^<B^>^<I^>服务^</Font^>
^</H3^>^</B^>^</I^> >> %zOutPut%
wmic /node:"%zSrv%" /append:"%zOutPut%" service where
startmode!="disabled" get pathname, state, startmode, displayname,
processid /format:"htable.xsl":"sortby=State" >NUL

:Cleanup
echo ^<I^>^<Font Size=-1^>^<BR^>%zver% >>%zOutput%
date /t >>%zOutput%
time /t >>%zOutput%
echo - %username% ^</I^>>>%zOutput%

echo 打开 %zOutPut% 以查看结果
Start %zOutPut%

if exist %zSrv%-Error.log del %zSrv%-Error.log >NUL

set zSrv=
set zOutput=
set zver=

::EOF
```

> **注意** 在这个批处理文件中，每个 *echo* 和 *wmic* 命令都在单独的一行上。出于代码清单的目的，某些行被分开了。CD 上的脚本文件格式正确。

此批处理文件构建一个包含有关单个计算机的 WMI 信息的 HTML 页面。你可以在运行时将计算机名指定为参数。如果未指定，脚本默认为本地系统。该脚本使用 /output 和 /append 开关来构建一个文件。然后它运行一系列 WMIC 命令，将结果附加到文件中。我们使用 `htable.xsl` 文件来格式化结果。图 12-9 让你对脚本的输出有个概念。

如你所见，无需编写一行 VBScript，你就可以使用 WMI 信息生成一个相当完整的系统报告。WMIC 的功能还有更多更多，我们将留待你自己去探索。

> **更多信息** 你可以通过在 Windows XP 桌面上的“帮助和支持中心”中搜索来了解更多关于 WMIC 的信息。在 Windows\Help 文件夹中还有一个帮助文件 `wmic.chm`。你也可以访问以下网站：

http://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/wmic.mspx

http://support.microsoft.com/kb/290216/EN-US/

（这些链接可在附带的 CD 上找到；分别点击 *WMIC Introduction* 和 *A Description of WMIC*。）

### 使用 WBEMTest

在第 11 章中，我们演示了如何使用 WBEMTest 来处理 WMI 事件通知。我们认为 WBEMTest 的主要目的是作为一个查询验证工具。如果你的 WMI 查询在 WBEMTest 中有效并返回了你期望的信息，那么它应该在你的脚本中也能工作。

##### 连接到命名空间

通过单击“开始”菜单，单击“运行”，然后在命令提示符窗口中键入 **wbemtest** 来启动 WBEMTest。你需要单击“连接”按钮来连接到一个命名空间。即使你可能倾向于接受默认值，如果你想使用 Win32 对象类，你必须将其更改为 **root\cimv2**。

> **提示** 如果你想连接到远程系统，请输入 `\\servername\root\cimv2`。

#### 启用特权

正如我们在第 11 章“WMI 事件”中解释的那样，要启用特权，例如，读取安全日志或关闭远程系统，你必须在单击“连接”按钮 *之前* 选中“启用所有特权”复选框。如果你在运行 WBEMTest 查询时遇到错误，你可能需要选中该复选框，然后重新连接。

#### 启用模拟

“连接”对话框包含一个指定模拟级别的选项。请记住，WMI 通过模拟用户并执行命令来工作。这意味着，没有适当的权限，用户无法访问任何系统资源或信息。你应该接受默认设置。



# 第三部分：高级脚本技术、工具与技术

#### 启用身份验证

身份验证级别指的是系统之间通信的处理方式。如果只连接到本地系统，可以接受默认设置，因为数据包不会离开计算机。否则，应选择适当的安全级别。其中，“数据包隐私”级别提供最高安全性。

> **更多信息** 有关身份验证级别（包括如何在 VBScript 中设置）的更多信息，请访问 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/wmisdk/wmi/setting_the_default_process_security_level_using_vbscript.asp。（此链接也位于随附光盘中；请点击 *WMI 身份验证级别*。）

#### 启用权限

如果指定了备用凭据，WMI 将使用 NTLM 进行用户身份验证。请不要将其与我们刚刚讨论的身份验证级别混淆。如果“权限”字段留空且需要输入备用凭据，请使用 `域\用户名` 的格式。如果要显式使用 NTLM，只需输入用户名即可。WMI 将假定运行 WBEMTest 的计算机与远程系统位于同一域中。

或者，可以使用 Kerberos，此时权限的格式为 `Kerberos:域\计算机名`。域名应为 Active Directory 域的完全限定名称，计算机名应为远程系统的名称。图 12-10 展示了使用备用凭据和 Kerberos 身份验证连接到远程系统 APP01 的 WBEMTest “连接”对话框。

![](img/4fefd6988ba5d4a92a65127617ca24c2_361_0.png)

图 12-10 使用 WBEMTest 连接到远程系统

#### 枚举实例

连接后，点击“查询”按钮，输入如 *Select * from win32\_physicalmemory* 的 WMI 查询，然后点击“应用”。WBEMTest 将执行查询并返回所有实例的列表。双击某个实例可打开对象编辑器窗口，显示该实例的所有对象属性和值。这验证了查询语法的正确性，并展示了可用的信息类型。你可能需要优化查询，例如 *Select DeviceLocator,Capacity,Speed from win32\_physicalmemory*，然后在 WBEMTest 中运行以验证 WMI 属性名称是否正确。

> **提示** 查看对象属性时，选中“隐藏系统属性”复选框。这将隐藏类和系统属性，仅显示对象属性。

随着你开始编写更复杂的 WMI 查询和脚本，你会发现 WBEMTest 是管理脚本开发中的宝贵工具。

> **提示** 某些查询（如 *Select DeviceLocator,Capacity,Speed from win32\_physicalmemory*）会返回类似 *Win32\_PhysicalMemory=<no key>* 的结果。双击实例时，对象编辑器窗口仍然会打开。此类结果仅反映查询未包含键索引属性。缺少键索引不会影响查询或结果。

### 使用 WMI 工具

我们在第 11 章讨论了事件查看器和注册工具，因此在本章中，我们将简要介绍另外两个 WMI 工具：CIM Studio 和 WMI 对象浏览器。

#### 使用 CIM Studio

CIM Studio 是一个包含 ActiveX 组件的网页，允许你查看 CIM 存储库中及关于该存储库的信息。所有 WMI 信息都存储或生成于此。你必须在 Internet Explorer 中打开 CIM Studio，如果运行的是 Windows XP Service Pack 2，则需允许阻止的内容。

##### 连接到命名空间

首次启动 CIM Studio 时，系统会提示你输入命名空间。除非你正在处理特殊的 WMI 命名空间（例如 Exchange 2003 的命名空间），否则应接受默认值 `root\cimv2`，如图 12-11 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_363_0.png)

图 12-11 连接到命名空间

如果要连接到不同的命名空间，请点击连接对话框中命名空间字段旁的计算机图标。确保 `root` 作为起始命名空间输入，然后点击“连接”。“浏览命名空间”对话框将出现，如图 12-12 所示。

![](img/4fefd6988ba5d4a9a65127617ca24c2_363_1.png)

图 12-12 浏览命名空间

双击命名空间即可连接到该命名空间。

##### 连接到远程计算机

我们通常使用 CIM Studio 来处理本地 CIM 存储库。你也可以连接到远程机器并查看其 CIM 存储库和 WMI 对象。浏览命名空间时，可以输入远程计算机名称。CIM Studio 默认为本地系统。

##### 使用备用凭据

如果指定了远程系统，可以选择使用备用凭据。点击 **“连接”** 后，请清除“以当前用户身份登录”复选框。

> **注意** 连接到本地系统时，“以当前用户身份登录”复选框呈灰色不可用状态，因为你不能为本地系统指定备用凭据，而 CIM Studio 足够智能，不会让你尝试。WBEMTest 允许你为本地连接输入备用凭据，但在尝试连接时会给出错误提示。

如果要指定其他连接属性（如身份验证级别、权限和特权），请点击“选项”按钮。然后按照我们之前为 WBEMTest 概述的相同指南操作。如果连接成功，将显示一个类似图 12-13 的页面。

![](img/4fefd6988ba5d4a92a65127617ca24c2_364_0.png)

##### 搜索类

点击或展开左窗格中的元素，可在右窗格中显示其类、属性、方法和关联。要搜索 WMI 类，请点击左窗格顶部的望远镜按钮。在“搜索类”对话框中，无需输入完整的类名。图 12-14 显示了搜索名称中包含“display”一词的所有类的返回结果。

![](img/4fefd6988ba5d4a92a65127617ca24c2_364_1.png)

点击所需的类，然后点击“确定”。CIM Studio 页面将重新显示，并高亮显示所选类。与往常一样，右窗格显示该类的属性、方法和关联。

##### 返回实例

现在你已经知道可以帮助你开发脚本的属性名称，可能还想知道在你连接的计算机上存在该类的哪些实例。要返回特定类的所有实例，请点击右窗格中磁盘按钮右侧的“实例”按钮。将鼠标指针悬停在按钮上时，会出现屏幕提示，告知你每个按钮的名称。

点击“实例”按钮后，所连接计算机上存在的该类所有实例将列在右窗格中。双击某个实例可显示填充了值的实例，如图 12-15 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_365_0.png)

**图 12-15 返回实例**

点击右窗格中的“关联”选项卡，可查看关联类之间的关系。双击其中一个连接图，可在 CIM Studio 中显示该类实例。

##### 运行查询

CIM Studio 还包含 WMI 查询功能。要运行查询，请点击问号按钮左侧的 WQL（WMI 查询语言）按钮。在“查询”对话框的“查询”窗格中输入任何类型的 WMI 查询，就像在 WBEMTest 中一样。点击“执行”按钮运行查询。如果找到任何实例，请双击以查看详细信息。CIM Studio 的一个优势是可以保存查询。

#### 使用 WMI 对象浏览器

CIM Studio 用于浏览 WMI 类，尽管你也可以用它返回指定计算机上的类实例。为简化此过程并探索计算机上的所有 WMI 对象，请使用 WMI 对象浏览器。

连接本地和远程系统以及更改命名空间的方式与在 CIM Studio 中相同。当你使用 WMI 对象浏览器连接到本地计算机的默认命名空间时，将显示一个类似图 12-16 的页面。

![](img/4fefd6988ba5d4a92a65127617ca24c2_366_0.png)

**图 12-16 启动 WMI 对象浏览器**

请注意，无需查找实例；它们会立即显示。如果展开左窗格中的树，你将看到所有 WMI 组件，可以进一步展开以查看底层的 WMI 对象。

例如，展开 *Win32_SystemServices.PartComponent* 以显示 *Win32_Service*。当你尝试展开 *Win32_Service* 时，将启动 WMI 查询以返回所选类的所有实例，如图 12-17 所示。



# 第13章
## Windows XP 和 Windows Server 2003 中的高级脚本编写

**本章内容：**

- 使用新的和已弃用的 WMI 类 …………………355
- 使用 *Win32_PingStatus* 类 ……………………356
- 配置 Windows 防火墙 ………………………359
- 使用磁盘配额管理 …………………………364
- 使用 DNS 提供程序 ………………………………365
- 使用 Active Directory 复制和信任 …………371
- 使用 Internet Information Services 6.0 …………………374
- 管理打印.……………………………………381
- 使用 Windows 更新服务.……………………385
- 总结.……………………………………………389

Microsoft Windows XP 和 Microsoft Windows Server 2003 引入了大量新的管理功能，特别是通过新的 WMI 类。我们将探讨其中一些最有用的类，并向您展示一些可以使管理任务更快、更简单的示例脚本。

Microsoft Windows 2000 引发了对 Windows 管理脚本编写的巨大兴趣。它是第一个包含 Windows 管理规范 (WMI) 的 Windows 版本，这为 VBScript 等脚本语言创造了巨大的新能力。微软对管理员们新发现的脚本编写热情做出了回应，在 Windows XP 和 Windows Server 2003 中包含了更多的功能。

> **注意** 我们将在本章中介绍的一些主题——例如 Active Directory 和 Internet Information Services 脚本编写——它们本身的内容就足以轻松填满一本书。我们并非试图在此提供全面的介绍；相反，我们只是向您展示可用的内容。

需要注意的是，本章中的脚本并非都是完整的管理脚本。事实上，大多数脚本都尽可能简短，以尽可能清晰地展示这些功能的工作原理。然而，本章中的大多数脚本可以通过将它们放入一个包装器中而轻松变得更加实用。例如，清单 13-1 展示了一个从文本文件中读取计算机名称的包装器脚本。

```
清单 13-1 从文件中读取名称
'创建一个 FileSystemObject
Set oFS = _
    CreateObject("Scripting.FileSystemObject")

'打开一个包含计算机名称的文本文件
'每行一个计算机名称
Set oTS = oFS.OpenTextFile("c:\computers.txt")
Set oTSOut = oFS.CreateTextFile("c:\errors.txt")

'遍历文本文件
Do Until oTS.AtEndOfStream
    '获取下一台计算机
    sComputer = oTS.ReadLine

    On Error Resume Next
    '***建立连接***
    If Err <> 0 Then
        oTSOut.WriteLine "Error on " & sComputer & _
            ":" & Err.Number & ", " & Err.Description
    Else
        On Error Goto 0
        '***其余代码在此处
    End If
Loop

oTS.Close
oTSOut.Close
```

> **随书附带的 CD** 您可以在本书附带的 CD 上找到此脚本以及本章中列出的其他脚本。

您需要将您的代码插入到 *其余代码在此处* 占位符的位置。这个包装器可以将一个查询单个 DNS 服务器 A 记录的基本脚本，例如，转变为一个完整的清单脚本，用于记录所有 DNS 服务器中的记录。我们将在本章后面的示例中使用这个包装器。您还可以结合一个包装器来从 Active Directory 读取计算机名称，然后针对每台计算机执行一些脚本化的管理任务。清单 13-2 就是这样做的。

### 第 348 页 第 III 部分：高级脚本技术、工具和技术

与 CIM Studio 类似，您可以在右窗格中双击一个实例，以显示该特定实例的 WMI 属性。单击左窗格顶部的双筒望远镜按钮，可以浏览其他类的实例。图 12-18 显示了搜索 Win32_Processor 的结果。

WMI 对象浏览器是一个优秀的工具，可以帮助您了解 WMI 的所有不同元素和组件如何协同工作。请记住，仅仅因为一个类被列出，并不意味着您的计算机上存在该类的实例。出现 *No Instances Available* 的消息并不罕见。

### 比较 WMI 向导

一些商业脚本编辑器包含一个 WMI 向导，以帮助加快代码开发。即使 WMI 经验很少，这些向导也可以帮助您生成功能完备的脚本，就像 Scriptomatic 一样。让我们来看看 iTripoli 的 AdminScriptEditor 和 Sapien 的 PrimalScript 中的 WMI 向导。我们无意评判哪个产品更好，只是演示这些功能并指出一些差异。

AdminScriptEditor 的 WMI 向导位于应用程序的右窗格中。要使用该向导，首先创建一个空白的 VBScript 文件。WMI 向导允许您浏览本地计算机上所有可用的 Win32 类。似乎没有连接到远程系统的方法，也没有连接到 root\cimv2 之外的任何命名空间的方法。当您选择一个类时，相应的属性会显示在面板的中间。图 12-19 显示了 WMI 向导及其生成的代码。

通过选择左窗格中相应的复选框，指定您希望报告的属性。当您选择一个属性时，AdminScriptEditor 会显示一个示例值。如果您想了解有关特定类的更多信息，单击 WMI 帮助按钮将启动您的 Web 浏览器并加载有关所选类的 MSDN WMI 页面。

该向导使用 *winmgmt* 标记和一个 *select* 查询。如果您想要更具选择性的查询，请清除“始终使用通配符”复选框。通常，生成的代码将回显 WMI 属性及其值，但如果您只需要值，请清除“描述属性”复选框。

在“条件”选项卡上，您可以基于所选属性为查询构建条件 *WHERE* 子句。您无需键入太多内容，只需选择属性和一个运算符，然后输入您的约束条件。图 12-20 使用 *Win32_Process* 类对此进行了说明。您也可以在左窗格中看到完成的脚本。

**图 12-20** 创建条件子句

当您对选择满意时，单击“输出”选项卡上的“显示”按钮以显示代码预览。单击“插入”将生成您的脚本，您可以直接运行它，或者进一步修改。

您可以使用 AdminScriptEditor WMI 向导来生成一些非常特定的 WMI 代码，尽管它不支持远程系统或远程凭据。您可以轻松地修改代码以连接到远程系统，但添加备用凭据需要进行重大修改。

PrimalScript 对他们的 WMI 向导采用了略有不同的方法。您可以从“脚本”菜单访问该向导。与 AdminScriptEditor 一样，该向导默认为本地 root\cimv2 命名空间中的 Win32 类。但是，您可以在 WMI 向导的底部指定服务器名称或不同的命名空间。还有输入备用用户名和密码的选项。

选择一个类将生成一个脚本，该脚本枚举该类的所有属性。您可以指定是要使用 JScript 还是 VBScript。您会注意到 PrimalScript 使用 WbemScripting.SWbemLocator 对象而不是 winmgmt 标记。这不仅允许使用备用凭据，还为该对象提供了 PrimalSense 支持，这是 Sapien 版本的 Intellisense。图 12-21 显示了 PrimalScript WMI 向导及其为 Win32_DiskPartition 类生成的代码。

您可以在向导中进行简单的脚本编辑，例如删除或添加行注释。单击“复制”按钮将脚本复制到剪贴板，或者如果您在 PrimalScript 中打开了文件，可以使用“插入”按钮将代码直接插入到您的脚本中。与 AdminScriptEditor 一样，您可以在几分钟内获得一个功能完备的脚本或您自己工作的基础，而无需键入一行代码。

PrimalScript 向导缺少 AdminScriptEditor 的精细度，但它允许连接到远程系统和其他命名空间。无论哪种情况，WMI 脚本开发的时间和工作量都可以大大减少。

### 总结

要真正提升您的脚本编写能力，您需要一个装备齐全的工具箱。幸运的是，有许多与 WMI 相关的工具可以免费或以很小的投资添加。在本章中，我们回顾了一些与 WMI 相关的工具，这些工具可以帮助您了解 WMI 并显著提高您的脚本编写效率。我们向您展示了如何使用 Scriptomatic 创建 WMI 脚本并将其作为多台机器的包装器来执行。我们向您介绍了 WMIC，它允许您从命令行执行 WMI 查询。我们向您展示了如何使用 WBEMTest 进行查询测试，并演示了如何使用 WMI 工具探索 CIM 存储库。尽管 WMI 工具不生成任何代码，但它们将帮助您更好地理解 WMI 的工作原理。最后，我们探讨了一些商业脚本编辑器中的 WMI 向导。这些向导可以将您的脚本开发时间缩短到仅仅一分钟，并且几乎不需要键入任何内容。



### 清单 13-2 从 Active Directory 读取名称

'连接到 AD 的根目录
Dim rootDSE, domainObject
Set rootDSE=GetObject("LDAP://RootDSE")
domainContainer = rootDSE.Get("defaultNamingContext")
Set oDomain = GetObject("LDAP://" & domainContainer)

'从域根目录开始
workwithObject(oDomain)

Sub WorkwithObject(oContainer)
  Dim oADObject
  For Each oADObject in oContainer
    Select Case oADObject.Class
      Case "computer"
        'oADObject 代表一个计算机对象；
        '在此处对其执行操作
        '** 你的代码在这里 **
      Case "organizationalUnit" , "container"
        'oADObject 是一个组织单元或容器...
        '遍历其对象
        workwithObject(oADObject)
    End select
  Next
End Sub

同样，只需将你的代码插入 *你的代码在这里* 占位符处即可。变量 *oADObject* 代表一个计算机对象。你可以访问 *oADObject.cn* 属性来获取计算机名称，然后你可以执行例如，清点 Windows Update 配置设置，以确保你所有的客户端计算机都配置一致。这些包装器可以使对多台计算机的脚本编写更简单、更高效，我们鼓励你使用它们。

## 使用新的和已停用的 WMI 类

Windows XP 和 Windows Server 2003 引入了各种新的 WMI 类。脚本编写中最大的挑战之一是记住哪些类在 Windows 2000 和更早版本的 Windows 中不受支持。编写一个在某台计算机上运行完美但在另一台计算机上完全无法运行的脚本，这可能令人沮丧。

我们发现，要确定哪些 WMI 类可在特定操作系统上使用的最佳资源是 MSDN 库，可通过 http://msdn.microsoft.com/library 访问。

要访问库中关于 WMI 类的信息，请按照以下步骤操作。

+   1. 在库的主页上，单击左窗格中的 Win32 和 COM 开发链接以展开列表。

2. 单击以下每个链接以进一步展开列表并在右窗格中显示信息：单击管理和管理，单击 Windows 管理规范，单击 SDK 文档，单击 Windows 管理规范，单击 WMI 参考，单击 WMI 类，最后，单击 Win32 类。

> **注意** 此信息的路径在库的 CD 或 DVD 版本上有些不同，而此面向 Web 的库的路径也可能发生变化。

在每个类的描述中——通常在 WMI 类描述的底部——你会找到客户端和服务器操作系统的要求列表。较旧的类会将客户端要求列为，例如，*需要 Windows XP、Windows 2000 Professional 或 Windows NT Workstation 4.0 SP4 及更高版本*。较新的类可能只需指定 *需要 Windows XP*。在较旧版本 Windows 上不受支持的类不会在类描述中将较旧版本列为要求。例如，*Win32_Ping* 类列出了 Windows XP 和 Windows Server 2003，但未列出较旧版本的 Windows。

关于 Windows Server 2003 的一个有趣事实是，它实际上*省略*了一组 WMI 类，并停止了对其他几类的支持。这些类仍然受支持，但你必须专门安装它们。一组类提供了处理已安装软件包的支持，而另一组则为 WMI 提供了处理简单网络管理协议的能力。要在 Windows Server 2003 服务器上安装 WMI SNMP 提供程序，请按照以下步骤操作。

+   1. 打开控制面板。
2. 单击添加或删除程序。
3. 单击左窗格中的添加/删除 Windows 组件图标。
4. 单击管理和监视工具详细信息，然后单击详细信息按钮。
5. 选择 WMI SNMP 提供程序复选框，然后单击确定。

Windows Installer 提供程序，提供对已安装软件的支持，位于 Windows Server 2003 产品 CD 上。请注意，此提供程序在未来版本的 Windows 中可能无法直接使用。Windows Server 2003 还停止了对 WMI ADSI 扩展和 ODBC WMI 适配器的支持，尽管两者可能仍然存在于 Windows XP 系统上。

### 使用 *Win32_PingStatus* 类

Windows XP 和 Windows Server 2003 中新增的最实用的 WMI 类之一是 *Win32_PingStatus*。与大多数代表操作系统或计算机硬件某一部分的 WMI 类不同，此类执行网络 ping 命令并将结果作为类实例的属性返回。清单 13-3 展示了此新类的基本格式。

## 清单 13-3 查看 *Win32_PingStatus* 类结果

```vb
Set cPingResults = _
    GetObject("winmgmts://./root/cimv2").ExecQuery("SELECT * " & _
    "FROM Win32_PingStatus WHERE Address = 'don-laptop'")
For Each oPingResult In cPingResults
    If oPingResult.StatusCode = 0 Then
        WScript.Echo "Responds"
    Else
        WScript.Echo "Doesn't respond"
    End If
Next
```

如你所见，你只需添加一个 WHERE 子句并指定要 ping 的地址。该地址可以是网络可解析的名称，也可以是 IP 地址，任你选择。返回的实例将具有 StatusCode 属性，如果指定的地址有响应，则为 0；如果没有响应，则为非零值。这是一个很好的工具，可以添加到连接远程计算机的脚本中。与其让脚本在无法连接时失败，或者添加错误处理然后等待漫长的超时，你可以在尝试任何其他类型的连接之前，主动 ping 该计算机以查看其是否可用。清单 13-4 将 ping 功能包装成一个易于使用的函数，你可以将其粘贴到你的脚本中。

## 清单 13-4 Ping 网络

```vb
Function Ping(strComputer)
    Set cPingResults = _
        GetObject("winmgmts://./root/cimv2").ExecQuery("SELECT * " & _
        "FROM Win32_PingStatus WHERE Address = '" & strComputer & "'")
    For Each oPingResult In cPingResults
        If oPingResult.StatusCode = 0 Then
            Ping = True
        Else
            Ping = False
        End If
    Next
End Function
```

在脚本中使用此函数，你可以通过添加如下内容来执行基本测试：

```vb
wScript.Echo Ping("192.168.0.1")
```

当然，*Win32_PingStatus* 类除了 *Status* 属性外还有其他属性，它们可以提供有关你正在 ping 的计算机的有用信息。请看下一页的清单 13-5，它使用了此新类的一些其他属性。

## 清单 13-5 获取 Ping 信息

```vb
strComputer = "www.sapien.com"
Set cPingResults = _
    GetObject("winmgmts://./root/cimv2").ExecQuery("SELECT * " & _
    "FROM Win32_PingStatus WHERE Address = '" & strComputer & "'")
For Each oPingResult In cPingResults
    If oPingResult.StatusCode = 0 Then
        WScript.Echo strComputer & " Responds from "
        WScript.Echo oPingResult.ProtocolAddress
        WScript.Echo "Response time " & oPingResult.ResponseTime
        WScript.Echo "Source routes " & oPingResult.SourceRoute
    Else
        WScript.Echo strComputer & " Doesn't respond"
    End If
Next
```

此脚本将检查计算机的可用性，然后显示从该名称解析出的地址、ping 的响应时间以及任何可用的源路由信息。例如，你可以在启动某些特别耗资源的管理任务之前，检查到远程计算机的响应时间。响应时间较慢的计算机可能不是执行该任务的理想目标。清单 13-6 是一个返回计算机响应时间的函数。

## 清单 13-6 返回 Ping 响应时间

```vb
Function PingResponse(strComputer)
    Dim t, intResponse
    intResponse = -1
    For t = 1 To 5
        Set cPingResults = _
            GetObject("winmgmts://./root/cimv2").ExecQuery("SELECT * " & _
            "FROM Win32_PingStatus WHERE Address = '" & strComputer & "'")
        For Each oPingResult In cPingResults
            If oPingResult.StatusCode = 0 Then
                If intResponse = -1 Then intResponse = 0
                intResponse = intResponse + oPingResult.ResponseTime
            End If
        Next
    Next
    If intResponse = -1 Then
        PingResponse = -1
    Else
        PingResponse = Int(intResponse/5)
    End If
End Function
```

你可以如下测试此函数。

```vb
WScript.Echo PingResponse("192.168.0.1")
```



该函数将向远程计算机发送五次ping请求，然后以毫秒为单位列出其平均响应时间，这与命令行*Ping*命令的功能非常相似。之后你的脚本可以据此采取相应的操作。

```vbscript
If PingResponse(strComputer) < 75 Then
    'Perform Tasks
Else
    'Don't perform tasks
End If
```

虽然它相当简单，但新的*Win32_PingStatus*类功能非常强大。请记住，被ping的计算机不需要此类。只有运行脚本的计算机才需要拥有*Win32_PingStatus*类（这意味着它必须是Windows XP或更高版本）。

### 配置Windows防火墙

Windows防火墙在Windows XP Service Pack 2和Windows Server 2003 Service Pack 1中引入，提供了每台系统的防火墙功能。Windows防火墙完全可通过其本地图形用户界面或Active Directory中集中配置的组策略对象进行配置。后者是我们配置Windows防火墙的首选方法，因为它更简单，并且与大多数组织的管理模式非常契合。

然而，如果你想通过脚本操作Windows防火墙，有一整套接口可供使用。与本章涵盖的许多主题不同，Windows防火墙并非通过一组WMI类暴露。相反，你将使用来自家庭网络配置（HNetCfg）库的一组COM对象。具体来说，你将使用*HNetCfg.FwMgr*对象，它提供了大部分防火墙管理功能。例如，清单13-7是一个基本脚本，用于列出防火墙中全局开放的端口。

```vbscript
'清单 13-7 列出开放的防火墙端口
Set objFirewall = CreateObject("HNetCfg.FwMgr")
Set objPolicy = objFirewall.LocalPolicy.CurrentProfile

Set colPorts = objPolicy.GloballyOpenPorts

For Each objPort in colPorts
    Wscript.Echo "端口名称: " & objPort.Name
    Wscript.Echo "端口号: " & objPort.Port
    Wscript.Echo "端口IP版本: " & objPort.IPVersion
    Wscript.Echo "端口协议: " & objPort.Protocol
    Wscript.Echo "端口范围: " & objPort.Scope
    Wscript.Echo "端口远程地址: " & objPort.RemoteAddresses
    Wscript.Echo "端口已启用: " & objPort.Enabled
    Wscript.Echo "端口内置: " & objPort.BuiltIn
Next
```

该脚本首先实例化Windows防火墙的管理器对象。请注意，脚本通过以下方式实例化本地对象。

```vbscript
Set objFirewall = CreateObject("HNetCfg.FwMgr", "\\Client23")
```

你可以在远程计算机上实例化该对象（如果你有权执行此操作且Windows防火墙未阻止分布式COM通信）。此对象在物理上实现于System32文件夹中的Hnetcfg.dll文件。

然后，脚本访问当前配置文件（指防火墙配置文件，而非当前用户配置文件）的本地防火墙策略。最后，脚本枚举当前配置文件*GloballyOpenPorts*列表中的端口并将其显示出来。

当前配置文件的本地策略是你将用于大多数Windows防火墙操作的对象。清单13-8配置了Windows防火墙以允许远程管理流量，包括远程WMI脚本。

```vbscript
'清单 13-8 启用远程管理
Set objFirewall = CreateObject("HNetCfg.FwMgr")
Set objPolicy = objFirewall.LocalPolicy.CurrentProfile

Set objAdminSettings = objPolicy.RemoteAdminSettings
objAdminSettings.Enabled = True
```

你经常会在登录脚本中部署这个简单的脚本，因为Windows防火墙会阻止管理流量。在某些环境中，这是我们放入登录脚本的首要任务之一，因为它确保用户无法阻止管理流量。（请注意，组策略对象可以阻止此脚本工作，但如果你已经部署了组策略对象，你就已经能够集中控制此设置。）

由于组策略可用于有效控制Windows防火墙，你可能会想为什么还要费心使用脚本。有时你可能需要进行一些更改，而当用户的计算机（例如笔记本电脑）未连接到公司网络时，难以指导用户完成。在这种情况下，发送一个简短的脚本可以提供临时快速解决方案。例如，假设一名远程员工需要在Windows防火墙中授权某个特定应用程序。清单13-9就是一个可以完成此任务的脚本。

```vbscript
'清单 13-9 授权应用程序
Set objFirewall = CreateObject("HNetCfg.FwMgr")
Set objPolicy = objFirewall.LocalPolicy.CurrentProfile

Set objApplication = CreateObject("HNetCfg.FwAuthorizedApplication")
objApplication.Name = "Corp App"
objApplication.IPVersion = 2
objApplication.ProcessImageFileName = "C:\myappl.exe"
objApplication.RemoteAddresses = "*"
objApplication.Scope = 0
objApplication.Enabled = True

Set colApplications = objPolicy.AuthorizedApplications
colApplications.Add(objApplication)
```

此脚本使用本地策略中的当前配置文件。但是，请注意它还使用了第二个对象HNetCfg.FwAuthorizedApplication，该对象表示Windows防火墙中的一个授权应用程序。该脚本首先为应用程序分配一个显示名称，并将IP版本设置为2。

```vbscript
objApplication.Name = "Corp App"
objApplication.IPVersion = 2
```

然后指定应用程序的可执行文件或映像。这是Windows防火墙将用来标识应用程序的内容。

```vbscript
objApplication.ProcessImageFileName = "c:\myapp1.exe"
```

接下来，脚本指示允许连接到应用程序的远程地址。在此示例中，我们指定了通配符字符（*）以指示允许所有远程地址连接。我们还指定了连接的本地范围，并将新应用程序设置为已启用。

```vbscript
objApplication.RemoteAddresses = "*"
objApplication.Scope = 0
objApplication.Enabled = True
```

最后，我们从当前配置文件的防火墙策略中检索当前授权应用程序列表。我们使用集合的Add方法将新创建的应用程序添加到集合中，使其成为Windows防火墙中正式授权的应用程序。

```vbscript
Set colApplications = objPolicy.AuthorizedApplications
colApplications.Add(objApplication)
```

并非所有对Windows防火墙的更改都必须如此复杂（尽管这是一个相当直接的示例）。清单13-10是一个更简单的示例，用于在全局开放端口列表中打开一个端口（端口9999）。

```vbscript
'清单 13-10 打开一个全局开放端口
Set objFirewall = CreateObject("HNetCfg.FwMgr")
Set objPolicy = objFirewall.LocalPolicy.CurrentProfile
Set colPorts = objPolicy.GloballyOpenPorts

Set objPort = colPorts.Item(9999,6)
objPort.Enabled = TRUE
```

*HNetCfg*对象库包含许多可能有用的对象类别，包括以下内容：

-   **LocalPolicy** 此对象代表本地防火墙策略，与域防火墙策略相对。你已经在本章前面看到过此类对象的实际应用，以及如何使用*HNetCfg.FwMgr*对象的*LocalPolicy*属性来检索它。
-   **Profile** 用于操作Windows防火墙配置文件的这些对象包括：
    -   **AuthorizedApplications** 此对象是防火墙中授权应用程序的集合。你可以通过任何配置文件对象检索此集合。
    -   **CurrentProfile** 此对象表示当前防火墙配置文件。使用*HNetCfg.FwMgr.LocalPolicy.CurrentProfile*命令是检索配置文件对象（具体来说是当前配置文件）的一种方式。
    -   **CurrentProfileType** 此属性指示当前生效的Windows防火墙配置文件的类型。如果当前配置文件是域配置文件，则此属性将为0（零），如果是标准配置文件，则为1。
    -   **ExceptionsNotAllowed** 此属性可以是TRUE或FALSE，它告诉Windows防火墙是否允许防火墙例外。它是任何配置文件对象的一部分。
    -   **FirewallEnable** 此属性可以是TRUE或FALSE，指示防火墙是否已启用。它可通过配置文件对象访问。
    -   **GetProfileByType** 此方法检索指定类型的Windows防火墙配置文件。除了*CurrentProfile*对象外，使用此方法是检索配置文件对象的唯一方式。例如，*HNetCfg.FwMgr.GetProfileByType*命令将检索域防火墙配置文件。
    -   **GloballyOpenPorts** 这是配置文件中全局开放端口的集合。它可通过配置文件对象访问。
    -   **IcmpSettings** 这是一个只读属性，详细说明了配置文件中的ICMP设置。它可通过配置文件对象访问。
    -   **NotificationsDisabled** 此属性可以是TRUE或FALSE，指示交互式用户通知是打开还是关闭。此属性通过配置文件对象访问。
    -   **RemoteAdminSettings** 这是一个子对象，代表防火墙配置文件的远程管理设置。它可通过配置文件对象访问。
    -   **Services** 这是配置文件中服务的集合。它可通过配置文件对象访问。
    -   **Type** 这指示配置文件的类型（0表示域，1表示标准）。它作为配置文件对象的属性进行访问。



### 使用磁盘配额管理

尽管 Windows 2000 为 Windows 操作系统引入了内置磁盘配额，但基于 WMI 的磁盘配额管理功能首次在 Windows Server 2003 中提供。一个新类 `Win32_DiskQuota` 表示单个磁盘配额条目。清单 13-11 列出了名为 FILES1 的文件服务器上的所有配额。

```
清单 13-11 列出配额条目
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\FILES1\root\cimv2")

Set colDiskQuotas = objWMIService.ExecQuery( _
    "Select * from win32_DiskQuota")

For each objQuota in colDiskQuotas
    wscript.Echo "Disk Space Used: " & objQuota.DiskSpaceUsed
    wscript.Echo "           Limit: " & objQuota.Limit
    wscript.Echo "   Quota Volume: " & objQuota.QuotaVolume
    wscript.Echo "          Status: " & objQuota.Status
    wscript.Echo "            User: " & objQuota.User
    wscript.Echo "   Warning Limit: " & objQuota.WarningLimit
    wscript.Echo "-----------------------------------------"
Next
```

`Win32_DiskQuota` 类支持多个属性，可以轻松查看当前配额条目。不过，你可能会发现 `User` 属性需要一点时间来适应。它实际上是 `Win32_Account` 类实例的引用，因此你需要使用该类来获取用户属性信息。类似地，`QuotaVolume` 属性是 `Win32_LogicalDisk` 类实例的引用。例如，考虑下面这个替代查询，它检索特定卷上特定用户的配额条目。

```
Set objQuota = objWMIService.Get _
    ("win32_DiskQuota.QuotaVolume=" & _
    "'win32_LogicalDisk.DeviceID=""C:""'"," & _
    "User='win32_Account.Domain=""company"",Name=""donj""'")
```

此处，使用的是 WMI 服务的 `Get` 方法（而非 `ExecQuery` 方法）来检索类实例。具体来说，它正在检索服务器 C 卷上用户 donj 的实例。

检索到类实例后，你可以对其进行修改。最有可能的是，你想要修改 `Limit` 属性。

```
objQuota.Limit = 10000
objQuota.Put_
```

这会将限制修改为 10,000KB，即 10MB。

另一个类 `Win32_QuotaSetting` 提供了对整个服务器配额配置设置的访问。该类有几个属性；清单 13-12 显示了所有属性。

```
清单 13-12 列出配额设置
Set objWMIService = GetObject("winmgmts://FILESI/root/cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_QuotaSetting",,48)
For Each objItem in colItems
    WScript.Echo "Caption: " & objItem.Caption
    WScript.Echo "DefaultLimit: " & objItem.DefaultLimit
    WScript.Echo "DefaultWarningLimit: " & objItem.DefaultWarningLimit
    WScript.Echo "Description: " & objItem.Description
    WScript.Echo "ExceededNotification: " & objItem.ExceededNotification
    WScript.Echo "SettingID: " & objItem.SettingID
    WScript.Echo "State: " & objItem.State
    WScript.Echo "VolumePath: " & objItem.VolumePath
    WScript.Echo "WarningExceededNotification: " & _
        objItem.WarningExceededNotification
Next
```

你可以修改其中的许多设置。例如，要更改默认配额限制，假设你已经将一个配额设置实例查询到变量 *objQuotaSetting* 中，你需要输入以下内容：

```
objQuotaSetting.DefaultLimit = 10000000
objQuotaSetting.Put_
```

> **更多信息** 你可以在 TechNet 脚本中心找到用于管理磁盘配额的其他示例脚本，地址为

http://www.microsoft.com/technet/scriptcenter/scripts/storage/quotas/default.mspx

（此链接包含在随附的 CD 上；点击 *Disk Quotas*。）

### 使用 DNS 提供程序

Windows Server 2003 中包含的 WMI 新 DNS 提供程序将 Windows DNS 服务器的大部分功能暴露给 WMI，从而暴露给你的脚本。请记住，此提供程序仅存在于已安装并运行 DNS 服务器软件的 Windows Server 2003 计算机上。虽然你可以在任何 Windows 计算机上运行本节中的脚本，但它们需要以安装了 DNS 软件的服务器为目标。

> **注意** 此提供程序的一个版本已为 Windows 2000 Server 发布。你可以在 Windows 2000 Server 资源工具包中找到它。

该提供程序暴露了两个不同的 WMI 类别：一个用于 DNS 记录管理，另一个用于 DNS 服务器管理。作为第一个类别的一个例子，下一页的清单 13-13 显示了如何使用 `MicrosoftDNS_Cache` 类清除 DNS 服务器的名称解析缓存。

```
清单 13-13 清除 DNS 服务器缓存
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\DNS1" & _
    "\\root\\MicrosoftDNS")
Set colItems = objWMIService.ExecQuery("Select * From MicrosoftDNS_Cache")
For Each objItem in colItems
    objItem.ClearCache()
Next
```

此脚本最显著的特征是它没有查询常用的 `root\cimv2` WMI 命名空间。相反，DNS 提供程序可通过新的命名空间 `root\MicrosoftDNS` 访问。另请注意，类名与 `root\cimv2` 中的大多数类不同，它们不以 `Win32_` 开头。清单 13-13 是一个简短、简单的脚本，但它仍然提供了大多数 WMI 脚本的灵活性。例如，清单 13-14 重新利用该脚本，针对列在文本文件 `C:\Dnsservers.txt` 中的多个 DNS 服务器运行。

```
清单 13-14 清除多个 DNS 服务器的缓存
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("c:\\dnsservers.txt")
Do Until objTS.AtEndOfStream
    strComputer = objTS.ReadLine
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" & strComputer & _
        "\\root\\MicrosoftDNS")
    Set colItems = objWMIService.ExecQuery( _
        "Select * From MicrosoftDNS_Cache")
    For Each objItem in colItems
        objItem.ClearCache()
    Next
Loop
objTS.Close
```

以下类提供其他服务器管理功能。

- **MicrosoftDNS_Zone** 此类表示一个 DNS 区域。你可以用它来老化记录、暂停区域、更改区域类型等。
- **MicrosoftDNS_Server** 此类表示服务器本身。你可以用它来启动记录清理、启动和停止 DNS 服务器服务，以及访问服务器配置属性。清单 13-15 列出了该类的所有属性。
- **MicrosoftDNS_Domain** 此类提供对 DNS 域配置设置的访问。
- **MicrosoftDNS_RootHints** 此类提供对服务器根提示的访问。
- **MicrosoftDNS_Statistic** 此类提供对各种性能统计信息的访问。



## 清单 13-15 列出 DNS 服务器属性

```vbscript
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & _
        "\\root\\MicrosoftDNS")

Set colItems = objWMIService.ExecQuery("Select * from MicrosoftDNS_Server")

For Each objItem in colItems
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Address Answer Limit: " & objItem.AddressAnswerLimit
    Wscript.Echo "Allow Update: " & objItem.AllowUpdate
    Wscript.Echo "Autocache Update: " & objItem.AutoCacheUpdate
    Wscript.Echo "Autoconfig File Zones: " & objItem.AutoConfigFileZones
    Wscript.Echo "Bind Secondaries: " & objItem.BindSecondaries
    Wscript.Echo "Boot Method: " & objItem.BootMethod
    Wscript.Echo "Default Aging State: " & objItem.DefaultAgingState
    Wscript.Echo "Default No-Refresh Interval: " & _
        objItem.DefaultNORefreshInterval
    Wscript.Echo "Default Refresh Interval: " & objItem.DefaultRefreshInterval
    Wscript.Echo "Disable AutoReverse Zones: " & _
        objItem.DisableAutoReverseZones
    Wscript.Echo "Disjoint Nets: " & objItem.DisjointNets
    Wscript.Echo "Directory Service Available: " & objItem.DsAvailable
    Wscript.Echo "Directory Service Polling Interval: " & _
        objItem.DsPollingInterval
    Wscript.Echo "Directory Service Tombstone Interval: " & _
        objItem.DsTombstoneInterval
    Wscript.Echo "EDNS Cache Timeout: " & objItem.EDnsCacheTimeout
    Wscript.Echo "Enable Directory Partitions: " & _
        objItem.EnableDirectoryPartitions
    Wscript.Echo "Enable DNSSec: " & objItem.EnableDnsSec
    Wscript.Echo "Enable EDNS Probes: " & objItem.EnableEDnsProbes
    Wscript.Echo "Event Log Level: " & objItem.EventLogLevel
    Wscript.Echo "Forward Delegations: " & objItem.ForwardDelegations
    If Not IsNull(objItem.Forwarders) Then
        strForwarders = Join(objItem.Forwarders, ",")
        Wscript.Echo "Forwarders: " & strForwarders
    Else
        Wscript.Echo "Forwarders:"
    End If
    Wscript.Echo "Forwarding Timeout: " & objItem.ForwardingTimeout
    Wscript.Echo "Is Slave: " & objItem.IsSlave
    If Not IsNull(objItem.ListenAddresses) Then
        strListenAddresses = Join(objItem.ListenAddresses, ",")
        Wscript.Echo "Listen Addresses: " & strListenAddresses
    Else
        Wscript.Echo "Listen Addresses:"
    End If
    Wscript.Echo "Local Net Priority: " & objItem.LocalNetPriority
    Wscript.Echo "Logfile Maximum Size: " & objItem.LogFileMaxSize
    Wscript.Echo "Logfile Path: " & objItem.LogFilePath
    Wscript.Echo "Log Level: " & objItem.LogLevel
    Wscript.Echo "Loose Wildcarding: " & objItem.LooseWildcarding
    Wscript.Echo "Maximum Cache Time-to-Live: " & objItem.MaxCacheTTL
    Wscript.Echo "Maximum Negative Cache Time-to-Live: " & _
        objItem.MaxNegativeCacheTTL
    Wscript.Echo "Name Check Flag: " & objItem.NameCheckFlag
    Wscript.Echo "No Recursion: " & objItem.NoRecursion
    Wscript.Echo "Polling Interval: " & objItem.PollingInterval
    Wscript.Echo "Preferred IP Port: " & objItem.PreferredIPPort
    Wscript.Echo "Recursion Maximum: " & objItem.RecursionMaximum
    Wscript.Echo "Recursion Timeout: " & objItem.RecursionTimeout
    Wscript.Echo "Round Robin: " & objItem.RoundRobin
    Wscript.Echo "Scavenging State: " & objItem.ScavengingState
    Wscript.Echo "Scavenging Interval: " & objItem.ScavengingInterval
    Wscript.Echo "Secure Responses: " & objItem.SecureResponses
    Wscript.Echo "Send Port: " & objItem.SendPort
    Wscript.Echo "Server Addresses: " & objItem.ServerAddresses
    Wscript.Echo "Server Level Update: " & objItem.ServerLevelUpdate
    Wscript.Echo "Strict File Parsing: " & objItem.StrictFileParsing
    Wscript.Echo "Synchronize Scavenging State: " & objItem.SyncScavengingState
    Wscript.Echo "Update Options: " & objItem.UpdateOptions
    Wscript.Echo "Version: " & objItem.Version
    Wscript.Echo "Zone Directory Partition: " & objItem.ZoneDirectoryPartition
    Wscript.Echo "Zone Type: " & objItem.ZoneType
Next
```

> 提示 清单 13-15 是由 WMI 代码向导生成的，例如 Scriptomatic v2.0 和 SAPIEN PrimalScript 中的向导。你可以看到这些向导在快速生成列出给定类所有属性（包括像 *Forwarders* 这样的数组式属性）的脚本时非常有用。请注意，如上所述，此脚本必须在安装了 DNS 服务器软件的服务器上运行。

此外，大量的类提供了对 DNS 记录管理的访问。本质上，DNS 服务器可以包含的每种记录类型都存在一个对应的类：A、MX、CNAME、TXT、NS、SRV 等。清单 13-16 展示了如何列出服务器上的所有 A 记录。（同样，WMI 代码向导通过快速生成此类简单脚本节省了大量时间。）

## 清单 13-16 列出所有 A 记录

```vbscript
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\DNS1" & _
    "\\root\\MicrosoftDNS")
Set colItems = objWMIService.ExecQuery("Select * from MicrosoftDNS_AType")
For Each objItem in colItems
    wscript.Echo "IP Address: " & objItem.IPAddress
    wscript.Echo "Owner Name: " & objItem.OwnerName
    wscript.Echo "Container Name: " & objItem.ContainerName
    wscript.Echo "DNS Server Name: " & objItem.DnsServerName
    wscript.Echo "Domain Name: " & objItem.DomainName
    wscript.Echo "Record Class: " & objItem.RecordClass
    wscript.Echo "Record Data: " & objItem.RecordData
    wscript.Echo "Text Representation: " & objItem.TextRepresentation
    wscript.Echo "Time-to-Live: " & objItem.TTL
    wscript.Echo
Next
```

请注意，WMI 类名是 *MicrosoftDNS_AType*。你可以根据这个模式轻松地推断出其他记录类型的类名。例如，*CNAME* 记录通过 *MicrosoftDNS_CNAMEType* 类公开。如清单 13-17 所示，使用不同的类不需要对脚本进行太多修改。

## 清单 13-17 列出所有 CNAME 记录

```vbscript
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\DNS1" & _
    "\\root\\MicrosoftDNS")
Set colItems = objWMIService.ExecQuery("Select * from MicrosoftDNS_CNAMEType")
For Each objItem in colItems
    Wscript.Echo "Owner Name: " & objItem.OwnerName
    Wscript.Echo "Primary Name: " & objItem.PrimaryName
    Wscript.Echo "Container Name: " & objItem.ContainerName
    Wscript.Echo "DNS Server Name: " & objItem.DnsServerName
    Wscript.Echo "Domain Name: " & objItem.DomainName
    Wscript.Echo "Record Class: " & objItem.RecordClass
    Wscript.Echo "Record Data: " & objItem.RecordData
    Wscript.Echo "Text Representation: " & objItem.TextRepresentation
    Wscript.Echo "Time-to-Live: " & objItem.TTL
    Wscript.Echo
Next
```

注意 *A* 和 *CNAME* 之间的属性有细微差别。由于这两种记录类型非常相似，它们的属性列表也同样相似。然而，像 *MX* 这样的记录（通过 *MicrosoftDNS_MXType* 类访问）具有完全不同的属性，对应于 MX 记录中的不同字段。这些 WMI 类非常适合用于列出记录和创建新记录。编写脚本来创建新的静态记录，是确保它们在多个服务器上一致创建，并自动化创建多个新记录这一繁琐过程的绝佳方式。清单 13-18 是使用 *MicrosoftDNS_MXType* 类创建新记录的示例。

## 清单 13-18 创建 MX 记录

```vbscript
strDNSServer = "dns1.company.com"
strContainer = "company.com"
strOwner = "mail1.company.com"
intRecordClass = 1
intTTL = 600
intPreference = 0
strMailExchanger = "mail1.company.com"

Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\DNS1" & _
    "\\root\\MicrosoftDNS")

Set objItem = objWMIService.Get("MicrosoftDNS_MXType")
errResult = objItem.CreateInstanceFromPropertyData _
    (strDNSServer, strContainer, strOwner, intRecordClass, intTTL, _
    intPreference, strMailExchanger)
```

请注意，您需要修改此示例以及其他与 DNS 相关的示例，以包含适当的值。例如，如果您的域不是 company.com，此脚本将无法工作，因为 mail1.company.com 对您的域无效。

在此处，字符串变量用于为新记录设置属性。然后，脚本直接查询 DNS 提供程序本身，而不是查询特定的类。

```
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\DNS1" & _
    "\\root\\MicrosoftDNS")
```

接下来，脚本要求 DNS 提供程序返回所需的记录类型。此处没有检索特定的实例；相反，提供程序返回所谓的*类原型*，这本质上只是类的描述。

```
Set objItem = objWMIService.Get("MicrosoftDNS_MXType")
```

有了该类描述，脚本就可以通过使用类自身的 `CreateInstanceFromPropertyData` 方法来创建新实例——即一条新记录。该方法要求脚本提供所有类属性的值。

```
errResult = objItem.CreateInstanceFromPropertyData _
    (strDNSServer, strContainer, strOwner, intRecordClass, intTTL, _
    intPreference, strMailExchanger)
```

此技术可用于创建任何 DNS 记录类的新实例。例如，清单 13-19 使用此技术创建了一个新的 *TXT* 记录，并填充了发件人策略框架 (SPF) 描述。

```
清单 13-19 创建 TXT 记录
strDNSServer = "dns1.company.com"
strContainer = "company.com"
strOwner = "dns1.company.com"
intRecordClass = 1
intTTL = 600
strText = "v=spf1 a ~all"

Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\DNS1" & _
    "\\root\\MicrosoftDNS")

Set objItem = objWMIService.Get("MicrosoftDNS_TXTType")
errResult = objItem.CreateInstanceFromPropertyData _
    (strDNSServer, strContainer, strOwner, intRecordClass, intTTL, strText)
```

同样，新实例的属性值被赋给了变量。脚本连接到 DNS 提供程序并请求 *MicrosoftDNS_TXTType* 类的类原型。脚本使用该信息创建类的新实例，并传入变量以填充新实例的属性。

> **更多信息** 其他 DNS 记录管理示例脚本可在 http://www.microsoft.com/technet/scriptcenter/scripts/network/dns/records/default.mspx 找到（此链接包含在随附的 CD 中；单击 *DNS Records*。）管理 DNS 服务器本身的脚本可在 http://www.microsoft.com/technet/scriptcenter/scripts/network/dns/manage/default.mspx 找到（此链接包含在随附的 CD 中；单击 *DNS Server Management Tasks*。）

### 使用 Active Directory 复制和信任

Windows Server 2003 域控制器公开了一组用于管理 Active Directory 的新类。与 DNS 类一样，这些类安装在其自己的命名空间 *root\MicrosoftActiveDirectory* 中。从管理角度来看，一些最有用的类与 Active Directory 复制相关。例如，清单 13-20 使用 *MSAD_ReplPendingOp* 类（该类列出待处理的复制操作）来显示给定域控制器上待处理的复制作业数量。

```
清单 13-20 列出待处理的复制作业
strComputer = "DC1"
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\MicrosoftActiveDirectory")

Set colReplicationOperations = objWMIService.ExecQuery _
    ("Select * from MSAD_ReplPendingOp")

If colReplicationOperations.Count = 0 Then
    WScript.Echo "There are no replication jobs pending."
Else
    Dim intCount
    For each objReplicationJob in colReplicationOperations
        intCount = intCount + 1
    Next
    WScript.Echo "There are " & intCount & " replication" & _
        " job(s) pending."
End If
```

提示 在本章开头，我们提供了两个设计用于针对多台计算机的包装器。如果您有一个文本文件，列出了您域中所有域控制器的名称，然后将清单 13-20 插入从文本文件读取名称的包装器（清单 13-1），您将拥有一个工具，可以显示您环境中每个域控制器的待处理复制情况。这对于各种故障排除任务或常规监视来说将是一个方便的工具。

每个域控制器还包括一个名为 *MSAD_DomainController* 的类，该类代表域控制器并提供对各种状态信息的访问。清单 13-21 展示了如何查询此类，并显示其几个属性。

```
清单 13-21 显示域控制器属性
strComputer = "DC"
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\MicrosoftActiveDirectory")

Set colDC = objWMIService.ExecQuery _
    ("Select * from MSAD_DomainController")

For Each objDC In colDC
    WScript.Echo "Common name: " & objDC.CommonName
    WScript.Echo "Is a GC: " & objDC.IsGC
    WScript.Echo "Next RID pool available?: " & _
        objDC.IsNextRIDPoolAvailable
    WScript.Echo "In DNS?: " & objDC.IsRegisteredInDNS
    WScript.Echo "Sysvol ready?: " & objDC.IsSysVolReady
    WScript.Echo "% RIDs left: " & objDC.PercentOfRIDsLeft
    WScript.Echo "Site: " & objDC.SiteName
    WScript.Echo "oldest add: " & objDC.TimeOfOldestReplAdd
    WScript.Echo "oldest delete: " & objDC.TimeOfOldestReplDel
    WScript.Echo "oldest mod: " & objDC.TimeOfOldestReplMod
    WScript.Echo "oldest sync: " & objDC.TimeOfOldestReplSync
Next
```

此脚本也可以成为快速显示环境中域控制器关键统计数据的有用工具。其他类包括 *MSAD_ReplNeighbor*，它提供对域控制器所有复制邻居的访问，并公开有关上次同步和同步失败次数的信息。

还有一些 WMI 类可用于处理域信任关系。例如，*Microsoft_LocalDomainInfo* 类（也位于 *root\MicrosoftActiveDirectory* 命名空间中）提供有关本地域（即查询的域控制器所属的域）的信任相关信息。清单 13-22 说明了此类及其属性。

#### 清单 13-22 列出域属性

```
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & _
 "DC1\root\MicrosoftActiveDirectory")

Set colDomainInfo = objWMIService.ExecQuery _
 ("Select * from Microsoft_LocalDomainInfo")

For each objDomain in colDomainInfo
    wscript.Echo " DNS name: " & objDomain.DNSName
    wscript.Echo "Flat name: " & objDomain.FlatName
    wscript.Echo "     SID: " & objDomain.SID
    wscript.Echo "Tree name: " & objDomain.TreeName
    wscript.Echo "  DC name: " & objDomain.DCName
Next
```

更有趣且有用的是 *Microsoft_DomainTrustStatus* 类，它提供有关域内所有信任关系的信息。清单 13-23 中的脚本是获取域信任及其当前状态快速概览的绝佳工具。

#### 清单 13-23 列出信任状态

```
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & _
 "DC1\root\MicrosoftActiveDirectory")

Set colTrustList = objWMIService.ExecQuery _
 ("Select * from Microsoft_DomainTrustStatus")

For each objTrust in colTrustList
    wscript.Echo "  Trusted domain: " & objTrust.TrustedDomain
    wscript.Echo " Trust direction: " & objTrust.TrustDirection
    wscript.Echo "     Trust type: " & objTrust.TrustType
    wscript.Echo " Trust attributes: " & objTrust.TrustAttributes
    wscript.Echo "  Trusted DC name: " & objTrust.TrustedDCName
    wscript.Echo "    Trust status: " & objTrust.TrustStatus
    wscript.Echo "    Trust is OK: " & objTrust.TrustIsOK
    WScript.Echo "------------------------------------------"
Next
```

与许多其他 WMI 类一样，您可以修改实例属性来重新配置 Active Directory。例如，名为 *Microsoft_TrustProvider* 的类公开了管理域信任的 Active Directory 部分的配置信息。通过修改其属性，您可以更改 Active Directory 该部分的行为方式。清单 13-24（从下一页开始）展示了如何更改信任提供程序的 *TrustListLifetime*、*TrustStatusLifetime* 和 *TrustCheckLevel* 属性。



第三部分：高级脚本技术、工具与技术

> **注意** 如果操作不慎，修改信任提供程序的工作方式可能会在你的域中引发问题。在进行此操作前，请确保你已了解更改这些属性可能带来的后果。

```
代码清单 13-24 修改信任提供程序
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    "DC1\root\MicrosoftActiveDirectory")

Set colTrustList = objWMIService.ExecQuery _
    ("Select * from Microsoft_TrustProvider")

For Each objTrust in colTrustList
    objTrust.TrustListLifetime = 25
    objTrust.TrustStatusLifetime = 10
    objTrust.TrustCheckLevel = 1
    objTrust.Put_
Next
```

请注意，此处的修改遵循一个你应该熟悉的模式：将新值赋给属性，然后调用 *Put* 方法保存更改。

> **更多信息** 你可以在以下位置找到更多 Active Directory 信任和复制示例脚本：
>
> http://www.microsoft.com/technet/scriptcenter/scripts/ad/monitor/default.mspx
>
> （此链接已包含在配套 CD 中；点击 *AD Trust and Replication*。）

### 使用 Internet Information Services 6.0

Internet Information Services (IIS) 6.0 通过 WMI 几乎将其所有的管理信息和功能都暴露出来，使用的是一个新的 *root\MicrosoftIISv2* 命名空间中的类。（请注意，名称中的 v2 指的是命名空间的版本，而不是 IIS 的版本。）使用此命名空间与其他 WMI 命名空间的使用方式截然不同，因此你需要了解一些关于 IIS 的 XML 配置元数据库如何构建的知识。该元数据库由一个层次结构组成，其顶层是 *IisComputer* 类。其下是 Web、FTP、NNTP 等服务。当然，IIS 支持每个服务器上运行多个网站，因此 Web 服务可以包含多个子站点。这种层次结构通常以类似于文件路径的路径格式表示。例如，*W3SVC/1/ROOT* 指的是 Web 服务（W3SVC）、第一个子站点（通常是默认 Web 站点）以及该站点的根虚拟目录。

IIS 命名空间分为两组类。一组类提供对只读属性的访问，另一组提供对读/写属性的访问。例如，虚拟目录——*IisWebVirtualDir* 类——由只读属性组成，而其配套类——IisWebVirtualDirSettings——包含可读和可写（更改）的属性。代码清单 13-25 展示了如何查询特定的虚拟目录并显示其所有属性。

```
代码清单 13-25 列出 IIS 虚拟目录属性
On Error Resume Next
set oProvider = GetObject("winmgmts://localhost/root/MicrosoftIISv2")
set oVirtualDir = oProvider.get("IIsWebVirtualDir='W3SVC/1/ROOT'")
set oVirtualDirSetting = oProvider.get("IIsWebVirtualDirSetting='W3SVC/1/ROOT'")

WScript.Echo "Read only properties of W3SVC/1/Root:"
For Each Property in oVirtualDir.Properties_
    WScript.Echo Property.Name & " = " & Property.Value
Next

WScript.Echo
WScript.Echo "Read/Write properties of W3SVC/1/Root:"
For Each Property in oVirtualDirSetting.Properties_
    WScript.Echo Property.Name & " = " & Property.Value
Next
```

让我们快速了解一下这是如何工作的。该脚本首先连接到 *MicrosoftIISv2* 命名空间。请注意，它没有查询特定的类；相反，它通过使用 *Get* 方法要求命名空间返回匹配指定路径的特定类（*IIsWebVirtualDir*）。

```
On Error Resume Next
set oProvider = GetObject("winmgmts://localhost/root/MicrosoftIISv2")
set oVirtualDir = oProvider.get("IIsWebVirtualDir='W3SVC/1/ROOT'")
set oVirtualDirSetting = oProvider.get("IIsWebVirtualDirSetting='W3SVC/1/ROOT'")
```

然后，脚本遍历该类的属性集合，显示每个属性的名称和值。

```
WScript.Echo "Read only properties of W3SVC/1/Root:"
For Each Property in oVirtualDir.Properties_
    WScript.Echo Property.Name & " = " & Property.Value
Next
```

同样的技术用于显示配套类 *IIsWebVirtualDirSettings* 中的读/写设置。

```
WScript.Echo "Read/Write properties of W3SVC/1/Root:"
For Each Property in oVirtualDirSetting.Properties_
    WScript.Echo Property.Name & " = " & Property.Value
Next
```

IIS WMI 命名空间通常用于一致地配置 IIS 服务器。例如，在拥有 20 台服务器的 Web 场中手动创建新的网站可能会很繁琐且容易出错。使用脚本更快，并且可以大幅减少拼写错误和其他错误的可能性。代码清单 13-26 在单台计算机上创建一个新的网站。你可以将其添加到一个包装脚本中，以针对多台计算机执行。

## 代码清单 13-26 创建新网站

```
set oLocator = CreateObject("wbemScripting.SWbemLocator")
set oProvider = oLocator.ConnectServer("Server2", "root/MicrosoftIISv2")
set oService = oProvider.Get("IIsWebService='w3SVC'")

oBindings = Array(0)
Set oBindings(0) = oProvider.Get("ServerBinding").SpawnInstance_()
oBindings(0).IP = ""
oBindings(0).Port = "8383"
oBindings(0).Hostname = ""

Dim sSiteObjectPath
sSiteObjectPath = oService.CreateNewSite("NewWebSite", oBindings, "C:\Inetpub\wwwroot")
If Err Then
    WScript.Echo "*** Error Creating Site: " & Hex(Err.Number) & ": " & Err.Description & " ***"
    WScript.Quit(1)
End If

Set oPath = CreateObject("wbemScripting.SWbemObjectPath")
oPath.Path = sSiteObjectPath
sSitePath = oPath.Keys.Item("")

Set oVirtualDir = oProvider.Get("IIsWebVirtualDirSetting='" & sSitePath & "/ROOT'")
oVirtualDir.AuthFlags = 5 ' AuthNTLM + AuthAnonymous
oVirtualDir.EnableDefaultDoc = True
oVirtualDir.DirBrowseFlags = &H4000003E ' date, time, size, extension, longdate
oVirtualDir.AccessFlags = 513 ' read, script
oVirtualDir.AppFriendlyName = "Root Application"

oVirtualDir.Put_()

Set oServer = oProvider.Get(sSiteObjectPath)
oServer.Start

WScript.Echo "Complete"
```

同样，我们将逐步讲解这个脚本的功能。它首先连接到命名空间，并检索 IIsWebService 类。

```
set oLocator = CreateObject("wbemScripting.SWbemLocator")
set oProvider = oLocator.ConnectServer("Server2", "root/MicrosoftIISv2")
set oService = oProvider.Get("IIsWebService='w3SVC'")
```

然后，脚本为新网站设置*绑定*。绑定是用于访问此站点的 IP 地址、端口和主机头的唯一组合。在这里，脚本获取 *ServerBinding* 类的新实例来填充它。

```
oBindings = Array(0)
Set oBindings(0) = oProvider.Get("ServerBinding").SpawnInstance_()
```

接下来，脚本设置一个空白的 IP 地址（意味着将使用所有未分配的 IP 地址）、一个空白的主机名和一个特定的端口。这些信息以数组的形式表示。

```
oBindings(0).IP = ""
oBindings(0).Port = "8383"
oBindings(0).Hostname = ""
```

接下来，脚本要求 Web 服务创建一个新的网站。它传递了站点的名称、绑定数组以及新站点根文件夹的文件系统路径。如果此操作未能完成，错误处理将结束脚本。变量 *sSiteObjectPath* 将包含新创建网站的 WMI 路径。

```
Dim sSiteObjectPath
sSiteObjectPath = oService.CreateNewSite("NewWebSite", _
    oBindings, "C:\Inetpub\wwwroot")
If Err Then
    WScript.Echo "*** Error Creating Site: " & Hex(Err.Number) & _
        ": " & Err.Description & " ***"
    WScript.Quit(1)
End If
```

现在，脚本创建一个新的 WMI 对象路径对象，并将其设置为等于新创建的站点。这用于检索站点的 IIS 元数据库路径。

```
Set oPath = CreateObject("WbemScripting.SWbemObjectPath")
oPath.Path = sSiteObjectPath
sSitePath = oPath.Keys.Item("")
```

使用新的元数据库路径，脚本要求 IIS WMI 提供程序获取新站点的 *IIsWebVirtualDirSetting* 类。具体来说，它检索站点的根文件夹。请记住，这个类包含可写属性，因此我们可以配置站点的属性。

```
Set oVirtualDir = oProvider.Get("IIsWebVirtualDirSetting='" & _
    sSitePath & "/ROOT'")
```

设置了许多属性，包括身份验证级别、默认文档、目录浏览标志、访问标志以及站点的应用程序名称。*Put* 方法用于保存更改。

```
oVirtualDir.AuthFlags = 5 ' AuthNTLM + AuthAnonymous
oVirtualDir.EnableDefaultDoc = True
oVirtualDir.DirBrowseFlags = &H4000003E ' date, time, size, _
                                    extension, longdate
oVirtualDir.AccessFlags = 513 ' read, script
oVirtualDir.AppFriendlyName = "Root Application"
oVirtualDir.Put_()
```



# 第三部分：高级脚本技术、工具与技术

最后，系统会请求提供程序检索新创建并配置好的网站，以便将其启动。

```vb
Set oServer = oProvider.Get(sSiteobjectPath)
oServer.Start
WScript.Echo "Complete"
```

操作步骤繁多，但当你将其分解后，就会发现该脚本遵循的流程与手动创建新网站时完全相同。

现在，我们将重点关注备份元数据库。元数据库备份功能有多个选项；例如，你可以包含元数据库备份部分的子键，或者包含继承的属性。我们通常将这些值定义为命名常量，以便更轻松地使用。

```vb
Const EXPORT_CHILDREN = 0
' Adds properties of child keys to the export file.

Const EXPORT_INHERITED = 1
' Adds inherited properties of the exported keys to the export file.

Const EXPORT_NODE_ONLY = 2
' Does not add subkeys of the specified key to the export file.
```

你也可以为元数据库备份分配一个密码。

```vb
sPassword = "ExportingPassw0rd"
```

此密码将在稍后导入配置时使用（如果需要）。你必须告诉 IIS 要导出元数据库的哪个部分：为此你将使用一个元数据库路径。例如，以下是如何导出元数据库配置的自定义日志记录部分。

```vb
sMetabasePath = "/lm/logging/custom logging"
```

在此示例中，*lm* 是 IIS 计算机的根名称，这就是它出现在路径开头的原因。执行备份只需连接到 IIS WMI 命名空间，检索代表 IIS 的 *IisComputer* 实例，然后要求 IIS 导出选定的元数据库部分。

```vb
set oLocator = CreateObject("wbemScripting.SWbemLocator")
set oProvider = oLocator.ConnectServer("Server2", "root/MicrosoftIISv2")
Set oComputer = oProvider.get("IISComputer='LM'")
oComputer.Export sPassword, sFilePath, sMetabasePath, iFlags
```

清单 13-27 是完整的脚本。

#### 清单 13-27 导出 IIS 元数据库

```vb
Const EXPORT_CHILDREN = 0
' Adds properties of child keys to the export file.

Const EXPORT_INHERITED = 1
' Adds inherited properties of the exported keys to the export file.

Const EXPORT_NODE_ONLY = 2
' Does not add subkeys of the specified key to the export file.

Dim sPassword, sFilePath, sMetabasePath, iFlags
sPassword = "ExportingPassw0rd"
' Use this password to import the configuration.

sFilePath = "C:\exported.xml"

sMetabasePath = "/lm/logging/custom logging"
' As represented in the metabase.xml file.

iFlags = EXPORT_NODE_ONLY OR EXPORT_INHERITED

set oLocator = CreateObject("WbemScripting.SwbemLocator")
set oProvider = oLocator.ConnectServer("Server2", "root/MicrosoftIISv2")
Set oComputer = oProvider.get("IIsComputer='LM'")

oComputer.Export sPassword, sFilePath, sMetabasePath, iFlags

wScript.Echo "Exported the node at " & sMetabasePath & " to " & sFilePath
```

想象一下能够定期运行这样的脚本——也许作为计划任务——以定期保存 IIS 元数据库的部分内容，用于灾难恢复场景。这只是此类脚本的一种用途，它很好地说明了脚本如何使 IIS 更易于管理。

当然，你无需编写一行 VBScript 代码就能进行大量的脚本化 IIS 管理。这是因为 Windows Server 2003 包含一些命令行实用程序，例如 *iisweb*、*iisftp* 等，可用于自动化配置 IIS。（这些实用程序实际上是用 VBScript 编写的，展示了该语言的强大功能。）作为额外内容，我们在下一页提供了清单 13-28。此脚本创建一个包含 IIS 服务器名称的文本文件，插入一个 IIS 命令行字符串，并针对文件中列出的每个 IIS 服务器执行该命令。这提供了对 Web 服务器场的批量管理，而无需学习任何 VBScript。

#### 清单 13-28 创建多 IIS 管理模板

```vb
Dim sCommand
sCommand = "INSERT IIS COMMAND HERE"

Dim sFile
sFile = "c:\ListOfIISservers.txt"

Dim oFSO, oTS
Set oFSO = CreateObject("Scripting.FileSystemObject")
On Error Resume Next
Set oTS = oFSO.OpenTextFile(sFile)
If Err <> 0 Then
    WScript.Echo Err.Description
    WScript.Echo "** Couldn't open " & sFile
    WScript.Quit
End If

Dim sServer, oShell, oExec, sCmd
Set oShell = CreateObject("WScript.Shell")
Do Until oTS.AtEndOfStream
    sServer = oTS.ReadLine
    sCmd = Replace(sCommand,"%name%",sServer)
    WScript.Echo "Running against " & sServer
    Set oExec = oShell.Exec(sCmd & " /s " & sServer)
    Do While oExec.Status = 0
        WScript.Sleep 100
    Loop
    WScript.Echo " Completed with exit code " & oExec.ExitCode
Loop
oTS.Close
WScript.Echo "Completed."
```

> **注意** 此脚本摘自 Don 的著作 *Windows Administrator's Automation Toolkit* (Microsoft Press, 2005)，该书解释了如何使用现成的工具和脚本自动化超过 100 个常见的 Windows 管理任务。

使用此脚本的诀窍是首先在单台计算机上测试你的 IIS 命令行任务。然后，在命令行文本中用 *%name%* 替换服务器名称。将命令行文本粘贴到此脚本中指示的位置（第 2 行）。然后创建一个文本文件（默认为 *C:\ListOfIISservers.txt*），就可以开始使用了。

> **更多信息** 更多 IIS 管理脚本（包括 IIS 5.0 的脚本）可在以下地址找到：
http://www.microsoft.com/technet/scriptcenter/scripts/iis/default.mspx
（此链接包含在随附光盘中；点击 *Script Repository-Internet Information Server*。）

### 管理打印

Windows XP 和 Windows Server 2003 包含一个新的 *Win32_Printer* 类，该类提供了一些出色的管理功能，用于管理打印队列、打印作业等。该类公开了可以暂停和恢复打印队列的方法。例如，清单 13-29 暂停一个打印队列（或使用正确的 Windows 术语称为*打印机*）。

#### 清单 13-29 暂停打印队列

```vb
Dim strServer, objWMI, strQueue, colPrinters, objPrinter
strServer = "."
strQueue = "HP LaserJet 5"
Set objWMI = GetObject("winmgmts:\\" & _
    strServer & "\\root\\cimv2")
Set colPrinters = objWMI.ExecQuery _
    ("SELECT * FROM win32_Printer WHERE Name = '" & _
    strQueue & "'")
For Each objPrinter In colPrinters
    objPrinter.Pause
Next
```

WQL 查询中的 *WHERE* 子句指定要检索的队列。然后，*colPrinters* 集合将只包含要暂停的类的一个实例。当然，如果你需要暂停目标服务器上的每个队列，只需删除 *WHERE* 子句即可。如编写的那样，此脚本影响本地计算机，但你可以更改 *strComputer* 变量来定位服务器。清单 13-30 只需将方法调用从 *Pause* 更改为 *Resume* 即可恢复打印队列。

#### 清单 13-30 恢复打印队列

```vb
Dim strServer, objWMI, strQueue, colPrinters, objPrinter
strServer = "."
strQueue = "HP LaserJet 5"
Set objWMI = GetObject("winmgmts:\\" & _
    strServer & "\\root\\cimv2")
Set colPrinters = objWMI.ExecQuery _
    ("SELECT * FROM win32_Printer WHERE Name = '" & _
    strQueue & "'")
For Each objPrinter In colPrinters
    objPrinter.Resume
Next
```

你也可以取消打印队列中的所有作业。如果服务器出现问题，这尤其有用。清单 13-31 与清单 13-29 和 13-30 类似，但它使用了不同的方法调用。此外，清单 13-31 已被修改为提示输入服务器和队列名称，使其成为更直接有用的管理工具。

#### 清单 13-31 取消打印队列中的作业

```vb
Dim strServer, objWMI, strQueue, colPrinters, objPrinter
strServer = InputBox("Server name to target?")
strQueue = InputBox("Name of queue?",,"HP LaserJet 5")
Set objWMI = GetObject("winmgmts:\\" & _
    strServer & "\\root\\cimv2")
Set colPrinters = objWMI.ExecQuery _
    ("SELECT * FROM win32_Printer WHERE Name = '" & _
    strQueue & "'")
For Each objPrinter In colPrinters
    objPrinter.CancelAllJobs
Next
```

> **提示** 你可能会问自己，为什么需要一个脚本来执行此操作，而 Windows 已经有了一个完全可以执行相同功能的图形用户界面。（事实上，Windows Server 2003 Release 2 提供了一个完整的打印管理控制台。）假设你希望你的帮助台能够删除打印队列中的作业，但又不想授予他们直接执行此操作的权限。你可以采用类似清单 13-31 中的脚本，将其打包（使用 iTripoli AdminScriptEditor 或 SAPIEN PrimalScript 4 Professional 等产品中可用的脚本打包工具），并在包中包含备用凭据。通过运行该包（一个独立的可执行文件），帮助台可以在没有必要权限的情况下访问脚本来执行此任务。

Win32_Printer 类还公开了许多描述打印设备功能的属性。例如，清单 13-32 显示打印设备的分辨率、分页功能、双面打印功能和名称。

#### 清单 13-32 检查打印设备功能

```vb
Dim strServer, objWMI, strQueue, colPrinters, objPrinter
strServer = "."
strQueue = "HP LaserJet 5"
Set objWMI = GetObject("winmgmts:\\" & _
    strServer & "\\root\\cimv2")
Set colPrinters = objWMI.ExecQuery _
    ("SELECT * FROM win32_Printer WHERE Name = '" & _
    strQueue & "'")
For Each objPrinter In colPrinters
    WScript.Echo " Printer: " & objPrinter.Name
    WScript.Echo "Collation: " & objPrinter.Collate
    WScript.Echo "Duplexing: " & objPrinter.Duplex
    WScript.Echo "Horiz res: " & _
        objPrinter.HorizontalResolution
    WScript.Echo " Vert res: " & _
        objPrinter.VerticalResolution
Next
```



你还可以将打印作业从一个设备重定向到另一个设备。为此，你需要知道原始设备和目标设备的名称。指定原始队列名称和作业应被重定向到的端口。

```
strQueue = "HP LaserJet 5"
strNewPort = "IP_192.168.0.25"
```

然后只需设置队列的 *PortName* 属性，并调用 *Put* 方法来保存更改。

```
objPrinter.PortName = strNewPort
objPrinter.Put_
```

清单 13-33 是完整的脚本。这是一个非常有用的工具；我们曾用它临时将队列重定向到同品牌型号的不同设备，确保用户在原设备离线时仍可打印。

```
清单 13-33 重定向打印队列
Dim strServer, objWMI, strQueue, colPrinters
Dim objPrinter, strNewPort
strServer = "."
strQueue = "HP LaserJet 5"
strNewPort = "IP_192.168.0.25"
Set objWMI = GetObject("winmgmts:\\" & _
    strServer & "\\root\\cimv2")
Set colPrinters = objWMI.ExecQuery _
    ("SELECT * FROM Win32_Printer WHERE Name = '" & _
    strQueue & "'")
For Each objPrinter In colPrinters
    objPrinter.PortName = strNewPort
    objPrinter.Put_
Next
```

Windows 还有一个名为 *Win32_TCPPrinterPort* 的 WMI 类，允许你在系统上创建、删除和修改 TCP/IP 打印机端口。这对于自动化配置组织中的新打印服务器非常有用。第三个类 *Win32_PrinterDriver* 提供打印设备驱动程序功能，允许你枚举已安装的驱动程序、安装新驱动程序以及删除不需要的驱动程序。这个类需要一些特殊处理，因此我们将快速演示如何安装新驱动程序。

你首先对想要安装驱动程序的服务器上的 WMI 服务建立标准 WMI 连接。使用 *Get* 方法而不是查询，这样你才能检索到 *Win32_PrinterDriver* 类本身，而不是现有的实例。

```
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\\\SERVER1\\root\\cimv2")
Set objDriver = objWMIService.Get("Win32_PrinterDriver")
```

注意，模拟指令可能不是必需的，因为它是默认设置，但安装打印机驱动程序是安全敏感任务，因此最好确保无误。要激活 LoadDriver 安全权限，请将其添加到 WMI 服务的安全对象（具体来说，是 Privileges 属性）。

```
objWMIService.Security_.Privileges.AddAsString _
    "SeLoadDriverPrivilege", True
```

接下来，指定驱动程序的名称和版本。这必须是服务器上物理安装或可访问的驱动程序名称——软件必须物理存在。对于随 Windows 附带的驱动程序，这很容易；对于其他驱动程序，你需要先复制它们。我们正在构建的这个脚本不会运行安装可执行文件；它期望软件已经位于正确的位置。

```
objDriver.Name = "HP LaserJet 5"
objDriver.SupportedPlatform = "windows NT x86"
objDriver.Version = "3"
```

还请注意，我们指定了 SupportedPlatform 属性。请记住，Windows 支持为打印设备安装多个驱动程序；这允许打印服务器托管客户端所需的驱动程序。这里，我们指定了 Windows NT x86，这涵盖了从 Windows NT 和 Windows 2000 起的大多数 Windows 版本。我们也可以指定 Windows IA64，例如，指定用于 Itanium 64 位系统的驱动程序。

我们使用 AddPrinterDriver 方法完成。本质上，我们是在要求我们创建的新实例将自身添加到系统中。这看起来有些奇怪，但效果很好。

```
errResult = objDriver.AddPrinterDriver(objDriver)
```

清单 13-34 是完整的脚本。

```
清单 13-34 添加打印机驱动程序
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\SERVER1\root\cimv2")
Set objDriver = objWMIService.Get("win32_PrinterDriver")
objWMIService.Security_.Privileges.AddAsString _
    "SeLoadDriverPrivilege", True
objDriver.Name = "HP LaserJet 5"
objDriver.SupportedPlatform = "windows NT x86"
objDriver.Version = "3"
errResult = objDriver.AddPrinterDriver(objDriver)
```

> **更多信息** 其他客户端打印管理脚本示例可在以下网址找到：
http://www.microsoft.com/technet/scriptcenter/scripts/printing/client/default.mspx
（此链接包含在随附 CD 上；点击客户端打印。）

### 使用 Windows 更新服务

Windows XP Service Pack 2 和 Windows Server 2003 Service Pack 1 引入了自动更新软件。（可在 Microsoft Update 网站 http://update.microsoft.com 上获取较新版本。）这个新软件对应于 Windows 软件更新服务 (WSUS) 服务器软件。虽然服务器软件主要为托管代码（如 VB.NET 和 C#）设计，但自动更新客户端现在通过一组 COM 对象公开，脚本可以轻松访问。这意味着你可以编写一个 VBScript 来管理 Windows XP 和 Windows Server 2003 计算机上的自动更新客户端。

最简单的情况下，你可能如清单 13-35 所示使用这个新功能。此清单只是将自动更新客户端的设置更改为在当地时间星期二凌晨 4:00 安装下载的更新。

```
清单 13-35 配置自动更新设置
Set objAutoUpdate = CreateObject("Microsoft.Update.AutoUpdate")
Set objSettings = objAutoUpdate.Settings
objSettings.ScheduledInstallationDay = 3
objSettings.ScheduledInstallationTime = 4
objSettings.Save
```

当然，因为此信息是通过 COM 对象而不是 WMI 公开的，从远程计算机执行此任务可能很复杂。你可以在 *CreateObject* 调用中指定远程计算机。

```
Set objAutoUpdate = _
CreateObject("Microsoft.Update.AutoUpdate", "\\Client2")
```

你也可以轻松地将这个简短的脚本放入分配给所有计算机的登录脚本中。这样，你可以确保这些设置始终生效。当然，自动更新客户端也可以通过组策略进行配置，因此你有多种方法来部署这些设置并确保客户端计算机自动更新。

下页的清单 13-36 展示了如何使用 *CreateObject* 函数在远程计算机上实例化 COM 对象。此脚本旨在连接到 Active Directory 中的每台计算机并显示其自动更新配置，包括通知级别、安装日期和时间等。（这是通过使用本章开头的包装脚本构建的。）

第三部分：高级脚本技术、工具和技术

```
清单 13-36 显示自动更新清单
' 需要 Windows XP Service Pack 2 或更高版本
' 连接到 AD 根
Dim rootDSE, domainObject
Set rootDSE=GetObject("LDAP://RootDSE")
domainContainer = rootDSE.Get("defaultNamingContext")
Set oDomain = GetObject("LDAP://" & domainContainer)

' 从域根开始
workwithObject(oDomain)

Sub workwithObject(oContainer)
Dim oADObject
For Each oADObject in oContainer
 Select Case oADObject.Class
 Case "computer"
 'oADObject 代表一个计算机对象；
 ' 对其执行某些操作
 wScript.Echo String(40,"-")
 wScript.Echo oADObject.cn
 On Error Resume Next
 Set objWU = CreateObject("Microsoft.Update.AutoUpdate", _
 "\\" & oADObject.cn)
 If Err <> 0 Then
 wScript.Echo Err.Description
 Else
 Set objSetting = objWU.Settings
 wScript.Echo "通知：" & objSetting.NotificationLevel
 wScript.Echo "只读：" & objSetting.ReadOnly
 wScript.Echo "必需：" & objSetting.Required
 wScript.Echo "安装时间：" & _
 objSetting.ScheduledInstallationDay
 wScript.Echo "安装日期：" & _
 objSetting.ScheduledInstallationTime
 End If
 Case "organizationalUnit" , "container"
 'oADObject 是一个 OU 或容器...
 ' 遍历其对象
 workwithObject(oADObject)
 End Select
Next
End Sub
```

当然，这个脚本效率不高，因为它一次只能连接一台计算机。此外，Windows 防火墙可能使此脚本根本无法工作。为帮助解决这两个问题，我们创建了清单 13-37。它旨在作为登录脚本部署，通过消除对传入远程连接的需求来绕过 Windows 防火墙。同时，性能也得到了提高，因为每台计算机执行自己的清单操作，并将信息写入文件服务器上的 Microsoft Access 数据库。（默认位置是 \\fileserver\share\wuinventory.mdb；你应该将其更改为合适的路径。）



**关于 CD** 我们在光盘中提供了一个名为 `wuinventory.mdb` 的空 Access 数据库，其中已设置好适当的表和列布局。您可以在光盘中找到它以及相关脚本。

```
清单 13-37 显示自动更新数据库清单
'假设所有客户端都已安装 Access 驱动程序
'假设 Access 数据库中有一个名为 Updates 的表
'假设表中包含 Name、Required、ReadOnly、
' Day 和 Time 列。所有列均假定为文本类型。

On Error Resume Next
Dim strCN, objWU, objSet, objNet, strComputer
Dim strSQL, objCN

'设置连接字符串
strCN = "Provider=Microsoft.Jet.Oledb.4.0;" & _
    "Data Source=\\fileserver\share\wuinventory.mdb;"

'打开 WU 对象
Set objWU = CreateObject("Microsoft.Update.AutoUpdate")
Set objSet = objWU.Settings
Set objNet = CreateObject("WScript.Network")

'获取计算机名称
strComputer = objNet.ComputerName

'打开数据库
Set objCN = CreateObject("ADODB.Connection")
objCN.Open strCN

'删除现有行
strSQL = "DELETE FROM Updates WHERE Name = '" & _
    strComputer & "')"
objCN.Execute strSQL

'构建新行
strSQL = "INSERT INTO Updates (Name,Required,ReadOnly" & _
    ",Day,Time) VALUES("
strSQL = strSQL & "'" & strComputer & "','"
strSQL = strSQL & "'" & objSet.Required & "','"
strSQL = strSQL & "'" & objSet.ReadOnly & "','"
strSQL = strSQL & "'" & objSet.ScheduledInstallationDay & "','"
strSQL = strSQL & "'" & objSet.ScheduledInstallationTime & "')"

'插入新行
objCN.Execute strSQL
objCN.Close
```

该脚本首先通过 OLE DB 连接字符串连接到数据库。

```
strCN = "Provider=Microsoft.Jet.Oledb.4.0;" & _
    "Data Source=\\fileserver\share\wuinventory.mdb;"
```

然后，脚本实例化自动更新客户端的 COM 对象并检索其设置。它还从 *WshNetwork* 对象获取本地计算机名称。

```
Set objWU = CreateObject("Microsoft.Update.AutoUpdate")
Set objSet = objWU.Settings
Set objNet = CreateObject("WScript.Network")
strComputer = objNet.ComputerName
```

打开数据库连接，并删除任何具有相同计算机名称的现有行。这确保每台计算机在数据库中只列出一次。

```
Set objCN = CreateObject("ADODB.Connection")
objCN.Open strCN

strSQL = "DELETE FROM Updates WHERE Name = '" & _
    strComputer & "')"
objCN.Execute strSQL
```

包含计算机名称和自动更新设置值的 SQL *INSERT* 语句被放置在一个字符串变量中。

```
strSQL = "INSERT INTO Updates (Name,Required,ReadOnly" & _
    ",Day,Time) VALUES(" 
strSQL = strSQL & "'" & strComputer & "',"
strSQL = strSQL & "'" & objSet.Required & "',"
strSQL = strSQL & "'" & objSet.Readonly & "',"
strSQL = strSQL & "'" & objSet.ScheduledInstallationDay & "',"
strSQL = strSQL & "'" & objSet.ScheduledInstallationTime & "')"
```

最后，执行 SQL 语句将计算机添加到数据库中，并关闭数据库连接。

```
objCN.Execute strSQL
objCN.Close
```

这样的脚本有助于“闭环”补丁管理；也就是说，它可以帮助确保每台计算机上的设置实际上确实按您希望的方式配置。如果您已集中配置这些设置，它们在网络中应保持一致。您可以通过打开 Access 数据库并滚动浏览表格来快速发现任何异常设置。

> **更多信息** TechNet 脚本中心包含其他 Windows 更新管理脚本，位于

http://www.microsoft.com/technet/scriptcenter/scripts/sus/client/default.mspx

（此链接包含在随附光盘中；请点击 *Windows Update Client-Side Management*。）

### 总结

Windows Server 2003 和 Windows XP 是迄今为止最易于访问的 Windows 版本，至少在基于脚本的管理方面是如此。利用您在本章中学到的技术，您可以编写大量原本繁琐或困难的管理任务的脚本，使管理变得更加轻松。为了帮助确保未来版本的 Windows 对基于脚本的管理更加开放，请与您所在地区的 Microsoft 办事处和其他 Microsoft 代表沟通，让他们知道您欣赏他们在使 Windows XP 和 Windows Server 2003 更易于脚本访问方面所做的工作。告诉他们，您期待未来版本能更进一步。希望未来涵盖 Windows 下一版本中脚本编写的本章版本篇幅足够大，能够填满整本书。

# 第 IV 部分

## 企业脚本

- 本部分包含：
  - 第 14 章：组策略管理脚本编写 ....................393
  - 第 15 章：Exchange 2003 脚本编写 .............................425
  - 第 16 章：Microsoft Operations Manager 2005 脚本编写 ........463
  - 第 17 章：Virtual Server 2005 脚本编写.......................483

# 第 14 章
组策略管理脚本编写

**本章内容：**

介绍组策略管理脚本编写 ……………………………… 394
脚本化 GPO 权限 ……………………………………………………………… 407
脚本化 GPO 报告 …………………………………………………………………… 411
脚本化 GPO 备份 …………………………………………………………………… 412
脚本化 GPO 还原 …………………………………………………………………… 412
脚本化策略结果集 ……………………………………………………… 413
查看 GPO 脚本实践 ………………………………………………………… 414
总结 …………………………………………………………………………………… 423

在大多数中大型企业中，组策略管理可能是一项全职工作。幸运的是，Microsoft Windows Server 2003 包含了组策略管理控制台。GPMC 对系统管理员来说是一个福音，而且它还附带了一个额外的好处——脚本接口。现在，可以使用 VBScript 管理组策略对象。我们将在本章中探讨 GPMC 脚本编写。

组策略是大多数企业通过迁移到 Microsoft Windows 2000 获得的主要好处之一。不幸的是，组策略的管理工具很弱。随着 Windows Server 2003 的到来，Microsoft 引入了一个全新的组策略管理控制台。使用它，您可以创建、备份、复制、移动和生成企业中所有 GPO 的报告。作为额外奖励，几乎所有功能也可以通过脚本接口获得。

> **注意** 我们假设您已经熟悉组策略管理控制台和一般的组策略。本章重点介绍如何使用 VBScript 管理组策略。

### 介绍组策略管理脚本编写

首先，让我们先说个坏消息。Microsoft 没有提供用于创建或编辑 GPO 的脚本接口。您无法编写脚本来禁用对控制面板的访问、从“开始”菜单中删除“运行”命令，或禁用注册表编辑工具。使用 GPMC 脚本编写，您可以做的是备份和还原 GPO、设置 GPO 权限、构建 GPO 报告，以及获取用户和计算机的策略结果集。

当您安装组策略管理控制台时，会在 `%ProgramFiles%\GPMC` 下创建一个 Scripts 文件夹。Microsoft 提供了超过 30 个优秀的脚本，您可以立即使用它们来管理企业中的组策略。这些脚本采用 WSF 格式，因此可以在运行时接受参数，例如组织单元名称。我们不会花时间详细讲解这些脚本，尽管我们可能会涵盖一些相同的核心功能。

> **注意** 组策略管理控制台包含在 Windows Server 2003 中，但也可以从以下地址免费下载

http://www.microsoft.com/windowsserver2003/gpmc/default.mspx

（此链接包含在随附光盘中；请点击 *Enterprise Management with Group Policy Management Console*。）

### 组策略管理脚本编写要求

要使用 GPMC，您必须运行 Windows Server 2003 或 Microsoft Windows XP，并且已安装 Microsoft .NET Framework。如果您仍在运行 XP SP1，则应安装知识库文章 Q326469 中引用的修补程序。GPMC 无法在 Microsoft Windows 2000 Professional 或 Microsoft Windows 2000 Server 上运行。但是，您可以使用 XP 桌面上的控制台来管理 Windows 2000 域中的组策略。当然，您需要适当的凭据，无论是域管理员身份还是通过委托。可以委托组策略管理权限。

> **最佳实践** 将 GPMC 安装在与承担 PDC 仿真器角色的域控制器位于同一站点的安全 Windows XP SP2 桌面上。

### 组策略管理控制台对象模型

GPMC 对象模型有点复杂，但幸运的是，文档非常齐全。图 14-1 展示了该对象模型。帮助文件和 MSDN 库中都有大量信息。不幸的是，许多文档是针对应用程序开发人员的，而不是希望开发 VBScript 的管理员。我们不会详细介绍完整的对象模型，但会探讨其基础知识。



## 第14章：组策略管理脚本

![GPMC 对象模型](img/4fefd6988ba5d4a92a65127617ca24c2_414_0.png)

图 14-1 GPMC 对象模型

**396  第四部分：企业脚本编写**

> **更多信息** GPMC 对象模型在帮助文件 `gpmc.chm` 中有文档说明，也可参见
> http://msdn.microsoft.com/library/default.asp?url=/library/en-us/gpmc/gpmc/
> gpmc_object_model.asp
> （此链接在配套光盘上；点击 *GPMC 对象模型*）。

你主要将使用 *GPM* 对象，其实例化方式如下：

```
set GPM=CreateObject("GPMGMT.GPM")
```

所有其他对象都从 *GPM* 对象创建。使用此对象模型，你可以执行以下操作：

-   备份、还原、导入和复制 GPO。
-   创建和删除 GPO 及 WMI 筛选器。
-   将 GPO 和 WMI 筛选器链接到组织单元、域和站点。
-   搜索 GPO。
-   报告 GPO 设置。
-   管理 GPO 权限和委托。
-   获取 GPO 的策略结果集。
-   创建和修改 GPO 迁移表。

我们将介绍大多数管理员需要了解的一些基础知识。

### 常量

正如你从对象模型中可能判断的那样，GPMC 脚本编写是一个复杂的主题，特别是在安全权限和访问控制列表方面。对象模型需要许多常量来定义属性（如 *PermGPOApply*）和方法（如 *get_ProcessSecurity*）。幸运的是，你不必在脚本开头定义每个常量。对象模型包含一个名为 *GPMConstants* 的对象。你需要在脚本开头使用 *GetConstants* 方法实例化此对象。

```
Set GPM=CreateObject("GPMGMT.GPM")
set gpmConstants=GPM.GetConstants
```

在编写示例脚本和阅读文档时，你会看到哪里需要不同的常量值。在使用 GPMC 脚本编写时，拥有一个能在你编码时显示 COM 对象属性和方法的脚本编辑器将是非常宝贵的。表 14-1 定义了方法常量，表 14-2 定义了属性常量。此信息也可通过 MSDN 和 GPMC 文档获取。

#### 表 14-1 GPMC 方法常量

| 方法常量 | 描述 |
|---|---|
| get_DestinationOptionByRelativeName | 获取与 opDestination-ByRelativeName 的 GPMDestinationOption 对应的常量值 |
| get_DestinationOptionNone | 获取与 opDestination-None 的 GPMDestinationOption 对应的常量值 |
| get_DestinationOptionBySameAsSource | 获取与 opDestination-SameAsSource 的 GPMDestinationOption 对应的常量值 |
| get_DestinationOptionSet | 获取与 opDestination-Set 的 GPMDestinationOption 对应的常量值 |
| get_EntryTypeComputer | 获取与 typeComputer 的 GPMEntryType 对应的常量值 |
| get_EntryTypeGlobalGroup | 获取与 typeGlobalGroup 的 GPMEntryType 对应的常量值 |
| get_EntryTypeLocalGroup | 获取与 typeLocalGroup 的 GPMEntryType 对应的常量值 |
| get_EntryTypeUniversalGroup | 获取与 typeUniversalGroup 的 GPMEntryType 对应的常量值 |
| get_EntryTypeUNCPath | 获取与 typeUNCPath 的 GPMEntryType 对应的常量值 |
| get_EntryTypeUnknown | 获取与 typeUnknown 的 GPMEntryType 对应的常量值 |
| get_EntryTypeUser | 获取与 typeUser 的 GPMEntryType 对应的常量值 |
| get_PermGPOApply | 获取与 permGPOApply 权限类型对应的常量值 |
| get_PermGPOCustom | 获取与 permGPOCustom 权限类型对应的常量值 |
| get_PermGPOEdit | 获取与 permGPOEdit 权限类型对应的常量值 |
| get_PermGPOEditSecurityAndDelete | 获取与 permGPOEditSecurityAndDelete 权限类型对应的常量值 |
| get_PermGPORead | 获取与 permGPORead 权限类型对应的常量值 |
| get_PermSOMGPOCreate | 获取与 permSOMGPOCreate 权限类型对应的常量值 |
| get_PermSOMLink | 获取与 permSOMLink 权限类型对应的常量值 |
| get_PermSOMLogging | 获取与 permSOMLogging 权限类型对应的常量值 |
| get_PermSOMPlanning | 获取与 permSOMPlanning 权限类型对应的常量值 |
| get_PermSOMWMICreate | 获取与 permSOMWMICreate 权限类型对应的常量值 |
| get_PermSOMWMIFullControl | 获取与 permSOMWMIFullControl 权限类型对应的常量值 |
| get_PermWMIFilterCustom | 获取与 permWMIFilterCustom 权限类型对应的常量值 |
| get_PermWMIFilterEdit | 获取与 permWMIFilterEdit 权限类型对应的常量值 |
| get_PermWMIFilterFullControl | 获取与 permWMIFilterFullControl 权限类型对应的常量值 |
| get_SearchPropertyBackupMostRecent | 获取与 backupMostRecent 搜索属性对应的常量值 |
| get_SearchPropertyGPODisplayName | 获取与 GPODisplayName 搜索属性对应的常量值 |
| get_SearchPropertyGPODomain | 获取与 GPODomain 搜索属性对应的常量值 |
| get_SearchPropertyGPOEffectivePermissions | 获取与 GPOEffectivePermissions 搜索属性对应的常量值 |
| get_SearchPropertyGPOID | 获取与 GPOID 搜索属性对应的常量值 |
| get_SearchPropertyGPOPermissions | 获取与 GPOPermissions 搜索属性对应的常量值 |
| get_SearchPropertyGPOUserExtensions | 获取与 GPOUserExtensions 搜索属性对应的常量值 |
| get_SearchPropertyGPOWMIFilter | 获取与 GPOWMIFilter 搜索属性对应的常量值 |
| get_SearchPropertySOMLinks | 获取与 somLinks 搜索属性对应的常量值 |
| get_SearchOpContains | 获取与 opContains 搜索运算符对应的常量值 |
| get_SearchOpEquals | 获取与 opEquals 搜索运算符对应的常量值 |
| get_SearchOpNotContains | 获取与 opNotContains 搜索运算符对应的常量值 |
| get_SearchOpNotEquals | 获取与 opNotEquals 搜索运算符对应的常量值 |
| get_SOMDomain | 获取与 *somDomain* SOM 类型对应的常量值 |
| get_SOMOU | 获取与 *somOU* SOM 类型对应的常量值 |
| get_SOMSite | 获取与 *somSite* SOM 类型对应的常量值 |
| get_DoNotValidateDC | 获取 *DoNotValidateDC* 属性的值 |
| get_SecurityFlags | 获取 *SecurityFlags* 属性的值 |
| get_UseAnyDC | 获取与 *UseAnyDC* 属性对应的常量值 |
| get_DoNotUseW2KDC | 获取与 *DoNotUseW2KDC* 属性对应的常量值 |
| get_UsePDC | 获取与 *UsePDC* 属性对应的常量值 |
| get_SearchPropertyGPOComputerExtensions | 获取与 *GPOComputerExtensions* 搜索属性对应的常量值 |
| get_ReportHTML | 获取与 *ReportHTML* 属性对应的常量值 |
| get_ReportXML | 获取与 *ReportXML* 属性对应的常量值 |
| get_RSOPModeUnknown | 获取与 *RSOPModeUnknown* 属性对应的常量值 |
| get_RSOPModePlanning | 获取与 *RSOPModePlanning* 属性对应的常量值 |
| get_RSOPModeLogging | 获取与 *RSOPModeLogging* 属性对应的常量值 |
| get_RSOPLoggingNoComputer | 获取与 *RsopLoggingNoComputer* 属性对应的常量值 |
| get_RSOPLoggingNoUser | 获取与 *RsopLoggingNoUser* 属性对应的常量值 |
| get_RSOPPlanningAssumeSlowLink | 获取与 *RSOP_PLANNING_ASSUME_SLOW_LINK* 属性对应的常量值 |
| get_RSOPPlanningLoopbackOption | 获取与 *RsopPlanningLoopbackOption* 属性对应的常量值 |
| get_RSOPPlanningAssumeUserWQLFilterTrue | 获取与 *RsopPlanningAssumeUserWQLFilterTrue* 属性对应的常量值 |



## 400 第四部分：企业级脚本编写

#### 表 14-1 GPMC 方法常量

| 方法常量 | 描述 |
|---|---|
| get_RSOPPlanningAssumeCompWQLFilterTrue | 检索与 RsopPlanningAssumeCompWQLFilterTrue 属性对应的常量值 |
| get_MigrationTableOnly | 检索与 MigrationTableOnly 属性对应的常量值 |
| get_ProcessSecurity | 检索与 ProcessSecurity 属性对应的常量值 |

#### 表 14-2 GPMC 属性常量

| 属性常量 | 描述 |
|---|---|
| DestinationOptionByRelativeName | 与 GPMDestinationOption of opDestinationByRelativeName 对应的值 |
| DestinationOptionNone | 与 GPMDestinationOption of opDestinationNone 对应的值 |
| DestinationOptionSameAsSource | 与 GPMDestinationOption of opDestinationSameAsSource 对应的值 |
| DestinationOptionSet | 与 GPMDestinationOption of opDestinationSet 对应的值 |
| DoNotUseW2KDC | 与 DoNotUseW2KDC 属性对应的常量值 |
| DoNotValidateDC | 与 DoNotValidateDC 属性对应的常量值 |
| EntryTypeComputer | 与 GPMEntryType of type-Computer 对应的值 |
| EntryTypeGlobalGroup | 与 GPMEntryType of type-GlobalGroup 对应的值 |
| EntryTypeLocalGroup | 与 GPMEntryType of type-LocalGroup 对应的值 |
| EntryTypeUNCPath | 与 GPMEntryType of type-UNCPath 对应的值 |
| EntryTypeUniversalGroup | 与 GPMEntryType of type-UniversalGroup 对应的值 |
| EntryTypeUnknown | 与 GPMEntryType of type-Unknown 对应的值。 |
| EntryTypeUser | 与 GPMEntryType of type-User 对应的值 |
| MigrationTableOnly | 与 GPM_MIGRATIONTABLE_ONLY 常量对应的值 |
| PermGPOApply | 与 permGPOApply 权限类型对应的常量值 |
| PermGPOCustom | 与 permGPOCustom 权限类型对应的常量值 |
| PermGPOEdit | 与 permGPOEdit 权限类型对应的常量值 |
| PermGPOEditSecurityAndDelete | 与 permGPOEdit-SecurityAndDelete 权限类型对应的常量值 |
| PermGPORead | 与 permGPORead 权限类型对应的常量值 |
| PermSOMGPOCreate | 与 permSOMGPO-Create 权限类型对应的常量值 |
| PermSOMLink | 与 permSOMLink 权限类型对应的常量值 |
| PermSOMLogging | 与 permSOMLogging 权限类型对应的常量值 |
| PermSOMPlanning | 与 permSOM-Planning 权限类型对应的常量值 |
| PermSOMWMICreate | 与 permSOMWMI-Create 权限类型对应的常量值 |
| PermSOMWMIFullControl | 与 permSOMWMI-FullControl 权限类型对应的常量值 |
| PermWMIFilterCustom | 与 permWMIFilter-Custom 权限类型对应的常量值 |
| PermWMIFilterEdit | 与 permWMIFilter-Edit 权限类型对应的常量值 |
| PermWMIFilterFullControl | 与 permWMIFilter-FullControl 权限类型对应的常量值 |
| ProcessSecurity | 与 GPM_PROCESS_SECURITY 常量对应的值 |
| ReportHTML | 与 ReportHTML 属性对应的常量值 |
| ReportXML | 与 ReportXML 属性对应的常量值 |
| RSOPLoggingNoComputer | 与 RSOP_NO_COMPUTER 常量对应的值 |
| RSOPLoggingNoUser | 与 RSOP_NO_USER 常量对应的值 |
| RSOPModeLogging | 与 RSOPMode-Logging 属性对应的常量值 |
| RSOPModePlanning | 与 RSOPMode-Planning 属性对应的常量值 |
| RSOPModeUnknown | 与 RSOPMode-Unknown 属性对应的常量值 |
| RSOPPlanningAssumeCompWQLFilterTrue | 与 RSOP_PLANNING_ASSUME_COMP_WQLFILTER_TRUE 常量对应的值 |
| RSOPPlanningAssumeSlowLink | 与 RSOP_PLANNING_ASSUME_SLOW_LINK 常量对应的值 |
| RSOPPlanningAssumeUserWQLFilterTrue | 与 RSOP_PLANNING_ASSUME_USER_WQLFILTER_TRUE 常量对应的值 |
| RSOPPlanningLoopbackOption | 如果 vbMerge 为 VARIANT_TRUE，则与 RSOP_PLANNING_ASSUME_LOOPBACK_MERGE 常量对应的值；如果 vbMerge 为 VARIANT_FALSE，则与 RSOP_PLANNING_ASSUME_LOOPBACK_REPLACE 常量对应的值 |
| SearchOpContains | 与 opContains 搜索运算符对应的常量值 |
| SearchOpEquals | 与 opEquals 搜索运算符对应的常量值 |
| SearchOpNotContains | 与 opNotContains 搜索运算符对应的常量值 |
| SearchOpNotEquals | 与 opNotEquals 搜索运算符对应的常量值 |
| SearchPropertyBackupMostRecent | 与 backupMostRecent 搜索属性对应的常量值 |
| SearchPropertyGPOComputerExtensions | 与 GPOComputerExtensions 搜索属性对应的常量值 |
| SearchPropertyGPODisplayName | 与 GPODisplayName 搜索属性对应的常量值 |
| SearchPropertyGPODomain | 与 GPODomain 搜索属性对应的常量值 |
| SearchPropertyGPOEffectivePermissions | 与 GPOEffectivePermissions 搜索属性对应的常量值 |
| SearchPropertyGPOID | 与 GPOID 搜索属性对应的常量值 |
| SearchPropertyGPOPermissions | 与 GPOPermissions 搜索属性对应的常量值 |
| SearchPropertyGPOUserExtensions | 与 GPOUserExtensions 搜索属性对应的常量值 |
| SearchPropertyGPOWMIFilter | 与 GPOWMIFilter 搜索属性对应的常量值 |
| SearchPropertySOMLinks | 与 somLinks 搜索属性对应的常量值 |
| SecurityFlags | 表示要为 GPO 检索或设置的安全描述符部分。调用 IGPMGPO::GetSecurityDescriptor 和 IGPMGPO::SetSecurityDescriptor 函数（GPMGPO.GetSecurityDescriptor 和 GPMGPO.SetSecurityDescriptor 方法）需要这些值。 |
| SOMDomain | 与 somDomain SOM 类型对应的常量值 |
| SOMOU | 与 somOU SOM 类型对应的常量值 |
| SOMSite | 与 somSite SOM 类型对应的常量值 |
| UseAnyDC | 与 UseAnyDC 属性对应的常量值 |
| UsePDC | 与 UsePDC 属性对应的常量值 |

## 第 14 章：组策略管理脚本编写

清单 14-1 展示了 GPMC 常量。此脚本搜索当前域并列出所有组策略对象。

### 清单 14-1 列出所有组策略对象

```vb
Dim GPM, gpmConstants, gpmDomain
Dim collGPOS, gpmSearchCriteria, gpo, gpmResult
Dim RootDSE, objDomain

Set GPM = CreateObject("GPMGMT.GPM")
Set gpmConstants = GPM.GetConstants
strFQDN = GetDomainFQDN

Set gpmDomain = GPM.GetDomain(strFQDN, "", gpmConstants.UseAnyDC)

Set gpmSearchCriteria = GPM.CreateSearchCriteria
Set collGPOS = gpmDomain.SearchGPOs(gpmSearchCriteria)
WScript.Echo "Found " & collGPOS.Count & " group policy objects in " & _
    gpmDomain.Domain & "(" & gpmDomain.DomainController & ")"
For Each gpo In collGPOS
    WScript.Echo gpo.DisplayName & " [" & gpo.Path & "]"
Next

WScript.Quit

'************************************************
Function GetDomainFQDN()
    Set RootDSE = GetObject("LDAP://RootDSE")
    DomainPath = RootDSE.Get("DefaultNamingContext")
    DomainPath = Replace(DomainPath, "DC=", "")
    GetDomainFQDN = Replace(DomainPath, ",", ".")
End Function
```

脚本首先实例化 *GPM* 和 *GPMConstants* 对象。

```vb
Set GPM = CreateObject("GPMGMT.GPM")
Set gpmConstants = GPM.GetConstants
```

要搜索域，我们需要知道域的完全限定名，例如 *company.pri*。我们编写了一个函数，它从默认命名上下文中获取域路径并将其转换为完全限定域名（FQDN）。换句话说，该函数会将 *DC=company,DC=pri* 转换为 *company.pri*。



# 第四部分：企业级脚本编写

```vb
Function GetDomainFQDN()
  set RootDSE=GetObject("LDAP://RootDSE")
  DomainPath= RootDSE.Get("DefaultNamingContext")
  DomainPath=Replace(DomainPath,"DC=","")
  GetDomainFQDN=Replace(DomainPath,",",".")
End Function
```

有了这些信息，我们就可以使用 `GetDomain` 方法连接到域并创建一个 `gpmDomain` 对象。

```vb
set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UseAnyDC)
```

如你所见，该方法接受多个参数。第一个是域的完全限定域名（FQDN），我们已通过函数获取。第二个参数（在我们的示例中为空）用于指定要连接到的特定域控制器。因为我们希望脚本能在任何域中运行，所以将其留空。不过，这意味着我们可以使用第三个参数来指定如何查找域控制器。此标志由一个常量设置。我们可以使用 `gpmConstants.UseAnyDC` 来引用 `GPM_USE_ANYDC` 常量，否则我们就必须自己定义它。顺便提一下，我们也可以使用 `gpmConstants.UsePDC` 来指定连接到 PDC 模拟器。

脚本接下来实例化一个 `gpmSearchCriteria` 对象（我们将在本章稍后介绍）。然后我们调用 `SearchGPOS` 方法来实例化一个 GPO 集合对象。

```vb
set gpmSearchCriteria=GPM.CreateSearchCriteria
set collGPOS=gpmDomain.SearchGPOs(gpmSearchCriteria)
```

有了这个集合对象，我们现在可以遍历并显示集合成员的信息，这些成员将是来自对象模型的 GPO 对象。

```vb
wscript.Echo "Found " & collGPOS.Count & " group policy objects in " &_
gpmDomain.Domain & "(" & gpmDomain.DomainController & ")"
For Each gpo In collGPOS
    WScript.Echo gpo.Displayname & " [" & gpo.path & "]"
Next
```

当你在命令提示符下使用 CScript 运行脚本时，你应该会看到类似的输出。

```
Found 5 group policy objects in company.pri(DC02.company.pri)
Test Security [cn={20029756-EC91-44FB-B57C-87A9A5584880},cn=policies,cn=system,DC=matrix,DC=local]
Default Domain Policy [cn={31B2F340-016D-11D2-945F-00C04FB984F9},cn=policies,cn=system,DC=matrix,DC=local]
New Group Policy Object [cn={4962C921-BCFC-4B22-BF39-8746D9CD8536},cn=policies,cn=system,DC=matrix,DC=local]
Default Domain Controllers Policy [cn={6AC1786C-016F-11D2-945F-00C04FB984F9},cn=policies,cn=system,DC=matrix,DC=local]
Desktop Restrictions [cn={B171DED9-C308-45C5-A1B5-48494C0B6DB5},cn=policies,cn=system,DC=matrix,DC=local]
```

## 第14章：组策略管理脚本

### 管理范围

GPMC 脚本中的另一个重要概念是*管理范围* (Scope of Management, SOM)。一个 SOM 是一个站点、域或组织单元 (OU)，其上链接了一个或多个 GPO。单个 GPO 可以链接到一个或多个 SOM。清单 14-2 扩展了清单 14-1 中的脚本，以查找特定 GPO 链接到的所有 SOM，并显示该信息。

```vb
清单 14-2 列出所有组策略对象及其 SOM 链接

Dim GPM, gpmConstants, gpmDomain
dim collGPOs, gpmSearchCriteria, collSOMs
dim RootDSE, objDomain

Set GPM=CreateObject("GPMGMT.GPM")
set gpmConstants=GPM.GetConstants
strFQDN=GetDomainFQDN

set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UsePDC)
set gpmSearchCriteria=GPM.CreateSearchCriteria
set collGPOs=gpmDomain.SearchGPOs(gpmSearchCriteria)

wscript.Echo "Found " & collGPOs.Count & " group policy objects in " &_
gpmDomain.Domain & " (" & gpmDomain.DomainController & ")"
For Each gpo In collGPOs
    WScript.Echo gpo.Displayname & " [" & gpo.id & "]"
    gpmSearchCriteria.Add gpmConstants.SearchPropertySOMLinks,_
    gpmConstants.SearchOpContains, gpo
    Set collSOMs=gpmDomain.SearchSOMs(gpmSearchCriteria)
    WScript.Echo "Linked to " & collSOMs.Count & " container(s)"
    If collSOMs.Count>0 Then
        For Each gpmSOM In collSOMs
            Select Case gpmSOM.Type
                Case gpmConstants.SOMSite
                    WScript.Echo vbtab & "Site:" & gpmSOM.Name
                Case gpmConstants.SOMDomain
                    WScript.Echo vbTab & "Domain:" & gpmSOM.Name
                Case gpmConstants.SOMOU
                    WScript.Echo vbTab & "OU:" &gpmSOM.Name
            End Select
        Next
    End if
Next

wScript.Quit

'**************************************************************
Function GetDomainFQDN()
    set RootDSE=GetObject("LDAP://RootDSE")
    DomainPath= RootDSE.Get("DefaultNamingContext")
    DomainPath=Replace(DomainPath,"DC=","")
    GetDomainFQDN=Replace(DomainPath,",",".")
End Function
```

由于此脚本与清单 14-1 非常相似，让我们重点关注新增内容。获取 GPO 集合后，我们可以枚举该集合并获取单个 *GPO* 对象。我们正在显示 GPO 的显示名称及其 GUID。

```vb
For Each gpo In collGPOS
    WScript.Echo gpo.Displayname & " [" & gpo.id & "]"
```

我们将使用 *gpmDomain* 对象的 *searchSOMS* 方法来搜索 SOM 链接。然而，这需要搜索条件。虽然搜索 GPO 不需要条件，但我们需要通过使用 *Add* 方法来指定搜索 SOM 链接的条件。当我们添加搜索条件时，其格式为 *属性, 操作, 值*。前两个参数由 *gpmConstant* 指定。

```vb
For Each gpo In collGPOS
    WScript.Echo gpo.Displayname & " [" & gpo.id & "]"
    gpmSearchCriteria.Add gpmConstants.SearchPropertySOMLinks,_
        gpmConstants.SearchopContains,gpo
    Set collSOMs=gpmDomain.SearchSoms(gpmSearchCriteria)
```

此代码片段添加了使用 *包含* 操作来搜索 SOM 链接的条件。我们使用 *gpmDomain* 对象的 *searchSOMS* 方法创建一个 SOM 的集合。我们现在可以枚举这个 SOM 集合。

```vb
WScript.Echo "Linked to " & collSOMs.count & " container(s)"
    If collSOMs.Count>0 Then
        For Each gpmSOM In collSOMs
            Select Case gpmSOM.Type
                Case gpmConstants.SOMSite
                    WScript.Echo vbtab & "Site:" & gpmSOM.Name
                Case gpmConstants.SOMDomain
                    WScript.Echo vbTab & "Domain:" & gpmSOM.Name
                Case gpmConstants.SOMOU
                    WScript.Echo vbTab & "OU:" & gpmSOM.Name
            End Select
        Next
    End if
```

集合中的每个成员都是一个 SOM 对象，我们可以返回 SOM 的名称以及 SOM 的类型——OU、域或站点。这是另一个可以使用 *gpmConstants* 的例子。*gpmSOM.Type* 属性返回一个数字常量，除非你知道它的含义，否则它几乎没有意义。我们可以在 *Select Case* 语句中使用 *SOMSite*、*SOMDomain* 和 *SOMOU* 常量属性。以下是清单 14-2 的示例输出。

```
Found 5 group policy objects In company.pri(DC02.company.pri)
Test Security [{20029756-EC91-44FB-B57C-87A9A5584880}]
Linked to 1 container(s)
    OU:TestingOU
Default Domain Policy [{31B2F340-016D-11D2-945F-00C04FB984F9}]
Linked to 1 container(s)
    Domain:company.pri
New Group Policy Object [{4962C921-BCFC-4B22-BF39-8746D9CD8536}]
Linked to 0 container(s)
Default Domain Controllers Policy [{6AC1786C-016F-11D2-945F-00C04fB984F9}]
Linked to 1 container(s)
    OU:Domain Controllers
Desktop Restrictions [{B171DED9-C308-45C5-A1B5-48494C0B6DB5}]
Linked to 1 container(s)
    OU:TestingOU
```

### GPO 权限的脚本编写

GPMC 对象模型通过权限对象提供了对 GPO 权限的访问。*gpmGPO* 对象具有 *GetSecurityInfo* 方法，该方法返回一个 *gpmPermission* 对象集合。这些对象提供了一个接口，用于返回有关受托者（即持有特定权限的帐户）的信息。

清单 14-3 中的脚本在我们一直用来显示域中所有 GPO 的脚本基础上，增加了一个用于显示权限的部分。

```vb
清单 14-3 列出 GPO 权限
Dim GPM,gpmConstants,gpmDomain
dim collGPOs,gpmSearchCriteria,gpo
Dim gpmResult,gpmSecurityInfo,gpmPerm
dim RootDSE,objDomain

set GPM=CreateObject("GPMGMT.GPM")
set gpmConstants=GPM.GetConstants
strFQDN=GetDomainFQDN

set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UseAnyDC)

set gpmSearchCriteria=GPM.CreateSearchCriteria
set collGPOs=gpmDomain.SearchGPOs(gpmSearchCriteria)
wscript.Echo "Found " & collGPOs.Count & " group policy objects in " &_
gpmDomain.Domain & "(" & gpmDomain.DomainController & ")"

For Each gpo In collGPOs
    WScript.Echo gpo.Displayname
    set gpmSecurityInfo=gpo.GetSecurityInfo
    wscript.Echo gpmSecurityInfo.Count & " permission objects"
    For Each gpmPerm In gpmSecurityInfo
        Select Case gpmPerm.permission
            Case gpmConstants.permGPOApply
                WScript.Echo vbTab & "GPO Applies"
                wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
            Case gpmConstants.permGPOCustom
                WScript.Echo vbTab & "GPO Custom"
                wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
            Case gpmConstants.permGPOEdit
                WScript.Echo vbTab & "GPO Edit"
                wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
            Case gpmConstants.permGPORead
                WScript.Echo vbTab & "GPO Read"
```



# 第四部分：企业级脚本编写

```
wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPOEditSecurityAndDelete
    WScript.Echo vbTab & "GPO 编辑安全"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case Else
    WScript.Echo vbTab & gpmPerm.Permission
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
End select
next
Next

WScript.Quit

'*********************************************************
Function GetDomainFQDN()
set RootDSE=GetObject("LDAP://RootDSE")
DomainPath= RootDSE.Get("DefaultNamingContext")
DomainPath=Replace(DomainPath,"DC=","")
GetDomainFQDN=Replace(DomainPath,",",".")
End Function

'*********************************************************
Function ListTrustees(gpmPerm)
On Error Resume Next
    If gpmPerm.Trustee.TrusteeDSPath="" Then
        ListTrustees= gpmPerm.Trustee.TrusteeName
    Else
        ListTrustees= gpmPerm.Trustee.TrusteeName & " [" & _
            gpmPerm.Trustee.TrusteeDSPath & "]"
    End If
End Function
```

对于每个 GPO 对象，我们通过调用 *GetSecurityInfo* 方法创建一个 `gpmSecurityInfo` 对象。

```
set gpmSecurityInfo=gpo.GetSecurityInfo
```

接下来，我们遍历 *gpmSecurityInfo* 中的每个权限对象，首先通过查看 *Permission* 属性来确定它属于哪种权限类型。

```
select Case gpmPerm.permission
```

正如你在 *Select Case* 语句中看到的，我们再次使用 `gpmConstants` 对象来比较对应于不同权限类型的值。如果不这样做，我们看到的只会像 6547 这样的数字，那将相当没有意义。

```
Case gpmConstants.permGPOApply
    WScript.Echo vbTab & "GPO 应用"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPOCustom
    WScript.Echo vbTab & "GPO 自定义"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPOEdit
    wScript.Echo vbTab & "GPO 编辑"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPORead
    WScript.Echo vbTab & "GPO 读取"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPOEditSecurityAndDelete
    WScript.Echo vbTab & "GPO 编辑安全"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case Else
    WScript.Echo vbTab & gpmPerm.Permission
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
End select
```

## 第 14 章：组策略管理脚本

```
Case gpmConstants.permGPOEdit
    wScript.Echo vbTab & "GPO 编辑"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPORead
    WScript.Echo vbTab & "GPO 读取"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case gpmConstants.permGPOEditSecurityAndDelete
    WScript.Echo vbTab & "GPO 编辑安全"
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
Case Else
    WScript.Echo vbTab & gpmPerm.Permission
    wscript.Echo vbTab & vbTab & ListTrustees(gpmPerm)
End select
```

为了获取每个权限的委托人信息，我们调用了一个函数，该函数返回委托人的名称以及目录服务路径（如果存在）。当你运行脚本时，你会得到如下输出。

```
在 company.pri(DC02.company.pri) 中找到 5 个组策略对象
Test Security
5 个权限对象
    GPO 编辑安全
        Domain Admins [CN=Domain Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        Enterprise Admins [CN=Enterprise Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        SYSTEM
    GPO 应用
        Authenticated Users
    GPO 读取
        ENTERPRISE DOMAIN CONTROLLERS
Default Domain Policy
5 个权限对象
    GPO 编辑安全
        Domain Admins [CN=Domain Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        Enterprise Admins [CN=Enterprise Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        SYSTEM
    GPO 应用
        Authenticated Users
    GPO 读取
        ENTERPRISE DOMAIN CONTROLLERS
New Group Policy Object
5 个权限对象
    GPO 编辑安全
        Domain Admins [CN=Domain Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        Enterprise Admins [CN=Enterprise Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        SYSTEM
    GPO 应用
        Authenticated Users
    GPO 读取
        ENTERPRISE DOMAIN CONTROLLERS
Default Domain Controllers Policy
5 个权限对象
    GPO 编辑安全
        Domain Admins [CN=Domain Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        Enterprise Admins [CN=Enterprise Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        SYSTEM
    GPO 应用
        Authenticated Users
    GPO 读取
        ENTERPRISE DOMAIN CONTROLLERS
Desktop Restrictions
5 个权限对象
    GPO 编辑安全
        Domain Admins [CN=Domain Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        Enterprise Admins [CN=Enterprise Admins,CN=Users,DC=company,DC=pri]
    GPO 编辑安全
        SYSTEM
    GPO 应用
        Authenticated Users
    GPO 读取
        ENTERPRISE DOMAIN CONTROLLERS
```

设置权限相对容易。你需要使用 `CreatePermission` 方法来创建一个新的权限对象。该方法需要三个参数。

- 你授予权限的委托人名称。通常，这类似于 `Company\SalesUsers`。
- 权限类型。使用 `gpmConstants` 对象，以便你可以指定 `permGPOApply`、`permGPORead`、`permGPOEdit` 或 `permGPOEditSecurityAndDelete`。
- 一个布尔值，指示权限是否可继承。

最终你会得到一行类似这样的代码。

```
Set GPM = CreateObject("GPMgmt.GPM")
set gpmConstants=GPM.GetConstants
Set gpmPermission=GPM.CreatePermission("Company\SalesUsers",
gpmConstants.GPOApply,True)
```

> **提示** 你可以使用此方法将权限应用于 GPO、SOM 或 WMI 筛选器。有关可以设置的权限类型的详细信息，请查看文档。

权限对象创建后，使用 `gpmSecurityInfo` 对象中的 `Add` 方法来设置权限。

```
set gpmSecurityInfo=gpo.GetSecurityInfo
gpmSecurityInfo.Add gpmPermission
```

### GPO 报告脚本

GPO 管理的一项重大改进是添加了 GPO 配置报告。你可以使用 GPO 配置许多项目，但以前总是很难看到哪些设置实际被配置了。组策略管理控制台包含一个报告查看器和一个将报告保存到文件的菜单命令。我们也可以非常轻松地从命令行执行这些任务。

GPO 对象有一个名为 *GenerateReportToFile* 的方法。该方法接受一个参数，指示报告应该是 HTML 格式还是 XML 格式。同样，我们可以使用 *gpmConstants* 对象来指定常量，其名称更易于使用，例如 *gpmConstants.ReportHTML* 或 *gpmConstants.ReportXML*。另一个参数只是报告应保存的文件名和路径。清单 14-4 获取我们的 GPO 枚举脚本，并使用 GPO 显示名称作为文件名的一部分，为每个 GPO 生成一份 HTML 报告。

```
清单 14-4 生成 GPO 报告
'GPOMasterSummary.vbs
Dim GPM,gpmConstants,gpmDomain
dim collGPOS,gpmSearchCriteria,gpo
dim RootDSE,objDomain

set GPM=CreateObject("GPMGMT.GPM")
set gpmConstants=GPM.GetConstants

strFQDN=GetDomainFQDN

set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UseAnyDC)
set gpmSearchCriteria=GPM.CreateSearchCriteria
set collGPOS=gpmDomain.SearchGPOs(gpmSearchCriteria)

wscript.Echo "Found " & collGPOS.Count & " group policy objects in " &
gpmDomain.Domain & "(" & gpmDomain.DomainController & ")"

For Each gpo In collGPOS
    wScript.Echo gpo.Displayname & " [" & gpo.path & "]"
    gpo.GenerateReportToFile gpmConstants.ReportHTML, gpo.Displayname &
    ".html"
Next

WScript.Quit

'******************************************************
Function GetDomainFQDN()
    set RootDSE=GetObject("LDAP://RootDSE")
    DomainPath= RootDSE.Get("DefaultNamingContext")
    DomainPath=Replace(DomainPath,"DC=","")
    GetDomainFQDN=Replace(DomainPath,",",".")
End Function
```

### GPO 备份脚本

一项常见的 GPO 管理任务是备份 GPO。在编辑 GPO 之前，这是一个显而易见的最佳实践；它可以确保你拥有策略的良好版本，以防你需要恢复它。你可能还想运行一个定期备份 GPO 的任务。这可以通过 `gpmGPO` 对象的 *Backup* 方法来完成。

该方法需要备份文件夹的路径。该文件夹必须已经存在，否则方法将失败。你还可以指定要与备份关联的注释。

```
Set gpmResult=gpmGPO.Backup("d:\backups\SalesDesktop-bkup", "baseline")
```

执行时，该方法会创建一个 `gpmResult` 对象，你可以通过调用 *OverAllStatus* 方法来检查备份的状态。如果在备份期间没有错误，该方法返回错误代码 0；否则，它返回一个失败错误代码。

```
gpmResult.overAllStatus
if err.number<>0 then
    wscript.echo "Backup failed"
else
    wscript.echo "Backup successful"
end if
```

> **故障排除** 如果你的备份命令不起作用，请确保文件夹路径存在并且你有权限。不要在路径中包含尾部反斜杠 (\)。如果你不包含注释，你必须至少为第二个参数包含两个双引号 ("")。

`gpmResult` 对象的另一个有用特性是其 *Result* 方法将返回有关隐式创建的 `gpmBackup` 对象的信息。因此，我们可以扩展我们的代码片段。

```
gpmResult.overAllStatus
if err.number<>0 then
    wscript.echo "Backup failed"
else
    wscript.echo "Backup successful"
    Set gpmBackup=gpmResult.Result
    wScript.Echo "Backed up " & gpmBackup.GPODisplayName &
        "to " & gpmBackup.BackupDir & "\" & gpmBackup.ID
end if
```

### GPO 恢复脚本

恢复 GPO 比备份稍复杂一些。你必须使用 `gpmDomain` 对象的 *RestoreGPO* 方法。此外，你只能将 GPO 恢复到它被创建的域。该方法需要一个对 `gpmBackup` 对象的引用以及一个恢复标志



用于域控制器验证。如果值为0，该方法会验证域控制器是否能执行还原操作。你也可以使用 *gpmConstant* 对象的 *DoNotValidateDC* 属性来跳过验证。

> **最佳实践** Microsoft 建议你始终进行验证，尤其是在使用软件策略设置时。应将包含软件策略设置的组策略对象还原到 Windows 2003 域控制器，以最大程度减少对客户端的影响。你也可以还原到 Windows 2000 域控制器，但用户可能需要重新安装软件。

当然，在还原备份之前，你需要先找到它。你可以使用 *gpmBackupDir* 对象的 *Search-Backups* 方法。

```vbs
strBackupDir="c:\\backups"
Set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UseAnyDC)
Set gpmSearchCriteria=GPM.CreateSearchCriteria
Set gpmBackupDir=GPM.GetBackupDir(strBackupDir)
Set collBackups=gpmBackupDir.SearchBackups(gpmSearchCriteria)
WScript.Echo collBackups.count & " Backups found in " & strBackupDir
For Each gpmBackup In collBackups
    WScript.Echo "ID:" & gpmBackup.ID
    WScript.Echo " Name:" & gpmBackup.GPODisplayName
    WScript.Echo " Comment:" & gpmBackup.Comment
    WScript.Echo " Backed up:" & gpmBackup.TimeStamp
Next
```

这将返回一个 *gpmBackup* 对象的集合。上面的代码片段只是列出了所有可用的备份。在添加了你的代码以确定要还原的备份后，你只需添加这段代码片段。

```vbs
Set gpmResult=gpmDomain.RestoreGPO(gpmBackup,0)
```

你可以使用 *gpmResult* 对象来验证还原，其方式与我们之前验证备份方法时类似。

### 脚本化策略结果集

组策略管理控制台包含一个出色的规划和故障排除工具，称为策略结果集 (RSOP)。该工具可以计算在用户会话期间可能已应用的所有策略的最终结果。你可以在两种模式下使用 RSOP：规划和日志记录。在规划模式下，RSOP 模拟某些用户、计算机、组成员身份和管理单元组合的结果。在日志记录模式下，RSOP 检查实际用户和计算机会话的结果。无论在哪种模式下，你都可以生成一个漂亮的 HTML 报告，以查看应用了哪些设置以及来自哪些 GPO。

GPMC 对象模型有一个 *gmpRSOP* 对象，你可以通过 *GPM* 对象的 *GetRSOP* 方法创建它。该方法需要几个参数。第一个是 RSOP 是在规划模式还是日志记录模式下。你可以使用 gmpConstant 指定 RSOPModePlanning 或 RSOPModeLogging。第二个参数是用于 WMI 命名空间的，你可以将其留空，最后一个参数必须为 0。

```vbs
Set GPM=CreateObject("GPMGMT.GPM")
set gpmConstants=GPM.GetConstants
set gpmRSOP=GPM.GetRSOP(gpmConstants.RSOPModePlanning,"",0)
```

在此代码片段中，我们将进行一些 RSOP 规划。我们定义要测试的用户帐户和计算机，以及一个域控制器。CreateQueryResults 方法在规划模式下运行 RSOP。然后，我们可以像本章前面那样，使用 GenerateReportToFile 方法将结果写入 HTML 文件。

```vbs
gpmRSOP.PlanningComputer="company\XPDesk01"
gpmRSOP.PlanningUser="company\a.user"
gpmRSOP.PlanningDomainController="DC01"
gpmRSOP.CreateQueryResults
gpmRSOP.GenerateReportToFile gpmConstants.ReportHTML,".\rsop.htm"
```

还有一些其他的规划参数可以指定，例如 PlanningUserSecurityGroups 和 PlanningUserSOM。它们在 GPMC 帮助文件中有解释。对于日志记录模式，你可以采用类似的方法。

### 查看 GPO 脚本的实际应用

让我们将本章涵盖的所有内容整合到一个脚本中。清单 14-5 中的脚本生成一个 HTML 文档，其中包含有关域中每个 GPO 的信息，包括其权限、SOM 链接以及每个 SOM 的权限。

```vbs
'Listing 14-5 Generate GPO Master
Dim GPM,gpmConstants,gpmDomain
dim collGPOS,gpmSearchCriteria,collSOMs
dim gpo
dim RootDSE,objDomain
Dim objFSO,objFile
Dim objDict
strFile="GPOMaster.htm"
WScript.Echo "Building GPO Master Report"

Set objDict=CreateObject("Scripting.Dictionary")
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objFile=objFSO.CreateTextFile(strFile,True)
'build the beginning of the html report
objFile.writeline "<html>"
objFile.writeline "<head>"
objFile.writeLine "<style type=text/css>"
objFile.writeLine "body   {font-size:80%; font-family:Tahoma;}"
objFile.writeLine "table  { font-size:100%; width:100%; }"
objFile.writeLine "</style>"
objFile.writeLine "</head>"
objFile.WriteLine "<body>"
objFile.WriteLine "<H3>Group Policy Master Report</H3><hr>"

'Create GPMC object
Set GPM=CreateObject("GPMGMT.GPM")
'Create GPMC constant object,
Set gpmConstants=GPM.GetConstants
strFQDN=GetDomainFQDN

set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UsePDC)

set gpmSearchCriteria=GPM.CreateSearchCriteria
set collGPOS=gpmDomain.SearchGPOs(gpmSearchCriteria)

objFile.WriteLine "Found " & collGPOS.Count & _
 " group policy objects in " & gpmDomain.Domain & " (" & _
 gpmDomain.DomainController & ")"

For Each gpo In collGPOS
objFile.WriteLine "<Table border=0 cellpadding=3 cellspacing=3>"
objFile.WriteLine "<tr><td align=Center><B><a href=" & CHR(34) & _
 gpo.Displayname & ".htm" & Chr(34) & " target=_Blank>" & _
 gpo.Displayname & "</a></B></td><td>" & gpo.path & "</td></tr>"
objFile.WriteLine "<tr><td></td><td>Created " & gpo.CreationTime & _
 "<br> Modified " & gpo.ModificationTime &"</td></tr>"

'Get SOM Links
gpmSearchCriteria.Add gpmConstants.SearchPropertySOMLinks,_
 gpmConstants.SearchOpContains,gpo
Set collSOMs=gpmDomain.SearchSOMs(gpmSearchCriteria)
objFile.WriteLine "<tr><td>Linked to " & collSOMs.Count & _
 " container(s)</td></tr>"
If collSOMs.Count>0 Then
For Each gpmSOM In collSOMs
objDict.RemoveAll
 Select Case gpmSOM.Type
 Case gpmConstants.SOMSite
 objFile.WriteLine "<tr><td align=Right>[Site] " & gpmSOM.Name & _
 "</td><td>" & gpmSOM.Path &"</td></tr>"
 Set gpmSecurityInfo=gpmSOM.GetSecurityInfo
 objFile.WriteLine "<tr><td colspan=2>" & gpmSecurityInfo.Count & _
 " SOM permission objects</td></tr>"
 For Each gpmPerm In gpmSecurityInfo
 GetPerms(gpmPerm)
 Next
 k=objDict.Keys
 For i=0 To objDict.Count-1
 Select Case k(i)
 Case gpmConstants.permSOMLink
 objFile.WriteLine "<tr><td align=right>SOM Linking</td></tr>"
 tmpArray=Split(objDict.Item(k(i)),"||")
 For j=0 To UBound(tmpArray)
 objFile.WriteLine "<tr><td></td><td align=left>" & _
 tmpArray(j)&"</td></tr>"
 Next
 End Select
    Next
 Case gpmConstants.SOMDomain
 objFile.WriteLine "<tr><td align=Right>[Domain] " & gpmSOM.Name & _
 "</td><td>" & gpmSOM.Path &"</td></tr>"
 Set gpmSecurityInfo=gpmSOM.GetSecurityInfo
 objFile.WriteLine "<tr><td colspan=2>" & gpmSecurityInfo.Count & _
 " SOM permission objects</td></tr>"

 For Each gpmPerm In gpmSecurityInfo
 GetPerms(gpmPerm)
 Next
 k=objDict.Keys
 For i=0 To objDict.Count-1
 Select Case k(i)
 Case gpmConstants.permSOMLink
 objFile.WriteLine "<tr><td align=Right>SOM Linking</td></tr>"
 tmpArray=Split(objDict.Item(k(i)),"||")
 For j=0 To UBound(tmpArray)
 objFile.WriteLine "<tr><td></td><td align=left>" & _
 tmpArray(j)&"</td></tr>"
 Next
 Case gpmConstants.permSOMLogging
 objFile.WriteLine "<tr><td align=Right>RSOP Logging</td></tr>"
 tmpArray=Split(objDict.Item(k(i)),"||")
 For j=0 To UBound(tmpArray)
 objFile.WriteLine "<tr><td></td><td align=left>" & _
 tmpArray(j)&"</td></tr>"
 Next
 Case gpmConstants.permSOMPlanning
 objFile.WriteLine "<tr><td align=Right>RSOP Planning</td></tr>"
 tmpArray=Split(objDict.Item(k(i)),"||")
 For j=0 To UBound(tmpArray)
 objFile.WriteLine "<tr><td></td><td align=left>" & _
 tmpArray(j)&"</td></tr>"
 Next
 End Select
    Next
 Case gpmConstants.SOMOU
 objFile.WriteLine "<tr><td align=Right>[OU] " &gpmSOM.Name & _
 "</td><td>" & gpmSOM.Path &"</td></tr>"
 Set gpmSecurityInfo=gpmSOM.GetSecurityInfo
 objFile.WriteLine "<tr><td colspan=2>" & gpmSecurityInfo.Count & _
 " SOM permission objects</td></tr>"
 For Each gpmPerm In gpmSecurityInfo
 GetPerms(gpmPerm)
 Next
 k=objDict.Keys
 For i=0 To objDict.Count-1
 Select Case k(i)
 Case gpmConstants.permSOMLink
 objFile.WriteLine "<tr><td align=Right>SOM Linking</td></tr>"
 tmpArray=Split(objDict.Item(k(i)),"||")
 For j=0 To UBound(tmpArray)
 objFile.WriteLine "<tr><td></td><td align=left>" & _
 tmpArray(j)&"</td></tr>"
 Next
```



## 第14章：组策略管理脚本编写

417

```
Next
Case gpmConstants.permSOMGPOCreate
    objFile.WriteLine "<tr><td align=right>Create GPO</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
    Next
Case gpmConstants.permSOMLogging
    objFile.WriteLine "<tr><td align=right>RSoP Logging</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
    Next
Case gpmConstants.permSOMPlanning
    objFile.WriteLine "<tr><td align=right>RSoP Planning</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
    Next
Case gpmConstants.permSOMWMICreate
    objFile.WriteLine "<tr><td align=right>Create WMI Filters</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
    Next
Case gpmConstants.permSOMWMIFullControl
    objFile.WriteLine "<tr><td align=right>Full WMI Control</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
    Next
End Select
Next
End Select
Next
End If
'获取 GPO 权限
'清空字典
objDict.RemoveAll
Set gpmSecurityInfo=gpo.GetSecurityInfo
objFile.WriteLine "<tr><td colspan=2>" & gpmSecurityInfo.Count & _
    " GPO permission objects</td></tr>"
For Each gpmPerm In gpmSecurityInfo
    GetPerms(gpmPerm)
Next
k=objDict.Keys
For i=0 To objDict.Count-1
    Select Case k(i)
        Case gpmConstants.permGPOApply
            objFile.WriteLine "<tr><td align=right>GPO Applies</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
    Next
    Case gpmConstants.permGPOCustom
        objFile.WriteLine "<tr><td align=right>GPO Custom</td></tr>"
        tmpArray=Split(objDict.Item(k(i)),"||")
        For j=0 To UBound(tmpArray)
            objFile.WriteLine "<tr><td></td><td align=left>" & _
                tmpArray(j)&"</td></tr>"
        Next
    Case gpmConstants.permGPOEdit
        objFile.WriteLine "<tr><td align=right>GPO Edit</td></tr>"
        tmpArray=Split(objDict.Item(k(i)),"||")
        For j=0 To UBound(tmpArray)
            objFile.WriteLine "<tr><td></td><td align=left>" & _
                tmpArray(j)&"</td></tr>"
        Next
    Case gpmConstants.permGPORead
        objFile.WriteLine "<tr><td align=right>GPO Read</td></tr>"
        tmpArray=Split(objDict.Item(k(i)),"||")
        For j=0 To UBound(tmpArray)
            objFile.WriteLine "<tr><td></td><td align=left>" & _
                tmpArray(j)&"</td></tr>"
        Next
    Case gpmConstants.permGPOEditSecurityAndDelete
        objFile.WriteLine "<tr><td align=right>GPO Edit Security</td></tr>"
        tmpArray=Split(objDict.Item(k(i)),"||")
        For j=0 To UBound(tmpArray)
            objFile.WriteLine "<tr><td></td><td align=left>" & _
                tmpArray(j)&"</td></tr>"
        Next
    End Select
Next
'生成 HTML 报告
gpo.GenerateReporttoFile gpmConstants.ReportHTML, ".\" & _
    gpo.Displayname & ".htm"
objFile.WriteLine "</Table><br><br>"
Next
objFile.WriteLine "<I>Report run " & Now & "</I>"
objFile.WriteLine "</Body>"
objFile.WriteLine "</html>"
objFile.Close
wScript.Echo "Finished building report page."
WScript.Quit

'*****************************************
Function GetDomainFQDN()
    Set RootDSE=GetObject("LDAP://RootDSE")
    DomainPath= RootDSE.Get("DefaultNamingContext")
    DomainPath=Replace(DomainPath,"DC=","")
    GetDomainFQDN=Replace(DomainPath,",",".")
End Function
'*****************************************
Function ListTrustees(gpmPerm)
On Error Resume Next
    If gpmPerm.Trustee.TrusteeDSPath="" Then
        ListTrustees= gpmPerm.Trustee.TrusteeName
    Else
        ListTrustees= gpmPerm.Trustee.TrusteeName & " [" & _
            gpmPerm.Trustee.TrusteeDSPath & "]"
    End If
End Function
'********************************************
Sub GetPerms(gpmPerm)
    If objDict.Exists(gpmPerm.Permission) Then
        strTemp=objDict.Item(gpmPerm.Permission)
        objDict.Remove gpmPerm.Permission
        'WScript.Echo "Adding " & strTemp & "," & ListTrustees(gpmPerm)
        objDict.Add gpmPerm.permission,strTemp & "||" & ListTrustees(gpmPerm)
    Else
        objDict.Add gpmPerm.Permission,ListTrustees(gpmPerm)
    End If
End Sub
```

我们从该章节中提取了一些脚本示例，并将结果写入 HTML 表格。我们首先获取与域的连接并搜索所有 GPO。

```
'创建 GPMC 对象
Set GPM=CreateObject("GPMGMT.GPM")
'创建 GPMC 常量对象
Set gpmConstants=GPM.GetConstants
strFQDN=GetDomainFQDN
set gpmDomain=GPM.GetDomain(strFQDN,"",gpmConstants.UsePDC)
set gpmSearchCriteria=GPM.CreateSearchCriteria
set colIGPOs=gpmDomain.SearchGPOs(gpmSearchCriteria)
```

对于每个 GPO，我们将显示名称、路径、创建时间和修改时间写入表格。

```
objFile.WriteLine "<Table border=0 cellpadding=3 cellspacing=3>"
objFile.WriteLine "<tr><td align=Center><B><a href=" & CHR(34) & _
    gpo.Displayname & ".htm" & Chr(34) & " target=_Blank>" & _
    gpo.Displayname & "</a></B></td><td>" & gpo.path & "</td></tr>"
objFile.WriteLine "<tr><td></td><td>Created " & gpo.CreationTime & _
    "<br> Modified " & gpo.ModificationTime &"</td></tr>"
```

接下来我们获取 GPO 的 SOM 链接。

```
'获取 SOM 链接
gpmSearchCriteria.Add gpmConstants.SearchPropertySOMLinks,_
    gpmConstants.SearchOpContains,gpo
Set colSOMs=gpmDomain.SearchSOMs(gpmSearchCriteria)
objFile.WriteLine "<tr><td>Linked to " & colSOMs.Count & _
    " container(s)</td></tr>"
```

# 第四部分：企业脚本编写

我们将有关 SOM 的信息写入表格。

```
For Each gpmSOM In collSOMs
objDict.RemoveAll
  Select Case gpmSOM.Type
    Case gpmConstants.SOMSite
      objFile.WriteLine "<tr><td align=Right>[Site] " & gpmSOM.Name & _
        "</td><td>" & gpmSOM.Path & "</td></tr>"
```

对于每种 SOM 类型（如 OU 或站点），我们获取该 SOM 的权限。

```
Set gpmSecurityInfo=gpmSOM.GetSecurityInfo
  objFile.WriteLine "<tr><td colspan=2>" & gpmSecurityInfo.Count & _
    " SOM permission objects</td></tr>"
  For Each gpmPerm In gpmSecurityInfo
    GetPerms(gpmPerm)
  Next
```

我们使用字典对象，通过一个名为 *GetPerms* 的子例程将权限类型分组在一起。

```
Sub GetPerms(gpmPerm)
If objDict.Exists(gpmPerm.Permission) Then
  strTemp=objDict.Item(gpmPerm.Permission)
  objDict.Remove gpmPerm.Permission
  'WScript.Echo "Adding " & strTemp & "," & ListTrustees(gpmPerm)
  objDict.Add gpmPerm.permission,strTemp & "||" & ListTrustees(gpmPerm)
Else
  objDict.Add gpmPerm.Permission,ListTrustees(gpmPerm)
End If
End Sub
```

该子例程将每个新的委托方用两个管道符（||）分隔添加。这样我们稍后可以将项目拆分为数组，并分别写出每个条目。我们不使用逗号，因为委托方信息包含 Active Directory 路径，其中包含逗号。

每个字典键对应一个特定的权限类型，而项目值则保存着委托方。然后我们可以枚举字典，并使用 *Select Case* 来比较权限类型。每个字典项目都被拆分为一个数组，以便可以分别写出每个委托方。

```
k=objDict.Keys
  For i=0 To objDict.Count-1
    Select Case k(i)
      Case gpmConstants.permSOMLink
        objFile.WriteLine "<tr><td align=Right>SOM Linking</td></tr>"
        tmpArray=Split(objDict.Item(k(i)),"||")
        For j=0 To UBound(tmpArray)
          objFile.WriteLine "<tr><td></td><td align=left>" & _
            tmpArray(j)&"</td></tr>"
        Next
      Case gpmConstants.permSOMLogging
        objFile.WriteLine "<tr><td align=Right>RSOP Logging</td></tr>"
        tmpArray=Split(objDict.Item(k(i)),"||")
```



## 第14章：组策略管理脚本编写

```
For j=0 To UBound(tmpArray)
    objFile.WriteLine "<tr><td></td><td align=left>" & _
    tmpArray(j)&"</td></tr>"
Next
```

```
Case gpmConstants.permSOMPlanning
    objFile.WriteLine "<tr><td align=Right>RSOPplanning</td></tr>"
    tmpArray=Split(objDict.Item(k(i)),"||")
    For j=0 To UBound(tmpArray)
        objFile.WriteLine "<tr><td></td><td align=left>" & _
        tmpArray(j)&"</td></tr>"
    Next
End Select
Next
```

此过程会对每种SOM类型重复执行，然后我们使用相同的技术来获取GPO权限。

```
'获取GPO权限
'清空字典
objDict.RemoveAll
Set gpmSecurityInfo=gpo.GetSecurityInfo
objFile.WriteLine "<tr><td colspan=2>" & gpmSecurityInfo.Count & _
" 个GPO权限对象</td></tr>"
For Each gpmPerm In gpmSecurityInfo
    GetPerms(gpmPerm)
Next
```

```
k=objDict.Keys
    For i=0 To objDict.Count-1
        Select Case k(i)
            Case gpmConstants.permGPOApply
                objFile.WriteLine "<tr><td align=right>GPO 应用</td></tr>"
                tmpArray=Split(objDict.Item(k(i)),"||")
                For j=0 To UBound(tmpArray)
                    objFile.WriteLine "<tr><td></td><td align=left>" & _
                    tmpArray(j)&"</td></tr>"
                Next
            Case gpmConstants.permGPOCustom
                objFile.WriteLine "<tr><td align=right>GPO 自定义</td></tr>"
                tmpArray=Split(objDict.Item(k(i)),"||")
                For j=0 To UBound(tmpArray)
                    objFile.WriteLine "<tr><td></td><td align=left>" & _
                    tmpArray(j)&"</td></tr>"
                Next
            Case gpmConstants.permGPOEdit
                objFile.WriteLine "<tr><td align=right>GPO 编辑</td></tr>"
                tmpArray=Split(objDict.Item(k(i)),"||")
                For j=0 To UBound(tmpArray)
                    objFile.WriteLine "<tr><td></td><td align=left>" & _
                    tmpArray(j)&"</td></tr>"
                Next
            Case gpmConstants.permGPORead
                objFile.WriteLine "<tr><td align=right>GPO 读取</td></tr>"
                tmpArray=Split(objDict.Item(k(i)),"||")
                For j=0 To UBound(tmpArray)
                    objFile.WriteLine "<tr><td></td><td align=left>" & _
                    tmpArray(j)&"</td></tr>"
                Next
            Case gpmConstants.permGPOEditSecurityAndDelete
                objFile.WriteLine "<tr><td align=right>GPO 编辑安全性</td></tr>"
                tmpArray=Split(objDict.Item(k(i)),"||")
                For j=0 To UBound(tmpArray)
                    objFile.writeLine "<tr><td></td><td align=left>" & _
                    tmpArray(j)&"</td></tr>"
                Next
        End Select
    Next
```

该脚本会为每个GPO生成一个HTML报告。

```
'生成HTML报告
gpo.GenerateReporttoFile gpmConstants.ReportHTML, ".\\" & _
gpo.Displayname & ".htm"
```

当我们将GPO显示名称写入表格时，包含了用于链接到报告的HTML代码。

```
objFile.WriteLine "<tr><td align=Center><B><a href=" & CHR(34) & _
gpo.Displayname & ".htm" & Chr(34) & " target=_Blank>" & _
gpo.Displayname & "</a></B></td><td>" & gpo.path & "</td></tr>"
```

运行该脚本后，您应该会得到如图14-2所示的结果。

![](img/4fefd6988ba5d4a92a65127617ca24c2_441_0.png)

图14-2 GPO主报告摘要

### 总结

编写GPO管理脚本可能不是您经常做的事情。但是，您会发现组策略管理控制台易于使用，尤其是对于RSOP规划等任务。我们认为您会发现使用GPMC编写脚本对于自动化备份和报告生成等任务特别有用。我们演示了对象模型的工作原理，以及如何使用非常有用的*Constants*对象。GPMC脚本编写需要一点练习，但如果您想要一些与工具附带脚本不同的东西，您会很高兴花了时间。

> **更多信息** 我们在附带光盘上包含了一些关于GPMC脚本编写的有用Web链接。并且不要忘记查看%ProgramFiles%\GPMC\Scripts文件夹中的组策略管理控制台帮助文件（gpmc.chm）。

# 第15章

## Exchange 2003 脚本编写

| 本章内容： | |
| --- | --- |
| 介绍Exchange脚本编写 | 425 |
| 查询Active Directory | 426 |
| 理解Exchange 2003 WMI类 | 432 |
| 编写Exchange服务器状态类脚本 | 435 |
| 编写Exchange存储组脚本 | 436 |
| 编写Exchange邮箱脚本 | 441 |
| 查看实际运行中的Exchange服务器脚本 | 454 |
| 总结 | 462 |

Microsoft Exchange 2003是管理脚本编写理想平台。如果您曾经希望使用VBScript管理Exchange环境，那么Exchange 2003就是您一直在等待的。在本章中，我们将探讨使用Exchange 2003进行脚本编写的各种方法。您将看到如何管理Exchange服务器、存储组和邮件存储。正如您将看到的，没有单一的脚本编写方法，您必须精通Active Directory服务接口（ADSI）、Windows管理规范（WMI）等，才能充分利用Exchange 2003脚本编写的优势。

Exchange 2003是迄今为止Microsoft推出的最强大的企业邮件平台。其最大优势之一是它有许多管理方式；您不再需要依赖管理控制台。现在您可以为管理控制台或昂贵的第三方工具无法完成的自定义管理任务创建脚本。

### 介绍Exchange脚本编写

使用Exchange 2003进行脚本编写涉及多种技术。您使用轻量级目录访问协议（LDAP）ADSI提供程序从Active Directory中发现有关Exchange组织的信息。您使用WinNT ADSI提供程序管理Exchange 2003服务。您使用WMI管理Exchange邮箱和Exchange服务器。最后，您使用协作数据对象（CDO）和Exchange管理协作数据对象（CDOEXM）管理存储组和邮箱存储。使用Exchange 2003进行脚本编写的一个好处是，您可以从桌面远程管理Exchange组织。假设您具有适当的管理凭据，您可以从Microsoft Windows XP桌面执行大多数管理任务，无需额外软件。

# 第四部分：企业脚本编写

但是，如果您需要开发或运行任何使用CDO或CDOEXM的脚本，则需要在桌面上安装Exchange 2003管理控制台。如果您正在管理Exchange服务器，很可能已经安装了它。

我们还建议您安装Exchange 2003软件开发工具包（SDK）。SDK可从Microsoft免费下载，地址为：

http://www.microsoft.com/downloads/details.aspx?FamilyId=E7E34B5B-01B0-45ED-B91F-F7064875D379&displaylang=en

> **光盘内容** 与本书中引用的大多数链接一样，此链接也包含在附带光盘中。点击*Exchange 2003 SDK*。

SDK包含大量代码示例和优秀的文档。SDK的大部分内容针对应用程序开发人员，但您会找到大量关于Exchange对象、属性和方法的信息。

## 查询Active Directory

从Exchange 2000开始，Microsoft开始使用Active Directory作为Microsoft Exchange的目录服务。有关Exchange组织、服务器、存储组等的所有配置信息现在都存储在Active Directory中。这意味着我们可以使用LDAP提供程序的ADSI查询来发现有关Exchange环境的信息。例如，我们可以发现组织中的所有Exchange服务器。考虑清单15-1中的脚本。

```
清单15-1 列出Exchange服务器
'从AD获取Exchange服务器列表
Dim objRootDSE
Dim objConfiguration
Dim cat
Dim conn
Dim cmd
Dim RS
Set objRootDSE = GetObject("LDAP://rootDSE")

strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)

'选择Exchange服务器，但排除碰巧共享相同类别的策略
strQuery="Select distinguishedname,name,serialnumber,whencreated from '" & _
objConfiguration.ADSPATH & "' where objectclass='msExchExchangeServer' " & _
"AND objectclass<>'msExchExchangeServerPolicy'"

WScript.Echo strQuery & VbCrLf

Set cat=GetObject("GC:")
```



对于 `cat` 中的每个对象
  将 `GC` 设置为该对象
Next

Set conn=CreateObject("ADODB.Connection")
Set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open

Set cmd.ActiveConnection=conn
Set RS=conn.Execute(strQuery)

Do While not RS.EOF
  if isArray(RS.Fields("serialnumber")) Then tmpArray=RS.Fields("serialnumber")
  wscript.Echo rs.Fields("name") & " (创建于 " &
    RS.Fields("whencreated") & ")" & vbTab & tmpArray(0)
  RS.movenext
Loop
RS.Close
conn.Close

你可以在随书附带的 CD 上找到这个脚本，以及本章列出的其他脚本。

我们首先定义一个查询，用于搜索 Active Directory 森林的默认配置命名上下文。我们将搜索对象类等于 `ms-ExchExchangeServer` 但不等于 `msExchExchangeServerPolicy` 的对象，因为 `msExchExchangeServerPolicy` 对象从 `msExchExchangeServer` 继承类设置。如果我们查询 `msExchExchangeServer` 对象，也会得到服务器策略的列表。脚本会显示查询语句，以便你可以准确看到正在查找的内容。

```
Set objRootDSE = GetObject("LDAP://rootDSE")

strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)

'选择 Exchange 服务器，但排除恰好共享相同类的策略
strQuery="Select distinguishedname,name,serialnumber,whencreated from '"& _
         objConfiguration.ADSPath & "' where objectclass='msExchExchangeServer' "&_
         "AND objectclass<>'msExchExchangeServerPolicy'"

wScript.Echo strQuery & VbCrLf
```

通过使用简单的 ADODB 代码，我们处理记录集并显示 `name`、`whencreated` 和 `serialnumber` 属性。

> 提示：尽管我们不显示它，但我们查询了服务器的可分辨名称。你可能想将其添加到脚本输出中，作为学习辅助，以更好地理解 Exchange 信息在 Active Directory 中的存储方式。

请注意，我们将 *serialnumber* 属性作为数组进行处理。

```
if isArray(RS.Fields("serialnumber")) Then tmpArray=RS.Fields("serialnumber")
```

这是因为该属性是一个多值属性。如果我们只尝试使用以下语句，将会得到类型不匹配错误。

```
wscript.echo RS.fields("serialnumber")
```

我们之所以知道 *serialnumber* 是多值属性，是因为我们使用了 Windows 支持工具中的 ADSIEdit 来查看属性。打开 *Configuration* 命名上下文并导航到 *CN=Services*。展开此项，你会看到 *CN=Microsoft Exchange*。这是 Active Directory 中存储大多数 Exchange 信息的地方。当你探索这个层次结构时，最终会找到你的管理组，以及其中的服务器。右键单击服务器名称（例如 *CN=Mail01*），然后单击“属性”以显示所有属性。如果你编辑 *serialnumber*，会看到它是一个多值属性。

如果你继续在 ADSIEdit 中探索，会看到 *CN=InformationStore*，这是存储特定服务器所有存储组信息的地方。清单 15-2 中的脚本在 Active Directory 的默认命名上下文中搜索所有存储组。

### 清单 15-2 列出 Exchange 存储组

```
'获取存储组列表
Dim objRootDSE
Dim objConfiguration
Dim conn
Dim cmd
Dim RS

Set objRootDSE = GetObject("LDAP://rootDSE")
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)
strPath=objConfiguration.ADSpath

strQuery="Select distinguishedname,name,whencreated from '" & strPath & "
" WHERE objectclass='msExchStorageGroup'"

WScript.Echo strQuery & VbCrLf

set cat=GetObject("GC:")
for each obj in cat
  set GC=obj
Next

set conn=Createobject("ADODB.Connection")
set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open

set cmd.ActiveConnection=conn
set RS=conn.Execute(strQuery)

do while not RS.EOF
    wscript.echo rs.Fields("distinguishedname")
    wscript.echo vbtab & rs.Fields("name") & "(创建于 " & _
    rs.fields("whencreated") & ")"
    rs.movenext
Loop
rs.close
conn.Close
```

此脚本的格式与清单 15-1 基本相同。查询搜索任何 *msExchStorageGroup* 类的对象。

```
strQuery="Select distinguishedname,name,whencreated from '" & strPath & _
"' WHERE objectclass='msExchStorageGroup'"
```

运行此脚本时，将获得如下输出。

```
Select distinguishedname,name,whencreated from 'LDAP://CN=Configuration,DC=company,DC=pri'
WHERE objectclass='msExchStorageGroup'

CN=First Storage Group,CN=InformationStore,CN=MAIL01,CN=Servers,CN=First Administrative
Group,CN=Administrative Groups,CN=company,CN=Microsoft
Exchange,CN=Services,CN=Configuration,DC=company,DC=pri
    First Storage Group(创建于 12/1/2004 8:29:59 PM)
CN=Second Storage Group,CN=InformationStore,CN=MAIL01,CN=Servers,CN=First Administrative
Group,CN=Administrative Groups,CN=company,CN=Microsoft
Exchange,CN=Services,CN=Configuration,DC=company,DC=pri
    Second Storage Group(创建于 4/27/2005 12:06:55 AM)
CN=ScriptingAnswers,CN=InformationStore,CN=MAIL01,CN=Servers,CN=First Administrative
Group,CN=Administrative Groups,CN=company,CN=Microsoft
Exchange,CN=Services,CN=Configuration,DC=company,DC=pri
    ScriptingAnswers(创建于 8/9/2005 5:13:13 PM)
```

此代码将返回整个 Exchange 组织的所有存储组。如果你只有一台 Exchange 服务器，则所有存储组都将在同一台服务器上。但是，如果你有多个服务器，并且只想显示特定服务器上的存储组信息，则必须搜索存储组的可分辨名称。因为存储组是 Exchange 服务器的子对象，所以 Exchange 服务器名称出现在可分辨名称中。例如，服务器 `MAIL01` 上的存储组的可分辨名称可能类似于 *CN=First Storage Group,CN=InformationStore,CN=MAIL01,CN=Servers, CN=First Administrative Group,CN=Administrative Groups,CN=COMPANY,CN=Microsoft Exchange,CN=Services,CN=Configuration,DC=company,DC=pri*。如果我们只想查看此服务器的存储组，可以像这样修改脚本。

```
strSrv="MAIL01"
do while not RS.EOF
    If InStr(rs.Fields("distinguishedname"),strSrv) then
        wscript.echo rs.Fields("distinguishedname")
        wscript.echo vbtab & rs.Fields("name") & "(创建于 " & _
        rs.fields("whencreated") & ")"
    end if
    rs.movenext
Loop
```

我们也可以通过查询 Active Directory 来获取有关 Exchange 邮箱存储的信息，如清单 15-3 中的脚本所示。

### 清单 15-3 列出 Exchange 邮箱存储

```
'获取邮箱存储列表
Dim objRootDSE
Dim objConfiguration
Dim conn
Dim cmd
Dim RS

Set objRootDSE = GetObject("LDAP://rootDSE")
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)
strPath=objConfiguration.ADSpath

strQuery="Select distinguishedname,name,whencreated from '" & strPath & "' WHERE objectclass='msExchPrivateMDB' "

WScript.Echo strQuery & vbcrLf
set cat=GetObject("GC:")
for each obj in cat
	set GC=obj
Next

set conn=Createobject("ADODB.Connection")
set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open

set cmd.ActiveConnection=conn
set RS=conn.Execute(strQuery)
do while not RS.EOF
	WScript.Echo RS.Fields("distinguishedname")
	WScript.Echo vbTab & RS.Fields("name") & "(创建于 " &_
	RS.fields("whencreated") & ")"
	rs.movenext
Loop
rs.Close
conn.Close
```

同样，脚本并没有真正改变，只是查询中的对象类不同。现在我们搜索 *msExchPrivateMDB* 对象。

```
strQuery="select distinguishedname,name,whencreated from '" & strPath & "' WHERE objectclass='msExchPrivateMDB' "
```

Active Directory 无法告诉我们太多关于实际邮箱存储的信息。例如，它无法告诉我们它有多大，但它可以告诉我们它是如何定义的，这些信息可以包括每个邮箱存储中的邮箱。清单 15-4 中的脚本与清单 15-3 非常相似，不同之处在于它还将显示存储组中的每个邮箱。



## 第15章：Exchange 2003 脚本

### 清单 15-4：列出邮箱存储和邮箱

```vb
'获取邮箱存储列表
Dim objRootDSE
Dim objConfiguration
Dim conn
Dim cmd
Dim RS

Set objRootDSE = GetObject("LDAP://rootDSE")
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)
strPath=objConfiguration.ADspath

strQuery="Select distinguishedname,name,homeMDBBL from '" & strPath &_
"' WHERE objectclass='msExchPrivateMDB' "

wScript.Echo strQuery & vbcrlf
set cat=GetObject("GC:")
for each obj in cat
    set GC=obj
Next

set conn=Createobject("ADODB.Connection")
set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open

set cmd.ActiveConnection=conn
set RS=conn.Execute(strQuery)
do while not RS.EOF
    wScript.Echo RS.Fields("distinguishedname")
    wScript.Echo vbTab & "Mailboxes on " & RS.Fields("name")
    tmpArray=RS.Fields("homeMDBBL")
    For m=0 To UBound(tmpArray)
        wScript.Echo vbTab & " " & tmpArray(m)
    next
    rs.movenext
Loop
rs.Close
conn.Close
```

此脚本基于清单 15-3 中的脚本，并在查询中添加了 `homeMDBBL` 属性。

```vb
strQuery="Select distinguishedname,name,homeMDBBL from '" & strPath &_
"' WHERE objectclass='msExchPrivateMDB' "
```

`homeMDBBL` 属性是一个多值属性，包含附加到每个邮箱的帐户的可分辨名称。由于该属性是多值的，我们将其视为数组处理。

```vb
do while not RS.EOF
    WScript.Echo RS.Fields("distinguishedname")
    WScript.Echo vbTab & "Mailboxes on " & RS.Fields("name")
    tmpArray=RS.Fields("homeMDBBL")
    For m=0 To UBound(tmpArray)
        WScript.Echo vbTab & " " & tmpArray(m)
    next
    rs.movenext
Loop
```

### 理解 Exchange 2003 WMI 类

Microsoft Exchange 2000 引入了一些新的 WMI 类，而 Exchange 2003 又增加了更多。现在，你有更多机会在脚本中使用 WMI 类。表 15-1 列出了新增的类。

**表 15-1：Exchange 2003 WMI 类**

| Exchange_FolderTree | Exchange_QueueSMTPVirtualServer |
| :--- | :--- |
| Exchange_Link | Exchange_QueueX400VirtualServer |
| Exchange_Logon | Exchange_ScheduleInterval |
| Exchange_Mailbox | Exchange_Server |
| Exchange_PublicFolder | Exchange_SMTPLink |
| Exchange_Queue | Exchange_SMTPQueue |
| Exchange_QueueCacheReloadEvent | Exchange_X400Link |
| Exchange_QueuedMessage | Exchange_X400Queue |
| Exchange_QueuedSMTPMessage | Exchange_QueuedX400Message |

这些类位于 `root\MicrosoftExchangev2` 命名空间中。你可以使用 Scriptomatic 等工具查看它们。

![img/4fefd6988ba5d4a92a65127617ca24c2_451_0.png](img/4fefd6988ba5d4a92a65127617ca24c2_451_0.png)

> **重要提示：** 如果你在 Microsoft Windows Server 2000 上运行 Exchange 2003，很可能看不到这些类中的大多数。要使用新的 WMI 类，你需要在 Microsoft Windows Server 2003 上运行 Exchange 2003。

我们不会详细介绍每一个新类，但让我们快速看一下 `Exchange_Server` 类。清单 15-5 是一个使用此 WMI 类的脚本。

### 清单 15-5：列出 Exchange 服务器信息

```vb
On Error Resume Next
strSrv="MAIL01"

Set objWMIService = GetObject("winmgmts:\\\\" & strSrv &
 "\\root\\MicrosoftExchangev2")
Set colItems = objWMIService.ExecQuery("Select AdministrativeGroup,DN," &
 "ExchangeVersion,FQDN,Name,RoutingGroup,CreationTime,Name," &
 "IsFrontEndServer,MessageTrackingEnabled,SubjectLoggingEnabled," &
 "LastModificationTime  from Exchange_Server where name='" & strSrv &
 "'",,48)

For Each objItem In colItems
    If objItem.FQDN="" Then
        wscript.echo "Failed to get Exchange server information from WMI." &
        " Verify the Microsoft Exchange Management service is running on " &
        strSRV
    Else
        wscript.echo UCase(objItem.FQDN) & " [" &
        objItem.Exchangeversion & "]"
        wscript.echo "Administrative Group: " &
        objItem.AdministrativeGroup
        wscript.echo "Last modified: " &
        ConvertTime(objItem.LastModificationTime)
        wscript.echo "Front End Server: " & objItem.IsFrontEndServer
        wscript.echo "Message Tracking: " & objItem.MessageTrackingEnabled
        wscript.echo "Subject logging: " & objItem.SubjectLoggingEnabled
    End If
Next

Function ConvertTime(strTime)
On Error Resume Next

yr = Left(strTime,4)
mo = mid(strTime,5,2)
dy = mid(strTime,7,2)
tm = Mid(strTime,9,6)

ConvertTime=mo & "/" & dy & "/" & yr

End Function
```

我们首先连接到 Exchange 2003 服务器上的 Exchange 命名空间。

```vb
strSrv="MAIL01"
Set objWMIService = GetObject("winmgmts:\\\\" & strSrv &
 "\\root\\MicrosoftExchangev2")
```

这个对象类有许多属性，我们将查询其中的几个。

```vb
Set colItems = objWMIService.ExecQuery("Select AdministrativeGroup,DN," & _
"ExchangeVersion,FQDN,Name,RoutingGroup,CreationTime,Name," & _
"IsFrontEndServer,MessageTrackingEnabled,SubjectLoggingEnabled," & _
"LastModificationTime from Exchange_Server where name='" & strSrv & _
"'",,48)
```

> **故障排除：** 你可能觉得奇怪，为什么我们必须在查询的条件子句中指定服务器名称。这里似乎存在一个小缺陷。查询字符串 `Select * from *Exchange_Server*` 可以正常工作。但如果你查询 `Select FQDN, ExchangeVersion, Name from Exchange_Server`，查询将会失败。如果你想进行选择性查询，需要使用限定符，正如我们在这里所做的。

该查询返回一个 WMI 集合，然后我们对其进行遍历。

```vb
For Each objItem In colItems
    If objItem.FQDN="" Then
        wscript.echo "Failed to get Exchange server information from WMI." & _
        " Verify the Microsoft Exchange Management service is running on " & _
        strSRV
    Else
        wscript.echo UCase(objItem.FQDN) & " [" & _
        objItem.Exchangeversion & "]"
        wscript.echo "Administrative Group: " & _
        objItem.AdministrativeGroup
        wscript.echo "Last modified: " & _
        ConvertTime(objItem.LastModificationTime)
        wscript.echo "Front End Server: " & objItem.IsFrontEndServer
        wscript.echo "Message Tracking: " & objItem.MessageTrackingEnabled
        wscript.echo "Subject logging: " & objItem.SubjectLoggingEnabled
    End If
Next
```

这里是另一个代码片段，展示了使用 WMI Exchange 类可以做的事情。此代码使用 `Exchange_PublicFolder` 类来计算所有公共文件夹邮件的总大小。

```vb
strSrv="MAIL01"
iTotal=0
Set objWMIService = GetObject("winmgmts:\\" & strSrv & _
"\\root\\MicrosoftExchangev2")
strPFQuery="Select * from Exchange_PublicFolder"
Set colItems = objWMIService.ExecQuery(strPFQuery,,48)
For Each objItem in colItems
    strFldrName=objItem.Name
    iFldrsize=objItem.TotalMessageSize
    iTotal=iTotal + iFldrSize
Next

wscript.echo FormatNumber(iTotal/1048576,2) & " MB"
```

> **更多信息：** 要获取更多关于将 WMI 与 Exchange 2003 结合使用的信息，请查看 Alain Lisoir 撰写的精彩教程：
>
> www.microsoft.com/technet/scriptcenter/topics/exchange/ex03_wmi1.mspx
>
> www.microsoft.com/technet/scriptcenter/topics/exchange/ex03_wmi2.mspx
>
> www.microsoft.com/technet/scriptcenter/topics/exchange/ex03_wmi3.mspx
>
> （这些链接位于附带的 CD 上；分别点击 *使用 WMI 管理 Exchange 2003* 的第 1、2 和 3 部分。）

### 脚本化 ExchangeServerState 类

WMI 类 `ExchangeServerState` 将为你提供有关 Exchange 服务器状态的信息。例如，如果你有一个 Exchange 群集，可以使用此类来检查群集状态。你可以使用的一些关键属性包括：

- `ClusterState`：指示你的 Exchange 群集的状况。此属性返回 0（未知）、1（正常）、2（警告）或 3（错误）的值。这是一个只读属性。
- `DiskState`：指示磁盘存储的状况。此属性返回 0（未知）、1（正常）、2（警告）或 3（错误）的值。这是一个只读属性。
- `DN`：返回你的 Exchange 服务器的可分辨名称。
- `GroupDN`：返回 Exchange 服务器所属的路由组的可分辨名称。
- `MemoryState`：指示 Exchange 服务器上内存的状况。此属性返回 0（未知）、1（正常）、2（警告）或 3（错误）的值。这是一个只读属性。
- `Name`：返回 Exchange 服务器的 netBIOS 名称。
- `QueueState`：指示 Exchange 邮件队列的状况。此属性返回 0（未知）、1（正常）、2（警告）或 3（错误）的值。这是一个只读属性。
- `ServerState`：指示 Exchange 服务器的整体状况。此属性返回 0（未知）、1（正常）、2（警告）或 3（错误）的值。这是一个只读属性。
- `Unreachable`：返回一个布尔值，指示是否可以联系到 Exchange 服务器。如果服务器不可达，则返回 TRUE。
- `Version`：返回 Microsoft Exchange 的版本信息。

下一页的清单 15-6 中的脚本演示了此类。与我们之前查看的一些其他 WMI 类不同，此类位于 `root\cimv2\applications\exchange` 命名空间中。



## 清单 15-6 列出 Exchange 服务器信息
On Error Resume Next
Dim strComputer
Dim objWMIService
Dim propvalue
Dim objItem
Dim SWbemlocator
Dim UserName
Dim Password
Dim colItems

strComputer = "MAIL01"
UserName = ""
Password = ""
Set SWBemlocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer,_
    "\\root\cimv2\applications\exchange",UserName,Password)
strQuery="Select * from ExchangeServerState"
Set colItems = objWMIService.ExecQuery(strQuery,,48)
For Each objItem in colItems
    WScript.Echo "ClusterState: " & objItem.ClusterState
    WScript.Echo "ClusterStateString: " & objItem.ClusterStateString
    WScript.Echo "CPUState: " & objItem.CPUState
    WScript.Echo "CPUStateString: " & objItem.CPUStateString
    WScript.Echo "DisksState: " & objItem.DisksState
    WScript.Echo "DisksStateString: " & objItem.DisksStateString
    WScript.Echo "DN: " & objItem.DN
    WScript.Echo "GroupDN: " & objItem.GroupDN
    WScript.Echo "GroupGUID: " & objItem.GroupGUID
    WScript.Echo "GUID: " & objItem.GUID
    WScript.Echo "MemoryState: " & objItem.MemoryState
    WScript.Echo "MemoryStateString: " & objItem.MemoryStateString
    WScript.Echo "Name: " & objItem.Name
    WScript.Echo "QueuesState: " & objItem.QueuesState
    WScript.Echo "QueuesStateString: " & objItem.QueuesStateString
    WScript.Echo "ServerMaintenance: " & objItem.ServerMaintenance
    WScript.Echo "ServerState: " & objItem.ServerState
    WScript.Echo "ServerStateString: " & objItem.ServerStateString
    WScript.Echo "ServicesState: " & objItem.ServicesState
    WScript.Echo "ServicesStateString: " & objItem.ServicesStateString
    WScript.Echo "Unreachable: " & objItem.Unreachable
    WScript.Echo "Version: " & objItem.Version
Next

### 脚本化 Exchange 存储组

要处理 Exchange 存储组，您必须安装 Exchange 管理的 CDO (CDOEXM)。在您的桌面上安装 Exchange 管理控制台后，您就拥有了所需的一切。CDOEXM 包含几个您将在脚本中实例化的对象。让我们看一下清单 15-7 中的脚本。

## 清单 15-7 列出存储组

```
On Error Resume Next
strTitle="Storage Group Report"
strServer=InputBox("What is the name of the Exchange Server?",_
strTitle,"MAIL01")
If strServer="" Then
    WScript.Quit
else
    'Call report subroutine
    SGReport strServer
End if
WScript.Quit
'//////////////////////////////////////////////////////////////
Sub SGReport(strServer)
Dim iServer
Dim iSGs
Dim iMBS

Set iServer=CreateObject("CDOEXM.ExchangeServer")
Set iSGs=CreateObject("CDOEXM.StorageGroup")
'connect to Exchange server with CDOEXM
iServer.DataSource.Open strServer

'return array of storage groups
arrSGs=iServer.StorageGroups

'enumerate the array
For i=0 To UBound(arrSGs)
    'get the URL for each storage group
    strSGUrl=arrSGs(i)
    'connect to each storage group
    iSGs.DataSource.Open "LDAP://" & iServer.DirectoryServer & "/" &_
    strSGUrl
    strData=strData & iSGs.Name & VBCRLF
    strData=strData & vbTab & "LogPath: " &iSGs.LogFilePath & VBCRLF
    strData=strData & vbTab & "SystemPath:" & iSGs.SystemFilePath & VBCRLF
Next

'display the data
WScript.Echo strData

End sub
```

此脚本只是列出了指定 Exchange 服务器上每个存储组的名称及其日志和数据库路径。该脚本的核心是创建两个 CDOEXM 对象。我们需要一个用于 Exchange 服务器对象，一个用于存储组对象。

```
Set iServer=CreateObject("CDOEXM.ExchangeServer")
Set iSGs=CreateObject("CDOEXM.StorageGroup")
```

有了这些对象，我们现在可以连接到由 `strServer` 变量指定的 Exchange 服务器，并返回所有存储组的数组。

```
'connect to Exchange server with CDOEXM
iServer.DataSource.Open strServer
'return array of storage groups
arrSGs=iServer.StorageGroups
```

然后就是枚举数组的问题。我们通过使用组的 URL（本质上是其可分辨名称）建立到每个存储组的连接来实现这一点。

```
'get the URL for each storage group
    strSGUrl=arrSGs(i)
     'connect to each storage group
     iSGs.DataSource.Open "LDAP://" & iServer.DirectoryServer & "/" &_
strSGUrl
```

存储组对象有几个值得关注的属性，包括存储组日志文件的路径和系统事务日志的路径。

```
strData=strData & iSGs.Name & VBcRLF
        strData=strData & vbTab & "LogPath: " &iSGs.LogFilePath & vbCrlf
        strData=strData & vbTab & "SystemPath:" & iSGs.SystemFilePath & VBCRLF
```

有一个 `MailboxStoreDBs` 属性可用于获取邮箱存储信息。我们将在本章后面介绍这个属性。

虽然在单个 Exchange 服务器上创建新的存储组是一个相对简单的任务，但如果您希望自动化构建过程或必须配置许多 Exchange 服务器，您可能希望将这个过程脚本化。清单 15-8 中的脚本可用于创建新的存储组。

## 清单 15-8 创建存储组

```
'CreateNewSG.vbs
strTitle="Create New Storage Group"
strServer=InputBox("What is the name of the Exchange Server?",strTitle,_
"MAIL01")
strNewSG=InputBox("What is the name of the new storage group?",strTitle,_
"ScriptingAnswers")

CreateNewStorageGroup strNewSG,strServer
WScript.Echo "Done!"

WScript.quit

Sub CreateNewStorageGroup(strSGName,strComputerName)

  On Error Resume Next
  Dim iServer
  Dim iStGroup
  Dim strTemp
Set iServer=CreateObject("CDOEXM.ExchangeServer")
Set iStGroup=CreateObject("CDOEXM.StorageGroup")

    ' Set the name of the StorageGroup
    iStGroup.Name = strSGName

    ' Bind to the Exchange Server
    iServer.DataSource.Open strComputerName

    For Each sg In iServer.StorageGroups
        strTemp = sg
        Exit For
    Next
    'cut out the Storage Group name from URL
    strTemp = Mid(strTemp, InStr(2, strTemp, "CN"))
    ' Build the URL to the StorageGroup
    strSGUrl = "LDAP://" & iServer.DirectoryServer & "/CN=" & strSGName & _
    "," & strTemp
    WScript.Echo "Creating " & strSGUrl
    ' Save the StorageGroup
    iStGroup.DataSource.SaveTo strSGUrl

End Sub
```

该子程序创建存储组。我们需要指定存储组的名称以及它将在其上创建的 Exchange 服务器的名称。就像我们在清单 15-7 中所做的那样，我们为 Exchange 服务器和存储组创建 CDOEXM 对象。

```
Set iServer=CreateObject("CDOEXM.ExchangeServer")
Set iStGroup=CreateObject("CDOEXM.StorageGroup")
```

给定存储组的名称，我们可以设置存储组对象的名称。

```
' Set the name of the StorageGroup
iStGroup.Name = strSGName
```

我们通过使用 *Exchange CDOEXM* 对象的 *DataSource* 属性绑定到 Exchange 服务器。

```
' Bind to the Exchange Server
iServer.DataSource.Open strComputerName
```

要创建新的存储组，我们需要知道存储组的完整 URL。我们可以将长字符串作为参数输入，但那会很麻烦。相反，我们查看 Exchange 服务器上任何现有存储组的 URL，并保存我们需要的部分。我们遍历所有存储组，获取第一个并退出循环。

```
For Each sg In iServer.StorageGroups
    strTemp = sg
    Exit For
Next
```

我们使用 *Mid* 函数来删除存储组的名称，这将为我们留下基础 URL。

```
'cut out the Storage Group name from URL
strTemp = Mid(strTemp, InStr(2, strTemp, "CN"))
```

然后我们可以创建新存储组的 URL。

```
' Build the URL to the StorageGroup
strSGUrl = "LDAP://" & iServer.DirectoryServer & "/CN=" & strSGName & "," & strTemp
```

有了 URL，我们就可以使用 *SaveTo* 方法来创建新的存储组。

```
wScript.Echo "Creating " & strSGUrl
' Save the StorageGroup
istGroup.DataSource.SaveTo strSGUrl
```

新存储组的日志和数据库文件将使用其默认设置。您可以在创建存储组后使用 *MoveLogFiles* 和 *MoveSystemFiles* 方法来更改位置。

删除存储组非常容易，如清单 15-9 所示。

## 清单 15-9 删除存储组
```
'Delete Storage Group
strTitle="Delete Storage Group"
strServer=InputBox("What is the name of the Exchange Server?",_
strTitle,"MAIL01")
strSG=InputBox("What is the name of the storage group to delete?",_
strTitle,"ScriptingAnswers")

DeleteSG strServer,strSG

Sub DeleteSG(strServer,strSGName)

Dim iServer, iSTGroup
Dim arrSGs

strSGUrl=""
Set iServer=Createobject("CDOEXM.ExchangeServer")
Set iSTGroup=Createobject("CDOEXM.storagegroup")

iServer.DataSource.Open strServer

arrSGs=iServer.StorageGroups

For i=0 To UBound(arrSGs)
If InStr(1, UCase(arrSGs(i)), UCase(strSGName)) <> 0 Then
strSGUrl = arrSGs(i)
End If
Next
```



如果 `strSGurl` 不为空，则：
    ' 绑定到存储组
    iSTGroup.DataSource.Open "LDAP://" & iServer.DirectoryServer & "/" & strSGurl
    rc = MsgBox("您确定要删除" & vbCrLf & strSGurl & "吗？", vbYesNo, strTitle)
        If rc = vbYes Then
            ' 删除存储组
            iSTGroup.DataSource.Delete
        End If
    End If

End Sub
```

从结构上看，此脚本与清单 15-8 非常相似。在我们连接到 Exchange 服务器和存储组之后，我们只需查看每个存储组的名称，直到找到我们想要删除的那一个。

```
arrSGs = iServer.StorageGroups
For i = 0 To UBound(arrSGs)
    If InStr(1, UCase(arrSGs(i)), UCase(strSGName)) <> 0 Then
        strSGUrl = arrSGs(i)
    End If
Next
```

获得存储组的 URL 后，我们就可以绑定到它。

```
If strSGurl <> "" Then
    ' 绑定到存储组
    iSTGroup.DataSource.Open "LDAP://" & iServer.DirectoryServer & "/" & strSGurl
```

在删除像存储组这样重要的内容时，向用户确认总是一个好主意。但假设用户确认了删除，我们只需调用 Delete 方法，存储组就会被删除。

```
rc = MsgBox("您确定要删除" & vbCrLf & strSGurl & "吗？", vbYesNo, strTitle)
    If rc = vbYes Then
        ' 删除存储组
        iSTGroup.DataSource.Delete
```

### 编写 Exchange 邮箱脚本

处理邮箱存储和单个邮箱需要多种技术。我们将使用 CDOEXM 来管理邮箱存储，其方式与我们管理存储组的方式非常相似。我们将使用 WMI 来管理每个存储组中的单个邮箱。我们还将使用 ADSI 来管理邮箱和安全账户之间的连接。让我们从下一页清单 15-10 中的脚本开始，该脚本将列出给定 Exchange 服务器的所有邮箱存储。

第四部分：企业脚本编写

```
清单 15-10 列出邮箱存储
strTitle = "邮箱存储数据库报告"
strServer = InputBox("Exchange 服务器的名称是什么？", _
    strTitle, "MAIL01")

MBReport strServer
WScript.Quit

Sub MBReport(strServer)
Dim iServer
Dim iSGs
Dim iMBS

Set iServer = CreateObject("CDOEXM.ExchangeServer")
Set iSGs = CreateObject("CDOEXM.StorageGroup")
Set iMBS = CreateObject("CDOEXM.MailboxStoreDB")
iServer.DataSource.Open strServer

arrSGs = iServer.StorageGroups

For i = 0 To UBound(arrSGs)
    strSGUrl = arrSGs(i)
    'WScript.Echo strSGUrl
    iSGs.DataSource.Open "LDAP://" & iServer.DirectoryServer & _
    "/" & strSGUrl
    strData = strData & iSGs.Name & vbCrlf
    arrMBStores = iSGs.MailboxStoreDBs
    For j = 0 To UBound(arrMBStores)
        iMBS.DataSource.open "LDAP://" & arrMBStores(j)
        strData = strData & vbTab & iMBS.Name & vbCrLf
        strData = strData & vbTab & iMBS.Status & vbCrLf
        strData = strData & vbTab & " 数据库路径:" & iMBS.DBPath & vbCrLf
        strData = strData & vbTab & " 流式数据库路径:" & _
        iMBS.SLVPath & vbCrLf
        strData = strData & vbTab & " 上次备份时间:" & _
        iMBS.LastFullBackupTime & vbCrLf
        strData = strData & vbTab & " 存储配额警告:" & _
        iMBS.StoreQuota & vbCrLf
        strData = strData & vbTab & " 存储配额限制:" & _
        iMBS.OverQuotaLimit & vbCrLf
    Next
Next

WScript.Echo strData

End Sub
```

此脚本的格式现在应该看起来非常熟悉了，因此我们不会花太多时间重新分析它。每个存储组对象都有一个 *MailboxStoreDBs* 属性，该属性返回给定存储组的邮箱存储集合。

```
arrMBStores = iSGs.MailboxStoreDBs
```

与存储组一样，每个邮箱存储都用 URL 定义。我们可以使用此 URL 建立与每个邮箱存储的连接。

```
For j = 0 To UBound(arrMBStores)
    iMBS.DataSource.open "LDAP://" & arrMBStores(j)
```

连接后，我们可以显示有关每个邮箱存储的属性信息。

```
iMBS.DataSource.open "LDAP://" & arrMBStores(j)
strData = strData & vbTab & iMBS.Name & vbCrLf
strData = strData & vbTab & iMBS.Status & vbCrLf
strData = strData & vbTab & " 数据库路径:" & iMBS.DBPath & vbCrLf
strData = strData & vbTab & " 流式数据库路径:" & _
    iMBS.SLVPath & vbCrLf
strData = strData & vbTab & " 上次备份时间:" & _
    iMBS.LastFullBackupTime & vbCrLf
strData = strData & vbTab & " 存储配额警告:" & _
    iMBS.StoreQuota & vbCrLf
strData = strData & vbTab & " 存储配额限制:" & _
    iMBS.OverQuotaLimit & vbCrLf
```

如果您想装入或卸除存储，可以分别使用 Mount 或 Dismount 方法。

iMBS.Dismount

如果您创建新的邮箱存储，就像我们在清单 15-11 中所做的那样，您必须使用 Mount 方法。

```
清单 15-11 创建邮箱存储
strTitle = "创建新邮箱存储"
strServer = InputBox("Exchange 服务器的名称是什么？", _
    strTitle, "MAIL01")
strSG = InputBox("要在哪个存储组下创建新邮箱存储？", strTitle, "第一个存储组")
strMDBName = InputBox("新邮箱存储的名称是什么？", _
    strTitle, "ScriptingAnswers Mail")

CreateNewMailStoreDB strMDBName, strServer, strSG
wScript.Quit

Sub CreateNewMailStoreDB(strMDBName, strServer, strSG)

Dim iServer
Dim iMDB

Set iServer = CreateObject("CDOEXM.ExchangeServer")
Set iMDB = CreateObject("CDOEXM.MailboxStoreDB")
' 设置 MailboxStoreDB 的名称
iMDB.Name = strMDBName
```

第四部分：企业脚本编写

```
' 绑定到 Exchange 服务器
iServer.DataSource.Open strServer

' 开始构建指向 MailboxStoreDB 的 URL - 第一部分
strTemp = "LDAP://" & iServer.DirectoryServer & "/" & "cn=" & strMDBName & ","

arrStGroup = iServer.StorageGroups

' 检查 StorageGroups 数组中是否存在名为 strSG 的存储组
If strSG = "" Then
    ' 完成构建指向 MailboxStoreDB 的 URL - 添加最后一部分
    strMDBUrl = strTemp & iServer.StorageGroups(0)
Else
    For i = 0 To UBound(arrStGroup)
        If InStr(1, UCase(arrStGroup(i)), UCase(strSG)) <> 0 Then
            strMDBUrl = arrStGroup(i)
        End If
    Next
    If strMDBUrl <> "" Then
        ' 完成构建指向 MailboxStoreDB 的 URL - 添加最后一部分
        strMDBUrl = strTemp & strMDBUrl
    End If
End If

' 保存新的 MailboxStoreDB
iMDB.DataSource.SaveTo strMDBUrl

' 装入 MailboxStoreDB
iMDB.Mount
WScript.Echo "已完成 " & strMDBName & " 的创建"
End Sub
```

要创建邮箱存储，我们需要知道 Exchange 服务器、存储组和新邮箱存储的名称。

```
strServer = InputBox("Exchange 服务器的名称是什么？", _
    strTitle, "MAIL01")
strSG = InputBox("要在哪个存储组下创建新邮箱存储？", _
    strTitle, "第一个存储组")
strMDBName = InputBox("新邮箱存储的名称是什么？", _
    strTitle, "ScriptingAnswers Mail")
```

创建邮箱存储需要 Exchange 服务器和邮箱存储的 CDOEXM 对象，但有趣的是，不需要存储组的。

```
Set iServer = CreateObject("CDOEXM.ExchangeServer")
Set iMDB = CreateObject("CDOEXM.MailboxStoreDB")
```

就像我们创建存储组时所做的一样，我们可以设置邮箱存储的平面名称并创建邮箱存储 URL。在将更改提交给 Exchange 服务器时，我们将需要此 URL。

```
' 设置 MailboxStoreDB 的名称
iMDB.Name = strMDBName
```

```
' 绑定到 Exchange 服务器
iServer.DataSource.Open strServer
```

```
' 开始构建指向 MailboxStoreDB 的 URL - 第一部分
strTemp = "LDAP://" & iServer.DirectoryServer & "/" & "cn=" & _
    strMDBName & ","
```

因为邮箱存储包含在存储组中，所以我们需要获取存储组的 URL，因为这将是最终邮箱存储 URL 的一部分，即 strMDBUrl 变量。

```
arrStGroup = iServer.StorageGroups
```

```
' 检查 StorageGroups 数组中是否存在名为 strSG 的存储组
If strSG = "" Then
    ' 完成构建指向 MailboxStoreDB 的 URL - 添加最后一部分
    strMDBUrl = strTemp & iServer.StorageGroups(0)
Else
    For i = 0 To UBound(arrStGroup)
        If InStr(1, UCase(arrStGroup(i)), UCase(strSG)) <> 0 Then
            strMDBUrl = arrStGroup(i)
        End If
    Next
    If strMDBUrl <> "" Then
        ' 完成构建指向 MailboxStoreDB 的 URL - 添加最后一部分
        strMDBUrl = strTemp & strMDBUrl
    End If
End If
```

获得邮箱存储的 URL 后，我们就可以将更改提交给 Exchange 服务器，然后邮箱存储就会被创建。

```
' 保存新的 MailboxStoreDB
iMDB.DataSource.SaveTo strMDBUrl
```

装入存储后，它就可以使用了。

```
' 装入 MailboxStoreDB
iMDB.Mount
```

正如下一页清单 15-12 中的脚本所示，要删除邮箱存储，我们首先需要其 URL。获得该 URL 后，我们就可以连接到邮箱存储并调用 Delete 方法。



## 清单 15-12 删除邮箱存储

```vb
strTitle="Delete MailBox Store"
strServer=InputBox("What is the name of the Exchange Server?",
strTitle,"MAIL01")
strSG=InputBox("What Storage Group is the mail db in?",strTitle,
"First Storage Group")
strMDBName=InputBox("What is the name of the mail store to delete?",
strTitle,"ScriptingAnswers Mail")

DeleteMDBStore strServer,strSG,strMDBName
wScript.Quit

Sub DeleteMDBStore(strServer,strSG,strMDBName)

Dim iServer,iMDB

Set iServer=CreateObject("CDOEXM.ExchangeServer")
Set iMDB=CreateObject("CDOEXM.MailboxStoreDB")

iServer.DataSource.Open strServer

strTemp = "LDAP://" & iServer.DirectoryServer & "/" & "cn=" & strMDBName &
""

arrStGroup = iServer.StorageGroups

' 在 StorageGroups 数组中查找是否存在名为 strSGName 的存储组
If strSG = "" Then
    ' 将 URL 的最后部分添加到 MailboxStoreDB
    strMDBUrl = strTemp & iServer.StorageGroups(0)
Else
    For i = 0 To UBound(arrStGroup)
        If InStr(1, UCase(arrStGroup(i)), UCase(strSG)) <> 0 Then
            strMDBUrl = arrStGroup(i)
        End If
    Next
    If strMDBUrl <> "" Then
        ' 将 URL 的最后部分添加到 MailboxStoreDB
        strMDBUrl = strTemp & strMDBUrl
    End If
End If

' 绑定到 MailboxStoreDB
iMDB.DataSource.Open strMDBUrl

' 删除 MailboxStoreDB
iMDB.DataSource.Delete

WScript.Echo "Deleted " & strMDBName

End Sub
```

要在特定的邮箱存储中创建一个单独的邮箱，我们需要使用 ADSI。每个邮箱都连接到 Active Directory 中的一个用户或组 SID，因此我们使用 ADSI 来修改 Active Directory 中的用户对象。要创建邮箱，你需要知道邮箱存储的可分辨名称。它看起来会像这样。

```vb
"CN=Mailbox Store (MAIL01),CN=First Storage Group,CN=InformationStore," & _
"CN=MAIL01,CN=Servers,CN=First Administrative Group,CN=Administrative " & _
"Groups,CN=MATRIX,CN=Microsoft Exchange,CN=Services, CN=Configuration," & _
"DC=COMPANY,DC=PRI"
```

如果你只有一个邮箱存储，你可以将此名称硬编码到脚本中。但对于更动态的情况，你可能需要搜索 Active Directory 获取邮箱存储列表，将其呈现给管理员，然后让他或她进行选择。清单 15-13 中的脚本演示了这一点。

## 清单 15-13 创建邮箱

```vb
Dim objUser
On Error Resume Next
strUserDN="CN=Jeff Hicks,OU=Employees,DC=Company,DC=Pri"

Set objUser=GetObject("LDAP://" & strUserDN)
If objUser.HomeMDB="" Then
    strMailDN=SelectMailStore()
    WScript.Echo "Creating mailbox For " & objUser.cn & " on " & _
        strMailDN
    objUser.CreateMailbox strMailDN
    objUser.SetInfo
    If Err.Number <>0 Then
        strMsg="Error creating mailbox for " & objUser & " on " & _
            strMailDN & vbCRLF & Err.Number & " " & Err.Description
        WScript.Echo strMsg
    Else
        WScript.Echo "Successfully created mailbox for " & strUserDN
    End If
Else
    WScript.Echo objUser.cn & " already has a mailbox"
End If
WScript.Quit
'///////////////////////////////////////////////////
Function SelectMailStore()
On Error Resume Next
Dim objRootDSE
Dim objConfiguration
Dim cat
Dim conn
Dim cmd
Dim RS
Dim objDict

Set objDict=CreateObject("scripting.dictionary")
Set objRootDSE = GetObject("LDAP://rootDSE")
x=1

strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)

strQuery="Select name,cn,distinguishedname from '" & _
objConfiguration.ADSPath & "' Where objectclass='msExchPrivateMDB'"

set cat=GetObject("GC:")
for each obj In cat
    set GC=obj
Next

AdsPath=GC.ADSPath

set conn=CreateObject("ADODB.Connection")
set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open

set cmd.ActiveConnection=conn
set RS=conn.Execute(strQuery)

do while not RS.EOF
    DN=rs.Fields("distinguishedname")
    CN=RS.Fields("cn")
    NM=RS.Fields("name")
    objDict.Add x,DN
    strResults=strResults & "(" & x & ") " &DN & VbCrLf
    x=x+1
    rs.movenext
Loop
rs.Close
conn.Close
t=1

a=objDict.Items
    For i=0 To objDict.Count-1
    c=c & "(" & i+1 & ")" & a(i) & VbCrLf
    '以每组4个的方式显示可用的邮箱存储
            If t<4 AND i<>objDict.count-1 Then
                t=t+1
            Else
                MsgBox c,vbOKOnly,"Available Mailbox Stores"
                t=1
                c=""
            End If
    Next
iDN=Inputbox("Enter in the number of the mail store you want to use.",_
"Select Mail Store","0")
    If iDN = "" Then
        WScript.Echo "Nothing entered or you cancelled."
        WScript.Quit
    End If

If objDict.Exists(Int(iDN)) Then
    SelectMailStore=objDict.Item(Int(iDN))
Else
    rc=msgBox ("You selected an invalid number. Try again.",_
    vbOKCancel+vbExclamation,"Select Mail Store")
    if rc=vbCancel Then
        wscript.Quit
    Else
        Main()
    End If
End If
End Function
```

该脚本需要一个用户对象的可分辨名称。在这个脚本中，为了简单起见，我们硬编码了一个名称。然后我们连接到 Active Directory 中的用户对象，并通过检查 *HomeMDB* 属性来检查是否已存在邮箱。

```vb
strUserDN="CN=Jeff Hicks,OU=Employees,DC=Company,DC=Pri"

Set objUser=GetObject("LDAP://" & strUserDN)
If objUser.HomeMDB="" Then
```

如果该属性为空，我们调用函数来列出可用的邮箱存储。

```vb
    strMailDN=SelectMailStore()
```

该函数在配置命名上下文中搜索所有对象类为 *msExch-PrivateMDB* 的对象。

```vb
Set objDict=CreateObject("scripting.dictionary")
Set objRootDSE = GetObject("LDAP://rootDSE")
x=1
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)

strQuery="Select name,cn,distinguishedname from '" & _
objConfiguration.ADSPath & "' Where objectclass='msExchPrivateMDB'"
```

该函数将结果放入一个字典对象中。

```vb
set cmd.ActiveConnection=conn
set RS=conn.Execute(strQuery)

Do while not RS.EOF
    DN=rs.Fields("distinguishedname")
    CN=RS.Fields("cn")
    NM=RS.Fields("name")
    objDict.Add x,DN
    strResults=strResults &"(" & x & ") " &DN & VbCrLf
    x=x+1
    'wscript.Echo vbcrlf
    rs.movenext

Loop
```

字典对象的项是所有邮箱存储的可分辨名称。我们枚举字典并向管理员呈现一个带编号的列表。

```vb
a=objDict.Items
    For i=0 To objDict.Count-1
        c=c & "(" & i+1 & ")" & a(i) & vbCrLf
        '以每组4个的方式显示可用的邮箱存储
            If t<>4 AND i<>objDict.count-1 Then
                t=t+1
            Else
                MsgBox c,vbOKOnly,"Available Mailbox Stores"
                t=1
                c=""
            End If
    Next
```

紧接着是一个 *InputBox* 函数，管理员可以在此输入他或她想要使用的邮箱存储的编号。该函数返回邮箱存储的可分辨名称。一旦我们获得了此信息，创建邮箱就非常简单了。

```vb
objUser.CreateMailbox strMailDN
objUser.SetInfo
```

> **注意** 你可以从你的桌面运行清单 15-13 中的脚本，前提是你除了安装 Exchange 管理控制台外，还安装了管理工具包 (adminpak.msi)。你可以在域控制器上创建邮箱，但该控制器也必须安装 Exchange 管理控制台。如果没有它，你将无法在 Active Directory 中的用户对象上看到 Exchange 管理选项卡。

如果你想移动一个用户的邮箱，你需要知道它将被移动到的邮箱存储的名称。考虑清单 15-14 中的脚本。它与清单 15-13 非常相似，只是我们使用了 *MoveMailbox* 方法。

## 清单 15-14 移动邮箱

```vb
On Error Resume Next
Dim objUser
strTitle="Move Mailbox Demo"
strDefault="LDAP://CN=Jeff Hicks,CN=Users,DC=Company,DC=Pri"
strUserDN=InputBox("Enter the full distinguished name of the user:",_
                strTitle,strDefault)

Set objUser=GetObject(strUserDN)

if objUser.HomeMDB="" Then
    MsgBox "User has no mailbox defined"
    WScript.Quit
Else
    MsgBox "The user's current mailbox is on " & vbcrlf & objUser.HomeMDB
End If
```



## 第15章：Exchange 2003 脚本编程

'调用一个函数来列出可用的邮箱存储
strNewMailDN=SelectMailStore

MsgBox "根据邮箱大小，移动操作可能需要几分钟"

objUser.MoveMailBox "LDAP://" & strNewMailDN
objUser.SetInfo
Wscript.Echo "已完成。"

Wscript.quit

Function SelectMailStore()
On Error Resume Next
Dim objRootDSE
Dim objConfiguration
Dim cat
Dim conn
Dim cmd
Dim RS
Dim objDict

Set objDict=CreateObject("scripting.dictionary")
Set objRootDSE = GetObject("LDAP://rootDSE")
x=1
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)

strQuery="Select name,cn,distinguishedname from '" & _
objConfiguration.ADSPath & "' where objectclass='msExchPrivateMDB'"

set cat=GetObject("GC:")
for each obj in cat
    set GC=obj
Next

AdsPath=GC.ADSPath

set conn=CreateObject("ADODB.Connection")
set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open

set cmd.ActiveConnection=conn
set RS=conn.Execute(strQuery)

do while not RS.EOF
    DN=rs.Fields("distinguishedname")
    CN=RS.Fields("cn")
    NM=RS.Fields("name")
    objDict.Add x,DN
    strResults=strResults &"(" & x & ") " &DN & vbcrlf
    x=x+1
    rs.movenext
Loop

rs.Close
conn.Close
t=1

a=objDict.Items
    For i=0 To objDict.Count-1
    c=c & "(" & i+1 & ")" & a(i) & vbcrLf
    '每组显示4个可用的邮箱存储
        If t<4 And i<>objDict.count-1 Then
            t=t+1
        Else
            MsgBox c,vbOKOnly,"可用的邮箱存储"
            t=1
            c=""
        End If
    Next

iDN=Inputbox("输入你想使用的邮箱存储的编号。","选择邮箱存储","0")
    If iDN = "" Then
        WScript.Echo "未输入内容或已取消。"
        WScript.Quit
    End If

If objDict.Exists(Int(iDN)) Then
    SelectMailStore=objDict.Item(Int(iDN))
Else
    rc=msgBox ("你选择的编号无效。请重试。",
vbOKCancel+vbExclamation,"选择邮箱存储")
    if rc=vbCancel Then
        wscript.Quit
    Else
        Main()
    End If
End If

End Function

要删除邮箱，实际上只是切断邮箱与用户 SID 的关联，我们只需建立到 Active Directory 中用户对象的连接，并调用 *DeleteMailbox* 方法。

```
strUserDN="CN= Jeff Hicks,OU=Authors,DC=company,DC=pri"
set objUser=GetObject("LDAP://" & strUserDN)
objUser.DeleteMailbox
```

要收集特定邮箱的信息，我们回到 WMI 和 *Exchange_Mailbox* 类。清单 15-15 枚举了给定用户邮箱的属性。

### 清单 15-15 获取邮箱信息
```
On Error Resume Next
Dim strComputer
Dim objWMIService
Dim propValue
Dim SWBemlocator
Dim UserName
Dim Password
Dim colItems

strComputer = "MAIL01"
'如有必要，指定备用凭据
UserName = ""
Password = ""
strTitle="邮箱查询"
strMailBox=InputBox("输入邮箱的显示名称",_
strTitle,"Administrator")
Set SWBemlocator = CreateObject("WbemScripting.SwbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer,_
"\\root\\microsoftexchangev2",UserName,Password)
Set colItems = objWMIService.ExecQuery("Select * from Exchange_Mailbox " &_
"WHERE MailboxDisplayName='" & strMailBox & "'",,48)
For Each objItem in colItems
	If UCase(objItem.MailboxDisplayName)=UCase(strMailBox) Then
		WScript.Echo "AssocContentCount: " & objItem.AssocContentCount
		WScript.Echo "Caption: " & objItem.Caption
		WScript.Echo "DateDiscoveredAbsentInDS: " &_
			objItem.DateDiscoveredAbsentInDS
		WScript.Echo "DeletedMessageSizeExtended: " &_
			objItem.DeletedMessageSizeExtended
		WScript.Echo "Description: " & objItem.Description
		WScript.Echo "InstallDate: " & objItem.InstallDate
		WScript.Echo "LastLoggedOnUserAccount: " &_
			objItem.LastLoggedOnUserAccount
		WScript.Echo "LastLogoffTime: " & objItem.LastLogoffTime
		WScript.Echo "LastLogonTime: " & objItem.LastLogonTime
		WScript.Echo "LegacyDN: " & objItem.LegacyDN
		WScript.Echo "MailboxDisplayName: " & objItem.MailboxDisplayName
		WScript.Echo "MailboxGUID: " & objItem.MailboxGUID
		WScript.Echo "Name: " & objItem.Name
		WScript.Echo "ServerName: " & objItem.ServerName
		WScript.Echo "Size: " & objItem.Size
		WScript.Echo "Status: " & objItem.Status
		WScript.Echo "StorageGroupName: " & objItem.StorageGroupName
		WScript.Echo "StorageLimitInfo: " & objItem.StorageLimitInfo
		WScript.Echo "StoreName: " & objItem.StoreName
		WScript.Echo "TotalItems: " & objItem.TotalItems
	Else
		WScript.Echo "无法找到 " & strMailBox & " 的邮箱"
	End If
Next
```

该脚本使用查询返回 Exchange 邮箱对象的所有属性，其中显示名称与输入框中提供的名称匹配。

```
Set colItems = objWMIService.ExecQuery("Select * from Exchange_Mailbox " &_
"WHERE MailboxDisplayName='" & strMailbox & "'",48)
```

如果你想获取多个用户的信息，只需查询所有用户。查看清单 15-16 中的脚本。

### 清单 15-16 创建邮箱报告
```
Dim SWBemlocator
Dim objWMIService
Dim colItems
Dim objFSO
Dim objFile
strTitle="邮箱报告"
strComputer ="MAIL01"
UserName = ""
Password = ""
strLog="MailboxReport.csv"
Set objFSO=CreateObject("Scripting.FileSystemObject")
Set objFile=objFSO.CreateTextFile(strLog,True)

strQuery="Select * from Exchange_Mailbox"
objFile.WriteLine "Server,StorageGroup,MailStore,User,Size(KB),TotalItems"
WScript.Echo "正在检查 " & strComputer
Set SWBemlocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer,_
"\root\MicrosoftExchangeV2",UserName,Password)
Set colItems = objWMIService.ExecQuery(strQuery,,48)

For Each objItem in colItems
  objFile.writeline objItem.ServerName & "," &objItem.StorageGroupName &_
  "," & objItem.StoreName & "," & Chr(34) & objItem.MailboxDisplayName &_
  Chr(34) & "," & objItem.Size & "," & objItem.TotalItems
Next

objFile.close

wScript.Echo "结果请查看 " & strLog
```

此脚本为给定 Exchange 服务器上的所有 Exchange 邮箱创建报告。结果写入逗号分隔值（CSV）文件，因此你可以轻松地在 Microsoft Excel 中查看该文件。

## 实际查看 Exchange 服务器脚本

在结束本章之前，让我们再看一个脚本示例，它将大量材料汇集在一个脚本中。清单 15-17 中的脚本将为组织中的所有 Exchange 服务器生成一份主报告，包含版本信息、服务信息、队列状态、存储组、邮箱存储、邮箱和公共文件夹。

### 清单 15-17 创建主 Exchange 报告
```
'MasterExchange.vbs
'用法：cscript MasterExchange.vbs
'你必须安装 Exchange 管理工具才能运行此脚本。

arrServers=GetExchangeServers

For s = 0 To UBound(arrServers)-1
    WScript.Echo "*****服务器信息*****"
    ExchangeServerInfo arrServers(s)
    WScript.Echo "*****服务器状态*****"
    ExchangeServerState arrServers(s),"","
    WScript.Echo "*****服务状态*****"
    GetServiceStatus arrServers(s)
    WScript.Echo "*****队列状态*****"
    GetQueueInfo arrServers(s)
    WScript.Echo "*****存储组*****"
    GetStorageGroups arrServers(s)
    WScript.Echo "*****公共文件夹*****"
    GetPublicFolderInfo arrServers(s),"","
Next
WScript.quit
'/////////////////////////////////////////////////
Function GetExchangeServers()
' 在 AD 中查找所有服务器
'返回 Exchange 服务器名称数组
wScript.Echo "正在查询 Active Directory 中的 Exchange 服务器"
Dim objRootDSE
Dim objConfiguration
Dim cat
Dim conn
Dim cmd
Dim RS
Set objRootDSE = GetObject("LDAP://rootDSE")

strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)

'选择 Exchange 服务器，但不选择共享相同类的策略
strQuery="Select distinguishedname,name from '" & _
objConfiguration.ADSPath & "' where objectclass='msExchExchangeServer' " &_
"AND objectclass<>'msExchExchangeServerPolicy'"

strResults=""
Set cat=GetObject("GC:")
For each obj In cat
  Set GC=obj
Next

AdsPath=GC.ADSPath

Set conn=CreateObject("ADODB.Connection")
Set cmd=CreateObject("ADODB.Command")
```

# 第四部分：企业脚本编写

```
conn.Provider="ADSObject"
conn.Open

Set cmd.ActiveConnection=conn
Set RS=conn.Execute(strQuery)
Do While Not RS.EOF
  strResults=strResults & RS.Fields("name") & ";"
  RS.MoveNext
Loop
RS.Close
conn.Close
GetExchangeServers=Split(strResults, ";")

End Function

Sub GetStorageGroups(strServer)
'获取指定服务器上的存储组列表
Dim objRootDSE
Dim objConfiguration
Dim conn
Dim cmd
Dim RS

Set objRootDSE = GetObject("LDAP://rootDSE")
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)
strPath=objConfiguration.ADSPath

strQuery="Select distinguishedname,name,whencreated from '" & strPath & _
"' WHERE objectclass='msExchStorageGroup'"

Set cat=GetObject("GC:")
For Each obj In cat
  Set GC=obj
Next

Set conn=CreateObject("ADODB.Connection")
Set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSObject"
conn.Open

Set cmd.ActiveConnection=conn
Set RS=conn.Execute(strQuery)
Do While Not RS.EOF
  If InStr(UCase(RS.Fields("distinguishedname")),UCase(strServer)) Then
    WScript.Echo RS.Fields("name") & "(创建于 " & _
      RS.Fields("whencreated") & ")"
    SGReport strServer,RS.Fields("name")
  End If
  RS.MoveNext
Loop
RS.Close
conn.Close

End Sub

Sub ExchangeServerInfo(strSrv)
Set objWMIService = GetObject("winmgmts:\\" & strSrv & _
    "\\root\\MicrosoftExchangev2")
Set colItems = objWMIService.ExecQuery("Select AdministrativeGroup,DN," & _
    "ExchangeVersion,FQDN,Name,RoutingGroup,CreationTime,Name," & _
    "IsFrontEndServer,MessageTrackingEnabled,SubjectLoggingEnabled," & _
    "LastModificationTime from Exchange_Server where name='" & strSrv & _
    "'",,48)

For Each objItem In colItems
    If objItem.FQDN="" Then
        WScript.Echo "无法从 WMI 获取 Exchange 服务器信息。" & _
            "请验证 Microsoft Exchange 管理服务是否在 " & _
            strSrv & " 上运行"
    Else
        WScript.Echo UCase(objItem.FQDN) & " [" & _
            objItem.ExchangeVersion & "]"
        WScript.Echo "管理组: " & _
            objItem.AdministrativeGroup
        WScript.Echo "最后修改时间: " & _
            ConvertTime(objItem.LastModificationTime)
        WScript.Echo "前端服务器: " & objItem.IsFrontEndServer
        WScript.Echo "邮件跟踪: " & objItem.MessageTrackingEnabled
        WScript.Echo "主题记录: " & objItem.SubjectLoggingEnabled
    End If
Next
End Sub

Function ConvertTime(strTime)
On Error Resume Next

Yr = Left(strTime,4)
Mo = Mid(strTime,5,2)
Dy = Mid(strTime,7,2)
Tm = Mid(strTime,9,6)

ConvertTime=Mo & "/" & Dy & "/" & Yr

End Function

Sub ExchangeServerState(strComputer,UserName,Password)
Dim objWMIService
Dim PropValue
Dim objItem
Dim SWBemLocator
Dim colItems

Set SWBemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemLocator.ConnectServer(strComputer,_
    "\\root\\cimv2\\applications\\exchange",UserName,Password)
strQuery="Select * from ExchangeServerState"
Set colItems = objWMIService.ExecQuery(strQuery,,48)
For Each objItem In colItems
    WScript.Echo "群集状态: " & objItem.ClusterState
    WScript.Echo "群集状态字符串: " & objItem.ClusterStateString
    WScript.Echo "CPU状态: " & objItem.CPUState
    WScript.Echo "CPU状态字符串: " & objItem.CPUStateString
    WScript.Echo "磁盘状态: " & objItem.DisksState
    WScript.Echo "磁盘状态字符串: " & objItem.DisksStateString
    WScript.Echo "标识名: " & objItem.DN
    WScript.Echo "组标识名: " & objItem.GroupDN
    WScript.Echo "组GUID: " & objItem.GroupGUID
    WScript.Echo "GUID: " & objItem.GUID
    WScript.Echo "内存状态: " & objItem.MemoryState
    WScript.Echo "内存状态字符串: " & objItem.MemoryStateString
    WScript.Echo "名称: " & objItem.Name
    WScript.Echo "队列状态: " & objItem.QueuesState
    WScript.Echo "队列状态字符串: " & objItem.QueuesStateString
    WScript.Echo "服务器维护: " & objItem.ServerMaintenance
    WScript.Echo "服务器状态: " & objItem.ServerState
    WScript.Echo "服务器状态字符串: " & objItem.ServerStateString
    WScript.Echo "服务状态: " & objItem.ServicesState
    WScript.Echo "服务状态字符串: " & objItem.ServicesStateString
    WScript.Echo "不可达: " & objItem.Unreachable
    WScript.Echo "版本: " & objItem.Version
Next

End Sub

Sub GetServiceStatus(strSrv)
On Error Resume Next
Set objWMIService = GetObject("winmgmts://" & strSrv)
strQuery="Select displayname,startmode,status,state from win32_service " & _
"where displayname LIKE 'Microsoft Exchange%'"

Set colSvc=objWMIService.ExecQuery(strQuery,,48)

For Each svc In colSvc
    WScript.Echo svc.DisplayName & vbTab & svc.State & vbTab & _
    svc.StartMode
Next

End Sub

Sub SGReport(strServer,strSG)
Dim iServer
Dim iSGs
Dim iMBS

Set iServer=CreateObject("CDOEXM.ExchangeServer")
Set iSGs=CreateObject("CDOEXM.StorageGroup")
Set iMBS=CreateObject("CDOEXM.MailboxStoreDB")
iServer.DataSource.Open strServer

arrSGs=iServer.StorageGroups

For i=0 To UBound(arrSGs)
    strSGUrl=arrSGs(i)
    'WScript.Echo strSGUrl
    If InStr(UCase(strSGUrl),UCase(strSG)) Then
        iSGs.DataSource.Open "LDAP://" & iServer.DirectoryServer & _
            "/" & strSGUrl
        'strData=strData & iSGs.Name & vbCrLf
        WScript.Echo vbTab & "日志路径: " & iSGs.LogFilePath
        WScript.Echo vbTab & "系统路径:" & iSGs.SystemFilePath
        WScript.Echo "  邮箱存储:"
        arrMBStores=iSGs.MailboxStoreDBs
        For j=0 To UBound(arrMBStores)
            iMBS.DataSource.Open "LDAP://" & arrMBStores(j)
            WScript.Echo vbTab & iMBS.Name
            WScript.Echo vbTab & "  数据库路径:" & iMBS.DBPath
            WScript.Echo vbTab & "  流文件路径:" & iMBS.SLVPath
            WScript.Echo vbTab & "  最后备份:" & iMBS.LastFullBackupTime
            WScript.Echo vbTab & "  存储配额警告:" & iMBS.StoreQuota
            WScript.Echo vbTab & "  存储配额限制:" & iMBS.OverQuotaLimit
            ListMailboxes iMBS.Name
        Next
    End If
Next
End Sub

Sub ListMailboxes(strMailStore)
On Error Resume Next
Dim objRootDSE
Dim objConfiguration
Dim conn
Dim cmd
Dim RS

Set objRootDSE = GetObject("LDAP://rootDSE")
strConfiguration = "LDAP://" & objRootDSE.Get("configurationNamingContext")
Set objConfiguration = GetObject(strConfiguration)
strPath=objConfiguration.ADSPath

strQuery="Select distinguishedname,name,homeMDBBL from '" & strPath & _
"' WHERE objectclass='msExchPrivateMDB' AND name='" & strMailStore & "'"

Set cat=GetObject("GC:")
For Each objCat In cat
    Set GC=objCat
Next

Set conn=CreateObject("ADODB.Connection")
Set cmd=CreateObject("ADODB.Command")
conn.Provider="ADSDSOObject"
conn.Open
Set cmd.ActiveConnection=conn
Set RS=conn.Execute(strQuery)

Do While Not RS.EOF
    WScript.Echo RS.Fields("distinguishedname")
    WScript.Echo vbTab & "位于 " & RS.Fields("name") & " 上的邮箱"
    tmpArray=RS.Fields("homeMDBBL")
    For m=0 To UBound(tmpArray)
        WScript.Echo vbTab & "  " & tmpArray(m)
    Next
    RS.MoveNext
Loop
RS.Close
conn.Close

End Sub

Sub GetQueueInfo(strSrv)
On Error Resume Next
Set objWMIService = GetObject("winmgmts:\\" & strSrv & _
    "\root\MicrosoftExchangev2")
strQuery="select * from Exchange_Queue"
Set colItems = objWMIService.ExecQuery(strQuery,,48)

WScript.Echo "队列 (协议)" & vbTab & "大小 (邮件数)"

For Each objItem In colItems
    WScript.Echo objItem.LinkName & "(" & objItem.ProtocolName & ")" & _
        vbTab & FormatNumber(objItem.Size/1024,2) & "(" & _
        objItem.MessageCount & ")"
Next

End Sub

Sub GetPublicFolderInfo(strComputer,UserName,Password)
On Error Resume Next
Dim objWMIService
Dim PropValue
Dim objItem
Dim SWBemLocator
Dim colItems

Set SWBemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWBemLocator.ConnectServer(strComputer,_
    "\\microsoftexchangev2",UserName,Password)
strQuery="Select * from Exchange_PublicFolder"
Set colItems = objWMIService.ExecQuery(strQuery,,48)
For Each objItem In colItems
    WScript.Echo "通讯簿名称: " & objItem.AddressBookName
    WScript.Echo "创建时间: " & ConvertTime(objItem.CreationTime)
    WScript.Echo "已删除项目保留期: " & objItem.DeletedItemLifetime
    WScript.Echo "描述: " & objItem.Description
    WScript.Echo "文件夹树: " & objItem.FolderTree
    WScript.Echo "友好 URL: " & objItem.FriendlyUrl
    WScript.Echo "是否有子项: " & objItem.HasChildren
    WScript.Echo "是否有本地副本: " & objItem.HasLocalReplica
    WScript.Echo "安装日期: " & ConvertTime(objItem.InstallDate)
    WScript.Echo "是否启用邮件: " & objItem.IsMailEnabled
    WScript.Echo "是否为普通文件夹: " & objItem.IsNormalFolder
    WScript.Echo "是否在站点内安全: " & objItem.IsSecureInSite
    WScript.Echo "最后访问时间: " & ConvertTime(objItem.LastAccessTime)
    WScript.Echo "最后修改时间: " & _
        ConvertTime(objItem.LastModificationTime)
    WScript.Echo "最大项目大小: " & objItem.MaximumItemSize
    WScript.Echo "邮件数: " & objItem.MessageCount
```

## 第15章：Exchange 2003 脚本编写

459



脚本的主要部分通过调用 *GetExchangeServers* 函数来获取组织中所有Exchange服务器的数组，然后简单地枚举每个服务器。

```
arrServers = GetExchangeServers

For s = 0 To UBound(arrServers) - 1
    WScript.Echo "*****Server Information*****"
    ExchangeServerInfo arrServers(s)
    WScript.Echo "*****Server Status*****"
    ExchangeServerState arrServers(s), "", ""
    WScript.Echo "*****Service Status*****"
    GetServiceStatus arrServers(s)
    WScript.Echo "*****Queue Status*****"
    GetQueueInfo arrServers(s)
    WScript.Echo "*****Storage Groups*****"
    GetStorageGroups arrServers(s)
    WScript.Echo "*****Public Folders*****"
    GetPublicFolderInfo arrServers(s), "", ""
Next
```

我们将脚本分解为从脚本主部分调用的子程序和函数。其中大多数函数都以Exchange服务器的名称作为参数。当您浏览脚本时，会看到我们使用了ADSI、WMI、CDOEXM和ADO。我们不会详细讲解这个脚本，因为本章前面已经涵盖了大部分内容。我们希望您能将脚本中的部分代码用作构建自己的Exchange管理脚本的积木。

### 总结

在本章中，我们向您展示了如何管理Exchange 2003服务器。没有单一的脚本技术，而是需要掌握一系列技术，具体取决于您想要管理的内容。您需要使用ADSI、ADO、CDOEXM和WMI来全面掌握您的Exchange环境。我们演示了如何管理服务器、存储组、邮箱存储和邮箱。Exchange 2003的脚本编写还有更多内容，足以单独写成一本书。我们鼓励您下载并使用Exchange 2003 SDK，这将使脚本开发变得更加容易。最后，我们强烈建议您如果还没有的话，建立一个测试环境。一个开发和测试不佳的脚本很容易导致Exchange服务器宕机或数据丢失。我们总是强调测试，但考虑到电子邮件的业务关键性，这一点更为重要。

> **附带光盘** 附带光盘中包含一个可用于监控Exchange 2003服务器的HTA。它使用了我们在本章中演示的大部分代码。您还可以找到一些对编写Exchange 2003脚本有帮助的网站链接。

# 第16章
Microsoft Operations Manager 2005 脚本编写

- **本章内容：**
    - 介绍MOM脚本编写。........................................................................ 464
    - 在MOM中使用脚本。........................................................................ 473
    - 自定义MOM脚本。........................................................................ 478
    - 查看MOM脚本实际应用。........................................................... 479
    - 总结。........................................................................ 482

Microsoft Operations Manager 2005 (MOM) 密切关注您的企业，并可以根据检测到的事件进行反应、修复或恢复。MOM工具箱包含一个庞大的脚本库。这些脚本在企业服务器上远程执行。在本章中，我们将探讨MOM如何使用脚本、这些脚本是如何构建的，以及您如何将自己的脚本添加到MOM中。

MOM 2005是一个企业级管理应用程序。MOM部署用于监控服务器健康状况和状态的管理代理。这些代理将信息报告回MOM，在MOM中信息被整合并报告给网络管理员。在本章中，我们假设您至少对该产品有基本的了解。

> **更多信息** 有关Microsoft Operations Manager 2005的更多信息以及下载评估版本，请访问Microsoft网站：http://www.microsoft.com/mom/default.mspx （此链接在附带光盘上；点击 *Microsoft Operations Manager Home*。）

MOM包含许多脚本，您随MOM安装的大多数管理包也包含脚本。安装几个关键管理包（例如Exchange 2003、Active Directory、Group Policy和Windows Operating System）后，您将拥有相当多的可用脚本，如第479页图16-1所示。其中许多脚本使用WMI。

# 第四部分：企业脚本编写

您可能会遇到一些希望在自己的环境中运行的脚本，或者希望将其作为MOM事件的一部分。现在还不应急于复制粘贴代码。MOM的脚本与传统脚本有些不同。我们将介绍这些差异，并向您展示如何将传统脚本转换为MOM脚本。

### 介绍MOM脚本编写

到目前为止，我们一直在处理的脚本与MOM脚本之间最大的区别之一是脚本的执行和处理方式。在传统脚本中，脚本在主机计算机上执行，即使脚本的目标是远程系统，也可以通过使用`wscript.echo`将结果返回到主机计算机。

在MOM环境中，所有脚本都由MOM代理在远程计算机上执行。绝对没有用户交互。脚本在后台静默运行。这意味着任何用于MOM的脚本都不能要求用户输入，例如通过输入框或消息框。MOM脚本也不能使用`wscript.echo`，因为没有管理员来接收消息。实际上，在使用MOM进行脚本编写时，我们根本不使用WScript环境。相反，MOM使用一个名为`ScriptContext`的新脚本宿主。在MOM中，脚本在MOM代理的上下文中运行，并向MOM服务器报告。这是一个相当简化的解释，但应该足以满足我们的目的。

> 注意：您不必实例化`ScriptContext`对象，因为它由MOM隐式创建。这与您从不实例化WScript非常相似，它就在那里。

这意味着像`wscript.echo`和`wscript.sleep`这样的命令在脚本由MOM执行时将不再起作用。有等效的方法可用，但我们使用`ScriptContext`对象来代替。表16-1和表16-2列出了`ScriptContext`的方法和属性。

表16-1 **ScriptContext 方法**

| 名称 | 描述 |
| :--- | :--- |
| CreateAlert | 生成一个新的Alert对象 |
| CreateDiscoveryData | 生成一个新的DiscoveryData对象 |
| CreateEvent | 生成一个新的Event对象 |
| CreatePerfData | 生成一个新的PerfData对象 |
| Echo | 将消息写入文本文件用于调试目的 |
| GetOverride | 获取当前规则的指定覆盖 |
| GetScriptState | 获取ScriptState对象 |
| IsAlert | 确定MOM提供给脚本的对象是否为Alert对象 |
| IsEvent | 确定MOM提供给脚本的对象是否为Event对象 |
| IsPerfData | 确定MOM提供给脚本的对象是否为PerfData对象 |
| Quit | 停止脚本运行并退出 |
| Sleep | 将脚本运行挂起指定的秒数 |
| Submit | 将Alert、Event、PerfData或DiscoveryData对象提交到MOM数据流 |

表16-2 **ScriptContext 属性**

| 名称 | 描述 |
| :--- | :--- |
| Alert | 获取导致MOM调用脚本的Alert对象 |
| Event | 获取导致MOM调用脚本的Event对象 |
| IsTargetAgentless | 检查计算机是否在没有MOM代理的情况下被监控 |
| IsTargetVirtualServer | 获取一个布尔值，指示计算机是否作为Windows Server群集服务器运行 |
| ManagementGroupName | 获取部署当前响应的管理组的名称 |
| Name | 获取当前脚本的名称 |
| ProcessingRule | 返回调用当前响应脚本的处理规则 |
| Parameters | 获取一个VarSet对象，其中包含在脚本被调用时从MOM发送的参数 |
| PerfData | 获取导致MOM调用脚本的PerfData对象 |
| TargetComputer | 获取被监控的计算机的名称 |
| TargetComputerIdentity | 获取当前脚本响应的目标计算机的身份 |



表 16-2 *ScriptContext* 属性

| 名称 | 描述 |
| :--- | :--- |
| *TargetNetbios-Computer* | 获取目标计算机的 NetBIOS 名称 |
| *TargetNetbios-Domain* | 获取目标计算机的 NetBIOS 域名 |
| *TargetFQDN-Computer* | 获取目标计算机的完全限定域名 |

你可能会认出其中一些方法。有些方法的行为与在 WScript 中完全一致，但有些则略有不同。

请记住，MOM 的目的是集中管理，并且脚本是在无人监控的情况下运行的。我们仍然可以从脚本中输出信息，但这些信息不会出现在命令窗口或消息框中。当我们调用 *ScriptContext.Echo* 时，它会将消息发送到 MOM 服务器。如果脚本是作为响应脚本的一部分被调用，该消息将被写入 MOM 日志文件。如果脚本是 MOM 任务的一部分，该消息将被写入任务事件窗口。我们将在本章稍后介绍响应脚本和任务脚本。

### 添加脚本

因为 MOM 将所有内容都存储在 SQL 数据库中，所以你不能简单地将脚本文件复制到 MOM 服务器。你需要在数据库中为其创建一个条目，然后插入脚本的内容。遗憾的是，插入代码并没有一种优雅的方法。请按照以下步骤操作。

1.  在 MOM 服务器上打开 MOM 管理员控制台。
2.  在 Microsoft 记事本中打开你的脚本。选中并复制脚本。
3.  导航到 Scripts 文件夹。
4.  右键单击 Scripts 文件夹，然后单击“创建脚本”。
5.  输入脚本名称和描述。如果你的脚本不是用 VBScript 编写的，请选择相应的语言。单击“下一步”。
6.  按 Ctrl+V 将复制的脚本粘贴到窗口中。单击“下一步”。
7.  要定义运行时参数，请单击“添加”，然后输入名称、描述和默认值。单击“完成”，你的脚本将被添加到列表中。现在，它可用于你想要创建的任何 MOM 任务、事件或响应。
8.  要编辑脚本，请在右窗格中右键单击它，然后单击“属性”。单击“脚本”选项卡。选中文本，将其复制并粘贴到记事本或你的脚本编辑器中。

### 定义脚本参数

在传统的 VBScript 中，我们使用 *wscript.arguments* 属性来获取运行时参数。但是，在 MOM 下运行脚本时，*wscript* 对象不可用。相反，我们使用 *ScriptContext.Parameters* 属性。当你在 MOM 中创建脚本时，你需要定义所需的运行时参数，如图 16-2 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_486_0.png)

**图 16-2** MOM 脚本参数

在脚本内部，你通常使用 *ScriptContext.Parameters.Get* 将参数值设置给一个内部变量。

```
strDomainFilter = Trim(ScriptContext.Parameters.Get("Domains"))

On Error Resume Next
Dim strSeparator
If CBool(Trim(ScriptContext.Parameters.Get("CSV"))) Then
  strSeparator = ","
Else
  strSeparator = vbTab
End If
```

> **最佳实践** 与任何脚本一样，你应该检查必需参数是否存在并验证它们。如果有什么不正确，使用 *ScriptContext.Echo* 将信息写入事件选项卡并优雅地终止脚本。这样，当你在 MOM 操作员控制台中检查任务状态时，就能了解哪里出了问题。

### 使用运行时脚本对象

*ScriptContext* 对象只是 MOM 运行时脚本对象的一种类型。然而，正如你从表 16-1 中看到的那样，它用于创建几个你可能会觉得有用的其他对象。

#### 使用 *PerfData* 对象

就像你可以使用性能监视器管理控制台或在 MOM 中监视计数器一样，你也可以创建一个 *PerfData* 对象来处理性能计数器，并将信息返回给 MOM 服务器。这意味着你可以根据任何你计算为数字的内容创建自定义性能计数器，例如文件的大小或任何给定时间运行的进程数。

要创建性能数据，你需要一个 *PerfData* 对象、一个自定义计数器的名称、一个实例名称以及你想要记录的值。获得此信息后，你使用 *ScriptContext.Submit* 将信息发送到 MOM 服务器。清单 16-1 中的脚本创建了一个名为 *ProcessCount* 的新自定义性能计数器，该计数器返回托管服务器上运行的进程数。将脚本添加到 MOM 后，你可以创建一个任务或定时事件，以便在托管计算机上运行该脚本。

```
清单 16-1 创建计数器
On Error Resume Next
Dim strComputer
Dim objWMIService
Dim propValue
Dim objItem
Dim SWBemlocator
Dim colItems

strComputer = "."
iCount=0
Set SWBemlocator = CreateObject("wbemScripting.SWbemLocator")
Set objWMIService = SWBemlocator.ConnectServer(strComputer,"\\root\\CIMV2")
Set colItems = objWMIService.ExecQuery("Select caption from win32_Process" _
    ,,48)
For Each objItem in colItems
    iCount=iCount+1
    ScriptContext.Echo "Caption: " & objItem.Caption
Next

ScriptContext.echo iCount & " Processes counted."

CreatePerfData "Processes","Process Count","ProcessInfo",iCount

Sub CreatePerfData(strObjectName,strCounterName,strInstanceName,numValue)
    Set objPerfData = ScriptContext.CreatePerfData
    objPerfData.ObjectName = strObjectName
    objPerfData.CounterName =strCounterName
    objPerfData.InstanceName = strInstanceName
    objPerfData.Value = numValue
    ScriptContext.Submit objPerfData
End Sub
```

**随书附赠** 你可以在本书附带的光盘上找到此脚本以及本章中列出的其他脚本。

脚本的第一部分是基本的 WMI 代码，用于计算本地计算机上运行的进程数。

```
Set SWbemlocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = SWbemlocator.ConnectServer("\\root\\CIMV2")
Set colItems = objWMIService.ExecQuery("Select caption from Win32_Process",,48)
For Each objItem in colItems
    iCount=iCount+1
    ScriptContext.Echo "Caption: " & objItem.Caption
Next
```

*ScriptContext.Echo* 命令将输出发送到事件任务的“属性”选项卡，如图 16-3 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_488_0.png)

**图 16-3** 事件任务属性

我们正在创建的计数器是当前运行的进程数，存储在 *iCounter* 变量中。我们调用 *CreatePerfData* 子程序，该子程序创建 *PerfData* 对象并将其提交给 MOM 服务器。该子程序需要知道性能对象的名称、计数器名称、实例名称和实例的值。

```
CreatePerfData "Processes","Process Count","ProcessInfo",iCount
```

在子程序内部，我们使用 *ScriptContext.CreatePerfData* 来创建 *PerfData* 对象。然后子程序设置一些对象属性并将其提交给 MOM。

470  第四部分： 企业脚本

```
Sub CreatePerfData(strObjectName,strCounterName,strInstanceName,numValue)
    Set objPerfData = ScriptContext.CreatePerfData
    objPerfData.ObjectName = strObjectName
    objPerfData.CounterName =strCounterName
    objPerfData.InstanceName = strInstanceName
    objPerfData.Value = numValue
    ScriptContext.Submit objPerfData
End Sub
```

根据你执行脚本的频率，你可以在 MOM 中生成一个漂亮的性能图，如图 16-4 所示。

![](img/4fefd6988ba5d4a92a65127617ca24c2_489_0.png)

图 16-4   自定义性能图

#### 使用 *Alert* 对象

*Alert* 对象可以通过 *ScriptContext.CreateAlert* 方法或 *ScriptContext.Alert* 属性来创建或操作。就像我们使用 *PerfData* 对象一样，我们可以根据任何我们想要的脚本条件创建自定义警报。有许多警报属性可以指定，但通常你至少会希望指定以下内容：

- *Name* 此属性是你用于定义警报的名称。
- *Level* 此属性是警报严重性。以下值用于指示警报的严重性级别。
  - 10. 此值表示成功。
  - 20. 此值表示信息。
  - 30. 此值表示警告。
  - 40. 此值表示错误。
  - 50. 此值表示严重错误。



清单 16-2 中的这个简短脚本演示了如何在 MOM 中创建新的警报。

```
清单 16-2 创建警报
'创建警报对象
Set objCreatedAlert = ScriptContext.CreateAlert()
'设置警报属性
objCreatedAlert.Name = "Test Alert"
objCreatedAlert.AlertLevel = 20
objCreatedAlert.Owner = "[unassigned]"
objCreatedAlert.ResolutionState = 0
objCreatedAlert.Description="This is a test demonstration alert."
'将警报对象提交到 MOM
ScriptContext.Submit objCreatedAlert
```

图 16-5 显示了在 MOM 操作员控制台中的最终警报。

![MOM 测试警报属性](img/4fefd6988ba5d4a92a65127617ca24c2_490_0.png)

#### 使用 *Event* 对象

*Event* 对象在 MOM 中通常用于指代任何与事件相关的元素，例如应用程序日志或 NT 事件日志。但是，就像 *PerfData* 和 *Alert* 对象一样，我们可以通过脚本创建自己的事件，或者处理 MOM 没有提供程序的事件。与之前的对象一样，我们使用 *ScriptContext* 来创建对象并定义其属性，然后使用 *ScriptContext.Submit* 将对象提交到 MOM 服务器。至少，你应该设置下一页所示的属性。

- *EventNumber* 这通常是 Windows 事件 ID 号，但在创建自己的事件时，你可以使用任何想要的编号。
- *EventSource* 这是事件的来源。它通常是应用程序，但你可能希望将其设置为生成事件的脚本的名称。
- *EventType* 这是表示事件类型的值，例如 *Success*、*Failure* 或 *Information*。清单 16-3 中的脚本将这些值定义为常量。
- *Message* 这是你希望作为事件一部分显示的文本。

```
清单 16-3 创建事件
Const EVENT_TYPE_SUCCESS = 0
Const EVENT_TYPE_ERROR   = 1
Const EVENT_TYPE_WARNING = 2
Const EVENT_TYPE_INFORMATION = 4
Const EVENT_TYPE_AUDITSUCCESS = 8
Const EVENT_TYPE_AUDITFAILURE = 16
'创建事件对象
Set objEvent = ScriptContext.CreateEvent()
'定义事件属性
objEvent.EventSource = "Demo Event Script"
objEvent.EventNumber = 9999
objEvent.EventType = EVENT_TYPE_INFORMATION
objEvent.Message="Your sample event has been raised."
'将事件对象提交到 MOM
ScriptContext.Submit objEvent
```

图 16-6 中的图表说明了最终的事件。

![MOM 中的事件](img/4fefd6988ba5d4a92a65127617ca24c2_491_0.png)

### 理解脚本跟踪和调试

使用 MOM 调试脚本比传统的 VBScript 调试要复杂得多，因为你无法“看到”脚本在做什么。如果需要真正的调试，你需要使用 Microsoft Visual Studio .NET 并远程连接调试器。（使用 Microsoft .NET 进行调试超出了本书的范围。）但是，你可以在受管理服务器上启用跟踪。启用跟踪后，任何 *ScriptContext.Echo* 命令都将写入跟踪日志文件。以下是来自 MOM SDK 文档的步骤。

1. 运行 Windows 注册表编辑器 (Regedit.exe)。
2. 浏览到 HKEY_LOCAL_MACHINE\SOFTWARE\Mission Critical Software\OnePoint 注册表项。
3. 如果 *EnableActiveDebugging* 尚不存在，请为其创建一个新的 DWORD 条目。将 *EnableActiveDebugging* 条目的值设置为 1。
4. 跟踪将在下次 MOM 服务启动时开始。你可以立即重启服务，或者等到下次计划重启。

该文件将在 %TEMP%\Microsoft Operation Manager 文件夹中创建，名称类似于 AgentResponses-MOMGroup.log，其中 *MOMGroup* 是你的管理组的名称。

要禁用跟踪，请将 *EnableActiveDebugging* 更改为 0。新设置将在下次 MOM 服务启动时生效。请务必在完成后关闭跟踪，因为跟踪会增加显著的开销并导致性能下降。

> **注意** 你需要安装 MOM SDK 才能启用跟踪。

### 在 MOM 中使用脚本

在 MOM 中定义脚本后，可以在 MOM 服务器本地或受管理服务器上使用。当脚本在受管理服务器上执行时，该服务器上运行的 MOM 代理执行该脚本。由于 MOM 代理服务帐户通常在本地系统下运行，脚本只能访问本地资源和信息。MOM 脚本通常分为以下四类：响应脚本、定时脚本、状态变量脚本和发现脚本。

#### 使用响应脚本

这种类型的脚本作为对某些事件规则、性能计数器值或警报的响应而执行。例如，你可能有一个规则或定时事件来检查事件日志的大小，然后定义一个脚本将日志备份到文件并清除日志。你可以有多个脚本作为响应的一部分。如果有多个，脚本将同步运行。脚本也必须在 MOM 处理其余事件或警报之前完成。

##### 使用定时脚本

定时脚本是一种特殊类型的响应脚本。你可以在 MOM 中创建自己的定时事件，并指定一个脚本在定时事件间隔运行。在刚刚提到的例子中，响应脚本仅负责备份和清除事件日志。你同样可以创建一个脚本作为定时事件的一部分运行，该脚本检查大小，将大小报告回 MOM，如果大小超过某个阈值，则备份并清除日志。这将是使用参数的理想脚本，例如事件日志类型、大小阈值和备份目录。

##### 使用状态变量脚本

存储状态变量的脚本可以帮助你关联多个受管理服务器之间的事件。只要管理服务器上的 MOM 服务正在运行，状态变量对所有脚本都是全局可用的。如果服务停止或重启，变量将重置。例如，你可能针对 Exchange 2003 服务器运行脚本作为定时事件的一部分，该脚本检查有消息等待传递的队列数量。如果在 15 分钟内增加到某个水平，可能表示 DNS、网络连接或传播的病毒出现问题。15 分钟后，脚本可以重置并再次开始监控。

*ScriptState* 对象用于在脚本会话之间存储变量信息。将 *ScriptState* 视为一种全局缓存，用于存储你需要在多个脚本之间访问的信息。在 *ScriptState* 中，为你想要存储的每个数据创建一个 *varSet* 对象。

此代码片段创建一个名为 *Queue Tracker* 的新 *varSet* 对象。在该对象内部，有一个名为 *Number of Queues with messages* 的 *varSet* 变量，它将具有一些你指定的值，也许是返回有消息的 Exchange 队列数量的函数的结果。

```
Const VARSET_NAME = "Queue Tracker"
Const QUEUE_COUNT = "Number of Queues with messages"
iCount=GetQCount '某个返回有消息的队列数量的函数。
'创建 ScriptState 对象
Set objScriptState = ScriptContext.GetScriptState()
'创建 VarSet 对象
Set objVarSet = objScriptState.CreateSet()

'将变量更改保存回 VarSet
obVarSet.put QUEUE_COUNT, iCount

'通过传递 varSet 对象的名称和脚本中创建的 varSet 对象来保存 VarSet。
'你必须这样做才能将更改提交到 ScriptState。
objScriptState.SaveSet VARSET_NAME, objvarSet
```

> **提示** 作为 *CreateSet* 的替代方法，你可以使用 *GetSet(varSetName)*。如果指定的 *varSet* 对象存在，它将被返回；否则将创建一个具有指定名称的新对象。

要读取 *varSet* 对象，我们需要获取 *ScriptState* 对象，然后使用其 *GetSet* 方法检索指定的 *varSet*。获取此对象后，我们可以获取存储在对象内部的变量。

```
Const VARSET_NAME = "Queue Tracker"
Const QUEUE_COUNT = "Number of Queues with messages"
'创建 ScriptState 对象
Set objScriptState = ScriptContext.GetScriptState()
'获取 VarSet 对象
Set objVarSet = objScriptState.GetSet(VARSET_NAME)
'检索 Number of Queues with messages 变量的值
'并将 iStoredCount 设置为此值。
iStoredCount=objVarSet.Get(QUEUE_COUNT)
```

这是一个更完整的示例，将任务的两个部分放在单个脚本中。

```
Const VARSET_NAME = "Queue Tracker"
Const QUEUE_COUNT = "Number of Queues with messages"

'创建 ScriptState 对象
Set objScriptState = ScriptContext.GetScriptState()
'创建 VarSet 对象
Set objVarSet = objScriptState.GetSet(VARSET_NAME)

iCount=GetQCount '某个返回有消息的队列数量的函数。

'获取存储的值。假设此脚本每 15 分钟运行一次
'这里的任何值都是 15 分钟前的队列计数。
iStoredCount=objVarSet.Get(QUEUE_COUNT)

'将存储的计数与当前计数进行比较
If iCount>iStoredCount Then
  '计数已增加
  '执行一些代码来通知管理员，写入事件
  '或创建警报。
End If

'将变量更改保存回 VarSet
obVarSet.put QUEUE_COUNT, iCount

'通过传递 varSet 对象的名称和脚本中创建的 varSet 对象来保存 VarSet。
'你必须这样做才能将更改提交到 ScriptState。
objScriptState.SaveSet VARSET_NAME, objVarSet
```



# 第四部分：企业级脚本编写

如果你正在尝试调试 *ScriptState* 代码，可以使用 *varSet* 对象的 *DumpToFile* 方法，将指定的 *varSet* 对象内容写入文本文件。

```vbscript
Const VARSET_NAME = "Queue Tracker"
dtmNow = Now()
'specify the filename
strFileName = Month(dtmNow) & "_" & Day(dtmNow) & "_" & _
              Hour(dtmNow) & "_" & Minute(dtmNow) & "_" & _
              Second(dtmNow) & ".dat"
'Get the ScriptState
Set objScriptState = ScriptContext.GetScriptState()
'Get the varSet object
Set objVarSet = objScriptState.GetSet(VARSET_NAME)
objVarSet.DumpToFile strFileName
```

你可以创建类似这样的脚本，并将其作为任务在 MOM 服务器上运行，从而为你的 Exchange 2003 服务器提供额外的监控功能。

> **注意：** 如果未指定文件名和路径，文件将在 Microsoft Operations Manager 2005 文件夹中创建。

#### 使用发现脚本

发现脚本在 MOM 服务器或受管计算机上执行。这些脚本根据 MOM 服务器上定义的计算机属性来发现信息。这些属性（如操作系统详细信息、硬件、服务或应用程序）有助于对受管计算机进行分组，以便应用适当的管理规则。*ScriptContext* 对象通过调用 *CreateDiscoveryData* 方法创建一个 *DiscoveryData* 对象。

```vbscript
Set objDiscData=ScriptContext.CreateDiscoveryData()
```

你不能直接向 *DiscoveryData* 对象添加信息。相反，该对象包含你需要填充的集合。完成后，必须调用 *ScriptContext.Submit* 将更改保存到 MOM 服务器。查看清单 16-4 中的脚本，该脚本来自 IIS 管理包。当此脚本针对受管计算机运行时，它会被“发现”为 IIS 服务器，并添加到 MOM 中的 IIS 服务器组中。

##### 清单 16-4：发现 IIS 角色

```vbscript
'------------------------------------------------------
' <company>Microsoft Corporation</company>
' <copyright>Copyright (c) Microsoft Corporation. All rights reserved.
' </copyright>
' <name> IIS Role Discovery '</name>
' <summary>
' Creates an IIS server role for this computer
' </summary>
'-------------------------------------------------------

Option Explicit

Const COMPUTER_CLASS_ID = "Computer"

Const COMPUTER_COMPUTER_NAME_ATTRIBUTE_ID = "ComputerName"
Const COMPUTER_TIME_ZONE_BIAS_ATTRIBUTE_ID = "Time Zone Bias"
Const COMPUTER_OPERATING_SYSTEM_VERSION_ATTRIBUTE_ID = _
    "Operating System Version"
Const COMPUTER_IP_ADDRESS_ATTRIBUTE_ID = "IPAddress"
Const COMPUTER_FQDN_ATTRIBUTE_ID = "FQDN"
Const COMPUTER_VIRTUAL_SERVER_TYPE_ATTRIBUTE_ID = "Virtual Server Type"

Sub Main()
    Dim oDiscData
    Dim oCollection
    Dim oInstance

    Set oDiscData = ScriptContext.CreateDiscoveryData()
    Set oCollection = oDiscData.CreateCollection()
    oCollection.AddScopeFilter COMPUTER_COMPUTER_NAME_ATTRIBUTE_ID, _
        ScriptContext.TargetComputerIdentity
    oCollection.ClassID = "IIS"

    Set oInstance = oCollection.CreateInstance()
    oInstance.AddKeyProperty "Server Name", _
        ScriptContext.TargetNetbiosComputer
    oCollection.AddInstance oInstance
    oDiscData.AddCollection oCollection

    ScriptContext.Submit oDiscData
End Sub
```

发现脚本需要一个 *DiscoveryData* 对象，之后我们可以实例化一个 *DiscoveryCollection* 对象，该对象将用于保存信息。

```vbscript
Set oDiscData = ScriptContext.CreateDiscoveryData()
Set oCollection = oDiscData.CreateCollection()
```

拥有集合对象后，我们需要添加一个作用域过滤器。

```vbscript
oCollection.AddScopeFilter COMPUTER_COMPUTER_NAME_ATTRIBUTE_ID, _
    ScriptContext.TargetComputerIdentity
```

我们为发现的数据设置类 ID，在此例中是 *IIS*。

```vbscript
oCollection.ClassID = "IIS"
```

要向集合添加更多信息，我们创建一个新实例并定义一个属性。

```vbscript
Set oInstance = oCollection.CreateInstance()
oInstance.AddKeyProperty "Server Name", _
  ScriptContext.TargetNetbiosComputer
```

然后我们需要将实例添加到集合中。

```vbscript
oCollection.AddInstance oInstance
```

我们将集合添加到集合对象。

```vbscript
oDiscData.AddCollection oCollection
```

最后，我们将 *DiscoveryData* 对象提交给 MOM 服务器。

> **注意：** 关于发现脚本的 SDK 文档非常简略，坦率地说，帮助不大。如果你需要创建自定义发现脚本，我们建议你研究一些 MOM 附带的现成发现脚本，然后修改其中一个以满足你的需求。

### 自定义 MOM 脚本

根据你安装的管理包，你的 MOM 服务器可能有很多脚本，其中一些你可能希望修改以更好地适应你的目的。理想情况下，MOM 脚本会使用参数使其更灵活，但情况并非总是如此。如果你想修改现有的 MOM 脚本，最好的做法是手动操作。查看脚本的属性，然后点击脚本源代码选项卡。复制脚本文本，并将其粘贴到记事本中以创建新的脚本文件。根据需要编辑脚本文件，完成后，只需按照本章前面“添加脚本”部分概述的步骤创建一个新脚本。然后你可以根据需要使用该脚本。

你可能还会发现一个你想在 MOM 环境之外作为单独脚本运行的 MOM 脚本。然而，你不能简单地将代码粘贴到新脚本中并运行它。首先，你必须移除任何与 *ScriptState*、*DiscoveryData*、*Alerts* 或 *Events* 相关的代码，因为这些对象在 VBScript 中不存在。修改 MOM 脚本时，你需要将 *ScriptContext* 替换为 *wscript*。任何 *ScriptContext.Echo* 语句都应替换为 *wscript.echo*。你必须确定如何处理其他所有与 *ScriptContext* 相关的内容。如果脚本使用参数，你需要将其修改为使用 *wscript.arguments*，或者将独立版本创建为 Windows 脚本文件（.wsf）并使用命名参数。

你可能会发现最有用的是可移植的 WMI 函数和子程序。但是，请记住，MOM 脚本是由 MOM 服务帐户在受管服务器上本地运行的。你需要修改 WMI 代码以访问远程计算机，并根据需要传递凭据。要将 MOM 脚本转换为独立脚本，请按照以下步骤操作。

1.  移除所有 MOM 特定对象的引用，例如 *ScriptState*。
2.  将 *ScriptContext.Echo* 转换为 *wscript.echo*。
3.  移除所有其他对 *ScriptContext* 的引用。
4.  将参数转换为 *wscript.arguments*，或在 .wsf 脚本中使用命名参数。
5.  转换 WMI 代码以访问远程计算机，必要时传递替代凭据。

### 查看 MOM 脚本实战

让我们将本章中涵盖的一些内容应用到一个新的 MOM 脚本中。在创建自己的 MOM 脚本时，我们建议首先使用传统脚本开发和测试核心功能。一旦你知道 VBScript 代码正确，你就可以开始修改脚本以在 MOM 环境中使用，并根据需要添加 MOM 特定功能。

#### 清单 16-5：检查文件夹大小

```vbscript
strFolder="e:\temp"
iThreshold=100000
iSize=GetFolderSize(strFolder)

If Int(iSize) > Int(iThreshold) Then
    'folder size exceeds threshold so generate an alert
    wscript.Echo "Alert!"
    strDescription=strFolder & " has exceeded the specified threshold of " & _
        FormatNumber(iThreshold,0,,True) & " bytes. Folder size is " & _
        FormatNumber(iSize,0,,True) & " bytes"
    wscript.echo strDescription
Else
    'folder size is OK
    wScript.Echo "The size of " &strFolder & " (" & iSize & _
        ") is within the threshold of " & iThreshold
End If

Function GetFolderSize(strFolder)
    dim objFSO,objFldr
    set objFSO=CreateObject("Scripting.FileSystemObject")
    set objFldr=objFSO.GetFolder(strFolder)
    GetFolderSize=objFldr.Size
End Function
```

按原样编写，此脚本在 MOM 环境中无法工作，因为它利用了 *wscript* 对象。我们希望利用一些 MOM 的优势，例如使用参数、创建警报和捕获性能数据。后者特别有用，因为文件夹大小的性能图表可能有助于容量规划。下一页清单 16-6 中的脚本与清单 16-5 的脚本基本相同，只是添加了 MOM 相关对象。



## 清单 16-6 监控文件夹大小

```
strFolder=ScriptContext.Parameters.Get("folder")
iThreshold=ScriptContext.Parameters.Get("threshold")
iSize=GetFolderSize(strFolder)

If Int(iSize)>Int(iThreshold) Then
    '文件夹大小超过阈值，生成警报
    ScriptContext.Echo "Alert!"
    strDescription=strFolder & " has exceeded the specified threshold of " & _
        FormatNumber(iThreshold,0,True) & " bytes.  Folder size is " & _
        FormatNumber(iSize,0,True) & " bytes"
    ScriptContext.echo strDescription
    CreateAlert "Folder Size Exceeded",20,"[unassigned]",0,strDescription
Else
    '文件夹大小正常
    '将数据写入MOM事件
    ScriptContext.Echo strFolder & " is OK. Size=" & _
        FormatNumber(iSize,0,True) & " bytes"
End If

'创建性能数据
CreatePerfData "Monitored Folder","FolderSize",strFolder,_
    FormatNumber((iSize/1024000),2)

Function GetFolderSize(strFolder)
    dim objFSO,objFldr
    set objFSO=CreateObject("Scripting.FileSystemObject")
    set objFldr=objFSO.GetFolder(strFolder)
    GetFolderSize=objFldr.Size
End Function

Sub CreateAlert(strObjectName,iAlertLevel,strOwner,iResolutionState,_
    strDescription)
    '创建警报对象
    Set objCreatedAlert = ScriptContext.CreateAlert()
    '设置警报属性
    objCreatedAlert.Name = strObjectName
    objCreatedAlert.AlertLevel = iAlertLevel
    objCreatedAlert.Owner = strOwner
    objCreatedAlert.ResolutionState = iResolutionState
    objCreatedAlert.Description=strDescription
    '将警报对象提交给MOM
    ScriptContext.Submit objCreatedAlert
End Sub

Sub CreatePerfData(strObjectName,strCounterName,strInstanceName,numvalue)
    '创建性能数据对象
    Set objPerfData = ScriptContext.CreatePerfData
    '设置性能数据属性
    objPerfData.ObjectName = strObjectName
    objPerfData.CounterName =strCounterName
    objPerfData.InstanceName = strInstanceName
    objPerfData.Value = numValue
    '将性能数据对象提交给MOM
    ScriptContext.Submit objPerfData
End Sub
```

让我们更详细地看看这个脚本。

当我们在MOM中创建一个新脚本并粘贴这段代码时，我们有机会定义参数。通过使用参数，我们可以将此脚本重用于各种计划任务，这些任务可以针对不同的托管服务器使用不同的参数运行。前两行根据启动脚本的任务参数定义了脚本变量。

```
strFolder=ScriptContext.Parameters.Get("folder")
iThreshold=ScriptContext.Parameters.Get("threshold")
```

接下来，我们通过调用 *GetFolderSize* 函数定义一个变量来存储文件夹的当前大小。

```
iSize=GetFolderSize(strFolder)
```

我们已经在VBS脚本中测试过这个函数，所以应该不会有任何问题。如果文件夹大小大于阈值，我们希望记录该信息并生成警报。

```
If Int(iSize)>Int(iThreshold) Then
'文件夹大小超过阈值，生成警报
ScriptContext.Echo "Alert!"
strDescription=strFolder & " has exceeded the specified threshold of " & _
  FormatNumber(iThreshold,0,True) & " bytes.  Folder size is " & _
  FormatNumber(iSize,0,True) & " bytes"
ScriptContext.echo strDescription
CreateAlert "Folder Size Exceeded",20,"[unassigned]",0,strDescription
```

*ScriptContext.Echo* 命令会将信息写入任务完成时创建的事件中。如果有人在监控事件，这可能就足够了。创建一个警报对象以便问题可以得到处理和解决也是很好的。我们通过调用 *CreateAlert* 子程序来创建 *Alert* 对象来实现这一点。

```
Sub CreateAlert(strObjectName,iAlertLevel,strOwner,_
              iResolutionState,strDescription)
  '创建警报对象
  Set objCreatedAlert = ScriptContext.CreateAlert()
  '设置警报属性
  objCreatedAlert.Name = strObjectName
  objCreatedAlert.AlertLevel = iAlertLevel
  objCreatedAlert.Owner = strOwner
  objCreatedAlert.ResolutionState = iResolutionState
  objCreatedAlert.Description=strDescription
  '将警报对象提交给MOM
  ScriptContext.Submit objCreatedAlert
End Sub
```

Else
'文件夹大小正常
'将数据写入MOM事件
ScriptContext.Echo strFolder & " is OK. Size=" & FormatNumber(iSize,0,True) & " bytes"
End If

我们要做的最后一件事是将大小信息作为性能对象捕获。我们调用 *CreatePerfData* 子程序。

```
'创建性能数据
CreatePerfData "Monitored Folder","FolderSize",strFolder,_
FormatNumber((iSize/1024000),2)
```

该子程序创建一个名为 *Folder Size* 的新性能对象。这将作为托管服务器在MOM操作控制台中的性能计数器出现。实例是被监控文件夹的名称，值是以兆字节为单位的当前大小。*GetFolderSize* 函数返回一个以字节为单位的值，我们只是简单地将其格式化为兆字节。

```
Sub CreatePerfData(strObjectName,strCounterName,strInstanceName,numValue)
  '创建性能数据对象
  Set objPerfData = ScriptContext.CreatePerfData
  '设置性能数据属性
  objPerfData.ObjectName = strObjectName
  objPerfData.CounterName =strCounterName
  objPerfData.InstanceName = strInstanceName
  objPerfData.Value = numValue
  '将性能数据对象提交给MOM
  ScriptContext.Submit objPerfData
End Sub
```

就像 *CreateAlert* 子程序一样，我们只需要创建 *PerfData* 对象，设置一些属性，然后将对象提交给MOM服务器。

正如我们所展示的，你可以轻松地获取现有的管理脚本并将其扩展以在MOM环境中运行，通常还能增强功能。

### 总结

在本章中，我们讨论了如何在 Microsoft Operations Manager 2005 环境中处理脚本。我们解释了 *ScriptContext* 对象在MOM服务器上取代 *wscript* 成为脚本宿主，并概述了脚本在托管服务器上的执行方式。我们了解了MOM中不同类型的脚本对象，例如 *Alerts*、*Performance Data* 和 *Events*。你还学习了使用脚本的各种方式，包括作为响应和计划任务。最后，我们演示了如何扩展现有脚本以在MOM环境中运行。在MOM中进行脚本编写比传统脚本编写稍微复杂一些，但它提供了一些巨大的好处和价值。

**更多信息** 有关更多信息，请访问 Technet 脚本中心，或查看附送 CD 上本章的 Web 链接。

# 第 17 章
## Virtual Server 2005 脚本编写

- **本章内容：**
  - 介绍 Virtual Server 脚本编写.................484
  - 理解 Virtual Server 对象模型........486
  - 编写配置脚本.........................488
  - 编写管理脚本...........................490
  - 查看 Virtual Server 脚本编写实际操作............498
  - 总结............................................501

Microsoft Virtual Server 2005 是微软有史以来脚本可访问性最强的产品之一。其设计通过组件对象模型（COM）对象公开了大部分功能，Virtual Server 的可脚本性使其非常易于管理。我们将介绍 Virtual Server 对象模型的基础知识，并向您展示一些示例，说明脚本如何使 Virtual Server 更易于使用和更高效。

当微软从原始创建者 Connectix（http://www.connectix.com）购买 Virtual Server 时，大多数行业观察家认为微软会快速发布这个几乎完成的产品。相反，微软让所有人感到惊讶，它花了相当长的时间来提高 Virtual Server 的稳定性和性能，并通过添加基于组件对象模型（COM）的综合应用程序编程接口（API）使其更易于管理。该 API 确保其他 COM 兼容语言（包括 VBScript）可以自动化与虚拟磁盘驱动器、虚拟机、虚拟网络、Virtual Server 安全性等相关的管理任务。Virtual Server 附带了一份程序员指南，解释了完整的 API，因此在本章中，我们将重点介绍 Windows 管理员认为最有用的核心功能。

> **注意** 我们在本章中演示的技术仅适用于 Virtual Server；它们与 Virtual Server 的姊妹产品 Virtual PC 不兼容。Virtual PC 旨在在客户端计算机上运行，并且一次只运行几个虚拟机；Virtual Server 是一个企业级应用程序，旨在持续运行更多数量的虚拟机，这些虚拟机充当您网络上实际生产服务器的角色。



### 介绍虚拟服务器脚本

Virtual Server 设计用于运行一个或多个虚拟机。虚拟机是物理计算机的一种表示。运行 Virtual Server 的基础服务器通常称为主机，在主机上运行的 Microsoft Windows 被称为主机操作系统，或主机 OS。主机硬件通常是高端多处理器服务器，而主机操作系统通常是 Microsoft Windows Server 2003 的某个版本。每个虚拟机运行自己独立的操作系统，称为客户操作系统。在 Virtual Server 下运行的虚拟机可以运行几乎任何版本的 Windows——包括 Microsoft Windows NT——或任何其他与 32 位 Intel 处理器兼容的操作系统，包括各种 Linux 版本、不同品牌的 Unix 等。每个虚拟机有一个或多个虚拟磁盘，它们本质上是主机计算机上的文件，对虚拟机而言表现为存储设备。例如，一个运行 Microsoft Windows 2000 Server 的虚拟机可能有两个硬盘，C 和 D，它们作为两个独立文件存在于主机计算机上。同样，虚拟网络允许虚拟机相互通信。

> **更多信息** 关于 Virtual Server 概念和功能的全面讨论超出了本书范围。但是，您可以通过 Virtual Server 网站了解更多：
> http://www.microsoft.com/virtualserver
> 另一个良好的信息来源是 John Howard 的博客：
> http://blogs.technet.com/howard/

Virtual Server API 暴露了五个主要功能类别，每个类别与 Virtual Server 的一个特定功能组件相关。

- Virtual Server 客户端功能，例如单击鼠标按钮或按键，允许您在客户操作系统内自动化任务。Virtual Server 不直接在虚拟机内提供自动化（意味着您无法自动化虚拟机客户操作系统内部发生的事情，尽管您可以编写在虚拟机内运行的脚本），但它确实提供了向虚拟机发送按键、鼠标单击等的能力——本质上允许您自动化现场用户会执行的手动任务。
- 虚拟磁盘驱动器，包括可移动介质设备（如 DVD 驱动器），以及虚拟固定存储（如虚拟硬盘）。API 还提供对虚拟 SCSI 控制器和驱动器的控制。
- 虚拟机设置，包括虚拟机硬件的详细信息（如端口）、保存状态等。
- 虚拟网络配置，包括虚拟网络适配器、连接虚拟机的虚拟网络、内置的虚拟 DHCP 服务器等。
- Virtual Server 访问权限和安全性，包括搜索和列出访问权限的能力。

Microsoft TechNet Script Center 有许多设计用于管理 Virtual Server 各个方面的脚本。您可以在以下网址访问完整集合：
http://www.microsoft.com/technet/scriptcenter/scripts/vs/default.mspx

> **在 CD 上** 此链接包含在附带的 CD 上。单击 *Script Repository-Virtual Server*。

事实上，我们使用其中一些脚本作为示例的基础。我们还将向您展示如何将这些示例扩展为执行更全面管理任务的脚本。

#### 虚拟硬件

如果您计划编写在虚拟机内运行的脚本，您的脚本需要与虚拟机内运行的客户操作系统兼容。但是，您可能有兴趣了解客户操作系统将在什么硬件上运行，因为这些信息也会影响您编写脚本的方式。

每个虚拟机模拟 Intel 440BX 芯片组和 AMI BIOS。虚拟机内的处理器被暴露为主机计算机的处理器，意味着处理器不是以任何方式模拟的——它只是传递给虚拟机。在图形方面，每个虚拟机模拟一个具有 4MB 视频内存的 S3 Trio 32/64。虚拟机还模拟一个标准的 104 键、Windows 兼容的键盘，带有 PS/2 接口。（如果您使用物理 USB 键盘，虚拟机仍然将其视为 PS/2 键盘；Virtual Server 2005 不支持虚拟机内的 USB 设备。）同样，每个虚拟机内的鼠标被视为 PS/2 鼠标。不支持声音或游戏控制器。

每个虚拟机最多可以有两个串行端口和一个并行端口；同样，不支持 USB 设备。最多可以附加两个 1.44 MB 软盘驱动器。对于硬盘驱动器，最多可以附加四个 IDE 设备，包括 CD-ROM 或 DVD 驱动器。最多可以模拟四个 SCSI 主机控制器；Virtual Server 模拟 Adaptec 7870 SCSI 控制器芯片组。每个控制器最多可以托管七个虚拟 SCSI 硬盘。虚拟 IDE CD-ROM 和 DVD-ROM 的大小限制为 128 GB，尽管要存储最大数量，您显然需要在主机计算机上具有足够的物理存储。SCSI 磁盘映像最多可为 2 TB 大小。不支持 SCSI CD-ROM 或 DVD-ROM 驱动器。

对于网络，Virtual Server 模拟一个 DEC 21140 10/100 MB 多端口以太网卡，卡上最多有四个独立网络连接。

关于 Virtual Server 架构要记住的重要事项——因为它们会在您为该产品编写脚本时出现——是：

- Virtual Server 可以包含一个或多个虚拟机配置，它们是构成虚拟机的所有设置。当虚拟机执行时，它被称为 *会话*。
- 每个虚拟机都有自己私有的虚拟资源，例如虚拟磁盘、串行端口等。其中一些资源，例如串行端口，可能映射到主机计算机上的物理资源。
- Virtual Server 可以包含一个或多个虚拟网络，其中一些可能连接到主机计算机的物理网络。每个虚拟机可以通过虚拟网络适配器连接到一个或多个虚拟网络。

### 理解 Virtual Server 对象模型

Virtual Server 对象模型以 *VirtualServer.Application* 对象开始，该对象实现名为 *IVMVirtualServer* 的 COM 接口。此对象提供了访问 Virtual Server COM API 支持的所有其他对象的方法。*VirtualServer.Application* 对象的一些主要方法和属性包括：

- *FindVirtualMachine* 此方法根据您提供的配置名称返回一个虚拟机对象（*IVMVirtualMachine* 接口）。
- *CreateVirtualMachine* 此方法创建一个新的虚拟机配置，并返回一个代表新虚拟机的 *VirtualMachine* 对象。还有一个 *DeleteVirtualMachine* 方法删除虚拟机配置。
- *RegisterVirtualMachine* 此方法将现有的虚拟机配置添加到 Virtual Server，允许您，例如，从另一个服务器导入虚拟机。*UnregisterVirtualMachine* 方法删除虚拟机而不从磁盘删除其配置文件。
- *FindVirtualNetwork, CreateVirtualNetwork, DeleteVirtualNetwork, RegisterVirtualNetwork* 和 *UnregisterVirtualNetwork* 这些方法执行与上述类似的任务，但使用虚拟网络而不是虚拟机。
- *GetHardDisk, CreateFloppyDiskImage, GetFloppyDiskImageType, CreateDynamicVirtualHardDisk, CreateFixedVirtualHardDisk, CreateDifferencingVirtualHardDisk* 和 *CreateHostDriveVirtualHardDisk* 这些方法都处理虚拟存储。

> **注意** *差异*磁盘包含虚拟机状态的所有差异。例如，您可以创建一个虚拟机，然后基于虚拟机的原始虚拟磁盘创建一个新的差异磁盘。对虚拟机的任何更改都存储在差异磁盘上。通过删除差异磁盘并恢复到原始虚拟磁盘，您可以有效地回滚对虚拟机所做的所有更改。有关详细信息，请参阅 Virtual Server 文档。

![](img/4fefd6988ba5d4a92a65127617ca24c2_505_0.png)



## 虚拟服务器 API 方法

虚拟服务器 API 包含约 40 个对象。除了顶层的 *VirtualServer.Application* 对象外，您最可能使用的对象包括以下（此处列出它们的 COM 接口名称）：

- *IVMDHCPVirtualNetworkServer*
- *IVMDVDDrive*
- *IVMFloppyDrive*
- *IVMGuestOS*
- *IVMHardDisk*
- *IVMHostInfo*
- *IVMNetworkAdapter*
- *IVMSCSIController*
- *IVMSerialPort*
- *IVMVirtualMachine*
- *IVMVirtualNetwork*

这些方法允许您操作虚拟服务器配置设置：

- `GetConfigurationValue`、`RemoveConfigurationValue` 和 `SetConfigurationValue`
- `GetHardDiskFiles`、`GetVirtualMachineFiles`、`GetVirtualNetworkFiles`、`GetFloppyDiskFiles` 和 `GetDVDFiles` - 这些方法返回相应类型文件的数组。
- `AvailableSystemCapacity` - 此方法返回一个可用容量百分比，基于当前运行的虚拟机数量计算。
- `VirtualMachines` - 此方法返回一个 VirtualMachine 对象的集合。您可以枚举此集合，例如，对每个已配置的虚拟机执行任务。
- `VirtualNetworks` - 此方法返回一个 VirtualNetwork 对象的集合。您可以枚举此集合，例如，检查每个已配置虚拟网络的属性。

例如，这是一个快速脚本片段，它将显示在虚拟服务器下配置的所有虚拟机的名称。

```
Set objVS = Createobject("virtualserver.Application")
For Each objVM In objVS.VirtualMachines
    WScript.Echo "VM: " & objVM.Name
Next
```

> **注意** 本章中的所有脚本都假设您直接在虚拟服务器计算机上运行脚本，这通常是唯一可用虚拟服务器 COM 对象的地方。理论上，您可以使用 VBScript *CreateObject* 函数在远程虚拟服务器计算机上实例化 *VirtualServer.Application* 对象。不过，我们未能持续成功使用此技术，更倾向于直接在虚拟服务器主机上运行脚本。如果您想在 Windows XP Professional 计算机上使用商用脚本编辑器（如 PrimalScript 或 OnScript）编写脚本，可以安装 Virtual Server 2005 用于开发目的。这将为您的计算机提供必要的类型库，使编辑器的类 IntelliSense 代码提示功能能够与虚拟服务器对象一起使用。

### 编写预配置脚本

预配置是初始配置新虚拟机的行为。使用脚本可以节省时间，并使配置多个新虚拟机的过程更简单、更一致。创建新虚拟机很简单。

```
Set objVS = CreateObject("VirtualServer.Application")
Set objVM = objVS.CreateVirtualMachine("MyMachine", _
    "D:\Virtual Machines\MyMachine")
```

创建新虚拟机后，*objVM* 将成为新创建虚拟机对象的引用。当然，单独的虚拟机本身用处不大。您至少需要连接一个硬盘，并且可能希望为虚拟机配备 DVD-ROM 驱动器，以便安装操作系统。我们通常更喜欢创建动态虚拟硬盘，它们开始时是较小的物理文件，然后增长到您指定的最大大小（这意味着一个 4GB 的磁盘在未填满之前不会占用 4GB 存储空间）。要创建新虚拟机，假设 *objVS* 已如上所示实例化，请执行以下操作：

```
errReturn = objVS.CreateDynamicVirtualHardDisk _
    ("D:\Virtual Machines\MyMachine\HardDisk.vhd", 10000)
```

这将在指定位置创建一个新的 10GB 动态磁盘。假设我们有一个包含操作系统安装介质的 ISO 格式 DVD-ROM 镜像。我们现在希望将该 DVD-ROM 镜像以及新创建的硬盘连接到虚拟机（由变量 *objVM* 表示）。首先，我们将硬盘镜像作为 IDE 镜像（零）连接到第一个 IDE 总线（零），然后将驱动器添加为设备零。我们将获得一个 *HardDiskConnection* 对象，并将其存储在 *objDrive* 中。

```
Set objDrive = objVM.AddHardDiskConnection _
    ("D:\Virtual Machines\MyMachine\HardDisk.vhd",0,0,0)
```

现在我们将添加一个 DVD-ROM 驱动器。同样，我们将它连接到 IDE 总线（即总线零），但这次，我们将 DVD-ROM 驱动器作为第二条总线上的第一个设备（设备零）。

```
Set objDVD = objVM.AddDVDRAMDrive(0,1,0)
```

这返回一个 DVDDrive 对象，我们将其存储在 objDVD 中。要附加我们的 ISO 镜像，请执行以下操作：

```
errReturn = objDVD.AttachImage("D:\ISO\win2003Standard.iso")
```

我们现在可能希望调整硬盘的某些属性。objDrive 变量代表硬盘连接；要获得实际的驱动器，我们需要使用连接的 HardDisk 属性。

```
Set objHDisk = objDrive.HardDisk
```

目前，我们对磁盘能做的不多，因为它不包含任何数据，但知道如何访问它很有用。

我们的虚拟机如果有网络连接也会更有用，所以让我们为它添加一个网络适配器。

```
Set objNIC = objVM.AddNetworkAdapter()
```

当然，目前我们还没有可以将适配器插入的网络，所以让我们创建一个。

```
Set objNetwork = CreateVirtualNetwork("MyNetwork", _
    "D:\Virtual Networks\MyNetwork\")
```

现在我们可以将我们的虚拟网络适配器连接到新的虚拟网络。

```
objNIC.AttachToVirtualNetwork("MyNetwork")
```

剩下的就是启动新虚拟机。如果我们附加的 DVD-ROM ISO 镜像设置了无人参与安装脚本，操作系统安装就可以自行启动，并使我们的新虚拟机启动并运行。要启动虚拟机，请执行以下操作：

```
objVM.Startup()
```

就是这样。我们创建了一个新虚拟机并启动了它。清单 17-1 是整个脚本。

#### 清单 17-1：创建并启动新虚拟机

```
Set objVS = CreateObject("VirtualServer.Application")
Set objVM = objVS.CreateVirtualMachine("MyMachine", _
    "D:\Virtual Machines\MyMachine")

'创建并连接硬盘
errReturn = objVS.CreateDynamicVirtualHardDisk _
    ("D:\Virtual Machines\MyMachine\HardDisk.vhd", 10000)
Set objDrive = objVM.AddHardDiskConnection _
    ("D:\Virtual Machines\MyMachine\HardDisk.vhd",0,0,0)

'连接 DVD-ROM 设备和 ISO 镜像
Set objDVD = objVM.AddDVDDrive(0,1,0)
objDVD.AttachImage "D:\ISO\win2003Standard.iso"

'获取硬盘的引用，即使我们现在
'不打算使用它
Set objHDisk = objDrive.HardDisk

'连接虚拟网络适配器，创建网络，
'并将适配器连接到网络
Set objNIC = objVM.AddNetworkAdapter()
Set objNetwork = CreateVirtualNetwork("MyNetwork", _
    "D:\Virtual Networks\MyNetwork\")
objNIC.AttachToVirtualNetwork("MyNetwork")
objVM.Startup()
```

> **随书附带 CD** 您将在此书随附的 CD 上找到此脚本以及本章中列出的其他脚本。

这是大多数预配置脚本将遵循的基本模式。

1.  创建新虚拟机。
2.  创建外围设备，例如网络适配器和磁盘。
3.  将外围设备连接到虚拟机。
4.  设置外围设备的属性（例如，将 DVD-ROM 连接到 ISO 镜像）。
5.  启动虚拟机。

在启动虚拟机之前，您可能需要配置虚拟机本身的其他属性。例如，我们通常包括以下一些内容：

```
objVM.Undoable = True
objVM.UndoAction = 1
objVM.Memory = 256
objVM.AutoStartAtLaunch = True
```

这些行将新虚拟机配置为可撤销，指定在关闭虚拟机时应保留当前状态（而不是自动提交或回滚当前状态），指定为虚拟机分配 256 MB 内存，并配置虚拟机在虚拟服务器启动时启动（这样，虚拟机始终处于运行状态并可用）。

### 编写管理脚本

虚拟服务器管理脚本对于执行定期计划的任务、自动化繁琐的任务或自动化需要同时针对多个虚拟机执行的任务非常有用。



#### 获取对象引用

在操作虚拟机、虚拟网络、虚拟磁盘或任何其他 Virtual Server 对象之前，您需要先获取该对象的引用。顶层的 *VirtualServer* 对象（使用 *ProgID VirtualServer.Application*）提供了返回各种类型对象引用的方法。例如：

-   要获取虚拟机的引用，请使用 `FindVirtualMachine("machinename")`。
-   要获取虚拟网络的引用，请使用 `FindVirtualNetwork("networkname")`。
-   要获取虚拟硬盘的引用，请使用 `GetHardDisk("disk_file_path")`。

您还可以枚举大多数二级对象。例如，*VirtualServer* 对象包含一个 *VirtualMachines* 属性，它是所有虚拟机的集合，以及一个 *VirtualNetworks* 属性，它是所有虚拟网络的集合。例如，要操作名为 *Win2003Server* 的虚拟机，您可以执行以下操作：

```
Set objVS = CreateObject("VirtualServer.Application")
Set objVM = objVS.FindVirtualMachine("win2003Server")
```

如果您想枚举所有虚拟机，请执行以下操作：

```
Set objVS = CreateObject("VirtualServer.Application")
For Each objVM in objVS.VirtualMachines
  'objVM 是一个虚拟机对象
Next
```

获取相应对象的引用后，您就可以使用其属性和方法来管理它。

#### 管理多虚拟机模板

管理多个虚拟机非常简单。只需编写一个脚本，针对一个虚拟机执行您需要的任何任务，确保使用对象变量 *objVM* 来引用该虚拟机。然后将您的脚本粘贴到一个多虚拟机包装器中。您的脚本将为该包装器所针对的每个虚拟机执行您编写的任务。

为了帮助您入门，我们提供了两个包装器。清单 17-2 是一个包装器，它从文本文件（默认为 C:\vmlist.txt，您可以轻松修改）中读取虚拟机名称。

492 第 IV 部分：企业脚本

```
清单 17-2 针对虚拟机列表
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("C:\vmlist.txt")
Set objVS = CreateObject("VirtualServer.Application")
Do Until objTS.AtEndOfStream
    '读取下一个虚拟机名称
    strVMName = objTS.ReadLine
    Set objVM = objVS.FindVirtualMachine(strVMName)
    '在此处使用 objVM 插入您的代码
Loop
objTS.Close
WScript.Echo "完成"
```

清单 17-3 针对 Virtual Server 中配置的所有虚拟机。

```
清单 17-3 针对所有虚拟机
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objVS = CreateObject("VirtualServer.Application")
For Each objVM In objVS.VirtualMachines
    '在此处使用 objVM 插入您的代码
Next
```

我们将在本章末尾使用清单 17-2，这样您就可以看到如何插入您自己的单虚拟机代码来创建一个多虚拟机脚本。我们将在清单 17-4 中使用清单 17-3，再次演示针对多个虚拟机编写任务脚本是多么简单。

#### 执行虚拟机任务

有许多虚拟机管理任务可以通过脚本完成。我们不会包括配置任务，例如附加新硬盘，这些任务通常只执行一次；相反，我们将重点放在您可能经常需要执行的管理任务上。

*VirtualMachine* 对象的多种方法可用于控制虚拟机的状态。（这些示例假设您已经在变量 *objVM* 中获取了 *VirtualMachine* 对象引用。）

```
objVM.Startup
objVM.TurnOff
objVM.Pause
objVM.Reset
objVM.Resume
objVM.Save
```

这些方法执行的任务相当于相应的用户界面控件：

-   *Startup* 方法启动虚拟机。
-   *Pause* 方法暂时挂起虚拟机，但不保存其状态。虚拟机实际上被挂起；Virtual Server 保持虚拟机“开机”状态，但停止执行虚拟机的客户操作系统。
-   *Resume* 方法将虚拟机从 *Pause* 模式中恢复出来，使其返回到您暂停时的状态。
-   *TurnOff* 方法切断虚拟机的虚拟电源，类似于从物理计算机上拔掉电源线。
-   *Reset* 方法类似于按下物理计算机上的重置按钮，其效果类似于快速连续运行 *TurnOff* 然后 *Startup*。
-   *Save* 方法保存虚拟机的当前状态，然后将其关闭。

> **注意** 虚拟机的*保存状态*包括其虚拟磁盘的当前状态以及整个内存，内存保存在主机计算机上的一个文件中。保存状态代表了虚拟机在某个时间点的确切状态，类似于在物理计算机上激活休眠模式。

一些额外的方法允许您操作虚拟机的保存状态。

-   *DiscardSavedState* 方法销毁虚拟机的保存状态数据，将虚拟机恢复到创建该保存状态的会话之前的状态。例如，假设您启动了一个虚拟机，然后将其关闭。然后您第二次启动它，保存其状态，然后丢弃该保存状态。虚拟机将处于第一次关闭后的状态，这是最后一次将更改提交到磁盘的时间点。
-   *DiscardUndoDisks* 方法与 *DiscardSavedState* 有些相似。正如我们解释过的，虚拟机可以配置为可撤销模式，这意味着其原始虚拟磁盘不受影响，磁盘更改被写入一个特殊的撤销文件。丢弃该撤销文件（或*撤销磁盘*）会将虚拟机恢复到原始虚拟磁盘的状态。或者，您可以使用 *MergeUndoDisks* 方法将撤销磁盘的更改合并到原始虚拟磁盘文件中，从而使更改成为永久性的。

例如，假设您已将所有虚拟机配置为可撤销模式。每天晚上，您希望合并撤销磁盘，并使当天的更改成为永久性的。（因此，在合并磁盘之前的任何时候，您都可以将虚拟机的状态恢复到前一天晚上的合并状态。）要合并 Virtual Server 计算机上所有虚拟机的撤销磁盘，您可以运行清单 17-4 中的简短脚本。

```
清单 17-4 合并所有虚拟机的撤销磁盘
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objVS = CreateObject("VirtualServer.Application")
For Each objVM In objVS.VirtualMachines

    '在此处使用 objVM 插入您的代码
    objVM.MergeUndoDisks

Next
```

您会注意到我们使用了一个包装器脚本来完成此任务。

*VirtualMachine* 对象公开了许多在各种管理任务中有用的属性。

-   *AutoStartAtLaunch* 当设置为 TRUE 时，此属性导致 Virtual Server 在自身启动时（例如在主机计算机重启后）自动启动虚拟机。
-   *AutoStartAtLaunchDelay* 此属性指定 Virtual Server 在自动启动虚拟机前等待的秒数。这很有用，因为一些虚拟机依赖于其他虚拟机（例如域控制器）才能运行。
-   *GuestOS* 此属性返回一个 *GuestOS* 对象，该对象表示在虚拟机内运行的客户操作系统。我们将在本章后面更详细地讨论这个对象。
-   *Keyboard* 此属性返回一个 *Keyboard* 对象，该对象表示虚拟机的键盘。我们将在本章后面更详细地讨论这个属性。
-   *Memory* 此属性允许您检查或更改分配给虚拟机的内存量，单位为兆字节。请注意，除非虚拟机已关闭，否则您无法更改此属性。
-   *Mouse* 此属性返回一个 *Mouse* 对象，该对象表示虚拟机的鼠标。我们将在本章后面更详细地讨论这个属性。
-   *State* 此属性列出虚拟机的当前状态。此属性是只读的；您不能通过直接修改此属性来更改状态。此属性的可能值包括以下内容：

-   0：无效
-   1：已关闭
-   2：已保存
-   3：正在启动
-   4：正在还原
-   5：正在运行
-   6：已暂停
-   7：正在保存



##### 10: 删除虚拟机

**Undoable** 当此属性设置为 TRUE 时，虚拟机将被设置为可撤销状态；设置为 FALSE 时则不可撤销。

**UndoAction** 此属性设置当虚拟机的客户操作系统通常关闭时，虚拟服务器应采取的操作。此属性的可能值为：
- 0 丢弃撤销驱动器（从而撤销自虚拟机启动以来所做的任何更改）。
- 1 保留撤销驱动器（保留任何更改，但保留稍后撤销它们的能力）。
- 2 提交撤销驱动器中的更改（合并驱动器），使更改永久生效。

清单 17-5 是一个使用 *VirtualMachine* 对象属性生成虚拟机清单列表的示例。请注意，这仅在每台虚拟机都安装了客户操作系统且功能正常时才有效。

```
清单 17-5 列出虚拟机
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objVS = CreateObject("VirtualServer.Application")
For Each objVM In objVS.VirtualMachines

    If objVM.AutoStartAtLaunch Then
        strAuto = "Auto start"
    Else
        strAuto = "Manual start"
    End If

    strGuestOS = objVM.GuestOS.Name
    strDisks = objVM.HardDiskConnections.Count & " Disks"
    strNICs = objVM.NetworkAdapters.Count & " NICs"
    Select Case objVM.ShutdownActionOnQuit
        Case 0
            strAction = "Save state on quit"
        Case 1
            strAction = "Turn off on quit"
        Case 2
            strAction = "Shutdown on quit"
    End Select

    Select Case objVM.State
        Case 0
            strState = "Invalid"
        Case 1
            strState = "Off"
        Case 2
            strState = "Saved"
        Case 3
            strState = "Turning on"
        Case 4
            strState = "Restoring"
        Case 5
            strState = "Running"
        Case 6
            strState = "Paused"
        Case 7
            strState = "Saving"
        Case 8
            strState = "Turning off"
        Case 9
            strState = "Merging"
        Case 10
            strState = "Deleting"
    End Select

    If objVM.Undoable Then
        strUndo = "Undoable"
    Else
        strUndo = "Not undoable"
    End If

    WScript.Echo objVM.Name & ": " & _
        strUndo & "," & _
        strState & "," & _
        strAction & "," & _
        strGuestOS & "," & _
        strDisks & "," & _
        strNICs & "," & _
        strAuto

Next
```

以下是此脚本在 CScript.exe 下运行时的输出示例。

winXP: Undoable,Running,Shutdown on quit,Windows XP Professional,1 Disks,1 NICs,Auto start
win2003: Undoable,Running,Shutdown on quit,Windows Server 2003,1 Disks,1 NICs,Auto start
Linux: Not undoable,Turned off,Shutdown on quit,Red Hat Linux,2 Disks,1 NICs,Manual start

#### 执行虚拟磁盘任务

*HardDisk* 对象表示一个虚拟磁盘，并包含一些对管理很有用的方法，特别是定期维护任务。
- **Compact** 对于动态（相对于固定大小）磁盘，此方法尽可能减小磁盘文件大小，消除未使用的空间。
- **Merge** 此方法将虚拟磁盘的撤销文件与父文件合并。
- **MergeTo** 此方法将撤销磁盘及其父文件合并到一个新的独立虚拟磁盘文件中。必须向此方法传递两个参数，指示新虚拟磁盘的文件名和要使用的类型（固定大小或动态）。例如，*objDisk.MergeTo("C:\Newdisk.vmdk",0)* 将合并到一个新的动态磁盘（对于固定大小磁盘使用 1）。

所有这些方法都返回一个 *Task* 对象；您可以检查该对象的 *IsComplete* 方法以了解操作何时完成。例如：

```
Set objTask = objDisk.Compact
Do Until objTask.IsComplete
    wScript.Sleep 5000
Loop
```

> **注意** 我们将 *撤销磁盘* 之类的东西称为似乎是单独的磁盘，但它们并非如此。任何给定的虚拟磁盘——即 Virtual Server *HardDisk* 对象的一个实例——由一个或多个包含磁盘永久部分的 *基本* 文件组成。它还可以包括一个或多个 *撤销* 或 *差异* 文件，这些文件通常被称为 *撤销磁盘*。然而，所有这些文件——基本和撤销——构成了实际的 *HardDisk* 对象。

#### 执行客户操作系统任务

*GuestOS* 对象提供了一些方法和属性，用于对在虚拟机中运行的客户操作系统进行基本控制。此对象可通过虚拟机的 *GuestOS* 属性访问。请注意，*GuestOS* 对象的某些功能要求在客户操作系统上安装虚拟服务器附加软件。属性包括：
- *AdditionsVersion* 此属性是已安装的虚拟服务器附加软件的版本。如果未安装附加软件，则此值可能为空。
- *CanShutdown* 如果虚拟服务器可以触发普通客户操作系统关闭，则此属性设置为 TRUE。
- *OSName* 此属性是客户操作系统的名称。
- *IsHeartBeating* 如果客户操作系统中安装的附加软件表明客户操作系统正在运行，则此属性返回 TRUE。如果已安装附加软件但 *IsHeartBeating* 为 FALSE，则客户操作系统可能已锁定或崩溃。

*GuestOS* 对象的方法包括：
- *InstallAdditions* 此方法尝试定位包含适用于客户操作系统的适当虚拟服务器附加软件的 ISO 镜像（随虚拟服务器一起提供）。它将 ISO 镜像附加到 DVD 驱动器，如果客户操作系统是 Windows 版本，它将启动附加软件安装程序。
- **ExecuteCommand** 我们提到此方法是因为您可能会遇到它，并且因为它的名字如此诱人且充满希望。在 Virtual Server 2005 中，遗憾的是，它没有任何作用。
- **ShutDown** 此方法触发客户操作系统中的普通关闭。它要求安装并运行附加软件。目前仅支持 Windows 客户操作系统。

#### 执行鼠标和键盘任务

您可以使用虚拟机的 *Mouse* 和 *Keyboard* 对象（分别通过虚拟机的 *Mouse* 和 *Keyboard* 属性获得）来自动执行按键操作并在虚拟机内执行其他手动任务。*Keyboard* 对象包含几个方法。
- **PressKey** 此方法模拟在虚拟机内按下一个键。
- **ReleaseKey** 此方法模拟在虚拟机内释放一个键。
- **PressAndReleaseKey** 此方法模拟在虚拟机内按下并释放一个键。
- **TypeAsciiText** 此方法模拟在虚拟机内键入纯文本。
- **TypeKeySequence** 此方法模拟在虚拟机内键入一系列按键。

除了 *TypeAsciiText*，您都需要提供一个适当的键标识符。常规字符——字母、数字和标点符号——被标识为 *Key_A*，将 *A* 替换为相应的字符。特殊键的标识方式不同。例如，*F1* 键被标识为 *Key_F1*。Virtual Server 程序员指南包含键标识符的完整参考。要向虚拟机发送 *F1* 按键操作（其中您在 *objVM* 变量中持有对该虚拟机的引用），您可以执行如下操作。

```
Set objKey = objVM.Keyboard
objKey.PressAndReleaseKey("Key_F1")
```

类似地，*Mouse* 对象包含一个 *Click* 方法，它模拟在虚拟机内点击鼠标按钮。此方法需要一个参数，指示要点击的鼠标按钮：1 表示左键，2 表示右键，3 表示中键或鼠标滚轮点击。例如，*objMouse.Click(1)* 模拟在虚拟机内左键单击（假设变量 *objMouse* 引用虚拟机的 *Mouse* 对象）。

### 查看虚拟服务器脚本的实际运行

我们有一台运行着半打虚拟机的 Virtual Server 2005 计算机；每台虚拟机包含不同版本的 Windows。我们使用它们来测试脚本和其他项目。其中一台虚拟机是域控制器，我们已在其上配置



# 第四部分：企业脚本编写

我们在测试中使用了各种计算机账户。我们已将每台虚拟机配置为*可撤销*模式，这意味着测试结束后，我们可以将每台虚拟机回滚到初始状态，为下一轮测试做好准备。当然，由于虚拟机处于一个域中，我们倾向于将它们作为整体进行回滚——这样，我们就知道它们处于一致的状态，为我们的下一次测试做好了准备。手动回滚多台虚拟机有点耗时，因此我们编写了一个简单的脚本来完成这项工作。

我们首先打开一个名为 TestVMs.txt 的文本文件。在这个文件中，我们列出了每个测试虚拟机的名称。通过使用这个列表，我们可以避免影响 Virtual Server 可能正在运行的任何其他虚拟机。（我们曾不小心关闭并回滚了一台 SQL Server 开发人员正在使用的虚拟机——他相当生气。）

```vbscript
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("C:\TestVMs.txt")
```

接下来，我们实例化 Virtual Server COM 对象。

```vbscript
Set objVS = CreateObject("VirtualServer.Application")
```

我们使用一个循环来读取文本文件，直到到达文件末尾。

```vbscript
Do Until objTS.AtEndofStream
```

我们将虚拟机名称读入一个字符串变量，然后要求 Virtual Server 查找该虚拟机并返回一个 *VirtualMachine* 对象。

```vbscript
'Read the next VM name
strVMName = objTS.ReadLine
Set objVM = objVS.FindVirtualMachine(strVMName)
```

因为我们此时并不关心虚拟机的内容，所以只是将其关闭。这相当于虚拟机的直接切断电源，而不是进行正常的操作系统关机。同样，我们正在回滚虚拟机，因此任何因不当关机造成的损害都不会被保留。

```vbscript
'Turn off the VM
Set objTask = objVM.TurnOff
```

*TurnOff* 方法返回一个 *Task* 对象。Virtual Server 使用 *Task* 对象来跟踪可能需要一些时间才能完成的任务。在虚拟机完全关闭之前，我们无法回滚它，这可能需要一两秒钟，因此我们将每隔五秒左右检查一次任务的 *IsComplete* 属性。在 *IsComplete* 属性变为 TRUE 后，我们将继续下一步。

```vbscript
Do Until objTask.IsComplete
    WScript.Sleep 5000
Loop
```

由于我们将虚拟机配置为可撤销，Virtual Server 不会接触虚拟机的原始硬盘（我们安装 Windows 的地方）。相反，我们的测试导致的客户操作系统更改被写入一个特殊的撤销磁盘。我们始终可以选择提交撤销磁盘，从而将到目前为止的更改作为虚拟机的永久部分。相反，我们正在丢弃撤销磁盘，将虚拟机恢复到其原始状态。

```vbscript
'Discard undo disks
objVM.DiscardUndoDisks
```

然后，我们再次启动虚拟机，使其为下一轮测试做好准备。此技术也返回一个 Task 对象，但我们没有将其捕获到变量中。这是因为我们知道虚拟机启动需要一段时间，但我们并不关心；我们可以继续处理下一个虚拟机，让这个虚拟机执行它需要的任何操作。

```vbscript
'restart VM
objVM.Startup
Loop
```

最后，我们关闭输入文本文件并显示一条消息，表明脚本已完成。

```vbscript
objTS.Close
WScript.Echo "Complete"
```

**清单 17-6** 回滚一组虚拟机

```vbscript
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objTS = objFSO.OpenTextFile("C:\TestVMs.txt")
Set objVS = CreateObject("VirtualServer.Application")
Do Until objTS.AtEndOfStream
    'Read the next VM name
    strVMName = objTS.ReadLine
    Set objVM = objVS.FindVirtualMachine(strVMName)

    'Turn off the VM
    Set objTask = objVM.TurnOff
    Do Until objTask.IsComplete
        wScript.Sleep 5000
    Loop

    'Discard undo disks
    objVM.DiscardUndoDisks

    'restart VM
    objVM.Startup

Loop
objTS.Close
WScript.Echo "Complete"
```

这是一个很好的例子，展示了脚本如何为 Virtual Server 管理员节省时间。例如，我们有一个客户使用脚本定期关闭——意味着操作系统的正常关闭，而不仅仅是关闭虚拟电源——他们的虚拟机。然后，他们将虚拟硬盘文件备份到磁带，然后重新启动虚拟机。这为他们提供了整个虚拟机集的完整、时间点备份，而无需在客户操作系统内安装备份软件或代理。

### 总结

Virtual Server 2005 脚本编写有助于使 Virtual Server 管理更轻松、更有效。当然，它可以自动执行日常任务，例如设置新虚拟机或在组中回滚虚拟机。但除了 Virtual Server 的具体应用外，我们还向您展示了脚本编写的一个全新领域，并希望帮助您意识到脚本编写实际上有多么可扩展。只要您能找到它们的文档，Windows 计算机上存在的众多 COM 对象就可以提供广泛的管理功能。熟练编写 COM 对象脚本——例如 Virtual Server API——是成为更成功、更灵活的 Windows 管理脚本编写者的基石。

# 第五部分

## 附录

**本部分内容：**

附录 A：高级脚本编辑器功能

---

### 附录 A：高级脚本编辑器功能

| **本附录内容：** | |
| :--- | :--- |
| 通用功能 | 506 |
| 键盘快捷键 | 507 |
| 脚本片段 | 508 |
| 代码提示和完成 | 509 |
| 向导 | 510 |
| 调试 | 513 |
| 企业功能 | 514 |
| 安全功能 | 515 |
| 脚本部署和远程脚本 | 516 |
| WSF 和 WSC 支持 | 518 |
| 其他功能 | 518 |
| 如何获取软件 | 519 |

一个业余木匠可以用一把简单的锤子应付，但真正的专业人士使用的是射钉枪——用于高级工作的高级工具。脚本编写也是如此：虽然 Microsoft 记事本对初学者来说已经足够，但作为高级脚本编写者，您应该使用商业脚本编辑器，使脚本编写更轻松、更高效。我们将向您介绍几款，并重点介绍我们认为最有用的功能。

大多数 Microsoft Windows 管理员最初都在记事本中编写脚本。它是免费的，几乎可以在任何运行任何版本 Windows 的计算机上轻松获得，并且易于使用。不幸的是，使用记事本编写脚本有点像用剪刀修剪树篱——您可以这样做，但它当然不能让您的工作变得更轻松。记事本缺少行号，这在脚本编写中至关重要，因为您从 VBScript 获得的所有错误消息都将引用发生错误的行。记事本也不会正确格式化您的脚本，或在循环内添加缩进、正确大写关键字等等。当然，您的脚本在没有这些花哨功能的情况下也能运行。VBScript 在这方面非常宽容。但是，您的脚本将更难阅读，这意味着它们更难调试，从长远来看也更难维护。

这就是为什么我们建议认真的脚本编写者——因为您正在阅读一本关于高级脚本编写的书，您符合“认真”的标准——投资于商业脚本工具。这意味着您必须进行财务投资；但我们认为，从长远来看，您在创建、调试和维护脚本方面节省的时间和精力，这项投资是非常值得的。

> **注意** 有一些免费的脚本编辑器提供基本功能。在搜索引擎（如 Google 或 MSN）中输入 **VBScript Editor**，或访问下载网站（如 Download.com），看看能找到什么。

当然，如果不能利用它们，世界上所有的花哨功能都是无用的。本附录的目的是帮助您识别哪些功能在 Windows 管理脚本编写中真正有用，并让您了解这些功能如何工作以及它们如何帮助您。您可以在您最终购买的任何工具中训练自己使用这些功能。我们将重点介绍四款商业编辑器，它们各自提供了专门为 Windows 管理脚本编写设计的各种功能。

我们考察的四款商业脚本应用程序是 PrimalScript、AdminScriptEditor、OnScript 和 VBSEdit。我们不直接比较这些编辑器，也不提供其所有功能的完整列表。相反，我们指出它们提供的一些功能，这些功能帮助我们更快地编写出更好的脚本。您应该自行评估这些和其他工具，以决定哪些最能满足您的需求。

#### 通用功能

任何优秀的商业脚本编辑器都应包含一些功能。第一种是语法着色，这意味着编辑器会为 VBScript 关键字、变量、文字和其他语言元素着色。通常，您可以自定义着色以适应您的偏好或视觉要求。着色通常伴随着大小写更正，这允许编辑器将，例如，*msgbox* 更改为 *MsgBox*。与 JScript 等语言不同，VBScript 不区分大小写，但所有内容都正确大写确实会使您的脚本更易于阅读，也更专业。这实际上是着色和大小写更正的最终目的：使您的脚本更易于阅读。当您查看一百行 VBScript 代码并试图查找错误时，易读性非常重要。事实上，您会惊讶于一个格式整齐的脚本甚至如何帮助使基本的调试变得更轻松。您无需学习如何使用着色功能，因为编辑器会自动完成。

另一个自动功能是缩进。这允许您输入脚本而无需过多担心格式。这样，当您开始一个新构造——例如一个 *Do...Loop* 构造——您只需在构造内按 *Tab* 键。这会使下一行代码缩进，像这样。

```vbscript
DO Until objTS.AtEndofStream
    strName = objTS.ReadLine
```

后续代码行会自动缩进到同一级别。当您完成循环后，只需按 *Backspace*，然后输入循环的结束语句。结果就像这样。



##### 脚本代码片段

大约一年前，PrimalScript 几乎是唯一一款以*代码片段*为特色的脚本编辑器，这些代码片段是你可以在脚本中重复使用的短小代码块。如今，几乎所有的编辑器都在其产品中加入了代码片段或类似功能。iTripoli 公司的 AdminScriptEditor 称之为 ScriptBits，XLnow 公司的 OnScript 则拥有一个代码库，而 Adersoft 公司的 VBSEdit 提供了一个可以访问代码片段的菜单。尽管如此，我们仍然最喜欢 PrimalScript（来自 SAPIEN 公司）。如图 A-1 所示，PrimalScript 在屏幕右侧显示一个代码片段浏览器窗格。你可以浏览数十个代码片段（该公司甚至在其网站上销售附加组件包），并将它们直接拖放到你的脚本中。代码片段可以包含填充区域，你可以在其中完成语句以根据你的脚本自定义代码片段。

![](img/4fefd6988ba5d4a92a65127617ca24c2_527_0.png)

**图 A-1** 在 PrimalScript 中使用代码片段

这是我们正在讨论的所有编辑器都提供的功能。然而，我们最喜欢 PrimalScript 代码片段的原因是，也可以通过键盘快捷键访问这些代码片段。例如，如果你需要创建一个 ActiveX 数据对象 (ADO) 记录集，你只需键入 `createrecordset`（代码片段的名称）并按 *Ctrl+J*。整个代码片段（在这种情况下是十几行代码）会立即出现在你的脚本中，替换代码片段的名称。

为什么代码片段如此有用？想想看，你需要编写多少时间才能写出例如打开一个记录集并遍历其记录所需的大约十几行代码。两分钟？也许五分钟？有了代码片段，你只需几秒钟就能完成。诀窍在于训练自己尽可能使用这些代码片段，而不是从头开始编写代码。扩展你的代码片段库也有帮助。例如，PrimalScript 可以将任何代码段转换为可重用的代码片段。只需选择代码，右键单击它，然后从快捷菜单中点击“另存为代码片段”。这是一个非常有用的功能，因为它本质上意味着你永远不必输入两次相同的代码。第一次输入时将其保存为代码片段，然后从此使用该代码片段。Windows 管理脚本通常需要打开文本文件以读取名称，甚至枚举 Active Directory 中的对象。没有理由不将这些代码转换为代码片段，以便你可以在需要时轻松地重用它。

##### 代码提示与补全

我们正在讨论的所有四种编辑器——PrimalScript、VBSEdit、AdminScriptEditor 和 OnScript——都提供某种形式的代码提示和补全。微软为此功能注册的商标是 Intellisense，如果你曾见过开发人员使用 Microsoft Visual Studio 工作，你会立即认出此功能。如图 A-2 所示，OnScript 显示一个选项菜单以补全你正在输入的代码。你通常可以按一个操作键（空格键、Tab 键等）来接受当前突出显示的选择并完成你的语句。

![](img/4fefd6988ba5d4a92a65127617ca24c2_528_0.png)

**图 A-2** 在 OnScript 中使用代码补全

代码补全通常可以为你节省查阅文档以查找使用哪种方法、属性名称或对象 ProgID 所需的时间。所有选项按字母顺序列在菜单中，你只需向下滚动到所需的选择——当然，使用方向键，因为伸手去拿鼠标会浪费时间——按操作键，然后完成你的代码。

代码提示是一个类似的功能，服务于相同的目的：避免需要查阅文档。下一页的图 A-3 显示了 PrimalScript 的代码提示功能。一个屏幕提示会提醒你函数和语句的正确语法——甚至包括你在脚本中自己定义的那些。通过这种快速、不引人注目的提醒，你可以弄清楚例如 *InStr* 函数中哪个参数在前——这是我们总是很难记住的事情——而无需浪费时间在 VBScript 文档中查找函数的语法。

![](img/4fefd6988ba5d4a92a65127617ca24c2_529_0.png)

**图 A-3** 在 PrimalScript 中使用代码提示

##### 向导

向导是脚本编辑器提供的一些小型内置工具，旨在使脚本编写更容易。一个很好的例子是 AdminScriptEditor 的 MessageBox 向导。VBScript 的 *MsgBox* 语句（或函数，取决于你的使用方式）具有很大的灵活性。你可以指定各种按钮组合、图标等。不幸的是，记住所有可用选项以及选择它们的值很难，通常需要快速查阅 VBScript 文档。MessageBox 向导为你提供了一个简单的图形用户界面来选择你想要的选项，如图 A-4 所示。完成后，正确的 VBScript 代码会自动插入到你的脚本中。

其他向导可以执行更复杂的任务。例如，VBSEdit、AdminScript Editor 和 PrimalScript 都包含一个 Windows 管理规范 (WMI) 向导，它会为你生成简短的 WMI 脚本。图 A-5 显示了 PrimalScript 的向导，它允许你浏览你计算机上的 WMI 类，以及你有权限访问的任何远程计算机上的类。

附录 A：高级脚本编辑器功能 511

![](img/4fefd6988ba5d4a92a65127617ca24c2_530_0.png)

**图 A-4** 在 AdminScriptEditor 中使用 MessageBox 向导

![](img/4fefd6988ba5d4a92a65127617ca24c2_530_1.png)

**图 A-5** 在 PrimalScript 中查看 WMI 向导

> **更多信息** 第 12 章“使用 WMI 工具改进脚本编写”更详细地介绍了 PrimalScript WMI 向导，并提供了使用它在更短时间内编写更复杂脚本的建议。

向导生成的脚本可以插入到你自己的脚本中，然后进行调整以满足你的需求。使用这样的向导通常比手动创建代码来查询某些 WMI 信息容易得多，而且向导还提供了一种方便的方式来浏览可用的 WMI 类。一些 WMI 向导，例如 AdminScriptEditor 中的那个，还会显示你选择的 WMI 类的示例数据，帮助你确认该类是否正确。

Do Until objTS.AtEndOfStream
    strName = objTS.ReadLine
    If strName = "Server1" Then
        WScript.Echo "Skipping Server1"
    Else
        ConnectToServer(strName)
    End If
Loop

每个结构都很好地缩进，让你可以直观地识别每个循环或其他结构的开始和结束位置。这在调试脚本时非常有用，并且使长期维护更容易。这样的缩进被认为是行业最佳实践（实际上多年来一直如此），而脚本编辑器中的自动缩进使得在你自己的脚本中遵循这一最佳实践变得更加容易。

##### 键盘快捷键

这看起来可能像一件很傻的事情需要指出，但键盘快捷键极其重要，而且令人惊讶的是，并非每个脚本编辑器都提供了很多快捷键。想一想：你是通过打字而不是使用鼠标来创建脚本的。因此，你的双手在键盘上停留的时间越长，你的工作效率可能就越高。我们大概可以在三到四秒内输入一行平均长度的脚本。这大约是伸手去拿鼠标并点击工具栏按钮所需的时间。然而，按一个键盘快捷键来激活该工具栏按钮的功能可能需要不到一秒钟，而这段时间足够多写一行代码。将节省的时间乘以你在编写脚本过程中可能点击的几十个工具栏按钮，你可能会损失大量的时间。是的，你确实需要训练自己记住并使用键盘快捷键，但这最初的投入是值得的。

作为技术专业人士，你可能对那些不使用键盘快捷键的人感到有些沮丧。例如，你有多少次站在一个有技术问题的用户身后，要求他或她复制和粘贴少量文本？一个没有经验的用户会抓起鼠标，高亮显示文本（可能需要一两次尝试），右键单击文本，然后从快捷菜单中点击“复制”。与此同时，你的手指正急不可耐地想要接管，用键盘高亮显示文本，并按 *Ctrl+C* 将其复制到剪贴板。那样你就能更快地回到其他工作上。这就是我们谈到脚本编辑器中的键盘快捷键时所指的那种事情。找一个为其尽可能多的关键功能提供快捷键的编辑器，包括运行脚本、设置调试断点、启动向导、插入代码片段等。然后训练自己使用键盘快捷键，并尽可能让双手远离鼠标。



## 512 第五部分：附录

有时，向导程序不仅仅编写简单的示例脚本，而是实际扩展了脚本的功能。一个很好的例子是 PrimalScript 的 ADSI 向导（仅在专业版中提供）。图 A-6 展示了运行中的向导。与向导通常提供的功能不同，这里没有预览将要生成的脚本。然而，向导所做的远比仅仅创建一些示例代码复杂得多。它正在你的脚本中创建全新的对象类。每个类都代表一个 Active Directory 对象，例如用户或计算机。

![图 A-6 运行 PrimalScript ADSI 向导](img/4fefd6988ba5d4a92a65127617ca24c2_531_0.png)

将这些添加到你的脚本后，你将能够创建这些对象类的新实例来表示 ADSI 用户、计算机或其他对象。如图 A-7 所示，PrimalScript 可以对这些对象提供完整的代码补全和提示功能，使 ADSI 脚本编写变得更加直观。

```
Dim objADSI
Dim objADSIUser
Dim objADSIContact

Set objADSI = New ADSIConnection
Set objADSIUser = New ADSIUser
Set objADSIContact = New ADSIContact

If False Then
    ' Additional Wizard Sample Code
    Call objADSI.GetUser(objADSIUser, "cn=Users", "Hooten")
    Call objADSI.GetContact(objADSIContact, "ou=HR,ou=Depts")
    objADSI.CreateContact("ou=HR,ou=Depts", "Gates")
End If
' End sample ADSI Wizard code

' ************* End ADSI Wizard generated code. Do not modif

objADSIUser.
```

![图 A-7 测试新 ADSI 相关对象的代码补全功能](img/4fefd6988ba5d4a92a65127617ca24c2_531_1.png)

这里的教训是，代码向导可以节省时间，让脚本编写更轻松，并提供你自己可能需要花费数小时甚至数天才能编写的功能。学会使用这些向导可以为你节省大量时间，尤其是在复杂的脚本编写任务中，即使你不得不对其输出进行一些调整以满足你的精确需求。

> **提示** 一些编辑器——例如 AdminScriptEditor 和 PrimalScript——是可扩展的，这意味着你可以向产品中添加向导。例如，SAPIEN 发布了用几乎任何兼容 COM 的语言（包括 Visual Basic）编写你自己的向导所需的规范。这些编辑器的制造商有时会发布额外的向导加载包，为其工具增加功能和价值。

向导的优点在于，它们为你提供了经验更丰富的开发人员的脚本编写能力——也就是编写向导的那个人或那些人。只要你掌握基础知识并保持简单，向导通常可以为你编写自动化 Windows 管理所需脚本的三分之二或更多。

##### 调试

编写脚本时，调试是生活中一个不幸的事实。除非你编写的是只有几行代码的最简单脚本，否则你很可能会在某个时刻遇到错误。我们讨论的三个编辑器——OnScript、AdminScriptEditor 和 VBSEdit——提供了与 Microsoft Script Debugger 的集成，该调试器可从 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/sdebug/Html/sdebug_1.asp 免费下载。

> **提示** 此链接，以及本书中引用的大多数链接，都包含在附带的 CD 上。点击 *Introducing Microsoft Script Debugger*。

这种集成允许你在编辑器的代码窗口中设置调试断点，然后从编辑器内（通常通过使用工具栏按钮或菜单命令）启动脚本调试器。如果你正在使用这些编辑器中的任何一个，请花时间下载并安装 Microsoft Script Debugger，以便你可以使用一些基本的调试功能。

> **更多信息** 全面讨论调试技术和概念超出了本书的范围。如果你想了解更多关于 VBScript 调试的信息，我们建议观看 *VBScript Debugging* 培训视频，可从以下两个网站获取：www.ScriptingAnswers.com www.ScriptingOutlook.com

PrimalScript 标准版包含相同风格的集成，但 PrimalScript 专业版包含一个名为 PrimalScope 的定制调试器。PrimalScope 比 Windows Script Debugger 功能更强大，它使得在脚本运行时深入查看其操作变得容易得多——这是成功高效调试的关键。与其他编辑器一样，PrimalScript 允许你设置断点——脚本执行将在此暂停，以便你可以检查到该点的脚本操作——在代码窗口中。然而，当你开始调试时，一切都在 PrimalScript 窗口内进行，如图 A-8 所示。

![图 A-8](img/4fefd6988ba5d4a92a65127617ca24c2_533_0.png)

左下方的窗格显示所有当前变量和对象属性值，因此你可以一目了然地看到脚本在循环和逻辑比较中使用的值。在右侧，表达式计算器显示任何表达式的当前结果。你可以在脚本中高亮显示甚至复杂的表达式，并将其拖入计算器中。随着脚本的执行，PrimalScript 会持续更新表达式的结果，因此你可以看到脚本生成和使用的值。按 *F11* 键可将脚本推进一行代码，使你能够逐行单步执行脚本，在每行代码执行后检查脚本的值。使用这些工具，你可以快速查看脚本在何处产生了意料之外的值、采取了不当操作等等。这是查找和消除错误的最快方法。

##### 企业功能

脚本编写常被视为一种擅自进行的操作，许多信息技术经理不喜欢它。尽管脚本编写对管理员有明显的好处，但公司经理们经常担心公司会依赖这些脚本，而当管理员离开时，这些脚本会带来维护噩梦。

帮助缓解这种担忧的一种方法是采用软件开发的企业最佳实践；也就是说，将脚本视为常规的、完整的软件开发项目。我们已经讨论了其中一些最佳实践，例如正确的代码格式化。另一个最佳实践是使用源代码管理软件，例如 Microsoft Visual SourceSafe、Borland StarTeam 等。此软件使你能够签入脚本，将它们保存在中央存储库中，该存储库可以备份并被视为公司的资产。当你需要修改脚本时，你将其签出，进行修改，然后签入修改后的版本。你签入的每个版本都会被保留，因此可以轻松检索以前的版本，与其他版本进行比较等等。虽然我们不知道任何包含源代码管理软件的脚本编辑器，但 PrimalScript 提供了一种与你单独获取的源代码管理软件集成的方法。（几乎任何拥有内部软件开发人员的公司都已经拥有某种源代码管理解决方案。）PrimalScript 提供了一个源代码管理工具栏，通过它可以访问源代码管理软件，并签入和签出脚本。图 A-9 显示了“签入文件”对话框，你可以在其中输入关于正在签入的脚本版本的注释。

![图 A-9 通过 PrimalScript 签入脚本](img/4fefd6988ba5d4a92a65127617ca24c2_534_0.png)

虽然使用源代码管理不会消除对管理脚本编写的所有潜在异议，但它会表明你认真地将脚本编写作为更有效地实现组织目标的工具。随着脚本库的增长，源代码管理还提供了宝贵的备份和版本控制资源。通过你的脚本编写环境访问源代码管理使其更加方便，这意味着你更有可能使用源代码管理系统。

##### 安全功能

在第 2 章“脚本安全”中，我们讨论了脚本安全如何成为大多数企业关注的问题，以及 Windows Script Host (WSH) 如何配置为具有 TrustPolicy 以使脚本编写更安全。我们认为，一个适当保护的脚本编写环境对于任何环境都是必须的，我们赞赏一些与脚本相关的工具也采纳了这一信念。在本附录中我们考察的四个编辑器中，只有 PrimalScript 提供了与 WSH TrustPolicy 的完全集成。图 A-10 显示了 PrimalScript 的“选项”对话框，以及

您可以注意到，有一个完整的部分专门用于介绍安全功能。您可以指定代码签名证书的名称，这使得 PrimalScript 能够按需对脚本进行数字签名，或者在每次保存脚本时自动进行签名。由于 WSH TrustPolicy 依赖数字签名来识别受信任的脚本，因此能够轻松且自动地签署脚本是构建更安全脚本环境的关键部分。

![](img/4fefd6988ba5d4a92a65127617ca24c2_535_0.png)

图 A-10 配置 PrimalScript 的 WSH 安全集成选项

在“安全设置”下拉列表中，您可以选择所需的 WSH TrustPolicy 级别，这可能允许您覆盖整个域范围的 TrustPolicy 配置，以便您可以在不受 TrustPolicy 限制干扰的情况下测试脚本。

##### 脚本部署与远程脚本

有时，运行特定脚本的最佳方式是直接在一台或多台远程计算机上运行它。我们在第 6 章“远程脚本”中讨论了远程脚本，但很多时候 *WshController* 对象对于特定情况无法提供足够的控制或反馈。这时，您可以借助您的脚本工具来提供优于 WSH 内置功能的部署和远程脚本能力。

AdminScriptEditor 和 PrimalScript 都提供了脚本打包功能。AdminScriptEditor 的打包器称为脚本打包器，而 PrimalScript 的则称为 ESP（进化脚本打包器）。这两个工具本质上都是将 VBScript 文件捆绑成一个独立的可执行文件，并允许您应用替代安全凭据，这样该可执行文件就可以由不一定有权限执行脚本任务的用户来运行。图 A-11 展示了 PrimalScript 的打包器，它允许您为最终的可执行文件指定自定义图标，还允许您将多个脚本文件、数据文件甚至 COM 组件包含在包中。该包将自动解压数据文件和 COM 组件、注册 COM 组件，然后按顺序或并行（由您决定）执行您的脚本。它甚至可以在脚本执行完成后删除数据文件。作为 PrimalScript 注重脚本安全性的一部分，包中的脚本可以进行数字签名，使其与 WSH TrustPolicy 兼容。

![](img/4fefd6988ba5d4a92a65127617ca24c2_536_0.png)

图 A-11 使用 PrimalScript 的 ESP 打包脚本

以这种方式打包脚本，可以更轻松地将它们作为独立工具部署给技术能力较弱的用户，甚至可以通过使用组策略对象或其他软件部署机制将它们作为应用程序部署。

将脚本部署到远程计算机的另一种方式是通过远程脚本，这非常类似于 *WshController* 所做的。PrimalScript（企业版）和 OnScript（网络版）都包含远程脚本功能。PrimalScript 的功能称为远程脚本执行引擎（RSEE）；OnScript 则直接将其作为其功能集的一部分。OnScript 的远程脚本要求您在希望管理和执行远程脚本的每台远程计算机上安装一个小型的 COM 组件。然后，该产品允许您连接到任何包含该 COM 组件的计算机，并在该远程计算机上维护一个脚本库。任何远程脚本都可以被执行，这会导致 COM 组件在远程计算机上本地运行该脚本。基本的状态信息会反馈到您的 OnScript 副本，以便您可以查看脚本何时结束。PrimalScript 的 RSEE 更为强大，它提供了将脚本部署到多台计算机的能力，而不是一次执行一个远程脚本。

远程脚本是分散大型脚本工作负载的一种绝佳方式。例如，与其编写一个脚本去连接一千台计算机中的每一台来进行某些配置更改，不如将脚本直接部署到每台计算机上，让脚本并行执行。这节省了大量时间，而将这种能力内置于您的脚本工具中，使其更加方便且更易于管理。

##### WSF 和 WSC 支持

在第 3 章和第 4 章中，我们向您展示了如何使用 Windows 脚本文件（WSF）和 Windows 脚本组件（WSC）将您的脚本打包成更模块化的独立文件。WSF 和 WSC 格式都需要相当复杂的 XML 格式，尽管大多数脚本工具和编辑器可以显示这些文件，但它们并没有提供任何简化格式的方法。PrimalScript 是一个例外。它提供了一个图形用户界面，使您能够配置 WSF 或 WSC 格式支持的各种选项，同时完全在后台处理复杂的 XML 格式。我们喜欢这些功能，因为它们使得使用这些强大的脚本文件格式变得更加实用。手动格式化 XML 是令人生畏且容易出错的，这常常导致管理员干脆放弃这些格式，从而无法享受其宝贵的优势。

> **更多信息** 有关 WSF 格式的更多信息，请参见第 3 章“Windows 脚本文件”。WSC 格式则在第 4 章“Windows 脚本组件”中介绍。

##### 其他功能

商业脚本编辑器可以提供额外的功能，使脚本编写更高效。我们特别喜欢的一些功能包括：

- 能够捕获来自 WSH 的输出，并在编辑器本身内显示脚本输出。
- 用于添加其他工具的选项，例如用于处理数据库的工具、其他脚本语言等。一些编辑器允许您集成计算机上已安装的现有工具，而其他编辑器则出售或提供可执行特定任务的加载项工具。
- 集成文档，例如可下载的 VBScript 文档或 Microsoft MSDN Library。最佳的集成形式是允许您突出显示一个语言关键字，按下一个热键（如 *F1*），然后在弹出框中查看该关键字的帮助。
- 允许您查看计算机上安装的 COM 对象的属性和方法的浏览器。这些浏览器通常使定位和使用 COM 对象变得更容易。
- 代码折叠，这是一个在脚本中定义*区域*的功能。这些区域可以代表一个子例程或函数，或者您定义的脚本区域。然后可以折叠（或*折叠*）和展开这些区域，帮助您隐藏脚本的部分内容，以便专注于其他部分。
- 块格式化功能，例如能够缩进或取消缩进代码块、将代码块转换为注释，或将注释块转换为活动代码。这些功能在编写较长、复杂的脚本时有助于节省时间。

这个列表还在继续。随着您使用所选的编辑器，您会发现自己变得越来越高效，您的脚本工作将花费更少的时间并产生更好的结果。

##### 在哪里获取软件

您可以从制造商的网站获取我们讨论过的四个产品的评估副本，当然也可以获取产品本身：

- AdminScriptEditor 可从以下两个网站获取：
    - http://www.itripli.com
    - http://www.adminscripteditor.com
    - 本书使用的是 2.2 版本。
- OnScript 可从以下网站获取：
    - http://www.onscript.com
    - 本书使用的是 1.0 版本。
- PrimalScript 可从以下网站获取：
    - http://www.sapien.com
    - http://www.primalscript.com
    - 本书使用的是 4 版本，主要关注专业版（尽管我们确实提到了一些仅在企业版中才有的功能）。
- VBSEdit 可从以下网站获取：
    - http://www.vbsedit.com
    - 本书使用的是 3 版本。

我们要再次强调，市面上还有*大量*其他的编辑器。有些是免费的，有些则需要购买。我们之所以专注于这四种产品，是因为它们提供了最专门针对 Windows 管理脚本的功能。许多其他产品只是花哨的文本编辑器，或许提供行号和其他一些有用的功能。还有一些是专门为 Web 开发设计的，尽管它们可能提供一些其他 VBScript 开发功能。虽然所有这些工具肯定都有用，但它们远不如一个专门为简化 Windows 管理脚本而设计的编辑器有用。当然，功能最强大、最丰富的工具成本也更高——事实上，我们的经验是，在功能方面，您确实物有所值。几乎每个行业的专业人士都会告诉您，花一点钱购买一套优秀的工具，从节省的时间和精力来看，是值得的。



我们经常被问到偏好和推荐哪款脚本编辑器。我们尝试过本附录中涵盖的所有编辑器，我们两人都将 PrimalScript 作为日常编辑器。然而，我们无法说哪一款最适合你。正因如此，我们很高兴这些产品的制造商大多提供 30 到 45 天试用期的试用版本，并且大多数在试用期内提供完整的产品功能。这为你提供了机会，可以下载每一个，试用一个月左右，然后决定哪一款的功能最适合你。当然，正如我们在本附录开头所说，请确保你正在训练自己使用这些功能，以便你能从最终决定使用的任何工具中获得全部收益。

## 索引

**符号**
- 三维滚动条，在 HTAs 中显示，142

**A**
- 中止脚本，20，292
- AbsolutePage 属性（ADO Recordset 对象），249
- AbsolutePosition 属性（ADO Recordset 对象），249
- Access。*参见* Microsoft Access
- 帐户。*参见* 用户帐户
- ACE（访问控制条目），241
- 激活 ODBC DSN，184
- Active Directory
    - 通过备用凭据连接，53
    - 使用 WMI 类进行配置，373–374
    - 连接到，快捷方式，255
    - 作为数据库，248–251
    - 查看 Exchange 信息，428
    - 映射列表，248
    - 检索其对象的 LDAP 路径，254
    - 查询和数组，428
    - 查询默认配置命名上下文，427
    - 查询 Exchange 邮箱存储，430
    - 查询 Exchange 存储组，428–429
    - 使用 homeMDBBL 属性进行查询，431–432
    - 注册 Schema 管理单元，251
    - 搜索，257
    - 修改信任提供程序，373–374
- Active Directory 浏览器 (ADSVW)，217–218
    - 连接到域根，218
    - 图形界面，218
    - 导航，218
- Active Directory 服务接口 (ADSI)。*参见* ADSI（Active Directory 服务接口）
- ActiveConnection 属性（ADO Recordset 对象），249
- ActiveX，96。*另见* COM 对象
- ActiveX 数据对象 (ADO)。*参见* ADO（ActiveX 数据对象）
- Add 方法（Dictionary 对象），23
- AddAsString 方法（SwBemPrivilegeSet 对象），275
- AdditionsVersion 属性（GuestOS 对象），497
- AddPrinterDriver 方法，384
- 管理员密码，使用脚本更改，26
- AdminScriptEditor MessageBox 向导，510
- AdminScriptEditor WMI 向导，349，350
- ADO（ActiveX 数据对象），179–180
    - 优势，180
    - 使用备用凭据连接，247
    - 关闭连接，255
    - Command 对象。*参见* Command 对象 (ADO)
    - 使用 ADO 连接到 ADSI，247
    - Connection 对象，181–182
    - 连接字符串。*参见* 连接字符串
    - 数据源。*参见* 特定数据源
    - 文档，191
    - 灵活性，180
    - 大结果集和 ADO，245
    - ODBC DSN 连接，182–184
    - 使用字符串变量过滤查询，258
    - Recordset 对象。*参见* Recordset 对象 (ADO)
    - 与 ADSI 结合测试组成员身份，256–259
- ADSCmd，220–225
- ADSI（Active Directory 服务接口），24–29
    - 其中的 ADO Recordset 对象属性，249–251
    - 其备用凭据，53
    - 区分大小写，25
    - 关闭连接，253
    - 命令行工具，220–225
    - ConnectionString 属性与 Provider 属性，247
    - 数据返回限制，227–229
    - 目录服务类型。*参见* LDAP 提供程序；WinNT 提供程序
    - 启用自动分页，250
    - 权限和 ADSI，167
    - 提供程序。*参见* LDAP 提供程序；WinNT 提供程序
    - 查询。*参见* ADSI 查询
    - 记录集支持的方法，250–251
    - Scriptomatic。*参见* ADSI Scriptomatic
    - 设置更改，26
- ADSI 提供程序，246–247
- ADSI 查询
    - 语法中的属性部分，252
    - 语法中的筛选器部分，251–252
    - 筛选，251–252，253
    - 使用查询进行更改，254–256
    - 远程查询，163
    - 指定范围，253
    - 专有语法，251–254
- ADSI Scriptomatic，207–209。*另见* Scriptomatic
    - 使用其创建用户帐户，207–208
    - 下载，209
    - 重用其中的代码，209
- ADSI 软件开发工具包 (SDK)，217。*另见* Active Directory 浏览器 (ADSVW)；ADSCmd；ADSIDump
- ADSIDump，222–225
- ADSVW。*参见* Active Directory 浏览器 (ADSVW)
- Alert 对象，470–471
- Alert 属性（ScriptContext 对象），465
- 在 MOM（Microsoft Operations Manager）中创建警报，481
- 别名，WMIC，326–328
    - 确定 get 命令返回哪些属性，333
    - 目标类，329–331
    - 查看其信息，331
- 备用凭据，52
    - 使用 Active Directory 服务接口 (ADSI)，53
    - 使用 ADO，247
    - CIM Studio 和备用凭据，344–345
    - 使用备用凭据进行远程脚本编写，165
    - 使用 RunAs 命令，52
    - 本地系统不可用，344
    - 使用 Windows Management Instrumentation (WMI)，54
    - 使用 Windows 任务计划程序，53
    - 使用 WMI 事件注册，301
    - 使用 WMIC (WMI 命令行)，332
- applicationname 属性（HTAs），141
- 在 Windows 防火墙中授权应用程序，361

### 应用程序，HTML
- 应用程序，HTML。*参见* HTAs（HTML 应用程序）
- 参数，验证，78
- Array 函数，22
- 数组，22
    - 关联数组，23。*另见* Dictionary 对象
    - 创建，22
    - 循环遍历数组元素，22
    - 在同一脚本中与 Dictionary 对象一起使用，24
    - 数组元素编号，22
    - 将查询的属性作为数组处理，428
    - 设置数组中数据的变量，29
    - 显示数组上限，22
    - 何时使用，23-24
- 关联查询，268-272
- 关联，267-268。*另见* 引用查询
- 关联数组，23。*另见* Dictionary 对象
- 关联类 (WMI)，267。*另见* 关联查询
- 异步通知查询，294，302
- 身份验证
    - 为异步查询设置身份验证，302
    - 在 WBEMTest 中启用身份验证，342
    - 为单个数据包设置身份验证，274
    - Kerberos，342
- 身份验证级别，设置，274
- AuthenticationLevel 属性（SWBemSecurity 对象），274
- AuthorizedApplications 对象（Windows 防火墙），362
- 在 Windows 防火墙中授权应用程序，361
- 自动更新，385
    - 实例化 COM 对象，388
    - 配置，385
    - 登录脚本，386-387
    - 显示远程清单，385-386
    - 部署设置，385
- AutoStartAtLaunch 属性（VirtualMachine 对象），494
- AutoStartAtLaunchDelay 属性（VirtualMachine 对象），494
- AvailableSystemCapacity 方法（VirtualServer.Application 对象），487

### B
- 后端数据库，196
- 备份
    - GPO，412
    - IIS 元数据库，378-379
- WMI 中的反斜杠，276
- Backup 方法（gpmGPO 对象），412
- 包含 WMIC 的批处理文件，337-341
- 绑定，376
- 位标志，277
- 阻塞，291-293
- BOF 属性（ADO Recordset 对象），249
- Bookmark 属性（ADO Recordset 对象），190，249
- 布尔参数，77
- 布尔类型，66
- border 属性（HTAs），141
- borderstyle 属性（HTAs），142
- 构建 HTAs（HTML 应用程序），132
- 按钮，149-150

### C
- 缓存，DNS，清除，366
- CacheSize 属性（ADO Recordset 对象），249
- 回调，295
- Cancel 事件 (WMI)，295
- CanShutdown 属性（GuestOS 对象），497
- caption 属性（HTAs），142
- CA（受信任的证书颁发机构）。*参见* 受信任的证书颁发机构 (CA)
- 全局编录 (GC)，228
- <CDATA> 标签 (XML)，58
- 创建 CDOEXM 对象，437
- 证书。*参见* 数字证书
- 证书颁发机构 (CA)，44
    - 检查，45
    - 商业与内部，49
    - 从受信任列表中移除，45
    - 受信任。*参见* 受信任的证书颁发机构 (CA)
- 复选框
    - checked 属性，150
    - 在 HTAs 中，150
    - 检查值，150
- checked 属性（HTML 复选框），150
- 检查错误，10-11
- 校验和，43
- CIM Studio
    - 使用备用凭据，344-345
    - 显示类信息，346
    - 查看类关系，346
    - 返回类的所有实例，346
    - 指定连接属性，344-345
    - 连接到命名空间，343-344
    - 远程连接，344
    - 搜索 WMI 类，345
    - Windows XP Service Pack 2 和 CIM Studio，343
- 类 ID，为集合对象设置，477
- ClassDefsOnly 关键字（ASSOCIATORS OF 查询），272
- 类
    - 在 CIM Studio 中，显示类信息，346
    - 在 CIM Studio 中，返回类的所有实例，346
    - DNS 记录类型的类，369
    - IIS 类，375
    - IIS 命名空间中的类，374-375
    - 在 CIM Studio 中查看类关系，346
- 类，WMI。*另见* 特定类
    - 检查操作系统对其支持，355-356
    - 使用 WMI 类配置 Active Directory，373-374
    - 在 Scriptomatic 中显示，320
    - Exchange 中的类，432
    - Windows Server 2003 省略的类，356
    - 按单个类查看支持的操作系统，356
    - 远程类，查看，324
    - 在 CIM Studio 中搜索，345
- classid，96
- classid 属性（XML 注册标签），97
- 子句，SQL。*参见* 特定子句
- 清除 DNS 缓存，365-366
- 在创建错误日志之前清除错误，10
- Click 方法（Mouse 对象），498
- 在虚拟机中单击鼠标按钮，498
- 剪贴板，将 WMIC 输出保存到，334
- ClusterState 属性（ExchangeServerState 类），435
- 脚本编辑器中的代码完成，509-510
- 代码折叠，518
- 脚本编辑器中的代码提示，226，509-510
- 重用代码。*另见* Windows 脚本组件 (WSC)
- 代码签名，49-50
    - 校验和，43
    - 公钥加密和代码签名，43
    - 使用 SAPIEN PrimalScript。*参见* SAPIEN PrimalScript
- 集合对象
    - 用于文件夹中的所有文件，20
    - 类 ID，设置，477



databases 523

- collections, 478
- columns, database, 180
- COM objects, 95–96. See also ActiveX code as. See Windows Script Components (WSCs)
- methods, 96
- command-line string, incorporating in IIS scripts, 380
- command-line utilities, 64
- Command objects (ADO), 191–192
  - creating, 191–192
  - data field length, specifying, 193
  - opening Recordset objects with, 192
  - parameters, adding, 192
  - parameters, data types for, 193
  - required properties, 192
  - setting up, 252
  - stored procedures and, 192
- command window
  - accessing WMI with. See WMIC (WMI Command Line)
  - saving WMIC output to, 334
  - writing script results to, 21
- commands
  - executing, 6
  - parsing output of, 6
  - waiting for finish before executing script, 6
- `<comment>` 标签 (XML), 59, 77, 99
- comments
  - converting into Windows Script File scripts, 77
  - converting into XML `<description>` tag, 77
  - in DSNs (Data Source Names), 184
  - in Windows Script Components (WSCs), 99
  - in Windows Script Files (WSFs), 59
- commercial certification authorities (CAs), 49
- Compact method (HardDisk object), 496
- compacting dynamic disks, 496
- `<component>` 标签 (XML), 97
- connecting to Active Directory, 255
- connecting to ADSI, 247
- connecting to databases, 181–182
- connecting to domains, 209, 221–222
- connecting to Exchange mailbox stores, 443
- connecting to global catalogs, 228
- connecting to namespaces
  - in CIM Studio, 343–344
  - in Exchange, 433
  - in IIS, 375
  - with Scriptomatic, 321
  - in WBEMTest, 341
  - in WMI Event Registration, 301
  - with WMIC (WMI Command Line), 326
- connecting to remote systems, 26
  - with alternate credentials, 33. See also alternate credentials;
  - 'SWbemLocator object
    - with distinguished object names, 27
    - pinging computers before, 357
    - specific object in, 26
  - with WMIC (WMI Command Line), 332
- connecting to Server service, 230
- connecting to users, 240
- Connection objects (ADO), 181–182
- connection strings, 181
  - ADO and, 246–247
  - italicized elements in, 185
  - to Microsoft Access, 185
  - to Microsoft Excel, 185
  - passwords in, avoiding, 185
  - placeholders in, 185
  - providers, 246
  - to SQL Server, 185
  - text files and, 185, 195
- ConnectionString property (ADSI), 247
- connectivity
  - permission, 163
  - remote scripting and, 162–165
- constants, 5
- GPMC (Group Policy Management Console), 397–403
- consumers, 286
  - defining, 300
  - registering filters with, 305
  - temporary vs. permanent, 286
  - in WMI Event Registration, 303
- containers, 209
- context, and remote scripting, 167–170
- context menus in HTAs, turning off, 142
- contextmenu attribute (HTAs), 142
- controlling software execution. See Software Restriction Policies (SRP)
- Count method (Dictionary object), 23
- Create method, 27
- CreateAlert method (ScriptContext object), 465
- CreateDifferencingVirtualHardDisk method (VirtualServer.Application object), 486
- CreateDiscoveryDat method (ScriptContext object), 465
- CreateDynamicVirtualHardDisk method (VirtualServer.Application object), 486
- CreateEvent method (ScriptContext object), 465
- CreateFixedVirtualHardDisk method (VirtualServer.Application object), 486
- CreateFloppyDiskImage method (VirtualServer.Application object), 486
- CreateHostDriveVirtualHardDisk method (VirtualServer.Application object), 486
- CreateParameter method (ADO Command object), 192–193
- CreatePerfData method (ScriptContext object), 465
- CreatePermission method, 410
- CreateScript method (WshController object), 172, 174
- CreateTextFile method, 16–17
- CreateTextFile parameter, 16–17
- CreateVirtualMachine method (VirtualServer.Application object), 486
- CreateVirtualNetwork method (VirtualServer.Application object), 486
- cross-frame security, disabling, 146
- CScript, 7, 21, 61
- CSV XSL file, 335
- CurrentProfile object (Windows Firewall), 362
- CurrentProfileType object (Windows Firewall), 362
- CursorLocation property (ADO Recordset object), 249
- CursorType property (ADO Recordset object), 249
- customizing launch permissions, 163

### D

- DACLs (discretionary access control lists), 240
  - adding ACEs to, 241
  - retrieving, 278
- data, organizing external. See arrays; Dictionary objects
- data return limits, 227–229
- Data Source Names (DSNs). See DSNs (Data Source Names), ODBC
- data sources. See specific data sources
- data types, common values for, 193
- databases, 180
  - Access, as data sources, 196
  - Active Directory as, 248–251
  - adding rows to, 201–202
  - back-end, 196
  - columns, 180
  - connecting to, 181–182
  - querying, 186
  - retrieving all rows/columns from table, 197
  - rows. See rows, database
  - scripting with connection string. See connection strings
  - SQL Server, 196–197
  - stored procedures in, listing all, 194
  - tables. See tables, database
- debugging
  - queries, 196, 197
  - in script editors, 513–514
  - scripts, 134, 473
- decoding scripts, 42
- defining
  - event handlers, for HTML events, 132
  - Windows Script Components (WSCs), 101–102
- Delete method (ADO Recordset object), 190
- DELETE query (SQL), 201
- DeleteVirtualMachine method
  (VirtualServer.Application object), 486
- DeleteVirtualNetwork method
  (VirtualServer.Application object), 486
- deleting
  - database tables, 201
  - Exchange mailbox stores, 445
  - Exchange mailboxes, 452
  - Exchange storage groups, 440–441
  - recordset rows, 190
  - virtual machine configurations, 486
- delimiting
  - Access databases, 196
  - text files, 195
- dependencies, service, 267
- deployed scripts, 171. See also remote scripting
- deployment script, 171
- Description property (Alert object), 471
- description property (XML `<registration>` tag), 98
- `<description>` 标签 (XML), 60, 64, 77
- dialog boxes, adding icons to, 14–15
- Dictionary objects, 23–24
  - Add method, 23
  - and arrays, in same script, 24
  - Count method, 23
  - data storage pages. See keys, dictionary
  - items, 23
  - keys. See keys, dictionary
  - referencing individual items in, 23
  - returning all items in, 23
  - storing data in, 23
  - when to use, 23–24

- differencing disks, 486
- digital certificates. See also code signing
  - certification authorities (CAs). See certification authorities (CAs)
  - certification path, reviewing, 45
  - obtaining, 49
  - self-signed, 49
  - signing scripts with, 49
  - storage location, 49
  - trusted certification authorities (CAs). See certification authorities (CAs)
- digital signatures
  - example of, 50
  - Windows verification of, 43
- directory service scripting interface. See ADSI (Active Directory Services Interface)
- DiscardSavedState method (VirtualMachine object), 493
- DiscardUndoDisks method (VirtualMachine object), 493
- DisconnectObject method, 300
- discovery scripts (Microsoft Operations Manager), 476–478
- DiscoveryCollection object, 477
- DiscoveryData object, 476
- discretionary access control lists (DACLs). See DACLs (discretionary access control lists)
- disk quotas, 364–365
  - default limit, configuring, 365
  - retrieving for user, 364
- DiskState property (ExchangeServerState class), 435
- dismounting Exchange mailbox stores, 443
- displaying full user names, 9
- distinguished names, 27
  - for Exchange routing groups, returning, 435
  - returning for Exchange servers, 435
  - searching by, 429
- distributing HTAs (HTML applications), 127
- distribution lists, 211. See also group accounts
- `<div>` 标签, 144
  - creating dynamic, 144–145
  - innerHTML property, 144
- DLL files, registering, 96
- DN property (ExchangeServerState class), 435
- DNS provider, 365–371
  - class prototype, returning, 370
  - namespace for, 366
  - querying, 370
  - records, creating, 369–370
  - where supported, 365

- DNS records, listing all of single type, 368
- DNS servers
  - clearing cache, 366
  - listing all records of single type, 368
  - performance statistics, accessing, 366
  - properties of, 367
  - record types, class names for, 369
  - root hints, accessing, 366
- documenting named parameters, 65–66
- DOM, 130–131
- domain controllers
  - pending replication jobs, displaying number of, 371
  - validating, 412–413
- domain names, fully qualified (FQDNs), 403
- domains
  - connecting to, 209
  - connecting to root with LDAP provider, 221–222
  - listing all users in, 25
  - listing objects in, 222–225. See also ADSCmd
  - trust relationships, displaying, 372–373
- drives
  - mapped, building list of, 9
  - remote, gathering information on, 33
- drop-down list boxes. See list boxes
- DSNs (Data Source Names), ODBC, 184
  - creating, 182
- DumpToFile method (varSet object), 476
- DVD-ROM drives, adding to virtual machines, 488
- dynamic disks, 488, 496
- dynamic link library (DLL) files, 96
- dynamic messages, displaying in HTAs, 144–145
- dynamic recordsets, 187–188
  - adding records with, 188
  - deleting current row, 190
  - error when opening, 188
  - modifying, 188

### E

- Echo method (ScriptContext object), 465
- editing
  - registry keys, for TrustPolicy, 46–47
  - scripts, in MOM (Microsoft Operations Manager), 466, 478–479
  - scripts, in SAPIEN PrimalScript, 351



### FormatPercent 函数

525

EditMode 属性 (ADO Recordset 对象), 249

编辑器, 513. *另请参阅脚本编辑器*

Enabled 对象 (Windows 防火墙), 363

编码脚本。*另请参阅脚本编码*

脚本编辑器的企业功能, 514–515

实体, 数据库。*另请参阅表, 数据库*

枚举字典键, 23

EnumNetwork 函数, 9

EnumPrint 函数, 9

EOF 属性 (ADO Recordset 对象), 186, 249

Err.Clear 语句, 10

错误检查, 10–11

错误处理, 9–15

- 使用 FileSystemObject 库, 22
- 用于覆写文件, 20

错误消息, 其中显示的项目, 10–11

Error 属性 (WshRemote 对象), 172

事件处理程序

- 分配给按钮, 149–150
- 为 HTML 事件定义, 132

事件日志, 264–265

Event 对象, 471–472

Event 属性 (ScriptContext 对象), 465

事件接收器, 108, 294–300

- 取消, 295, 300
- 创建, 294
- 创建消息框直到运行时, 108–109
- 定义, 313
- 多个, 297

`<event>` 标签 (XML), 98

EventNumber 属性 (Event 对象), 472

事件, 285

- 消费者。*另请参阅消费者*
- 跨多个服务器关联, 474–476
- 在 MOM (Microsoft Operations Manager) 中创建, 471–472
- 为 Windows 脚本组件 (WSC) 定义, 103
- 过滤。*另请参阅过滤; 筛选器*
- 触发, 98, 108
- 用于 HTML 标签, 131
- 用返回参数, 109
- 添加安全权限, 293
- 设置超时参数, 292
- 在 VBScript 中, 173
- 图形化查看, 314
- 在 WBEMTest 中查看属性, 290
- 在 WMI 中, 285–286

EventSource 属性 (Event 对象), 472

eventtriggers.exe, 286

EventType 属性 (Event 对象), 472

Evolved Script Packager (SAPIEN PrimalScript), 172

`<example>` 标签 (XML), 60, 64, 78

Excel, 连接字符串到, 185

Excel 工作簿

- 创建列名, 196
- 作为数据源, 195–196

ExceptionsNotAllowed 对象 (Windows 防火墙), 362

Exchange

- 确定是否不可达, 435
- 创建邮箱报告, 454
- 邮箱存储。*另请参阅邮箱存储, Exchange*
- 邮箱。*另请参阅邮箱, Exchange*
- 创建主报告, 455
- 连接到命名空间, 433
- 在 Active Directory 中查看属性, 428
- 计算公共文件夹消息的总大小, 434
- 服务器。*另请参阅 Exchange 服务器*
- 存储组, 428–429, 436–441
- 查看版本信息, 435
- WMI 类, 432

Exchange 2003 软件开发工具包 (SDK), 下载, 426

Exchange 服务器

- 返回可分辨名称, 435
- 列出域中的所有服务器, 426
- 创建主报告, 455
- 返回 NetBIOS 名称, 435
- 返回路由组可分辨名称, 435
- 查看状态。*另请参阅 ExchangeServerState 类 (WMI)*

Exchange_PublicFolder 类 (WMI), 434

Exchange_Server 类 (WMI), 432–434

ExchangeServerState 类 (WMI), 435, 435–436

Exec 方法, 6, 7

ExecNotificationQuery 方法, 291–292, 293

ExecNotificationQueryAsync 方法, 294. *另请参阅异步通知查询*

Execute 方法 (WshRemote 对象), 173

ExecuteCommand 方法 (GuestOS 对象), 498

执行

- 命令, 6
- 使用 Exec 方法执行 Nslookup 命令, 7
- 脚本。*另请参阅运行脚本*

执行权限, 163, 165–167

导出 IIS 元库, 378–379

扩展权限, 240

外部数据, 组织。*另请参阅数组; Dictionary 对象*

EZ-AD Scriptomatic。*另请参阅 ADSI Scriptomatic*

# F

显示进度反馈, 21

字段, 数据库。*另请参阅列, 数据库*

文件权限, 276–280. *另请参阅权限*

文件

- 关闭, 21
- 记录信息, 20
- 覆写, 错误处理, 20
- 设置文件夹中所有文件的集合对象, 20

FileSystemObject 库, 15, 15–22

FileSystemObject 对象, 163, 176

Filter 属性 (ADO Recordset 对象), 190, 249

过滤

- 使用字符串变量过滤 ADO 查询, 258
- 过滤 ADSI 查询, 251–252
- 使用多个条件过滤 ADSI 查询, 253
- 过滤 LDAP 查询, 227
- 按日志文件过滤查询, 293
- 过滤 SQL 查询, 197–198, 198

筛选器, 287

Find 方法 (ADO Recordset 对象), 190

查找 GPO 备份, 413

FindVirtualMachine 方法 (VirtualServer.Application 对象), 486

FindVirtualNetwork 方法 (VirtualServer.Application 对象), 486

FirewallEnable 对象 (Windows 防火墙), 362

防火墙。*另请参阅 Windows 防火墙*

触发事件, 98, 108

标志, 检查状态, 277

在 HTA 中显示平面滚动条, 142

文件夹

- 设置文件夹中所有文件的集合对象, 20
- 验证路径, 19

For...Each...Next 循环, 20

FormatPercent 函数, 21

526 格式化 WMIC (WMI 命令行) 输出

- 格式化 WMIC (WMI 命令行) 输出, 334-335

只进记录集, 186

FQDN (完全限定域名), 403

框架, HTML。*另请参阅内联框架*

清理 FrontPage 代码, 147

显示完整用户名, 9

完全限定域名 (FQDN), 403

函数。*另请参阅特定函数*

- 添加到 HTA, 151-152
- 通过函数计算 Windows 脚本组件属性, 106
- 指定内部名称, 107
- 重用, 63

# G

- 连接到 GC (全局编录), 228

GenerateReportToFile 方法 (GPO 对象), 411

GetConfigurationValue 方法 (VirtualServer.Application 对象), 487

GetDVDFiles 方法 (VirtualServer.Application 对象), 487

GetFloppyDiskFiles 方法 (VirtualServer.Application 对象), 487

GetFloppyDiskImageType 方法 (VirtualServer.Application 对象), 486

GetHardDisk 方法 (VirtualServer.Application 对象), 486

GetHardDiskFiles 方法 (VirtualServer.Application 对象), 487

GetOverride 方法 (ScriptContext 对象), 465

GetProfileByType 对象 (Windows 防火墙), 362

GetScriptState 方法 (ScriptContext 对象), 465

GetSecurityInfo 方法 (gpmGPO 对象), 407

GetVirtualMachineFiles 方法 (VirtualServer.Application 对象), 487

GetVirtualNetworkFiles 方法 (VirtualServer.Application 对象), 487

全局编录 (GC), 连接到, 228

- GloballyOpenPorts 对象 (Windows 防火墙), 362

gmpRSOP 对象参数, 413-414

GPM 对象, 实例化, 396, 403

GPMC (组策略管理控制台)

- 常量, 列表, 397-403
- 对象模型, 394-396
- 要求, 394
- 策略的结果集 (RSOP), 413-414
- 管理范围 (SOM), 405-406
- 脚本编写, 394, 396, 403-404

GPMConstants 对象, 实例化, 396, 403

gpmGPO 对象, 407

GPO (组策略对象)。*另请参阅组策略对象 (GPO)*

图形脚本应用程序。*另请参阅 HTA (HTML 应用程序)*

HTA 中的图形, 151

组帐户

- 创建, 211
- 设置类型, 211

使用 ADO 和 ADSI 测试组成员身份, 256-259

组策略管理控制台 (GPMC)。*另请参阅 GPMC (组策略管理控制台)*

组策略对象 (GPO)

- 备份, 412, 413
- 列出所有, 403-404, 419
- 生成主文档, 414
- 创建权限对象, 410
- 权限, 407-410
- 显示首选项, 49
- 报告, 411
- 还原脚本, 412-413
- 检索信息, 419
- 检索 SOM 链接, 419

GroupDN 属性 (ExchangeServerState 类), 435

GuestOS 对象, 497-498

GuestOS 属性 (VirtualMachine 对象), 494

GUID, 97, 241

# H

- 处理错误。*另请参阅错误处理*

HardDisk 对象, 496-497

虚拟机上的硬件, 485

head 方法, 123

`<head>` 标签 (HTML), 141

向脚本添加帮助信息, 77-78

hform XSL 文件, 335

- 隐藏

    - 在 HTA 中隐藏最大化按钮, 142
    - 在 HTA 中隐藏最小化按钮, 142
    - 在 HTA 中隐藏滚动条, 142
    - 在 WBEMTest 中隐藏系统属性, 343
    - 窗口, 6

HNetCfg 库, 362-363

Hnetcfg.dll, 360

HNetCfg.FwMgr 对象, 359

家庭网络配置库, 362-363

HTA Helpomatic, 140

HTA 标签, 141

htable XSL 文件, 335

HTA (HTML 应用程序)

- 属性, 141-143. *另请参阅特定属性*
- 定义边框, 141
- 构建, 132
- 按钮, 149
- 复选框, 150
- 关闭上下文菜单, 142
- 将 HTML 转换为 HTA, 153
- 自定义外观, 126
- 调试, 133, 134
- 指定默认窗口状态, 143
- 在 HTA 中显示动态消息, 144-145
- 在 Windows 任务栏中显示, 143
- 分发, 127
- 从 Internet 下载, 126
- 在 HTA 中引用外部文件, 152
- 文件名扩展名关联, 126
- 在 HTA 中使用框架, 146
- 添加函数, 151-152
- 指定目标, 134
- 添加图形, 151
- HTA 标签, 141
- HTML 与 HTA, 128
- 在 HTA 中设置超链接以打开新窗口, 142
- 显示内部边框, 142
- 在 HTA 中使用交互元素, 129
- 限制为单实例, 143
- 用列表框填充数据, 148
- 隐藏最大化/最小化按钮, 142
- HTA 的模块化, 138
- 在框架中显示输出, 146
- 单选按钮, 150
- 设置右键单击行为, 142
- 自定义滚动条, 142
- 安全绕过功能, 126
- HTA 的安全性, 128
- 调整大小, 143-144
- 添加子程序, 151-152



### 邮箱存储，Exchange 527

- 系统菜单，显示，143
- 允许在其中选择文本，143
- 设置标题栏文本，142
- 设置版本号，143
- 与网页的对比，141
- 窗口图标，127，142

#### HTML

- 转换为 HTA，153
- 在其中显示脚本输出，136
- 框架，146
- 层级结构，130-131
- 嵌套标签。*另请参阅* DOM
- 渲染引擎，128
- 子程序命名，132
- 将 WMIC 输出格式化为表格，335
- 标签。*请参阅* 标签，HTML
- 文本框，147
- 空白，129

#### HTML 应用程序。*请参阅* HTA（HTML 应用程序）

#### HTML 事件，为其定义事件处理程序，132

#### HTA 中的超链接，设置为打开新窗口，142

- 模拟，指定级别，274
- ImpersonationLevel 属性（SwBemSecurity 对象），274
- 缩进，由脚本编辑器自动完成，506-507
- 内联框架，146
- innerborder 属性（HTA），142
- `<input>` 标签（HTML），129
- InputBox 函数，12。*另请参阅* MsgBox 函数

#### INSERT 查询（SQL），201-202

- 提供列值，202
- 数据类型错误，202

- InstallAdditions 方法（GuestOS 对象），497
- 已安装的服务，依赖关系，267

### 安装

- 打印机驱动程序，383-384
- SNMP 提供程序，用于 WMI，356
- WMIC（WMI 命令行），325

- InstancesOf 方法，30
- 内部证书颁发机构（CA），49

### Internet Explorer 文档对象模型（DOM），130-131

### Internet Explorer 渲染引擎，128

### Internet Information Services (IIS) 6.0。*请参阅* IIS（Internet Information Services 6.0）

- IpVersion 对象（Windows 防火墙），363
- ISA 运算符（WQL），287
- IsAlert 方法（ScriptContext 对象），465
- IsEvent 方法（ScriptContext 对象），465
- IsHeartBeating 属性（GuestOS 对象），497
- IsPerfData 方法（ScriptContext 对象），465
- IsTargetAgentless 属性（ScriptContext 对象），465
- IsTargetVirtualServer 属性（ScriptContext 对象），465
- 字典条目，返回所有，23
- iTriopoli AdminScriptEditor，172

### K

- Kerberos 身份验证，342
- Keyboard 属性（VirtualMachine 对象），494
- 键盘快捷键，507，508
- 字典键，23
- Keys 方法，23
- KiXtart，38

### L

- language 属性（`<script>` 标签），62
- lanmanserver 服务，230
- 自定义启动权限，163
- 使用 WshShell 对象启动程序，5

#### 检索 LDAP 对象路径，254

#### LDAP 提供程序，25

- 大小写敏感性，25
- 使用其连接到根域，221-222

#### LDAP 查询

- 从 ADSIDump 文件，225
- 过滤，227
- 限制，227
- 测试，222

- Level 属性（Alert 对象），470-471
- 库，FileSystemObject，15-22
- 外部引用库脚本，94

#### WQL WHERE 子句中的 LIKE 运算符，265-267

- 返回数据的限制。*请参阅* 数据返回限制

#### 列表框

- `<option>` 标签，148
- 在 HTA 中填充，148
- 滚动，148

- LoadDriver 安全特权，激活，384
- 列出所有本地用户账户，261
- LocalPolicy 对象（HNetCfg 库），362
- LockType 属性（ADO Recordset 对象），249

#### 日志文件，20

- 按日志文件过滤查询，293
- 用于跟踪，473
- 验证，19

- 登录脚本，使用其远程修改用户配置文件，170
- 循环脚本，15-16，315

### I

- IcmpSettings 对象（Windows 防火墙），362
- icon 属性（HTA），142
- HTA 窗口的图标，127
- id 属性（HTML 标签），131
- id 属性（`<object>` 标签），62
- id 属性（XML `<component>` 标签），97
- id 属性（XML `<resource>` 标签），99
- 身份验证与远程脚本，165
- `<iframe>` 标签，146
- IFrame。*请参阅* 内联框架

#### IIS 类，显示读/写设置，375

#### IIS（Internet Information Services 6.0），374-380

- 管理脚本，379
- 在脚本中整合命令行字符串，379
- 使用其配置网站，377
- 连接到命名空间，375
- 使用其创建网站，375-378
- 备份元数据库，378-379
- 检索元数据库路径，377
- 命名空间，374
- 命名空间中的类，374-375
- 查询虚拟目录，374-376
- XML 配置元数据库，374

- IisWebVirtualDirSetting 类（WMI），377
- `<img>` 标签（HTML），151

### J

- `<job>` 标签（XML），59
- Windows 脚本文件（WSF）中的作业，59

#### JOIN 子句（SQL），199-200

- JScript，37

### M

#### 邮箱存储，Exchange

- 连接到，443
- 创建，443-445
- 在其中创建邮箱，447
- 删除，445
- 卸载，443
- 显示属性信息，443
- 列出所有，430，441-442
- 列出可用存储，449-450
- 装载，445
- 设置 URL，445

#### 邮箱，Exchange

- 创建，447
- 删除，452
- 枚举属性，452-454
- 移动，450
- 查询多个，454

- ManagementGroupName 属性（ScriptContext 对象），465
- 映射驱动器，9
- 映射打印机，9
- MarshalOptions 属性（ADO Recordset 对象），249
- 匹配校验和，43
- 在 HTA 中隐藏最大化按钮，142
- maximizebutton 属性（HTA），142
- 最大数据返回限制。*请参阅* 数据返回限制
- MaxRecords 属性（ADO Recordset 对象），190，249
- Memory 属性（VirtualMachine 对象），494
- MemoryState 属性（ExchangeServerState 类），435
- Merge 方法（HardDisk 对象），496
- MergeTo 方法（HardDisk 对象），497
- MergeUndoDisks 方法（VirtualMachine 对象），493
- 合并虚拟机撤消磁盘，493
- 显示消息框。*请参阅* MsgBox 函数
- Message 属性（Event 对象），472
- 用户消息，9

#### 元数据库，IIS

- 备份，378-379
- 检索路径，377

#### 方法。*另请参阅* 具体方法

- 在 ADSI 记录中，250-251
- 用于 COM 对象，96
- 在 Windows 脚本组件（WSC）中，102，107

#### Microsoft Access

- 连接字符串，185
- 使用 SQL JOIN 子句创建查询，200
- 数据库，196。*另请参阅* 数据库

#### Microsoft Excel，连接字符串，185

#### Microsoft Excel 工作簿

- 创建列名，196
- 作为数据源，195-196

#### Microsoft Exchange 2003。*请参阅* Exchange

#### 清理 Microsoft FrontPage 代码，147

#### Microsoft OLE DB Provider for Microsoft Active Directory Service，246-247

#### Microsoft Operations Manager (MOM)。*请参阅* MOM（Microsoft Operations Manager）

#### Microsoft Script Encoder，42。*另请参阅* 脚本编码

#### Microsoft SQL Server。*请参阅* SQL Server

#### Microsoft Virtual Server 2005。*请参阅* Virtual Server

#### Microsoft Windows Script Host。*请参阅* Windows Script Host (WSH)

- MicrosoftDNS_Domain 类（WMI），366
- MicrosoftDNS_RootHints 类（WMI），366
- MicrosoftDNS_Server 类（WMI），366
- MicrosoftDNS_Statistic 类（WMI），366
- MicrosoftDNS_Zone 类（WMI），366
- Microsoft_DomainTrustStatus 类（WMI），373
- Microsoft_LocalDomainInfo 类（WMI），372
- 在 HTA 中隐藏最小化按钮，142
- minimizebutton 属性（HTA），142
- 脚本模块化，140

#### MOM（Microsoft Operations Manager）

- 创建警报，470-471，481
- 返回计算机属性信息，476-478
- 使用其调试脚本，473
- 在其编辑脚本，466
- 创建事件，471-472
- 插入代码，466
- PerfData 对象，468
- 创建性能数据，468
- 生成性能图，470
- 创建性能对象，482
- ScriptContext 脚本宿主。*请参阅* ScriptContext
- 脚本编写，464，466
- 脚本，466-467，473-479，481
- 定时脚本，474

##### 监视事件

- 按日志文件过滤，293
- 查询。*请参阅* 通知查询

- 装载 Exchange 邮箱存储，445
- Mouse 属性（VirtualMachine 对象），494

#### MoveFirst 语句（ADO），186

#### MoveLast 语句（ADO），186

#### MoveNext 语句（ADO），186

#### MovePrevious 语句（ADO），186

- 移动 Exchange 邮箱，450
- MSAD_DomainController 类（WMI），372
- MSAD_ReplNeighbor 类（WMI），372
- MSAD_ReplPendingOp 类（WMI），371
- MSDN Library，355

#### MsgBox 函数，13-15。*另请参阅* InputBox 函数

- 按钮选项，13，14
- 包含对话框图标，14-15

#### Mshta.exe，125-126，126。*另请参阅* HTA（HTML 应用程序）

### N

- Name 属性（Alert 对象），470-471
- Name 属性（ExchangeServerState 类），435
- Name 属性（ScriptContext 对象），465

#### 命名参数，65-67

- 编写文档，65-66
- helpstring 属性，65-66
- name 属性，65
- 其中的引号，65
- required 属性，66-67
- type 属性，66

#### `<named>` 标签（XML），61

- 属性，65-67
- 语法，65

#### 命名空间

- 连接到。*请参阅* 连接到命名空间
- 用于 DNS 提供程序，366
- IIS（Internet Information Services 6.0），374-375
- 权限，166
- WMI，连接到，30，321

#### 命名

- Exchange 存储组，439
- 内部函数，107
- Windows 脚本组件（WSC）中的方法，107
- 子程序，132

- navigable 属性（HTA），142
- 在活动目录浏览器（ADSVW）中导航，218
- 使用 ADO 和 ADSI 测试嵌套组成员身份，256-259
- 嵌套 HTML 标签，130。*另请参阅* DOM



NetBIOS 名称，从 Exchange 服务器返回，435
网络适配器，连接到虚拟机，489
网络 ping 命令，356-359
记事本，脚本编写，505
通知查询，286-287
- 异步，294
  - 在 WBEMTest 中创建，288-291
  - 半同步，291-294
NotificationDisabled 对象（Windows 防火墙），362
Nslookup 命令，7

### O

对象允许权限，241
对象模型，虚拟服务器，486-487
<object> 标签（XML），61-62
对象
- 类信息，检索，211
- 消费者。请参阅消费者
- 创建，61-62、78、210-211
- 字典。请参阅字典对象
- 可分辨名称，27、429
- GuestOS，497-498
- 列出域中的所有对象，220-225
  - 在组织单位（OU）中查看，222
- PerfData，468
- 属性，检索，211
- 远程脚本，171
- 检索信息，211
- 设置属性，27
- SWbemLocator。请参阅 SWbemLocator 对象
- 类型库。请参阅类型库
- 虚拟服务器，获取引用，491
- Winmgmts，30-31
- WshNetwork，8
- WshShell。请参阅 WshShell 对象
ODBC（开放数据库连接）
- DSN，创建，182
OnCompleted 事件（WMI），295
onLoad 事件（窗口对象），用于调整 HTA 大小，143-144
OnObjectPut 事件（WMI），295
OnObjectReady 事件（WMI），295
OnProgress 事件（WMI），295
OnScript，172，517
开放数据库连接（ODBC）
- DSN，创建，182
开放防火墙端口，列出，359
Open 方法（ADO Recordset 对象），187
打开文本文件，15-16，176
OpenTextFile 方法，15-16，16

选项按钮。请参阅单选按钮
<option> 标签，148
ORDER BY 子句（SQL），199
- 与 TOP 子句结合使用，198
- 默认排序顺序，199
组织单位（OU）
- 授予权限，242-243
- 查看其中的对象，222
组织外部数据。请参阅数组；字典对象
OSName 属性（GuestOS 对象），497
覆盖 TrustPolicy 每用户设置，47
覆盖文件，16-17，20
Owner 属性（Alert 对象），471

### P

<package> 标签（XML），59
打包脚本，516-517。请参阅 Windows 脚本文件（WSF）
数据包，单独验证，274
PageCount 属性（ADO Recordset 对象），250
PageSize 属性（ADO Recordset 对象），250
Parameters 属性（ScriptContext 对象），465
参数，运行时。请参阅运行时参数
密码框（HTML），147。另请参阅文本框（HTML）
密码
- 管理员，26
- 在连接字符串中避免使用，185
- IIS 元数据库备份，378
- 安全，26
- 为用户指定，27
Pause 方法（VirtualMachine 对象），493
暂停
- 打印队列，381
- 虚拟机，493
显示完成百分比，21
PerfData 对象，468
PerfData 属性（ScriptContext 对象），465
MOM（Microsoft Operations Manager）性能计数器，468-470
性能统计信息，访问，366
Perl，37
永久消费者，286。另请参阅消费者
权限。另请参阅文件权限
- 用于操作。请参阅扩展权限
- ADSI（Active Directory 服务接口）和，167
- 为远程脚本访问配置，163-165
- 连接性，163
- 执行，165-167
- 用于 GPO，407-410
- 启动，自定义，163
- 在命名空间上，166
- 对象允许，241
- 用于组织单位（OU），242-243
- 远程脚本和，163-165
执行 ping 命令，356-359
在连接到远程系统之前 ping 计算机，357
<pkg> 标签（XML），97
策略与首选项，49
轮询，287-288
在 HTA 中填充列表框，148
Popup 方法
- 参数，5
- WshShell 对象，4-5
弹出窗口
- 自动关闭。请参阅 Popup 方法
- 需要单击按钮才能关闭，13
- 脚本编写。请参阅 Popup 方法
在 Windows 防火墙中打开的端口，361
首选项与策略，49
PressAndReleaseKey 方法（Keyboard 对象），498
PressKey 方法（Keyboard 对象），498
阻止软件运行。请参阅软件限制策略（SRP）
PrimalScope，514
PrimalScript。请参阅 SAPIEN PrimalScript
主要用户，Windows 中不存在，168
打印设备，检索功能，382
打印队列
- 取消所有作业，381-382
- 暂停，381
- 重定向，383
- 恢复，381
打印机驱动程序，安装，383-384
打印机端口，修改，383
打印机，列出映射的，9
权限
- 在 WBEMTest 中启用，341
- 在 WMI 中启用，275-276
- 安全，列表，275-276
- 用户，32

Privileges 属性（SwBemSecurity 对象）
- 权限，529
- Privileges 属性（SwBemSecurity 对象），275-276
- ProcessingRule 属性（ScriptContext 对象），465
- Profile 对象（HNetCfg 库），362
- progid，95-96
- progid 属性（<object> 标签），62
- progid 属性（XML <registration> 标签），97
- 程序，使用 WshShell 对象启动，5
- 进度反馈，显示，21
- Provider 属性（ADSI）与 ConnectionString 属性，247
- 配置，488-489，490
- 公用文件夹消息，计算总大小，434
- 公钥加密，43
- <public> 标签（XML），98
- Python，38

### Q

查询
- ADO，使用字符串变量过滤，258
- ADSI。请参阅 ADSI 查询
- 关联，268-272
- 异步，身份验证级别，302
- 调试，196，197
- 用于事件通知。请参阅通知查询
- 在 WBEMTest 中执行，343
- 按日志文件过滤，293
- LDAP，222
- 限制。请参阅数据返回限制
- 多个，297
- 通知。请参阅通知查询
- 引用，273
- 返回特定属性，262-263
- Select，31-32
- SQL。请参阅 SQL 查询
- 在字符串变量中，248
- 测试，343。另请参阅 WBEMTest
- 验证，343。另请参阅 WBEMTest
- 在 WBEMTest 中执行，343
- Windows Management Instrumentation（WMI）。请参阅 WMI 查询
- 编写高效查询，263
查询
- Active Directory，427，428，431-432
- 数据库，186
- DNS 提供程序，370
- Exchange 邮箱存储，在 Active Directory 中，430
- IIS 虚拟目录，374-376
- MSAD_DomainController 类，372
QueueState 属性（ExchangeServerState 类），435
Quit 方法（ScriptContext 对象），465

### R

单选按钮，设置默认选项，150
RAWXML XSL 文件，335
读/写权限，分配给 Windows 脚本组件属性，106
使用 WshShell 对象读取注册表，5
读取文本文件，15-16
ReadLine 方法，16
记录查询限制。请参阅数据返回限制
RecordCount 属性（ADO Recordset 对象），189，250
记录，数据库。请参阅行，数据库
记录，DNS
- 创建，370
- 列出所有单一类型，368
Recordset 对象（ADO），185-186。另请参阅 recordset
- Bookmark 属性，190
- Delete 方法，190
- EOF 属性，186
- Filter 属性，190
- Find 方法，190
- MaxRecords 属性，190
- 使用 Command 对象打开，192
- 属性，在 ADSI 连接中，249-251
- RecordCount 属性，189
- Sort 属性，190
- State 属性，190
- Supports 方法，190
recordset。另请参阅 Recordset 对象（ADO）
- 在记录中设置书签，190
- 检查功能，190
- 检查是否为空，189
- 检查是否打开，190
- 关闭，187
- 从连接表创建，使用 SQL 查询，200
- 定义，185
- 动态。请参阅动态 recordset
- 提取数据，187
- 查找匹配记录，190
- 仅向前，186
- 支持的方法，250-251
- 指针，移动，186
- 静态，189

重定向打印作业，383
reference 属性（<object> 标签），62
引用查询，273
区域，定义，518
注册
- Active Directory 架构管理单元，251
- DLL 文件，96
- 过滤器，与消费者，305
- Windows 脚本组件（WSC），97-98，121
- WScript 对象，作为错误修复，174
RegisterVirtualMachine 方法（VirtualServer.Application 对象），486
RegisterVirtualNetwork 方法（VirtualServer.Application 对象），486
<registration> 标签（XML），97-98
注册表
- 使用远程脚本修改，169
- 使用 WshShell 对象读取，5
- 注册表项，编辑，46-47
关系，在 CIM Studio 中查看，346
ReleaseKey 方法（Keyboard 对象），498
释放 WshRemote 对象，176
远程管理，为 Windows 防火墙启用，360
远程脚本。另请参阅已部署的脚本
- ADSI 查询，163
- 使用备用凭据获取访问权限，165
- 为 Windows 防火墙配置，170
- 为配置权限，163-165
- 连接，类型，163
- 连接性和，162-165
- 上下文和，167-170
- 已部署脚本，171
- 部署脚本，171
- 执行权限，165-167
- FileSystemObject 查询，163
- 身份和，165
- 为设计的对象。请参阅远程脚本对象
- 权限，163-165
- 注册表，使用其修改，169
- 使用 RunAs 命令，165
- 脚本编辑器和，516-517
- 涉及的脚本，171
- 安全性和，167
- 安全上下文和，162
- 安全层和，166
- 用于远程脚本的第三方应用程序，172
- 用户配置文件和，167-170
- WMI 查询，163



远程脚本对象，171。*另见* WshController 对象
远程关机，授予权限，32
远程属性（XML `<registration>` 标签），98
RemoteAddresses 对象（Windows 防火墙），363
RemoteAdministration 对象（Windows 防火墙），363
RemoteAdminSettings 对象（Windows 防火墙），362
RemoveConfigurationValue 方法（VirtualServer.Application 对象），487
从受信任列表中移除证书颁发机构（CA），45
报告，为 GPO 编写脚本，411
RequiredAssocQualifier=qualifier 关键字（ASSOCIATORS OF 查询），272
RequiredQualifier=qualifier 关键字（ASSOCIATORS OF 查询），272
表单中的重置按钮，为何不使用，149
Reset 方法（VirtualMachine 对象），493
ResolutionState 属性（Alert 对象），471
资源 ID，大小写敏感性，64
`<resource>` 标签（XML），63-64，99
响应脚本（Microsoft Operations Manager），473
RestoreGPO 方法（gpmDomain 对象），412-413
还原，GPO，411-413
限制 Select 查询，31-32
限制软件。*见* 软件限制策略（SRP）
Result 方法（gpmResult 对象），412
策略结果集（RSOP），413-414
ResultClass=classname 关键字（ASSOCIATORS OF 查询），272
Resume 方法（VirtualMachine 对象），493
恢复打印队列，381
重用代码。*见* Windows 脚本组件（WSC）
重用函数/子程序，63
右键单击 HTA 时设置行为，142
回滚虚拟机，498-500

行，数据库
- 添加，201-202
- 添加（使用动态记录集），188
- 更改数据，201
- 定义，181

RSOP（策略结果集），413-414

运行时参数
- 布尔型，77
- 命名参数。*见* Popup 方法的命名参数，5
- 使用 Windows 脚本文件（WSF）指定，61，65
- 验证，68
Windows 脚本文件（WSF）与，61，65

运行时语法，验证，64

RunAs 命令
- 使用替代凭据，52
- 远程脚本，165
- 语法，52

运行脚本
- 使用替代凭据。*见* 替代凭据
- 使用 CScript，7
- 阻止。*见* 软件限制策略（SRP）
- 作为服务，317
- 仅受信任，46
- 请求用户输入，11-12
- 在用户的安全上下文下，170

运行 WBEMTest，268
`<runtime>` 标签（XML），60

**S**

SAM（安全账户管理器）
- 名称，设置，210

sAMAccountName，25

SAPIEN PrimalScript，51，172
- 添加方法/属性，115
- 创建脚本，350
- 创建 Windows 脚本组件（WSC），112-117
- 创建 Windows 脚本文件（WSF），68-72
- 调试，514
- 编辑脚本，351
- 远程脚本执行引擎（RSEE），517
- 代码片段，508-509
- WSC 支持，518
- WSF 支持，518

SAPIEN PrimalScript Professional，225-226
Save 方法（VirtualMachine 对象），493

扫描事件日志，264-265
计划任务，使用替代凭据运行，53

架构管理单元（Active Directory），注册，251
Schtasks 命令，53
作用域筛选器，477
Scope 对象（Windows 防火墙），363
管理范围（SOM），405-406

脚本组件向导，101-105
- 下载，100
- 位置，101

脚本组件，Windows。*见* Windows 脚本组件（WSC）

脚本编辑器，38
- 块格式化，518
- 大小写更正，506
- 代码补全，509-510
- 代码提示，509-510
- 调试，513-514
- 下载，519
- 企业功能，514-515
- 可扩展性，513
- 包含的功能，506-507
- 缩进，506-507
- PrimalScript Professional，225-226
- 远程脚本，516-517
- SAPIEN PrimalScript。*见* SAPIEN PrimalScript
- 安全功能，515-516
- 快捷方式，507
- 代码片段，508-509
    - 用于 Windows 脚本文件（WSF），68-72
- 向导，510-513
    - 用于 XML，68-72

脚本编码，41-42。*另见* Microsoft 脚本编码器
- 解码工具，42
- 局限性，42
- 安全性，42

脚本作业（Windows 脚本文件），62-63
脚本库，添加，94

脚本安全
- 代码签名。*见* 代码签名
- 删除 wscript.exe/cscript.exe，无效性，41
- 为脚本编码。*见* 脚本编码
- 重新分配文件扩展名，无效性，41
- 对代码签名。*见* 代码签名
- 软件限制策略（SRP）与，52

脚本签名。*见* 代码签名
`<script>` 标签（XML），62，98
脚本跟踪，473
ScriptContext，465-466

## 532 脚本

脚本
- Exchange 存储组，436-441
- ExchangeServerState 类（WMI），435-436
- 扩展权限，240
- GPO 备份，412
- GPO 权限，407-410
- GPO 报告，411
- GPO 还原，412-413
- MOM（Microsoft Operations Manager）。*见* MOM（Microsoft Operations Manager）；ScriptContext
- 在 Notepad 中，505
- 远程。*见* 远程脚本
- RSOP（策略结果集），413-414
- 安全，240
- Windows 防火墙，与组策略，360

Scriptomatic，126-128。*另见* ADSI Scriptomatic
- 使用连接到 WMI 命名空间，321
- 保存脚本，325
- 选择脚本输出格式，323
- 启动，320
- 显示 WMI 类，320

脚本
- 中止，20，292
- 添加作用域筛选器，477
- 添加到 MOM（Microsoft Operations Manager），466
- 用于更改管理员密码，26
- 使用更改 HTML 标签，131
- 颜色编码，38
- 将按钮连接到，149-150
- 使用替代凭据连接到远程系统，33
- 转换为 Windows 脚本文件（WSF），72-79
- 使用创建网站，375-378
- 调试，134，473
- 在其中定义区域，518
- 已部署，171
- 目录服务接口。*见* ADSI（Active Directory 服务接口）
- 在 HTML 中显示输出，136
- 在 MOM（Microsoft Operations Manager）中编辑，466
- 在 SAPIEN PrimalScript 中编辑，351
- 错误处理。*见* 错误处理
- 检查错误状态，137
- 执行。*见* 运行脚本
- 图形输入选项。*见* InputBox 函数
- 设置帮助信息，65-66
- 循环，15-16
- 用于管理用户/组。*见* ADSI（Active Directory 服务接口）
- 模块化，140
- 在 MOM（Microsoft Operations Manager）中，467，473-478，478-479，481
- 用于打开文本文件。*见* 打开文本文件
- 打包，516-517。*见* Windows 脚本文件（WSF）
- 显示进度反馈，21
- 用于预配置，490
- 远程。*见* 远程脚本
- 作为对 MOM（Microsoft Operations Manager）事件的响应，473
- 具有健壮用户界面的。*见* HTA（HTML 应用程序）
- 运行。*见* 运行脚本
- 在 Scriptomatic 中保存，325
- 脚本的安全性。*见* 脚本安全
- 跨会话存储信息。*见* ScriptState 对象
- 在其中存储状态变量，474-476
- 技术，决定使用适当的技术，39
- 与 Microsoft Operations Manager（MOM）事件定时运行，474
- 受信任的，46
- 不受信任的，设置警告消息，47
- 创建用户消息，9
- 验证输入，12
- 用于虚拟机管理，492-496
- 包装器，354-355
- 将结果写入命令窗口，21

Scripts 文件夹，394
ScriptState 对象，474，476
scroll 属性（HTA），142
HTA 中的滚动条，隐藏/显示，142
scrollflat 属性（HTA），142
SDK（ADSI 软件开发工具包），217。*另见* ADSCmd；ADSVW
LDAP 查询上的搜索筛选器，227
SearchBackups 方法（gpmBackupDir 对象），413

搜索
- Active Directory，257
- CIM Studio，用于 WMI 类，345

安全
- 跨框架，禁用，146
- HTA（HTML 应用程序）的安全性，126，128
- 权限列表，275-276
- 远程脚本，167
- 脚本编辑器中的，515-516
- 脚本安全，240
- 脚本。*见* 脚本安全
- Windows 脚本组件（WSC），98

安全账户管理器（SAM）
- 名称，设置，210

安全上下文，162
安全组，211。*另见* 组账户
安全层，166
Security_ 属性（SWbemLocator 对象），274-276
Select Case 语句，11
SELECT * FROM Users 语句，为何不推荐使用，186
Select 查询，限制，31-32
SELECT 查询（SQL），197
selection 属性（HTA），143
自签名证书，49
半同步通知查询，291-294
Server 服务，连接到，230
服务器，Exchange。*见* Exchange 服务器
ServerState 属性（ExchangeServerState 类），435
服务依赖项，267

服务
- 作为服务运行脚本，317
- 在 WBEMTest 中停止，290

Services 对象（Windows 防火墙），362
SetConfigurationValue 方法（VirtualServer.Application 对象），487
SetInfo 方法，26
SetPassword 方法，26，27
showintaskbar 属性（HTA），143
ShowUsage 方法，64
- 括号参数，67
- 可选参数，67
- 设置显示的文本，65-66

ShutDown 方法（GuestOS 对象），498
关机，远程，32
对脚本签名。*见* 代码签名
简单网络管理协议（SNMP），356
singleinstance 属性（HTA），143
接收器。*见* 事件接收器
Sleep 方法（ScriptContext 对象），465
代码片段，508-509
SNMP（简单网络管理协议），356



# 信任策略

软件限制策略（SRP），52
排序属性（ADO Recordset 对象），190
源代码管理软件，515
Source 属性（ADO Recordset 对象），250
\<span\> 标签，144–145
Split 函数，22
SQL
    大小写敏感性，197
    JOIN 子句。参见 JOIN 子句（SQL）
    ORDER BY 子句。参见 ORDER BY 子句（SQL）
    查询。参见 SQL 查询
    SELECT * FROM Users 语句，为何不推荐使用，186
    TOP 子句，198–199
    WHERE 子句，197–198
SQL 查询
    合并两个表的数据。参见 JOIN 子句（SQL）
    从连接表创建记录集，200
    DELETE，201
    INSERT，201–202
    包含 JOIN 子句的查询中，列名前缀，200
    限制返回的行数，197–198
    返回特定数量/百分比的行，198–199
    字符串字面值，大小写敏感性，249
    UPDATE，201
SQL Server
    连接字符串，185
    数据库作为数据源，196–197
    ODBC DSN 向导，183
SRP（软件限制策略），52
Startup 方法（VirtualMachine 对象），493
State 属性（ADO Recordset 对象），190，250
State 属性（VirtualMachine 对象），494–495
状态变量脚本（MOM），474–476
静态记录集，189
Status 属性（ADO Recordset 对象），250
Status 属性（WshRemote 对象），172
StdOut 方法（Wscript 对象），21
在 WBEMTest 中停止服务，290
存储组，Exchange
    绑定到服务器，439
    创建，438–440
    删除，440–441
    列出，437–438
    列出所有，428–429
    命名，439
    属性，438
    保存，440
    脚本编写，436–441
    查看完整 URL，439
存储过程
    Command 对象与，192
    定义，191–192
    列出数据库中所有存储过程，194
    参数化，192
    字符串字面值，大小写敏感性，249
字符串变量
    使用字符串变量过滤 ADO 查询，258
    在字符串中进行查询，248
Submit 方法（ScriptContext 对象），465
子程序
    添加到 HTA 中，151–152
    常用子程序，在外部文件中循环，152
    使用子程序处理 VBScript 事件，173
    命名，132
    重用，63
Supports 方法（ADO Recordset 对象），190
挂起虚拟机，493
SWbemLocator 对象，32–33
    创建，32
    ImpersonationLevel，设置，32
    用户权限，设置，32
    与 winmgmts 的比较，273
对称密钥，42
sysmenu 属性（HTA），143
系统属性，在 WBEMTest 中隐藏，343

# T

表，数据库，180
    删除，201
    连接表，使用 SQL 查询创建记录集，200
    检索所有行/列。参见 SELECT 查询（SQL）
表，HTML，将 WMIC 输出格式化为表格，335
标签，HTML。另见特定标签
    使用脚本更改，131
    children 集合，130
    标签的事件，131
    层次结构，130–131
    id 属性，131
    innerHTML 属性，130
    嵌套标签，130。另见 DOM
    parentElement 属性，130
    作为可编程对象，130–131
    用于编辑标签的所见即所得编辑器，147
标签，XML。另见特定标签
    闭合标签，58
    在 WSC 文件中，97–99
    tail 方法，123
    TargetComputer 属性（ScriptContext 对象），465
    TargetComputerIdentity 属性（ScriptContext 对象），465
    TargetFQDNComputer 属性（ScriptContext 对象），466
    TargetNetbiosComputer 属性（ScriptContext 对象），466
    任务计划程序，53
    计划任务，53
    临时使用者。参见使用者
    Terminate 方法（WshRemote 对象），173
测试
    ADO，用于测试组成员资格，256–259
    LDAP 查询，222
    查询，343。另见 WBEMTest
testvaluelist XSL 文件，335
文本区域（HTML），147
文本框（HTML），147
文本文件
    关闭，16
    连接字符串，185，195
    创建，16–17
    作为数据源，195
    分隔符，195
    打开，15–16，16，176
    覆盖先前版本，16–17
    读取，15–16
定时脚本（Microsoft Operations Manager），474
TOP 子句（SQL），198–199
跟踪脚本，473
转换文件。参见 XSL 文件
故障排除
    GPO 备份，412
    ScriptState 对象，476
    WshController 对象，174
信任提供程序，Active Directory，373–374
受信任的证书颁发机构（CA），44
    信任的含义，45
    从列表中移除，45
受信任的脚本，46
信任策略，5。另见代码签名
    管理模板，47
    计算机范围设置，46–47
    使用组策略配置，47–49
    默认设置，46
    启用/禁用，47
    覆盖每用户设置，47
    首选项，49
    模板，47
    用户特定设置，46
    用户特定设置，覆盖，47
TurnOff 方法（VirtualMachine 对象），493
类型库，107
    访问，61
    为 Windows 脚本组件（WSC）生成，107
Type 对象（Windows 防火墙），362
TypeAsciiText 方法（Keyboard 对象），498
TypeKeysSequence 方法（Keyboard 对象），498
类型，布尔型，66

# U

UBound 函数，22
下划线字符作为通配符，267
撤销磁盘，493，500
Undoable 属性（VirtualMachine 对象），495
UndoAction 属性（VirtualMachine 对象），495
Unreachable 属性（ExchangeServerState 类），435
取消注册 Windows 脚本组件（WSC），121
UnregisterVirtualMachine 方法（VirtualServer.Application 对象），486
UnregisterVirtualNetwork 方法（VirtualServer.Application 对象），486
不受信任的代码，43，47
不受信任的脚本，设置警告消息，47
UPDATE 查询（SQL），201
用户帐户
    交替帐户，使用交替凭据运行脚本。参见交替凭据
    创建，28–29，210
    组。参见组帐户
    组成员资格，使用 ADO 和 ADSI 测试，256–259
    使用 WMI 列出所有本地用户帐户，261
    用于远程访问，165
用户界面，健壮型。参见 HTA（HTML 应用程序）
用户消息，创建，9
用户名称
    显示常用名称，25
    显示完整名称，9
用户权限，设置，32

# V

验证
    参数，78
    域控制器，412–413
    文件夹路径，19
    日志文件，19
    运行时参数，68
    运行时语法，64
    脚本输入，12
变量，474–476
varSet 对象，475，476
vbInformation 常量，5
vbOkOnly 常量，5
VBScript
    错误处理。参见错误处理
    事件，173
    图形应用程序。参见 HTA（HTML 应用程序）
version 属性（HTA），143
Version 属性（ExchangeServerState 类），435
version 属性（XML \<registration\> 标签），98
虚拟目录，IIS，374–376
虚拟磁盘，484
虚拟机
    在虚拟机中单击鼠标按钮，498
    配置，486
    配置，488–489，490
    创建，488
    定义，484
    差异磁盘，486
    DVD-ROM 驱动器，添加，488
    DVD-ROM 镜像，附加，488
    动态磁盘，488，496
    枚举所有虚拟机，491
    客户机操作系统，484
    GuestOS 对象，497–498
    硬盘属性，修改，489
    HardDisk 对象，496–497
    硬件仿真，485
    初始配置，488–489
    关键标识符，498
    键盘任务，498
    启动延迟，设置，494
    列出所有虚拟机，495
    管理脚本，492–496
    内存分配，配置，494
    鼠标任务，498
    多个虚拟机，管理，491–492
    网络适配器，附加，489
    操作系统兼容性，484
    重置，493
    资源，486
    回滚多个虚拟机，498–500
    保存的状态，管理，493
    保存当前状态，493
    虚拟机脚本包装器，491–492
    会话，486
    启动，489
    挂起，493
    关闭，493，499
    撤销磁盘，493，500
Virtual Server
    Additions 版本，检查，497
    API，483，484–485，487
    架构，486
    可用容量，检查，487
    功能，484–485
    COM 对象，实例化，499
    主机操作系统，定义，484
    启动延迟，设置，494
    对象模型，486–487
    对象引用，获取，491
    虚拟机。参见虚拟机
    虚拟网络，486
VirtualMachine 对象
    方法，492–493
    返回，499
VirtualMachines 方法（VirtualServer.Application 对象），487
VirtualNetworks 方法（VirtualServer.Application 对象），487
VirtualServer.Application 对象，486–487

# W

WaitOnReturn 变量，6
WBEMTest
    启用身份验证，342
    启用权限，342
    连接到命名空间，341
    指定连接信息，288–289
    创建通知查询，288–291
    启用特权，288，341
    枚举实例，343
    执行查询，343
    指定模拟级别，341
    Kerberos 身份验证，342
    运行，268
    启动，341
    停止服务，290
    隐藏系统属性，343
    测试查询，268–269
    查看事件属性，290
网页，与 HTA（HTML 应用程序）的比较，141
网站
    绑定，376
    使用 IIS 配置，377
    使用脚本创建，375–378
WHERE 子句（ASSOCIATORS OF 查询），272
WHERE 子句（SQL），197–198
WHERE 子句（WQL）
    提高效率，263–265
    LIKE 运算符，265–267
    多个条件，265
    引号，264
    指定通配符，265–267
WHERE 查询（WMI）在命令行中，333
通配符
    在 WQL WHERE 子句中指定，265–267
    下划线字符作为通配符，267
Win32_DependentService 类，267
Win32_DiskQuota 类（WMI），364
Win32_PingStatus 类（WMI），356–359
Win32_Printer 类（WMI），381
Win32_PrinterDriver 类（WMI），384
Win32_QuotaSetting 类（WMI），364–365
Win32_TCPIPPrinterPort 类（WMI），383
Windows 防火墙
    授权应用程序，361
    配置，359–363
    允许例外，362
    检索 ICMP 设置，362
    实例化管理器对象，360
    列出打开的端口，359
    打开端口，361
    检索配置文件，362
    启用远程地址的连接授权，361
    启用远程管理，360
    远程管理设置，363
    配置远程脚本，170
    脚本编写与组策略，360
    检索服务，362
    隐藏窗口，6
Windows 管理规范（WMI）。参见 WMI（Windows 管理规范）
Windows 脚本组件（WSC）
    使用 Script Component 向导构建。参见 Script Component 向导
    定义特征，101
    WSC 中的注释，99，120
    使用 PrimalScript 编辑器创建，112–117
    定义，101–102
    事件，103，108
    触发事件，98
    标记事件，98
    指定函数的内部名称，107
    get 命令，333–334
    生成 GUID，97
    方法，107
    定义方法，102
    方法，121
    对象，99，114，121，122
    属性，102，105–106，120
    注册，97–98，121
    创建远程实例，98
    向用户显示脚本错误，97
    安全与，98
    接收器。参见事件接收器
    骨架大纲，99
    标签，97–99
    模板。参见 Script Component 向导
    生成类型库，107
    取消注册，121
    在脚本中使用，122
    可见性，98
Windows 脚本文件（WSF），57–58。另见 XML
    创建子对象，62
    注释，59，60
    将脚本转换为 WSF，69–72
    强制执行 XML 规则，58
    执行特定任务，59
    强制严格 XML 解析，58
    帮助信息，60
    任务，59
    多个脚本，63
    命名参数，60
    命名参数。参见命名参数
    创建对象，61–62
    添加资源，63–64
    运行时功能，60
    运行时参数，61，65
    将结果保存到文本文件，77
    脚本编辑器，68–72
    脚本任务，62–63，63
    添加脚本库，94
    脚本，77，82–83
    显示语法示例，60
    作为包装器脚本，83–84
    XML 格式，58
Windows 脚本宿主（WSH），4。另见信任策略
Windows Server 2003，WMI 类省略，356
Windows 服务，服务间的依赖关系，267
Windows 任务计划程序，53
Windows 任务栏，在任务栏中显示 HTA，143
Windows Update 服务，385–388
windowstate 属性（HTA），143
Winmgmts 对象，30–31
WinNT 提供程序，24，230–240
    大小写敏感性，25
    连接到远程系统，26
    持续的相关性，231
WITHIN 子句（WQL），288
向导，在脚本编辑器中，510–513
向导，WMI，349–351。另见 AdminScriptEditor WMI 向导；SAPIEN PrimalScript
WMI 命令行（WMIC）。参见 WMIC（WMI 命令行）
WMI 事件注册
    使用交替凭据，301
    连接到命名空间，301
    使用者，303
    启动，301
WMI 事件查看器，305，306
WMI 对象浏览器，347–349
WMI 查询
    远程查询，163
    在 CIM Studio 中运行查询，346
WMI 查询语言（WQL）。参见 WQL
WMI 源按钮，324
WMI（Windows 管理规范），29–30
    查看别名信息，332
    交替凭据，54
    关联类，267
    身份验证级别，274
    反斜杠，276
    阻塞。参见阻塞
    CIM Studio。参见 CIM Studio
    缺少类属性，31



## 536 WMIC（WMI 命令行）

WMI *(续)*
类。*参见* 类，WMI
命令行工具。*参见* WMI 命令行 (WMIC)
连接到命名空间，30
磁盘配额管理。*参见* 磁盘配额
DNS 提供程序。*参见* DNS 提供程序
在其中启用权限，275–276
事件，285–286
list 命令，333
使用它列出所有本地用户账户，261
使用它管理文件权限，276–280
命名空间，使用 Scriptomatic 连接到，321
对象，浏览。*参见* WMI 对象浏览器
属性，31，262–263
查询，31–32。*另见* WMI 查询语言 (WQL)
远程访问，用于其的 Windows 防火墙设置，170
脚本阻止。*参见* 阻止
安全层，管理，166
SNMP 提供程序，安装，356
向导，349–351，510

WMIC（WMI 命令行），325
别名，326–331，333
使用备用凭据，332
在批处理文件中，337–341
使用它连接到命名空间，326
使用它连接到远程系统，332
/every 开关，333
get 命令，按计划间隔运行，333–334
安装，325
list 命令，333–334
输出。*参见* XSL 文件
关于它的补充信息，341
在其中使用 WHERE 查询，333
工作簿，Excel。*参见* Microsoft Excel 工作簿

WQL
WITHIN 子句，288
ISA 运算符，287
查询，效率，262–265
WHERE 子句，使用它提高效率，263–265
包装脚本，354–355，491–492
包装 Windows 脚本文件，83–84
将脚本结果写入命令窗口，21
WScript 对象，注册为 bug 修复，174

WSCs。*参见* Windows 脚本组件 (WSCs)
WSFs（Windows 脚本文件）。*参见* Windows 脚本文件 (WSFs)
WSH。*参见* Windows 脚本宿主 (WSH)
WshController 对象
使用它避免对话框，171
CreateScript 方法，172，174
声明，176
对其的限制，171
故障排除，174
WshNetwork 对象，8
WshRemote 对象，172–173
Error 事件处理程序，177
Execute 方法，173
释放，176
Status 属性，172
Terminate 方法，173
WshRemoteError 对象，172

WshShell 对象，4–7
按钮选项，作为常量，14
Exec 方法，248
隐藏窗口，6
使用它启动程序，5
Popup 方法，4–5
使用它读取注册表，5

## X

XML
闭合标签，58
在 CDATA 标签中封装脚本，58
在 Windows 脚本文件 (WSF) 中强制执行，58
用于其的脚本编辑器，68–72

XSL 文件
创建，336–337
用于格式化 WMIC 输出，335

## 关于作者

Don Jones 是一位独立作家、顾问和培训师。他也是行业领先的 Windows 脚本专家之一。Don 拥有并运营 ScriptingAnswers.com。他是 Microsoft 认证系统工程师 (MCSE) 和 Microsoft 最有价值专家 (MVP)。Don 是 *Microsoft Windows Administrator's Automation Toolkit*（Microsoft Press，2005）、*VBScript and WMI for Windows Administrators*（Addison-Wesley Professional，2004）和 *Managing Windows with VBScript and WMI*（Addison-Wesley Professional，2004）的作者。他也是 *Microsoft Windows Server 2003 Resource Kit*（Microsoft Press，2005）的合著者，并且是 *Redmond Magazine*（前身为 *Microsoft Certified Professional Magazine*）的定期专栏作家。

Jeffery Hicks（MCSE，MCT，MCSA）是 Visory Group（Microsoft 金牌合作伙伴）的高级网络工程师。他还是 JDH Information Technology Solutions 的总裁兼首席顾问。他在 IT 行业工作了 15 年，从帮助台支持到项目管理，做过各种工作。他是一位自由技术作家，并开发了多个管理脚本培训视频。Jeff 是多个在线 IT 社区网站的常客，并且是计算机会议和研讨会的特邀演讲者。他目前是 ScriptingAnswers.com 的特约编辑。

### 面向管理员的其他 Windows (R2) 资源

Microsoft Press 已出版和即将出版的图书

#### Microsoft® Windows Server™ 2003 Administrator’s Pocket Consultant, Second Edition

William R. Stanek • ISBN 0-7356-2245-0

这是一本为支持 Microsoft Windows Server 2003 的 IT 专业人员准备的实用、袖珍参考书——已针对 Service Pack 1 和 Release 2 进行了全面更新。这本便携式指南专为快速查阅而设计，涵盖了执行日常系统管理任务所需的所有要素。主题包括管理工作站和服务器、使用 Active Directory® 目录服务、创建和管理用户及组账户、管理文件和目录、执行数据安全和审计任务、处理数据备份和恢复，以及使用 TCP/IP、WINS 和 DNS 管理网络等。

![](img/4fefd6988ba5d4a92a65127617ca24c2_558_0.png)

#### Microsoft Windows® Small Business Server 2003 R2 Administrator’s Companion

Charlie Russel, Sharon Crawford, and Jason Gerend • ISBN 0-7356-2280-9

获取此管理 Windows Small Business Server 2003 R2 的必备指南，快速启动和运行您的小型企业网络、消息传递和协作系统。本参考书详细介绍了标准版和高级版的功能、能力和技术——包括 Microsoft Windows Server 2003 R2、带 Service Pack 1 的 Exchange Server 2003、Windows SharePoint® Services、SQL Server™ 2005 Workgroup Edition 和 Internet Information Services。了解如何安装、升级或迁移到 Windows Small Business Server 2003 R2；规划和实施您的网络、Internet 访问和安全服务；根据您的电子邮件需求自定义 Microsoft Exchange Server；以及管理用户权限、共享、权限和组策略。

![](img/4fefd6988ba5d4a92a65127617ca24c2_558_1.png)

#### MCSE Self-Paced Training Kit (Exams 70-290, 70-291, 70-293, 70-294): Microsoft Windows Server 2003 Core Requirements, Second Edition

Holme, Thomas, MacKin, McLean, Zacker, Spealman, Hudson, and Craft • ISBN 0-7356-2290-6

Microsoft 认证系统工程师 (MCSE) 证书是专业人士的首要认证，他们分析业务需求，并基于 Microsoft Windows Server 2003 平台和 Microsoft Windows Server System 设计和实施业务解决方案的基础设施——现已更新至 Windows Server 2003 Service Pack 1 和 R2。这个全套资料为四门必考的网络系统考试提供了深入的准备。按照您自己的进度学习课程、动手练习、故障排除实验室和复习题。您将获得专家考试技巧，以及覆盖每个学习指南中所有目标和子目标的完整复习部分。然后使用 CD 上的 Microsoft Practice Tests，通过超过 1500 道题进行自我评估和练习来挑战自己！

#### Microsoft Windows Small Business Server 2003 R2 Administrator’s Companion

Charlie Russel, Sharon Crawford, and Jason Gerend • ISBN 0-7356-2280-9

这是一本理想的单卷指南，面向管理 Windows Server 2003 的 IT 专业人员。现已全面更新至 Windows Server 2003 Service Pack 1 和 R2，这本管理员指南提供了关于 Microsoft Windows 核心系统管理主题的最新信息，包括 Active Directory 服务、安全、脚本、灾难计划和恢复，以及与 UNIX 的互操作性。它还包括关于 Service Pack 1 安全更新和 R2 新功能的全新部分。本书具有易于使用的程序和便捷的解决方法，为实际工作结果提供即时答案。

#### MCSA/MCSE Self-Paced Training Kit (Exam 70-290): Managing and Maintaining a Microsoft Windows Server 2003 Environment, Second Edition

Dan Holme and Orin Thomas • ISBN 0-7356-2289-2

#### MCSA/MCSE Self-Paced Training Kit (Exam 70-291): Implementing, Managing, and Maintaining a Microsoft Windows Server 2003 Network Infrastructure, Second Edition

J.C. MacKin and Ian McLean • ISBN 0-7356-2288-4

#### MCSE Self-Paced Training Kit (Exam 70-293): Planning and Maintaining a Microsoft Windows Server 2003 Network Infrastructure

Craig Zacker • ISBN 0-7356-2287-6

#### MCSE Self-Paced Training Kit (Exam 70-294): Planning, Implementing, and Maintaining a Microsoft Windows Server 2003 Active Directory® Infrastructure

Jill Spealman, Kurt Hudson, and Melissa Craft • ISBN 0-7356-2286-8



## Microsoft Windows Server 2003 资源工具包

### *权威级* Windows Server 2003 参考资源！

获取深入的技术信息和工具，以管理和优化 Microsoft® Windows Server™ 2003——其中包含来自微软 MVP、行业顶尖顾问以及 Microsoft Windows Server 团队的专业指导与最佳实践。这套官方*资源工具包*包含七卷综合指南：

- Microsoft Windows® Security Resource Kit，第二版
- Microsoft Windows 管理员自动化工具包
- Microsoft Windows 组策略指南
- Microsoft Windows Server 2003 性能指南
- Microsoft Windows Server 2003 故障排除指南
- Microsoft Windows 注册表指南，第二版
- Microsoft Windows 内部原理，第四版

您将找到 300 多种节省时间的工具和脚本，以及整套*资源工具包*的电子书和五本额外附赠电子书。这是您最大化提升系统性能和可靠性，并降低所有权与支持成本所需的一切。

**Microsoft Windows Server 2003 资源工具包**
微软 MVP 和合作伙伴与 Microsoft Windows Server 团队
**ISBN：** 0-7356-2232-9

*有关 Microsoft Press® 图书的更多信息，请访问：www.microsoft.com/mspress*
*有关在线评估、电子学习和认证等学习工具的更多信息，请访问：www.microsoft.com/learning*

# 面向管理员的其他 SQL Server 资源

Microsoft Press 已出版及即将出版的书目

## Microsoft® SQL Server™ 2005 Reporting Services 逐步深入

Hitachi Consulting Services • ISBN 0-7356-2250-7

SQL Server Reporting Services (SRS) 是 Microsoft 为业务数据分析提供的可定制报表解决方案。它是 SQL Server 2005 的关键价值特性之一：功能比其竞争对手更先进，且成本低得多。SRS 功能强大，因此理解如何设计报表，以及如何安装和编程 SRS，是充分利用 SQL Server 全部功能的关键。本循序渐进的教程展示了如何使用报表项目向导，如何思考和访问数据，以及如何构建查询。它还引导读者创建图表和可视化布局，以实现对数据分析的最大视觉理解。交互性（在 SQL Server 2005 中得到增强）和安全性也进行了详细阐述。

## Microsoft SQL Server 2005 管理员伴侣

Marci Frohock Garcia, Edward Whalen, and Mitchell Schroeter • ISBN 0-7356-2198-5

Microsoft SQL Server 2005 管理员伴侣是一本全面、深入的指南，通过提供部署、管理、优化和支持 SQL Server 2005 所需的全部技术信息来节省您的时间。采用实践为主、示例丰富的方法，这本权威的单卷参考书提供了来自经验丰富的 SQL Server 2005 专业人士的专家建议、产品信息、详细解决方案、操作步骤和实际故障排除技巧。这本专家指南向您展示如何设计高可用性数据库系统、为安装做准备、安装和配置 SQL Server 2005、管理服务和功能，以及维护和故障排除您的数据库系统。它涵盖了如何为您的 I/O 系统配置系统、建模和优化系统容量。专家作者详细介绍了如何创建和使用默认值、约束、规则、索引、视图、函数、存储过程和触发器。本指南向您展示如何管理报表服务、分析服务、通知服务和集成服务。它还提供了关于复制以及快照、事务和合并复制具体细节的丰富信息。最后，它广泛涵盖了如何管理和调优您的 SQL Server 系统，包括自动化任务、数据库备份与还原，以及用户和安全管理。

## Microsoft SQL Server 2005 管理员袖珍指南

William R. Stanek • ISBN 0-7356-2107-1

这是一本极其务实、便于携带的参考书，适用于需要在组织中管理、优化和维护 SQL Server 2005 的 IT 专业人士。这本独特的指南提供了使用 SQL Server 2005 保护和管理公司数据的必要细节——无论是自动化任务；创建索引和视图；执行备份和恢复；复制事务；调优性能；管理服务器活动；导入和导出数据；还是执行其他关键任务。本书提供快速参考表格、列表和分步说明，无论您是在办公桌前还是在现场，这本便捷的一站式指南都能提供快速、准确的答案！

## Microsoft SQL Server 2005 Analysis Services 逐步深入

Hitachi Consulting Services • ISBN 0-7356-2199-3

SQL Server 2005 的关键特性之一是 SQL Server Analysis Services——Microsoft 为业务数据建模和阐释提供的可定制分析解决方案。只需将 SQL Server Analysis Services 与其竞争对手进行比较，就能理解/掌握其增强功能所带来的巨大价值。充分利用 SQL Server 全部功能的关键之一，就是将 Analysis Services 作为强大的工具来利用——包括创建多维数据集，以及部署、自定义和扩展基本计算。这本循序渐进的教程讨论了如何入门、如何构建可扩展的分析应用程序，以及如何使用和管理高级功能。交互性（在 SQL Server 2005 中得到增强）、数据转换和安全性也进行了详细阐述。

## Microsoft SQL Server 2005 Express Edition 逐步深入

Jackie Goldstein • ISBN 0-7356-2184-5

## 深入了解 Microsoft SQL Server 2005：存储引擎

Kalen Delaney • ISBN 0-7356-2105-5

## 深入了解 Microsoft SQL Server 2005：T-SQL 编程

Itzik Ben-Gan • ISBN 0-7356-2197-7

## 深入了解 Microsoft SQL Server 2005：查询处理与优化

Kalen Delaney • ISBN 0-7356-2196-9

有关 Microsoft Press® 图书和其他学习产品的更多信息，请访问：www.microsoft.com/mspress 和 www.microsoft.com/learning

Microsoft Press 产品在全球各地销售优质计算机书籍的地方均有售。如需了解更多信息，请联系您的图书或计算机零售商、软件经销商或当地的 Microsoft 销售办事处，或访问我们的网站 www.microsoft.com/mspress。要查找距离您最近的 Microsoft Press 产品来源，或直接订购，请在美国致电 1-800-MSPRESS。（在加拿大，请致电 1-800-268-2222。）

Microsoft Press

# 您对这本书有何看法？
我们想听听您的意见！

您有几分钟时间参与一项简短的在线调查吗？Microsoft 希望听取您对本出版物的反馈，以便我们能持续为您改进图书和学习资源。

要参与我们的调查，请访问：
**www.microsoft.com/learning/booksurvey**

并输入本书的 ISBN，0-7356-2244-2。为了感谢美国和加拿大的调查参与者，我们每月将随机抽取五名受访者，赢取来自一家领先在线商家的五张 100 美元礼品卡之一。*调查结束后，您可以通过提供电子邮件地址参与抽奖，该地址将*仅*用于奖品通知。

提前感谢您的反馈。您的意见很重要！

此致，

Microsoft Learning

学得更多，走得更远。

要查看针对开发人员、IT 专业人士以及家庭和办公室用户的 Microsoft Learning 产品特别优惠，请访问：www.microsoft.com/learning/booksurvey

* 无需购买。在禁止地区无效。仅限美国 50 个州（包括哥伦比亚特区）和加拿大居民参与（魁北克省无效）。抽奖活动截止日期为 2006 年 6 月 30 日。有关官方规则，请参见：www.microsoft.com/learning/booksurvey



# IT专业人士的更多优秀资源

微软出版社已出版及即将推出的图书

### 管理员袖珍宝典

-   实用、便携的指南，助您在需要时快速获得答案
-   聚焦核心运维与支持任务
-   编排清晰，便于快速精准查阅——高效完成工作

Microsoft SQL Server™ 2005 管理员袖珍宝典
William R. Stanek
0-7356-2107-1

Microsoft Windows Server™ 2003 管理员袖珍宝典（第二版）
William R. Stanek
0-7356-2245-0

Microsoft Windows XP Professional 管理员袖珍宝典（第二版）
William R. Stanek
0-7356-2140-3

Microsoft Windows 命令行管理员袖珍宝典
William R. Stanek
0-7356-2038-5

### 管理员伴侣

-   全面的、单卷本系统管理指南
-   来自实战的见解、流程、故障排除策略与解决方案
-   随书CD包含可全文检索的电子书

Microsoft Windows Server 2003 管理员伴侣（第二版）
Charles Russel, Sharon Crawford, and Jason Gerend
0-7356-2047-4

Microsoft Windows Small Business Server 2003 管理员伴侣
Charles Russel, Sharon Crawford, and Jason Gerend
0-7356-2020-2

Microsoft Exchange Server 2003 管理员伴侣
Walter J. Glenn and Bill English
0-7356-1979-4

Microsoft Systems Management Server 2003 管理员伴侣
Steven D. Kaczmarek
0-7356-1888-7

### 资源工具包

-   由最精通该技术的专家提供的深度技术信息与工具
-   部署与运维的权威参考和最佳实践
-   随书CD包含资源工具包，含电子书

Microsoft Windows Vista™ 资源工具包
Tulloch, Honeycutt, Northrup, and Russel with the Microsoft Windows Vista Team
0-7356-2283-3

Microsoft Exchange Server 2003 资源工具包
Unkroth, Molony, Cherny, Reid, Strachan, English, and the Microsoft Exchange Server Team
0-7356-2072-5

Microsoft Windows Server 2003 资源工具包
Microsoft MVPs and Partners with Microsoft Windows Server Team
0-7356-2232-9

Microsoft Windows 安全资源工具包（第二版）
Ben Smith and Brian Komar with the Microsoft Security Team
0-7356-2174-8

### 自学培训工具包

-   二合一产品：官方考试准备 + 模拟测试
-   包含课程、练习和案例场景
-   综合自测；试用软件；随书CD包含电子参考库

实施和维护 Microsoft SQL Server 2005 MCTS 自学培训工具包
0-7356-2271-X

设计 Microsoft SQL Server 2005 数据库服务器基础设施 MCITP 自学培训工具包
0-7356-2173-X

Microsoft Windows Server 2003 核心要求（第二版）MCSE 自学培训工具包
0-7356-2290-6

安装、配置和管理 Microsoft XP Professional（第二版）MCSA/MCSE 自学培训工具包
0-7356-2152-7

访问我们的完整学习资源系列：microsoft.com/mspress 和 microsoft.com/learning

# 面向 Microsoft® Windows® 管理员的高级 VBScript

通过这本权威、深入的指南，将您的脚本编写技能提升至更高层次。

通过向两位专家学习高级脚本技术，掌握对系统管理的*终极*控制。经验丰富的 Windows 脚本编写者可以通过实践指导、高级技术和使用 Microsoft Visual Basic® Scripting Edition (VBScript) 作为企业级管理工具的最佳实践，超越基础。您还将获得即用型脚本和随书CD中的电子书。

**了解如何：**

-   构建自己的脚本组件和库
-   使用数字签名和证书创建安全增强的脚本
-   使用高级 ADSI 技术从 Active Directory® 检索信息
-   使用高级 Windows 管理规范 (WMI) 技术管理您的 Windows 环境
-   使用脚本备份、复制、还原和设置组策略环境的权限
-   编写脚本使用 ADO 访问数据库
-   构建用于脚本图形界面的超文本应用程序
-   开发与 Microsoft Exchange Server 和 Microsoft Operations Manager 协同工作的脚本
-   利用 Microsoft Windows Server™ 2003 和 Windows XP 的脚本更新功能

**CD 特色：**

-   超过 100 个示例脚本，可供您改编用于自己的工作
-   可全文检索的电子书

*有关**系统要求**，请参见引言。*

**关于作者：**

**Don Jones**，MCSE，是 Windows 管理脚本方面的专家。他运营着 ScriptingAnswers.com，并撰写了超过 15 本书，包括 *Microsoft Windows Administrator's Automation Toolkit*。作为 Windows Server 的 Microsoft MVP，Don 也是 *Redmond* 杂志的专栏作家。

**Jeffery Hicks** 是 Visory Group 的高级网络工程师，也是 JDH Information Technology Solutions 的总裁和首席顾问。他在 IT 行业拥有 15 年经验，并定期为多个 IT 社区网站供稿。

## IT 专业人士的更多资源

### 管理员袖珍宝典

-   实用、便携的指南，助您在需要时快速获得答案
-   聚焦核心运维与支持任务
-   编排清晰，便于快速精准查阅——高效完成工作

### 管理员伴侣

-   全面的、单卷本系统管理指南
-   来自实战的见解、流程、故障排除策略与解决方案
-   随书CD包含可全文检索的电子书

### 资源工具包

-   由最精通该技术的专家提供的深度技术信息与工具
-   部署与运维的权威参考和最佳实践
-   随书CD包含资源工具包，含电子书

### 自学培训工具包

-   二合一产品：官方考试准备 + 模拟测试
-   包含课程、练习和案例场景
-   综合自测；试用软件；随书CD包含电子参考库

*欲了解更多信息，请参见封底内页。*
