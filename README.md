[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/beryx-gist/badass-runtime-pacman/blob/master/LICENSE)
[![Build Status](https://img.shields.io/travis/beryx-gist/badass-runtime-pacman/master.svg?label=Build)](https://travis-ci.org/beryx-gist/badass-runtime-pacman)

## Badass Runtime Plugin - Pacman Example ##

This project shows how to use the [Badass Runtime Plugin](https://github.com/beryx/badass-runtime-plugin/) to create a
custom runtime image of a non-modularized application.
Our example application is [Almas Baimagambetov's](https://github.com/AlmasB) Pacman.
This application is available in the [FXGLGames](https://github.com/AlmasB/FXGLGames) repository, which includes several games based on his awesome [FXGL](https://github.com/AlmasB/FXGL) game library.

### Quick start
From the [releases page](https://github.com/beryx-gist/badass-runtime-pacman/releases) download the archived custom runtime image for your operating system.
Unpack the archive and execute the `pacman` script found in the `pacman/bin` directory.  


### Creating a custom runtime image

Gradle must use Java 11 in order to be able to build the project.
To create the custom runtime image execute:

```
./gradlew runtimeZip
```

This command creates the runtime image in the `build/pacman` directory and a zip file of it in `build/image-zip`.

The start scripts are found in the `build/pacman/bin` directory.

(Before creating the runtime image, the Gradle script creates a clone of the FXGLGames repository in the `build/clone` directory.
  This may take several minutes. Be patient.)

You can easily adjust the `build.gradle` script if you want to create a runtime image for another game from the FXGLGames repository.
