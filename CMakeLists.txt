# Generated by `boostdep --cmake crc`
# Copyright 2020, 2021 Peter Dimov
# Distributed under the Boost Software License, Version 1.0.
# https://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.8...3.20)

project(boost_crc VERSION "${BOOST_SUPERPROJECT_VERSION}" LANGUAGES CXX)

add_library(boost_crc INTERFACE)
add_library(Boost::crc ALIAS boost_crc)

target_include_directories(boost_crc INTERFACE include)

target_compile_features(boost_crc INTERFACE cxx_std_11)

if(BUILD_TESTING AND EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/test/CMakeLists.txt")

  add_subdirectory(test)

endif()
