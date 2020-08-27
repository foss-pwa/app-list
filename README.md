# app-list
List of foss PWAs for use in foss-pwa app store

## How to add an app?

- Check the app meets the conditions
- Build yaml representation of the app based on schema
- Open a new issue

## Conditions

- The app must be available online.
- Source code must be available online, under a (OSI or FSF approved) license.
  - Source code must include every library, dependency, and entire build system
- When including donation information, That must be available on source code readme or inside application.
- The app must have (at least) a webmanifest
- The app should do some kind of computations. Content-only websites may be rejected.
- The app must not abuse users or other kind of illegal behaviours.

## Schema

The yaml representation of the app should have following structure:

```yaml
id: foss_pwa_app_store # your app name. must be unique, and contain only [0-9a-z_]
source: # MANDATORY
  # if it is on github:
  type: github
  repository: foss-pwa/app-store # e.g. your-username/repo
  # else, open an issue
category: # an array of categories available here. open an issue for suggesting a category
  - game # for games
  - tool # like camera, barcode scanner, speed meter, ...
  - social # for social networks and related apps
  - dev # for everything related to programming
  - music # for everything that make a sound
antifeature: # an array of antifeatures possible. open an issue for suggesting a category
  - nfbackend # depend on some non free backend or api
  - nfasset # use copyrighted assets
lang: # MANDATORY, main part, place of (possibly) localized contents
  en: # MANDATORY (at least one), Or any language code in navigator.languages like fa, en-US, ...
    manifest: https://foss-pwa.org/manifest.json # MANDATORY, url of manifest
    keyword: # list of key words
      - app
      - index
  fa: # Add as many languages as supported
    manifest: https://foss-pwa.org/manifest.fa.json # Could be the same url with en, We fetch it with diffrent Accept-language header
    keyword:
      - برنامه
```

## Maintainer
We need maintainer. Call me on mastodon (https://norden.social/@hamid) if you are volunteer.

