cmake_minimum_required(VERSION 3.8)
project(stanley_controller_cpp)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
#add_subdirectory(.)

find_package(PythonLibs 3.8 REQUIRED)
find_package(Python 3.8 REQUIRED)
include_directories(${PYTHON_INCLUDE_DIRS})


add_executable(stanley_controller_cpp
        Animation.cpp
        BicycleModel.cpp
        BicycleModel.h
        CubicSpline1D.cpp
        CubicSpline1D.h
        Linear_Interpolation.cpp
        Linear_Interpolation.h
        matplotlibcpp.h
        StanleyController.cpp
        StanleyController.h
        ../../../../../usr/lib/python3/dist-packages/numpy/core/include/numpy/ndarrayobject.h
)

target_link_libraries(stanley_controller_cpp ${PYTHON_LIBRARIES})
