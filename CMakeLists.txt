# CMakeLists files in this project can
# refer to the root source directory of the project as ${HELLO_SOURCE_DIR} and
# to the root binary directory of the project as ${HELLO_BINARY_DIR}.
cmake_minimum_required (VERSION 2.8.11)
project (PDI)

# Recurse into the "Hello" and "Demo" subdirectories. This does not actually
# cause another cmake executable to run. The same process will walk through
# the project's entire directory structure.
add_executable (Eigenfaces Eigenfaces/eigenfaces.cpp)
add_executable (Fihserfaces Fihserfaces/fihserfaces.cpp)
add_executable (LBP LBP/lbp.cpp)

#Dependencies

find_package(OpenCV REQUIRED)
target_link_libraries(Eigenfaces ${OpenCV_LIBS})
target_link_libraries(Fihserfaces ${OpenCV_LIBS})
target_link_libraries(LBP ${OpenCV_LIBS})