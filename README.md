# Android Gradle Java Library Template 

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)
[![TravisCI OSX Build](https://img.shields.io/travis/jaredsburrows/android-gradle-java-library-template/master.svg)](https://travis-ci.org/jaredsburrows/android-gradle-java-library-template)
[![Coveralls Code Coverage](https://img.shields.io/coveralls/jaredsburrows/android-gradle-java-library-template/master.svg?label=Code%20Coverage)](https://coveralls.io/github/jaredsburrows/android-gradle-java-library-template?branch=master)
[![Twitter Follow](https://img.shields.io/twitter/follow/jaredsburrows.svg?style=social)](https://twitter.com/jaredsburrows)

Gradle + Android Studio + Robolectric + Espresso + Mockito + EasyMock/PowerMock + JaCoCo

## Technologies used:
#### Build Tools:
|Name|Description|
|---|---|
| [Gradle](http://gradle.org/docs/current/release-notes) | Gradle build system |
| [Android Gradle Build Tools](http://tools.android.com/tech-docs/new-build-system) | Official Gradle Plugin |
| [Android SDK](http://developer.android.com/tools/revisions/platforms.html#5.1) | Official SDK |
| [Android SDK Build Tools](http://developer.android.com/tools/revisions/build-tools.html) | Official Build Tools |
| [Android Studio](http://tools.android.com/recent) or | Official IDE |
| [Intellij](https://www.jetbrains.com/idea/download/) | Intellij IDE |

#### Testing Frameworks:
|Name|Description|
|---|---|
| [JUnit](https://github.com/junit-team/junit) | Java Unit Testing Framework |
| [AssertJ](http://joel-costigliola.github.io/assertj/) | Matchers for Unit Tests |
| [Mockito](https://github.com/mockito/mockito) | Mocking Framework |

#### Reporting Plugins:
|Name|Description|
|---|---|
| [JaCoCo](http://www.eclemma.org/jacoco/) | JaCoCo Test Coverage |
| [Coveralls](https://coveralls.io/) | Hosts test reports published from TravisCI |

#### Continuous Integration:
|Name|Description|
|---|---|
| [TravisCI](http://docs.travis-ci.com/user/languages/android/) | Build Server(Builds, Tests, Publishes reports to Coveralls) |

# Getting Started:
## `Android Studio` or `Intellij` Support(Simple):
 - **Import/Open this project with Android Studio/Intellij(click on `build.gradle`)**

 - **Unit Tests:**
  - Change the Build Variant Test Artifact to `Unit Tests`
  - Right click a unit test located in `src/main/test` and click test

## Comand Line(Advanced):
##### Clone with `Git`:
 - `git clone https://github.com/jaredsburrows/android-gradle-java-library-template.git`
 - `cd android-gradle-java-library-template`

##### Publish via the Gradle "maven" plugin:
 - **Install Maven `debug flavor` dependencies locally:**
   - `gradlew assembleDebug installArchives`
 - **Upload Maven `debug flavor` dependencies to a specified repository:**
   - `gradlew assembleDebug uploadArchives`

##### Publish via the Gradle "maven-publish" plugin:
 - **Install Maven `debug flavor` dependencies locally:**
   - `gradlew assembleDebug publishDebugPublicationToMavenLocalRepository`
 - **Upload Maven `debug flavor` dependencies to a specified repository:**
   - `gradlew assembleDebug publish`

##### Publish via the Jfrog Bintray plugin:
 - **Upload Maven `debug flavor` dependencies to Jfrog Bintray:**
   - `gradlew assembleDebug bintrayUpload`

##### Running Unit Tests with `Gradle`:
 - **Run all unit tests in all `flavors`:**
   - `gradlew test`
 - **Run a single unit test in all `flavors`:**
   - `gradlew test --tests="*MainActivityTest*"`
 - **Run all unit `debug flavor` tests:**
   - `gradlew testDebug`
 - **Run a single unit test in the `debug flavor`:**
   - `gradlew testDebug --tests="*MainActivityTest*"`
 - **Run a single unit test in the `debug flavor` with `Jacoco` test reports:**
   - `gradlew testDebug --tests="*MainActivityTest*" jacocoDebugReport`
