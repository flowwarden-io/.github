# Contributing to FlowWarden

Thank you for your interest in contributing to a FlowWarden project! Every contribution matters — whether it's a bug report, a feature suggestion, a documentation fix, or a code change.

This document covers the **organization-wide policies** that apply to every `flowwarden-io` repository (DCO, sign-off, commit conventions, review process, license). Each project may add a short per-repo `CONTRIBUTING.md` for its specific development setup (build commands, language versions, package layout). When in doubt, the per-repo file overrides this one.

All participants are expected to follow the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).

## Ways to Contribute

> **Please open an issue before submitting a PR**, both for bug fixes and new features. This avoids wasted work on changes that may not align with the project direction, and keeps reviews focused.

- **Report bugs** — Open an issue with clear reproduction steps, expected vs. actual behavior, and your environment. For non-trivial bugs, please provide a **runnable test case** (pushed to your fork) that isolates the issue. This dramatically speeds up triage and resolution.
- **Suggest features** — Open an issue describing the use case and why it would benefit the project.
- **Submit pull requests** — Code, tests, documentation improvements are all welcome.
- **Improve documentation** — Typos, unclear explanations, missing examples — every bit helps.

## Commit & PR Guidelines

- Use [Conventional Commits](https://www.conventionalcommits.org/) format:
  `feat:`, `fix:`, `docs:`, `test:`, `refactor:`, `chore:`
- Open PRs against `main`.
- Describe the **why**, not just the what.
- Reference the related issue (`Closes #123`).
- One PR = one topic. Keep changes focused.
- **Update `CHANGELOG.md`** when present: any user-visible change (new feature, bug fix, breaking change, deprecation) must add an entry under the `[Unreleased]` section, in the appropriate category (`Added`, `Changed`, `Fixed`, `Deprecated`, `Removed`, `Security`). Internal-only changes (refactors, tests, CI) don't need a changelog entry.

### Squash strategy

- **Before opening the PR:** rebase on `main` and squash your work-in-progress commits into a small number of meaningful commits. The reviewer should see a clean history, not your local trial-and-error.
- **During code review:** do **not** squash. Each round of review feedback should land as its own commit (e.g., `review: rename variable X`). This lets reviewers verify only what changed instead of re-reading the whole PR. The final history is squashed automatically at merge time via "Squash and merge".

## Review Process

- Every PR is reviewed by at least one maintainer.
- CI must be green before merge.
- Changes to the public API require prior discussion via an issue.
- Be patient — we review as fast as we can; FlowWarden projects are maintained as side projects.
- Stale PRs and issues with no activity for an extended period may be flagged and eventually closed. Reopening is always welcome with fresh context.

## License

All contributions to a FlowWarden project are submitted under that project's license (typically the [Apache License 2.0](LICENSE)). By opening a pull request, you agree that your contribution will be licensed under the project's same license.

When a project enforces license headers on source files, the CI build runs a license check. If you add a new source file, ensure the header is present (most projects expose a `mvn license:format` or equivalent task).

## Developer Certificate of Origin (DCO)

We use the [Developer's Certificate of Origin 1.1 (DCO)](https://developercertificate.org/) — the same lightweight mechanism used by the Linux kernel and many other open source projects — instead of a formal CLA.

Each commit must include a `Signed-off-by` line in its message:

```text
Signed-off-by: Jane Doe <jane.doe@example.com>
```

Add it automatically by committing with the `-s` flag:

```bash
git commit -s -m "feat: add new feature"
```

Or configure git once to sign every commit:

```bash
git config --global format.signOff true
```

A DCO bot enforces this on every pull request. Commits without the sign-off will block the merge.

## Signed commits (cryptographic)

Most FlowWarden repositories require commits to be cryptographically signed (SSH or GPG) as part of branch protection on `main`. This is **distinct from DCO sign-off**: DCO attests the legal origin, the cryptographic signature attests the commit hasn't been tampered with.

To enable SSH signing once:

```bash
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

Then register the public key on GitHub as a **Signing Key** (distinct from Authentication Key) under `Settings → SSH and GPG keys`.

Full guide: [GitHub docs on signing commits](https://docs.github.com/en/authentication/managing-commit-signature-verification).
