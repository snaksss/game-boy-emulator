

file (GLOB sources CONFIGURE_DEPENDS "${PROJECT_SOURCE_DIR}/lib/*.c")

file (GLOB headers CONFIGURE_DEPENDS "${PROJECT_SOURCE_DIR}/include/*.h")

add_library(emu STATIC ${sources} ${headers})

target_include_directories(emu PUBLIC ${PROJECT_SOURCE_DIR}/include )


# Add SDL2 include directories
include_directories(/opt/homebrew/include)
include_directories(${CMAKE_SOURCE_DIR}/include)


# Create the library
add_library(gbemu_lib
    bus.c
    cart.c
    common.c
    cpu.c
    emu.c
    ppu.c
    timer.c
)



# Link the library with SDL2
target_link_libraries(gbemu_lib SDL2 SDL2_ttf)


if (WIN32)
  target_include_directories(emu PUBLIC "${PROJECT_SOURCE_DIR}/../windows_deps/sdl2/include" )
  target_include_directories(emu PUBLIC ${PROJECT_SOURCE_DIR}/../windows_deps/sdl2_ttf/include )
else()
  target_include_directories(emu PUBLIC ${SDL2_INCLUDE_DIR})
  target_link_libraries(emu PUBLIC ${SDL2_LIBRARY}) 
  target_link_libraries(emu PUBLIC ${SDL2_TTF_LIBRARY}) 
endif()

include_directories("/usr/local/include")
include_directories(${SDL2_INCLUDE_DIRS})
target_link_libraries(emu ${SDL2_LIBRARIES})
target_link_libraries(emu ${SDL2_TTF_LIBRARIES})
