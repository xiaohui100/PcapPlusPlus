file(GLOB files "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/header /usr/include/netinet)

add_library(Common++ SHARED ${files})