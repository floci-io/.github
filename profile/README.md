<div align="center">
<img  alt="floci-white" src="https://github.com/user-attachments/assets/edfff8b3-926c-471e-9549-77fb90a21b49#gh-dark-mode-only" width="640"/>

<img alt="floci-black" src="https://raw.githubusercontent.com/floci-io/.github/main/floci.svg#gh-light-mode-only" width="640"/>

### Any cloud. Locally.

**Light, fluffy, and always free. Zero cost. Zero compromise.**

[![Stars](https://img.shields.io/github/stars/floci-io/floci?style=flat&color=blue)](https://github.com/floci-io/floci/stargazers)
[![License](https://img.shields.io/badge/license-MIT-green)](https://github.com/floci-io/floci/blob/main/LICENSE)
[![Slack](https://img.shields.io/badge/Slack-join%20the%20community-4A154B?logo=slack&logoColor=white)](https://join.slack.com/t/floci/shared_invite/zt-3tjn02s3q-A00kEjJ1cZxsg_imTfy6Cw)
[![Website](https://img.shields.io/badge/website-floci.io-0ea5e9)](https://floci.io)

</div>

## What is Floci?

Floci is a family of fast, free, open-source **local cloud emulators** built with Quarkus Native. One container per cloud, one port each, no auth tokens, no feature gates, no telemetry. Ever.

Named after [*cirrocumulus floccus*](https://en.wikipedia.org/wiki/Cirrocumulus_floccus), the cloud formation that looks like popcorn. 🍿

```bash
docker run --rm -p 4566:4566 floci/floci:latest        # AWS
docker run --rm -p 4577:4577 floci/floci-az:latest     # Azure
docker run --rm -p 4588:4588 floci/floci-gcp:latest    # Google Cloud
```

That's it. No sign-ups. No API keys.

## Why this org exists

LocalStack's community edition [sunset in March 2026](https://blog.localstack.cloud/the-road-ahead-for-localstack/), now requiring auth tokens and frozen security updates. Microsoft's Azure emulators are fragmented across Azurite, Cosmos DB Emulator (Windows-only), and Functions Core Tools. Google ships per-service `gcloud beta emulators` that each run on a different port with different config.

Floci fills all of that with one consistent emulator family, and stays MIT-licensed forever.

| | Floci | LocalStack Community | Azurite + friends | `gcloud` emulators |
| --- | --- | --- | --- | --- |
| Auth token | None | Required (since March 2026) | N/A | N/A |
| Unified endpoint | **One port per cloud** | One port | Per-service | Per-service |
| Startup time (AWS) | **~24 ms** | ~3.3 s | n/a | n/a |
| Idle memory (AWS) | **~13 MiB** | ~143 MiB | n/a | n/a |
| Docker image size | **~90 MB** | ~1.0 GB | varies | varies |
| License | **MIT** | Restricted | varies | varies |
| Real Docker engines | ✅ Lambda, RDS, EKS, MSK, … | ❌ | partial | partial |

## Clouds

### ☁️ Floci for AWS

**[github.com/floci-io/floci](https://github.com/floci-io/floci)** · port `4566` · image `floci/floci`

41 services including EC2, ECS, EKS, Lambda, RDS, ElastiCache, MSK, OpenSearch, ECR, CodeBuild, S3, DynamoDB, SQS, SNS, IAM, STS, KMS, Cognito, EventBridge, Step Functions, CloudFormation, API Gateway, and more. 100% SDK compatibility (1,925 / 1,925 tests).

### ☁️ Floci-az for Azure

**[github.com/floci-io/floci-az](https://github.com/floci-io/floci-az)** · port `4577` · image `floci/floci-az`

Blob, Queue, Table, Cosmos DB, Functions, App Configuration, Key Vault, and Event Hubs on a single endpoint. Drop-in alternative to running Azurite, Cosmos DB Emulator, and Functions Core Tools side by side.

### ☁️ Floci-gcp for Google Cloud

**[github.com/floci-io/floci-gcp](https://github.com/floci-io/floci-gcp)** · port `4588` · image `floci/floci-gcp`

Cloud Storage, Pub/Sub, Firestore, Datastore, Bigtable, Spanner, and Cloud Functions on a single endpoint. One container instead of seven separate `gcloud beta emulators` processes.

## Supporting projects

### Sidecars

- **[floci-duck](https://github.com/floci-io/floci-duck)**: a DuckDB-backed query sidecar that powers Athena and Firehose.

### Testcontainers modules

- **[testcontainers-floci](https://github.com/floci-io/testcontainers-floci)**: Java, published to Maven Central as [`io.floci:testcontainers-floci`](https://central.sonatype.com/artifact/io.floci/testcontainers-floci).
- **[testcontainers-floci-python](https://github.com/floci-io/testcontainers-floci-python)**: Python.
- **[testcontainers-floci-node](https://github.com/floci-io/testcontainers-floci-node)**: Node.js.
- **[testcontainers-floci-go](https://github.com/floci-io/testcontainers-floci-go)**: Go.

## What makes it different

**Real engines, not mocks.** Lambda, RDS, ElastiCache, ECS, EC2, EKS, MSK, OpenSearch, ECR, and CodeBuild spin up real Docker containers and speak real wire protocols (RESP, JDBC, k8s, IMDS). IAM auth and SigV4 validation work the same as production AWS. The same philosophy carries over to Azure Functions and Cloud Functions in the sibling emulators.

**Drop-in replacement.** Same ports. Same wire protocols. Switch from LocalStack, Azurite, or `gcloud emulators` by changing your endpoint URL with zero application code changes.

**Consistent across clouds.** Same Quarkus Native foundation, same storage architecture (memory / hybrid / persistent / WAL), same Testcontainers patterns. Learn one Floci, you've learned them all.

## Get involved

- 💬 **[Join Slack](https://join.slack.com/t/floci/shared_invite/zt-3tjn02s3q-A00kEjJ1cZxsg_imTfy6Cw)** for questions, feedback, and popcorn-fueled brainstorms
- 🗣️ **[GitHub Discussions](https://github.com/orgs/floci-io/discussions)** for feature ideas, design tradeoffs, and half-baked thoughts
- 🐛 Open an issue on the cloud you're using: [AWS](https://github.com/floci-io/floci/issues) · [Azure](https://github.com/floci-io/floci-az/issues) · [GCP](https://github.com/floci-io/floci-gcp/issues)
- 📖 **[Read the docs](https://floci.io/floci/)** for quick start guides, configuration, and per-service details

## License

Everything in this org is **MIT licensed**. Fork it, embed it, ship it. No "community edition" sunset. No enterprise feature flags.

<div align="center">

*Built with Quarkus + GraalVM Mandrel · Made for developers who ship.*

**[floci.io](https://floci.io)** · **[Documentation](https://floci.io/floci/)** · **[Blog](https://hectorvent.dev/posts/introducing-floci/)**

</div>
