 01/05/2020
 Based on this video:
 https://www.youtube.com/watch?v=lI2nwZSMvlE&list=PLK6MXr8gasrGmIiSuVQXpfFuE1uPT615s&index=2

**1. Created a CMakeLists.txt** 
    -Desccribed a minimum required version and named the project. 

**2. Created a directory.**
    - I called it build. This directory is the one
      that we are going to build from or run CMake from. It will
      reference the source directory.

**3. Write a cmake file**
    - In order to run the CMake through the terminal, we need to write
      cmake and then add a path to the source directory. 
      So we enter directory 'build' by entering cd build in the terminal
      and then we write cmake .. (as the source is one step back)
      in the terminal. It will do some 'work'
      Once we open build, we find 4 files. That's the output
      of this command. Once the project gets more complicated
      there will be more files generated. 

**4. Creating a .c file **
    - That would need to be compiled to an executable.
      Adding a line add_executable() where you define the name of an
      executable and then file names (any_name.c) separated by spaces.
      Once this is done, enter build directory and run cmake ..
      and then cmake --build . in the terminal.
      Last command will build an executable in the build directory. 

**5. Adding a library** 
  - All is done in CMakeLists.txt
    We can add it just adding libraries .c file to executables. 
    Another way is in the example of CMakeLists.txt
    We add library defining its name, .h and .c files
    and then targert link libraries at the end.
    At the line of name, we can specify if the library is STATIC, 
    SHARED or MODULAR. 
    Static is shared only with this executable. Shared library will
    be visible outside. (ldd executable in terminal)
