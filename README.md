# vscode-script-library
A slim version of VS Code's / GitHub Codespaces' [bash script library](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library) that can be used as a [Git Submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) in other repos. This repo uses GitHub Actions for automatic updates.

Scripts live in the `release` branch. 

## Installing

1.  Add this repo as a `git` submodule under `./devcontainer/scripts/vscode-script-library` (or your favorite directory):

```shell
git submodule add -b release git@github.com:CarlosDomingues/vscode-script-library.git .devcontainer/scripts/vscode-script-library
```

2. Now you can use the scripts in a `Dockerfile` like so:

```Dockerfile
COPY --chown=<user>:<user> --chmod .devcontainer/scripts/vscode-script-library/common-debian.sh /usr/local/bin/common-debian.sh
RUN common-debian.sh
```

## Removing

```shell
git submodule deinit .devcontainer/scripts/vscode-script-library
git rm .devcontainer/scripts/vscode-script-library
git commit -am "Removed vscode-script-library submodule"
rm -rf .devcontainer/scripts/vscode-script-library
```

## Why?

I wanted to use Microsoft's suberb bash script library, but:

1. I also wanted to keep it up to date automatically.
2. I didn't want to clone their entire repo as a git submodule, as it's over 11 MB in size.

## Script documentation

[Can be found here](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library)
