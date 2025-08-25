# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository manages Homebrew package installations through a Brewfile. It defines a declarative list of formulae (command-line tools) and casks (GUI applications) to be installed on macOS systems.

## Key Commands

### Install all packages from Brewfile
```bash
brew bundle install --file=brewfile
```

### Check which packages would be installed/upgraded
```bash
brew bundle check --file=brewfile
```

### List all dependencies from Brewfile
```bash
brew bundle list --file=brewfile
```

### Clean up packages not listed in Brewfile
```bash
brew bundle cleanup --file=brewfile
```

### Generate a new Brewfile from current system
```bash
brew bundle dump --file=brewfile --force
```

## File Structure

- `brewfile` - Main configuration file containing:
  - Tap repositories (package sources)
  - Formulae (command-line tools)
  - Casks (GUI applications with installation directory set to `/Applications`)

## Working with the Brewfile

When modifying the Brewfile:
- Formulae are added with `brew "package-name"`
- Casks are added with `cask "app-name"`
- Taps are added with `tap "repo/name"`
- The cask application directory is configured at the top of the file