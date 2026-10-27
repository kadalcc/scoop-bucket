# Kadal's Scoop bucket

[Kadal Deck](https://deck.kadal.cc/) for Windows through [Scoop](https://scoop.sh/): the desktop
app and the `kadal-deck` command.

```powershell
scoop bucket add kadal https://github.com/kadalcc/scoop-bucket

# The desktop app (Windows 10 or 11, x64)
scoop install kadal/kadal-deck

# The command-line tool, from npm @kadal/deck (Scoop installs Node.js LTS alongside it)
scoop install kadal/kadal-deck-cli
```

`scoop update kadal-deck` moves to a new release; the app also updates itself in the background,
checking every update against Kadal's signature. The installer is not Authenticode-signed yet.

On winget instead? `winget install Kadal.KadalDeck` works once the package is accepted into
[winget-pkgs](https://github.com/microsoft/winget-pkgs) (submitted, in review).

## What is here

| Path                         | What it is                                                                 |
| ---------------------------- | -------------------------------------------------------------------------- |
| `bucket/kadal-deck.json`     | The desktop app: Kadal's NSIS installer, run silently into Scoop's folder   |
| `bucket/kadal-deck-cli.json` | `kadal-deck`, the npm package `@kadal/deck` installed into Scoop's folder   |
| `chocolatey/kadal-deck/`     | The Chocolatey package's source (its `packageSourceUrl`), for when it's listed |

The manifests are generated from the published files by Kadal's release pipeline (`checkver` and
`autoupdate` are filled in too); please open an issue rather than a pull request that edits them.
Bugs in the app or the CLI: <https://github.com/kadalcc/deck/issues>.

The manifests in this repository are MIT-licensed. Kadal Deck itself is free to use
([terms](https://deck.kadal.cc/terms/)); the `@kadal/deck` engine and CLI are AGPL-3.0-or-later.
