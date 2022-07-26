cmake_minimum_required (VERSION 3.12)

project ("JoyShockLibrary" CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

include (cmake/LinuxConfig.cmake)
include (cmake/WindowsConfig.cmake)

if (BUILD_SHARED_LIBS)
    set (JSL_PLATFORM_DEPENDENCY_VISIBILITY PRIVATE)
else ()
    set (JSL_PLATFORM_DEPENDENCY_VISIBILITY PUBLIC)
endif ()

add_subdirectory (JoyShockLibrary)
