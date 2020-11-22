# Amanda's Home IT

This repo tracks the progress of my home IT server that runs on a Raspberry Pi 4B.

# Getting started

In order to get started with this project, a few tools are required on the control node.
This README assumes you are using a Mac OS X system as the control node.

> Note: see the Wiki for information about getting started on
> [Debian-based](https://github.com/amandamabbott/home-it/wiki/Debian-Project-Setup) Linux
> systems.

## Python 3

On Mac OS X, it's recommended to install Python 3 using Homebrew, like so:

```bash
$ brew install python3
```

## virtualenv

This project uses [Poetry](https://github.com/python-poetry/poetry) to manage its Python
dependencies,

On Mac OS X, it's recommended to install Poetry by running the following command:

```bash
$ curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
```

Poetry uses the `pyproject.toml` and `poetry.lock` files to track dependencies. Install the
project dependencies, like so:

```bash
$ cd home-it
$ poetry install
```

## Test the connection via an Ansible ad-hoc command

Ansible connects to managed nodes via SSH. Load your SSH private key into `ssh-agent` by
running the following command:

```bash
$ ssh-add ~/.ssh/id_rsa
```

Ping the managed node (the Raspberry Pi 4B) to verify the connection:

```bash
$ poetry run ansible home_it -m ping
```
