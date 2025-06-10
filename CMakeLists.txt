cmake_minimum_required(VERSION 3.5)

project(boost_template_app) # <-- change this for your name

include(FetchContent)

FetchContent_Declare(boost
    GIT_REPOSITORY https://github.com/boostorg/boost.git
    GIT_TAG boost-1.88.0
)

FetchContent_MakeAvailable(boost)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE Boost::spirit)

