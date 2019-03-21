cmake_minimum_required(VERSION 3.5)
project(convex_decomposition)

find_package(ament_cmake REQUIRED)

file(GLOB_RECURSE CD_SOURCE_CODE src/ConvexDecomposition/*.cpp)
add_executable(${PROJECT_NAME} src/DecomposeSample.cpp ${CD_SOURCE_CODE})

install(TARGETS ${PROJECT_NAME}
  RUNTIME DESTINATION bin)

ament_package()
