cmake_minimum_required(VERSION 3.10)
project(vss-vision-proto)

find_package(Protobuf REQUIRED)

protobuf_generate_cpp(VSS_VISION_PROTO_CPP VSS_VISION_PROTO_H
  "state.proto")

add_library(${PROJECT_NAME}
  ${VSS_VISION_PROTO_CPP})
target_link_libraries(${PROJECT_NAME}
  ${Protobuf_LIBRARIES})

install(TARGETS ${PROJECT_NAME}
  DESTINATION "lib")
install(FILES ${VSS_VISION_PROTO_H}
  DESTINATION "include/vss-vision-proto")