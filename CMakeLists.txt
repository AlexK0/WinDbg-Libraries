cmake_minimum_required(VERSION 3.16)

project(WinDbg-Libraries)

add_library(DbgModelCppLib INTERFACE)
add_library(WinDbg-Libraries::DbgModelCppLib ALIAS DbgModelCppLib)

target_include_directories(DbgModelCppLib
        INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/DbgModelCppLib>
)
