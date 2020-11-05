# Welcome 👋

Developers write better apps when they can [read the source](https://blog.codinghorror.com/learn-to-read-the-source-luke/). Unfortunately, the sources for the Android framework and various Google Android libraries are scattered all over the web.

This pages helps Android developers find the sources they're looking for.

🙏🙏 You can improve this page and help the Android community by opening [an issue](https://github.com/pyricau/androidsrc/issues/new) or [a pull request](https://github.com/pyricau/androidsrc/edit/main/README.md).

# Libraries

## Jetpack

* Most Jetpack libraries have sources available [on cs.android.com](https://cs.android.com/androidx/platform/frameworks/support) in the _androidx_ subproject. Some interesting ones:
  * [Activity](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:activity/)
  * [Compose](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:compose/)
  * [Fragment](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:fragment/)
  * [Navigation](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:navigation/)
  * [Paging](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:paging/)
  * [Room](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:room/)
  * [WorkManager](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:work/)
  * [Startup](https://cs.android.com/androidx/platform/frameworks/support/+/androidx-master-dev:startup/)
* That repository is also synced [to GitHub](https://github.com/androidx/androidx)
    * You can contribute via GitHub to a [subset of projects](https://github.com/androidx/androidx#contribution-guide) (experimental workflow). You can also contribute by clicking **Edit Code** in a file on cs.android.com, which should work for all projects in that repository.

## ConstraintLayout / MotionLayout

* Developed directly [on GitHub](https://github.com/androidx/constraintlayout), browsable on [cs.android.com](https://cs.android.com/androidx/constraintlayout/+/main:constraintlayout/).
  * The git history starts at 2.0.0, 1.x sources are available [here](https://cs.android.com/androidx/constraintlayout/+/main:constraintlayout/constraintlayout/src/main/java/androidx/constraintlayout/widget/ConstraintLayout.java).

## Espresso / Android Test

* Developed directly [on GitHub](https://github.com/android/android-test).

## Data Binding

* Latest sources are [on android.googlesource.com](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/mirror-goog-studio-master-dev/extensions/library/src/main/java/androidx/databinding) on the `mirror-goog-studio-master-dev` branch.
* When a release is stable, its sources are synced [to cs.android.com](https://cs.android.com/android/platform/superproject/+/studio-master-dev:tools/data-binding/extensions/library/src/main/java/androidx/databinding/) on the `studio-master-dev` branch.
  * 👎🔎 Not searchable online: the `studio-master-dev` branch is not indexed.

## Dagger 2

* Developed directly [on GitHub](https://github.com/google/dagger).

# The Android Framework

* Available [on cs.android.com](https://cs.android.com/android/platform/superproject)
* View internals? See [View.java](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/core/java/android/view/View.java).
* Activity lifecycle? See [ActivityThread.java](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/core/java/android/app/ActivityThread.java).
* Art Runtime? See [class.cc](https://cs.android.com/android/platform/superproject/+/master:art/runtime/mirror/class.cc).

## What if it's a new version, sources not available yet?

* Start an emulator for the latest version.
* Run `adb pull /system/framework/framework.jar`.
* Unzip `framework.jar` (contains dexes).
* Use dex2jar to turn dexes into jars.
* Explore with [jd-gui](http://java-decompiler.github.io/) or IntelliJ (hack: add as a dependency)

# Android Studio

* Latest sources are [on android.googlesource.com](https://android.googlesource.com/platform/tools/adt/idea/+/refs/heads/mirror-goog-studio-master-dev/) on the `mirror-goog-studio-master-dev` branch.
* When a release is stable, its sources are synced [to cs.android.com](https://cs.android.com/android/platform/superproject/+/studio-master-dev:tools/adt/idea/) on the `studio-master-dev` branch.
  * 👎🔎 Not searchable online: the `studio-master-dev` branch is not indexed.

# Android Gradle Plugin (AGP)

* Latest sources are [on android.googlesource.com](https://android.googlesource.com/platform/tools/base/+/refs/heads/mirror-goog-studio-master-dev/build-system/) on the `mirror-goog-studio-master-dev` branch.
* When a release is stable, its sources are synced [to cs.android.com](https://cs.android.com/android/platform/superproject/+/studio-master-dev:tools/base/build-system/;bpv=1) on the `studio-master-dev` branch.
  * 👎🔎 Not searchable online: the `studio-master-dev` branch is not indexed.
* [@jrodbx](https://github.com/jrodbx) dumped the sources for each release [on github](https://github.com/jrodbx/agp-sources).
  * This is handy for debugging Gradle builds, however these sources might miss commits cherry-picked into weekly release branches, as those aren't reflected in any AOSP branch.

# Kotlin

* Sources for the Kotlin compiler and standard lib are [on GitHub](https://github.com/JetBrains/kotlin).

# Firebase

* A subset of Firebase Android libraries have sources available [on GitHub](https://github.com/firebase/firebase-android-sdk), also browsable [on cs.opensource.google](https://cs.opensource.google/firebase-sdk/firebase-android-sdk).

# Bazel

Bazel is a build tool maintained by Google but not part of the official Android toolchain. Some Android devs begrudgingly use it.

* Bazel is developed [on Github](https://github.com/bazelbuild/) and browsable [cs.opensource.google](https://cs.opensource.google/bazel).

# Skia

Skia is a 2D graphics library used by Android and Compose Desktop. On Android it's always been used for software rendering, and is used for hardware rendering except from Android 3.0 to 9.0.

* Available [on cs.opensource.google](https://cs.opensource.google/skia/skia).

# Google Play Services

* Play Services is not open source. I added this entry because people keep asking about it 😅.
