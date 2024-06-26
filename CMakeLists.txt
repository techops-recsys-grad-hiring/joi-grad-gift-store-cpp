cmake_minimum_required(VERSION 3.14)
project(GiftStoreApp)

# GoogleTest requires at least C++14
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FetchContent)
FetchContent_Declare(
  googletest
  URL https://github.com/google/googletest/archive/refs/tags/v1.14.0.zip
)
# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

# Add source files
add_executable(GiftStoreApp
  src/gift_store.cpp
  src/service/gift_service.h
  src/model/gift.cpp
  src/model/transaction.hpp
)

# Add test files
add_executable(GiftStoreAppTest
  test/gift_store_test.cpp
  test/service/gift_service_test.cpp
)

# Link GoogleTest to the test executable
enable_testing()
target_link_libraries(GiftStoreAppTest GTest::gtest_main)
include(GoogleTest)
gtest_discover_tests(GiftStoreAppTest)

