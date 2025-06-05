add_executable(gvec_tests 
        vecTests.cpp
        )
target_link_libraries(gvec_tests PUBLIC gvec Catch2::Catch2WithMain)
