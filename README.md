This repository is a starting point for creating audio plugins with the JUCE framework. [Fork it](https://github.com/maxwellpollack/juce-plugin-ci/fork) to start a new, empty audio plugin project on Github that automatically builds cross-platform (x64 Mac, Windows, Linux) binaries every time you push to it.

---

It borrows the boilerplate audio plugin code from [`JUCE/examples/CMake/AudioPlugin`](https://github.com/juce-framework/JUCE/tree/master/examples/CMake/AudioPlugin), and adds:
1. a CMake `FetchContent` call to automatically download and link the JUCE library, and
2. a GitHub Actions script which automatically builds (with CMake) and tests (with CTest) the audio plugin for 64-bit MacOS, Windows, and Linux platforms on every push.

To publish a new Release build, tag your commit with a version number before pushing:
```shell
git tag v1.0.0
git push origin master --tags
```

---

## How to build your audio plugin:

#### From the command line:

1. [Install CMake](https://cmake.org/install/)
2. Run these commands in a folder of your choosing:
```
git clone --recurse-submodules https://github.com/maxwellpollack/juce-plugin-ci.git
cd juce-plugin-ci
cmake .
cmake --build build
```

#### In Visual Studio Code:

1. [Install CMake](https://cmake.org/install/)
2. [Install VS Code](https://code.visualstudio.com/)
3. [Install the CMake Tools extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
4. [Install the C/C++ language extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
5. Run these commands in a folder of your choosing:
```
git clone --recurse-submodules https://github.com/maxwellpollack/juce-plugin-ci.git
cd juce-plugin-ci
code .
```
6. [Follow this guide to get started with CMake Tools](https://code.visualstudio.com/docs/cpp/cmake-linux)
