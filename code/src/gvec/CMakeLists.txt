add_library(gvec STATIC vec.cu)

message(STATUS "includind dir: ${PROJECT_SOURCE_DIR}/include/gvec")
target_include_directories(gvec PUBLIC "${PROJECT_SOURCE_DIR}/include/gvec")

get_target_property(gvec_includes gvec INCLUDE_DIRECTORIES)
message(STATUS "gvec includes: ${gvec_includes}")