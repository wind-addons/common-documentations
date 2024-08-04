# Wind Addons Development Guide

This guide outlines the development standards and practices used in Wind Addons projects.

<details>
<summary>📖 Table of Contents</summary>

- [🛠️ Development Setup](#️-development-setup)
  - [Git](#git)
  - [Lua 5.1](#lua-51)
  - [Code Editor](#code-editor)
- [📐 Coding Standards](#-coding-standards)
  - [General Guidelines](#general-guidelines)
  - [Linters and Formatters](#linters-and-formatters)
- [📑 Git Commit Guidelines](#-git-commit-guidelines)
- [📜 License](#-license)

</details>

## 🛠️ Development Setup

WoW addon development is typically done on Windows. This guide will help you align your environment with the standards used in Wind Addons development.

While it's possible to develop on macOS or Linux, ensure that you use the same formatter and Git configuration as outlined here.

### Git

Download and install the latest version of Git from [git-scm.com](https://git-scm.com).

On Windows, after cloning a project from wind-addons, run the following command to enable the `autocrlf` feature:

```powershell
git config core.autocrlf true
```

For contributors working on multiple Wind Addons projects, it may be more convenient to set this globally:

```powershell
git config --global core.autocrlf true
```

### Lua 5.1

WoW uses Lua 5.1, so you'll need to install it for testing and running Lua scripts.

To install Lua 5.1 on Windows:

1. Find the latest 5.1.x version on [LuaBinaries](https://luabinaries.sourceforge.net) and open the SourceForge page.
2. Download `lua-5.1.x_Win64_bin.zip` from the `Tools Executables` folder and extract it to your desired location.
3. Add the extracted folder to your system's `Path`.

### Code Editor

[Visual Studio Code](https://code.visualstudio.com) is highly recommended.

You can also use other editors like Neovim, Sublime Text, etc., but you'll need to configure formatters and linters manually.

## 📐 Coding Standards

### General Guidelines

1. All code must be formatted using [stylua](https://github.com/JohnnyMorganz/StyLua) with the configuration provided in the addon repository or the default settings.
2. Use `LF` as the line ending for all code.

### Linters and Formatters

| **Language** | **Linter**          | **Formatter**                                                 |
| ------------ | ------------------- | ------------------------------------------------------------- |
| Lua          | Any                 | `stylua`                                                      |
| Markdown     | `markdownlint-cli2` | [`wind-addons/wmdfmt`](https://github.com/wind-addons/wmdfmt) |
| Rust         | `clippy`            | `rustfmt`                                                     |
| Python       | `ruff`              | `ruff`                                                        |
| Bash         | Any                 | `shfmt`                                                       |
| Go           | `golangci-lint`     | `goimports`, `gofumpt`                                        |

## 📑 Git Commit Guidelines

Please follow the [Angular Git Commit Guidelines](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines).

## 📜 License

Wind Addons projects generally use the MIT or GPLv3 licenses.

However, if the project contains the submodule of another project, the license may differ. Check the project's `LICENSE` file for details.
