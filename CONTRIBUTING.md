# Contributing to Vaneta OS

Vaneta OS is a commercial operating system. Its repositories are private and open to members of the Vaneta OS organization and to invited contractors. This page explains how changes reach the code; the [Code of Conduct](CODE_OF_CONDUCT.md) explains how we work with each other.

## Before you start

- Start from the workspace repository: it carries the shared rules, the architecture, the decision records and the task list, and it clones every other repository for you.
- Check whether a task or an issue already covers the work, and say that you are taking it.
- A change to the architecture (boot chain, packaging, installer, update mechanism, desktop foundations) needs an architecture decision record before the implementation.

## Branches

| Branch                            | Purpose                                                      |
| --------------------------------- | ------------------------------------------------------------ |
| `main`                            | Always releasable. Changes arrive only through pull requests |
| `feat/...`                        | New functionality                                            |
| `fix/...`                         | A bug fix                                                    |
| `docs/...`, `ci/...`, `chore/...` | Documentation, CI, maintenance                               |
| `hotfix/...`                      | An urgent fix for released software                          |

Branch from `main` and keep branches short-lived.

## Commit messages

Commits follow [Conventional Commits](https://www.conventionalcommits.org/):

```text
type(scope): lowercase subject without a final period

The body explains why the change was made; the diff already shows what.
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`, `security`, `config`, `deps`, `hotfix`, `rollback`, `locale`, `ux`, `release`. The scope is the area or package touched, for example `feat(iso): add the boot check unit`.

Write in English, plainly. No em dashes, no emoji, and no attribution lines for tools. A shared commit-msg hook and CI check these rules.

## Pull requests

- One pull request per repository; a change across repositories is merged in dependency order (shared CI, components, packages, ISO).
- The title follows the commit rules, because the squash merge turns it into the commit subject on `main`.
- Fill in the template: what changed, why, and how it was tested. Attach screenshots for anything visible.
- CI must pass. Changes to boot, the installer or the disk layout are tested in UEFI and BIOS virtual machines.
- Mark an unfinished pull request with the `do-not-merge` label.

## Releases

Components use semantic versions (`v1.2.0`); ISO images use the year and month (`v26.10`). A version tag starts the release workflow; nothing is uploaded by hand. Tags are annotated and never reused.

## Assets and licenses

Every third-party file (code, artwork, fonts, sounds) needs a license that allows redistribution and an entry in the repository's `NOTICE`. Apple's fonts, icons, wallpapers, sounds, logos and product names are never used.

## Security

Never put passwords, tokens, keys or personal data in commits, issues, pull requests or screenshots. Report vulnerabilities as described in [SECURITY.md](SECURITY.md).
