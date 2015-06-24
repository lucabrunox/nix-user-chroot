Run nix as user in a lightweight chrooted container.

1. Create an empty directory somewhere, `mkdir $DIR`
2. Run `nix-user-chroot $DIR bash` as user

You are now in a chroot where `/` is owned by your user, hence you can now install nix under `/nix` as user and run nix commands.
