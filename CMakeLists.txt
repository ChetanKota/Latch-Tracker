#Set minimum version requered
cmake_minimum_required(VERSION 2.4.6)
set (CMAKE_CXX_STANDARD 11)
#just to avoid the warning
if(COMMAND cmake_policy)
     cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)
#set project name
project(TLD)
#Append path to the module path
list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})
#OpenCV
find_package(OpenCV REQUIRED)
#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/./)

add_executable(latch latch_tracker.cpp)
#link the libraries
target_link_libraries(run_tld latch ${OpenCV_LIBS})
#set optimization level 
set(CMAKE_BUILD_TYPE Release)

