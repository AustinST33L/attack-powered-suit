[![build](https://github.com/center-for-threat-informed-defense/attack-powered-suit/actions/workflows/build.yml/badge.svg)](https://github.com/center-for-threat-informed-defense/attack-powered-suit/actions/workflows/build.yml)
[![codecov](https://codecov.io/gh/center-for-threat-informed-defense/attack-powered-suit/branch/main/graph/badge.svg?token=ejCIZhBRGr)](https://codecov.io/gh/center-for-threat-informed-defense/attack-powered-suit)

# ATT&CK Powered Suit

- [ATT&CK Powered Suit](#attck-powered-suit)
  - [Questions and Feedback](#questions-and-feedback)
  - [Guidance](#guidance)
    - [Getting Started](#getting-started)
    - [Proposing Changes](#proposing-changes)
    - [Updating Dependencies](#updating-dependencies)
  - [How Do I Contribute?](#how-do-i-contribute)
  - [Developers](#developers)
    - [Developer Setup](#developer-setup)
    - [Unit Tests](#unit-tests)
    - [Upgrading ATT&CK](#upgrading-attck)
    - [Releasing a New Version](#releasing-a-new-version)
  - [Notice](#notice)

## Questions and Feedback

Please submit issues for any technical questions/concerns or contact
ctid@mitre-engenuity.org directly for more general inquiries.

Also see the guidance for contributors if are you interested in contributing or
simply reporting issues.

## Guidance

### Getting Started

TODO

### Proposing Changes

* Please open a [Pull
  Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
  (PR) against the `main` branch for any desired changes. The PR will be
  reviewed by the project team.
* Note that all PR checks must pass to be eligible for merge approval.

### Updating Dependencies

TODO

## How Do I Contribute?

We welcome your feedback and contributions to help advance ATT&CK Powered Suit.
Please see the guidance for contributors if are you interested in [contributing
or simply reporting issues.](/CONTRIBUTING.md)

Please submit
[issues](https://github.com/center-for-threat-informed-defense/attack_powered_suite/issues)
for any technical questions/concerns or contact ctid@mitre-engenuity.org
directly for more general inquiries.

## Developers

### Developer Setup

To set up a development environment, you first need to [install Node.JS and
NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm). Then
clone this repository and run the following commands.

```shell
$ cd src
$ npm install
$ npm run fetch-attack
$ npm run build-index
$ npm run dev
```

At this point, the dev server is running and will automatically recompile after
you change any source code files. You can develop and debug the code by visiting
[localhost:8080](http://localhost:8080). This view will automatically reload
each time the source code is saved, which is useful for rapid development
cycles.

Alternately, you can load it as an extension into chrome:

1. Go to the extensions settings.
2. Make sure "Developer mode" is enabled.
3. Click "Load unpacked" and select the `attack_powered_suite/src` directory.
4. The extension will appear in the extension list and is now usable.

### Unit Tests

To run the test suite:

```shell
$ npm run test
```

Alternately, use "watch" mode to automatically re-run tests each time you modify
the source code:

```shell
$ npm run watch-test
```

The test suite writes code coverage data to `./coverage/`. For more information
on writing unit tests, see:

* [Unit Testing Svelte
  Components](https://sveltesociety.dev/recipes/testing-and-debugging/unit-testing-svelte-component/)
* [Testing Library Svelte
  API](https://testing-library.com/docs/svelte-testing-library/api).
* [Testing Library
  API](https://testing-library.com/docs/queries/about/#types-of-queries)

### Upgrading ATT&CK

To upgrade the extension to use a newer version of ATT&CK, there are a few
changes that need to be made:

* `fetch-attack.js`: update `attackUrls`

### Releasing a New Version

Use NPM to generate a new version number:

```shell
$ npm version minor
v0.2.0
```

NPM automatically does the following:

* Put new version number in `package.json` and `manifest.json`.
* Commit those changes.
* Create a new Git tag.

If you are satisfied with the changes, you just need to push them, e.g.

```shell
$ git push
$ git push origin v0.2.0

## Notice

Copyright 2021 MITRE Engenuity. Approved for public release. Document number
XXXXX

Licensed under the Apache License, Version 2.0 (the "License"); you may not use
this file except in compliance with the License. You may obtain a copy of the
License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.

This project makes use of ATT&CK®

[ATT&CK Terms of Use](https://attack.mitre.org/resources/terms-of-use/)
