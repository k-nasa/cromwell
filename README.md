# Cromwell

[![CircleCI](https://circleci.com/gh/guni1192/cromwell/tree/master.svg?style=svg)](https://circleci.com/gh/guni1192/cromwell/tree/master)
![crates.io](https://img.shields.io/crates/v/cromwell.svg)
![docs](https://docs.rs/cromwell/badge.svg)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/41323aa3cce44cd586d683bdb62f6812)](https://app.codacy.com/app/guni1192/cromwell?utm_source=github.com&utm_medium=referral&utm_content=guni1192/cromwell&utm_campaign=Badge_Grade_Settings)

Rust Rootless Container Runntime

![logo](./logos/facebook_cover_photo_2.png)

## Dependency

Enable user namespaces

```
$ sudo sysctl kernel.unprivileged_userns_clone=1
```

## Installation

```
$ cargo install cromwell
```

or 

```
$ cargo install --git https://github.com/guni1192/cromwell
```

## Usage

```
Rust Rootless Container Runntime

USAGE:
    cromwell [SUBCOMMAND]

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

SUBCOMMANDS:
    help    Prints this message or the help of the given subcommand(s)
    pull    pull oci image
    run     run cromwell container
```

## Example

### Run Container

```bash
$ cromwell run -n library/alpine:3.8
~ $
```

```bash
$ cromwell run -n library/alpine:3.8 --exec 'ls -a'
bin  boot  dev  etc  home  lib  lib64  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
```

### Pull Image from DockerHub

```bash
$ cromwell pull -n library/alpine:3.8
```

## Test

```bash
$ cargo test
```
