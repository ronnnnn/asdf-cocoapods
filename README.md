<div align="center">

# asdf-cocoapods [![Build](https://github.com/ronnnnn/asdf-cocoapods/actions/workflows/build.yml/badge.svg)](https://github.com/ronnnnn/asdf-cocoapods/actions/workflows/build.yml) [![Lint](https://github.com/ronnnnn/asdf-cocoapods/actions/workflows/lint.yml/badge.svg)](https://github.com/ronnnnn/asdf-cocoapods/actions/workflows/lint.yml)


[cocoapods](https://cocoapods.org) plugin for the [asdf version manager](https://asdf-vm.com).

</div>

# Contents

- [Dependencies](#dependencies)
- [Install](#install)
- [Contributing](#contributing)
- [License](#license)

# Dependencies

**TODO: adapt this section**

- `bash`, `curl`, `tar`: generic POSIX utilities.
- `SOME_ENV_VAR`: set this environment variable in your shell config to load the correct version of tool x.

# Install

Plugin:

```shell
asdf plugin add cocoapods
# or
asdf plugin add cocoapods https://github.com/ronnnnn/asdf-cocoapods.git
```

cocoapods:

```shell
# Show all installable versions
asdf list-all cocoapods

# Install specific version
asdf install cocoapods latest

# Set a version globally (on your ~/.tool-versions file)
asdf global cocoapods latest

# Now cocoapods commands are available
pod --version
```

Check [asdf](https://github.com/asdf-vm/asdf) readme for more instructions on how to
install & manage versions.

# Contributing

Contributions of any kind welcome! See the [contributing guide](contributing.md).

[Thanks goes to these contributors](https://github.com/ronnnnn/asdf-cocoapods/graphs/contributors)!

# License

See [LICENSE](LICENSE) © [Seiya Kokushi](https://github.com/ronnnnn/)
