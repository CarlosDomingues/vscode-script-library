# vscode-script-library

A slim, up-to-date fork of VS Code's [bash script library](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library) optimized to be used as a [Git Submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

Scripts live under the `release` branch. 

## ✔️ Installing

```bash
# You can use your favorite directory instead of .devcontainer/scripts/vscode-script-library
git submodule add -b release git@github.com:CarlosDomingues/vscode-script-library.git .devcontainer/scripts/vscode-script-library
git commit -am "Added vscode-script-library."
```

Now you can write your `Dockerfile` like so:

```Dockerfile
COPY --chown=<user>:<user> --chmod .devcontainer/scripts/vscode-script-library/common-debian.sh /usr/local/bin/common-debian.sh
RUN common-debian.sh
```

## ❌ Removing

```bash
git submodule deinit .devcontainer/scripts/vscode-script-library
git rm .devcontainer/scripts/vscode-script-library
git commit -am "Removed vscode-script-library submodule"
rm -rf .devcontainer/scripts/vscode-script-library
```

## 🤷 Why? 

Because Git does not support clonning a specific part of a repository and vscode-dev-containers has over 10 MB in size.

## 📚 Documentation

[Can be found here](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library)
