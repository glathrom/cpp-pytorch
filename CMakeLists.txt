cmake_minimum_required(VERSION 3.10)
project(example-app)
set(CMAKE_CXX_STANDARD 14)

# setting paths for libraries and executable outputs
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) 

# setting path to include files 
include_directories(${CMAKE_SOURCE_DIR}/include) 

find_package(Torch REQUIRED)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${TORCH_CXX_FLAGS}")

add_executable(example-app ${CMAKE_SOURCE_DIR}/src/example-app.cpp)
target_link_libraries(example-app "${TORCH_LIBRARIES}")
set_property(TARGET example-app PROPERTY CXX_STANDARD 14)

