cmake_minimum_required(VERSION "3.23.0-rc1")

project("TestCMakeTie")

add_executable("${PROJECT_NAME}" "Main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin)   #${CMAKE_INSTALL_PREFIX}/bin
install(FILES "Main.cpp" DESTINATION src) 			#${CMAKE_INSTALL_PREFIX}/bin

INCLUDE(CTest)

add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")


