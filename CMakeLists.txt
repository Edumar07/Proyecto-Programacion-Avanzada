cmake_minimum_required(VERSION 3.14)

project(Proyecto_Programacion_Avanzada LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core)

add_executable(Proyecto_Programacion_Avanzada
  main.cpp
)
target_link_libraries(Proyecto_Programacion_Avanzada Qt${QT_VERSION_MAJOR}::Core)

include(GNUInstallDirs)
install(TARGETS Proyecto_Programacion_Avanzada
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
