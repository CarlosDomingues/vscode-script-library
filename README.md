# vscode-script-library
A slim version of VS Code's / GitHub Codespaces' [bash script library](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library) that can be used as a Git Submodule in other repos. This repo uses GitHub Actions for automatic updates.

## Why?

I wanted to use Microsoft's suberb bash script library, but:

1. I also wanted to keep it up to date automatically.
2. I didn't want to clone their entire repo as a git submodule, as it's over 11 MB in size.

## Installing

1.  Add this repo as a `git` submodule under `./devcontainer/scripts/vscode-script-library` (or your favorite directory):

```shell
git submodule add git@github.com:CarlosDomingues/vscode-script-library.git .devcontainer/scripts/vscode-script-library
```

## Script documentation

[Can be found here.](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library).