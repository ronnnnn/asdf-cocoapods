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

# Troubleshooting

## Incompatibility Errors After Updating Ruby
If you encounter errors like the following after updating your Ruby version and running `pod`, it's likely due to a dependency mismatch:

```
~/.asdf/installs/cocoapods/1.15.2/vendor/bundle/ruby/3.3.0/gems/bigdecimal-3.1.4/lib/bigdecimal.rb:4:in `require': linked to incompatible ~/.asdf/installs/ruby/3.3.3/lib/libruby.3.3.dylib - ~/.asdf/installs/cocoapods/1.15.2/vendor/bundle/ruby/3.3.0/gems/bigdecimal-3.1.4/lib/bigdecimal.bundle (LoadError)
```

CocoaPods uses Bundler to manage its dependencies. When you change Ruby versions, you need to redownload these dependencies to ensure compatibility.

### Resolution

1. Navigate to your CocoaPods installation directory:

```bash
cd ~/.asdf/installs/cocoapods/{version}  # Replace {version} with your installed version
```

2. Redownload and reinstall the dependencies:

```bash
bundle install --redownload
```

Now you should be able to run `pod` commands without errors.

# Contributing

Contributions of any kind welcome! See the [contributing guide](contributing.md).

[Thanks goes to these contributors](https://github.com/ronnnnn/asdf-cocoapods/graphs/contributors)!

# License

See [LICENSE](LICENSE) © [Seiya Kokushi](https://github.com/ronnnnn/)
