# Bucket

This repository is a collection of Scoop manifests for my tools.

## Adding the Bucket to Scoop

To add this bucket to your Scoop installation, open PowerShell or CMD and run:

Already have scoop and git installed ?
```powershell
scoop bucket add sadirano https://github.com/sadirano/bucket
```

From scratch ?
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
scoop install git
scoop bucket add sadirano https://github.com/sadirano/bucket
```

Optional (nice to have):
```powershell
scoop add bucket extras
```

## Installing Tools

Once the bucket is added, you can install tools from it. For example, to install the **nix** tool, run:

```powershell
scoop install nix
```

## Nightly Channel

**nix-nightly** installs a rolling build of `nix`'s `main` branch, rebuilt daily.
It shares the same `nix.exe` as the stable `nix` package, so install one or the
other, not both:

```powershell
scoop install sadirano/nix-nightly
```

Scoop only re-pulls a nightly-versioned package once its global `UPDATE_NIGHTLY`
config is enabled (off by default, every `nightly-*` version otherwise compares
as equal, so `scoop update` sees nothing to do):

```powershell
scoop config UPDATE_NIGHTLY true
```

## License

This project is released under the [MIT License](LICENSE).
