# Change Management Discovery: [Changeset](https://intuit.github.io/auto/index)

## Why ?

Currently we have a lot of inconsistencies in versioning, releasing and managing changelogs across applications and libraries. Partly there is no reasonable versioning in place and changelogs hardly exist, mostly being manually created and managed.

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

## Gimmicks

* Changeset bot checks pull requests for changeset
