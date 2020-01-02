cmake_minimum_required(VERSION 3.5)
project(convex_decomposition)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)

file(GLOB_RECURSE CD_SOURCE_CODE src/ConvexDecomposition/*.cpp)
add_executable(${PROJECT_NAME} src/DecomposeSample.cpp ${CD_SOURCE_CODE})

install(TARGETS ${PROJECT_NAME}
  RUNTIME DESTINATION bin)

ament_package()
