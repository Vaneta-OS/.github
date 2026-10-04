## What

<!-- The change in a few sentences. Link the issue or the task: Closes #123, VANETA-ISO-001 -->

## Why

<!-- The reason behind it. This is what a reviewer cannot read from the diff. -->

## How it was tested

<!-- CI runs, commands, virtual machine scenarios (UEFI, BIOS, encrypted, upgrade), and screenshots for visible changes. -->

## Checklist

<!-- Tick what applies; delete what clearly does not. -->

- [ ] The title follows Conventional Commits: `type(scope): lowercase subject`
- [ ] CI is green
- [ ] The task is updated, and an ADR exists for an architecture change
- [ ] Packages: `pkgver` or `pkgrel` bumped, checksums updated, namcap clean or explained
- [ ] Boot, initramfs, installer or disk layout: tested in UEFI and BIOS virtual machines
- [ ] Desktop: `docs/macos-parity.md` updated in `desktop`, screenshots attached
- [ ] Third-party code, artwork, fonts or sounds: license recorded in `NOTICE`; no Apple assets
- [ ] Security-sensitive: the risk and the rollback are described above
- [ ] No secrets, no AI attribution, no em dashes or emoji
