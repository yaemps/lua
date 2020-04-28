cmake_minimum_required (VERSION 2.8)

project (Lua)
aux_source_directory(. DIR_SRCS)

list(REMOVE_ITEM DIR_SRCS "./onelua.c")

list(REMOVE_ITEM DIR_SRCS "./luac.c")
message("${DIR_SRCS}")
add_executable(lua ${DIR_SRCS})

aux_source_directory(. DIR_SRCS1)

list(REMOVE_ITEM DIR_SRCS1 "./onelua.c")
list(REMOVE_ITEM DIR_SRCS1 "./lua.c")
message("${DIR_SRCS}")
add_executable(luac ${DIR_SRCS1})

#add_executable(luaone onelua.c)
