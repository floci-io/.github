<div align="center">

<img src="https://github.com/floci-io/floci/raw/main/floci_banner.svg" alt="Floci" width="640" />

### Light, fluffy, and always free.

**Local AWS. Zero cost. Zero compromise.**

[![Stars](https://img.shields.io/github/stars/floci-io/floci?style=flat&color=blue)](https://github.com/floci-io/floci/stargazers)
[![License](https://img.shields.io/badge/license-MIT-green)](https://github.com/floci-io/floci/blob/main/LICENSE)
[![Slack](https://img.shields.io/badge/Slack-join%20the%20community-4A154B?logo=slack&logoColor=white)](https://join.slack.com/t/floci/shared_invite/zt-3tjn02s3q-A00kEjJ1cZxsg_imTfy6Cw)
[![Website](https://img.shields.io/badge/website-floci.io-0ea5e9)](https://floci.io)

</div>

---

## What is Floci?

Floci is a fast, free, open-source **AWS emulator** built with Quarkus Native — and a free **Azure emulator** too. Drop-in replacement for LocalStack with no auth token, no feature gates, no telemetry. Ever.

Named after [*cirrocumulus floccus*](https://en.wikipedia.org/wiki/Cirrocumulus_floccus) — the cloud formation that looks like popcorn. 🍿

```bash
docker run --rm -p 4566:4566 floci/floci:latest
```

That's it. All 41 services on `:4566`. No sign-ups. No API keys.

## Why this org exists

LocalStack's community edition [sunset in March 2026](https://blog.localstack.cloud/the-road-ahead-for-localstack/) — requiring auth tokens and freezing security updates. Floci fills that gap completely, and stays MIT-licensed forever.

| | Floci | LocalStack Community |
| --- | --- | --- |
| Auth token | None | Required (since March 2026) |
| Startup time | **~24 ms** | ~3.3 s |
| Idle memory | **~13 MiB** | ~143 MiB |
| Docker image size | **~90 MB** | ~1.0 GB |
| License | **MIT** | Restricted |
| EC2 / ECS / EKS / RDS / ElastiCache / MSK | ✅ Real Docker engines | ❌ |
| SDK compatibility | 100% (1,925 / 1,925) | Partial |

## Projects

### Core

- **[floci](https://github.com/floci-io/floci)** — the AWS emulator. 41 services, port 4566, GraalVM native.
- **[floci-az](https://github.com/floci-io/floci-az)** — the Azure emulator. Blob, Queue, Table, Functions on port 4577.
- **[floci-duck](https://github.com/floci-io/floci-duck)** — DuckDB-backed query sidecar that powers Athena.

### Testcontainers modules

- **[testcontainers-floci](https://github.com/floci-io/testcontainers-floci)** — Java module. Published to Maven Central as [`io.floci:testcontainers-floci`](https://central.sonatype.com/artifact/io.floci/testcontainers-floci).
- **[testcontainers-floci-python](https://github.com/floci-io/testcontainers-floci-python)** — Python module.
- **[testcontainers-floci-node](https://github.com/floci-io/testcontainers-floci-node)** — Node.js module.
- **[testcontainers-floci-go](https://github.com/floci-io/testcontainers-floci-go)** — Go module.

### Quality

- **[floci-compatibility-tests](https://github.com/floci-io/floci-compatibility-tests)** — 1,925 cross-SDK tests covering Java v2, Node.js v3, boto3, Go v2, Rust, AWS CLI, Terraform, OpenTofu, and CDK.
- **[floci-io.github.io](https://github.com/floci-io/floci-io.github.io)** — the [floci.io](https://floci.io) website source.

## What makes it different

**Real engines, not mocks.** Lambda, RDS, ElastiCache, ECS, EC2, EKS, MSK, OpenSearch, ECR, and CodeBuild spin up real Docker containers and speak real wire protocols (RESP, JDBC, k8s, IMDS). IAM auth and SigV4 validation work the same as production AWS.

**SDK source is the contract.** Every service is validated against the actual SDK deserializers — not the AWS prose docs. If the Rust SDK panics on an empty XML body ([#11](https://github.com/floci-io/floci/issues/11)), that's a Floci bug. We fix the wire, not the docs.

**Drop-in replacement.** Same port 4566. Same wire protocols. Switch from LocalStack by changing your endpoint URL — zero application code changes.

## Get involved

- 💬 **[Join Slack](https://join.slack.com/t/floci/shared_invite/zt-3tjn02s3q-A00kEjJ1cZxsg_imTfy6Cw)** — questions, feedback, popcorn-fueled brainstorms
- 🗣️ **[GitHub Discussions](https://github.com/orgs/floci-io/discussions)** — feature ideas, design tradeoffs, half-baked thoughts welcome
- 🐛 **[Open an issue](https://github.com/floci-io/floci/issues)** — bug reports, missing operations, SDK incompatibilities
- 📖 **[Read the docs](https://floci.io/floci/)** — quick start, configuration, per-service guides

## License

Everything in this org is **MIT licensed**. Fork it, embed it, ship it. No "community edition" sunset. No enterprise feature flags.

<div align="center">

---

*Built with Quarkus + GraalVM Mandrel · Made for developers who ship.*

**[floci.io](https://floci.io)** · **[Documentation](https://floci.io/floci/)** · **[Blog](https://hectorvent.dev/posts/introducing-floci/)**

</div>
