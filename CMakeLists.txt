cmake_minimum_required( VERSION 3.8 )

project( fragmentzip ) 

add_library( fragmentzip libfragmentzip/libfragmentzip.c )
target_include_directories( fragmentzip PUBLIC include include/libfragmentzip )

if( BUILD_EXE )
    add_executable( fragmentzip_exe libfragmentzip/main.c )
    target_link_libraries( fragmentzip_exe fragmentzip )
endif()
