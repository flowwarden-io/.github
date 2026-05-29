# `.github` — Default community health files for `flowwarden-io`

This repository hosts the **default community health files** for the [flowwarden-io](https://github.com/flowwarden-io) organization.

GitHub automatically uses these files as fallbacks for any repo in the org that does not define its own version. See [GitHub's docs on default community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).

## What lives here

| File | Applies to |
|---|---|
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | All `flowwarden-io` repos |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Generic policies (DCO, sign-off, commit conventions, review) — each project may add a short per-repo override for dev setup |
| [`SECURITY.md`](SECURITY.md) | Generic vulnerability reporting process — each project may keep a per-repo `SECURITY.md` for its "Supported Versions" table |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Auto-applied on new PRs |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Auto-applied on new issues |
| [`.github/FUNDING.yml`](.github/FUNDING.yml) | Sponsorship config |
| [`profile/README.md`](profile/README.md) | Org landing page at [github.com/flowwarden-io](https://github.com/flowwarden-io) |

## What stays per-repo

`LICENSE`, `README.md`, `CHANGELOG.md`, `.github/CODEOWNERS`, `.github/dependabot.yml`, and `.github/workflows/*.yml` cannot be inherited from this repo and must be present in every project.

## License

The content of this repository is licensed under the [Apache License 2.0](LICENSE).
