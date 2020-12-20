# Install the Homebrew Package Manager on macOS
## Preface
[Homebrew](https://brew.sh) is a package manager for Mac that gives users a Linux-like methodology for installing software on Mac. A lot of common software is available as [Formulae](https://formulae.brew.sh/formula/) and [Casks](https://formulae.brew.sh/cask/) for Homebrew.
> **NOTE:** It is recommended to install iTerm2 prior to following this tutorial as it is much more customisable than Apple’s Terminal. It may be downloaded [here](https://iterm2.com/downloads.html).  

## Workflow
1. Open iTerm2 (if installed) or Terminal
2. Copy the following command and paste into the terminal:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)”
```

## Operations and Maintenance
All programmes installed with Homebrew can be upgraded by executing `brew upgrade`.