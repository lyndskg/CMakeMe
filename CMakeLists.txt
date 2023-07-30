cmake_minimum_required(VERSION 3.15)

# Set the project name and language
project(MyAdvancedCppProject CXX)

# Set C++ standard (change to your desired version)
set(CMAKE_CXX_STANDARD 17)

# Add compile options (optional)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra")

# Add your source files here
set(SOURCES
    src/main.cpp
    src/my_file.cpp
)

# Add headers (if any)
set(HEADERS
    include/my_file.h
)

# Add external libraries (if any)
set(EXTERNAL_LIBRARIES
    # Example: pthread, boost, etc.
)

# Add executable target
add_executable(MyAdvancedCppProject ${SOURCES} ${HEADERS})

# Set include directories (if any)
target_include_directories(MyAdvancedCppProject PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

# Link external libraries (if any)
target_link_libraries(MyAdvancedCppProject PUBLIC
    ${EXTERNAL_LIBRARIES}
)

# Set output directories (optional)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

# Set build type (optional, default is "Release")
if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

# Add compiler-specific flags (optional)
if (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    target_compile_options(MyAdvancedCppProject PRIVATE -fconcepts)
elseif (CMAKE_CXX_COMPILER_ID MATCHES "Clang")
    target_compile_options(MyAdvancedCppProject PRIVATE -fcoroutines-ts)
endif()

# Enable testing (optional)
enable_testing()

# Add unit tests
add_subdirectory(tests)

# Additional comments
# -----------------------------------------------------------------------------
# If you have more directories with source files, you can add them here
# Example: add_subdirectory(src/other_directory)

# If your project requires specific include paths for tests, add them here
# Example: target_include_directories(tests PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

# If you have custom compiler flags for the tests, set them here
# Example: target_compile_options(tests PRIVATE -Wno-unused-variable)

# If your tests require external libraries, link them here
# Example: target_link_libraries(tests PRIVATE ${EXTERNAL_LIBRARIES})

# You can add more configuration options or features as needed for your project
# -----------------------------------------------------------------------------

