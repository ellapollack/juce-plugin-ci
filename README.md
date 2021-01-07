This repository is a starting point for building audio plugins with [JUCE](https://github.com/juce-framework/JUCE).

It borrows the boilerplate audio plugin code from [`JUCE/examples/CMake/AudioPlugin`](https://github.com/juce-framework/JUCE/tree/master/examples/CMake/AudioPlugin), adds a CMake `FetchContent` call to automatically download and link the JUCE library, and adds a GitHub Actions script which automatically builds (with CMake) and tests (with CTest) the audio plugin for 64-bit MacOS, Windows, and Linux platforms on every push.

To publish a new Release, tag your commit with a version number and push:
```shell
git tag v1.0.0
git push origin master --tags
```

---

## Building from the command line

1. [Download + install CMake](https://cmake.org/install/)
2.
```
git clone --recurse-submodules https://github.com/maxwellpollack/juce-plugin-ci.git
cd juce-plugin-ci
cmake .
cmake --build build
```

## Building in VS Code

1. [Install CMake](https://cmake.org/install/)
2. [Install VS Code](https://code.visualstudio.com/)
3. [Install the CMake Tools extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
4. [Install the C/C++ language extensison for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
5.
```
git clone --recurse-submodules https://github.com/maxwellpollack/juce-plugin-ci.git
cd juce-plugin-ci
code .
```
6. [Follow this guide to get started with CMake Tools](https://code.visualstudio.com/docs/cpp/cmake-linux)
