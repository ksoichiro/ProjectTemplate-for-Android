Project Template for Android
====
[![Build Status](https://travis-ci.org/ksoichiro/ProjectTemplate-for-Android.png?branch=master)](https://travis-ci.org/ksoichiro/ProjectTemplate-for-Android)

Android application project template files for both Android Studio and Eclipse.

## How to use

### Edit project name

1. Download this project.
1. Rename the root directory(`ProjectTemplate`) to your project name.
1. Add `local.properties`.  
   If you don't have appropriate one, execute this in the project directory:

        android update project -p .

1. Edit `.project` and modify `<name>` tag which has name of the Eclipse project.

        <name>ProjectTemplate</name>

1. Edit `build.xml` and modify `<project>` tag.
   This will be used for APK file name when building by Ant.

        <project name="ProjectTemplate" default="help">

1. Import your project according to the following guides.

### For Eclipse users

1. In Eclipse, select File > Import
1. General > Existing Projects into Workspace
1. Select the project directory.

### For Android Studio users

Just select File > Import Project... in Android Studio.

## Warning

If you `git clone`d this project for your own projects,
remove `.git` directory and `git init` at first to track your own project.

## How to build project

### Eclipse

For debug:

1. Select project in Package Explorer.
1. Select Run > Run from the menu.

### Android Studio

1. Select build types from `Build Variants` view.
1. Select Run > Run 'ProjectTemplate' from the menu.

### Ant

For debug:

    ant debug

For release:

    ant release

### Gradle

For debug:

    ./gradlew assembleDebug

For test(staging):

    ./gradlew assembleStaging

For release:

    ./gradlew assembleRelease

For all build types:

    ./gradlew assemble

## Supported versions

Developed and tested under the following conditions.

Software                      | Version
----------------------------- | -----------------
OS X                          | 10.9.2
Android SDK Tools             | 22.6
Android SDK Platform-tools    | 19.0.1
Android SDK Build-tools       | 19.0.3
Android SDK Platform          | API level 19 Rev.3
Android Developer Tools (ADT) | v22.3
Android Studio (Preview)      | 0.5.1
Android Support Library       | 19.0.1
Gradle                        | 1.11
Android Gradle Plugin         | 0.9.0
Git                           | 1.8.3.4
