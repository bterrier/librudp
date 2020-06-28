cmake_minimum_required(VERSION 3.5)

project(rudp LANGUAGES C)

set(SOURCES 
  src/address.c
  src/client.c
  src/endpoint.c
  src/packet.c
  src/peer.c
  src/rudp.c
  src/rudp_error.h
  src/rudp_list.h
  src/rudp_packet.h
  src/rudp_rudp.h
  src/server.c)

add_library(rudp
    ${SOURCES}
    )
target_link_libraries(rudp PUBLIC ela)
target_include_directories(rudp PUBLIC include)