# Section9Labs Homebrew Tap

Homebrew formulae for [rupu](https://github.com/Section9Labs/rupu), an agentic
code-development CLI.

## Install

```sh
brew install section9labs/tap/rupu
```

Or tap first, then install:

```sh
brew tap section9labs/tap
brew install rupu
```

Works on macOS (Apple Silicon) and Linux (x86_64, aarch64).

## How this tap is maintained

`Formula/rupu.rb` is **generated, not hand-written**. Every stable rupu release
runs a `publish-homebrew` job that rewrites the formula with that release's
version and asset checksums and pushes it here. The generating template lives at
[`packaging/templates/rupu.rb.in`](https://github.com/Section9Labs/rupu/blob/main/packaging/templates/rupu.rb.in)
in the rupu repository.

Edits made directly to `Formula/rupu.rb` are overwritten by the next release.
Fix the template instead.

Prereleases are never published here — the job is gated to stable releases only,
so `brew upgrade` will not move you onto a beta.

## Other install methods

The tap is one of several. See
[rupu's README](https://github.com/Section9Labs/rupu#install) for the install
script, `.deb`/`.rpm` packages, the apt and yum repositories, the AUR package
(`rupu-bin`), and the Nix flake.

## License

Apache-2.0, matching rupu itself. See [LICENSE](LICENSE).
