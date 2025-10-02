# 定义可执行文件目标
add_executable(eigenMatrix eigenMatrix.cpp)

# 将该目标链接到 Eigen3 库
# Eigen3::Eigen 是由顶层 CMakeLists.txt 找到的，这里直接使用即可
# 它会自动处理头文件路径，不再需要 include_directories
target_link_libraries(eigenMatrix PRIVATE Eigen3::Eigen)