cmake_minimum_required(VERSION 3.10)

# avoids c compiler test program error
# set(CMAKE_TRY_COMPILE_TARGET_TYPE "STATIC_LIBRARY")

#SET( CMAKE_C_COMPILER ${CC} )
#SET( CMAKE_CXX_COMPILER ${CXX} )

# set the project name
project(SQRT)

# add the executable
add_executable(Tutorial tutorial.cxx )