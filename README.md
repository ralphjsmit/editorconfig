# Personal Editor Configuration

This repository houses the editorconfiguration I use for my projects and packages. Because the config is not static and may subject to change, I created this repository in order to synchronize the file across my projects.

## Installation

Run the following commands in a project to fetch the latest version of the editorconfig:

```bash
git remote add editorconfig git@github.com:ralphjsmit/editorconfig.git
git remote set-url --push editorconfig DISABLED
git remote -v
git fetch editorconfig
git checkout editorconfig/main .editorconfig
# Commit editorconfig to your own repos history
```

## Updating the editorconfig

Run the following commands in order to update the editorconfig to the latest version:
```bash
git fetch editorconfig
git checkout editorconfig/main .editorconfig
# Commit editorconfig to your own repos history
```

## Shell aliases

Add the following aliases to your `.zshrc` or `.bashrc` file to speed up the process:

```shell
alias editorConfig="git remote add editorconfig git@github.com:ralphjsmit/editorconfig.git && git remote set-url --push editorconfig DISABLED && git remote -v && git fetch editorconfig && git checkout editorconfig/main .editorconfig"
alias fetchEditorConfig="git fetch editorconfig && git checkout editorconfig/main .editorconfig"
alias ec="editorConfig"
alias fec="fetchEditorConfig"
```
