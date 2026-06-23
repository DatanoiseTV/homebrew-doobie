# homebrew-doobie

Homebrew tap for [**Doobie**](https://github.com/DatanoiseTV/doobie) — an
analog dub delay plug-in (VST3, AU, Standalone) for macOS.

## Install

```sh
brew tap DatanoiseTV/doobie
brew install --cask doobie
```

The cask drops Doobie into the standard macOS plug-in / app locations:

- `~/Library/Audio/Plug-Ins/Components/Doobie.component` (AU)
- `~/Library/Audio/Plug-Ins/VST3/Doobie.vst3` (VST3)
- `/Applications/Doobie.app` (Standalone)

It also strips the Gatekeeper quarantine attribute from each on install
via `xattr -cr`, which is currently required because the macOS build is
unsigned while the Apple Developer agreement is being re-accepted.

## Updating

```sh
brew update
brew upgrade --cask doobie
```

## Uninstalling

```sh
brew uninstall --cask doobie
brew untap DatanoiseTV/doobie    # optional
```

## Source of truth

The cask is authored in the main Doobie repo at
[`packaging/homebrew/Casks/doobie.rb`](https://github.com/DatanoiseTV/doobie/tree/main/packaging/homebrew/Casks/doobie.rb)
and copied here on each release. File issues against the main repo, not
this tap.
