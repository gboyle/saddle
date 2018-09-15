cmake_minimum_required(VERSION 3.11)

include("cmake/HunterGate.cmake")

HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.23.21.tar.gz"
    SHA1 "15e27f2fe47d4f162b5cab1e6dfecc699ebaa304"
)

project(saddle VERSION 0.0.1)


hunter_add_package(SDL2)
find_package(SDL2 CONFIG REQUIRED)

add_executable(
    saddle
    main.cpp
)

target_link_libraries(
    saddle
    SDL2::SDL2main
    SDL2::SDL2
)