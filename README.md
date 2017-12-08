# alpine-pkg-git-crypt

[![CircleCI](https://img.shields.io/circleci/project/sgerrand/alpine-pkg-git-crypt/master.svg)](https://circleci.com/gh/sgerrand/alpine-pkg-git-crypt)

This is [`git-crypt`][git-crypt] packaged for [Alpine Linux][alpine-linux].

## Releases

See the [releases page][releases] for the latest download links.

## Installing

The current installation method for these packages is to pull them in using
`wget` or `curl` and install the local file with `apk`:

    apk --no-cache add ca-certificates
    wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://raw.githubusercontent.com/sgerrand/alpine-pkg-git-crypt/master/sgerrand.rsa.pub
    wget https://github.com/sgerrand/alpine-pkg-git-crypt/releases/download/0.6.0-r0/git-crypt-0.6.0-r0.apk
    apk add git-crypt-0.6.0-r0.apk

[alpine-linux]: https://www.alpinelinux.org
[git-crypt]: https://www.agwa.name/projects/git-crypt/
[releases]: https://github.com/sgerrand/alpine-pkg-git-crypt/releases/
