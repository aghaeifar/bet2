cmake_minimum_required(VERSION 3.11.1)
PROJECT(fslio)

# add_subdirectory(znz)

INCLUDE_DIRECTORIES(.  .. )

set(Srcs fslio.c)

add_library(fslio ${Srcs})

