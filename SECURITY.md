# Security policy

Thanks for taking the time to report something. Quiet, early reports are much
appreciated, and you will be credited in the advisory unless you would rather
not be.

## Reporting a vulnerability

Please use GitHub's private reporting rather than a public issue, so a fix can
go out before the details are visible:

**Security → Report a vulnerability**, on the repository in question. The direct
link is `https://github.com/openfluids/<repo>/security/advisories/new`.

That opens a private thread visible only to you and the maintainer.

Helpful to include, as far as you have it: which version and platform, the
smallest input or script that reproduces the problem, and what an attacker
would gain. A partial report is still worth sending — please do not sit on
something because it feels incomplete.

## What happens next

This is a small project maintained by one person, so these are honest targets
rather than a guaranteed SLA:

- an acknowledgement within about a week
- an assessment, and a fix or an explanation of why it is not one, within
  about 30 days
- a released fix and a published advisory before any public disclosure

If a report has gone quiet for two weeks, please do nudge the thread — it means
the notification was missed, not that it was ignored.

## Scope

Fixes go into the latest release of each package; earlier versions are not
backported.

These are scientific and visualization tools, not hardened services. Reports of
crashes, hangs or excessive memory use on deliberately malformed input are
genuinely welcome as **bug reports** in the public tracker — they are usually
robustness problems rather than security ones, and they do not need to be
private.

The reports most worth sending here are ones where a user could be harmed by
running the software normally: arbitrary code execution while loading a data
file, path traversal when writing output, a leaked credential or token, or a
compromised dependency or release artifact.

## Conduct

Please do not test against infrastructure that is not yours, and please do not
access or retain anyone else's data while investigating.
