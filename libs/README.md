# Local Hytale Server jar

The build compiles against the Hytale Server jar placed in this folder
(see `compileOnly(fileTree("libs"))` in `build.gradle.kts`).

The current server jar (e.g. `2026.05.26-c68d7d0d7` / Update 5) is not
published to a public Maven repository, so copy the server jar you run your
server with into this folder before building:

```
libs/
  <your-hytale-server>.jar
```

Any `*.jar` here is git-ignored, so the proprietary server jar is never
committed. Once Hytale's server jar is available on a Maven repo again you can
revert to a normal `compileOnly("com.hypixel.hytale:Server:<version>")`
dependency.
