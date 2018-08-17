cmake_minimum_required(VERSION 3.4)

set (PROJECT epoll_examples)

project (${PROJECT} C)
set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

add_executable (eventfd_thread_pool eventfd_thread_pool/eventfd_thread_pool.c)
target_link_libraries(eventfd_thread_pool Threads::Threads)

add_executable (timerfd_thread_pool timerfd_thread_pool/timerfd_thread_pool.c)
target_link_libraries(timerfd_thread_pool Threads::Threads)
