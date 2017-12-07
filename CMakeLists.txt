cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
  URL "https://github.com/ruslo/hunter/archive/v0.20.53.tar.gz"
  SHA1 "56ac21f53b95ad8d56fbee39b227608bafcbd84e"
)

project(message_runtime)

hunter_add_package(catkin)
hunter_add_package(roscpp_core)

find_package(catkin REQUIRED)

catkin_package(CATKIN_DEPENDS cpp_common roscpp_serialization roscpp_traits rostime)
