# setup-CSC
[![Actions Status](https://github.com/yoavain/Setup-CSC/workflows/PR%20Checks/badge.svg)](https://github.com/yoavain/Setup-CSC/actions)
![types](https://img.shields.io/npm/types/typescript.svg)
![commit](https://img.shields.io/github/last-commit/yoavain/Setup-CSC.svg)
[![Known Vulnerabilities](https://snyk.io//test/github/yoavain/Setup-CSC/badge.svg?targetFile=package.json)](https://snyk.io//test/github/yoavain/Setup-CSC?targetFile=package.json)
[![Renovate](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com)
![used by](https://img.shields.io/endpoint?url=https%3A%2F%2Fapi-git-master.endbug.vercel.app%2Fapi%2Fgithub-actions%2Fused-by%3Faction%3Dyoavain%2FSetup-CSC%26badge%3Dtrue)
![visitors](https://visitor-badge.glitch.me/badge?page_id=yoavain.Setup-CSC)


This action sets up csc.exe as a CLI tool for use in actions by:
- optionally downloading and caching a version of VSWhere.exe to help find the latest CSC on the machine
- Adds the location of the CSC to the PATH


# Usage

Basic:
```yaml
steps:
name: ASP.NET CI
on: [push]
jobs:
  build:
    runs-on: windows-latest

    steps:
    - uses: actions/checkout@master

    - name: Setup csc.exe
      uses: yoavain/Setup-CSC@v5

    - name: CSC
      working-directory: src
      run: csc source.cs
```


# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

# Contributions

Contributions are welcome!  See [Contributor's Guide](docs/contributors.md)
