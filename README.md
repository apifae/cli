# apifae/cli

**This repository holds release binaries. It contains no source code.**

APIFae's CLI is developed in a private repository. This repository exists so
that the compiled binaries have a public, stable home that package managers can
download from — nothing more. There is no source to read here, no issue tracker,
and pull requests cannot be accepted.

- Product and documentation: <https://apifae.com>
- Install instructions: <https://apifae.com/docs/getting-started>

## Installing

Do not download assets from this repository's Releases page directly. Every
published channel resolves through `https://apifae.com/dl/...`, which rewrites
onto a function that counts the download and then redirects to the asset for
the version you asked for. That indirection is what lets the storage backend
move without breaking a Homebrew formula that is already sitting in someone's
tap.

```sh
# macOS and Linux (Homebrew / Linuxbrew)
brew install apifae/tap/apifae

# macOS and Linux (shell installer)
curl -fsSL https://apifae.com/install.sh | sh

# Windows (Scoop)
scoop bucket add apifae https://github.com/apifae/scoop-bucket
scoop install apifae

# Any platform with Node.js
npm install -g apifae
npx apifae --help
```

## Verifying a download

Each release publishes a `dist-manifest.json` listing every artifact with its
target triple and SHA-256. That manifest is the integrity source — verify
against it, not against the URL you fetched from.

## Reporting a problem

Email <hello@apifae.com>. Issues opened here are not monitored.

## Licence

The binaries are distributed under MIT OR Apache-2.0.
