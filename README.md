### [Use this template](https://github.com/maxwellpollack/juce-plugin-ci/generate) to start a new JUCE audio plugin project in a Github repository.

It contains:
1. the boilerplate audio plugin code from [`JUCE/examples/CMake/AudioPlugin`](https://github.com/juce-framework/JUCE/tree/master/examples/CMake/AudioPlugin)
2. a CMake `FetchContent` call to automatically download and link the JUCE library
3. a GitHub Actions workflow which automatically builds (with CMake) and tests (with CTest) the audio plugin for 64-bit MacOS, Windows, and Linux platforms on every push

#### To publish a new Release, tag your commit with a version number before pushing:
```shell
git tag v1.0.0
git push origin main --tags
```

---

## Building from the command line

- Install [CMake](https://cmake.org/install/) and run:
```
cmake .
cmake --build build
```

## Building in Visual Studio Code

- Install [CMake](https://cmake.org/install/), [VS Code](https://code.visualstudio.com/), the [VS Code C/C++ language extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools), and [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools).
- [Follow this guide to get started with CMake Tools](https://code.visualstudio.com/docs/cpp/cmake-linux).
