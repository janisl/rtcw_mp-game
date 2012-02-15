project(rtcw_mp-game)

cmake_minimum_required(VERSION 2.6)
if(COMMAND cmake_policy)
	cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

option(ENABLE_DEMO "Build pre-release demo version")

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -pipe -fsigned-char")
set(CMAKE_C_FLAGS_RELEASE "-DNDEBUG -O6 -fomit-frame-pointer -ffast-math -malign-loops=2 -malign-jumps=2 -malign-functions=2 -fno-strict-aliasing -fstrength-reduce")

include(CheckTypeSize)
check_type_size(void*  SIZEOF_VOID_PTR)

if(${SIZEOF_VOID_PTR} MATCHES "8")
	set(ARCH "x86_64")
else()
	set(ARCH "i386")
	set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -mcpu=pentiumpro -march=pentium")
endif()
message(STATUS "Using platform suffix ${ARCH}")

if(ENABLE_DEMO)
add_definitions(-DPRE_RELEASE_DEMO)
endif()

set(LIBRARY_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR})

add_subdirectory(src)
