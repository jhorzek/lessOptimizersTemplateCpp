cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

# define project:
project(lesstimateTemplate 
        VERSION 0.2.0
        DESCRIPTION "Template for the lesstimate library"
        HOMEPAGE_URL "https://jhorzek.github.io/lesstimateTemplate/"
        LANGUAGES CXX)

# add dependencies
# First: add CPM to download dependencies if necessary
include(cmake/CPM.cmake)

# add armadillo
CPMAddPackage(
	URL "https://sourceforge.net/projects/arma/files/armadillo-12.6.3.tar.xz"
	NAME armadillo
	VERSION 12.6.3
)

# add lesstimate
# WARNING: REPLACE THE VERSION WITH THE GITHUB COMMIT THAT YOU WANT TO USE
set(LESSTIMATE_VERSION "9f61f3fbc4ff1f288797e21a5f8d76e6af464f51")

CPMAddPackage("gh:jhorzek/lesstimate#${LESSTIMATE_VERSION}")

# set compiler settings
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# create target:
add_executable(${PROJECT_NAME} "linear_regression.cpp")

# link to dependencies
target_link_libraries(${PROJECT_NAME} PRIVATE 
                      armadillo
                      lesstimate::lesstimate)
