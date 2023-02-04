# Bazel Svelte Example

This repository houses an example of how to use Bazel to build a Svelte application.

It leverages [rules_js][1], [rules_ts][2], [rules_esbuild][3], and [rules_pkg][4] to hermetically build and package the application.

## Prerequisites

[Install Bazel][5] on your development machine.

## Development

1. Run `bazel run //dev/server`
1. Navigate to <localhost:8080>

To enable live-reload run with [Bazel watcher][6].

## Build the app

1. From within the repository run `bazel build //:static_tar`
1. The resulting `tar` file will be located under `bazel-bin/static_tar.tar` relative to the directory root

## Hold on, this doesn't look like a Svelte app!

This example is the bare-bones minimum to build a Svelte app. It does not contain any of the syntactic sugar such as `+page.svelte` provided by the [Vite][7] compiler in [SvelteKit][9]. This example compiles and bundles using [esbuild][8] instead.

For an example of how to use Vite check out <https://github.com/mikberg/bazel-vite>.

[1]: https://github.com/aspect-build/rules_js
[2]: https://github.com/aspect-build/rules_ts
[3]: https://github.com/aspect-build/rules_esbuild
[4]: https://github.com/bazelbuild/rules_pkg
[5]: https://bazel.build/install
[6]: https://github.com/bazelbuild/bazel-watcher
[7]: https://vitejs.dev/
[8]: https://esbuild.github.io/
[9]: https://kit.svelte.dev/
