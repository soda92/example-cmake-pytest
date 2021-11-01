cmake_minimum_required(VERSION "3.16")
project(example_cmake_pytest)

enable_testing()
find_package(Python3 COMPONENTS Interpreter)
if(Python3_Interpreter_FOUND)
  add_test(NAME TestPython COMMAND Python3::Interpreter  -m pytest WORKING_DIRECTORY ${PROJECT_SOURCE_DIR})
endif()
