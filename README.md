# Change Management Discovery: [Changeset](https://intuit.github.io/auto/index)
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

## Why ?

Currently we have a lot of inconsistencies in versioning, releasing and managing changelogs across applications and libraries. Partly there is no reasonable versioning in place and changelogs hardly exist, mostly being manually created and managed.

Changeset handles version release and changelog management by actively enforcing the usage of change descriptions. You can collect changes up to a certain point before releasing them in a controlled way.

## Setup

Follow the [guide](https://github.com/changesets/changesets/blob/main/docs/intro-to-using-changesets.md). for initial setup.

## Usage

* Create a new branch
* run `pnpm changeset` and follow prompt

```shell
$ pnpm changeset
🦋  What kind of change is this for @juicyarts/cm-discovery-changesets? (current version is 0.1.0) · minor
🦋  Please enter a summary for this change (this will be in the changelogs).
🦋    (submit empty line to open external editor)
🦋  Summary · This change introduces the source code from the initial discovery project
🦋
🦋  === Summary of changesets ===
🦋  minor:  @juicyarts/cm-discovery-changesets
🦋
🦋  Is this your desired changeset? (Y/n) · true
🦋  Changeset added! - you can now commit it
🦋
🦋  If you want to modify or expand on the changeset summary, you can find it here
🦋  info /Users/yildiz/repos/goingForward/case-studies/change-and-release-mngmnt/cm-discovery-changesets/.changeset/polite-dodos-live.md
```

* Push your branch and open a merge request.

![Screen](docs/changeset%20bot%20detected.png)

* After the merge request is merged changeset will create a new pull request containing the appropriate version bump/s and changelog updates.

![Screen](docs/release%20bot%20merge%20requests.png)

* this is only a request for a version bump, not yet the version bump itself. If we merge this pr changeset will create relevant tags, publish needed packages and write the changelog.

* if we would not not add a changeset to your pr the changeset bot comes into action

![Screen](docs/changeset%20bot%20undetected.png)

* if we add another changeset that does not affect the previous version bump the version stays the same.

![Screen](docs/release%20bot%20merge%20request%20update.png)

* this pr stays open until merged, it updates every time a new changeset lands in the main branch

-----------------------

## Observations

* only works with node based packages
* simple changelog

### pro's

* easy to set up and use
* provides high level of control over _when_ to release
* allows [snapshot releases](https://github.com/changesets/changesets/blob/main/docs/snapshot-releases.md) for testing

### con's

* more active interaction needed
* changelogs don't contain participants
  * could be customized through <https://github.com/changesets/changesets/blob/main/docs/modifying-changelog-format.md>

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://juicyarts.de/"><img src="https://avatars.githubusercontent.com/u/1132937?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Huess</b></sub></a><br /><a href="#infra-juicyarts" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="https://github.com/juicyarts/cm-discovery-changesets/commits?author=juicyarts" title="Tests">⚠️</a> <a href="https://github.com/juicyarts/cm-discovery-changesets/commits?author=juicyarts" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!