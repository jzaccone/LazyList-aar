LazyList Android ARchive
========

LazyList library built with gradle in aar format for usage with android gradle build system.

How to use
========

Remote repository
--------

Maven repository on [GitHub Pages](http://pages.github.com/)

```groovy
...

repositories {
    maven { url "http://jzaccone.github.io/LazyList-aar" }
    ...
}

dependencies {
    compile 'com.thest1.lazylist:library:1.0@aar'
    ...
}
```

> In your `build.gradle` include `maven{ url "http://jzaccone.github.io/LazyList-aar" }` as repository priorior to `mavenCentral()`

Local repository
--------

Before you can get aar you should checkout submodule. Overall build process including build is straightforward:

```bash
  $ git submodule update --init
  ...
  $ ./gradlew build
  ...
```

When build is finished aar file will be located in `build/libs`.

Maven artifact

```bash
  $ ./gradlew -Dorg.gradle.project.repoDir="${HOME}/.m2/repository" uploadArchives
```

`build.gradle` example

```groovy
...

repositories {
    mavenLocal()
    ...
}

dependencies {
    compile 'com.thest1.lazylist:library:1.0@aar'
    ...
}
```
