cmake_minimum_required(VERSION 03.10)

project(
  yocto_recipe
  LANGUAGES C
  VERSION 1.0.0)

add_executable(${PROJECT_NAME} main.c)
target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Werror)

include(GNUInstallDirs)
install(
  TARGETS ${PROJECT_NAME}
  RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
          PERMISSIONS OWNER_READ OWNER_EXECUTE GROUP_READ GROUP_EXECUTE
                      WORLD_READ WORLD_EXECUTE)
