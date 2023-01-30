# Bazel Svelte Example

This repository houses an example of how to use Bazel to build a Svelte application.

It leverages [rules_js][1], [rules_ts][2], [rules_esbuild][3], and [rules_pkg][4] to hermetically build and package the application.

## Prerequisites

[Install Bazel][5] on your development machine.

## Build the app

1. Check out this repository from the local machine
1. From within the repository run `bazel build //:static_tar`
1. The resulting `tar` file will be located under `bazel-bin/static_tar.tar` relative to the directory root

[1]: https://github.com/aspect-build/rules_js
[2]: https://github.com/aspect-build/rules_ts
[3]: https://github.com/aspect-build/rules_esbuild
[4]: https://github.com/bazelbuild/rules_pkg
[5]: https://bazel.build/install
