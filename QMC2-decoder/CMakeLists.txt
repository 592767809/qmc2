﻿# CMakeList.txt : CMake project for QMC2-decoder, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

# Add source to this project's executable.
add_executable (QMC2-decoder
	"QMC2-decoder.cpp"
	"QMC2-decoder.h"
)

include_directories($<TARGET_PROPERTY:QMC2-crypto,INTERFACE_INCLUDE_DIRECTORIES>)

target_link_libraries(QMC2-decoder QMC2-crypto)

# TODO: Add tests and install targets if needed.
