# Contributing

Testing Locally:

```shell
asdf plugin test <plugin-name> <plugin-url> [--asdf-tool-version <version>] [--asdf-plugin-gitref <git-ref>] [test-command*]

#
asdf plugin test cocoapods https://github.com/ronnnnn/asdf-cocoapods.git "pod --version"
```

Tests are automatically run in GitHub Actions on push and PR.
