# Brainrot Brawl development content

An iOS Addressables development-content channel for Brainrot Brawl. This repository stores versioned manifests, catalogs, and Unity asset bundles; it does not contain the game's Unity source project or a playable application build.

## Repository layout

| Area | Contents |
| --- | --- |
| [manifests/dev/](manifests/dev/) | Development-channel client manifests |
| [content/dev/](content/dev/) | Versioned iOS catalogs and asset bundles |
| [.nojekyll](.nojekyll) | Static-hosting configuration marker |

The retained `dev-20260424-144242` payload includes a catalog/hash pair, a remote-menu bundle, and five remote-arena bundles.

## Current manifest state

The committed [latest manifest](manifests/dev/latest.json) points to `dev-20260503-force-local-1777847540`. That manifest sets `forceFallbackScene` to `true`, leaves `remoteCatalogUrl` empty, and records `minClientBuild` as `1777847540`.

The older [dev-20260424-144242 manifest](manifests/dev/dev-20260424-144242.json) records a remote catalog URL with fallback disabled. It remains in the repository alongside its versioned payload. A retained payload should not be assumed to be the content selected by the latest manifest.

## Client integration

A compatible Brainrot Brawl client must interpret the manifest fields and load the matching Addressables content. The client implementation, Unity build settings, bundle-generation workflow, release approval process, and current host behavior are not documented here. These need to be verified in the source project before changing a channel pointer or distributing content to users.

This repository is an artifact channel, not a standalone setup tutorial or code-library showcase. No current device/content-load test or playable demo is claimed.

## License and provenance

No redistribution license or complete asset-source inventory is included. Bundled game assets need the project's own ownership and third-party license review; public artifact hosting does not establish general reuse permission.
