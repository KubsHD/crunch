file(GLOB_RECURSE crunch_SRC RELATIVE
    "${CMAKE_CURRENT_SOURCE_DIR}"
    "*.h"
    "*.cpp"
    "*.rc"
    "*.ico"
)

add_definitions ( -D_UNICODE )

add_executable(
    Crunch
    ${crunch_SRC}
)

set_property(TARGET Crunch PROPERTY VS_DEBUGGER_WORKING_DIRECTORY $<TARGET_FILE_DIR:LevelEditor>)

