cmake_minimum_required(VERSION 3.5)
# Set extension name here
set(TARGET_NAME chsql)
# DuckDB's extension distribution supports vcpkg. As such, dependencies can be added in ./vcpkg.json and then
# used in cmake with find_package. Feel free to remove or replace with other dependencies.
# Note that it should also be removed from vcpkg.json to prevent needlessly installing it..
set(EXTENSION_NAME ${TARGET_NAME}_extension)
set(LOADABLE_EXTENSION_NAME ${TARGET_NAME}_loadable_extension)
project(${TARGET_NAME})
set(EXT_NAME chsql)
set(DUCKDB_EXTENSION_CONFIGS ../chsql/extension_config.cmake)
add_subdirectory(./duckdb)
