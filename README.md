# forgejo-runner-deb
Debian package for Forgejo Runner

## Prepare
- Put Forgejo Runner [release](https://code.forgejo.org/forgejo/runner/releases) to `usr/bin/` directory with name `forgejo-runner`

## Make package
```bash
apt update & apt install df-make
# Import GPG key for package sign
gpg --import ${KEY_FILE}
dpkg-buildpackage -b -k${KEY_EMAIL}
```

## Runner init
```bash
forgejo-runner create-runner-file --secret <secret>
```
