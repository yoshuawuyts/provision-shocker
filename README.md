# provision-shocker
Provision a linux instance to run [shocker][0].

## Features
- [x] install [Nix][3] dependencies on [Alpine][2]
- [ ] install Nix
- [ ] install shocker dependencies
- [ ] mount [btrfs][1] copy-on-write subvolume
- [ ] create any missing directories
- [ ] download and link shocker
- [ ] enable a shocker Nix profile (needs investigating)

## Dependencies
This package is fully self-contained and installs all dependencies needed to
run [shocker][0]. On [Alpine][2] it will instrument
[Alpine Package Keeper (apk)][4] to provision the right dependencies to run
[Nix][3].

On systems other than Alpine, `bash` and `curl` are required for `Nix` to run.

## Why?
[shocker][0] provides minimal containers that can be instrumented using shell.
In order to run containers efficiently it uses a [brfs][1] copy-on-write
filesystem and recent versions of some tools. This script installs all
dependencies necessary to run `shocker` without conflicting with the rest of
your OS.

## See Also
- [shocker][0]
- [brfs][1]
- [Alpine Linux][2]
- [Nix package manager][3]
- [Alpine Package Keeper][4]
- [nixos.org/manual][5]

## License
[MIT](https://tldrlegal.com/license/mit-license)

[0]: https://github.com/stamf/shocker
[1]: https://en.wikipedia.org/wiki/Btrfs
[2]: http://alpinelinux.org/
[3]: https://nixos.org/nix/
[4]: http://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management
[5]: http://nixos.org/nix/manual/
