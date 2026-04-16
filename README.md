# OpenDev SDK — Desktop (prebuilt JAR)

**Language:** English (default) · [简体中文](README.zh-CN.md)

This repository contains a **prebuilt JVM JAR** for the **OpenDev SDK** (`jvm("desktop")` target). Use it for GitHub-based consumption before **Maven Central** publishing.

> **Brand:** Public name **OpenDev SDK**. References to **Walknote** are examples only.

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
