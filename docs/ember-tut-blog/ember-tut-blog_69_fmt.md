

# 如何搭建 Ember.js 开发环境

本篇是针对完全的小白开发者，如果你已经懂得如何搭建 [Ember.js](http://emberjs.com) 开发环境则不需要再看了！

## Windows 系统

### 软件需求

Windows 系统搭建 `Ember.js` 开发环境主要有如下几个步骤：

#### 安装 [Node.js](http://nodejs.org/)

- 推荐使用最新稳定版 `node-v4.4.4`，[百度网盘下载地址](http://pan.baidu.com/s/1c2dWJsc)。

- `Node.js` 的安装我就不啰嗦了，下载之后按照普通的软件安装方式安装。

- 安装完毕之后再打开 `cmd` 控制台，输入 `node -v`，如果能看到 `Node.js` 的版本信息，说明安装成功。

#### 安装 [Git](https://www.git-scm.com/download/)

- `Git` 安装与 `Node.js` 一样，下载安装后打开一个新的 `cmd` 命令窗口，输入 `git -v`，如果看到下面的信息，说明安装成功。

- [Git 网盘下载地址](http://pan.baidu.com/s/1eShq1kI)。

```js
Unknown option: -v
usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p|--paginate|--no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]
```

说明安装成功。

#### 安装 [Ember CLI](http://ember-cli.com/user-guide)

- `Ember CLI` 的安装很简单，但是安装 `Ember CLI` 的前提是你必须成功安装了 `Node.js`。

- 执行命令 `npm install -g ember-cli@2.6` 安装 `Ember CLI`。

- 验证是否安装成功，打开 `cmd` 命令窗口输入 `ember -v`。如果看到下面的打印信息，说明安装成功。

```js
C:\Users\Administrator>ember -v
ember-cli: 2.6.3
node: 4.4.4
os: win32 x64
```

#### 安装 [Bower](https://bower.io/)

- `Bower` 的安装与 `Ember CLI` 安装方式一样。直接执行命令 `npm install -g bower` 安装即可。

- 如果控制台没有出现报错的信息，则说明安装成功。

到此所必须的软件全部安装完毕！！！

### 验证

创建一个 `Ember` 项目，验证环境是否搭建成功了。

#### 创建项目

创建项目使用 `Ember CLI` 命令。

```js
ember new new-app
```

创建了一个名为 `new-app` 的项目。

注意：创建的过程可能会比较慢，请耐心等待，创建过程中会下载项目所需的 `npm`、`Bower` 依赖。

#### 运行项目

进入项目目录。

```js
cd new-app
```

运行：

```js
ember server
```

等待运行完毕，可以看到控制台会打印信息 `Livereload server on http://localhost:49152 Serving on http://localhost:4200/`。然后在浏览器打开 [`localhost:4200`](http://localhost:4200)，如果在界面上看到 `Welcome to Ember` 字样，说明环境搭建成功。

到此 Windows 系统的 `Ember.js` 开发环境搭建完毕。

## Mac、Linux 系统

Mac 和 Linux 系统的环境搭建与 Windows 基本类似。主要用到的软件都是一样的，唯一不同的是可以安装更多其他可选的软件。

1. 安装 [Watchman](https://facebook.github.io/watchman/)，安装命令 `brew install watchman`。

2. 安装 [PhantomJS](https://ember-cli.com/user-guide/#phantomjs)，安装命令 `npm install -g phantomjs-prebuilt`。

### 验证

验证方式与 Windows 系统一致。

### IDE 推荐

对于 IDE 各有所好，没有最好的，只有最合适的，只要自己用习惯了就是最好的。

目前我用的是 [Atom](https://atom.io/)，个人觉得比 Sublime Text 好，而且是免费，还有非常丰富的插件。

其他的重量级的就没必要了，开发 `Ember` 应用普通的编辑器就够用了。我是不推荐使用 WebStorm 或者 IntelliJ 这些比较大型的 IDE。

如果你还不懂如何搭建，请给我留言吧！！

