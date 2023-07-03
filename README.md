# lesstimateTemplateCpp

This repository demonstrates the use of lesstimate as submodule in C++ projects. The project may be used as a template to create new C++ libraries. 
A full documentation of the procedure is provided in the [Documentation of lesstimate](https://jhorzek.github.io/lesstimate/).

## Installation

We recommend using vcpkg to install the dependencies of lesstimateTemplatesCpp. 

````
# Install vcpkg
git clone https://github.com/Microsoft/vcpkg.git
./vcpkg/bootstrap-vcpkg.sh

# clone lesstimateTemplateCpp
git clone --recurse-submodules https://github.com/jhorzek/lesstimateTemplateCpp.git

# create build directory
cd build

# compile project
cmake build .. -DCMAKE_TOOLCHAIN_FILE=vcpkg/scripts/buildsystems/vcpkg.cmake
cd ..
cmake --build build

# run example
build/testDocumentation
````

