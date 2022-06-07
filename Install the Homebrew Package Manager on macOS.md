## Preface
[Homebrew](https://brew.sh) is a package manager for Mac that gives users a Linux-like methodology for installing software on Mac. A lot of common software is available as [Formulae](https://formulae.brew.sh/formula/) and [Casks](https://formulae.brew.sh/cask/) for Homebrew. 

## Workflow
1. Open Terminal
2. Copy the following command and paste into the terminal:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)”
```
3. Once the installation is complete, the terminal will provide two further commands that must be run in order for the Brew path to be evaluated

## Operations and Maintenance
1. All programmes installed with Homebrew can be upgraded by executing `brew upgrade`.
	1. If Oh My ZSH is setup per the tutorial, the command `bubc` will upgrade and cleanup all packages
