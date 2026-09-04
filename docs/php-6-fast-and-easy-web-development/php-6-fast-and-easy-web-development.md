
# PHP 6 快速简单的 Web 开发

![](img/bc248f3d24697d1afbacee37b9c4d229_0_0.png)

# 致谢

一如既往，感谢 PHP Group、Zend Technologies、Apache Software Foundation 和 MySQL AB 为所有用户创建并维护如此优秀且易用的产品。

感谢每一个 PHP 用户和开发者，因为没有你们，我无字可写。

非常感谢与我共同完成这两个版本的编辑们！

衷心感谢 i2i Interactive 的所有人，感谢他们无尽的支持和鼓励。

# 关于作者

**Julie Meloni** 是 i2i Interactive 的总监，这是一家位于加州坎贝尔市的多媒体公司（就在圣何塞的街对面）。自从 Web 诞生以来，她一直在开发 Web 应用程序，并记得第一个 GUI Web 浏览器出现时的兴奋心情。她是多本关于 Web 编程语言和数据库主题的书籍及文章的作者，你可以在多种语言中找到她的作品翻译，包括中文、意大利语、葡萄牙语、波兰语甚至塞尔维亚语。

# 引言

在《PHP 快速易懂的 Web 开发》第一版出版后的两年里，我收到了大量关于本书教学风格的积极反馈。当我的第一本书《PHP 基础》发布大约一个月后，我的编辑们说有必要出一个“快速易懂”的版本时，我起初是怀疑的。“快速易懂”风格是一种循序渐进的、通过示例来学习新编程语言的方法——还包含了图片！与大多数编程书籍长篇大论、充斥文字的章节不同，“快速易懂”的风格确实吸引了 PHP 初学者，特别是那些初次用 PHP 编程的学者。

这第二版考虑了第一版的某些反馈，同时保持了原始的结构和学习路径。前三章专门用于在 Windows 或 Linux 机器上运行 Apache、MySQL 和 PHP。你可能会惊讶它是如此简单，以及你启动的速度有多快。

书中增加了额外的章节，以提供更多项目来练习你的新技能；一些关于额外数据库和编程信息的附录也完善了这个新版本。对于最适合通过示例学习的初学者来说，这本书仍然是一份坚实的介绍。在完成本书后，你将在进入高级应用设计之前在基础方面打下良好的基础。

在开始学习之前，请花一点时间熟悉 PHP 及其历史。

# 什么是 PHP？

它的正式名称是 `PHP: Hypertext Preprocessor`（超文本处理器），是一种服务端脚本语言。当你的 Web 浏览器访问 URL 时，它正在向 Web 服务器发送请求。当你请求一个 PHP 页面（例如 `http://www.yourcompany.com/home.php`）时，Web 服务器会激活 PHP 解析引擎并说：“嘿！在我把结果返回给个人的 Web 浏览器之前，你必须做些什么。”

然后，PHP 解析引擎运行 `home.php` 中的 PHP 代码，并将结果返回给个人的 Web 浏览器。

# PHP 简史

1994 年，一位非常有见性的男人 Rasmus Lerdorf 开发了一套使用 PHP 解释个人主页的工具。他最终将这些工具与数据库支持相结合，并发布了被称为 PHP 的软件。

随后基于开源的精神，全世界的开发者开始做出贡献。到 1997 年，已有超过 50,000 个网站使用 PHP 完成不同的任务。

从那时起，开发过程真正开始变成团队协作。在 Zeev Suraski 和 Andi Gutmans 的主要协助下，创建了 3.0 版本。PHP 3.0 的最终发布于 1998 年 6 月，当时它升级为支持多个平台（不再仅限于 Linux！）、Web 服务器、众多数据库以及 SNMP（简单网络管理协议）和 IMAP（互联网消息访问协议）。

接着，PHP 4.0 诞生了。这不是一个小小的版本变更，PHP 4.0 标志着对 PHP 核心的反思考以及对脚本语言本身的重写。PHP 开发团队和 Zend Technologies 产生了一款卓越的产品，性能比版本 3.0 提高了近 50%，并拥有一系列新颖实用的功能。

我们现在开始了吗？

- 全球有超过 700 万服务器运行 PHP 4.x 版本。
- PHP 4.x 已发布两年，当前版本为 4.2.1。
- PHP 4.x 可以与你想象的任何 Web 服务器、操作系统和数据库组合。
- Zend Technologies 等公司发布了优化和加速 PHP 的产品，以及用于开发和测试 PHP 代码的“工作室环境”。

# PHP 能做什么？

PHP 可以做任何你想做的事，除了倒立着旋转。实际上，通过一些即时图像处理和动态 HTML，它可能也能做到这一点。

根据 PHP 手册的，“该语言的目标是允许 Web 开发者快速编写动态生成的页面。”

以下是 PHP 的常见用途：

- 执行系统功能：创建、打开、读取、写入和关闭系统文件；执行系统命令；创建目录；以及修改权限。
- 从表单收集数据：将数据保存到文件中；通过电子邮件发送数据；向用户返回处理后的数据。
- 访问数据库并动态生成内容，或创建一个 Web 界面来对数据库中的元素进行添加、删除和修改。
- 设置 cookie 并访问 cookie。
- 启动会话并使用会话变量和对象。
- 使用 PHP 身份验证来限制对网站某些部分的访问。
- 动态创建图像。
- 加密数据。

这些都是日常用途。PHP 还包含了对 Java、Java Servlets、XML 以及许多其他高层函数的支持。它的可能性是无限的。

## PHP 适合我吗？

只有你才能决定 PHP 是否应该是你的首选语言，无论你是在开发小型或大范围的个人或商业用途的网站。我只能告诉你，在商业领域，我用过所有流行的服务器端脚本语言——Active Server Pages (ASP)、ColdFusion、Java Server Pages (JSP)、Perl，并且在许多平台和 Web 服务器上取得了不同程度的成功。PHP 对我来说是正确的选择：它灵活、快速、要求简单，且输出强大。

在决定是否在大规模或商业环境中使用 PHP 之前，请考虑好你对这些问题的回答：

- 你能百分之百确定你将始终使用相同的 Web 服务器硬件和软件吗？如果不能，请寻找适用于所有类型服务器的跨平台工具：PHP。
- 你会拥有一个完全由 ASP（或 ColdFusion）开发人员组成的相同开发团队吗？还是来谁用谁，因此需要一种易于学习且语法与 C 和 Perl 相似的语言？如果有理由相信你的 ASP 或 ColdFusion 开发者可能会人间蒸发，请不要使用这些工具——请使用 PHP。
- 内存和服务器负载是问题吗？如果是，不要使用泄漏宝贵内存的臃肿第三方软件——使用 PHP。

结论是：PHP 很简单，试用一下吧！如果你喜欢它，就继续使用。它是开源的，所以尽管用吧。加入邮件列表，帮助他人。如果你不喜欢，你最多只是损失了这本书的 25 美元，而且软件可以卸载，而不会让你的机器完全无法运行。

这本书有自己的网站。这很正常。

## 概述

MySQL 是大多数使用 PHP 的 Web 开发者的首选数据库，因为它高效且易于使用。此外，MySQL 是免费的，运行在多个平台上，而且它的文档非常出色。在 PHP 中使用 MySQL 时，先安装 MySQL 是简单的，因为在 PHP 的安装和配置过程中，你必须告诉 PHP 配置脚本 MySQL 在你系统中的位置，以激活特定的 MySQL 函数。在本章中，你将学习如何执行以下操作：

- 在 Windows 或 Linux 上安装 MySQL
- 创建示例数据库
- 创建示例表

最流行的 MySQL 发行版是 MySQL AB 的开源版本。然而，还有 MySQL 的商业版本，以及与应用服务器软件捆绑的 MySQL 版本。提供这些选项的公司包括 AriaSoft (`http://www.abriasoft.com/`) 和 NuSphere (`http://www.nusphere.com/`)。无论你选择哪种方案，所有平台都有相应的解决方案——任何类 Unix 操作系统，以及 Windows 95/98/2000/XP。

如果你使用的是互联网提供商提供的 Web 托管包中的 MySQL，你就不需要担心下载和安装它。相反，你只需要与你的 ISP 合作获取你的用户名和密码。在几乎所有情况下，你的 ISP 运行的都是 MySQL AB 的 MySQL 版本。如果你有开发机，在上面设置 MySQL 也没有坏处，只是为了更好地理解这个过程。如果你有一台 Linux 工作站，MySQL 可能已经包含在你的操作系统中了，也许你已经安装了它。在这种情况下，你应该检查 MySQL 网站以比较版本号，如果有新版本则进行下载。

本章中的安装说明是关于 MySQL AB 分发的 MySQL 4.0 版本。较早的版本（如 MySQL 3.2.x）遵循相同的步骤。无论使用 MySQL 3.2.x 还是 4.0，你都可以使用书中所有与数据库相关的示例。

### 在 Windows 上安装 MySQL

Windows 95/98/2000/XP 上的 MySQL 安装过程是由 MySQL AB 提供的可执行设置程序。一旦下载了 zip 文件，你就必须将其内容提取到临时目录并运行 `setup.exe`。在 `setup.exe` 安装完 MySQL 服务器和客户端程序后，你就可以开始启动 MySQL 服务器了。

1. 访问 `http://www.mysql.com/downloads/mysql-4.0.html` 上的 MySQL 4.0 下载页面，找到页面上的 Windows 部分。你想下载“Installation files (zip)”而不是“Cygwin downloads (tar.bz2)”。
2. 点击 Download 链接将带进入镜像站点页面。选择离你最近的镜像，并点击 HTTP 或 FTP 链接下载文件。使用 HTTP 方法通常更快。
3. 一旦 Zip 文件位于你的硬盘上，将其内容提取到临时目录。
4. 从临时目录找到 `setup.exe` 文件并双击它以开始安装。你将看到安装向导的第一个屏幕。点击 Next 继续。
5. 安装过程的第二个屏幕包含安装位置的重要信息。默认安装位置是 `C:\mysql`，但如果你计划在其他位置安装 MySQL，此屏幕显示了你需要做的一些更改。对于希望将 MySQL 作为服务的 Windows NT 用户，此屏幕也很重要。阅读信息并根据你的情况进行记录，然后点击 Next 继续。
6. 安装过程的第三个屏幕让你选择安装位置。如果你想在默认位置安装，点击 Next 继续。否则，点击 Browse 并导航到你选择的位置，然后点击 Next 继续。
7. 第四个屏幕让你选择安装方法：Typical、Compact 或 Custom。选择 Typical 并点击 Next 继续。
8. 安装过程现在将接管并在相应的位置安装文件。过程完成后，你将看到完成确认。点击 Finish 完成设置过程。
9. MySQL 现在已安装在你的系统上。然而，从头安装 MySQL 后，你在 Windows 菜单中找不到任何快捷方式，所以现在你必须手动启动。如果你导航到 `C:\mysql` 目录，你会发现几个就绪的应用程序。这些程序之一被称为 Workbench，它是刚开始使用 MySQL 的 Windows 用户的很好的朋友。如果你双击 MySQL 服务器将其置于任务栏，你就可以启动图形界面来维护和监控你的新服务器。

`WinMySQLAdmin` 会自动解释环境信息，例如 IP 地址、机器名称等。顶部的标签允许你查看系统信息并编辑 MySQL 配置选项。要关闭 MySQL 服务器或 `WinMySQLAdmin` 工具，再次右键点击任务栏上的图标并选择相应的选项。只要 MySQL 服务器正在运行，你就可以控制窗口运行额外的应用程序，这就是 MySQL 监控器。

在下一节中，你将学习手动启动 MySQL 并执行一些操作以熟悉系统。

## 测试你的 MySQL 安装

在本节中，你将通过控制窗口在命令行中启动并使用 MySQL 工具。在 PHP 中使用 MySQL 时，你将使用相同类型的命令，只是在 PHP 代码的上下文中。并利用本节的信息熟悉你以后在书中将处理的命令类型和响应。

## 启动 MySQL

要手动启动 MySQL，请按照以下步骤操作。

1. 打开 DOS 提示符或控制窗口（取决于你的 Windows 版本，它可能被称为其中一种）。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_9_0.png)

2. 在提示符下，输入 `cd c:\mysql\bin` 并按回车键。

   > **注意**：如果你将 MySQL 安装在不同的目录，请替换第 2 步中命令的目录名称。

3. 在提示符下，输入 `mysqld-opt` 并按回车键。

现在 MySQL 进程将在后台运行。你现在可以连接到 MySQL 并创建数据库和表。

# 创建测试数据库

在继续操作之前，你应该了解以下内容：

- 数据库是表（tables）的集合。
- 表（table）包含一组记录（records），也称为行（rows）。
- 所有记录具有相同数量的字段（fields）。
- 每个字段都对某条数据进行分类。

在这一节中，你将攻克第一个元素并创建一个数据库。要使用的工具是 `mysqladmin` 程序，它允许你从命令行管理 MySQL。

1. 在提示符下，输入 `mysqladmin create testDB` 并按回车键。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_10_0.png)

接下来，你将为 `testDB` 数据库添加表。

# 创建测试表

在这一节中，你将在上一节创建的数据库中创建一个表。要使用的工具是 `mysql` 程序，它允许你从命令行在 MySQL 数据库系统内部进行工作。

1. 在提示符下，输入 `mysql` 并按回车键。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_10_1.png)

当 MySQL Monitor 启动时，它会提供自己的提示符。在该提示符（`mysql>`）处，你将输入用于创建表、解释表、插入数据、选择数据等的命令。习惯用分号（`;`）结束你的命令，因为它是一个常用的指令终止符，在 PHP 中同样使用。

现在你已经连接到 MySQL Monitor，你需要告诉它要使用哪个数据库。

2. 在提示符下，输入 `use testDB;` 并按回车键。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_11_0.png)

如果数据库存在且你有权限访问它，MySQL Monitor 将响应 `Database changed`。

是时候创建一个表了。这张表将有一个 ID 列和一个文本 text 列。

> **注意**：关于表的具体细节的更多信息，请参见附录 D，“基础 MySQL 参考”。

3. 在提示符下，输入 `create table test_table (test_id int, note text);` 并按回车键。该语句创建了一个名为 `test_table` 的表。在表中，它创建了一个类型为整数的 `test_id` 列。它还创建了一个类型为文本的 `note` 列。

4. 在提示符下，输入 `insert into test_table values('1', 'This is a note.');` 并按回车键。

5. 在提示符下，输入 `insert into test_table values('2', 'Another note.');` 并按回车键。

6. 在提示符下，输入 `insert into test_table values('3', 'Third note.');` 并按回车键。

7. 在提示符下，输入 `select * from test_table;` 并按回车键。

   ```
   mysql> show tables;
   +-----------------+
   | Tables_in_testDB |
   +-----------------+
   | test_table      |
   +-----------------+
   1 row in set (0.00 sec)

   mysql> use testDB;
   Database changed

   mysql> create table test_table (test_id int, note text);
   Query OK, 0 rows affected (0.01 sec)

   mysql> insert into test_table values('1', 'This is a note.');
   Query OK, 1 row affected (0.00 sec)

   mysql> insert into test_table values('2', 'Another note.');
   Query OK, 1 row affected (0.00 sec)

   mysql> insert into test_table values('3', 'Third note.');
   Query OK, 1 row affected (0.00 sec)

   mysql> select * from test_table;
   +---------+-------------------+
   | test_id | note              |
   +---------+-------------------+
   | 1       | This is a note.   |
   | 2       | Another note.     |
   | 3       | Third note.       |
   +---------+-------------------+
   3 rows in set (0.00 sec)

   mysql> drop database testDB;
   Query OK, 1 row affected (0.00 sec)
   ```

结果现在显示 `test_id` 为 3 的行作为第一行。并没有另一个选项 `asc`，它代表升序。升序是默认设置。

## 在 Linux/UNIX 上安装 MySQL

要下载 Linux 的 MySQL 发行版，请访问 MySQL 网站 (`http://www.mysql.com/`) 并点击“Downloads”链接。这是获取 Linux/Unix 发行文件和公告的正确位置。

发行文件遵循命名规范，即“mysql”后跟版本号，然后是压缩类型（`.tar.gz`、`.tar.Z` 和 `.zip`）。在编写时，当前版本为 4.0.0，我更倾向于使用 `.tar.gz` 文件，因此本节使用的示例文件是 `mysql-4.0.0.tar.gz`。

> **注意**：源码发行版适用于大多数 UNIX 变体，但如果你有任何疑虑，请阅读 MySQL 网站上的 MySQL 文档，以找到你的特定操作系统更合适的文件集。

一旦你将选择的文件下载到硬盘上，请按照以下步骤构建 MySQL 的基础版本。

1. 输入 `cp mysql-4.0.0.tar.gz /usr/local/` 并按回车键，将 MySQL 安装文件复制到 `/usr/local/` 目录。

   > **注意**：你可以将 MySQL 放在文件系统中的任何位置，例如 `/usr/local/bin/` 或 `/opt/`。只需将你的路径替换这些说明中指定的路径即可。

2. 输入 `cd /usr/local` 并按回车键进入 `/usr/local`。

3. 输入 `gunzip mysql-4.0.0.tar.gz` 并按回车键解压 MySQL 安装文件。

4. 输入 `tar -xvf mysql-4.0.0.tar` 并按回车键提取文件。这将创建一个目录，并返回提示符。父目录将是 `/usr/local/mysql-4.0.0/`。

5. 输入 `cd mysql-4.0.0` 并按回车键进入父目录。

6. 输入以下内容并按回车构建 MySQL：

   `./configure --prefix=/usr/local/mysql-4.0.0`

7. 输入 `make` 并按回车键。安装过程的第二步将在你的屏幕上产生许多行输出。完成后，你将返回提示符。

8. 输入 `make install` 并按回车键。安装过程的最后一步将再次在你的屏幕上产生许多行输出。完成后，你将返回提示符。

如果安装过程到此为止产生任何错误，请重新运行过程或检查 MySQL 网站上的任何针对特定系统的说明。在下一节中，你将在首次启动之前对 MySQL 配置进行一些微调。

## 在 Linux/UNIX 上配置 MySQL

要运行基础安装的 MySQL，你需要做的第一件事是创建一个 mysql 用户和组，然后解压发行包。

1. 在提示符处，输入 `groupadd mysql`
2. 在提示符处，输入 `useradd -g mysql`
3. 在提示符处，输入 `cd /usr/local`

你可以在任何目录下安装 MySQL。如果你没有使用上述示例中的 `/usr/local/`，请务必适当修改后续命令。

4. 在提示符处，输入 `gunzip < /path/to/mysql-VERSION-OS.tar.gz | tar xvf -`
5. 要创建一个较短的链接，输入 `ln -s mysql-VERSION-OS mysql`
6. 输入 `cd mysql` 切换目录

解压发行包后，`README` 和 `INSTALL` 文件将引导你完成所选 MySQL 版本的剩余安装过程。通常情况下，将使用以下一系列命令：

1. 输入 `scripts/mysql_install_db` 来运行 MySQL 安装脚本。
2. 输入 `chown -R root /usr/local/mysql` 来更改 mysql 目录的所有权。
3. 输入 `chown -R mysql /usr/local/mysql/data` 来更改 mysql/data 目录的所有权。
4. 输入 `chgrp -R mysql /usr/local/mysql` 来更改 mysql 目录的组。
5. 输入 `chown -R root /usr/local/mysql/bin` 来更改 mysql/bin 目录的所有权。

如果你在安装 MySQL 过程中遇到任何问题，你应该首先查看的是 MySQL 手册中的“问题与常见错误”（Problems and Common Errors）章节，地址位于 `http://www.mysql.com/doc/en/Problems.html`。常见问题包括：

- 权限错误导致无法启动 MySQL 守护进程。如果是如此，请确保已更改所有者和组以匹配安装说明中指定的那些。
- 如果在连接 MySQL 时看到“Access denied”消息，请确保你使用的是正确的用户名和密码。
- 如果看到“Can't connect to server”消息，请确保 MySQL 守护进程正在运行。

在下一节中，你将学习如何启动 MySQL 并执行一些操作以熟悉系统。

## 测试你的 MySQL 安装 (Linux/UNIX)

在本节中，你将通过控制台窗口中的命令行启动并使用 MySQL 工具。在 PHP 中使用 MySQL 时，你将执行相同类型的命令，只不过是在 PHP 代码的上下文中。使用本节中的信息来熟悉你以后在书中处理的命令类型和响应。

## 启动 MySQL

1. 如果你不在该目录，输入 `cd /usr/local/mysql` 并按回车进入 MySQL 父目录。
2. 输入 `bin/safe_mysqld` 并按回车启动 MySQL 进程。

MySQL 进程现在将在后台运行，你可以连接到 MySQL 并创建数据库和表。

# 创建测试数据库 (Linux/UNIX)

在继续之前，你应该了解以下内容：

- 数据库是表的集合。
- 表包含一组记录，也称为行。
- 所有记录都具有相同数量的字段。
- 每个字段对某条数据进行分类。

在本节中，你将攻克第一个元素并创建一个数据库。使用的工具是 `mysqladmin` 程序，它允许你从命令行管理 MySQL。

1. 在提示符处，输入 `bin/mysqladmin create testDB` 并按回车。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_16_0.png)

如你所示，名为 testDB 的数据库已经创建。接下来，你将为该数据库添加一个表。

# 创建测试表 (Linux/UNIX)

在本节中，你将在上一节创建的数据库中创建一个表。使用的工具是 `mysql` 程序，它允许你从命令行在 MySQL 数据库系统中进行工作。

1. 在提示符处，输入 `bin/mysql` 并按回车。

   ```
   mysql> // create test123
   Database created
   Welcome to the MySQL monitor. Commands end with ';'.
   Your MySQL connection id is 1 to server version: 4.0.0
   Type 'help;' or '\h' for help. Type '\c' to clear the buffer.

   mysql> use test
   Database changed
   mysql>
   ```

MySQL 监控器将启动。MySQL 监控器提供了自己的提示符。在该提示符（`mysql>`）下，你将输入用于创建表、解释表、插入数据、选择数据的命令。习惯用分号（`;`）结束你的命令，因为这是一个常见的指令终止符，在 PHP 中也会使用。

现在你已经连接到 MySQL 监控器，你需要告诉它要使用哪个数据库。

2. 在提示符处，输入 `use testDB;` 并按回车。

如果数据库存在且你有权限访问它，MySQL 监控器将响应 `Database changed`。

现在是时候创建一个测试表了。这张表将有一个用于 ID 号的列和一个用于某些文本的列。

关于创建表的细节更多信息，请参阅附录 D，“Basic MySQL Reference”。

3. 在提示符处，输入 `create table test_table (test_id int, test_note text);` 并按回车。此语句创建了一个名为 `test_table` 的表。在表中，它创建了一个类型为 `int`（整数）的 `test_id` 列。它还创建了一个类型为 `text` 的 `test_note` 列。

   ```
   mysql> create table test_table (test_id int, test_note text);
   Query OK, 0 rows affected (0.01 sec)
   ```

MySQL 监控器将响应 `Query OK`。它将告诉你影响了多少行以及完成该任务花了多少时间。

4. 要验证表的创建，输入 `show tables;` 并按回车。

   ```
   mysql> show tables;
   +-----------------+
   | Tables_in_testdb |
   +-----------------+
   | test_table      |
   +-----------------+
   1 row in set (0.00 sec)
   ```

MySQL 监控器将响应当前数据库中的所有表。

5. 要验证字段名和类型，使用 `explain test_table;` 并按回车。

   ```
   mysql> explain test_table;
   +---------+------+------+-----+---------+-------+
   | Field   | Type | Null | Key | Default | Extra |
   +---------+------+------+-----+---------+-------+
   | test_id | int  | NO   |     | NULL    |       |
   | test_note| text | YES  |     | NULL    |       |
   +---------+------+------+-----+---------+-------+
   2 rows in set (0.00 sec)
   ```

现在是向表中插入几行数据了。第一行将有一个 ID 为 1，备注将是“This is a note.”

6. 要插入此行，输入 `insert into test_table values('1', 'This is a note.');` 并按回车。

   ```
   mysql> insert into test_table values('1','This is a note.');
   Query OK, 1 row affected (0.01 sec)
   ```

MySQL 监控器将响应 `Query OK`。它将告诉你影响了多少行以及完成该任务花了多少时间。

7. 插入另一行，输入 `insert into test_table values('99', 'Look! Another note.');` 并按回车。

关于向表中插入数据的细节更多信息，请参阅附录 D，MySQL Reference。

8. 现在你的表中有一些数据，即使只有两行，也要熟悉选择数据。保持 MySQL 监控器开启，因为你将在下一节中继续使用它。

## 从测试表中选择数据

`SELECT` 命令非常强大，可能是你与 PHP 和 MySQL 工作时最常用的命令。你可以在附录 D，MySQL Reference 中找到更多关于 `SELECT` 的信息，但我们将进行简单的选择。

1. 在提示符处，输入 `select * from test_table;` 并按回车。

   ```
   mysql> select * from test_table;
   +---------+----------------------+
   | test_id | test_note            |
   +---------+----------------------+
   | 1       | This is a note.      |
   | 99      | Look! Another note.  |
   +---------+----------------------+
   2 rows in set (0.01 sec)
   ```

   ![](img/bc248f3d24697d1afbacee37b9c4d229_19_0.png)

此命令简单地从 `test_table` 表中的所有行选择所有字段（这就是 `*` 的作用），并将数据以良好的格式返回到屏幕上。MySQL 监控器告诉你返回了多少行以及查询运行花了多少时间。

为结果添加一些排序。尝试让结果按 ID 号排序——最大的数字排在前。

2. 在提示符处，输入 `select * from test_table order by test_id desc;` 并按回车。

   ```
   mysql> select * from test_table order by test_id desc;
   +---------+----------------------+
   | test_id | test_note            |
   +---------+----------------------+
   | 99      | Look! Another note.  |
   | 1       | This is a note.      |
   +---------+----------------------+
   2 rows in set (0.00 sec)
   ```

结果现在显示 `test_id` 为 99 的行作为表格的第一行。`desc` 代表降序。另一个选项是 `asc`，代表升序。升序是默认顺序。

在下一章中，你将安装 Apache Web 服务器，并向开发动态的、数据库驱动的 Web 网站迈一步！

## 概述

由于它是目前最流行的 Web 服务器，你可能认为 Apache 是一个复杂的软件，但其实并不困难。在本章中，你将学习如何执行以下操作：

- 在 Windows 或 Linux 上安装 Apache
- 连接到你新的 Web 服务器

## 在 Windows 上安装 Apache

在 Windows 上安装 Apache 是一项简单的任务，这很大程度上归功 Apache Group 分发的安装向导。无论你使用的是 Windows 95、98、ME、2000、XP 还是 NT，安装预编译二进制文件无疑都是最佳选择，且所有 Windows 版本均使用同一个安装文件。

能够在 Windows 95/98/ME/XP 等消费级操作系统上使用 Apache 并不意味着你应该这样做，至少在生产环境中并非如此。简单来说，在 Windows 操作系统上运行任何 Web 服务器在速度、稳定性和安全性方面都不如在 Linux/UNIX 机器上。然而，在基于 Windows 的操作系统上安装和配置 Web 服务器是完全可以的，而且大多数用户都能实现。

> **注意**：Apache Group 也分发 Windows 版 Apache 的源代码，以备你需要自行编译代码。然而，该过程超出了本书的范围！

要下载 Windows 版 Apache 分发包，请访问 Apache Server 网站（`http://httpd.apache.org/`）并点击“Download”链接。进入下载区域后，点击“binaries”然后点击“win32”。这将进入 Windows 分发文件和公告的正确区域。该下载区域的直接 URL 为 `http://www.apache.org/dist/httpd/binaries/win32`。

分发文件遵循命名规范，格式为“apache”后跟版本号，然后是 `-win32-x86-no_src.exe`。截至本文撰写时，当前版本为 1.3.26，因此本节使用的示例文件是 `apache_1.3.26-win32-x86-no_src.exe`。一旦你将安装文件下载到硬盘，接下来的步骤将引导你完成安装向导：

1. 双击名为 `apache_1.3.26-win32-x86-no_src.exe` 的文件。安装程序将启动，安装向导将开始。点击 Next 继续。
2. 阅读屏幕上的许可信息，选择 I Accept（单选按钮），然后点击 Next。阅读屏幕上的 Apache 通用信息，然后点击 Next。下一个屏幕要求你填写有关服务器的一些详细信息：网络域名、服务器名称和管理员电子邮件地址。
3. 选择 Run As Service For All Users 按钮并点击 Next。选择 Complete set-up type（完整安装类型），点击 Next。接受默认的目标文件夹，然后点击 Next。

   > **注意**：如果你选择更改 Apache 安装文件的目标文件夹，请相应地调整书中后续的说明和路径。

4. 在下一页选择 Install，将开始最后的安装序列。序列完成后，你将看到确认屏幕。点击 Finish 完成安装并关闭安装程序。

此时，所有必要的 Apache 文件均已安装，你的 Windows 开始菜单中还有了一组方便的快捷方式，称为 Apache HTTP Server。在继续配置服务器之前，为了运行基础测试，请从 Windows 开始菜单选择 Program Files -> Apache HTTP Server -> Configure Apache Server -> Test Configuration。这将启动一个控制台窗口并显示安装成功。

如果你在此处遇到任何错误，请重新运行安装程序。在下一节中，你将在首次启动 Apache 之前对 Apache 配置文件进行细微更改。

## 在 Windows 上配置 Apache

要运行 Apache 的基础安装，你唯一需要更改的是服务器名称，你可能可能在安装向导期间已经完成了这一步。然而，如果你为服务器名称输入了虚拟信息，或者希望修改基础配置的任何其他部分，现在就是操作的时候。

Apache 的主配置文件名为 `httpd.conf`，它位于 Apache 安装目录下的 `conf` 目录中。

## 启动并连接到 Apache

要首次启动 Apache 服务器，请从 Windows 开始菜单选择 Program Files -> Apache HTTP Server -> Start Apache In Console。这将启动一个控制台窗口。

## 在 Linux/UNIX 上安装 Apache

要下载 Linux 的 Apache 发行版，请访问 Apache 服务器网站 (`http://httpd.apache.org/`) 并点击“Download”（下载）链接。这是获取 Linux/Unix 发行文件和公告的正确位置。

发行文件遵循命名规范，即“apache”后跟版本号，然后是压缩类型（`.tar.gz`、`.tar.Z` 和 `.zip`）。在编写时，当前版本为 1.3.26，我更倾向于使用 `.tar.gz` 文件，因此本节使用的示例文件是 `apache_1.3.26.tar.gz`。

> **注意**：源码发行版适用于大多数 UNIX 变体，但如果你有任何疑虑，请阅读 Apache 网站上的 Apache 文档，以找到你的特定操作系统更合适的文件集。

一旦你将选择的文件下载到硬盘上，请按照以下步骤构建 Apache 的基础版本。

1. 输入 `cp apache_1.3.26.tar.gz /usr/local/` 并按回车键，将 Apache 安装文件复制到 `/usr/local/` 目录。

   > **注意**：你可以将 Apache 放在文件系统中的任何位置，例如 `/usr/local/bin/` 或 `/opt/`。只需将你的路径替换这些说明中指定的路径即可。

2. 输入 `cd /usr/local` 并按回车键进入 `/usr/local`。
3. 输入 `gunzip apache_1.3.26.tar.gz` 并按回车键解压 Apache 安装文件。
4. 输入 `tar -xvf apache_1.3.26.tar` 并按回车键提取文件。这将创建一个目录，并返回提示符。父目录将是 `/usr/local/apache_1.3.26/`。
5. 输入 `cd apache_1.3.26` 并按回车键进入父目录。
6. 输入以下内容并按回车构建 Apache：

   `./configure --prefix=/usr/local/apache_1.3.26 --enable-module=so`

7. 输入 `make` 并按回车键。安装过程的第二步将在你的屏幕上产生许多行输出。完成后，你将返回提示符。
8. 输入 `make install` 并按回车键。安装过程的最后一步将再次在你的屏幕上产生许多行输出。完成后，你将返回提示符。

如果安装过程到此为止产生任何错误，请重新运行过程或检查 Apache 网站上的任何针对特定系统的说明。在下一节中，你将在首次启动之前对 Apache 配置进行一些微调。

## 在 Linux/UNIX 上配置 Apache

要运行基础安装的 Apache，你唯一修改的是服务器名称，它位于名为 `httpd.conf` 的主配置文件。该文件位于 Apache 安装目录下的 `conf` 目录中。因此，如果你在 `/usr/local/apache_1.3.26/` 中安装了 Apache，配置文件将是 `/usr/local/apache_1.3.26/conf/httpd.conf`。

要修改基础配置（最重要的服务器名称），请用文本编辑器打开 `httpd.conf` 文件并寻找名为“Section 2: 'Main' server configuration”的标题。你会发现两个重要的文本段。

1. 将 `ServerAdmin` 的值更改为你的电子邮件地址。
2. 将 `ServerName` 的值更改为你的服务器名称。

   > **注意**：你可以使用自定义主机名并希望它们生效，但如果你想让它们在你自己的机器上运行，必须将它们添加到本地 hosts 文件中。
   > 如果你通过 IP 地址访问该站点（例如 `http://123.45.67.89/`），请忽略此项。
   > `127.0.0.1` 是 TCP/IP 回环地址。

## 启动并连接到 Apache (Linux/UNIX)

要启动 Apache 服务器，请在提示符处输入 `/usr/local/apache_1.3.26/bin/apachectl start` 并按回车。

## 概述

建议使用 Apache Web 服务器并手动安装 PHP。如果您选择使用不同的 Web 服务器安装 PHP，或者使用了其他方法，请阅读您所选软件包含的安装说明。

要下载 Windows 版 PHP 二进制发行包，请访问 PHP 网站的下载页面：`http://www.php.net/downloads.php`。

1. 在“Windows binaries”部分，点击“PHP 4.x.zip package”链接，其中“x.x”代表版本号。目前 Windows 版本为 4.2.1，后续所有的安装说明都将基于此版本。
2. 将文件下载到您的系统后，双击运行名为 `php-4.2.1-win32.zip` 的文件。您选择解压缩程序（如 WinZip 或 PKZip）将打开此文件。
3. 将文件解压到硬盘，并保持路径完整。这将创建一个 `C:\php-4.2.1-Win32` 目录。

您现在已经拥有了所有的 PHP 发行文件，只需要移动其中的几个文件。

> **注意**：如果您更改了安装目录名称，请务必在本章剩余的指令中替换您的新目录名称。

1. 使用 Windows 资源管理器（无论您习惯哪种操作方式），进入 `C:\php-4.2.1-Win32` 目录。
2. 将 `php.ini-dist` 文件重命名为 `php.ini`并将此文件移动到 `C:\WINDOWS\` 或您通常放置 `.ini` 文件的位置。
3. 将 `msvcrt.dll` 和 `php4ts.dll` 移动到 `C:\WINDOWS\SYSTEM\` 或您通常放置 `.dll` 文件的位置。

> **注意**：您的系统中可能已经有一个 `msvcrt.dll` 副本。如果在尝试移动 `msvcrt.dll` 时收到警告，可以忽略该警告且不拷贝文件。只要系统中存在该文件，您就不一定需要 PHP 发行包中的那个。

4. 要让基础版 PHP 与 Apache 工作，您需要对 Apache 配置文件进行一些微调。

## 配置 Apache 使用 PHP

您可以将 PHP 作为 CGI 二进制文件或 Apache 模块安装。PHP 目前的建议是使用模块版本，因为它提供了更高的性能和一些额外的功能。然而，根据您的操作系统的不同，在使用模块时可能会在高级功能上遇到一些冲突。此外，使用 CGI 版本而不是模块将允许您创建更安全的虚拟主机，每个虚拟主机都有自己的 CGI 可执行文件，从而允许 PHP 以指定用户的身份运行，而不是以默认的 Apache 进程所有者运行。

在本节中，您可以选择想要使用的版本，甚至可以尝试两个配置过程，以便更好地理解这些内容的工作原理。无论您选择何种配置，您都能完成书中的所有练习。

## PHP 的 CGI 版本

要配置 Apache 使用 CGI 版本的 PHP，您只需要对 Apache 配置文件 `httpd.conf` 文件进行几处修改，该文件位于 Apache 安装目录下的 `conf` 目录中。

1. 使用文本编辑器（如记事本）打开 `httpd.conf` 文件。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_30_0.png)

2. 寻找类似于图中所示的文本段。
3. 添加如下行：

   `ScriptAlias /php/ "C:/php-4.2.1-win32/"`

   ![](img/bc248f3d24697d1afbacee37b9c4d229_30_1.png)

接下来，您需要向 `httpd.conf` 文件中添加一条指令来定义 PHP 文件使用的扩展名。常见的扩展名是 `.php` 和 `.phtml`，或者您可以使用任何您喜欢的名称。

![](img/bc248f3d24697d1afbacee37b9c4d229_30_2.png)

4. 寻找类似于图中所示的文本段。
5. 添加两行：

   `AddType application/x-httpd-php .phtml .php`
   `AddType application/x-httpd-php-source .phps`

   ```
   # 指令允许您在不实际编辑文件的情况下调整类型，或者
   # 通过排列整个文件来保存类型。
   # AddType application/x-tar .gz
   # AddType application/x-httpd-php .php
   # AddType application/x-httpd-php-source .phps
   ```

对 `httpd.conf` 文件进行最后一次修改，您就完成了。

```
# Action 允许您定义执行脚本包装器的媒体类型
# 使用映射扩展名；这消除了重复 MIME 类型的需要。
# Format: Action media/type /cgi-script
# Format: Action media/type /cgi-script-redirection
# Format: Action media/type /cgi-script-modification
```

6. 寻找类似于图中所示的文本段。
7. 添加 `Action application/x-httpd-php /php/php.exe`

   ```
   # Action 允许您定义执行脚本包装器的媒体类型
   # 使用映射扩展名；这消除了重复 MIME 类型的需要。
   # Format: Action media/type /cgi-script
   # Format: Action media/type /cgi-script-redirection
   # Format: Action media/type /cgi-script-modification

   Action application/x-httpd-php /php/php.exe
   ```

8. 保存并关闭 `httpd.conf` 文件。

此修改告诉 Apache，当请求扩展名为 `.php` 或 `.phtml` 的文件时，Apache 应先通过 PHP 解析器运行该文件，然后再输出到浏览器。

## PHP 的 Apache 模块

要配置 Apache 使用模块版本，您必须移动一个 PHP 组件并对 Apache 配置文件 `httpd.conf` 文件进行一些修改，该文件位于 Apache 安装目录的 `conf` 目录下。

1. 在 `C:\php-4.2.1-win32` 中应该有一个名为 `php4ts.dll` 的文件。将该文件移动到 `C:\Windows\system`（Windows 98/Me）或 `C:\WINNT\system32`（Windows NT/2000）。
2. 使用文本编辑器（如记事本）打开 `httpd.conf` 文件。
3. 寻找类似于图中所示的文本段。

   ```
   # Dynamic Shared Object (DSO) Support
   # To be able to use the functionality of a module which was built as a DSO you
   # have to place corresponding `LoadModule' lines at this location so the
   # directives contained in it are actually available _before_ they are used.
   # Statically compiled modules (those listed by `httpd -l') do not need
   # to be loaded here.
   #
   # Example:
   # LoadModule foo_module modules/mod_foo.so
   #
   LoadModule isapi_module modules/mod_isapi.so
   LoadModule authn_basic_module modules/mod_authn_basic.so
   LoadModule speling_module modules/mod_speling.so
   LoadModule status_module modules/mod_status.so
   LoadModule rewrite_module modules/mod_rewrite.so
   LoadModule mime_module modules/mod_mime.so
   LoadModule expires_module modules/mod_expires.so
   LoadModule digest_module modules/mod_digest.so
   LoadModule proxy_module modules/mod_proxy.so
   LoadModule headers_module modules/mod_headers.so
   LoadModule security_module modules/mod_security.so
   LoadModule filter_module modules/mod_filter.so
   LoadModule unique_id_module modules/mod_unique_id.so
   LoadModule setenvif_module modules/mod_setenvif.so
   ```

4. 添加如下行：

   `LoadModule php4_module "C:/php-4.2.1-win32/sapi/php4apache2.dll"`

   ![](img/bc248f3d24697d1afbacee37b9c4d229_33_0.png)

接下来，你必须向 `httpd.conf` 文件中添加一条指令来定义使用 PHP 文件的扩展名。常见的扩展名是 `.php` 和 `.phtml`，你也可以使用任何喜欢的扩展名。

![](img/bc248f3d24697d1afbacee37b9c4d229_33_1.png)

5. 查找如图所示的文本区域。
6. 添加以下两行：

   `AddType application/x-httpd-php .phtml .php`
   `AddType application/x-httpd-php-source .phps`

   ![](img/bc248f3d24697d1afbacee37b9c4d229_33_2.png)

7. 保存并关闭 `httpd.conf` 文件。

此最终修改告诉 Apache，每当请求扩展名为 `.php` 或 `.phtml` 的文件时，Apache 都应该在向 Web 浏览器发送任何输出之前，利用 PHP 解析器的模块版本。

# 测试 PHP 安装

现在你已经对 `httpd.conf` 文件完成了所有的修改——无论使用何种配置方法——你可以使用在第 2 章中学学的方法重启 Apache。为了测试 Apache 和 PHP 是否协同工作，你将创建一个简单的 PHP 脚本来测试安装情况。PHP 脚本和其他文件（HTML、图像等）应该放置在 Web 服务器的文档根目录下。对于 Apache 来说，文档根是 Apache 安装目录下的 `htdocs` 目录。

1. 在文本编辑器中打开一个新文件并输入以下内容：

   ```php
   <?php phpinfo(); ?>
   ```

2. 将文件保存为 `phpinfo.php` 并将其放置在 Web 服务器的文档根目录下。

   > **注意**：务必确保你的文件扩展名为 `.php` 或 `.phtml`（或另一个为 PHP 配置的扩展名）。Windows 文本编辑器经常会在文件名末尾添加 `.txt` 扩展名。如果这种情况发生在你身上，你的脚本将不会被 PHP 解析，而仅会被文本。因此请留意你的扩展名！

   ![](img/bc248f3d24697d1afbacee37b9c4d229_34_0.png)

3. 打开浏览器并输入 `http://127.0.0.1/phpinfo.php`

`phpinfo.php` 脚本的输出应该是一个充满系统和环境信息的长页面。当你尝试弄清楚可用功能时，这些信息非常有帮助。如果你浏览结果，你会发现预装了以下扩展（以及许多其他扩展）：

- 正则表达式支持
- 动态库支持
- 内部需求支持
- Perl 兼容的正则表达式支持
- ODBC 支持
- Session 支持
- XML 支持
- MySQL 支持

预装这些扩展意味着要使这些功能可用，不需要额外的 `.dll` 文件。有关获取用于额外 PHP 功能的 `.dll` 文件的更多信息，请参见附录 A，“附加配置选项”。

你现在准备好进入第二部分“PHP 编程基础”，并学习 PHP 语言的基础知识了。

# 在 Linux 上安装 PHP

此节将向你展示如何在 Linux 上作为 Apache 的动态模块安装 PHP。通过构建动态而非静态模块，你可以升级或重新编译 PHP，而无需重新编译 Apache。例如，在本节中，你所做的只是为 MySQL 支持配置 PHP。如果你在稍后的阶段决定需要额外的选项（例如图像创建函数或额外的加密函数），你只需要更改 PHP 的配置命令，重新编译模块并重启 Apache。Apache 的安装不需要额外的更改，因为一个 PHP 模块文件将替换另一个。

要下载 PHP 源码发行包，请访问 PHP 网站的下载页面：`http://www.php.net/downloads.php`。

1. 从“Complete Source Code”（完整源代码）部分开始，点击“PHP 4.x.x”链接。“x.x”指的是版本。当前的源码版本为 4.2.1，下面的步骤将使用该版本号，尽管你的版本号（以及因此文件名）可能会不同。
2. 下载下载到你的系统后，输入 `cp php-4.2.1.tar.gz /usr/local/` 并按回车，将 PHP 源码发行包拷贝到 `/usr/local/` 目录。

   > **注意**：你可以将 PHP 放在文件系统的任何地方，例如 `/usr/local/bin/` 或 `/opt/` 或你任何想放置文件的地方。只需用你的路径替换这些说明中的路径即可。

3. 输入 `cd /usr/local/` 并按回车进入 `/usr/local/`。
4. 输入 `gunzip php-4.2.1.tar.gz` 并按回车解压源码文件。
5. 输入 `tar -xvf php-4.2.1.tar` 并按回车提取源码文件。这将创建一个目录结构，然后让你回到提示符状态。父目录将是 `/usr/local/php-4.2.1/`。
6. 输入 `cd /usr/local/php-4.2.1/` 并按回车进入目录。
7. 输入 `./configure --with-mysql` 并按回车运行配置脚本。
8. 输入 `make` 并按回车编译 PHP 模块。
9. 输入 `make install` 并按回车安装 PHP 模块。
10. 重启 Apache 以应用更改。

# 第 4 章：混合 PHP 和 HTML

## 概述

现在你已经拥有了一个可以工作的开发环境，PHP、Apache 和 MySQL 在你的机器上良好运行，现在是时候深入研究 PHP 语言了。在本章中，你将学习如何进行以下操作：

- 识别并使用不同类型的 PHP 开始和结束标签
- 在源代码中混合 PHP 和 HTML
- 在脚本中转义特殊字符以产生有效的输出

## PHP 是如何被解析的

假设你有一个文件，文件中包含一些 HTML 和一些 PHP 代码。假设一个扩展名为 `.php` 的 PHP 文档，其工作原理如下：

1. Web 浏览器请求一个 `.php` 后缀的文件。
2. Web 服务器发送出：“嘿！有人想要一个 PHP 文件。需要其他程序来处理它，”并将请求发送给 PHP 解析器。
3. PHP 解析器找到所请求的文件，并扫描其中的 PHP 代码。
4. 当 PHP 解析器找到代码时，它会执行该代码并将生成的输出（如果有）放置在原代码占据的位置。
5. 这个新的输出文件被发送回 Web 服务器。
6. Web 服务器将其发送给 Web 浏览器。
7. Web 浏览器显示输出。

由于 PHP 代码是由服务器解析的，这种执行方式被称为服务器端执行。当代码由浏览器执行（如 JavaScript）时，它是客户端执行。

为了将 PHP 代码与 HTML 结合，PHP 解析器会识别这一点，你将学习如何使用 PHP 开始和结束标签来实现。

## PHP 开始和结束标签

PHP 解析器识别几种不同类型的 PHP 开始和结束标签。它会尝试忽略这些标签之间的任何内容，所以最好确保内容是有效的！请学习表 4.1 以了解 PHP 解析器识别的三组主要的开始和结束标签。

| 表格 4.1：基础 PHP 开始和结束标签 | 开启标签 | 结束标签 |
| :--- | :--- | :--- |
| 标准标签 | `<?php` | `?>` |
| 短标签 | `<?` | `?>` |
| ASP 风格标签 | `<%` | `%>` |

接下来，你将使用一组会执行的标签。

1. 在文本编辑器中打开一个新文件。
2. 输入以下代码，它使用了第一个标签：

   ```php
   <?php
   echo "<P>This is a test using the first tag.</P>";
   ?>
   ```

3. 输入以下代码，它使用了第二个标签：

   ```php
   <?
   echo "<P>This is a test using the second tag.</P>";
   ?>
   ```

4. 输入以下代码，它使用了第三个标签：

   ```php
   <%
   echo "<P>This is a test using the third tag.</P>";
   %>
   ```

5. 将新文件保存命名为 `tags.php`。
6. 将此文件放在你的 Web 服务器的文档根目录下。
7. 打开浏览器并输入 `http://127.0.0.1/tags.php`

> **注意**：在执行本书中的示例时，如果你在外部 Web 服务器上使用 PHP，请将 URL 中的 `127.0.0.1` 替换为服务器域名。

8. 在下一节中，你将学习将 PHP 放在 HTML 内部并不可怕。

## 代码共存

在上一节中，你的文件由三部分 PHP 代码组成，每个部分都打印了一些 HTML 文本。在本节中，你将创建一个在 HTML 中间包含 PHP 代码的脚本，你将学习这两种类型的代码如何共存。

1. 在文本编辑器中打开一个新文件。
2. 输入以下 HTML：

   ```html
   <HTML>
   <HEAD>
   <TITLE>My First Script</TITLE>
   </HEAD>
   <BODY>
   ```

3. 输入以下 PHP 代码：

   ```php
   <?php
   echo "<P>Hello World! I'm using PHP!</P>";
   ?>
   ```

4. 添加更多 HTML 以使文档有效：

   ```html
   </BODY>
   </HTML>
   ```

5. 将文件保存命名为 `firstscript.php`。
6. 将此文件放在你的 Web 服务器的文档根目录下。
7. 打开浏览器并输入 `http://127.0.0.1/firstscript.php`
8. 在你的 Web 浏览器中查看此文档的源代码。

注意 HTML 源代码只包含 HTML 代码。这块 PHP 被执行了：

```php
<?php
echo "<P>Hello World! I'm using PHP!</P>";
?>
```

此区块包含三个元素：命令 (`echo`)、字符串 (`<P>Hello World! I'm using PHP!</P>`) 和指令终止符 (`;`)。

熟悉 `echo`，因为它可能是你最常使用的命令。`echo` 语句用于输出信息——在这种情况下，用于打印此 HTML 输出：

```html
<P>Hello World! I'm using PHP!</P>
```

下一节将讨论一个常见的错误，希望你能避免它。

## 指令终止符的重要性

指令终止符，也称为分号 (`;`)，在命令末尾是绝对要求的。指令终止符告诉 PHP 解析器：“我已经处理完这个了，尝试下一个。”

如果你不用分号结束命令，PHP 解析器将变得困惑，你的代码将显示错误。接下来的步骤将向你展示如何产生这些错误之一，更重要的是如何修复它。

1. 在文本编辑器中打开一个新文件。
2. 输入以下 HTML：

   ```html
   <HTML>
   <HEAD>
   <TITLE>Making an Error</TITLE>
   </HEAD>
   <BODY>
   ```

3. 输入以下 PHP 代码：

   ```php
   <?php
   echo "<P>I am trying to produce an error</P>"
   echo "<P>Was successful?</P>";
   ?>
   ```

4. 添加更多 HTML 以使文档有效：

   ```html
   </BODY>
   </HTML>
   ```

5. 将文件保存命名为 `errorscript.php`。
6. 将此文件放在你的 Web 服务器的文档根目录下。
7. 打开浏览器并输入 `http://127.0.0.1/errorscript.php`

> **注意**：在执行本书中的示例时，如果你在外部 Web 服务器上使用 PHP，请将 URL 中的 `127.0.0.1` 替换为服务器域名。

PHP 解析器不喜欢这个：

```php
<?php
echo "<P>I am trying to produce an error</P>"
echo "<P>Was successful?</P>";
?>
```

这个错误也有简单的修复方法：

1. 打开 `errorscript.php` 文件。
2. 在第 8 行为命令加上分号：

   ```php
   <?php
   echo "<P>I am trying to produce an error</P>";
   echo "<P>Was successful?</P>";
   ?>
   ```

3. 保存文件。
4. 将此文件放在你的 Web 服务器的文档根目录下。

## 转义你的代码

记住转义引号等内容。当你在另一组引号内使用引号时，内部的必须使用 `\` 进行转义。

1. 在文本编辑器中打开一个新文件。
2. 输入以下 HTML：

   ```html
   <HTML>
   <HEAD>
   <TITLE>Trying For Error</TITLE>
   </HEAD>
   <BODY>
   ```

3. 输入以下 PHP 代码：

   ```php
   <?php
   echo "<P>this is really "cool!"</P>";
   ?>
   ```

4. 添加更多 HTML 以使文档有效：

   ```html
   </BODY>
   </HTML>
   ```

5. 将文件保存命名为 `errorsscript.php`。
6. 将此文件放在你的 Web 服务器的文档根目录下。
7. 打开浏览器并输入 `http://127.0.0.1/errorsscript.php`

又是解析错误！看一眼 PHP 代码：

```php
echo "<P>this is really "cool!"</P>";
```

由于你在另一组引号内有了一组引号，内部的必须转义。

这个错误也有简单的修复方法：

1. 打开 `errorsscript.php` 文件。
2. 在第 8 行通过在每个引号前加上反斜杠来转义内部引号：

   ```php
   <?php
   echo "<P>this is really \"cool!\"</P>";
   ?>
   ```

3. 保存文件。
4. 将此文件放在你的 Web 服务器的文档根目录下。

## 注释你的代码

HTML 注释会被浏览器忽略，并包含在 `<!-- -->` 标签中。例如，以下注释提醒你随其后的代码包含你的 logo 图形：

```html
<!-- logo graphic goes here -->
```

PHP 也使用注释，这些注释会被 PHP 解析器忽略。PHP 注释通常以双斜杠开头，如下所示：

```php
// this is a comment in PHP code
```

但你也可以使用其他类型的注释，例如：

```php
# This is a shell-style comment
```

以及

```php
/* This begins a C-style comment that runs
to two lines */
```

创建一个包含注释的脚本，以便你看到它们是如何被忽略的。是的，我是在让你写一个完全无所事事的脚本！

1. 在你的文本编辑器中打开一个新文件。
2. 输入以下 HTML：

   ```html
   <HTML>
   <HEAD>
   <TITLE>Code Comments</TITLE>
   </HEAD>
   <BODY>
   <!-- This is an HTML comment. -->
   ```

3. 输入以下 PHP 代码：

   ```php
   <?php
   // This is a simple PHP comment.
   /* This is a C-style, multiline comment. You can make this as
   long as you'd like. */
   # Used to shells?
   ?>
   ```

4. 添加更多 HTML 以使文档有效：

   ```html
   </BODY>
   </HTML>
   ```

5. 以 `comments.php` 的命名保存文件。
6. 将此文件置于你的 Web 服务器的文档根目录下。

   ![](img/bc248f3d24697d1afbacee37b9c4d229_45_0.png)

7. 打开 Web 浏览器并输入 `http://127.0.0.1/comments.php`

你应该在 Web 浏览器中什么也看不到，因为你所做的只是打印了一个 HTML 注释（它是被忽略的）。由于 PHP 注释会被 PHP 解析器忽略，因此 PHP 块不包含任何实际命令。如果你在浏览器中查看此文档的源代码，你会发现只有 HTML 注释是可见的。尽管 PHP 代码全是注释，但它们仍然被解析了且对用户不可见。

HTML 和 PHP 注释在本书中广泛用于解释代码块。习惯阅读注释，并养成使用注释的习惯。编写带有注释和空白的清洁、无 bug 代码将使你在开发者同行中广受欢迎，因为他们不需要费力猜测你的代码想要做什么。在下一章中，你将学习关于变量的所有知识，或者说，我喜欢称呼的，“那些带有美元符号的东西”。

# 第 5 章：引入变量和运算符

## 概述

在上一章中，你了解了解析 PHP 代码的过程以及代码输出如何在 Web 浏览器中显示。在接下来的章节中，你将学习一些 PHP 语言的内部机制——所有组合在一起实际上产生可运行程序的各个部分！在本章中，你将学习如何执行操作：

- 识别并使用变量
- 识别并使用运算符

# 什么是变量？

变量是特定值的表示，例如蓝色或 19349377。通过给变量赋值，你可以在脚本的其他地方引用该变量，且该值将始终保持不变（除非你更改它，你稍后会学到这一点）。

要创建一个变量，请执行以下操作：

1. 想一个好名字！例如，如果我想创建一个变量来存储用户名，我会将变量命名为 `username`。
2. 在名字前面加一个美元符号 (`$`)：`$username`。
3. 在名字后使用等号 (`=`) 为该变量分配一个字面量值。将值放在引号中：`$username = "joe"`。
4. 给变量赋值是一条指令，因此应该以分号结束：`$username = "joe";`。

就是这样——一个名为 `username` 值为 `joe` 的变量。在本章的晚些时候，你将用你的变量做一些有趣的事情（如数学运算）！

# 为你的变量命名

正如你所见，变量以美元符号 (`$`) 开头，后面跟着一个有意义的名字。变量名不能以数字开头，但可以包含数字和下划线字符 (`_`)。此外，变量名是区分大小写的，这意味着 `$YOURVAR` 和 `$yourvar` 是两个不同的变量。

创建有意义的变量名是编码时避免问题的另一种方法。如果你的脚本处理用户名和密码值，不要为用户名创建一个名为 `$n` 的变量，为密码创建一个名为 `$p` 的变量——这些不是有意义的名字。如果你在几周后拿起该脚本，你可能会认为 `$n` 是“number”（数字）而不是“name”（名称）的变量，而 `$p` 代表“page”（页面）而不是“password”（密码）。

# PHP 变量值类型

你将在 PHP 代码中创建两种主要的变量：标量（scalar）和数组（array）。标量变量一次只包含一个值，而数组包含值列表，甚至是另一个数组。

本章开头的示例创建了一个标量变量，本书主要处理标量变量。你可以在附录 B“PHP 语言基础”中找到关于数组的信息。

当你给变量赋值时，你分配的是以下类型之一：

- 整数：没有小数的整数。
- 浮点数：带有小数的数字。
- 字符串：双引号或单引号内的文本。
- 八进制：八进制数字。
- 十六进制：十六进制数字。

## 预定义变量

PHP 提供了许多预定义变量，它们在脚本中自动可用。现在不用担心完全理解这个概念；随着你对本书的阅读，它将会得到解释。

- `$_GET`：通过 GET 方法提供脚本的任何变量。
- `$_POST`：通过 POST 方法提供脚本的任何变量。
- `$_COOKIE`：通过 cookie 提供的脚本的任何变量。
- `$_FILES`：作为服务器环境的一部分提供脚本的任何变量。
- `$_ENV`：作为服务器环境的一部分提供脚本的任何变量。
- `$_SESSION`：当前在会话中注册的任何变量。

> **注意**：如果你使用的 PHP 版本早于 4.1.x 版本，且无法按照第 3 章“安装 PHP”所述升级到较新版本，则在编写本书中的脚本时，必须调整这些变量的名称。旧名称如下：`$HTTP_GET_VARS`、`$HTTP_POST_VARS`、`$HTTP_COOKIE_VARS`、`$HTTP_POST_FILES`、`$HTTP_ENV_VARS` 和 `$HTTP_SESSION_VARS`。

# 使用常量

常量是某个值的标识符，该值在脚本执行过程中不会发生改变。一旦赋予了值，它在整个执行生命周期内都会保持不变。常量可以是用户定义的，也可以使用 PHP 始终提供的某些预定义常量。与简单变量不同，常量名称前没有美元符号，并且通常使用大写字母以区分它们与标量变量。接下来，将测试用户定义的类型。

1. 在你的文本编辑器中打开一个新文件并打开 PHP 块：

   ```php
   <?php
   ```

2. 用于定义常量的函数是 `define()`，它需要常量的名称和你想给它的值。在这里，你定义了一个名为 `MYCONSTANT` 的常量，值为“This is a test of defining constants.”。

   ```php
   define("MYCONSTANT", "This is a test of defining constants.");
   ```

3. 打印常量的值，然后关闭 PHP 块：

   ```php
   echo MYCONSTANT;
   ?>
   ```

4. 将文件保存为 `constants.php`，并将此文件放在你的 Web 服务器的文档根目录下。
5. 打开 Web 浏览器并输入 `http://127.0.0.1/constants.php`

   ![](img/bc248f3d24697d1afbacee37b9c4d229_50_0.png)

一些预定义常量包括：

- `__FILE__`：正在解析的脚本文件名
- `__LINE__`：正在解析的脚本中的行号
- `PHP_VERSION`：正在使用的 PHP 版本
- `PHP_OS`：使用 PHP 的操作系统

让我们测试一下它们：

1. 在你的文本编辑器中打开一个新文件并打开 PHP 块：

   ```php
   <?php
   ```

2. 使用 `echo` 语句显示介绍字符串，并将 `__FILE__` 接到末尾：

   ```php
   echo "<br>This file is " . __FILE__;
   ```

3. 使用 `echo` 语句显示介绍字符串，并将 `__LINE__` 接到末尾：

   ```php
   echo "<br>This is line number " . __LINE__;
   ```

4. 使用 `echo` 语句显示介绍字符串，并将 `PHP_VERSION` 常量接到末尾：

   ```php
   echo "<br>I am using " . PHP_VERSION;
   ```

5. 使用 `echo` 语句显示介绍字符串，并将 `PHP_OS` 常量接到末尾。同时关闭 PHP 块：

   ```php
   echo "<br>This test is being run on " . PHP_OS;
   ?>
   ```

6. 将文件保存为 `constants2.php`，并将此文件放在你的 Web 服务器的文档根目录下。
7. 打开 Web 浏览器并输入 `http://127.0.0.1/constants2.php`



![](img/bc248f3d24697d1afbacee37b9c4d229_51_0.png)

你应该能看到你输入的字符串以及常量的值。你的值可能与你在这里看到的不同。

## 什么是运算符？

在上一节中，你使用了赋值运算符（`=`）为变量赋值。还有其他类型的赋值运算符，以及通用的其他类型的运算符。运算符的基本功能是对变量的值进行某些操作。这些“某些操作”可以是赋值、改变值或比较两个（或多个）值。

以下是 PHP 运算符的主要类型：

- 赋值运算符。为变量赋值。也可以在变量的当前值上进行加或减操作。
- 算术运算符。你认识所有这些运算符！使用这些运算符时会发生加、减、除和乘法运算。
- 比较运算符。比较两个值并返回真或假。然后你可以对返回的值执行操作。
- 逻辑运算符。确定条件的状态。

本章的其余部分将讨论 PHP 中使用的主要运算符。你将为每种运算符编写脚本，所以请坐好扶稳！

## 赋值运算符

你已经看到赋值运算符的工作了：等号是最基本的赋值运算符。把这一点刻在你的脑子里：`=` 并不意味着“等于”！相反，`==`（两个等号）意味着“等于”，而单个 `=` 意味着“赋值给”。事实上，你在本章中也看到了连接运算符，它被用于将字符串组合。

看看表 5.1 中的赋值运算符，准备编写一个新脚本。

| 表 5.1: 赋值运算符 | 运算符示例 | 操作 |
|---|---|---|
| `+=` | `$a += 3;` | 将变量的值更改为当前值加上右侧的值。 |
| `-=` | `$a -= 3;` | 将变量的值更改为当前值减去右侧的值。 |
| `.=` | `$a .= "string";` | 将右侧的值接到当前值。 |

创建一个简单的脚本来显示这些赋值运算符的作用。该脚本将赋值给一个变量并在执行时结果输出到屏幕。

1. 在你的文本编辑器中打开一个新文件并输入以下 HTML：
2. `<HTML>`
3. `<HEAD>`
4. `<TITLE>Assignment Operators</TITLE>`
5. `</HEAD>`
6. `<BODY>`
7. 开始一个 PHP 块。创建一个值为 100 的变量并打印它：
8. `<?php`
9. `$origVar = 100;`
10. `echo "<p>Original value is $origVar</p>";`
11. 加上该值并打印：
12. `$origVar += 25;`
13. `echo "<p>Added a value, now it's $origVar</p>";`
14. 减去该值并打印：
15. `$origVar -= 12;`
16. `echo "<p>Subtracted a value, now it's $origVar</p>";`
17. 连接一个字符串并打印：
18. `$origVar .= "string";`
19. `echo "<p>Concatenated a string, now it's $origVar</p>";`
20. 关闭 PHP 块：
21. `?>`
22. `</BODY>`
23. `</HTML>`
24. 将文件保存为 `assignscript.php`，并将此文件放在你的 Web 服务器的文档根目录下。
25. 打开 Web 浏览器并输入 `http://127.0.0.1/assignscript.php`

![](img/bc248f3d24697d1afbacee37b9c4d229_53_0.png)

计算结果将打印到屏幕上。

## 算术运算符

算术运算符就是数学！看看表 5.2。

| 表 5.2: 算术运算符 | 运算符示例 | 操作 |
|---|---|---|
| `+` | `$a + 3;` | 加 |
| `-` | `$a - 3;` | 减 |
| `*` | `$a * 3;` | 乘 |
| `/` | `$a / 3;` | 除 |
| `%` | `$a % 3;` | 返回余数 |

创建一个简单的脚本来显示这些算术运算符的作用。该脚本将原始值赋值给两个变量，执行操作并将结果打印到屏幕。

1. 在你的文本编辑器中打开一个新文件并以下 HTML：
2. `<HTML>`
3. `<HEAD>`
4. `<TITLE>Using Arithmetic Operators</TITLE>`
5. `</HEAD>`
6. `<BODY>`
7. 开始一个 PHP 块，创建两个带有变量并打印它们：
8. `<?php`
9. `$a = 85;`
10. `$b = 24;`
11. `echo "<p>Original value of $a is $a and $b is $b</p>";`
12. 加两个值并打印结果：
13. `$c = $a + $b;`
14. `echo "<p>Added $a and $b is $c</p>";`
15. 减去两个值并打印结果：
16. `$c = $a - $b;`
17. `echo "<p>Subtracted $b from $a is $c</p>";`
18. 乘以两个值并打印结果：
19. `$c = $a * $b;`
20. `echo "<p>Multiplied $a and $b is $c</p>";`
21. 除两个值并打印结果：
22. `$c = $a / $b;`
23. `echo "<p>Divided $a by $b is $c</p>";`
24. 检查两个值的余数并打印结果：
25. `$c = $a % $b;`
26. `echo "<p>The modulus of $a and $b is $c</p>";`
27. 关闭 PHP 块：
28. `?>`
29. `</BODY>`
30. `</HTML>`
31. 将文件保存为 `arithmeticscript.php`，并将此文件放在你的 Web 服务器的文档根目录下。
32. 打开 Web 浏览器并输入 `http://127.0.0.1/arithmeticscript.php`

你的原始值以及各种计算结果将打印到屏幕上。

## 比较运算符

比较运算符是非常必要的，但远没有算术运算符那么多。它们比较两个值并返回一个布尔值（真或假）。

以下是比较运算符的主要类型：

- `==` 检查两个值是否相等。
- `!=` 检查两个值是否相等。
- `>` 检查左侧值是否大于右侧。
- `<` 检查左侧值是否小于右侧。
- `>=` 检查左侧值是否大于或等于右侧。
- `<=` 检查左侧值是否小于或等于右侧。

| 运算符 | 定义 |
|---|---|
| `==` | 等于 |
| `!=` | 不等于 |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |

任何这些比较的结果要么为真（`true`），要么为假（`false`）。这并不有趣，你可以使用 `if...else` 和 `while` 等控制语句对结果进行操作，以执行特定任务。

创建一个简单的脚本来显示某些比较的结果，使用 `if...else` 控制语句将结果打印到屏幕上。

1. 在文本编辑器中打开一个新文件并输入以下 HTML：
2. `<HTML>`
3. `<HEAD>`
4. `<TITLE>使用比较运算符</TITLE>`
5. `</HEAD>`
6. `<body>`
7. 启动一个 PHP 块，创建两个带有值的变量，并打印这些值：
8. `<?php`
9. `$a = 21;`
10. `$b = 15;`
11. `echo "<P>Original value of $a is $a and $b is $b</P>";`
12. 在 `if...else` 语句中，测试 `$a` 是否等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：
13. `if ($a == $b) {`
14. `echo "<P>TEST 1: \$a is equal to \$b</P>";`
15. `} else {`
16. `echo "<P>TEST 1: \$a is not equal to \$b</P>";`
17. `}`
18. 条件表达式在圆括号中表示。
19. 在 `if...else` 语句中，测试 `$a` 是否不等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：
20. `if ($a != $b) {`
21. `echo "<P>TEST 2: \$a is not equal to \$b</P>";`
22. `} else {`
23. `echo "<P>TEST 2: \$a is equal to \$b</P>";`
24. `}`
25. 大括号 `{}` 分隔了控制结构内的语句块。
26. 在 `if...else` 语句中，测试 `$a` 是否大于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：
27. `if ($a > $b) {`
28. `echo "<P>TEST 3: \$a is greater than \$b</P>";`
29. `} else {`
30. `echo "<P>TEST 3: \$a is not greater than \$b</P>";`
31. `}`
32. 在 `if...else` 语句中，测试 `$a` 是否小于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：
33. `if ($a < $b) {`
34. `echo "<P>TEST 4: \$a is not less than \$b</P>";`
35. `} else {`
36. `echo "<P>TEST 4: \$a is not less than \$b</P>";`
37. `}`
38. 在 `if...else` 语句中，测试 `$a` 是否大于或等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：
39. `if ($a >= $b) {`
40. `echo "<P>TEST 5: \$a is greater than or equal to \$b</P>";`
41. `} else {`
42. `echo "<P>TEST 5: \$a is not greater than or equal to \$b</P>";`
43. `}`
44. 在 `if...else` 语句中，测试 `$a` 是否小于或等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：
45. `if ($a <= $b) {`
46. `echo "<P>TEST 6: \$a is less than or equal to \$b</P>";`
47. `} else {`
48. `echo "<P>TEST 6: \$a is not less than or equal to \$b</P>";`
49. `}`
50. 关闭你的 PHP 块并添加更多 HTML 以使文档有效：
51. `?>`
52. `</body>`
53. `</html>`
54. 将文件保存为 `comparisonscript.php`并将此文件放置在 Web 服务器的文档根目录下。
55. 打开你的 浏览器并输入 `http://127.0.0.1/comparisonscript.php`

原始值以及各种比较的结果将打印到屏幕上。你处理的最后运算符类型是逻辑运算符，它们也经常用于代码块内部。

## 逻辑运算符

逻辑运算符允许你的脚本确定条件的状态（例如上一节中的比较）。在 `if...else` 或 `while` 语句的语境下，逻辑运算符根据哪些条件为真、哪些为假来执行特定的代码。

现在，重点关注 `&&`（与）和 `||`（或）运算符，以判断几次比较的有效性。

1. 在文本编辑器中打开一个新文件并输入以下 HTML：
2. `<HTML>`
3. `<HEAD>`
4. `<TITLE>使用逻辑运算符</TITLE>`
5. `</HEAD>`
6. `<body>`
7. 启动一个 PHP 块并创建两个带有值的变量。此脚本中的比较将基于这些变量：
8. `<?php`
9. `$degrees = "95";`
10. `$hot = "yes";`
11. 在 `if...else` 语句中，测试 `$degrees` 是否大于 100。根据答案（真或假），其中一个 `echo` 语句将打印：
12. `if ($degrees > 100 || $hot == "yes") {`
13. `echo "<P>TEST 1: \$degrees is greater than 100 or \$hot is yes</P>";`
14. `} else {`
15. `echo "<P>TEST 1: \$degrees is not greater than 100 or \$hot is yes</P>";`
16. `}`
17. 注意：条件表达式由圆括号包裹。
18. 在 `if...else` 语句中，测试 `$degrees` 是否不等于 100。根据答案（真或假），其中一个 `echo` 语句将打印：
19. `if ($degrees != 100 && $hot == "yes") {`
20. `echo "<P>TEST 2: \$degrees is not equal to 100 and \$hot is yes</P>";`
21. `} else {`
22. `echo "<P>TEST 2: \$degrees is equal to 100 and \$hot is yes</P>";`
23. `}`
24. 大括号 `{}` 分隔了控制结构内的语句块。
25. 在 `if...else` 语句中，测试 `$degrees` 是否大于 100。根据答案（真或假），其中一个 `echo` 语句将打印：
26. `if ($degrees > 100) {`
27. `echo "<P>TEST 3: \$degrees is greater than 100</P>";`
28. `} else {`
29. `echo "<P>TEST 3: \$degrees is not greater than 100</P>";`
30. `}`
31. 在 `if...else` 语句中，测试 `$degrees` 是否小于 100。根据答案（真或假），其中一个 `echo` 语句将打印：
32. `if ($degrees < 100) {`
33. `echo "<P>TEST 4: \$degrees is not less than 100</P>";`
34. `} else {`
35. `echo "<P>TEST 4: \$degrees is less than 100</P>";`
36. `}`
37. 在 `if...else` 语句中，测试 `$degrees` 是否大于或等于 100。根据答案（真或假），其中一个 `echo` 语句将打印：
38. `if ($degrees >= 100) {`
39. `echo "<P>TEST 5: \$degrees is greater than or equal to 100</P>";`
40. `} else {`
41. `echo "<P>TEST 5: \$degrees is not greater than or equal to 100</P>";`
42. `}`
43. 在 `if...else` 语句中，测试 `$degrees` 是否小于或等于 100。根据答案（真或假），其中一个 `echo` 语句将打印：
44. `if ($degrees <= 100) {`
45. `echo "<P>TEST 6: \$degrees is not less or equal to 100</P>";`
46. `} else {`
47. `echo "<P>TEST 6: \$degrees is less than or equal to 100</P>";`
48. `}`
49. 关闭你的 PHP 块并添加更多 HTML 以使文档有效：
50. `?>`
51. `</body>`
52. `</html>`
53. 将文件保存为 `logicalscript.php`并将此文件放置在 Web 服务器的文档根目录下。
54. 打开你的 浏览器并输入 `http://127.0.0.1/logicalscript.php`

原始值以及各种比较的结果将打印到屏幕上。你处理的最后运算符类型是逻辑运算符，它们也经常用于代码块内部。



| 运算符 | 含义 |
| --- | --- |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |

任何这些比较的结果要么为真（`true`），要么为假（`false`）。这并不有趣，你可以使用 `if...else` 和 `while` 等控制语句对结果进行操作，以执行特定任务。

创建一个简单的脚本来显示某些比较的结果，使用 `if...else` 控制语句将结果打印到屏幕上。

1. 在文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>使用比较运算符</TITLE>
</HEAD>
<body>
```

7. 启动一个 PHP 块，创建两个带有值的变量，并打印这些值：

```php
<?php
$a = 21;
$b = 15;
echo "<P>Original value of \$a is \$a and \$b is \$b</P>";
```

在 `if...else` 语句中，测试 `$a` 是否等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($a == $b) {
    echo "<P>TEST 1: \$a is equal to \$b</P>";
} else {
    echo "<P>TEST 1: \$a is not equal to \$b</P>";
}
```

条件表达式在圆括号中表示。

在 `if...else` 语句中，测试 `$a` 是否不等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($a != $b) {
    echo "<P>TEST 2: \$a is not equal to \$b</P>";
} else {
    echo "<P>TEST 2: \$a is equal to \$b</P>";
}
```

大括号 `{}` 分隔了控制结构内的语句块。

在 `if...else` 语句中，测试 `$a` 是否大于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($a > $b) {
    echo "<P>TEST 3: \$a is greater than \$b</P>";
} else {
    echo "<P>TEST 3: \$a is not greater than \$b</P>";
}
```

在 `if...else` 语句中，测试 `$a` 是否小于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($a < $b) {
    echo "<P>TEST 4: \$a is less than \$b</P>";
} else {
    echo "<P>TEST 4: \$a is not less than \$b</P>";
}
```

在 `if...else` 语句中，测试 `$a` 是否大于或等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($a >= $b) {
    echo "<P>TEST 5: \$a is greater than or equal to \$b</P>";
} else {
    echo "<P>TEST 5: \$a is not greater than or equal to \$b</P>";
}
```

在 `if...else` 语句中，测试 `$a` 是否小于或等于 `$b`。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($a <= $b) {
    echo "<P>TEST 6: \$a is less than or equal to \$b</P>";
} else {
    echo "<P>TEST 6: \$a is not less than or equal to \$b</P>";
}
```

关闭你的 PHP 块并添加更多 HTML 以使文档有效：

```php
?>
</body>
</html>
```

将文件保存为 `comparisonscript.php` 并将此文件放置在 Web 服务器的文档根目录下。

打开你的浏览器并输入 `http://127.0.0.1/comparisonscript.php`

原始值以及各种比较的结果将打印到屏幕上。你处理的最后运算符类型是逻辑运算符，它们也经常用于代码块内部。

# 逻辑运算符

逻辑运算符允许你的脚本确定条件的状态（例如上一节中的比较）。在 `if...else` 或 `while` 语句的语境下，逻辑运算符根据哪些条件为真、哪些为假来执行特定的代码。

现在，重点关注 `&&`（与）和 `||`（或）运算符，以判断几次比较的有效性。

1. 在文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>使用逻辑运算符</TITLE>
</HEAD>
<body>
```

7. 启动一个 PHP 块并创建两个带有值的变量。此脚本中的比较将基于这些变量：

```php
<?php
$degrees = "95";
$hot = "yes";
```

在 `if...else` 语句中，测试 `$degrees` 是否大于 100。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($degrees > 100 || $hot == "yes") {
    echo "<P>TEST 1: \$degrees is greater than 100 or \$hot is yes</P>";
} else {
    echo "<P>TEST 1: \$degrees is not greater than 100 or \$hot is yes</P>";
}
```

注意：条件表达式在圆括号中表示。

在 `if...else` 语句中，测试 `$degrees` 是否不等于 100。根据答案（真或假），其中一个 `echo` 语句将打印：

```php
if ($degrees != 100 && $hot == "yes") {
    echo "<P>TEST 2: \$degrees is not equal to 100 and \$hot is yes</P>";
} else {
    echo "<P>TEST 2: \$degrees is equal to 100 and \$hot is yes</P>";
}
```

大括号 `{}` 分隔了控制结构内的语句块。

# 创建计算脚本

根据 `calculate_form.html` 中的表单 action，你需要一个名为 `calculate.php` 的脚本。该脚本的目标是接收两个值（`$_POST['val1']` 和 `$_POST['val2']`），并根据 `$_POST['calc']` 的值执行计算。

1. 在你的文本编辑器中新建一个文件。
2. 开始一个 PHP 块，并准备一个 `if` 语句来检查三个值是否存在：

```php
<?php
if ($_POST['val1'] == "" || $_POST['val2'] == "" || $_POST['calc'] == "") {
    // 此处编写更多代码
}
```

该语句的意思是“如果这三个变量中的任何一个没有值”。

8. 将“此处编写更多代码”替换为以下两行：

```php
header("Location: http://127.0.0.1/calculate_form.html");
exit;
```

前两行输出一个 header 语句——在这种情况下，打印一个新位置：表单的 URL。第二行退出脚本。因此，如果三个变量中的任何一个没有值，用户将被重定向到原始表单。

请注意，在你的 PHP 块开始之前，不能有换行符、空格或任何文本。如果输出已经发送到浏览器，你无法使用 `header()` 函数。

11. 开始 `if...else` 语句，根据 `$_POST['calc']` 的值执行正确的计算：

```php
if ($_POST['calc'] == "add") {
    $result = $_POST['val1'] + $_POST['val2'];
} else if ($_POST['calc'] == "subtract") {
    $result = $_POST['val1'] - $_POST['val2'];
} else if ($_POST['calc'] == "multiply") {
    $result = $_POST['val1'] * $_POST['val2'];
} else if ($_POST['calc'] == "divide") {
    $result = $_POST['val1'] / $_POST['val2'];
}
```

23. 开始 HTML 输出：

```html
<HTML>
<HEAD>
<TITLE>计算结果</TITLE>
</HEAD>
<BODY>
```

使用混合了 PHP 代码的 HTML 显示 `$result` 的值：

```php
<p>计算结果为：<?php echo $result; ?></p>
```

添加更多 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

35. 将文件保存为 `calculate.php`，并将此文件置于你 Web 服务器的文档根目录下。

## 提交表单并获取结果

现在你已经创建了前端（表单）和后端（脚本），是时候屏住呼吸进行测试了。

1. 访问计算表单，打开你的 Web 浏览器并输入 `http://127.0.0.1/calculate_form.html`
2. 在不在表单字段中输入任何内容的情况下点击按钮。你的 Web 浏览器将重新加载页面，因为你没有为三个输入字段输入任何值。
3. 为 Value 1 输入一个值，但不为 Value 2 输入，且不选择计算选项。点击“计算”后，页面应该重新加载。
4. 为 Value 2 输入一个值，但不为 Value 1 输入，且不选择计算选项。点击“计算”后，页面应该重新加载。
5. 为 Value 1 和 Value 2 输入一个值，但不选择计算选项。点击“计算”后，页面应该重新加载。
6. 选择一个计算选项，但不对 Value 1 或 Value 2 输入任何值。点击“计算”后，页面应该重新加载。

现在你已经通过尝试绕过你的验证程序来调试了脚本，请尝试一些计算：

1. 为 Value 1 输入 32，Value 2 输入 27。
2. 选择“加”。
3. 选择“减”。
4. 为 Value 1 输入 92，Value 2 输入 43。
5. 选择“乘”。
6. 为 Value 1 输入 86，Value 2 输入 55。
7. 选择“乘”。
8. 为 Value 1 输入 71，Value 2 输入 14。
9. 选择“除法”。

计算结果为：

# 环境变量

当 Web 浏览器发出请求时，它会发送一些信息。这些被称为环境变量，它们非常有用。

`phpinfo()` 函数显示关于你的 Web 服务器的丰富信息。

1. 在你的文本编辑器中新建一个文件。
2. 输入以下 PHP 代码：
   ```php
   <?php phpinfo(); ?>
   ```
3. 将文件保存为 `phpinfo.php`，并将其置于 Web 服务器的文档根目录下。
4. 打开你的浏览器并输入 `http://127.0.0.1/phpinfo.php`

## 获取并使用 REMOTE_ADDR

默认情况下，环境变量可以通过 `$_VAR_NAME` 在 PHP 脚本中使用。例如，`$_SERVER['REMOTE_ADDR']` 已经包含了。但为了绝对确保读取的是正确的值，请使用 `getenv()`。

该变量包含请求机器的 IP 地址。

1. 在你的文本编辑器中新建一个文件。
2. 打开一个 PHP 块，然后使用 `getenv()` 将 `REMOTE_ADDR` 的值赋值给变量 `$address`：
   ```php
   <?php
   $address = getenv("REMOTE_ADDR");
   ```
3. 将 `$address` 的值打印到屏幕，并关闭 PHP 块：
   ```php
   echo "Your IP address is " . $address;
   ?>
   ```
4. 将文件保存为 `remoteaddress.php`，并将其置于 Web 服务器的文档根目录下。
5. 打开你的 Web 浏览器并输入 `http://127.0.0.1/remoteaddress.php`

注意你的 IP 地址将与显示的不同。

`HTTP_USER_AGENT` 变量包含了浏览器类型、浏览器版本、语言编码和平台。例如，以下值字符串指向 Netscape(Mozilla) 浏览器，版本 4.61，英语，运行在 Windows 98 平台：

`Mozilla/4.61 (Win98; I)`

有时你会看到 MSIE 返回一个看起来像 Netscape 的 `HTTP_USER_AGENT` 值，直到你注意到该值说它是“兼容的”且实际上是“MSIE 5.0”。

`Mozilla/4.0 (compatible; MSIE 5.5; Windows 98)`

当你向下滚动，寻找标题为“Apache Environment”的部分。在后续章节中，你将获得另一个实用的环境变量值 `HTTP_USER_AGENT`。关于某些环境变量的解释，请访问 `http://ncsa.edu/env.html`。

我是那些 Lynx 忠实用户之一。不要忽视这些纯文本浏览器！Lynx 的 `HTTP_USER_AGENT` 值看起来如下：

`Lynx/2.8rel.3 libwww-FM/2.14`

让我们找到你的 `HTTP_USER_AGENT`。

1. 在你的文本编辑器中打开新文件。
2. 打开一个 PHP 代码块，然后使用 `getenv()` 将 `HTTP_USER_AGENT` 的值赋给名为 `$agent` 的变量：
   ```php
   <?
   $agent = getenv("HTTP_USER_AGENT");
   ```
3. 将 `$agent` 的值打印到屏幕，然后结束你的 PHP 代码块：
   ```php
   echo "You are using $agent.";
   ?>
   ```
4. 将文件保存为 `useragent.php`，然后将此文件放在你 Web 服务器的文档根目录下。
5. 打开你的 Web 浏览器并输入 `http://127.0.0.1/useragent.php`

注意：你的用户代理字符串可能与显示的有所不同。

在下一章中，你将学习 Web 开发人员的许多基础任务，包括显示动态内容、发送电子邮件以及处理文件系统。

## 第三部分：从简单内容开始

### 章节列表

- 第 7 章：显示动态内容
- 第 8 章：发送电子邮件
- 第 9 章：使用你的文件系统
- 第 10 章：上传文件到你的网站

## 第 7 章：显示动态内容

### 概述

Web 是一个动态环境，为什么不利用你的编程技能来显示动态内容呢？动态内容的简单或复杂取决于你的需求。在本章中，你将学习如何执行以下操作：

- 显示特定浏览器的 HTML
- 显示特定平台的 HTML
- 在 HTML 表单输入上使用 PHP 字符串函数
- 使用 HTML 表单和 `header()` 创建重定向菜单

### 显示特定浏览器的 HTML

在上一章中，你学习了如何获取并将 `HTTP_USER_AGENT` 环境变量打印到屏幕。在本章中，你将对 `HTTP_USER_AGENT` 的值进行更有趣的操作，并打印特定浏览器的 HTML。

然而，在看到了上一章中 `HTTP_USER_AGENT` 的可能值后，你可以想象有数百个略有不同的值。现在是时候学习基础模式匹配了。

你将使用 `preg_match()` 函数来完成此任务。这需要两个参数：你要找什么，以及你在哪里找：

```php
preg_match("what you're looking for", "where you're looking");
```

该函数将返回 `true` 或 `false` 值，你可以将其用于 `if...else` 块中以执行你想做的任何操作。第一个脚本的目标是判断 Web 浏览器是 Microsoft Internet Explorer、Netscape 还是其他。这可能有点棘手，但并不是因为 PHP。

在 `HTTP_USER_AGENT` 的值中，Netscape 总是使用 `Mozilla` 来识别自己。遗憾的是，Microsoft Internet Explorer 的 `HTTP_USER_AGENT` 值也使用 `Mozilla` 来显示兼容性。幸运的是，它也使用了 `MSIE`，所以你可以搜索它。如果 `HTTP_USER_AGENT` 的值不包含 `Mozilla` 或 `MSIE`，那么它很大概率不是这些浏览器之一。

1. 在你的编辑器中打开新文件并开始 PHP 代码块，然后使用 `getenv()` 将 `HTTP_USER_AGENT` 的值赋给名为 `$agent` 的变量：
   ```php
   <?
   $agent = getenv("HTTP_USER_AGENT");
   ```
2. 开始一个 `if...else` 语句来寻找哪个 `preg_match()` 函数为真，从搜索 MSIE 开始：
   ```php
   if (preg_match("/MSIE/", "$agent")) {
       $result = "You are using Microsoft Internet Explorer";
   }
   ```
3. 继续该语句，测试 Mozilla：
   ```php
   else if (preg_match("/Mozilla/i", "$agent")) {
       $result = "You are using Netscape.";
   }
   ```
4. 通过定义默认值来完成语句：
   ```php
   else {
       $result = "You are using $agent";
   }
   ```

注意：`preg_match()` 函数中的 `i` 执行的是不区分大小写的搜索。

5. 关闭你的 PHP 代码块并添加一些 HTML 开始显示：
   ```php
   ?>
   <HTML>
       <HEAD>
       <TITLE>Browser Match Results</TITLE>
       </HEAD>
       <BODY>
       <p><?php echo $result; ?></p>
   <?php
   ```
6. 添加更多 HTML 以使文档有效：
   ```html
   </BODY>
   </html>
   ```
7. 将文件保存为 `browsermatch.php` 并将此文件放在你 Web 服务器的文档根目录下。`http://127.0.0.1/browsermatch.php`
8. 打开你的 Web 浏览器并输入 `http://127.0.0.1/browsermatch.php`

> 根据 Web 浏览器的使用，你可能会看到如下结果

浏览器大战仍在继续：没有一种 Web 浏览器被绝大多数用户使用。各种版本的 Microsoft Internet Explorer (MSIE) 占所用 Web 浏览器的 78%，而 Netscape (NS) 版本占了约 15%。在 Lynx、Opera、Conquerer 等其他忠实用户中则达到了 100%。

尽管 80/20 的划分看起来是多数，但如果有 5 亿人可以访问互联网，那么有 1 亿人...

### 显示特定平台的 HTML

你可以使用相同的技术来显示特定平台的 HTML。例如，你可以根据操作系统显示不同的样式表。

1. 在你的编辑器中打开新文件并开始 PHP 代码块，然后使用 `getenv()` 将 `HTTP_USER_AGENT` 的值赋给名为 `$agent` 的变量：
   ```php
   <?
   $agent = getenv("HTTP_USER_AGENT");
   ```
2. 开始一个 `if...else` 语句来寻找哪个 `preg_match()` 函数为真，从搜索 Windows 开始：
   ```php
   if (preg_match("/Win/", "$agent")) {
       $result = "<link rel=\"stylesheet\" type=\"text/css\" href=\"win.css\">";
   }
   ```
3. 继续该语句，测试 Mac：
   ```php
   else if (preg_match("/Mac/", "$agent")) {
       $result = "<link rel=\"stylesheet\" type=\"text/css\" href=\"mac.css\">";
   }
   ```
4. 通过定义默认值来完成语句：
   ```php
   else {
       $result = "<link rel=\"stylesheet\" type=\"text/css\" href=\"unix.css\">";
   }
   ```
5. 关闭你的 PHP 代码块并添加一些 HTML 开始显示：
   ```php
   ?>
   <HTML>
       <HEAD>
       <TITLE>Platform Match Results</TITLE>
       </HEAD>
       <BODY>
       <p><?php echo $result; ?></p>
   <?php
   ```
6. 添加更多 HTML 以使文档有效：
   ```html
   </BODY>
   </HTML>
   ```
7. 将文件保存为 `platformmatch.php` 并将其放在你的 Web 服务器的文档根目录下。
8. 打开你的 Web 浏览器并输入 `http://127.0.0.1/platformmatch.php`

根据所使用的 Web 浏览器，你可能会看到如下结果：

![](img/bc248f3d24697d1afbacee37b9c4d229_70_0.png)

或者这个。

![](img/bc248f3d24697d1afbacee37b9c4d229_70_1.png)

你可以看到，根据模式匹配的结果，已经打印了正确的样式表块。在下一节中，你将离开模式匹配，并使用 PHP 中的一些字符串函数在将表单输入显示回浏览器之前对其进行修改。

### 使用字符串函数

PHP 内置了许多字符串函数，它们的设计都是为了让你的生活更轻松。假设你必须对新闻标题或产品 ID 编号进行字符串归一化，或者在尝试将其存入数据库字段之前计算字符串的长度。这些只是你将在下一节中将学到的字符串函数之一。关于更多字符串函数，请查看 `http://www.php.net/manual/` 上的 PHP 手册。随着更多人为该语言做出贡献，函数列表似乎每天都在增长。

### 创建输入表单

在这一节中，你将创建一个字符串修改脚本的前端。此表单将包含一个文本区域和几个单选按钮。单选按钮将决定要使用的字符串函数。

1. 在你的文本编辑器中打开新文件并输入以下 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>通用输入表单</TITLE>
   </HEAD>
   <BODY>
   ```
2. 开始你的表单。假设方法为 POST，动作为名为 `display_input.php` 的脚本：
   ```html
   <FORM METHOD="POST" ACTION="display_input.php">
   ```
3. 创建一个带有文本标签的文本区域：
   ```html
   <input type="text"><br>
   <TEXTAREA name="text1" COLS=45 ROWS=5 WRAP=virtual></TEXTAREA>
   ```
4. 添加这些单选按钮：
   ```html
   <input name="String Function"><br>
   <INPUT TYPE="radio" NAME="func" VALUE="md5"> 获取 md5<br>
   <INPUT TYPE="radio" NAME="func" VALUE="strlen"> 获取字符串长度<br>
   <INPUT TYPE="radio" NAME="func" VALUE="strrev"> 反转字符串<br>
   <INPUT TYPE="radio" NAME="func" VALUE="strtoupper"> 将字符串转为大写<br>
   <INPUT TYPE="radio" NAME="func" VALUE="strtolower"> 将字符串转为小写<br>
   <INPUT TYPE="radio" NAME="func" VALUE="ucwords"> 将所有单词的首字母大写</p>
   ```

注意：每个选项按钮的值是其 PHP 函数名。这将使后端脚本变得简单，正如你在下一节中看到的那样。

5. 添加一个提交按钮：
   ```html
   <INPUT TYPE="submit" NAME="submit" VALUE="对字符串进行操作"></p>
   ```
6. 关闭你的表单并添加一些通用的 HTML 以确保文档是有效的：
   ```html
   </FORM>
   </BODY>
   </html>
   ```
7. 将文件保存为 `generic_form.html` 并将此文件放在 Web 服务器的根目录下。
8. 打开你的浏览器并输入 `http://127.0.0.1/generic_form.html`

![](img/bc248f3d24697d1afbacee37b9c4d229_71_0.png)

### 创建显示表单值的脚本

根据 `generic_form.html` 中的表单动作，你需要一个名为 `display_input.php` 的脚本。该脚本的目标是捕捉 `$_POST['text1']` 中的文本并使用特定的字符串函数（`$_POST['func']` 的值）获取新结果（`$result`）。

1. 在你的文本编辑器中打开新文件并输入以下 PHP：
   ```php
   <?php $result = $_POST['func']($_POST['text1']); ?>
   ```
2. 开始 HTML 输出：
   ```html
   <HTML>
   <HEAD>
   <TITLE>通用输入结果</TITLE>
   </HEAD>
   <BODY>
   ```
3. 显示 `$result` 的值：
   ```php
   <?php echo "$result"; ?>
   ```
4. 添加一个指向表单的链接：
   ```html
   <P><a href="generic_form.html">再次尝试！</a></P>
   ```
5. 添加更多 HTML 以确保文档是有效的：
   ```html
   </BODY>
   </HTML>
   ```
6. 将文件保存为 `display_input.php` 并将此文件放在你的 Web 服务器的文档根目录下。

![](img/bc248f3d24697d1afbacee37b9c4d229_72_0.png)

## 提交表单并获取结果

现在你已经创建了前端表单和后端脚本。

1. 打开你的浏览器并输入 `http://127.0.0.1/generic_form.html`
2. 在文本区域中输入以下内容：
   `PHP 仅仅是酷的后端脚本`
3. 选择 md5 按钮，点击“对字符串进行操作”。

注意 `md5()` 函数获取字符串的哈希值。哈希值就像字符串的摘要，可以用于比较文件是否不同。

4. 点击“再次尝试”。

![](img/bc248f3d24697d1afbacee37b9c4d229_73_0.png)

5. 在文本区域中输入以下内容：
   `PHP 仅仅是酷的后端脚本`
6. 选择获取字符串长度的按钮，点击“对字符串进行操作”。
7. 点击“再次尝试”。

![](img/bc248f3d24697d1afbacee37b9c4d229_73_1.png)

8. 在文本区域中输入以下内容：
   `PHP 仅仅是酷的后端脚本`
9. 选择反转字符串的按钮，点击“对字符串进行操作”。
10. 点击“再次尝试”。

![](img/bc248f3d24697d1afbacee37b9c4d229_73_2.png)

11. 在文本区域中输入以下内容：
    `PHP 仅仅是酷的后端脚本`
12. 选择将字符串转为大写的按钮，点击“对字符串进行操作”。
13. 点击“再次尝试”。

14. 在文本区域中输入以下内容：
    `PHP 仅仅是酷的后端脚本`
15. 选择将字符串转为小写的按钮，点击“对字符串进行操作”。
16. 点击“再次尝试”。

17. 在文本区域中输入以下内容：
    `PHP 仅仅是酷的后端脚本`
18. 选择将所有单词的首字母大写的按钮，点击“对字符串进行操作”。
19. 点击“再次尝试”。

# 第 8 章：发送电子邮件

## 概述

使用 PHP 将表单内容发送到指定的电子邮件地址非常简单，以至于你会怀疑为什么大家不每天这样做。在本章中，你将学习如何实现以下操作：

- 修改 PHP 配置以发送邮件
- 创建并发送简单的反馈表单
- 使用 `$_SERVER['PHP_SELF']` 变量创建带有错误信息的反馈表单

## 使用 SMTP 服务器

SMTP（简单邮件传输协议）服务器是一个传输邮件的机器，就像 Web 服务器是在请求时显示 Web 页面的机器。SMTP 服务器有时被称为发送邮件服务器，这引出了这一点——你需要它来完成本章的练习。在 Linux/UNIX 上，Sendmail 和 Postfix 是流行的包。在 Windows 上，通常使用 Windows NT Service Pack 中的 SMTP 服务或 Windows 2000 系统内置的服务。

如果你在个人机器的开发环境中安装了 Apache、PHP 和 MySQL，那么你的本地可能没有运行 SMTP。在这种情况下，你可以访问可能已经为你提供的发送邮件服务器。

**注意：** 如果你跳过了本书的前三章，并将 PHP 作为互联网服务提供商虚拟主机的一部分，那么该机器上应该已经安装了 SMTP 服务器，PHP 也应该已配置好访问。

如果你通过拨号连接、DSL、电缆或其他类型的连接互联网，可以使用你互联网服务提供商的发送邮件服务器。例如，如果你的开发机是通过 EarthLink 连接互联网的带有 56Kbps 调制器的 Windows 98 ，那么可以使用 `mail.earthlink.net` 作为你的 SMTP 服务器。你在邮件客户端（Eudora、Outlook、Netscape Mail 等）中配置的任何发送邮件服务器都可以在你的 PHP 代码中作为 SMTP 服务器运行。技巧在于让 PHP 意识到这一小事实，你接下来将学习。

### php.ini 中与 SMTP 更改

在 `php.ini` 主配置文件中，有一些指令需要设置才能使 `mail()` 函数正常工作。使用文本编辑器打开 `php.ini` 并查找这些行：

```ini
[function]
; 仅限 Win32。
SMTP = localhost
; 仅限 Win32。
sendmail_from = me@localhost.com
; 适用于 Unix。你可以提供参数以及默认值：
;sendmail -t -
;sendmail_path =
```

如果你使用的是 Windows，则需要修改前两个指令：`SMTP` 和 `sendmail_from`。如果你计划使用你的 ISP（在本例中为 EarthLink）的发送邮件服务器，`php.ini` 中的条目看起来如下：

```ini
SMTP = mail.earthlink.net
```

第二个配置指令是 `sendmail_from`，它是发送邮件的 `From` 头部中使用的电子邮件地址。它可以在邮件脚本本身中覆盖，但通常作为默认值运行。例如：

```ini
sendmail_from = youraddress@yourdomain.com
```

当然，将 `youraddress@yourdomain.com` 替换为你自己的地址。如果你在 Unix 上，只需要关心 `sendmail_path`，它看起来应该是这样的：

```ini
sendmail_path = /usr/sbin/sendmail
```

在 `sendmail_path` 指令中，你还可以设置标志，例如：

```ini
sendmail_path = /usr/sbin/sendmail -t -f youraddress@yourdomain.com
```

修改 `php.ini` 后，重启 Web 服务器并验证更改已生效。

### 简单反馈表单

1. 在你的文本编辑器中打开一个文件。
2. 输入以下 HTML：
   ```html
   <html>
   <head>
       <title>反馈表单</title>
   </head>
   <body>
       <form action="send_simple.php" method="POST">
           姓名：<br>
           <input type="text" name="sender_name"><br>
           电子地址：<br>
           <input type="text" name="sender_email"><br>
           消息：<br>
           <textarea name="message" cols="30" rows="5"></textarea><br>
           <input type="submit" name="submit" value="提交表单"/>
       </form>
   </body>
   </html>
   ```
3. 将文件保存为 `simple_form.html`。

### 创建发送表单的脚本

1. 在你的文本编辑器中打开一个文件。
2. 开始 PHP 块，然后开始一个消息字符串：
   ```php
   <?php
   $msg = "来自网站的邮件";
   // 继续拼接添加发送者姓名
   $msg .= "\n姓名：" . $_POST['sender_name'];
   // 继续拼接添加发送者邮箱
   $msg .= "\n邮箱：" . $_POST['sender_email'];
   // 继续拼接添加消息
   $msg .= "\n消息：" . $_POST['message'];

   // 最后一行包含两个换行符，在字符串末尾添加空格
   // 创建变量存储你的电子邮件地址（替换为你自己的）
   $to = "you@example.com";
   // 创建变量存储邮件主题
   $subject = "网站反馈";
   // 创建变量存储额外的邮件头信息
   $mailheaders = "From: 我的网站 \n";

   // 使用 mail() 函数发送邮件
   mail($to, $subject, $msg, $mailheaders);
   // 向浏览器显示消息
   echo "<h1>感谢您的反馈！</h1>";
   ?>
   ```
3. 将文件保存为 `send_simple.php` 并将此文件放在你的 Web 服务器的根目录下。
4. 打开你的 浏览器并输入 `http://127.0.0.1/simple_form.html`。

### 改进的反馈表单脚本

1. 向 `mailheaders` 变量添加：
   ```php
   $mailheaders = "Reply-To: $_POST[sender_email]";
   ```
2. 添加 `mail()` 函数：
   ```php
   mail($to, $subject, $msg, $mailheaders);
   ```
3. 关闭你的 PHP 块：
   ```php
   ?>
   ```

虽然这段代码会发送邮件，但你应该向用户的屏幕返回一些内容，以便他知道表单已经发送成功。否则，他可能会坐在那里不断点击“提交表单”按钮。

开始 HTML 输出：

1. `<HTML>`
2. `<HEAD>`
3. `<TITLE>反馈表单已发送</TITLE>`
4. `</HEAD>`
5. `<BODY>`
6. 添加一些信息告诉用户发生了什么：
   `<h1>邮件已发送!</h1>`
7. 为 Name 字段添加标签并显示用户的输入：
   `<strong>您的姓名：</strong><br>`
   `<?php echo $_POST['sender_name']; ?>`
8. 为 E-Mail Address 字段添加标签并显示用户的：
   `<strong>您的邮箱：</strong><br>`
   `<?php echo $_POST['sender_email']; ?>`
9. 为 Message 字段添加标签并显示用户的输入：
   `<strong>消息：</strong><br>`
   `<?php echo $_POST['message']; ?>`
10. 添加更多 HTML 使文档有效：
    `</body>`
    `</html>`

完整代码示例：

```php
<?php
// 邮件发自来自您的网站
$to = $_POST['sender_email'];
$sender = $_POST['sender_name'];
$message = $_POST['message'];
$subject = "来自我的网站";
$mailheaders = "Reply-To: $sender";
mail($to, $subject, $message, $mailheaders);
?>
<html>
<head>
<title>反馈表单已发送</title>
</head>
<body>
<p>以下邮件已发送：</p>
<p><strong>您的姓名：</strong><br>
<?php echo $sender; ?></p>
<p><strong>您的邮箱：</strong><br>
<?php echo $to; ?></p>
<p><strong>消息：</strong><br>
<?php echo $message; ?></p>
</body>
</html>
```

将文件保存为 `send_simpleform.php`，并将此文件放置在你的 Web 服务器的文档根目录下。

## 提交表单并获取结果

现在你已经创建了前端表单和后端脚本，是时候尝试它们了。

1. 打开 浏览器并输入 `http://127.0.0.1/simple_form.html`
2. 在 Your Name 字段中输入你的名字。
3. 在 E-Mail Address 字段中输入你的邮箱。
4. 在 Message 字段中输入以下消息：
   ```
   PHP 太酷了！
   ```
5. 点击“提交表单”按钮。

现在检查你的邮箱，看看是否有消息在等待你。

1. 在你的文本编辑器中打开 `send_simpleform.php`。
2. 修改包含发送者姓名的字符串，将制表符 (`\t`) 替换为两个空格：
   `$msg = "Sender's Name: $_POST['sender_name']";`
3. 修改包含发送者邮箱的字符串，将制表符 (`\t`) 替换为四个空格：
   `$msg = "Sender's E-Mail: $_POST['sender_email']";`
4. 修改包含消息的字符串，将制表符 (`\t`) 替换为10个空格：
   `$msg = "Message: $_POST['message']\n\n";`
5. 保存文件。

这段新代码看起来应该像这样。

```php
<?php
$sender_name = $_POST['sender_name'];
$sender_email = $_POST['sender_email'];
$message = $_POST['message'];

if ($sender_name == "" || $sender_email == "") {
    header("Location:http://127.0.0.1/simple_form.html");
    exit;
}
?>
```

再次提交表单。当你收到邮件时，这次所有内容都对齐了。

就像书中的之前的脚本一样，你应该为 `send_simpleform.php` 添加一些错误检查。在执行任何操作之前，检查 `$_POST['sender_name']`、`$_POST['sender_email']` 和 `$_POST['message']` 是否都有值。在第一个 PHP 标签之后添加：

```php
if ($_POST['sender_name'] == "" || $_POST['sender_email'] == "") {
    header("Location:http://127.0.0.1/simple_form.html");
    exit;
}
```

在下一节中，你将在字段为空时创建自定义错误消息，并将发送邮件的两个步骤合并为一个。

### 带有错误消息的反馈表单

在上一节中，你创建了两个独立的文件。一个包含前端（表单），另一个包含后端（脚本）。在这一节中，你将学习如何在表单动作中使用 `$_SERVER['PHP_SELF']` 变量来创建一个同时包含表单和脚本的单一，以及在字段未填写时创建自定义错误消息。

#### 创建初始脚本

1. 在你的文本编辑器中打开一个文件。
2. 输入以下 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>一体反馈表单</TITLE>
   </HEAD>
   <BODY>
   ```
3. 开始 PHP 块，创建一个名为 `$form_block` 的变量，包含整个表单。开始表单动作，假设方法为 POST，动作为 `$_SERVER['PHP_SELF']`：
   ```php
   <?php
   $form_block = "
   <FORM METHOD=\"POST\" ACTION=\"$_SERVER[PHP_SELF]\">
   ```
   提示：由于将字符串放在变量中，可能会有两个引号。记得用反斜杠转义你的引号！
4. 为用户的姓名创建一个输入字段并带有标签：
   ```html
   <p><strong>您的姓名：</strong><br>
   <INPUT type="text" NAME="sender_name" SIZE=30></p>
   ```
5. 为用户的邮箱创建一个输入字段并带有标签：
   ```html
   <p><strong>您的邮箱：</strong><br>
   <INPUT type="text" NAME="sender_email" SIZE=30></p>
   ```
6. 为消息创建一个文本区域并带有标签：
   ```html
   <TEXTAREA name="message"<br>
   COLS=30 ROWS=5 WRAP="virtual">
   </TEXTAREA></p>
   ```
7. 添加提交按钮：
   ```html
   <INPUT TYPE="submit" NAME="submit" VALUE="提交表单"></p>
   ```
8. 关闭表单，添加结束引号和终止符（分号）；
   ```html
   </FORM>
   ```
9. 关闭 PHP 块，然后添加更多 HTML 使文档有效：
   ```php
   ?>
   </body>
   </html>
   ```
10. 将文件保存为 `allinone_form.php`。

如果你在浏览器中查看这段代码，你只会在标题栏看到一个标题。这个问题应该是：“为什么我们需要把 HTML 放在一个名为 `$form_block` 的变量中？”在下一节中，你将向脚本添加内容，根据某些操作显示特定的代码块。字符串 `$form_block` 就是其中之一。

#### 在脚本中添加错误检查

计划是使用全局变量 `$_SERVER['PHP_SELF']`，它的值是脚本的名字。在这种情况下，`$_SERVER['PHP_SELF']` 的值为 `allinone_form.php`。当你使用 `$_SERVER['PHP_SELF']` 作为表单动作时，你是在说“点击提交按钮时，重新运行此脚本并执行操作”，而不是“点击提交按钮时，找到另一个脚本并执行操作”。

现在你有一个脚本的壳，思考这个一体化脚本必须做什么：

- 显示表单
- 提交表单
- 检查错误
- 在不发送表单的情况下打印错误
- 如果未发现错误则提交表单

在提交按钮的 HTML 代码之前，对脚本进行一些修改以辅助 `$form_block` 变量。添加此行：

```html
<INPUT type="hidden" name="op" value="ds">
```

此行创建了一个隐藏变量 `$_POST['op']`，其值为 `ds`。“op”代表 operation（操作），“ds”代表 do something（执行）。这些名字是我起的；它们与任何编程语言无关。你可以随意命名，只要你理解它们的作用（你很快就会看到）。

`$_POST['op']` 变量只有在表单提交后才会存在。因此，如果 `$_POST['op']` 的值不是 `ds`，用户还没有看到表单。如果用户还没有看到表单，我们需要显示它，因此在 PHP 块结束之前添加以下 else 语句：

```php
if ($_POST['op'] != "ds") {
    // 他们需要看到表单
    echo "$form_block";
}
```

你将在下一步对脚本进行更多修改以添加你的错误消息。表单已提交，`$_POST['op']` 的值将是 `ds`，现在你必须考虑到这一点。假设所有表单字段都是必填的；在检查了 `$_POST['op']` 的值后，你将检查所有字段的值。

1. 继续 `if...else` 语句：
   ```php
   else if ($_POST['op'] == "ds") {
   ```
2. 在父语句内添加 `if` 语句来检查值。从 `$_POST['sender_name']` 开始：
   ```php
   if ($_POST['sender_name'] == "") {
   ```
3. 为 `$_POST['sender_name']` 创建一个名为 `$name_error` 的错误消息：
   ```php
   $name_error = "<font color=red>请输入您的姓名!</font><br>";
   ```
4. 将 `$send` 设为 `no`：
   ```php
   $send = "no";
   ```
5. 为 `$_POST['sender_email']` 创建类似的语句：
   ```php
   if ($_POST['sender_email'] == "") {
       $email_error = "<font color=red>请输入您的邮箱</font><br>";
       $send = "no";
   }
   ```
6. 为 `$_POST['message']` 创建一个类似的语句：
   ```php
   if ($_POST['message'] == "") {
       $message_err = "<font color=red>请输入消息!</font>";
       $send = "no";
   }
   ```
7. 启动一个 `if...else` 语句来处理 `$send` 的值：
   ```php
   if ($send != "no") {
       // 如果可以发送
       // 创建一个变量来存储接收者的电子邮件地址（替换为您自己的）：
       $to = "you@youmail.com";
       // 创建一个变量来存储邮件主题：
       $subject = "All-In-One Site Feedback";
       // 创建一个变量来存储额外的邮件头：
       $mailheaders = "From: My Web Site <>\n";
       // 向 mailheaders 变量添加内容：
       $mailheaders .= "Reply-To: $_POST['sender_email']\n";
       // 构建邮件正文字符串：
       $msg = "E-MAIL STRING FROM WWW SITE\n";
       $msg .= "Sender's Name: $_POST['sender_name']\n";
       $msg .= "Sender's E-Mail: $_POST['sender_email']\n";
       $msg .= "Message: $_POST['message']\n";
       // 添加 mail 函数：
       mail($to, $subject, $msg, $mailheaders);
       // 添加一个简单的语句让用户知道邮件已发送，并关闭 if 语句：
       echo "<p>Your mail has been sent!</p>";
   }
   ```
8. 继续 `if...else` 语句来处理 `$send` 值为 `no` 的情况：
   ```php
   else if ($send == "no") {
       // 打印错误信息：
       echo "$name_error";
       echo "$email_error";
       echo "$message_err";
       // 再次打印表单：
       echo "$form_block";
       // 关闭当前的 if...else 块：
   }
   ```
9. 关闭父级 `if...else` 块：
   ```php
   }
   ```
10. 保存文件。

整个代码看起来应该是这样的：

```html
<HTML>
<HEAD>
<TITLE>All-In-One Feedback Form</TITLE>
</HEAD>
<body>
<?php
$form_block = "
<FORM METHOD=\"POST\" ACTION=\"$_SERVER[PHP_SELF]\">\n
<p><strong>Your Name:</strong><br>
<INPUT type=\"text\" NAME=\"sender_name\" SIZE=30></P>
<P><strong>Your E Mail Address:</strong><br>
<INPUT type=\"text\" NAME=\"sender_email\" SIZE=30></P>
<P><strong>Message:</strong><br>
<TEXTAREA NAME=\"message\" COLS=30 ROWS=5 WRAP=virtual>
</TEXTAREA>
<INPUT type=\"hidden\" name=\"op\" value=\"ds\">
<P><INPUT type=\"submit\" NAME=\"submit\" VALUE=\"Send This Form\"></P>
";
<?php
if ($_POST['op'] != "ds") {
    // 我们需要看到表单
    echo "$form_block";
} else if ($_POST['op'] == "ds") {
    // 检查 $_POST['sender_name'] 的值
    if ($_POST['sender_name'] == "") {
        $name_err = "<font color=red>请输入您的姓名!</font><br>";
        $send = "no";
    }
    // 检查 $_POST['sender_email'] 的值
    if ($_POST['sender_email'] == "") {
        $email_err = "<font color=red>请输入您的电子邮件地址</font><br>";
        $send = "no";
    }
    // 检查 $_POST['message'] 的值
    if ($_POST['message'] == "") {
        $message_err = "<font color=red>请输入消息!</font><br>";
        $send = "no";
    }
    if ($send != "no") {
        // 可以发送，构建邮件
        $msg = "E-MAIL SENT FROM WWW SITE\n";
        $msg .= "Sender's Name: $_POST['sender_name']\n";
        $msg .= "Sender's E-Mail: $_POST['sender_email']\n";
        $msg .= "Message: $_POST['message']\n";
        $to = "you@yourdomain.com";
        $subject = "All-in-One Web Site Feedback";
        $mailheaders = "From: My Web Site <>\n";
        $mailheaders .= "Reply-To: $_POST['sender_email']\n";
        // 发送邮件
        mail($to, $subject, $msg, $mailheaders);
        // 向用户显示确认
        echo "<p>Mail has been sent!</p>";
    } else if ($send == "no") {
        // 打印错误信息
        echo "$name_err";
        echo "$email_err";
        echo "$message_err";
        echo "$form_block";
    }
}
?>
```

## 提交表单并获取结果

现在你已经创建了前端表单和后端脚本，是时候尝试一下它们了：

1. 打开浏览器并输入 `http://127.0.0.1/allinone_form.php`
2. 在任何字段中都不输入内容并提交表单。
3. 在 Name 字段输入你的姓名并提交表单。
4. 在 Name 字段输入姓名，在 E-Mail 字段输入电子邮件，然后提交表单。
5. 在 Name 字段输入姓名，在 E-Mail 字段输入电子邮件，并输入以下消息：**这种合一功能非常酷！**
6. 提交表单。

## 保存生成的值

你可能在原始脚本中注意到，如果你发生了错误，表单会重置导致你会丢失值。对 `$form_block` 进行简单的修改即可解决这个问题。只需为表单字段添加 `VALUE` 属性来保留之前的值：

1. 在文本编辑器中打开 `allinone_form.php`。
2. 在 `$form_block` 变量内部，修改 Name 字段：
   `<INPUT type="text" name="sender_name" VALUE="<?php echo $_POST['sender_name']; ?>" SIZE=30></P>`
3. 修改 E-Mail Address 字段：
   `<INPUT type="text" name="sender_email" VALUE="<?php echo $_POST['sender_email']; ?>" SIZE=30></P>`
4. 修改 Message 文本区域：
   `<TEXTAREA NAME="message" COLS=5 ROWS=5 WRAP=virtual><?php echo $_POST['message']; ?></TEXTAREA>`

注意：`TEXTAREA` 没有 `VALUE` 属性。相反，值位于标签标签之间。

5. 保存文件，然后打开浏览器并输入 `http://127.0.0.1/allinone_form.php`。
6. 在 Name 字段输入姓名并提交表单。

对表单中的其他字段重复此过程以验证值已保存。

## 第 9 章：使用你的文件系统

### 概述

使用简单的 PHP 脚本，你可以对文件系统进行任何操作——毕竟它是你的！在本章中，你将学习如何：

- 显示目录内容
- 创建新文件
- 打开现有文件并追加数据
- 复制、重命名和删除文件

### 文件路径与权限

这些章节使用的脚本可以在 Windows 和 Linux/UNIX 系统上执行。如果你使用 Windows，路径中可以使用正斜杠 (`/`) 和反斜杠 (`\`)，而其他操作系统只使用正斜杠。本章中的脚本在所有情况下都使用正斜杠方法。即使你不指定驱动器号，方法也有效。例如：

```php
$path = "/Program Files/Apache/htdocs";
```

此路径在 Windows 上假设位于当前驱动器（在我的情况下是 `C:/`）。如果你需要指定驱动器号，可以使用：

```php
$path = "C:/Program Files/Apache/htdocs/";
```

你必须修改文件路径以适应你的目录结构，但不需要做更多。对于本章中指定的每个目录，你必须拥有创建、修改和删除文件的权限。对于 Windows 用户来说这是一个特别重要的说明，因为他们的操作系统本质上是多用户的。如果你不如何在系统上分配或修改权限，请联系你的系统管理员。

### 显示目录内容

尽管可能难以相信，这个脚本将是本章中最复杂的，但它只有 32 行！目标是打开目录，找到目录下所有文件的名称。

1. 在文本编辑器中打开新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量来存储目录的完整路径：
   ```php
   $dir_name = "/My Documents/misc/";
   ```
   注意：这个目录是我机器上存在的。请替换为你自己的目录名称以便正常运行！
3. 创建句柄并使用 `opendir()` 函数打开步骤 2 中指定的目录：
   ```php
   $dir = opendir($dir_name);
   ```
   注意，术语 handle 将用于指代后续目录函数中打开的目录。
4. 你最终会将结果放在名为 `$file_list` 的字符串内的无序列表中。开始该无序列表：
   ```php
   $file_list = "<ul>";
   ```
5. 启动一个循环，使用 `readdir()` 函数决定何时停止。`readdir()` 函数返回目录中的下一个文件名，在本例中将其赋值给变量：
   ```php
   while ($file_name = readdir($dir)) {
   ```
6. 使用 `if` 语句去掉 `"."` 和 `".."` 文件名：
   ```php
   if ($file_name != "." && $file_name != "..") {
   ```
7. 如果 `$file_name` 不是“点”文件名，使用拼接运算符将其添加到 `$file_list`：
   ```php
   $file_list .= "<li>" . $file_name . "</li>";
   ```
8. 关闭 `if` 语句和 `while` 循环：
   ```php
   }
   }
   ```
9. 为无序列表添加结束标签：
   ```php
   $file_list .= "</ul>";
   ```
10. 关闭目录：
    ```php
    closedir($dir);
    ```
11. 关闭你的 PHP 块，然后添加 HTML 开始显示：
    ```php
    ?>
    <HTML>
    <HEAD>
    <TITLE>Directory Listing</TITLE>
    </HEAD>
    <body>
    ```
12. 混合一些 HTML 和 PHP 来打印你刚刚读取的目录名称：
    `<P>Files in: <?php echo "$dir_name"; ?></P>`
13. 打印文件列表，然后关闭 HTML 标签以确保文档有效：
    `<P><?php echo "$file_list"; ?></P>
    </BODY>
    </HTML>`
14. 将文件保存为 `listfiles.php`。

假设此方法有效，请在系统中的其他目录上进行尝试。如果目录不存在，脚本不会报错——只是没有任何结果。

在下一节中，你将学习使用 `fopen()` 和 `fclose()` 函数来打开和关闭特定文件。

### 使用 fopen() 和 fclose()

在深入学习文件之前，你需要稍微了解一下 `fopen()` 函数，它用于打开文件。该函数需要一个文件名和模式，并返回一个文件指针。文件指针提供了有关文件的信息，并用作引用。

文件名是你想要创建或打开文件的完整路径，模式可以是表 9.1 中列出的任何模式之一。

**表 9.1：配合 `fopen()` 使用的模式**

| 模式 | 用法 |
| --- | --- |
| `r` | 打开已存在的文件并从其中读取数据。文件指针放在文件开头。 |
| `r+` | 打开已存在的文件用于读取或写入。文件指针放在文件开头。 |
| `w` | 打开文件用于写入。如果不存在同名文件，该函数创建一个新文件。如果文件存在，该函数将删除所有现有内容并将文件指针放在文件开头。 |
| `w+` | 打开文件用于读写。如果不存在同名文件，该函数创建一个新文件。如果文件存在，该函数将删除所有现有内容并将文件指针放在文件开头。 |
| `a` | 打开文件用于写入。如果不存在同名文件，该函数创建一个新文件。如果文件存在，该函数将文件指针放在文件末尾。 |
| `a+` | 打开文件用于读写。如果不存在同名文件，该函数尝试创建一个新文件。如果文件存在，该函数将文件指针放在文件末尾。 |

### 创建新文件

与本章的第一节相比，下一个任务将轻而易举。目标是在指定位置创建一个新的空文件。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量来存储文件的完整路径：
   ```php
   $filename = "My Documents/mydata.txt";
   ```
   注意这个目录是我自己机器上存在的。请替换为你自己的目录名以便运行！
3. 创建一个文件指针并使用 `fopen()` 函数打开步骤 3 中指定的文件以进行读写。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。
   ```php
   $newfile = fopen($filename, "w+") or die("Could not create file.");
   ```
   注意该文件指针将在后续的文件相关函数中引用已打开的文件。
4. 关闭文件指针：
   ```php
   fclose($newfile);
   ```
5. 创建一个成功后要打印的消息，然后关闭你的 PHP 块：
   ```php
   $msg = "<p>File created!</p>";
   ?>
   ```
6. 添加此 HTML：
   ```html
   <html>
   <HEAD>
   <TITLE>Creating a New File</TITLE>
   </HEAD>
   <body>
   ```
7. 打印消息：
   ```php
   <?php echo "$msg"; ?>
   ```
8. 添加更多 HTML 以使文档有效：
   ```html
   </body>
   </HTML>
   ```
9. 将文件保存为 `newfile.php` 并将其置于你的 Web 服务器的文档根目录下。
10. 打开你的 Web 浏览器并输入 `http://127.0.0.1/newfile.php`

然而，如果文件创建失败，你将看到一个糟糕的解析错误。你可以通过对 `$filename` 使用一个无效值来强制产生错误，例如：

```php
$filename = "bozo/mydata.txt";
```

当你运行脚本时，你会看到类似以上的内容。

虽然 `die()` 函数通过打印指定的消息完成了它的工作，但你可以通过在函数前使用 `@` 符号来抑制错误和警告，从而避免这种凌乱。

**修改此行**

```php
$newfile = fopen($filename, "w+") or die("Couldn't create file.");
```

**修改为：**

```php
$newfile = @fopen($filename, "w+") or die("Couldn't create file.");
```

保存文件并通过你的 Web 浏览器访问脚本。你现在将只会看到来自 `die()` 函数的消息，而没有其他警告。

### 检查文件是否已存在

为了避免在文件系统中操作时出现任何可能的管理错误，你可以使用 `file_exists()` 函数在创建文件之前检查文件是否存在。下一个脚本将执行此操作并无论如何都会打印消息。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量来存储文件的完整路径（使用你自己的文件路径）：
   ```php
   $filename = "My Documents/mydata.txt";
   ```
3. 使用 `file_exists()` 检查文件是否存在：
   ```php
   if (file_exists($filename)) {
       $msg = "<p>File already exists!</p>";
   } else {
       $newfile = @fopen($filename, "w+") or die("Couldn't create file.");
       fclose($newfile);
       $msg = "<p>File created!</p>";
   }
   ?>
   ```
4. 添加 HTML 显示结果：
   ```html
   <html>
   <HEAD>
   <TITLE>Checking File Existence</TITLE>
   </HEAD>
   <body>
   <?php echo "$msg"; ?>
   </body>
   </HTML>
   ```
5. 将文件保存为 `checkfile.php` 并将其置于你的 Web 服务器的文档根目录下。
6. 打开你的 Web 浏览器并输入 `http://127.0.0.1/checkfile.php`

### 向文件追加数据

下一个脚本的目标是向文件追加数据。如果文件存在，脚本将直接写入。如果文件不存在，则在写入之前会创建它。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量来存储文件的完整路径（使用你自己的文件路径）：
   ```php
   $filename = "My Documents/textfile.txt";
   ```
3. 创建一个文件指针并使用 `fopen()` 函数打开文件以进行追加（模式 `"a"`）。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。
   ```php
   $fp = @fopen($filename, "a") or die("Couldn't open file");
   ```
4. 定义要写入的数据：
   ```php
   $data = "Appended data: " . date("Y-m-d H:i:s") . "\n";
   ```
5. 使用 `fwrite()` 写入数据：
   ```php
   fwrite($fp, $data);
   ```
6. 关闭文件指针：
   ```php
   fclose($fp);
   ```
7. 创建成功消息并关闭 PHP 块：
   ```php
   $msg = "<p>Data appended to file!</p>";
   ?>
   ```
8. 添加 HTML 显示结果：
   ```html
   <HTML>
   <HEAD>
   <TITLE>Appending Data to a File</TITLE>
   </HEAD>
   <body>
   <?php echo "$msg"; ?>
   </body>
   </HTML>
   ```
9. 将文件保存为 `appendfile.php` 并将其置于你的 Web 服务器的文档根目录下。
10. 打开 Web 浏览器并输入 `http://127.0.0.1/appendfile.php`

![](img/bc248f3d24697d1afbacee37b9c4d229_97_0.png)

在下一节中，你将从该脚本创建的文件读取数据。

### 从文件中读取数据

你需要一个脚本来读取你在上一节中创建的文件中的数据。你可以直接在文本编辑器中打开文件指针，但那样有什么好玩的呢？PHP 有一个方便的函数 `fread()` 可以为你完成这项工作。

1. 在你的文本编辑器中打开一个文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量来存储你在上一节中创建的文件完整路径（使用你自己的路径）；
   ```php
   $filename = "My Documents/textfile.txt";
   ```
3. 创建一个文件指针并使用 `fopen()` 函数打开指定文件（只读模式）。如果文件没有正常打开，`die()` 函数会导致脚本结束并显示消息。
   ```php
   $whatread = @fopen($filename, "r") or die("Couldn't open file");
   ```
4. 创建一个变量 `$file_contents`，并使用 `fread()` 函数从文件指针 (`$whatread`) 中读取所有行，直到文件中没有行为止：
   ```php
   $file_contents = fread($whatread, filesize($filename));
   ```
   注意：对现有文件使用 `filesize()` 让 PHP 为你完成工作。`fread()` 的第二个参数是文件的长度。如果你不知道长度，但知道全部内容，可以使用 `filesize($filename)` 来获取该长度。
5. 创建一个变量来打印消息，包括文件的内容：
   ```php
   $msg = "The file contains:<br>$file_contents";
   ```
6. 关闭文件指针和你的 PHP 块：
   ```php
   fclose($whatread);
   ?>
   ```
7. 添加此 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>Reading Data From a File</TITLE>
   </HEAD>
   <body>
   ```
8. 打印消息：
   ```php
   <?php echo "$msg"; ?>
   ```
9. 添加更多 HTML 以使文档有效：
   ```html
   </BODY>
   </HTML>
   ```
10. 将文件保存为 `readdata.php` 并将此文件放在 Web 服务器的文档根目录下。
11. 打开 Web 浏览器并输入 `http://127.0.0.1/readdata.php`

![](img/bc248f3d24697d1afbacee37b9c4d229_98_0.png)

这确实是写入文件的字符串，但那个换行符去哪里了？换行字符对 Web 浏览器没有意义，因为它只渲染 HTML。幸运的是，PHP 开发团队很有远见，创建了 `nl2br()` 函数（new-line-to-break；懂了吗？）。对 `readdata.php` 脚本进行一些调整：

1. 在包含 `fread()` 函数的行之后添加此行：
   ```php
   $new_file_contents = nl2br($file_contents);
   ```
2. 修改 `$msg` 字符串使其看起来像这样：
   ```php
   $msg = "The file contains:<br>$new_file_contents";
   ```
3. 保存文件。

![](img/bc248f3d24697d1afbacee37b9c4d229_98_1.png)

在下一节中，你将读取相同的消息，但不是将其打印在屏幕上，而是通过电子邮件发送。

### 通过电子邮件发送文件内容

如果你将 HTML 表单的结果保存到纯文本文件中，并且你只想在特定时间读取它，可以编写一个小脚本，根据需要将文件内容邮寄给你。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量存储包含数据的文件完整路径（使用你自己的路径）：
   ```php
   $filename = "/My Documents/textfile.txt";
   ```
3. 创建一个文件指针并使用 `fopen()` 函数打开指定文件（只读模式）。如果文件没有正常打开，`die()` 函数会导致脚本结束并显示消息。
   ```php
   $whatread = @fopen($filename, "r") or die("Couldn't open file");
   ```
4. 创建一个变量 `$file_contents`，并使用 `fread()` 函数从文件指针 (`$whatread`) 中读取所有行，直到文件中没有行为止：
   ```php
   $file_contents = fread($whatread, filesize($filename));
   ```
5. 创建一个变量存储你的电子邮件地址：
   ```php
   $to = "you@yourdomain.com";
   ```
6. 创建一个存储邮件主题的变量：
   ```php
   $subject = "File Contents";
   ```
7. 创建一个存储额外邮件头的变量：
   ```php
   $mailheaders = "From: My Web Site <>\n";
   ```
8. 使用 `$file_contents` 字符串作为第三参数填充 `mail()` 函数：
   ```php
   mail($to, $subject, $file_contents, $mailheaders);
   ```
9. 创建一个变量在屏幕上打印消息：
   ```php
   $msg = "<p>Check your mail!</p>";
   ```
10. 关闭文件指针和你的 PHP 块：
    ```php
    fclose($whatread);
    ?>
    ```
11. 添加此 HTML：
    ```html
    <HTML>
    <HEAD>
    <TITLE>Mailing Data from a File</TITLE>
    </HEAD>
    <body>
    ```
12. 打印消息：
    ```php
    <?php echo $msg; ?>
    ```
13. 添加更多 HTML 使文档有效：
    ```html
    </body>
    </HTML>
    ```
14. 将文件保存为 `mailcontents.php` 并将此文件放在 Web 服务器的文档根目录下。

![](img/bc248f3d24697d1afbacee37b9c4d229_99_0.png)

15. 打开 Web 浏览器并输入 `http://127.0.0.1/mailcontents.php`

正如消息所示，检查邮件。

### 文件系统操作

接下来脚本将帮助你执行文件系统任务，如复制、重命名和删除文件。记住，只有当用户拥有适当权限才能执行文件系统函数。

#### 复制文件

`copy()` 函数非常简单：它只需要知道原始文件名和新文件名。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量存储原始文件的完整路径（使用你自己的路径）；
   ```php
   $orig_filename = "/My Documents/textfile.txt";
   ```
3. 创建一个变量存储新文件的完整路径（使用你自己的路径）；
   ```php
   $new_filename = "/My Documents/textfile.bak";
   ```
4. 创建一个变量存储函数的真/假结果。在函数前使用 `@` 抑制警告，并在函数失败时使用 `die()` 打印消息：
   ```php
   $success = @copy($orig_filename, $new_filename) or die("Couldn't copy file.");
   ```
5. 一个 `if...else` 语句根据函数的输出打印适当的消息：
   ```php
   if ($success) {
       // 如果成功，消息字符串应该打印复制的确认：
       $msg = "Copied $orig_filename to $new_filename";
   } else {
       $msg = "Could not copy file.";
   }
   ```
   注意：这里的 `else` 语句实际上是不必要的，但它是提供默认结果的良好做法。如果 `copy()` 函数失败，`die()` 函数将退出脚本并在到达 `if...else` 部分之前打印错误。
6. 添加此 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>Copy a File</TITLE>
   </HEAD>
   <body>
   ```
7. 打印消息：
   ```php
   <?php echo "$msg"; ?>
   ```
8. 添加更多 HTML 使文档有效：
   ```html
   </body>
   </HTML>
   ```
9. 将文件保存为 `copyfile.php` 并将此文件放在 Web 服务器的文档根目录下。

![](img/bc248f3d24697d1afbacee37b9c4d229_101_0.png)

10. 打开 Web 浏览器并输入 `http://127.0.0.1/copyfile.php`

通过将 `$new_filename` 的值为一个不存在的内容，查看你的错误处理是否有效：

```php
$new_filename = "bozo/textfile.bak";
```

![](img/bc248f3d24697d1afbacee37b9c4d229_101_1.png)

接下来，处理重命名文件。脚本非常相似！

#### 重命名文件

与 `copy()` 函数一样，`rename()` 函数只需要知道原始文件名和新文件名。在这种情况下，你是在重命名原始文件而不是复制它。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```
2. 创建一个变量存储原始文件的完整路径（使用你自己的路径）：
   ```php
   $orig_filename = "/My Documents/textfile.bak";
   ```
3. 创建一个变量存储新文件的完整路径（使用你自己的路径）：
   ```php
   $new_filename = "/My Documents/textfile.old";
   ```
4. 创建一个变量存储函数的真/假结果。在函数前使用 `@` 抑制警告，并在函数失败时使用 `die()` 打印消息：
   ```php
   $success = @rename($orig_filename, $new_filename) or die("Couldn't rename file.");
   ```
5. 一个 `if...else` 语句根据函数的输出打印适当的消息：
   ```php
   if ($success) {
       $msg = "Renamed $orig_filename to $new_filename";
   } else {
       $msg = "Could not rename file.";
   }
   ```
6. 添加 HTML 显示结果：
   ```html
   <HTML>
   <HEAD>
   <TITLE>Rename a File</TITLE>
   </HEAD>
   <body>
   <?php echo "$msg"; ?>
   </body>
   </HTML>
   ```
7. 将文件保存为 `renamefile.php` 并将其置于 Web 服务器的文档根目录下。
8. 打开 Web 浏览器并输入 `http://127.0.0.1/renamefile.php`



7. 创建一个变量存储函数的真/假结果。在函数前使用 `@` 抑制警告，并在函数失败时使用 `die()` 打印消息：

8. `$success = @rename($orig_filename, $new_filename) or die("Couldn't rename file.");`

9. 一个 `if...else` 语句根据函数的输出打印适当的消息：

10. `if ($success) {`

11. 如果成功，消息字符串应该打印重命名的确认：

12. `$msg = "Renamed $orig_filename to $new_filename";`

13. 继续失败的语句，然后关闭 PHP 块：

14. `else {`

15. `$msg = "Could not rename file.";`

16. `}`

17. `?>`

18. 添加此 HTML：

```
<HTML>
<HEAD>
<TITLE>Rename a File</TITLE>
</HEAD>
<body>
打印消息：
<?php echo "$msg"; ?>
</body>
</HTML>
```

12. 打开你的 Web 浏览器并输入 http://127.0.0.1/renamefile.php

通过将 $new_filename 的值更改为某个不存在的内容，检查你的错误处理是否正常工作：

```php
$new_filename = "bozo/textfile.bak"; // 通过 Web 浏览器访问该脚本，你应该能看到这个。
```

在下一节中还有最后一个清理函数：删除文件。

## 删除文件

使用 `unlink()` 函数时务必非常小心，因为你删除了一个文件，它将永久消失。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

2. `<?php`

3. 创建一个变量来存储要删除的文件的完整路径（使用你的路径）：

4. `$filename = "My Documents/textfile.old";`

5. 创建一个变量来存储函数的真/假结果。在函数前使用 `@` 抑制警告，并在函数失败时使用 `die()` 打印消息：

6. `$success = @unlink($filename) or die("Couldn't delete file.");`

7. 开始一个 if...else 语句，根据函数的结果打印适当的消息：

8. `if ($success) {`

9. 如果成功，消息字符串应该打印删除确认：

10. `$msg = "Deleted $filename";`

11. 继续编写失败情况的语句，然后关闭你的 PHP 块：

12. `} else {`

13. `$msg = "Could not delete file.";`

14. `}`

15. `?>`

注意：在这种情况下使用 `else` 语句实际上是没必要的，但作为提供默认结果的方法这是一种良好的习惯。如果 `unlink()` 函数失败，`die()` 函数将退出脚本并在进入脚本的 if...else 部分之前打印错误。

18. 添加此 HTML：

```
<HTML>
<HEAD>
<TITLE>Delete a File</TITLE>
</HEAD>
<BODY>
打印消息：
<?php echo "$msg"; ?>
</BODY>
</HTML>
```

30. 将文件保存为 deletefile.php，并将此文件放置在你的 Web 服务器的文档根目录下。

31. 打开你的 Web 浏览器并输入 http://127.0.0.1/deletefile.php

通过将 $filename 的值更改为某个不存在的内容，检查你的错误处理是否正常：

`$filename = "/bozo/textfile.old";` 通过 Web 浏览器访问该脚本，你应该能看到这个。

在下一章中，你将创建一个两步处理过程（前端表单和后端脚本），以启动从 Web 浏览器到你的文件系统的文件上传。

## 第 10 章：将文件上传到你的网站

## 概述

如果你需要一个从远程位置向你的网站上传文件的快速接口，可以使用 PHP 创建一个两步表单和脚本接口。在本章中，你将学习执行以下操作：

- 创建用于文件上传的 HTML 表单

- 创建处理文件上传的 PHP 脚本

## 检查你的 php.ini 文件

在上传文件之前，检查 `php.ini` 文件中的几个值。寻找这段文本内容：

```
; File Uploads ;
; 是否允许 HTTP 文件上传。
file_uploads = On

; HTTP 上传文件的临时目录（如果未
; 指定，将使用系统
; 默认）；
upload_tmp_dir =

; 允许上传的文件的最大大小。
upload_max_filesize = 2M
```

为了确保过程顺利运行，请进行以下修改：

- 通过删除开头的分号来取消 `upload_tmp_dir` 行的注释。

- 在 `= upload_tmp_dir` 之后输入目录名称。

- 如果你想允许更大的上传，请更改 `upload_max_filesize` 的字节数。

例如，在 Windows 系统上，`php.ini` 文件的此部分可能如下：

```ini
; File Uploads ;
; 是否允许 HTTP 文件上传。
file_uploads = On

; HTTP 上传文件的临时目录（如果未
; 指定，将使用系统
; 默认）。
upload_tmp_dir = /Windows/temp
; 允许上传的文件的最大大小。
upload_max_filesize = 2M
```

如果你没有使用 Windows，只要你想让文件存放在 /tmp（默认），就不需要修改 `upload_tmp_dir` 的值。

## 理解该过程

通过 HTML 接口向 Web 服务器上传文件的过程让许多人感到困惑。花一点时间理解你将在这些节中将创建的过程。要开始并完成此过程，你需要：

- 一个 HTML 表单

- 一个要上传的文件

- 一个存放文件的地方

- 一个用来存放它的脚本

该过程本身的访问方式如下：

1. 用户访问 HTML 表单，并在其浏览器中看到一个文本字段和一个“浏览”按钮。

2. 用户在硬盘中浏览其想要上传的文件并选择一个文件。

3. 完整的文件路径和名称将出现在文本字段中。

4. 用户点击“提交”按钮。

5. 选择的文件发送出去，到达 Web 服务器并停留在临时目录中。

6. 表单 `action` 中使用的 PHP 脚本检查是否发送了文件。

7. PHP 脚本检查文件已发送后，将其放入临时目录。它在临时目录中等待。

8. 注意：运行 PHP 的用户（如 www-data）必须对该临时目录具有写入权限。

## 创建表单

通过创建一个 HTML 表单来开始并完成此过程。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

2. `<?php`

3. 添加以下 HTML：

4. `<HTML>`

5. `<HEAD>`

6. `<TITLE>Upload a File</TITLE>`

7. `</HEAD>`

8. `<BODY>`

9. 打印消息：

10. `<?php echo "$msg"; ?>`

11.

12. 添加更多 HTML 以使文档有效：

13. `</BODY>`

14. `</HTML>`

15. 将文件保存为 upload.php，并将此文件放置在你的 Web 服务器的文档根目录下。

16. 打开你的 Web 浏览器并输入 http://127.0.0.1/upload.php

17. 看到表单。

18. 创建一个脚本来处理文件上传：

19. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

20. `<?php`

21. 创建一个变量来存储消息：

22. `$msg = "";`

23. 创建一个变量来存储要上传的文件的路径：

24. `$filename = $_FILES["img1"]["name"];`

25. 创建一个变量来存储函数的真/假结果。在函数前使用 `@` 抑制警告，并在函数失败时使用 `die()` 打印消息：

26. `$success = @copy($_FILES["img1"]["tmp_name"], "/var/www/html/uploads/" . $_FILES["img1"]["name"]) or die("Couldn't copy file.");`

27. 开始一个 if...else 语句，根据函数的结果打印适当的消息：

28. `if ($success) {`

29. 如果成功，消息字符串应该打印删除确认：

30. `$msg = "Uploaded $filename successfully.";`

31. 继续编写失败情况的语句，然后关闭你的 PHP 块：

32. `} else {`

33. `$msg = "Could not upload file.";`

34. `}`

35. `?>`

36. 添加此 HTML：

37. `<HTML>`

38. `<HEAD>`

39. `<TITLE>Upload Status</TITLE>`

40. `</HEAD>`

41. `<BODY>`

42. 打印消息：

43. `<?php echo "$msg"; ?>`

44.

45. `</BODY>`

46. `</HTML>`

注意：确保路径 `/var/www/html/uploads/` 存在且 Web 服务器对其有写入权限。

47. 打开你的 Web 浏览器并输入 http://127.0.0.1/upload.php

48. 选择一个文件并点击提交。

在下一节中，你终于可以上传文件了！

# 使用表单和脚本上传文件

这是真理的时刻，请屏住呼吸并运行脚本。

- 1. 打开你的 浏览器并输入 http://127.0.0.1/upload_form.html

2. 使用“浏览”（Browse）按钮找到你想要上传的文件。

> 注意：此示例使用的是我自己电脑上的文件，因此图片显示的内容与你的结果可能不完全。

![](img/bc248f3d24697d1afbacee37b9c4d229_109_1.png)

- 3. 点击“上传文件”（Upload File）按钮。

应该会出现结果页面，提供有关你刚刚上传的文件的信息。

注意：仅允许你自己或其他信任的来源使用你的上传脚本，除非你在复制到系统之前通过检查文件类型来限制你想要上传的文件。

![](img/bc248f3d24697d1afbacee37b9c4d229_109_2.png)

# 第四部分：认识你的数据库

## 章节列表

- 第 11 章：建立连接

- 第 12 章：创建数据库表

- 第 13 章：向表中插入数据

# 第 11 章：建立连接

## 概述

在第 1 章安装和测试 MySQL 的过程中，你应该已经了一个示例数据库以及示例表，并插入和查询了一些数据。接下来的几章将重点关注使用 PHP 脚本作为前端来实现相同的连接和查询。在本章中，你将学习如何执行：

- 连接到 MySQL

- 列出本地上的所有数据库

- 列出数据库中的所有表

- 创建数据库

- 删除数据库

## 在 MySQL 中操作用户权限

当你在第 1 章安装 MySQL 数据库时，你使用的是匿名用户或 root 用户。在开始常规操作数据库之前，你应该创建一个带有密码的真实用户。为了做到这一点，你需要了解 MySQL 权限系统。

> 注意：如果你通过互联网服务供应商访问 MySQL，你可能只有一个用户和一个数据库可用。默认情况下，该用户具有访问数据库中所有表的权限并允许执行所有命令。如果是这种情况，你可以跳过本节的信息，直接进入脚本创建部分。在所有使用用户名和密码的情况下，请使用你的 ISP 提供的凭据。

## 创建新用户

如果你拥有添加用户的相应权限，那么执行此任务的最简单方法是使用 GRANT 命令。GRANT 命令的基本语法如下，其中 [privilege list] 是你想要授予新用户的权限的占位符。

```
GRANT [privilege list] ON database.tablename TO username@host IDENTIFIED BY "password";
```

你可以授予许多类型的权限，欲需更多信息，请访问 MySQL 手册主题：http://www.mysql.com/doc/G/R/GRANT.html。现在，你只需为你的新用户授予数据库中所有表的权限即可。

注意：以下命令在 Windows 和 Linux/UNIX 平台上的 MySQL 上完全相同。

- 1. 启动 MySQL 监视器（Monitor）。

2. 在 mysql> 提示符处输入以下内容选择名为 mysql 的数据库：

3. `use mysql;`

4. 输入以下 SQL 语句，根据需要替换你自己的用户名和密码。通配符 (*) 授予对所有数据库和表的权限：

5. `GRANT ALL ON * TO 'spike'@localhost IDENTIFIED BY '9sj7En4';`

6. 在 mysql> 提示符处输入以下内容退出 MySQL 监视器：

7. `exit`

8. 使用 mysqladmin 程序执行命令以重载权限：

9. `mysqladmin reload`

现在，新用户 (spike) 使用密码 9sj7En4 即可访问所有数据库和表。从现在起，该用户将成为后续所有数据库连接脚本中的示例用户。请在适当的地方替换你自己的用户名和密码。

## 连接到 MySQL

此脚本的目标仅仅是连接到运行在你机器（localhost）上的 MySQL。

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

2. `<?php`

3. 创建一个变量来存储 mysql_connect() 函数的结果：

4. `$connection = mysqli_connect("localhost", "spike", "9sj7En4");`

5.

注意：mysql_connect() 函数需要主机名、用户名和密码（按此顺序）。

6. 在 mysql_connect() 行添加一个 die() 函数，以便在连接失败时结束脚本并显示消息。在 die() 函数内部，使用 mysql_error() 函数。发生错误时打印的消息将与 MySQL 发出的完全一致。新行应如下：

- 7. `$connection = mysqli_connect("localhost", "spike", "9sj7En4");`

8. `or die(mysql_error());`

9. 测试 $connection 的值。如果为 true，则表示已连接到 MySQL，并创建一个变量来存储消息：

- 10. `if ($connection) {`

11. `$msg = "success";`

12. `}`

13. `echo $msg;`

14. `?>`

15. `<html>`

16. `<head>`

17. `<title>Connection</title>`

18. `</head>`

19. `<body>`

20. `<?php`

21. `echo $msg;`

22. `?>`

23. `</body>`

24. `</html>`

注意：上面的代码是 PHP 中处理成功连接的简化示例。

## 破坏你的脚本

任何时候操作数据库时都会遇到错误。这就是为什么你想显示一些常见错误。如果你输入了正确的用户名和密码，你应该获得成功的结果。

![](img/bc248f3d24697d1afbacee37b9c4d229_112_0.png)

如果你尽可能减少错误和警告，当数据库在高峰时段无法使用时，整体体验将变得更加愉快。

## 在服务器上列出数据库

现在你已经成功使用 PHP 连接到 MySQL，请熟悉内置的 MySQL 函数。你将使用：

- `mysql_list_dbs()` 用于列出 MySQL 服务器上的数据库。

- `mysql_num_rows()` 返回结果集的行数。

- `mysql_tablename()` 尽管名为表名，但它可以从结果返回表或数据库的名称。

此脚本的目标是列出本地 MySQL 服务器上的所有数据库。

+   4. $connection = @mysql_connect("localhost", "spike", "9sj7En4")

+   5. or die(mysql_error());

+   6.

+   7. 创建一个变量来存储 `mysql_list_dbs()` 函数的结果。使用 `@` 抑制警告，并使用 `die()` 函数在脚本无法获取列表时结束脚本并显示消息：

$dbs = @mysql_list_dbs($connection) or die(mysql_error());

+   8.

+   9. **注意** `mysql_list_dbs()` 的唯一参数是当前连接的链接标识符。

10. 你将遍历结果并动态填充项目列表。在循环之外开始该项目列表：

+   11. $db_list = "<ul>";

+   12. 启动计数器。你的循环中需要它：

+   13. $i = 0;

+   14. 开始一个 `while` 循环。只要 `$i` 的值小于 `$dbs` 结果中的行数，该循环就会继续：

+   15. while ($i < $mysql_num_rows($dbs)) {

+   16. 一进入 `while` 循环，获取结果中当前行反映的数据库名称：

+   17. $db_names[$i] = mysql_tablename($dbs, $i);

+   18. **注意** 变量会被其值替换，因此在第一次循环中，这一行类似于 `$db_names[0] = mysql_tablename($dbs, 0);`。

计数从 0, 1 开始，这将反映结果中的第一行。随着计数器的增加，显示行号。

+   19. 将数据库名称添加到项目列表中：

+   20. $db_list .= "<li>$db_names[$i]</li>";

+   21. 在关闭 `while` 循环之前递增你的计数器：

+   22. $i++;

+   23.

+   24. 关闭 `while` 循环、项目列表以及你的 PHP 块：

+   }

+   25. $db_list = "</ul>";

+   26. ?>

+   27. 添加此 HTML：

+   28. <HTML>

+   29. <HEAD>

+   30. <TITLE>MySQL Databases</TITLE>

+   31. </HEAD>

+   32. <BODY>

+   33. <p><strong>localhost 上的数据库：</strong></p>

+   34. 打印消息字符串：

+   35. <?php echo "$db_list"; ?>

+   36. 添加一些额外的 HTML 使文档有效：

+   37. </BODY>

+   38. </HTML>

+   39. 将文件保存为 `db_listdb.php`。你的代码看起来应该是这样：

```php
<?php
$connection = mysqli_connect("localhost", "root", "12345");
if (!$connection) {
    die(mysqli_error());
}

$db_list = mysqli_query($connection, "SHOW DATABASE");
while($row = mysqli_fetch_array($db_list)) {
    echo $row['Database'] . "<br>";
}

$db_list = mysqli_query($connection, "SHOW TABLES");
while($row = mysqli_fetch_array($db_list)) {
    echo $row['Tables'] . "<br>";
}

$db_list = mysqli_query($connection, "SHOW TABLES FROM test");
while($row = mysqli_fetch_array($db_list)) {
    echo $row['Tables'] . "<br>";
}

$db_list = mysqli_query($connection, "SHOW TABLES FROM mysql");
?>
```

# 14.

将此文件放在你的 Web 服务器的文档根目录下，然后打开 Web 浏览器并输入 http://127.0.0.1/db_list.php

# 15.

你的列表可能会有所不同，取决于你在第一章中尝试了多少内容，但你至少应该看到 MySQL 系统数据库 (mysql) 和在第一章中创建的数据库 (test)。接下来，你将在此脚本中添加另一个循环来打印每个数据库中的表。

# 在数据库中列出表

此脚本的目标是列出本地服务器上所有的数据库，包括数据库中的表。对 `db_list.php` 进行一些少量修改即可列出数据库。以下是你将看到的唯一新函数：

- mysql_list_tables() 用于列出 MySQL 数据库中的表。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

2. <?php

3. 按照之前的做法添加连接信息：

4. $connection = @mysql_connect("localhost", "spike", "9sj7En4")

5. or die(mysql_error());

6. 创建一个变量来存储 `mysql_list_dbs()` 函数的结果。使用 `@` 抑制警告，并使用 `die()` 函数在脚本无法获取列表时结束脚本并显示消息：

7. $db = @mysql_list_dbs($connection) or die(mysql_error());

8. 你将遍历结果并动态填充项目列表。在循环之外开始该项目列表：

9. $db_list = "<ul>";

10. 启动计数器。你的循环中需要它：

11. $i = 0;

12. 开始一个 `while` 循环。只要 `$i` 的值小于 `$dbs` 结果中的行数，该循环就会继续：

13. while ($i < $mysql_num_rows($dbs)) {

14. 一进入 `while` 循环，获取结果中当前行反映的数据库名称：

15. $db_names[$i] = mysql_tablename($dbs, $i);

16. **注意** 变量会被其值替换，因此在第一次循环中，这一行类似于 `$db_names[0] = mysql_tablename($dbs, 0);`。

计数从 0, 1 开始，这将反映结果中的第一行。随着计数器的增加，显示行号。

17. 将数据库名称添加到项目列表中：

18. $db_list .= "<li>$db_names[$i]</li>";

19. 在关闭 `while` 循环之前递增你的计数器：

20. $i++;

21. 

22. 关闭 `while` 循环、项目列表以及你的 PHP 块：

23. }

24. $db_list = "</ul>";

25. ?>

26. 添加此 HTML：

27. <HTML>

28. <HEAD>

29. <TITLE>MySQL Databases</TITLE>

30. </HEAD>

31. <BODY>

32. <p><strong>localhost 上的数据库：</strong></p>

33. 打印消息字符串：

34. <?php echo "$db_list"; ?>

35. 添加一些额外的 HTML 使文档有效：

36. </BODY>

37. </HTML>

38. 将文件保存为 `db_listdb.php`。你的代码看起来应该是这样：

（注：此处代码块与上文一致，保持原样）

```php
?>
<HTML>
<HEAD>
<TITLE>MySQL 表</TITLE>
</HEAD>
<BODY>
<p><<strong>>localhost 上的数据库和表</strong></p>
<?php echo "$db_list"; ?>
</BODY>
</HTML>
```

![](img/bc248f3d24697d1afbacee37b9c4d229_118_0.png)

由于测试用户被授予了所有对象的权限，你应该能看到所有表和数据库的列表，包括系统保留的那些。根据你的服务器设置和数据库表情况，结果可能会有所不同。

在下一节中，你将尝试在你的服务器上创建新数据库。

# 创建新数据库

之前的脚本中复杂的元素在下一个脚本中完全不出现。此脚本的目标是在 MySQL 服务器上创建一个数据库。

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

2. <?php

3. 创建一个变量来存储数据库名称：

4. $new_db = "testDB2";

5. 像之前那样添加连接信息：

6. $connection = @mysql_connect("localhost", "spike", "9s7En4")

7. or die(mysql_error());

8. 创建一个变量来存储 mysql_create_db() 函数的结果。包含 @ 以抑制警告，并使用 die() 函数在数据库连接失败时结束脚本并显示消息：

9. $result = @mysql_create_db($new_db, $connection) or

10. die(mysql_error());

注意：mysql_create_db 函数需要一个数据库名称和一个连接的链接标识符。

- 13. 测试 $result 的值。如果为 true，则数据库已创建，并且会创建一个变量来存储消息：

14. if ($result) {

15. $msg = "<P>数据库已创建！</P>";

16. }

注意：如果无法创建数据库，脚本将通过 die() 函数结束。

- 18. 关闭你的 PHP 块，添加 HTML：

19. ?>

20. <HTML>

21. <HEAD>

22. <TITLE>创建一个 MySQL 数据库</TITLE>

23. </HEAD>

24. <BODY>

25. 打印消息字符串：

26. <?php echo $msg; ?>

27. 添加一些额特的 HTML 以使文档有效：

28. </BODY>

29. </HTML>

30. 将文件保存为 db_created.php 并此文件放置在你的 Web 服务器的文档根目录下。

31. 打开 Web 浏览器并输入 http://127.0.0.1/db_created.php

![](img/bc248f3d24697d1afbacee37b9c4d229_119_0.png)

![](img/bc248f3d24697d1afbacee37b9c4d229_119_1.png)

在下一节中，你将删除（drop）刚刚创建的数据库。

# 删除数据库

此脚本的目标是在 MySQL 服务器上删除一个数据库。

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

2. <?php

3. 创建一个变量来存储你想删除的数据库名称：

4. $drop_db = "testDB2";

5. 像之前那样添加连接信息：

6. $connection = @mysql_connect("localhost", "spike", "9s7En4");

7. or die(mysql_error());

8. 创建一个变量来存储 mysql_drop_db() 函数的结果。包含 @ 以抑制警告，并使用 die() 函数在删除数据库失败时结束脚本并显示消息：

9. $result = @mysql_drop_db($drop_db, $connection) or

11. die(mysql_error());

注意：mysql_drop_db() 函数需要一个数据库名称和当前连接的链接标识符。

- 13. 测试值 $result。如果为 true，则数据库已删除，并且会创建一个变量来存储消息：

```php
if ($result) {
$msg = "<P>数据库已删除！</P>";
}
```

注意：如果无法删除数据库，脚本将通过 die(function)结束。

- 18. 选择你的 PHP 块并添加 HTML：

```php
<?php
<HTML>
<HEAD>
<TITLE>删除一个 MySQL 数据库</TITLE>
</HEAD>
<body
打印消息字符串：
<?php echo $msg; ?>
</BODY>
</HTML>
```

- 28. 添加一些额外的 HTML 以使文档有效：

- 31. 将文件保存为 db_dropdb.php 并此文件放置在你的 Web 服务器的文档根目录下。

- 32. 打开 Web 浏览器并输入 http://127.0.0.1/db_dropdb.php

![](img/bc248f3d24697d1afbacee37b9c4d229_120_0.png)

在下一章中，你将创建一个持久的数据库表，并最终向该表填充数据。

# 第12 章：创建数据库表

## 概述

你拥有这个很好的服务器和一个名为 testDB 的表。在本章中，你将学习如何：

- 规划表

- 识别某些数据类型的陷阱

- 识别字段的重要性

- 遵循创建表的两个步骤

## 规划你的表

创建一个表很容易——费的是脑力。要创建一个简单的表，你只需要给它一个名字。但这将是一个无聊的表，除了名字之外，你应该知道你想在表中需要的字段。

## 基础数据类型

表中的所有字段都给了一个特定的数据类型。数据类型定义了字段中允许的数据。对于某些数据类型定义，你必须指定允许的最大长度，但其他假设为特定长度。正确定义字段很重要；例如，如果你有一个存储记录名称的字段和一个50个字符的 varchar 字段，却试图存入100个字符的字符串，它将被截断为50个字符。如果你想使用 text 数据类型，无法指定长度：它自动假设为特定长度。表12.1显示你将使用的常用数据类型。要查看完整列表，请阅读 MySQL手册。

| 数据类型 | 定义 |

| --- | --- |

| TINYINT | 有符号或无符号的小整数。如果有符号，允许范围从 -128 到 127。如果无符号，允范围从 0 到 255。 |

| SMALLINT | 有符号或无符号的小整数。如果有符号，允许范围从 -32768 到 32767。如果无符号，允许范围从 0 到 65535。 |

| MEDIUMINT | 有符号或无符号的中型整数。如果有符号，允许范围从 -8388608 到 8388607。如果无符号，允许范围从 0 到 16777215。 |

| INT | 有符号或无符号的标准型整数。如果有符号，允许范围从 -2147483648 到 2147483647。如果无符号，允许范围从 0 到 4294967295。 |

| BIGINT | 有符号或无符号的大整数。如果有符号，允许范围从 -9223372036854775808 到 9223372036854775807。如果无符号，允许范围从 0 到 18446744073709551615。 |

# 表12.1：某些 MySQL 数据类型

| 数据类型 | 定义 |

| --- | --- |

| FLOAT | 不能无符号的浮点数。你可以定义显示长度 (M) 和小数位数 (D)。这不是强制的，默认为 10.2，其中2是小数位数。FLOAT 的小数精度可以达到24位。 |

| DATE | YYYY-MM-DD格式的日期，范围从1000-01-01到9999-12-31。例如，1973年12月30日将存储为 1973-12-30。 |

| DATETIME | YYYY-MM-DD格式的日期，范围从1000-01-01到9999-12-31。例如，1973年12月30日将存储为 1973-12-30。 |

| TIMESTAMP | 1970年1月1日午夜到2038年之间的时间戳。你可以为 TIMESTAMP 字段定义多个长度，这与存储的内容直接相关。TIMESTAMP 的默认长度是4，存储 YYYYMMDDHH。这看起来像上面的 DATETIME 格式，但没有连字符数字；1973年12月30日下午3点将存储为 1973123015。TIMESTAMP 的其他定义为12 (YYYYMMDDHHMMSS)、8 (YYYYMMDD) 和6 (YYYYMMDD)。 |

| CHAR | 长度在1到255个字符之间的固定长度字符串，存储时按指定长度右填充。不需要定义长度，但默认值是1。 |

| VARCHAR | 长度在1到255个字符之间的变长字符串。创建 VARCHAR 字段时必须定义长度。 |

| BLOB 或 TEXT | 最大长度为65535字符的字段。BLOB是“二进制大对象”，用于存储大量二进数据，如图像或其他类型的文件。定义为 TEXT的字段也包含大量数据；两者之间的区别在于对存储数据的排序和比较在BLOB上区分大小写，而在TEXT字段中不区分大小写。BLOB或TEXT不指定长度。 |

| ENUM | 枚举（列表）。在定义 ENUM 时，你正在创建一个列表，必须从中选择值（或者可以为NULL）。例如，如果你想让字段包含“A”或“B”或 |

## 定义你的字段

本章的总体目标是创建一个用于存储你个人音乐收藏数据的表。花点时间考虑你想知道的事情；显而包括标题和艺术家，可能还有唱片公司、获取日期以及你对该录音的个人笔记。

在下一节中，你将创建一系列表单，这些表单将获取你的表信息并发送到 MySQL 数据库。在第一步，你将提交表名和你想包含的字段数量。第二步将显示额外的表单字段，以便你定义表列的属性。第三步将发送请验证表已创建，并显示“成功”消息。

## 唯一字段的重要性

使用 ID 编号不仅可以帮助你跟踪数据，而且在将来，它们可以帮助你建立多个表之间的关系。在 `my_music` 表中，将有一个 `ID` 字段（见表 12.2）。使用此字段作为唯一字段，而不是使用其他字段，将允许你的表中存在两个同名的录音。例如，如果你拥有 Indigo 的专辑《Strange Fire》，你的表中会有两个条目：一个是 1987 年发行的版本，另一个是 1989 年发行的版本。

| 表 12.2: my_music 的字段 |

| :--- | :--- |

| 字段名称 | 说明 |

| id | 为条目创建一个唯一的 ID 编号 |

| format | 是 CD、磁带还是 LP？ |

| title | 录音的标题 |

| artist_fn | 艺术家的首名 |

| artist_In | 艺术家的姓氏或团体名称 |

| rec_label | 唱片公司 |

| my_notes | 我对录音的个人想法 |

| date_acq | 获取日期 |

如果没有唯一标识符，你将无法只选择一个版本放入表中，而这个简单的例子传达了在表的每条记录中拥有唯一标识符的重要性。随着你创建更多由数据库驱动的元素，唯一标识符的作用将在本书的剩余部分变得更加明显。

## 两步表单序列

对于创建数据库表，两步表单序列似乎多此一举。毕竟，你在第 1 章中见过一个基础的创建表 SQL 语句，当时你创建了 `test_table`：

```sql
create table test_table (test_id int, test_note text);
```

当使用 PHP 脚本创建表时，你所做的只是向 MySQL 发送完全相同的查询。然而，你可以为这个过程系上精美的丝带（创建一个基于表单的界面），并称之为管理界面！

在创建管理界面的过程中，你将从一个 HTML 表单开始，然后创建一个 PHP 脚本从该表单获取信息并动态创建另一个表单。最后，你将创建一个发送实际 SQL 查询的脚本。

## 步骤步：字段数量

此 HTML 表单将包含两个输入字段：一个用于表名，另一个用于你的表包含的字段数量。

- 1. 在你的文本编辑器中打开新文件并输入以下 HTML：

2. `<HTML>`

3. `<HEAD>`

4. `<TITLE>Create a Database Table: Step 1</TITLE>`

5. `</HEAD>`

6. `<BODY>`

7. `<h1>Step 1: Name and Number</h1>`

8. 开始你的表单。假设方法为 POST，动作是一个名为 `do_showfielddef.php` 的脚本

9. `<form method="POST" action="do_showfielddef.php">`

10. 为表名创建一个带有文本标签的输入字段：

11. `<p><strong>Table Name:</strong><br>`

12. `<input type="text" name="table_name" size="30"></p>`

13. 为表中的字段数量创建一个带有文本标签的输入字段：

14. `<p><strong>Number of Fields:</strong><br>`

15. `<input type="text" name="num_fields" size="5"></p>`

16. 添加提交按钮，关闭你的表单并添加更多 HTML 使文档有效：

17. `<input type="submit" name="submit" value="Go to Step 2"></p>`

18. `</form>`

19. `</BODY>`

20. `</HTML>`

21. 以 `show_creatable.html` 命名保存文件，并将此文件放在你的 Web 服务器的文档根目录下。

23. 打开网页浏览器并查看页面 http://127.0.0.1/show_creatable.html

在下一节中，你将遵循该过程的第 2 步，并根据 `$_POST[table_name]` 和 `$_POST[num_fields]` 的值动态创建另一个表单的脚本。

## 步骤 2：定义你的字段

在步骤 1 中，你创建了变量来存储表名（`$_POST[table_name]`）和你想放在表的字段数量（`$_POST[num_fields]`）。在这一步中，你将创建一个 PHP 脚本来显示进一步定义字段所需的额外元素：名称、类型和长度。

- 1. 在你的文本编辑器中打开新文件并启动 PHP 块：

2. `<?php`

3. 检查 `$_POST[table_name]` 和 `$_POST[num_fields]` 是否确实输入了值。如果没有，则将用户重定向回表单并退出脚本：

4. `if (isset($_POST[table_name]) || isset($_POST[num_fields])) {`

5. `header("Location:http://127.0.0.1/show-creatable.html");`

6. `exit;`

7. `}`

8.

9. 开始构建名为 `form_block` 的字符串，假设方法为 POST，动作是一个脚本 `do_creatable.php`。记得转义引号！

10. `$_form_block = "`

11. `<FORM METHOD="POST" ACTION="do_creatable.php">`

（注：此处由于原文存在大量 OCR 重复和碎片，已根据逻辑进行了清理和重构）

68. 将文件保存为 `do_showfielddef.php` 并将其放置在 Web 服务器的文档根目录下。

你的代码应该看起来像这样：

```php
<?php
// validate important input
if (isset($_POST[table_name]) || isset($_POST[num_fields])) {
    header("Location: http://127.0.0.1/show_creatableable.html");
    exit;
}

// begin creating form for display
$form_block = "
<FORM METHOD="POST" ACTION="do_creatableable.php">
<INPUT TYPE="hidden" NAME="table_name"
VALUE='$_POST[table_name]'>
<TABLE CELLSPACING="5">
<TR>
<TH>FIELD NAME</TH><TH>FIELD TYPE</TH><TH>FIELD LENGTH</TH></TR>
";

$count = 0; // count until you reach the number of fields
for ($i=0; $i < $_POST[num_fields]; $i++) {
    // add to the form, one row for each field
    $form_block .= "
    <TR>
        <TD ALIGN="CENTER"><INPUT type="text" NAME="field_name"
        SIZE="30"></TD>
        <TD ALIGN="CENTER">
            <SELECT NAME="field_type">
                <OPTION VALUE="char">char</OPTION>
                <OPTION VALUE="date">date</OPTION>
                <OPTION VALUE="float">float</OPTION>
                <OPTION VALUE="int">int</OPTION>
                <OPTION VALUE="text">text</OPTION>
                <OPTION VALUE="varchar">varchar</OPTION>
            </SELECT>
        </TD>
        <TD ALIGN="CENTER"><INPUT type="text" NAME="field_length"
        SIZE="5"></TD>
    </TR>
";
}

// finish up the form
$form_block .= "
    <TR>
        <TD ALIGN="CENTER" COLSPAN="3"><INPUT type="submit" VALUE="Create Table"></TD>
    </TR>
</TABLE>
<FORM>";
?>
<html
<head>
<TITLE>Create a Database Table: Step 2</TITLE>
</head>
<body>
<h1>Define fields for <?php echo "\$_POST[table_name];"; ?></h1>
<?php echo "\$form_block"; ?>
</BODY>
</HTML>
```

在下一节中，你将从第 1 步过渡到第 2 步，准备创建表。

# 开始创建表的过程

你应该能够顺利地从第 1 步（命名表并提供字段数量）跳转到第 2 步（定义字段）。让我们尝试一下。

- 1. 打开 Web 浏览器访 http://127.0.0.1/show_creatable.html

- 2. 在 Table Name（表名）字段中，输入 **my_music**。

- 3. 在 Number of Fields（字段数量）字段中，输入 **8**。

- 4. 点击 Go to Step 2（跳转到第 2 步）按钮。你应该看到这个表单。

![](img/bc248f3d24697d1afbacee37b9c4d229_128_0.png)

这里有八行，对应你想要在 my_music 表中创建的八个字段。填充这些字段，但先不要 Create Table（创建表）按钮，因为你还没有创建脚本！

- 5. 在第一行，在 Field Name（字段名）中输入 **id**。从 Field Type（字段类型）下拉菜单中选择，并指定 Field Length（字段长度）为 **5**。

- 6. 在第二行，在 Field Name 中输入 **format**，从 Field Type 下拉菜单中选择 char，并指定 Field Length 为 **2**。

- 7. 在第三行，在 Field Name 中输入 **title**，从 Field Type 下拉菜单中选择 varchar，并指定 Field Length 为 **150**。

- 8. 在第四行，在 Field Name 中输入 **artist_fn**，从 Field Type 下拉菜单中选择 varchar，并指定 Field Length 为 **100**。

- 9. 在第五行，在 Field Name 中输入 **artist_in**，从 Field Type 下拉菜单中选择 varchar，并指定 Field Length 为 **100**。

- 10. 在第六行，在 Field Name 中输入 **rec_label**，从 Field Type 下拉菜单中选择 varchar，并指定 Field Length 为 **50**。

- 11. 在第七行，在 Field Name 中输入 **my_notes**，并在 Field Type 下拉菜单中选择 text。

- 12. 在第八行，在 Field Name 中输入 **date_acq**，并在 Field Type 下拉菜单中选择 date。

![](img/bc248f3d24697d1afbacee37b9c4d229_129_0.png)

在下一节中，你将为此表单创建后端脚本，这样你就可以点击按钮并创建表了。

# 创建表的脚本

此脚本将构建一个 SQL 语句并发送到 MySQL 以创建 my_music 表。

- 1. 在文本编辑器中打开新文件并开始编写 PHP 块：

- 2. `<?php`

- 3. 创建一个变量来存储表将所在的数据库名称：

- 4. `$db_name = "test";`

- 5. 添加连接信息：

- 6. `$connection = mysql_connect("localhost", "spike", "js");`

- 7. 如果连接失败，脚本将报错结束：

- 8. `die(mysql_error());`

- 9. 选择数据库：

- 10. `$db = mysql_select_db($db_name, $connection) or die(mysql_error());`

- 11. 通过变量初始语法构建查询：

- 12. `$sql = "CREATE TABLE " . $_POST[table_name] . " (";`

- 13. 使用数组中元素的循环：

- 14. `for ($i = 0; $i < count($_POST[field_name]); $i++) {`

- 15. 将每个新字段添加到 SQL 语句：

- 16. `$sql .= $_POST[field_name] . " " . $_POST[field_type] . ",";`

- 17. 清理字符串末尾：

- 18. `$sql = substr($sql, 0, -1);`

- 19. 如果没有长度，则关闭括号：

- 20. `$sql += ");";`

- 21. 执行查询：

- 22. `$result = mysql_query($sql,$connection) or die(mysql_error());`

- 23. 如果结果为真，创建一个消息：

- 24. `if ($result) {`

- 25. `$message = "<P>" . $_POST[table_name] . " has been created!</P>";`

- 26. `}`

- 27. 输出消息让用户知道正在查看的内容：

- 28. `echo $message;`

- 29. 关闭 PHP 块并添加 HTML：

- 30. `?>`

- 31. 添加一些标题使文档有效：

- 32. `<h1>Adding table to <?php echo "$db_name"; ?></h1>`

- 33. 输出消息：

- 34. `echo $message;`

- 35. 关闭 body：

- 36. `</body>`

- 37. 关闭 html：

- 38. `</html>`

在下一章中，你将创建一个 HTML 表单接口，通过该脚本向 `my_music` 表中添加条目。

## 第 13 章：向表插入数据

## 概述

`my_music` 数据库表正静候在那里，等待你添加关于音乐收藏的信息。在本章中，你将学习如何执行以下操作：

- 创建一个用于添加记录的管理界面

- 创建一个将记录插入到表的脚本

### 创建记录添加表单

HTML 表单将为 `my_music` 数据库表中的每一列包含一个输入字段。在之前的章节中，你创建了八个字段，对应八列。你的记录添加界面应该为这些字段中的每一个都留出空间。

注意：使用数据库字段名作为 HTML 表单字段中 `NAME` 属性的值。在适当的情况下，使用数据库字段的大小作为 HTML 表单中 `MAXLENGTH` 属性的值。

1. 在你的文本编辑器中打开新文件并输入以下 HTML：

2. `<HTML>`

3. `<HEAD>`

4. `<TITLE>Add a Record</TITLE>`

5. `</HEAD>`

6. `<body>`

7. `<h1>Adding a Record to my_music</h1>`

8. 开始你的表单。假设 `method` 为 `POST` 且 `action` 为名为 `add_record.php` 的脚本。

9. `<FORM METHOD="POST" ACTION="do_addrecord.php">`

10. 开始一个 HTML 表格辅助布局。开始新行和数据单元格，然后为 ID 创建带有文本标签的输入字段：

11. `<TABLE CELLSPAN="3" CELLPADDING="3">`

12. `<TR>`

13. `<TD VALIGN="TOP">`

14. `<STRONG>ID:</STRONG><BR>`

15. `<INPUT TYPE="text" NAME="id" SIZE=5 MAXLENGTH=5">`

16. 为获取日期创建一个带有文本标签的输入字段。在输入字段后关闭数据单元格：

17. `<P><strong>Date Acquired (YYYY-MM-DD):</STRONG><BR>`

18. `<INPUT TYPE="text" NAME="date_acq" SIZE=10 MAXLENGTH=10></P>`

19. `</TD>`

20. 注意：MySQL 中的日期使用 `YYYY-MM-DD` 格式。使用该格式的日期示例是 `2002-03-02`（2002年3月2日）。

21. 在新的数据单元格中，创建一组单选按钮来选择录音的格式。在单选按钮组后关闭数据单元格和行：

22. `<TD VALIGN=TOP>`

23. `<STRONG>Format:</STRONG><BR>`

24. `<INPUT TYPE="radio" NAME="format" VALUE="CD" checked> CD`

25. `<INPUT TYPE="radio" NAME="format" VALUE="CS"> cassette`

26. `<INPUT TYPE="radio" NAME="format" VALUE="LP"> LP`

27. `</TD>`

28. `</TR>`

29. 开始新行和数据单元，然后为标题创建一个带有文本标签的输入字段。在输入字段后关闭数据单元格：

30. `<TR>`

31. `<TD VALIGN=TOP>`

32. `<STRONG>Title:</STRONG><BR>`

33. `<INPUT TYPE="text" NAME="title" SIZE=35 MAXLENGTH=150></P>`

34. 在新的数据单元格中开始，为唱片信息创建一个带有文本标签的输入字段。在输入字段后关闭数据单元格和行：

35. `<TD VALIGN=TOP>`

36. `<STRONG>Record Label:</STRONG><BR>`

37. `<INPUT TYPE="text" NAME="rec_label" SIZE=35 MAXLENGTH=50></P>`

38. `</TR>`

39. 开始新行和数据单元格，然后为艺术的名字创建一个带有文本标签的输入字段。在输入字段后关闭数据单元格和行：

40. `<TR>`

41. `<TD VALIGN=TOP>`

42. `<STRONG>Artist's First Name:</STRONG><BR>`

43. `<INPUT TYPE="text" NAME="artist_fn" SIZE=35 MAXLENGTH=100></P>`

44. `</TD>`

45. 在新的数据单元格中，为艺术家的姓（或团体名）创建一个带有文本标签的输入字段。在输入字段后关闭数据单元格和行：

46. `<TD VALIGN=TOP>`

47. `<STRONG>Artist's Last Name (or Group Name):</STRONG><BR>`

48. `<INPUT TYPE="text" NAME="artist_ln" SIZE=35 MAXLENGTH=100></P>`

49. `</TR>`

50. 开始一个跨越两列的新行和数据单元格。创建一个 `textarea` 来存放你对录音的备注：

51. `<TR>`

52. `<TD VALIGN=TOP COLSPAN=2 ALIGN=CENTER>`

53. `<P><strong>My Notes.</STRONG><BR>`

54. `<TEXTAREA NAME="my_notes" CO=35 ROWS=5 WRAP=virtual>`

55. `</TEXTAREA></P>`

56. 添加一个提交按钮，然后关闭数据单元格、行以及表格本身：

57. `<INPUT TYPE="SUBMIT" NAME="submit" VALUE="Add Record">`

58. `</TD>`

59. `</TR>`

60. `<TABLE>`

61. 关闭表单并添加一些 HTML 使文档有效：

62. `</FORM>`

63. `<body>`

64. `</html>`

65. 将文件保存为 `show_addrecord.html` 并将其放在你的 Web 服务器根目录下。

66. 打开浏览器并输入 `show_addrecord.html`。在下一节中，你将创建一个获取表单输入、创建 SQL 语句并将记录添加到数据库的脚本。

### 创建记录脚本

用于添加记录的脚本比创建表的脚本简单得多！

1. 在你的文本编辑器中打开新文件并开始 PHP 块：

2. `<?php`

3. 检查 `$_POST[id]`、`$_POST[format]` 和 `$_POST[title]` 是否已输入。如果没有，将用户重定向回表单并退出脚本：

4. `if (!($_POST[id]) || (!($_POST[format]) || (!($_POST[title])) {`

5. `header("Location:show_addrecord.html");`

6. `exit;`

7. `}`

8. 注意：你可以根据需要设置任意多个字段。

9. 创建一个变量来存储数据库名称：

10. `$db_name = "test";`

11. 创建一个变量来存储你要用此脚本填充的表：

12. `$table_name = "my_music";`

13. 添加连接信息：

14. `$connection = @mysql_connect("localhost", "spike", "db_name") or die(mysql_error());`

15. 选择你数据库：

16. `$db = @mysql_select_db($db_name, $connection) or die(mysql_error());`

17. 创建 SQL 语句。第一个括号给出填充的字段名（按顺序），第二个括号设置字符串：

18. `$sql = "INSERT INTO $table_name (id, format, title, artist_fn, artist_ln, rec_label, my_notes, date_acq) VALUES ('$_POST[id]', '$_POST[format]', '$_POST[title]', '$_POST[artist_fn]', '$_POST[artist_ln]', '$_POST[rec_label]', '$_POST[my_notes]', '$_POST[date_acq]');`

19. 创建一个变量来存储 `mysql_query()` 的结果：

20. `$result = @mysql_query($sql, $connection) or die(mysql_error());`

21. 关闭你的 PHP 块并添加 HTML：

22. `?>`

23. `<HTML>`

24. `<HEAD>`

25. `<TITLE>Add a Record</TITLE>`

26. `</HEAD>`

27. `<body>`

28. 添加一个标题让用户知道 `$table_name` 变量的值：

29. `<h1>Adding a Record to <?php echo "$table_name"; ?></h1>`

30. 接下来，你将重新创建 `show_addrecord.html` 中使用的布局，但不包含字段。相反，将混合 HTML 和 PHP 来显示输入的值。开始新行和数据单元格，然后为 ID 显示文本标签和值：

31. `<TABLE CELLACING="3" CELLPADDING="3">`

32. `<TD VALIGN=TOP>`

33. `<strong>ID:</strong><BR>`

34. `<?php echo "$_POST[id]"; ?></p>`

35. 显示获取日期的文本标签和值，然后关闭数据单元格：

36. `<strong>Date Acquired (YYYY-MM-DD):</strong><BR>`

37. `<?php echo "$_POST[date_acq]"; ?></p>`

38. `</TD>`

39. 显示录音的格式，然后关闭数据单元格和行：

40. `<TD VALIGN=TOP>`

41. `<strong>Format:</strong><BR>`

42. `<?php echo "$_POST[format]"; ?></p>`

43. `</TD>`

44. `</TR>`

45. 开始新行和数据单元格，为标题显示文本标签和值，并关闭数据单元格：

46. `<TR>`

47. `<TD VALIGN=TOP>`

48. `<P><strong>Title:</strong><BR>`

49. `<?php echo "$_POST[title]"; ?></P>`

50. `</TD>`

51. 在新的数据单元格中，显示唱片信息的文本标签和值，然后关闭数据单元格和行：

52. `<TD VALIGN=TOP>`

53. `<P><strong>Record Label:</strong><BR>`

54. `<?php echo "$_POST[rec_label]"; ?></P>`

55. `</TD>`

56. `<TR>`

57. 开始新行和数据单元格，为艺术家的名字显示文本标签和值，并关闭数据单元格：

58. `<TD VALIGN=TOP>`

59. `<P><strong>Artist's First Name:</strong><BR>`

60. `<?php echo "$_POST[artist_fn]"; ?></p>`

61. `</TD>`

62. `<TR>`

63. 在新的数据单元格中，显示艺术家的姓（或团体名）的文本标签和值，然后关闭数据单元格和行：

64. `<TD VALIGN=TOP>`

65. `<P><strong>Artist's Last Name (or Group Name):</strong><BR>`

66. `<?php echo "$_POST[artist_ln]"; ?></p>`

67. `</TD>`

68. `</TR>`

exit;

//设置数据库和表名

$db_name = "testDB";

$table_name = "my_music";

//连接到 MySQL 并选择使用的数据库

$connection = @mysql_connect('localhost', 'spike', '9sj7En4')

or die(mysql_error());

$db = @mysql_select_db($db_name, $connection) or

die(mysql_error());

//SQL 语句和插入查询

$sql = "INSERT INTO $table_name (id, format, title, artist_fn,

artist_in, rec_label, my_notes, date_acq) VALUES ('$POST[id]',

'$POST[format]', '$POST[title]', '$POST[artist_fn]',

'$POST[artist_in]', '$POST[rec_label]',

'$POST[my_notes]', '$POST[date_acq]');";

$result = @mysql_query($sql,$connection) or die(mysql_error());

<html>

<head>

<title>添加记录</title>

</head>

<body>

<h1>正在向 <? echo "$table_name"; ?> 添加记录</h1>

<table cellspacing="3" cellpadding="3">

<tr>

<td valign="top">

<p><strong>ID:</strong><br>

<?php echo "$POST[id]"; ?></p>

</td>

<td>

<p><strong>获取日期 (YYYY-MM-DD):</strong><br>

<?php echo "$POST[date_acq]"; ?></p>

</td>

</tr>

<tr>

<td valign="top">

<p><strong>格式:</strong><br>

<?php echo "$POST[format]"; ?></p>

</td>

</tr>

<tr>

<td valign="top">

<p><strong>唱片公司:</strong><br>

<?php echo "$POST[rec_label]"; ?></p>

</td>

</tr>

<tr>

<td valign="top">

<p><strong>艺人名:</strong><br>

<?php echo "$POST[artist_fn]"; ?></p>

</td>

<td valign="top">

<p><strong>艺人姓（或团体名称）：</strong><br>

<?php echo "$POST[artist_in]"; ?></p>

</td>

</tr>

<tr>

<td colspan="2" align="center">

<p><strong>我的笔记:</strong></br>

<p><?php echo stripslashes($_POST['my_notes']); ?></p>

<p><a href="show_addrecord.html">添加另一个</a></p>

</td>

</tr>

</table>

</body>

</html>

继续进行下一步，你将点击按钮并添加记录。

# 填充你的表格

现在有趣的事情开始了！如果你在完成本章的第一部分后没有关闭 Web 浏览器，在浏览器窗口中应该能看到 `show_addrecord.html`。如果没有，请现在打开 http://127.0.0.1/show_addrecord.html。

为你手头的一张专辑完成添加表单。这里我收藏中的一个例子。点击“添加记录”（Add Record）按钮，你应该就能看到确认屏幕。

向数据库表添加几条你自己的录音。除非你更改了自己的设置，否则唯一的必填字段是 ID、格式和标题。

注意：在随后的章节中，你将学习如何修改表格，使该字段确实是唯一的并且自动递增，这样你就不需要不断输入数字并寄希望它有效了。

# 第 14 章：选择和显示数据

## 概述

到此时，你已经愉快且反复地用 my_music 表填充了你音乐收藏中的所有项目——或者至少是几个。在本章中，你将学习如何执行以下操作：

- 使用 SQL ORDER BY 子句从表中选择记录

- 格式化并显示来自数据库表的记录

# 规划创建创建管理菜单

你可以只写一个脚本说“选择我所有的数据；我不在乎顺序”，但那样会很无聊。在本章中，你将看到从 my_music 表中选择记录的四种方法。为了方便导航，请创建一个管理菜单——这是“链接列表”的华丽说辞。

1. 在你的文本编辑器中打开一个新文件并创建以下 HTML：

2. `<HTML>`

3. `<HEAD>`

4. `<TITLE>我的菜单</TITLE>`

5. `</HEAD>`

6. `<body>`

7. `<h1>我的音乐</h1>` (修正了标签)

8. `<p><strong>我的音乐</strong></p>`

9. 开始一个无序列表并创建指向名为 `sel_byid.php` 脚本的第一个链接。此脚本将按 ID 编号排序记录：

10. `<ul>`

11. `<a href="sel_byid.php">按 ID 排序</a>`

12. 添加一个指向名为 `sel_dateacq.php` 脚本的链接。此脚本将按获取日期排序记录。最近获取的项目将列在第一个：

13. `<a href="sel_dateacq.php">按日期排序</a>` (最新)

14. 添加一个指向名为 `sel_bytitle.php` 脚本的链接。此脚本将按标题排序记录：

15. `<a href="sel_bytitle.php">按标题排序</a>`

16. 添加一个指向名为 `sel_byartist.php` 脚本的链接。此脚本将按艺人排序记录：

17. `<a href="sel_byartist.php">按艺人排序</a>`

18. 关闭无序列表：

19. `</ul>`

20. `</body>`

21. `</html>`

22. 将文件命名为 `menu.html` 并放在根目录。

23. 打开浏览器并输入 127.0.0.1/menu.html

# 从 my_music 表选择数据

在后续章节中，你将学习如何修改表格，使该字段确实是唯一的并且自动递增，这样你就就不需要不断输入数字并寄希望它有效了。

# 按 ID 选择数据

到此时，你已经愉快且反复地用 my_music 表填充了你音乐收藏中的所有项目——或者至少是几个。

# 按日期选择数据

# 按标题选择数据

# 按艺人选择数据

括号中是艺术家名称。接下来是一个换行符，然后是你的备注，最后是一个包含获取日期格式的强调性括号语句：

```php
45. $display_block = "
46. <p><<strong>($artist fullname)</strong><br>
47. $my_notes <em>(获取日期: $date_ac, 格式: $format)</em></p>";


48. 关闭 while 循环，然后是你的 PHP 块：
49. }
50. ?>
51. 添加此 HTML：
```html

52. <html>

53. <HEAD>

54. <TITLE>我的音乐（按 ID 排序)</TITLE>

55. </HEAD>

56. <body>

57. <h1>按 ID 排序的我的音乐</h1>

```
58. 显示结果：
```php

59. <?php echo "$display_block"; ?>

```
60. 添加一个返回主菜单的链接，然后添加更多 HTML 以形成一个有效的文档：
```html

61. <a href="my_menu.html">返回菜单</a>

62. </body>

63. </html>

```
64. 将文件保存为 sel_by_id.php，并将此文件放置在你 Web 服务器的文档根目录下。
65. 打开你的 浏览器并输入 http://127.0.0.1/my_music.html
66. 点击“按 ID 排序”的链接。

在下一节中，你将创建一个按获取日期排序显示结果脚本。

# 按获取日期显示记录

虽然这不是一个必填字段，但记录添加脚本有一个空间用于记录进入你音乐收藏的日期。在这个脚本中，你将选择 my_music_table 中的所有记录，并按此日期排序，使最近获取的排在列表前面。

- 1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：
```php

2. <?php

```
3. 创建一个变量来存储表所在的数据库名称：
4. $db_name = "testDB";
5. 创建一个变量来存储你正在使用此脚本查询的表名：
6. $table_name = "my_music";
7. 按照你之前的方法添加连接信息：
```php

8. $connection = @mysql_connect("localhost","spike","95j7En4")

9. or die($mysql_error());

```
10. 如你所学的那样选择数据库：

```php

11. $db = @mysql_select_db($db_name, $connection) or

12. die($mysql_error());

```
13. 创建 SQL 语句，使用通配符选择所有字段：
14. $sql = "SELECT * FROM $table_name ORDER BY date_acq DESC";

15. 创建一个变量来存储 mysql_query() 函数的结果，如你所学的那样：
16. $result = @mysql_query($sql,$connection) or die($mysql_error());

17. 开始 while 循环。while 循环将为结果集($result) 中的每条记录创建一个数组 $row：
```php

18. while($row = @mysql_fetch_array($result)) {

```
19. 获取结果的各个元素，并给它们起好名字。对任何可能添加了斜杠的自由文本添加 stripslashes()：
20. $id = $row['id'];
21. $format = $row['format'];
22. $title = stripslashes($row['title']);
23. $artist_fn = stripslashes($row['artist_fn']);
24. $artist_in = stripslashes($row['artist_in']);
25. $rec_label = stripslashes($row['rec_label']);
26. $my_notes = stripslashes($row['my_notes']);
27. $date_acq = stripslashes($row['date_acq']);

28. 对艺术家名称进行一些格式化。由于某些艺术家只有名字，且有些姓名被丢进了 artist_in 字段中，开始一个 if...else 块来处理这种情况。查找：

```php

29. if ($artist_fn != "") {

30. 创建名为 $artist_full 的变量，它将包含一个字符串，$artist_fn 后面跟着一个空格，然后是 $artist_in，都在 trim() 函数内：

31. $artist_full = trim($artist_fn." ".$artist_in);

```
32. 注意 trim() 函数可以删除字符串开头和结尾多余的空格。

33. 继续该块，将修剪后的 $artist_in 值赋值给 $artist_full：
34. } else {
35. $artist_full = trim($artist_fn);
36. }

37. 再进行一些格式化。如果你没有在 date_acq 字段中输入日期，MySQL 将输入默认值 0000-00-00。创建一个代码块来查找此值并将其替换为更友善的内容：

```php

38. if ($date_acq == "0000-00-00") {

39. $date_acq = "unknown";

40. }

```
41. 创建一个名为 $display_block 的变量，括号中是艺术家名称。接下来是一个换行符，然后是你的备注，最后是一个包含获取日期格式的强调性括号语句：

```php

45. $display_block = "

46. <p><strong>($artist fullname)</strong><br>

47. $my_notes <em>(获取日期: $date_ac, 格式: $format)</em></p>";

48. 关闭 while 循环，然后是你的 PHP 块：

49. }

50. ?>

51. 添加此 HTML：

```html
52. <html>
53. <HEAD>
54. <TITLE>我的音乐（按 ID 排序)</TITLE>
55. </HEAD>
56. <body>
57. <h1>按 ID 排序的我的音乐</h1>
```

58. 显示结果：

```php
59. <?php echo "$display_block"; ?>
```

60. 添加一个返回主菜单的链接，然后添加更多 HTML 以形成一个有效的文档：

```html
61. <a href="my_menu.html">返回菜单</a>
62. </body>
63. </html>
```

64. 将文件保存为 sel_by_id.php，并将此文件放置在你 Web 服务器的文档根目录下。

65. 打开你的 浏览器并输入 http://127.0.0.1/my_music.html

66. 点击“按 ID 排序”的链接。

在下一节中，你将创建一个按获取日期排序显示结果脚本。

# 按获取日期显示记录

虽然这不是一个必填字段，但记录添加脚本有一个空间用于记录进入你音乐收藏的日期。在这个脚本中，你将选择 my_music_table 中的所有记录，并按此日期排序，使最近获取的排在列表前面。

选择 my_music_table 中的所有记录，按字母顺序排序。

- 1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

```php
2. <?php
```

3. 创建一个变量来存储表所在的数据库名称：

4. $db_name = "testDB";

5. 创建一个变量来存储你正在使用此脚本查询的表名：

6. $table_name = "my_music";

7. 按照你之前的方法添加连接信息：

```php
8. $connection = @mysql_connect("localhost","spike","95j7En4")
9. or die($mysql_error());
```

10. 如你所学的那样选择数据库：

```php
11. $db = @mysql_select_db($db_name, $connection) or
12. die($mysql_error());
```

13. 创建 SQL 语句，使用通配符选择所有字段：

14. $sql = "SELECT * FROM $table_name ORDER BY title";

15. 创建一个变量来存储 mysql_query() 函数的结果，如你所学的那样：

16. $result = @mysql_query($sql,$connection) or die($mysql_error());

17. 开始 while 循环。while 循环将为结果集($result) 中的每条记录创建一个数组 $row：

```php
18. while($row = mysql_fetch_array($result)) {
```

19. 获取结果的各个元素，并给它们起好名字。对任何可能添加了斜杠的自由文本添加 stripslashes()：

20. $id = $row['id'];

21. $format = $row['format'];

22. $title = stripslashes($row['artist_name']);

23. $artist_fn = stripslashes($row['artist_fn']);

24. $artist_in = stripslashes($row['artist_in']);

25. $rec_label = stripslashes($row['rec_label']);

26. $my_notes = stripslashes($row['my_notes']);

27. $date_acq = stripslashes($row['date_acq']);

46. ";

47. 关闭 while 循环，然后关闭你的 PHP 块：

48. }

49. ?> 添加此 HTML：

50. <HTML>

51. <HEAD>

52. <TITLE>我的音乐（按标题排序）</TITLE>

53. </HEAD>

54. <BODY>

55. <h1>我的音乐：按标题排序</h>

56. 显示结果：

57. <?php echo "$block"; ?>

58. 添加一个返回主菜单的链接，并添加更多 HTML 以构建有效的文档：

59. <a href="my_music.html">返回菜单</a></a></p>

60. </body>

61. </HTML>



## 将文件保存为 `set_by_title.php`

将文件保存为 `set_by_title.php`，并将此文件放在 Web 服务器的文档根目录下。

## 打开浏览器并访问

打开你的浏览器并输入 `http://127.0.0.1/my_music.html`。

## 点击链接

点击“按标题排序”的链接。

![image](img/bc248f3d24697d1afbacee37b9c4d229_146_0.png)

> *你的记录将与我的不同，但你应该会看到像这样的屏幕，其中记录是按标题排序的*

在下一节中，你将创建一个按艺术家名称排序显示结果的脚本。

# 按艺术家显示记录

这个脚本稍微复杂一点，因为你必须考虑与艺术家名称相关的问题：有些人有名字，有些既有名又有姓，而乐队名称也被包含在 `artist_name` 中。在这个脚本中，你将选择 `my_music` 表中的所有记录，并按艺术家全名的字母顺序排序。

## 步骤

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：
   ```php
   <?php
   ```

2. 创建一个变量来存储该表所在的数据库名称：
   ```php
   $db_name = "testDB";
   ```

3. 创建一个变量来存储你正在查询的表名，使用此脚本：
   ```php
   $table_name = "my_music";
   ```

4. 按照你之前的方法添加连接信息：
   ```php
   $connection = mysqli_connect("localhost", "spike", "9sj7En4")
   or die(mysql_error());
   ```

5. 选择你学过的数据库：
   ```php
   $db = @mysql_select_db($db_name, $connection) or
   die(mysql_error());
   ```

6. 创建 SQL 语句。回到那个在 SELECT 语句中命名所有字段的方法：
   ```php
   $sql = "SELECT id, format, title, trim(concat(artist_fn,
   ' ', artist_in)) as artist_fullname, rec_label, my_notes, date_acq
   FROM $table_name ORDER BY artist_fullname";
   ```

   注意在该 SQL 语句中，你本质上是在从两个已存在的字段创建一个新字段，使用 `concat()` 函数（一个 MySQL 字符串函数）将 `artist_fn` 和 `artist_in` 结合，中间留一个空格。

   使用 `artist_fullname` 将此新值分配给名为 `artist_fullname` 的字段。例如，如果你拥有 David Gray 的《White Ladder》。艺术家的名 "David" 和姓 "Gray" 将进入表单中相应的区域，但输出时将作为一个字符串 "David Gray" 输出。

   `trim()` 函数仍然会去除空格。短语 `concat(artist_fn,' ',artist_in) as artist_fullname` 替换了在之前的脚本循环中常见的 `if...else` 块。

7. 创建一个变量来存储 `mysql_query()` 函数的结果，正如你所学的那样：
   ```php
   $result = @mysql_query($sql, $connection) or die(mysql_error());
   ```

8. 开始 while 循环。循环将为结果集 (`$result`) 中的每条记录创建一个数组 `$row`：
   ```php
   while ($row = $mysql_fetch_assoc($result)) {
   ```

9. 获取记录的各个元素并给它们命名。记住，你有一个了一个新字段 `artist_fullname`。在你已添加的任何文本字段周围加上 `striplashes()` 函数：
   ```php
   $id = $row['id'];
   $format = $striplashes($row['format']);
   $title = $striplashes($row['title']);
   $artist_fullname = $striplashes($row['artist_fullname']);
   $rec_label = $striplashes($row['rec_label']);
   $my_notes = $striplashes($row['my_notes']);
   $date_acq = $row['date_acq'];
   ```

   如果你不在 `date_acq` 字段中输入日期，MySQL 将输入默认的 `0000-00-00`。创建一个 if 字段来查找此日期，然后将其替换为更友好的：
   ```php
   if ($date_acq == "0000-00-00") {
       $date_acq = "unknown";
   }
   ```

10. 创建一个变量 `$display_block` 来存储所有格式化后的记录。此块中的格式化将录音的标题加粗，随后是括号中的艺术家名称。接着是一个换行，然后是你的笔记，最后是包含日期和格式的强调语句。
    ```php
    $display_block = "<p><strong>$title</strong> <strong>$artist_fullname</strong><br>$date_acq $format</p>";
    ```

11. 关闭 while 循环，然后你的 PHP 块：
    ```php
    }
    ?>
    ```

12. 添加此 HTML：
    ```html
    <HTML>
    <HEAD>
    <TITLE>我的音乐（按标题排序）</TITLE>
    </HEAD>
    <body>
    <h1>我的音乐：按标题排序</h1>
    显示结果：
    <?php echo "$display_block"; ?>
    ```

13. 添加一个返回主菜单的链接，并添加更多 HTML 以构建有效的文档：
    ```html
    <a href="my_music.html">返回菜单</a></p>
    </body>
    </HTML>
    ```

14. 将文件保存为 `set_by_title.php`，并将此文件放在 Web 服务器的文档根目录下。

15. 打开你的浏览器并输入 `http://127.0.0.1/my_music.html`。

16. 点击按标题排序的链接。

![image](img/bc248f3d24697d1afbacee37b9c4d229_148.png)

接下来的章节将通过你学习用户验证、Cookies 和 Session 来提供数据库工作。

# V 部分：用户验证与跟踪

## 列表

- 第 15 章：数据库驱动验证
- 第 16 章：使用 Cookies
- 第 17 章：Session 基础

# 第 15 章：数据库驱动验证

## 概述

每个人都有不想与全世界分享的秘密。但某些秘密可以与特定的人共享。在本章中你将学习如何：

- 为授权用户创建一个数据库表
- 创建在显示秘密之前验证用户的登录表单和脚本

## 为什么要进行验证？

在最初开发网站时，你可能希望限制开发团队的某些成员访问。如果你的公司网站包含财务数据，你可能希望将财务信息限制给特定的投资者。或者你不想让人们看到个人隐私。

一种常见的用户验证类型是**数据库驱动**的，将用户名和密码存储在数据库表中，并通过登录表单和脚本访问。在下一节中，你将创建此数据库表并添加用户。

## 创建用户表

在第 12 章“创建表”中，你遵循了两步建表过程。现在你可以使用相同的过程来创建 `auth_users` 表。

- 打开浏览器访问 `http://127.0.0.1/create_table.html`
- 在表名字段输入 **auth_users**。
- 在字段数量字段输入 **4**。
- 点击“转到第 2 步”按钮。你会看到一个有四行的表单，对应 `auth_users` 表中的字段。
- 在第一行，字段名输入 **f_name**，在字段类型下拉菜单中选择 `varchar`，并指定长度为 **50**。该字段将存储用户的名。
- 在第二行，字段名输入 **l_name**，在字段类型下拉菜单中选择 `varchar`，并指定长度为 **50**。该字段将存储用户的姓。
- 在第三行，字段名输入 **username**，在字段类型下拉菜单中选择 `varchar`，并指定长度为 **25**。该字段将存储用户名。
- 在第四行，字段名输入 **password**，在字段类型下拉菜单中选择 `varchar`，并指定长度为 **100**。该字段将存储密码的哈希。

![image](img/bc248f3d24697d1afbacee37b9c4d229_150.png)

在下一节中，你将创建一个记录添加表单并将用户添加到 `auth_users` 表。

## 向你的表添加用户

一个空的 `auth_users` 表毫无用。在本节中，你将创建一个简单的记录添加表单和脚本，类似于你在第 13 章“向表中插入数据”中创建的那些。

### 创建用户添加表单和脚本

HTML 表单将包含 `auth_users` 表中的每一列一个输入字段。

1. 在你的文本编辑器中打开一个新文件并输入以下 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>添加用户</TITLE>
   </HEAD>
   <body>
   <h1>向 auth_users 添加记录</h1>
   ```

2. 开始你的表单。假设方法是 POST，动作是一个名为 `do_adduser.php` 的脚本：
   ```html
   <FORM METHOD="POST" ACTION="do_adduser.php">
   ```

3. 为用户的名创建一个输入字段，并带有文本标签：
   ```html
   <p><strong>名：</strong><br>
   <input type="text" name="f_name" size=25 maxlength=50></p>
   ```

4. 为用户的姓创建一个输入字段，并带有文本标签。
   ```html
   <p><strong>姓：</strong><br>
   <input type="text" name="l_name" size=25 maxlength=50></p>
   ```

5. 为用户名创建一个输入字段，并带有文本标签：
   ```html
   <p><strong>用户名：</strong><br>
   <input type="text" name="username" size=25 maxlength=25></p>
   ```

6. 为密码创建一个输入字段，并带有文本标签。
   ```html
   <p><strong>密码：</strong><br>
   <input type="text" name="password" size=25 maxlength=25></p>
   ```

   字段最大长度为 100。长度上的这种差异考虑了将要发生的加密。在该字段中输入的 25 个字符的明文密码在加密后其长度可能会超过 25 个字符。由于数据库中只存储加密后的密码，较大的最大长度将处理这些数据。

7. 添加一个提交按钮，关闭你的表单并添加一些额外的 HTML 以使文档有效：
   ```html
   <INPUT TYPE="SUBMIT" NAME="submit" VALUE="Add User"></P>
   </FORM>
   </BODY>
   </HTML>
   ```

8. 将文件保存为 `show_adduser.html` 并将此文件放在你的 Web 服务器的文档根目录下。

9. 打开你的网络浏览器并输入 `http://127.0.0.1/show_adduser.html`。

你将看到一个用于添加用户的表单，包含四个用于姓名和密码信息的字段以及一个提交按钮。接下来，你将为记录添加表单创建后端脚本。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：
   ```php
   <?
   ```

2. 检查所有四个字段是否都输入了值。如果没有，将用户重定向到表单并退出脚本：
   ```php
   if (isset($_POST[name]) || isset($_POST[username]) || isset($_POST[password])) {
       header("Location: http://127.0.0.1/show_adduser.html");
       exit;
   }
   ```

3. 创建一个变量来存储表所在的数据库名称：
   ```php
   $db_name = "testDB";
   ```

4. 创建一个变量来存储你用此脚本填充的表名称：
   ```php
   $table_name = "auth_users";
   ```

5. 按照你所学的方法添加连接信息：
   ```php
   $connection = @mysql_connect("localhost", "spike", "9sj7En4")
   or die(mysql_error());
   ```

6. 如你学的那样选择数据库：
   ```php
   $db = @mysql_select_db($db_name, $connection) or die(mysql_error());
   ```

7. 创建 SQL 语句。第一个括号语句给出要填充的字段名称（按顺序），第二个括号语句发送实际的字符串：
   ```php
   $sql = "INSERT INTO $_table (f_name, l_name, username,
   password) VALUES ('{$_POST[f_name]}', '{$_POST[l_name]}',
   '{$_POST[username]}, '{$_POST[password]}";
   ```

   注意 password 函数插入的是密码的哈希，而不是密码本身。这缓解了数据库中存在明文密码的安全风险。

8. 创建一个变量来存储 `mysql_query()` 函数的结果，如你所学的那样：
   ```php
   $result = @mysql_query($sql,$connection) or die(mysql_error());
   ```

9. 关闭你的 PHP 块，然后添加 HTML：
   ```php
   ?>
   <HTML>
   <HEAD>
   <TITLE>Add a User</TITLE>
   </HEAD>
   <BODY>
   <h1>Add to users:</h1>
   混合 HTML 和 PHP 以显示每个字段的值，从第一个名字开始：
   <p>First Name:</p><BR>
   <?php echo "${$_POST[f_name]}"; ?></p>
   <p>Last Name:</p><BR>
   <?php echo "${$_POST[l_name]}"; ?></p>
   <p>Username:</p><BR>
   <?php echo "${$_POST[username]}"; ?></p>
   <p>Password:</p><BR>
   <?php echo "${$_POST[password]}"; ?></p>
   添加一个返回原始表单的链接：
   <a href="show_adduser.html">Add Another</a></p>
   添加一些额外的 HTML 以使文档有效：
   </BODY>
   </HTML>
   ```

你的代码看起来应该是这样：

```php
<?php
//检查必填字段
if (!($_POST[f_name]) || (!($_POST[l_name]) || (!($_POST[username])
 || (!($_POST[password])) {
header("Location: http://127.0.0.1/show_adduser.php");
exit();
}
//设置数据库和表的名称
$db_name = "testDB";
$table_name = "auth_users";
```

```
//连接到服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9j7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or
die(mysql_error());

//创建并插入查询
$sql = "INSERT INTO table_name (f_name, l_name, username, password) 
VALUES ('$_POST[f_name]', '$_POST[l_name]', '$_POST[username]', '$_POST[password]}";

<HTML>
<HEAD>
<TITLE>Add a User</TITLE>
</HEAD>
<BODY>
<h1>Added to users:</h1>
<p>First Name</p>
<p>Last Name</p>
<p>Username</p>
<p>Password</p>
<a href="show_adduser.html">Add Another</a></p>
```

```html
<HTML>
<HEAD>
<TITLE>秘密区域</TITLE>
</HEAD>
<BODY>

显示消息：

<? echo "$msg"; ?>

添加一些额外的 HTML 以使文档有效：

</BODY>
</HTML>
```

将文件保存为 `do_autouser.php`，并将此文件放置在 Web 服务器的文档根目录中。

你的代码应该像这样：

```php
<?
//检查所需的必填字段
if (!$_POST['username']) || (!$_POST['password'])) {
header("Location: http://127.0.0.1/show_login.html");
exit();
}
```

```php
//设置使用的数据库名称和表名
$db_name = "testDB";
$table_name = "auth_users";
```

```php
//连接服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9j7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection);
```

```php
//构建并插入查询
$sql = "SELECT * FROM $table_name WHERE username='$_POST['username']' AND password='$_POST['password']';";
```

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

```php
//获取结果中的行数
$num = mysql_num_rows($result);
```

```php
//根据结果打印消息或重定向到其他地方
if ($num == 0) {
$msg = "<p>恭喜，你获得了授权！</p>";
} else {
header("Location: http://127.0.0.1/show_login.html");
exit();
}
```

```html
<HTML>
<HEAD>
<TITLE>秘密区域</TITLE>
</HEAD>
<BODY>
<? echo "$msg"; ?>
</BODY>
</HTML>
```

接下来你就可以测试登录表单了！

## 尝试验证你的身份

在本节中，你将尝试以 `auth_users` 表中添加的用户之一身份登录。你的结果将取决于你使用的用户名和密码。要进入登录表单，请打开 Web 浏览器并输入 `http://127.0.0.1/show_login.html`。

![](img/bc248f3d24697d1afbacee37b9c4d229_157_0.png)

在我点击“登录”按钮后，我被带回了登录页面，因为用户名和密码都是无效的。

注意：任何错误的用户名和错误的密码的组合都会导致验证失败。

![](img/bc248f3d24697d1afbacee37b9c4d229_157_1.png)

在[下一章]中，你将学习到 cookies，并且你将看到如何在身份验证方案中使用它们，或仅用于通用的用户跟踪。

# 第 16 章：使用 Cookies

## 概述

Cookies 是非常棒的小工具，但当坏人滥用它们时，它们在媒体中会饱受恶评。如果你正确使用它们，这些小文本片段会让你的开发工作变得简单得多。在本章中，你将学习执行以下操作：

- 设置 cookie
- 从 cookie 中提取数据
- 修改你的用户身份验证程序以使用 cookie

## 什么是 Cookie？

Cookies 是发送到用户 Web 浏览器的文本段。Cookies 可以帮助你创建购物车、用户社区和个性化网站。不建议你在 cookie 中存储敏感数据，但你可以存储一个唯一标识字符串，该字符串将与安全存储在数据库中的数据相匹配。

以购物为例。假设你为一个用户分配了一个标识变量，这样你就可以跟踪他在访问你的网站时所做的。首先，用户登录，你发送一个带有变量的 cookie，其设计目的是“这是 Joe，且 Joe 被允许访问白色区域”。当 Joe 在你的网站上浏览时，你可以在每一个页面都说：“你好，Joe”。如果 Joe 点击浏览你的目录并选择了 14 个不同的项目进行购买，你可以跟踪这些项目并在 Joe 去往结算区域时将它们全部显示出来。

## 设置 Cookies

在开始设置 cookie 之前，请确定你将如何使用它们以及在何时设置它们。无论你决定如何做，请记住，必须在向浏览器发送任何其他内容之前设置 cookie，因为 cookie 实际上是头部信息的一部分。

![](img/bc248f3d24697d1afbacee37b9c4d229_158_0.png)

如果你听从了这个警告，你将花费几个小时思考为什么收到“无法添加头部信息 (Cannot add header information)”的错误。这个示例代码正是如此。

![](img/bc248f3d24697d1afbacee37b9c4d229_158_1.png)

每当你看到此错误时，假设你已经向 Web 浏览器发送了内容。这包括空格、换行符或你可以看到的文本。

`setcookie()` 函数期望这些参数：

- **Name**：cookie 的名称。
- **Value**：cookie 的值。
- **Expiration**：cookie 过期的时间。
- **Path**：cookie 有效的服务器路径。
- **Domain**：cookie 有效的域名。
- **Secure**：如果设置，cookie 将通过 HTTPS 发送。

## 时间计数

| 值 | 定义 |
| :--- | :--- |
| 60 | 一分钟 |
| 900 | 15 分 |
| 1800 | 30 分 |
| 3600 | 一小时 |
| 14400 | 四 小时 |
| 43200 | 12 小时 |
| 86400 | 24 小时 |
| 259200 | 三天 |
| 604800 | 一周 |
| 2592000 | 三十天 |

## 设置测试 Cookie

此小脚本的目标是设置 cookie 并在屏幕上打印消息。在开始之前，确保你没有防火墙阻止传入 cookie。此外，修改你的 Web 浏览器设置以便提示 cookie。这是观察服务器尝试发送 cookie 的唯一方法。

1. 在文本编辑器中打开一个文件并启动 PHP 块，然后创建名为 `$cookie_name`、`$cookie_value`、`$cookie_expire` 和 `$cookie_domain` 的变量，并给它们赋予以下值：
   ```php
   $cookie_name = "test_cookie";
   $cookie_value = "test string";
   $cookie_expire = time()+86400;
   $cookie_domain = "127.0.0.1";
   ```

   > 注意：如果你的域名不是 127.0.0.1 (localhost)，请将 `$cookie_domain` 的值替换为你自己的域名。

2. 使用 `setcookie()` 函数设置此 cookie，然后关闭 PHP 块：
   ```php
   setcookie($cookie_name, $cookie_value, $cookie_expire, "/",
   $cookie_domain, 0);
   ```

3. 输入以下 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>设置测试 Cookie</TITLE>
   </HEAD>
   <BODY>
   <h1>1mmm...cookie!</h1>
   </BODY>
   </HTML>
   ```

4. 将文件保存为 `cookie.php`，并将此文件放置在 Web 服务器的根目录下。

5. 打开你的 Web 浏览器并输入 `http://127.0.0.1/setcookie.php`。

![](img/bc248f3d24697d1afbacee37b9c4d229_160_0.png)

点击“确定”接受 cookie。

![](img/bc248f3d24697d1afbacee37b9c4d229_161_0.png)

# 使用 Cookie 变量

在使用 Cookie 时，有一个元素大多数人都会忘记，直到他们花费几个小时试图调试一个根根本不是问题的东西（我也经历过这种情况）。当 Web 浏览器接受一个 Cookie 时，在发送下一次 HTTP 请求之前，你是无法提取它的值的。

换句话说，如果你在第 1 页上设置了一个值为 Julie 的 Cookie 名称，在用户到达第 2 页（或第 28 页——即任何不是初始设置 Cookie 的其他页面）之前，你无法提取出该值。

# 在身份验证中使用 Cookie

在上一章节的身份验证脚本中，你有一个登录表和一个结果页。然而，身份验证仅对结果页有效，因为它动态显示了秘密内容（在本例中为“恭喜！”）。如果你需要对某些静态页面进行身份验证，必须进行一些细微调整。

1. 在文本编辑器中打开 `do_auth.php`。
2. 滚动到处理身份验证结果的 `if...` 块。

添加一个设置 Cookie 的代码块：

```php
if ($name == 0) {
    $cookie_name = "auth";
    $cookie_value = "ok";
    $cookie_expire = "0";
    $cookie_domain = "127.0.0.1";
    setcookie($cookie_name, $cookie_value, $cookie_expire, "/",
    $cookie_domain, 0);
}
```

> [!CAUTION] 注意 Cookie 那行：它将在浏览器话结束时过期，并对 127.0.0.1 上的所有目录有效。如果适用，请使用你自己的域名。

3. 删除此行：
   `$msg = "<p>Congratulations, you're authorized!</p>";`

4. 添加此字符串：
   ```php
   $display_block = "
   <p><strong>秘密菜单：</strong></p>
   <ul>
       <li><a href=\"secretA.php\">秘密页面 A</a></li>
       <li><a href=\"secretB.php\">秘密页面 B</a></li>
   </ul>";
   ```

5. 注意：别担心；你很快就会创建这些页面。

6. 滚动直到看到以下内容：
   `<? echo "$msg"; ?>`

7. 将其替换为：
   `<? echo "$display_block"; ?>`

8. 保存文件。

你的新代码应该看起来所示：

```php
<?
//检查必填字段
if (($_POST[username]) || (!$_POST[password])) {
    header("Location: http://127.0.0.1/show_login.html");
    exit;
}

//设置要使用的数据库和表名
$db_name = "testDB";
$table_name = "auth_users";
//连接服务器并选择数据库
$connection = mysqli_connect("127.0.0.1", "spike", "9s7En4")
or die(mysql_error());

$db = mysqli_select_db($db_name, $connection)
die(mysql_error());

//构建并插入查询
$sql = "SELECT * FROM $table_name WHERE username = \n$_POST[username] AND password=\$_POST[password]";

$result = mysql_query($sql) or die(mysql_error());

//获取结果中的行数
$num = mysql_numrows($result);

//如果授权则打印消息并设置 Cookie，
//如果未授权则重定向到其他地方
if ($num == 1) {
    $cookie_name = "auth";
    $cookie_value = "ok";
    $cookie_expire = "0";
    $cookie_domain = "127.0.0.1";
    setcookie($cookie_name, $cookie_value, $cookie_expire, "/", $cookie_domain, 0);
}

$display_block = "
<p>秘密菜单:</p>
<ul>
    <li><a href=\"secretA.php\">秘密页面 A</a></li>
    <li><a href=\"secretB.php\">秘密页面 B</a></li>
</ul>
";
} else {
    header("Location: http://127.0.0.1/show_login.html");
    exit;
}
?>
```

```html
<HTML>
<HEAD>
<TITLE>秘密区域</TITLE>
</HEAD>
<BODY>
 <?php echo "display_block"; ?>
</BODY>
</HTML>
```

打开你的 Web 浏览器并输入 `http://127.0.0.1/show_login.html` 获取登录表单，然后输入用户名和密码。如果你仍然设置了在接受 Cookie 之前进行警告，你将看到一个包含变量信息的对话框。再次，此对话框因浏览器而异。

![](img/bc248f3d24697d1afbacee37b9c4d229_163_0.png)

当你点击“是”（或“确定”，取决于你的浏览器）后，将显示新菜单。

# 检查 Cookie

菜单链接到两个文件：`secretA.php` 和 `secretB.php`。通过向这些页面添加代码，你将能够检查授权用户。

1. 在文本编辑器中打开 `secretA.php`。
2. 在文件开头开始一个 PHP 块：
   ```php
   <?php
   if ($_COOKIE["auth"] == "ok") {
       $msg = "欢迎来到秘密 A!";
   } else {
       header("Location: http://127.0.0.1/show_login.html");
       exit;
   }
   ?>
   ```

3. 变量 `$msg` 将持有成功消息。

4. 在文本编辑器中打开 `secretB.php`。
5. 在文件开头开始一个 PHP 块：
   ```php
   <?php
   if ($_COOKIE["auth"] == "ok") {
       $msg = "欢迎来到秘密 B!";
   } else {
       header("Location: http://127.0.0.1/show_login.html");
       exit;
   }
   ?>
   ```

6. 注意 Cookie 那行：它将在浏览器话结束时过期，并对 127.0.0.1 上的所有目录有效。如果适用，请使用你自己的域名。

7. 在两个文件中添加以下 HTML 内容：
   ```html
   <HTML>
   <HEAD>
   <TITLE>秘密区域</TITLE>
   </HEAD>
   <BODY>
    <?php echo $msg; ?>
   </BODY>
   </HTML>
   ```

打开你的 Web 浏览器并输入 `http://127.0.0.1/show_login.html` 获取登录表单，然后输入用户名和密码。如果你仍然设置了在接受 Cookie 之前进行警告，你将看到一个包含变量信息的对话框。再次，此对话框因浏览器而异。

到此结束了对身份验证简短但实用的介绍。

# 第 17 章：会话基础

## 概述

Session 类似于 Cookie。使用 Session，你可以在不设置 Cookie 的情况下维护用户特定信息。在本章中，你将学习如何：

- 启动会话
- 向 `$_SESSION` 全局添加变量
- 在多个页面之间维护用户偏好

## 理解会话变量

会话变量（及其值）存储在 Web 服务器上的临时会话文件中。由于这些值和变量没有存储在数据库中，因此不需要额外的系统资源来连接和从数据库表中提取信息。你可以通过 `$_SESSION` 超全局变量访问会话变量。

例如，一个临时会话文件可能包含以下内容：

```
count[7]:"76";valid[7]:"yes";
```

在此示例中，count 和 value 是会话变量的名称，76 和 yes 是它们对应的值。然而，要将变量放入会话中，你必须先显式地将其添加到 `$_SESSION` 超全局变量。一旦添加，你就可以提取该值（在本示例中，使用 `$_SESSION[count]` 或 `$_SESSION[valid]`）。

当你尝试检索会话变量时，执行序列如下（这是你尝试获取 `$_SESSION[count]` 值的过程）：

1. PHP 解析器从用户 cookie 中获取 `PHPSESSID` 的值。
2. PHP 解析器找到匹配的会话文件。
3. 在会话文件内部，PHP 解析器查找 `count` 并找到它的值（例如，76）。
4. `$_SESSION[count]` 等于 76。

接下来，你将使用会话开始你的每个用户计数器脚本。

## 启动会话

启动会话非常轻而易举。你只需要调用 `session_start()` 函数，PHP 就会处理其余工作——发送 cookie 并创建会话文件。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
   ```php
   <?php
   ```

2. 调用 `session_start()` 函数：
   ```php
   session_start();
   ```

3. 创建一个存储消息的字符串：
   ```php
   $msg = "started a session...";
   ```

4. 关闭 PHP 块：
   ```php
   ?>
   ```

5. 输入以下 HTML：
   ```html
   <HTML>
   <HEAD>
   <TITLE>Start a Session</TITLE>
   </HEAD>
   <body>
   ```

6. 显示消息字符串：
   ```php
   <?php echo $msg; ?>
   ```

7. 添加一些额外的 HTML 以确保文档有效：
   ```html
   </BODY>
   </HTML>
   ```

8. 将文件保存为 `session.php`，并将此文件放在你的 Web 服务器的文档根目录下。

9. 打开 浏览器并输入 `http://127.0.0.1/session.php`。

这多么具有启发性呢？在[下一节](https://www.w3schools.com/php/php_session_set.asp?ref=https://www.w3schools.com/php/php_session_getstarted.asp)中，你将注册一个实际的值并在会话期间观察它的变化。

## 注册和修改会话变量

此脚本的目标是注册变量并在用户会话期间更改其值。

1. 在你的文本编辑器中打开一个新文件，开始 PHP 块，并调用 `session_start()` 函数：
   ```php
   <?php
   session_start();
   ```

2. 注册一个名为 `count` 的变量：
   ```php
   session_register('count');
   ```

   > 注意：现在，只要此会话存在，名为 `$_SESSION[count]` 的变量将是可用的。目前，该变量没有值。

3. 增加 `$_SESSION[count]` 的值以记录当前访问：
   ```php
   $_SESSION[count]++;
   ```

4. 创建一个存储消息的字符串，包括 `$_SESSION[count]` 的值：
   ```php
   $msg = "<p>You've been here, $_SESSION[count] times. Thanks!</p>";
   ```

5. 关闭 PHP 块并输入以下 HTML：
   ```php
   ?>
   <HTML>
   <HEAD>
   <TITLE>Count Met</TITLE>
   </HEAD>
   <BODY>
   ```

6. 显示消息字符串：
   ```php
   <?php echo "$msg"; ?>
   ```

7. 添加一些额外的 HTML 以确保文档有效：
   ```html
   </BODY>
   </html>
   ```

8. 将文件保存为 `countme.php`，并将此文件放在你的 Web 服务器的文档根目录下。

9. 打开 浏览器并输入 `http://127.0.0.1/countme.php`。

在下一节中，你将处理访问计数：将在用户会话期间设置并显示用户偏好。

## 使用会话管理用户偏好

除了简单的访问计数器，你可以使用会话在用户访问你的网站时管理他们的偏好。在这个三步示例中，你将启动一个会话，询问用户字体族和字体大小，在后续页面上显示这些偏好，并允许用户更改和重置值。

### 启动会话并注册默认值

在此脚本中，你将启动会话并注册 `font_family` 和 `font_size` 变量。显示的 HTML 将是一个允许你更改偏好的表单。

1. 在你的编辑器中打开一个新文件，开始 PHP 块并调用 `session_start()` 函数：
   ```php
   <?php
   session_start();
   ```

2. 注册 `font_family` 和 `font_size` 变量。显示的 HTML 将是一个允许你更改偏好的表单。

   *(注：由于原文后续部分存在严重的乱码重复，此处已根据前文逻辑完成了核心内容的翻译与对齐。)*

   ```html
   <STYLE>
   H1 {font-size: $font_size + 4pt;font-weight:bold;}
   </STYLE>
   <HEAD>
   <BODY>
   <h1>设置您的显示偏好</h1>
   <FORM METHOD="POST" ACTION="session02.php">
   <P>选择字体族：<br>
   <input type="radio" name="sel_font_family" value="serif"> serif
   <input type="radio" name="sel_font_family" value="sans-serif" checked="sans-serif">
   <input type="radio" name="sel_font_family" value="Courier"> Courier
   <input type="radio" name="sel_font_family" value="Wingdings"> Wingdings</P>
   <P>选择基础字体大小：<br>
   <input type="radio" name="sel_font_size" value="8"> 8pt
   <input type="radio" name="sel_font_size" value="10" checked>10pt
   <input type="radio" name="sel_font_size" value="12"> 12pt
   <input type="radio" name="sel_font_size" value="14"> 14pt</P>
   <P><input type="submit" name="submit" value="设置显示偏好"></P>
   </FORM>
   </BODY>
   </html>
   ```

   现在打开您的 浏览器并输入 `http://127.0.0.1/session01.php`。

   在下一节中，您将创建一个处理偏好更改的脚本。

### 修改偏好

在此脚本中，您将为 `font_family` 和 `font_size` 分配新值，并显示更改已完成。

1. 在您的文本编辑器中打开一个新文件，开始一个 PHP 块并调用 `session_start()`：
   ```php
   <?php
   session_start();
   ```

2. 使用 if {...else} 块来检查提交的 `font_family` 和 `font_size` 值。如果存在这些值，则将其加入会。
   ```php
   if (($_POST['sel_font_family']) && ($_POST['sel_font_size'])) {
       $font_family = $_POST['sel_font_family'];
       $font_size = $_POST['sel_font_size'];
       $_SESSION['font_family'] = $font_family;
       $_SESSION['font_size'] = $font_size;
   ```

3. 如果没有提交的值，则继续该块以检查之前存储的 `font-family` 和 `font-size` 值。
   ```php
   } else if (($_POST['sel_font_family']) && ($_SESSION['font_family']) &&
   ($_POST['sel_font_size']) && ($_SESSION['font_size'])) {
       $font_family = $_SESSION['font_family'];
       $font_size = $_SESSION['font_size'];
       $_SESSION['font_family'] = $font_family;
       $_SESSION['font_size'] = $font_size;
   ```

4. 最后，如果表单或之前的会话中不存在值，则定义并添加一些默认值：
   ```php
   } else {
       $font_family = "sans-serif";
       $font_size = "10";
       $font_family = $font_family;
       $font_size = $font_size;
   }
   ```

5. 关闭 PHP 块并输入以下 HTML：
   ```php
   ?>
   <HTML>
   <HEAD>
   <TITLE>我的显示偏好</TITLE>
   <STYLE type="text/css">
   ```

6. 为 BODY、P 和 A 标签添加样式表项。混合 HTML 和 PHP 以显示 `$font_family` 和 `$font_size` 的当前值：
   ```css
   BODY, P, A {font-family:<?php echo $font_family;?>;font-size:<?php
   echo $font_size;?>;font-weight:normal;}
   ```

7. 为 H1 标签添加样式表项。混合 HTML 和 PHP 以显示 `$font_family` 的值和 `$font_size` 的修改后的值（基础值加 4）：
   ```css
   H1 {font-family:<?php echo $font_family;?>;font-size:<?php
   $font_size + 4;?>;font-weight:bold;}
   ```

8. 关闭 `</STYLE>` 标签并继续处理 HTML，显示两个已注册会话变量的值：
   ```html
   </STYLE>
   </HEAD>
   <body>
   <h1>您的偏好已设置</h1>
   <p>如您所见，您选择的字体现在是 <?php echo "$font_size";?>；基础大小为 <?php echo "$font_size";?>
   </p>
   ```

9. 如果用户想更改偏好，则提供一个指向 `session01.php` 的链接，然后添加一些 HTML 使文档有效：
   ```html
   <p>欢迎再次点击 <a href="session01.php">更改您的偏好</a>。</p>
   </html>
   ```

将该文件命名为 `session02.php` 并保存在您的 Web 服务器的根目录中。您的整个代码应该像这样：

```php
<?php
session_start();

//check for posted values
if ($_POST['sel_font_family']) && ($_POST['sel_font_size']) {
  $font_family = $_POST['sel_font_family'];
  $font_size = $_POST['sel_font_size'];
  $_SESSION['font_family'] = $font_family;
  $_SESSION['font_size'] = $font_size;
} else if ($_POST['sel_font_family']) && ($_SESSION['font_family']) &&
($_POST['sel_font_size']) && ($_SESSION['font_size']) {
  $font_family = $_SESSION['font_family'];
  $font_size = $_SESSION['font_size'];
  $_SESSION['font_family'] = $font_family;
  $_SESSION['font_size'] = $font_size;
} else {
  $font_family = "sans-serif";
  $font_size = "10";
  $font_family = $font_family;
  $font_size = $font_size;
}
?>
<HTML>
<HEAD>
<TITLE>我的显示偏好</TITLE>
<STYLE type="text/css">
BODY, P, A {font-family:<?php echo $font_family;?>;font-size:<?php
echo $font_size;?>;font-weight:normal;}
H1 {font-family:<?php echo $font_family;?>;font-size:<?php
$font_size + 4;?>;font-weight:bold;}
</STYLE>
</HEAD>
<body>
<h1>您的偏好已设置</h1>
<p>如您所见，您选择的字体现在是 <?php echo "$font_size";?>；基础大小为 <?php echo "$font_size";?></p>
<p>欢迎再次点击 <a href="session01.php">更改您的偏好</a>。</p>
</body>
</HTML
```

17. 继续 if...else 语句：
    ```php
    } else {
    ```

    如果用户一直执行到这里，说明用户名和密码是正确的。创建一个名为 `$valid` 的变量，将其值为 yes，然后添加一个名为 valid 的会话变量，其值为 `$valid`：
    ```php
    $valid = "yes";
    $_SESSION[valid] = $valid;
    ```

    创建一个名为 `$show_menu` 的变量，并给它赋值为 yes。这个值将在脚本稍后的部分中被检查，以决定显示什么内容：
    ```php
    $show_menu = "yes";
    ```

    关闭内层的 if...else 块：
    ```php
    }
    ```

    继续外层的 if...else 块：
    ```php
    } else {
    ```

    如果用户处于外层 if...else 块的此区域，说明他没有通过表单就到达了此脚本。检查 `$SESSION[valid]` 的值，并决定显示什么——菜单还是表单：
    ```php
    if ($SESSION[valid] == "yes") {
        $show_menu = "yes";
    } else {
        $show_form = "yes";
    }
    }
    ```

    关闭外层的 if...else 块：
    ```php
    }
    ```

    创建表单块，如果用户未登录或登录错误，则将显示该块。首先创建变量并打印页头：
    ```php
    $form_block = "
    <h1>Login</h1>";
    ```

    开始表单。在这种情况下，方法是 POST，action 是一个名为 `$_SERVER[PHP_SELF]` 的变量：
    ```html
    <form method="POST" action="$_SERVER[PHP_SELF]">
    ```

    > 注意 `$_SERVER[PHP_SELF]` 是一个全局变量，其值等于当前脚本的。通过使用 `$_SERVER[PHP_SELF]` 作为表单动作，你实际上是在说：“当点击提交按钮时，重新加载我！”

    打印 `$msg` 的值：
    ```php
    $msg;
    ```

    > 注意，如果登录错误，`$msg` 将包含一个值，该值将在此处被打印。如果 `$msg` 没有被创建或没有赋值，则什么都不会打印，所以即使它存在那里也不会产生任何影响。

    为用户名和密码创建输入字段，并带有文本标签：
    ```html
    <input type="text" name="username" size="15" maxlength="25">
    <input type="password" name="password" size="15" maxlength="25">
    ```

    添加隐藏字段：
    ```html
    <input type="hidden" name="op" value="$val">
    ```

    添加提交按钮，并关闭表单字符串：
    ```html
    <input type="submit" name="submit" value="login">
    </FORM>;
    ```

    创建菜单块，如果用户已登录且有效，则将显示该块。首先创建变量并打印页头：
    ```php
    $menu_block = "
    <h1>My Contact Administration System</h1>
    ```

    添加几个菜单项，然后关闭字符串：
    ```html
    <ul>
    <li><a href="show_addcontact.php">Add a Contact</a></li>
    <li><a href="pick_modcontact.php">Modify a Contact</a></li>
    <li><a href="pick_delcontact.php">Delete a Contact</a></li>
    </ul>
    <strong>View Records</strong>
    <ul>
    <li><a href="show_contactsbyname.php">Show Contacts, Ordered by Name</a></li>
    </ul>
    ```

    使用 if...else 块进行最后的检查，以根据新变量 `$display_block` 的值决定应该显示哪个内容：
    ```php
    if ($show_form == "yes") {
        $display_block = $show_block;
    } else if ($show_menu == "yes") {
        $display_block = $menu_block;
    }
    ```

    关闭你的 PHP 块并添加 HTML：
    ```php
    ?>
    <HTML>
    <HEAD>
    <TITLE>My Contact Management System</TITLE>
    </HEAD>
    <BODY>
    显示结果：
    <?php echo $display_block; ?>
    添加更多 HTML 以使其成为一个有效的文档：
    </body>
    </HTML>
    ```

    将文件保存为 `contact_menu.php` 并将其放置在 Web 服务器的文档根目录下。

    你刚刚创建了大量的代码。它看起来应该像这样：

    ```php
    //开始会话
    session_start();

    // 检查用户是否来自表单
    if ($_POST[op] == "ds") {

        // 检查用户名和密码
        if ($_POST[username] != "admin" || $_POST[password] != "abc123") {
            //处理错误的登录
            $msg = "<p color='#FF0000'><<strong>Bad Login - Try Again</strong></p>";
            $show_form = "yes";
        } else {
            // 处理正确的登录
            $valid = "yes";
            $_SESSION[valid] = "yes";
            $show_menu = "yes";
        }
    } else {
        // 决定显示什么
        if ($valid == "yes") {
            $show_menu = "yes";
        } else {
            $show_form = "yes";
        }
    }

    // 构建表单块
    $form_block = "
    <h1>Login</h1>
    <form method='POST' action='$_SERVER[PHP_SELF]'>
        $msg
        <p><input type='text' name='username' size='15' maxlength='25'></p>
        <p><input type='password' name='password' size='15' maxlength='25'></p>
        <input type='hidden' name='op' value='ds'>
        <input type='submit' name='submit' value='login'></p>
    </form>";

    // 构建菜单块
    $menu_block = "
    <h1>My Contact Administration System</h1>

    <ul>
        <li><a href='show_addcontact.php'>Add a Contact</a></li>
        <li><a href='pick_modcontact.php'>Modify a Contact</a></li>
        <li><a href='pick_delcontact.php'>Delete a Contact</a></li>
    </ul>

    <p><strong>View Records</strong></p>
    <ul>
        <li><a href='show_contactsbyname.php'>Show Contacts, Ordered by Name</a></li>
    </ul>";

    // 分配显示块给 display_block
    if ($show_form == "yes") {
        $display_block = $form_block;
    } else if ($show_menu == "yes") {
        $display_block = $menu_block;
    }
    ?>
    <HTML><HEAD><TITLE>My Contact Management System</TITLE></HEAD><BODY>
    <?php echo $display_block; ?>
    </BODY></HTML>
    ```

    ```html
    <FORM METHOD="POST" ACTION="do_creatable.php">
    <INPUT TYPE="hidden" NAME="table_name" VALUE="$_POST[table_name]">
    <TABLE CELLSPACING=5 CELLPADDING=5>
    <TR>
    <TH NAME="TH"><TH TYPE="TH">FIELD LENGTH</TH><TH> PRIMARY KEY="TH"><TH> AUTO-INCREMENT="TH"></TH></TR>
    ```

    ```php
    //从 0 计数到字段数量
    for ($i = 0; $i < $_POST[num_fields]; $i++) {
      // 将添加到表单中，每个字段占一行
      $form_block .= "
    <TR>
    <TD ALIGN="CENTER"><INPUT TYPE="text" NAME="field_name[$i]" SIZE="20"/></TD>
    <TD ALIGN="CENTER"><SELECT NAME="field_type[$i]
    ```

    接下来，你将修改创建表脚本的最后部分。

    1. 在文本编辑器中打开 `do_createtable.php`。
    2. 在循环内部，第一行将文本附加到 `sql` 变量，该变量持有用于创建表的 SQL 语句。由于你已经为 SQL 语句的额外元素添加两个复选框，你需要对它们进行检查。首先创建一个 if...else 块，用来检查 `auto_increment` 复选框是否被被勾选：
       ```php
       if ($POST[auto_increment][$i] == "Y")
       ```

    3. 如果 `auto_increment` 复选框被勾选，创建一个变量来存储额外的 SQL 选项：
       ```php
       $additional = "NOT NULL null auto_increment";
       ```

    4. 当将字段标记为自动递增时，它也必须定义为 NOT NULL。

    5. 如果 `auto_increment` 复选框未被勾选，创建该变量但不放入任何文本，然后关闭代码块。这将有助于在循环继续时将字符串值重置为空：
       ```php
       } else {
       $additional = "";
       }
       ```

    6. 创建一个 if...else 块来检查主键复选框是否被勾选：
       ```php
       if ($POST[primary][$i] == "Y") {
       ```

    7. 如果主键复选框被勾选，将主键语法附加到 `$additional` 变量：
       ```php
       $additional = "primary key (\$POST[field_name][$i])";
       ```

       > 注意，字段作为主键的命名与初始字段定义用逗号分隔。它看起来像：`primary key (field_name)`

    8. 如果主键复选框未被勾选，则向 `$additional` 值附加一个空值，然后关闭代码块：
       ```php
       } else {
       $additional = "";
       }
       ```

    9. 最后一次修改是现有的字段长度循环，它创建了 SQL 语句的部分。找到如下所示的一行：
       ```php
       $sql = "(\$POST[field_length][$i])";
       ```

    10. 修改该行使其如下所示：这确保了该部分被放置在 SQL 语句的正确位置：
        ```php
        $sql = "(\$POST[field_length][$i]) \$additional,";
        ```

    11. 同样，找到如下所示的一行：
        ```php
        $sql = ",";
        ```

    12. 修改该行使其如下：
        ```php
        $sql = "\$additional,";
        ```

    13. 保存文件。

    你修改该脚本后的代码应该像下面：

    ```php
    <?
    //指定你想使用的数据库
    $db_name = "testDB";

    //连接数据库
    $connection = @mysql_connect("localhost", "spike", "9sj7En")
    or die(mysql_error());
    $db = @mysql_select_db($db_name, $connection) or
    ```

    ```php
    die(mysql_error());

    //开始 SQL 语句
    $sql = "CREATE TABLE $_POST[table_name] (";

    //为每个字段继续 SQL 语句
    for ($i = 0; $i < count($_POST[field_name]); $i++) {
      $sql .= "$POST[field_name][$i] = "" . \POST[field_type][$i];";

      if ($_POST[auto_increment][$i] == "Y") {
        $additional = "NOT NULL auto_increment";
      } else {
        $additional = "";
      }

      if ($_POST[primary][$i] == "Y") {
        $additional .= ", primary key (\$_POST[field_name][$i]).";
      } else {
        $additional = ",";
      }

      if ($_POST[field_length][$i] != "") {
        $sql .= " " \POST[field_length][$i]);";
      } else {
        $sql .= " " $additional,";
      }
    }

    // 清理字符串末尾
    $sql = substr($sql, 0, -1);
    $sql .= ")";

    // 执行查询
    $result = mysql_query($sql, $connection) or die(mysql_error());

    // 成功后获取一个良好的显示消息
    if ($result) {
      $msg = "<P>$_POST[table_name]. 已经创建。</P>";
    }
    ?>
    <html>
    <head>
    <title>创建表</title>
    </head>
    <body>
    <h1><?php echo $msg; ?></h1>
    </body>
    </html>
    ```

## 添加联系人

19. 开始你的表单。假设方法为 POST，action 为名为 `do_addcontact.php` 的脚本。

21. ```html
    <FORM METHOD="POST" ACTION="do_addcontact.php">
    ```

22. 开始一个 HTML 表格进行布局。开启新的一行，两个列标题，然后关闭该行：
    ```html
    <table cellspacing="3" cellpadding="5">
    <br>
    <th>姓名与地址信息</th>
    </tr>
    <br>
    ```

28. 开启新的一行和数据单元格，然后为人的名字创建一个输入字段，并带有文本标签：
    ```html
    <br>
    <td valign="top">
    <strong>名字：</strong><br>
    <input type="text" name="fname" size=35 MAXLENGTH=75></p>,
    ```

33. 在同一个数据单元格中，为人的姓氏创建一个输入字段，并带有文本标签：
    ```html
    <strong>姓氏：</strong><br>
    <input type="text" name="lname" size=35 MAXLENGTH=75></p>
    ```

36. 在同一个数据单元格中，为人的地址（第一行）创建一个输入字段，并带有文本标签：
    ```html
    <strong>地址行 1：</strong><br>
    <input type="text" name="address1" size=35 MAXLENGTH=100></p>
    ```

39. 在同一个数据单元格中，为人的地址（第二行）创建一个输入字段，并带有文本标签：
    ```html
    <strong>地址行 2：</strong><br>
    <input type="text" name="address2" size=35 MAXLENGTH=100></p>
    ```

42. 在同一个数据单元格中，为人的地址（第三行）创建一个输入字段，并带有文本标签：
    ```html
    <strong>地址行 3：</strong><br>
    <input type="text" name="address3" size=35 MAXLENGTH=100></p>
    ```

46. 在同一个数据单元格中，为人的邮政编码创建一个输入字段，并带有文本标签：
    ```html
    <strong>邮政编码：</strong><br>
    <input type="text" name="postcode" size=35 MAXLENGTH=25></p>
    ```

49. 在同一个数据单元格中，为人的国家创建一个输入字段，并带有文本标签。在此输入字段后关闭数据单元格：
    ```html
    <strong>国家：</strong><br>
    <input type="text" name="country" size=35 MAXLENGTH=100></p>
    </td>
    ```

53. 在一个新的数据单元格中，为人的电话号码创建一个输入字段，并带有文本标签：
    ```html
    <td valign="top">
    <strong>主电话：</strong><br>
    <input type="text" name="prim_tel" size=35 MAXLENGTH=75></p>
    ```

57. 在同一个数据单元格中，为人的次电话创建一个输入字段，并带有文本标签：
    ```html
    <strong>次电话：</strong><br>
    <input type="text" name="sec_tel" size=35 MAXLENGTH=75></p>
    ```

60. 在同一个数据单元格中，为人的邮箱地址创建一个输入字段，并带有文本标签：
    ```html
    <strong>邮箱地址：</strong><br>
    <INPUT TYPE="text" name="email" SIZE=35 MAXLENGTH=100>
    ```

63. 在同一个表格数据单元格中，为人的生日创建一个输入字段，并带有文本标签。在此输入字段后关闭表格数据单元格、表格行和表格本身：
    ```html
    <P><STRONG>生日 (YYYY-MM-DD)</STRONG><BR>
    <INPUT TYPE="text" NAME="birthday" SIZE=10 MAXLENGTH=10></P>
    <td>
    <tr>
    ```

    > 注意：你在 MySQL 中使用的日期使用 YYYY-MM-DD 格式。使用此格式的日期示例是 2002-03-20 (2000年3月20日)。

69. 开启一个新的跨两列的表格行和表格单元格。在内部添加一个返回主菜单的提交按钮。关闭表格数据单元格、表格行和表格本身：
    ```html
    <td align colspan="2"><br>
    <INPUT TYPE="SUBMIT" NAME="submit" VALUE="添加联系人到
    系统"></p>
    <p><a href="contact_menu.php">返回菜单</a></p>
    </td>
    </tr>
    </table>
    ```

77. 关闭表单并添加一些 HTML 以使文档有效：
    ```html
    </form>
    </body>
    </html>
    ```

81. 以 `add_contact.php` 命名文件，然后将其放在服务器根目录下。你的代码应该如下：

    ```php
    <?php
    // 开始会话
    session_start();

    // 验证用户是否允许在此操作
    if ($_SESSION[valid] == "yes") {
    header("Location:http://127.0.0.1/contact_menu.php");
    exit;
    }
    ?>
    <html
    <head>
    <TITLE>联系人系统：添加联系人</TITLE>
    </head>
    <body>
    <h1>联系人系统</h1>
    <h2>添加联系人 *</h2>
    <form method="POST" action="do_addcontact.php">
    <table cellspacing="3" cellpadding="5">
    <tr>
    <th>姓名与地址信息</th>
    <th>其他/个人信息</th>
    </tr>
    <tr>
    <td valign="top">
    <p>名字：</p><br>
    ```

    ```html
    <input type="text" name="fname" size=35 MAXLENGTH=75></p>
    ```

    ```html
    <p>姓氏：</p><br>
    <input type="text" name="lname" size=35 MAXLENGTH=75></p>
    ```

    ```html
    <p>地址行 1：</p><br>
    <input type="text" name="address1" size=35 MAXLENGTH=100></p>
    ```

    ```html
    <p>地址行 2：</p><br>
    <input type="text" name="address2" size=35 MAXLENGTH=100></p>
    ```

    ```html
    <p>地址行 3：</p><br>
    <input type="text" name="address3" size=35 MAXLENGTH=100></p>
    ```

    ```html
    <p>邮政编码：</p><br>
    <input type="text" name="postcode" size=35 MAXLENGTH=25></p>
    ```

    ```html
    <p>国家：</p><br>
    <input type="text" name="country" size=35 MAXLENGTH=100></p>
    </td>
    ```

    ```html
    <td valign="top">
    <p>电话号码：</p><br>
    <input type="text" name="prim_tel" size=35 MAXLENGTH=75></p>
    ```

    ```html
    <p>次电话：</p><br>
    <input type="text" name="sec_tel" size=35 MAXLENGTH=75></p>
    ```

    ```html
    <p>邮箱地址：</p><br>
    <input type="text" name="email" size=35 MAXLENGTH=100></p>
    ```

    ```html
    <p>生日 (YYYY-MM-DD)：</p><br>
    <input type="text" name="birthday" size=10 MAXLENGTH=10></p>
    </td>
    ```

    ```html
    <tr>
    <td align="center" colspan="2">
    <p><INPUT TYPE="SUBMIT" NAME="submit" value="添加到联系人系统"/></p>
    <p><a href="contact_menu.php">返回菜单</a></p>
    </td>
    </tr>
    ```

    ```html
    <TABLE>
    <FORM>
    <BODY>
    </HTML>
    ```

在下一节中，你将创建一个脚本，用于获取表单输入、创建 SQL 语句并将记录添加到数据库。

## 创建记录添加脚本

此脚本将你的记录添加到 `my_contacts` 表中，并考虑到自增 ID 字段。

1. 在文本编辑器中打开一个新文件并开启 PHP 块：
   ```php
   <?php
   ```

2. 开启 `if... else` 块检查 `$_POST [f_name]` 和 `$_POST[i_name]` 中的值。如果没有值，则将用户重回表单并退出脚本；
   ```php
   if ((_POST[f_name]) || ($_POST[i_name])) { // 注意：这里的 OCR 逻辑与标准逻辑相反，但我将遵循文本。
   ```

   > 注意：你可以根据需要设置任意（或少量）必填字段。

3. 如果必填字段有值，启动会话，或者如果当前存在则继续会话。然后关闭该块：
   ```php
   else {
       session_start();
   }
   ```

4. 开启 `if...else` 块检查 `$_SESSION[valid]` 的值并根据结果执行特定操作。如果值不是 `yes`，则用户没有通过适当的验证通道：
   ```php
   if ($_SESSION[valid] = "yes") {
   ```

5. 将用户送回登录表单并退出脚本：
   ```php
   header("Location:http://127.0.0.1/contact_menu.php");
   exit;
   }
   ```

6. 创建一个变量来存储表所在的数据库名称：
   ```php
   $db_name = "testDB";
   ```

7. 创建一个变量来存储你要填充的表名：
   ```php
   $table_name = "my_contacts";
   ```

8. 按照你的方法添加连接信息：
   ```php
   $connection = @mysql_connect("localhost", "s7")
   or die(mysql_error());
   ```

9. 按照你的方法选择数据库：
   ```php
   $db = @mysql_select_db($db_name, $connection)
   die(mysql_error());
   ```

10. 创建 SQL 语句。第一个语句给出要填充的字段（按顺序），第二个语句给出实际字符串：
    ```php
    $sql = "INSERT INTO $table (f_name, l_name, address1, address2, address3, postcode, country, prim_tel, email, birthday) VALUES ('$POST[f_name], '$POST[l_name], '$POST[address1], '$POST[address2], '$POST[address3], '$POST[postcode], '$POST[country], '$POST[prim_tel], '$POST[email], '$POST[birthday])";
    ```

    > 留出一个空的 ID 字段将确保它会自动自增。

11. 按照你的方法创建一个变量来存储 `mysql_query()` 函数的结果：
    ```php
    $result = @mysql_query($sql, $connection) or die(mysql_error());
    ```

12. 关闭你的 PHP 块并添加此 HTML：
    ```php
    ?>
    <HTML>
    <HEAD>
    <TITLE>联系人系统：添加联系人</TITLE>
    </HEAD>
    <BODY>
    <h1>联系人系统</h1>
    <h2>添加联系人 - 联系人已添加</h2>
    ```

13. 添加一条确认语句。将 HTML 和 PHP 混合到 `$table_name` 变量的值：
    ```html
    <p>以下信息已成功添加到：</p>
    <?php echo "$table_name"; ?></p>
    ```

14. 接下来，你将重新创建在 addcontact.php 中所示的布局，但它不包含表单字段。相反，你将混合 HTML 和 PHP 来显示已输入的值。
    ```php
    <table cellspacing="5">
    <tr>
    <th>姓名与地址信息</th>
    </tr>
    <tr>
    <th>其他联系/个人信息</th>
    </tr>
    <tr>
    <td valign="top">
        <p><strong>名字：</strong><BR>
        <?php echo $_POST['first_name']; ?>
        </p>
        <p><strong>姓氏：</strong><BR>
        <?php echo $_POST['last_name echo $_POST['last_name']; ?>
        </p>
        <p><strong>地址第 1 行：</strong><BR>
        <?php echo $_POST['address1']; ?>
        </p>
        <p><strong>地址第 2 行：</strong><BR>
        <?php echo $_POST['address2']; ?>
        </p>
        <p><strong>地址第 3 行：</strong><BR>
        <?php echo $_POST['address3']; ?>
        </p>
        <p><strong>邮政编码：</strong><BR>
        <?php echo $_POST['zip']; ?>
        </p>
        <p><strong>邮政编码：</strong><BR>
        <?php echo $_POST['postcode']; ?>
        </p>
        <p><strong>国家：</strong><BR>
        <?php echo $_POST['country']; ?>
        </p>
        <p><strong>主电话号码：</strong><BR>
        <?php echo $_POST['primtel']; ?>
        </p>
        <p><strong>次电话号码：</strong><BR>
        <?php echo $_POST['secttel']; ?>
        </p>
    ```



# 联系人管理系统开发指南

## 添加联系人

### 显示添加联系人表单

进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`。

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```php
if (condVar > someVal) {console.log("xxx")}
```

### 处理添加联系人表单提交

```php
<?php
// 检查所需的变量
if (!isset($_POST['first_name']) || !isset($_POST['last_name'])) {
    header("Location: http://127.0.0.1/show_addcontact.php");
    exit;
}
```

```php
} else {
    // 如果表单变量存在，则启动会话
    session_start();
}

// 检查用户有效性
if ($_SESSION["valid"] == "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}

// 设置表名和数据库名
$db_name = "testDB";
$table_name = "my_contacts";

// 连接到服务器并选择数据库
$connection = @mysql_connect("localhost","spike","9sj7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or
die(mysql_error());

// 构建并执行查询
$sql = "INSERT INTO table_name (id, f_name, l_name, address1, address2, address3, country, prim, tel, email, birthday)
VALUES ('$_POST[f_name]', '$_POST[l_name]', '$_POST[address1]', '$_POST[address2]', '$_POST[address3]', '$_POST[postcode]', '$_POST[country]', '$_POST[prim]', '$_POST[tel]', '$_POST[birthday]')";
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

```html
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：已添加联系人</TITLE>
</HEAD>
<BODY>
<h1>我的联系人管理系统</h1>
<h2><em>添加联系人 - 已添加联系人</em></h2>
<p>以下信息已成功添加到：</p>
<table cellpadding="5">
<tr>
<th>姓名与地址信息</th>
</tr>
<tr>
<th>其他联系/个人信息</th>
</tr>
<tr>
<td>
    <p><strong>名字：</strong><BR>
    <?php echo $_POST['f_name']; ?></p>
    <p><strong>姓氏：</strong><BR>
    <?php echo $_POST['l_name']; ?></p>
    <p><strong>地址第 1 行：</strong><BR>
    <?php echo $_POST['address1']; ?></p>
    <p><strong>地址第 2 行：</strong><BR>
    <?php echo $_POST['address2']; ?></p>
    <p><strong>地址第 3 行：</strong><BR>
    <?php echo $_POST['address3']; ?></p>
    <p><strong>邮政编码：</strong><BR>
    <?php echo $_POST['postcode']; ?></p>
    <p><strong>国家：</strong><BR>
    <?php echo $_POST['country']; ?></p>
</td>
<td valign="top">
    <p><strong>主电话号码：</strong><BR>
    <?php echo $_POST['prim_tel']; ?></p>
    <p><strong>次电话号码：</strong><BR>
    <?php echo $_POST['secttel']; ?></p>
    <p><strong>邮箱地址：</strong><BR>
    <?php echo $_POST['email']; ?></p>
    <p><strong>出生日期 (YYYY-MM-DD)：</strong><BR>
    <?php echo $_POST['birthday']; ?></p>
</td>
</tr>
</table>
</BODY>
</HTML>
```

将文件保存为 `addcontact.php` 并将此文件放在你的 Web 服务器的文档根目录下。

## 修改联系人

### 创建记录选择表单

永远不会这一步，所以你无需担心变量被覆盖，可以开始创建你的表单。对于表单，假设方法为 POST，action 是名为 `show_modcontact.php` 的脚本：

```php
$display_block = "
<FORM METHOD=\"POST\" ACTION=\"show_modcontact.php\">
为下拉菜单创建一个文本标签：
<p>Contact:</p>
开始下拉菜单：
<select name=\"id\">
将 `$option_block` 字符串放在 `<select> </select>` 标签对内部。它应该至少包含一个 `<option>` 元素：
<option>
完成下拉菜单：
</select>
添加一个提交按钮：
<INPUT TYPE=\"SUBMIT\" NAME=\"submit\" VALUE=\"Select this
Contact\"/></p>
关闭你的表单、字符串、if...else 块以及 PHP 块：
</form>
}
?>
```

添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>My Contact Management System: Modify a Contact</TITLE>
</HEAD>
<BODY>
<h1>My Contact Management System</h1>
<h2>Modify a Contact - Select from List</h2></h2>
<p>从列表中选择一个联系人，以修改联系人的记录。</p>
显示 `$display_block` 的内容：
<echo "$display_block"; ?>
to
添加返回主菜单的链接：
<p><a href="contact_menu.php">Return to Main Menu</a>a></p>
添加一些 HTML 以确保文档有效：
</BODY>
</HTML>
```

将文件保存为 `pick_modcontact.php` 并将此文件放在 Web 服务器的文档根目录下。

你的代码看起来应该是这样的：

```php
<?php
//start a session
session_start();

//check validity of user
if ($_SESSION['valid'] != "yes") {
    header("Location:http://127.0.0.1/contact_menu.php");
    exit;
}

//set up table and database names
$db_name = "testDB";
$table_name = "my_contacts";
?>
```

```php
//connect to server and select database
$connection = @mysql_connect("localhost", "spike", "9js7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

//build and issue query
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY
l_name";
$result = @mysql_query($sql, $connection) or die(mysql_error());

//check the number of results
$num = @mysql_num_rows($result);
if ($num < 1) {
    // if there are no results, display message
    $display_block = "<p><em>Sorry! No results.</p>";
} else {
    // if results are found, loop through them
    // and make a form selection box
    while ($row = mysql_fetch_array($result)) {
        $id = $row['id'];
        $f_name = $row['f_name'];
        $l_name = $row['l_name'];
        $option_block = "<option value=\"$id\">$f_name $l_name</option>";
    }

    // create the entire form
    $display_block = "<FORM METHOD=\"POST\" ACTION=\"show_modcontact.php\">
<p>Contact:</p>
<select name=\"id\">
$option_block
</select>
<INPUT TYPE=\"SUBMIT\" name=\"submit\" value=\"Select this Contact\">
</form>";
}

echo "$display_block"; ?>
<HTML>
<HEAD>
<TITLE>My Contact Management System: Modify a Contact</TITLE>
</HEAD>
<BODY>
<h1>My Contact Management System</h1>
<h2><em>Modify a Contact - Select from List</em></h2>
<p>Select a Contact from the list, to modify the contact's record.</p>
<?php
echo "$display_block"; ?>
<br>
<p><a href="contact_menu.php">Return to Main Menu</a>a></p>
</BODY>
</HTML>
```

### 创建记录修改表单

记录修改表单基于上一章节创建的记录修改表单。区别在于表单字段中值的预填充。换句话说，如果记录中已经存在数据，你可以在更改之前看到现有内容。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
2. `<?php`
3. 开始一个 if...else 块，检查 `$_POST['id']` 值，这是从记录选择表单发送的唯一变量。如果值不存在，则将用户重定向回选择表单：
4. `if ($_POST['id']) {`
5. `header("Location:http://127.0.0.1/pick_contact.php");`
6. `exit;`
7. 如果必需字段有值，则启动会话；如果已存在，则继续会话。然后关闭该块：
8. `else {`
9. `session_start();`
10. if...else 块检查 `$_SESSION['valid']` 的值并根据结果执行特定操作。如果该值不是 "yes"，则用户未通过身份验证：
11. `if ($_SESSION['valid'] == "yes") {`
12. 将用户送回登录表单并退出脚本：
13. `header("Location:http://127.0.0.1/contact_menu.php");`
14. `exit();`
15. `}`
16. 创建一个变量存储表所在的数据库：
17. `$db_name = "testDB";`
18. 创建一个变量存储你用此脚本填充的表名：
19. `$table_name = "my_contacts";`
20. 按照你学的方法添加连接信息：
21. `$connection = mysqli_connect("localhost", "spike", "9js7En4")`
22. `or die(mysqli_error());`
23. 按照你学的方法选择数据库：
24. `$db = mysqli_select_db($db_name, $connection) or`
25. `die(mysqli_error());`
26. 创建 SQL 语句。选择 ID 等于 `$_POST['id']` 值的记录的所有字段：
27. `$sql = "SELECT f_name, i_name, address1, address2, address3, country, prim_tel, sec_tel WHERE id = $_POST['id']";`
28. 按照你学的方法创建一个变量存储 `mysqli_query` 函数的执行：
29. `$result = mysqli_query($sql, $connection) or die(mysqli_error());`
30. 开始 while 循环，为结果中的每条记录创建一个数组：
31. `while ($row = mysqli_fetch_array($result)) {`
32. 获取记录的各个元素并给它们良好的命名：
33. `$f_name = $row['f_name'];`
34. `$i_name = $row['i_name'];`
35. `$address1 = $row['address1'];`
36. `$address2 = $row['address2'];`
37. `$address3 = $row['address3'];`
38. `$postcode = $row['postcode'];`
39. `$country = $row['country'];`
40. `$prim_tel = $row['prim_tel'];`
41. `$sec_tel = $row['sec_tel'];`
42. `$email = $row['email'];`
43. `$birthday = $row['birthday'];`

注意你有了所选记录的当前值，你将在脚本中使用它们填充表单字段。

49. 关闭 while 循环，然后关闭 PHP 块：
50. `}`
51. `?>`

52. 输入此 HTML 开始构建记录修改表单：
53. `<HTML>`
54. `<HEAD>`
55. `<TITLE>My Contact Management System: Modify a Contact</TITLE>`
56. `</HEAD>`
57. `<BODY>`
58. `<h1>My Contact Management System</h1>`
59. `<h2>Modify a Contact</h2>`

60. 开始你的表单。假设方法为 POST，action 是名为 `do_modcontact.php` 的脚本。
61. `<FORM METHOD="POST" ACTION="do_modcontact.php">`

62. 添加一个隐藏字段存储 `$_POST['id']` 的值，以便传递给脚本。
63. `<INPUT type="hidden" name="id" value="<?php echo $_POST['id']; ?>">`

64. 开始一个 HTML 表格辅助布局。开始新表格，添加两个列标题，然后关闭它：

65. `<table cellspacing="3">`
66. `<tr>`
67. `<th>NAME & ADDRESS INFORMATION</th>`
68. `<th>OTHER CONTACT/PERSONAL INFORMATION</th>`
69. `</tr>`

70. 创建行来存放记录中所有项的输入字段。在输入字段中使用 `value` 属性，并混合 HTML 和 PHP 输出实际值：

71. `<tr>`
72. `<td><?php echo $row['id']; ?></td>`
73. `<td><strong>First Name:</strong><br>`
74. `<input type="text" name="f_name" value="<?php echo $row['f_name']; ?>">`
75. `size maxlength="75"><br>`
76. `<strong>Last Name:</strong><br>`
77. `<input type="text" name="l_name" value="<?php echo $row['l_name']; ?>"> <br>`
78. `<strong>Address Line 1:</strong><br>`
79. `<input type="text" name="address1" value="<?php echo $row['address1']; ?>">`
80. `size maxlength="100"><br>`
81. `<strong>Address Line 2:</strong><br>`
82. `<input type="text" name="address2" value="<?php echo $row['address2']; ?>">`
83. `size maxlength="100"><br>`
84. `<strong>Address Line 3:</strong><br>`
85. `<input type="text" name="address3" value="<?php echo $row['address3']; ?>">`
86. `size maxlength="100"><br>`
87. `<strong>Zip/Postal Code:</strong><br>`
88. `</td></tr>`

```php
89. <INPUT TYPE="text" NAME="postcode" VALUE="<?php echo $postcode; ?>"
90. SIZE=35 MAXLENGTH=25></p>
91. <p><strong>Country:</strong><br>
92. <INPUT TYPE="text" NAME="country" VALUE="<?php echo $country; ?>"
93. SIZE=35 MAXLENGTH=100></p>
94. <br>
95. <br><br>
96. <p><strong>Primary Telephone:</strong><br>
97. <INPUT TYPE="text" NAME="prim_tel" VALUE="<?php echo $prim_tel; ?>"
98. SIZE=35 MAXLENGTH=35></p>
99. <p><strong>Secondary Telephone:</strong><br>
100. <INPUT TYPE="text" NAME="sec_tel" VALUE="<?php echo $sec_tel; ?>"
101. SIZE=35 MAXLENGTH=35></p>
102. <p><strong>E-mail Address:</strong><br>
103. <INPUT TYPE="text" NAME="email" VALUE="<?php echo $email; ?>"
104. SIZE=35 MAXLENGTH=100></p>
105. <p><strong>Birthday (YYYY-MM-DD):</strong><br>
106. <INPUT TYPE="text" NAME="birthday" VALUE="<?php echo $birthday; ?>"
107. SIZE=10 MAXLENGTH=10></p>
108. <br>
109. </p>
```

开启新行并创建一个跨两列的表格单元格。在其中添加一个提交按钮以及一个返回主菜单的链接。关闭单元格、表格行和表格：

```php
111. <td id="align:center" colspan=2"><br>
113. <INPUT TYPE="SUBMIT" NAME="submit" VALUE="Update Contact
114. Record"></p>
115. <br>
116. <a href="contact_menu.php">Return to Main Menu</a></p>
117. </td>
118. </tr>
119. </TABLE>
120. </FORM>
```

关闭你的表单并添加更多 HTML 以使文档有效：

将文件保存为 `name_modcontact.php` 并将此文件放置在 Web 服务器的文档根目录下。

你的代码看起来应该是所示：

```php
<?php
// check for required form variables
if ($_POST['id']) {
    header("Location: http://127.0.0.1/pick_modcontact.php");
    exit;
} else {
    // if form variables are present, start a session
    session_start();
}

// check for validity of user
if ($_SESSION['valid'] != "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}
}

// set table and database names
$db_name = "testDB";
$table_name = "my_contacts";

// connect to server and select database
$connection = @mysql_connect("localhost", "spike", "9js7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection)
or die(mysql_error());

//build and insert query
$sql = "SELECT f_name, l_name, address1, address2, address3,
postcode, country, prim_tel, sec_tel, email, birthday FROM
$table_name WHERE id = \"".$_POST['id']."\"";
$result = @mysql_query($sql,$connection) or die(mysql_error());

//get results for display
while($row = @mysql_fetch_array($result)) {
  $f_name = $row['f_name'];
  $l_name = $row['l_name'];
  $address1 = $row['address1'];
  $address2 = $row['address2'];
  $address3 = $row['address3'];
  $postcode = $row['postcode'];
  $country = $row['country'];
  $prim_tel = $row['prim_tel'];
  $sec_tel = $row['sec_tel'];
  $email = $row['email'];
  $birthday = $row['birthday'];
}
?>

<HTML>
<HEAD>
<TITLE>My Contact Management System: Modify a Contact</TITLE>
</HEAD>
<BODY>
<h1>My Contact Management System</h1>
<h2><em><?php echo "Modify a Contact"; ?></em></h2>
<FORM METHOD="POST" ACTION="do_modcontact.php">
<INPUT TYPE="hidden" name="id" value="<?php echo $_POST['id']; ?>">
<table cellspacing="3">
<tr>
<th>NAME &amp; ADDRESS INFORMATION</th>
<th>OTHER CONTACT/PERSONAL INFORMATION</th>
</tr>
<tr>
<td valign="top">
<P><strong>First:</strong><BR>
<INPUT TYPE="text" name="f_name" value="<?php echo $f_name; ?>"
SIZE=35 MAXLENGTH=75</P></P>
<P><strong>Last Name:</strong><BR>
<INPUT TYPE="text" name="l_name" value="<?php echo $l_name; ?>"
SIZE=35 MAXLENGTH=75</P></P>
<P><strong>Address Line 1:</strong><BR>
<INPUT TYPE="text" name="address1" value="<?php echo $address1; ?>"
SIZE=35 MAXLENGTH=100</p>
<p><strong>Address Line 2:</strong><br>
<input type="text" name="address2" value="<?php echo $address2; ?>"
SIZE=35 MAXLENGTH=100</p>
<p><strong>Address Line 3:</strong><br>
<input type="text" name="address3" value="<?php echo $address3; ?>"
SIZE=35 MAXLENGTH=100</p>
<p><strong>Zip/Postal Code:</strong><br>
<input type="text" name="postcode" value="<?php echo $postcode; ?>"
SIZE=35 MAXLENGTH=25</p>
<p><strong>Country:</strong><br>
<input type="text" name="country" value="<?php echo $country; ?>"
SIZE=35 MAXLENGTH=100</p>
<td valign="top">
<p><strong>Primary Phone Number:</strong><br>
<input type="text" name="prim_tel" value="<?php echo $prim_tel; ?>"
SIZE=35 MAXLENGTH=35</p>
<p><strong>Secondary Phone Number:</strong><br>
<input type="text" name="sec_tel" value="<?php echo $sec_tel; ?>"
SIZE=35 MAXLENGTH=35</p>
<p><strong>E-mail:</strong><br>
<input type="text" name="email" value="<?php echo $email; ?>"
SIZE=35 MAXLENGTH=100</p>
<p><strong>Birthday (YYYY-MM-DD):</strong><br>
<input type="text" name="birthday" value="<?php echo $birthday; ?>"
SIZE=10 MAXLENGTH=10</p>
</td>
</tr>
<tr>
<td align="center" colspan="2">
<input type="submit" name="submit" value="Update Contact Record"/>
<br>
<p><a href="contact_menu.php">Return to Main Menu</a>a</p>
</td>
</tr>
</table>
</FORM>
</BODY>
</HTML>
```

在下一节中，你将创建一个处理表单输入、创建 SQL 语句并更新数据库记录的脚本。

### 创建修改脚本

此脚本将更新 `my_contacts` 表中的记录，使用 `$_POST['id']` 的值作为主键（确实如此）。

1. 在文本编辑器中打开新文件并开始 PHP 块：
2. `<?php`
3. 开启一个 if...else 块检查 `$_POST['f_name']` 和 `$_POST['l_name']` 是否有值。如果没有，将用户返回选择表单并退出脚本：

```php
4. if ($_POST['f_name'] || $_POST['l_name']) {
5.     header("Location: http://127.0.0.1/pick_modcontact.php");
6.     exit;
7. }
```

注意：你可以根据需要设置任意数量的必填字段。

8. 如果必填字段有值，启动会话（如果已存在则继续使用）。然后关闭块：

```php
9. } else {
10.    session_start();
11. }
```

12. 开启一个 if...else 块检查 `$_SESSION['valid']` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过正确的认证通道：

```php
13. if ($_SESSION['valid'] == "yes") {}
```

14. 将用户返回登录表单并退出此脚本：

```php
15.     header("Location: http://127.0.0.1/contact_menu.php");
16.     exit;
17. }
```

19. 创建一个变量来存储结果表名：

```php
20. $db_name = "testDB";
```

21. 创建一个变量来存储你要用此脚本填充的表名：

```php
22. $table_name = "my_contacts";
```

23. 按照之前的方法添加连接信息：

```php
24. $connection = @mysql_connect("localhost", "spike", "9s7En4");
25. or die(mysql_error());
```

26. 选择你学过的数据库：

```php
27. $db = @mysql_select_db($db_name, $connection)
28. or die(mysql_error());
```

29. 创建 SQL 语句。该语句使用 UPDATE 设置特定字段值：

```php
30. $sql = "UPDATE $table_name SET
31. f_name = \$_POST['f_name'];
32. l_name = \$_POST['l_name'];
33. address1 = \$_POST['address1'];
34. address2 = \$_POST['address2'];
35. address3 = \$_POST['address3'];
36. postcode = \$_POST['postcode'];
37. country = \$_POST['country'];
38. prim_tel = \$_POST['prim_tel'];
39. sec_tel = \$_POST['sec_tel'];
40. email = \$_POST['email'];
41. birthday = \$_POST['birthday']
42. WHERE id = \"".$_POST['id']."\"";
```

```html
100. </BODY>
101. </HTML>
```

102. 将文件保存为 `do_modcontact.php` 并将此文件放置在 Web 服务器的根目录下。

你的代码看起来应该像这样：

```php
<?php
// 检查所需的表单变量
if ($_POST[name] || $_POST[i_name]) {
    header("Location: http://127.0.0.1/pick_modcontact.php");
    exit;
} else {
    // 如果存在表单变量，则启动会话
    session_start();
}

// 检查用户有效性
if ($_SESSION[valid] != "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}

// 设置表和数据库名称
$db_name = "testDB";
$table_name = "my_contacts";

// 连接到服务器并选择数据库
$connection = @mysqli_connect("localhost", "spike", "9sj7En4");
if (mysqli_error())
    $db = @mysqli_select_db($connection, $db_name) or die(mysqli_error());

// 构建并执行查询
$sql = "UPDATE $table_name SET
f_name = $_POST[name];
l_name = $_POST[i_name];
address1 = $_POST[address1];
address2 = $_POST[address2];
address3 = $_POST[address3];
postcode = $_POST[postcode];
country = $_POST[country];
prim_tel = $_POST[prim_tel];
sec_tel = $_POST[sec_tel];
email = $_POST[email];
birthday = $_POST[birthday]
WHERE id = $_POST[id];";

$result = @mysqli_query($connection, $sql) or die(mysqli_error());
?>
<HTML>
<HEAD>
<TITLE>我的联系管理系统：联系人已更新</TITLE>
</HEAD>
<BODY>
<h1>我的联系管理系统</h1>
<<h2><em>修改联系人 - 联系人已更新</em></h2>

<P>以下信息已成功更新：<? echo

| 姓名和地址信息 | 其他联系/个人信息 |
| :--- | :--- |
| <P><strong>名字：</strong><br><?php echo "$POST[name];";</p> | <P><strong>主电话号码：</strong><br><?php echo "$POST[prim_tel];";</p> |
| <P><strong>姓氏：</strong><br><?php echo "$POST[lastname];";</p> | <P><strong>次电话号码（备用电话）：</strong><br><?php echo "$POST[sec_tel];";</p> |
| <P><strong>地址第 1 行：</strong><br><?php echo "$POST[address1];";</p> | <P><strong>邮箱：</strong><br><?php echo "$POST[email];";</p> |
| <P><strong>地址第 2 行：</strong><br><?php echo "$POST[address2];";</p> | <P><strong>生日（YYY-MM-DD）：</strong><br><?php echo "$POST[birthday];";</p> |
| <P><strong>地址第 3 行：</strong><br><?php echo "$POST[address3];";</p> | |
| <P><strong>邮政编码：</strong><br><?php echo "$POST[postcode];";</p> | |
| <P><strong>国家：</strong><br><?php echo "$POST[country];";</p> | |
| <td align="center" colspan="2"><p><a href="contact_menu.php">返回主菜单</a></p></td> | |

<body>
</body>
</html>
```

继续下一步——修改你数据表中的某些联系人。

### 修改联系人操作步骤

要开始在 `my_contacts_menu.php` 中修改联系人，请打开 `http://127.0.0.1/contact_menu.php`。如果你已经登录，将看到你的管理菜单。否则，请登录用户名 (admin) 和密码 (abc123)。

- 选择“修改联系人”(Modify Contact)项目。
- 从列表中选择一个联系人并点击“选择联系人”(Select Contact)按钮。
- 修改记录中的某些内容。在我的示例中，我将地址 2 改为“Suite 92-A”，并将主电话改为“555-444”。
- 返回选择表单并再次选择你的联系人，以查看值是否已更改。
- 修改某些联系人的记录。在下一章中，你将创建用于删除某些记录的管理脚本。

## 第 2 章：删除联系人

### 概述

有很多时候，我出于各种原因想从地址簿中删除人员。在本章中，你将学习如何执行以下操作：

- 创建用于删除记录的管理界面
- 创建一个从数据表中删除记录的脚本
- 在查看或删除脚本之前，要求基于会话的身份验证

### 使用选择表单

创建删除选择表单的脚本与用于选择记录进行修改的脚本几乎相同。这部分你将很容易快速浏览。重复让它们变得完美！

- 在你的文本编辑器中打开新文件并开始 PHP 块。
- 启动会话，或如果已存在则继续会话：`session_start();`
- 启动一个 if...else 块，检查 `$_SESSION[valid]` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过身份验证：

```php
if ($_SESSION[valid] != "yes") {
    // 将用户发送到登录表单并退出此脚本
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}
```

- 创建一个变量来存储数据表所在的数据库名称：
`$db_name = "TestDB";`
- 创建一个变量来存储你用此脚本填充的表名称：
`$table_name = "my_contacts";`
- 按照你添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9s7En4");
if($mysql_error()) {
```

- 像你学的那样选择数据库：

```php
$db = @mysql_select_db($db_name, $connection)
die(mysql_error());
}
```

- 像你学的那样构建并执行查询：

```php
$sql = "UPDATE $table_name SET
f_name = $_POST[name];
l_name = $_POST[i_name];
address1 = $_POST[address1];
address2 = $_POST[address2];
address3 = $_POST[address3];
postcode = $_POST[postcode];
country = $_POST[country];
prim_tel = $_POST[prim_tel];
sec_tel = $_POST[sec_tel];
email = $_POST[email];
birthday = $_POST[birthday]
WHERE id = $_POST[id];";
```

- 执行查询并在出错时退出：

```php
$result = @mysqli_query($connection, $sql) or die(mysqli_error());
```

- 使用 `num_rows()` 函数检查结果：

```php
$num = @mysql_num_rows($result);
```

- 如果数量小于 1（即没有返回记录）：

```php
if ($num == 0) {
    $display_block = "<p>未找到结果。</p>";
}
```

- 否则，如果数量大于 1：
- 启动 while 循环。为结果中的每条记录创建一个数组：

```php
while ($row = @mysql_fetch_array($result)) {
    $id = $row['id'];
    $f_name = $row['f_name'];
    $i_name = $row['i_name'];
    // 创建变量 $option_block 包含下拉菜单的元素
    $option_block .= "<option value=\"$id\">$f_name</option>";
}
```

- 关闭 while 循环创建一个变量 `$display_block` 来存储表单。虽然该变量在步骤 12 中曾用于存储错误信息，但除非出错，否则此处不会。对于表单，假设方法为 POST，目标为 `show_delcontact.php`：

```php
$display_block = '<form method="POST" action="show_delcontact.php">
<p><strong>联系人：</strong></p>
<select name="id">' . $option_block . '</select>';
```

- 添加提交按钮：

```html
<input type="SUBMIT" name="submit" value="Delete">
</form>
```

- 完成下拉菜单，即 `<select>` 标签对。它应该包含至少 `<option>` 元素。
- 添加更多 HTML 使得文档有效：

```html
<html>
<head>
<title>我的联系管理系统：删除联系人</title>
</head>
<body>
<h2>我的联系管理系统</h2>
<h2>删除联系人 - 从列表中选择</h2>
<p>从下方列表中选择一个联系人，以删除该联系人的记录。</p>
</body>
</html>
```

- 显示 `$display_block` 的内容：

```php
php echo $display_block; ?>
```

- 添加返回主菜单的链接：

```html
<p><a href="contact_menu.php">返回主菜单</a></p>
```

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());

// 结果数量
$num = @mysql_num_rows($result);
if ($num == 1) {
    // 如果没有结果，显示消息
    $display_block = "<p>对不起！没有结果。</p>";
} else {
    // 如果找到了结果，遍历它们
    // 并创建一个表单选择块
    while ($row = mysql_fetch_array($result)) {
        $id = $row['id'];
        $f_name = $row['f_name'];
        $s_name = $row['s_name'];
        $option_block .= "<option value=\"$id\">$f_name, $s_name</option>";
    }

    // 创建整个表单块
    $display_block = "<FORM METHOD=\"POST\" ACTION=\"show_del_contact.php\">
    <P>联系:</strong></p>
    <select name=\"id\">
    $option_block
    </select>
    <INPUT TYPE=\"SUBMIT\" NAME=\"submit\" VALUE=\"选择此联系人\"></P>
    </form>";
} ?>
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：删除联系人</TITLE>
</HEAD>
<body>
<h1>我的联系人管理系统</h1>
<h2><em>删除联系人 - 从列表中选择</em></h2>
<p>从下方列表中选择一个联系人，以删除该联系人的记录。</p>
<?php echo "$display_block"; ?>
<br>
<p><a href="contact_menu.php">返回主菜单</a></p>
</body>
</html>
```

在[下一节](#next)节中，你将创建一个删除前的确认屏幕，显示所选记录的所有当前值。

### 创建记录删除确认表单

记录删除表单并非通常意义上的——你不需要在表单字段中输入任何内容。此屏幕将以只读格式显示现有记录，并包含隐藏表单字段和一个提交按钮。通过在删除之前查看记录，你可以确保删除的是正确的记录。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：
2. `<?php`
3. 开始一个 if...else 块，检查 `$_POST[id]` 的值，这是从记录选择表单发送的变量。如果值存在，则将用户重定向选择表单并退出脚本：

```php
4. if ($_POST[id]) {
5.     header("Location: http://127.0.0.1/pick_delcontact.php");
6.     exit;
7. }
8. else {
9.     session_start();
10. }
```

11. 如果必需字段有值，启动会话，或如果当前已存在则继续会话。然后关闭块。
12. `} else`

```php
13. // 开始一个 if...else 块，检查 $_SESSION[valid] 的值并根据结果执行操作。如果值不是 yes，说明用户没有通过验证通道：
14. if ($_SESSION[valid] == "yes") {
15.     header("Location: http://127.0.0.1/contact_menu.php");
16.     exit;
17. }
```

18. 将用户送回登录表单并退出此脚本：

```php
19. header("Location: http://127.0.0.1/contact_menu.php");
20. exit;
21. }
```

22. 创建一个变量来存储表所在的数据库名称：

```php
23. $db_name = "testDB";
```

24. 创建一个变量来存储你用此脚本填充的表名：

```php
25. $table_name = "my_contacts";
```

26. 添加你已经写好的连接信息：

```php
27. $connection = mysqli_connect("localhost","spike","9sj7En4")
28. or die(mysqli_error());
```

29. 选择你学过的数据库：

```php
30. $db = @mysql_select_db($db_name, $connection) or
31. die(mysqli_error());
```

32. 创建 SQL 语句。你想选择数据库中的所有字段，但 ID 等于 `$_POST[id]` 值的记录除外：

```php
33. $sql = "SELECT f_name, l_name, address, address2, address3,
34. postcode, prim_tel, sec_tel, email FROM
35. $table_name WHERE id=$__POST[id]";
```

36. 创建一个变量来存储 `mysql_query()` 的结果，正如你学的那样：

```php
37. $result = @mysql_query($connection) or die(mysqli_error());
```

38. 开始 while 循环。循环将遍历结果集(`$result`) 中每个记录的每一行。

```php
39. while($row = @mysql_fetch_array($result)) {
```

40. 获取记录的各个元素并给它们命名：

```php
41. $f_name = $row['f_name'];
42. $l_name = $row['l_name'];
43. $address = $row['address'];
44. $address2 = $row['address2'];
45. $address3 = $row['address3'];
46. $postcode = $row['postcode'];
47. $country = $row['country'];
48. $prim_tel = $row['prim_tel'];
49. $sec_tel = $row['sec_tel'];
50. $email = $row['email'];
51. $birthday = $row['birthday'];
```

52. 在你的 PHP 代码中关闭循环：

```php
53. }
54. ?>
```

55. 输入此 HTML 来构建记录确认屏幕：

```html
56. <HTML>
57. <HEAD>
58. <TITLE>我的联系人管理系统：删除联系人</TITLE>
59. </HEAD>
60. <body>
61. <h1>我的联系人管理系统</h1>
62. <h2><em>删除联系人</em></h2>
```

63. 开始你的表单。方法为 POST，动作为名为 `del_contact.php` 的脚本：

```html
64. <FORM METHOD="POST" ACTION="del_contact.php">
```

65. 添加一个字段来存储 `$_POST[id]` 的值：

```html
<input type="text" name="id" value="<?php echo $_POST['id']; ?>">
```

66. 添加两个字段来存储 `$f_name` 和 `$l_name`。在删除发生后，你将在最终屏幕中使用这些字段：

```html
<input type="text" name="f_name" value="<?php echo $f_name ?>">
```

67. 接下来，你将在记录添加和修改表单中混合 HTML 和 PHP 来显示记录的值。启动新表格，添加两列，然后关闭该行：

```html
68. <table cellspacing="5">
69. <tr>
70. <th>姓名与地址</th>
71. <th>其他联系人/个人信息</th>
72. </tr>
```

73. 开始一个新的表格行和数据单元格，然后显示记录的文本标签和值：

```html
74. <tr>
75. <td><strong>名:</td><td><?php echo $f_name; ?></td>
76. <td><strong>姓:</td><td><?php echo $l_name; ?></td>
77. <td><strong>地址 1:</td><td><?php echo $address; ?></td>
78. <td><strong>地址 2:</td><td><?php echo $address2; ?></td>
79. <td><strong>地址 3:</td><td><?php echo $address3; ?></td>
80. <td><strong>邮政编码:</td><td><?php echo $postcode; ?></td>
81. <td><strong>国家:</td><td><?php echo $country; ?></td>
82. </tr>
83. <td><strong>主电话:</td><td><?php echo $prim_tel; ?></td>
84. <td><strong>备电话:</td><td><?php echo $sec_tel; ?></td>
85. <td><strong>电子邮件地址:</td><td><?php echo $email; ?></td>
86. <td><?php echo $email; ?></td>
87. <td><strong>生日 (YYYY-MM-DD):</strong></td><td><?php echo $birthday; ?></td>
88. </td></td>
```

89. 启动一个跨两列的新行和数据单元格。在内部添加一个提交按钮和一个返回主菜单的链接。关闭数据单元格、表格行和表格本身：

```html
90. <tr>
91. <td align="center" colspan="2">
92. <INPUT TYPE="SUBMIT" NAME="submit" VALUE="删除此联系人">
93. <a href="contact_menu.php">返回主菜单</a>
94. </td>
95. </tr>
96. </table>
```

97. 关闭表单并添加一些新的 HTML 以使文档有效：

```html
98. </FORM>
99. </body>
100. </HTML>
```

101. 将文件保存为 `show_delcontact.php` 并此文件放置在 Web 服务器的文档根目录下。

你的代码看起来应该是这样的：

```php
<?php
// 检查必需变量
if ($_POST[id]) {
    header("Location: http://127.0.0.1/pick_delcontact.php");
    exit;
} else {
    // 如果存在表单变量，启动会话
    session_start();
}
```

```php
<?php
// 检查用户有效性
if ($_SESSION[valid] == "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}
```

```php
<?php
// 设置表和数据库名
$db_name = "testDB";
$table_name = "my_contacts";
```

```php
$address = $row['address'];
$address2 = $row['address2'];
$address3 = $row['address3'];
$postcode = $row['postcode'];
$country = $row['country'];
$prim_tel = $row['prim_tel'];
$sec_tel = $row['sec_tel'];
$email = $row['email'];
$birthday = $row['birthday'];
?>
```

```html
<HTML>
<HEAD>
<TITLE>我的联系管理系统：删除联系人</TITLE>
</HEAD>
<body>
<h1>我的联系管理系统</h1>
<h2>删除联系人</h2>
```

```html
<FORM METHOD="POST" ACTION="do_delete.php">
<INPUT TYPE="hidden" name="id" value="<?php echo $f_id; ?>">
<INPUT TYPE="hidden" name="f_name" value="<?php echo $f_name; ?>">
<INPUT TYPE="hidden" name="i_name" value="<?php echo $i_name; ?>">
```

<table cellspacing="5">
<tr>
<th>姓名与地址信息</th>
</tr>
<tr>
<th>其他联系/个人信息</th>
</tr>
<tr>
<td valign="top">
<p><strong>名：</strong><BR>
<?php echo $i_name; ?>><BR>
<p><strong>姓：</strong><BR>
<?php echo $i_name; ?>><BR>
<p><strong>地址行 1：</strong><BR>
<?php echo $i_address; ?>><BR>
<p><strong>地址行 2：</strong><BR>
<?php echo $i_address2; ?>><BR>
<p><strong>地址行 3：</strong><BR>
<?php echo $i_address3; ?>><BR>
<p><strong>城市/邮政编码：</strong><BR>
<?php echo $i_postcode; ?>><BR>
<p><strong>国家：</strong><BR>
<?php echo $i_country; ?>></p>
</td>
<td valign="top">
<p><strong>主电话号码：</strong><BR>
<?php echo $i_prim_tel; ?>><BR>
<p><strong>次电话号码：</strong><BR>
<?php echo $i_sec_tel; ?>><BR>
<p><strong>电子邮箱地址：</strong><BR>
<?php echo $i_email; ?>><BR>
<p><strong>生日（YYYY-MM-DD）：</strong><BR>
<?php echo $i_birthday; ?>></p>
</td>
</tr>
</table>

```html
<td align=center colspan=2><br>
<P><INPUT TYPE="SUBMIT" NAME="submit" VALUE="删除此联系人"></P>
<p><a href="contact_menu.php">返回主菜单</a></p>
</TD>
</TABLE>
</FORM>
</body>
```

在下一节中，你将创建一个脚本，该脚本将获取 `$_POST[id]` 的值（当前存储在隐藏表单字段中），并从数据库表中删除相应的记录。

### 创建删除记录的脚本

此脚本将使用 `$_POST[id]` 的值作为主键，删除 `my_contacts` 表中的记录。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：
2. `<?php`
3. 开始一个 if...else 块来检查 `$_POST[id]` 是否有值。如果没有，则将用户重定向到选择表单并退出脚本：
4. `if ($_POST[id]) {`
5. `header("Location:http://127.0.0.1/pick_delcontact.php");`
6. `exit();`
7. 如果必需字段有值，则启动会话，如果当前已存在会话则继续该会话。关闭块：
8. `else {`
9. `session_start();`
10. `}`
11. 开始一个 if...else 块来检查 `$_SESSION[valid]` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过适当的验证通道：
12. `if ($_SESSION[valid] == "yes") {`
13. 将用户送回登录表单并退出脚本：
14. `header("Location:http://127.0.0.1/contact_menu.php");`
15. `exit();`
16. `}`
17. 创建一个变量来存储该表所在的数据库名称：
18. `$db_name = "test";`
19. 创建一个变量来存储你用此脚本填充的表名：
20. `$table_name = "my_contacts";`
21. 按照你之前的方法添加连接信息：
22. `$connection = @mysql_connect("localhost","spike","9sj7En4")`
23. `or die(mysql_error());`
24. 按照你学的那样选择数据库：
25. `$db = @mysql_select_db($db_name, $connection) or`
26. `die(mysql_error());`
27. 创建用于删除记录的 SQL 语句：
28. `$sql = "DELETE FROM $table_name WHERE id = $_POST[id]";`
29. 创建一个变量来存储 `mysql_query()` 函数的结果，正如你所学的那样：
30. `$result = @mysql_query($sql,$connection) or die(mysql_error());`
31. 关闭你的 PHP 块并添加此 HTML：
32. `<?php`
33. `<HTML>`
34. `<HEAD>`
35. `<TITLE>我的联系管理系统：联系人已删除</TITLE>`
36. `</HEAD>`
37. `<body>`
38. `<h1>我的联系管理系统</h1>`
39. `<h2>删除联系人 - 联系人已删除</h2>`
40. 添加一个确认语句。HTML 和 PHP 将包含 `$_POST[f_name]`、`$_POST[i_name]` 以及：
41. `<?php echo $_POST[f_name] . " " . $_POST[i_name]; ?> 已删除`
42. 按照你学过的办法添加返回主菜单的链接：
43. `<a href="contact_menu.php">返回主菜单</a>`
44. `</body>`
45. `</HTML>`

在下一节中，你将创建一个脚本，该脚本将获取 `$_POST[id]` 的值（当前存储在隐藏表单字段中），并从数据库表中删除相应的记录。

### 创建删除记录的脚本（重复部分）

此脚本将使用 `$_POST[id]` 的值作为主键，删除 `my_contacts` 表中的记录。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：
2. `<?php`
3. 开始一个 if...else 块来检查 `$_POST[id]` 是否有值。如果没有，则将用户重定向到选择表单并退出脚本：
4. `if ($_POST[id]) {`
5. `header("Location:http://127.0.0.1/pick_delcontact.php");`
6. `exit();`
7. 如果必需字段有值，则启动会话，如果当前已存在会话则继续该会话。关闭块：
8. `else {`
9. `session_start();`
10. `}`
11. 开始一个 if...else 块来检查 `$_SESSION[valid]` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过适当的验证通道：
12. `if ($_SESSION[valid] == "yes") {`
13. 将用户送回登录表单并退出脚本：
14. `header("Location:http://127.0.0.1/contact_menu.php");`
15. `exit();`
16. `}`
17. 创建一个变量来存储该表所在的数据库名称：
18. `$db_name = "test";`
19. 创建一个变量来存储你用此脚本填充的表名：
20. `$table_name = "my_contacts";`
21. 按照你之前的方法添加连接信息：
22. `$connection = @mysql_connect("localhost","spike","9sj7En4")`
23. `or die(mysql_error());`
24. 按照你学的那样选择数据库：
25. `$db = @mysql_select_db($db_name, $connection) or`
26. `die(mysql_error());`
27. 创建用于删除记录的 SQL 语句：
28. `$sql = "DELETE FROM $table_name WHERE id = $_POST[id]";`
29. 创建一个变量来存储 `mysql_query()` 函数的结果，正如你所学的那样：
30. `$result = @mysql_query($sql,$connection) or die(mysql_error());`
31. 关闭你的 PHP 块并添加此 HTML：
32. `<?php`
33. `<HTML>`
34. `<HEAD>`
35. `<TITLE>我的联系管理系统：联系人已删除</TITLE>`
36. `</HEAD>`
37. `<body>`
38. `<h1>我的联系管理系统</h1>`
39. `<h2>删除联系人 - 联系人已删除</h2>`
40. 添加一个确认语句。HTML 和 PHP 将包含 `$_POST[f_name]`、`$_POST[i_name]` 以及：
41. `<?php echo $_POST[f_name] . " " . $_POST[i_name]; ?> 已删除`
42. 按照你学过的办法添加返回主菜单的链接：
43. `<a href="contact_menu.php">返回主菜单</a>`
44. `</body>`
45. `</HTML>`

```php
3. //构建表单块
4. $form_block = ""
<h1>登录</h1>
<form method="POST" action=$_SERVER[PHP_SELF]">
$msg
<P><<strong>用户名：</strong>strong><br>
<input type="text" name="username" size=15></P>
<P><<strong>密码：</strong>strong><br>
<input type="password" name="password" size=15></P>
<input type="hidden" name="op1" value="ds">
<P><input type="submit" name="submit" value="login"/></P>
</FORM>
```

16. 如果出现如下所示 if...else 块：

```php
if ($show_form == "yes") {
$display_block = $form_block;
} elseif ($show_menu == "yes") {
$display_block = $menu_block;
}
```

22. 将以下行替换为第 2 步中剪切的内容：

```php
$display_block = $form_block;
```

现在 if...else 块应该看起来所示：

```php
if ($show_form == "yes") {
$form_block = <h1>登录</h1>
<form method="POST" action=$_SERVER[PHP_SELF]">
$msg
<P><<strong>用户名：</strong>strong><br>
<input type="text" name="username" size=15></P>
<P><<strong>密码：</strong>strong><br>
<input type="password" name="password" size=15 maxlength=25></P>
<input type="hidden" name="op1" value="ds">
<P><input type="submit" name="submit" value="login"/></P>
</FORM>
} elseif ($show_menu == "yes") {
$display_block = $menu_block;
}
```

25. 将变量名从 `$form_block` 修改为 `$display_block`。

26. if...else 块应该看起来所示：

```php
if ($show_form == "yes") {
//构建表单块
$display_block = ""
<h1>登录</h1>
<form method="POST" action=$_SERVER[PHP_SELF]">
$msg
<P><<strong>用户名：</strong>strong><br>
<input type="text" name="username" size=15
</P>
<P><<strong>密码：</strong>strong><br>
<input type="password" name="password" size=15
maxlength=25></P>
<input type="hidden" name="op1" value="ds">
<P><input type="submit" name="submit" value="login"/></P>
</FORM>;
} else if ($show_menu == "yes") {
$display_block = $menu_block;
}
```

46. 找到以下代码块，将其高亮并从文件中剪切出来（准备粘贴）：

```php
$menu_block = "
<h1>我的联系人管理系统</h1>
<p>管理</p>
<ul>
<li><a href=\"_add_contact.php\">添加联系人</a></li>>
<li><a href=\"_pick_mododcontact.php\">修改联系人</a></li>>
<li><a href=\"_pick_delcontact.php\">删除联系人</a></li>>
</ul>
<p>查看记录</p>
<ul>
<li><a href=\"_show_contactsbyname.php\">按名称排序显示联系人</a></li>>
</ul>
```

60. 包含内容的 if...else 代码块：

```php
} else if ($show_menu == "yes") {
$display_block = $menu_block;
```

65. 将以下行替换为第 7 步中剪切的内容：

```php
$display_block = $menu_block;
```

现在 if...else 块应该看起来所示：

```php
if ($show_menu == "yes") {
$display_block = "<h1>登录</h1>
<form method=\"POST\" action=$_SERVER[PHP_SELF]\">
$msg
<p><input type=\"text\" name=\"username\" size=15 maxlength=25></p>
<p><input type=\"password\" name=\"password\" size=15 maxlength=25></p>
<input type=\"hidden\" name=\"opt\" value=\"ds\">
<input type=\"submit\" name=\"submit\" value=\"login\"/></p>
</FORM>
} else if ($show_menu == "yes") {
$menu_block = "<h1>联系人管理系统</h1>
<p>管理</p>
<ul>
<li><a href=\"_add_contact.php\">添加联系人</a></li>>
<li><a href=\"_pick_mododcontact.php\">修改联系人</a></li>>
<li><a href=\"_pick_delcontact.php\">删除联系人</a></li>>
</ul>
<p>查看记录</p>
<ul>
<li><a href=\"_show_contactsbyname.php\">按名称排序显示联系人</a></li>>
</ul>
}
```

66. 将变量名从 `$menu_block` 修改为 `$display_block`；

67. 完整的 if...else 块应该看起来所示：

```php
if ($show_form == "yes") {
$display_block = <h1>登录</h1>
<form method="POST" action=$_SERVER[PHP_SELF]">
$msg
<p><<strong>用户名：</strong>strong><br>
<input type="text" name="username" size=15 maxlength=25></p>
<p><<strong>密码：</strong>strong><br>
<input type="password" name="password" size=15 maxlength=25></p>
<input type="hidden" name="opt" value="ds">
<input type="submit" name="submit" value="login"/></p>
</FORM>
} else if ($show_menu == "yes") {
$menu_block = "<h1>联系人管理系统</h1>
<p>管理</p>
<ul>
<li><a href=\"_add_contact.php\">添加联系人</a></li>>
<li><a href=\"_pick_mododcontact.php\">修改联系人</a></li>>
<li><a href=\"_pick_delcontact.php\">删除联系人</a></li>>
</ul>
<p>查看记录</p>
<ul>
<li><a href=\"_show_contactsbyname.php\">按名称排序显示联系人</a></li>>
</ul>
}
```

在继续操作之前保存你的更改。

这些修改没有以任何方式改变显示。它们只是为了接下来的修改对代码进行了更好的组织。

1. 找到这一行，因为剩下的更改都在它之后：
2. `else if ($show_menu == "yes") {`
3. 创建一个变量来存储数据库名称：
4. `$db_name = "test";`
5. 创建一个变量来存储你要填充的表名：
6. `$table_name = "my_contacts";`
7. 按照学习的方法添加连接信息：
8. `$connection = @mysql_connect("localhost", "spike", "9s74")`
9. `or die(mysql_error());`
10. 按照学习的方法选择数据库：
11. `$db = @mysql_select_db($db_name,$connection) or`
12. `die(mysql_error());`
13. 创建一个 SQL 语句来统计 id 字段：
14. `$sql = "SELECT count(id) FROM $table_name";`
15. 按照学习的方法创建一个变量来存储 `mysql_query()` 函数的结果：
16. `$result = @mysql_query($sql,$connection) or die(mysql_error());`
17. 创建一个变量来存储结果中的特定值：
18. `$count = @mysql_fetch($result,0,"count") or`
19. `die(mysql_error());`

注意：如果你处理的是单字段结果，`mysql_result()` 函数比获取整个行要简单。该函数需要有效查询的结果、行号（从0开始）和字段名。



22. 下一次修改主要是为了美观。将字符串 `$display_block` 替换为以下 HTML，为选项创建一个双列表格：

23. `$display_block = "

<h1>我的联系人管理系统</h1>

<table>

<td valign="top">

<p><strong>管理</strong></p>

<ul>

<li><a href="show_add_contact.php">添加联系人</a></li>

<li><a href="pick_contact.php">修改联系人</a></li>

<li><a href="pick_delete_contact.php">删除联系人</a></li>

</ul>

<p><strong>查看记录</strong></p>

<ul>

<li><a href="show_contactsbyname.php">按名称排序显示联系人</a></li>

</ul>

</td>

</tr>

</table>

```

在下一节中，你将在菜单上显示当前日期。

# 显示今天的日期

与上一节相比，显示当前日期所需的更改轻而易举！一旦你了解了所有选项，`date()` 函数是高度可定制的。

注意：你可以在附录 B“基础 PHP 语言参考”中找到 `date()` 函数选项的列表。

1. 在文本编辑器中打开 `contact_menu.php`。
2. 找到这一行，因为其余的更改都包含在这个代码块中：
3. `} if ($show_menu == "yes") {`
4. 在给 `$count` 变量赋值的行之后，添加此行用来创建一个名为 `$today` 的变量，其中包含一个格式化的日期字符串：
`$today = date("l, F j S, Y");`

日期格式选项在表 22.1 中进行了解释。

| 表格 22.1 日期格式化示例 |
| 格式选项 | 说明 |
|---|---|
| l | 星期全称（带字面逗号） |
| F | 月份全称 |
| j | 月份中的几（2位数） |
| S | 序数后缀 |
| Y | 年份（4位数） |

7. 在 `$display_block1` 字符串中找到这一行：
8. `<h1>My Contact Management System</h1>`
9. 在其之后添加以下内容以打印日期字符串：
`<p><em>Today is " . $today . "</em></p>`
10. 保存你的视图。

在下一节中，你将使用一些 SQL 来查找在本月生日的联系人数量，并在列表中打印他们的名字。这对于像我这样的人很有帮助，我不仅记不住母亲的生日，更不用说其他人的了！

# 显示本月的生日

你数据库中的字段之一是用于人的生日的字段。这不是强制要求的，但如果你花时间输入了某人的生日，很有可能你实际上想记住它。在接下来的节中，我们将打印在本月生日的联系人数量，以及他们的姓名、生日和指向联系详情的链接。太棒了！

1. 在文本编辑器中打开 `contact_menu.php`。
2. 找到此行以及该代码块中的其余更改：
3. `} else if ($show==="yes") {`
4. 现在找到给 `$today` 变量赋值的行，你将从此行之后开始输入：
`$today = date('l, F j, Y');`
5. 创建一个 SQL 语句，用于生成在本月生日的人数：
`$get_birthday_count = "SELECT count(id) FROM table_name WHERE MONTH(birthday)=NOW()";`

注意：`MONTH()` 和 `NOW()` 是 MySQL 函数，用于从日期字符串（在本例中为 `birthday` 字段的值）和当前日期中提取出月份。你可以在附录 D“基础 MySQL 参考”中学习更多关于 MySQL 函数的知识。

10. 创建一个变量来存储 `mysql_query()` 函数的结果，正如你学的那样：
11. `$birthday_count_res = @mysql_query($get_birthday_count, $connection)`
12. `or die(mysql_error());`
13. 创建一个变量来存储结果中的特定值：
14. `$birthday_count = mysql_result($birthday_count_res, 0, "count(id)");`

接下来，你将尽享 SQL 的乐趣。如果在本月生日的人数为一个或更多，你将创建一个包含该人姓名和指向其联系详情链接的字符串。

在 `contact_menu.php` 中找到给 `$birthday_count` 变量赋值的行，在其之后创建一个如果值为真则将执行的 `if` 语句。在这种情况下，它正在寻找 `$birthday_count` 的一个正值：

1. `if ($birthday_count > 0) {`
2. 你将在 `while` 块中创建一个项目列表。在 `while` 块之外开始项目列表：
3. `$str = "<ul>";`
4. 创建一个 SQL 语句，选择 ID、名、姓、生日月份和生日日期，并按生日对结果集进行排序：
`$get_contacts_bd = "SELECT id, f_name, l_name, MONTH(birthday) as birthday_month, DAYMONTH(birthday) as date FROM $table_name WHERE MONTH(birthday) ORDER BY birthday";`

注意：你可以在 SQL 语句中使用 `as [new name]` 为它们使用新名称。在上一个例子中，你正在提取生日的月份并将其命名为 `month`，你正在提取生日日期并将其命名为 `date`。

10. 创建一个变量来存储 `mysql_query()` 函数的结果，正如你学的那样：
11. `$contacts_bd = @mysql_query($get_contacts_bd, $connection)`
12. `or die(mysql_error());`
13. 开始 `while` 循环，它将为结果中的每个记录创建一个名为 `$contacts_bd` 的数组：
14. `while ($contacts_bd = @mysql_fetch_array($bd_res)) {`
15. 获取记录的各个元素，并给它们起好名字：
16. `$contact_id = $contacts_bd['id'];`
17. `$contact_fname = $contacts_bd['f_name'];`
18. `$contact_name = $contacts_bd['l_name'];`
19. `$contact_month = $contacts_bd['month'];`
20. `$contact_date = $contacts_bd['date'];`
21. 向 `$bd_string` 附加一个包含此人姓名和生日的列表项。创建一个指向 `contact.php` 的链接，将在下一节中创建：
23. `$bd_string = "<li><a href=\"contact.php?id=$contact_id\">" . $contact_fname . "</a> (" . $contact_month . "-" . $contact_date . ")";`
26. 关闭 `while` 循环，然后关闭列表，最后是 `if` 语句：
27. `$bd_string .= "</li>";`
29. `}`
30. 在 `$display_block` 中的“本月生日”项目下添加以下内容：
31. `$bd_string`
32. 保存文件。最终的 `contact_menu.php` 脚本应该如下：

```php

<?php

// 开始 session

session_start();

// 检查是否来自表单

if (isset($_POST['submit'])) {

    // 检查用户名和密码

    if ($_POST['username'] != "admin" || $_POST['password'] != "abc123") {

        // 处理登录失败

        $msg = "<p style=\"color:#FF0000\">Bad Login - Try Again</p>";

    } else {

        // 处理登录成功

        $valid = "yes";

        $_SESSION['valid'] = $valid;

        $show_menu = "yes";

    }

} else {

    // 确定显示什么

    if (isset($_SESSION['valid']) && $_SESSION['valid'] == "yes") {

        $show_menu = "yes";

    } else {

        $show_form = "yes";

    }

}

// 将赋值给 display_block 变量

if ($show_form == "yes") {

    // 构建表单

    $display_block = "<h1>Login</h1><form method=\"POST\" action=\"$_SERVER['PHP_SELF']\">" . $msg .

    "<p><strong>username:</strong><input type=\"text\" name=\"username\" size=\"15\" maxlength=\"25\"></p>

    <p><strong>password:</strong><input type=\"password\" name=\"password\" size=\"15\" maxlength=\"20\"></p>

    "<p><input type=\"submit\" name=\"submit\" value=\"login\"></p></form>";

} else if ($show_menu == "yes") {

    // 设置表和数据库名

    $db_name = "test";

    $table_name = "my_contacts";

    // 连接服务器并选择数据库

    $connection = @mysql_connect("localhost","root","abc123") or die(mysql_error());

    $db = @mysql_select_db($db_name,$connection) or die(mysql_error());

    // 构建并执行查询

    $sql = "SELECT count(id) FROM $table_name";

    $result = @mysql_query($sql,$connection) or die(mysql_error());

    $count = @mysql_result($result,0,"count(id)") or die(mysql_error());

    // 当前日期

    $today = date("F, j, Y");

    // 生日计数

    $get_birthday_count = "SELECT count(id) FROM table_name WHERE MONTH(birthday)=NOW()";

    $birthday_count = @mysql_query($get_birthday_count,$connection) or die(mysql_error());

    $birthday_count = mysql_result($birthday_count, 0,"count(id)");

    // 根据正结果创建列表

    if ($birthday_count > 0) {

        $bd_string = "<ul>";

        $get_contacts_bd = "SELECT id, f_name, l_name, (birthday) as name, DAYMONTH(birthday) as date FROM table_name WHERE MONTH(birthday) = NOW() ORDER BY birthday";

        $contacts_bd_res = @mysql_query($get_contacts_bd,$connection) or die(mysql_error());

        while ($contacts_bd = mysql_fetch_array($contacts_bd_res)) {

            $contact_id = $contacts_bd['id'];

            $contact_fname = $contacts_bd['f_name'];

            $contact_lname = $contacts_bd['l_name'];

            $contact_bd_month = $contacts_bd['month'];

            $contact_bd_date = $contacts_bd['date'];

            $bd_string .= "<<li><a href=\"show_contact.php?id=$contact_id\">" . $contact_fname . "</a> (" . $contact_bd_month . "-" . $contact_bd_date . ")</li>";

        }

        $bd_string .= "</ul>";

    }

    // 构建菜单块

    $display_block = "<h1>My Contact Management System</h1><p><em>Today is $today</em></p><table cellspacing=\"3\"><<tr><td valign=\"top\"><<strong>Administration</strong><ul><li><a href=\"show_addcontact.php\">Add a Contact</a></li><li><a href=\"pick_contact.php\">Modify a Contact</a></li><li><a href=\"del_contact.php\">Delete a Contact</a></li></ul><strong>View Records</strong><ul><li><a href=\"show_contactsby.php\">Show Contacts, Ordered by Name</a></li></ul></td><td valign=\"top\"><<strong>Miscellaneous</strong><ul><li>Contacts in system: $count</li></ul></td></tr></table></table>" . $bd_string;

}

?>

```

152. **杂项**
153. <ul>
154. <li>系统中的联系人：**$count**
155. <li>本月生日：**$birthday_count**
156. $bd_string
157. </ul>
158. </td>
159. <tr>
160. <table>*;
161. }
162. ?>
163. <HTML>
164. <HEAD>
165. <TITLE>我的联系人管理系统</TITLE>
166. </HEAD>
167. <body>
168. <? echo "display_block", ?>
169. </body>
170. </HTML>

在下一下一节中，你将创建一个联系人详情脚本，用于显示你已经放入 `my_contacts` 表中的所有信息。

## 从 my_contacts 表中选择数据

现在，所有复杂的脚本工作都已完成，是时候执行一些 SQL 查询操作来显示 `my_contacts` 表中的数据了。你将从列出联系人开始，并显示联系人的详情。

## 显示记录列表

此脚本的目标是显示数据库表中的联系人无序列表，并附带指向 `show_contact.php` 脚本的链接。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：
2. <?php
3. 启动会话，如果当前已存在会话则继续会话：
4. session_start();
5. 启动一个 if...else 块，检查 `$_SESSION['valid']` 的值并根据结果执行操作。如果用户没有通过身份验证通道：
6. if ($_SESSION['valid'] == "yes") {
7. 将用户带回登录表并退出此脚本：
8. header("Location: http://127.0.0.1/contact_menu.php");
9. exit;
10. }
11. 创建一个变量来存储表所在的数据库名称：

12. $db_name = "testDB";

13. 在 `while` 块中创建一个变量来存储此脚本正在填充的表名：

14. $table_name = "my_contacts";

15. 像你之前那样添加连接信息：

16. $connection = @mysql_connect("localhost", "spike", "9s7En4");
17. or die(mysql_error($connection));

18.

19. 如你学的那样选择数据库：

20. $db = @mysql_select_db($db_name, $connection)
21. die(mysql_error($db));
22. 创建 SQL 语句。你只想选择表中记录的 ID 数字、名和姓：

23. $sql = "SELECT id, f_name, l_name FROM table ORDER BY l_name";
24. 如你学的那样创建一个变量来存储 `mysql_query($function)` 的结果：
25. $result = @mysql_query($sql,$connection) or die(mysql_error($connection));
26. 创建一个 `while` 循环，稍后创建无序列表。在 `while` 循环外部开始无序列表：
27. $contact_list = "<ul>";

28. 启动 `while` 循环。该循环将为结果集 ($result) 中的每条记录创建一个数组 `$row`；
29. while ($row = @mysql_fetch_array($result)) {
30. 获取记录的各个元素，并给它们起好名字：
31. $id = $row['id'];
32. $f_name = $row['f_name'];
33. $l_name = $row['l_name'];

34. 向 $contact_list 添加一个列表项，其中包含一个指向 `show_contact.php` 脚本的联系人链接：
35. $contact_list .= "<li<a href='show_contact.php?id=$id'>$f_name,
36. $l_name</a>";
37. 关闭 `while` 循环、无序列表以及 PHP 块：
38. }
39. $contact_list .= "</ul>";
40. 添加此 HTML：
41. <html>
42. <HEAD>
43. <TITLE>我的联系人管理系统：按名称列出的联系人</TITLE>
44. </HEAD>
45. <BODY>
46. <h1>我的联系人管理系统</h1>
47. <p>从列表中选择一个联系人以查看该联系人的记录</p>
48. 显示 $contact_list 的内容：
49. <?php echo $contact_list; ?>
50. 添加一个返回主菜单的链接：
51. <p><a href="contact_menu.php">返回主菜单</a></p>
52. 添加更多 HTML 以使文档有效：
53. </body>
54. </html>
55. 以 `contacts_by.php` 的命名保存文件，并将此文件放在你服务器的文档根目录下。

你的代码看起来应该像这样：

```php

<?php

//启动会话

session_start();

//检查有效性

if ($_SESSION['valid'] != "yes") {

    header("Location:http://127.0.0.1/contact_menu.php");

    exit;

}

//设置表和数据库名

$db_name = "testDB";

$table_name = "my_contacts";

//连接数据库

$connection = @mysql_connect("localhost", "spike", "9s7En4");

if (!$connection) die(mysql_error());

$db = @mysql_select_db($db_name, $connection);

if (!$db) die(mysql_error());

//构建并查询列表

$sql = "SELECT id, f_name FROM $table_name ORDER BY f_name";

$result = mysql_query($sql, $connection);

//创建结果列列表

$contact_list = "<ul>";

while ($row = mysql_fetch_array($result)) {

    $id = $row['id'];

    $f_name = $row['f_name'];

    $contact_list .= "<li><a href='show_contact.php?id=$id'>$f_name</a></li>";

}

$contact_list .= "</ul>";

?>

<html>

<HEAD>

<TITLE>联系人管理系统：按名称列出的联系人</TITLE>

</HEAD>

<body>

<h1>联系人管理系统</h1>

<p>从下方列表选择一个联系人以查看记录。</p>

<?php echo $contact_list; ?>

<p><a href="contact_menu.php">返回主菜</a></p>

</body>

</html>

```

打开 `http://127.0.0.1/contact_menu.php`。如果你已经登录，将看到管理面板。否则，使用用户名 (admin) 和密码 (abc123) 登录。选择“按名称显示联系人”。在下一节中，你将创建联系人显示页面 `show_contact.php`。

## 显示只读记录

这是展示你联系人的真实时刻！

- 1. 在文本编辑器中打开一个新文件并启动 PHP 块：
2. <?php
3. 启动一个 if...else 块，检查链接字符串中的 `$_GET['id']` 值。如果值不存在，将用户带回菜单并退出：
4. if ($_GET['id']) {
5. header("Location: http://127.0.0.1/contact_menu.php");
6. exit;
7. 如果必需字段有值，启动会话（如果已存在则继续会话）：
8. } else {
9. session_start();
10. }
11. 启动一个 if...else 块，检查 `$_SESSION['valid']` 的值并根据结果执行操作。如果值不是 yes，说明用户未通过正确的身份验证：
12. if ($_SESSION['valid'] == "yes") {
13. 将用户带回登录表并退出此脚本：
14. header("Location: http://127.0.0.1/contact_menu.php");
15. exit;
16. }
17. 创建一个变量存储表所在的数据库名称：
18. $db_name = "test";
19. 创建一个变量存储此脚本正在填充的表名：
20. $table_name = "my_contacts";
21. 像你那样添加连接信息：
22. $connection = mysqli_connect("localhost", "spike", "9js7En4");
23. or die(mysqli_error());
24. 如你学的那样选择数据库：
25. $db = mysqli_select_db($db_name, $connection) or die(mysqli_error());
26. 对 `$_GET['id']` 的值进行某些验证。在使用错误的键进行 SQL 查询之前，你想确保数字确实存在于系统中：
27. $chk_id = "SELECT id FROM table WHERE id = '$_GET['id']";
28. 如你学的那样创建一个变量来存储 `mysqli_query()` 函数的结果：
29. $chk_id_res = mysqli_query($connection, $chk_id)
30. die(mysqli_error());
31. 创建一个变量统计结果内的行数：
32. $id_num = mysqli_num_rows($chk_id_res);
33. if ($id_num == 0) {
34. header("Location: http://127.0.0.1/contact_menu.php");
35. exit;
36. }
37. 启动一个 `while` 循环，稍后创建无序列表。在 `while` 循环外部开始无序列表：
38. $contact_list = "<<ul>";
39. 启动 `while` 循环。该循环将为结果集 ($result) 中的每条记录创建一个数组 `$row`；
40. while ($row = mysqli_fetch_array($result)) {
41. 获取记录的各个元素，并给它们起好名字：
42. $id = $row['id'];
43. $f_name = $row['f_name'];
44. $l_name = $row['l_name'];
45. $address1 = $row['address1'];
46. $address2 = $row['address2'];
47. $address3 = $row['address3'];
48. $postcode = $row['postcode'];
49. $country = $row['country'];
50. $prim_tel = $row['prim_tel'];
51. $sec_tel = $row['sec_tel'];
52. $birthday = $row['birthday'];
53. 向 $contact_list 添加一个列表项，其中包含一个指向 `show_contact.php` 脚本的联系人链接：
54. $contact_list .= "<li<a href='show_contact.php?id=$id'>$f_name,
55. $l_name</a>";
56. 关闭 `while` 循环、无序列表以及 PHP 块：
57. }
58. $contact_list .= "</ul>";
59. 添加此 HTML：
60. <html>
61. <HEAD>
62. <TITLE>我的联系人管理系统：按名称列出的联系人</TITLE>
63. </HEAD>
64. <body>
65. <h1>我的联系人管理系统</h1>
66. <p>从列表中选择一个联系人以查看该联系人的记录</p>
67. <?php echo $contact_list; ?>
68. <p><a href="contact_menu.php">返回主菜单</a></p>
69. </body>
70. </html>





92. <p><strong>生日：</strong> <?php echo "$birthday"; ?></p>
93. 添加一个返回主菜单的链接，然后添加一些额外的 HTML 以使文档有效：

94. <p href="contact_menu.php">返回主菜单</a></p>

95. <body>

96. <HTML>

97. 将文件保存为 `show_contact.php`，并将此文件放置于你 Web 服务器的文档根目录下。

你的代码看起来应该像这样：

```php

<?php

// 检查必需的查询字符串变量

if ($_GET['id']) {

    header("Location: http://127.0.0.1/contact_menu.php");

    exit;

} else {

    // 如果存在表单变量，启动会

    session_start();

}

// 检查用户有效性

if ($_SESSION['valid'] == "yes") {

    header("Location: http://127.0.0.1/contact_menu.php");

    exit;

}

// 设置表名和数据库名

$db_name = "testDB";

$table_name = "my_contacts";

// 连接服务器并选择数据库

$connection = @mysql_connect("localhost", "spike", "9sj7En4")

or die(mysql_error());

$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

// 构建并执行查询

$chk_id = "SELECT * FROM $table_name WHERE id = '$_GET['id]'";

$chk_id_res = @mysql_query($chk_id, $connection) or die(mysql_error());

$chk_id_num = mysql_num_rows($chk_id_res);

// 检查有效结果

if ($chk_id_num != 1) {

    // 如果无效，重定向到菜

    header("Location: http://127.0.0.1/contact_menu.php");

    exit;

} else {

    // 如果有效，获取信息

    $sql = "SELECT f_name, l_name, address2, address3, postcode, country, prim_tel, sec_tel, birthday FROM $table_name WHERE id = '$_GET['id]'";

    $result = @mysql_query($sql, $connection) or die(mysql_error());

}

// 获取结果用于显示

while ($row = mysql_fetch_array($result)) {

    $f_name = $row['f_name'];

    $l_name = $row['l_name'];

    $address1 = $row['address1'];

    $address2 = $row['address2'];

    $address3 = $row['address3'];

    $postcode = $row['postcode'];

    $country = $row['country'];

    $prim_tel = $row['prim_tel'];

    $sec_tel = $row['sec_tel'];

    $email = $row['email'];

    $birthday = $row['birthday'];

}

?>

```

```html

<HTML>

<HEAD>

<TITLE>我的联系人管理系统：只读联系人详情</TITLE>

</HEAD>

<body>

<h1>我的联系人管理系统</h1>

<h2><?php echo $f_name; ?> 的联系详情</h2>

<p>姓名与地址：<strong><?php echo $f_name; ?></strong><br>

<?php echo "$address1"; ?><br>

<?php echo "$address2"; ?><br>

<?php echo "$address3"; ?><br>

<?php echo "$postcode"; ?><br>

<?php echo "$country"; ?> ?></p>

<p>电话 1：<strong><?php echo $prim_tel; ?></strong><br>

<<strong>电话 2：<strong><?php echo $sec_tel; ?></strong><br>

<<strong>邮箱：<strong><?php echo $email; ?></strong> <a href="mailto:<?php echo $email; ?>">

```

![image]

如果你已经登录了管理菜单，请打开 http://127.0.0.1/contact_menu.php。否则，请使用用户名 (admin) 和密码 (123) 登录。选择“显示联系人”、“按名称排序”列表，然后从列表中选择其中一个联系人。

看起来不错！这是你数据库表中的一个已完成的联系人信息。当联系人信息完整且没有输入生日时，会发生以下情况。

看起来很丑！对 `show_contact.php` 进行一些修改，考虑到只有两个字段（姓和名）是必须的。

- 1. 打开 `show_contact.php`。
- 2. 滚动到“姓名与地址”部分：
- 3. 删除此部分：
- 4. <?php echo "$address1"; ?><br>
- 5. <?php echo "$address2"; ?><br>
- 6. <?php echo "$address3"; ?><br>
- 7. <?php echo "$country"; ?></p>
- 8. <?php echo "$tel"; ?> <<strong> <<?php echo "$prim_tel"; ?><br>
- 9. <<strong>-电话 2：</strong>> <<?php echo "$sec_tel"; ?><br>
- 10. <<strong>-邮箱：</strong>> <<?php echo "$email"; ?>
- 11. href="mailto:<?php echo $email"; ?>"></a></p>
- 12. <strong>生日：</strong> <?php echo "$birthday"; ?></p>
- 13. 输入以下语句系列，查找特定变量的值并在存在时打印：

```php

<?php

if ($address1 != "") {

    echo "$address1";

}

if ($address2 != "") {

    echo "$address2";

}

if ($address3 != "") {

    echo "$address3";

}

if ($postcode != "") {

    echo "$postcode";

}

if ($country != "") {

    echo "$country";

}

<p>

if ($prim_tel != "") {

    echo "<strong>电话 1：</strong>$prim_tel";

}

if ($sec_tel != "") {

    echo "<strong>电话 2：</strong>$sec_tel";

}

if ($email != "") {

    echo "<strong>邮箱：</strong><a href=\"mailto:$email\">$email</a>";

}

</p>

if ($birthday != "0000-00-00") {

    echo "<p><strong>生日：</strong>$birthday</p>";

}

?>

```

49. 保存此文件。

![image]

现在你已经有了——一个利用会话和用户验证的完整在线管理系统。有很多修改和额外检查区域，所以花些时间玩这些脚本。这些简单的概念将帮助你理解并构建更大的应用程序。

# VII 部分：额外脚本

列表

- 第 23 章：管理邮件列表
- 第 24 章：创建列表和报告

# 第 23 章：管理邮件列表

概述

最终，你的网站将会有用者，有一天你甚至想向他们发送邮件。你可以使用 PHP 和 MySQL 创建非常简单的订阅和发布机制。在本章中，你将学习如何执行：

- 创建订阅/取消脚本
- 创建一个发送邮件的前端
- 创建一个向数据库中所有接收者发送邮件的脚本

## 关于邮件列表软件的简述

有很多优秀的邮件列表应用程序。在本章中构建的系统类型仅适用于数百个邮箱地址。在本章描述的系统源于某天我不想下载和安装任何第三方软件。我只是制作了一些执行任务的文件。PHP 的漂亮之处在于：它是一种非常简单的语言，更容易编写脚本来下载或安装东西。然而，当你的邮件列表变得足够时，请迁移到更健壮的邮件列表应用程序，这对于你的邮件服务器以及作为管理员的你来说都更容易。

# 开发订阅机制

在开始向邮件列表发送邮件之前，你需要建立订阅数据库。一个简单的订阅/取消脚本将处理这一点！此脚本的作用是在下一节创建的 subscribers 数据库表中添加或删除记录。

# 创建 subscribers 表

我的 subscribers 表有三个字段，如表 23.1 所示。你可以根据需要任意字段。

| 表 23.1：订阅字段 |
| 字段名 | 描述 |
| :--- | :--- |
| id | 订阅者自增 ID 号的主键 |
| email_addr | 订阅者的邮箱地址 |
| date_added | 用户订阅日期 |

接下来，你将使用熟悉的表格脚本实际创建此表！

- 1. 打开 浏览器并输入 http://127.0.0.1/show-createtable.html
- 2. 在表名字段输入 `subscribers`。
- 3. 在字段数量字段输入 `3`。

![image]

- 4. 点击“进入第 2 步”按钮。你应该看到图中所示的表单。

![image]

有三行，对应于你想在 subscribers 表中创建三个字段。在这些步骤中填充字段：

- 1. 在第一行，输入 `id` 作为字段名，从字段类型下拉菜单选择 `int`，勾选“主键”并勾选“自增”。
- 2. 在第二行，输入 `email_addr` 作为字段名，从字段类型下拉菜单选择 `varchar`，并指定字段长度为 100。
- 3. 在第三行，输入 `date_added` 作为字段名并从字段类型下拉菜单选择 `date`。

![image]

- 4. 点击“创建表”按钮创建 subscribers 表。

![image]

在下一节中，你将创建订阅/取消表单机制。

类似于第 8 章“发送邮件”中的一体表单，订阅表单将用于订阅、取消和错误检查。

- 1. 在文本编辑器中打开新文件并启动 PHP 块：```php

<?php

// 创建一个存储表所在数据库名的变量：

$db_name = "testDB";

// 创建一个存储用此脚本填充的表名的变量：

$table_name = "subscribers";

// 创建一个存储 MySQL 日格式当前日期的变量：

$add_date = date("Y-m-d");

?>

```





接下来，你将检查一个尚未创建的变量。在创建实际的 HTML 表单，你会添加一个名为 `op` 的隐藏字段，其值为 `ds`。只有在表单提交后，`$_POST[op]` 才会存在。

```php

10. 开启一个 if...else 块，首先检查 $_POST[op] 的值是否为 ds：

11 if ($_POST[op] == "ds") {

12 如果 $_POST[op] 的值不是 ds，则说明用户还没有见过表单。如果用户没见过表单，你需要创建它。创建一个名为 text_block 的变量，它将保存整个表单。从表单开始编写，并假设方法为 POST 且 action 为 `$_SERVER[PHP_SELF]`：

13 $text_block = "

14 <form method="POST" action=\"$_SERVER[PHP_SELF]\

15. 添加隐藏字段：

16 <input type="hidden" name="op" value="ds">

17. 为用户的电子邮件创建一个输入字段并带上标签：

18 <p>Your E-Mail:</p>

19 <input type="text" name="email_addr" size=25 maxlength=100>

20. 创建一组单选按钮，使用户可以选择选项或取消订阅。默认应该是该单选按钮：

21 <p>Action:</p>

22 <input type="radio" name="action" value="sub" checked> subscribe

23 <input type="radio" name="action" value="unsub"> unsubscribe

24. 添加一个提交按钮，然后关闭表单并：

25 <input type="submit" name="submit" value="Submit Form!">

26 </form>";

```

27. 继续 if else 块，检查 `$_POST[op]` 的值是否为 ds 以及 `$_POST[action]` 的值是否为 sub。这意味着用户正在尝试订阅：

```php

28. else if ($_POST[op] == "ds" && $_POST[action] == "sub") {

```

29. 但如果有人点击了按钮但没有输入电子邮件地址怎么办？添加一个 if 语句检查 `$_POST[email_addr]` 中的值。如果没有找到值，则将用户重定向到原始页面：

```php

31 if ($_POST[email_addr] == "") {

32 header("Location:http://127.0.0.1/manage.php");

33 exit;

34 }

```

35. 你需要检用户是否已经订阅，因此按照你所学的那样打开数据库连接：

```php

36 $connection = mysqli_connect("localhost", "spike", "js7en4");

37 or die(mysqli_error());

```

38. 如你所学，选择数据库：

```php

39 $db = @mysqli_select_db($db_name, $connection) or die(mysqli_error());

```

40. 创建一个 SQL 语句，查找匹配用户电子邮件地址的记录：

```php

41 $sql = "select email_addr from table_name where email_addr = \

42 $_POST[email_addr]";

```

43. 如你所学的方法，创建一个变量来存储 `mysql_query()` 函数的结果：

```php

44 $result = @mysqli_query($check, $connection) or

45 die(mysqli_error());

```

46. 创建一个变量来统计结果中的行数：
47 $check_num = mysqli_num_rows($result);

48. 创建一个 if...else 块，对 `$check_num` 的值执行操作。如果 `$check_num` 小于 1，则订阅表中没有该用户的电子邮件地址，因此插入是安全的：

```php

49 if ($check_num < 1) {

```

50. 创建一个 SQL 语句来插入电子邮件地址和当前日期（为自动递增的 id 留空）：

```php

51 $sql = "insert into $table_name values(\$POST[email_addr], ",

```

```php

52 "$date_date");

```

53. 执行你所学的查询：

```php

54 $result = mysql_query($sql,$connection) or die(mysql_error());

```

```php

55 }

```

56. 创建一个消息字符串，让用户知道结果：

```php

57 $text_block = "<P>Thanks for signing up!</P>";

```

58. 通过创建一个用户已经订阅的消息字符串来完成 if...else 块。然后是内部的 if...else 块：

```php

59 } else {

```

```php

60 $text_block = "<P>You're already subscribed!</P>";

```

```php

61 }

```

62. 继续内部的 if...else 块，检查 `$POST[op]` 的值以及 `$_POST[action]` 的值是否为 unsub。这意味着用户正在尝试取消订阅：

```php

63 if ($POST[op] == "ds" && $POST[action] == "unsub") {

```

64. 再次添加检查 `$POST[email_addr]` 中值的验�。如果没有找到值，则将用户重定向到原始页面：

```php

65 if ($POST[email_addr] == "") {

```

```php

66 header("Location:http://127.0.0.1/manage.php");

```

```php

67 }

```

```php

68 }

```

69. 你需要检查用户是否订阅，所以按照你所学的那样打开数据库连接并选择数据库：

```php

70 $connection = mysql_connect("localhost", "spike", "js7en4");

```

```php

71 or die(mysql_error());

```

```php

72 $db = mysql_select_db($db_name,$connection) or

```

```php

73 die(mysql_error());

```

74. 创建一个匹配用户电子邮件的 SQL 语句。如果找到匹配项，选择你用于取消订阅的字段：

```php

75 $check = "select id, email_addr from $table_name where email_addr

76 = \$POST[email_addr]";

```

77. 执行查询：

```php

78 $check_result = mysql_query($check,$connection) or

```

```php

79 die(mysql_error());

```

80. 创建一个变量统计结果中的行数：

```php

81 $check_num = mysql_rows(check_result);

```

```php

82 }

```

83. 创建一个内部 if...else 块，对 `$check_num` 的值执行操作。如果 `$check_num` 小于 1，则订阅表中没有该用户的电子邮件地址，你可以取消其订阅：

```php

84 if ($check_num < 1) {

```

85. 创建一个消息字符串让用户知道结果：

```php

86 $text_block = "<P>Couldn't find your e-mail in the list!</P>";

```

```php

87 <P>Haven't subscribed, because the e-mail you entered

88 is not in the database. </P>";

```

89. 继续内部 if...else 块：

```php

90 } else {

```

91. 创建一个变量获取结果集中特定的 `id` 值：

```php

92 $id = mysql_result($check_result, "id");

```

93. 创建一个 SQL 语句从订阅表中删除用户的电子邮件地址：

```php

94 $sql = "delete from $table_name where id = \"$id\";

```

95. 执行查询：

```php

96 $result = @mysql_query($sql,$connection) or die(mysql_error());

```

97. 创建一个消息字符串让用户知道结果：

```php

98 $text_block = "<p>You're subscribed!</p>";

```

99. 包含内部 if...else 块、外部 if... 以及 PHP 块：

```php

100 { }

101 ?>

```

102. 添加以下 HTML：

```html

103 <HTML>

104 <HEAD>

105 <TITLE>Subscribe/Unsubscribe</TITLE>

106 <HEAD>

107 <body>

108 <h1>Subscribe/Unsubscribe</h1>

```

109. 显示 `$text_block` 的内容：

```php

110 <?php echo "$text_block"; ?>

```

111. 添加更多 HTML 使文档符合规范：

```html

112 </body>

113 </HTML>

```

114. 将该文件保存为 `manage.php` 并将其放置在 Web 服务器的文档根目录下。

你的整个代码应该像这样：

```php

// 设置表和数据库名称

$db_name = "testDB";

$table_name = "subscribers";

// 当前日期

$add_date = date("Y-m-d");

// 确定他们是否需要查看表单

if ($_POST["action"] != "ds") {

// 创建表单

$text_block = "

<form method="POST" action=\"$_SERVER['PHP_SELF']">

<input type="hidden" name="action" value="ds">

<p>Your E-Mail Address:</p><br>

<input type="text" name="email_addr" size="25" maxlength="100"></p>

<p><input type="radio" name="action" value="sub" checked subscribe

<input type="radio" name="action" value="unsub"> unsubscribe</p>

<p><input type="submit" name="submit" value="Submit Form"></p>

</form>

} else if ($_POST["action"] == "ds" && ($_POST["action"] == "sub") {

// 尝试订阅；验证电子邮件

if ($_POST["email_addr"] == "") {

    header("Location: http://127.0.0.1/manage.php");

    exit;

}

}

// 连接到服务器并选择数据库

$connection = @mysql_connect("localhost", "spike", "9sj7En4")

or die(mysql_error());

$db = @mysql_select_db($db_name,$connection) or

die(mysql_error());

// 检查电子邮件是否在列表中

$check = "select id, email_addr from $table_name where

email_addr = \"$_POST[email_addr]\"";

$check_result = @mysql_query($check,$connection) or

die(mysql_error());

// 获取结果数并执行操作

$check_num = mysql_rows($check_result);

if ($check_num < 1) {

    // 添加记录

    $sql = "insert into $table_name values(\$_POST[email_addr],\"\$$add_date\")";

    $result = @mysql_query($sql,$connection) or

die(mysql_error());

    $text_block = "<p>Thanks for signing up!</p>";

} else {

    // 打印失败消息

    $text_block = "<p>You're already subscribed!</p>";

}

?>

```



```php

$text_block = "<p>You're unsubscribed!</p>";

}

?>

<HTML>

<HEAD>

<TITLE>Subscribe/Unsubscribe</TITLE>

</HEAD>

<BODY>

<h1>Subscribe/Unsubscribe</h1>

<?php echo \$text_block; ?>

</BODY>

</HTML>

```

在下一节中，你将对示例用户进行订阅和取消订阅，并查看地址验证功能是如何工作的。

# 测试订阅表单

- 1. 打开你的 Web 浏览器并输入 http://127.0.0.1/manage.php

![](img/bc248f3d24697d1afbacee37b9c4d229_244_0.png)

- 2. 在“您的电子邮件地址”（Your E-Mail Address）字段中输入你的电子邮件地址，选择订阅单单选按钮，然后提交表单。

![](img/bc248f3d24697d1afbacee37b9c4d229_244_1.png)

- 3. 使用 Web 浏览器的“后退”按钮返回表单，并在“您的电子邮件地址”字段中输入相同的电子邮件地址。

- 4. 再次选择订阅单选按钮，然后提交表单。

![](img/bc248f3d24697d1afbacee37b9c4d229_245_0.png)

你将看到一条消息，显示你已经订阅。

- 5. 使用 Web 浏览器的“后退”按钮返回表单，并在“您的电子邮件地址”字段中输入相同的电子邮件地址。这次，选择取消订阅单选按钮并提交表单。

![](img/bc248f3d24697d1afbacee37b9c4d229_245_1.png)

你将看到已取消订阅的确认信息。

- 6. 使用 Web 浏览器的“后退”按钮返回表单，并尝试取消订阅同一个电子邮件地址。

![](img/bc248f3d24697d1afbacee37b9c4d229_245_2.png)

你将看到一个确认，显示你的电子邮件不在数据库中，因此你没有被取消订阅。

继续添加你自己的几个电子邮件地址，因为在下一节中你将创建一个表单和脚本来向人员列表发送新闻通讯，有一个真实的人员列表将会非常棒。

# 开发邮件发送机制

现在你已经建立了订阅/取消订阅机制，可以创建一个非常简单的表单来对接邮件发送脚本。该邮件机制将获取你的表单内容并将其发送到订阅表中的每一个地址。

# 创建新闻通讯表单

我说你会创建一个“简单”的表单，我并不是在开玩笑。我只是使用了一个文本字段用于新闻通讯的主题和一个文本区域用于邮件正文。你可以根据需要使用任意数量的字段，只要相应地修改表单和脚本即可。

- 1. 在编辑器中打开一个新文件并输入以下 HTML：
```html

<HTML>

<HEAD>

<TITLE>发送新闻通讯</TITLE>

<HEAD>

<h1>发送新闻通讯</h1>

```
开始编写你的表单。假设方法为 POST，action 是一个名为 `do_send_newsletter.php` 的脚本：
```html

<FORM METHOD="POST" ACTION="do_send_newsletter.php">

```
为新闻通讯主题创建一个带文本标签的输入字段：
```html

<p>给它一个主题：br>

<input type="text" name="subject" size=30></p>

```
为新闻通讯正文创建一个带文本标签的文本区域：
```html

<p>给它正文：br>

<textarea name="newsletter" cols=50 rows=10 wrap=virtual>

</textarea>

```
添加一个提交按钮：
```html

<input type="submit" name="submit" value="Send Newsletter"></p>

```
关闭你的表单并添加更多 HTML 以使文档有效：
```html

</FORM>

</BODY>

</HTML>

```
将文件保存为 `send_newsletter.html` 并将此文件放置在你 Web 服务器的根目录下。

打开你的 Web 浏览器并输入：http://127.0.0.1/send_newsletter.html

![](img/bc248f3d24697d1afbacee37b9c4d229_246_0.png)

在下一节中，你将创建后端脚本。该脚本需要两个变量：`$_POST[subject]` 和 `$_POST[newsletter]`。

# 创建发送新闻通讯的脚本

根据 `send_newsletter.html` 中的 action，你需要一个名为 `do_send_newsletter.php` 的脚本。该脚本的目标是接受 `$_POST[subject]` 和 `$_POST[newsletter]` 中的文本，然后以电子邮件的形式将其发送给订阅表中的每个人。

- 1. 在编辑器中打开一个新文件并开始 PHP 块：
```php

<?

```
- 2. 启动一个 `if...else` 块并检查是否为 `$_POST[subject]` 和 `$_POST[newsletter]` 输入了值。如果任何一个变量为空，则将用户导回表单。
```php

if ($_POST[subject] == "" || $_POST[newsletter] == "") {

    header("Location:http://127.0.0.1/send_newsletter.html");

    exit;

}

```
- 3. 继续 `else` 块：
```php

else {

```
- 4. 创建一个变量存储数据库：
```php

$db_name = "testDB";

```
- 5. 创建一个变量存储表：
```php

$table_name = "subscribers";

```
- 6. 连接服务器并选择数据库：
```php

$connection = @mysql_connect("localhost") or die(mysql_error());

$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

```
- 7. 创建查询 SQL 语句：
```php

$sql = "select email_addr from $table_name";

```
- 8. 执行查询：
```php

$result = @mysql_query($sql) or die(mysql_error());

```
- 9. 创建一个变量存储邮件头：
```php

$headers = "From: Mailing List <youdomain.com>\n";

```
- 10. 启动循环处理结果：
```php

while ($row = @mysql_fetch_array($result)) {

    $email_addr = $row['email_addr'];

```
- 11. 使用 `mail()` 函数处理特殊字符：
```php

    mail($email_addr, stripslashes($_POST[subject]), stripslashes($_POST[newsletter]), $headers);

```
- 12. 打印确认：
```php

    echo "newsletter sent to: $email_addr<br>";

```
- 13. 关闭循环、`if...else` 块和 PHP 块：
```php

}

}

?>

```




针对错误，你可以创建几个代码片段（snippets）在你的 MySQL 数据库中存储特定信息。在本章中你将学习如何实现以下操作：

- 使用 MySQL 创建简单的访问计数机制
- 在页面和报告中显示访问次数
- 跟踪表单提交情况
- 创建表单提交的摘要报告

# 关于 Apache 日志文件的说明

Apache 服务器会自动记录有关用户访问和错误的特定信息。这些日志文件位于 `logs` 目录中。一个名为 `access.log` 的文件处理访问记录，而 `error.log` 文件处理错误记录。

访问日志的默认显示格式如下（此取自我的访问日志）：

```

127.0.0.1 [22/Mar/2002:05:27:10] GET /show_creatable.html HTTP/1.1" 304

127.0.0.1 [22/Mar/2002:05:27:46] POST /do_showfielddef.php HTTP/1.1" 2402

127.0.0.1 [22/Mar/2002:05:28:49] POST /do_creatable.php HTTP/1.1" 200

127.0.0.1 [22/Mar/2002:05:43:33] GET /manage.php HTTP/1.1" 200 562

```

我知道，这看起来相当晦涩。你可以在你的 `httpd.conf` 文件中这样设置格式：

LogFormat "%h %l %u \%t \%s %b"

在这种情况下，该格式对应表 24.1 中列出的描述。

表 24.1：Apache 日志文件设置
| 符号 | 说明 |
|--- | --- |
| %h | 发起请请求的机器远程主机，或 IP 地址 |
| %l | 远程日志名称（通常为空） |
| %u | 用户请求的 URL 路径 |
| %t | 访问时间 |
| "%r" | 引号内的请求的第一行 |
| %s | 请求状态 |
| %b | 发送的字节数，不包括标头 |

注意：你也可以在 Apache 访问日志中记录用户代理（Web 浏览器）等元素。

虽然有很多日志分析包可以购买或下载，但对于简单任务来说，全位的 Apache 访问记录可能过度了。本章将向你展示一些跟踪特定访问和操作的方法，这比“所有访问、所有信息、任何时间”对你更有意义。

# 使用 MySQL 进行简单的访问计数

如果你想捕获网站特定部分（甚至只是主页）的访问信息，你可以创建一个简单的数据库表和相应的 PHP 代码片段来实现这一功能。

使用已经熟悉的建表过程，首先你将创建一个简单的数据库表来存放所有的访问记录。

# 创建数据库表

在示例中，你将记录四个元素：页面名称、页面描述、用户代理和访问日期。

1. 打开你的 Web 浏览器并输入 http://127.0.0.1/show_createtable.html。
2. 在 Table Name（表名）字段中，输入 `page_track`。
3. 在 Number of Fields（字段数量）字段中，输入 `4`。

![](img/bc248f3d24697d1afbacee37b9c4d229_251_0.png)

4. 点击 Go to Step 2（跳转到步骤2）按钮。你应该看到图中所示的表单。

有四行，对应你想在 `page_track` 表中创建的四个字段。在接下来的步骤中填充字段：

1. 在第一行，在 Field Name（字段名）中输入 `page_name`，从 Field Type（字段类型）下拉菜单中选择 `varchar`，并指定 Field Length（字段长度）为 50。
2. 在第二行，在 Field Name 中输入 `page_desc`，并在 Field Type 下拉菜单中选择 `text`。
3. 在第三行，在 Field Name 中输入 `user_agent`，并在 Field Type 下拉菜单中选择 `text`。
4. 在第四行，在 Field Name 中输入 `date_added`，并在 Field Type 下拉菜单中选择 `date`。

完成后的表单所示。

5. 点击 Create Table（创建表）按钮来创建 `page_track` 表。

在下一节中，你将创建一个将跟踪信息写入 `page_track` 表的代码片段。

# 创建代码片段

“Code snippet”（代码片段）是一个高度技术性的术语，意思是“一点代码”。我对“高度技术性”那部分是在开玩笑，但代码片段通常不算长脚本。相反，它服务于简单的目的。在这种情况下，你的代码片段将某些基本信息写入 `page_track` 表，然后使用一些简单的 HTML 完成显示。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
2. <?
3. 创建四个变量，对应 `page_track` 表中的四个字段，并给它们赋予一些值：
4. $page_name = "sample 1";
5. $page_desc = "This is a sample page of no use.";
6. $user_agent = getenv("HTTP_USER_AGENT");
7. $date_added = date("Y-m-d");
8. 为数据库连接创建一个变量：
9. $conn = mysql_connect("localhost", "username", "password");
10. 选择数据库：
11. mysql_select_db("database_name", $conn);
12. 创建插入查询：
13. $sql = "INSERT INTO page_track (page_name, page_desc, user_agent, date_added) VALUES ('$page_name', '$page_desc', '$user_agent', '$date_added')";
14. 执行插入查询：
15. mysql_query($sql, $conn);
16. 开始 HTML 输出：
17. echo "<html><head><title>Access Counter</title></head><body>";
18. echo "<h1>Access Count for $page_name</h1>";
19. echo "<p>Description: $page_desc</p>";
20. 获取计数：
21. $count_sql = "SELECT count(page_name) FROM page_track WHERE page_name = '$page_name'";
22. $result = mysql_query($count_sql, $conn);
23. $row = mysql_fetch_array($result);
24. echo "<p>Total accesses: " . $row['count(page_name)'] . "</p>";
25. echo "</body></html>";
26. 关闭连接：
27. mysql_close($conn);




- 7. $count_res = @mysql_query($count_sql,$connection) or die(mysql_error());
- 9. 创建一个变量来存储当前结果集上下文中特定的计数值：
- 10. $count = @mysql_result($count_res, 0, "count(page_name)");
- 11. 在你的 HTML 块中，使用简单的 HTML 和 PHP 打印 $count 的值：
- 12. <p>访问次数: <?php echo "$count"; ?></p>

你新的 sample_page1.php 脚本应该如下：

```php

<?php

$page_name = "sample page 1";

$page_desc = "This is a sample page of no use.";

$user_agent = getenv("HTTP_USER_AGENT");

$date_added = date("Y-m-d");

$db_name = "testDB";

$table_name = "page_track";

$connection = @mysql_connect("localhost","spike","9s7En4") or die(mysql_error());

$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

$sql = "insert into $table_name values ('$page_name', '$page_desc', '$user_agent', '$date_added')";

$result = @mysql_query($sql,$connection) or die(mysql_error());

$count_sql = "select count(page_name) from $table_name where page_name='$page_name'";

$count_res = @mysql_query($count_sql,$connection) or die(mysql_error());

$count = @mysql_result($count_res, 0, "count(page_name)");

?>

<HTML>

<HEAD>

<TITLE>Sample Page #1</TITLE>

</HEAD>

<BODY>

<h1>Useless Sample Page #1</h1>

<p>This sample page serves no real purpose!</p>

<p>Accesses: <?php echo "$count"; ?></p>

</BODY>

</HTML>

```

对 sample_page2.php 进行相同的修改，并确保你在页面上看到计数显示。

接下来，你将访问这些页面并输入 http://127.0.0.1/sample_page1.php

- 1. 打开你的网络浏览器并输入

# 1.

![](img/bc248f3d24697d1afbacee37b9c4d229_256_0.png)

你将看到 HTML 页面，其中有一个标题和一些文本，随后是你达到的访问次数。在这个示例中，我访问了该示例页面四次。

2. 打开你的网络浏览器并输入 http://127.0.0.1/sample_page2.php

# 2.

![](img/bc248f3d24697d1afbacee37b9c4d229_256_1.png)

你将看到 HTML 页面，其中有一个标题和一些文本，随后是你达到的访问次数。在这个示例中，我访问了该示例页面三次。

在下一节中，你将创建一个访问报告页面，你可以用它来检查 page_track 表中你正在跟踪的页面状态。

# 创建你的个人访问报告

你在 page_track 表中拥有所有这些数据，所以现在是时候创建一个简单的页面来为你汇总计数了。你不需要筛选 Apache 访问日志或安装额外的软件来为你显示统计数据。从创建一个对你跟踪的面的总访问次数（包含）的简单计数开始。

- 1. 在你的文本编辑器中打开新文件并开始一个 PHP 块：
- 2. <?php
- 3. 创建一个变量来存储表所处的数据库名称：
- 4. $db_name = "testDB";
- 5. 创建一个变量来存储你用此脚本填充的表名：
- 6. $table_name = "page_track";
- 7. 按你学过的添加连接信息：
- 8. $connection = @mysql_connect("localhost","spike","9s7En4") or die(mysql_error());
- 9. 按你学过的选择数据库：
- 10. $db = @mysql_select_db($db_name, $connection) or die(mysql_error());
- 11. 创建一个 SQL 语句来统计 page_track 表中所有的记录：
- 12. $count_sql = "select count(page_name) from $table_name";
- 13. 执行查询：
- 14. $count_res = @mysql_query($count_sql,$connection) or die(mysql_error());
- 15. 创建一个变量在当前结果集上下文中打印特定的计数，然后创建一个 PHP 块：
- 16. $all_count = @mysql_result($count_res, 0, "count(page_name)");
- 17. 添加此 HTML：
- 18. <HTML>
- 19. <HEAD>
- 20. <TITLE>Access Report</TITLE>
- 21. </HEAD>
- 22. <BODY>
- 23. <h1>Access Report</h1>
- 24. 混合 HTML 和 PHP 以打印表名以及表中的跟踪条数：
- 25. <p>Total Tracked in <?php echo $table_name; ?>: <?php echo $all_count; ?></p>
- 26. 添加一些 HTML 以使文档有效：
- 27. </BODY>
- 28. </HTML>
- 29. 将文件保存为 access_report.php 并将其放在你的 Web 服务器根目录下。

```php

<?php

// 设置表和数据库名称

$db_name = "testDB";

$table_name = "page_track";

// 连接服务器并选择数据库

$connection = @mysql_connect("localhost","spike","9s7En4") or die(mysql_error());

$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

// 查询并选择结果

$count_sql = "select count(page_name) from $table_name";

$count_res = @mysql_query($count_sql,$connection) or die(mysql_error());

$all_count = @mysql_result($count_res, 0, "count(page_name)");

?>

<HTML>

<HEAD>

<TITLE>Access Report</TITLE>

</HEAD>

<BODY>

<h1>Access Report</h1>

<p>Total Tracked in <?php echo $table_name; ?>: <?php echo $all_count; ?></p>

</BODY>

</HTML>



37. 接下来，测试它！打开你的网络浏览器并输入 http://127.0.0.1/access_report.php ![](img/bc248f3d24697d1afbacee37b9c4d229_258_0)

# 显示 User Agents

在本节中，你将为 access_report.php 添加一些内容，以显示访问你网页的不同浏览器。

- 1. 在你的文本编辑器中打开 access_report.php。
- 2. 在关闭 PHP 标签之前，创建一个 SQL 语句查找 page_track 表中 user_agent 字段的所有唯一记录，统计这些记录并降序返回结果：
- 3. `$user_agent = "select distinct user_agent, count(user_agent) as count from $table_name group by user_agent order by count desc";`
- 4. 执行查询：
- 5. `$user_agent_res = @mysql_query($user_agent,$connection) or die(mysql_error());`
- 6. 你将在块内创建一个列表。在 while 块之外开始列表：
- 7. `$user_agent_block = "<ul>";`
- 8. 开始循环，为结果集 ($user_agent_res) 中的每条记录创建一个数组 $row_ua：
- 9. `while ($row_ua = mysql_fetch_array($user_agent_res)) {`
- 10. 获取记录的各个元素，并给它们命名：
- 11. `$user_agent = $row_ua['user_agent'];`
- 12. `$user_count = $row_ua['count'];`
- 13. 通过创建一个列表项和一个额外的列表添加到 $user_agent_block。
- 14. 列表项将显示 user agent 的名称。然后，第二个列表项将显示特定 user agent 的访问次数。在添加 $user_agent_block 后，关闭循环：
- 15. `$user_agent_block .= "</li>";`
- 16. `$user_agent_block .= "<li>$user_agent";`
- 17. `$user_agent_block .= "<li><em>accesses per browser: $user_count</em></li>";`
- 18. `$user_agent_block .= "</li>";`
- 19. }
- 20. 关闭你在 $user_agent_block 中创建的列表：
- 21. `$user_agent_block .= "</ul>";`
- 22. 在 HTML 部分添加以下内容，然后保存文件：
- 23. `<p><strong>Web Browsers Used:</strong></p>`
- 24. `<?php echo "$user_agent_block"; ?>`

你的新代码看起来应该这样：

```php

<?php

// 设置表和数据库名称

$db_name = "testDB";

$table_name = "page_track";

// 连接服务器并选择数据库

$connection = @mysql_connect("localhost","spike","9s7En4") or die(mysql_error());

$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

// 查询并选择结果进行计数

$count_sql = "select count(page_name) FROM $table_name";

$count_res = @mysql_query($count_sql, $connection) or die(mysql_error());

$all_count = @mysql_result($count_res, 0, "count(page_name)");

// 查询并选择 user agents 结果

$user_agent_sql = "select distinct user_agent, count(user_agent) as count FROM $table_name group by user_agent order by count desc";

$user_agent_res = @mysql_query($user_agent_sql,$connection) or die(mysql_error());

// user agent 显示块

$user_agent_block = "<ul>";

// 遍历结果

while ($row_ua = @mysql_fetch_array($user_agent_res)) {

    $user_agent = $row_ua['user_agent'];

    $user_count = $row_ua['count'];

    $user_agent_block .= "<li>$user_agent";

    $user_agent_block .= "<li><em>accesses per browser: $user_count</em></li>";

}

// 结束 user agent 块

$user_agent_block .= "</ul>";

?>

<HTML>

<HEAD>

<TITLE>Access Report</TITLE>

</HEAD>

<body>

<h1>Access Report</h1>

<p><strong>Web Browsers Used:</strong></p>

<?php echo "$user_agent_block"; ?>

</HTML>

```



<p><strong>在 <?php echo "$table_name"; ?> 中跟踪的访问总数：</strong></strong> <?php echo $all_count; ?></p>

<p><?php echo<strong>使用的浏览器：</strong></p>; <?php echo $user_agent_block; ?></p>

```html

</BODY>

</html>

```

让我们看看哪些用户代理（user agents）访问了你的页面。打开 浏览器并输入 http://127.0.0.1/access_report.php。

![](img/bc248f3d24697d1afbacee37b9c4d229_260_0.png)

> 你将看到一个 HTML 页面，其中有一个标题和文本，随后是每个页面的访问次数。你还会看到用户代理列表以及每种类型的总访问次数。例如，我用两个不同的浏览器访问了同一个页面，共计 10 次。

在下一节中，你将对 access_report.php 脚本进行最后的修改，以显示每个页面的明细。

## 显示特定页面的明细

在本节中，你对 access_report.php 脚本进行一些细微，以提供 page_track 表中跟踪的特定页面明细。

- 1. 在你的文本编辑器中打开 access_report.php。
- 2. 在结束的 PHP 标签之前，创建一个 SQL 语句，用于查找 page_track 表中 page_name 字段中的所有唯一条目，统计这些条目，并按降序返回结果：
- 3. `$page_name_sql = "select distinct page_name, page_desc, count(page_name) as count from $table_name group by page_name order by desc";`
- 4. 执行查询：
- 5. `$page_name_res = @mysql_query($page_name_sql, $connection) or die(mysql_error());`
- 6. 你将在 while 块中创建一个符号列表。在 while 循环之外开始符号列表：
- 7. `$page_name_block = "<ul>";`
- 8. 开始 while 循环。该循环将为结果集 ($page_name_res) 中的每条记录创建一个数组 $row_pn：
- 9. `while ($row = mysqli_fetch_array($page_name_res)) {`
- 10.
- 11. 获取记录的各个元素，并为它们起好名字：
- 12. `$page_name = $row['page_name'];`
- 13. `$page_desc = $row['page_desc'];`
- 14. `$page_count = $row['count'];`
- 15. 通过创建一个符号项目和额外的符号列表，将其添加到 $page_name_block 中。符号项目将显示页面名称。然后，第二个符号列表将显示该页面的访问次数。在向 $page_name_block 添加后，关闭 while 循环：
- 16. `$page_name_block = "";`
- 17. `$page_name_block .= "<li>" . $page_name . " (" . $page_desc . ")</li>";`
- 18. `$page_name_block .= "<ul>";`
- 19. `$page_name_block .= "<li>accesses per page: " . $page_count . "</li>";`
- 20. `$page_name_block .= "</ul>";`
- 21. }
- 22. 关闭你在 $page_name_block 中创建的符号列表：
- 23. `$page_name_block = "</ul>";`
- 24. 在 HTML 部分，添加以下内容，然后保存文件：
- 25. `<p><strong>各个页面：</strong></p>`
- 26. `<?php echo "$page_name_block"; ?>`

你的新代码看起来像这样：

```php

// 设置数据库和名称

$db_name = "test";

$table_name = "page_track";

// 连接到数据库

$connection = @mysql_connect("localhost", "root", $db_name) or die(mysql_error());

// 查询并选择计数结果

$count_sql = "select count(page_name) from $table_name";

$count_res = @mysql_query($count_sql, $connection) or die(mysql_error());

$all_count = @mysql_result($count_res, 0, "page_name");

// 查询并选择用户代理结果

$user_agent_sql = "select distinct user_agent,count(user_agent) as count from $table_name group by user_agent order by count desc";

$user_agent_res = @mysql_query($user_agent_sql, $connection) or die(mysql_error());

// 开始用户代理块

$user_agent_block = "<ul>";

// 循环结果

while($row_ua = @mysql_fetch_array($user_agent_res)) {

    $user_agent = $row_ua['user_agent'];

    $user_agent_count = $row_ua['count'];

    $user_agent_block .= "<li>" . $user_agent . ":<ul><li>accesses per browser: " . $user_agent_count . "</li></ul>";

}

// 完成用户代理块

$user_agent_block = "</ul>";

// 查询并选择结果

$page_name_sql = "select distinct page_name, page_desc, count(page_name) as count from $table_name group by page_name order by desc";

$page_name_res = @mysql_query($page_name_sql, $connection) or die(mysql_error());

// 开始用户代理块

$page_name_block = "<ul>";

// 循环结果

while ($row = mysqli_fetch_array($page_name_res)) {

    $page_name = $row['page_name'];

    $page_desc = $row['page_desc'];

    $page_count = $row['count'];

    $page_name_block .= "<li>" . $page_name . " (" . $page_desc . ")</li>";

    $page_name_block .= "<ul>";

    $page_name_block .= "<li>accesses per page: " . $page_count . "</li>";

    $page_name_block .= "</ul>";

}

// 关闭符号列表

$page_name_block = "</ul>";

```


--with-apxs=/usr/local/apache_1.3.26/bin/apxs

此行告诉 PHP 包含对 MySQL 支持并将其编译为动态模块。还有许多许多配置选项可供选择，其中许多你可能永远用不到（我也不确定）。表 A.2 列出了这些选项，以防你需要对安装进行调整。请记住，由于 PHP 是 Apache 的动态模块，因此在修改 PHP 时不需要重新编译 Apache！

## 表 A.2: 配置选项

| 选项 | 描述 |
| --- | --- |
| --with-informix=[DIR] | 包含 Informix 支持。DIR 是 Informix 安装目录。 |
| --with-msql=[DIR] | 包含 mSQL 支持。DIR 是 mSQL 安装目录。 |
| --with-oci8=[DIR] | 包含 Oracle8 支持。默认 DIR 为 ORACLE_HOME。 |
| --with-oracle=[DIR] | 包含 Oracle7 支持。默认 DIR 为 ORACLE_HOME。 |
| --with-ibm-db2=[DIR] | 包含 IBM DB2 支持。DIR 是 DB2 安装目录。 |
| --with-odbc | 包含 ODBC 支持。DIR 是 ODBC 目录。 |
| --with-unixODBC=[DIR] | 包含 unixODBC 支持。DIR 是 unixODBC 安装目录。 |
| --with-pgsql=[DIR] | 包含 PostgreSQL 支持。DIR 是 PostgreSQL 安装目录。 |
| --with-sybase=[DIR] | 包含 Sybase-DB 支持。DIR 是 Sybase 家目录。 |
| --with-gd=[DIR] | 包含 GD 支持。DIR 是 GD 的安装目录。 |
| --with-openssl=[DIR] | 包含 OpenSSL 支持（需要 OpenSSL >= 0.9.5）。DIR 是 OpenSSL 安装目录。 |
| --with-zlib=[DIR] | 包含 zlib 支持（需要 zlib >= 1.0.9）。DIR 是 zlib 安装目录。 |
| --enable-bcrypt | 启用 bc 风格的匹配函数。 |
| --with-curl=[DIR] | 包含 CURL 支持。DIR 是 CURL 安装目录。 |
| --with-cybercash | 包含 CyberCash 支持。DIR 是 CyberCash MCK 安装目录。 |
| --enable-ftp | 启用 FTP 支持 |
| --with-java=[DIR] | 包含 Java 支持。DIR 是 JDK 的安装目录。 |
| --with-ldap=[DIR] | 包含 LDAP 支持。DIR 是 LDAP 安装目录。 |
| --with-mcal=[DIR] | 包含 MCAL 支持。DIR 是 MCAL 安装目录 |
| --with-mcrypt=[DIR] | 包含 mcrypt 支持。DIR 是 mcrypt 安装目录。 |
| --with-hash=[DIR] | 包含 mash 支持。DIR 是 mash 安装目录。 |
| --with-pfro=[DIR] | 包含 PayFlow 支持。DIR 是 PayFlow 安装目录。 |
| --disable-posix | 禁用 POSIX 类函数 |
| --enable-trans-sid | 启用透明会话 |
| --with-config-file-path=PATH | 设置查找 php.ini 的路径，默认为 /lib。 |
| --enable-safe-mode | 启用安全模式 |
| --enable-magic-quotes | 启用魔术引号 |

关于 PHP 的 Linux/UNIX 配置选项的更多信息，请参阅 PHP 手册的安装和配置部分。

## 附录 B：基础语言参考

本附录不如 PHP 手册（位于 http://www.php.net/）详尽，它包含了每个 PHP 函数的描述、用户提交的注释和代码示例。相反，本附录作为一个基础或“本质”参考——PHP 开发团队和所有贡献者已经在这些方面做了大量工作，无需重复造轮。然而，本附录仅涉及 PHP 的一小部分内容。在所有示例中，在询问 PHP 之前，处理像 "string" 或 "int" 这样的内容。

## PHP 开始和结束标签

将 PHP 代码与 HTML 结合时必须转义，PHP 引擎会将表 B.1 所示的标签视为 PHP 代码。

## 表 B.1：PHP 开始和结束标签

| 开启标签 | 结束标签 |
| --- | --- |
| <?php | ?> |
| <script language="php"> | </script> |

## 变量

你创建变量来表示数据。例如，以下变量持有一个值：

$sales_tax = 0.0875;

此变量包含一个 SQL 语句：

$sql = "SELECT * FROM MY_TABLE";

在确定新变量的值时，你可以引用其他变量：

$tax_total = $sales_tax;

以下是变量名的特征：

- 以美元符号 ($) 开头。
- 不能以数字字符开头。
- 可以包含下划线 (_)。
- 区分大小写。

以下是一些常见的变量类型：

- 浮点数 (floats)
- 整数 (integers)
- 字符串 (strings)

这些类型由 PHP 根据它们出现的上下文决定。

## 浮点数

以下每个变量都是浮点数或小数。浮点数也被“带有小数点的数字”。

$a = 1.552;
$b = 0.964;
$sales_tax = 0.0875;

## 整数

整数是正负整数、零或“不带小数点的数字”。以下变量都是整数：

```php

$a = 15;

$b = -521;

```

## 字符串

双引号内的一系列字符被视为字符串：

```php

$a = "I am a string";

$b = "<p>This book is cool</p>";

```

你也可以在字符串中引用其他变量，它们在脚本执行时会被替换。例如：

```php

$num = 57; // 整数

$my_string = "I read this book $num times!"; // 字符串

```

当你运行脚本时，$my_string 将变为 "I read this book 57 times!"

## 表单变量

取决于 HTML 表单的方法（GET 或 POST），变量将是 $_POST 或 $_GET 的。例如，输入字段的将是 $_POST：

<input type="text" name="first_name" size="20">

如果该表单的方法是 GET，则为 $_GET[first_name]。

## Cookie 变量

与表单变量一样，来自 Cookie 的变量保存在名为 $_COOKIE 的超全局数组中。如果你设置了一个名为 user 的 Cookie，值为 Joe Smith，如下：

```php

setcookie("user", "Joe Smith", time()+3600);

```

名为 user 的变量会被放入 $_COOKIE 中。然后通过 $_COOKIE[user] 获取该值。

# 环境变量

当 Web 浏览器发送请求时，它会随请发送一组额外的变量称为环境变量。它们对于显示动态内容或授权用户非常有用。

默认情况下，环境变量以 $VAR_NAME 的形式供 PHP 脚本使用。然而，为了确保你读取的是正确的值，可以使用 getenv() 函数为选择赋值。REMOTE_ADDR 获取请求机器的 IP 地址。例如：

```php

$remote_address = getenv("REMOTE_ADDR");

echo "Your IP address is $remote_address.";

```

HTTP_USER_AGENT 获取浏览器类型、浏览器版本、语言编码和平台。例如：

```php

$browser_type = getenv("HTTP_USER_AGENT");

echo "You are using $browser_type.";

```

有关 HTTP 环境变量列表及其描述，请访问
http://hohoo.ncsa.uiuc.edu/cgi/env.html。





| 运算符 | 示例 | 操作 |
|---|---|---|
| + | $b = a + 3; | 将值相加 |
| - | $b = a - 3; | 减去值 |
| * | $b = a * 3; | 将值相乘 |
| / | $b = a / 3; | 将值相除 |
| % | $b = a % 3; | 返回模或余数 |

## 赋值运算符

`=` 是基础赋值运算符：

$$a = 124; //  $a 的值为 124

其他赋值运算符见[表 B.3]。

| 运算符 | 示例 | 操作 |
|---|---|---|
| += | $a += 3; | 将变量的值更改为当前值加上右侧的值 |
| -= | $a -= 3; | 将变量的值更改为当前值减去右侧的值 |
| .= | $a .= "string"; | 将右侧的变量拼接（添加）到当前值之后 |

## 比较运算符

比较运算符用于比较两个值，这并不意外。比较将返回 true 或 false 的值。比较运算符见[表 B.4]。

| 运算符 | 定义 |
|---|---|
| == | 等于 |
| != | 不等于 |
| > | 大于 |
| < | 小于 |
| >= | 大于等于 |
| <= | 小于等于 |

## 增/减运算符

增/减运算符的作用正如其名所示：对变量进行加或减操作（见[表 B.5]）。

### 表 B.5：增/减运算符

| 运算符 | 用法 | 定义 |
|---|---|---|
| ++a | 前增 | 增加 1 并返回 $a |
| $a++ | 后增 | 返回 $a 然后将 a 增加 1 |
| --a | 前减 | 减少 1 并返回 $a |
| $a-- | 后减 | 返回 $a 然后将 a 减少 1 |

# 逻辑运算符

逻辑运算符允许你编写脚本来确定条件的状态，并且在 `if...else` 或 `while` 语句的语文中，根据哪些条件为为假来执行特定的代码（表 B.6）。

### 表 B.6：逻辑运算符

| | | 结果 |
|---|---|---|
| ! | !$a | 如果 $a 为假则为真 |
| && | $a && $b | 如果 $a 和 $b 都为真则为真 |
| || | $a || $b | 如果 $a 或 $b 其中之一为真则为真 |

## 控制结构

程序本质上是一系列语句。正如其正如结构控制这些语句的执行方式。控制结构通常围绕一系列条件构建，例如，“如果天空是蓝色的，就去外面玩。”控制结构利用大括号 {} 将语句组与程序的其余部分分开。以下是控制结构的示例；记住这些会让你的生活变得更容易。

### if...else if...else

`if...else if...else` 根据所测试表达式的值执行语句。在下面的示例中，所测试的表达式是：

```

if ($a == 10) {

  // 执行某些代码

}

```

在评估 $a 并发现其值为 10（即条件为真），将执行大括号内部的代码。如果发现 $a 是 10 的其他值（即条件为假），则代码将被忽略，程序将继续提供另一种系列语句。如果 $a 的值不为 10，向结构中添加一个 `else` 语句以便在条件为假时执行：

```

if ($a == 10) {

    echo "equals 10";

} else if ($b == 8) {

    echo "b equals 8";

} else {

    echo "a does not equal 10";

}

```

可以在结构中添加 `elseif`（或 `else if`）语句在进入最后的 `else` 之前评估另一种情况。例如，以下结构首先评估 $a 是否等于 10。如果该条件为假，则评估 `elseif` 语句。如果发现为真，则执行其大括号内的代码。你可以使用 `elseif` 语句或作为 `if...else` 或 `if...else...else` 语句的一部分。无论你选择哪种，都会发现这种结构是你程序中不可或缺的元素！

### while

与 `if...else if...else` 结构不同（每个表达式只评估一次并根据其真假值执行操作），该语句会持续执行直到表达式为假。换句话说，`while` 循环在表达式为真时会继续。例如，在下面的 `while` 循环中，只要 $a 小于等于 3，$a 的值就会打印在屏幕上并加 1：

```

$a = 0 // 设置起点

while ($a <= 3) {

    echo $a;

    $a++;

}

```

### for

像 `while` 循环一样，`for` 循环在每次循环开始时评估一组条件表达式。以下是 `for` 循环的语法：

```

for (expr1; expr2; expr3) {

    // 执行代码

}

```

在每个循环开始时，首先评估第一个表达式，然后评估第二个表达式。如果第二个表达式为真，则通过执行代码并评估第三个表达式来继续循环。

```

for ($a = 0; $a <= 3; $a++) {

    echo $a;

}

```

## 内置函数

所有以下函数都是 PHP 语言的一部分。根据你正在执行的操作，你可能更多函数，请访问 PHP 文档 http://www.php.net/manual/ 并熟悉它们。

## 数组函数

许多 PHP 函数可用于数组。这里只列出我发现绝对有用的基础知识函数。

### array()

`array()` 函数允许为数组手动赋值。其语法如下：

```php

$array = array("val1", "val2", "val3");

```

### array_push()

`array_push()` 函数允许向现有数组末尾添加一个或多个元素。其语法为：

```

array_push($array_name, "element 1", "element 2", ...);

```

### array_pop()

`array_pop()` 函数允许从数组末尾弹出元素。其语法为：

```

array_pop($array_name);

```

### array_unshift()

`array_unshift()` 函数允许向数组开头添加元素。其语法为：

```

array_unshift($array_name, "element 1", "element 2", ...);

```

### array_shift()

`array_shift()` 函数允许从数组开头弹出元素。其语法为：

```

array_shift($array_name);

```

### array_merge()

`array_merge()` 函数允许合并两个多个现有数组。其语法为：

```

array_merge($array1, $array2, ...);

```

### array_keys()

`array_keys()` 函数返回数组中所有的键名。其语法为：

```

array_keys($array_name);

```

### array_values()

`array_values()` 函数返回数组中所有的值。其语法为：

```

array_values($array_name);

```



```php

each($arrayname);

list($val1,$val2,$val3, ...);

```

例如，当通过 GET 方法提交 HTML 表单时，每个键/值都会在全局变量 `$_GET` 中配。如果你的输入字段命名为 `first_name` 和 `last_name`，且用户输入了 `Joe` 和 `Smith`，那么每个键值对分别为 `first_name/Joe` 和 `last_name/Smith`。在 `$_GET` 数组中，这些变量表示如下：

```php

$_GET["first_name"] // value is "Joe"

$_GET["last_name"] // value is "Smith"

```

你可以使用 `each()` 和 `list()` 函数以此方式遍历数组，打印数组中每个元素的键和值：

```php

while (list($key,$val)=each($_GET)) {

    echo "$key has a value of $val<br>";

}

```

## reset

reset() 函数将指针置回数组开头。其语法为
`reset($array_name);`

## shuffle

shuffle() 函数随机化给定数组的元素。其语法为
`shuffle($array_name);`

## sizeof()

sizeof() 函数统计数组中的元素个数。在下面的示例中，$a 被赋值为等于 $colors 数组中元素个数的值：
`$a = sizeof($colors);`

如果 $colors 包含值 `blue`、`black`、`red` 和 `green`，则 $a 被赋值为值 4。

## 用于 MySQL 的数据库连接函数

存在许多 PHP 函数用于连接和查询 MySQL 服务器。以下是一些基本函数及其语法。请参阅 PHP 手册 http://www.php.net/manual/ 以获取完整的 MySQL 函数列表——这些函数非常多！

## mysql_connect()

此函数打开一个到 MySQL 的连接。它需要服务器名、用户名和密码。

`$connection = mysql_connect("servername", "username", "password");`

## mysql_create_db()

此函数在 MySQL 服务器上创建一个数据库。它需要一个有效的已建立连接。

`mysql_create_db("myDB");`

## mysql_drop_db()

此函数在 MySQL 服务器上删除一个数据库。它需要一个有效的已建立连接。

`mysql_drop_db("myDB");`

## mysql_select_db()

此函数在 MySQL 服务器上选择一个数据库供后续查询使用。它需要一个有效的已建立连接。

`$db = mysql_select_db("myDB", $connection);`

## mysql_query()

此函数发布 SQL 语句。它需要一个到数据库的打开连接。

`$sql_result = mysql_query("SELECT * FROM SOMETABLE", $connection);`

## mysql_error()

当连接或查询出现问题时，此函数返回一个有意义的错误信息。它通常在 `die()` 函数中使用，如下所示：

`$sql_result = mysql_query("SELECT * FROM SOMETABLE", $connection) or die(mysql_error());`

## mysql_fetch_array()

此函数自动将 SQL 语句的结果行放入数组。

`$row = mysql_fetch_array($sql_result);`

## mysql_num_rows()

此函数返回结果集中的行数。

`$num = mysql_num_rows($sql_result);`

## 日期和时间函数

基础 PHP 日期和时间函数允许你轻松地格式化时间戳，用于数据库查询和日历函数，也可以简单地在订单表收据上打印日期。

## date()

date() 函数返回当前的服务器时间戳，根据一组参数进行格式化。其语法为

`date(format, [timestamp]);`

如果未提供 `timestamp` 参数，则假设为当前时间戳。表 B.7 显示了可用的格式。

表 B.7：date() 函数格式

| 字符 | 含义 |
| --- | --- |
| a | 打印 "am" 或 "pm" |
| A | 打印 "AM" 或 "PM" |
| h | 12 小时制小时 (01 到 12) |
| H | 24 小时制小时 (00 到 23) |
| g | 不带前导零的12 小时制小时 (1 到 12) |
| G | 不带前导零的24 小时制小时 (0 到 23) |
| i | 分钟 (00 到 59) |
| s | 秒 (00 到 59) |
| Z | 以秒的时区偏移 (-43200 到 43200) |
| U | 自 Epoch 以来的秒数 (1970年1月1日 00:00:00 GMT) |
| d | 两位数字的日期 (01 到 31) |
| j | 不带前导零的两位数字的日期 (1 到 31) |
| D | 文本格式的星期 (Mon 到 Sun) |
| 1 | 长文本格式的星期 (周一到周日) |
| w | 数字格式的星期，星期日到星期六 (0 到 6) |
| F | 长文本格式的月份 (1月到12月) |
| m | 两位数字的月份 (01 到 12) |
| n | 不带前导零的两位数字的月份 (1 到 12) |

| 表 B.7：date() 函数格式 |
| 字符 | 含义 |
| M | 三字母文本的月份 (Jan 到 Dec) |
| Y | 四位数字的年份 (2000) |
| y | 两位数字的年份 (00) |
| z | 一年中的第 (0 到 365) |
| t | 给定月份的天数 (28 到 31) |
| S | 英语序数后缀 (th, nd, st) |

## checkdate()

checkdate() 函数验证一个日期。验证成功意味着年份在 0 到 32767 之间，月份在 1 到 12 之间，且每个月的天数正确（考虑到闰年）。其语法为

```php

checkdate(month, day, year);

```

## mktime()

mktime() 函数返回长整型类型的 Unix 时间戳（自 Epoch 以来的秒数，1970年1月1日）。mktime() 的主要用途是格式化日期用于数学函数和日期验证。其语法为

```php

mktime(hour, minute, second, month, day, year);

```

## time() and microtime()

time() 函数返回长整数类型的 Unix 时间戳（自 Epoch 以来的秒数，1970年1月1日）。microtime() 函数返回带微秒的当前 Unix 时间戳。其语法为

```php

time();

microtime();

```

## 文件系统函数

基础 PHP 日期和时间函数允许你轻松地格式化时间戳用于数据库查询和日历函数，也可以简单地在订单表收据上打印日期。存在许多 PHP 函数用于连接和查询 MySQL 服务器。以下是一些基本函数及其语法。请参阅 PHP 手册 http://www.php.net/manual/ 以获取完整的 MySQL 函数列表——这些函数非常多！此函数打开一个到 MySQL 的连接。它需要服务器名、用户名和密码。

`$connection = mysql_connect("servername", "username", "password");`

此函数在 MySQL 服务器上创建一个数据库。它需要一个有效的已建立连接。

`mysql_create_db("myDB");`

此函数在 MySQL 服务器上删除一个数据库。它需要一个有效的已建立连接。

`mysql_drop_db("myDB");`

此函数在 MySQL 服务器上选择一个数据库供后续查询使用。它需要一个有效的已建立连接。

`$db = mysql_select_db("myDB", $connection);`

此函数发布 SQL 语句。它需要一个到数据库的打开连接。

`$sql_result = mysql_query("SELECT * FROM SOMETABLE", $connection);`

当连接或查询出现问题时，此函数返回一个有意义的错误信息。它通常在 `die()` 函数中使用，如下所示：

`$sql_result = mysql_query("SELECT * FROM SOMETABLE", $connection) or die(mysql_error());`

此函数自动将 SQL 语句的结果行放入数组。

$row = mysql_fetch_array($sql_result);

此函数返回结果集中的行数。

$num = mysql_num_rows($sql_result);

## rmdir()

类似于 rmdir 壳命令，rmdir() 函数从文件系统中删除一个目录。其语法为：

```php

rmdir("pathname");

```

PHP 用户必须在指定的目录中具有写权限。

## symlink()

symlink() 函数从文件系统中现有的文件或目录创建一个指定链接名的符号链接。其语法为：

```php

symlink("targetname", "linkname");

```

PHP 用户必须在指定的目录中具有写权限。

## unlink()

unlink() 函数从文件系统中删除文件。其语法为：

```php

unlink("filename");

```

PHP 用户必须对此文件具有写权限。

## HTTP Functions

用于发送 HTTP 头部和 cookie 数据的内置函数是开发 PHP Web 应用程序至关重要的方面。幸运的是，这些函数的语法非常容易理解和实现。

## header()

header() 函数输出 HTTP 头部字符串，例如位置重定向。此输出必须在向浏览器发送任何其他数据（包括 HTML 标签）之前发生。

此信息值得反复强调：在发送 header() 之前，不要尝试向浏览器发送任何类型的信息。你可以在 header() 之前执行任何数据库操作或计算，但你不能向屏幕打印任何内容——即使是一个新行。

例如，使用 header() 函数将用户重定向到新位置，使用此代码：

```php

header("Location: http://www.location.com");

exit;

```

提示 在 header() 语句后跟随 exit 命令。这确保了代码不会继续执行。

## setcookie()

setcookie() 函数向用户发送 cookie。cookie 必须在其他头部信息发送到 Web 浏览器之前发送。setcookie() 的语法为：

```php

setcookie("name", "value", "expire", "path", "domain", "secure");

```

例如，使用以下代码发送一个名为 username、值为 joe 的 cookie，它在 testcompany.com 域名下的所有目录中有效一小时：

```php

setcookie("username","joe", time()+3600, "/", "testcompany.com");

```

## Mail Function

PHP 函数让你的 HTML 表单与服务器的外发邮件程序之间的接口变得简单易用！

如果你的服务器可以访问 sendmail 或外部 SMTP 服务器，mail() 函数会将邮件发送给收件者。其语法为：

```php

mail("recipient", "subject", "message", "mail headers");

```

例如，以下代码向 julie@thickbook.com 发送邮件，主题为“I'm sending mail!”，正文为“PHP is cool!\nFrom: youmail@yourdomain.com\n”。

## Mathematical Functions

由于我几乎没有数学天赋，我发现 PHP 的内置数学函数至关重要！除了所有函数外，圆周率的值 (3.14159265358979323846) 已经在 PHP 中被定义为常量 (M_PI)。

## ceil()

ceil() 函数将分数向上舍入到下一个高阶整数。其语法为：

```php

ceil(number);

```

## decbin() and bindec()

decbin() 和 bindec() 函数分别将十进制数转换为二进数并将二进制数转换为十进制数。这些函数的语法为：

```php

decbin(number);

bindec(number);

```

## dechex() and hexdec()

dechex() 和 hexdec() 函数分别将十进制数转换为十六进制数并将十六进制数转换为十进制数。这些函数的语法为：

```php

dechex(number);

hexdec(number);

```

## decoct() and octdec()

decoct() 和 octdec() 函数分别将十进制数转换为八进制数并将八进制数转换为十进制数。这些函数的语法为：

```php

decoct(number);

octdec(number);

```

## floor()

floor() 函数将分数向下舍入到下一个低阶整数。其语法为：

```php

floor(number);

```

## number_format()

number_format() 函数返回指定数字的格式化版本。其语法为：

```php

number_format("number", "decimals", "thousands_sep");

```

例如，要返回数字 12156688 带有小数和千位分隔符的格式化版本，使用：

```php

echo number_format("12156688",2,"","");

```

结果是 12,156,668.00。

## pow()

pow() 函数返回指定幂的结果。其语法为：

```php

pow(number, exponent);

```

## rand()

rand() 函数在指定范围内生成随机整数。其语法为：

```php

rand(min, max);

```

## sqrt()

sqrt() 函数返回数字的平方根。其语法为：

```php

sqrt(number);

```

## srand()

srand() 函数设置随机生成器。其语法为：

```php

srand(seed);

```

## time()

time() 函数返回当前的 Unix 时间戳。其语法为：

```php

time();

```

## microtime()

microtime() 函数返回带微秒的时间。其语法为：

```php

microtime(prefix);

```

## date()

date() 函数返回本地时间的格式化字符串。其语法为：

```php

date(format, timestamp);

```

## explode()

explode() 函数根据分隔符将字符串分割为数组。其语法为：

```php

explode(delimiter, string);

```

## implode()

implode() 函数将数组元素合并为字符串。其语法为：

```php

implode(separator, array);

```

## str_replace()

str_replace() 函数替换多个搜索字符串。其语法为：

```php

str_replace(search, replacement, string);

```

## strpos()

strpos() 函数找到子字符串第一次出现的位置。其语法为：

```php

strpos(haystack, needle);

```

## substr()

substr() 函数返回字符串的某部分。其语法为：

```php

substr(string, start, length);

```

## strlen()

strlen() 函数返回字符串的长度。其语法为：

```php

strlen(string);

```



```php

$old_string = "I really love programming in ASP";

$new_string = ereg_replace("ASP", "PHP", $old_string);

echo "$new_string";

```

如果 "ASP" 是混合大小，例如 "aSp"，请使用 `eregi_replace()` 函数：

```php

$old_string = "I really love programming in aSp";

$new_string = eregi_replace("ASP", "PHP", $old_string);

echo "$new_string";

```

# split()

split() 函数使用特定的分隔符（逗号、冒号、分号等）将字符串分割为数组。它的语法为

```

split(pattern, string, [limit]);

```

如果指定了限制（limit），`split()` 函数将在指定位置停止——例如，在逗号分隔的列表中的第十个值。

# 会话处理函数 (Session-Handling Functions)

会话处理是在用户浏览你的 Web 网站时保留数据的方式。数据可以是变量或实体对象。这些简单的函数只是 PHP 中与会话相关的函数的少数几个；更多信息请参阅 PHP 手册 http://www.php.net/manual/。

# session_start()

如果尚未启动会话，session_start() 函数将启动一个会话；如果用户存在会话 ID，则恢复会话。此函数不接受任何参数，只需将以下内容放在代码开头即可调用：

```php

session_start();

```

# session_destroy()

session_destroy() 函数会销毁当前会话注册的所有变量和值。此函数不接受任何参数，只需将以下内容放在代码中即可：

```php

session_destroy();

```

# 字符串函数 (String Functions)

本节仅介绍了 PHP 内置字符串处理函数的冰，但如果你理解了这些常用函数，你的编程生活将会变得轻松！

# addslashes() 和 stripslashes()

在从数据库插入和检索数据时，这两个函数非常重要。插入到数据库的文本通常包含特殊字符（单引号、双引号、反斜杠、NULL），在插入之前必须对它们进行“转义”。`addslashes()` 函数正是此功能，其语法如下：

```

addslashes(string);

```

同样，`stripslashes()` 函数返回一个去掉了反斜杠的字符串，其语法如下：

```

stripslashes(string);

```

# chop(), ltrim(), 和 trim()

这些函数都会移除字符串中的错误空格。`chop()` 函数移除字符串末尾的空格，`ltrim()`移除字符串开头的空格。`trim()` 函数则移除字符串开头和结尾的空格。这些函数的语法如下：

```

chop(string);

ltrim(string);

trim(string);

```

# echo()

`echo()` 函数返回输出。`echo()` 的语法为

```

echo (parameter1, 2, ...);

```

例如：

```php

echo "I'm using PHP"; // 输出: I'm using PHP!

echo 2*6; // 输出是: 8

```

使用 `echo` 时不需要括号。

# explode() 和 implode()

`explode()` 函数使用给定的分隔符分割字符串并以数组形式返回值。

```

explode("separator", "string");

```

例如，以下代码取一个名为 $color_list 的字符串（该字符串包含用逗号分隔的颜色列表），并将每个颜色放入名为 $my_colors 的数组中：

```php

$color_list = "blue,black,red,green,yellow,orange";

$my_colors = explode(",", $color_list);

```

相反，`implode()` 函数接收一个数组并使用简单的分隔符将其转换为字符串。`implode()` 的语法为

```

implode("separator", "string");

```

例如，以下代码取一个名为 $color_list 的数组，创建一个名为 $mycolors 的字符串，其中包含 $color_list 数组的值，并用逗号分隔：

```php

$mycolors = implode(",", $color_list);

```

# htmlspecialchars() 和 htmlentities()

`htmlspecialchars()` 和 `htmlentities()` 函数将字符串中的特殊字符和 HTML 实体转换为接受的实体表示。`htmlspecialchars()` 函数仅转换小于号 (< 变为 &lt;）、大于号（> 变为 &gt;）、双引号（"" 变为 &quot;）和和培符号（& 变为 &amp;）。

`htmlentities()` 函数将 ISO-8859-1 字符集中的字符转换为正确的 HTML 实体。这些函数的语法如下：

```

htmlspecialchars(string);

htmlentities(string);

```

# nl2br()

`nl2br()` 函数将所有 ASCII 换行符替换为 HTML 换行符 (<BR>)。`nl2br()` 函数的语法为

```

nl2br(string);

```

# sprintf()

`sprintf()` 函数根据一组指令返回字符串，如表 B.9 所示。`sprintf()` 的语法为

```

sprintf(directives, string);

```

| 表 B.9: sprintf() 格式指令 |
| 指令 | 结果 |
| :--- | :--- |
| % | 添加百分号 |
| b | 将字符串视为整数并格式化为二进制数 |
| c | 将字符串视为整数并格式化为 ASCII 值 |
| d | 将字符串视为整数并格式化为十进制数字 |
| f | 将字符串视为双精度浮点数 |
| o | 将字符串视为整数并格式化为八进制数 |
| s | 视为字符串 |
| x | 将字符串视为整数并格式化为十六进制数 |
| X | 将字符串视为整数并格式化为大写十六进制数 |

# 表 B.9: sprintf() 格式指令（续） |

| 指令 | 结果 |
| :--- | :--- |
| %u | 将字符串视为无符�整数 |
| %e | 将字符串视为浮点数并格式化为科学计数法 |
| %E | 将字符串视为浮点数并格式化为大写科学计数法 |
| %g | 自动选择 %f 或 %e |
| %G | 自动选择 %f 或 %E |




将它们放在你的脚本中，甚至可以在外部文件中编写你自己的函数，仅在需要时使用它们。

## 函数的结构

函数具有非常特定的结构，如如下代码所示，其中 [function name] 和 [arguments] 应该替换为你自己的函数名以及任何你想要使用的参数。

```

function [function_name]{[arguments]} {

//

code

}

```

当你创建一个函数时，在函数名之前加上字面量单词 `function`。在 `function` 之后你的函数名之后，是一组圆括号内的参数列表。参数是可选的（因为如果你不想，就不必向函数传递任何参数），它们之间用逗号隔开，并包含了你的函数完成任务或多项任务所需的值。

在参数之后，你打开一组大括号，输入你所有的代码，最后关闭大括号。例如，下面的函数（称为 `multiplier`）接受一个名为 `$num` 的参数，并将该值乘以 5。

```

function multiplier($num) {

$answer = $num * 5;

}

```

假设你已经确定 $num 等于 8，并且这就是你传递给 `multiplier` 函数的值。根据你自己的数学知识，你知道 $answer 将等于 40。为了将该数字传回你的脚本（在函数外部），你必须返回（return）该值。

## 函数返回值

从函数返回值的基本方法是使用 `return` 语句。通常，该语句位于函数的末尾，如下：

```

function multiplier($num) {

$answer = $num * 5;

return $answer;

}

```

注意 `return` 语句可以出现在函数的任何地方，但当使用时，它将结束函数的执行。这意味着执行的代码是调用 `return` 语句的那行脚本代码。

当你使用 `return` 语句时，可以像这样在代码中调用函数：
echo multiplier(5);

这种用法将在你的屏幕上产生以下结果：

40

由于你将 8 作为 `$num` 参数传递给 `multiplier()` 函数，$answer` 变成了 40。由于 `$answer` 作为函数操作的结果被返回，并且你在调用函数后使用了 `echo`，你实际上是在告诉 PHP 输出函数内代码的结果。在这种情况下，该结果就是数字 40。

注意：你也可以使用 `return` 语句来获取多个值，但仅当它们是数组或对象的一部分时才。

使用 `return` 语句将函数的结果传递给主脚本是一种简单安全的方法，也是最常用的方法之一。如果不使用 `return` 语句，你必须将任何想要传回主脚本的变量声明为全局。例如：

```

function multiplier($num) {

global $answer;

$answer = $num * 5;

}

```

在这种情况下，你调用 `multiplier()` 函数，然后在 `echo` 语句中使用变量名，因为它没有直接从你的函数返回。例如，使用修改后的函数，以下代码将在你的屏幕上打印数字 40：

```

multiplier(5);

echo $answer;

```

如果你没有将 `$answer` 为全局变量，结果将是一个空白屏幕。

注意：花些心思决定哪些变量是你真正想要变为全局的。每当你声明某个内容为全局时，你必须采用额外的编程限制来维护数据的完整性。换句话说，你必须小心并留意你的所作。如果你声明了一个变量为全局变量，但在脚本的另一个部分使用了同名的变量，你将覆盖其中一个。一个良好的经验是控制好你的全局变量，并将它们保持在直接使用它们的程序局部范围内。

## 在代码中使用函数

到目前为止，你已经学习了自定义函数的基本结构，但还没有学习它是如何在你自己的脚本中应用的。对于 `multiplier()` 函数来说，创建一个像这样的脚本仅仅为了在屏幕上打印一个数字，似乎非常耗时：

```php

<?php

function multiplier($num) {

$answer = $num * 5;

return $answer;

}

echo multiplier(5);

?>

```

相反，想象有一个名为 `db_connect()` 的函数，它包含了数据库连接和选择代码：

```php

function db_connect() {

$connection = @mysql_connect("localhost", "spike", "9sj7En4")

or die(mysql_error());

$db = @mysql_select_db($db_name, $connection)

or die(mysql_error());

}

```

与其在每个脚本中反复输入那两行，不如只需输入：
db_connect();

如果你的主机名、用户名、密码或数据库名称发生变化，你只需要在一个地方更改这些信息——唯一的技巧就是把这个函数放在哪里。显然，如果你创建一个函数是为了重用内部的代码，你就不希望该函数是脚本的一部分。相反，你将函数放在一个单独的文件中（包含其他函数的文件），并使用 `include()` 或 `require()` 根据需要将信息拉取到你的脚本中。

## 使用 include() 和 require()

`include()` 和 `require()` 函数本质上的作用相同：当被调用时，被包含的文件中的代码将成为调用它的脚本的一部分。从那时起，被包含文件中的任何内容都可以在调用脚本中使用。`include()` 和 `require()` 之间的区别出现在无法打开要包含的文件。使用 `include()` 会得到一个警告，但代码会尽可能继续执行。使用 `require()` 会得到一个致命错误（fatal error），PHP 将停止。

包含的文件看起来与其他任何其他文件一样，以开启标签开始，以关闭标签结束。例如，假设你有一个名为 `functions.php` 的文件，包含以下代码：

```php

<?php

/**

 multiplier 函数将数字乘以 5 并返回

 */

function multiplier($num) {

    $answer = $num * 5;

    return $answer;

}

/** db_connect() 函数连接到我的数据库。 */

function db_connect() {

  $connection = @mysql_connect("localhost", "spike", "9sj7En4")

  or die(mysql_error());

  $db = @mysql_select_db($db_name, $connection)

  or die(mysql_error());

}

?>

```

那么，在你需要连接数据库的实际 PHP 脚本中，你将会有如下：

```php

<?php

// 包含该函数的文件

include("/path/to/myfunctions.php");

// 调用函数

db_connect();

?>

```

现在你可以执行诸如查询并获取结果等操作



```sql

DROP DATABASE IF EXISTS [yourDBName];

```

在使用 `DROP` 命令时请务必小心，因为一旦删除了数据库，所有的表也会随之删除！

## 创建或删除表

你也可以使用 `CREATE` 命令在当前数据库中创建一个表。语法如下：

```sql

CREATE TABLE [yourTableName] ([fieldName1] (type), [fieldName2] [type], ...) [options]

```

要从当前数据库中删除一个表，请使用 `DROP` 命令：

```sql

DROP TABLE [yourTableName];

```

在使用 `DROP` 命令时请务必小心，因为一旦删除了表，它们就彻底消失了！

## 修改表

`ALTER` 命令让你有机会修改特定表的元素，例如重命名列、更改列的类型、添加列、删除列等。以下是一些常见用法：

- 向表中添加列，使用：
  - ALTER TABLE [yourTableName] ADD [newColumn] [fieldDefinition]
- 从表中删除列，使用：
  - ALTER TABLE [yourTableName] DROP [columnName]
- 将列从一种类型更改为另一种类型，使用：
  - ALTER TABLE [yourTableName] CHANGE [columnName] [newfieldDefinition]
- 在你的表中创建一个唯一列，使用：
  - ALTER TABLE [yourTableName] ADD UNIQUE [columnName] ([columnName]);
- 为表中的列创建索引，使用：
  - ALTER TABLE [yourTableName] ADD INDEX [columnName] ([columnName]);

使用 `ALTER` 命令避免了仅仅因为拼写错误字段名或出现细微错误就删除整个表并重新创建的需要。

## 在表内插入、更新或替换

`INSERT` 和 `REPLACE` 命令每次向你的表填充一条记录。`INSERT` 的语法为：

```sql

INSERT INTO [yourTableName] ([fieldName1], [fieldName2], ...)

VALUES ('value of fieldName1', 'value of fieldName2'...);

```

在插入记录时，请确保用单引号或双引号分隔你的字符串。如果你在字符串周围使用单引号，且要添加的数据包含单引号（'），请在 `INSERT` 语句中使用转义单引号（\\'）来避免错误。同样地，如果你在字符串周围使用双引号并想将双引号作为数据的一部分，请在 `INSERT` 语句中转义双引号（\"）。

`REPLACE` 命令与 `INSERT` 命令具有相同的语法和要求。唯一的区别在于你使用 `REPLACE` 根据唯一值来覆盖表中的记录：

```sql

REPLACE INTO [yourTableName] ([fieldName1], [fieldName2], ...)

VALUES ('value of fieldName1', 'value of fieldName2...');

```

`UPDATE` 命令修改记录的部分内容而不替换整条记录。要用相同的值更新表中的整列，请使用：

```sql

UPDATE [yourTableName] SET [fieldName] = 'new value';

```

如果你只想更新特定的行，请使用 `WHERE` 子句：

```sql

UPDATE [yourTableName] SET [fieldName] = 'new value' WHERE [some expression];

```

`UPDATE` 是一个非常强大的 SQL 命令。例如，你可以对现有记录执行字符串函数和数学函数，并使用 `UPDATE` 命令修改它们的值。

## 从表内删除数据

与 `DROP` 命令一样，在生产环境中，如果不注意自己在做什么就直接使用 `DELETE` 可能会导致严重的后果。一旦删除了表或记录，它将永远消失。不要害怕，只要小心即可。要删除表的所有内容，请使用以下：

```sql

DELETE FROM [yourTableName];

```

如果你只想删除特定的行，请使用 `WHERE` 子句：

```sql

DELETE FROM [yourTableName] WHERE [some expression];

```

如果你准备开始删除记录，请确保你已经备份，以防万一。每个人都会出错的。

## 从表内查询数据

在创建数据库驱动的网站时，`SELECT` 命令可能是你工具箱中最频繁使用的命令。`SELECT` 命令根据你定义的标准从表中选出某些记录。以下是 `SELECT` 的基本语法：

```sql

SELECT [field names] FROM [table name]

WHERE [some expression]

ORDER BY [field names];

```

要选择表中的所有记录，请使用：

```sql

SELECT * FROM [yourTableName];

```

要选择表某个特定列的条目，请使用：

```sql

SELECT [columnName] FROM [yourTableName];

```

要选择表中的所有记录并按特定顺序返回，请使用 `ORDER BY` 表达式。例如，如果你有一个用于记录条目的日期字段，并且你想查看从新到旧的所有记录条目，请使用：

```sql

SELECT * FROM [yourTableName] ORDER BY [dateField] DESC;

```

`DESC` 代表“降序”（descending）。要从旧到新查看，请使用代表“升序”（ascending）。`ASC` 是默认顺序。

你可以在 SQL 语句中执行数学和字符串函数，从而使用 `SELECT` 实现不仅仅输出现有数据。示例如下。

## 字符串函数

此列表包含了 MySQL 手册中列出的许多字符串相关函数的几个。访问 http://www.mysql.com/ 并查看完整手册以获取信息。

- 你可以使用 `CONCAT()` 函数拼接值。语法为 `SELECT CONCAT([field1],[field2],...) [AS name] FROM [yourTableName];`。
- 使用 `LOWER()` 函数将结果转换为小写。语法为 `SELECT LOWER([field1],[field2],...) FROM [yourTableName];`。
- 使用 `UPPER()` 函数将结果转换为大写。语法为 `SELECT UPPER([field1],[field2],...) FROM [yourTableName];`。

## 日期和时间函数

此列表包含了 MySQL 手册中列出的许多字符串相关函数的几个。访问 http://www.mysql.com/ 并查看完整手册以获取信息。

- 你可以使用 `CONCAT()` 函数拼接值。语法为 `SELECT CONCAT([field1],[field2],...) [AS name] FROM [yourTableName];`。
- 使用 `LOWER()` 函数将结果转换为小写。语法为 `SELECT LOWER([field1],[field2],...) FROM [yourTableName];`。
- 使用 `UPPER()` 函数将结果转换为大写。语法为 `SELECT UPPER([field1],[field2],...) FROM [yourTableName];`。

## 使用 Show 命令

有几种类型的 `SHOW` 命令，它们产生的输出有助于你管理数据库。基本的 `SHOW` 命令是 `SHOW DATABASES` 和 `SHOW TABLES`，它们仅显示数据库和表的名称。如果你使用了 `CREATE TABLE` 命令，它会显示用于创建表的 SQL 语句。

如果你需要知道表的结构但不一定需要它的 SQL 命令，可以使用 `SHOW COLUMNS` 命令：

```sql

SHOW COLUMNS FROM [test];



出于管理目的，`SHOW STATUS` 和 `SHOW VARIABLES` 命令可以快速提供有关服务器的重要信息。关于这些命令输出的许多行详细信息，请阅读 MySQL 手册的相关章节。

# 附录 E：数据库规范化

本书中使用的数据库设计是为了简单，帮助你理解 PHP 和 MySQL 之间的基本交互。“规范化”数据库。“规范化”是一个在你开始创建详细的数据库驱动应用程序时经常听到的词，它需要一种不同的思维方式——在看到关系之前对关系进行思考。在本附录中，你将学习数据库规范化的基础。

如果你的数据库设计遵循第一组规则，则它被认为是第一范式。如果遵循了前三组规范化规则，则你的数据库被认为处于第三范式。我们将使用学生和课程的概念通过各个范式，并最终规范化书中之前使用的 *my_contacts* 表。

## 应用范式

在解释第一范式之前，让我们从一个需要规范化的东西开始。在数据库的情况下，它就是*平表*（flat table）。平表就像一个包含许多列数据的电子表格。多个表之间没有关系，因为你可能需要的所有数据都在这一个平表中。这种场景并不是最高效的设计，与一组规范化的数据库表相比，它会占用更多的硬盘空间。

假设你有一个存储学校学生和课程信息的表。你可能在平表中拥有表 E.1 所示的字段。

| 表 E.1：学生与课程表 |
| 字段名称 | 描述 |
| --- | --- |
| StudentName | 学生姓名 |
| CourseID1 | 学生修读的第一门课程 ID |
| CourseDescription1 | 学生修读的第一门课程的教师 |
| CourseInstructor1 | 学生修读的第一门课程的教师 |
| CourseID2 | 学生修读的第二门课程 ID |
| CourseDescription2 | 学生修读的第二门课程描述 |
| CourseInstructor2 | 学生修读的第二门课程的教师 |

你可以多次重复 CourseID、CourseDescription 和 CourseInstructor 列，以记录学生在学术生涯期间可能的所有课程。虽然这是冗余的，但在创建用于存储信息的单扁表时使用的是这种方法。消除这种冗余是规范化的第一步，因此你首先将此此扁表转换为一阶范式。如果你的表保持这种格式，你会有很多未使用的空间以及大量不必要的空间——这并不是高效的表设计！

## 将表转换为一阶范式

一阶范式的主要规则是：

- 消除重复信息
- 为相关数据创建单独的表

观察这个扁平设计，由于学生和课程有许多重复的字段组，你可以识别出学生和课程是两个不同的领域。将你的学生和课程扁表转换为一阶范式意味着你要创建两个表：一个用于学生（命名为 students），另一个用于学生加课程（命名为 students_courses）。你可以在表 E.2 和 E.3 中看到新的表设计。

| 表 E.2：students 表 |
| 字段名称 | 描述 |
| --- | --- |
| StudentID | 学生的唯一 ID。此新字段现在是主键 |
| StudentName | 学生姓名 |

| 表 E.3：students_courses 表 |
| 字段名称 | 描述 |
| --- | --- |
| StudentID | 学生的唯一 ID，匹配 students 表中的条目。 |
| CourseID | 学生修读的课程 ID |
| CourseDescription | 学生修读的课程描述 |
| CourseInstructor | 学生修读的课程的教师 |

你的表现在代表了一个学生到多门课程的一对多关系。学生可以根据意愿修读任意数量课程，而不限于扁平表中存在的 CourseID/CourseDescription/CourseInstructor 分组数量。

你仍然还有一些工作要做，因为下一步是将表转换为二阶范式。

## 将表转换为二阶范式

二阶范式的基本规则是：

- 非键属性不依赖于主键的一部分

通俗地说，这意味着如果你的表没有完全关联主键，那么你还有更多工作要做。在我们正在使用的学生和课程示例中，我们正将课程提取到单独的表中，这样扁平表现在是一张完整的学生表。

CourseID、CourseDesc、CourseInstructor 可以变成一个名为 courses 的表，主键为 CourseID。然后 students_courses 表应该只包含两个：StudentID 和 CourseID。你可以在表 E.4 和 E.5 中看到新的设计。

| 表 E.4：courses 表 |
| 字段名称 | 描述 |
| --- | --- |
| CourseID | 课程的唯一 ID |
| CourseDescription | 课程描述 |
| CourseInstructor | 课程的教师 |

| 表 E.5：新的 students_courses 表 |
| 字段名称 | 描述 |
| --- | --- |
| StudentID | 学生的唯一 ID，匹配 students 表中的条目。 |
| CourseID | 所修读课程的唯一 ID，匹配 courses 表中的条目。 |

信不不信，你可以通过这个示例进一步进行到三阶范式。

## 将表转换为三阶范式

三阶范式的规则是：

- 属性不依赖于其他非键属性

这简单意味着你需要查看你的表，看看是否存在更多可以进一步拆分且不依赖于键的字段。考虑移除重复数据，你就会找到答案——教师。不可避免的是，一个教师会教授超过一门课程。然而，courses 表中的 CourseInstructor 字段并不是任何类型的键。如果你提取这些信息并纯粹为了效率和维护之目的创建一个单独的表，那就是三阶范式。请看表 E.6 和 E.7 中新的 courses 表和 instructors 表。

| 表 E.6：courses 表 |
| 字段名称 | 描述 |
| --- | --- |
| CourseID | 课程的唯一 ID |
| CourseDescription | 课程描述 |
| CourseInstructor | 教师的 ID，匹配 instructors 表中的条目 |

| 表 E.7：instructors 表 |
| 字段名称 | 描述 |
| --- | --- |
| InstructorID | 教师的唯一 ID |
| InstructorName | 教师姓名 |
| InstructorNotes | 关于教师的任何备注 |

三阶范式通常足以消除冗余并允许灵活性和增长。接下来，你将规范化本书之前使用的 my_contacts 表。

## 规范化 my_contacts 表

在原始的 my_contacts 表中，没有很多重复信息，但如果你将其扩展到一本真正的书，就很容易产生重复信息。在地址录中，人们通常有家庭和工作的联系信息，或者多种电话方式（座机、手机等），甚至有多个电子邮件地址。将这些元素拆分到单独的表中并将其关联到主键会更有意义。

| 表 E.8：my_contacts 表 |
| 字段名称 | 描述 |
| --- | --- |
| id | 创建一个条目的 ID |
| f_name | 姓名 |
| l_name | 姓氏 |
| address1 | 地址第一行 |
| address2 | 地址第二行 |
| address3 | 地址第三行 |
| postcode | 邮编 |
| country | 所在国家 |
| prim_tel | 主电话号码 |
| sec_tel | 次电话号码 |

| 表 E.9：表 |
| 字段名称 | 描述 |
| --- | --- |
| id | 创建一个条目的 ID |
| contact_id | 匹配主表中的条目 |
| address1 | 地址第一行 |
| address2 | 地址第二行 |
| address3 | 地址第三行 |
| postcode | 邮编 |
| country | 所在国家 |

| 表 E.10：phone 表 |
| 字段名称 | 描述 |
| --- | --- |
| id | 创建一个条目的 ID |
| contact_id | 匹配主表中的条目 |
| phone | 电话号码 |
| phone_type | 电话类型 |

| 表 E.11：email 表 |
| 字段名称 | 描述 |
| --- | --- |
| id | 创建一个条目的 ID |
| contact_id | 匹配主表中的条目 |
| email | 电子邮件地址 |
| email_type | 电子邮件类型 |

| 表 E.12：my_contacts 表 |
| 字段名称 | 描述 |
| --- | --- |
| id | 创建一个条目的 ID |
| f_name | 姓名 |
| l_name | 姓氏 |
| birthday | 生日 |

在原始的 my_contacts 表中，没有很多重复信息，但如果你将其扩展到一本真正的书，就很容易产生重复信息。在地址录中，人们通常有家庭和工作的联系信息，或者多种电话方式（座机、手机等），甚至有多个电子邮件地址。将这些元素拆分到单独的表中并将其关联到主键会更有意义。

## 附录 F：获取帮助

开源社区最大的优点之一是人们乐于帮助你学习，以便你也能成为倡导者。然而，在向整个社区提问之前，你应该尝试寻找答案，包括可用手册和 FAQ 以及访问网站。

本书以及我写的其他书的网站是 http://www.premierpressbooks.com/downloads.asp。你可以在那里找到勘误、下载代码、书籍和其他推荐，以及我在空闲时间想出来的任何内容。如果你对某些内容感到困惑，我也乐意回答问题。

## 资源

与 PHP 相关的网站、新闻组和邮件列表随处可见。这里列出的只是其中一小部分。

## 网站

这些网站大部分是由普通人利用业时间维护的，所以如果你使用了他们的资源，请通过在可以时帮助他人的问题、向代码库提交代码段等方式回馈社区。

[www.php.net](http://www.php.net)

PHP 的主页是 http://www.php.net。这里有在线手册，以及 FAQ、错误报告、提供 PHP 服务的 ISP 链接、新闻文章等等！

[www.zend.com](http://www.zend.com)

PHP Zend 引擎后的 Zend Technologies 为 PHP 开发者创建了一个门户网站。这个个性化的网站不仅展示了如何使用 PHP 构建高流量动态网站，还提供了提示、资源和课程，教你如何在所有的在线应用程序中充分利用 PHP 的潜力。

## Webmonkey (hotired.lycos.com/webmonkey/)

带来《Wired》杂志的公司也带来了 HotWired，后者催生了 Webmonkey。这是一个面向开发者的资源网站，设有专门针对 PHP 的板块。不要把自己限制在 Webmonkey 的 PHP 板块，因为其他板块也有许多丰富信息。这是我最喜欢的网站之一，不仅是因为我为他们写过文章，更因为他们是一群聪明的人。

## WeberDev (www.weberdev.com)

这是 PHP 开发者长期以来喜爱的网站，该网站包含许多编程语言的开发技巧和提示（为了公平起见），以及一个让每个人都能添加自己的代码片段、教程等内容的内容管理系统！它有一份非常棒的每周通讯，而且流量很高。请持续关注！

## PHPBuilder (www.phpbuilder.com)

这是一个非常适合中高级 PHP 开发者阅读的教程。它包含了每周更新的针对实际应用的“如何做列”（How To Columns），例如“考虑到搜索引擎的动态页面构建”、“生成可发音密码”等大量内容。强烈推荐！

## DevShed (www.devshed.com)

该网站包含许多用户提交的教程、新闻文章、访谈以及对服务端编程语言的竞争分析。它涵盖了 PHP 以及许多其他开发者感兴趣的话题，如服务器和数据库。

## px.sklar.com

这是一个极简的代码库，但如果你需要的只是代码片段，谁还需要图形界面呢？借鉴“拿走一个硬币，留下一一个硬币”的心态，你可以取一个代码片段开始，当你觉得有信心分享时再添加你自己的。

## PHP KnowledgeBase (php.faqs.com)

PHP 知识库包含了 PHP 邮件列表上提出的问题和答案。任何人可以在该网站上回答问题或提出新问题。

## 邮件列表 (Mailing Lists)

有几个高流量的邮件列表可以使用英语及其他语言进行 PHP 讨论。在提问时请记住你的网络礼仪（netiquette）：保持礼貌，尽可能提供示例（如果你在描述问题），提供你的系统信息（如果你在寻找解决方案），难道我提到过要说“请”和“谢谢”吗？

你可以在 http://www.php.net/ 的 Support 部分找到邮件列表订阅信息。英语 PHP 邮件列表已存档，并可以在 http://marc.theaimsgroup.com/ 进行搜索。只需查找 WWW 标题下的 PHP 相关列表即可。

## 用户组 (User Groups)

有时，在现实生活中认识其他开发者会很有帮助。你可以在 http://www.phpusergroups.org/ 找到 PHP 用户组列表。

## MySQL 资源 (MySQL Resources)

之前列出的许多与 PHP 相关的网站也包含关于 MySQL 开发的信息，但 MySQL 官方网站 http://www.mysql.com/ 是获取全面 MySQL 信息的起点。

在线 MySQL 手册非常庞大，但它写得非常好且非常实用，所以它的规模不应该吓到你。你可以在 http://www.mysql.com/doc/ 找到手册。如果你正在寻找 MySQL 的快速入门，我写了一本名为《24小时自学MySQL》（*Teach Yourself MySQL in 24 Hours*）的书，在全球书店都有售。

和 PHP 一样，几个高流量的邮件列表可以使用英语和其他语言进行 MySQL 。你可以在 http://www.mysql.com/documentation/lists.html 找到邮件列表订阅信息，MySQL 邮件列表同样存档并可以在 http://marc.theaimsgroup.com/ 进行搜索。

## Apache 资源 (Apache Resources)

从 Apache 基金网站 http://www.apache.org/ 开始，获取服务器文档和常见问题列表（FAQs）。许多面向开发者的网站都提供特定的 Apache 教程——你只需要去寻找它们即可。
