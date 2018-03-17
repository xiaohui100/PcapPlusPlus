file(GLOB files "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/header  ${CommonHeader} ${PacketHeader} ${3rdParty} /usr/include/netinet)

add_library(Pcap++ SHARED ${files})