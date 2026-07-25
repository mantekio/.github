# Contributing

These are small, single-file WordPress must-use plugins, each one extracted from a problem we hit running WordPress at scale and each paired with an article explaining it. Issues and pull requests are welcome. This page is mostly about what makes them easy to accept.

## What these projects are, and are not

Every plugin here is deliberately **one file, no dependencies, no build step**. That is a constraint, not an accident: they get dropped into `wp-content/mu-plugins/` on servers we do not always control. A change that introduces a package manager, a framework, or a second file has to justify itself.

They also aim to be **narrow**. Each solves one problem completely rather than several partially. The READMEs carry a "Known limits" section, and the things listed there are usually out of scope on purpose, not oversights. If you want to change something in that section, open an issue first so we can agree on it before you write code.

## Reporting a bug

Use the issue form and **fill in the environment fields**. This matters more here than in most projects: every real bug found in these plugins so far depended on the environment, and the instructive ones were invisible from reading the code. Versions, the table collation, and the FULLTEXT token size are usually what makes a report reproducible.

For anything exploitable, email [security@mantek.io](mailto:security@mantek.io) instead of opening an issue. See [SECURITY.md](SECURITY.md).

## Pull requests

- **Open an issue first** for anything beyond a typo or an obvious fix, so nobody writes code that gets declined on scope.
- **Match the surrounding style.** WordPress coding standards, tabs, Yoda conditions, and the same comment density. The comments in these files explain *why* a thing is done, especially where the obvious approach is wrong; please keep that habit rather than stripping it.
- **Say how you verified it.** These plugins have almost no unit tests, because most of what can break needs a real database: the query planner, the collation, the CLI, the hooks. So "I ran it" is the evidence that counts. Tell us the WordPress, PHP and MySQL versions you ran against, and what you observed.
- **One change per pull request.** Two unrelated fixes in one branch take twice as long to review and cannot be reverted independently.
- **Bump nothing.** Leave the version header and the changelog alone; releases are cut by the maintainer.

## A note on the tone of the code

Where a check exists, it is usually there because something once reported success while doing nothing. If you are touching a status command, a health check, or an error path, the bar is that **a check that cannot fail is not a check**. Please do not make one quieter to tidy it up.

## Licence

All of these plugins are GPL-2.0-or-later, the same as WordPress. By contributing you agree your changes ship under that licence.

---

Maintained by [ManTek Technologies](https://www.mantek.io), Dubai.
