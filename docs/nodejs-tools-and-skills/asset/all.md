![](Images/default_cover.jpeg)

![](Images/default_cover.jpeg)

## Node.js: Tools and Skills, 2nd Edition

Copyright © 2020 SitePoint Pty. Ltd.

Ebook ISBN: 978-1-925836-39-4

*   **Product Manager:** Simon Mackie
*   **Project Editor Editor:** James Hibbard
*   **English Editor:** Ralph Mason
*   **Cover Designer:** Alex Walker

## Notice of Rights

All rights reserved. No part of this book may be reproduced, stored in a retrieval system or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical articles or reviews.

## Notice of Liability

The author and publisher have made every effort to ensure the accuracy of the information herein. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors and SitePoint Pty. Ltd., nor its dealers or distributors will be held liable for any damages to be caused either directly or indirectly by the instructions contained in this book, or by the software or hardware products described herein.

## Trademark Notice

Rather than indicating every occurrence of a trademarked name as such, this book uses the names only in an editorial fashion and to the benefit of the trademark owner with no intention of infringement of the trademark.

![SitePoint logo](Images/sitepoint-logo-2012.png)
Published by SitePoint Pty. Ltd.

Level 1, 110 Johnston St, Fitzroy
VIC Australia 3065
Web: www.sitepoint.com
Email: books@sitepoint.com

## About SitePoint

SitePoint specializes in publishing fun, practical, and easy-to-understand content for web professionals. Visit [http://www.sitepoint.com/](http://www.sitepoint.com/) to access our blogs, books, newsletters, articles, and community forums. You’ll find a stack of information on JavaScript, PHP, design, and more.

## About Craig Buckler

[Craig](https://craigbuckler.com/) is a freelance developer, author, and speaker who never shuts up about the web.

He started coding in the 1980s when applications had to squeeze into a few kilobytes of RAM. His passion for the Web was ignited in the mid 1990s when 28K modems were typical and 100KB pages were considered extravagant.

Over the past decade, Craig has written 1,200 tutorials for SitePoint as web standards evolved. Despite living in a technically wondrous future, he has never forgotten what could be achieved with modest resources.

# Preface

While there have been quite a few attempts to get JavaScript working as a server-side language, Node.js (frequently just called Node) has been the first environment that's gained any traction. It's now used by companies such as Netflix, Uber and Paypal to power their web apps. Node allows for blazingly fast performance; thanks to its event loop model, common tasks like network connection and database I/O can be executed very quickly indeed.

In this book, we'll take a look at a selection of the related tools and skills that will make you a much more productive Node developer.

## Who Should Read This Book?

This book is for anyone who wants to start learning server-side development with Node.js. Familiarity with JavaScript is assumed, but we don't assume any previous back-end development experience.

## Conventions Used

### Code Samples

Code in this book is displayed using a fixed-width font, like so:

```
 <h1>A Perfect Summer's Day</h1>
<p>It was a lovely day for a walk in the park.
The birds were singing and the kids were all back at school.</p> 
```

Where existing code is required for context, rather than repeat all of it, ⋮ will be displayed:

```
 function animate() {
    ⋮
new_variable = "Hello";
}
```

Some lines of code should be entered on one line, but we’ve had to wrap them because of page constraints. An ➥ indicates a line break that exists for formatting purposes only, and should be ignored:

```
 URL.open("http://www.sitepoint.com/responsive-web-
➥design-real-user-testing/?responsive1");
```

You’ll notice that we’ve used certain layout styles throughout this book to signify different types of information. Look out for the following items.

### Tips, Notes, and Warnings

#### Hey, You!

Tips provide helpful little pointers.

#### Ahem, Excuse Me ...

Notes are useful asides that are related—but not critical—to the topic at hand. Think of them as extra tidbits of information.

#### Make Sure You Always ...

... pay attention to these important points.

#### Watch Out!

Warnings highlight any gotchas that are likely to trip you up along the way.

## Supplementary Materials

*   [https://www.sitepoint.com/community/](https://www.sitepoint.com/community/) are SitePoint’s forums, for help on any tricky problems.
*   **books@sitepoint.com** is our email address, should you need to contact us to report a problem, or for any other reason.

# Chapter 1: Installing Multiple Versions of Node.js Using nvm

### by Michael Wanyoike and James Hibbard

When working with Node.js, you might encounter situations where you need to install multiple versions of the runtime.

For example, maybe you have the latest version of Node set up on your machine, yet the project you’re about to start working on requires an older version. Or maybe you’re upgrading an old Node project to a more modern version and it would be handy to be able to switch between the two while you make the transition.

Without a good tool, this would mean spending a lot of time and effort manually uninstalling and reinstalling Node versions and their global packages. Fortunately, there’s a better way!

## Introducing nvm

[nvm](https://github.com/creationix/nvm) stands for Node Version Manager. As the name suggests, it helps you manage and switch between different Node versions with ease. It provides a command-line interface where you can install different versions with a single command, set a default, switch between them and much more.

## OS Support

nvm supports both Linux and macOS, but that’s not to say that Windows users have to miss out. There’s a second project named [nvm-windows](https://github.com/coreybutler/nvm-windows) that offers Windows users the option of easily managing Node environments. Despite the name, nvm-windows is not a clone of nvm, nor is it affiliated with it. However, the basic commands listed below (for installing, listing and switching between versions) should work for both nvm and nvm-windows.

## Installation

Let’s first cover installation for Windows, macOS and Linux.

### Windows

First, we need to do a little preparation:

*   uninstall any existing versions of Node.js
*   delete any existing Node.js installation directories (such as `C:\Program Files\nodejs`)
*   delete the existing npm install location (such as `C:\Users\<user>\AppData\Roaming\npm`)

After this, download and run the [latest stable installer](https://github.com/coreybutler/nvm-windows/releases) and you should be good to go!

### macOS/Linux

Unlike Windows, removing previous Node and npm installations in macOS and Linux is optional. If this is something you want to do, there are plenty of good resources available online. For example, here’s how to remove Node on [macOS](http://stackoverflow.com/q/11177954/1136887) and on [Linux](http://stackoverflow.com/q/5650169/1136887). And here’s how you can [remove any previous npm installation](https://docs.npmjs.com/misc/removing-npm) you might have.

You can install nvm using cURL or Wget. On your terminal, run the following:

With [cURL](https://curl.haxx.se/):

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.2/install.sh | bash
```

Or with [Wget](https://www.gnu.org/software/wget/):

```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.35.2/install.sh | bash
```

Note that the version number (`v0.35.2`) will change as the project develops, so it’s worth checking the [relevant section of project’s home page](https://github.com/creationix/nvm#install-script) to find the most recent version.

This will clone the nvm repository to `~/.nvm` and will make the required changes to your bash profile, so that `nvm` is available from anywhere in your terminal.

And that’s it! Reload (or restart) your terminal and nvm is ready to be used.

## Using nvm

If installed correctly, the `nvm` command is available anywhere in you terminal. Let’s see how to use it to manage Node.js versions.

### Install Multiple Versions of Node.js

One of the most important parts of nvm is, of course, installing different versions of Node.js. For this, nvm provides the `nvm install` command. You can install specific versions by running this command followed by the version you want. For example:

```
nvm install 12.14.1
```

By running the above in a terminal, nvm will install Node.js version `12.14.1`.

#### Running `nvm use`

nvm-windows users will have to run `nvm use 12.14.1` after installing.

nvm follows [SemVer](http://semver.org/), so if you want to install, for example, the latest `12.14` patch, you can do it by running:

```
nvm install 12.14
```

nvm will then install Node.js version `12.14.X`, where `X` is the highest available version. At the time of writing, this is 1, so you’ll have the `12.14.1` version installed on your system.

You can see the full list of available versions by running:

```
nvm ls-remote
```

For nvm-windows, this is:

```
nvm ls available
```

#### Reducing Output

Listing all available Node versions produces a lot of output. Linux users might like to qpipe that to `less` or `grep` the version they’re after. For example, `nvm ls-remote | less`, or `nvm ls-remote | grep v12`.

### npm

When installing a Node.js instance, nvm will also install a compatible [npm](http://www.sitepoint.com/beginners-guide-node-package-manager/) version. Each Node version might bring a different npm version, and you can run `npm -v` to check which one you’re currently using. Globally installed npm packages aren’t shared among different Node.js versions, as this could cause incompatibilities. Rather, they’re installed alongside the current Node version in `~/.nvm/versions/node/<version>/lib/node_modules`. This has the added advantage that users won’t require `sudo` privileges to install global packages.

Fortunately, when installing a new Node.js version, you can reinstall the npm global packages from a specific version. For example:

```
nvm install v12.14.1 --reinstall-packages-from=10.18.1
```

By running the above, nvm will install Node.js version `12.14.1`, the corresponding npm version, and reinstall the global npm packages you had installed for the `10.18.1` version.

If you’re not sure what the latest version is, you can use the `node` alias:

```
nvm install node
```

This will currently pull in version `13.6.0`.

Or you can install the most recent [LTS release](https://en.wikipedia.org/wiki/Long-term_support), using:

```
nvm install --lts
```

This will currently pull in version `12.14.1`.

You can also uninstall any instance you no longer think is useful, by running:

```
nvm uninstall 13.6.0
```

### Switching Between Versions

So far, we’ve seen how to install different Node versions. Now let’s go through how to switch between them. Let me first note that when a new version is installed, it’s automatically put to use. So if you install the latest Node.js version, and run `node -v` right after, you’ll see the latest version output.

To switch through installed versions, nvm provides the `nvm use` command. This works similarly to the install command. So, you need to follow this by a version number or an alias.

Switch to Node.js version `13.6.0`:

```
nvm use 13.6.0
```

Switch to Node.js version `12.14.1`:

```
nvm use 12.14.1
```

Switch to the latest Node.js version:

```
nvm use node
```

Switch to the latest LTS version:

```
nvm use --lts
```

When switching to a different version, nvm will make the `node` instance in your terminal symlink to the proper Node.js instance.

### Custom Aliases

You can also create custom aliases beyond the ones that come with nvm. For example, by running:

```
nvm alias awesome-version 13.6.0
```

You’re setting an alias with the name “awesome-version” for Node.js version `13.6.0`. So, if you now run:

```
nvm use awesome-version
```

nvm will switch `node` to version `13.6.0`. You can delete an alias by running:

```
nvm unalias awesome-version
```

You can also set a default instance to be used in any shell, by targeting a version to the “default” alias, like so:

```
nvm alias default 12.14.1
```

### Listing Installed Instances

At any time you can check which versions you have installed by running:

```
nvm ls
```

This will display something resembling the following:

![nvm versions list](Images/nvm_1.png)

The entry in green, with an arrow on the left, is the current version in use. Below the installed versions, there’s a list of available aliases. Try executing the following now:

```
nvm use node
nvm ls
```

It will display like so:

![nvm use and versions list](Images/nvm_2.png)

You can also check what is the current version in use with the command:

```
nvm current
```

### Specify a Node Version on a Per-project Basis

Version managers such as [rbenv](https://github.com/rbenv/rbenv) allow you to specify a Ruby version on a per-project basis (by writing that version to a `.ruby-version` file in your current directory). This is kind of possible with nvm in that, if you create a `.nvmrc` file inside a project and specify a version number, you can cd into the project directory and type `nvm use`. nvm will then read the contents of the `.nvmrc` file and use whatever version of Node you specify.

If it’s important to you that this happens automatically, there are a couple of snippets on the project’s home page for you to add to your `.bashrc` or `.zshrc` files to make this happen.

Here’s the ZSH snippet. Place this below your nvm config:

```
autoload -U add-zsh-hook
load-nvmrc() {
  local node_version="$(nvm version)"
  local nvmrc_path="$(nvm_find_nvmrc)"

  if [ -n "$nvmrc_path" ]; then
    local nvmrc_node_version=$(nvm version "$(cat "${nvmrc_path}")")

    if [ "$nvmrc_node_version" = "N/A" ]; then
      nvm install
    elif [ "$nvmrc_node_version" != "$node_version" ]; then
      nvm use
    fi
  elif [ "$node_version" != "$(nvm version default)" ]; then
    echo "Reverting to nvm default version"
    nvm use default
  fi
}
add-zsh-hook chpwd load-nvmrc
load-nvmrc
```

Now, when you change into a directory with a `.nvmrc` file, your shell will automatically change Node version.

![Automatically apply nvm use](Images/nvm_3.png)

### Other nvm Commands

nvm provides a couple of other commands that are more advanced or less commonly used.

You can run a command directly for an installed version without switching the `node` variable:

```
nvm run 13.6.0 --version
```

You can run a command on a sub-shell, targeting a specific version:

```
nvm exec 13.6.0 node --version
```

You can get the path to the Node.js executable of a specific installed version:

```
nvm which 13.6.0
```

This might be useful when configuring a text editor plugin that needs to know where your current version of Node lives.

## Conclusion

nvm is a great tool for any Node.js developer. It enables a concern-free installation and easy switching between different versions, saving time for what really matters.

A thank you note to [Tim Caswell](https://github.com/creationix), the creator of nvm, and also to [Corey Butler](https://github.com/coreybutler) for the nvm for Windows support, and of course to those contributing to these great projects. Your work is greatly appreciated by the Node.js community.

# Chapter 2: A Beginner’s Guide to npm

### by Michael Wanyoike and Peter Dierx

Node.js makes it possible to write applications in JavaScript on the server. It’s built on the [V8 JavaScript runtime](https://v8.dev/) and written in C++—so it’s fast. Originally, it was intended as a server environment for applications, but developers started using it to create tools to aid them in local task automation. Since then, a whole new ecosystem of Node-based tools (such as [Grunt](http://gruntjs.com/), [Gulp](http://gulpjs.com/) and [webpack](https://webpack.js.org)) has evolved to transform the face of front-end development.

To make use of these tools (or packages) in Node.js, we need to be able to install and manage them in a useful way. This is where npm, the Node package manager, comes in. It installs the packages you want to use and provides a useful interface to work with them.

In this guide, we're going to look at the basics of working with npm. We'll show you how to install packages in local and global mode, as well as delete, update and install a certain version of a package. We’ll also show you how to work with `package.json` to manage a project’s dependencies. If you’re more of a video person, why not sign up for SitePoint Premium and watch our free screencast: [What is npm and How Can I Use It?](https://www.sitepoint.com/premium/screencasts/what-is-npm-and-how-can-i-use-it?utm_source=blog&utm_medium=articles)

But before we can start using npm, we first have to install Node.js on our system. Let’s do that now.

## Installing Node.js

Head to the Node.js [download page](https://nodejs.org/en/download/) and grab the version you need. There are Windows and Mac installers available, as well as pre-compiled Linux binaries and source code. For Linux, you can also install Node via the package manager, [as outlined here](https://nodejs.org/en/download/package-manager/).

For this tutorial, we’re going to use v12.15.0\. At the time of writing, this is the current [Long Term Support (LTS) version of Node](https://github.com/nodejs/Release#release-schedule).

#### Using a Version Manager

You might also consider [installing Node using a version manager](http://sitepoint.com/quick-tip-multiple-versions-node-nvm). This negates the permissions issue raised in the next section.

Let’s see where node was installed and check the version:

```
$ which node
/usr/bin/node
$ node --version
v12.15.0
```

To verify that your installation was successful, let’s give Node’s REPL a try:

```
$ node
> console.log('Node is running');
Node is running
> .help
.break    Sometimes you get stuck, this gets you out
.clear    Alias for .break
.editor   Enter editor mode
.exit     Exit the repl
.help     Print this help message
.load     Load JS from a file into the REPL session
.save     Save all evaluated commands in this REPL session to a file

Press ^C to abort current expression, ^D to exit the repl
```

The Node.js installation worked, so we can now focus our attention on npm, which was included in the install:

```
$ which npm
/usr/bin/npm
$ npm --version
6.13.7
```

## Updating npm

npm, which originally stood for Node Package Manager, is a separate project from Node.js. It tends to be updated more frequently. You can check the latest available npm version on this [page](https://www.npmjs.com/package/npm). If you realize you have an older version, you can update as follows.

For Linux and Mac users, use the following command:

```
npm install -g npm@latest
```

For Windows users, the process might be slightly more complicated. This is what it says on the [project's home page](https://github.com/npm/cli/#windows-install-or-upgrade):

> Many improvements for Windows users have been made in npm 3 - you will have a better experience if you run a recent version of npm. To upgrade, either use [Microsoft's upgrade tool](https://github.com/felixrieseberg/npm-windows-upgrade), [download a new version of Node](https://nodejs.org/en/download/), or follow the Windows upgrade instructions in the [Installing/upgrading npm](https://npm.community/t/installing-upgrading-npm/251/2) post.

For most users, the upgrade tool will be the best bet. To use it, you’ll need to open PowerShell as administrator and execute the following command:

```
Set-ExecutionPolicy Unrestricted -Scope CurrentUser -Force
```

This will ensure you can execute scripts on your system. Next, you’ll need to install the [npm-windows-upgrade](https://www.npmjs.com/package/npm-windows-upgrade) tool. After you’ve installed the tool, you need to run it so that it can update npm for you. Do all this within the elevated PowerShell console:

```
npm install --global --production npm-windows-upgrade
npm-windows-upgrade --npm-version latest
```

## Node Packaged Modules

npm can install packages in local or global mode. In local mode, it installs the package in a `node_modules` folder in your parent working directory. This location is owned by the current user.

If you’re not using a [version manager](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/) (which you probably should be), global packages are installed in `{prefix}/lib/node_modules/`, which is owned by root (where `{prefix}` is usually `/usr/` or `/usr/local`). This means you would have to use `sudo` to install packages globally, which could cause permission errors when resolving third-party dependencies, as well as being a security concern.

Let’s change that!

## Changing the Location of Global Packages

Let’s see what output `npm config` gives us:

```
$ npm config list
; cli configs
metrics-registry = "https://registry.npmjs.org/"
scope = ""
user-agent = "npm/6.13.7 node/v12.15.0 linux x64"

; node bin location = /usr/bin/nodejs
; cwd = /home/sitepoint
; HOME = /home/sitepoint
; "npm config ls -l" to show all defaults.
```

This gives us information about our install. For now, it’s important to get the current global location:

```
$ npm config get prefix
/usr
```

This is the prefix we want to change, in order to install global packages in our home directory. To do that create a new directory in your home folder:

```
$ cd ~ && mkdir .node_modules_global
$ npm config set prefix=$HOME/.node_modules_global
```

With this simple configuration change, we’ve altered the location to which global Node packages are installed. This also creates a `.npmrc` file in our home directory:

```
$ npm config get prefix
/home/sitepoint/.node_modules_global
$ cat .npmrc
prefix=/home/sitepoint/.node_modules_global
```

We still have npm installed in a location owned by root. But because we changed our global package location, we can take advantage of that. We need to install npm again, but this time in the new, user-owned location. This will also install the latest version of npm:

```
npm install npm@latest -g
```

Finally, we need to add `.node_modules_global/bin` to our `$PATH` environment variable, so that we can run global packages from the command line. Do this by appending the following line to your `.profile`, `.bash_profile`or `.bashrc` and restarting your terminal:

```
export PATH="$HOME/.node_modules_global/bin:$PATH"
```

Now our `.node_modules_global/bin` will be found first and the correct version of npm will be used:

```
$ which npm
/home/sitepoint/.node_modules_global/bin/npm
$ npm --version
6.13.7
```

#### Version Manager?

As said earlier, you can avoid all of this if you use a Node version manager. Check out this tutorial to find out how: [Installing Multiple Versions of Node.js Using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

## Installing Packages in Global Mode

At the moment, we only have one package installed globally—the npm package itself. So let’s change that and install [UglifyJS](https://www.npmjs.com/package/uglify-js) (a JavaScript minification tool). We use the `--global` flag, but this can be abbreviated to `-g`:

```
$ npm install uglify-js --global
/home/sitepoint/.node_modules_global/bin/uglifyjs -> /home/sitepoint/.node_modules_global/lib/node_modules/uglify-js/bin/uglifyjs
+ uglify-js@3.7.7
added 3 packages from 38 contributors in 0.259s
```

As you can see from the output, additional packages are installed. These are UglifyJS’s dependencies.

## Listing Global Packages

We can list the global packages we've installed with the `npm list` command:

```
$ npm list --global
home/sitepoint/.node_modules_global/lib
├─┬ npm@6.9.0
│ ├── abbrev@1.1.1
│ ├── ansicolors@0.3.2
│ ├── ansistyles@0.1.3
│ ├── aproba@2.0.0
│ ├── archy@1.0.0
....................
└─┬ uglify-js@3.5.3
  ├── commander@2.19.0
  └── source-map@0.6.1
```

The output, however, is rather verbose. We can change that with the `--depth=0` option:

```
$ npm list -g --depth=0
/home/sitepoint/.node_modules_global/lib
├── npm@6.13.7
└── uglify-js@3.7.7
```

That’s better; now we see just the packages we’ve installed along with their version numbers.

Any packages installed globally will become available from the command line. For example, here’s how you would use the Uglify package to minify `example.js` into `example.min.js`:

```
$ uglifyjs example.js -o example.min.js
```

## Installing Packages in Local Mode

When you install packages locally, you normally do so using a `package.json` file. Let’s go ahead and create one:

```
$ mkdir project && cd project

$ npm init
package name: (project)
version: (1.0.0)
description: Demo of package.json
entry point: (index.js)
test command:
git repository:
keywords:
author:
license: (ISC)
```

Press `Return` to accept the defaults, then press it again to confirm your choices. This will create a `package.json` file at the root of the project:

```
{
  "name": "project",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```

#### A Quicker Way

If you want a quicker way to generate a `package.json` file, use `npm init --y`.

The fields are hopefully pretty self-explanatory, with the exception of `main` and `scripts`. The `main` field is the primary entry point to your program, and the `scripts` field lets you specify script commands that are run at various times in the life cycle of your package. We can leave these as they are for now, but if you’d like to find out more, see the [package.json documentation on npm](https://docs.npmjs.com/files/package.json) and this article on [using npm as a build tool](https://www.sitepoint.com/guide-to-npm-as-a-build-tool/).

Now let’s try and install [Underscore](http://underscorejs.org/):

```
$ npm install underscore
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN project@1.0.0 No repository field.

+ underscore@1.9.2
added 1 package from 1 contributor and audited 1 package in 0.412s
found 0 vulnerabilities
```

#### Lockfile

Note that a lockfile is created. We’ll be coming back to this later.

Now if we have a look in `package.json`, we’ll see that a `dependencies` field has been added:

```
{
  ...
  "dependencies": {
    "underscore": "^1.9.2"
  }
}
```

## Managing Dependencies with package.json

As you can see, Underscore v1.9.2 was installed in our project. The caret (`^`) at the front of the version number indicates that when installing, npm will pull in the highest version of the package it can find where only the major version has to match (unless a `package-lock.json` file is present). In our case, that would be anything below v2.0.0\. This method of versioning dependencies (major.minor.patch) is known as **semantic versioning**. You can read more about it here: [Semantic Versioning: Why You Should Be Using it](https://www.sitepoint.com/semantic-versioning-why-you-should-using/).

Also notice that Underscore was saved as a property of the `dependencies` field. This has become the default in the latest version of npm and is used for packages (like Underscore) required for the application to run. It would also be possible to save a package as a `devDependency` by specifying a `--save-dev` flag. `devDependencies` are packages used for development purposes—for example, for running tests or transpiling code.

#### Publication and Warnings

You can also add `private: true` to `package.json` to prevent accidental publication of private repositories, as well as suppressing any warnings generated when running `npm install`.

Far and away the biggest reason for using `package.json` to specify a project’s dependencies is portability. For example, when you clone someone else’s code, all you have to do is run `npm i` in the project root and npm will resolve and fetch all of the necessary packages for you to run the app. We’ll look at this in more detail later.

Before finishing this section, let’s quickly check that Underscore is working. Create a file called `test.js` in the project root and add the following:

```
const _ = require("underscore");
console.log(_.range(5));
```

Run the file using `node test.js` and you should see `[0, 1, 2, 3, 4]` output to the screen.

## Uninstalling Local Packages

npm is a package manager, so it must be able to remove a package. Let’s assume that the current Underscore package is causing us compatibility problems. We can remove the package and install an older version, like so:

```
$ npm uninstall underscore
removed 1 package in 0.386s

$ npm list
project@1.0.0 /home/sitepoint/project
└── (empty)
```

## Installing a Specific Version of a Package

We can now install the Underscore package in the version we want. We do that by using the @ sign to append a version number:

```
$ npm install underscore@1.9.1
+ underscore@1.9.1
added 1 package in 1.574s

$ npm list
project@1.0.0 /home/sitepoint/project
└── underscore@1.9.1
```

## Updating a Package

Let’s check if there’s an update for the Underscore package:

```
$ npm outdated
Package     Current  Wanted  Latest  Location
underscore    1.9.1   1.9.2   1.9.2  project
```

The **Current** column shows us the version that is installed locally. The **Latest** column tells us the latest version of the package. And the **Wanted** column tells us the latest version of the package we can upgrade to without breaking our existing code.

Remember the `package-lock.json` file from earlier? Introduced in npm v5, the purpose of this file is to ensure that the dependencies remain **exactly** the same on all machines the project is installed on. It’s automatically generated for any operations where npm modifies either the `node_modules` folder or the `package.json` file.

You can go ahead and try this out if you like. Delete the `node_modules` folder, then re-run `npm i` (this is short for `npm install`). npm will re-install Underscore v1.9.1, even though we just saw that v1.9.2 is available. This is because we specified version 1.9.1 in the `package-lock.json` file:

```
{
  "name": "project",
  "version": "1.0.0",
  "lockfileVersion": 1,
  "requires": true,
  "dependencies": {
    "underscore": {
      "version": "1.9.1",
      "resolved": "https://registry.npmjs.org/underscore/-/underscore-1.9.1.tgz",
      "integrity": "sha512-5/4etnCkd9c8gwgowi5/om/mYO5ajCaOgdzj/oW+0eQV9WxKBDZw5+ycmKmeaTXjInS/W0BzpGLo2xR2aBwZdg=="
    }
  }
}
```

Prior to the emergence of the `package-lock.json` file, inconsistent package versions proved a big headache for developers. This was normally solved by using an `npm-shrinkwrap.json` file, which had to be manually created.

Now, let’s assume the latest version of Underscore fixed the bug we had earlier and we want to update our package to that version:

```
$ npm update underscore
+ underscore@1.9.2
updated 1 package in 0.236s

$ npm list
project@1.0.0 /home/sitepoint/project
└── underscore@1.9.2
```

#### Dependency

For this to work, Underscore has to be listed as a dependency in `package.json`. We can also execute `npm update` if we have many outdated modules we want to update.

## Searching for Packages

We’ve used the `mkdir` command a couple of times in this tutorial. Is there a Node package that has this functionality? Let’s use `npm search`:

```
$ npm search mkdir
NAME                      | DESCRIPTION          | AUTHOR          | DATE
mkdir                     | Directory creation…  | =joehewitt      | 2012-04-17
fs-extra                  | fs-extra contains…   | =jprichardson…  | 2019-06-28
mkdirp                    | Recursively mkdir,…  | =isaacs…        | 2020-01-24
make-dir                  | Make a directory…    | =sindresorhus   | 2019-04-01
...
```

There’s ([mkdirp](https://www.npmjs.com/package/mkdirp)). Let’s install it:

```
$ npm install mkdirp
+ mkdirp@1.0.3
added 1 package and audited 2 packages in 0.384s
```

Now create a `mkdir.js` fie and copy–paste this code:

```
const mkdirp = require('mkdirp');

const made = mkdirp.sync('/tmp/foo/bar/baz');
console.log(`made directories, starting with ${made}`);
```

Next, run it from the terminal:

```
$ node mkdir.js
made directories, starting with /tmp/foo
```

## Re-installing Project Dependencies

Let’s first install one more package:

```
$ npm install request
+ request@2.88.0
added 48 packages from 59 contributors and audited 65 packages in 2.73s
found 0 vulnerabilities
```

Check the `package.json`:

```
"dependencies": {
  "mkdirp": "^1.0.3",
  "request": "^2.88.0",
  "underscore": "^1.9.2"
},
```

Note the dependencies list got updated automatically. If you wanted to install a package without saving it in `package.json`, just use the `--no-save` argument.

Let’s assume you’ve cloned your project source code to a another machine and we want to install the dependencies. Let’s delete the `node_modules` folder first, then execute `npm install`:

```
$ rm -R node_modules
$ npm list --depth=0
project@1.0.0 /home/sitepoint/project
├── UNMET DEPENDENCY mkdirp@1.0.3
├─┬ UNMET DEPENDENCY request@2.88.0
  ...
└── UNMET DEPENDENCY underscore@1.9.2

npm ERR! missing: mkdirp@1.0.3, required by project@1.0.0
npm ERR! missing: request@2.88.0, required by project@1.0.0
npm ERR! missing: underscore@1.9.2, required by project@1.0.0
...

$ npm install
added 50 packages from 60 contributors and audited 65 packages in 1.051s
found 0 vulnerabilities
```

If you look at your `node_modules` folder, you’ll see that it gets recreated again. This way, you can easily share your code with others without bloating your project and source repositories with dependencies.

## Managing the Cache

When npm installs a package, it keeps a copy, so the next time you want to install that package, it doesn’t need to hit the network. The copies are cached in the `.npm` directory in your home path:

```
$ ls ~/.npm
anonymous-cli-metrics.json  _cacache  index-v5  _locks  _logs  node-sass
```

This directory will get cluttered with old packages over time, so it’s useful to clean it up occasionally:

```
$ npm cache clean --force
```

You can also purge all `node_module` folders from your workspace if you have multiple node projects on your system you want to clean up:

```
find . -name "node_modules" -type d -exec rm -rf '{}' +
```

## Audit

Have you noticed all of those `found 0 vulnerabilities` scattered throughout the CLI output? The reason for this is that a new feature was introduced in npm that allows developers to scan the dependencies for known security vulnerabilities.

Let’s try out this feature by installing an old version of `express`:

```
$ npm install express@4.8.0

express@4.8.0
added 36 packages from 24 contributors and audited 123 packages in 2.224s
found 21 vulnerabilities (8 low, 9 moderate, 4 high)
  run `npm audit fix` to fix them, or `npm audit` for details
```

As soon as we finish installing, we get a quick report that multiple vulnerabilities have been found. You can run the command `npm audit` to view more details:

```
$ npm audit

 === npm audit security report ===

# Run  npm install express@4.17.1  to resolve 21 vulnerabilities
┌───────────────┬──────────────────────────────────────────────────────────────┐
│ High          │ Regular Expression Denial of Service                         │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ Package       │ negotiator                                                   │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ Dependency of │ express                                                      │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ Path          │ express > accepts > negotiator                               │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ More info     │ https://nodesecurity.io/advisories/106                       │
└───────────────┴──────────────────────────────────────────────────────────────┘

┌───────────────┬──────────────────────────────────────────────────────────────┐
│ Moderate      │ Timing Attack                                                │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ Package       │ cookie-signature                                             │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ Dependency of │ express                                                      │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ Path          │ express > cookie-signature                                   │
├───────────────┼──────────────────────────────────────────────────────────────┤
│ More info     │ https://nodesecurity.io/advisories/134                       │
└───────────────┴──────────────────────────────────────────────────────────────┘
```

You’ll get a detailed list of packages that have vulnerabilities. If you look at the `Path` field, it shows the dependency path. For example, the Path `express > accepts > negotiator` means Express depends on the `Accepts` package. The `Accepts` package depends on the the `negotiator` package, which contains the vulnerability.

There are two ways of fixing all these problems. We can either execute the command `npm install express@4.17.1` as suggested, or run `npm audit fix`. Let’s do the latter:

```
$ npm audit fix

+ express@4.17.1
added 20 packages from 14 contributors, removed 7 packages and updated 29 packages in 1.382s
fixed 21 of 21 vulnerabilities in 122 scanned packages
```

The command `npm audit fix` automatically installs any compatible updates to vulnerable dependencies. While this might seem like magic, do note that vulnerabilities can’t always be fixed automatically. This could happen if you’re using a package that’s undergone a major change which could break your current project if updated. For situations such as this, you’ll have to review your code and manually apply the fix.

You can also run `npm audit fix --force` if you don’t mind upgrading packages with breaking changes. After you’ve executed the command, run `npm audit` to ensure that all vulnerabilities have been resolved.

## Aliases

As you may have noticed, there are multiple ways of running npm commands. Here’s a brief list of some of the commonly used npm aliases:

*   `npm i <package>`: install local package
*   `npm i -g <package>`: install global package
*   `npm un <package>`: uninstall local package
*   `npm up`: npm update packages
*   `npm t`: run tests
*   `npm ls`: list installed modules
*   `npm ll` or `npm la`: print additional package information while listing modules

You can also install multiple packages at once like this:

```
$ npm i express momemt lodash mongoose body-parser webpack
```

If you want to view all the common npm commands, just execute `npm help` for the full list. You can also learn more in our article [10 Tips and Tricks That Will Make You an npm Ninja](https://www.sitepoint.com/10-npm-tips-and-tricks/).

## npx

You might also hear talk of npx on your travels. Don't confuse this with npm. As we’ve learned, npm is a tool for *managing* your packages, whereas npx is a tool for *executing* packages. It comes bundled with npm version 5.2+.

A typical use of npx is for executing one-off commands. For example, imagine you wanted to spin up a simple HTTP server. You *could* install the [http-server package](https://www.npmjs.com/package/http-server) globally on your system, which is great if you’ll be using `http-server` on a regular basis. But if you just want to test the package, or would like to keep your globally installed modules to a minimum, you can change into the directory where you’d like to run it, then execute the following command:

```
npx http-server
```

And this will spin up the server without installing anything globally.

You can [read more about npx here](https://blog.npmjs.org/post/162869356040/introducing-npx-an-npm-package-runner).

## Conclusion

In this tutorial, we’ve covered the basics of working with npm. We’ve demonstrated how to install Node.js from the project’s download page, how to alter the location of global packages (so we can avoid using `sudo`), and how to install packages in local and global mode. We also covered deleting, updating and installing a certain version of a package, as well as managing a project’s dependencies.

With every new release, npm is making huge strides into the world of front-end development. [According to its co-founder](http://frontendhappyhour.com/episodes/npm-install-beer-save-in-mouth/), its user base is changing and most of those using it are not using it to write Node at all. Rather, it’s becoming a tool that people use to put JavaScript together on the front end (seriously, you can use it to install just about anything) and one which is becoming an integral part of writing modern JavaScript.

Are you using npm in your projects? If not, now might be a good time to start.

# Chapter 3: Create New Express.js Apps in Minutes with Express Generator

### by Paul Suave and Nilson Jacques

[Express.js](https://expressjs.com/) is a Node.js web framework that has gained immense popularity due to its simplicity. It has easy-to-use routing and simple support for view engines, putting it far ahead of the basic Node HTTP server.

However, starting a new Express application requires a certain amount of boilerplate code: starting a new server instance, configuring a view engine, and setting up error handling.

Although there are various starter projects and boilerplates available, Express has its own command-line tool that makes it easy to start new apps, called the [express-generator](https://expressjs.com/en/starter/generator.html).

## What is Express?

Express has a lot of features built in, and a lot more features you can get from other packages that integrate seamlessly, but there are three main things it does for you out of the box:

1.  **Routing**. This is how `/home` `/blog` and `/about` all give you different pages. Express makes it easy for you to modularize this code by allowing you to put different routes in different files.
2.  **Middleware**. If you’re new to the term, basically middleware is “software glue”. It accesses requests before your routes get them, allowing them to handle hard-to-do stuff like cookie parsing, file uploads, errors, and more.
3.  **Views**. Views are how HTML pages are rendered with custom content. You pass in the data you want to be rendered and Express will render it with your given view engine.

## Getting Started

The first thing you’ll need is to get Node and npm installed on your machine. To do this, either head to [the official Node download page](https://nodejs.org/en/download/) and grab the correct binaries for your system, or use a version manager such as nvm. We cover installing Node using a version manager in our quick tip, “[Install Multiple Versions of Node.js Using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/)”.

Starting a new project with the Express generator is as simple as running a few commands:

```
npm install express-generator -g
```

This installs the Express generator as a global package, allowing you to run the `express` command in your terminal:

```
express myapp
```

This creates a new Express project called `myapp`, which is then placed inside of the `myapp` directory:

```
cd myapp
```

If you’re unfamiliar with terminal commands, this one puts you inside of the `myapp` directory:

```
npm install
```

If you’re unfamiliar with npm, it’s the [default Node.js package manager](https://www.sitepoint.com/beginners-guide-node-package-manager/). Running `npm install` installs all dependencies for the project. By default, the `express-generator` includes several packages that are commonly used with an Express server.

### Options

The generator CLI takes half a dozen [arguments](https://expressjs.com/en/starter/generator.html), but the two most useful ones are the following:

*   **-v <ejs|hbs|hjs|jade|pug|twig|vash>**. This lets you select a view engine to install. The default is `jade`. Although this still works, it has been deprecated and you should always specify an alternative engine.
*   **-c <less|stylus|compass|sass>**. By default, the generator creates a very basic CSS file for you, but selecting a CSS engine will configure your new app with middleware to compile any of the above options.

Now that we’ve got our project set up and dependencies installed, we can start the new server by running the following:

```
npm start
```

Then browse to [http://localhost:3000](http://localhost:3000) in your browser.

## Application Structure

The generated Express application starts off with four folders.

### `bin`

The `bin` folder contains the executable file that starts your app. It starts the server (on port 3000, if no alternative is supplied) and sets up some basic error handling. You don’t really need to worry about this file, because `npm start` will run it for you.

### `public`

The `public` folder is one of the important ones: ​*everything​* in this folder is accessible to people connecting to your application. In this folder, you’ll put JavaScript, CSS, images, and other assets that people need when they load your website.

### `routes`

The `routes` folder is where you’ll put your router files. The generator creates two files, `index.js` and `users.js`, which serve as examples of how to separate out your application’s route configuration.

Usually, you’ll have a different file here for each major route on your website. So you might have files called `blog.js`, `home.js`, and/or `about.js` in this folder.

### `views`

The `views` folder is where you have the files used by your templating engine. The generator will configure Express to look in here for a matching view when you call the `render` method.

Outside of these folders, there’s one file that you should know well.

## `app.js`

The `app.js` file is special, because it sets up your Express application and glues all of the different parts together. Let’s walk through what it does. Here’s how the file starts:

```
var createError = require('http-errors');
var express = require('express');
var path = require('path');
var cookieParser = require('cookie-parser');
var logger = require('morgan');
```

These first six lines of the file are required. If you’re new to Node, be sure to read “[Understanding module.exports and exports in Node.js](https://www.sitepoint.com/understanding-module-exports-exports-node-js/)”.

```
var indexRouter = require('./routes/index');
var usersRouter = require('./routes/users');
```

The next two lines of code `require` the different route files that the Express generator sets up by default: `routes` and `users`.

```
var app = express();
```

After that, we create a new app by calling `express()`. The app variable contains all of the settings and routes for your application. This object glues together your application.

```
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'jade');
```

Once the app instance is created, the templating engine is set up for rendering views. This is where you’d change the path to your view files if necessary.

After this, you’ll see Express being configured to use middleware. The generator installs several common pieces of middleware that you’re likely to use in a web application:

```
app.use(logger('dev'));
app.use(express.json());
app.use(express.urlencoded({ extended: false }));
app.use(cookieParser());
app.use(express.static(path.join(__dirname, 'public')));
```

*   **logger**. When you run your app, you might notice that all the routes that are requested are logged to the console. If you want to disable this, you can just comment out this middleware.
*   **express.json**. You might notice that there are two lines for parsing the body of incoming HTTP requests. The first line handles when JSON is sent via a POST request and it puts this data in `request.body`.
*   **express.urlencoded**. The second line parses query string data in the URL (e.g. `/profile?id=5`) and puts this in `request.query`.
*   **cookieParser**. This takes all the cookies the client sends and puts them in `request.cookies`. It also allows you to modify them before sending them back to the client, by changing `response.cookies`.
*   **express.static**. This middleware serves static assets from your `public` folder. If you wanted to rename or move the public folder, you can change the path here.

Next up is the routing:

```
app.use('/', indexRouter);
app.use('/users', usersRouter);
```

Here, the example route files that were required are attached to our app. If you need to add additional routes, you’d do it here.

All the code after this is used for error handling. You usually won’t have to modify this code unless you want to change the way Express handles errors. By default, it’s set up to show the error that occurred in the route when you’re in development mode.

## Bootstrapping a New Project

Let’s apply what we’ve learned so far to kick-start a basic Express.js application.

Assuming you’ve already installed `express-generator` as a global module, run the following command to create a new skeleton project:

```
express -v hbs signup-form
```

As I mentioned earlier, it’s a good idea to opt for something other than the default (Jade) templating library. Here I’ve gone with [Handlebars.js](https://handlebarsjs.com/), as I find the mustache-like syntax easy to read and work with.

Once the generator has run, switch into the newly created folder and install the dependencies:

```
cd signup-form
npm i
```

At this point, you may notice several warnings about package vulnerabilities. Let’s update the version of Handlebars.js to fix those:

```
npm install hbs@4.1.0
```

Now that the project dependencies are installed and updated, let’s customize some of the boilerplate view templates.

The generator creates a layout template which is used to render all the markup that’s shared between views. Open up `views/layout.hbs` and replace the content with the following:

```
<!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <meta name="description" content="">
  <meta name="author" content="">

  <title>{{title}}</title>

  <!-- Bootstrap core CSS -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css"
    integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">

  <!-- Custom styles for this template -->
  <link href="/stylesheets/style.css" rel="stylesheet">
</head>

<body>
  {{{body}}}
</body>

</html>
```

The markup here is adapted from an [example](https://getbootstrap.com/docs/4.1/examples/sign-in/) shown on the [Bootstrap website](https://getbootstrap.com/). We also need to add some custom styles, so open up `public/stylesheets/style.css` and paste in the following:

```
html,
body {
  height: 100%;
}

body {
  display: -ms-flexbox;
  display: flex;
  -ms-flex-align: center;
  align-items: center;
  padding-top: 40px;
  padding-bottom: 40px;
  background-color: #f5f5f5;
}

.full-width {
  width: 100%;
  padding: 15px;
  margin: auto;
}

.form-signin {
  max-width: 330px;
}
.form-signin .checkbox {
  font-weight: 400;
}
.form-signin .form-control {
  position: relative;
  box-sizing: border-box;
  height: auto;
  padding: 10px;
  font-size: 16px;
}
.form-signin .form-control:focus {
  z-index: 2;
}
.form-signin input {
  border-radius: 0;
  margin-bottom: -1px;
}
.form-signin input:first-of-type {
  border-top-left-radius: 0.25rem;
  border-top-right-radius: 0.25rem;
}
.form-signin input:last-of-type {
  border-bottom-left-radius: 0.25rem;
  border-bottom-right-radius: 0.25rem;
  margin-bottom: 10px;
}
```

Now that we’ve customized the layout, let’s add the markup for the home page. Open `views/index.hbs` and replace the contents with the following:

```
<form action="/subscribe" method="POST" class="form-signin full-width text-center">
  <h1 class="h3 mb-3 font-weight-normal">Join the mailing list</h1>
  <label for="name" class="sr-only">First name</label>
  <input type="text" name="name" class="form-control" placeholder="First name" required autofocus>
  <label for="email" class="sr-only">Email</label>
  <input type="email" name="email" class="form-control" placeholder="Your email" required>
  <label for="emailConfirmation" class="sr-only">Email (confirm)</label>
  <input type="email" name="emailConfirmation" class="form-control" placeholder="Your email (confirm)" required>
  <button class="btn btn-lg btn-primary btn-block" type="submit">Subscribe</button>
  <p class="mt-5 mb-3 text-muted">&copy; 2020</p>
</form>
```

This will display a newsletter signup form on our home page.

Let’s add a route our form can be submitted to, where we can access the form data and do something with it. Open up the file `routes/index.js` and add the following route beneath the home-page route:

```
router.post("/subscribe", function(req, res, next) {
  const { name, email } = req.body;

  // 1\. Validate the user data
  // 2\. Subscribe the user to the mailing list
  // 3\. Send a confirmation email

  res.render("subscribed", {
    title: "You are subscribed",
    name,
    email
  });
});
```

In the route handler, we’ve extracted the form data from the request object. After processing the signup (shown as pseudo-code), we pass the data through to our `subscribed` view.

#### Working with Forms in Node

If you want to learn more about working with forms in Node, read “[Forms, File Uploads and Security with Node.js and Express](https://www.sitepoint.com/forms-file-uploads-security-node-express/)”.

Let’s create that now, by opening a new file, `views/subscribed.hbs`, and adding the following markup:

```
<div class="full-width text-center">
  <h1 class="display-3">Thank You, {{name}}!</h1>
  <p class="lead"><strong>Please check your email</strong> to confirm your subscription to our newsletter.</p>
  <hr>
  <p>
      Having trouble? <a href="">Contact us</a>
  </p>
  <p class="lead">
      <a class="btn btn-primary btn-sm" href="/" role="button">Continue to homepage</a>
  </p>
</div>
```

To give our new site a try, fire it up by running `npm run start` in the project folder, and visit [http://localhost:3000](http://localhost:3000).

And here’s [the demo running on CodeSandbox](https://codesandbox.io/embed/cranky-feistel-6u6po).

## A Useful Tool

Hopefully you now have a clear idea of how the express-generator tool can save you time writing repetitive boilerplate when starting new Express-based projects.

By providing a sensible default file structure, and installing and wiring up commonly needed middleware, the generator creates a solid foundation for new applications with just a couple of commands.

# Chapter 4: An Introduction to AdonisJs, a Laravel-like Node.js Framework

### by Nilson Jacques

Developers looking to start building Node.js web apps often run into Express early on. While Express is undoubtedly one of the most popular HTTP application framework for Node, it’s quite minimal, leaving it down to the developer to piece together the functionality they want from third-party packages.

[AdonisJs](https://adonisjs.com/) is an MVC framework for Node that aims to provide all the main functionality you need to build a modern web application. It’s heavily inspired by the [Laravel PHP framework](https://laravel.com/), borrowing much of the syntax and layout.

This guide aims to take a high-level overview of the features offered by Adonis, to help you decide whether it’s for you. Throughout the guide, I’ll be comparing the functionality to that offered by Laravel, so PHP devs will have a good reference point.

#### Adonis Versions

At the time of writing, Adonis v5 is in preview but still incomplete, so this article will look at v4.

## Basics

Let’s start by taking a look at the tools Adonis provides for creating and maintaining projects.

### CLI Tool

The AdonisJs CLI is a tool that is broadly equivalent to Laravel’s artisan command. It’s installed as a global Node module:

```
 npm i -g @adonisjs/cli
```

The CLI makes it easy to create new projects:

```
 adonis new my-new-project
```

It also makes it easy to serve them:

```
 adonis serve
 # or, with file watching
 adonis serve --dev
```

Like artisan, when run within an Adonis project directory it, can be used to create and run database migrations, scaffold models and controllers, and run custom command-line jobs.

### REPL

You can also use the CLI tool to boot into a command-line environment similar to [tinker](https://laravel.com/docs/6.x/artisan#tinker). Inside this environment you have access to your application’s code plus all the framework libraries and helpers.

```
adonis repl
```

The [repl](https://adonisjs.com/docs/4.0/database-basics#_what_is_repl) (read–eval–print loop) is really useful for debugging and maintenance tasks—for example, to create new users or reset passwords while in development.

### File Structure

The [file structure of a new AdonisJs project](https://adonisjs.com/docs/4.1/folder-structure) bears more than a passing similarity to that of a Laravel project:

```
├── ace
├── app
│   ├── Controllers
│   │   └── Http
│   ├── Middleware
│   └── Models
│       └── Traits
├── config
├── database
│   └── migrations
├── public
├── resources
│   └── views
├── server.js
└── start
    ├── app.js
    ├── kernel.js
    └── routes.js
```

You’ll find an `app` folder, grouping together the controllers (by type), models, and middleware; a `config` folder, with files for general application configuration, authentication, sessions, and database configuration (among others); a `database` folder, for migrations, factories, and seeders; and a `resource` folder, for your view templates.

An important deviation from the familiar is the `start` folder, which in Adonis holds the files responsible for configuring service providers, middleware, and routing.

## HTTP

### Defining Routes

A core component of any web application framework is routing, and the Adonis developers have opted to closely mirror Laravel’s syntax for specifying HTTP routes.

An [application’s routes](https://adonisjs.com/docs/4.1/routing) are defined in `start/routes.js` and will be familiar to anyone coming from a Laravel background:

```
Route.get('posts', () => {...});
Route.post('posts', () => {...});
Route.put('posts/:id', () => {...});
Route.delete('posts/:id', () => {...});
```

As you can see from the last two routes, it’s pretty easy to define routes with parameters:

```
Route.get('posts/:id', ({ params }) => {
  return `Post ${params.id}`
});
```

Like Laravel, AdonisJs also provides a handy shortcut for defining a bunch of CRUD routes for a resource (that is, RESTful routes):

```
Route.resource('posts', 'PostController');
```

### Middleware

Adonis’ way of dealing with middleware should also be very familiar to Laravel devs. [Middleware](https://adonisjs.com/docs/4.1/middleware) is registered within the `start/kernel.js` file, and is done in one of three different ways.

**Server middleware:**

```
const serverMiddleware = [
  'Adonis/Middleware/Static',
  'Adonis/Middleware/Cors',
]
```

Server middleware is run for every incoming request, regardless of whether it matches a route or not.

**Global middleware:**

```
const globalMiddleware = [
  'Adonis/Middleware/BodyParser',
]
```

Global middleware is run for every request that matches a defined route in your application.

**Named middleware:**

```
const namedMiddleware = {
  auth: 'Adonis/Middleware/Auth',
}
```

Once registered, named middleware can be attached to a route, or group of routes:

```
Route.get('admin', 'AdminController.index').middleware(['auth'])
```

### Controllers

Creating controllers in Adonis is a breeze with the CLI. There’s an option for specifying the type, to create either an HTTP or WebSocket controller:

```
adonis make:controller Posts --type http
```

There’s also an option to create a resourceful controller, which has stub methods for the CRUD actions. These methods correspond with the routes created by the `Route.resource()` we saw earlier, helping to speed up the creation of CRUD applications.

## Database

Adonis has database support for MySQL/MariaDB, MSSQL, Oracle, PostgreSQL, and SQLite3\. The driver and connection settings are pulled in from environment variables, or the `.env` file if working locally.

### Query Builder

The framework comes with a [query builder](https://adonisjs.com/docs/4.1/query-builder) that works in a similar way to the one that comes with Laravel. It provides you with a fairly intuitive API for building up complex queries without having to write any SQL:

```
const adults = await Database
  .from('users')
  .where('age', '>', 18)
  .first();
```

Adonis (or rather [Knex.js](https://knexjs.org/), which Adonis uses under the hood), translates this into the correct SQL dialect for your chosen database engine.

### Lucid ORM

Even with a query builder, writing all the code to fetch and update data for your app would quickly become verbose and repetitive. Thankfully, AdonisJs provides the [Lucid ORM](https://adonisjs.com/docs/4.1/lucid) (object-relational mapper) to make our jobs a little easier.

Lucid, like Laravel’s Eloquent, is based on the active record pattern, and the Adonis team have clearly put in a lot of effort to try to achieve feature parity between the two libraries.

*   **Relationships**: you can define `hasOne`, `hasMany`, `belongsTo`, `belongsToMany`, and `manyThrough` relationships easily with the built-in methods.
*   **Traits**: you can define “traits” to share functionality between different models without duplicating code.
*   **Hooks**: you can attach callbacks to model lifecycle events such as `beforeCreate` and `beforeSave` in order to modify records.
*   **Mutators**: you can define getters and setters for model attributes to mutate their values.

As mentioned earlier, the CLI can be used to create new models:

```
adonis make:model Post
```

This will generate the following file:

**app/Models/Post.js:**

```
'use strict'

const Model = use('Model')

class Post extends Model {
}

module.exports = Post
```

Passing the `--migration` flag to the command will also generate a skeleton migration file to create the model’s corresponding DB table.

Let’s look at some code examples to get a feel for the syntax.

**Creating new records:**

```
const post = new Post();

post.name = 'My first blog post';
post.content = 'Blah blah blah...';

await post.save();
```

There’s also a convenience method for creating and returning a new model from a data object:

```
const post = await Post.create({
  name: 'My first blog post',
  content: 'Blah blah blah...'
});
```

Other common Eloquent convenience methods are also available, such as `findOrFail` and `findOrCreate`.

**Retrieving records:**

```
// Return all records
const posts = Post.all();

// Find by ID
const post = Post.find(1);
```

**Using the query builder with models:**

```
const adults = await User
  .query()
  .where('age', '>', 18)
  .fetch();
```

### Migrations

Another core part of Laravel’s database-related functionality is the migrations system. If you’re not familiar with it, a **migration** is a set of schema changes, defined in code. A migration can then be run against your application’s database in different environments (such as development, staging, and production) ensuring that all copies of the database are updated when your code is deployed.

Adonis’ way of doing things will be familiar to a Laravel developer. [Migrations](https://adonisjs.com/docs/4.1/migrations) are created via the CLI:

```
adonis make:migration posts
# ✔ create  database/migrations/1502691651527_posts_schema.js
```

They’re run from there too:

```
adonis migration:run
# migrate: 1502691651527_posts_schema.js
# Database migrated successfully in 117 ms
```

As well as running migrations, there are commands to roll back the last set, or completely roll back and reapply all migrations from scratch, [among others](https://adonisjs.com/docs/4.1/migrations#_migration_commands).

Let’s take a look at how a migration is defined:

```
// database/migrations/1502691651527_posts_schema.js

'use strict'

const Schema = use('Schema')

class PostsSchema extends Schema {
  up () {
    this.create('users', (table) => {
      table.increments()
      table.string('title').notNullable().unique()
      table.text('content').notNullable()
      table.integer('comment_count').notNullable()
      table.timestamps()
    })
  }

  down () {
    this.drop('posts')
  }
}

module.exports = PostsSchema
```

Each migration has both an `up()` and `down()` method, run on migrate and rollback respectively. Within the `up()` method, changes to the table schema are declared with chainable method calls to define/alter the columns.

## Views

In addition to creating REST APIs, Adonis also aims to make server-rendered apps painless. To this end, it includes the [Edge template engine](https://edge.adonisjs.com/).

### Edge templates

The view templates are files with an `.edge` extension, and can contain a mixture of HTML (including JS and CSS) and Edge’s own template tags.

The syntax is very similar to that used by Laravel’s Blade. Data is output via double curly braces (for example, `{{ my_variable }}`). Tags, which are used for things like conditional rendering and iteration, begin with an `@` symbol.

A typical template might look something like this:

**resources/views/list.edge:**

```
@layout('main')

@section('content')
<div>
  <ul>
  @each(item in list)
  <li>
      <a href="{{ item.url }}">{{ item.text }}</a>
    </li>
  @endeach
  </ul>
</div>
@endsection
```

Here there are several Edge tags being used:

*   `@layout`: specifies that the current template will be rendered into the named layout (for example, “main”)
*   `@section` and `@endsection`: specifies that the contents of this block will be inserted into the named section of the layout (for example, “content”)
*   `@each` and `@endeach`: specifies that the block should be repeated for each item in a collection

Partials are also supported, so you can extract common pieces of markup to their own files and include them wherever they’re needed using the `@include` tag.

Like Blade, Edge also provides a “component” syntax, which allows you to treat partials as if they were web components, with their own isolated variable scope:

```
@component('edit-post-modal', { title: 'Add a new post' })
  <form>
    ...
  </form>
@endcomponent
```

In the above example, the form markup would be rendered inside a modal template, which has access to any data passed in (such as the title) but not variables from the parent template.

### Global functions

[Globals](https://adonisjs.com/docs/4.1/views#_globals) are helper functions you can access from within your Edge templates. You can define your own, but Adonis ships with a bunch of predefined ones—both framework specific (such as route url generator) and general helpers (such as a camel case convertor).

To use them, you just call them from within curly braces.

**Generating a route URL:**

```
<a href="{{ route('post', { id: 1 }) }}">
  View post
</a>
```

**Generating the path to a file in the `public` folder:**

```
<img src="{{ assetsUrl('images/logo.png') }}" />
```

Both Blade and Edge also allow you to define custom template tags to help make your views cleaner and more readable.

## Advanced

There are two more advanced topics I wanted to touch on before wrapping up: the way Adonis handles dependency injection (DI), and authentication.

### IoC Container

Laravel has a sophisticated DI system, allowing you to inject dependencies into your controllers and other classes by type-hinting them in the constructor.

Adonis also has an [Inversion of Control (IoC) container](https://adonisjs.com/docs/4.1/ioc-container) that can be set up to resolve your project’s dependencies, while allowing them to be easily swapped out for fakes/mocks during testing.

Getting the dependencies into your code is a little different that in Laravel. You have to fetch them from the container with the globally available `use()` helper:

```
const redis = use('My/Redis')
```

It’s worth mentioning that the next version of Adonis (v5 at the time of writing) plans to replace this with ESM imports:

```
import Route from  '@ioc:Adonis/Core/Route'
```

### Authentication

When it comes to authentication, Laravel makes it very easy to implement. It comes with a session-based auth system out of the box, and JWT and OAuth2 systems are available via downloadable packages.

[Adonis aims to cover all the bases here](https://adonisjs.com/docs/4.1/authentication), shipping with authentication schemes for session, basic auth, JWT, and personal API tokens.

The framework also provides middleware for authenticating routes and helpers for retrieving the currently logged-in user that will be familiar to Laravel developers. Unlike Laravel, however, there’s no command to scaffold out the views and controllers to quickly get a working auth system.

## Adonis Pros

*   closely follows Laravel in terms of features and API design
*   takes a more batteries-included approach than frameworks like Express
*   documentation has plenty of examples

## Adonis Cons

*   some Laravel features are noticeable by their absence, such as job queues
*   the documentation is a little sparse in places, and sometimes relies on videos in place of written guides

## Verdict

Overall, the Adonis team has done a great job at creating a Node.js framework that’s as easy to use and (almost) as fully featured as Laravel.

Those getting started with Node development will find everything they need to start building applications out of the box, with enough documentation to get up and running quickly.

Laravel developers transitioning from PHP (or dipping their toes in Node) will feel especially at home, and should find enough similarity between the two frameworks to be productive fairly quickly.

Unless you have some experience of Node.js development and want to build up a specific back-end stack from your favorite packages, it’s hard not to recommend Adonis.

# Chapter 5: Top 5 Developer-friendly Node.js API Frameworks

### by Michael Wanyoike

In the past, we used to build monolithic applications that handled views, business logic and data management in one single codebase. This architecture created a number of problems that affected an application’s stability, performance and maintainability.

Nowadays, many web applications favor a more modular approach. This typically involves creating a public-facing API that exposes endpoints for interacting with an application’s data. In this guide, we’ll take a quick look what an API is, as well as five developer-friendly frameworks we can use to build them in Node.js.

## What is an API?

In simple English, an API (short for Application Programming Interface) is a server application that responds to requests from client applications such as browsers and mobile apps. If you’ve had to fetch data from another source on the Internet (such as Twitter or GitHub), chances are you’ve used one already.

One big advantage of this approach is you build your back-end server API once, then you can connect it to different types of client interfaces—such as desktop, web, mobile or console apps. Having an API ensures data is consistent in all the front-facing apps that have been built for an organization.

An API provides important back-end functions such as:

*   CRUD operations
*   data validation and transformation
*   authentication
*   access control
*   business logic
*   transactional email
*   task scheduling
*   event handling

Building an API server in Node is quite simple. If you need to set one up quickly to test your front-end code, you can install [JSON server](https://www.npmjs.com/package/json-server#getting-started) to quickly prototype your back end. If you’ve started building your own API and you don’t have a front end yet, you can use the following tools to test your endpoints:

*   [Postman](https://www.getpostman.com/)
*   [Insomnia](https://insomnia.rest/)

These tools allow you to perform both REST and GraphQL queries. We’ll get into them some more later on.

To build your own API, you’ll need a framework that will provide you with the necessary libraries and tools to create your back-end server. I’ve ordered the following list based on how user-friendly the framework is. The last one is the least technical to use.

## 1\. Express

![express](Images/express.png)

If you’re a Node.js beginner, this is the framework you should start with. You can [install Express](https://expressjs.com/en/starter/installing.html) as a package dependency with the command `npm install express`. Alternatively, you can use the [express-generator](https://expressjs.com/en/starter/generator.html) command-line tool to quickly spin up a starter Express project. We also have a [tutorial on using this library](https://www.sitepoint.com/create-new-express-js-apps-with-express-generator/).

Let’s look at what a simple REST API for managing users might look like in Express.

First, create a new project then install Express:

```
mkdir express-api
cd express-api
npm init -y
npm i express
```

Next, create an `server.js` file and add the following content:

```
let data = [
  { id: 1, firstName: 'Michael', lastName: 'Wanyoike' },
  { id: 2, firstName: 'James', lastName: 'Hibbard' },
];

const express = require('express');
const bodyParser = require('body-parser');
const app = express().use(bodyParser.json());

// GET all users
app.get('/users', (req, res) => { res.json(data); });

// GET a user
app.get('/users/:id', (req, res) => {
  const id = Number(req.params.id);
  const user = data.find(user => user.id === id);
  res.json(user ? user : { message: 'Not found' });
});

// ADD a user
app.post('/users', (req, res) => {
  const user = req.body;
  data.push(user);
  res.json(data);
});

// UPDATE a user
app.put('/users/:id', (req, res) => {
  const id = Number(req.params.id);
  const updatedUser = req.body;
  data = data.map(user => user.id === id ? updatedUser : user);
  res.json(data);
});

// DELETE a user
app.delete('/users/:id', (req, res) => {
  const id = Number(req.params.id);
  data = data.filter(user => user.id !== id);
  res.json(data);
});

app.listen(3000, () => { console.log('Server listening at port 3000'); });
```

Save this code, then start the server using `node server.js`. It’s now running on `http://localhost:3000`.

### Interacting with the API Using Postman

We can test that our API does what it should using [Postman](https://www.getpostman.com/), an API testing environment. Download the correct version for your system, then follow the [instructions to get it installed](https://learning.getpostman.com/docs/postman/launching-postman/installation-and-updates/).

We can start by sending a GET request to `http://localhost:3000/users` to list all of our users.

You should see the following response:

```
[
  {
    "id": 1,
    "firstName": "Michael",
    "lastName": "Wanyoike"
  },
  {
    "id": 2,
    "firstName": "James",
    "lastName": "Hibbard"
  }
]
```

![Postman making a GET request to the "users" endpoint](Images/postman.png)

After that, feel free to experiment. For example, if you want to create a user, send a POST request to `http://localhost:3000/users`, along with a JSON payload containing the user’s details. You can do this by clicking the **Body** tab, then selecting the **raw** radio button and **JSON** from the dropdown.

If you’d like a more in-depth tutorial on using Postman to interact with an API, I recommend [Making API Requests with Postman or cURL](https://www.taniarascia.com/making-api-requests-postman-curl/).

### Taking it Further

With Express, you can connect to any database by installing an [adapter](https://expressjs.com/en/guide/database-integration.html) that will allow you to connect and execute queries. You can also write [middleware functions](https://expressjs.com/en/guide/using-middleware.html) to handle tasks such as routing, logging and error handling.

Unfortunately, it lacks built-in support for authentication and authorization. You’ll have to implement that yourself using third-party libraries such as [Passport](https://www.sitepoint.com/local-authentication-using-passport-node-js/). Personally, I’m not a big fan of Express since it involves writing a lot of repetitive code when defining CRUD API routes for each database table.

### Express Links

*   [Home page](http://expressjs.com/)
*   [Documentation](http://expressjs.com/en/starter/installing.html)
*   [GitHub](https://github.com/expressjs/express)
*   [npm](https://www.npmjs.com/package/express)

Before we move on, here are similar frameworks that are based on or influenced by Express:

*   [Koa](https://koajs.com/)
*   [Hapi](https://hapi.dev/)
*   [Restify](http://restify.com/)
*   [NestJS](https://nestjs.com/)

## 2\. Fastify

![fastify](Images/fastify.png)

Fastify is a Node.js framework inspired by Hapi and Express. It’s designed to handle high numbers of requests as fast as possible. According to their [synthetic benchmarks](https://www.fastify.io/benchmarks/), Fastify is twice as fast as Express:

| Framework | Version | Router? | Requests/sec |
| --- | --- | --- | --- |
| hapi | 18.1.0 | ✓ | 29,998 |
| Express | 4.16.4 | ✓ | 38,510 |
| Restify | 8.0.0 | ✓ | 39,331 |
| Koa | 2.7.0 | ✗ | 50,933 |
| **Fastify** | **2.0.0** | **✓** | **76,835** |
| - |  |  |  |
| `http.Server` | 10.15.2 | ✗ | 71,768 |

To get started, you can install it as a package dependency in your project. Simply execute the following commands:

```
mkdir fastify-app
cd fastify-app
npm init -y
npm install fastify
touch server.js
```

Copy the following code to `server.js`:

```
const fastify = require('fastify')({ logger: true })

fastify.route({
  method: 'GET',
  url: '/',
  schema: {
    // request needs to have a query string with a `name` parameter
    querystring: {
      name: { type: 'string' }
    },
    // the response needs to be an object with a `hello` property of type 'string'
    response: {
      200: {
        type: 'object',
        properties: {
          hello: { type: 'string' }
        }
      }
    }
  },
  // this function is executed for every request before the handler is executed
  preHandler: async (request, reply) => {
    // E.g. check authentication
  },
  handler: async (request, reply) => {
    return { hello: 'world' }
  }
})

const start = async () => {
  try {
    await fastify.listen(3000)
    fastify.log.info(`server listening on ${fastify.server.address().port}`)
  } catch (err) {
    fastify.log.error(err)
    process.exit(1)
  }
}
start()
```

To start and test the server, you can do as follows:

```
$ node server.js
{"level":30,"time":1579520918815,"pid":23484,"hostname":"linux-msi","msg":"Server listening at http://127.0.0.1:3000","v":1}
{"level":30,"time":1579520918815,"pid":23484,"hostname":"linux-msi","msg":"server listening on 3000","v":1}

# Run the following command in a separate terminal
$ curl http://localhost:3000
{"hello":"world"}
```

This is a slightly advanced example where we highlight Fastify’s feature of [defining JSON schemas to validate requests and responses](https://www.fastify.io/docs/latest/Validation-and-Serialization/). Something else you may have noted is that Fastify code is able to handle JSON data out of the box. In addition to better performance, Fastify offers developers new features such as expressive coding style, hooks and decorators. Let’s break down what these features mean.

### Expressive style

In Fastify, you write less code than you normally would in Express. For example, in Express you need to import an additional package to handle JSON requests and responses. In Fastify, you simply work with object literals and the JSON part is handled automatically by the framework.

### Hooks

Hooks are special functions that are triggered by events. They allow you to interact with Fastify’s life cycle, which includes:

*   onRequest
*   preParsing
*   preValidation
*   preHandler
*   preSerialization
*   onError
*   onSend
*   onResponse

Hooks allow you to perform functions such as transforming data, performing validation or handling errors. You can [read more about hooks in the Fastify documentation](https://www.fastify.io/docs/latest/Hooks/).

## Decorators

Decorators is a feature that allows you to add functionality and new properties to a Fastify instance. You can [read more about decorators in the Fastify documentation](https://www.fastify.io/docs/latest/Decorators/).

Fastify also has an extensive [ecosystem of plugins](https://www.fastify.io/ecosystem/). These plugins allow you to connect to a specific database system, perform authentication and access third-party services such as Google Cloud Storage. About half are official plugins while the rest have been created by the community.

### Fastify Links

*   [Home page](https://www.fastify.io/)
*   [Documentation](https://www.fastify.io/docs/latest/)
*   [GitHub](https://github.com/fastify/fastify)
*   [npm](https://www.npmjs.com/package/fastify)

## 3\. FeathersJS

![feathers](Images/feathers.png)

If you detest writing repetitive code when building API routes, then Feathers could be the framework for you. Feathers is like Express on steroids. With simple commands, you can perform the following operations without writing a single line of code:

*   generate an API project
*   connect to any database
*   create CRUD API endpoints
*   set up authentication
*   define tests

Both Express and Fastify are light-weight frameworks that allow you to work on simple projects. Feathers is a heavy-weight framework that allows you to easily build a database-driven API server using its command-line tools. Its code is organized into various types of files:

*   Config: database configuration for production, development and testing.
*   Models: schema for a specific database table/collection.
*   Services: API function routes can be overridden here, or new ones can be added.
*   Hooks: perform tasks based on an event life cyle method—such as `beforeCreate`, `afterCreate` `beforeUpdate`, `afterUpdate`. Useful for transforming data or restricting access to fields such as passwords.

Out of the box, Feathers supports real-time communication via [Socket.io](https://socket.io/). This means you can build an interface using any front-end JavaScript framework that displays results in real time using Feathers as a back-end. It would be ideally suited to applications such as chats or trading platforms that require real-time capability.

Feathers also features a huge [ecosystem of plugins](https://github.com/feathersjs/awesome-feathersjs) allowing you to implement many extra features in your project. One of my favorite plugins is [feathers-seeder](https://www.npmjs.com/package/feathers-seeder), which fills your database with relevant data. This is a very useful feature when developing front-end code, ensuring that data is displayed correctly and can be paginated.

While it’s possible to install Feathers into a project as a dependency, it’s easier to use the command-line tool to build an API project for you. Here are a few instructions to get you started:

```
# Install Feathers CLI
npm install -g @feathersjs/cli

# Create a directory for your project
mkdir contacts-api && cd contacts-api

# Generate Feathers Project (you'll need to answer some basic questions)
feathers generate app

# Create Service (choose NeDB for local database, contacts for service, /contacts for API route)
feathers generate service

# Start the API server
npm start
```

If you follow the above commands, you’ll have created a database-driven API in just a few clicks. The server should be accessible on `localhost:3030`. However, you’ll need to use Postman or Insomnia to interact with the REST API you created like this:

![insomnia-app](Images/create-contact.png)

If you’d like to learn more, start with this [guide to Feathers](https://www.sitepoint.com/feathers-js-guide/), which will teach you how to set up a secure, database-driven API. Next, check out this [tutorial](https://www.sitepoint.com/crud-app-react-redux-feathersjs/) to learn how to connect a React front end with a Feathers back end.

### Feathers Links

*   [Home page](https://feathersjs.com/)
*   [Documentation](http://docs.feathersjs.com/)
*   [GitHub](https://github.com/feathersjs/feathers)
*   [npm](https://www.npmjs.com/package/@feathersjs/feathers)

## 4\. KeystoneJS

![keystone](Images/keystonejs.png)

KeystoneJS takes the ease of building APIs to another level. Straight out of the box, you get first-class GraphQL support, an extensible architecture and admin user interface for populating your database. Unfortunately, it only supports Mongo and PostgreSQL database, so you’ll need to install either before you start a KeystoneJS project. Other than that limitation, Keystone comes with a lot of built-in and very useful features such as:

*   authentication
*   access Control
*   email support
*   hooks
*   advanced Field Types
*   and more …

KeystoneJS is built on top of Express and the Mongoose ODM. Creating a KeystoneJS project can be done using the following commands:

```
npm init keystone-app my-app

✔ What is your project name? … keystone-app
✔ Select a starter project › Todo
✔ Select an adapter › Mongoose
```

In the above example, we’ve created a simple database-driven API with a `Todo` endpoint. We’ve configured the project to use Mongo and you can start it up with the following commands:

```
# Make sure Mongo is running
sudo service mongod start

# Start your Keystone project
cd my-app
npm run dev

ℹ Command: keystone dev
✔ Validated project entry file ./index.js
✔ Keystone server listening on port 3000
✔ Initialised Keystone instance
✔ Connected to database
✔ Keystone instance is ready at http://localhost:3000 🚀
🔗 Keystone Admin UI:  http://localhost:3000/admin
🔗 GraphQL Playground: http://localhost:3000/admin/graphiql
🔗 GraphQL API:    http://localhost:3000/admin/api 
```

Next, you can visit `http://localhost:3000/admin`, where you can use the UI to create new `Todos`. You can also go to the GraphQL API, `http://localhost:3000/admin/api`, and perform some queries. For example, to list all `todos`, you can use this query:

```
query {
  allTodos {
    id
    name
  }
}
```

When you press the play button, it should display the results:

```
{
  "data": {
    "allTodos": [
      {
        "id": "5e257020db53a03f48782463",
        "name": "Write Articles"
      },
      {
        "id": "5e257033db53a03f48782464",
        "name": "Eat lunch"
      }
    ]
  }
}
```

The main advantage of GraphQL over REST is that you can easily extract any data you need without defining a new API route. In a REST API, if you wanted to access records that were linked to other records via a relationship key, the back-end developer would need to create a new API endpoint that can handle the join operation. With GraphQL, such queries are defined on the front-end app. This frees up the back-end developer from having to add more API endpoints, which may become harder to maintain over time.

If you’re new to GraphQL, you should check out our [tutorials](https://www.sitepoint.com/tag/graphql/). To quickly confirm that your `todos` have been saved into your Mongo database, just execute the following:

```
# Open mongo client shell
mongo

# List all databases
show databases

# Switch to database
use keystone-app

# Display todos
db.todos.find()

{ "_id" : ObjectId("5e257020db53a03f48782463"), "name" : "Write Articles", "__v" : 0 }
{ "_id" : ObjectId("5e257033db53a03f48782464"), "name" : "Eat lunch", "__v" : 0 }
```

### Keystone Links

*   [Home page](http://keystonejs.com/)
*   [Documentation](https://www.keystonejs.com/quick-start/)
*   [GitHub](https://github.com/keystonejs/keystone)
*   [npm](https://www.npmjs.com/package/keystone)

## 5\. Strapi

![strapi](Images/strapi.png)

Strapi is by far the most powerful framework in the Node.js ecosystem, and you can use it to build a REST API with the least effort of all frameworks listed. Strapi is based on [Koa](https://koajs.com/), a web framework designed by the team behind Express. Koa is described as a more modern, modular and light-weight version of the Express framework. Earlier benchmarks I showed indicate that Koa has significantly better performance than Express.

With Strapi, you’re presented with a well-designed web user interface that allows you to:

*   connect to any database
*   set up as many collections (tables) and complex relations as you like
*   define field validation rules
*   set up different types of authentication methods (email, GitHub, Facebook etc.)
*   implement role-based access control

All this is done without hand coding anything. Strapi is mostly known as an open-source, headless CMS, and is built to favor non-technical users who are most likely going to be your project’s end users.

The primary advantage of Strapi is that end users can alter their API without involving developers. They also get an admin dashboard at an early stage in the project to upload and modify back-end data. This saves developers from creating the back-end user interface in the first place. If there’s a specific function that Strapi can’t provide, it can normally be easily implemented via plugins found in their [marketplace](https://strapi.io/marketplace). In addition, you may find that other front-end frameworks have support for Strapi through their own plugins. For example, you can use [gatsby-source-plugin](https://www.npmjs.com/package/gatsby-source-strapi) to connect Gatsby to a Strapi back end.

At the time of writing, Strapi is currently in beta. Depending on your internet speed and machine specs, the installation process can take upwards of ten minutes. My recommendation is to install and use [Yarn](https://yarnpkg.com/lang/en/), since it’s a bit faster. Hopefully, future versions will take a shorter time to set up. To start using Strapi right away, just execute the following commands:

```
# create a new strapi project based on quickstart template
yarn create strapi-app strapi-project --quickstart

# Start strapi server
yarn develop

yarn run v1.21.1

Project information

┌────────────────────┬──────────────────────────────────────────────────┐
│ Time               │ Mon Jan 20 2020 17:10:48 GMT+0300 (East Africa … │
│ Launched in        │ 7866 ms                                          │
│ Environment        │ development                                      │
│ Process PID        │ 25635                                            │
│ Version            │ 3.0.0-beta.18.4 (node v12.13.0)                  │
└────────────────────┴──────────────────────────────────────────────────┘

Actions available

Welcome back!
To manage your project 🚀, go to the administration panel at:
http://localhost:1337/admin

To access the server ⚡️, go to:
http://localhost:1337
```

Once the Strapi server has initialized, you can visit `http://localhost:1337/admin` to access the admin dashboard. First, you’ll need to create an admin account. Then you’ll be able to log in and start creating models. Once you save all the changes, Strapi should restart automatically in order to write code to its project folder. Next, click on your newly created **Content Type** to start inputting data. Finally, click on **Roles & Permissions** to set an appropriate access level for unauthenticated users. You can now use Postman or Insomnia to interact with your API, or consume it from a front-end app.

Strapi has been making great progress of late. The maintainers managed to [raise $4 million](https://strapi.io/blog/top-10-questions-to-strapi-ceo) in seed funding that’s being used to scale the team, ready the product for stable release and implement the most requested features proposed by its community. This means that it is safe for companies to invest time using the product to build their content management systems.

### Strapi Links

*   [Home page](https://strapi.io/)
*   [Documentation](https://strapi.io/documentation/3.0.0-beta.x/getting-started/introduction.html#strapi-documentation)
*   [GitHub](https://github.com/strapi/strapi)
*   [npm](https://www.npmjs.com/package/strapi)
*   [Slack](http://slack.strapi.io/)

## Summary

And there you have it. These are my top five developer-friendly Node.js frameworks that you can use to build your API in 2020.

So which should you use? Well, if you’re a beginner, it’s best to start with Express or Fastify. If you’re already comfortable with Express, you should dive into Feathers, as it can help you avoid writing repetitive code by scaffolding your API project using command-line tools. If GraphQL is important to you, KeystoneJS will help you set up an API effortlessly (although all frameworks I’ve mentioned here are capable of providing a GraphQL interface via extensions). My favorite platform for building an API is Strapi, as it provides a friendly user interface to define your API structure and manage data. I also like the fact that user authentication and access control is built in, meaning I don’t have to code anything.

I hope this guide will help you make an informed choice on which framework to use for your next project.

# Chapter 6: Using MySQL with Node.js and the mysql JavaScript Client

### by James Hibbard and Jay Raj

NoSQL databases are rather popular among Node developers, with MongoDB (the “M” in the MEAN stack) leading the pack. When starting a new Node project, however, you shouldn’t just accept Mongo as the default choice. Rather, the type of database you choose should depend on your project’s requirements. If, for example, you need dynamic table creation, or real-time inserts, then a NoSQL solution is the way to go. If your project deals with complex queries and transactions, on the other hand, an SQL database makes much more sense.

In this tutorial, we’ll have a look at getting started with the [mysql module](https://github.com/felixge/node-mysql)—a Node.js client for MySQL, written in JavaScript. We’ll explain how to use the module to connect to a MySQL database and perform the usual CRUD operations, before looking at stored procedures and escaping user input.

## Quick Start: How to Use MySQL in Node

If you’ve arrived here looking for a quick way to get up and running with MySQL in Node, we’ve got you covered!

Here’s how to use MySQL in Node in five easy steps:

1.  Create a new project: `mkdir mysql-test && cd mysql-test`.
2.  Create a `package.json` file: `npm init -y`.
3.  Install the mysql module: `npm install mysql`.
4.  Create an `app.js` file and copy in the snippet below (editing the placeholders as appropriate).
5.  Run the file: `node app.js`. Observe a “Connected!” message.

```
const mysql = require('mysql');
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'user',
  password: 'password',
  database: 'database name'
});
connection.connect((err) => {
  if (err) throw err;
  console.log('Connected!');
});
```

## Installing the mysql Module

Now let’s take a closer look at each of those steps.

```
mkdir mysql-test
cd mysql-test
npm init -y
npm install mysql
```

First of all, we’re using the command line to create a new directory and navigate to it. Then we’re creating a `package.json` file using the command `npm init -y`. The `-y` flag means that npm will use defaults without going through an interactive process.

This step also assumes that you have Node and npm installed on your system. If this is not the case, then check out this SitePoint article to find out how to do that: [Install Multiple Versions of Node.js using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

After that, we’re installing the [mysql module](https://www.npmjs.com/package/mysql) from npm and saving it as a project dependency. Project dependencies (as opposed to devDependencies) are those packages required for the application to run. You can read [more about the differences between the two here](https://stackoverflow.com/q/22891211).

If you need further help using npm, then be sure to check out [this guide](http://www.sitepoint.com/beginners-guide-node-package-manager/), or ask in [our forums](http://community.sitepoint.com/c/javascript).

## Getting Started

Before we get on to connecting to a database, it’s important that you have MySQL installed and configured on your machine. If this is not the case, please consult the [installation instructions on their home page](https://dev.mysql.com/doc/refman/8.0/en/installing.html).

The next thing we need to do is to create a database and a database table to work with. You can do this using a graphical interface, such as [Adminer](https://www.adminer.org/), or using the command line. For this guide, we’ll be using a database called `sitepoint` and a table called `authors`. Here’s a dump of the database, so that you can get up and running quickly if you wish to follow along:

```
CREATE DATABASE sitepoint CHARACTER SET utf8 COLLATE utf8_general_ci;
USE sitepoint;

CREATE TABLE authors (
  id int(11) NOT NULL AUTO_INCREMENT,
  name varchar(50),
  city varchar(50),
  PRIMARY KEY (id)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=5 ;

INSERT INTO authors (id, name, city) VALUES
(1, 'Michaela Lehr', 'Berlin'),
(2, 'Michael Wanyoike', 'Nairobi'),
(3, 'James Hibbard', 'Munich'),
(4, 'Karolina Gawron', 'Wrocław');
```

![Using MySQL with Node.js & the mysql JavaScript Client](Images/adminer.png)

## Connecting to the Database

Now, let’s create a file called `app.js` in our `mysql-test` directory and see how to connect to MySQL from Node.js:

```
const mysql = require('mysql');

// First you need to create a connection to the database
// Be sure to replace 'user' and 'password' with the correct values
const con = mysql.createConnection({
  host: 'localhost',
  user: 'user',
  password: 'password',
});

con.connect((err) => {
  if(err){
    console.log('Error connecting to Db');
    return;
  }
  console.log('Connection established');
});

con.end((err) => {
  // The connection is terminated gracefully
  // Ensures all remaining queries are executed
  // Then sends a quit packet to the MySQL server.
});
```

Now open up a terminal and enter `node app.js`. Once the connection is successfully established you should be able to see the “Connection established” message in the console. If something goes wrong (for example, you enter the wrong password), a callback is fired, which is passed an instance of the JavaScript Error object (`err`). Try logging this to the console to see what additional useful information it contains.

### Using nodemon to Watch the Files for Changes

Running `node app.js` by hand every time we make a change to our code is going to get a bit tedious, so let’s automate that. This part isn’t necessary to follow along with the rest of the tutorial, but will certainly save you some keystrokes.

Let’s start off by installing a the [nodemon](https://nodemon.io/) package. This is a tool that automatically restarts a Node application when file changes in a directory are detected:

```
npm install --save-dev nodemon
```

Now run `./node_modules/.bin/nodemon app.js` and make a change to `app.js`. nodemon should detect the change and restart the app.

#### Running nodemon

We’re running nodemon straight from the `node_modules` folder. You could also install it globally, or create an npm script to kick it off.

## Executing Queries

### Reading

Now that you know how to establish a connection to a MySQL database from Node.js, let’s see how to execute SQL queries. We’ll start by specifying the database name (`sitepoint`) in the `createConnection` command:

```
const con = mysql.createConnection({
  host: 'localhost',
  user: 'user',
  password: 'password',
  database: 'sitepoint'
});
```

Once the connection is established, we’ll use the `con` variable to execute a query against the database table `authors`:

```
con.query('SELECT * FROM authors', (err,rows) => {
  if(err) throw err;

  console.log('Data received from Db:');
  console.log(rows);
});
```

When you run `app.js` (either using nodemon or by typing `node app.js` into your terminal), you should be able to see the data returned from the database logged to the terminal:

```
[ RowDataPacket { id: 1, name: 'Michaela Lehr', city: 'Berlin' },
  RowDataPacket { id: 2, name: 'Michael Wanyoike', city: 'Nairobi' },
  RowDataPacket { id: 3, name: 'James Hibbard', city: 'Munich' },
  RowDataPacket { id: 4, name: 'Karolina Gawron', city: 'Wrocław' } ]
```

Data returned from the MySQL database can be parsed by simply looping over the `rows` object:

```
rows.forEach( (row) => {
  console.log(`${row.name} lives in ${row.city}`);
});
```

This gives you the following:

```
Michaela Lehr lives in Berlin
Michael Wanyoike lives in Nairobi
James Hibbard lives in Munich
Karolina Gawron lives in Wrocław
```

### Creating

You can execute an insert query against a database, like so:

```
const author = { name: 'Craig Buckler', city: 'Exmouth' };
con.query('INSERT INTO authors SET ?', author, (err, res) => {
  if(err) throw err;

  console.log('Last insert ID:', res.insertId);
});
```

Note how we can get the ID of the inserted record using the callback parameter.

### Updating

Similarly, when executing an update query, the number of rows affected can be retrieved using `result.affectedRows`:

```
con.query(
  'UPDATE authors SET city = ? Where ID = ?',
  ['Leipzig', 3],
  (err, result) => {
    if (err) throw err;

    console.log(`Changed ${result.changedRows} row(s)`);
  }
);
```

### Destroying

The same thing goes for a delete query:

```
con.query(
  'DELETE FROM authors WHERE id = ?', [5], (err, result) => {
    if (err) throw err;

    console.log(`Deleted ${result.affectedRows} row(s)`);
  }
);
```

## Advanced Use

We’ll finish off by looking at how the mysql module handles stored procedures and the escaping of user input.

### Stored Procedures

Put simply, a stored procedure is prepared SQL code that you can save to a database, so that it can easily be reused. If you’re in need of a refresher on stored procedures, then check out [this tutorial](https://code.tutsplus.com/articles/an-introduction-to-stored-procedures-in-mysql-5--net-17843).

Let’s create a stored procedure for our `sitepoint` database which fetches all the author details. We’ll call it `sp_get_authors`. To do this, you’ll need some kind of interface to the database. We’re using [Adminer](https://www.adminer.org/). Run the following query against the `sitepoint` database, ensuring that your user has admin rights on the MySQL server:

```
DELIMITER $$

CREATE PROCEDURE `sp_get_authors`()
BEGIN
  SELECT id, name, city FROM authors;
END $$
```

This will create and store the procedure in the `information_schema` database in the `ROUTINES` table.

![Creating stored procedure in Adminer](Images/adminer2.png)

#### Understanding Delimiter Syntax

If the delimiter syntax looks strange to you, it’s explained [here](http://www.mysqltutorial.org/mysql-stored-procedure/mysql-delimiter/).

Next, establish a connection and use the connection object to call the stored procedure as shown:

```
con.query('CALL sp_get_authors()',function(err, rows){
  if (err) throw err;

  console.log('Data received from Db:');
  console.log(rows);
});
```

Save the changes and run the file. Once it’s executed, you should be able to view the data returned from the database:

```
[ [ RowDataPacket { id: 1, name: 'Michaela Lehr', city: 'Berlin' },
    RowDataPacket { id: 2, name: 'Michael Wanyoike', city: 'Nairobi' },
    RowDataPacket { id: 3, name: 'James Hibbard', city: 'Leipzig' },
    RowDataPacket { id: 4, name: 'Karolina Gawron', city: 'Wrocław' },
  OkPacket {
    fieldCount: 0,
    affectedRows: 0,
    insertId: 0,
    serverStatus: 34,
    warningCount: 0,
    message: '',
    protocol41: true,
    changedRows: 0 } ]
```

Along with the data, it returns some additional information, such as the affected number of rows, `insertId` and so on. You need to iterate over the 0th index of the returned data to get employee details separated from the rest of the information:

```
rows[0].forEach( (row) => {
  console.log(`${row.name} lives in ${row.city}`);
});
```

This gives you the following:

```
Michaela Lehr lives in Berlin
Michael Wanyoike lives in Nairobi
James Hibbard lives in Leipzig
Karolina Gawron lives in Wrocław
```

Now let’s consider a stored procedure which requires an input parameter:

```
DELIMITER $$

CREATE PROCEDURE `sp_get_author_details`(
  in author_id int
)
BEGIN
  SELECT name, city FROM authors where id = author_id;
END $$
```

We can pass the input parameter while making a call to the stored procedure:

```
con.query('CALL sp_get_author_details(1)', (err, rows) => {
  if(err) throw err;

  console.log('Data received from Db:\n');
  console.log(rows[0]);
});
```

This gives you the following:

```
[ RowDataPacket { name: 'Michaela Lehr', city: 'Berlin' } ]
```

Most of the time when we try to insert a record into the database, we need the last inserted ID to be returned as an out parameter. Consider the following insert stored procedure with an out parameter:

```
DELIMITER $$

CREATE PROCEDURE `sp_insert_author`(
  out author_id int,
  in author_name varchar(25),
  in author_city varchar(25)
)
BEGIN
  insert into authors(name, city)
  values(author_name, author_city);
  set author_id = LAST_INSERT_ID();
END $$
```

To make a procedure call with an out parameter, we first need to enable multiple calls while creating the connection. So, modify the connection by setting the multiple statement execution to `true`:

```
const con = mysql.createConnection({
  host: 'localhost',
  user: 'user',
  password: 'password',
  database: 'sitepoint',
  multipleStatements: true
});
```

Next, when making a call to the procedure, set an out parameter and pass it in:

```
con.query(
  "SET @author_id = 0; CALL sp_insert_author(@author_id, 'Craig Buckler', 'Exmouth'); SELECT @author_id",
  (err, rows) => {
    if (err) throw err;

    console.log('Data received from Db:\n');
    console.log(rows);
  }
);
```

As seen in the above code, we have set an `@author_id` out parameter and passed it while making a call to the stored procedure. Once the call has been made we need to select the out parameter to access the returned ID.

Run `app.js`. On successful execution you should be able to see the selected out parameter along with various other information. `rows[2]` should give you access to the selected out parameter:

```
 [ RowDataPacket { '@author_id': 6 } ] ]
```

#### Deleting a Stored Procedure

To delete a stored procedure you need to run the command `DROP PROCEDURE <procedure-name>;` against the database you created it for.

### Escaping User Input

In order to avoid SQL Injection attacks, you should *always* escape any data you receive from users before using it inside an SQL query. Let’s demonstrate why:

```
const userSubmittedVariable = '1';

con.query(
  `SELECT * FROM authors WHERE id = ${userSubmittedVariable}`,
  (err, rows) => {
    if(err) throw err;
    console.log(rows);
  }
);
```

This seems harmless enough and even returns the correct result:

```
 { id: 1, name: 'Michaela Lehr', city: 'Berlin' }
```

However, try changing the `userSubmittedVariable` to this:

```
const userSubmittedVariable = '1 OR 1=1';
```

We suddenly have access to the entire data set. Now change it to this:

```
const userSubmittedVariable = '1; DROP TABLE authors';
```

We’re now in proper trouble!

The good news is that help is at hand. You just have to use the [mysql.escape](https://www.npmjs.com/package/mysql#escaping-query-values) method:

```
con.query(
  `SELECT * FROM authors WHERE id = ${mysql.escape(userSubmittedVariable)}`,
  (err, rows) => {
    if(err) throw err;
    console.log(rows);
  }
);
```

You can also use a question mark placeholder, as we did in the examples at the beginning of this guide:

```
con.query(
  'SELECT * FROM authors WHERE id = ?',
  [userSubmittedVariable],
  (err, rows) => {
    if(err) throw err;
    console.log(rows);
  }
);
```

## Why Not Just USE an ORM?

Before we get into the pros and cons of this approach, let’s take a second to look at what ORMs are. The following is taken from [an answer on Stack Overflow](https://stackoverflow.com/a/1279678/1136887):

> Object-Relational Mapping (ORM) is a technique that lets you query and manipulate data from a database using an object-oriented paradigm. When talking about ORM, most people are referring to a library that implements the Object-Relational Mapping technique, hence the phrase “an ORM”.

So this means you write your database logic in the domain-specific language of the ORM, as opposed to the vanilla approach we’ve been taking so far. To give you an idea of what this might look like, here’s an example using [Sequelize](http://docs.sequelizejs.com/), which queries the database for all authors and logs them to the console:

```
const sequelize = new Sequelize('sitepoint', 'user', 'password', {
  host: 'localhost',
  dialect: 'mysql'
});

const Author = sequelize.define('author', {
  name: {
    type: Sequelize.STRING,
  },
  city: {
    type: Sequelize.STRING
  },
}, {
  timestamps: false
});

Author.findAll().then(authors => {
  console.log("All authors:", JSON.stringify(authors, null, 4));
});
```

Whether or not using an ORM makes sense for you will depend very much on what you’re working on and with whom. On the one hand, ORMS tend to make developers more productive, in part by abstracting away a large part of the SQL so that not everyone on the team needs to know how to write super efficient database specific queries. It’s also easy to move to different database software, because you’re developing to an abstraction.

On the other hand, however, it’s possible to write some really messy and inefficient SQL as a result of not understanding how the ORM does what it does. Performance is also an issue in that it’s much easier to optimize queries that don’t have to go through the ORM.

Whichever path you take is up to you, but if this is a decision you’re in the process of making, check out this Stack Overflow thread: [Why should you use an ORM?](https://stackoverflow.com/q/448684/1136887). Also check out this post on SitePoint: [3 JavaScript ORMs You Might Not Know](https://www.sitepoint.com/3-javascript-orms-you-might-not-know/).

## Conclusion

In this tutorial, we’ve installed the [mysql client](https://github.com/mysqljs/mysql) for Node.js and configured it to connect to a database. We’ve also seen how to perform CRUD operations, work with prepared statements and escape user input to mitigate SQL injection attacks. And yet, we’ve only scratched the surface of what the mysql client offers. For more detailed information, we recommend reading the [official documentation](https://github.com/mysqljs/mysql).

And please bear in mind that the mysql module is not the only show in town. There are other options too, such as the popular [node-mysql2](https://github.com/sidorares/node-mysql2).

# Chapter 7: Introduction to MongoDB

### by Manjunath M. and James Hibbard

MongoDB is a cross-platform, open-source, NoSQL database, used by many modern Node-based web applications to persist data.

In this beginner-friendly tutorial, I’ll demonstrate how to install Mongo, then start using it to store and query data. I’ll also look at how to interact with a Mongo database from within a Node program, and also highlight some of the differences between Mongo and a traditional relational database (such as MySQL) along the way.

## Terminology and Basic Concepts

MongoDB is a document-oriented database. This means that it doesn’t use tables and rows to store its data, but instead *collections* of JSON-like *documents*. These documents support embedded fields, so related data can be stored within them.

MongoDB is also a schema-less database, so we don’t need to specify the number or type of columns before inserting our data.

Here’s an example of what a MongoDB document might look like:

```
{
  _id: ObjectId(3da252d3902a),
  type: "Tutorial",
  title: "An Introduction to MongoDB",
  author: "Manjunath M",
  tags: [ "mongodb", "compass", "crud" ],
  categories: [
    {
      name: "javascript",
      description: "Tutorialss on client-side and server-side JavaScript programming"
    },
    {
      name: "databases",
      description: "Tutorialss on different kinds of databases and their management"
    },
  ],
  content: "MongoDB is a cross-platform, open-source, NoSQL database..."
}
```

As you can see, the document has a number of *fields* (`type`, `title` etc.), which store *values* (“Tutorial”, “An Introduction to MongoDB” etc.). These values can contain strings, numbers, arrays, arrays of sub-documents (for example, the `categories` field), geo-coordinates and more.

The `_id` field name is reserved for use as a primary key. Its value must be unique in the collection, it’s immutable, and it may be of any type other than an array.

#### JSON-like?

For those wondering what “JSON-like” means, internally Mongo uses something called [BSON](http://bsonspec.org/) (short for Bin­ary JSON). In practice, you don’t really need to know much about BSON when working with MongoDB.

As you might guess, a **document** in a NoSQL database corresponds to a **row** in an SQL database. A group of documents together is known as a **collection**, which is roughly synonymous with a **table** in a relational database.

Here’s a table summarizing the different terms:

| SQL Server | MongoDB |
| --- | --- |
| Database | Database |
| Table | Collection |
| Row | Document |
| Column | Field |
| Index | Index |

If you’re starting a new project and are unsure whether to choose Mongo or a relational database such as MySQL, now might be a good time to read our tutorial [SQL vs NoSQL: How to Choose](https://www.sitepoint.com/sql-vs-nosql-choose/).

With that said, let’s go ahead and install MongoDB.

## Installing MongoDB

#### Online Playgrounds

If you’d just like to follow along with this tutorial without installing any software on your PC, there are a couple of online services you can use. [Mongo playground](https://mongoplayground.net/), for example, is a simple sandbox to test and share MongoDB queries online.

MongoDB comes in various editions. The one we’re interested in is the MongoDB Community Edition.

The project’s home page has excellent documentation on installing Mongo, and I won’t try to replicate that here. Rather, I’ll offer you links to instructions for each of the main operating systems:

*   [Install MongoDB Community Edition on Windows](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)
*   [Install MongoDB Community Edition on macOS](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/)
*   [Install MongoDB Community Edition on Ubuntu](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)

If you use a non-Ubuntu-based version of Linux, you can check out [this page](https://docs.mongodb.com/manual/installation/#mongodb-community-edition-installation-tutorials) for installation instructions for other distros. MongoDB is also normally available through the official Linux software channels, but sometimes this will pull in an outdated version.

### Post Installation Configuration

Once you have MongoDB installed for your system, you might encounter this error:

```
dbpath (/data/db) does not exist.
 Create this directory or give existing directory in --dbpath.
 See http://dochub.mongodb.org/core/startingandstoppingmongo
```

This means that Mongo can’t find (or access) the directory it uses to store its databases. This is pretty easy to remedy:

```
sudo mkdir -p /data/db
sudo chown -R `id -un` /data/db
```

The first command creates the `data/db` directory. The second sets permissions so that Mongo can write to that directory.

### Install the Compass GUI

We’ll be using the command line in this tutorial, but MongoDB also offers a tool called Compass to connect to and manage your databases using a GUI.

If you’re on Windows, Compass can be installed as part of the main Mongo installation (just select the appropriate option from the wizard). Otherwise, you can [download Compass for your respective OS here](https://docs.mongodb.com/compass/master/install/).

This is what it looks like:

![Mongo DB Compass GUI](Images/MongoDB-Compass.png)

### The Mongo Shell

We can test our installation by opening the Mongo shell. You can do this by opening a terminal window and typing `mongo`.

#### Check Your Path

This assumes that `<mongodb installation dir>/bin` is in your path. If for any reason this isn’t the case, change into the `<mongodb installation dir>/bin` directory and rerun the command.

If you get an `Error: couldn't connect to server` error, you’ll need to start the Mongo server (in a second terminal window) with the command `mongod`.

Once you’re in the Mongo shell, type in `db.version()` to see the version of MongoDB you’re running. At the time of writing, this should output `4.2.2`.

Please note that you can exit the Mongo shell by running `quit()` and the Mongo daemon by pressing `Ctrl` + `C` at any time.

Now let’s get acquainted with some MongoDB basics.

## Basic Database Operations

Enter the Mongo shell if you haven’t already (by typing `mongo` into a terminal):

```
[mj@localhost ~]$ mongo
MongoDB shell version v4.2.2
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("08a624a0-b330-4233-b56b-1d5b15a48fea") }
MongoDB server version: 4.2.2
```

Let’s start off by creating a database to work with. To create a database, MongoDB has a `use DATABASE_NAME` command:

```
> use exampledb
switched to db exampledb
```

To display all the existing databases, try `show dbs`:

```
> show dbs
admin          0.000GB
config         0.000GB
local          0.000GB
```

The `exampledb` isn’t in the list because we need to insert at least one document into the database. To insert a document, you can use `db.COLLECTION_NAME.insertOne({"key":"value"})`. Here’s an example:

```
> db.users.insertOne({name: "Bob"})
{
   "acknowledged" : true,
   "insertedId" : ObjectId("5a52c53b223039ee9c2daaec")
}
```

MongoDB automatically creates a new `users` collection and inserts a document with the key–value pair `'name':'Bob'`. The ObjectId returned is the ID of the document inserted. MongoDB creates a unique ObjectId for each document on creation, and it becomes the default value of the `_id` field.

Now we should be able to see our database:

```
>show dbs
admin          0.000GB
config         0.000GB
exampledb      0.000GB
local          0.000GB
```

Similarly, you can confirm that the collection was created using the `show collections` command:

```
> show collections
users
```

We’ve created a database, added a collection named `users` and inserted a document into it. Now let’s try dropping it. To drop an existing database, use the `dropDatabase()` command, as exemplified below:

```
>db.dropDatabase()
{ "dropped" : "exampledb", "ok" : 1 }
```

`show dbs` confirms that the database was indeed dropped:

```
> show dbs
admin          0.000GB
config         0.000GB
local          0.000GB
```

For more database operations, please consult the MongoDB reference page on [database commands](https://docs.mongodb.com/manual/reference/command/).

## User Management

By now you’ve probably noticed that MongoDB doesn’t come with any kind of access control enabled.

While not having to supply a username and password is nice for development, this is something you should change when using Mongo in production.

Here are the steps for creating a database user with full read/write privileges:

*   Ensure that you’ve started the Mongo server without any kind of access control (typically by typing `mongod`).
*   Open a shell by typing `mongo`.
*   From the shell, add a user with the `readWrite` role to the `exampledb` database. This will prompt you to enter a password. Obviously, replace “manjunath” with your desired user name:

    ```
     use exampledb
      db.createUser(
        {
          user: "manjunath",
          pwd: passwordPrompt(),
          roles: [ { role: "readWrite" ]
        }
      )
    ```

*   Exit the Mongo shell.
*   Shut down the Mongo server, then restart it using `mongod --auth`. Clients that connect to this instance must now authenticate themselves.
*   Reopen a shell like so: `mongo --authenticationDatabase "exampledb" -u "manjunath" -p`. You’ll now be prompted for your password.

For further information, please consult the [project’s documentation on enabling access control](https://docs.mongodb.com/manual/tutorial/enable-authentication/).

## MongoDB CRUD Operations

As you might already know, the CRUD acronym stands for **c**reate, **r**ead, **u**pdate, and **d**elete. These are the four basic database operations that you can’t avoid while building an application. For instance, any modern application will have the ability to create a new user, read the user data, update the user information and, if needed, delete the user account. Let’s accomplish this at the database level using MongoDB.

### Create Operation

Creation is the same as [inserting a document](https://docs.mongodb.com/manual/tutorial/insert-documents/) into a collection. In the previous section, we inserted a single document using the `db.collection.insertOne()` syntax. There’s another method called `db.collection.insertMany()` that lets you insert multiple documents at once. Here’s the syntax:

```
> db.collection.insertMany([ <document 1> , <document 2>, ... ])
```

Let’s create a `users` collection and populate it with some actual users:

```
> use exampledb
> db.users.insertMany([
   { name: "Tom",age:15, email: "tom@example.com" },
   { name: "Bob", age:35, email:"bob@example.com" },
   { name: "Kate", age: 27, email: "kate@example.com" },
   { name: "Katherine", age:65, email:"katherine@example.com"}
])

{
   "acknowledged" : true,
   "insertedIds" : [
      ObjectId("5e25bb58ba0cf16476aa56ff"),
    ObjectId("5e25bb58ba0cf16476aa5700"),
    ObjectId("5e25bb58ba0cf16476aa5701"),
    ObjectId("5e25bb58ba0cf16476aa5702")
   ]
}
```

The `insertMany` method accepts an array of objects and, in return, we get an array of `ObjectId`s.

### Read Operation

A read operation is used to [retrieve a document, or multiple documents](https://docs.mongodb.com/manual/tutorial/query-documents/) from a collection. The syntax for the read operation is as follows:

```
> db.collection.find(query, projection)
```

To retrieve all user documents, you can do this:

```
> db.users.find().pretty()
{
  "_id" : ObjectId("5e25bb58ba0cf16476aa56ff"),
  "name" : "Tom",
  "age" : 15,
  "email" : "tom@example.com"
}
{
  "_id" : ObjectId("5e25bb58ba0cf16476aa5700"),
  "name" : "Bob",
  "age" : 35,
  "email" : "bob@example.com"
}
{
  "_id" : ObjectId("5e25bb58ba0cf16476aa5701"),
  "name" : "Kate",
  "age" : 27,
  "email" : "kate@example.com"
}
{
  "_id" : ObjectId("5e25bb58ba0cf16476aa5702"),
  "name" : "Katherine",
  "age" : 65,
  "email" : "katherine@example.com"
}
```

This corresponds to the `SELECT * FROM USERS` query for an SQL database.

The `pretty` method is a [cursor method](https://docs.mongodb.com/manual/reference/method/js-cursor/), and there are many others too. You can chain these methods to modify your query and the documents that are returned by the query.

Perhaps you need to filter queries to return a subset of the collection—such as finding all users who are below 30\. You can modify the query like this:

```
> db.users.find({ age: { $lt: 30 } })
{ "_id" : ObjectId("5e25bb58ba0cf16476aa56ff"), "name" : "Tom", "age" : 15, "email" : "tom@example.com" }
{ "_id" : ObjectId("5e25bb58ba0cf16476aa5701"), "name" : "Kate", "age" : 27, "email" : "kate@example.com" }
```

In this example, `$lt` is a query filter operator that selects documents whose `age` field value is less than 30. There are many comparison and logical query filters available. You can see the entire list in the [query selector documentation](https://docs.mongodb.com/manual/reference/operator/query/#query-selectors).

#### Replicating a Regex

In Mongo, You can replicate SQL’s `like` query using a regex. For example, `SELECT` *`FROM users WHERE name LIKE 'Kat%'`* *translates to `db.users.find({ name: /Kat.`*`/ })`.

### Update Operation

An [update operation](https://docs.mongodb.com/manual/tutorial/update-documents/) modifies documents in a collection. Similar to the create operation, MongoDB offers various methods for updating a document. For example:

1.  `db.collection.updateOne(<filter>, <update>, <options>)`
2.  `db.collection.updateMany(<filter>, <update>, <options>)`.

If you need to add an extra field—say, `registration`—to all the existing documents in a collection, you can do something like this:

```
> db.users.updateMany({}, {$set: { registration: "incomplete"}})
{ "acknowledged" : true, "matchedCount" : 4, "modifiedCount" : 4 }
```

The first argument is an empty object because we want to update all documents in the collection. The `$set` is an update operator that sets the value of a field with the specified value. You can verify that the extra field was added using `db.users.find()`.

To update the value of documents that match certain criteria, `updateMany()` accepts a filter object as its first argument. For instance, you might want to overwrite the value of `registration` to `complete` for all users who are aged 18+. Here’s what you can do:

```
> db.users.updateMany(
  {age:{ $gt: 18} },
  {$set: { registration: "complete"}
})

{ "acknowledged" : true, "matchedCount" : 3, "modifiedCount" : 3 }
```

To update the registration details of a single user, you can do this:

```
> db.users.updateOne(
 {email: "tom@example.com" },
 {$set: { registration: "complete"}
})

{ "acknowledged" : true, "matchedCount" : 1, "modifiedCount" : 1 }
```

### Delete Operation

A [delete operation](https://docs.mongodb.com/manual/tutorial/remove-documents/) removes a document from the collection. To delete a document, you can use the `db.collection.deleteOne(<filter>, <options>)` method, and to delete multiple documents, you can use the `db.collection.deleteMany(<filter>, <options>)` method.

To delete documents based on certain criteria, you can use the filter operators that we used for the read and update operation:

```
> db.users.updateOne(
 {email: "tom@example.com" },
 {$set: { status: "dormant"}
})

{ "acknowledged" : true, "matchedCount" : 1, "modifiedCount" : 1 }

> db.users.deleteMany( { status: { $in: [ "dormant", "inactive" ] } } )

{ "acknowledged" : true, "deletedCount" : 1 }
```

This deletes all documents with a status of “dormant” or “inactive”.

## Schema Validation

Earlier in this tutorial, when I said that Mongo is a schema-less database, I was over simplifying somewhat.

It *is* schema-less in so far as we don’t need to specify the number or type of columns before inserting our data. However, it’s also possible to define a JSON schema and use it to enforce validation rules for our data.

Let’s create a `validatedUsers` collection, where we can use the `validator` construct to specify that a `name` is mandatory and that an `email` field matches a certain pattern:

```
> db.createCollection("validatedUsers", {
  validator: {
    $jsonSchema: {
      required: [ "name", "email" ],
      properties: {
        name: {
          bsonType: "string",
          description: "must be a string and is required"
        },
        email: {
          bsonType: "string",
          pattern: "^.+\@.+$",
          description: "must be a valid email and is required"
        }
      }
    }
  }
})

{ "ok" : 1 }
```

Now if we try to insert incorrect data, we’ll receive a validation error:

```
> db.validatedUsers.insertOne({ name: "Jim", email: "not-an-email" })

2020-01-22T09:56:56.918+0100 E  QUERY    &lsqb;js] uncaught exception: WriteError({
  "index" : 0,
  "code" : 121,
  "errmsg" : "Document failed validation",
  "op" : {
    "_id" : ObjectId("5e280e5847eb18010666530c"),
    "name" : "Jim",
    "email" : "not-an-email"
  }
}) :
WriteError({
  "index" : 0,
  "code" : 121,
  "errmsg" : "Document failed validation",
  "op" : {
    "_id" : ObjectId("5e280e5847eb18010666530c"),
    "name" : "Jim",
    "email" : "not-an-email"
  }
})
WriteError@src/mongo/shell/bulk_api.js:458:48
mergeBatchResults@src/mongo/shell/bulk_api.js:855:49
executeBatch@src/mongo/shell/bulk_api.js:919:13
Bulk/this.execute@src/mongo/shell/bulk_api.js:1163:21
DBCollection.prototype.insertOne@src/mongo/shell/crud_api.js:264:9
@(shell):1:1
```

You can read [more about schema validation in the project’s documentation](https://docs.mongodb.com/manual/core/schema-validation/).

## An Overview of MongoDB Drivers

For an application to communicate with the MongoDB server, you have to use a client-side library called a **driver**. The driver sits on top of the database server and lets you interact with the database using the driver API. MongoDB has official and third-party drivers for all popular languages and environments.

The most popular drivers for Node.js include [the native MongoDB driver](https://docs.mongodb.com/ecosystem/drivers/node/) and [Mongoose](https://mongoosejs.com/). I’ll briefly discuss both of these here.

### MongoDB Node.js Driver

This is the official [MongoDB driver for Node.js](https://mongodb.github.io/node-mongodb-native/). The driver can interact with the database using either callbacks, promises or `async … await`.

You can install it like so:

```
npm install mongod
```

The example below demonstrates how to connect the driver to the server, and list out all of the documents in the `users` collection.

#### Name and Password

If you connected to the Mongo server using a name and password, you’ll need to specify these details in your code.

```
const MongoClient = require('mongodb').MongoClient;
const url = 'mongodb://localhost:27017/exampledb';

// With authentication:
// const url = 'mongodb://<userName>:<passWord>@localhost:27017/exampledb';
// Further reading: https://docs.mongodb.com/manual/reference/connection-string/

(async () => {
  let client;

  try {
    client = await MongoClient.connect(url, {
      useNewUrlParser: true,
      useUnifiedTopology: true
    });

    const db = client.db('exampledb');
    const collection = db.collection('users');
    const users = await collection.find().toArray();
    console.log(users);
  } catch (err) {
    console.log(err.stack);
  }

  if (client) {
    client.close();
  }
})(); 
```

The `MongoClient.connect` returns a promise. Any error is caught by the `catch` block and any database actions go inside the `try` block. If you look through the [Mongo driver documentation](https://mongodb.github.io/node-mongodb-native/3.5/), you’ll see that the API is pretty similar to what we’ve been using in the shell.

### Mongoose Driver

Another popular Node.js driver for MongoDB is [Mongoose](http://mongoosejs.com/docs/index.html). Mongoose is built on top of the official MongoDB driver. Back when Mongoose was released, it had tons of features that the native MongoDB driver didn’t have. One prominent feature was the ability to define a schema structure that would get mapped onto the database’s collection. However, the latest versions of MongoDB have adopted some of these features in the form of JSON schema and schema validation.

Apart from schema, other fancy features of Mongoose include [models](https://mongoosejs.com/docs/models.html), [validators](https://mongoosejs.com/docs/validation.html) and [middleware](https://mongoosejs.com/docs/middleware.html), the [populate method](https://mongoosejs.com/docs/populate.html), [plugins](https://mongoosejs.com/docs/plugins.html) and so on. You can read more about these in the Mongoose docs.

You can install Mongoose like so:

```
npm install mongoose
```

Here’s the Mongoose equivalent of the previous example:

```
const mongoose = require('mongoose');

async function run() {
  await mongoose.connect('mongodb://localhost:27017/exampledb', {
    useNewUrlParser: true,
    useUnifiedTopology: true
  });

  const userSchema = new mongoose.Schema({ name: String, age: String, email: String });
  const User = mongoose.model('User', userSchema);

  const users = await User.find();
  console.log(users);
  mongoose.connection.close();
}

run().catch(error => console.log(error.stack));
```

In Mongoose, everything starts with a a [Schema](https://mongoosejs.com/docs/guide.html). Each schema maps to a MongoDB collection and defines the shape of the documents within that collection.

## Conclusion

MongoDB is a popular NoSQL database solution that suits modern development requirements. In this tutorial, we’ve covered the basics of MongoDB, the Mongo shell and some of the popular drivers available. We’ve also explored the common database operations and CRUD actions within the Mongo shell. Now it’s time for you to head out and try what we’ve covered here and more. If you want to learn more, I recommend creating a REST API with MongoDB and Node to acquaint yourself with the common database operations and methods.