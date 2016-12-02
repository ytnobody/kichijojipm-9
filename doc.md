# VSCode and Perl
Kichijoji.pm VERSION 9.00

@ytnobody

---

## Hello, ytnobody.

![It's me](https://pbs.twimg.com/profile_images/378800000466143858/93673f957eb413a7a34410d930afa5f7.png)

* AZUMA Satoshi
* System Advisor / Technology Specialist
* CPAN Author [YTURTLE]
* Perl, PHP, Go, Unity, Azure, Docker, etc...

---

## I'm from the Ooi-machi.pm 

* A.K.A. Machi-P
* It inherits the Machida.pm
* But, we still live in #machidapm on hachiojipm.slack.com like a vagabond :p

---

## What is the VSCode?

Visual Studio Code

[http://code.visualstudio.com/](http://code.visualstudio.com/)

* From Microsoft Corp.
* Version 1.7 is the newest. (in 2016-11-15)
* [The source code is available under the MIT license agreement.](http://code.visualstudio.com/License)
* Is not a full-stack IDE. A code editor that integrated with the tarminal.

---

## Why use it?

VSCode is ...

* the Vim.
* and the Emacs.
* and the Mega-customizable editor.
* and it is Git friendly.
* and it supports MacOS / Windows and Linux.
* and ... it is very fast and lightweight. 

I still bit use the Vim for some traditional system.

But, VSCode is the better-Vim for me.

---

## Why VSCode is the better-Vim?

Because, the [VSCodeVim/Vim](https://github.com/VSCodeVim/Vim) extension is there.

---

## Why VSCode is the Emacs...?

Because, the [nisheetjain/vscode-emacs](https://github.com/nisheetjain/vscode-emacs) extension is there, And more.

:p

---

## FUDs Buster

---

### FUD 

Become cannot to input `"*"` with VSCodeVim/Vim.

---

### Answer 

I never encountered such bug with VSCodeVim/Vim v0.4.1. 

I think it was fixed.

---

### FUD

VSCode often encounters to sudden-death.

---

### Answer 

I use VSCode since version 1.0.x. 

But I never saw that VSCode is encountered to sudden-death to today.

---

# VSCode Technics for Perl Mongers

---

## Bring Your Needed Terminal

---

You can launch default terminal (ex. `Terminal.app`) on the VSCode with hotkey `Ctrl+｀`  

---

But, we want that VSCode is been customised as we like.

---

Edit `.vscode/setting.json`

```
{
    ...
    // for MacOSX
    "terminal.external.osxExec": "Terminal.app",

    // for Linux
    "terminal.external.linuxExec": "xterm",

    // for Windows
    "terminal.external.windowsExec": "%COMSPEC%",
    ...
}
```

---

Then, `Ctrl+｀` to launch your wanted terminal on the VSCode.

---

## Run `prove` with hotkey

---

Create `build.sh`

```
#!/bin/sh
export LANG=ja_jp.UTF-8
cpanm --installdeps .
prove -Ilib t/
```

---

Edit `.vscode/tasks.json`

```
{
    "version": "0.1.0",
    "command": "bash",
    "isShellCommand": true,
    "tasks": [
        {
            "taskName": "build",
            "isBuildCommand": true,
            "suppressTaskName": true,
            "args": [
                "build.sh"
            ]
        }
    ],
    "showOutput": "always"
}
```

---

Then, `Cmd+Shift+B` to launch `build.sh` in VSCode.

---

## Debugger

---

We can install [`Perl Debug`](https://github.com/raix/vscode-perl-debug) Extension. :)

---

## And more technics

---

with demo...

---

## Appendix 

Write a presentation and show it with VSCode

---

## Use [vscode-reveal](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)

---

# Happy Hacking 
# with VSCode!

