## Slambook2
# My Learning Journey with "Visual SLAM Fourteen Lectures" (slambook2)

This repository contains my personal study notes and code implementations while working through the second edition of the excellent book, *Visual SLAM Fourteen Lectures* (视觉SLAM十四讲).

The primary goal of this repository is for my own learning. As part of this process, I have refactored the original project's build system to use modern, portable CMake best practices. This makes the code easier to compile and manage in modern development environments like CLion or VS Code (Cursor).

---

## Acknowledgments

A huge thank you to the original author, Dr. Gao Xiang (高翔), for this fantastic book and the accompanying source code. This work would not be possible without his effort.

The original, official repository can be found here: **[gaoxiang12/slambook2](https://github.com/gaoxiang12/slambook2)**

---

## Key Modifications

The core logic of the SLAM algorithms remains untouched. The main changes are focused on the build system and project structure:

* **Modern CMake Structure**: The entire project has been refactored to use a modern, target-based CMake approach.
* **Centralized Dependency Management**: All dependencies (Eigen, Pangolin, etc.) are now found once in the top-level `CMakeLists.txt` and are linked to specific targets as needed.
* **Improved Portability**: Removed all hardcoded system paths to ensure the project can be built on different machines without modification.
* **IDE-Friendly**: The new structure is fully compatible with modern IDEs, providing correct code completion, indexing, and debugging support.
* **C++17 Standard**: The project is configured to use the C++17 standard.

---
---

