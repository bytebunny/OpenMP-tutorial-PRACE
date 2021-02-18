cmake_minimum_required( VERSION 3.13 )
project( MatMul LANGUAGES C )
add_executable( matmul.exe )

target_sources( matmul.exe
  PRIVATE matmul.c )

find_package(OpenMP)
if(OpenMP_C_FOUND)
  target_link_libraries( matmul.exe PUBLIC OpenMP::OpenMP_C )
endif()
