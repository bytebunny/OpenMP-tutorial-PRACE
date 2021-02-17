cmake_minimum_required( VERSION 3.13 )
project( mat-mul LANGUAGES C )
add_executable( mat-mul.exe mat-mul.c )

find_package(OpenMP)
if(OpenMP_C_FOUND)
  target_link_libraries( mat-mul.exe PUBLIC OpenMP::OpenMP_C )
endif()
