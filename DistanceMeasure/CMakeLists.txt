PROJECT(DistanceMeasure C CXX)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

FIND_PACKAGE(OpenCV REQUIRED)
FIND_PACKAGE(OpenGL REQUIRED)
FIND_PACKAGE(GLUT)

FIND_PATH(ARTP_INCLUDES ARToolKitPlus/ARToolKitPlus.h)
FIND_LIBRARY(ARTP_LIBS ARToolkitPlus)
INCLUDE_DIRECTORIES(${ARTP_INCLUDES})

ADD_EXECUTABLE(DistanceMeasure main.cpp)
TARGET_LINK_LIBRARIES(DistanceMeasure ${ARTP_LIBS} ${OpenCV_LIBS} ${OPENGL_gl_LIBRARY} ${OPENGL_glu_LIBRARY} ${GLUT_glut_LIBRARY})
