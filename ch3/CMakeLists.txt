# 设置一个合理的最低CMake版本，以启用现代CMake功能
cmake_minimum_required(VERSION 3.10)

# 定义项目名称和语言
project(chapter3 CXX)

# 使用现代方法设置C++标准（我们之前需要C++17来支持filesystem）
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# === 在顶层统一查找所有依赖项 ===
# 这会让Eigen3和Pangolin在整个项目中都可用
find_package(Eigen3 REQUIRED)
find_package(Pangolin REQUIRED)

# 依次添加所有子目录
# CMake会进入这些子目录并执行其中的CMakeLists.txt文件
add_subdirectory(useEigen)
add_subdirectory(useGeometry)
add_subdirectory(visualizeGeometry)
add_subdirectory(examples)