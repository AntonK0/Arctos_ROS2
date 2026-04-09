cmake_minimum_required(VERSION 3.8)
project(arctos_urdf_description)

find_package(ament_cmake REQUIRED)

install(
  DIRECTORY urdf launch config
  DESTINATION share/${PROJECT_NAME}
)

if(EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/meshes")
  install(
    DIRECTORY meshes
    DESTINATION share/${PROJECT_NAME}
  )
endif()

ament_package()
