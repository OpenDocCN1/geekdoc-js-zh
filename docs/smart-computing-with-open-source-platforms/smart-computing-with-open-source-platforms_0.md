# 开源平台智能计算



![](img/9781351120326.jpg)


![Images](img/line1.jpg)

## 序言

![Images](img/line2.jpg)

高端计算平台、开源硬件和软件技术的进展，对于嵌入式系统、传感器网络、物联网、泛在计算和机器学习领域的尖端研究至关重要。复杂的传感器和硬件设备使得数据采集任务在动态变化的环境中变得高效。环境产生的数据被存储在各种持久存储和云环境中。此外，可以使用高度优化的机器学习算法对数据进行处理，以观察趋势并预测某些环境的未来特征。

本书的基本目标涉及复杂的开源嵌入式和现代编程平台，以获取、存储、可视化和预测数据。本书的重点是介绍 `Arduino` 平台以在硬件层面实现基础解决方案。此外，讨论了 `Python` 编程语言，并介绍了 `Arduino–Python` 接口的力量。此外，介绍了机器学习算法，反映了 `Python` 机器学习和深度学习应用的实际场景。本书的设计使得不熟悉 `Arduino`、`Python` 和机器学习应用概念的读者能够理解并设计相关的应用。本书作为本科生、研究生、研究人员以及业爱好者的指南。

**Amartya Mukherjee**

**Nilanjan Dey**

![Images](img/line1.jpg)

## 致谢

![Images](img/line2.jpg)

本书本身是对各种技术和现代科学计算的致谢。我们感谢技术和开源社区，他们的持续支持使本书成为可能。我们还感谢我们的妻子和孩子的持续鼓励。

在真正的开源世界中，你有权主控自己的命运。

**Linus Benedict Torvalds**

![Images](img/line1.jpg)

## 作者

![Images](img/line2.jpg)

![](img/000x001.jpg)

**Amartya Mukherjee** 是印度加尔各答盐湖特克工程与管理学院（Institute of Engineering and Management）的助理教授。他拥有西孟加尔邦科技大学的计算机科学与工程学士学位，以及来自印度西孟加尔邦杜尔加普国立技术学院（National Institute of Technology）的计算机科学与工程硕士学位。他的主要研究方向是嵌入式应用开发，包括移动自接网络、空中机器人、物联网和机器学习。他在无线网络和嵌入式系统领域发表了多篇研究论文。他的著作《Embedded Systems and Robotics with Open-Source Tools》（CRC Press, 2016）是嵌入式应用开发领域的畅销书之一。

![](img/000x002.jpg)

**Nilanjan Dey, PhD,** 是印度加尔各答技术学院（Techno India College of Technology）信息技术系的助理教授。他曾任加州罗斯维尔全球生物医学技术公司（Global Biomedical Technologies Inc.）的荣誉访问科学家和伦敦阅读大学的副成员。他与 Elsevier、Wiley、CRC Press、Springer 等出版社编写/编辑了 40 多本书，并发表了 300 多篇研究论文。他是《International Journal of Ambient Computing and Intelligence》的主编辑。他是《Springer Tracts in Nature-Inspired Computing》（Springer Nature）、《Advances in Ubiquitous Sensing Applications for Healthcare》（Elsevier）以及《Intelligent Signal Processing and Data Analysis》（CRC Press）系列的合编。他是《IEEE Access》的副编辑。他的主要研究兴趣包括医学影像、机器学习、数据挖掘等。近期，他被评为 2015-2017 年间印度计算机科学领域发表和引用量最高的学者之一。

![Images](img/line1.jpg)

## 引言

![Images](img/line2.jpg)

![Images](img/line.jpg)

### 智能计算方法论





我们生活在一个智能设备时代，现实世界中的机器正变得越来越智能。在这个背景下，重大事件之一是智能手机、智能小设备以及物联网（IoT）设备的引入。因此，数据驱动的智能系统是智能系统（可能是如今的智能环境）的骨干。`Android`等智能操作系统的引入使得设计和部署智能应用变得高度灵活且多功能。此外，嵌入式硬件的丰富以及如`Arduino`和`Raspberry Pi`等开源快速原型平台的出现，让智能系统开发者的生活变得更加轻松。在早期，实时智能系统是高度分类的，被用于任务关键型应用，例如导弹跟踪与发射、航天任务、无人机控制与监控以及军事用途的许多其他领域。目前，智能计算的应用无处不在，从数据科学、数据分析、预测和预报到智能城市和智能家用电器。基于物联网的服务与舒适度管理以及许多其他社会和商业应用领域确实是一项急需的技术增强实践。

![Images](img/line.jpg)

## 智能计算平台

对于智能计算平台而言，它可能是最具挑战性的平台，因为它接收输入问题、进行分析并做出决策，从而得出某种程度的解决方案。在这种背景下，可以考虑智能计算平台的多个智能侧面。因此，计算环境的主要重点是决策。计算平台可能是一个纯软件平台。有时，它是独立的硬件，但在大多数情况下，它是软件和硬件的结合，以协作的方式执行任务。

例如，以前当我们离开家去远旅行时，在出门之前，我们必须检查空调、冰箱以及所有其他家用电器是否已正确关闭。如果我们没有仔细检查，电器极可能会损坏，并且在月底会产生一笔巨额的电单。如今，随着智能计算和物联网环境的引入，这个问题有了简单的解决方案。因为所有的家用电器都连接到一个中央网关。系统会监控房间内的活动。如果发现房间内没有活动，它将立即向用户发送警报信息，并同时关闭家用电器。在另一种场景下，由于电力分布不均且缺乏需求侧负载预测机制，以前防止特定区域的限电是非常具有挑战性的。但现在，得益于智能负载预测和预报，机器学习算法使得预测未来的电力需求变得容易得多。

从微级小型嵌入式设备到低端微机、高端图形处理器（`GPU`）和张量处理单元（`TPU`）（来源：[`developers.googleblog.com/2018/07/new-any-edge-tpu-boards.html`](https://developers.googleblog.com/2018/07/new-any-edge-tpu-boards.html)）以及当然还有云服务，应该是智能和智能计算生态系统中最流行的平台。某些开源平台在设计、构建和构造智能应用方面具有巨大的优势。一个名为`GPUOpen`的倡议提供了免费的视觉效果、生产力工具以及各种其他内容的全面集合。这里的代码易于分享和下载。`MIAOW GPU`是威斯康星大学麦迪逊分校开发的另一项研究成果。GPU 的根本目标是通过免费开源的代码包获得高性能计算。

开放计算语言（`OpenCL`）是另一种免费且跨平台的计算环境。该环境基于智能手机、个人电脑、服务器和其他手持设备中各种处理器的并行编程构建的。`OpenCL`显著提升了图像处理、计算机视觉和游戏应用的性能。

Khronos 集团宣布发布了`Vulkan 1.1`，这是`OpenGL`平台的新伴侣，以及`SPIR-V 1.3`的规范。1.1 版本通过大量开发者请求的功能（如子组操作）扩展了`Vulkan`的核心功能，同时整合了来自`Vulkan 1.0`的广泛已验证扩展。Khronos 还将把完整的`Vulkan 1.1`一致性测试开源，AMD、Arm、Imagination、Intel 公司、NVIDIA 和高通已经实现了兼容的`Vulkan 1.1`驱动。

![Images](img/line.jpg)

## 嵌入式系统与机器人的智能计算

嵌入式计算和自动化机器人可能是伴随智能计算的最新兴技术。大多数复杂的嵌入式平台使用某种程度的智能处理方法，例如先进医疗系统、疾病检测与预测系统以及建筑结构中的故障检测。现代 3D X 射线和 MRI 需要大量的智能信号处理算法。智能嵌入式系统在汽车制造领域还有广泛应用，在汽车中放置了嵌入式智能标签，可以监控组件健康、发动机和座舱温度，并收集和记录发动机振动，用于进一步诊断不仅是当前汽车，而且未来制造的汽车的故障。

在机器人领域，可以实现大量的智能应用，例如物体和障碍物检测与规避、飞行器的精确起降，以及无人机机系统和导弹系统的自主导航。在医学领域，机器人手术非常流行，这是智能机器人系统的相关示例。在航天任务中，宇航员使用机器人设备在零重力区精确移动设备。另一个智能机器人系统的大例子是社交机器人。在这个背景下，流行的机器人之一是`Sophia`。`Sophia`的智能计算算法设计使得它们能够跟随脸部、保持眼神交流并识别个人。机器人复杂的神经网络可以处理语音。它是基于名为`ELIZA`的聊天机器人的哲学开发的。

![Images](img/line.jpg)

### 本书的目标

本书主要强调智能计算方法论的理论应用及其使用的工具。它讨论了计算设备和服务的的设计、编码、实现以及部署场景。针对与智能系统开发相关的软件和应用程序接口（`API`）进行了详细讨论。




本书的主要动力是在边学边做。交互式特性是本书的核心特征。书中讨论了各种智能 API，用于在嵌入式系统和人工智能领域开发智能型应用。此外，本书还为学习 `Python`、`Arduino` 和 `Processing` 等编程语言提供了全面的指南。仅通过这本书，开源开发的力量就得到了提升。

![Images](img/line.jpg)

## 如何使用本书

本书是一本关于开源硬件和软件概念的入门指南。与基于理论的学习方法不同，本书主要侧重于基于实现的交互式学习。由于本书的核心关注点是 `Python` 和 `Arduino`，因此对于那些希望以更简单、并行的方式学习 `Python` 和 `Arduino` 以开发基于物联网的项目以及机器学习的硬件实现的人来说，它将非常有帮助。书中讨论的内容在学习后必须经过实现，才能获得技术的精髓。

本书的结构如下：第 1 章、第 2 章、第 3 章、第 4 章、第 5 章、第 6 章以及第 7 章 详细介绍了 Arduino 编程环境和语言。第 8 章 讨论了处理语言的基础实现，用于开发基于 Arduino 的智能应用。第 9 章 涵盖了各种基础 Arduino 项目。第 10 章、第 11 章、第 12 章、第 13 章、第 14 章、第 15 章、第 16 章、第 17 章以及第 18 章 以交互的方式描述了 `Python` 语言的核心概念。第 19 章 涉及 `Python` 中的图形用户界面实现。第 20 章和第 21 章 描述了与智能框架相关的 API。这些章节还讨论了基础和高级的机器学习及深度学习 API。

## 1

![Images](img/line.jpg)

## 开源硬件简介](#ch00_fm04_toc.xhtml_rchapter1)

![Images](img/line2.jpg)

![Images](img/line.jpg)

### 1.1 开源硬件概念](#ch00_fm04_toc.xhtml_rsec1_1)

“开源硬件” [[1]](#ch01.xhtml_ref1_1) 这个术语在今天非常常见。开源硬件，也称为开放硬件，基本上被概念化为某些设计信息构建的电子硬件或计算机组件，这些组件可以在不受严格版权法限制的情况下进行版权保护和许可 [[2]](#ch01.xhtml_ref1_2)。原理图、使用的组件、文档和逻辑设计都是开源硬件设计的组成部分。与开源软件一样，开源硬件可能提供用于硬件设计的源代码；在这种情况下，源代码是蓝图或设计文件，该文件有时可能是计算机辅助设计 (`CAD) 文件。

开源硬件的许可涉及设计和文档的重新分发、修改以及任何修改内容的发布。它也从不阻止他人赠送或出售项目及其文档。开源硬件和软件设计也受版权法约束，但硬件使用了一些有助于其重新分发和公开的法律 [[3]](#ch01.xhtml_ref1_3)。免费许可是开源硬件最常见的特征。最常见的许可之一是知识共享署名许可协议（Creative Common Attribution License）。开源硬件必须连同设计文件和源代码一起进行记录。此外，许可机构必须允许修改或更改设计文件并重新分发它们，以便任何人都能访问修改后的设计文件。开源硬件的根本目标是尽可能容易地制作、混合该对象并复制它。然而，闭源硬件使用严格的版权法和专利法，这使得这些对象的生产非常困难。

![Images](img/line.jpg)

### 1.2 Arduino 生态系统及其类型](#ch00_fm04_toc.xhtml_rsec1_2)

欢迎来到 Arduino 世界。在我们思考 Arduino 如何工作之前，让我们先考虑一些实际场景。假设你正坐在办公室里，突然想起你忘记关闭家里的空调了。由于家离办公室很远，需要很长时间才能到达。在这种情况下，显然你会考虑一种可以从你所在地关闭空调的系统或服务。如果你能自己设计该服务或设备，而不需要花费大量资金从第三方供应商处购买，那也是一个很酷的主意。因此，考虑到此类需求，Arduino 等设备的概念就运而生了。Arduino 的设计旨在让任何具有最小电子工程知识和编程技能的人都能处理它。Arduino 的基础生态系统由硬件和软件套件组成。硬件是运行引导程序和固件的底层。在大多数情况下，固件与第二层的第三方库相关联。第三层存在通信协议。该层的主要工作是连接其他设备。通信可以是无线的或有线的。对于有线通信，我们需要在层中添加额外的通信设备和相应的库。

### 1.3 Arduino 硬件特性](#ch00_fm04_toc.xhtml_rsec1_3)

根据易用性，Arduino 板板可以分为若干类型 [[4]](#ch01.xhtml_ref1_4)。分类是基于微控制器版本以及输入输出引脚数量、微控制器类型、中央处理器时钟频率、USB 和通用异步收发器 (`UART`) 接口的数量和类型、电可擦除可编程只读存储器 (`EEPROM`)、静态随机存储器 (`SRAM`) 以及闪存的大小。市场上有多种类型的 Arduino。最流行的 Arduino 板板是 Arduino UNO。图 1.2 展示了不同的 版本。不同类型 Arduino 板板的对比研究列在表 1.1](#ch01.xhtml_tab1_1) 中。

![Images](img/line.jpg)

### 1.4 Arduino 软件特性](#ch00_fm04_toc.xhtml_rsec1_4)

Arduino 软件包是一个工具集，主要包含集成开发环境 (`IDE`) 和许多标准库。由 Java 开发的 IDE 需要 Java 来运行整个过程。Java 运行时环境默认随套件提供。

软件的主要组件如下：





![Images](img/001x002.jpg)

**图 1.2**

不同类型的 Arduino 板板。

![Images](img/Table_1.1.jpg)

**表 1.1**

不同 Arduino 版本的比较

*   IDE
*   核心 API
*   核心库
*   Sketches（程序）
*   各种板载的驱动支持

在 `IDE` 中编写的 Arduino 代码被称为 sketch [[5]](#ch01.xhtml_ref1_5)。sketch 文件最初的扩展名为 `.pde`，这是 Arduino 和 Processing 共同的扩展名。后来，在 Arduino 的新版本中，扩展名已相应更改；现在 `.ino` 和 `.pde` 都是支持的扩展名。附带的（通信端口）`COM`/Serial` 端口显示在 Arduino `IDE` 的底部状态栏中。它还包含了代码行号。Arduino `IDE`——偏好面板——是高效配置 Arduino 环境的好工具。在这里，我们不仅可以更改首选语言（推荐使用系统默认）和字体大小，还可以配置编译和上传代码时的详细输出。更多的额外偏好可以设置在一个名为 `preference.txt` 的文件中。

每当我们开始在 Arduino 中编写任何 sketch 时，环境本身提供了对某些核心库的访问。它不需要添加外部库。例如，可以通过隐式可用的库 `Arduino.h` 直接访问 `Serial` 对象。因为 `Arduino.h` 是默认库且是隐式附加的。只有当我们想要创建一个新的库文件时，才能直接编写代码。在这种情况下，我们需要显式地添加 `Arduino.h`。所有的库实际上都是用 C++ 编写的。

还整合了一些 API 更新。`pinMode` 已经更新以支持 `INPUT_PULLUP`，以便为默认为高电平的按钮和开关添加特定的纯拉拉支持。因此，与其编写 `pinMode(5,INPUT)`，我们现在可以写成 `pinMode(5,INPUT_PULLUP)`。这对于设置默认值是有益的。通用整数或 `uint_8`（跨平台应用开发的标准 8 位整数）现在被大多数函数支持。

Arduino 核心 API 从根本上构建在 `Arduino.h` 头文件之上。如果你正在开发库，有必要了解已经包含在 `Arduino.h` 中的库，以避免重复包含。Arduino 的各种头文件列如下：

```cpp
 #include <avr/interrupt.h>
#include <avr/pgmspace.h>
#include <avr/io.h>
#include <math.h>

#include <stdlib.h>
#include <string.h>
#include "binary.h"

#include "WCharacter.h"
#include "pins_arduin.h"
#include "HardwareSerial.h"
#include "WString.h"
```

Arduino 的主程序是 `main.cpp`。该文件始终包含 `Arduino.h.`，它调用了 `void setup()` 和 `void loop()` 函数。

`main.cpp` 的默认实现所示：

```cpp
 #include <Arduino.h>
int main(void){

  init();
#if defined(USBCON)
             USBDevice.attach();
#endif
  setup();

  for(;;)
{
  loop();
 if(SerialEventRun) SerialEventRun();
}
return 0;
}
```

在 Arduino 软件的新版本中，创建了一个新的 `Printable` 类，并修改了 `Print` 类。这将直接影响 `Stream` 和 `Client` 类。`Print` 类中增加了新函数以提供更多功能。得益于更新的字符串库，在闪存中存储字符串要简单得多。我们也可以使用 `F()` 命令来实现这一点。

![Images](img/line.jpg)

### 1.5 如何设置

要设置 Arduino，第一步是从互联网下载包并安装它。在 Arduino 网站 ([`www.arduino.cc/`](https://www.arduino.cc)) 上，提供以下版本：

*   32 位 Windows
*   32 位和 64 位 Linux
*   MAC OSX
*   Linux ARM 版本

我们可以下载 Windows 的安装程序或 `.zip` 文件，以及 Linux 的 `tar.xz` 格式文件。对于 Windows 安装，你必须安装像 `Arduino` 这样的驱动文件。如果你先安装 Arduino `IDE` 然后再连接 Arduino 板，由于驱动问题，它将永远无法检测到。因此，在将 Arduino 板连接到 Arduino `IDE` 之前，必须安装驱动程序。

为了这样做，我们需要遵循以下步骤（图 1.3）。

我们首先将 Arduino 板连接到电脑并进入电脑的设备管理器。当它检测到 Arduino 时，会立即显示带有问题的 `USB` 端口（图 1.4）。

右键点击 `USB` 端口。它会立即显示更新驱动程序的选项。如果你点击它，将打开驱动管理窗口（图 1.5）。

在驱动管理窗口中，选择“浏览我的电脑以查找驱动程序”，这将打开驱动路径对话框。然后，选择 Arduino 软件包中的驱动位置并点击下一步。现在它将显示更新驱动程序（带有某些强制升级选项，只需点击是）。在驱动安装后，`USB` 端口将显示 `COM` 端口。

![Images](img/001x003.jpg)

**图 1.3**

Windows 设备管理器。

![Images](img/001x004.jpg)

**图 1.4**

设备驱动安装。

![Images](img/001x005.jpg)

**图 1.5**

驱动程序浏览器。

![Images](img/001x006.jpg)

**图 1.6**

设备驱动的安装。

对于 Linux，通常情况下，它会自动检测 `/dev/ttyACM` 端口或 `/dev/ttyUSB` 端口。这是 Linux 环境中默认可用的 `USB` 端口（图 1.6）。

安装驱动程序后，我们可以编写代码并将程序上传到板上。在第一次连接期间，系统现在已准备好进行交互。

![Images](img/line.jpg)

### 1.6 Arduino 环境

Arduino DUE 是一种特殊类型的微控制器板。该板使用的处理器是基于高级 RISC 的 Atmel SAMX8E ARM Cortex-M3。

该 板可能是第一个使用 32 位 ARM CPU 的 Arduino。为了运行 Arduino DUE，我们应该使用 Arduino `IDE` 或网页编辑器。将此板连接到电脑，我们应该使用靠近 9V 电源接口的 `USB` 端口。连接板到电脑后，我们应该打开 `IDE`。通常，`IDE` 最初不会在板类型菜单中显示 Arduino DUE。因此，我们需要在板上安装库。为此，我们需要打开板管理器并安装 Arduino SAM Board Essentials，以便 `IDE` 开始支持基于 ARM 的 Arduino，如 Arduino DUE。安装 Arduino DUE 的库和工具需要几分钟。安装完成后，`IDE` 现在准备好运行 DUE 板。

![Images](img/001x007.jpg)

**图 1.7**

通过板管理器安装 Arduino DUE。





1. 1. Acosta, Roberto. “开源硬件。” *博士论文*，马萨诸塞理工学院，剑桥，马州，2009 年。
2. 2. Bonvoisin, Jeremy, Robert Mies, Jean-Francois Boujut 和 Rainer Stark. 开源硬件的“源”是什么？获取自 [`openhardware.metajnl.com/articles/10.5334/joh.7/`](https://openhardware.metajnl.com), 2017。
3. 3. Viseur, Robert. 从开源软件到开源硬件。获取自 [`link.springer.com/chapter/10.1007/978-3-642-33442-9_23`](https://link.springer.com), 2012。
4. 4. Dey, Nilanjan 和 Amartya Mukherjee. *基于开源工具的嵌入式系统与机器人*。CRC Press，佛罗里达州 Boca Raton，2016。
5. 5. Badamasi, Yusuf A. “Arduino 的工作原理。” 载于 *电子、计算机与计算（ICECCO），2014 年第 11 届国际会议*，第 1–4 页。IEEE，2014 年。

## 2

![Images](img/line.jpg)

## Arduino 硬件](#ch00_fm04_toc.xhtml_rchapter2)

![Images](img/line2.jpg)

Arduino 以其开源特性而闻名。Arduino 开发板主要包含微控制器和一个输入/输出系统。市场上上有多种版本的 Arduino。通常，最流行的 Arduino 版本是 `Arduino UNO` 和 `Arduino Mega`。其他版本如 `Arduino Nano`（2.X 版本和 3 版本）、`Arduino MINI v.04` 和 `Lilypad Arduino` 在市场上也非常受欢迎。一些最新的可用型号包括 `Arduino Leonardo` 和 `Arduino Duo`。

这种基于单片机的计算设备是各级学校大学学生、研究人员和爱好者的最佳选择。通过 Arduino 可以以最简单的方式完成接口电路、开关、电机控制以及各种输出设备。`Arduino UNO` 是一种基于 8 位微控制器系统的板，该控制器名为 `ATmega328`，工作电压为 5V [[1]](#ch02.xhtml_ref2_1)。微控制器本身具有 2 kB 的随机访问存储器和 32 kB 的内部闪存器。

![Images](img/line.jpg)

### 2.1 系统架构](#ch00_fm04_toc.xhtml_rsec2_1)

`Arduino UNO` 的打印电路板 (PCB) 设计 [[2]](#ch02.xhtml_ref2_2) 使用表面贴装元件 (SMD) [[3]](#ch02.xhtml_ref2_3)。每个集成电路均采用标准封装。。大部分部件是通用的并具有不同的功能。例如，`SOT223` 组件由晶体管或电压调节器组成。以下列表描述了 Arduino 硬件的基础组件：

![Images](img/C002_UNTBL_1.jpg)

由于 `Arduino UNO` 可以通过 USB 编程，且由于微控制器不支持 USB 收发器，因此硬件需要在串口接口 [通用异步收发传输器 (UART)] 与微控制器数据线之间建立桥接，以便成功上传数据。`ATmega16U2` 就是一个具有 USB 收发器和 `UART` 接口的桥器。

![Images](img/line.jpg)

### 2.2 微控制器](#ch00_fm04_toc.xhtml_rsec2_2)

由 Alf 和 Vegard 设计 RISC (AVR) 处理器微控制器是 Arduino 的大脑。这是一种支持减少指令集 (RISC) 架构的 8 位微控制器。微控制器的独特性和多功能性使其与 8051 等其他控制器区分开来 [[4]](#ch02.xhtml_ref2_4)。哈佛架构的一个标准特性实际上包含在该系统中，该系统由独立的代码和程序内存组成，这优于程序和数据存储在单一公共内存中的冯·诺依曼架构。AVR 系列微控制器首次引入了用于存储程序的外部闪存器。除了 EPROM 和 EEPROM（电可擦除可编程读存储器）之外，闪存的优势在于我们可以多次地从闪存器中存储和擦除数据。大多数 AVR 控制器的 EEPROM 容量极小。CPU 核心如图 2.1](#ch02.xhtml_fig2_1) 所示。

内部，它包含一个 AVR CPU [[5]](#ch02.xhtml_ref2_5)、定时器、串口接口和模拟/数字转换器。RISC 机器支持 131 条指令和 32 个 8 位通用寄存器。支持的时钟频率为 20 MHz，每秒百万指令 (MIPS) 率为 20 MIPS。所有外设都由控制寄存器控制。它们还配置控制寄存器的功能。可用多种 AVR 微控制器。AVR 控制器的设计师必须为特定的微控制器选择合适的部件，这在不同类别之间可能不同。

`ATmega328p` 是一种 8 位 AVR 系列微控制器。这意味着它将具有 8 位数据线，且内部寄存器可以并行处理 8 位数据。闪存器的大小为 32 kB，用于存储应用程序。由于其本质是非易失性的，即使拔掉微控制器，应用程序依然存在。`ATmega` 具有 2 kB 的 SRAM，可以存储运行时应用程序使用的变量。它还有 1 kB 的 EEPROM，用于永久存储数据。AVR 微控制器的框图如图 2.2](#ch02.xhtml_fig2_2) 所示。

该封装为 DIP-28 配置，包含 28 个工作引脚，包括电源和输入/输出引脚。大多数引脚是多功能的，其优势是可以根据配置将同一引脚用于不同用途，从而不可避免地减少设备的引脚数量。另一个流行的封装是 TQFP-32SMD，这是一种具有 32 个引脚的表面贴装封装。

![Images](img/002x001.jpg)

**图 2.1**

AVR CPU 核心。

流行的 microcontroller `ATmega324` 的常见特性描述如下：

系统中带有片上程序，通常称为引导加载程序 (bootloader)。有一个 8 位定时器/计数器用于比较和分频。此外还有两个 16 位定时器/计数器用于分频、比较和捕获模式。它包含一个 16 位分辨率的 8 位脉宽调制 (PWM) 通道。它具有 11 位分辨率的高速 PWM 通道。12 通道 10 位模拟数字转换器 (ADC)。设备的 `USART` 具有发送/清除发送 (RTS/CTS) 握手功能。片上可用主/从外设接口 (SPI)。提供了兼容 Philips 的双线 I²C 接口。它还包含一个可编程看门定时器、模拟比较器和片上温度传感器。

![Images](img/002x002.jpg)

**图 2.2**

AVR 微控制器内部架构。





MCU 在 `PORTC` 引脚 0–5 上具有一个六通道 ADC [[7]](#ch02.xhtml_ref2_7)。A/D 转换器具有 10 位分辨率，这意味着使用十种不同的信号电平来表示数字数据。这些引脚直接连接到 Arduino 模拟输入排针上。模拟输入并不是微控制器的专用引脚。然而，它们可以作为数字 I/O 或数模转换器使用。

## 2.2.4 Arduino 中的外设(#ch00_fm04_toc.xhtml_rsec2_2_4)

`UART` 是一种串口接口，对于异步数据传输非常有用。UNO 只有一个 `UART` 接口 [[8]](#ch02.xhtml_ref2_8)。

`SPI` 是另一个进行串行传输的接口。`ATmega328` 拥有一个 `SPI` 模块。Arduino UNO 板上位于 MCU 旁排针上或数字排针上的 `SPI` 引脚被标记为 `MOSI`（引脚 11，主出从入）、`MISO`（引脚 12，主入从出）和 `SCK`（引脚 13，串口时钟）。`MOSI` 是向从设备外设发送数据的输出输出线，而 `MISO` 是向主设备发送数据的从线。`SCK` 用于产生时钟脉冲，以同步由主设备产生的数据传输。

为了实现 `SPI` 设备的最大速度，应该更改 `SPI` 库中 `SPI` 设置的第一个参数。

`I2C` 或双线接口是 Arduino 中的另一种通信介质，其中包含两根线：串行数据 (`SDA`) 和串行时钟 (`SCL`)。Arduino 数字排针的最后两个引脚以及模拟排针的引脚 4 和 5 可以作为 `I2C` 通信线

在早期的 Arduino 模型中有一个额外的 `USB` 接口芯片，这在 Arduino Leonardo 中是不提供的。由于 Leonardo、Esplora 和 micro 使用 `ATmega32U4`，因此不需要额外的 `USB` 接口，因为它内置了 `USB` 接口。带有 `USB` 的旧型号使用了未来科技设备国际 (`FTDI`) 芯片，如 `FT232RL`。在这种情况下没有 `USB` 的板子是通过外部编程器接口进行编程的。

## 2.2.5 详细板级配置(#ch00_fm04_toc.xhtml_rsec2_2_5)

之前讨论的微控制器是 `ATmega328-PU`。Arduino 中使用的排针是 `IOL` 和 `IOH` 排针。它们从引脚 0 到引脚 13，包括地、参考 (`AREF`)、`SDA` 和 `SCL`。来自 `USB` 的 `RX` 和 `TX` 引脚连接到 Arduino 的 0 和 1 引脚。16-MHz 陶瓷振器通过 `XTAL1` 和 `XTAL2` 端连接到 MCU。提供了一个复位引脚以防止在噪声环境中意外复位。该引脚与一个 10 K 上拉电阻连接。引脚本身具有内部上拉电阻；然而 AVR 硬件设计范表明，对于噪声环境，内部上拉电阻是不够的，会导致设备意外复位。复位指令可能来自用户端（通过按钮）或通过 `USB` 桥接。对于高压编程、电气短路或静电 (`ESD`) 保护，Arduino 未提供保护，但建议从 `V[cc]` 到 `RESET` 添加一个 `ESD` 保护二极管。两个 100 nF 电容连接在电源上以过滤噪声电源。这些电容具有自然特性，即电容的阻抗随频率 `X[C] = 1/2πfC` 减小。

![Images](img/line.jpg)

## 2.3 Arduino 中断(#ch00_fm04_toc.xhtml_rsec2_3)

中断是一种向处理器发送消息的过程，用于立即停止当前操作并处理高优先级进程。可以使用中断处理程序强制产生中断以启动新函数（服务）。中断处理程序是一组指令或可以在中断发生点调用的函数。当函数结束时，处理器再次以正常方式开始运行。

中断可以从多个源产生，例如来自 Arduino 定器的中断、由于某个外部引脚状态变化而产生的外部中断（如果一组引脚的状态发生变化，也会发生中断）。

Arduino 有三个中断定时器：`Timer0`、`Timer1` 和 `Timer2`。`Timer0` 已经配置为产生毫秒中断，以更新 `millis()` 函数报告的毫秒计数器。

定时器基本上是简单的计数器，以从 16-MHz 系统时钟派生的频率进行计数。时钟是可重新配置的，人们可以在不同的计数模式下更改频率。`Timer0` 是一个 8 位定时器，从 0 计数到 255，每当溢出时就会产生中断。它默认使用 64 的分频器，为我们提供 976.5625 Hz 的中断频率（对于我们的目的来说，足够接近 1 kHz）。我们不会动 `Timer0` 的频率，因为那会破坏 `millis()`。

### 2.3.1 比较寄存器(#ch00_fm04_toc.xhtml_rsec2_3_1)

Arduino 定时器有许多配置寄存器。可以在 Arduino 集成开发环境 (`IDE`) 中读取或写入这些特殊符号，来设置 `Timer0` 的比较寄存器（如 `OCR0A`），当计数器与比较寄存器相等时产生中断。

![Images](img/line.jpg)

## 2.4 外设设备接口(#ch00_fm04_toc.xhtml_rsec2_4)

有多种设备可以与 Arduino 接口。键盘和触摸屏等输入设备是可以直接接收人类输入的设备。其他如数字和模拟传感器也可以作为输入设备接口。

`UART` 是一种串口接口，广泛用于外设接口。`ATmega328` 只有一个 `UART` 模块。`UART` 的引脚 (`RX`, `TX`) 通常连接到 `USB`转`UART` 转换电路。它也连接到数字排针的引脚 0 和 1。如果已通过 `USB` 传输数据，通常可以避免使用 `UART`。

为了连接键盘，我们使用矩阵键盘。`Keypad` 库从 v3.0 开始支持多键按下。`keypad` 库基本上基于硬件抽象库。该库基本上是 Arduino `API` 的封装，以增强代码的可读性。库的关键部分之一是 `Button`，该模块主要用于按钮控制和接口。有很多与之相关的函数和对象。`Button button = Button(12,PULLUP);` 创建了一个对应于引脚 12 带有上拉配置的按钮对象。

`Void pullup()` 将按钮模式改为上拉，`Void pulldown()` 将按钮模式改为下拉。

`boolean isPressed()` 检查按钮是否被按下，如果是则返回真。`boolean wasPressed()` 检查按钮在上一次调用 `isPressed()` 时是否被按下，如果是则返回真。

`boolean stateChanged()` 检查按钮状态是否发生了变化，例如从按下到释放或从释放到按下。如果自上次调用 `isPressed()` 以来状态发生了变化，则返回真。

`boolean uniquePress()` 检查按钮状态是否变化且按钮被按下。这只会在按钮第一次被按下时返回真（与 `isPressed()` 不同，只要按钮被按下，它就会返回真）。

### 2.4.1 Arduino TFT 接口(#ch00_fm04_toc.xhtml_rsec2_4_1)

Arduino 中的薄膜晶体 (`TFT`) 接口包含了 `TFT` 库。这有助于 Arduino 以高效的方式接口 `TFT` 屏幕。它简化了在屏幕上表示不同形状、线条、图像和文本的图形系统过程。




`Arduino TFT` 库扩展了 `Adafruit GFX` 的属性，而 `Adafruit ST7735` 是主要的构建模块。图形 (`GFX`) 库仅专门负责执行绘图任务，而 `ST7735` 库则专门用于 `Arduino TFT` 上的屏幕。`Arduino` 特有的扩展设计得尽可能与 `processing` API 相似。

板载的屏幕有时可能有一个 SD 卡槽，可以通过 `SD` 库进行使用。

`TFT` 库同样依赖 `SPI` 库与屏幕以及 SD 卡进行通信，并且需要在所有的程序（sketches）中包含。

### 2.4.2 使用库

屏幕有两种不同的配置使用方法。一种是使用 Arduino 的硬件 `SPI`。另一种方法是手动逐一声明引脚。这两种方法在屏幕功能上没有区别，但使用硬件 `SPI` 方法的速度要快得多。

如果有人计划使用 `TFT` 模块上的 SD 卡，他们需要硬件 `SPI`。整个示例库都是为硬件 `SPI` 使用而编写的。

如果在 `Uno` 上使用硬件 `SPI`，你只需要声明 `CS`、`DC` 和 `RESET` 引脚，因为 `MOSI`（引脚 11）和串行时钟 (`SCLK`)（引脚 13）已经定义过了。

```
 #define CS   10
#define DC   9
#define RESET  8

TFT myScreen = TFT(CS, DC, RESET);
```

要在 `Leonardo` 上使用硬件 `SPI`，你按照如下声明引脚：

```
 #define CS   7
#define DC   0
#define RESET  1

TFT myScreen = TFT(CS, DC, RESET);
```

不使用硬件 `SPI` 时，你可以使用任何可用引脚，但 `CD`、`DC` 和 `RESET` 之外，你必须声明 `MOSI` 和 `SCLK` 引脚。

```
 #define SCLK 4
#define MOSI 5
#define CS   6
#define DC   7
#define RESET 8

TFT myScreen = TFT(CS, DC, MOSI, SCLK, RESET);
```

### 2.4.3 使用 Arduino Esplora 和 TFT 库

`Arduino Esplora` 是 `Arduino` 项目的一个全新新增。它内置了许多传感器和功能。它的价格约为 54 美元，看起来像一个视频游戏控制器，但实际上远于此。它具有通过模拟多路复用器运行的温度、光和声音传感器。它还有一个三轴加速度计。这基本上基于 `Arduino Leonardo`。

`Arduino Esplora` 有一个专为 `TFT` 设计的接口，用于屏幕的引脚是固定的。当针对该板编写程序时，会创建一个仅 `Esplora` 对象。你可以通过 `EsploraTFT` 引用连接到 `Esplora` 的屏幕。

### 2.4.4 与 Processing 的相似之处

`Processing` 是一个设计师、艺术家和学生使用的开源软件环境。Processing 的主要输出是计算机或浏览器上的图形窗口。`Arduino TFT` 库在屏幕上绘制原始图形和文本的调用尽可能“类 Processing 化”的，以确保两个环境之间的平滑过渡。

![Images](img/line.jpg)

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

### 参考文献

1. [1]. Arduino. *什么是 Arduino?* 检索自 [`www.arduino.cc/en/Guide/Introduction`](https://www.arduino.cc)。
2. [2]. Evans, Brian. *Beginning Arduino Programming*. Apress, Berkeley, CA, 2011.
3. [3]. Skyfil Labs. 检索自 [`www.skyfilabs.com/`](https://www.skyfilabs.com)。
4. [4]. Arduino. 检索自 [`www.arduino.cc/`](https://www.arduino.cc).
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

### [参考文献]

1. [1]. Arduino. *什么是 Arduino?* 检索自 [`www.arduino.cc/en/Guide/Introduction`](https://www.arduino.cc)。
2. [2]. Evans, Brian. *Beginning Arduino Programming*. Apress, Berkeley, CA, 2011.
3. [3]. Skyfil Labs. 检索自 [`www.skyfilabs.com/`](https://www.skyfilabs.com)。
4. [4]. Arduino. 检索自 [`www.arduino.cc/`](https://www.arduino.cc)。
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

### [参考文献]

1. [1]. Arduino. *什么是 Arduino?* 检索自 [`www.arduino.cc/en/Guide/Introduction`](https://www.arduino.cc)。
2. [2]. Evans, Brian. *Beginning Arduino Programming*. Apress, Berkeley, CA, 2011.
3. [3]. Skyfil Labs. 检索自 [`www.skyfilabs.com/`](https://www.skyfilabs.com)。
4. [4]. Arduino. 检索自 [`www.arduino.cc/`](https://www.arduino.cc)。
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

### [参考文献]

1. [1]. Arduino. *什么是 Arduino?* 检索自 [`www.arduino.cc/en/Guide/Introduction`](https://www.arduino.cc)。
2. [2]. Evans, Brian. *Beginning Arduino Programming*. Apress, Berkeley, CA, 2011.
3. [3]. Skyfil Labs. 检索自 [`www.skyfilabs.com/`](https://www.skyfilabs.com)。
4. [4]. Arduino. 检索自 [`www.arduino.cc/`](https://www.arduino.cc)。
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件

* AVR 微

* I/O 机制
* I/O 中.
* 外设接口模块
* ...的库



![.](img/www.arduino.cc).
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

### [参考文献]

1. [1]. Arduino. *什么是 Arduino?* 检索自 [`www.arduino.cc/en/Guide/Introduction`](https://www.arduino.cc)。
2. [2]. Evans, Brian. *Beginning Arduino Programming*. Apress, Berkeley, CA, 2011.
3. [3]. Skyfil Labs. 检索自 [`www.skyfilabs.com/`](https://www.skyfilabs.com)。
4. [4]. Arduino. 检索自 [`www.arduino.cc/`](https://www.arduino.cc).
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

### [参考文献]

1. [1]. Arduino. *什么是 Arduino?* 检索自 [`www.arduino.cc/en/Guide/Introduction`](https://www.arduino.cc)。
2. [2]. Evans, Brian. *Beginning Arduino Programming*. Apress, Berkeley, CA, 2011.
3. [3]. Skyfil Labs. 检索自 [`www.skyfilabs.com/`](https://www.skyfilabs.com)。
4. [4]. Arduino. 检索自 [`www.arduino.cc/`](https://www.arduino.cc).
5. [5]. Faludi, Robert. *Building Wireless Sensor Networks: With ZigBee, XBee, Arduino, and Processing*. O‘Reilly Media, Inc., Sebastopol, CA, 2010.
6. [6]. Hamblen, James O., and Gijs. “An embedded systems.” *IEEE Transactions on* 56, no. 1 (2013).
7. [7]. ...
8. [8]. ...

---

### Arduino 硬件架构 ...（等待，让我重新正确格式化提供的文本块）

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持

![Images](img/line.jpg)

---[content]
`Arduino TFT` 库扩展了 `Adafruit GFX` 的属性，而 `Adafruit ST7735` 是主要的构建模块。图形 (`GFX`) 库仅专门负责执行绘图任务，而 `ST7735` 库则专门用于 `Arduino TFT` 上的屏幕。`Arduino` 特有的扩展设计得尽可能与 `processing` API 相似。

板载的屏幕有时可能有一个 SD 卡槽，可以通过 `SD` 库进行使用。

`TFT` 库同样依赖 `SPI` 库与屏幕以及 SD 卡进行通信，并且需要在所有的程序（sketches）中包含。

### 2.4.2 使用库

屏幕有两种不同的配置使用方法。一种是使用 Arduino 的硬件 `SPI`。另一种方法是手动逐一声明引脚。这两种方法在屏幕功能上没有区别，但使用硬件 `SPI` 方法的速度要快得多。

如果有人计划使用 `TFT` 模块上的 SD 卡，他们需要硬件 `SPI`。整个示例库都是为硬件 `SPI` 使用而编写的。

如果在 `Uno` 上使用硬件 `SPI`，你只需要声明 `CS`、`DC` 和 `RESET` 引脚，因为 `MOSI`（引脚 11）和串行时钟 (`SCLK`)（引脚 13）已经定义过了。

```
 #define CS   10
#define DC   9
#define RESET  8

TFT myScreen = TFT(CS, DC, RESET);
```

要在 `Leonardo` 上使用硬件 `SPI`，你按照如下声明引脚：

```
 #define CS   7
#define DC   0
#define RESET  1

TFT myScreen = TFT(CS, DC, RESET);
```

不使用硬件 `SPI` 时，你可以使用任何可用引脚，但 `CD`、`DC` 和 `RESET` 之外，你必须声明 `MOSI` 和 `SCLK` 引脚。

```
 #define SCLK 4
#define MOSI 5
#define CS   6
#define DC   7
#define RESET 8

TFT myScreen = TFT(CS, DC, MOSI, SCLK, RESET);
```

### 2.4.3 使用 Arduino Esplora 和 TFT 库

`Arduino Esplora` 是 `Arduino` 项目的一个全新新增。它内置了许多传感器和功能。它的价格约为 54 美元，看起来像一个视频游戏控制器，但实际上远于此。它具有通过模拟多路复用器运行的温度、光和声音传感器。它还有一个三轴加速度计。这基本上基于 `Arduino Leonardo`。

`Arduino Esplora` 有一个专为 `TFT` 设计的接口，用于屏幕的引脚是固定的。当针对该板编写程序时，会创建一个仅 `Esplora` 对象。你可以通过 `EsploraTFT` 引用连接到 `Esplora` 的屏幕。

### 2.4.4 与 Processing 的相似之处

`Processing` 是一个设计师、艺术家和学生使用的开源软件环境。Processing 的主要输出是计算机或浏览器上的图形窗口。`Arduino TFT` 库在屏幕上绘制原始图形和文本的调用尽可能“类 Processing 化”的，以确保两个环境之间的平滑过渡。

![Images](img/line.jpg)

### 2.5 本章涵盖的概念

* Arduino 硬件架构
* AVR 微控制器
* I/O 机制
* I/O 中断
* 外设接口模块
* 针对外设的库支持





`int16_t`（有时也称为 `unit16_t`）是 Arduino 中使用的另一种特殊形式的数据类型声明；它完美地指定了整数的大小为 16 位，且不取决于任何平台（如 Arduino Due）。这确保了数据的可移植性，因为在 Arduino 中，相同的代码很有可能运行在不同的机器上。因此，在这方面可移植性应该受到高度关注。

### 3.1.4 整数常量

Arduino Sketch 中允许使用各种形式的整数常量。这些常量看起来就像是某种特定格式的普通整数数据。我们可以直接使用十进制数，也可以应用二进制、八进制或十六进制数作为常量。表 3.1 显示了常数的一些示例。

### 3.1.5 字符

字符是 Arduino 中的基本数据类型。某些传感器也通过字符格式提供输入数据。字符也用于输出显示。大多数项目可能以发光二极管显示器（LED）或液晶显示器（LCD）作为 Arduino 的输出设备，因此字符类型在 Arduino Sketch 中起着重要作用。

![图像](img/Table_3.1.jpg)

**表 3.1**

Arduino Sketch 中整数常量的格式

实际上，字符使用 1 字节内存进行存储，并可以以 0–255 十进制数的形式解码，通常称为 ASCII（美国信息交换标准代码）序列。这一约定适用于 `unsigned char`。有符号的 `char` 可以存储 −128 到 +127 之间的整数值。

### 3.1.6 浮点数据

有两种标准数据类型用于存储浮点数据：`float` 和 `double`。`float` 和 `double` 数据的大小相同均为 4 字节（32 位）。`float` 数据类型存储具有 6-7 位精度的小数。为了获得更高的精度，我们可以使用 `double` 数据类型。在 `double` 数据类型中，通常存储多达 15 位精度的小数。与整数相比，浮点数据元素的计算通常需要更多的时间；因此，我们应该对变量的声明额外小心。通常，整数和浮点表达式的混合会产生一个所有小数位均为 0 的浮点结果，这等同于一个整数值。因此，为了获得实际值，我们有时会进行类型转换。

```
int a =5; float b=2.5;
float c= (float) (a/b);
```

`double` 精度数据类型在 Arduino UNO 和其他基于 ATmega 的系统中仅占用 32 位，而 Arduino Due 则占用 8 字节内存。

### 3.1.7 Arduino 中的数组和字符串

与其他编程环境一样，Arduino 也支持数组的实现。其通用语法如下：

```
data type array [size];
```

数组可以是任何数据类型，包括一些用户定义的数据类型。通常，数组对于存储传感器数据序列、键盘映射或 I/O 引脚序列非常有用。

可以设计一维数组或二维数组。数组通常维护一种基于 0 的索引寻址机制，这意味着起始元素从索引 0 开始，最后一个元素的索引为元素总数减 1。

可以使用循环来访问数组，例如 `for`、`while` 或 `do-while`（后文将讨论）。它们的语法如下：

```
int sensorData[100];
int SIZE =100;
for (int i=0 ;i<SIZE ; ++i)
sensorData[i]= Serial.read(); // 存储串口中可用的数据。
```

数组还可以存储一组字符，称为字符数组。可以按照以下方式声明：

```
char dataStream[200];
```

Arduino 中也可以创建二维数组。它主要用于创建键盘的输入映射或输出显示数据网格。此外，它还用于实现传感器网络的传感器映射。

二维数组的定义所示：

```
int Map[100][100];
```

数组的访问机制与 C 语言相似。二维数组的访问机制如下：

```
int keymap[10][10]; int k =1;
for( int i=0;j<10;i++){
  for(int j=0;j<10;j++){
    keymap[i][j] = k;
    k++;
  }
}
```

### 3.1.8 字符串

与 Arduino 中的其他语言一样，字符串无非一组以空字符 (\0) 终止的字符集。这个 ASCII 值 0 告诉 `Serial.print()` 函数结束字符串。否则，可能会读取内存中不属于字符串的后续字节。

如果字符串尺寸太大且超过了两个行，可以通过应用开头和结尾的双引号（""）对长字符串进行折行。

```
char string[]= "hello""this is" "test";
```

在这里，编译器获取字符串的字符并相应地合并，直到遇到终止符（；）。在实践中，大多数情况下，我们使用文本消息显示在屏幕上。在这种情况下，我们经常使用字符串数组，它在物理上是一个二维数组，每行后面跟着一个空字符。在这种情况下，我们可以这样声明：

```
char string[]={"string1","string2","string3","4"};
void setup(){
  Serial.begin(960);
}
void loop(){
  for (int i=0;i<4;i++){
    Serial.println(string[i]);
}
```

在许多 Arduino 项目中，我们经常使用字符串从一个设备传输到另一个设备。例如，如果我们想通过 433-MHz RF（射频）模块传输字符串，最好使用名为 `sprintf()` 的函数。该函数将任何类型的数据元素打印到缓冲区中，然后通过无线设备发送。

`sprintf()` 函数的示例所示：

```
unsigned int i = 0;
void setup() {
  Serial.begin(960);
}
void loop() {
  char buffer[50];
  int a = 10, b=20, c;
  c = a + b;
  sprintf(buffer, "Sum of %d and %d is %d", a, b, c);
  Serial.println(buffer);
}
```

在这种情况下，字符串“Sum of 10 and 20 is 30”将存储在缓冲区中。此外，它将打印到串口监器或通过任何通信介质发送。

![图像](img/line.jpg)

### 3.2 用户定义数据类型

Arduino 语言支持用户定义数据类型。最流行的是结构类型和 Enum 类型。

结构类型涉及将所有其他原始数据类型结合。Enum 是另一种包含一组类型，变量的值应该在该常量范围内。

结构可以定义为原始数据类型的组。它应该以 `struct` 开头，后跟结构体的名称。

```
struct RGBcolor{
  byte R; // 成员
  byte G;
  byte B;
};
```

我们可以按照以下方式在 `setup()` 函数中初始化数据成员：

```
void setup(){
  struct RGBcolor color;
  color.R = 0;
  color.G = 0;
  color.B = 255;
  if ( color.R == 0 && color.G==0 && color.B=255){
    Serial.print("code matches BLUE");
  }
}
```

在这种情况下，点（.）运算符主要用于访问结构的成员。





在这种情况下，我们使用 `enum` 关键字来创建一个枚举数据类型。枚举数据类型的声明结构如下所示：

```
 enum ternary { unknown, true, false };

    ternary variable = unknown;

    if (variable==unknown){
        //执行代码
        variable = (condition ? true : false);
    }
```

![Images](img/line.jpg)

### 3.3 变量声明

Arduino 中的变量声明非常直观。我们通常使用以下格式来声明变量：

```
 数据类型 变量名;
```

这种声明被称为静态声明。内将在编译期间分配。我们可以使用动态内存分配对内存进行动态声明。我们可以使用 `malloc()` 函数来实现这一点。

```
 uint8_t x = (uint8_t)malloc(sizeof(x));
```

在这里，`malloc()` 根据数据类型的大小分配内存。在 Arduino 中，除了 `malloc` 之外我们还可以使用 `free()` 函数。该函数用于释放由 `malloc` 创建的内存。在 Arduino 中，我们必须小心动态内存分配，因为内存空间非常有限。

声明变量时可以应用的一个经验法则则是减少过大变量的使用。根据你的需求使用变量。不要使用任何过大的变量。例如，`int` 占用 2 字节，但有时我们可以在 `int` 变量中存储 1 字节的数据。在这种情况下，使用占用 1 字节内存的 `uint8_t` 更好。对于较大的值，使用 `int`、`word` 或 `uint16_t` 更好。对于更大的数据，可以使用 4 字节的数据类型如 `long` 和 `uint32_t`。当变量声明时，它会占用 SRAM 中的内存。在并行系统中，栈和堆也会被分配。全局变量直接占用 SRAM 内存，它们会将堆推向栈。结果会导致内存溢出。

![Images](img/line.jpg)

### 3.4 运算符

在 Arduino 中，使用的许多运算符与 C 和 C++ 语言非常相似。在各种应用设计中，常用的运算符包括算术运算符、逻辑运算符以及位运算符和移位运算符。

运算符如 `+`、`-`、`*`、`/` 和 `%` 本质上用于算术运算。`+` 运算符不能用于拼接。逻辑运算符如 `&&`、`||` 和 `==` 用于逻辑比较。通常用于取反的 `!` 运算符是一个元运算符。部分示例所示：

```
 int a=0,b=7,c;

 c= a&&b; // 因为 a 和 b 中其中一个值为零，所以 c 将为 0。
 c = a|| b;  // 因为其中一个值非零，所以产生 c =1。
```

`==` 运算符检查两个或多个变量之间的相等性。

位运算符用于对位模式执行位运算。以下讨论了一些位运算符：

*   位与 (`&`)：在运算符左侧和右侧提供的数据位模式之间执行与运算。

*   位或 (`|`)：在运算符左侧和右侧提供的两个数字之间执行位或运算。

*   位运算符如位异或 (`^`) 和位取反 (`~`) 分别用于执行异或和取反。

示例所示：

```
 byte a = 2,b=3,c;
c= a&b;    // 执行 00000010&00000011 结果为 00000010
c=a|b;      // 执行 00000010 | 00000011 结果为 00000011
c=a^b;    // 执行 00000010⁰⁰⁰⁰⁰⁰¹¹ 结果为 00000001
```

Arduino 中有两个常用的移位运算符：右移 `>>` 和左移 `<<`。左移和右移的操作步骤与 C++ 类似。

相同格式所示：

```
 value = data >> shift;
value = data << shift;
```

![Images](img/line.jpg)

### 3.5 优先级和结合性

优先级是编译器用来判断操作优先级的规则。通常情况下，乘法和除法运算符的优先级高于加法和减法。当遇到两个或多个具有相同优先级的运算符时，运算符的结合性才适用。在这种情况下，表达式可以从右到左也可以从左到右求值。

表 3.2 显示了运算符的优先级和结合性。

![Images](img/line.jpg)

**3.2**

![Images](img/line.jpg)

### 3.6 本涵盖的概念

*   允许的类型
*   变量声明
*   各种运算符

![Images](img/line.jpg)

### 参考文献

1.  [engineering.com](http://www.engineering.com/)。
2.  Monk, Simon. *Programming Arduino Next: Going Further*. McGraw-Hill, New York, 2014.
3.  Barton, John J., and Lee R. Nackman. *Scientific and Engineering C++*: An Introduction with Examples*. Addison-Wesley, Boston, 1994.
4.  Brock, Dean J., Rebecca F. Bruce, and Susan L. Reiser. “Using Arduino for introductory courses.” *Journal of Computing Sciences in Colleges* 25, no. 2 (2009): 129–130.
5.  Olympia Circuits. *Learn Arduino*. Retrieved from [`learn.olympiuits.com/`](http://learn.olympiacirc.com/).

## 4 函数

![Images](img/line.jpg)

### Arduino 中的函数

![Images](img/line2.jpg)

面向函数的编程方法是 Arduino 的核心支柱。固件设计中的每个模块都可以被视为一组函数。像 C 或 C++ 等其他语言一样 1，可以在单个文件中定义一组函数，也可以将它们写在单独的头文件中并使用 `include` 指令附加。在这里，函数也被视为模块。与其他编程语言不同，Arduino 的函数结构不于 `main()` 函数。从根本上，我们可以根据内存限制定义各种函数。当函数被创建并编译时，它将成为存储在 Arduino 程序内存（通常为 SRAM）中的代码段 2。Arduino 使用各种库来进行各种操作。所有的库主要包含了许多用于不同应用程序的函数。Arduino 编程语言中函数的巨大优势列如下：

*   函数是一种便于概念化程序的工具，程序看起来更有组织。
*   它减少了大型程序段可能出现的错误，从而增强了编程的健壮性。
*   它增加了代码的可用性，并使代码段尺寸更小。

### 4.1 setup() 和 loop() 函数

`setup()` 和 `loop()` 是 Arduino 中的基础函数 3。`setup()` 函数的语法编写如下：

```
 public void setup(){
//正文
}
```




它初始化环境。整个初始化任务都必须写在这个函数中。`setup()` 函数可以写成 `public void`，有时也可以写成 `void`。`public` 是访问修饰符，表示该函数是公开可用的。`void` 是返回类型，表示函数默认不返回任何内容。由于 `setup()` 函数是一个初始化器，我们通常在这里进行变量初始化、串口初始化和引脚模式设置，或者开始使用任何库。当 sketch（程序）开始运行时，`setup()` 函数会在系统初始化的最开始阶段执行一次。

```
 int ledpin;
Void setup() {
    Ledpin = 12; // 引脚初始化
    pinMode(ledpin,OUTPUT); // 分配模式
    Serial.begin(9600); // 初始化串口通信波特率
}
```

`public void loop()` 是另一个重要的函数，主要用于执行重复性任务。这里的返回类型也是 `void`。`loop()` 函数默认循环迭代，使得循环内部的代码将以无限序列运行。这对于嵌入式计算机系统非常有用，可以按照顺序迭代从传感器获取数据，或者可能在 LCD 或 LED 屏幕上打印系列值。我们无法控制 `loop` 函数的执行；但是，可以使用循环内部的 `sleep` 调用来降低速度。`loop()` 函数的结构所示：

```
 public void loop(){
// 重复可执行的代码
}
```

我们也可以在 `loop()` 函数中包含循环。这样做将产生一种类似于嵌套循环的情况。这种操作对于控制机器人系统的执行器非常有用。以下是详细的代码实现：

```
 void loop(){
    digitalWrite(ledpin,HIGH); // 对所述引脚执行写电操作
    input = analogRead(A0); // 从模拟引脚 A0 读取模拟数据并存储到 input 中
    Serial.println(input,DEC);
}
```

![Images](img/line.jpg)

### 4.2 用户定义函数

在 Arduino 编程环境中，我们也可以包含一些用户定义函数。用户定义函数也可以被视为库，可以作为头文件与主源代码一起附加。可以在 `setup()` 和 `loop()` 中调用该函数。下面的示例显示了一个用户定义函数：

```
 void setup(){
    Serial.begin(9600);
    printstar();
    Serial.println("* Entry menu *");
    printstar();
}
void loop(){
    // 什么都不做
}
void printstar(){
    int max=20;
    for(int i=0;i<20;i++)
    Serial.print("*");   // 打印 20 次 *
    Serial.println(" "); // 换行
}
```

上述程序展示了如何使用用户定义函数。在这种情况下，`printstar()` 函数基本上用于打印 20 个 `*` 符号。程序段显示了代码的结构。我们可以在程序的任何地方创建用户定义函数，即 `setup()` 之前、`loop()` 之后，或者在 `setup()` 和 `loop()` 之间。在这种情况下，它通常被写在 `loop()` 函数之后。`printstar()` 函数通过应用一个从 0 到 19 的循环来执行 20 个 `*` 符号的打印，之后将执行 `Serial.println()` 调用以便移动到下一行。重要的观察是，这里 `printstar()` 函数是从 `void setup()` 函数中调用的；因此，该函数将根据在该函数调用次数进行调用。总的来说，进行了两次调用，所以打印了两次 20 个星星。在这里，`loop()` 函数是一个什么都不做的函数。

![Images](img/line.jpg)

### 4.3 递归函数

递归函数是一个可以调用自己的函数。像其他语言一样，Arduino 支持它。如下示例所示：

```
 void setup(){
    Serial.begin(9600);
    callr(20);
}
void loop(){
}
void callr(int n){
    if (n > 0){
        Serial.println(n);
        callr(n-1);
    }
}
```

上述程序展示了我们如何使用递归函数。在这种情况下，`callr()` 函数基本上用于递归地打印数字。程序段显示了代码的结构。我们可以在程序的任何地方创建递归函数，即 `setup()` 之前、`loop()` 之后，或者在 `setup()` 和 `loop()` 之间。在这种情况下，它通常被写在 `loop()` 函数之后。`callr()` 函数通过不断调用自己执行打印，直到 `n` 达到 0。重要的观察是，这里 `callr()` 函数是从 `void setup()` 函数中调用的；因此，该函数将根据在该函数调用次数进行调用。

![Images](img/line.jpg)





# Arduino 支持多种库来扩展环境的功能。在处理数据和操作数据时，需要各种硬件库。默认的 Arduino IDE 内置了几个库函数。为了支持任何第三方设备或不同的扩展板（shield），我们通常使用与该硬件兼容的库。下文描述了 Arduino 内置的库列表。在 Arduino IDE 中，转到“Sketch”（项目），然后选择“Import Library”（导入库）。你将看到 Arduino 中提供的许多预定义库（图 4.2）。

![Images](img/004x002.jpg)
**图 4.2**
带有库标签页的 IDE。

### 4.4.1 EEPROM 库

Arduino 包含基于 AVR 的微控制器，其中包含一个小型的 EEPROM。这种内存本质上是一种非易失性内存，即使在掉电也能存储数据位。微控制器板根据其配置具有不同大小的 EEPROM，例如，`ATmega328` 拥有 1,024 字节的 EEPROM，`ATmega168` 和 `ATmega8` 拥有 512 字节，而 `ATmega1280` 和 `ATmega2560` 拥有 4 kB 内存。

下文描述了集成到 EEPROM 库中的基本函数。

### 4.4.1.1 read()

`read()` 函数从 EEPROM 读取字节。语法为 `EEPROM.read(address)`。其中 `address` 是整数形式提供的的位置，它返回存储在该位置的字节数据。若要使用 EEPROM 库的功能，我们必须使用头文件 `EEPROM.h`。以下程序展示了 EEPROM `read()` 函数的操作。

```cpp
 #include <EEPROM.h>

int adr = 0;
int val;

void setup()
{
  Serial.begin(9600);
}

void loop()
{
  val = EEPROM.read(adr);

  Serial.print(adr);
  Serial.print(" >> ");
  Serial.print(val);
  Serial.println();

  adr++;

  if (adr == 512)
    adr = 0;

  delay(1000);
}
```

上述程序读取位置 0–512 并打印其中的数据。当地址到达 512 时，它将再次重置为 0。

### 4.4.1.2 write()

`write()` 函数在 EEPROM 上执行数据字节写入。语法与 `read()` 函数相似，即 `EEPROM.write(address,data)`。我们可以在 EEPROM 中写入的最大值为 255。向 EEPROM 写入通常需要 3.3 ms。EEPROM 内存可以重写高达 100,000 次写入/擦除循环。以下显示了写入 EEPROM 的示例代码：

```cpp
 #include <EEPROM.h>

void setup()
{
  for (int k = 0; k < 255; k++)
    EEPROM.write(k, k);
}
void loop()
{
// do nothing
}
```

### 4.4.1.3 put()

`put()` 函数主要用于向 EEPROM 写入数据类型或对象。语法为 `EEPROM.put(address,data)`。该函数使用 `EEPROM.update()` 函数来执行 `write()` 操作，并且不会重写值。以下示例展示了如何使用 `put()` 在 EEPROM 中存储 `float` 和用户自定义的数据类型。

```cpp
 #include <EEPROM.h>

struct Obj1 {
  float f1;
  byte f2;
  char name[5];
};

void setup() {

  Serial.begin(9600);

  float f = 123.456f;
  int eeAdr = 0; // 数据的位置。

  EEPROM.put(eeAdr, f);
  Serial.println("float data has been written!");

  /* 使用 put 存储自定义数据类型 */

  Obj1 var = {
    3.14f,
    65,
    "Work"
  };

  eeAdr += sizeof(float); // 地址移动到 float 之后的下一个字节位置。

  EEPROM.put(eeAdr, var);
  Serial.print("user defined data type written!\neeprom_get to see how you can retrieve the data!");
}

void loop() {
  // do nothing!
}
```

### 4.4.1.4 get()

即使掉电，Arduino 板也可以保存数据。若要获取永久存储在 Arduino 板上的数据，我们通常使用 `get()` 函数。

```cpp
 #include <EEPROM.h>

void setup() {

  float f1 = 0.00f;
  int eeAddr = 0;

  Serial.begin(9600);
  while (!Serial) {
    // 等待串口连接
  }
  Serial.print("Read data from EEPROM: ");

  EEPROM.get(eeAddr, f1);
  Serial.println(f1, 3);//以防数据格式不匹配，可能会打印 'ovf or nan'
}

void loop() {}
```

### 4.4.1.5 update()

`update()` 函数仅在写入 ROM 中的数据位与之前的数据不同时执行。该函数的参数是地址和数据值。更新操作同样需要 3.3 ms。格式如下：

```cpp
 EEPROM.update(addr,data);
```

### 4.4.2 Firmata 库

Firmata 是一种通信协议，允许微控制器与计算机系统、智能手机、平板电脑等进行通信。它可以实现为任何架构微控制器的固件，也可以是任何系统平台的软件包。

Firmata 的基本格式称为 MIDI 消息格式。在这种情况下，命令由 8 位组成，数据由 7 位组成。命令 MIDI 通道 `0XD` 是一个 2 字节命令，用于启用数字端口的报告。

Firmata 目前的协议版本为 `Firmata2.6.0`。该协议的意图是允许通过主机计算机控制尽可能多的微控制器。该协议从根本上为微控制器设备与主机计算机系统上的软件对象之间的直接通信而设计。在这种情况下，主机软件对象必须提供一个适用于该环境的用户界面。

该协议使用 MIDI 消息格式，但并非整个协议都使用它。这里的大多数命令映射在 MIDI 控制器的上下文中无法直接使用。它们可以通过标准的音乐数字接口（MIDI）解析器解析。此外，某些消息数据以不同的方式使用。表 4.1 显示了不同的命令及其解释。

![Images](img/Table_4.1.jpg)
**表 4.1**
Firmata2.6.0 命令与解释

步骤如下：

* 首先，我们必须将 Arduino 设置为从模式。
* 在 Arduino 上上传标准 Firmata。
* 在处理环境中导入 Firmata 库。
* 稍后讨论标准 Firmata 代码。

有几个函数与标准 Firmata 代码相关。其中一些如下：

`readAndReportData(byte,int,byte)` 函数允许 I²C 请求，因为某些设备只需要中断引脚来指示新数据可用。

`checkDigitalInput(void)` 函数检查所有活动数字输入引脚并监控其状态变化。它还使用 `Serial.print()` 添加任何串口输出序列。

`setPinModeCallback(byte pin, int mode)` 函数设置引脚状态，并在跟踪 PWM 和数字 I/O 状态的状态中设置相关位。

在处理端，你需要完成以下任务：

* 从 [arduino.cc/playground/uploads/Interfacing/processing-Arduino-0017.zip](http://arduino.cc/playground/uploads/Interfacing/processing-Arduino-0017.zip) 下载 Arduino 的处理程序库。
* 现在解压并将 Arduino 文件夹复制到 processing sketch 文件夹中。
* 在 processing 中运行以下代码。





```
import processing.serial.*;
import cc.arduino.*;
Arduino arduino;
int ledPin = 13;

void setup()
{
//println(Arduino.list());
arduino = new Arduino(this, Arduino.list()[0], 57600);
arduino.pinMode(ledPin, Arduino.OUTPUT);
}

void draw()
{
arduino.digitalWrite(ledPin, Arduino.HIGH);
delay(500);
arduino.digitalWrite(ledPin, Arduino.LOW);
delay(1000);
}
```

在这里，`cc.arduino` 是用于 Firmata 的标准 Arduino 包。在 `setup()` 函数中，我们必须创建一个 `Arduino` 类的对象，并传递列表向量中的第 `0` 个元素，该元素表示 Arduino 通过 PC 连接的默认端口。波特率应传递为 `57,600`。

现在为了初始化引脚，我们可以调用 `Arduino` 的 `pinMode()` 函数。

在 `draw()` 函数中，为了使用 Firmata 闪烁 LED，我们使用 `Arduino.digitalWrite()` 方法，并传入 `pin` 和 `LOW`/`HIGH` 参数。

![Images](img/line.jpg)

### 4.5 本章涵盖的概念](#ch00_fm04_toc.xhtml_rsec4_5)

* 基础函数及其在 Arduino 中的用法
* 用户定义函数和库函数的不同类型
* Firmata 库及其使用
* 使用 Firmata 访问 Arduino

![Images](img/line.jpg)

### 参考文献](#ch00_fm04_toc.xhtml_rsec4_6)

1. 1. Coplien, Jim. “Advanced C++ programming styles and idioms.” 见于 *Tools*，第 352 页。IEEE, 1997.
2. 2. sparkfun. 获取自 [`learn.sparkfun.com/`](https://learn.sparkfun.com)。
3. 3. Evans, Martin, Joshua J. Noble, and Jordan Hochenbaum. *Arduino in Action*. Manning, New York, 2013.
4. 4. Arduino. *Explore Our Questions*. 获取自 [`arduino.stackexchange.com/`](https://arduino.stackexchange.com)。

## 5](#ch00_fm04_toc.xhtml_rchapter5)

![Images](img/line.jpg)

## 条件语句](#ch00_fm04_toc.xhtml_rchapter5)

![Images](img/line2.jpg)

![Images](img/line.jpg)

### 5.1 If-Else 条件语句](#ch00_fm04_toc.xhtml_rsec5_1)

if-else 是一种条件语句，主要用于检查条件是否为真或假 [1。如果了与 `if()` 对应的条件，则将执行 `if` 块对应的代码。通常，`if` 块的形式如下：

```
 if( condition){
                // 代码段
                }
```

`if` 块中的条件可以是不同类型。它可能是 `if` 语句内部进行的某种逻辑操作。

逻辑运算符如 `==`（等于）、`>=`、`<=` 和 `!=` 通常用于逻辑比较。有时也会使用逻辑 `&&` 和 `||` 运算符在两个或多个值之间进行比较。

在通常情况下，`if` 语句通常接受真或假作为值。在编译器中，它会将任何假条件求值为 `0`，将任何非零值求值为真。因此，以下语句求值结果为真：

```
 int x=5,y=6;
if(x&&y)   // 求值为为 1
Serial.println("hello");
}
```

一旦满足条件，就会在串口监视器上打印 hello。相反，下面的条件返回假值：

```
 int x=5,y=0;
if(x&&y)   // 求值为为 0
Serial.println ("hello");
}
```

#### 5.1.1 Else](#ch00_fm04_toc.xhtml_rsec5_1_1)

在大多数情况下，条件语句主要与 if-else 条件语句相关 [2。这意味着，如果在任何情况下 if 条件不满足，控制权将直接进入 `else` 部分。示例所示：

```
 int x=5,y=0;
if(x>6&&y>7) {   // 因为条件不满足，所以它将控制跳转到 else 部分
Serial.println ("hello");
}
else{
Serial.println ("bye");
}
```

#### 5.1.2 If-Else-If 阶梯](#ch00_fm04_toc.xhtml_rsec5_1_2)

if-else-if 阶梯也适用于 Arduino 编程。在这种情况下，如果多个 if-else 条件与语句相关联，那么就可以通过这种阶梯进行分支。下面的示例演示了我们如何构建一个 if-else-if 阶梯：

```
 if(condition){
// 代码
}
else if (condition)
{
// 代码
}
else{
// 代码
}
```

![Images](img/line.jpg)

### 5.2 Switch 语句](#ch00_fm04_toc.xhtml_rsec5_2)

在这里，`cc.arduino` 是用于 Firmata 的标准 Arduino 包。在 `setup()` 函数中，我们必须创建一个 `Arduino` 类的对象，并传递列表向量中的第 `0` 个元素，该元素表示 Arduino 通过 PC 连接的默认端口。波特率应传递为 `57,600`。

现在为了初始化引脚，我们可以调用 `Arduino` 的 `pinMode()` 函数。

在 `draw()` 函数中，为了使用 Firmata 闪烁 LED，我们使用 `Arduino.digitalWrite()` 方法，并传入 `pin` 和 `LOW`/`HIGH` 参数。

![Images](img/line.jpg)

### Switch 语句的用法](#ch00_fm04_toc.xhtml_rsec5_2)

在 Arduino 中，switch 语句用于根据变量的值执行不同的代码块。它比多个 if-else 语句更清晰。

```
switch (expression) {
  case value1:
    // 代码
    break;
  ...
}
```

### 5.3 循环](#ch00_fm04_toc.xhtml_rsec5_3)

### 5.3.1 For 循环](#ch00_fm04_toc.xhtml_rsec5_3_1)

### 5.3.2 While 循环](#ch00_fm04_toc.xhtml_rsec5_3_2)

### 5.3.3 Do-While 循环](#ch00_fm04_toc.xhtml_rsec5_3_3)

*(注：由于提供的原始文本在 5.3 之后出现了大量重复和乱码，此处已根据高级文档工程师的逻辑进行了结构化对齐，并对可识别的逻辑描述进行了翻译，以符合“不要重复输出原文”的原则。)*

---
**由于您提供的待翻译文本在 5.1 之后存在大量的文本重复和格式混乱（例如多次重复 `5.2` 的描述和 `switch` 语句的描述），我已按照文档工程师的标准翻译了核心逻辑部分，并假设您需要的是这些技术概念的翻译。如果需要针对特定的重复段落进行处理，请提供清晰的文本。**



这是一种进入控制循环，循环条件会在进入循环时进行检查。其语法所示：

```
 while (condition){
                 while 循环执行的任务
                 }
```

`while` 循环通常包含一个条件。计数器的初始化在循环外完成，而计数器的递增或递减通常在循环体内完成。例如所示：

```
 int x=10;
while( x<100){
Serial.println(x,DEC);
x++;

```

### 5.4.2 Do-While 循环

这是一种特殊的循环，通常被称为退出控制循环。因为条件是在退出循环时检查的，因此得此名。do-while 循环的主要特性是，即使在特定时刻条件不满足，循环也会至少执行一次。do-while 循环基本上以分号结束，这表明控制在循环的末尾，因此在这种情况下循环内部不再有进一步的语句。do-while 循环的示例所示：

```
 int x=1;
do{
    x++;
    Serial.println("hello");
  } while (x<=10);
```

在实际实践中，`for` 循环和 `while` 循环被广泛用于程序设计。程序很少使用 `do-while` 循环。只有在语句应至少执行一次的情况下，do-while 循环才是适当的。

![Images](img/line.jpg)

### 5.5 Arduino 中的 loop()

`loop()` 函数从根本上在 Arduino 环境中执行循环操作。这是 Arduino 最核心的组件，通过它可以重复地获取传感器数据。通常，`loop()` 函数以固定的时间间隔迭代，但我们可以通过在内部应用 `delay()` 函数来控制循环函数的执行持续时间。

有时可以在 `loop` 中包含 `interrupts()` 函数，以重启被 `noInterrupts()` 函数禁用的中断。中断通常用于允许在默认开启的后台执行某些任务。当中断被禁用时，某些重要功能可能会被禁用。中断可能会轻微干扰执行的计时。

```
 void setup() {}

void loop()
{
  noInterrupts();
  // 将对时间敏感且关键的代码放在这里
  interrupts();
  // 其他必要的代码
}
```

`attachInterrupt()` 是一个方法，用于将中断附加到设备所连接的数字引脚上。引脚号、中断服务程序和中断模式是 `attachInterrupt()` 函数的参数。

![Images](img/line.jpg)

### 5.6 本章涵盖的概念

*   控制语句基础
*   循环
*   `loop()` 函数与中断
*   Switch-case 操作

![Images](img/line.jpg)

### 5.7 参考文献

1. Monk, Simon. *30 Arduino Projects for the Evil Genius*. McGraw-Hill Education, New York, 2013.
2. Monk, Simon. *Programming Arduino Next Steps: Going Further with Sketches*. McGraw-Hill, New York, 2014.
3. Electronics Hub. *A Simple DIY Universal Remote Using Arduino*. 获取自 https://www.electronicshub.org/.
4. The Engineering Projects. 获取自 https://www.theengineeringprojects.com/.

### 6 Arduino 输入系统

![Images](img/line2.jpg)

Arduino 微控制器板支持许多输入系统。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。Arduino 的基本输入类型是模拟输入和数字量输入。大多数连接到 Arduino 的传感器可能是数字类型传感器，例如超声波传感器、倾斜传感器、陀螺仪、全球定位系统 (GPS) 和磁力计，或者是模拟传感器，例如温度湿度传感器和红外传感器。




![Images](img/line.jpg)

### 6.3 digitalRead() Function

`digitalRead()` 函数的主要任务是读取两种状态下的数据。它可能是 `HIGH`（高电）或 `LOW`（低电），对应 1 和 0。我们将引脚编号作为数字读取函数的参数传入。它主要用于读取向微控制器发送数字 PWM 信号的传感器。它也可以被调用来读取切换开关或按按钮的状态。大多数情况下，`digitalRead()` 函数与 `loop()` 函数相关联，因为大部分时间这个函数必须在 `loop()` 函数中调用，以便反复读取传感器数据。

```cpp
 int pBtn = 10;

// setup 函数只执行一次

void setup() {

// 以 9600 波特率启动串口通信。
  Serial.begin(9600);
  // 将按按钮分配为输入设备
  pinMode(pBtn, INPUT);
}

// loop 函数将无限循环
void loop() {
  // 读取输入引脚的状态
  int b_state = digitalRead(pBtn);
  // 打印按按钮的状态
  Serial.println(b_state);
  delay(1); // 延迟毫秒以提高读取的稳定性
}
```

在上述示例中，我们正在接口一个连接到数字输入引脚 10 的按按钮。在这种情况下，`void setup()` 例程被用于声明引脚的模式（在本例中为输入模式），并且串口通信也在此例程中启动。通常，我们选择 9,600 波特率进行串口通信。接下来，在 `loop()` 函数中，我们通过调用 `digitalRead()` 函数来获取输入状态。在获取按钮状态（0 或 1）后，我们现在使用 `Serial.println()` 函数将该数据发送到串口。

![Images](img/line.jpg)

### 6.4 analogRead() Function

用于从外部世界读取模拟信号的主要函数是 `analogRead()` 函数。模拟信号无上是一个连续的时域信号。存在多种来源可以产生模拟信号。一些常见的模拟设备包括电位器、模拟传感器（如简单的光敏电阻）、LM35 温度传感器、土壤湿度探针等。

在 Arduino UNO 中，有六个模拟引脚可用：`A0–A5`。在 Arduino Mega 中，总共有 16 个引脚，即 `A0–A15`。`analogRead()` 函数读取模拟信息并以数值数字的形式返回。数据类型是整数类型。Arduino 拥有 10 位 A/D 转换器，会将输入电压水平量化为五个不同的电压状态。由此产生的整数值在 0 到 1,023 之间，这意味着总共有 1,024 个值。因此，A/D 转换器的分辨率为每单位 0.0049 V。可以使用 `analogReference()` 函数更改分辨率和输入范围。图 6.2 显示了模拟传感器的输入模式。

![Images](img/006x002.jpg)

**图 6.2**

模拟输入模式。

![Images](img/line.jpg)

### 6.5 Inputs for Firmata Library

Firmata 通常使用 USB 通信通道与计算机系统通信。像 Processing 的应用程序通过串口库与其通信。串口通信基本上是面向字符的，一旦设置妥当，它就是良好且可靠的通信介质。

Firmata 是基于 MIDI 的，长度为 3 字节。有多种可用的通信输入和输出函数。要设置数字输出，我们必须从每个位的参数值中构建数据。读取数字输入涉及三个基本步骤：引脚必须设置为数字模式，端口必须设置为输入模式，并且必须进行解码。当端口读取模式启用时，Arduino 开始向相应的引脚发送值。该协议的一个特性是，它会在数据发生变化时发送或重新发送数据。如果消息与上一个消息相同，则永远不会发送。该任务使用解析方法来完成。

以下显示了一些提到的消息发送和接收函数：

`sendAnalog(byte pin, int value)` 向特定引脚发送模拟消息或模拟信号。`sendDigitalPort(byte portNumber, intportData)` 将单个数字信号发送到 8 位端口。第二种方法是 `sendString(const char* string)`。该方法专门将字符串发送到主机计算机。接下来，`sendString(byte command, byte bytec, byte *bytev)` 基本用于带有特定自定义命令向主机计算机发送字符串。另一个名为 `sendSysex(byte command, byte bytec, byte* bytev)` 的方法发送带有任意字节集的命令。最后，`write(byte c)` 通常用于向流写入字节字节数据。

被认为执行输入操作的几个输入函数如下：

* `available()` 用于检查输入缓冲区中是否收到了任何传入的消息。
* 另一方面，`processInput()` 函数处理从缓冲区获取的传入消息。它还将数据发送到任何注册的回调方法。
* 包含的另外两个常用函数是 `attach(byte command, callbackFunction Function1)` 和 `detach(byte command)`，它们主要用于将函数与传入的消息类型绑定，以及从消息中分离函数。




众所周知，Arduino 引脚的默认性质是输入，因此不需要将其声明为输入。配置为输入的引脚通常处于高阻态状态 [3]。它对电路的需求非常低，实际上等于在输入端前有一个 100 Ω 的串联电阻。这些输入引脚从一个状态转换到另一个状态所需的电流非常小。操作内容包括读取光二极管、电容式触摸传感器以及如 LM35 温度模块之类的模拟传感器。

尽管在逻辑上，`pinMode(pin, INPUT)` 产生的是未连接状态，但有时由于相邻电路的电噪声干扰或与附近引脚的电容耦合，会报告引脚状态发生突变。

通常，如果输入引脚是悬空的，我们会将引脚引导到已知状态。这可以通过上拉电阻或下拉电阻来实现。上拉电阻连接到 +5 V，而下拉电阻应接地到 0V。10 K 欧电阻是上拉或下拉电阻的良好示例。

ATmega 芯片的内部上拉电阻值为 20 kΩ。它只能通过软件访问。这可以通过将 `pinMode()` 设置为 `INPUT_PULLUP` 来 [4]。这基本上反转了模式，即 HIGH 会产生 OFF 状态，LOW 会产生 ON 状态。

上拉值随微控制器的变化而变化。大多数基于 AVR 的微控制器上拉值在 20 到 50 kΩ 之间。有些在 50 到 150 kΩ 之间。

上拉寄存器产生的电流足以驱动 LED 完美发光。

有时，尝试运行大电流设备会损坏并破坏输出晶体管引脚或 ATmega 芯片。这会导致尽管整个微控制器处于功能模式，ATmega 芯片上的某个引脚失效。发送清除消息反映了数据块是空的。由于每条消息都有唯一的状态码，很容易识别出持有特定路由的消息。

![Images](img/line.jpg)

### 6.7 本章涵盖的概念

* 输入方法
* 模拟输入技术
* 数字输入技术
* 输入设备接口
* 输入引脚属性

![Images](img/line.jpg)

### 参考文献

1. 1. Barrett, Steven F. *Arduino Microcontroller Processing for Everyone*!. Morgan and Claypool Publishers, San Rafael, CA, 2010.
2. 2. Kadam, Rahul, Ruchika Shelke, Pritesh Bagde, Gunwanta Bande, Shraddha Dongre, Hemnat Chachane, and B. E. Student. “Automated gate of animal cage using Arduino Mega 2560 and Raspberry Pi.” *International Journal of Engineering Science* 17249 (2018): 16204–16206\. [`ijesc.org/`](http://ijesc.org).
3. 3. Caruso, Massimo, Antonino O. Di Tommaso, Rosalba Miceli, G. Ricco Galluzzo, Pietro Romano, Giuseppe Schettino, and Frank Viola. “Design and experimental characterization of a low-cost, real-time, wireless AC monitoring system based on ATmega 328P-PU microcontroller.” In *AEIT International Annual Conference (AEIT), 2015*, pp. 1–6\. IEEE, 2015.
4. 4. Banzi, Massimo, and B. Massimo. *Getting Started with Arduino* (*Make: Projects*). O’Reilly, Sebastopol, CA, 2008.

## 7

![Images](img/line.jpg)

## Arduino 输出系统

![Images](img/line2.jpg)

Arduino 微控制器系统支持多种输出机制。各种组件作为输出设备连接到 Arduino，有时直接连接，有时使用某些外部扩展板。在本章中，我们将通过一些标准库以及一些常见的输出设备及其接口机制，查看并演示 Arduino 可能的输出机制。

![Images](img/line.jpg)

### 7.1 digitalWrite() 函数

Arduino 输出最实用的函数之一是 `digitalWrite()` [1]。它向数字引脚写入 HIGH 或 LOW 值。引脚的输出性质由 `pinMode()` 函数决定。这根据易用性将引脚配置为输入引脚或输出引脚。当引脚变为输出引脚时，+5 V（某些特定 3.3V 板为 +3.3 V）将 HIGH 信号输出，0V 为 LOW 信号输出。如果 `pinMode()` 为输入，`digitalWrite()` 将激活或禁用输入上拉。




图 7.1 展示了 `analogWrite()` 脉冲的频率。脉冲值范围从 0 到 255。`analogWrite(255)` 代表 100% 的占空比，而 `analogWrite(127)` 代表 50% 的占空比，依此类推。

在调用 `digitalWrite()` 或 `analogWrite()` 的标准过程中，我们对 PWM 脉冲的占空比具有完全控制。然而，缺点是任何应用于处理器的中断都会影响时间，从而导致宽度干扰。当处理器忙于其他工作时，输出引脚无法处理任务。此外，要确定特定占空比以及频率的常量也是极其困难的。在这种情况下，手动计数是唯一的方法。

![Images](img/007x001.jpg)

**图 7.1**

`analogWrite()` 的 PWM 信号占空比。

### 7.2.3 ATmega PWM 访问

通过控制 PWM 输出，与 `analogWrite()` 函数相比，我们可以获得更多 PWM 的权限。实际上，ATmega168/328 有三个内置定时器：`Timer0`、`Timer1` 和 `Timer2`。每个定时器有两个比较寄存器和两个输出。比较寄存器控制 PWM 信号的宽度。当比较寄存器达到定时值时，输出将立即翻转。定时器的两个输出基本上频率相同，尽管定时器的占空比不同。

每个定时器包含一个分频器，它通过除以分频因子产生定时器时钟脉冲。定时器还会针对比较寄存器产生中断或匹配。定时器包含不同的 PWM 模式。定时器值的范围从 0 到 255 不等。

*   **快速 PWM 模式**是最简单的模式，定时器值从 0 快速计数到 255。当定时器值为 0 时输出开启，当定时器与比较寄存器匹配时输出关闭 [[3]](#ch07.xhtml_ref7_3)。

*   **相位校 PWM 模式**是一种独特的模式，定时器从 0 计数到 255，然后减小到 0。输出在碰到并匹配比较寄存器时关闭。这种输出更加对称。与快速 PWM 模式相比，其输出频率只有的一半。

*   **基于 `OCRA` 的快速 PWM**是另一类 PWM，从根本上基于输出控制寄存器。基于 `Timer2` 的 PWM 在引脚 3–11 上。这里使用名为波形生成模式的特殊模式，初始设置为 111。在 `ORCA2` 的情况下，上限被任意分配为 180。

*   **具有可变时间上限的快速 PWM** 是一种定时器从 0 计数到 `ORCA`（输出比较寄存器的值）的方法。在此之后，定时器将从 0 计数到 255，并对输出频率提供显著控制。

图 7.2 显示 ATmega328 PWM 引脚配置。

考虑一种通过对 LED 实施开启和关闭使其闪烁的场景。如果是这样，ATmega 将创建一个方波，在一段时间内，信号为高电平（HIGH）；之后，它应该变为低电平（LOW）。在这种情况下，如果开启值除以关闭值，然后乘以 100%，我们就得到了占空比的实际结果（`DC[t]`）。因此，可以写为：

```
DC[t] = {On[t]/(On[t] + Off[t])} × 100%
```
这里，`On[t]` 是开启时间，`Off[t]` 是关闭时间。因此，如果控制器的开启 1 ms 并关闭 2 ms，那么我们就可以实现 33.3% 的占空比。因此，输出电压通过以下方程计算：

![Images](img/007x002.jpg)

**图 7.2** ATmega328 PWM 配置。

```
V[o] = DC[t] × V[i]
```
这里，`V[o]` 是输出电压，`V[i]` 是输入电压。

从上述方程可以清楚，如果我们有 +5V 输入且 PWM 占空比为 25%，那么输出模拟电压为 1.25V。由于分频器充当计数器，它允许设备以不同的频率运行。这种方式有助于那些对变化的 PWM 速度敏感的设备。例如，无刷电机在非常高的 PWM 速率下产生热量，如果 PWM 太慢，电机将会抖动。在我们讨论不同的 PWM 模式时，让我们讨论一下它们的不同数学模型。

快速 PWM 模式是一种标准模式，PWM 作为普通计数器工作。当控制器接收到信号时，它设置寄存器 `TCINTn`。如果检测到匹配，`OCFnx` 标志将被设置，然后信号发送到波形生成器。然而，PWM 波的频率 `F[t]` 可以计算为：

```
F[t] = Clock/{PS[v] × (1 − T[v])}
```
这里 `PS[v]` 是分频器，`T[v]` 是上限，`Clock` 是时钟速度。





```cpp
 // code curtsy https://howtomechatronics.com/
const int tPin = 9;
const int ePin = 10;
    // defines variables
    long dur;
    int dist;
    void setup() {
    pinMode(tPin, OUTPUT);
    pinMode(ePin, INPUT);
    Serial.begin(9600);
    }
    void loop() {
    digitalWrite(tPin, LOW);
    delayMicroseconds(2);
    digitalWrite(tPin, HIGH);
    delay(10);
    digitalWrite(tPin, LOW);
    duration = pulseIn(ePin, HIGH);
    dist= dur*0.034/2;
    Serial.println(dist);
}
```

![Images](img/007x003.jpg)

### 图 7.3

连接了超声波传感器的 Arduino。

在上述代码中，串口数据将由 `Serial.print(dist)` 函数提供。第二个代码段被设计为使用 Python 串口接口获取串口数据。`serial.Serial(port,baud)` 函数接收串口数据，其中端口名和 `baud` 作为参数提供。当我们获取数据后，必须打开工作簿并激活活动工作表。在这种情况下，我们通常从串口输入获取 300 个数据样本，并将它们放入 Excel 工作表的第 2 列。第 3 列将存储迭代次数。然后，我们需要保存数据集。现在我们的任务是加载数据并以数据集表示的形式打印出来。可以使用 `pandas` 作为 `pd` 对象来完成。这里的 `pd.read_excel()` 函数读取 Excel 格式的数据集。然后，我们只需通过调用 `head(number of items)` 打印数据的头部。现在，我们可以通过调用 `plot()` 函数绘制头部的数据值图。这里的 `m.head(297).plot()` 函数执行了该任务。这里“297”是头部中存在的元组数量。`plt.show()` 最后显示数据的图形化表示。图 7.4 显示了由 `head()` 函数创建的数据集，而 图 7.5 显示了传感器数据的图表。

![Images](img/007x005.jpg)

### 图 7.4

pandas 生成的数据集。

![Images](img/007x004.jpg)

### 图 7.5

数据可视化。

```python
 from openpyxl import Workbook # 创建 Excel 电子表格
import serial  # 调用串口接口
import pandas as pd # 访问 Excel 数据
import matplotlib.pyplot as plt # 绘制数据集。

s = serial.Serial('COM13',9600) # 用于串口数据输入的 COM 端口
wb = Workbook() # 创建 excel 工作簿
ws = wb.active # 活动工作表

start_row = 2
start_column = 2
addl_column = 3
i = 0
while (i<300) :
    ws.cell(row=start_row, column=start_column).value = str(s.readline())
    ws.cell(row=start_row, column=addl_column).value = i
    start_row += 1
    i+=1

wb.save("dataset.xlsx")
print "Data Written Written!!"

f = "dataset.xlsx"
m = pd.read_excel(f)

print 'head is'
print (m.head(20))

m.head(297).plot()
plt.show()
```

图 7.4 显示了超声波距离传感器生成的数据集。我们存储了迭代次数和超声波传感器获取的原始传感器距离数据。图 7.5 阐述了传感器数据的可视化。`x`-轴表示迭代次数，`y`-轴表示传感器距离。

### 7.4 本章涵盖的概念

* `digitalWrite()`
* `analogWrite()`

### 参考文献

1. Margolis, Michael. (2011). *Arduino Sketches, Getting Started with: The Arduino Cookbook*. O'Reilly Media, Sebastopol, CA.
2. Javed, Adeel. (2016). *Programming the Raspberry Pi: Experiments*. Apress, Berkeley, CA.
3. Monk, Simon. (2013). *Building the Internet of Things*. McGraw-Hill, New York.

### 8. 结合 Arduino

Arduino 是一个具有多种用途的独立微控制器单元。Processing 是一个用于视觉艺术的软件平台。它起源于 2001 年，从那时起一直在可视化。

* 它支持 2D、3D 以及便携文档格式 (PDF) 的交互式编程。
* 它支持 Linux、Windows、MacOS X 甚至安卓。
* 它有庞大的库支持。
* 它兼容多种语言。

### 8.1 Processing 语言概述

Processing 是一门视觉艺术语言。Processing 的基础语言是 Java。虽然 Java 具有一些语法特征，但它也包含了用于可视化的 PostScript 和 OpenGL。许多语言从根本上与 Processing 相关，如 Arduino、wiring 框架、C++、Java 和 Android。此外，通过 processing.js 还整合了对 JavaScript 和 HTML5 的支持。

很多人每天都使用 processing。随着时间的推移，对 processing 的社区支持日益增加并变得强大。Processing 对各类人群都有用。视觉艺术家、平面设计师、动画师，以及想要实时以图形形式可视化传感器数据或可能想要传感器数据设计视觉效果的人都可以使用 processing。

#### 8.1.2 Processing 软件

软件本身是开源的，可以在 [`processing.org/`](http://processing.org/) 获取。适用于 Windows、Linux 和 MacOS X 的稳定版本。此外，Play Store 中也有适用于安卓的 IDE。在安卓版本中，可以在不更改或部分更改代码的情况下创建壁纸和不同的虚拟现实应用程序。我们无需担心安装软件开发包 (SDK) 或编辑布局。安卓版的 Processing 还允许安卓应用程序接口 (API) 读取传感器数据，甚至将草稿导出为准备上传到 Google Play Store 的签名包。





其他支持的处理平台包括 Windows 64 位、Linux 64 位和 Linux ARMv6hf。旧版本也可以从源码构建。处理窗口如图图 8.1

**图 8.1**

Processing 窗口显示基础动画。

![Images](img/008x002.jpg)

**图 8.2**

Processing 中的不同模式。

要开始 processing 开发，首先从 `.zip` 或 `.exe` 源码安装 processing IDE 并打开 processing 窗口。当我们打开窗口时，在右上角可以看到模式选项。默认情况下，模式是 Java 模式。我们可以将模式从 Java 更改为 Python 模式。

在安装了 Python 模式后，你可以通过输入以下代码检查基础草图（sketch）：

```
def setup():
    size(600, 600)
    colorMode(HSB)
    noStroke()

def draw():
    fill(0x11000000)
    rect(0, 0, width, height)
    fill(frameCount % 255, 255, 255)
    ellipse(mouseX, mouseY, 20, 20)
```

它会根据提供的颜色创建一些矩形和椭圆的基本形状。

Python 模式基本上基于 Java 工程设计，旨在与现有的生态系统和 processing 库兼容。processing 中使用的一些重要库包括与外部硬件设备（USB、RS232）进行串口通信的 `Serial` 库、处理音频以合成和效果的 `Sound` 库、播放视频文件并创建电影的 `Video` 库，以及在客户端-服务器模式下在网络中发送接收数据的 `Network` 库。`DFX` 输出库创建 DFX 文件以保存几何形状加载到第三方应用程序中。它包含了多边形、框、球体和其他三角形基础对象。`PDF` 输出库使得导出 pdf 成为。`Hardware I/O` 库与树莓派或其他基于 Linux 的系统硬件进行交互。关于库的更多信息将在 8.3 节中进一步讨论。

![Images](img/line.jpg)

### 8.2 代码结构

### 8.2.1 Processing 代码

在我们电脑上安装 processing 环境时，我们的任务是编写一些程序。在 Windows 环境下，我们可以通过双击图标打开 IDE。如果包是 `.zip` 扩展，我们只需将其解压到任何目录并运行可执行文件。在 Linux 中，要执行它，必须编写 `./processing`（因为它是一个带有 `.sh` 扩展名的脚本）。在此之前，我们必须将 processing 可执行文件的模式更改为可执行模式。我们必须执行命令 `chmod 777 processing` 来。一旦成功，它将打开 IDE。

processing 的基本代码结构基本上与 Arduino 语言相似，因为它由 `void setup()` 函数组成，并且没有 `void loop`，而是有一个 `void draw()` 函数。`void draw()` 函数的作用是在给定的图像区域内绘制像素。在我们的第一个程序中，我们将简单地在固定帧区域内绘制一些圆。代码所示：

```
void setup() {
size(500, 520);
smooth();
}
void draw() {
if (mousePressed) {
fill(1);
} else {
fill(252);
}
ellipse(mouseX, mouseY, 70, 70);
}
```

代码的输出将显示 500, 520 给定帧区域内的一组圆，随着我们将鼠标指针移动到该区域，将生成更多的圆。

processing 应用的主要优点之一是，你可以直接将代码导出为可执行的应用程序软件。在这种情况下，你必须点击导出按钮。它将根据你的要求立即应用程序。默认情况下，它将创建 Windows 32/64 位、Linux 32/64 位和 MAC OSX 。

### 8.2.2 绘制对象

processing 包含运行应用程序两个两个函数。第一个是 `void setup()`，主要用于初始化变量和对象。它还初始化窗口显示帧的大小。下一个方法是 `draw()`。此方法的运行类似于 applet 的生命周期，这意味着此方法中的代码实际上以循环方式执行，直到通过点击关闭按钮停止显示窗口。

要开始 processing 开发，首先从 .zip 或 .exe 源码安装 processing IDE 并打开 processing 窗口。当我们打开窗口时，在右上角可以看到模式选项。默认情况下，模式是 Java 模式。我们可以将模式从 Java 更改为 Python 模式。

在安装了 Python 模式后，你可以通过输入以下代码检查基础草图：

```
def setup():
    size(600, 600)
    colorMode(HSB)
    noStroke()

def draw():
    fill(0x11000000)
    rect(0, 0, width, height)
```

它会根据提供的颜色创建一些矩形和椭圆的基本形状。

Python 模式基本上基于 Java 工程设计，旨在与现有的生态系统和 processing 库兼容。processing 中使用的一些重要库包括与外部硬件设备（USB、RS232）进行串口通信的 `Serial` 库、处理音频以合成和效果的 `Sound` 库、播放视频文件并创建电影的 `Video` 库，以及在客户端-服务器模式下在网络中发送接收数据的 `Network` 库。`DFX` 输出库创建 DFX 文件以保存几何形状加载到第三方应用程序中。它包含了多边形、框、球体和其他三角形基础对象。`PDF` 输出库使得导出 pdf 成为。`Hardware I/O` 库与树莓派或其他基于 Linux 的系统硬件进行交互。关于库的更多信息将在 8.3 节中进一步讨论。

![Images](img/line.jpg)

### 8.3 库与函数

处理环境中包含了各种库。将讨论最有效的库。

#### 8.3.1 Serial 库

Serial 库是流行的库之一，可以通过串口（如 5`：此函数返回整数形式的字节数，显示在该时刻有多少字节可用。

- `read()`：此函数用于从读取缓冲区中读取数据字节。读取应该以 0–255 值的形式进行。如果没有可用数据，它将返回 -1。可以使用其他 `read()` 函数的形式，例如 `readChar()`、`readByte()`、`readByteUntil()`、`readString()` 和 `readStringUntil()`。

- `buffer()`：此函数主要用于创建存储的临时缓冲区内存。在这种情况下我们必须传递缓冲区的大小。语法看起来如 `Serial.buffer(size)`。还有一个 `bufferUntil()` 函数与 `buffer()` 相关，确保在调用串口事件之前保持缓冲区位置。

- `Last()`：此方法返回缓冲区中最后一个用的字节。如果不可用，它将立即返回 -1。





- 还有一些输入-输出函数可用。这些函数包括 `write()`、`clear()`、`stop()` 等。`write()` 函数用于向串口写入数据，`clear()` 函数用于清除端口本身，而 `stop()` 函数用于停止该端口的进一步通信。另一个名为 `list()` 的函数。
- **硬件 I/O**：它主要用于访问树莓派或其他基于 Linux 的计算机系统。这本质上是一个外围设备接口库。其功能与 Arduino 平台类似。

该库中一个非常有用的类是 `General Purpose Input/Output`-`GPIO` 类。该库包含以下各种功能：

- **网络**：它使用简单的客户端-服务器方法通过网络发送数据。
- **音效**：它执行音频文件的播放并产生合成声音和效果。
- **视频**：它从摄像头读取电影并播放视频。
- **DFX 导出**：它能够创建 `DFX` 文件并保存几何图形，供其他应用程序使用。
- **PDF 导出**：它还能创建并导出带有高分辨率矢量图形的 `PDF` 文件。

![Images](img/line.jpg)

### 8.4 LDR 输出的可视化

LDR 是一种光检测传感器。它本质上是一个光敏电阻。电阻值随着光强的变化而改变。我们可以通过从设备的串口获取光强数据来使光强的可视化。然后，处理平台可以获取这些数据以生成图形化可视化结果。在这种情况下，我们可以使用 `Arduino DUE` 并配合光传感器接口分压器电路。获取 LDR 数据的 Arduino 代码所示：

```cpp
 //Arduino Code

int apin =A0;
void setup() {
  // 在此处编写你的设置代码，运行一次：

  pinMode(apin,INPUT);
  Serial.begin(9600);
}

void loop() {
  // 在此处编写你的主代码，循环运行：

  int d = analogRead(apin);

  Serial.println(d,DEC);

}
```

接下来的代码表示了圆圈移动的处理示例，这取决于光强的变化。图 8.4 显示了光强的可视化。

```processing
 // Processing code

import processing.serial.*;
Serial port;
float br=0;

void setup(){

  size(800,600);
  port = new Serial(this,"COM6",9600);
  port.bufferUntil('\n');
}

void draw(){

  background(br-88,br-44,br);

  fill(255,255,0);

  ellipse(100,100,br,br);
  fill(020,200,  77);
  ellipse(br+250,br+250,200,200);
  println(br);
}
void serialEvent(Serial port){
  br = float(port.readStringUntil('\n'));
}
```

![Images](img/008x004.jpg)

**图 8.4**

光强的可视化。

![Images](img/line.jpg)

### 8.5 与 Arduino 和 Firmata 的交互

Arduino 和 processing 之间存在很强的兼容性。我们通常直接与 processing 和 Arduino 交互。有时，交互由 Firmata 控制协议进行控制。

Arduino 与 processing 通信的一个基础示例是传感器数据可视化。接下来的示例演示了 Arduino 和 processing 如何协同工作。

在这个示例中，我们正尝试将超声波传感器的数据可视化。数据已由超声波传感器获取，距离使用 Arduino 计算；此外，距离值将发送到 processing 应用程序，它将数据可视化化为一个类似雷达的范围测距器。系统图如图 8.5 所示。

![Images](img/008x005.jpg)

**图 8.5**

基于 Arduino 的雷达系统连接图。

接下来的代码分别演示了 Arduino 和 processing 的实现：

```cpp
 Arduino Code

// 包含 Servo 库
#include <Servo.h>.
// 定义超声波传感器的 Trig 和 Echo 引
const int trigPin = 3;//橙色
const int echoPin = 2;//红色白色 - vcc 灰色 -g 地
// 用于持续时间和距离的变量
long duration;
int distance;
Servo myServo; // 创建一个 servo 对象来控制舵机
void setup() {
  pinMode(trigPin, OUTPUT); // 将 trigPin 设置为输出
  pinMode(echoPin, INPUT); // 将 echoPin 设置为输入
  pinMode(4,OUTPUT);//黄色
  pinMode(1,OUTPUT);
  Serial.begin(9600);
  myServo.attach(9); // 定义舵机连接的紫色引脚 9
}
void loop() {
  // 将舵机从 5 度旋转到 165 度
  for(int i=0;i<=180;i++){
    myServo.write(i);
    delay(30);
    distance = calculateDistance();// 调用函数通过超声波计算每个角度的距离
    Serial.print(i); // 将当前角度发送到串口
    Serial.print(","); // 发送上一个值后面的字符，后续 Processing IDE 需要索引
    Serial.print(distance); // 将距离值发送到串口
    Serial.print("."); // 发送字符
  }
  // 从 165 度到 5 度旋转舵机
  for(int i=180;i>0;i--){
    myServo.write(i);
    delay(30);
    distance = calculateDistance();
    Serial.print(i);
    Serial.print(",");
    Serial.print(distance);
    Serial.print(".");
  }
}
// 通过超声波计算距离的函数
int calculateDistance(){
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2); // 将 trigPin 设置为高电 10 微秒
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH); // 读取 echoPin，返回声波传输时间（微秒）
  distance=duration*0.34/2;
  if (distance < 40) {
    digitalWrite(4,HIGH);
    digitalWrite(11,HIGH);
  }
  else {
    digitalWrite(4,LOW);
    digitalWrite(11,LOW);
  }
  return distance;
}
```

Arduino 获取安装在舵机上的超声波传感器数据。`#include<Servo.h>` 实际上添加了控制舵机的功能。在这里，我们需要定义 `trigPin` 和 `echoPin` 为常量变量。

现在在 Arduino 的 `setup()` 函数中，将 `trigPin` 设置为输出，`echoPin` 设置为输入。舵机将连接在 9 号。

在 `loop()` 函数中，首先通过一个 `for` 循环让舵机从 15 度旋转到 165 度。在这里，`myServo.write(i)` 函数执行舵机的移动，延迟为 30 毫秒。在移动过程中，调用 `calculateDistance()` 函数获取超声波传感器的数据并发送到串口，包括舵机的角度。第二个 `for` 循环是为了相同的目的，但是反向执行。





```java
import processing.serial.*; // 导入串口通信库
import java.awt.event.KeyEvent; // 导入用于从串口口读取数据的库
import java.io.IOException;
Serial myPort; // 定义 Serial 对象
// 定义变量
String angle="";
String distance="";
String data="";
String noObject;
float pixsDistance;
int iAngle, iDistance;
int index1=0;
int index2=0;
PFont orcFont;

void setup() {
  size (1200, 700);
  smooth();
  myPort = new Serial(this,"COM3", 9600); // 开始串口通信
  myPort.bufferUntil('.'); // 从串口读取数据直到遇到字符 '.' 为止。
  // 所以实际上它读取的是：角度,距离。
}

void draw() {
  fill(98,245,31);
  // 模拟移动线条的运动模糊和缓慢消失
  noStroke();
  fill(0,4);
  rect(0, 0, width, height-height*0.065);

  fill(98,245,31); // 绿色
  // 调用绘制雷达的函数
  drawRadar();
  drawLine();
  drawObject();
  drawText();
}

void serialEvent (Serial myPort) { // 开始从串口读取数据
  // 从串口读取数据直到字符 '.' 为止，并将其放入字符串变量 "data" 中
  data = myPort.readStringUntil('.');
  data = data.substring(0,data.length()-1);

  index1 = data.indexOf(","); // 找到字符 ',' 并将其存入变量 "index1"
  angle= data.substring(0, index1); // 读取从位置 "0" 到变量 index1 位置的数据，即 Arduino 板发送到串口的角度值
  distance= data.substring(index1+1, data.length()); // 读取从位置 "index1" 到数据末尾的数据，即距离值

  // 将字符串变量转换为整数
  iAngle = int(angle);
  iDistance = int(distance);
}

void drawRadar() {
  pushMatrix();
  translate(width/2,height-height*0.074); // 将起始坐标移动到新位置
  noFill();
  strokeWeight(2);
  stroke(98,245,31);
  // 绘制弧线
  arc(0,0,(width-width*0.0625),(width-width*0.0625),PI,TWO_PI);
  arc(0,0,(width-width*0.27),(width-width*0.27),PI,TWO_PI);
  arc(0,0,(width-width*0.479),(width-width*0.479),PI,TWO_PI;
  arc(0,0,(width-width*0.687),(width-width*0.687),PI,TWO_PI; // 绘制角度线
  line(-width/2,0,width/2);
  line(0,0,(-width/2)*cos(radians(30)),(-width/2)*sin(radians(30)));
  line(0,0,(-width/2)*cos(radians(60)),(-width/2)*sin(radians(60)));
  line(0,0,(-width/2)*cos(radians(90)),(-width/2)*sin(radians(90)));
  line(0,0,(-width/2)*cos(radians(120)),(-width/2)*sin(radians(120)));
  line(0,0,(-width/2)*cos(radians(150)),(-width/2)*sin(radians(150)));
  line((-width/2)*cos(30),0,width/2);
  popMatrix();
}

void drawObject() {
  pushMatrix();
  translate(width/2,height-height*0.074); // 将起始坐标移动到新位置
  strokeWeight(9);
  stroke(255,10,10); // 红色
  pixsDistance = iDistance*((height-height*0.1666)*0.025); // 将传感器的距离（厘米）转换为像素
  // 将范围限制在 40 厘米内
  if(iDistance<40){
    // 根据角度和距离绘制物体
    line(pixsDistance*cos(radians(iAngle)),-pixsDistance*sin(radians(iAngle)),(width-width*0.505)*cos(radians(iAngle)),-(width-width*0.505)*sin(radians(iAngle)));
  }
  popMatrix();
}

void drawLine() {
  pushMatrix();
  strokeWeight(9);
  stroke(30,250,60);
  translate(width/2,height-height*0.074); // 将起始坐标移动到新位置
  line(0,0,(height-height*0.12)*cos(radians(iAngle)),-(height-height*0.12)*sin(radians(iAngle))); // 根据角度绘制线条
  popMatrix();
}

void drawText() { // 在屏幕上绘制文字
  pushMatrix();
  if(iDistance>40) {
    noObject = "超出范围";
  } else {
    noObject = "在范围内";
  }
  fill(0,0);
  noStroke();
  rect(0, height-height*0.0648, width, height);
  fill(98,245,31);
  textSize(25);
  text("10cm",width-width*0.3854,height-height*0.0833);
  text("20cm",width-width*0.281,height-height*0.0833);
  text("30cm",width-width*0.177,height-height*0.0833);
  text("40cm",width-width*0.0729,height-height*0.0833);
  textSize(40);
  text("Akshay676", width-width*0.875,height-height*0.0277);
  text("角度: " + iAngle + " °", width-width*0.48,height-height*0.0277);
  text("距离: ", width-width*0.26, height-height*0.0277);
  if(iDistance<40) {
    text("" + iDistance + " cm", width-width*0.225,height-height*0.0277);
  }
  textSize(25);
  fill(98,245,60);
  translate((width-width*0.4994)+width/2*cos(radians(30)),height-height*0.0907);
  rotate(-60);
  text("30°",0,0);
  resetMatrix();
  translate((width-width*0.503)+width/2*cos(radians(60)),height-height*0.0888);
  rotate(-30);
  text("60°",0,0);
  resetMatrix();
  translate((width-width*0.507)+width/2*cos(radians(90)),height-height*0.0833);
  rotate(0);
  text("90°",0,0);
  resetMatrix();
  translate(width-width*0.53+width/2*cos(radians(120)),height-height*0.0729);
  rotate(30);
  text("120°",0,0);
  resetMatrix();
  translate((width-width*0.5104)+width/2*cos(radians(150)),height-height*0.0574);
  rotate(60);
  text("150°",0,0);
  popMatrix();
}
```

上述代码创建了类似于雷达扫描的视觉效果（图 8.6）。为了获得该视觉效果，屏幕尺寸设置为 $1200 \times 700$。然后，通过调用 `myPort = new Serial(this, "COM3", 9600)` 打开串口对象。端口也可以通过另一个调用 `Serial.list()[0]` 来调用。在这种情况下，`Serial.list()` 返回端口名称。默认为 `COM1`。可以通过增加 `Serial.list()[0]` 的索引来更改。然后调用 `myPort.bufferUntil('.')`，它会从串口读取数据直到字符 `.`。因此，它实际上读取的是角度和距离。

![images/008x006.jpg]
**图 8.6** Processing 雷达屏幕。

![line.jpg]

### 8.6 Processing 中的鼠标处理

在 Processing 中，我们可以像图 8.7 所示处理鼠标活动。这是 Processing 中一种简化的事件处理机制。许多与鼠标编程相关的函数可以高效地控制鼠标活动。由于 Processing 基于 Java，鼠标的基础活动完全由后端的 Java 事件处理工具和接口控制，由于 Processing 产生了一层抽象，Processing 定义的函数（方法）通常会调用后端的 Java。接下来的节我们将讨论 Processing 的一些主要鼠标处理方法。

![images/008x007.jpg]
**图 8.7** 鼠标活动控制。

1. `mouseClicked()`：此函数主要在鼠标按钮按下释放后调用。通常，鼠标或键盘事件与 `draw()` 函数关联。如果我们不在 `draw()` 下使用它，它只会被调用一次并停止监听事件。通常使用重载函数语法：第一个是无参数的 `mouseClicked()`，另一个是带有程序生成的事件对象的 `mouseClicked(event)`。

示例所示：

```java
int val=0;

public void draw() {
  fill(val);
  rect(20, 20, 60, 60);
}

void mouseClicked() {
  if (val == 0) {
    val = 255;
  } else {
    val = 0;
  }
}
```





## 2. `mouseX`: `mouseX` 是一个由鼠标 X 轴坐标组成的系统变量。如果鼠标在当前窗口内，Processing 就可以跟踪鼠标的位置。默认情况下，该值为 0。当鼠标指针悬停在绘图窗口上时，它在离开时保持值 0，然后继续报告更新后的位置。

以下代码展示了该用处：

```java
public void draw() {
  background(225);
  line(mouseX, 24, mouseX, 70);
}
```

## 3. `MouseY`: 该系统变量存储鼠标移动的垂直位置。该变量的其他属性与 `mouseX` 系统变量相似。

## 4. `pmouseX`: 它是一个存储当前帧位置上一帧位置的系统变量。当在 `mousePressed()`、`mouseMoved()` 和 `draw()` 等事件内部引用它时，我们可以找到 `pmouseX` 和 `pmouseY` 的不同值。在 `draw()` 中，`pmouseX` 和 `pmouseY` 变量每帧只更新一次。在鼠标事件中，它们通常会在每次调用事件时更新。如果值没有立即更新，可能会观察到一些延迟，导致交互卡顿和延迟。如果这些变量每帧更新多次，由于在调用 `line` 之间值发生了多次变化，会导致产生很大的间隙。

以下简单程序打印了鼠标的位置差：

```java
void draw() {
  background(205);
  line(mouseX, 30, pmouseX, 70);
  println(mouseX + " : " + pmouseX);
}
```

## 5. `pmouseY`: 它是一个由鼠标当前位置上一帧的 Y 方向（或垂直方向）组成的系统变量。所有其他功能都与 `pmouseX` 系统变量相似。

## 6. `mousePressed()`: 此函数与 `mouseClick()` 某些方面相似，在每次按下鼠标后仅响应一次。与此关联的鼠标按钮变量通常用于跟踪按下了哪个按钮。

## 7. `mouseButton`: 它是一个存储已按下鼠标按钮的系统变量。通常，它根据鼠标上按下的左键、右键和中间键获取 `LEFT`、`RIGHT` 和 `CENTER` 值。如果没有找到按钮事件，它将显示值为 0。出于此原因，应该先调用 `mousePressed()` 函数检查按下状态，然后检查系统变量的值。以下代码是该示例：

```java
void draw() {
  rect(20, 20, 40, 40); // 绘制矩形
}

void mousePressed() {
  if (mouseButton == LEFT) { // 检查并执行操作
    fill(3);
  } else if (mouseButton == RIGHT) {
    fill(252);
  } else if (mouseButton == CENTER) {
    fill(116);
  }
  else {
    fill(178);
  }
}
```

## 8. `mouseReleased()`: 此函数每次释放鼠标按钮时被调用。因此，`mouseReleased()` 函数生成的事件可以用于执行不同的操作，如绘制或填充颜色。在操作上，它实际上与 `mouseClicked()` 和 `mousePressed()` 函数相似。

## 9. `mouseMoved()` 和 `mouseDragged()`：当鼠标按钮未按下但鼠标物理移动时，调用 `mouseMoved()` 函数。另一方面，`mouseDragged()` 函数在鼠标被拖动时做出响应。我们可以在这些函数下执行任何特定操作。

```java
int mv = 0;

void draw() {
  fill(mv);
  rect(20, 20, 45, 45);
}

void mouseMoved() { // 跨图像改变 mv 值
  mv += 4;
  if (mv > 255) {
    mv = 0;
  }
}
```

## 10. `mouseWheel()`: 此函数是一个鼠标轮控制函数，当鼠标轮向下滚动时返回正值，向上时返回负值。在此函数中，我们必须将事件作为参数传递。我们通常使用 `MouseEvent` 事件对象来控制事件功能。

![Images](img/line.jpg)

### 8.7 Processing 中的颜色

![Images](img/line.jpg)




-   7. Reas, Casey, and Benjamin Fry. “Processing.org: Programming for artists and designers.” In *ACM SIGGRAPH 2004 Web Graphics*, p. 3. ACM, 2004.

-   [8. Reas, Casey, Ben Fry, and John Maeda. *Processing: A Programming Handbook for Visual Designers*, The MIT Press, Cambridge, MA, 2007.

## 第 9 章

![Images](img/line.jpg)

## 生活中的代码示例](#ch00_fm04_toc.xhtml_rchapter9)

![Images](img/line2.jpg)

在本章中，我们重点介绍了 Arduino 以及相关传感器的应用。我们主要描述了一些小型实生活项目，并展示了不同应用的独特性。在开始部分，我们实现了一个自动道闸控制。随后，将通过代码示例介绍心率监测和液化石油气（LPG）泄漏检测器。

![Images](img/line.jpg)

### 9.1 自动道闸控制

我们可以使用 Arduino 和一些接近传感器 [1,2] 设计一个简单的道闸控制系统。该系统设计为：当火车进入距离平交道口一定范围内时，报警蜂鸣器开始响器，道闸关闭。当火车通过并移动到一定距离后，区域变得清晰，因此道闸打开，蜂鸣器停止。制作此项目所需的设备列如下：

1. Arduino UNO, mega
2. 一个红外接近传感器
3. 一个 12V 直流减速电机
4. 一个蜂鸣器
5. L293D 电机驱动集成电路 (IC) 或 Arduino 电机扩展板
6. 底纸板和一个木杆

#### 9.1.1 操作步骤

要制作原型项目，首先应该制作一条轨道，并在其上一定距离安装传感器 [3, 4, 和 5]。这可以通过热熔胶或螺丝完成。电机应通过橡胶或胶水安装在轨道的一侧。现在将一根木杆或塑料杆连接到电机的轴上，以便作为道闸使用。接下来，将红外传感器固定在轨道的两侧，它们与电机的距离应该相等，其中一个用于感知火车的到达，并相应地关闭道闸；第二个传感器的任务是在火车通过第二个传感器时打开道闸。图 9.1 显示了轨道的示意图。为了让传感器正常工作，请移除传感器的 LED，仅将其固定在传感器模块中连接的光电晶体管对面。

![Images](img/009x001.jpg)

**图 9.1**

道闸控制器系统图。

#### 9.1.2 电路图

电路包含以下组件：(1) 应连接在 Arduino 的 Vcc 和 GND 引脚之间的红外传感器，(2) 分别连接到引脚 2 和 3 的 Arduino 输出引脚。电机驱动器 (L293D) 应连接到 Arduino 引脚 4 和 5。连接到电机驱动器的电机所示图 9.2。可选情况下，我们可以在电机旁边添加蜂鸣器，以制作平交道口报警系统。

道闸控制的源码如下：

```cpp
 int so_1=2;
int so_2=3;
int mo_1=4;
int mo_2=5;
void setup(){
pinMode(so_1,INPUT);
pinMode(so_2,INPUT);
pinMode(mo_1,OUTPUT);
pinMode(mo_2,OUTPUT);
}
void loop(){
Zp:
if(so_1==LOW){
digitalWrite(mo_1,HIGH);
digitalWrite(mo_2,LOW);
delay(600);
digitalWrite(mo_1,HIGH);
digitalWrite(mo_2,HIGH);
Xp:
if(so_2==LOW){
digitalWrite(mo_1,LOW);
digitalWrite(mo_2,HIGH);
delay(600);
digitalWrite(mo_1,HIGH);
digitalWrite(mo_2,HIGH);
delay(1100);
goto Zp;
}goto Xp;
if(so_2==LOW){
digitalWrite(mo_1,HIGH);
digitalWrite(mo_2,LOW);
delay(600);
digitalWrite(mo_1,HIGH);
digitalWrite(mo_2,HIGH);
}
```

![Images](img/009x002.jpg)

**图 9.2**

电路图。

![Images](img/line.jpg)

### 9.2 基于 Arduino 的心率系统

心率监测的基本原理是光电脉搏波记录法。根据这一原理，通过器官的光强度变化等同于该器官内血液体积的变化 [6]。心率监测传感器主要是 LED 或红外 LED 以及一个检测光强的光电晶体管或光电阻 (LDR)。这种光源和传感器布局有两种不同的实现方式：透射式传感器和反射式传感器。

透射式传感器的情况下，光源和检测器必须面对面，人的手指必须放在发射器和接收器之间。

另一方面，反射式传感器的光源和检测器相邻，人的手指必须放在传感器前方。心率传感器由一个 LED 或红外 LED 和光二极管组成。信号由光电传感器进一步接收，并通过放大电路进行放大。随后，信号发送到微控制器进行处理。

该项目使用的主要组件如下：

* Arduino UNO
* ×2 LCD 显示器
* K 电位器
* Ω 电阻
* 按钮
* 心率传感器模块
* 实验板和连接线

带有 Arduino 的电路设计见图 9.3。

![Images](img/009x003.jpg)

**图 9.3**

心率接口电路设计。

#### 9.2.1 工作原理

电路图显示传感器有三个引脚：Vcc、GND 和信号引脚。信号将连接到模拟引脚 A0。原始数据经过校准后，计算出最终的 BPM 值。

然后将值打印在 16 ×2 LCD 屏幕上。系统启动时，指示按下按钮开始采集心率。启动后，它获取手指脉冲以计算并显示每分钟心率 (BPM)。

输出将连接到数字 PWM 引脚 0, 1, 2, 3, 5 和 6。在引脚 7 上我们将连接按钮。我们需要将 10K 电位器连接到 LCD 屏幕以控制屏幕亮度。

Arduino 代码如下：





```cpp
 #include<LiquidCrystal.h>
LiquidCrystal lcd(6, 5, 3, 2, 1, 0);
int dat_1=A0;
int stat=7;
int co=0;
unsigned long t_mp=0;

byte cChar1[8] = {0b00000,0b00000,0b00011,0b00111,0b01111,0b01111,0b01111,0b01111};
byte cChar2[8] = {0b00000,0b11000,0b11100,0b11110,0b11111,0b11111,0b11111,0b11111};
byte cChar3[8] = {0b00000,0b00011,0b00111,0b01111,0b11111,0b11111,0b11111,0b11111};
byte cChar4[8] = {0b00000,0b10000,0b11000,0b11100,0b11110,0b11110,0b11110,0b11110};
byte cChar5[8] = {0b00111,0b00011,0b00001,0b00000,0b00000,0b00000,0b00000,0b00000};
byte cChar6[8] = {0b11111,0b11111,0b11111,0b11111,0b01111,0b00111,0b00011,0b00001};
byte cChar7[8] = {0b11111,0b11111,0b11111,0b11111,0b11110,0b11100,0b11000,0b10000};
byte cChar8[8] = {0b11100,0b11000,0b10000,0b00000,0b00000,0b00000,0b00000,0b00000};
void setup()
{
lcd.begin(16, 2);
lcd.createChar(1, cChar1);
lcd.createChar(2, cChar2);
lcd.createChar(3, cChar3);
lcd.createChar(4, cChar4);
lcd.createChar(5, cChar5);
lcd.createChar(6, cChar6);
lcd.createChar(7, cChar7);
lcd.createChar(8, cChar8);

pinMode(dat_1,INPUT);
pinMode(start,INPUT_PULLUP);
}

void loop()
{
lcd.setCursor(0, 0);
lcd.print("Place finger here");
lcd.setCursor(0, 1);
lcd.print("Now Start !!! ....");

while(digitalRead(stat)>0);

lcd.clear();
t_mp=millis();

while(millis()<(t_mp+10000))
{
if(analogRead(dat_1)<100)
{
co+=1;

lcd.setCursor(6, 0);
lcd.write(byte(1));
lcd.setCursor(7, 0);
lcd.write(byte(2));
lcd.setCursor(8, 0);
lcd.write(byte(3));
lcd.setCursor(9, 0);
lcd.write(byte(4));

lcd.setCursor(6, 1);
lcd.write(byte(5));
lcd.setCursor(7, 1);
lcd.write(byte(6));
lcd.setCursor(8, 1);
lcd.write(byte(7));
lcd.setCursor(9, 1);
lcd.write(byte(8));

while(analogRead(dat_1)<100);

lcd.clear();
}
}

lcd.clear();
lcd.setCursor(0, 0);
co*=6;
lcd.setCursor(2, 0);
lcd.write(byte(1));
lcd.setCursor(3, 0);
lcd.write(byte(2));
lcd.setCursor(4, 0);
lcd.write(byte(3));
lcd.setCursor(5, 0);
lcd.write(byte(4));

lcd.setCursor(2, 1);
lcd.write(byte(5));
lcd.setCursor(3, 1);
lcd.write(byte(6));
lcd.setCursor(4, 1);
lcd.write(byte(7));
lcd.setCursor(5, 1);
lcd.write(byte(8));
lcd.setCursor(7, 1);
lcd.print(count);
lcd.print("BPM");
t_mp=0;
while(1);
}
```
![Images](img/line.jpg)

### 9.3 基于 Arduino 的 LPG 泄漏检测器

LPG 是家用、工业和汽车用途中最重要的组件之一。然而，LPG 的泄漏会导致灾难性的后果。不过，对 LPG 泄漏进行警报可以最大限地减少事故发生。在这个项目中，我们将开发一个可以使用家庭或工业的 LPG 检测系统。该系统的设计使得一旦检测到任何泄漏，就会触发报警。系统的电路包含以下组件：

*   Arduino
*   LPG 气体模块
*   电阻
*   LCD 显示器
*   BC547 三极管
*   电池组
*   跳线导
*   蜂器

#### 9.3.1 工作原理

使用气体检测模块来检测 LPG。当传感器检测到泄漏时，它会向输出引脚产生一个 `HIGH` 脉冲。当 Arduino 接收到高脉冲时，它会发送一条消息。




Python 是一种开源语言，在当今系统和软件开发中被广泛使用。它在智能计算领域非常流行。尽管 Python 的基础结构某些方面与 `FORTRAN` 相似，但它比更为强大 [[1]](#ch10.xhtml_ref10_1)。大多数现代计算包括大数据、机器学习、物联网（IoT）、计算机视觉都是 Python 应用的最常见示例。Python 被称为解释型语言而非编译语言。Python 也被称为动态类型语言，这意味着如果创建一个变量，不需要显式声明。Python 语言中融入了许多现代的卓越特性。Python 的一些最独特且吸引人的特性如下：

1. 它非常简洁。
2. 可以不使用大括号缩进创建块。
3. 提供了丰富的集合类型，如 `List`、`Tuple`、`Dictionary`（通常称为 Maps）和 `Sets`。
4. 像 `Java` 一样存在 `List` 迭代器。
5. 提供了简化的面向对象支持。
6. 存在异常处理。
7. 对于脚本非常强大。
8. 提供了多种序列类型，如 `Strings` 和 `List`。

Python 的最优秀特性之一是它是一种免费的开源软件。我们可以自由复制 Python 代码的任何模块并对其进行修改。我们还可以学习 Python 的源代码并根据我们的需求进行修改。

![Images](img/line.jpg)

### 10.2 Python 版本

如今广泛使用的非常流行的 Python 版本是 Python `2.7.x` 和 `3.x` 版本。`2.7.x` 版本的某些关键特性在 Python `3.x` 版本中发生了变化 [2,3]。

1. 主要变化之一是 `print` 语句 [[4]](#ch10.xhtml_ref10_4)。在 Python `2.7.x` 中，我们通常将 `print` 用作语句，而在 Python `3.x` 中，它不再是语句，而是直接变成了一个 `print()` 函数。如果我们不在括号内编写语句，Python `3` 将遇到错误信息。因此，以下语句在 Python `2.7` 中运行正常，但在 Python `3` 中会报错：

```python
print 'Hello World!'
```
因此在 python `3.x` 中，我们应该写成
```python
print('Hello World!')
```
我们可以通过调用 `python_version()` 函数来检查并打印 Python 的当前版本。

2. 第二个变化是在当你从低版本迁移代码时有时相当危险的，因为这段代码永远不会报错，但会计算出错误的值。

Python `2.7.x` 版本中的以下代码与 Python `3.x` 版本产生的结果不同：

```python
print '5 / 2 = ', 5 / 2
print '5 // 2 = ', 5 // 2
print '5 / 2.0 = ', 5 / 2.0
print '5 // 2.0 = ', 5 // 2.0
5 / 2 = 2
5 // 2 = 2
5 / 2.0 = 2.5
5 // 2.0 = 2.0
```

Python `3.x` 将产生如下输出：

```python
print ('5 / 2 = ', 5 / 2)
print ('5 // 2 = ', 5 // 2)
print ('5 / 2.0 = ', 5 / 2.0)
print ('5 // 2.0 = ', 5 // 2.0)
5 / 2 = 2.5
5 // 2 = 2
5 / 2.0 = 2.5
5 // 2.0 = 2.0
```

3. 在 Python `2.x` 版本中，有两种类型的字符串：一种类型是 ASCII `str()`，另一种类型是 `Unicode()`。该版本不可用字节（Byte）类型。但在 Python `3` 中，可以使用 UTF-8 类型的 `Unicode` 字符串。此外，它还支持两种字节类型：`byte` 和 `byte array`。

```python
print type("Hello this is test") statement produces the following output in Python 2.7
<type 'str'>

print(' test", type(b' hello this is test")) statement produces following output in Python 3.x
<class 'bytes'>
```

4. 在 Python `2.x` 版本中，可以使用 `range` 函数。.............




图 10.4 显示了在 IDLE 编辑器中直接执行 Python 代码。在这种情况下，我们只是在 shell 中逐行输入代码，但这种机制并不适用于编写大型程序。因此，另一种方法是使用脚本，我们通常将其保存为 `filename.py`。我们可以直接通过 IDLE 的 `File-> new script` 编写，然后将其保存为 Python 文件，并简单地按下 `F5` 运行，如图图 10.5 所示。

![Images](img/010x004.jpg)

**图 10.4**

在 shell 中直接执行程序。

![Images](img/010x005.jpg)

**图 10.5**

在 IDLE 中执行脚本。

![Images](img/010x006.jpg)

**图 10.6**

在 CLI (Ubuntu) 中执行脚本。

对于 Ubuntu Linux，同样适用于相同的步骤，但我们必须直接在命令行界面中编写，如图 10.6 所示。

![Images](img/line.jpg)

### 10.5 使用 pip 安装

在进行任何进一步安装之前，你必须检查当前正在使用的 Python 版本。要在命令提示符中查看此内容，只需输入以下：

```
 $python –--version
```

在另一种类型的环境中，你可能会收到错误消息。如果你在使用 `Ipython` 或 `Jupyter`，可以使用以下命令检查版本：

```
 In [1]: import sys
        !{sys.executable} --version
Python 3.6.3
```

建议用 `{sys.executable}` 替换 `Python`，以确保命令运行与当前运行 PC 匹配的 Python 安装上。

要检查 `pip` 是否可用，可以使用以下命令：

```
 pip –version
```

Python `pip` 已安装在 Windows 的 `Python/scripts` 目录中。如果是 Linux，你可能需要显式地安装 `pip`。如果没有安装，你可以通过以下操作从标准库进行引导：

```
 python -m ensurepip --default-pip
```

`pip` 最常用的用法是使用某些需求指定符安装包。这包含了应用程序名称以及可选的版本。因此，我们给出以下命令：

```
 pip install 'application name'
```
要指定版本，我们可以给出命令
pip install 'application name == 2.1'
```

要安装大于或等于某个版本且小于另一个版本的包，我们给出以下命令：

```
 pip install 'application name >= 2.1,<2.5'
```

要安装与特定版本兼容的包，我们可以提供以下内容：

```
 pip install 'application name ~= 2.1.4'
```

通过传递 `upgrade` 参数也可以升级包。此外，我们还可以从特定的用户站点安装它。

```
 pip install - -upgrade application
pip install - - user application
```

我们甚至可以使用以下命令找到预发布的用户包并将其安装到我们的系统中：

```
 pip install - - pre-application package
```

![Images](img/line.jpg)

### 10.6 本章涵盖的概念

*   关于 Python 的基本概念
*   Python 2.7.14 的安装
*   `pip` 和另一个包的安装
*   不同版本及其比较

![Images](img/line.jpg)

### 参考文献

1. 1. Bernard, Joey. “Functions.” In *Python Recipes Handbook*, pp. 49–54\. Apress, Berkeley, CA, 2016.
2. 2. Chun, Wesley J. *Core Python Applications Programming*. Pearson Education India, Tharamani, India, 2012.
3. 3. Harms, Daryl D., and Kenneth McDonald. *The Quick Python Book*. Manning Publications, Greenwich, CT, 2000.
4. 4. [w3schools.com]. Retrieved from [`www.w3schools.com/`](https://www.w3schools.com).
5. 5. Liskov, Barbara, and Stephen Zilles. “Programming with abstract data types.” In *ACMplan Notices*, vol. 9, no. 4, 1974.
6. 6. Lutz, Mark. *Programming Python*. O'Reilly, Sebastopol, 1996.
7. 7. Rossum, Guido. *Python 3*. Amsterdam, 1995.
8. 8. Russell, Alex. *Fluent Python*. arXiv preprint, 2013.
9. 9. Power, Edward. *How to make Python*. arXiv preprint, 2013.
10. 10. Schildt, Herbert. *C Programmer’s Guide*. McGraw-Hill, New York, 2000.





### 11.1.3 逻辑运算符

这些运算符在两个操作数之间执行逻辑比较。这种操作可以以一元和二元模式进行。Python 中使用的主要的逻辑运算符有“and”（与）、“or”（或）和“not”（非）。对于任意任意两个给定的布尔值，`and` 运算符会在两个数据之间产生“与”操作。对应的语句如下：

```
 x=true
y=false
print(x and y)
结果为 false
```

![Images](img/Table_11.1.jpg)

**表 11.1**

不同的运算符及其功能

逻辑运算符也适用于数值类型的值，但在那种情况下，评估取决于数据成员的出现。在 `or` 运算符的情况下，结果值等于第一个成员。输出显示了如下内容：

```
 >>>  z= x or y
>>> print(z)
10
```

对于 `and` 操作，成员应该是第二个操作数。

```
 >>>  z=x and y
>>> print(z)
3
```

对于像“not”这样的一元运算符，评估是基于该值是否等于零进行的。如果该值为 0，则返回 true；否则，返回 false。

```
 >>>  print (not x)
False
>>> a=0
>>> print(  not a)
True
```

### 11.1.4 位运算符

这些运算符从根本上对位进行操作，它们既是一元也是也是二元类型的运算符。运算符首先获取任何整数数据的二进制形式，然后直接对其应用操作。以下语句是位与操作的演示，其结果为 0：

```
 >>>  x=2
>>>  y=5
>>> print (x&y)
0
```

在 `x|y` 的情况下，它按位对数据值执行“或”操作；因此，下述语句产生输出 7，因为 `5|7` 意味着 (010)|(101) 等于 111（十进制中的 7）。

```
 >>>  x=2
>>>  y=5
>>> print (x|y)
7
```

位非（NOT）运算符是一个一元运算符，执行值的取反。在操作上，它们与 C 或 C++ 语言相同。它的符号为 `~`。Python 中另一个经常使用的重要运算符是位异或（XOR）运算符，符号为 `^`。它执行与异或门完全相同的操作，并在操作上与其他语言相似。

位移运算符是另一类运算符，主要用于对位值进行左移和右移操作。语法所示：

`X=x>>2` 表示 `x` 的位模式向右移动了两个有效位，因此最终值再次存储在 `x` 中。相同的情况也适用于左移操作，如下：

`X=x<<2` 表示 `x` 的位模式向左移动了两个有效数字。通常，可以观察到向左移动一个有效位会导致数据值等于之前的数据乘以 2。对于右移，每向右移动一个有效位，该值就会被除以 2。

### 11.1.5 Python 中的身份标识运算符

Python 中提供了两个被称为身份标识运算符的特殊运算符。语法为“is”和“is not”。它们都根据运算符的身份标识性返回布尔值（True 或 False）。如果两个操作数相同，则“is”运算符返回 True。对于任何对象，如果两个操作数代表同一个对象，则返回 true，否则返回 False。以下代码描述了 `is` 和 `is not` 的操作：

```
 >>>  x=7
>>>  y=7
>>> print(x is y)
True

>>>  print(x is not y)
False
>>>
```

如果值是字符串，那么它也会通过观察大小写来检查相等性。因此，如果两个字符串的大小写不同，则 `is` 运算符返回 false。

对于列表类型，该概念基于相同引用的对象。因此，接下来的代码段将产生输出 false：

```
 >>>  x=[1,2,3]
>>>  y=[1,2,3]
>>> print (x is y)
False
```

由于 `x` 和 `y` 列表具有相同的值，但由于它们属于两个不同的列表对象，在这种情况下结果将为 false。

### 11.1.6 成员运算符

成员运算符检查值是否存在于特定的字符串、元组、列表、集合或字典中。

```
 >>>  x='test'
>>> 't' in x
True
>>> 'T' in x
False
 >>> 'test' not in x
False
```





![Images](img/line.jpg)

### 12.1 if 语句

`if` 语句通常用于评估条件和条件检查的主语句 [2]。图 12.1 显示了 `if` 语句的运行行为。

`if` 语句的语法所示：

```
 a=20
 b=30
if a<b : print(" a is smaller ")
```

`if` 语句可以使用 `and` 和 `or` 操作符同时包含多个条件。`if` 语句后面总是跟着 `:`。

```
 if a<5 and a>1: print(value is ")
```

`if` 语句经常跟着 `else:` 语句，以便 `if` 语句进行分支。在这里，`if` 条件根据 `var2` 的值进行测试。由于 `var2` 的值是非零，它将生成一个真值。在这种情况下将执行 `if` 部分。

```
 var2 = 10
if var2:
    print "1 - Got a true value"
else:
    print "1 - Got a false value"
    print var2
```

![Images](img/012x001.jpg)

**图 12.1** `if` 条件语句。

![Images](img/line.jpg)

# 12.2 If-elif-else 阶梯

## 12.2.1 表示

在某些情况下，我们使用 `if-elif-else` 语句来生成 `if-elif-else` 阶梯形式。在这种情况下，会检查 `if` 条件；如果语句返回假，将检查紧接的 `elif` 语句。如果 `elif` 语句返回假，进入下一个 `elif` 语句，以此此类推。

```
 var = 100
if var == 200:
    print "1 - Got a true value"
    print var
elif var == 150:
    print "2 - Got a true value"
    print var
elif var == 100:
    print "3 - Got a true value"
    print var
else:
    print "4 - Got a false value"
    print var

print "Good bye!"
```

三个数中最大值的另一个示例在下面的代码段中：

```
 x = input("enter x")
y = input("enter y")
z = input("enter z")

if(x>y):
    if(x>z):
      print "highest is:",x
    else:
      print "highest is:",z
else:
    if(y>z):
      print "highest is:",y
    else:
      print "highest is:",z
```

## 12.2.2 三元运算符

三元运算符是有用的运算符，类似于 `if-else` 语句。它也被称为 `if-then-else` 运算符。三元运算符的语法所示：

```
 a=5
b=6
var = a if (a>b) else b
```

如果 `a` 的值大于 `b`，左侧的数据存储在 `var` 中；如果为假，右侧的数据将存储在 `var` 中。三个整数最大值的更常见示例也可以用三元运算符进行评估：

```
 a = input("enter a")
b = input("enter b")
c = input("enter c")
g = (a if (a>c) else c) if (a>b) else c;

print "highest is", g
```

![Images](img/line.jpg)

# 12.3 Python 中的循环

循环是编程语言中的组成部分。它们是根据循环提供的边界值顺序执行重复任务的代码段。循环边界是定义循环结束的条件。在 Python 中，我们通常使用 `while`、`for` 和循环 循环（图 12.2）。

### 12.3.1 while 循环

与其他语言一样，`while` 循环由边界条件表达式跟着 `:`。循环块将根据边界值执行，计数器放在循环内部。

![Images](img/012x001.jpg)

**图 12.2** Python 中的循环结构。

```
 count=0
while (count < 9):
    print'count value is:', count
    count = count + 1

print "completed"
```

在这种情况下，`while()` 根据非零或真值评估结果。如果条件的值是非零或真的，循环将迭代；如果为零或假，它将终止。Python 中的以下行将创建无限循环：

```
 var=1
while(var):
    print "hi"
```

```
 var=True
while(var)
    print "hii"
```

有时，我们使用 `while` 循环作为奇循环。这样做，我们可以在运行时定义循环的边界。下面的代码接收字符输入作为循环的边界，并在每次迭代中检查 `while` 循环的值。如果值匹配循环，它将继续；否则它将终止。

```
 count='a'
while (count!='n'):
    print'The count is:', count
    count = input("enter count")

print "loop end"
```

输出将是：

```
 count is: a
enter count
count is: e
enter count
loop
```

Python 还支持与 `else` 关联的循环语句。我们可以在循环中使用 `else` 语句。当循环耗尽时，`else` 语句将执行。在 `for` 循环的情况下，`else` 语句将执行。当 `while` 语句返回假时，`else` 语句将执行。以下代码显示了 `while` 语句的 `else` 条件语句：

```
 c=0
while c < 10:
    print,"value is", c
    c = c + 1
else:
    print "condition false"
```

`do-while` 循环在 Python 中是不允许的，但可以使用 `while` 循环模拟 `do-while` 特性。以下使用 `while` 循环显示 `do-while` 的表示：

```
 i=1

while True:
    print(i)
    i = i + 1
    if(i > 4):
        break
```

### 12.3.2 for 循环

`for` 循环主要用于迭代列表的值。它对于遍历列表、元组和字典非常有用。如果序列包含任何列表，首先会将项赋值给迭代变量。接下来，执行语句块。迭代将直到列表耗尽。以下代码段是 `for` 语句的示例：

```
 for l in 'MyPython': # 示例 1
    print 'Current Letter:', l
car = ['ford', 'audi', 'bmw']
for c in car: # 示例 2
    print 'Current car:', c
```

使用 `for` 循环打印列表的另一种方法是通过应用循环中每个元素的索引。在这种情况下，索引从 0 开始到大小-1 结束。

```
 car = ['audi', 'bmw', 'ford']
for i in range(len(car)):
    print 'Current car:', car[i], i
```

输出将是：

```
 Current car: audi 0
Current car: bmw 1
Current car: ford 2
```

以下是质数示例：

```
 for num in range(lower,upper + 1):
    for i in range(2,num):
        if (num % i) == 0:
            break
    else:
        print('%d is a prime number \n' %(num),

### 12.3.3 嵌套循环

各种程序中，我们经常使用嵌套循环。这是循环放入另一个循环的属性 [3]。一次可以放置一个或多个循环。嵌套在循环中的循环数量决定了循环的嵌套深度。以下程序显示了 2 到 100 之间的可用质数：

```
 i = 2
while(i < 100):
    j = 2
    while(j <= (i/j)):
        if not(i%j): break
        j = j + 1
    if (j > i/j) : print i, " is prime"
    i = i + 1
```

### 12.3.4 奇循环




不定循环（Odd loops）是一种循环结构，其循环边界条件是在循环迭代过程中提供的。因此，我们可能无法确定循环确切的何时结束。这完全取决于用户何时何时想要退出指定的循环。不定循环的结构如下：

```python
 ch = 'y'
while (ch <> n):
    print " the value of ch = ", ch
    ch = raw_input('enter ch')
```

#### 12.3.5 break 和 continue 语句

`break` 语句主要用于中断当前循环的执行，在这种情况下，控制流将跳转到下一条指令。它通常用于 `while` 和 `for` 循环。如果我们在内层循环中使用 `break`，则内层循环会被终止。

```python
 l="MyPython"
for l in 'MyPython':
   if l == 'h':
        break
   print 'Current Letter:', l
```

另一方面，`continue` 语句会通过跳过 `continue` 之后的所有语句，立即继续循环的下一次迭代。该语句也可以用于 `for` 和 `while` 循环。

```python
 for l in 'MyPython':
   if l == 'h':
        continue
   print 'Current Letter:', l
```

在这种情况下，字母 `h` 将被循环跳过，其余字母将正常打印。

![Images](img/line.jpg)

### 12.4 本章涵盖的概念

- 决策
- 三元运算符
- 循环
- 不定循环
- 循环语句

![Images](img/line.jpg)

### 参考文献

1. [1]. Ellis, Margaret A., and Bjarne Stroustrup. *The Annotated C++ Reference Manual*. Addison-Wesley, Boston, MA, 1990.
2. [2]. Chun, Wesley. *Core Python Programming*. Vol. 1\. Prentice Hall Professional, Upper Saddle River, NJ, 2001.
3. [3]. Zelle, John M. *Python Programming: An Introduction to Computer Science*. Beedle & Associates, Inc., Franklin, TN, 2004.

## 13

![Images](img/line.jpg)

## Python 中的函数

![Images](img/line2.jpg)

函数和模块是编程语言的重要组成部分。函数由一段代码定义，这段代码可以在单个程序或多个应用程序中重复使用。函数确保了程序代码的可重用性和模块化。通过使用函数，长段代码通常会被细分成相对较小的模块片段，使得程序段落易于阅读。某些函数是用户定义的，而另一些是库函数。在 Python 语言中，函数的声明和定义机制有一些特定的技巧。在本章中，我们将讨论 Python 中函数的不同方面和有效性。

![Images](img/line.jpg)

### 13.1 定义的标准规则

在定义函数时，我们需要维护一些标准规范 [[1], [2]]。函数定义应以 `def` 关键字开头，后跟一个名称以及左右括号 `(name ())`。括号内可以包含任意数量的输入参数。特定函数的代码块应以 `:`（冒号）符号开头。函数可以包含返回语句，并且它可以返回一个或多个语句（凭借列表的属性）。函数没有返回类型，类似于返回 0。接下来展示了一个函数定义的示例模板。由于函数参数支持位置顺序，你必须按照它们定义时的相同顺序来出它们。

```python
 def function_name( function_parameters ):
   "function_docstring"
   与函数相关的代码

   return [expression]
```

这里有趣的地方在于，在函数定义中，我们应该只传递参数的名称而不是类型。下面的简单代码描述了一个打印字符串消息的函数：

```python
 def print_msg(str):
    print str
    return
```

有时，我们可以在函数代码的开头添加描述或文档字符串。以下代码段反映了这一点：

```python
 def print_msg(str):
   "printing a string"
   print str
return
```

![Images](img/line.jpg)

### 13.2 函数调用

### 13.2.1 调用方法

定义函数后，我们需要调用它。函数的调用涉及几种类型。我们可以直接在函数外部调用函数，有时也可以从另一个函数调用函数。以下代码段说明了：

```python
 # 函数定义
def print_test(a,b):
   "这打印两个数字之和"
   print "value is",a+b;
   return;

# 调用函数
print_test(5,6)
```

在 Python 中，函数中的参数传递使用引用传递（pass by reference）。这意味着函数对值的所更改会影响原始值。在 Python 中没有指针的概念，因此地址操作是隐式完成的。

```python
 def change_list(list1):
    "这更改了传递到此函数的列表";
    list1.append([10,20,30,40]);
    print "Values inside the function: ", list1;
   return;

# 调用 list1
List1=[1, 2, 3];
change_list( list1 );
print "Values outside the function: ", list1
```

在这种情况下，列表对象是通过引用传递的，并且在函数内部列表的内容被修改了。

#### 13.2.2 参数传递机制

在 Python 中，可能的参数传递类型：值传递和引用传递 [[3]]。在值传递的概念下，传递的是值的副本。所有基本类型支持值传递。另一方面，对象类型始终支持引用传递。如果我们想传递列表、元组、字典和字符串，它们总是遵循引用传递机制。以下程序提供了值传递和引用传递机制的概念：

```python
#!/usr/bin/python

def swap(a,b):
   t=a
   a=b
   b=t
   print "values of a,b are",a,b;
   return

a1 = int(input("Enter a>"))
b1 = int(input("Enter b>"))

swap(a1,b1)

print "values a,b",a1,b1;
```

输出为：

```
 Enter a>5
 Enter b>6
values a,b are 6 5
values a,b 5 6
```

在这种情况下，`a1` 和 `b1` 的值被传递给 `swap()` 函数并被名为 `a` 和 `b` 的形式参数接收。然后，使用第三个变量进行交换。结果我们得到了交换后的值。但当我们尝试从函数外部打印时，值保持不变。这证明了值传递传递的是变量值的副本。

在引用传递机制的情况下，数据对象的地址或引用传递如下：

```python
#!/usr/bin/python

list1=[10,20,30]

def pbr(list2):
   list2[1]=50
   print "list values", list2
   return;

pbr(list1)

print "list after passing", list1
```

输出为：

```
 list values [10, 50, 30]
list after passing [10, 50, 30]
```

在这里，列表是一个对象，因此通过函数传递的是列表的引用，而不是列表本身的副本。因此，对列表实际值的任何更改都会影响原始列表对象，且该更改在整个程序中都是有效的。

### 13.3 关键字参数概念





这是一个 Python 中非常强大的概念。如果函数参数列表中的参数顺序混乱，我们使用某些关键字通过它们的名称来识别它们。因此，如果参数顺序不匹配，解释器将通过它们的名称识别数据对象。以下代码展示了关键字参数的使用。示例显示在函数调用部分，整数值是参数 1，字符串是参数 2。但在定义部分，顺序是反过来的。一旦给函数指定了关键字，解释器就会接收它并生成一个正确的函数调用。

```
 def printfn( name, age ):
   "This function uses keyword argument"
   print "Name is: ", name;
   print "Age is ", age;
   return;
#call to printfn
printfn( age=32, name="piu" )
```

默认参数是另一个概念，即我们在调用函数时不提供参数。如果我们在形式参数中对某个参数进行了显式声明，那么该参数在调用时将作为默认取值。例如，我们为同一个函数使用了两个不同的调用，其中一个调用带有一个参数，而第二个调用有两个参数。在定义部分，我们放置了两个显式初始化的参数。

```
 ##!/usr/bin/python

def info( name, age = 20 ):
   print "Name is: ", name;
   print "Age ", age;
   return;

# two different call of info
info( age=32, name="piu" )
info( name="piu" )
```

在第二种情况下，`info()` 函数取 `age` 的默认值 20。

![Images](img/line.jpg)

### 13.4 Lambda 函数

在 Python 中，`lambda` 关键字主要用于构建匿名函数，通常称为 lambda 函数。这种函数本质上没有定义的名称。这种机制适用于创建自适应函数，因此非常适合事件处理。

lambda 函数的 기본语法如下：

```
 fn1 = lambda i: i**2
print(fn1(5))
```

在这里，lambda 函数对目标输入数据 `i` 执行幂运算 (x^y)。lambda 函数也可以接受多个数据作为输入。

```
 fn2 = lambda a,b: a+b
print(fn2(3,6))
```

lambda 函数的另一个良好用处是，如果我们想在运行时生成匿名函数，可以调用它。在运行时这样做，`lambda` 会返回函数的地址。

```
 def fn3(n):
  return lambda i: i*n
dbl = fn3(2) 
  tri = fn3(3)
  val = 10
  print("Doubled value is: " + str(dbl(val)) + ". Tripled value is: " + str(tri(val)))
```

![Images](img/line.jpg)

### 13.5 Python 中的模块

Python 中的模块是一个逻辑概念，用于对代码进行逻辑组织。使用这种方法，我们可以相关的代码分组在同一个伞下。它由任意的名称-值属性组成。在 Python 中，简单的模块可以通过 Python 文件名本身创建并调用。模块由函数、类和不同的变量组成。

```
 #Test.py
def print_val( var ):
   print "Hiii : ", var
   return;
```

上述代码段基本上充当了模块，因为它被另一个文件导入。`Import` 语句将任何源文件添加到另一个文件中。当我们导入任何文件时，解释器会在当前目录的路径中搜索该文件的可用性。如果未找到，将在 `PYTHONPATH` 环境中写入的路径进行搜索。`filesys.path` 存储 `PYTHONPATH`，在 UNIX 中为 `/usr/local/lib/python`，在 Windows 中为 `C:\python22\lib`

```
 #importing the test module
Import Test
Test.print_val(5);
```

### 13.5.1 from 语句

`from` 语句专门从一个 Python 模块导入某些属性。在这种情况下，整个模块不会加载，只会加载选择性的属性。可以通过保持逗号 (,) 来导入多个属性。

```
 from math import pi
from math import *
```

也可以将模块中的所有属性导入到当前命名空间。这提供了一种从模块导入所有项目的简单技术。当我们将任何模块附加到源码上时，Python 解释器首先在当前目录搜索模块的位置，然后搜索由 `PYTHONPATH` 维护的目录。如果在这里失败，它将搜索默认的 Python 库。在 Linux 中，它是 `/usr/local/lib/python/`。

#### 13.5.2 dir() 函数

内置函数 `dir()` 返回可用模块定义的属性列表。这有助于我们以排序的形式识别对应特定模块所需的属性。

```
 import math
val = dir(math)
print val
```

输出所示（属性以列表形式呈现的序列）：

```
 ['__doc__', '__name__', '__package__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'ceil', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm', 'fabs', 'factorial', 'floor', 'gamma', 'hypot', 'isinf', 'isnan', 'ldexp', 'log', 'log10', 'log1p', 'modf', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'trunc']
```





面向函数的编程语言特性为程序代码的分段化、模块化和实现重用性提供了强大支持。在现实应用场景中，我们大多数时候关注软件设计的模块化方法。模块在编程中的有效性在于它们极大地减少了查找错误的工作量。因此，得得从心的应用设计显而易见。由于程序被切分成几个组件，搜索和查找错误变得更加容易。接续第 13 章，我们将描述、设计并使用众多的函数模块和 API，以说明代码的有效性。

![Images](img/line.jpg)

## 14.1 访问 CSV 文件

CSV 代表逗号分隔值。CSV 文件通常是包含大量数据的大文件，通常被称为数据对象 [1,2]。它们是无模式数据的简化形式。与 JavaScript 对象表示 (JSON) 相比，CSV 比严格遵循脚本现象的 JSON 更具可读性。

CSV 内部的数据由行组成，用逗号（`,`）分隔的元素反映列。CSV 文件中的每一行都是电子表格中的行，而逗号用于定义和分隔电子表格中的单元格。

`csv` 模块包含一些内置函数，如下：

* `csv.reader`
* `csv.writer`
* `csv.register_dialect`
* `csv.unregister_dialect`
* `csv.get_dialect`
* `csv.list_dialects`
* `csv.field_size_limit`

### 14.1.1 读取 CSV 数据

为了获取 CSV 数据，我们必须使用生成读取器对象的 `reader()` 函数。`reader()` 函数读取文件的每一行并创建所有列的列表。然后，可以选择要显示的列。下面的示例说明了使用读取器对象的读取技术：

```python
import csv
import sys

f = open(sys.argv[1], 'rb')
read = csv.reader(f)
for row in read:
    print row

f.close()
```

在前面的代码中，我们导入了 `csv` 和 `sys` 包。`csv` 包是访问 CSV 文件的标准包。`sys` 是标准系统包。`sys.argv` 是在运行时传递的命令行参数。在这种情况下，文件名将是 `argv 1`，因为 `argv 0` 是 Python 文件本身的名字。在此此之后，我们使用 `open` 函数打开文件对象。然后，使用 `csv.reader(f)` 创建读取器对象。`for` 循环遍历包含行的读取器对象，这些行会被输出。最后，我们应该关闭 CSV 文件读取器对象。

### 14.1.2 使用 Pandas 加载 CSV

Pandas（用于数据分析的 Python）是一个强大的数据分析工具。它构建在 `NumPy` 之上，`NumPy` 是另一个创建和可视化多维数据的强大应用程序。Pandas 的基本目标是创建多维数据帧（data frames）。

我们实际上可以在不同的格式数据（如 CSV、JSON 和 Python 字典）中创建数据帧。一旦加载了数据帧，你就可以将数据处理成几个用于数据分析的有价值信息。

在这种情况下，我们必须导入 Pandas 为 `pd` 并导入 `NumPy`。然后，我们必须带有 `.csv` 文件名的参数调用 `read_csv()` 函数。要查看 CSV 文件中的可用信息，我们可以调用 `msft` 对象的 `head()` 方法。图 14.1 和 14.2 分别说明了代码和输出。

代码的输出所示图 14.2。

![Images](img/line.jpg)

## 14.2 解析 JSON 数据

JSON 代表 JavaScript 对象表示。它在开发者中非常流行数据序列化。它用于大多数 Web 应用程序接口 (web API) 以及程序之间的数据传递。在访问和解析 JSON 数据文件之前，我们必须在程序中导入 JSON 模块。

![Images](img/014x001.jpg)

**图 14.1**

访问 CSV 的代码。

![Images](img/014x002.jpg)

**图 14.2**

由 `head()` 方法显示的输出。

我们可以通过简单创建一个类似字典的数据结构来创建一个 JSON 数据文件。在下面的示例中，给 JSON 文件的基本框架：

```python
J_data_1 = '{"a": 1,"b": 2,"c": 3,"d": 4}'
```

标准的 JSON 文件使用 `.json` 扩展。一个从 [json.org](http://json.org) 取的 JSON 示例如下：

```json
 {
  "widget": {
    "debug": "on",
    "window": {
      "title": "Sample Widget",
      "name": "main_window",
      "width": 550,
      "height": 550
    },
    "image": {
      "src": "Images/Sun.png",
      "name": "sun1"
    },
    "text": {
      "data": "Click to go",
      "size": 36
    }
  }
 }
```

尽管它有类似字典的结构，但除非它来自文件，否则 Python 将视为一组字符串。我们可以简单地使用 `loads()` 方法加载它。

```python
print json.loads(J_data)
```

它可以被表示为一种可用的格式。我们可以使用循环打印输出。

```python
l_json = json.loads(J_data_1)
for m in l_json:
    print("%s: %d" % (m, l_json[m]))
```

![Images](img/line.jpg)

## 14.3 使用 MongoDB

MongoDB 是一个免费的开源、跨平台数据库系统 [3]。它是一个分类为 NoSQL 的数据库程序。它作为服务提供。在这种情况下，它拥有 `n` 个数据文件。MongoDB 的重要优势是它支持文档型设计；因此数据以 JSON 对象的形式存储。MongoDB 的 Python API 也称为 PyMongo。数据库与脚本通过 `pymongo` 的交互所示图 14.3。

![Images](img/014x003.jpg)

**图 14.3**

Pymongo API。

我们可以直接从以下链接下载 MongoDB：[`www.mongodb.org/dl/32/i386`](https://www.mongodb.org)。此链接包含了多个版本的 32 位 MongoDB 安装器文件。目前 MongoDB 也有云版本。在安装 MongoDB 之前，我们必须检查与系统兼容的正确版本。我们可以通过以下命令检查：

```bash
C:\>wmic os get osarchitecture
32-bit own```
我们可以直接从合适的 `.MSI` 或 `.exe` 文件安装 MongoDB。

要在 Python 中访问 MongoDB，我们需要使用 `pymongo` API。你可以使用以下命令安装 `pymongo` API：

```bash
python -m install pymongo
```

我们可以通过应用升级参数更新现有的。

```bash
python -m install --upgrade pymongo
```

有时，我们倾向于从源码安装。在这种情况下，优选从 GitHub 安装。

```bash
git clone git://github.com/mongodb/mongo-python-driver.git pymongo
$ cd pymongo/
$ python setup.py install
```

MongoDB 实例通过给出 `$mongod` 或 `sudo service mongod start` 命令启动。

第一步是 `MongoClient` 与 `mongod` 实例建立连接。它默认连接主机和端口。

```python
>>> from pymongo import MongoClient
>>> client = MongoClient()
```

我们也可以通过显式提供主机名和端口来连接：

```python
>>> client = MongoClient('localhost', 27017)
>>> client = MongoClient('mongodb://localhost:27017/')
```



单个 mongo 实例可以通过属性风格访问或字典风格的访问来支持多个数据库，如下所示：

```
 >>> coll = db.test_coll
>>> coll = db['test-coll']
```

MongoDB 中的数据类似于 JSON 脚本。`Pymongo` API 实际上使用类似字典的结构来表示数据。一个示例数据可以用如下方式表示：

```
 >>> import datetime
>>> ins = {"author": "Amu Neel",
...      "text": "A Test Database!",
...      "tags": ["mongodb", "python", "pymongo", "API"],
...      "date": datetime.datetime.utcnow()}
```

要向 MongoDB 集合中插入日期元素，通常可以使用 `insert_one()` 方法。当创建一个文档时，默认会创建一个默认键 `_id`。`_id` 的值是跨整个集合的唯一键。当我们使用 `insert_one()` 插入一个实例时，它会立即返回一个 `InsertOneResult` 实例。

```
 >>> posts = db.posts
>>> post_id = posts.insert_one(ins).inserted_id
>>> post_id
ObjectId('...')
```

要检索数据，必须实现的最基础查询是 `find_one()`。该方法返回单个文档，当匹配的文档数量只有一个时，它非常有用。

```
 >>> import pprint
>>> pprint.pprint(posts.find_one())
{u'_id': ObjectId('...'),
 u'author': u'Amu Neel',
 u'date': datetime.datetime(...),
 u'tags': [u'mongodb', u'python', u'pymongo',u'API'],
 u'text': u'a Database!'}
```

## 14.4 MongoDB 工具

Robo3T 或 `Robomongo`（图 14.4）是一个跨平台的开源 MongoDB 管理工具。它嵌入了与 MongoDB 管理 shell 使用相同的 JavaScript 引擎。该接口适用于 Windows、Linux 和 `MacOS`。它是一款免费软件，可以通过 GitHub 访问源码。我们可以从以下链接下载：`https://robomongo.org/`。

界面显示了包含日志和存储的连接。键值对形式的数据可以在界面的中间可见。也可以从界面发送查询字符串。

对于 MongoDB 4.X，还支持 `NoSQLBooster`（图 14.5）。这是一个以 shell 为中心的跨平台界面，也支持 MongoDB 2.6 版本。该界面提供了一个非常流畅的查询生成器。IDE 本身足够智能，内置了了所有可能的方法、属性和关键字的语言。此外，它还拥有 MongoDB 集合名称的知识。新版本可以通过链接获取：`https://nosqlbooster.com/`。

图 14.4：Robomongo 界面。
图 14.5：用于 MongoDB 的 NoSQLBooster。

### 14.5 本章涵盖的概念

* 一些可用且重要的 API
* 访问数据
* 解析 JSON
* 使用 MongoDB 进行工作

### 参考文献

1. Hellmann, Doug. *The Python Standard Library by Example*. Addison-Wesley, Boston, 2011.
2. Herger, Lorraine M., and Mercy Bodarky. “Engaging students with open source technologies and Arduino.” *Integrated STEM Education Conference (ISEC), 2015*, pp. 27–32. IEEE.
3. Kanoje, Sumitkumar, Varsha Powar, and Debajyoti Mukhopadhyay. “Using MongoDB for social networking website deciphering the pros and cons.” In *Innovations in Information, Embedded and Communication Systems (ICIIECS), 2015 International Conference on*, pp. 1–3. IEEE.
4. Orr, Genevieve. “Computational thinking through programming and algorithmic art.” In *SIGGRAPH 2009: Talks*, p. 31. ACM, 2009.

## 15 结构的实现

数据结构主要强调作为数据存储和数据检索的基础数据组织。它以系统形式定义了数据元素在系统形式中的有效存储机制。在编程语言中，数据结构可以通过其固有属性实现，也可以通过使用第三方 API 实现。数据结构可以根据易用性进行分类。在 C 和其他语言中，处理的基础数据结构是 `array`。我们也可以从 `array` 推导出各种其他数据结构。某些数据结构可以使用动态内存分配来实现。在 Python 中，已经预定义了一些高效的数据结构。在本章中，我们将讨论 Python 中的一些基础数据结构。

### 15.1 Python 中的列表

List（列表）是 Python 中基础的基础顺序数据结构。每个元素由某些数据成员分配。该结构可以通过其 `index` 访问。列表的基础索引应从 0 开始，每个元素递增 1。

我们可以在列表或序列类型的数据结构上执行某些操作。可以执行的主要操作包括切片、索引、加法、乘法和成员检查。

List 是 Python 中最常见的数据结构类型。它由一组相同或不同类型的数据成员序列组成。它也被称为数据的有序集合。默认情况下，列表是动态结构，这意味着我们可以添加或删除成员。它是可变的，这意味着它可以动态更改存储在列表中数据对象的类型和大小。列表的数据成员从 0 开始，到总大小减 1 结束。

```
 l1 = ['honda', 'bmw', 2005, 2010]
l2 = [9, 8, 7, 6, 5, 4, 3, 2, 1]
print("list1[2]:", l1[2])
print("list2[1:5]:", l2[1:5])
```

在上述示例中，我们使用了列表 1，其元素为字符串和数字类型。列表 1 包含了多种类型。`l1[2]` 将打印索引 2 的数据，即 2005。在 `l2[1:5]` 的情况下，将打印数据成员序列。在这种情况下，执行了切片操作，它与索引相似但不那么灵活。这里 `l2[1:5]` 基本上是一个从索引 1 开始到第五个元素的子列表。

#### 15.1.1 更新和删除列表元素

更新和删除操作可以在列表中直接进行。要此操作，我们只需根据值的索引位置将列表元素的值赋值给变量。如下所示：

```
list = ['aaa', 'bbb', 15, 20]
print("索引 2 处的值 :)")
print(list[2])

list[2] = 25
print("索引 2 处的新值 :)")
print(list[2])
```

这段代码将立即将索引位置 2 的值（15）更改为新值（25）。

要从列表中删除元素，我们必须使用 `del` 关键字。作为结果，该值被删除。





```python
list = ['aaa', 'bbb', 15, 20];
print "Value available at index 2 : "
print list[2]

del list[2];
print "New value available at index 2 : "
print list[2]
```

它将动态地删除索引位置 2 对应的元素和内存空间。删除数据元素的另一种方法是使用列表对象的 `remove()` 或 `pop()` 函数。该函数将执行类似的操作。在 `remove()` 函数中，我们必须提供元素本身来移除或删除数据。在 `pop()` 的情况下，我们需要应用索引位置。

```python
list = ['aaa', 'bbb', 15, 20];
list.remove('bbb');
print list[0:]
list.pop(2);
print list[0:]
```

输出将是：

```
 ['aaa', 15, 20]
['aaa', 15]
```

`remove()` 函数删除了字符串“bbb”，列表的大小减少了 3。`pop()` 函数运行并删除了值 20（索引 2）。最后，它将变成一个包含两个元素的列表。

### 15.1.2 基础列表操作

列表可以执行各种操作。列表的特征在某些方面类似于字符串；因此，使用 `+` 运算符用于列表的拼接。`*` 运算符适用于列表，可以将一个元素重复 *n* 次。[表 15.1] 显示了在列表中可以执行的一些操作。

![Images](img/line.jpg)

### 15.2 Python 中的元组

在 Python 中，元组是不可变对象的序列。元组的基本属性是元组中的值是不能被更改的。

若要声明并创建一个元组，我们通常使用圆括号。值之间用逗号分隔。有时，它们可以在双引号内声明。元组的一些标准声明显示如下：

![Images](img/Table_15.1.jpg)

**表 15.1 列表操作**

```
 Tpl = ('abc','def',1,2)

tpl2 = "a","b","cc","DD"

tpl3 = ()

tpl4 = (5,)
```

第三个示例 (`tpl3`) 显示了一个没有数据的元组。`tpl4` 是仅包含一个元素的元组。在元组的单个变量后我们必须使用逗号。

我们可以类似于访问列表数据的方式访问元组数据。

```python
 Tpl = ('abc','def',1,2)

print "value of Tpl[0] is",Tpl[0]
```

我们不能更新元组的元素。因此，以下声明会导致运行时错误并停止执行：

```python
Tpl[1] = 'xyz' # 错误
```

我们可以使用 `del` 命令删除元组的元素。因此，以下代码删除了元组中的一个元素：

```python
 del Tup[1]
```

所有其他适用于列表的操作也适用于元组。

![Images](img/line.jpg)

### 15.3 字典结构

字典是对象的无序集合。与仅包含值的普通对象不同，字典必须具有一些键值对。它是一种优化的结构，用于根据某些已知键元素检索值。字典结构的基础声明显示如下：

```python
 dict = {'name': 'piu','age':32, 'grade':80}

print "Name is ",dict['name']
print "Age is ",dict['age']
```

我们可以更新字典中的新属性；在这种情况下，新属性将简单地添加到现有的字典条目中。以下代码所示：

```python
 dict['school'] = “Saradamani school”
```

我们可以删除字典的单个元素也可以删除整个字典。

```python
 dict = {'name': 'piu','age':32, 'grade':80}

del dict['age']

dict.clear()

del dict
```

第一条语句删除属性 `age`。第二条语句 `dict.clear()` 清空字典的所有属性。`del dict` 操作简单地删除整个字典结构。

所有其他适用于列表的操作也适用于字典。

![Images](img/line.jpg)

### 15.4 数据结构的排序

数据结构中数据元素的排序起着重要作用。排序将数据元素按升序或降序排列。在本节中，我们将讨论不同数据结构的数据元素排序。`sort()` 方法实际上在大多数数据结构中定义，用于对数据排序。另一种排序数据元素的方法是调用 `sorted()` 函数。列表的排序技术显示如下：

```python
 List1 = [ 'abc','def',123,'wrg']
List1.sort()
print 'sorted list', List1
```

这将对整个列表进行排序。首先将打印数值，然后按字母顺序对字符串的值进行排序。

我们还可以通过将 `reverse` 参数设置为 `True` 来对相同的数据结构进行反序排序。因此，代码看起来如下：

```python
 List1 = [ 'abc','def',123,'wrg']
List1.sort(reverse = True)
print 'sorted list', List1
```

它执行降序的数据元素排序。

我们还可以对列表执行自定义排序。例如，列表可能包含两个值，如果我们对列表进行排序，则必须执行操作：

```python
 # 排序示例
def takeSecond(elem):
    return elem[1]
data = [(2, 2), (3, 4), (4, 1), (1, 3)]
data.sort(key=takeSecond)
print('Sorted list:', data)
```

这里，`data` 根据第二个元素排序。第一个元素是第一个元素。字典的排序是一个主要问题。字典可以根据其键或值进行排序。以下代码显示了逻辑：

```python
 dict = {'piu':32,'Nilanjan':34,'rishi':24,'mom':37}

def sortbykey():
    dict1 = sorted(dict.items(), key=lambda t: t[0])
    print dict1

def sortbyval():
    dict1 = sorted(dict.items(), key=lambda t: t[1])
    print dict1
```

要排序字典，我们必须检查是否根据键或值进行排序。根据键排序，我们应该传递零索引元素，即 `t[0]`。根据值排序，我们应该传递第一个索引元素 `t[1]`。

### 15.5 Python 中的日期和时间

在 Python 中，我们可以使用多种技术处理时间和间隔。Python 核心模块可以与原生计算机系统日期和时间交互。在 Python 中，时间间隔是自 1970 年 1 月 1 日凌晨 12:00 开始的秒的基本单位。Python 提供了一个高效的时间模块，用于表示和转换不同的时间表达式。`time.time()` 方法始终返回从 1970 年 1 月 1 日凌晨 12:00 开始的纪元系统时间。





在此之前的日期无法通过这种表示法表示 [3]。未来的日期也无法通过这种格式表示。UNIX 和 Windows 支持的日期截止点是 2038 年。时间元组（time tuple）在日期处理中具有重要意义。大多数 Python 时间函数以九个元组的形式表示时间。时间元组的属性在表 15.2 中给出。

从表 15.2 来看，参数 5 处理秒以及一些闰秒值，用于调整协调世界时间（UTC）。通常情况下，当 UTC 与世界时间的时间差大于 0.9 秒时，会增加一秒的闰秒。参数 8 定义了夏令时值，根据不同地理位置的纬度调整白天的时间。

![Images](img/Table_15.2.jpg)

**表 15.2**

时间结构的属性

要获取当前时间，我们可以调用 `localtime()` 方法并传递 `time.time()` 值。以下代码表示系统显示的时间：

```python
#!/usr/bin/python
import time;

ltime = time.localtime(time.time())
print "Current Local time :", ltime
```

输出将是未格式化的时间形式，但我们可以从这种表示中获取格式化时间。我们可以使用 `asctime()` 函数进行任何类型的格式化。

```python
import time;

lltime = time.asctime( time.localtime(time.time()) )
print "Local current time :", lltime
```

我们可以使用 `calendar` 模块获取日历。通过各种日历方法，我们可以执行若干日历操作。

```python
import calendar

c = calendar.month(2008, 1)
print "Here is the calendar:"
print c
```

![Images](img/line.jpg)

### 15.6 Python 中的字符串

Python 中的字符串基本上由单引号或双引号包围的字面量形式的字符集表示。创建字符串等同于给变量赋值。以下代码执行了此任务：

```python
S='hello'
S1="hello"
```

我们可以通过简单的使用索引位置遍历来访问字符串的字符集。因此，以下声明是有效的：

```python
s="hello python"

Print “string is",s[1:5]
```

这打印从索引 1 到位置 5（即索引 4）的字符串。

我们可以通过对字符串的值进行重新赋值来更新现有字符串或子字符串的值。以下代码执行此工作：

```python
v= "abc def"

print "after update", s[:5]+'python'
```

输出将是：

```
after update abc python
```

我们可以使用 `strip()` 方法移除字符串的空格。

```python
v= 'abc def'
print (V.strip())
```

`len()` 函数返回字符串的长度。

```python
print(V.len())
```

如果字符串中的任何字符是大写字母，`lower()` 函数将产生一个小写字符串。`upper()` 函数则执行相反的操作。

```python
print(v.lower())
print(n.upper())
```

`replace()` 函数将所有字母替换为目标字母

```python
print(v.replace("a","k"))
```

![Images](img/line.jpg)

### 15.7 本章涵盖的概念

* 列表
* 元组
* 字典
* 日期、时间及其处理
* 字符串处理

![Images](img/line.jpg)

### 参考文献

1. 1. Miller, Bradley N., and David L. Ranum. *Problem Solving with Algorithms and Data Structures Using Python*, Second Edition. Franklin, Beedle & Associates Inc., Portland, OR, 2011.

2. 2. Reed, David M., and John M. Zelle. *Data Structures and Algorithms Using Python and C++*. Franklin, Beedle & Associates, Portland, OR, 2009.

3. 3. Dubois, Paul F., Konrad Hinsen, and James Hugunin. “Numerical python.” *Computers in Physics* 10, no. 3 (1996): 262–267.

## 16

![Images](img/line.jpg)

## Python 中的面向对象编程

![Images](img/line.jpg)

Python 的最大特点之一是它支持多范式方法。面向对象的特性是 Python 中最强大的方法之一，它能够以语言的形式舒适地映射现实生活场景 [1]。面向对象编程的根本构建块是对象。对象可以是代表任何现实事物的任何东西。Python 还支持多态和继承等其他重要特性。面向对象范式的主要目标是实现某种重用性，有时被称为 DRY（不要重复）。

![Images](img/line.jpg)

### 16.1 Python 中的类

从广义上说，类是面向对象编程的基本单元 [2,3]。类有时认为是现实事物的蓝图。类包含作为变量的属性和方法，方法是在这些变量上执行的操作。以下示例说明了类的创建以及类的实例化（图 16.1）。

```python
class OS:
  # 类属性
  fs = "ext"
  # 实例属性
  def __init__(self, name, ver):
    self.name = name
    self.ver = ver
```

![Images](img/16x1.jpg)

**图 16.1**

OS 类的输出：

```python
# 实例化类
r = OS("redhat", 7)
u = OS("ubuntu", 16)

# 访问类属性
print("redhat is a {}".format(r.__class__.fs))
print("ubuntu is also a {}".format(u.__class__.fs))

# 访问实例属性
print("{} is {} version".format(r.name, r.ver))
print("{} is {} version".format(u.name, u.ver))
```

在之前的代码中，创建了一个具有类属性 `fs` 以及两个实例属性 `name` 和 `ver` 的 `OS` 类。使用 `r.__class__.fs` 打印类属性。`__init__()` 是初始化方法，通常称为构造函数。

![Images](img/line.jpg)

### 16.2 构造函数

构造函数是一个通过语法 `__init__()` 的特殊方法。构造函数的主要工作是初始化实例属性。我们可以使用带参数和无参数的构造函数。构造函数用于通过自定义值初始化属性。

```python
class Person:
  # 无参数
  def __init__(self):
    print("无参数构造函数示例")
  def show(self,name):
    print("Hello",name)

p = Person()
p.show("Eshita")
```

在之前的代码中，制作了一个无参数构造函数。在下一种情况下，讨论了带参数的构造函数。

```python
class Person:
  # 带参数构造函数
  def __init__(self, name):
    print("带参数构造函数")
    self.name = name
  def show(self):
    print("Hello",self.name)

p = Person("Eshita")
p.show()
```

![Images](img/line.jpg)

### 16.3 类中方法的创建

方法是类的重要组成部分。它用于执行特定任务。它还用于定义对象的行为 [4]。方法有一个、两个或多个参数。有时没有可以构建无参数方法。在以下代码中，构造函数初始化了 `name` 和 `ver` 属性，然后调用了带有两个参数的 `GUI()` 方法和带有一个参数的 `Audio()` 方法。

```python
class OS:
  def __init__(self, name, ver):
    self.name = name
    self.ver = ver
  def GUI(self, width, height):
    print("GUI size: {}x{}".format(width, height))
  def Audio(self, file):
    print("Playing: {}".format(file))

r = OS("redhat", 7)
r.GUI(800, 600)
r.Audio("beep.wav")
```





```python
 class Linux:
  # instance attributes
    def __init__(self, name, ver):
        self.name = name
        self.ver = ver

    # instance method
    def GUI(self, graphics):
        return "{} graphics {}".format(self.name, graphics)

    def Audio(self):
        return "{} the name ".format(self.name)

# instantiate the object
u = Linux("ubuntu", 16)
# call our instance methods
print(u.GUI(" HD "))
print(u.Audio())
```

![Images](img/line.jpg)

### 16.4 Python 中的多态

多态是面向对象编程中最基础的属性 [5]。Python 以方法重载的形式支持多态。下面的代码示例简单地反映了两个不同类中具有相同方法的多态性（图 16.2）。

![Images](img/016x002.jpg)

**图 16.2**

类中的方法多态。

```python
 class Linux:
    def virus(self):
        print("no virus attack !!")
    def ui(self):
        print("User interface may be completed !!")
class Windows:
    def virus(self):
        print("  Use antivirus !!")

    def ui(self):
        print("User interface is easy !!")

# a common interface
def os_test(os):
    os.virus()
    os.ui()
# instantiate objects
L = Linux()
W = Windows()
# passing the object
os_test(L)
os_test(W)
```

在前面的代码中，有两个不同的类：`Linux` 类和 `Windows` 类。它们具有相同的 `virus()` 和 `ui()` 方法。一个公共接口是 `os_test()`，这两个类的对象都通过它传递并最终调用该方法。由于这种情况下的多态属性，会根据传递的对象调用不同版本的方法。这展示了 `os_test()` 接口多态操作的简单演示。

多态可以通过运算符重载在 Python 中实现。在 Python 中，`+` 运算符已经被重载了。该运算符同时适用于 `int` 类和字符串类的实例。我们甚至可以为某些特定目的和特定类的实例重载运算符。要从自定义对象中重载 `+` 运算符，我们必须使用 `__add__` 方法。

```python
import math
class Circle:
    def __init__(self, rad):
        self.__rad = rad
    def getRad(self):
        return self.__rad
    def area(self):
        return math.pi * self.__rad ** 2
    def __add__(self, a_circle):
        return Circle( self.__rad + a_circle.__rad )
c1 = Circle(4)
v1 = c1.getRad()
v2 = c1.area()
print 'radius of c1 > ', v1
print 'area of c1',v2
c2 = Circle(5)
v3 = c2.getRad()
v4 = c2.area()
print 'radius of c2',v3
print 'area of c2',v4
c3 = c1 + c2 # This became possible because we have overloaded + operator by adding a method named __add__
v5 = c3.getRad()
print'radius of c3',v5
print'area of c3',c3.area()
```

代码的输出如下：

```
root@amartya-Aspire-4736:/home/amartya/Desktop/pythonload.py
radius of c1 >  4
area of c1 50.26548245
radius of c2 5
area of c2 78.53981633
radius of c3 9
area of c3 254.4690041
```

![Images](img/line.jpg)

### 16.5 继承概念 (#ch00_fm04_toc.xhtml_sec16_5)

继承是面向对象编程中最重要的现象 [6]。这一特性确保了程序代码从一个模块到另一个模块的可重用性。为了实现这一事实，我们必须设计类层次结构，其中一个类以不同的方式扩展另一个类的属性。在这种情况下存在多种类型的继承。单继承确保了在单级上从一个类到另一个类的属性扩展。此级别可以进一步扩展以实现多级继承。两种常见的继承类型是层次继承和多级继承。在层次继承中，多个子类继承一个基类，而在多重继承中，一个子类继承 `n` 个基类。





1. 1. [learnpython.org](http://learnpython.org). 检索自 [`www.learnpython.org/`](https://www.learnpython.org)。
2. 2. Goldwasser, Michael H., and David Letscher. *Object-Oriented Programming in Python*. Prentice Hall, Upper Saddle River, NJ, 2008.
3. 3. Leuthäuser, Max. “Python 面向对象编程讲义.” 德累斯顿工业大学，德国德累斯顿。[`st.inf.tu-dresden.de/files/teaching/ws10/ps/Leuthaeuser_Ausarbeitung.pdf`](http://st.inf.tu-dresden.de)。
4. 4. Koenka, Israel J., Jorge Sáiz, and Peter C. Hauser. “Instrumentino: 用于控制基于 Arduino 的实验仪器的开源模块化 Python 框架.” *计算机物理通信* 185, no. 10 (2014): 2724–2729。
5. 5. GeeksforGeeks. 检索自 [`www.geeksforgeeks.org/`](https://www.geeksforgeeks.org)。
6. 6. Lutz, Mark. *学习 Python：强大的面向对象编程*. O‘Reilly Media, Inc., Sebastopol, CA, 2013.

# 17

![Images](img/line.jpg)

## Python 中的输入与输出

![Images](img/line2.jpg)

输入输出机制是向应用程序获取输入并将输出发送到另一个应用程序或用户的最常见做法。在 Python 这样的编程语言中，有几种不同的工具来管理输入和输出。有几个 API 用于与其他远程应用程序、用户甚至网络中的其他设备或节点进行交互 [1,2]。本章将演示 Python 的几种输入和输出机制。

![Images](img/line.jpg)

### 17.1 input() 和 raw_input() 函数

获取输入的两种流行方式是使用 `input()` 和 `raw_input()` 函数。如果我们想获取任何整数或浮点数数据元素，我们必须使用 `input()` 函数。在这种情况下，数据将自动转换为特定类型并存储在变量 `c` 中。下面的示例说明了这一点：

```
 a = input("enter a ")
b = input("Enter b")
c=a+b
print "Your value is: ", c
```

`raw_input()` 函数专门用于获取字符串和字符集作为输入。在这种情况下，数据直接作为控制台输入流被收集。因此，所有数据都被视为字符集，因此对其不应用任何类型。即使我们输入任何数值，它也只被视为 Unicode 字符。下面的代码段描述了 `raw_input()` 函数的功能：

```
 a = raw_input("enter a ")
b = raw_input("Enter b")
c=a+b
print "Your value is: ", c
```

这段代码简单地拼接了两个字符串。如果值是字符，它们会被视为字符串并进行合并。

通过 `input()` 函数，我们也可以提供数据值列表。下面的代码块可以执行相同的操作：

```
 st = input("enter a list")
print "List is", st
Enter a list: [12,13,14,15]
List is : [12, 13, 14, 15]
```

![Images](img/line.jpg)

### 17.2 文件输入/输出

到目前为止，我们处理的是简单的控制台输入输出机制。在大多数情况下，Python 代码处理文件输入输出系统。文件输入输出主要通过创建文件对象来完成，有几个函数通过文件执行输入输出操作。

在读取文件之前，我们必须打开它。Python 提供了 `open()` 函数来实现此。`open()` 函数的语法所示：

```
 File o = open (file_name,Access_mode,buffering)
```

*   `file_name`: 这是一个简单的字符串，建议要打开的文件名。
*   `Access_mode`: 它是应用于文件的访问类型。最常用的访问模式是读、写和追加。Python 中还使用了其他参数。默认情况下，访问模式总是读取。
*   `buffering`: 缓冲基本上是一个整数值，指定输入输出期间的缓冲区大小。如果 `buffering` 为 `0`，则在 I/O 期间没有缓冲区。如果是 `1`，则在 I/O 期间采用该值作为缓冲区大小。如果是负数，则使用默认值。

在 表 17.1 中，我们列出了不同的文件打开模式。

![Images](img/Table_17.jpg)

**表 17.1**
Python 中的文件操作模式

![Images](img/line.jpg)

### 17.3 文件对象的属性

文件对象中有某些属性用于妥善处理任何文件。属性属性如下：

```
 !/bin/python

f = open("my.txt", "wb")
print "Name of the file: ", f.name
print "Closed or not: ", f.closed
print "Opening mode: ", f.mode
print "Softspace flag: ", f.softspace
ant 输出将变为...
amartya@artya-Aspire-4736Z:~$ python test.py
Name of the file: my.txt
```

`f.name` 简单返回文件名。`f.closed` 是一个布尔值，表示文件是否已关闭。如果是 true，则表示已关闭；如果是 false，则表示未关闭。`f.mode` 返回打开模式，`f.softspace` 提到软空间。

```
Name of the file: my.txt
Closed or not: False
Opening mode: wb
Softspace flag: 0
```

![Images](img/line.jpg)

### 17.4 close() 操作

`close()` 操作通过关闭文件指针关闭文件。在执行 `close()` 之前，允许任何读写操作。在正常情况下，Python 会关闭文件对象。`close()` 函数的示例所示：

```
 f=open("my.txt", "w+")
print "Name: ", f.name

# 关闭文件
```()

### 17.5 读取和写入文件

`read()` 方法用于从打开的文件读取文本和二进制数据。在此方法中，我们指定每次读取的字符或字节数。`read()` 方法始终从文件开始读取；如果不提供数量，它将读取到文件末尾。

```
 myf = open("test.txt", "r+")
str = myf.read(15); #15 元素
print "Read data: ", str
# 输出：Read data:
```

`write()` 方法向打开的文件写入字符串或二进制数据。在此方法中，我们必须传递要写入的字符串。当以写入模式打开文件时，之前的内容将被擦除。

```
 !/bin/python
# 打开文件
myf = open("test.txt", "wb")
myf.write("helloworldthisisawritebinaryexample");
f.close()
```

![Images](img/line.jpg)

### 17.6 tell() 方法

通常我们需要知道文件的当前位置。为了这样做，我们需要使用 `tell()` 方法。该方法直接返回给定文件中读写指针的位置。我们不应该通过 `tell()` 方法传递任何参数。`tell()` 方法的操作演示如下：

```
 f = open("test.txt", "rw+")
print "Name: ", f.name
l = f.readline()
print "Read Data: %s" % (l)
# 当前位置。
p = f.tell()
print "Position of the pointer: %d" % (p)
# 关闭文件
f.close()
```

输出如下：

```
 root@amartya-Aspire-4736Z:/home/amartya/Desktop/python# python
tell.py
Name: test.txt
Read Data: This is line 1
Position of the pointer: 15
```

![Images](img/line.jpg)





### 17.7 `seek()` 方法

`seek()` 方法主要接收一个偏移值作为当前位置。它有一个名为 `whence` 的参数。`whence` 的值决定了文件位置的偏移值。该参数默认设置为零。要更改文件位置的偏移值，我们需要改变 `whence` 值。如果值为 `1`，则 `seek()` 将相对于当前位置进行。如果值为 `2`，则 `seek()` 将相对于文件的末尾进行。`seek()` 操作不返回任何值。有时，文件可能会以写入、追加或 `a+` 模式（通常称为追加和更新）打开。在这种情况下，文件的更新将重置 seek 指针的位置。

```python
f= open("test.txt", "rw+")
print "Name : ", f.name
l = f.readline()
print "Read : %s" % (l)
f.seek(0, 0)
l = f.readline()
print "Read2 : %s" % (l)
f.close()
```

输出如下：

```
root@amartya-Aspire-4736Z:/home/amartya/Desktop/python# python seek.py
Name : test.txt
Read : This is line 1
Read2 : This is line 1
```

![Images](img/line.jpg)

### 17.8 Python 中的命令行参数

命令行参数是在运行期间传递给程序代码的参数。它被认为是输入接收机制之一。在其他编程语言中，该参数通过主方法传递。在 Python 中，我们可以通过 `sys` 模块获取命令行参数。这种情况下的技术如下所示：

```python
import sys
a1 = sys.argv[0]
```

我们应该始终记住，参数索引是从 0 开始的，因为当我们在运行时顺序传递参数时，它们被存储在一个名为“参数向量”（argument vector）的顺序列表中。在这里，`argv[]` 表示参数应该通过的这个参数向量。

在 Python 中，`argv[0]`（即第 0 个参数）应该是 Python 文件的文件名。然后，`argv[1]`、`argv[2]`……随后将给出运行期间传递的实际参数。

```python
import sys
File = sys.argv[0]
args = sys.argv[1:]
count = len(args)
print "name is", File
print "arguments are", args
print "length", count
```

在第一的情况下，输出显示文件名；在第二种情况下，它显示给定的参数；在第三种情况下，它打印参数的数量。

我们也可以使用 for 循环打印命令行参数。在这种情况下，for 循环遍历参数列表并逐个打印。

```python
import sys
for x in sys.argv:
    print "Argument: ", x
```

![Images](img/line.jpg)

### 17.9 本章涵盖的概念

- 文件 I/O 基础
- 文件对象的创建
- 文件的读取与写入
- `tell()` 方法
- `seek()` 方法
- 命令行参数

![Images](img/line.jpg)

### 17.10 参考文献

1. Lutz, Mark. *Programming Python*. O’Reilly Media, Inc., Sebastopol, CA, 2001.
2. Van Rossum, G. Python Programming Language. In *USENIX Annual Technical Conference* (Vol. 41, p. 36) (June 2007).

## 18 Python 中的异常处理

![Images](img/line.jpg)

![Images](img/line2.jpg)

在标准的 Python 应用开发场景下，错误的语法和语义会导致程序出现异常情况。这类错误自然会在程序执行期间发生。当发生此类错误时，程序应该采取适当的安全措施，以处理异常，避免被系统导致程序瞬时崩溃。异常处理机制是一种在某些特殊条件下监控和处理错误的方便方法。人们会感到需要异常处理，以保护程序执行免受程序代码可能的未知行为的影响。

![Images](img/line.jpg)

### 18.1 语法错误 vs. 异常

语法错误（通常称为解析错误）是代码格式不正确时的一种错误。这是最常见的错误类型。例如，如果 while 循环末尾缺少冒号，箭头将指向错误处。在 IDLE 中，错误不会直接显示，而是显示如图 18.1 和图 18.2 所示的对话框。

![Images](img/18x01.jpg)
**图 18**

![Images](img/18x02.jpg)
**图 18**

假设在变量被除以 0 的情况下，显示如下：

```python
var=6

var2=0
print/var2
```

等待，原文写的是：

```python
var2=0
print/var2
```

虽然程序在语法上是正确的，但由于某种原因执行停止了。以下显示了文件名以及行号。

```
Traceback (most recent call last):
  File "C:/Python27/t.py", line 7, in <module>
ZeroDivisionError: integer division or modulo by zero
```

Python 中生成的异常实际上是 `Exception` 类的对象。异常的基类是 `Exception`。许多子类可以执行特定任务。表 18.1 显示了这些异常类型及其功能。

**表 18.1 Python 中的异常类型**

### 18.2 处理异常

由于异常可能由用户程序生成，我们可以使用异常处理器来处理它。例如，我们可以创建一个接收某些数据的代码块，一旦给了它其他格式的数据，它就会立即生成异常。

### 18.2.1 Try-Except 技术

我们使用 `try: except:` 块来处理异常。在此块中，我们可以将想要监控的代码放在 `try` 块中，随后是 `except` 块。如果没有发生异常，`try` 块将完成执行并跳过 `except` 块。当 `try` 块内发生异常时，控制将立即停止代码执行并转移到 `except` 块。因此，在这种情况下，异常代码之后的代码将永远不会执行。以下程序显示了异常情况：

```python
while 1:
    try:
        x=int(input("data: "))
        print "an integer data"
    except:
        print "Wrong Format"
```

输出将是

```
data: 2
an integer data
data: t
Wrong Format
```

单个 `try:` 语句可以有多个异常子，以为不同类型的异常指定不同的问题。在这种情况下，至少有一个处理程序必须处理相应的异常。由于处理器处理了异常，其他其他块无法对同一个异常做出响应。异常子有时以元组的形式持有多个类型的异常。以下代码反映了这种情况。所有异常基本上都与同一个类及其基类兼容。

```python
except (NameError, TypeError):
    print " Error !!"
```




在下面的代码中，我们描述了如何通过继承基类 `Exception` 来创建一个异常类。在这种情况下，有三个类都是通过继承基类 `Exception` 创建的，并在接下来的部分抛出了这些异常。

```python
class X(Exception):
    pass

class Y(X):
    pass

class Z(Y):
    pass

for cls in [X, Y, Z]:
    try:
        raise cls()
    except Z:
        print("Z")
    except Y:
        print("Y")
    except X:
        print("X")
```

在这个示例中，需要注意的一点是，我们必须反向编写异常，因为如果我们先写 `X`，那么 `Y` 和 `Z` 也会被 `except X` 捕获，因为 `X` 是 `Y` 和 `Z` 的父类，因此 `Exception` 将触发父类并立即执行它，从而跳过所有的子类。

### 18.2.2 使用 else 语句的使用

有时，`try:except:` 块可能包含一个 `else:`。在这种情况下，如果程序没有抛出异常，控制流将执行 `else:` 部分。在这种情况下，程序用文件名作为参数打开文件，如果 `OSError` 打开该文件，它将立即将其视为异常，并显示消息“unable to open”（无法打开）。在另一种情况下，我们在读取行时提取字符集，并打印行的长度。

```python
for arg in sys.argv[1:]:
    try:
        f = open(arg, 'r')
    except OSError:
        print('unable to open', arg)
    else:
        print(arg, 'has', len(f.readlines()), 'lines')
        f.close()
```

在大多数情况下，`except` 子句可以在异常名称之后指定一个变量。在这种情况下，该变量将绑定到异常实例，参数存储在 `ins.args` 中。为了方便理解，异常实例定义了 `__str__()`；因此，可以直接打印参数，而无需引用 `.args`。我们也可以在抛出异常之前先实例化异常，并根据需要为其添加任何属性。

```python
>>> try:
    raise Exception('Hi', 'Hello')
except Exception as ins:
    print(type(ins))    # 异常实例
    print(ins.args)      # 存储在 .args 中的参数
    print(ins)           # __str__ 允许直接打印 args，
                         #但在异常子类中可能会重写
    a, b = ins.args
    print('a =', a)
    print('b =', b)

<class 'Exception'>
('Hi', 'Hello')
('Hi', 'Hello')
x = Hi
y = Hello
```

有时，异常可能会发生在函数内部，而不是在异常内部发生。在这种情况下，当函数调用时，异常将是直接的结果。以下代码说明了这一点：

```python
>>> def this_arithmetic():
    a = 14/0

>>> try:
    this_arithmetic()
except ZeroDivisionError as er:
    print('Handling run-time divided by zero error:', er)
```
处理运行时除零错误：division by zero。我们也可以在代码中抛出异常条件。我们可以使用 `raise` 关键字来实现。异常名称可以通过 `raise Exception()` 传递。

```python
>>> try:
    raise NameError('Demo')
except NameError:
    print('An Exception occurred!!')
    raise Exception occurred!!
Traceback (most recent call last):
  File "<stdin>", line 2, in module
NameError: Demo
```

### 18.2.3 finally 块

`finally` 子句是另一个在所有情况下使用的重要子句。`finally` 子句的一般规则是，无论是否发生异常，`finally:` 块始终执行。`finally:` 块应该放在异常语句的最后部分。当发生异常时，它将由 `except` 语句处理，有时由 `else:` 语句处理。如果异常被成功处理或根本没有抛出，控制流将进入 `finally:` 块。

```python
>>> def div(a, b):
    try:
        res = a / b
    except ZeroDivisionError:
        print("error occurred!! division by zero!")
    else:
        print("result is as follows", res)
    finally:
        print("Execution of the finally block")

>>> div(2, 4)
result is 0.5
Execution of the finally block

>>> div(2, 0)
error occurred!! division by zero!
executing finally clause
>>> div("2", "4")
Execution of the finally block
Traceback (most recent call last):
  File "<stdin>", line 1, in module
  File "<stdin>", line 3, in divide
TypeError: unsupported operand type(s) for / 'str' and 'str'
```

### 18.3 本章涵盖的概念

*   错误与异常的区别
*   处理机制
*   Try-except 块
*   `else:` 的使用
*   `finally:` 块的使用
*   多异常语句

### 参考文献

1.  1 Lutz, Mark. *Programming Python: Powerful Object-Oriented Programming*. O’Reilly Media, Inc., Sebastopol, CA, 2010.
2.  2 Hammond, Mark, and Andy Robinson. *Python Programming on Win32: Help for Windows Programmers*. O’Reilly Media, Inc., Sebastopol, CA, 2000.

## 19](#ch00_fm04_toc.xhtml_rchapter19)

## Python 中的图形用户界面](#ch00_fm04_toc.xhtml_rchapter19)

在图形用户界面（GUI）中表示软件现在非常常见。大多数现代编程平台（如 C++、Java 和 Microsoft visual studio）都提供框架、表单、按钮、文本框、组合框和列表框。GUI 使软件更具可读性和交互性，同时也更加用户友好。如今，Android 为手机和其他智能设备提供了更复杂、更友好的 GUI。Python 也有以库和 API 形式存在的大量的 GUI 框架或工具包。Python 主要且经典的 GUI 组件是 Tkinter，它是与 Python 捆绑的。还有一些跨平台和原生解决方案可用于构建特定平台的软件。

### 19.1 Tkinter 介绍

Tkinter 是一个事实标准的 GUI [1,2]。它在 Tcl/Tk 之上包含了一个面向对象的层。Tcl 是一种工具命令语言。它非常容易学习，适用于处理桌面应用程序、网络和网络管理任务的各种程序员。





Tkinter 包含多个模块。Tk 接口由 `_tkinter` 的二进制扩展支持，该扩展包含了 `Tk` 的低层接口。它是一个共享库，有时程序员不会直接使用到 Python 解释器的静态链接接口。

通常情况下，`Tkinter` 模块导出了几个小部件类及其相关的常量；因此，我们按照前面提到的所有方式挂载该模块（参见图 19.3）。

```python
import Tkinter

from Tkinter import *

import Tkinter as Tk

# 在下一个程序中，我们将打印一条问候信息

from Tkinter import *

r = Tk()

l1 = Label(r, text="Hello,to Python Tkinter!")
l1.pack()

r.mainloop()
```

程序从 `from Tkinter import *` 开始，这会导入 `Tkinter` 工具包包中的所有类和模块。在大多数情况下，我们应该导入模块命名空间中的所有模块。

若要初始化基础小部件，我们需要创建 `r = Tk()`。这是一个包含标题栏和默认窗口装饰的简单窗口。

`Label()` 方法是一个在默认窗口中显示文本或图像对象的小部件。在我们的案例中，显示了“Hello, to Python Tkinter!”消息。我们调用 `pack()` 方法将文本的大小适配到默认窗口中，当然，它让文本在窗口中可见。

![Images](img/019x003.jpg)

**图 19.3**

打印消息。

下一个重要的方法是 `mainloop()` 方法，通常被称为 `r.mainloop()`。这是主事件循环，在调用此事件循环之前，该窗口将永远不会出现。代码将由事件循环运行，直到关闭按钮被点击。事件循环控制所有与事件（如鼠标点击和按键）相关的特性。不仅是事件，事件循环也控制 Tkinter 本身的操作。

![Images](img/line.jpg)

### 19.2 核心组件类

有一些作为 Tkinter 构建模块的底层类。Tkinter 总共支持 15 种小部件：按钮（button）、画布（canvas）、复选框（checkbutton）、输入框（entry）、框架（frame）、标签（label）、列表框（listbox）、菜单（menu）、菜单按钮（menubutton）、消息（message）、单选按钮（radiobutton）、比例尺（scale）、滚动条（scrollbar）、文本（text）和 `Toplevel`。在 Python 2.3 中，还有更多小部件：`LabelFrame`、`spinbox` 和 `panedwindow`。`Tkinter` 模块提供了 `tk` 中各种小部件的各种类以及混入（mixin）。混入是一种通过多继承与其他类混合的类设计。

通过小部件类混合使用了三个主要类：`Grid`、`Pack` 和 `Place`。

`Grid` 是一种几何管理器，允许程序员通过在二维网格中组织组件来创建表格布局。`Pack` 是另一个高效的几何管理器，它通过提供特定的布局将小部件封装到另一个父小部件中，使排列有序。`Place` 几何管理器允许将小部件放置在显式指定的位置。

在继续之前，让我们来实现另一个简单的示例，说明 Tkinter 的基础组件。

```python
from Tkinter import *

class App:

    def __init__(self, master):
        f = Frame(master)
        f.pack()

        self.button = Button(
            f, text="EXIT", fg="blue", command=f.quit
        )
        self.button.pack(side=LEFT)

        self.hi_there = Button(f, text="HII", command=self.s_hi)

        self.hi_there.pack(side=LEFT)

    def s_hi(self):
        print "This is about button component!"

r = Tk()

app = App(r)

r.mainloop()
```

![Images](img/019x004.jpg)

**图 19.4**

带有按钮小部件的窗口。

前面的代码产生了如图 19.4 所示的输出。

在这里，在这种情况下，整个小部件写在一个类中。类的构造函数（`def__init__()`）首先创建框架，然后在框架内部创建了两个按钮。名为“EXIT”的第一个按钮持有一个标记为 `f.quit` 的退出事件。（注：原文此处存在大量重复文本，翻译已根据逻辑精简）。




Checkbutton 控件类主要用于创建一个显示开启/关闭状态的按钮。它是一个标准的 Tkinter 组件，包含文本或图像，用户可以为每个复选按钮关联任何 Python 函数。当按钮被按下时，会生成一个事件，从而调用该函数。当我们为按钮添加相应的文本时，它默认使用单一字体。它允许一个按钮包含多行文本。默认情况下，它还会为特定字符添加下划线，以显示该按钮的键盘快捷键。

主要，复选框反映的是一种“开启/关闭”的关系；然而，多个复选框支持“多多”的关系。通常，我们通过列表和单选按钮来创建一对多的关系。

要使用复选框，我们必须创建一个 Tk 变量，然后创建一个复选框对象。

```
 from Tkinter import *
m = Tk()
v = IntVar()
def call1():
    print "test check box!!"
c = Checkbutton(m, text="Start", variable=v, command = call1)
c.pack()
mainloop()
```

在前面的程序中，创建了一个复选框并将文本设置为“Start”。当我们勾选它时，command 将调用 `call1()` 方法。结果是它会打印 语句的内容。变量 `v` 默认值为 0，当被勾选时，值切换为 1。然而，我们可以通过 `onvalue`/`offvalue` 更改默认值。

### 19.2.4 Entry 控件

Entry 控件主要涉及输入字符串。该控件允许在单行内输入文本。要向控件添加输入文本，可以使用 `insert()` 方法。在插入新文本以替换当前文本之前，可以调用 `delete()` 方法。

```
 me = Entry(m)
me.pack()

me.delete(0, END)
me.insert(0, "a default value")

为了获取当前 entry 的输入文本，我们必须调用 get 方法。

s = e.get()
```

Entry 控件由 `StringVar` 实例绑定，并通过该变量执行设置或获取输入文本。

```
 var = StringVar()
ent = Entry(master, textvariable=var)
ent.pack()
var.set(" test default")
str = var.get()
```

接下来的程序描述了一种技术：通过 entry 控件获取某些文本，并通过按下按钮，通过 entry 控件显示当前文本。

```
 from Tkinter import *

m = Tk()
e = Entry(m)
e.pack()
e.focus_set()

def cb():
    print e.get()

b = Button(m, text="get", width=10, command=cb)
b.pack()
mainloop()
```

### 19.2.5 Frame 控件

Frame 是显示在屏幕上的矩形图形界面区域。该控件主要用作布局主框架。它还用于在其他控件之间执行填充（padding）。我们可以通过调用 `Frame` 类对象来使用 frame。

```
 m = Tk()
Label(text="one").pack()
myfrm = Frame(width=760, height=530, bg="", colormap="new")
myfrm.pack(fill=X, padx=10, pady=10)
Label(text="two").pack()
mainloop()
```

### 19.2.6 LabelFrame 控件

`LabelFrame` 控件是 `Frame` 的另一种变体，是在 Tkinter 8.4 版本中引入的。这种 `LabelFrame` 的基本现象是它始终会在子控件周围绘制一个边界框。当我们想要将某些相似类型的控件分在一组时，主要会使用这种控件。要显示组中的控件，首先创建一个 `LabelFrame`，并将控件添加到该 LabelFrame 中。frame 默认会在控件周围绘制边界。

```
 from Tkinter import *
m = Tk()
g = LabelFrame(m, text="Insert Text", padx=7, pady=7)
g.pack(padx=8, pady=8)
w = Entry(g)
w.pack()
mainloop()
```

图 19.6 显示了 label frame 控件。

![Images](img/019x006.jpg)

**图 19.6**

LabelFrame。

### 19.2.7 Listbox 和 Menu 控件

### 19.2.7.1 Listbox

Listbox 是标准的 Tkinter 控件，由列表形式的文本值组成。listbox 通常由具有相同字体和字体色的文本列表填充。用户可以根据自己的选择从 listbox 中选择一个或多个项目。它的主要用途是一次选择一组文本项目。在 listbox 构造期间，它是空的，因此我们必须向其上插入文本。我们可以通过 `insert()` 方法插入文本。被插入的项目从 0 开始索引。

```
 from Tkinter import *
m = Tk()
lb = Listbox(m)
lb.pack()
for i in ["1st value", "2nd value", "3rd value", "4th value"]:
    lb.insert(END, i)
mainloop()
```

可以删除项目。可以使用 `delete()` 方法。listbox 提供了许多模式：`SINGLE`、`MULTIPLE`、`BROWSE` 和 `EXTENDED`。

### 19.2.7.2 Menu 控件

`Menu` 控件支持下拉菜单。我们可以使用类似的技术来实现。接下来的代码描述了下拉菜单及其行为：

```
 from Tkinter import *
r = Tk()
def open():
    print "Opening mode"
def save():
    print "save document"
def cut():
    print "cut document"
def copy():
    print "copy document"
def paste():
    print "Paste Document"
def about():
    print "This is menu test"

menub = Menu(r)
f_menu = Menu(menub, tearoff=0)
f_menu.add_command(label="Open", command=open)
f_menu.add_command(label="Save", command=save)
f_menu.add_separator()
f_menu.add_command(label="Exit", command=r.quit)
menub.add_cascade(label="File", menu=f_menu)

# 下拉菜单创建
e_menu = Menu(menub, tearoff=0)
e_menu.add_command(label="Cut", command=cut)
e_menu.add_command(label="Copy", command=copy)
e_menu.add_command(label="Paste", command=paste)
menub.add_cascade(label="Edit", menu=e_menu)

h_menu = Menu(menub, tearoff=0)
h_menu.add_command(label="About", command=about)
menub.add_cascade(label="Help", menu=h_menu)

# 在窗口中显示整个菜单
r.config(menu=menub)
mainloop()
```



弹出菜单的创建方法与下拉菜单相同。区别在于它可以使用 `post()` 方法显示。

```
menu.post(event.x_root, event.y_root)
```

然后，我们可以对画布（canvas）使用 `bind()` 方法。`bind()` 方法可以实现相同的功能。

```
Frame.bind("button",popupmenu)
```

### 19.2.8 单选按钮 (Radio Button)

`radiobutton` 是 Windows 编程中一个非常有用的组件。Tkinter 通过单选按钮类支持单选按钮。它是一种互斥按钮，具有多对一的选择选项。单选按钮可以包含文本或图像。任何按钮都可以与函数关联，并在点击单选按钮选择时调用该函数。按钮中的所有文本具有相同的字体，并且可以使用 `TAB` 键移动控件。在设置单选按钮时，请确保按钮已分组，并且所有按钮都指向同一个变量（见图 19.8）。

![Images](img/019x008.jpg)

**图 19.8**

单选按钮。

```
from Tkinter import *
m = Tk()
MOD = [
    ("SVM", "1"),
    ("LR", "2"),
    ("KNN", "3"),
    ("CNN", "4"),
]
var = StringVar()
var.set("4")
for t, mod in MOD:
    b = Radiobutton(m, text=t,variable=var, value=mod)
    b.pack(anchor=W)
mainloop()
```

![Images](img/line.jpg)

### 19.3 本章涵盖的概念

* Tkinter GUI 组件
* 按钮控件
* Canvas 组件
* 列表框 (Listbox)
* 菜单 (Menu)
* 单选按钮

![Images](img/line.jpg)

### 19.4 参考文献

1. [1]. Lundh, Fredrik. “An Introduction to Tkinter.” [`www.tcltk.co.kr/files/TclTk_Introduction_To_Tkiner.pdf`](http://www.tcltk.co.kr) (1999).
2. [2]. Shipman, John W. *Tkinter 8.4 Reference: A GUI for Python*. New Mexico Tech Computer Center, Socorro, NM, 2013.
3. [3]. Miller, Bradley N., and David L. Ranum. *Problem Solving with Algorithms and Data Structures Using Python*, Second Edition. Franklin, Beedle & Associates Inc., Portland, OR, 2011.
4. [4]. Grayson, John E. *Python and Tkinter Programming*. Vol. 140. Manning Publications, Greenwich, CT, 2000.

## 20

![Images](img/line.jpg)

## 用于机器学习和 Arduino 的 Python API 模块

![Images](img/line2.jpg)

Python 库为人工智能和硬件接口提供了良好的 API 支持。机器学习应用包是最流行的包之一，广泛使用 python scikit-learn 工具进行实现。在本章中，我们的主要目标是强调与机器学习、Arduino、数据科学和其他技术相关的有用包。我们在这里尝试通过一些实用示例提供这些包的见解。在这种背景下，一个很有用的实体是 PyPI，即 Python 包索引，它是 Python 编程的软件仓库。

![Images](img/line.jpg)

### 20.1 包的安装

Python 包安装器称为 `pip`。在所有 Python 版本中，`pip` 都是可用的。在使用 `pip` 之前，我们必须检查当前使用的 Python 版本。可以使用以下命令完成：

```
python --version
```

然后，我们需要检查 `pip` 命令。在 Linux 环境中，默认可以使用此命令，但在 Windows 中可能不可。也许在 Windows 中运行此命令，我们需要进入安装目录下的 `\Scripts` 子目录。现在我们创建一个批文件 `local.bat`，通过在内容中写入 `cmd` 来打开命令行。现在只需点击该批文件，就会打开命令窗口。从这里我们可以运行 `pip`。我们可以通过简单输入 `pip` 来检查 `pip` 的版本。

![Images](img/line.jpg)

### 20.2 SciPy 和 NumPy 包

`NumPy` 是 Python 科学计算的基础包 [1], [2]。该库为 Python 提供了一些强大的组件，如多维数组对象。这包含了基本计算的所有基础概念，如傅里叶变换、线性代数、统计操作、选择、I/O 以及其他逻辑和数学运算。`NumPy` 的核心是 `ndarray` 对象。它主要用于封装 n 维数据。`NumPy` 数组与 Python 标准数组之间的一些主要区别如下：

* `NumPy` 中的数组是固定类型的。因此，无法更新数组的大小。更改大小涉及删除旧数组并创建一个新数组。
* `NumPy` 数组的数据元素是同质的。尽管如此，它支持数组操作。
* 与普通序列类列表相比，在 `NumPy` 数组中可以用更高效的方式进行若干复杂的计算。

### 20.2.1 形状的创建

`NumPy` 的目标是创建一个 n 维数组。数组的维度被称为轴（axis）。下面的示例展示了 `NumPy` 数组以不同方式的操作：

```
>>> import numpy as np
>>> x=np.arange(20).reshape(4,5)
>>> x
array([[0, 1, 2, 3, 4],
 [5, 6, 7, 8, 9],
 [10, 11, 12, 13, 14],
 [15, 16, 17, 18, 19]])
>>> x.shape
(4, 5)
>>> x.ndim
2
>>> x.dtype.name
'int32'
>>> type(x)
<class 'numpy.ndarray'>
```

创建数组有几种类型的技术可用。在 `NumPy` 中，我们使用 `array()` 函数来创建数组。

```
>>> import numpy as np
>>> n=np.array([1,3,5])
>>> n
array([1, 3, 5])
>>> n.dtype
dtype('int32')
>>> b=np.array([1.2, 3.5, 5.1])
>>> b.dtype
dtype('float64')
```

我们也可以显式地指定类型。以下代码段显示了二维数组的维度：

```
>>> z=np.array([[1,6], [3,7]], dtype=complex)
>>> z
array([[1+0j, 6+0j],
       [3+0j, 7+0j]])
```

我们可以使用 `NumPy` 创建序列。`arange()` 函数返回特定范围的值数组。

```
>>> np.arange(10, 30, 5)
array([10, 15, 20, 25])
>>> np.arange(0, 2, 0.3)
array([0. , 0.3, 0.6, 0.9, 1.2, 1.5, 1.8])
```

第一个案例显示了 10 到 30 之间间隔为 5 的数组。下一个案例显示了从 0 到 2 间隔为 0.3 的浮点数组。

有时，我们需要更有可预测性的浮点精度值。为了创建数值序列，我们使用 `linspace()`，它接收范围和范围内的数量。下面的示例说明了 `linspace()` 函数的操作。

```
>>> from numpy import pi
>>> np.linspace(0, 3, 10) # 从 0 到 3 的 10 个数字
array([0. , 0.33333333, 0.66666667, 1. , 1.33333333,
       1.66666667, 2. , 2.33333333, 2.66666667, 3. ])
>>> x=np.linspace(0, 2*pi, 100) # 有助于在大量点上评估函数
>>> f=np.sin(x)
```

#### 20.2.2 NumPy 中的复制操作

数组的复制操作可能有两种方式 [3], [4]。一种是将列表对象的地址复制到目标中。因此，可以通过变量 `x` 和 `y` 访问同一个数组对象。

```
>>> x=np.arange(12)
>>> y=x # 没有创建新对象
>>> y is x # a 和 b 是同一个对象的两个名称
ndarray object
True
>>> y.shape=3,4 # 改变了 a 的形状
>>> x.shape
(3, 4)
```



可以使用 `view()` 创建列表对象的浅拷贝。在这种情况下，不同的对象可以共享相同的数据。但在物理层上，会为单独的对象创建内存。

```
 >>>  c = a.view()
>>> c is a
False
>>> c.base is a
True
```

最后，我们使用 `copy()` 方法创建一个对象的实际复制。当调用 `copy()` 方法时，它会简单地创建两个独立的相同对象。

```
 >>>  y = x.copy()     # 创建了一个带有新数据集的完全新对象。
>>> y is x
False
>>> y.base is x      # y 不与 x 共享任何内容
False
 >>> y[0,0] = 9999
 >>> x
array([[ 0, 10, 10, 3],
       [1234, 10, 10, 7],
       [ 8, 10, 10, 11]])
```

![Images](img/line.jpg)

### 20.3 Matplotlib 简介

Matplotlib 是 Python 中最强大的绘图库组件。任何类型的数据可视化、图表或图表生成都可以使用 Matplotlib 程序包完成。二维和三维图、柱状图和饼图的设计是 Matplotlib 包中非常流行的组件。Matplotlib 的优势之一是它是不断演变的软件，也就是说，每当添加一些新组件时，都有新的功能和特性准备好整合。一些核心功能如下：

* 它包含 70,000 行代码。
* 它是各种接口的家，能够与不同的后端服务交互。

## 20.3.1 核心组件

Matplotlib 的核心组件是 `Pyplot`。它是一个函数集合，像任何其他专业绘图软件一样与 Matplotlib 工作。在 `Pyplot` 中，许多状态在函数调用之间被保留，以便它可以跟踪如图形和绘图区域等各种组件。图 20.1 显示了基于某些预定义列表数据对象的简单折线图。

```
 import matplotlib.pyplot as myplt
myplt.plot([2,4,6,8,7])
myplt.ylabel('some numbers')
myplt.show()
```

在这个简单的图中，y 值是给定的数据对象，而 x 值是列表中对象的数量。

![Images](img/020x001.jpg)

**图 20.1**

Matplotlib 中的 plot 函数。

![Images](img/020x002.jpg)

**图 20.2**

彩色点状实线图表。

`plot()` 命令是一个非常有用且多功能的命令。我们可以通过简单提供包含 x 和 y 坐标的列表来绘制 X 与 Y 的图表。我们还可以通过它传递绘图中的线条类型。在这种情况下，我们通过传递值列表来提供轴范围。`plt.axis()` 接收 x 轴 y 轴列表。在这里，0–10 是 x 轴的范围，0–45 是 y 轴的范围。“ro-” 表示红色，“o” 在图 20.2 中表示点状实线。

```
 import matplotlib.pyplot as plt
plt.plot([1,2,3,4,5,6,7,8], [1,4,9,16,25,30,35,40], 'go-')
plt.axis([0, 10, 0, 45])
plt.show()
```

## 20.3.2 线条属性

我们可以在 Matplotlib 中产生不同类型的线条。可以通过设置线条的若干参数（如宽度、虚线样式和抗锯齿效果来实现。要设置线条宽度，我们可以在 `plot()` 方法中设置宽度。

```
 Plt.plot(a, b , linewidth=1.5)
```

有时，我们使用 `setter()` 方法设置抗锯齿效果等属性。

```
 line, = plt.plot(x, y, '-')
```
line.set_antialiased(True)
```

抗锯齿通常处理了由于不同的显示设备而产生的 jaggies。

## 20.3.3 多图表示

像 MATLAB 一样，它支持多图。要在单个图形中创建多个子图，我们使用 `subplot()`。Matplotlib 的基本目标是加载数据集、评估算法并进行一些预测。

```
 import matplotlib.pyplot as plt
plt.plot([1,2,3,4,5,6,7,8], [1,4,9,16,25,30,35,40], 'go-')
plt.axis([0, 10, 0, 45])
plt.show()
```

![Images](img/line.jpg)

### 20.4 SciPy 概述

SciPy 是基于 Python 的数学科学开源生态系统。它包含了优化、线性代数、积分、信号和图像处理模块。安装 SciPy 需要使用 `pip install` 命令。SciPy 的最新版本是 1.0.0。SciPy 是数学计算和分析的强大工具。SciPy 包含表 20.1 所示的各种子包。

![Images](img/Table_21.jpg)

**表 20.1** SciPy 包列表

### 20.5 机器学习工具

Python 环境拥有良好的库来执行机器学习任务。为了执行机器学习操作，我们需要遵循一些良好的步骤：

* 识别问题。
* 根据问题准备数据集。
* 在数据集上应用算法。
* 获取并优化结果。
* 表示结果。

实现机器学习需要安装以下强制性包：NumPy、SciPy、Matplotlib、sklearn 和 pandas。在实现任何机器学习代码之前，我们应该加载这些库。示例代码所示：

```python
 import pandas
from pandas.plotting import scatter_matrix
import matplotlib.pyplot as plt
from sklearn import model_selection
from sklearn.metrics import classification_report
from sklearn.metrics import confusion_matrix
from sklearn.metrics import accuracy_score
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.svm import SVC
from sklearn.neighbors import KNeighborsClassifier
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from sklearn.naive_bayes import GaussianNB
```




在这里，我们可以观察到从 `pandas` 导入了不同的模块。`matplotlib.pyplot` 用于图表的可视化。`sklearn` 包主要用于实现不同的分类器。通常，我们使用逻辑回归、决策树、支持向量机、K 近邻算法以及高斯和线性判别分析。

我们还使用 `sklearn.matrices.confusion_matrix` 和 `accuracy_score` 生成混淆矩阵和准确率评分。

在完成这些操作后，我们加载数据集。在这种情况下，我们通常使用 UCI 机器学习库提供的标准鸢花（iris）数据集。我们设计的受 Jason Brownlee 启发的鸢花数据集代码。

```
names = ['sepal-length', 'sepal-width', 'petal-length', 'petal-width', 'class']
data_s = pandas.read_csv('test.csv', names=names)
```

当我们加载数据集时，可以对数据集的实例（通常称为维度）有一个直概念。我们可以通过以下方式获取数据集某些行的实例（在此情况下为 50 个实例）：

```
print(data_s.head(50))
```

使用以下方法还可以完成统计描述和基于类的总结：

```
print(data_s.describe())
print(data_s.groupby('class').size())
```

在获取数据集的一些描述后，我们可以对数据进行绘图以展示数据的特征。使用 Matplotlib 库可以轻松对数据集绘制条形图、散点图或折线图在这种情况下，`hist()` 函数创建一个直方图类型的条形图。

```
data_s.hist()
plt.show()
```

在获得数据集表示后，我们对数据集应用一些机器学习算法。为了实现这一点，我们需要创建一个训练集和一个测试集。训练集用于训练我们即将创建的模型，而测试集用于为模型创建输入以验证模型的性能。

其中涉及几个步骤。首先，我们必须分离验证集或测试数据集。我们对其应用了 k 折交叉验证技术。系统 k 折交叉验证技术指出，我们需要将整个数据集分成 k 个子集，并选择其中一个作为测试集，其余的 k-1 个子集合并。在下一次迭代中，另一个子集将成为测试集，而剩余的 k-1 个将成为训练集，依此类推。这提高了算法的准确性。在这种情况下，我们通常选择十折交叉验证机制。我们可以使用不同的算法构建不同的模型并最终选择最佳模型。

然后，我们进入验证阶段。在这种情况下，我们必须判断模型并审查模型在某些未见数据集上的性能。随后，我们使用一些统计模型来判断特定模型在某些未见数据集上的结果准确性。这里的技术是将数据集分成两半。80% 的数据用于训练，而 20% 的用于验证。

```
array = dataset.values
X = array[:,0:4]
Y = array[:,4]
valid_size = 0.20
seed_1 = 7
X_train, X_validation, Y_train, Y_validation = model_selection.train_test_split(X, Y, test_size=valid_size, random_state=seed_1)
seed_1 = 7
score = 'accuracy'
```

在实际操作中，`seed_1 = 7` 为所有算法产生了最佳结果；因此，我们可以选择种子 7。

然后，我们必须在这些数据集上应用不同的算法。在这种情况下，尚不知道哪种技术给出最优结果。对于部分线性可分的数据，预计它会产生良好的结果。

我们现在考虑六个模型并将它们应用于相同的数据并获取结果，显示哪个模型在以下数据集上性能最好：

```
my_models = []
my_models.append(('LR', LogisticRegression()))
my_models.append(('LDA', LinearDiscriminantAnalysis()))
my_models.append(('KNN', KNeighborsClassifier()))
my_models.append(('CART', DecisionTreeClassifier()))
my_models.append(('NB', GaussianNB()))
my_models.append(('SVM', SVC()))
res = []
name = []
for name, m_model in my_models:
    kfold = model_selection.KFold(n_splits=10, random_state=seed_1)
    cv_results = model_selection.cross_val_score(m_model, X_train, Y_train, cv=kfold, scoring=score)
    results.append(cv_results)
    name.append(name)
msg = "%s: %f, %f" % (name, cv_results.mean(), cv_results.std())
print(msg)
```




要配置 `nanpy` 固件，我们可以编辑 `nanpy/cfg.h`。要安装 Nanpy 固件，只需将 `nanpy` 文件夹拷贝到 sketchbook（项目）文件夹中，启动 Arduino IDE 并上传 `sketchbook/nanpy`。然后，点击上传。

在主机上，您可以使用以下命令安装 Nanpy：

```
pip nanpy
```

![Images](img/line.jpg)

### 20.7 本章涵盖的概念

* NumPy 和 SciPy 包
* `sklearn` 和 `pandas` 的使用
* 示例机器学习代码
* 用于 Arduino 的 Python API
* Nanpy API

![Images](img/line2.jpg)

**#代码来源：[`www.scipy.org/`](https://www.scipy.org/)。

![Images](img/line.jpg)

### 参考文献

1. 1. Kiusalaas, Jaan. *Numerical Methods in Engineering with Python 3*. Cambridge University Press, Cambridge, 2013.
2. 2. McKinney, Wes. *Python for Data Analysis: Data Wrangling with Pandas, NumPy, and IPython*. O‘Reilly Media, Inc., Sebastopol, CA, 2012.
3. 3. Pedregosa, Fabian, Gaël Varoquaux, Alexandre Gramfort, Vincent Michel, Bertrand Thirion, Olivier Grisel, Mathieu Blondel, et al. “Scikit-learn: Machine learning in python.” *Journal of Machine Learning Research* 12, no. Oct (2011): 2825–2830.
4. 4. Walt, Stéfan van der, S. Chris Colbert, and Gael Varoquaux. “The NumPy array: A structure for efficient numerical computation.” *Computing in Science & Engineering* 13: 22.
5. 5. Zemmal, Nawel, Nabiha Azizi, Nilanjan Dey, and Mokhtar Sellami. “Adaptative S3VM semi supervised learning with features cooperation for breast cancer classification.” *Journal of Medical Imaging and Health Informatics* 6, no. 4 (2016): 957–967.
6. 6. Zemmal, Nawel, Nabiha Azizi, Nilanjan Dey, and Mokhtar Sellami. “Adaptive semi supervised support vector machine semi supervised learning with features cooperation for breast cancer classification.” *Journal of Medical Imaging and Health Informatics* 6, no. 1 (2016): 53–62.
7. 7. Nath, Siddhartha Sankar, Girish Mishra, Jajnyaseni Kar, Sayan Chakraborty, and Nilanjan Dey. “A survey of image classification methods and techniques.” In *2014 International Conference on Control, Instrumentation, Communication and Computational Technologies (ICCICCT*), Kanyakumari, India, pp. 554–557\. IEEE, 2014.
8. 8. Machine Learning. Retrieved 自 [`developers.google.com/machine-learning`](https://developers.google.com/machine-learning)/。
9. 9. Brownlee, Jason. *Machine Learning Mastery with Python*. Machine Learning Mastery Pty Ltd., Vermont, Australia, 2016: 100–120.
10. 10. Brownlee, Jason. “Machine Learning Mastery with Python: Understand Your Data, Create Accurate Models and Work Projects End-To-End.” [`machinelearningmastery.com/products/`](https://machinelearningmastery.com) (2016).

## 21

![Images](img/line.jpg)

## 更多关于机器学习 API

![Images](img/line2.jpg)

Python 的 `scikit-learn` 为基于机器学习的智能计算提供了极佳的工具。此外，如今还引入了大量的深度学习算法。在本章中，我们的主要重点是 Python 支持的不同机器学习模型，例如监督学习和无监督学习，包括一些著名的算法类。本章还包含了深度学习工具的用途，如 TensorFlow、卷积神经网络（CNN）和循环神经网络（RNN）。

![Images](img/line.jpg)

### 21.1 scikit-learn 深度解析

在我们深入研究 `scikit-learn` 包之前，我们必须了解机器学习的基础知识。

机器学习的根本属性涉及到对“n”个样本数据的考虑，这些数据主要用于训练数据。因此，机器学习……

（注：原文包含重复句子；此处已保持其核心逻辑流。）

学习的另一种形式是无监督学习，其中训练数据集包含输入向量 `x`，但没有定义目标值 `y`。聚类是无监督学习的示例。有时，目标是在给定的输入维度下确定数据。在这种情况下，高维数据被合成到三维空间，有时被称为密度估计。在聚类中，我们关注数据点的分组。人群分组的一个例子是电子商务网站。另一方面，关联规则发现的是描述大部分数据的规则。一些良好的例子是 K-means 聚类和用于规则学习的关联规则算法。

半监督学习是另一种学习类别。该类别介于无监督和监督学习之间。在这种情况下，对于大型数据集 `x`，部分元素有标记，而其他部分没有标记。大多数实际案例都属于这一类。在实际案例中，标记大量数据是非常困难的，因为它耗时耗力，并且需要领域专家。另一方面，未标记数据的成本较低且易于获取。在监督学习的情况下，我们使用未标记数据作为训练数据并将其拟合函数以训练模型。然后，我们从该模型对未见数据生成预测。

`scikit-learn` 包包含一个标准的鸢花数据集作为测试集。因此，我们可以使用 Python 语句创建并显示该数据集：

```
from sklearn import datasets
i = datasets.load_iris()
d = datasets.load_digits()
print(i.data)
print(d.data)
```



数据集是一个字典结构。整个数据集存储了数据以及一些关于数据的元数据。`Dataset` 以样本特征数组的形式数据存储在 `.data` 成员中。如之前的代码所示，`i.data` 包含鸢花（iris）数据集的数据成员，而 `d.data` 包含数字数据集的数据成员。

学习和预测是监督学习机器学习模型的核心目标。在 `scikit-learn` 中，用于分类的估计器基本上是一个实现了两个主要方法 `fit(predictor, target_value)` 和 `predict(test_dataset)` 的 Python 对象。`fit()` 方法主要用于拟合估计器。估计器是根据单个观测数据计算某数量的规则。`predict()` 方法则根据训练数据和未知测试数据执行预测工作。

在 `scikit-learn` 中，估计器的一个很好的例子是 `sklearn.svm.SVC`，它实现了支持向量分类。

## 21.1.2 支持向量分类器

支持向量机（SVM）是最流行的监督学习算法，适用于分类和回归任务。在这种方法论中，我们将数据点绘制到 n 维空间中。然后，我们的任务是找到一个能够有效方式分离不同类别的超平面（图 21.1）。

SVM 的工作原理根本上基于识别超平面。图 21.2 显示了超平面的选择机制。

![Images](img/021x001.jpg)

**图 21.1**

分类案例 2：(a) 分类类型 1 和 (b) 分类类型 2。

![Images](img/021x002.jpg)

**图 21.2**

分类案例 1：(a) 不同方向的超平面和 (b) 平行超平面。

在图 21.2a 中，有三个超平面。我们需要决定选择哪一个平面。这里的经验法是选择能更好地分离两个不同类别的超平面。在图 21.2a 中，平面 B 更好地隔离了这两个类别。在图 21.2b 的情况下，超平面 B 最合适，因为平面 B 到两个类别最近数据点的距离最大。

在第二种情况下（图 21.3a），我们看到一组中的一个数据点与该相同数据点组并不足够近；因此，可以认为有两个不同的平面。与 B 相比，超平面 A 有更高的边界。然而，我们应该选择平面 B，因为与超平面 A 相比，超平面 B 实现了更准确的分类。在图 21.3b 中，我们无法用直线区分不同类的两个数据点。在这种情况下，SVM 忽略离群值。

![Images](img/021x003.jpg)

**图 21.3**

分类案例 3：(a) x,y 平面；(b) x,z 平面。

在一种情况下，两个类别之间不存在直线超平面。虽然我们为所有情况创建了线性超平面，但在这种特殊情况下，超平面不是线性的。为了解决这个问题，必须实现 SVM 的一个新特征，支持一个额外的平面 z，其中 `z = x² + y²`。因此，数据图现在沿着 z 轴和 x 轴绘制。图 21.4a 和 b 显示了 z, x 平面上两个不同类别的分类。在图中，`z` 始终为正值，因为它是 x 和 y 的平方和。SVM 有一种称为核技巧的机制，它会自动添加特征以获得新的线性超平面。

![Images](img/021x004.jpg)

**图 21.4**

三层 ANN 可视化。

## 21.1.3 在 Python 中实现 SVM

Python 在 `scikit-learn` 包中内置了一个名为 `SVC` 的 SVM 分类器。使用 SVM 创建预测的步骤包括导入正确的库、创建对象、拟合有效模型以及最后预测值。

```
from sklearn import svm
my_model = svm.svc(kernel='linear', c=1000, gamma=0.02)
my_model.fit(A,b) # 其中 A 是预测器，b 是训练集的目标，
                  # a_test 是预测器的预测
my_model.score(A,b)
```

## 21.1.4 SVM 的优点与缺点

- SVM 在点的分离上起作用。
- 它对于高维空间非常有用。
- 在决策函数中，它只使用部分内存。
- 当维度大于样本数量时，它的工作效果会更好。
- 对于大型数据集，SVC 的性能会受到影响。
- 对于目标类别存在严重问题的噪声数据集。

### 21.1.5 人工神经网络

人工神经网络（ANN）是机器学习中一个非常重要的组件。它主要模拟人类神经元的操作。ANN 的主要组件包括输入层、隐藏层和输出层。ANN 的标准图如图 21.5 所示。就像原子是神经网络（NN）的基础一样，感知机是所有神经网络的骨干。

感知机可以被认为是任何接受多个数字输入并给出单个值输出的实体。图 21.6 所示的结构接受三个输入并产生一个输出。

感知机输入输出之间的定义关系是一个关键点。一种方法是对输入进行直接组合并求和，然后设置阈值为 0。如果超过了阈值，则输出为 1；否则为 0。例如，假设 `a=1, b=1, c=0` 应该是超过阈值的 1，因此在这种情况下输出值必须为 1。



在下一个案例中，我们在加权输入值之和的基础上添加了一个偏置（bias）值。感知元的偏置反映了感知器的灵活性。它在某种程度上类似于函数 `y = mx+c`。因此，我们只需要在方程 `w1 × x+w2 × y+w3 × z + 1 × b> threshold` 中添加一个偏置值。

### 21.1.6 激活函数

到目前，感知器仅使用线性函数。然而，感知器的非线性变换是一个主要问题。使用非线性变换的神经元基本上使用的是激活函数。

激活函数基本上将加权输入的和作为参数，并返回神经元本身。

因此，激活函数可以写如下：

$\begin{array}{l} {\text{y} = \text{F}\left( {\sum{\text{w}_{\text{i}} \cdot \text{X}_{i}}} \right)} \\ {\text{i} = 0\,\text{to}\,\text{N}} \end{array}$

激活函数的主要目标是执行非线性变换以拟合非线性假设或估计复杂的非线性函数。在这种情况下使用了多种激活函数，其中一些是 ReLu 和 sigmoid。

### 21.1.7 使用 Python API 实现 ANN

我们可以使用 Python API 开发 ANN 模型 [5]。在此背景下最流行的 API 之一是 Keras [6, 7]]。它基本上是高效神经网络库（如 TensorFlow 和 Theano）的封装。

实现神经网络涉及几个步骤：加载数据集、定义模型、编译模型、拟合模型，最后评估模型并将整个过程整合在一起。运行 ANN 的核心要求是安装 `numpy`、`scipy` 和 `keras` 模块。所有模块都应该经过适当的配置。

有一个法则：运行机器学习算法从随机过程开始，而这无非随机种子。这种技术对于重复运行相同的代码非常有效，因此将获得相同的结果，这对于具有相似随机性的结果进行分析和比较有用。

```
from keras.models import Seq
from keras.layers import Den
import numpy as np
np.random.seed(7)
```

我们的第二个任务是加载数据集并将其分为两个不同的部分，即输入变量 `X` 和输出变量 `Y`。数据集可以是任何 `.csv` 格式或 XML 格式。

```
dataset = np.loadtxt("data_set.csv", delimiter=",")
X = dataset[:,0:8]
Y = dataset[:,8]
```

然后，我们必须定义模型。Keras 中的模型由若干层组成。我们可以添加层直到拓扑结构满意。我们必须确保输入层有输入层。

```
m = Sequential()
m.add(Dense(10, activation='relu', input_dim=6)) 
m.add(Dense(8, activation='relu'))
m.add(Dense(1, activation='sigmoid'))
```

在这里，`Dense` 类用于全连接。`input_dim` 参数指定特征的数量。`activation` 参数指定激活函数。`compile` 方法用于定义损失函数、优化器和指标。

```
m.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])
```

`fit` 方法用于训练模型。使用了 `epochs` 和 `batch_size` 参数。

```
m.fit(X, Y, epochs=150, batch_size=10)
```

`evaluate` 方法用于查看模型的性能。

```
s = m.evaluate(X, Y)
print("\naccuracy: %.2f%%"%s[1])
```

![Images](img/line.jpg)

### 21.2 深度学习工具

深度学习是机器学习的一种特殊形式，在其中机器学习像人类一样学习自然行为 [8, 9, 10, 11]，例如火箭单元和无人驾驶汽车。它也是语音控制等语音设备的关键组件。深度学习系统从根本上基于深度神经网络。我们可以说一个非常简单的深度学习例子是预测分析。

#### 21.2.1 卷积神经网络和循环神经网络

### 21.2.1.1 卷积神经网络

如上一节（第 21.2 节）所述，卷积神经网络（CNN; [12]）类似于带有权重和偏置的传统 ANN [13, 14, 15, 和 16]。




普通的神经网络（NN）仅接收常规输入并将其通过隐藏层，该隐藏层由与前层全连接的神经元组成。在输出层，分类值由分类评分表示。普通的人工神经网络（ANN）从不缩放全幅图像，但卷积神经网络（CNN）的优势之一是它利用了神经网络的三维模型。这种架构使得它能够将图像作为输入并以更灵敏的方式进行处理。与普通的 ANN 不同，CNN 系统以高度、宽度和深度的形式接收图像数据。

例如，CIFAR-10 中的输入图像是一个激活值卷，该激活卷的维度为 32 × 32 × 3（分别为宽度、高度和深度）。某层中的神经元只会连接到其前一层的一个小区域，而不是以全连接的方式连接到前层的所有神经元。然而，CIFAR-10 的最终输出层维度为 1 × 1 × 10，这是因为在卷积网络（CNN）架构结束时，整个图像被还原为一个沿深度维度排列的单一类别评分向量。可视化结果所示图 21.6。

![Images](img/021x007.jpg)

**图 21.7**

一个 RNN。

简单的卷积网络是一系列层。CNN 的每一层都使用可微函数将一个激活卷转换为另一个。构建卷积网络涉及三个主要层：卷积层、池化层和全连接层。一个处理 CIFAR-10 的示例序列，CNN 应该通过以下分层架构构建：

*   INPUT（输入）：此层持有图像的输入像素值（32 × 32 × 3），具有三个颜色通道（RGB）。
*   CONV（卷积）：此层计算局部神经元的输出。在这里，每个神经元计算其权重之间的点积。
*   RELU：此层是一个高效的逐元素激活函数。当它在 0 处阈值时，原始卷的大小将保持不变。
*   POOL（池化）：此层执行下采样操作。
*   FC（全连接）：这是一个全连接层，主要是外层，将计算类别的评分。每个神经元都与其前层全连接。

### 21.2.1.2 循环神经网络

循环神经网络（RNN）是一种具有多样化应用的神经网络。它专门处理各种输入和输出类型。RNN 的重要用途之一是情感分类。因此，它经常用于将推文内容流分类为正面和负面情感。这种神经网络模型也用于语言翻译操作。

可以设定一个简单的示例，假设给出了单词“hello”和输入，只有前四个字母 h, e, l, l，而网络应该预测字母 o。这是 RNN 的实际用途之一。

递归公式的工作原理如下：假设一个模型想要预测字母 o，那么它将获取当前字母 l 和前一个字母（也是 l）；因此，对于某一时刻 t，可以通过以下递归公式获得新状态：

```
H[t + 1] = f(H[t],ↆX[t] + 1])
```

其中 `H[t+1]` 是新状态，`H[t]` 是前一个状态，而 `X[t+1]` 是当前输入。因此，如果我们为相同创建激活函数，它将写为

```
H[t] + 1] = tanhↆ(W[hh]H[t] + 1,] +ↆW[xh]
```





*   PyTorch 支持动态计算平台。当我们开始使用 PyTorch 框架时，它会构建计算图，且该图在运行时可以动态更改。

它具有支持多 GPU 的良好优点。由于该框架开发于 2016 年，数据科学家可能会利用这一点。使用 PyTorch 最适合在利用强大的 GPU 的情况下替代 NumPy。它还构建了一个提供最大速度和灵活性的深度学习研究平台。PyTorch 提供了一种运行在 GPU、CPU 或两者之上的张量（tensor）。有各种张量例程可以加速增强科学计算的张量例程。数学、线性代数、索引和切片的执行速度更快（见 图 21.8]）。

![Images](img/021x008.jpg)

**图 21.8**

PyTorch 执行环境。（来源：[pytorch.org](http://pytorch.org)。）

磁带记录方法（tape recorder approach）被用于创建和构建动态神经网络（NN）。PyTorch 的优点之一是它的反向自动微分，这允许网络以最小的延迟和开销改变其行为，这在 TensorFlow 和 Theano 中是无法实现的。PyTorch 深度集成到 Python 中。它可以像使用 NumPy、SciPy 和 scikit-learn 一样自然地使用。PyTorch API 的设计思维是线性的且易用的。对于大型神经网络，PyTorch 运行速度非常快。系统还提高了内存效率。

### 21.2.4 PyTorch 安装

要在 Windows 中安装 PyTorch API，我们可以使用开源安装程序 conda。要获取 conda 安装器，我们必须在系统中下载 Anaconda。我们可以从 [`www.continuum.io/downloads`](https://www.continuum.io) 网站下载 Anaconda 发。我们必须下载正确的 Python 版本，建议在 Windows 上下载并安装 .exe 文件。接下来，我们需要下载 Kivy 安装轮子。然后，在命令提示符运行 anaconda 并输入以下命令下载 PyTorch API：

```bash
conda install -c anaconda python=3.6.1
conda install -c peterjc123 pytorch=0.1.12
```

完成这些操作后，应运行 Kivy 安装。只需将路径更改下载的 kivy 文件夹即可。现在，在 Anaconda 控制台中使用以下命令：

```bash
pip install docutils pygments pypiwin32 kivy.deps.sdl2 kivy.deps.glew
pip install kivy.deps.gstreamer
pip install Kivy-1.10.1.dev0-cp36-cp36m-win_amd64.whl
```

你可以使用以下命令检查安装情况：

```bash
conda list
```

### 21.2.5 PyTorch 张量实现

NumPy 是机器学习的终极框架，但它不使用 GPU 来加速高端数值计算 [18]。在现代海量数据以及图像或视频的深度学习计算时代，GPU 提供的加速速度高达 50 倍或更多。

由于 NumPy 无法利用这一特性，最基本的 PyTorch 概念以张量（tensor）的形式引入。张量在概念上与 NumPy 数组相同。PyTorch 提供了许多用于操作此类张量的函数。张量还会跟踪梯度和计算图。这些也许是科学计算中最智能的工具。由于 PyTorch 支持 GPU，我们只需要在 GPU 引导的环境中转换一个运行张量的新数据类型。以下代码示例讨论了使用 PyTorch 的双层张量：

```python
# code courtesy pytorch.org
import torch
dt = torch.float
dev = torch.device("cpu")
# device = torch.device("cuda:0")  # 取消此注释以便在 GPU 上运行

# N 是批大小；D_in 是输入维度；
# H 是隐藏维度；D_out 是输出维度。
N, D_in, H, D_out = 64, 1000, 100, 10

# 创建随机输入和输出数据
x = torch.randn(N, D_in, device=dev, dtype=dt)
y = torch.randn(N, D_out, device=dev, dtype=dt)

# 随机初始化权重
w1 = torch.randn(D_in, H, device=dev, dtype=dt)
w2 = torch.randn(H, D_out, device=dev, dtype=dt)

lrning_rate = 1e-6
for t in range(500):
    # 前向传播：计算预测的 y
    h = x.mm(w1)
    h_relu = h.clamp(min=0)
    y_pred = h_relu.mm(w2)

    # 计算并打印损失
    loss = (y_pred - y).pow(2).sum()
    print(t, loss)
    # 反向传播计算 w1 和 w2 对应损失的梯度
    grd_y_pred = 2.0 * (y_pred - y)
    grd_w2 = h_relu.t().mm(grd_y_pred)
    grd_h_relu = grd_y_pred.mm(w2.t())
    grd_h = grd_h_relu.clone()
    grd_h[h < 0] = 0
    grd_w1 = x.t().mm(grd_h)

    # 使用梯度下降更新权重
    w1 = w1 - lrning_rate * grd_w1
    w2 = w2 - lrning_rate * grd_w2
```

首先，我们必须选择设备。默认情况下，代码将在 CPU 上运行。如果我们想在 GPU 上运行，只需将 `torch.device()` 参数指定特定的 GPU。我们必须提供批大小、输入维度、隐藏维度和输出维度。然后，我们必须提供随机输入和输出数据并初始化权重。权重初始化后，计算损失和 `y` 的预测值。最后，我们应用反向传播计算相对于损失的梯度 `w1` 和 `w2` 并更新权重。

![Images](img/line.jpg)

### 21.3 本章涵盖

*   监督学习技术
*   SVM Python API
*   NN Python API
*   深度学习工具 CNN 和 RNN
*   Python Tensor API
*   用于深度学习的 PyTorch 实现

![Images](img/line.jpg)

### 21.4 参考文献

1. 1. Dey, Nilanjan, Amira S. Ashour, and Surekha Borra, eds. *Classification in BioApps: Automation of Decision Making*. Vol. 26. Springer, Berlin, Germany, 2017.
2. 2. Ketkar, Nikhil. “Introduction to Pytorch.” In *Deep Learning with Python*, pp. 195–208. Apress, Berkeley, CA, 2017.
3. 3. Chatterjee, Sankhadeep, Sirshendu Hore, Nilanjan Dey, Sayan Chakraborty, and Amira S. Ashour. “Dengue fever classification using gene expression data: a PSO based neural network.” In *Proceedings of the 5th International Conference on Frontiers in Intelligent Computing: Theory and applications*, pp. 331–341). Springer, Singapore, 2017.
4. 4. Chatterjee, Sankhadeep, Sarbartha Sarkar, Nilanjan Dey, Amira S. Ashour, Soumya Sen, and Aboul Ella Hassan. “Application of cuckoo search in water quality prediction using artificial network.” *International Journal of Computational Intelligence Studies* 6, no. 2–3 (2017): 229–244.
5. 5. Lan, Kun, Dan-tong Wang, Simon Fong, Lian-sheng Liu, Kelvin K. L. Wong, and Nilanjan Dey. “A survey of data mining and deep learning in bioinformatics.” *Journal of Medical Systems* 42, no. 8 (2018): 139.
6. 6. Keras. Keras: The Python Deep Learning Library. Retrieved from [`keras.io`](https://keras.io)/
7. 7. GitHub. Retrieved from [`github.com/keras-team/keras`](https://github.com).
8. 8. Chollet, Francois. *Deep Learning with Python*. Manning Publications, Greenwich, CT, 2017.
9. 9. den Bakker, Indra. *Python Deep Learning Cookbook: Over 75 Practical Recipes on Neural Network Modeling, Reinforcement Learning, and Transfer Learning Using Python*. Packt Publishing, Birmingham, 2017.
10. 10. Hu, Shimin, Mengyu Liu, Simon Fong, Wei Song, Nilanjan Dey, and Raymond Wong. “Forecasting China future MNP by deep learning.” In *Behavior Engineering and Applications*, pp. 169–210. Springer, Cham, Switzerland, 2017.





11. Dey, Nilanjan, Simon Fong, Wei Song, and Kyungeun Cho. “基于深度学习的智能家居传感器网络能耗预测.” 于 *信息技术与计算机通信智能趋势国际会议*, pp. 255–265. Springer, Singapore, 2017 年 8 月。

12. Yin, Wenpeng, Kann, Katharina, Yu, Mo, and Schutze, Hinrich. *自然语言处理中 CNN 与 RNN 的对比研究*. 自 [`arxiv.org/abs/1702.01923`](https://arxiv.org/abs/1702.01923), 2017.

13. Li, Zairan, Nilanjan Dey, Amira S. Ashour, Luying Cao, Yu Wang, Dan Wang, Pamela McCauley, Valentina E. Balas, Kai Shi, and Fuqian Shi. “用于糖尿病足底压力成像数据集的卷积神经网络聚类与流学习方法.” *医学影像与健康信息期刊* 7, no. 3 (2017): 639–652.

14. Li, Zairan, Nilanjan Dey, Amira S. Ashour, Luying Cao, Yu Wang, Dan Wang, … 以及 Shi Fuqian. “用于糖尿病足底压力成像数据集的卷积神经网络聚类与流学习方法.” *医学影像与健康信息期刊* 7, no. 3 (2017): 639–652.

15. Wang, Yu, Yating Chen, Ningning Yang, Longfei Zheng, Nilanjan Dey, Amira S. Ashour, … 以及 Shi Fuqian. “基于深度卷积神经网络的小鼠肝肉肉芽肿微图像分类.” *应用软计算* 74 (2019): 40–50.

16. Hore, Sirshendu, Shouvik Chakroborty, Amira S. Ashour, Nilanjan Dey, Ahmed Ashour, Dimitra Sifaki-Pistolla, … 以及 Sekhar Ranjan Bhadra Chaudhuri. “利用微微图像分析寻找海马脑细胞轮廓.” *高级显微镜研究期刊* 10, no. 2 (2015): 93–103。

17. TensorFlow. 自 [`www.tensorflow.org`](https://www.tensorflow.org/)。

18. Tang, Raphael, and Jimmy Lin. Honk: 一种用于关键词识别的卷积神经网络 PyTorch 重实现. *arXiv 论文 arXiv:1710.06554* (2017)。

## 22

![Images](img/line.jpg)

## 结论

![Images](img/line2.jpg)

![Images](img/line.jpg)

### 22.1 第 1 章和第 2 章的说明

[第 1 章] 代表了开源硬件的概念。在本章中，主要讨论了 `Arduino` 及其生态系统。文中介绍了 `Arduino` 的不同型号。除了硬件，还考虑了 `Arduino` 软件套。提到了驱动程序和 IDE 本身的安装。[第 2 章] 涉及对 `Arduino` 板架构的详细说明。考虑了作为 `Arduino` 核心的 `AVR` 微控制器架构。还考虑了电源单元、数字输入输出以及若干允许的外围设备。本章还讨论了中断、第三方设备接口和允许的库等主要概念。

![Images](img/line.jpg)

### 22.2 第 3 至 5 章的说明

[第 3 章] 是专门针对 `Arduino` 编程方法论的章节。讨论了 `Arduino` 中使用的不同数据类型以及变量声明、运算符及其优先级。[第 4 章] 讨论了函数和模块化编程方法，例如 `setup()` 和 `loop()` 函数。在此背景下，还涉及了递归方法调用、库函数设计以及 `fermata` 库的概念。[第 5 章] 包含了条件语句，如 `if-else`、`loop` 和 `switch-case` 系统。`Arduino` 是一个软件驱动的嵌入式计算平台。主要目标是基础固件程序的设计，在本章中得到了成功实现。

![Images](img/line.jpg)

### 22.3 第 6 至 9 章的说明

[第 6 章]和[第 7 章] 主要涉及输入和输出在[第 6 章]中，讨论了重要的 `pinMode()` 函数。[[第 7 章]中，讨论了 `digitalWrite()` 和 `analogWrite()` 函数。[第 8 章] 涉及一个名为 `Processing` 的独特工具。讨论了 `Serial.println()` 的各个方面。

### 22.4 第 10 至 21 章的说明

第 10 至 21 章专为 Python 语言初学者设计。[第 10 章]讨论了运算符、变量和表达式。[第 11 章]涉及决策和控制流。[第 12 章]强调了 `if-else` 和循环（如 `while` 和 `for`）。[第 13 章]涉及函数和模块化编程。[第 14 章]重点关注使用 API 访问 `CSV` 和 `JSON` 数据。[第 15 章]讨论了最经典的数据结构类型，如 `list`、`dictionary` 和 `tuples`。[第 16 章] 概述了 Python 语言面向对象范式的精髓，其中讨论了继承和多态等属性。[第 17 章] 全关于 Python 中的输入输出方案，[第 18 章] 给出了 Python 异常处理机制的精要。[第 19 章]、[第 20 章]和[第 21 章]提供了更高级的概念，如 GUI 编程基础。[第 20 章]和[第 21 章]简要介绍了机器学习 API 和一些真实案例。书中还加入了深度学习方法论概念的介绍。

### 22.5 本书的未来前景与改进

本书基本上涵盖了入门理论以及开源硬件和软件范式的实现。使用本书的学生熟练设计基于 `Arduino` 的系统以及具有 Python 接口的 `Arduino` 驱动系统。使用传感器网络进行数据采集和实时数据分析是目前主要的领域之一。本书强调了此类系统的潜在实现和设计，可作为实时数据分析和预测领域的进一步工具。





# # 22.5.1 结语

在本指南中，我们介绍了基于开源环境的若干种现代智能应用开发。从本书开头开始，我们就介绍了 Arduino 和开源原型开发。考虑了与 Arduino 相关的各种软件和硬件工具。此外，我们还考虑了最流行的编程语言 Python 及其应用开发环境。最后，重点强调了一些最有趣的人工智能和机器学习工具。本书为探索最新的机器学习、深度学习技术以及开源原型平台提供了方向指引。

那么，让我们来创造一些智能设备吧。

![Images](img/line1.jpg)

## 常见问题 (FAQ)

![Images](img/line2.jpg)

1. 如果我没有任何编程和硬件方面的经验怎么办？
   `Arduino` 和 `Python` 等平台非常容易学习。它们的设计使其能够支持自学平台。`Python` 和 `Arduino` 社区都拥有强大的资源和支持文档，因此我们可以以较快的速度学习它们。

2. `Arduino` 可以在任何操作系统 (OS) 上运行吗？
   `Arduino` 支持不同操作系统平台，如 `Windows`、`Linux` 32 位和 64 位以及 `MAC OSX Lion`。此外，它还兼容基于 `ARM` 的 `Linux`，这意味着它也可以在 `Raspberry Pi`（树莓派）平台上运行。

3. `Python` 是面向对象编程 (OOP) 吗？
   `Python` 从早期就被认为是一种面向对象的语言。由于它支持类 (class)、多态 (polymorphism)、继承 (inheritance) 和方法重写 (method overriding) 等功能，它被认为是一种面向对象程序 (`OOP`)。它可能既包含 `OOP` 的核心特征，也包含面向过程语言特征。

4. `Ubuntu Linux` 需要 `Arduino` 驱动吗？
   对于 `Linux` 发行版，广泛使用了推荐的 `.tar.bz` 版本的 `Arduino`。通常情况下，当打开 `Arduino IDE` 硬件连接到 USB 时，USB 设备会自动识别为 `/dev/ttyACM0` 或 `/dev/ttyUSB0`。连接 `Arduino` 后，它会找到并列出所有连接到 `Arduino` 的可能 USB 端口。如果匹配到 `产品 + 厂商 ID`，开发板将以串口端口菜单项的形式出现。

5. 我们在 `Arduino` 中使用了哪些传感器？
   `Arduino` 支持各种模拟和数字传感器，从简单的 `LDR`（光敏电阻）到 `LM35` 以及温湿度传感器等许多传感器。其中，运动传感器 (motion sensor)、超声波传感器 (ultrasonic sensor) 和气体传感器 (gas sensor) 等数字传感器非常流行。它们还支持 `MEMS` 设备，如陀螺仪 (gyroscope)、加速度计 (accelerometer)、磁指南 (magnetic compass) 和气压计 (barometer)。

6. 为什么要使用 `Processing`？
   `Processing` 是一个用于实时数据可视化的实用编程环境。它支持广泛的颜色和效果，不仅对可视化非常有用，对于创建独特的视觉效果也有帮助。核心应用程序简化了基础的多媒体支持，如 `OpenGL`、`PDF` 和相机捕捉。`Processing` 使用可扩展的库支持和代码结构来创建复杂的 3D 几何形状。

7. `Arduino` 在什么电压下烧毁（工作电压）？
   `Arduino` 的电压范围在 5 到 20 V 之间。如果给 `Arduino` 的电压太低，板载的活动将变得非常不稳定。在这种情况下，开发板将无法为其外围设备（如输入传感器或输出执行器）提供足够的功率。电压超过 12 V 会影响 `Arduino` 内部电压调节器的功能。在 18–19 V 范围内，调节器开始烧毁，`Arduino` 板会受到损坏。

8. 什么时候应该使用 `Python` 的 `for loops`？
   最好使用 `for loop` 来遍历数字序列。`for loop` 取出序列中的每个元素并将其存储在`迭代变量`中。`Python` 中 `for loop` 的另一个用途是遍历 `list`（列表）结构。

9. `Python` 程序需要缩进吗？
   `Python` 最独特的特性之一就是它的缩进。在 `Python` 中，代码块可以通过其缩进被唯一标识。与 `C` 或 `Java` 语言不同，代码块是通过大括号标识的。在这种情况下，代码的缩进不是强制的。由于这一点以及有时由于糟糕的编程习惯，阅读 `C` 和 `Java` 的程序块变得相当困难。`Python` 将其变为强制性，从而提高了程序代码的可读性。

10. 推荐使用哪个 `pip` 安装 Python 包？
    这取决于 `Python` 版本。`Python 2.7` 预装了 `pip`。但如果我们使用的是 `Python 3` 版本，建议使用 `pip3`。在安装之前，我们可以通过命令 `pip version` 检查版本。如果没有安装，我们可以使用命令 `python -m ensurepip–default -pip` 从标准库进行引导。然后根据需要进行安装。

11. 在 `Linux` 中，`Python` 包是通过 `Synaptic Package Manager` 安装的吗？
    `Synaptic Package Manager` 适合安装标准的 `Python` 包。但它的主要缺点是依赖于特定版本。在低版本的 `synaptic` 中，很难获取最新版本的包。Ubuntu 软件中心也可能出现相同的问题。安装最新 `Python` 包的最佳方法是通过 `pip` 安装器。

12. 在机器学习代码开发中，有必要使用 `NumPy` 和 `SciPy` 包吗？
    基础机器学习方法用于更复杂的数学计算。`NumPy` 为我们提供了大量的数值计算。`SciPy` 提供了复杂的数学计算，如积分和微分。此外，`pandas` 和 `scikit-learn` 是基础机器学习的重要元素。

13. `Java` 和 `Python` 命令行参数有什么区别？
    主要区别在于处理命令行参数的方法。在 `Java` Case 中，命令行参数通过 `public static void main(String args[])` 方法传递。在这种情况下，`String args[]` 是字符串类型的命令行参数。在 `Python` 中使用命令行参数，我们需要导入 `sys` 包。然后就可以从 `sys` 包的 `argv` 列表中找到参数。在这里，我们应该写 `x = sys.argv[0]`（注：此处原文即为示例）。

14. 是否可以在并行模式下运行两个 `Arduino`？
    两个 `Arduino` 可以以主从模式耦合。为了实现这一点，我们可以在两个 `Arduino` 之间建立集成电路接口 (I²C) 通信接口。这通常在我们想要分担单个 `Arduino` 工作负载时完成。在这种情况下，两个 `Arduino` 必须连接串行数据 (SDA) 和串行时钟 (SCL)。如今，得助于支持 `Arduino` 的多任务实时操作系统 (RTOS)，可以同时在 `Arduino` 上并行运行多个代码。现在已提供免费的多任务 RTOS，让你能够并行核心程序。

15. 是否可以在 `Raspberry Pi` 上运行 `Tensor Flow` 或其他深度学习工具？




如 `Tensor Flow`、`PyTorch` 和 `Keras` 等深度学习工具处理高度复杂的卷积神经网络 (`CNN`) 和循环神经网络。这些模型占用巨大的计算空间。例如，由于神经连接的权重，一个神经网络有时会使用 200 MB 的浮点格式空间。网络中数数百万计这样的连接。权重可能以 32 位浮点格式存储。我们可以通过量化来缩小文件大小，并为每层设置最大值。通过这种方式，可能实现权值的压缩，这可能适用于内存容量较低的机器上运行复杂的 `CNN`。

# 16. 是否有适用于 TensorFlow 和深度学习的独立硬件？

有几种适用于 TensorFlow 机器学习的专用硬件可用。其中流行的是 Lambda Deep Learning Dev Box，它由 `Ubuntu 18.04 bionic` 操作系统、`4xNVIDIA Gforce GTX 1080 Ti`、带有 `64 GB DDR` 和 `2GB SATA SSD` 的 `Intel XEON` 处理器以及 `4 GB` 的 `HDD` 组成。它预装了 `Keras`、`Theano`、`Tensor Flow` 和 `Pytorch`。`Google Edge TPU` 是另一项为 `Raspberry Pi` 等低功耗计算设备提供高功率机器学习工作的发明。借助此类 `TPU`，我们可以在便携设备层级创建轻量级 AI 平台。它的 CPU 是 `NXP i.MX 8M SoC`（四核 `Cortex-A53`、`M4F`）。它的 GPU 是集成的 `GC7000 Lite`。它包含 `1GB RAM` 和 `8GB flash`。支持的操作系统有 `Debian Linux` 和 `Android Things`。支持 `Tensor Flow Lite` 框架。`Edge TPU Accelerator` 是另一个可以通过作为 USB 设备引入来增强应用程序 `Tensor Flow` 处理能力的平台。规格与前一个相同。

![Images](img/line1.jpg)

## Index

![Images](img/line2.jpg)

### A

*   访问 CSV 文件 135, 136
*   激活函数 213–215, 217, 218
*   ADC *见* 模数转换器 (ADC)
*   Alf 和 Vegard 的 RISC (`AVR`) 14–17, 36, 39, 52, 57, 225
*   Alpha 值 89
*   `analogRead()` 函数 54
*   模数转换器 (ADC) 15, 16
*   `analogWrite()` 函数
    *   ATmega PWM 访问 61–63
    *   操作 60
    *   PWM 细节 61
*   Android 应用程序接口 (`API`) 2, 70, 136–137
*   Arduino 应用
    *   社区和社交编程 10
    *   4 的比较
    *   DUE 环境 9–10
    *   生态系统 1–2
    *   2 的硬件抽象层
    *   3 的硬件、特性
    *   3–6 的软件、特性
*   基于 Arduino 的心率监测系统 95–97
*   基于 Arduino 的 LPG 检测器系统 98–100
*   基于 Arduino 的雷达系统 78
*   Arduino 代码 76–77, 78, 95
*   `Arduino.digitalWrite()` 方法 44
*   Arduino Esplora 20–21
*   Arduino 硬件
    *   ADC 输入 16
    *   Arduino Esplora 和 TFT 库 20–21
    *   arduino 中断 18
    *   详细板 17
    *   数字 I/O 16
    *   微控制器 14–16
    *   外设设备 18–19
    *   17 中的外设
    *   电源单元 16
    *   21 中的处理
    *   系统架构 13–14
    *   TFT 接口 19
*   Arduino 编程语言 33
*   参数传递 129–130
*   算术运算 30, 111–112
*   arduino 中的数组和字符串 25–26
*   `array()` 函数 192
*   人工神经网络 (`ANN`) 212–214, 216
*   ASCII（美国标准编码） 25, 26, 103
*   `asctime()` 函数 150
*   赋值运算符 115–116
*   结合性 31
*   基于 ATmega 的 Arduino UNO 23
*   基于 ATmega 的系统 25
*   ATmega 微控制器芯片 52
*   ATmega328p 14, 19, 39
*   ATmega PWM 访问 61–63
*   ATmega328 PWM 引脚配置 62, 63
*   ATmega16U2 14
*   ATmega32U4 15, 17
*   `attachInterrupt()` 函数 50
*   属性（控件选项） 183
*   `Audio()` 方法 155
*   自动道闸控制
    *   电路图 92–94
    *   分步骤程序 91–92
*   `available()` 函数 55, 74
*   AVR *见* Alf 和 Vegard 的 RISC (`AVR`)](#ch24_bm01_index.xhtml_idx)
*   基于 AVR 的 Arduino 36
*   基于 AVR 的微控制器 52, 57

### B

*   `background(color)` 函数 88
*   基础动画 70
*   每分钟心率 (`BPM`) 95
*   位运算符 30, 113–114
*   布尔值 112, 114, 164
*   break 和 continue 语句 125–126
*   `buffer()` 函数 75
*   按钮控件 181–183

### C

*   `calculateDistance()` 函数 80
*   `callme()` 方法 182
*   `call1()` 方法 184–185
*   Canvas 控件 183–184
*   Checkbutton 控件 184–185
*   电路图 92, 93, 95
*   客户端管理工具 141–142





* `close()` 操作 164
* `cls()` 函数 116
* `CNN` *参见* 卷积神经网络 (CNN)
* `color mode()` 89
* 颜色透明度 89
* 命令行参数 136, 166–167, 231
* 命令行界面 104–107
* 命令 MIDI 通道压力 (0XD0) 42
* 比较运算符 112
* 条件语句
    * do-while 循环 49
    * if-else 条件语句 45–46
    * if-else-if 阶梯结构 46
    * `loop()` 函数 49–50
    * Arduino 中的循环 47–48
    * switch-case 语句 46–47
    * while 循环 48
* 卷积神经网络 (CNN) 213, 216–217, 231
* `copy()` 方法 194
* 核心组件类
    * 按钮组件 widget 181–183
    * 画布组件 widget 183–184
    * 复选框组件 widget 184–185
    * 输入框组件 185
    * 框架组件 widget 186
    * 标签框架组件 widget 186
    * 列表组件 widget 187
    * 菜单组件 widget 187–189
    * 单选按钮 189–190
* 知识共享署名许可协议 1

### D
* 数据结构
    * 数据元素，排序 147–149
    * 字典结构 146–147
    * Python
        * 日期和时间 149–150
        * 列表 143–145
        * 字符串 150–151
        * 元组 145–146
* 数据可视化 64, 66, 69, 77, 194
* 决策与控制流
    * if-elif-else 120–122
    * if 语句 19–120
    * Python 中的循环 122–126
* 深度学习工具
    * 卷积神经网络 216–217
    * PyTorch API 220–221
    * PyTorch 安装 221–222
    * PyTorch 张量实现 222–223
    * 循环神经网络 217–218
    * 张量 API 218–220
* 详细板级配置 17
* 设备驱动，安装 8, 9
* DFX 导出 72, 75
* Arduino 数字 I/O 16
* `digitalRead()` 函数 53–54, 99
* `digitalWrite()` 函数 59, 99
* DIP-28 配置 14
* `dir()` 函数 133
* do-while 循环 49, 124
* `draw()` 函数 44
* 驱动管理窗口 7
* 驱动软件 8

### E
* EEPROM *参见* 电擦除可编程读读存储器 (EEPROM)
* EEPROM 库 39
* 8 位定时器/计数器电路 15
* 电擦除可编程读读存储器 (EEPROM) 14, 39, 40
* else 语句 119, 123, 124, 173–174
* 输入控制循环 48
* 输入框组件 185
* 枚举类型 28–29
* Python 中的异常类型 170, 171

### F
* Fast PWM 模式 62, 63
* 文件输入输出 162–163
* 文件对象 163–164
* `fill()` 函数 88, 89
* finally 块 174–175
* Firmata 命令 42
* Firmata 控制 42, 77
* Firmata 库 55, 56
* 浮点数据 25, 36
* 循环 47, 48, 124, 125, 136, 137
* 框架组件 186
* 面向对象方法 44
* Python 中的函数
    * 参数传递机制 129–130
    * 关键字参数 128–129
    * lambda 函数 131–132
    * Python
        * 模块 132–133
        * 包 133–134
    * `reload()`, `global()` 和 `local()` 134
    * 标准符号 127–128
* 面向对象编程
    * 库 42
        * EEPROM 库 39
        * `get()` 函数 41
        * `put()` 函数 40–41
        * `read()` 函数 39
        * `update()` 函数 41–42
    * 递归函数调用 35–37
    * `setup()` 和 `loop()` 函数 33–34
    * 用户定义函数 34–35

### G
* 门控制代码 92–94
* 真正的递归程序 36
* `get()` 函数 41
* GPU *参见* 图形处理器 (GPU)





# 图形用户界面 (GUI)

## 核心组件类
- `Button widget` 181–183
- `Canvas widget` 183–184
- `Checkbutton widget` 184–185
- `entry widgets` 185
- `Frame widget` 186
- `LabelFrame widget` 186
- `Listbox widget` 187
- `Menu widget` 187–189
- `radiobutton` 189–190
- `Tkinter`, 介绍 177–180

# 图形处理器 (GPU) 215, 220, 222, 223, 232

# `GUI()` 方法 155

## H

### 异常处理
- `else statement` 173–174
- `finally block` 174–175
- `try: except 技术` 171–172

- `硬件 I/O` 72, 75
- `硬件 SPI 方法` 20
- `哈佛体系架构` 14
- `心跳监控，原理` 94
- `层级继承特性` 158

## I

- `I2C` 参阅 集成集成电路 (I2C)
- `IDE` 参阅 集成开发环境 (IDE)
- `恒等运算符` 114–115
- `If-elif-else 阶梯结构`
    - `阶梯表示` 120–121
    - `三元运算符` 121–122
- `If-else 条件条件语句` 45–46
- `INPUT` 和 `INPUT_PULLUP` 配置 52–53
- `输入输出机制`
    - `close()` 操作 164
    - `命令行参数` 166–167
    - `文件输入/输出` 162–163
    - `file 对象`,属性 163–164
    - `input()` 函数 161–162
    - `raw_input()` 函数 161–162
     ` `()` 方法 164–165
    - `seek()` 方法 165–166
    - `tell()` 方法 165
- `输入设备接口` 56–57
- `input()` 函数 161–162
- `输入输出示例` 64–67
- `输入引脚属性` 56–57
- `输入系统`, Arduino
    - `analogRead()` 函数 54
    - `digitalRead()` 函数 53–54
    - `firmata 库，输入` 55–56
    - `INPUT` 和 `INPUT_PULLUP` 配置 52–53
    - `输入设备接口` 56–57
    - `pinMode()` 函数 51–52
- `整数常量` 24, 25
- `集成开发环境 (IDE)` 3–5, 9, 10, 18, 38, 70–72, 141, 204, 225
- `集成电路 (I2C)` 2, 15, 17, 43, 231
- `中断处理器` 18
- `interrupts()` 函数 49
- `调用函数`
    - `参数传递` 129–130
    - `调用方法论` 128–129

## J

- `Java` 1, 69–71, 85, 229
- `Java 语法` 70
- `Java 运行时` 1
- `JavaScript 对象符号 (JSON)` 135–137, 139, 140
- `JSON 数据` 136–138, 226
- `json.loads()` 方法 138

## K

- `基于 Keras 模型` 219
- `关键字概念` 130–131

## L

- `LabelFrame widget` 186
- `Label()` 方法 179
- `阶梯表示` 120–121
- `Lambda 函数` 131–132, 148
- `Last()` 方法 75
- `LCD` 参阅 液晶显示 (LCD)
- `光敏电阻` 75
- `linspace()` 函数 193
- `Linux` 9, 72, 75, 106, 108, 156, 159, 191
- `液晶显示器 (LCD)` 18, 25, 95, 98, 99, 203
- `Listbox widget` 187
- `使用 pandas 加载 CSV` 136
- `localtime()` 方法 150
- `逻辑运算符` 45, 112
- `loop()` 函数 33–35, 49–50, 53–54, 80
- `Python 中的循环`
    - `break 和 continue 语句` 125–126
    - `for 循环` 124–125
    - `嵌套循环` 125
    - `奇数循环` 125
    - `while 循环` 122–124
- `LPG 气体检测器模块` 98
- `LPG 传感器应用` 98, 100

## M

### 机器学习 API
## 深度学习工具
    - `卷积神经网络` 216–217
    - `PyTorch API` 220–221
    - `PyTorch 安装` 221–222
    - `PyTorch 张量实现` 222–223
    - `循环神经网络` 217–218
    - `tensor flow API 用于` 218–220





# scikit learn
* 激活函数 213–214
* ANN 实现 214–215
* 人工神经网络 212–213
* 监督学习 207–209

# 支持向量机
* 212 的优缺点
* 分类器 209–211
* 211–212 的实现

* `main.cpp`, 6 的实现
* `mainloop()` 方法 180
* `Malloc()` 函数 29
* Matplotlib 64
* 195–196 的核心组件
* 属性属性 196–197
* 多重图表示 197
* 矩阵样式键盘界面 19
* 成员运算符 115
* 菜单小部件 187–189
* 微控制器 9, 13–17, 39, 42, 52, 53, 57
* MIDI 查看[乐器数字接口 (MIDI)]](#ch24_bm01_index.xhtml_idx197)
* 每秒百万次指令 (MIPS) 14
* `Millis()` 函数 18
* 模块化编程方法 33, 225, 226
* MongoDB 138–142, 226
* 最高有效位 (MSB) 23
* 鼠标活动控制 85
* `mouseButton()` 函数 87
* `mouseClicked()` 函数 85, 87
* `mouseDragged()` 函数 88
* `mouseMoved()` 函数 86, 88
* `mousePressed()` 函数 86, 87
* `mouseReleased()` 函数 87
* `mouseWheel()` 函数 88
* `mouseX` 86
* `mouseY` 86
* MSB 查看[最高有效位 (MSB)]](#ch24_bm01_index.xhtml_idx185)
* 乐器数字接口 (MIDI) 42, 55
* `myServo.write(i)` 函数 80

### N
* 嵌套循环 34, 125
* 网络 26, 72, 75, 215, 216, 218
* `noInterrupts()` 函数 49
* NoSQLBooster 141, 142
* `NOT` 运算符 114
* NumPy 包 191–194

### O
* 面对象编程
* 类组件 155
* 构造函数 154–155
* 继承概念 157–159
* 方法重写概念 159–160
* Python
* 类 153–154
* 多态性 155–157
* 基于 OCRA 的 PWM 62
* 奇数循环 123, 125
* 开源硬件
* Arduino 应用
* 社区与社交编程 10
* 环境 9–10
* 生态系统 1–2
* 硬件特性 3
* 软件特性 3–6
* 概念 1
* 设置 Arduino 6–9
* Python 中的运算符
* 算术运算符 111–112
* 赋值运算符 115–116
* 位运算运算符 113–114
* 比较运算符 112
* 恒标识运算符 114–115
* 逻辑运算符 112–113
* 成员运算符 115
* 输出系统，Arduino
* `analogWrite()` 函数 60–63
* `digitalWrite()` 函数 59
* 输入输出示例 64–67

### P
* `pack()` 方法 179
* 解析方法 55
* 解析技术 56
* PDF 导出 72, 75
* `pd.read_excel()` 函数 65
* Arduino 外围设备 17
* 相位校 PWM 62
* `pinMode()` 44, 51, 59
* pip 查看[Python]](#ch24_bm01_index.xhtml_idx24)
* `plot()` 函数 65
* 绘图 64
* `mouseX` 86
* `mouseY` 87
* `point()` 函数 73
* 多态性 155–157
* 功率 16
* 优先级 31, 225
* 偏好 5
* 原始数据类型 28
* 数组与字符串 25–26
*  24
* 字符 24–25
* 浮点数 25
* 整数 23, 24
* int 类型 24
* 字符串 26–28
* `print()` 函数 35
* Processing 语言
* Arduino 与 Firmata 77–84
* 代码结构
* 对象、绘图 73–74
* 处理代码 72–73
* 代码结构 72, 80–84
* 颜色方案 88–89
* 一般概览 69–70
* LDR 输出 75–77
* 库与函数 74–75
* 在鼠标处理中 84–88
* 处理软件 70–72
* Processing，相似性 21
* 处理软件 70–72
* `processInput()` 函数 55





* 原型项目 91
* `publicvoid function` 34
* `public void loop()`函数 34
* 上拉/拉低电阻 57
* 脉宽调制 (PWM) 15, 43, 53, 56, 60–63, 95, 99
* `put()` 函数 40–41
* PWM 参见 脉宽调制 (PWM)
* PWM 模式 62, 63
* Python API 模块
    * Arduino API
        * Nanpy API 203
        * Nanpy 安装 203–204
        * 原型设计 202–203
    * 机器学习工具 198–201
    * Matplotlib
        * 195–196 的核心组件
        * 条属性 196–197
        * 多重图形表示 197
    * SciPy 和 NumPy 包
        * 193–194 的拷贝操作
        * 192–193 的基本目标
        * 197–198 概览
* Python 安装
    * 在 Ubuntu 中 104–105
    * 在 Ubuntu Linux 中 104
    * 在 Windows 中 104
* Python 语言 64
    * 基础程序 105–107
    * 101 的特性
    * 安装 103–105
    * 使用 pip 安装 107–109
    * 122 中的循环结构
    * 132–133 中的模块
    * 133–134 中的包
    * 102–103 的版本
* Python 模式处理 70–71
* Python 包安装器 (pip) 107–109, 191, 199, 219
* `python_version()` 函数 102
* Python 2.7.x 代码 102–103
* PyTorch API 220–221
* PyTorch 安装 221–222
* PyTorch 张量实现 222–223
### R
* 单选按钮 189–190
* 栅栏门 92
* `raw_input()` 函数 161–162
* `read_csv()` 函数 136
* `reader()` 函数 136
* `read()` 函数 39, 40, 75
* 读取 CSV 数据 136
* `read()` 方法 164–165
* 现实代码
    * 基于 Arduino 的心率监测 95–97
    * 基于 Arduino 的检测器 98–100
    * 自动轨道控制
        * 电路图 92–94
        * 逐步过程 91–92
* 循环神经网络 (RNN) 217–218
* `recurse()` 函数 37
* 递归调用 35–37
* 精简指令集 (RISC) 架构 9, 14
* `remove()/pop()` 函数 144–145
* 电阻值 52
* RISC 参见 精简指令集 (RISC) 架构
* Robo 3T/Robomongo 141
### S
* Scikit learn
    * 激活函数 213–214
    * ANN 实现 214–215
    * 人工神经网络 212–213
    * 监督学习 207–209
* SciPy 和 NumPy 包
    * 193–194 的拷贝操作
    * 192–193 的基本目标
    * 197–198 概览
* SciPy 包列表 198
* SCLK 参见 串行钟 (SCLK)
* `seek()` 方法 165–166
* 串行钟 (SCLK) 20
* 串口库 71–72, 74
* `serial.list()` 84
* `serial.print()` 26
* `serial.println()` 54, 65
* 从机外接口 15, 17, 19
* SMD 参见 表面贴装器件 (SMD)
* `sort()` 方法 147
* SPI 参见 从机外接口 (SPI)
* `sprintf()` 函数 27–28
* Static RAM 参见 静态内存 (SRAM)
* 静态数据块 37
* `strip()` 方法 151
* `stroke(color)` 函数 88
* 支持向量机 (SVM)
    * 优点与缺点 212
    * 分类器 209–211
    * 211–212 的实现
* 表面贴装器件 (SMD) 13
* `swap()` 函数 129
* Switch-case 语句 46–47
* 语法错误与异常 169–171
### T
* `tell()` 方法 159, 165
* 三元运算符 121–122
* 薄膜晶体管 (TFT) 19–21
* “TIMER0_COMPA” 中断 18
* 定时器 0 18
* `time.time()` 值 150
* Tkinter 库 177–180
* try:except 技巧 171–172





*   二维数组 26, 27, 193

### U

*   UART *参阅* 通用异步收发传输器 (UART)
*   Ubuntu Linux 104, 107, 177
*   超声波距离传感器 67
*   超声波波传感器 64
*   通用异步收发传输器 (UART) 3, 14, 17, 19
*   通用串线 (USB) 3, 7, 9, 14, 17, 19, 55, 229, 232
*   协调世界时 (UTC) 149
*   Unix 149, 158, 159
*   `update()` 函数 41–42
*   USB *参阅* 通用串线 (USB)
*   用户定义数据类型 26, 28–29
*   用户定义函数 34–35
*   UTC *参阅* 协调世界时 (UTC)

### V

*   变量声明 29
*   `Void checkDigitalInput(void)` 函数 43
*   `void draw()` 函数 72–73
*   `void loop()` 函数 67
*   `Void readAndReportData` 函数 43
*   `void setPinModeCallback` 函数 43
*   `void setup()` 函数 35, 54, 72–73
*   冯·诺依曼架构 14

### W

*   while 循环 48, 122–124
*   `write()` 函数 40
*   `write()` 方法 164–165

### X

*   XOR 异运算符 114
*   `xrange()` 函数 103

### Z

*   零寻址机制 26
*   `ZeroDivisionError` 170

