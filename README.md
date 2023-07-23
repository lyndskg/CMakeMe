# CMakeMe
Template for CMakeLists.txt

As of my last update in September 2021, CMake offers various commands to help define the build process in a CMakeLists.txt file. Below is a list of some commonly used CMake commands. Note that there may be additional commands not listed here, and new commands may have been introduced since then. Always refer to the official CMake documentation for the most up-to-date information.

1. `cmake_minimum_required`: Set the minimum required version of CMake for the project.
   ```
   cmake_minimum_required(VERSION <version>)
   ```

2. `project`: Set project information and specify languages used in the project.
   ```
   project(<project_name> [LANGUAGES <language>])
   ```

3. `add_executable`: Add an executable target to the project.
   ```
   add_executable(<target_name> [WIN32] [MACOSX_BUNDLE] [EXCLUDE_FROM_ALL] source1 source2 ...)
   ```

4. `add_library`: Add a library target to the project.
   ```
   add_library(<target_name> [STATIC | SHARED | MODULE] source1 source2 ...)
   ```

5. `add_subdirectory`: Add a subdirectory to the build.
   ```
   add_subdirectory(<directory>)
   ```

6. `target_link_libraries`: Link libraries to a specific target.
   ```
   target_link_libraries(<target_name> PRIVATE|PUBLIC|INTERFACE <library_name>)
   ```

7. `target_include_directories`: Add include directories to a target.
   ```
   target_include_directories(<target_name> PRIVATE|PUBLIC|INTERFACE <dir1> <dir2> ...)
   ```

8. `target_compile_definitions`: Add compile definitions to a target.
   ```
   target_compile_definitions(<target_name> PRIVATE|PUBLIC|INTERFACE <definition>)
   ```

9. `target_compile_options`: Add compile options to a target.
   ```
   target_compile_options(<target_name> PRIVATE|PUBLIC|INTERFACE <option>)
   ```

10. `find_package`: Find and load an external package.
    ```
    find_package(<package_name> [version] [QUIET] [NO_MODULE])
    ```

11. `configure_file`: Copy and configure a file.
    ```
    configure_file(input_file output_file [COPYONLY] [@ONLY])
    ```

12. `set`: Set variables.
    ```
    set(<variable_name> <value> [CACHE <type> <docstring>])
    ```

13. `if`, `elseif`, `else`, `endif`: Conditional blocks.
    ```
    if(<condition>)
      # code block
    elseif(<condition>)
      # code block
    else()
      # code block
    endif()
    ```

14. `foreach`: Loop over a list.
    ```
    foreach(<variable> IN LISTS <list>)
      # code block
    endforeach()
    ```

15. `while`: Loop while a condition is true.
    ```
    while(<condition>)
      # code block
    endwhile()
    ```

16. `function` and `endfunction`: Define a function.
    ```
    function(<function_name> [arg1 arg2 ...])
      # code block
    endfunction()
    ```

17. `add_custom_target`: Add a custom target.
    ```
    add_custom_target(<target_name> [ALL] [command1 [args...]]
                      [COMMAND command2 [args...]] [DEPENDS depend_targets...])
    ```

18. `add_custom_command`: Add a custom command to a target.
    ```
    add_custom_command(TARGET <target_name>
                       COMMAND command1 [args...]
                       [COMMAND command2 [args...]]
                       [DEPENDS depend_targets...]
                       [WORKING_DIRECTORY dir]
                       [COMMENT comment]
                       [VERBATIM])
    ```

19. `install`: Specify installation rules for targets or files.
    ```
    install(TARGETS <target_name> DESTINATION <destination>)
    install(FILES <file1> <file2> ... DESTINATION <destination>)
    ```

20. `set_source_files_properties`: Set properties on source files.
    ```
    set_source_files_properties(source1.cpp PROPERTIES COMPILE_FLAGS <flags>)
    ```

These are some of the common commands you'll find in CMakeLists.txt files. However, CMake is a highly flexible and extensible build system, so there are many more commands and options available to suit various project needs. Be sure to consult the official CMake documentation for comprehensive information and the latest updates.
