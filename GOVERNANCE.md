# Floci Project Governance

## Overview

Floci is an open-source family of local cloud emulators (AWS, Azure, GCP, OCI) and supporting
tooling. The project operates under a **Lead Maintainer** model: a single accountable owner
sets direction and guards the brand, while day-to-day authority over individual repositories
and service areas is delegated to trusted Maintainers.

This document describes who makes decisions, how, and how contributors grow into more
responsibility over time.

## Roles

### Contributor
Anyone who opens an issue, comments, reviews, or submits a pull request. No prior permission
is required. Contributions are accepted under the terms in `CONTRIBUTING.md`.

### Triager
Trusted community members who help manage issues and pull requests: labeling, triaging,
closing duplicates, reproducing bugs. Triagers do **not** have merge rights. Granted by a
Maintainer or the Lead.

### Maintainer
Owns one or more repositories or service areas. A Maintainer may review and merge pull
requests within their area, cut releases for their area, and mentor contributors. Maintainers
are listed in each repository's `MAINTAINERS.md`.

Maintainers may **not**, without Lead approval, change governance, licensing, the trademark
or brand assets, release infrastructure (`.releaserc`, signing keys, publishing credentials),
or the set of Maintainers.

### Lead Maintainer
Hector Ventura (@hectorvent), creator of Floci, is the Lead Maintainer. The Lead holds
final decision authority over project direction, the trademark and brand, licensing, release
infrastructure, and the addition or removal of Maintainers.

The Lead is the sole owner of the `floci-io` GitHub organization and of the official
distribution channels: Docker Hub (`floci/*`), Maven Central (`io.floci`), PyPI, npm,
and the `floci.io` domain and DNS.

## Decision making

- **Day to day:** lazy consensus. A Maintainer for the relevant area reviews and merges. If no
  objection is raised within a reasonable window, a change proceeds.
- **Cross-cutting or contested changes:** discussed openly in GitHub Discussions. If consensus
  is not reached, the Lead makes the final call.
- **Governance, licensing, trademark, brand, and release-infrastructure changes:** decided by
  the Lead.

## Becoming a Maintainer

There is no fixed contribution count. The bar is demonstrated judgment, reliability, and
sustained, high-quality contribution in an area. The path is:

1. A track record of merged contributions and constructive participation in one area.
2. Nomination by an existing Maintainer, or self-nomination via GitHub Discussions.
3. Approval by the Lead.

New Maintainers are scoped to a **specific repository or service area**, such as the
Azure emulator or the Java Testcontainers module, not the organization as a whole.

## Who maintains what

Each repository's own `MAINTAINERS.md` is authoritative. This table is a convenience index so
"who owns X" can be answered without walking every repository.

| Area | Repository | Maintainers |
|---|---|---|
| AWS emulator | `floci` | @hectorvent, @pgermosen |
| Azure emulator | `floci-az` | @hectorvent, @fredpena |
| GCP emulator | `floci-gcp` | @hectorvent |
| OCI emulator | `floci-oci` | @hectorvent, @gioandtonic |
| Web console | `floci-ui` | @fredpena, @hectorvent |
| CLI | `floci-cli` | @hectorvent |
| Testcontainers, Java | `testcontainers-floci` | @cfranzen, @hectorvent |
| Testcontainers, .NET | `testcontainers-floci-dotnet` | @hughesjs, @hectorvent |
| Testcontainers, Go | `testcontainers-floci-go` | @hectorvent |
| Testcontainers, Node | `testcontainers-floci-node` | @hectorvent |
| Testcontainers, Python | `testcontainers-floci-python` | @hectorvent |
| DuckDB executor sidecar | `floci-duck` | @hectorvent |
| Community projects | `floci-labs` | @hectorvent |
| Website | `floci-io.github.io` | @hectorvent |
| Org-level community health files | `.github` | @hectorvent |

Areas showing one name are areas looking for a second. See `CONTRIBUTING.md` and the path above.

## Stepping down and inactivity

Maintainers may step down at any time. Maintainers who are inactive for an extended period may
be moved to **emeritus** status by the Lead, with thanks. Emeritus Maintainers may return by
request.

## Scope of authority

**Delegated to Maintainers (within their area):**
code review and merge, releases, issue triage, mentoring new contributors.

**Reserved to the Lead:**
organization ownership; the trademark and brand; licensing and relicensing; CLA/DCO policy;
publishing credentials and signing keys; release-infrastructure configuration and protected
paths (see `CODEOWNERS`); adding and removing Maintainers; and the direction of any commercial
or hosted offering.

## Open source and commercial relationship

Floci's emulators are MIT-licensed and free, with **no feature gates**: every emulated
service is available to every user, always. Any commercial offering (hosted environments,
SLAs, paid support, governance tooling) is operated separately and **never gates emulated
services**. Contributions to the open-source repositories are accepted under the project's
sign-off policy in `CONTRIBUTING.md`.

## Code of Conduct

All participants are expected to follow the project `CODE_OF_CONDUCT.md`.

## Amending this document

This document is amended by the Lead Maintainer. Material changes are announced in GitHub
Discussions.
