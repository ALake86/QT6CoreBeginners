cmake_minimum_required(VERSION 3.16)

project(QT6CoreBeginnersTest LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core)

add_executable(QT6CoreBeginnersTest
  main.cpp
  README.md
  Section01/README.md
  Section02/README.md
  Section03/README.md
  Section04/README.md
  Section05/README.md
  Section06/README.md
  Section07/README.md
  Section08/README.md
  Section09/README.md
  Section10/README.md
  Section11/README.md
  Section12/README.md
  Section13/README.md
  Section14/README.md
  Section15/README.md
  Section16/README.md
)
target_link_libraries(QT6CoreBeginnersTest PRIVATE Qt${QT_VERSION_MAJOR}::Core)

include(GNUInstallDirs)
install(TARGETS QT6CoreBeginnersTest
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
