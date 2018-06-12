# Android GStreamer sample player application

Download and extract the universal GStreamer Android binaries to
a directory of your choice.

<https://gstreamer.freedesktop.org/data/pkg/android/>

Edit gradle.properties in order to set gstAndroidRoot to point to the
unpacked GStreamer Android binaries.

## Build and deploy on the command line

To build and deploy the rtsp example to your device, use a command similar to:

```bash
$ PATH=~/dev/android/tools/bin:~/dev/android/ndk-bundle:$PATH ANDROID_HOME="$HOME/dev/android/" ./gradlew installDebug
```

## Run the application on the device

```bash
$ adb shell am start -n org.freedesktop.gstreamer.rtsp_example/.RTSPExample
```

To see the GStreamer logs at runtime:

```bash
$ adb logcat | egrep '(gst)'
```

## Build and run from Android Studio

Launch Android-studio, opening this folder as a project.

The project should build automatically, once it has done successfully,
it should be possible to run the project with Run > Run 'app', provided
a device is attached and USB debugging enabled.

The logs can be seen in the logcat tab.
