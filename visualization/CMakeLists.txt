cmake_minimum_required(VERSION 3.10)
project(visualization)

set(CMAKE_CXX_STANDARD 11)
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

add_executable(visualization visualization.cpp)

#set(OpenCV_DIR /Users/mason/opencv/opencv/)
set(OpenCV_DIR /Users/mason/opencv/opencv/build) # from source
#set(OpenCV_DIR /usr/local/Cellar/opencv/3.4.2/share/OpenCV/) # brew opencv
find_package( OpenCV REQUIRED )

target_link_libraries( visualization ${OpenCV_LIBS} )