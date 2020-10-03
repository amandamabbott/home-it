# Amanda's Home IT

This repo tracks the progress of my home IT server that runs on a Raspberry Pi 4B.

# Getting started

In order to get started with this project, a few tools are required on the control node.
This README assumes you are using a Mac OS X system as the control node.

> Note: see the Wiki for information on getting started on Linux systems.

## virtualenv

This project uses Pipenv to track some of its dependencies,

On Mac OS X, it's recommended to manage your tools with Homebrew. Run the following
commands to install Pipenv:

```bash
$ brew install python3
$ brew install pipenv
```

Now install the project dependencies, like so:

```bash
$ pipenv install
```
