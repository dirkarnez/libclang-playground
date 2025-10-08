cmake_minimum_required(VERSION 3.24)
project("function-visitor" CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)


include_directories (${LIBCLANG_INCLUDE_DIRS} SYSTEM)

add_executable("function-visitor"
  "src/arguments.cc"
  "src/function-visitor.cc"
  "src/path_utilities.cc"
)

target_link_libraries("function-visitor" ${LIBCLANG_LIBRARIES})

target_link_options("function-visitor" 
  PRIVATE "-static"
)
