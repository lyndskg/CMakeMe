# CMakeMe

CMakeMe is a coding project that aims to simplify the process of creating CMakeLists.txt files for C++ projects. It offers users a basic template that can be customized for various C++ project structures and configurations. With CMakeMe, developers can quickly set up the build system for their C++ projects without the need to manually write CMakeLists.txt files from scratch. The tool will generate a well-structured and organized CMakeLists.txt template, providing a solid foundation for building and managing C++ projects efficiently.


Key Features:
1. C++ Project Template: CMakeMe provides a basic and adaptable template for CMakeLists.txt files tailored specifically for C++ projects.
2. Customizable Configuration: Users can easily customize the CMakeLists.txt template to fit their project's specific needs, including setting the C++ standard, compiler flags, output directories, external library dependencies, and more.
3. Support for Project Structure: CMakeMe accommodates various project structures, allowing users to include multiple source directories, headers, and external libraries seamlessly.
4. Target Generation: The tool supports the generation of multiple targets, such as executables and libraries, enabling users to build complex projects with ease.
5. Unit Testing Integration (Optional): CMakeMe offers the option to include unit testing support in the generated CMakeLists.txt template, making it easy to set up and execute tests for C++ projects.
6. Cross-Platform Compatibility: The generated CMakeLists.txt files are designed to be cross-platform compatible, ensuring consistent builds across different operating systems.
7. Simplified Build Process: CMakeMe eliminates the need to manually configure CMakeLists.txt files, reducing potential errors and saving development time.


Basic Workflow:
1. User Input: CMakeMe prompts users to provide essential project details, such as project name, C++ standard, compiler flags, and directories containing source files and headers.
2. Template Generation: Based on the user input, CMakeMe generates a CMakeLists.txt template with the specified configurations and project structure.
3. Customization: Users can further customize the generated template by adding external libraries, additional source directories, and any specific compiler options or targets as needed.
4. Integration with Existing Projects: CMakeMe can be integrated into existing C++ projects to create or update their CMakeLists.txt files efficiently.


Project Goals and Advantages:
1. Streamlined Project Setup: CMakeGen aims to simplify the initial setup of C++ projects by providing a ready-to-use CMakeLists.txt template.
2. Error Reduction: By automating the creation of CMakeLists.txt files, CMakeGen helps reduce human errors and ensures consistent build configurations.
3. Time Efficiency: Developers can save time in configuring CMakeLists.txt files, enabling them to focus more on the actual development process.
4. Enhanced Project Organization: CMakeGen encourages best practices in project structure and organization, leading to cleaner and more maintainable C++ projects.


CMakeMe will be a valuable tool for C++ developers, providing them with an efficient way to generate well-structured CMakeLists.txt files for various project configurations, ultimately enhancing their productivity and project management.

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
