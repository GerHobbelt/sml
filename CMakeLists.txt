#
# Copyright (c) 2016-2019 Jean Davy
#
# Distributed under the Boost Software License, Version 1.0.
# (See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#

###########################################################################################
cmake_minimum_required(VERSION 3.13)
project(sml LANGUAGES CXX)


include(GNUInstallDirs)
install(DIRECTORY "include/boost" DESTINATION "${CMAKE_INSTALL_INCLUDEDIR}")

add_library(Sml INTERFACE)

target_include_directories(Sml
    INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)
