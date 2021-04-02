# go-ipfs-routing

DAOT Labs's fork of [ipfs/go-ipfs-routing](https://github.com/ipfs/go-ipfs-routing).

[![](https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat-square)](http://ipn.io)
[![](https://img.shields.io/badge/project-DAOT%20Labs-red.svg?style=flat-square)](http://github.com/daotl)
[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)
[![Build Status](https://travis-ci.org/daotl/go-ipfs-routing.svg?branch=master)](https://travis-ci.org/daotl/go-ipfs-routing)

> go-ipfs-routing provides go-libp2p-routing implementations used in go-ipfs.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Contribute](#contribute)
- [License](#license)

## Install

`go-ipfs-routing` works like a set of regular Go packages:

```
> go get github.com/daotl/go-ipfs-routing/...
```

This module uses [Gx](https://github.com/whyrusleeping/gx) to manage
dependencies. You can use `make all` to build it with the `gx` dependencies.

## Usage

This repo contains 3 different packages.

### Mock

[![GoDoc](https://godoc.org/github.com/daotl/go-ipfs-routing/mock?status.svg)](https://godoc.org/github.com/daotl/go-ipfs-routing/mock)

```
import "github.com/daotl/go-ipfs-routing/mock"
```

Mock is a fake router useful for tests. It provides a mock client that
implements the `IpfsRouting` interface and a mock server from which the client
retrieves routing records.


### Offline

[![GoDoc](https://godoc.org/github.com/daotl/go-ipfs-routing/offline?status.svg)](https://godoc.org/github.com/daotl/go-ipfs-routing/offline)

```
import "github.com/daotl/go-ipfs-routing/offline"
```

Offline is an offline router that can put and get records to and from a local
`Datastore` but can't retrieve them from the network.

### None

[![GoDoc](https://godoc.org/github.com/daotl/go-ipfs-routing/none?status.svg)](https://godoc.org/github.com/daotl/go-ipfs-routing/none)

```
import "github.com/daotl/go-ipfs-routing/none"
```

None is a router no-op router that doesn't do anything. Puts always succeed and
lookups always fail.

## Contribute

PRs accepted.

Small note: If editing the README, please conform to the
[standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

Copyright for portions of this fork are held by Protocol Labs, Inc. as part of the original
[go-ipfs-routing](https://github.com/ipfs/go-ipfs-routing) project. All other copyright for
this fork are held by DAOT Labs. All rights reserved.
