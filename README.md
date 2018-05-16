# FOSS4G-StLouis-2018
Kotlin demonstration repo for FOSS4G-NA 2018

Also checkout my other Multi-Platform Kotlin project for  [Common Map API][1]

## Requirements
Java SDK 
Android SDK

## Running Javascript

```gradle
 ./gradlew build
```

The exported javascript will be located in the directory: *kotlin-gis-js/build/classes/main/kotlin-gis-js.js*


## Running JVM

```gradle
 ./gradlew build
```

The exported jar will be located in the directory: kotlin-gis-jvm//build/libs/foss4g-stlouis-2018-1.0.0.0.jar

## Running Android

Pull a docker container that can build Android:

```bash
docker pull runmymind/docker-android-sdk:ubuntu-standalone
```

Run the build:

```bash
cd your/sourcecode/root
docker run -t --rm \
    -v $(pwd):/opt/workspace \
    --workdir=/opt/workspace \
    runmymind/docker-android-sdk:ubuntu-standalone \
    -e /bin/sh -c "./gradlew build"
```

The built apk will be located in the directory kotlin-gis-android/build/outputs/apk/debug/kotlin-gis-android-debug.apk

----------------------------------------------------
 
 [1]: https://github.com/missioncommand/cmapi-kotlin
