set( BOOST_ROOT ../include/boost_1_65_1 )
set( CMAKE_RUNTIME_OUTPUT_DIRECTORY ../bin )

cmake_minimum_required (VERSION 2.6)
find_package( Boost 1.65.1 REQUIRED )

if(Boost_FOUND)
  include_directories(${Boost_INCLUDE_DIRS})
  project (music-tangram)
  add_executable(music-tangram ../src/main.cpp)
endif()

target_link_libraries( music-tangram LINK_PUBLIC ${Boost_LIBRARIES} )
