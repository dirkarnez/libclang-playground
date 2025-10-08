cmake_minimum_required(VERSION 3.24)
project("libclang-experiments" CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

list(APPEND CMAKE_MODULE_PATH
  ${CMAKE_SOURCE_DIR}/cmake/Modules
)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Wextra -pedantic")

find_package(libclang REQUIRED)

add_subdirectory("function-visitor")
add_subdirectory("ast-walker")


# add_executable("function-visitor"
#   "arguments.cc"
#   "function-visitor.cc"
#   "path_utilities.cc"
# )

# add_executable("ast-dumper"
#   "ast-dumper.cc"
# )

# add_executable("ast-walker"
#   "ast-walker.cc"
# )

# add_executable("count-function-extents"
#   "count-function-extents.cc"
# )

# add_executable("stockhausen"
#   "stockhausen.cc"
# )

# target_link_libraries("function-visitor" ${LIBCLANG_LIBRARIES})
# target_link_libraries("ast-dumper" ${LIBCLANG_LIBRARIES})
# target_link_libraries("ast-walker" ${LIBCLANG_LIBRARIES})
# target_link_libraries("stockhausen" ${LIBCLANG_LIBRARIES})
# target_link_libraries("count-function-extents" ${LIBCLANG_LIBRARIES})

# target_link_options("function-visitor" 
#   PRIVATE "-static"
# )

# target_link_options("ast-dumper" 
#   PRIVATE "-static"
# )

# target_link_options("ast-walker" 
#   PRIVATE "-static"
# )

# target_link_options("stockhausen" 
#   PRIVATE "-static"
# )

# target_link_options("count-function-extents" 
#   PRIVATE "-static"
# )
