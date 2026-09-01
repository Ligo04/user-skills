---
name: zsh-config-summary
description: Summarize a portable Zsh setup for Linux and macOS using Oh My Zsh and Oh My Posh. Use when asked about shell startup files, the selected plugins, or the bundled prompt configuration; do not assume host-specific paths or versions.
---

# Portable Zsh Configuration

Use this configuration without assuming a fixed username, Zsh executable location, package-manager prefix, or system-wide configuration directory.

## Shell and Startup Files

- Locate Zsh with `command -v zsh`; its executable location differs across Linux distributions, package managers, and macOS installations.
- Resolve the user startup directory as `${ZDOTDIR:-$HOME}`.
- `.zshenv` is read for every Zsh invocation. It may source `$HOME/.cargo/env` when that file exists.
- `.zprofile` and `.zlogin` apply to login shells, `.zshrc` applies to interactive shells, and `.zlogout` applies when a login shell exits.
- System-wide startup files may also be loaded; their directories differ between Linux and macOS.
- `.profile` is not a native Zsh startup file, although a desktop or login session may pass its environment into Zsh.

## Framework, Plugins, and Prompt

- Oh My Zsh is loaded from `$ZSH`, commonly set to `$HOME/.oh-my-zsh`.
- `ZSH_THEME` is empty because the prompt is provided by Oh My Posh rather than an Oh My Zsh theme.
- Enabled plugins: `git`, `zsh-autosuggestions`, `zsh-syntax-highlighting`, and `z`.
- Oh My Posh loads the bundled [amro.omp.json](amro.omp.json). Resolve it relative to this Skill or copy it to a chosen configuration directory and reference it through an environment variable; do not embed a machine-specific path.
- The two-line prompt shows the user, full working directory, active Python environment, Git upstream/branch/stash state, and a root indicator.
