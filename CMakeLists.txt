cmake_minimum_required(VERSION 3.10)
project(furgbol-core)

set(CMAKE_INSTALL_PREFIX "${CMAKE_SOURCE_DIR}")

add_subdirectory("ext/vss-vision-proto")
add_subdirectory("ext/ssl-vision-proto")
add_subdirectory("ext/ssl-refbox-proto")
add_subdirectory("ext/grSim-proto")
add_subdirectory("src/furgbol-proto")
add_subdirectory("src/io")

#[[
"ext/lua-5.3.5_Linux319_64_lib/include"
add_library(lua53 STATIC IMPORTED)
set_target_properties(lua53 PROPERTIES IMPORTED_LOCATION "${CMAKE_SOURCE_DIR}/ext/lua-5.3.5_Linux319_64_lib/liblua53.a")
]]
