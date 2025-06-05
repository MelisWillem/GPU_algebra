cmake_minimum_required(VERSION 3.20)
project(GPU_Algebra LANGUAGES CXX CUDA)

# tested with rtx 3060 => Ampere architecture
set(CMAKE_CUDA_ARCHITECTURES 86)


Include(FetchContent)

FetchContent_Declare(
  Catch2
  GIT_REPOSITORY https://github.com/catchorg/Catch2.git
  GIT_TAG        v3.8.1
)

FetchContent_MakeAvailable(Catch2)

set(CMAKE_CXX_STANDARD 17)

add_subdirectory("${CMAKE_SOURCE_DIR}/demos")
add_subdirectory("${CMAKE_SOURCE_DIR}/src/gvec")
add_subdirectory("${CMAKE_SOURCE_DIR}/tests/gvec")

enable_testing()
add_test(NAME gvec_tests COMMAND gvec_tests)