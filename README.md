This is a starting point for building audio plugins with JUCE.

It borrows the boilerplate audio plugin code from [`JUCE/examples/CMake/AudioPlugin`](https://github.com/juce-framework/JUCE/tree/master/examples/CMake/AudioPlugin), adds a CMake `FetchContent` call to automatically download and link the JUCE library, and adds a GitHub Actions script which automatically builds (with CMake) and tests (with CTest) the audio plugin for 64-bit MacOS, Windows, and Linux platforms on every push.

To trigger a new Release build, tag your latest commit with a version number before pushing:
```shell
git tag v1.0.0
git push origin master --tags
```
