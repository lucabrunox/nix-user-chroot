Run nix as user in a lightweight chrooted container.

1. Create an empty directory somewhere, `$DIR`
2. Run `nix-user-chroot $DIR bash`

You can now install nix under /nix as user.
