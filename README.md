# lesstimateTemplateCpp

This repository demonstrates the use of lesstimate as submodule in C++ projects. The project may be used as a template to create new C++ libraries. 
A full documentation of the procedure is provided in the [Documentation of lesstimate](https://jhorzek.github.io/lesstimate/).

## Installation

The repository includes a copy of the [**cpm.Cmake**](https://github.com/cpm-cmake/CPM.cmake) package manager. You can adapt the version of the **lesstimate** and **armadillo** libraries used in the package in the **CMakeLists.txt** file. 

````
# clone lesstimateTemplateCpp
git clone https://github.com/jhorzek/lesstimateTemplateCpp.git

# create build directory
mkdir build
cd build

# compile project
cmake .. --preset=linux
cmake --build .

# run example
./lesstimateTemplate
````

