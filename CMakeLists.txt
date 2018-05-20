cmake_minimum_required(VERSION 2.8.3)
project(core)
set(PROJECT_VERSION 1.2.1)



add_library(core SHARED core.cpp)



set_target_properties(${CMAKE_PROJECT_NAME}
    PROPERTIES   VERSION ${PROJECT_VERSION}
)

install(TARGETS ${CMAKE_PROJECT_NAME}
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
)

install(FILES
            ${CMAKE_CURRENT_LIST_DIR}/core.h
    DESTINATION include/${PROJECT_NAME}
)
