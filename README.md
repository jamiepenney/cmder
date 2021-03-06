# Cmder

[![Join the chat at https://gitter.im/cmderdev/cmder](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cmderdev/cmder?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Latest release is **[v1.2](https://github.com/bliker/cmder/releases/tag/v1.2)**

Cmder is a **software package** created out of pure frustration over absence of usable console emulator on Windows. It is based on [ConEmu](https://github.com/Maximus5/ConEmu) with *major* config overhaul. Monokai color scheme, amazing [clink](https://github.com/mridgers/clink) and custom prompt layout.

![Cmder Screenshot](http://i.imgur.com/g1nNf0I.png)

## Why use it

The main advantage of Cmder is portability. It is designed to be totally self-contained with no external dependencies, which makes it great for **USB Sticks** or **Dropbox** - you can carry your console, aliases and binaries (like wget, curl and git) with you anywhere!

## Installation

1. Download the latest release
2. Extract
3. (optional) Place your own executable files into the `bin` folder to be injected into your PATH.
4. Run cmder

*(There will be a version with installer)*

## Integration

So, you've experimented with cmder a little and want to give it a shot in a more permanent home:

### Shortcut to open Cmder in a chosen folder

1. Open a terminal as an Administrator
2. Navigate to the directory you have placed Cmder
3. Execute `.\cmder.exe /REGISTER ALL`
   _If you get a message "Access Denied" ensure you are executing the command in an **Administrator** prompt._

In a file explorer window right click in or on a directory to see "Cmder Here" in the context menu.

## Keyboard shortcuts

### Tab manipulation

* `Ctrl + t` : new tab dialog (maybe you want to open cmd as admin?)
* `Ctrl + w` : close tab
* `Ctrl + d` : close tab (if pressed on empty command)
* `Shift + alt + number` : fast new tab: `1` - CMD, `2` - Powershell `*` - More to come
* `Alt + enter`: Fullscreen

### Shell

* `Shift + Up` : Traverse up in directory structure (lovely feature!)
* `End, Home, Ctrl` : Traversing text with as usual on Windows
* `Ctrl + r` : History search
* `Shift + mouse` : Select and copy text from buffer

(Some shortcuts are not yet documented, thought they exist - please document them here)

## Features

### Aliases
You can define simple aliases with command `alias name=command`.

For example there is one defined for you `alias e.=explorer .`

All aliases will be saved in `/config/aliases` file

### SSH Agent

To start SSH agent simply call `agent`, which is in the `bin` folder.

If you want to run SSH agent on startup, uncomment the line in `/vendor/init.bat`so it says `@call "%CMDER_ROOT%/bin/agent.cmd"`.

## Todo

1. Git Bash
2. Check for clink and git before injecting them (Sort of done)

## Current development branch

You can download builds of the current development branch by going to Appveyor via the following link:

[![AppVeyor](https://ci.appveyor.com/api/projects/status/github/cmderdev/cmder?svg=True)](https://ci.appveyor.com/project/MartiUK/cmder/branch/development/artifacts)

## License

All software included is bundled with own license

The MIT License (MIT)

Copyright (c) 2015 Samuel Vasko

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
