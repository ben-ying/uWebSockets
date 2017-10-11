FILE(GLOB_RECURSE SOURCES *.[ch]pp *.[ch])
VS_GROUP_SOURCES("${SOURCES}" ${CMAKE_CURRENT_SOURCE_DIR})

BUILD_ARTIFACT("lib-static" ${SOURCES})

SET(LIBSRC Asio.h
        Backend.h
        Epoll.cpp
        Epoll.h
        Extensions.cpp
        Extensions.h
        Group.cpp
        Group.h
        HTTPSocket.cpp
        HTTPSocket.h
        Hub.cpp
        Hub.h
        Libuv.h
        Networking.cpp
        Networking.h
        Node.cpp
        Node.h
        Socket.cpp
        Socket.h
        WebSocket.cpp
        WebSocket.h
        WebSocketProtocol.h
        uWS.h)

ADD_LIBRARY(uWS ${LIBSRC})
