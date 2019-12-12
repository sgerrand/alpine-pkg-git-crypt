# alpine-pkg-git-crypt

:warning: Deprecate :warning:

This was [`git-crypt`][git-crypt] packaged for [Alpine Linux][alpine-linux]. It is now [available in Alpine Linux's aports repository][alpine-linux-package-search], so please install it from there using `apk add git-crypt`.

## Releases

See the [releases page][releases] for the latest download links.

## Installing

The current installation method for these packages is to pull them in using
`wget` or `curl` and install the local file with `apk`:

    apk --no-cache add ca-certificates
    wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://raw.githubusercontent.com/sgerrand/alpine-pkg-git-crypt/master/sgerrand.rsa.pub
    wget https://github.com/sgerrand/alpine-pkg-git-crypt/releases/download/0.6.0-r1/git-crypt-0.6.0-r1.apk
    apk add git-crypt-0.6.0-r1.apk

[alpine-linux]: https://www.alpinelinux.org
[git-crypt]: https://www.agwa.name/projects/git-crypt/
[alpine-linux-package-search]: https://pkgs.alpinelinux.org/packages?name=git-crypt
