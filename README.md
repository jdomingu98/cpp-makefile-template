# C++ Creation Template
This repository was created with the intention of helping whatever person that doesn't want to manually create the cpp and hpp files.

The Makefile itself create both files in a ortodox canonical form (this includes a constructor and destructor without parameters, an implemented copy constructor and an assignation operator overridden). This Makefile also compiles and execute a basic c++ project.

## File generation rules

### create_hpp class=name
Creates the header template of the class "name". If no classname is provided, the result classname is "class"

### create_cpp class=name
Creates the class implementation template of the class "name". If no classname is provided, the result classname is "class"

### create class=name
Creates both header and class implementation template files of the class "name". If no classname is provided, the result classname is "class"

## Compilation rules

### all
The default rule that generates the executable to be launch. Compiles the project with "c++" compiler and the following flags: -Wall -Wextra -Werror -std=c++98

### clean
Clean all the object files (*.o files)

### fclean
Full clean the project. Removes the object files and the executable file

### re
Recompiles the project. This rule only executes "fclean" and "all" rules, in that order

### e
Recompiles and executes the project. This rule only executes "re" rule and the executable
