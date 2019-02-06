# C++

## Compile cpp with sqlite3 library
g++ main.cpp -lsqlite3

# C/C++
## Compiling
gcc: GNU C      Compiler
g++: GNU C++    Compiler

gcc hello.c -o hello1           
g++ hello.cc -o hello1          # Can also use .cpp.

g++ -c file1.cpp file2.cpp file3.cpp                # Compiles the files to file1.o file2.o..
g++ -o prog file1.o file2.o file3.o                 # Links the files into one executable called prog.
g++ -o prog file1.cpp file2.cpp file3.cpp           # Combine and compile steps together.