cmake_minimum_required( VERSION 3.13 )
project( sin-cos LANGUAGES C )
add_executable( sin-cos.exe sin-cos.c )

find_package(OpenMP)
if(OpenMP_C_FOUND)
  target_link_libraries( sin-cos.exe PUBLIC OpenMP::OpenMP_C )
endif()
