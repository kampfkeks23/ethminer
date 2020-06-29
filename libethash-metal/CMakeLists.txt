file(GLOB sources "*.cpp")
file(GLOB headers "*.h")

add_library(ethash-metal ${sources} ${headers})
target_link_libraries(ethash-metal ethcore ethash::ethash Boost::thread)
target_include_directories(ethash-metal PRIVATE .. ${CMAKE_CURRENT_BINARY_DIR})
