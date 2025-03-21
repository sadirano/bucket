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

Once the bucket is added, you can install tools from it. For example, to install the **omni** tool, run:

```powershell
scoop install omni
```

## License

This project is released under the [MIT License](LICENSE).
