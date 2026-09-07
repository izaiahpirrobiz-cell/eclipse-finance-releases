# Eclipse Finance — downloads

Installers for **Eclipse Finance**, a local-first desktop bookkeeping app.

Grab the newest build from [Releases](../../releases).

| Platform | File |
| --- | --- |
| Windows | `EclipseFinance-Setup-<version>.exe` |
| macOS | `EclipseFinance-<version>.dmg` |
| Linux | `EclipseFinance-<version>.AppImage` |

The app updates itself: once installed it checks this repository for newer
releases and offers them. `latest.yml`, `latest-mac.yml` and the `.blockmap`
files alongside each installer are what it reads to do that — they are not
useful to download by hand, and removing them breaks updating for everyone
already running the app.

## Why this repository exists

It holds installers and nothing else. The source lives in a separate private
repository.

The app's updater has to reach its feed without credentials, so the
repository it reads must be public. The alternative — a private feed —
would mean shipping a GitHub token inside the app, where anyone who
downloaded it could read it. Publishing only the installers avoids that
trade: there is nothing here that is not already being handed to every
person who downloads the app.

## A note on the Windows warning

Builds are not yet code signed, so Windows SmartScreen will warn before it
runs the installer. That warning means "we have not seen this publisher
enough times to vouch for it", not "this is known to be harmful".
