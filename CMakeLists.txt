cmake_minimum_required(VERSION 3.26.1)
project(tetris VERSION 0.1.0)
set(CMAKE_CXX_STANDARD 17)

include(CTest)
enable_testing()

set(SOURCES game.h board.h piece.h cell.h game.cpp board.cpp piece.cpp cell.cpp)
add_executable(${PROJECT_NAME} main.cpp ${SOURCES})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)