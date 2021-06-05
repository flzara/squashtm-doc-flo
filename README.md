# Squash TM Documentation

🚨🚨 This is the **previous** official repository for Squash TM documentation. It has been transfered to a [new home on GitLab](https://gitlab.com/squashtest/doc/squashtm-doc-fr/) were contributions should be done. This repository is archived and read-only.

It is

- Done in markdown
- Generated using [MkDocs](https://www.mkdocs.org)

## Contributing to this documentation

You may contribute directly respecting the markdown syntax after cloning this repository. However of you want to generate the preview website, please read on.

### Prerequisite installation

How to install MkDocs to contribute to this documentation

> For windows, we will consider you are using [*Chocolatey*](https://chocolatey.org/) to manage your installation. If its note the case, you may install prerequisites manually. You must be install to do it.
> Under Linux, commands are Debian-based.

First install **Git** and **Python 3.7+**

For windows (using an administrative shell):

```cmd
choco install git python
```

For Linux :

```sh
sudo apt install git python3 python3-pip python3-venv
```

### Retrieve documentation

```sh
git clone https://github.com/squash-test/squashtm-doc.git
cd squashtm-doc
```

### MkDocs Installation

> If you know Python well enough, you may setup a virtual environnement before to keep your installation clean. `gitignore` contains an exclusion for a `.venv/` directory for this purpose.

MkDocs is a Python software. Once the latter is installed, the former is just a couple command away:

```sh
pip install wheel
pip install -r requirements.txt
```

Check that it works

```sh
$ mkdocs --version
mkdocs, version 1.1.2
```

### Useful commands

- `mkdocs serve` - Start the live-reloading docs server.
- `mkdocs build` - Build locally the documentation website. By default it is build under the `site/` directory. That's why it is declared in  `.gitignore`.
- `mkdocs -h` - Print help message and exit.

### Good practices

- Please configure your editor to
    - Use `CRLF` as End Of Line
    - Use spaces for tabs
    - Use a tab size of 4
