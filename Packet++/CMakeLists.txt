file(GLOB files "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/header ${CommonHeader} /usr/include/netinet)

add_library(Packet++ SHARED ${files})