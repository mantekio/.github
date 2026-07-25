<!--
Thanks for this. Keep it short; the only section that really matters is "How you
verified it". If this is a typo or a one-line doc fix, delete everything except
the first line and open it.
-->

## What this changes, and why

<!-- One or two sentences. If it fixes an issue, write "Fixes #123" so it closes on merge. -->

## How you verified it

<!--
These plugins have almost no unit tests, because most of what can break needs a
real database: the query planner, the collation, the CLI, the hooks. So running it
IS the evidence. Tell us what you ran it against.
-->

- WordPress:
- PHP:
- MySQL / MariaDB:
- What you observed:

## Checks

- [ ] There is an issue for this, or it is small enough not to need one.
- [ ] Still one file, no dependencies, no build step.
- [ ] No version bump and no changelog edit (releases are cut by the maintainer).
- [ ] One change only. Two unrelated fixes belong in two pull requests.
- [ ] If I touched a status command, a health check or an error path, it can still fail. A check that cannot fail is not a check.
