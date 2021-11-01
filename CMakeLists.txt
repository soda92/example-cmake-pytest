cmake_minimum_required(VERSION "3.16")
project(example_cmake_pytest)

enable_testing()
add_test(NAME TestPython COMMAND python -m pytest WORKING_DIRECTORY ${PROJECT_SOURCE_DIR})
