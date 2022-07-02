# TODO List:

All of this stuff I'm doing is clearly ineffective.  CMake is very badly designed software (or else was originally well-designed but then hotpatched into oblivion).  Everyone uses like 7 different ways of doing one thing, the only examples have the most trivial and useless project directory structures, and it's integration with conan is wildly opaque.

I think the only way to make progress here is just to itemize this into 6 different micro-projects, and just aim to solve each one:

## Build the following with purely CMake (no conan)
1. Write and build an app
    1. Tutorial: [https://www.dynamsoft.com/codepool/cc-barcode-app-cmake-windows.html](cpp app with cmake)
1. Write and build an app with tests
1. Write and build an app with static lib
1. Write and build a dynamic lib
1. Write and build a dynamic lib with tests
1. Write a dynamic lib (with a dependency on an external lib) that is build with 
1. Write a dynamic lib and an app that uses it with CMake (no conan)
1. Write a dynamic lib and an dependent app with CMake (just download SDL2 binaries and headers)

# Conan/CMake practice
1. Write and build an app
1. Write and build an app with tests
1. Write and build an app with static lib
1. Write and build a dynamic lib
1. Write and build a dynamic lib with tests
1. Write a dynamic lib (with a dependency on an external lib) that is build with 
1. Write a dynamic lib and an app that uses it with CMake (no conan)
1. Write a dynamic lib and an dependent app with CMake (just download SDL2 binaries and headers)
