cmake_minimum_required(VERSION 3.5)
set(CMAKE_CXX_STANDARD 14)
PROJECT(proyect)

#---------------to-opencv------------
#find_package( OpenCV REQUIRED ) #find_package( OpenCV 4 REQUIRED )
#include_directories( ${OpenCV_INCLUDE_DIRS})

MACRO(add_example name)
  ADD_EXECUTABLE(${name} src/${name}.cpp)
  TARGET_LINK_LIBRARIES(${name} ${OpenCV_LIBS})
ENDMACRO()

add_example(hello)
#add_example(programa1)
#add_example(programa2)
#add_example(programa3)
#add_example(programa4)
