### [Fork this repository](https://github.com/maxwellpollack/juce-plugin-ci/fork) to start a new audio plugin project on Github.

It contains an audio plugin template, and automatically builds cross-platform binaries every time you push.

#### To publish a new Release, tag your commit with a version number before pushing:
```shell
git tag v1.0.0
git push origin main --tags
```

---

It borrows the boilerplate audio plugin code from [`JUCE/examples/CMake/AudioPlugin`](https://github.com/juce-framework/JUCE/tree/master/examples/CMake/AudioPlugin), and adds
1. a CMake `FetchContent` call to automatically download and link the JUCE library, and
2. a GitHub Actions script which automatically builds (with CMake) and tests (with CTest) the audio plugin for 64-bit MacOS, Windows, and Linux platforms on every push.

---

## Downloading
```
git clone --recurse-submodules https://github.com/maxwellpollack/juce-plugin-ci.git
```

## Building from the command line

- Install [CMake](https://cmake.org/install/) and run:
```
cmake .
cmake --build build
```

## Building in Visual Studio Code

- Install [CMake](https://cmake.org/install/), [VS Code](https://code.visualstudio.com/), the [VS Code C/C++ language extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools), and [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools).
- [Follow this guide to get started with CMake Tools](https://code.visualstudio.com/docs/cpp/cmake-linux).
