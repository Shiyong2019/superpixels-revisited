include_directories(../lib_seeds_revised/ ../lib_seeds/)

find_package(Boost COMPONENTS system filesystem program_options REQUIRED)
find_package(OpenCV REQUIRED)

include_directories(${EIGEN_INCLUDE_DIRS})

add_executable(seeds_cli main.cpp)
target_link_libraries(seeds_cli ${Boost_LIBRARIES} ${OpenCV_LIBS} seeds_revised seeds)
