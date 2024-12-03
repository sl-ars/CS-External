cmake_minimum_required(VERSION 3.20)
project(Cs2External LANGUAGES CXX)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add preprocessor definitions for Unicode support
add_compile_definitions(UNICODE _UNICODE)

# Include directories
include_directories(
    Source
    Cheats
    Source/ExternalLibs
    Source/ExternalLibs/ImGui
    Source/ExternalLibs/Fonts
    Source/ExternalLibs/Json
)

# Add source files
set(SOURCES
    Cheats/main.cpp
    Source/ExternalLibs/ImGui/imgui.cpp
    Source/ExternalLibs/ImGui/imgui_demo.cpp
    Source/ExternalLibs/ImGui/imgui_draw.cpp
    Source/ExternalLibs/ImGui/imgui_impl_dx11.cpp
    Source/ExternalLibs/ImGui/imgui_impl_win32.cpp
    Source/ExternalLibs/ImGui/imgui_tables.cpp
    Source/ExternalLibs/ImGui/imgui_widgets.cpp
)

# Add header files (optional for IDE integration)
set(HEADERS
    Cheats/Hacks/Aimbot.hpp
    Cheats/Hacks/Antiflash.hpp
    Cheats/Hacks/Bhop.hpp
    Cheats/Hacks/Esp.hpp
    Cheats/Hacks/FovChanger.hpp
    Cheats/Hacks/Loop.hpp
    Cheats/Hacks/Rcs.hpp
    Cheats/Hacks/SensiChanger.hpp
    Cheats/Hacks/Triggerbot.hpp
    Cheats/Readers/Entity.hpp
    Cheats/Readers/Game.hpp
    Cheats/Readers/LocalPlayer.hpp
    Cheats/Utilities/Bomb.hpp
    Cheats/Utilities/Bones.hpp
    Cheats/Utilities/Config.hpp
    Cheats/Utilities/DrawUtils.hpp
    Cheats/Utilities/Gamemodes.hpp
    Cheats/Utilities/Threads.hpp
    Cheats/Utilities/Updater.hpp
    Cheats/Utilities/World.hpp
    Source/ExternalLibs/Fonts/Poppins.hpp
    Source/Functions/Console.hpp
    Source/Globals/Globals.hpp
    Source/Globals/Includes.hpp
    Source/Inputs/Events.hpp
    Source/Interfaces/Elements.hpp
    Source/Interfaces/Interfaces.hpp
    Source/ExternalLibs/ImGui/imconfig.h
    Source/ExternalLibs/ImGui/imgui.h
    Source/ExternalLibs/ImGui/imgui_impl_dx11.h
    Source/ExternalLibs/ImGui/imgui_impl_win32.h
    Source/ExternalLibs/ImGui/imgui_internal.h
    Source/ExternalLibs/ImGui/imstb_rectpack.h
    Source/ExternalLibs/ImGui/imstb_textedit.h
    Source/ExternalLibs/ImGui/imstb_truetype.h
    Source/ExternalLibs/Json/Json.hpp
    Source/Interfaces/Loader.hpp
    Source/Interfaces/LSConfigSystem.hpp
    Source/Maths/Vector.hpp
    Source/Maths/ViewMatrix.hpp
    Source/Maths/WorldToScreen.hpp
    Source/Memory/Handle.hpp
    Source/Memory/Memory.hpp
    Source/Memory/Process.hpp
    Source/Overlay/ExeConfig.hpp
    Source/Overlay/Overlay.hpp
)

# Add executable target
add_executable(Cs2External ${SOURCES} ${HEADERS})

# Link libraries
target_link_libraries(Cs2External
    WinINet
    d3d11
)

# Add compile options
target_compile_options(Cs2External PRIVATE
    $<$<CONFIG:Debug>:-Wall -Wextra>
    $<$<CONFIG:Release>:-O3>
)

# Add include directories for target
target_include_directories(Cs2External PRIVATE
    ${CMAKE_SOURCE_DIR}/Source
    ${CMAKE_SOURCE_DIR}/Cheats
    ${CMAKE_SOURCE_DIR}/Source/ExternalLibs
)
