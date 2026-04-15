# OpenDev SDK — Desktop（JAR 分发）

本仓库为 **预构建 JVM JAR**（`:core` `jvm("desktop")` 产出），供未发布 Maven Central 时直接依赖。

## 产物

- `opendev-sdk.jar`
- `opendev-sdk-sources.jar`（可选，IDE 源码）

## Gradle

```kotlin
dependencies {
    implementation(files("libs/opendev-sdk.jar"))
}
```

Maven 坐标（`io.github.zinben-opendev:opendev-desktop-sdk`）见主仓文档，待 Central 发布后切换。
