cmake_minimum_required(VERSION 3.16)

project(Planetoids_cpp LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(Planetoids_cpp main.cpp
    game.h game.cpp
    worldvector.h
    celestial.h celestial.cpp
    celestial.cpp celestial.h
    celestial.h
    worldvector.cpp
    celestialview.h celestialview.cpp
    solarconstants.h )
target_link_libraries(${PROJECT_NAME} raylib)

include(GNUInstallDirs)
install(TARGETS Planetoids_cpp
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
