cmake_minimum_required(VERSION 3.0)
project(libedit)

add_library(libedit STATIC
            src/chared.c
            src/el.c
            src/filecomplete.c
            src/history.c
            src/literal.c
            src/prompt.c
            src/refresh.c
            src/strlcat.c
            src/tokenizer.c
            src/unvis.c
            src/wcsdup.c
            src/chartype.c
            src/eln.c
            src/getline.c
            src/historyn.c
            src/map.c
            src/read.c
            src/search.c
            src/strlcpy.c
            src/tokenizern.c
            src/vi.c
            src/common.c
            src/emacs.c
            src/hist.c
            src/keymacro.c
            src/parse.c
            src/readline.c
            src/sig.c
            src/terminal.c
            src/tty.c
            src/vis.c)

target_include_directories(libedit PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/gen"
                                           "${CMAKE_CURRENT_SOURCE_DIR}/gen/src"
                                           "${CMAKE_CURRENT_SOURCE_DIR}/src")
target_link_libraries(libedit PUBLIC ncurses)

