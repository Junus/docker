# android-java8

This docker is to build Android Gradle project with Java 8.
Contains:

* Android SDK: r24.4.1
* Build tools: 23.0.2
* Android API: 23
* Support maven repository
* Google maven repository
* Arm emulator: v21
* Platform tools
* Created emulator image named: "Nexus 5"

## Build image

```bash
docker build -t junus/android-java8:v1 .
```

If building fail you can debug via where `709c6c40d0b1` is partial build

```bash
docker run --tty --interactive --rm 709c6c40d0b1 /bin/bash
```

## Usage
Change directory to your project directory, than run:

```bash
docker run --tty --interactive --volume=$(pwd):/opt/workspace --workdir=/opt/workspace --rm junus/android-java8:v1  /bin/sh -c "./gradlew build"
```

