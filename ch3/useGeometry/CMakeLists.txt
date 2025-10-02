# 定义可执行文件目标
add_executable(eigenGeometry useGeometry.cpp)

# 将该目标链接到 Eigen3 库
target_link_libraries(eigenGeometry PRIVATE Eigen3::Eigen)
