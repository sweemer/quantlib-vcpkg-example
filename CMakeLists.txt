cmake_minimum_required(VERSION 3.20.0)
project(quantlib-vcpkg-example LANGUAGES CXX)
add_executable(quantlib-vcpkg-example main.cpp)

if(WIN32)
  target_link_libraries(debug QuantLib-x64-mt-sgd.lib optimized QuantLib-x64-mt-s.lib)
else()
  target_link_libraries(quantlib-vcpkg-example QuantLib)
endif()
