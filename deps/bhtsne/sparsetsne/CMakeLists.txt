CMAKE_MINIMUM_REQUIRED(VERSION 2.8 FATAL_ERROR)
CMAKE_POLICY(VERSION 2.8)

project(bhtsne)

SET (CMAKE_CXX_FLAGS "-std=c++11")

SET(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake" "${CMAKE_MODULE_PATH}")

#FIND_PACKAGE(OpenMP REQUIRED)

#SET(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
#SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS} -O3 -fPIC -ffast-math -funroll-loops")
#SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${OpenMP_EXE_LINKER_FLAGS}")

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -fPIC -ffast-math -funroll-loops")

file(GLOB SRC_FILES *.cpp *.hpp *.c *.h)

add_executable(${PROJECT_NAME} ${SRC_FILES})

#ADD_LIBRARY(bhtsne MODULE ${src})
