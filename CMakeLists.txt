cmake_minimum_required (VERSION 2.6)
project (TowerDefenceUnnamed)
set(CMAKE_CODEBLOCKS_EXCLUDE_EXTERNAL_FILES "true")
include_directories ("include/")

set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/CMakeModules" ${CMAKE_MODULE_PATH})

find_package (SFML 2.5 COMPONENTS graphics audio REQUIRED)
find_package(Thor 2 REQUIRED)
include_directories(${THOR_INCLUDE_DIR})

add_executable (TowerDefenceUnnamed Main.cpp src/GameScreen.cpp src/Manager.cpp src/Screen.cpp src/TitleScreen.cpp include/GameScreen.h include/Globas.h include/icon.h include/json.hpp include/Manager.h include/Screen.h include/Tilemap.h include/TitleScreen.h)

target_link_libraries (TowerDefenceUnnamed sfml-graphics sfml-audio ${THOR_LIBRARY})
