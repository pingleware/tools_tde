# tools_tde

Some tools to facilitate the use of build tools (both CB and CMAKE)

The most important is "create_dir.bat". I use it constantly because it allows the creation of ALL the subdirectories needed for builds from the "master" directory. IMPORTANT: This "master" directory is the highest level of your application's structure, and it is recommended for CMAKE not to store the source code there. This is why I have always placed the source code in the "src" subdirectory. For CMAKE builds, it is necessary to create a "build.cmake" subdirectory under the master directory containing ALL the configuration files (CMAKELists.txt for CMAKE, and a makefile for each build managed outside of CMAKE). Thus, all these templates (parameters with the application name) are located here in the reference directory "build.cmake". For command-line generation, you need to create a `build.batch` directory containing the build/linking scripts for each development environment (compilers, IDES, or development package). There are also the `generate_all_with_cmake.bat` and `generate_all_with_command_files.bat` generation tools, which are also configurable. Simply run them in no-parameter mode to get the appropriate help. Finally, you'll find Python scripts for calculating file sizes (volumes generated on disk for statistical purposes if needed) and checksums of the generated executables, as well as for automatically transferring a file to a list of directories (currently, this list is fixed in the script, but you can modify it as needed by examining it).

The CB command-line automatic generation script doesn't work (...again!). So I launch the generation of ALL builds directly in the Code::Blocks IDE by choosing the "virtual target" -> All_build.

Finally, I've made available ALL the modifications made to each compiler or development environment in the "modifs_compilers" directory. These are the changes deemed necessary compared to the initial installations so that, for example, OpenGL works correctly with some "older" compilers.

Now it's your turn, everything is there, with explanatory comments in each script (or almost... -) ).
