CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

ADD_SUBDIRECTORY(googletest)

ADD_EXECUTABLE(c-echo
    main2.cpp
)
ADD_EXECUTABLE(c-echo-count
	    main.cpp
 )
ADD_EXECUTABLE(test
    test.cpp
)

TARGET_LINK_LIBRARIES(test gtest)
TARGET_COMPILE_DEFINITIONS(test PRIVATE gtest_disable_pthreads=ON)
