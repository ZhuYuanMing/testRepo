cmake_minimum_required(VERSION 3.12)
project(dsdd)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_PREFIX_PATH C:/Qt/5.13.0/mingw73_64/lib/cmake)
find_package(Qt5Widgets REQUIRED)
find_package(Qt5Core REQUIRED)
find_package(Qt5Gui REQUIRED)

include_directories(C:\\Qt\\5.13.0\\mingw73_64\\include)

set(UI_FILES)
set(RC_FILES)
set(QRC_FILES)


set(SOURCE_FILES ./src/main.cpp
        ./src/mainwindow.cpp
        ./src/adddialog.cpp
        ./src/addresswidget.cpp
        ./src/tablemodel.cpp
        ./src/newaddresstab.cpp
        ./include/adddialog.h
        ./include/addresswidget.h
        ./include/mainwindow.h
        ./include/newaddresstab.h
        ./include/tablemodel.h)


add_executable(dsdd ${RC_FILES} ${SOURCE_FILES} ${UI_FILES} ${QRC_FILES})

target_link_libraries(dsdd Qt5::Widgets)