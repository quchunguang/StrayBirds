---
layout: post
title: Git on Windows
categories: [tech]
tags: [git, powershell, windows]
published: True
comments: True
---

## Pre-requisites

1. Verify you have PowerShell 2.0 or better with `$PSVersionTable.PSVersion`. PowerShell 3.0 is preferred as 2.0 support is deprecated.

2. Verify execution of scripts is allowed with `Get-ExecutionPolicy` (should be RemoteSigned or Unrestricted). If scripts are not enabled, run PowerShell as Administrator and call `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Confirm`.

3. Verify that git can be run from PowerShell. If the command is not found, you will need to add a git alias or add `%ProgramFiles(x86)%\Git\cmd` (or `%ProgramFiles%\Git\cmd` if you're still on 32-bit) to your PATH environment variable.

## Install

```powershell
git clone https://github.com/dahlbyk/posh-git.git
cd posh-git
.\install.ps1
```

[1]: https://github.com/dahlbyk/posh-git
