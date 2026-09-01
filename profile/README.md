<div align="center">
<img  alt="floci-white" src="https://github.com/user-attachments/assets/edfff8b3-926c-471e-9549-77fb90a21b49#gh-dark-mode-only" width="640"/>

<img alt="floci-black" src="https://raw.githubusercontent.com/floci-io/.github/main/floci.svg#gh-light-mode-only" width="640"/>

### Any cloud. Locally.

**Light, fluffy, and always free. Local cloud emulators for AWS, Azure, GCP, and OCI.**

[![stars floci](https://img.shields.io/github/stars/floci-io/floci?style=flat&color=blue&label=stars%20floci)](https://github.com/floci-io/floci/stargazers)
[![stars floci-az](https://img.shields.io/github/stars/floci-io/floci-az?style=flat&color=blue&label=stars%20floci-az)](https://github.com/floci-io/floci-az/stargazers)
[![stars floci-gcp](https://img.shields.io/github/stars/floci-io/floci-gcp?style=flat&color=blue&label=stars%20floci-gcp)](https://github.com/floci-io/floci-gcp/stargazers)
[![stars floci-oci](https://img.shields.io/github/stars/floci-io/floci-oci?style=flat&color=blue&label=stars%20floci-oci)](https://github.com/floci-io/floci-oci/stargazers)
[![License](https://img.shields.io/badge/license-MIT-green)](https://github.com/floci-io/floci/blob/main/LICENSE)
[![Slack](https://img.shields.io/badge/Slack-join%20the%20community-4A154B?logo=slack&logoColor=white)](https://join.slack.com/t/floci/shared_invite/zt-3tjn02s3q-A00kEjJ1cZxsg_imTfy6Cw)
[![Website](https://img.shields.io/badge/website-floci.io-0ea5e9)](https://floci.io)

</div>

## What is Floci™?

Floci is a family of fast, free, open-source **local cloud emulators** built with Quarkus
Native, with one container per cloud, one port each, no auth tokens, no feature gates, no telemetry.
Around the emulators sits a consistent set of client libraries, tooling, and validation so the
whole suite feels like one project.

Named after [*cirrocumulus floccus*](https://en.wikipedia.org/wiki/Cirrocumulus_floccus), the
cloud formation that looks like popcorn. 🍿

```bash
docker run --rm -p 4566:4566 floci/floci:latest        # AWS
docker run --rm -p 4577:4577 floci/floci-az:latest     # Azure
docker run --rm -p 4588:4588 floci/floci-gcp:latest    # Google Cloud
docker run --rm -p 4599:4599 floci/floci-oci:latest    # Oracle Cloud
```

No sign-ups. No API keys. Point your existing SDK or CLI at the local endpoint and keep your
workflows.

## The suite

| Category | Repos |
| --- | --- |
| **Emulators** | [`floci`](https://github.com/floci-io/floci) (AWS, `:4566`) · [`floci-az`](https://github.com/floci-io/floci-az) (Azure, `:4577`) · [`floci-gcp`](https://github.com/floci-io/floci-gcp) (GCP, `:4588`) · [`floci-oci`](https://github.com/floci-io/floci-oci) (OCI, `:4599`) |
| **Client libraries** | [`testcontainers-floci`](https://github.com/floci-io/testcontainers-floci) (Java) · [`-python`](https://github.com/floci-io/testcontainers-floci-python) · [`-node`](https://github.com/floci-io/testcontainers-floci-node) · [`-go`](https://github.com/floci-io/testcontainers-floci-go) · [`-dotnet`](https://github.com/floci-io/testcontainers-floci-dotnet) |
| **Tooling** | [`floci-cli`](https://github.com/floci-io/floci-cli) · [`floci-ui`](https://github.com/floci-io/floci-ui) |
| **Docs & experimental** | [`floci-io.github.io`](https://github.com/floci-io/floci-io.github.io) · [`floci-duck`](https://github.com/floci-io/floci-duck) |

### The four emulators

- **☁️ AWS** · [`floci`](https://github.com/floci-io/floci) · port `4566` · image `floci/floci`.
  EC2, ECS, EKS, Lambda, RDS, ElastiCache, MSK, OpenSearch, S3, DynamoDB, SQS, SNS, IAM, STS,
  KMS, Step Functions, CloudFormation, and more, validated against its
  [compatibility test suite](https://github.com/floci-io/floci/tree/main/compatibility-tests).
- **☁️ Azure** · [`floci-az`](https://github.com/floci-io/floci-az) · port `4577` · image
  `floci/floci-az`. Blob, Queue, Table, Cosmos DB, Functions, App Configuration, Key Vault,
  Event Hubs, Azure SQL Database, AKS, and Virtual Machines on a single endpoint.
- **☁️ GCP** · [`floci-gcp`](https://github.com/floci-io/floci-gcp) · port `4588` · image
  `floci/floci-gcp`. Cloud Storage, Pub/Sub, Firestore, Datastore, Secret Manager, IAM, and
  Managed Kafka on a single endpoint.
- **☁️ OCI** · [`floci-oci`](https://github.com/floci-io/floci-oci) · port `4599` · image
  `floci/floci-oci`. Identity, Object Storage, Queue, Streaming, Vault + KMS, Secrets, and
  Functions on a single endpoint.

## Always free, no feature gates, MIT forever

Every emulated service is available to every user, always: no auth tokens, no paid unlocks, no
"community edition" sunset. The emulators are MIT-licensed and stay that way. Fork them, embed
them, ship them.

## Release train

Stable releases ship on the **1st and 3rd Tuesday of each month**, across all four emulators.
Between trains, the `nightly` tag on each image (`floci/floci`, `floci/floci-az`,
`floci/floci-gcp`, `floci/floci-oci`) tracks `main`, so every merged fix is available the next
day, and dated `nightly-mmddyyyy` tags let you pin a specific night's build.

Versions come from Conventional Commits by way of semantic-release, and every `CHANGELOG.md` is
generated rather than written by hand.

## Sponsors

Floci is independent open source, funded by the people and companies who use it.
Sponsorship buys gratitude and nothing else: every emulated service is free for
everyone, forever, and no sponsor gets features, priority, or roadmap influence
that the rest of the Flock does not.

### 🥇 Gold

Large logo with top placement in the emulator READMEs and on floci.io, plus a
mention in release notes.

[IceGuard](https://github.com/iceguard) · [Softmax](https://softmax.com/)

### 🥈 Silver

Logo in the emulator READMEs and on floci.io, plus a mention in release notes.

*Your logo here. [Become a sponsor](https://github.com/sponsors/floci-io).*

### 🥉 Community

Name in the emulator READMEs, a sponsor badge on GitHub, and our sincere thanks.

[AutoScout24](https://www.autoscout24.com) · [Nexxion AI](https://nexxion.ai/)

Every sponsor, including the Friends of the Flock who support Floci outside these
tiers, is listed in [THANKS.md](https://github.com/floci-io/.github/blob/main/THANKS.md).

**[Sponsor Floci](https://github.com/sponsors/floci-io)**

## Links

**[Website](https://floci.io)** ·
**[Documentation](https://floci.io)** ·
**[Slack](https://join.slack.com/t/floci/shared_invite/zt-3tjn02s3q-A00kEjJ1cZxsg_imTfy6Cw)** ·
**[Discussions](https://github.com/orgs/floci-io/discussions)** ·
**[Governance](https://github.com/floci-io/.github/blob/main/GOVERNANCE.md)** ·
**[Trademark](https://github.com/floci-io/.github/blob/main/TRADEMARK.md)**

---

<div align="center">

*Built with Quarkus + GraalVM Mandrel · Made for developers who ship.*

Floci™ is a trademark of Hector Ventura. Code is MIT-licensed; see
[TRADEMARK.md](https://github.com/floci-io/.github/blob/main/TRADEMARK.md) for name and logo use.

</div>
