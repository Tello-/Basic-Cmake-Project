cmake_minimum_required(VERSION "3.15.0")

#Define a project name
project("HelloWorld")

#De-reference variables in CMake with ${}
#It is wise to wrap strings in double-quotes in CMAKE
#Cmake uses spaces as a delimiter and lack of "" can result in parsing error
#ex: "${PROJECT_NAME}"


#Creates executable target in CMake
#@Param : Name of exe
#@Param : Source code required to build exe
add_executable("${PROJECT_NAME}" "main.cpp")


install(TARGETS "${PROJECT_NAME}" DESTINATION bin) #${CMAKE_INSTALL_PREFIX}/bin
install(FILES "main.cpp" DESTINATION src) #${CMAKE_INSTALL_PREFIX}/src
