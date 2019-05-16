
include_directories(${CMAKE_SOURCE_DIR}/src)

add_executable(benchmarks-cppma
   main.cpp 
)

target_link_libraries(benchmarks-cppma cppma)

install(
    PROGRAMS ${CMAKE_CURRENT_BINARY_DIR}/benchmarks-cppma
    DESTINATION bin
    RENAME ${CMAKE_PROJECT_NAME}-benchmarks
)
