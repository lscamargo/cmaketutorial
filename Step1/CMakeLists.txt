cmake_minimum_required(VERSION 3.10)

# avoids c compiler test program error
# set(CMAKE_TRY_COMPILE_TARGET_TYPE "STATIC_LIBRARY")

#SET( CMAKE_C_COMPILER ${CC} )
#SET( CMAKE_CXX_COMPILER ${CXX} )

# set the project name
project(Tutorial VERSION 1.0)

# set c++ version
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# add the executable
add_executable(Tutorial tutorial.cxx)

configure_file(TutorialConfig.h.in TutorialConfig.h)

# add the directory for the generated TutorialConfig.h file (in build folder)
target_include_directories(Tutorial PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )