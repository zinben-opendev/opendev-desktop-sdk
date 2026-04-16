# OpenDev SDK — Desktop (prebuilt JAR)

**Documentation:** English (default) · [简体中文](README.zh-CN.md)

This repository contains a **prebuilt JVM JAR** for the **OpenDev SDK** (`jvm("desktop")` target). Use it for GitHub-based consumption before **Maven Central** publishing.

> **Brand:** Public name **OpenDev SDK**. References to **Walknote** are examples only.

## Technical stack (languages)

| Aspect | What this repo contains / uses |
|--------|--------------------------------|
| **SDK implementation (source, not in this repo)** | **Kotlin Multiplatform** `jvm("desktop")` → **JVM bytecode** in **`opendev-sdk.jar`**. |
| **Artifacts here** | Precompiled **JAR** (and optionally `-sources.jar`) — no Java/Kotlin source tree. |
| **Typical consumer apps** | **Kotlin** or **Java** on the **JVM** (Compose Desktop / Swing / CLI, etc.) via Gradle `files(...)` or Maven when published. |

## Contents

- `opendev-sdk.jar`
- `CHECKSUMS.sha256`
- `sbom/` — resolved **Desktop runtime** Maven coordinates
- `opendev-sdk-sources.jar` — present only if published with `WALKNOTE_OPENDEV_DIST_INCLUDE_SOURCES=1` (omitted by default for public binary repos)

## Gradle

```kotlin
dependencies {
    implementation(files("libs/opendev-sdk.jar"))
}
```

For Maven coordinates (`io.github.zinben-opendev:opendev-desktop-sdk`), follow the OpenDev publishing guide when Central is enabled.

## Integration notes

- Initialize the SDK with your CDN / channel / environment configuration.
- Desktop builds often bundle logging; keep secrets out of VCS.

## Process

See **`Docs/01-SDK/SDK_GITHUB_BINARIES_DISTRIBUTION.md`** in the Walknote monorepo (maintainer-facing).

## License

See [LICENSE](LICENSE).
