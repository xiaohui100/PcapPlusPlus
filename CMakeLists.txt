cmake_minimum_required(VERSION 3.6)
project(PcapPlusPlus)

set(CMAKE_CXX_STANDARD 11)

set(CMKAE_C_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -g -O0")
set(CMKAE_C_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE}  -O3")
set(CMKAE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -g -O0")
set(CMKAE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE}  -O3")

add_definitions(-DLINUX)

set(CommonHeader "${PROJECT_SOURCE_DIR}/Common++/header")
set(PacketHeader "${PROJECT_SOURCE_DIR}/Packet++/header")
set(PcapHeader "${PROJECT_SOURCE_DIR}/Pcap++/header")
set(3rdParty "${PROJECT_SOURCE_DIR}/3rdParty/LightPcapNg/LightPcapNg/include")

set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

add_subdirectory(Common++)
add_subdirectory(Packet++)
add_subdirectory(Pcap++)
add_subdirectory(3rdParty/LightPcapNg/LightPcapNg)

message("LIBRARY_OUTPUT_PATH:" ${LIBRARY_OUTPUT_PATH})