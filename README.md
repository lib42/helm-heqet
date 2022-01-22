# Heqet Helm Plugin

A helm plugin for templating heqet configuration into kubernetes resources. It can also be used to e.g. validate your configuration or for CI/CD.
This plugin is part of [Heqet](https://github.com/lib42/heqet).

## Installation

```sh
helm plugin install https://github.com/lib42/helm-heqet.git
```

## Usage

Important: All commands must be executed inside your heqet project, with a `Heqetfile` in the current working directory!

* `helm heqet setup`: Clones heqet & insert your configuration
* `helm heqet update`: Updates heqet after setup
* `helm heqet template`: Templates the Heqet Chart with your config
* `helm heqet validate`: Simple syntax validation test
* `helm heqet generate`: Combination of update & template [for CI/CD usage]
* `helm heqet help`: print help

## Setup

Open a terminal & navigate to your Heqet userdata repository. Make sure a `Heqetfile` is in your current working directory.

Heqet needs to be setup first [e.g. to download the heqet chart]:
```sh
helm heqet setup
```

## Container Image

Additionally there is a container image containing the plugin: `lib42/heqet-cli`
