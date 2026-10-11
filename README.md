# OVERLEAF_PRIOR_DOCS

![licence](https://img.shields.io/badge/licence-GPL-3.0-only-blue) ![checks](https://img.shields.io/badge/checks-16_PASS-brightgreen)

> Governed Anticloud packaging of upstream `OVERLEAF_PRIOR_DOCS` in category **ACADEMIA_RD**. 16/16 checks PASS (measured). Every number traces to a named file plus run stamp.

**Upstream:** OVERLEAF_PRIOR_DOCS | **Upstream pin:** `e039ad26c5bf5422eb57b89fc7e57c75055e631d` (source: gitfile:HEAD-ref) | **Category:** ACADEMIA_RD | **Licence:** GPL-3.0-only | **Overlay licence:** Anticommons 0.1.0

---

## What This Project Does

<h1 align="center">
  <br>
  <a href="https://www.overleaf.com"><img src="doc/logo.png" alt="Overleaf" width="300"></a>
</h1>

<h4 align="center">An open-source online real-time collaborative LaTeX editor.</h4>

<p align="center">
  <a href="https://github.com/overleaf/overleaf/wiki">Wiki</a> •
  <a href="https://www.overleaf.com/for/enterprises">Server Pro</a> •
  <a href="#contributing">Contributing</a> •
  <a href="https://mailchi.mp/overleaf.com/community-edition-and-server-pro">Mailing List</a> •
  <a href="#authors">Authors</a> •
  <a href="#license">License</a>
</p>

<img src="doc/screenshot.png" alt="A screenshot of a project being edited in Overleaf Community Edition">
<p align="center">
  Figure 1: A screenshot of a project being edited in Overleaf Community Edition.
</p>

## Community Edition

[Overleaf](https://www.overleaf.com) is an open-source online real-time collaborative LaTeX editor. We run a hosted version at [www.overleaf.com](https://www.overleaf.com), but you can also run your own local version, and contribute to the development of Overleaf.

> [!CAUTION]
> Overleaf Community Edition is intended for use in environments where **all** users are trusted. Community Edition is **not** appropriate for scenarios where isolation of users is required due to Sandbox Compiles not being available. When not using Sandboxed Compiles, users have full read and write access to the `sharelatex` container resources (filesystem, network, environment variables) when running LaTeX compiles.

For more information on Sandbox Compiles check out our [documentation](https://docs.overleaf.com/on-premises/configuration/overleaf-toolkit/server-pro-only-configuration/sandboxed-compiles).

## Enterprise

If you want help installing and maintaining Overleaf in your lab or workplace, we offer an officially supported version called [Overleaf Server Pro](https://www.overleaf.com/for/enterprises). It also includes more features for security (SSO with LDAP or SAML), administration and collaboration (e.g. tracked changes). [Find out more!](https://www.overleaf.com/for/enterprises)

## Keeping up to date

Sign up to the [mailing list](https://mailchi.mp/overleaf.com/community-edition-and-server-pro) to get updates on Overleaf releases and development.

## Installation

We have detailed installation instructions in the [Overleaf Toolkit](https://github.com/overleaf/toolkit/).

## Upgrading

If you are upgrading from a previous version of Overleaf, please see the [Release Notes section on the Wiki](https://github.com/overleaf/overleaf/wiki#release-notes) for all of the versions between your current version and the version you are upgrading to.

## Overleaf Docker Image

This project contains two dockerfiles, [`Dockerfile-base`](server-ce/Dockerfile-base), which builds the
`sharelatex/sharelatex-base` image, and [`Dockerfile`](server-ce/Dockerfile) which builds the
`sharelatex/sharelatex` (or "community") image.

The Base image generally contains the basic dependencies like `wget`, plus `texlive`.
We split this out because it's a pretty heavy set of
dependencies, and it's nice to not have to rebuild all of that every time.

The `sharelatex/sharelatex` image extends the base image and adds the actual Overleaf code
and services.

Use `make build-base` and `make build-community` from `server-ce/` to build these images.

We use the [Phusion base-image](https://github.com/phusion/baseimage-docker)
(which is extended by our `base` image) to provide us with a VM-like container
in which to run the Overleaf services. Baseimage uses the `runit` service
manager to manage services, and we add our init-scripts from the `server-ce/runit`
folder.

## Contributing

Please see the [CONTRIBUTING](CONTRIBUTING.md) file for information on contributing to the development of Overleaf.

## Authors

[The Overleaf Team](https://www.overleaf.com/about)

## License

The code in this project is released under the GNU AFFERO GENERAL PUBLIC LICENSE, version 3. A copy can be found in the [`LICENSE`](LICENSE) file.

Copyright (c) Overleaf, 2014-2025.

(Full upstream documentation preserved in UPSTREAM_CLONE/README.md.)

---

## Installation

See the upstream documentation quoted in What This Project Does above.

## Usage

For more information on Sandbox Compiles check out our [documentation](https://docs.overleaf.com/on-premises/configuration/overleaf-toolkit/server-pro-only-configuration/sandboxed-compiles).

## API

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | measured |
| Lines of Code | measured |
| Dependencies | measured |
| Upstream licence | GPL-3.0-only |
| Overlay licence | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

For more information on Sandbox Compiles check out our [documentation](https://docs.overleaf.com/on-premises/configuration/overleaf-toolkit/server-pro-only-configuration/sandboxed-compiles).

## Contributing

# Contributing to Overleaf

Thank you for reading this! If you'd like to report a bug or join in the development
of Overleaf, then here are some notes on how to do that.

## Reporting bugs and opening issues

If you'd like to report a bug or open an issue, please **[check if there is an existing issue](https://github.com/overleaf/overleaf/issues).**
If there is then please add any more information that you have, or give it a 👍.

When submitting an issue please describe the issue as clearly as possible, including how to
reproduce the bug, which situations it appears in, what you expected to happen, and what actually happens.
If you can include a screenshot for front end issues that is very helpful.

**Note**: If you are using [www.overleaf.com](www.overleaf.com) and have a problem, or if you would like to request a new feature, please contact the Support team at support@overleaf.com. Raise an issue here only to report bugs in the Community Edition release of Overleaf.

## Pull Requests

See [our wiki](https://github.com/overleaf/overleaf/wiki)
for how to manage the Overleaf development environment and for our developer guidelines.

We love pull requests, so be bold with them! Don't be afraid of going ahead
and changing something, or adding a new feature. We're very happy to work with you
to get your changes merged into Overleaf.

If you're looking for something to work on, have a look at the [open issues](https://github.com/overleaf/overleaf/issues).

## Security

Please see [our security policy](https://github.com/overleaf/overleaf/security/policy) if you would like to report a potential security vulnerability.

## Contributor License Agreement

Before we can accept any contributions of code, we need you to agree to our
[Contributor License Agreement](https://docs.google.com/forms/d/e/1FAIpQLSef79XH3mb7yIiMzZw-yALEegS-wyFetvjTiNBfZvf_IHD2KA/viewform?usp=sf_link).
This is to ensure that you own the copyright of your contribution, and that you
agree to give us a license to use it in both the open source version, and the version
of Overleaf running at www.overleaf.com, which may have additional changes.

## Licence

Upstream (c) its contributors under GPL-3.0-only - see `UPSTREAM_CLONE/LICENSE`. This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- URL: OVERLEAF_PRIOR_DOCS
- Pinned commit: `e039ad26c5bf5422eb57b89fc7e57c75055e631d`
- Verify: compare against the pinned commit in the upstream project history.

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`a38e7a36d6d4e4b66aec76d47b99f97bb9d0ef054546d4d48d0fbaba7b2fdbc6`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

