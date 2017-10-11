CMAKE_MINIMUM_REQUIRED(VERSION 3.0)
PROJECT(${MODULE_NAME})

CREATE_DOXYGEN_DOC(${MODULE_PATH}/src) 

ADD_SUBDIRECTORY(src)

SET(LIBSRC src/Asio.h
        src/Backend.h
        src/Epoll.cpp
        src/Epoll.h
        src/Extensions.cpp
        src/Extensions.h
        src/Group.cpp
        src/Group.h
        src/HTTPSocket.cpp
        src/HTTPSocket.h
        src/Hub.cpp
        src/Hub.h
        src/Libuv.h
        src/Networking.cpp
        src/Networking.h
        src/Node.cpp
        src/Node.h
        src/Socket.cpp
        src/Socket.h
        src/WebSocket.cpp
        src/WebSocket.h
        src/WebSocketProtocol.h
        src/uWS.h)

ADD_LIBRARY(uWS ${LIBSRC})
