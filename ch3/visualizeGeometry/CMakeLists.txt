# 定义可执行文件目标
add_executable(visualizeGeometry visualizeGeometry.cpp)

# --- 为该目标添加依赖 ---

# 1. 添加Pangolin的头文件目录
target_include_directories(visualizeGeometry PRIVATE ${Pangolin_INCLUDE_DIRS})

# 2. 链接Pangolin和Eigen3的库
#    Pangolin_LIBRARIES 和 Eigen3::Eigen 都是由顶层 CMakeLists.txt 准备好的
target_link_libraries(visualizeGeometry PRIVATE
        ${Pangolin_LIBRARIES}
        Eigen3::Eigen
)
