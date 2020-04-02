cmake_minimum_required(VERSION 3.0.2)
project(convex_decomposition)

find_package(catkin REQUIRED)

catkin_package()

file(GLOB_RECURSE CD_SOURCE_CODE src/ConvexDecomposition/*.cpp)
add_executable(${PROJECT_NAME} src/DecomposeSample.cpp ${CD_SOURCE_CODE})

install(TARGETS ${PROJECT_NAME}
  RUNTIME DESTINATION ${CATKIN_GLOBAL_BIN_DESTINATION})
