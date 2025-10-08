cmake_minimum_required(VERSION 3.24)
project("ast-walker" CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)


include_directories (${LIBCLANG_INCLUDE_DIRS} SYSTEM)

add_executable("ast-walker"
  "src/ast-walker.cc"
)

target_link_libraries("ast-walker" ${LIBCLANG_LIBRARIES})

target_link_options("ast-walker"
  PRIVATE "-static"
)
