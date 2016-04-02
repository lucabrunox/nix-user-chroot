Run nix as user in a lightweight chrooted container.

```
$ mkdir -m 0755 ~/nix && chown $(whoami) ~/nix
$ nix-user-chroot ~/.nix sh
$ download and extract latest nix binary tarball
$ nix-*-linux/install
```

You are in a user chroot where `/` is owned by your user, hence also `/nix` is owned by your user. Everything else is bind mounted from the real root.

Notes:

- The nix config is not in `/etc/nix` but in `/nix/etc/nix`, so that you can modify it. This is done with the `NIX_CONF_DIR`, which you can override at any time.
- It requires user namespaces, at least Linux 3.8.
