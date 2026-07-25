# Security policy

This policy covers every public repository under [github.com/mantekio](https://github.com/mantekio), including the WordPress must-use plugins.

## Reporting a vulnerability

**Email [security@mantek.io](mailto:security@mantek.io).** Please do not open a public issue for anything exploitable.

Include whatever you have:

- Which plugin and which version (the `Version:` line in the plugin header).
- What an attacker can do, and roughly what access they need to do it.
- Steps to reproduce, or a proof of concept.
- Environment, if it is relevant: WordPress, PHP and MySQL versions.

You will get an acknowledgement within **3 working days** (Sunday to Thursday, GST). We will confirm whether we can reproduce it, tell you what we intend to do, and let you know when a fix ships. If we disagree that something is a vulnerability, we will say so and explain why rather than going quiet.

You are welcome to disclose publicly once a fix is released. If a report is serious and we are slow, chase us rather than sitting on it.

## Scope

**In scope:** anything in these repositories that lets an attacker read or modify data they should not, escalate privileges, or inject SQL or script through the plugin's own code paths.

**Out of scope:** vulnerabilities in WordPress core, in third-party plugins, or in a host's configuration; findings that need an already-compromised administrator account; and reports from automated scanners with no demonstrated impact.

## What we do not offer

No bug bounty. These are small open-source plugins maintained by one engineer, and pretending otherwise would waste your time. Credit in the changelog and the release notes if you want it.

## Supported versions

Only the latest release of each plugin is supported. All of them are pre-1.0 and ship a changelog, so the fix for anything reported will land in a new tagged release rather than a patch to an old one.

---

Maintained by [ManTek Technologies](https://www.mantek.io), Dubai. Our site-wide security posture is at [mantek.io/security](https://www.mantek.io/security).
