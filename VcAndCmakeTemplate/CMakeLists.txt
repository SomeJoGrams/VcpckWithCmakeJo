# CMakeList.txt: CMake-Projekt für "VcAndCmakeTemplate". Schließen Sie die Quelle ein, und definieren Sie
# projektspezifische Logik hier.
#


find_package(fmt CONFIG REQUIRED)


# Fügen Sie der ausführbaren Datei dieses Projekts eine Quelle hinzu.
add_executable (VcAndCmakeTemplate "VcAndCmakeTemplate.cpp" "VcAndCmakeTemplate.h")


target_link_libraries(VcAndCmakeTemplate PRIVATE fmt::fmt)
    # Or use the header-only version
#target_link_libraries(VcAndCmakeTemplate PRIVATE fmt::fmt-header-only)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET VcAndCmakeTemplate PROPERTY CXX_STANDARD 20)
endif()

# TODO: Fügen Sie bei Bedarf Tests hinzu, und installieren Sie Ziele.
