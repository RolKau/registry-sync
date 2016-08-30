# registry-sync

Synchronizes selected packages and their transitive dependencies from a remote NPM registry (such as https://registry.npmjs.org) to a local folder.
The local copy can then be used as a simple private NPM registry without publishing capabilities.

## Usage

Usage: bin/sync [options]

  Options:

    -h, --help           output usage information
    -V, --version        output the version number
    --root <path>        Path to save NPM package tarballs and metadata to
    --manifest <file>    Path to a package.json file to use as catalog for mirrored NPM packages. Their transitive (production) dependencies are mirrored as well.
    --localUrl <url>     URL to use as root in stored package metadata (i.e. where folder defined as --root will be exposed at)
    --registryUrl [url]  URL to use as NPM registry when fetching packages (defaults to https://registry.npmjs.org)


Usage: bin/server [options]

  Options:

    -h, --help       output usage information
    -V, --version    output the version number
    --root <path>    Path to serve NPM packages from
    --port [number]  Local HTTP port to bind the server to (defaults to 3000)