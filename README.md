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
