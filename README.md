## Mason

This project use mason from https://pub.dev/packages/mason



To get all bricks registered in `mason.yaml` run:

```sh
$ mason get
```

Then you can use `mason make` to generate your first file:

```sh
$ mason make hello
```

## Install Brick Templates Globally

The `install` command allows developers to install brick templates globally on their machines from either a local path or git url. Then developers can use globally installed brick templates anywhere (regardless of whether there is an existing `mason.yaml`).

### Install Usage

```sh
# install from path
$ mason install --source path ./path/to/brick

# install from git url
$ mason install --source git https://github.com/user/repo

# install from git url with path
$ mason install --source git https://github.com/user/repo --path path/to/brick

# install from git url with path and ref
$ mason install --source git https://github.com/user/repo --path path/to/brick --ref tag-name

# use alias "i" instead of "install" for a shorthand syntax
# since git is the default source we don't need to specify a source.
$ mason i https://github.com/user/repo
```

Once a brick is installed globally it can be used from anywhere via the `mason make` command:

```sh
$ mason make <BRICK_NAME>
```