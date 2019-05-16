

find_package(GTest REQUIRED)

include_directories(
    ${CMAKE_SOURCE_DIR}/src
    ${GTEST_INCLUDE_DIRS}
)

file(
    GLOB
    test_files
    *.cpp
)

add_executable(Tests-cppma
    ${test_files}
)

target_link_libraries(Tests-cppma
    cppma
    ${GTEST_BOTH_LIBRARIES}
)
