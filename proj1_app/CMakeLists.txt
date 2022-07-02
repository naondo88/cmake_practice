cmake_minimum_required (VERSION 3.24)
project (HelloWorldApp)
MESSAGE( STATUS "PROJECT_NAME: " ${PROJECT_NAME} )

option(ARM32_BUILD "Build for ARM32" OFF)

# Check platforms
if (CMAKE_HOST_WIN32)
    set(WINDOWS 1)
elseif(CMAKE_HOST_APPLE)
    set(MACOS 1)
elseif(CMAKE_HOST_UNIX)
    set(LINUX 1)
endif()

# Check compiler architecture
if(CMAKE_CL_64)
    MESSAGE( STATUS ">>> 64-bit")
else()
    MESSAGE( STATUS ">>> 32-bit")
endif()

# Check compilers
MESSAGE( STATUS ">>> ${CMAKE_CXX_COMPILER_ID}")
if (CMAKE_CXX_COMPILER_ID STREQUAL "Clang")
    MESSAGE( STATUS "Using Clang" )
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    MESSAGE( STATUS "Using GNU" )
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "Intel")
    MESSAGE( STATUS "Using Intel" )
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
    MESSAGE( STATUS "Using MSVC" )
endif()

include_directories("${PROJECT_BINARY_DIR}" "${PROJECT_SOURCE_DIR}/include/")

# Add the executable
add_executable(${PROJECT_NAME} app.cpp)


# # Use CTest
# include(CTest)
# add_test (BarcodeReaderRuns ${PROJECT_NAME})