# OpenDev SDK — Desktop（预构建 JAR）

**语言说明：** 默认以英文 [`README.md`](README.md) 为准；本页为简体中文补充。

本仓库提供 **OpenDev SDK**（`jvm("desktop")`）的 **预构建 JVM JAR**，用于在 **Maven Central** 未发布时通过 **GitHub** 依赖。

> **品牌：** 对外产品名为 **OpenDev SDK**。**Walknote** 仅作示例。

## 产物

- `opendev-sdk.jar`
- `CHECKSUMS.sha256`
- `sbom/` — Desktop runtime Maven 坐标
- `opendev-sdk-sources.jar` — 仅当发版方设置 `WALKNOTE_OPENDEV_DIST_INCLUDE_SOURCES=1` 时存在（公开仓默认常不含）

## Gradle

```kotlin
dependencies {
    implementation(files("libs/opendev-sdk.jar"))
}
```

Maven 坐标见 OpenDev 发布文档（Central 就绪后）。

## 集成注意

- 使用 CDN / channel / environment 初始化 SDK。
- 日志与配置勿把密钥写入版本库。

## 流程

维护者说明见 Walknote 主仓 **`Docs/01-SDK/SDK_GITHUB_BINARIES_DISTRIBUTION.md`**。

## 许可证

见 [LICENSE](LICENSE)。
