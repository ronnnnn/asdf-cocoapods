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

- `bash`, `curl`, `tar`: generic POSIX utilities.
- [Ruby](https://www.ruby-lang.org/en/) (>= 1.9)
  - [RubyGems](https://rubygems.org/?locale=en): manage Ruby packages.
- [Bundler](https://bundler.io): make downloaded cocoapods binary executable.

## Recommendation

Use Ruby and Bundler installed via asdf.

- [asdf-vm/asdf-ruby](https://github.com/asdf-vm/asdf-ruby)
- [jonathanmorley/asdf-bundler](https://github.com/jonathanmorley/asdf-bundler)

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
