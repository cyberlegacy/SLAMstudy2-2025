# === 定义 coordinateTransform 目标 ===
add_executable(coordinateTransform coordinateTransform.cpp)

# 将 coordinateTransform 目标链接到 Eigen3
# Eigen3::Eigen 是一个 IMPORTED 目标，它包含了所有需要的信息（头文件路径等）
# 不再需要手动 include_directories("/usr/include/eigen3")
target_link_libraries(coordinateTransform PRIVATE Eigen3::Eigen)


# === 定义 plotTrajectory 目标 ===
add_executable(plotTrajectory plotTrajectory.cpp)

# 显式地将Pangolin的头文件目录添加到目标的包含路径中
target_include_directories(plotTrajectory PRIVATE ${Pangolin_INCLUDE_DIRS})

# 将 plotTrajectory 目标链接到Pangolin库
target_link_libraries(plotTrajectory PRIVATE ${Pangolin_LIBRARIES})
