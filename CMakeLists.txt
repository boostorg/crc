cmake_minimum_required(VERSION 3.5)
project(boost-crc LANGUAGES CXX)

add_library(boost_crc INTERFACE)
add_library(Boost::crc ALIAS boost_crc)

target_include_directories(boost_crc INTERFACE include)

target_link_libraries(boost_crc
    INTERFACE
        Boost::assert
        Boost::array
        Boost::config
        Boost::core
        Boost::integer
        Boost::static_assert
        Boost::throw_exception
        Boost::type_traits
)

