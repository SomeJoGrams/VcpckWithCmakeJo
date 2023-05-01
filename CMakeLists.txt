# CMakeList.txt: CMake-Projektdatei der obersten Ebene. Führen Sie hier die globale Konfiguration aus,
# und schließen Sie Unterprojekte ein.
#
cmake_minimum_required (VERSION 3.8)

# Enable Hot Reload for MSVC compilers if supported.
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()


set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/VcAndCmakeTemplate/extern/vcpkg/scripts/buildsystems/vcpkg.cmake")

  
#message("test again" ${CMAKE_TOOLCHAIN_FILE})
#set(VCPKG_ROOT "${CMAKE_CURRENT_SOURCE_DIR}/VcAndCmakeTemplate/extern/vcpkg"
  #CACHE STRING "Vcpkg toolchain file")


#set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/extern/vcpkg/scripts/buil

project ("VcAndCmakeTemplate")


# Schließen Sie Unterprojekte ein.
add_subdirectory ("VcAndCmakeTemplate")
