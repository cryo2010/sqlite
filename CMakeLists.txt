set(LIB sqlite)
add_library(${LIB} sqlite3.h sqlite3.c)
string(REPLACE " " ";" COMPILE_OPTS "${CMAKE_C_FLAGS}")
list(APPEND COMPILE_OPTS "-O2")
target_compile_options(${LIB} PUBLIC ${COMPILE_OPTS})

