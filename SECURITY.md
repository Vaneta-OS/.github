# Security Policy

Vaneta OS runs on the computers people rely on every day, and its updates arrive with full system privileges. A vulnerability can cost someone their data or their machine, so every report is handled privately.

## Reporting a vulnerability

Do not report security problems in public issues, pull requests, discussions or social media.

Report through GitHub's private vulnerability reporting: [Report a vulnerability](https://github.com/Vaneta-OS/.github/security/advisories/new). Members of the organization can also tell the project lead directly.

Include what you can:

- The affected part: live ISO, installer, boot chain, package repository or updates, a Vaneta package, a service, CI or build infrastructure.
- The Vaneta OS version, and whether it happens on a live system, an installed system or a virtual machine.
- Steps to reproduce, and a proof of concept if you have one.
- What an attacker gains, and how bad it is.

Test only on systems you own. Do not access other people's data, and do not run load or denial-of-service tests against Vaneta OS infrastructure.

## What matters most

- Anything that lets someone else's code run with the privileges of an update: tampered packages or databases, a weakness in package signing or in the keyring.
- Privilege escalation through Vaneta services, polkit rules, or the installer.
- Default network exposure: a service that listens without a reason.
- Weaknesses in the boot chain or disk encryption setup.
- Secrets or signing material exposed by the build infrastructure.

Out of scope: scanner output with no working impact, and issues in upstream software that Vaneta ships unchanged (report those upstream; we will help if you ask).

## How we respond

- Critical and high severity problems are fixed before anything else, and before the details become public.
- Medium and low severity problems are fixed in the next scheduled release.
- Fixes are recorded in the changelog of the affected component once it is safe to mention them, and reporters are credited if they wish.

## Supported versions

The latest ISO release and the packages currently in the stable `vaneta` repository.

## Languages

Reports in English or Indonesian.
