# Contributing to Roxabi

Roxabi ships open-source primitives that compound. You're reading this because
you want to add to them — thanks.

This file is the org-wide default. A repository may override it with its own
`CONTRIBUTING.md`; if it does, that one wins.

## License: AGPL-3.0, both directions

Everything here is **AGPL-3.0**. Inbound matches outbound: what you contribute
is licensed under AGPL-3.0, the same terms the project ships under.

What that means in practice:

- **Read it, learn from it, reimplement an idea elsewhere** — free, no strings.
  The license covers code, not ideas.
- **Run it or self-host it for yourself** — free, no obligation.
- **Ship a service or product built on it** — your derivative stays open
  (AGPL §13 covers network-facing services, not just distributed binaries).

Inspiration is free. Building on it means building in the open.

## Two things on every contribution

**1. Sign off your commits (DCO).** Every commit must carry a `Signed-off-by`
line certifying you wrote the change or have the right to submit it. Add it
automatically with `git commit -s`. The full text is in [`DCO.txt`](./DCO.txt).

```
Signed-off-by: Your Name <you@example.com>
```

**2. Agree to the CLA.** By opening a pull request you agree to the
[Contributor License Agreement](./CLA.md). You keep ownership of your work; the
CLA grants Roxabi the rights needed to maintain the project and to keep a
commercial-licensing option open, which is how the open-source work is funded.
Every released version stays AGPL-3.0 for everyone — the CLA does not let the
project go closed.

## Workflow

1. Open an issue first for anything non-trivial — it's cheaper to align before
   the code than after.
2. Fork, branch, build. Match the surrounding code: its naming, its idioms, its
   comment density.
3. Keep the change focused. One concern per pull request.
4. `git commit -s`, push, open the PR. Describe what changed and why.

## Reporting security issues

Don't open a public issue for a vulnerability. See `SECURITY.md` if present, or
email mickael@bouly.io.

---

Questions belong in GitHub Discussions or an issue. The people who built this
are there.
