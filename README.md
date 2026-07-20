<h1 align="center"> Rope simulation </h1>

<p align="center">
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?logo=cplusplus&logoColor=fff&style=for-the-badge">
  <img src="https://img.shields.io/badge/OpenGL-5586A4?logo=opengl&logoColor=fff&style=for-the-badge">
  <img src="https://img.shields.io/badge/CMake-064F8C?logo=cmake&logoColor=fff&style=for-the-badge">
  <img src="https://img.shields.io/badge/physics-pink?style=for-the-badge&logo=pipecat&logoColor=black">
</p>
<p align="center"> Simulation of a rope under the effect of gravity </p>

<p align="center">
  <img width="400" height="400" alt="compressed_vertical_rope" src="https://github.com/user-attachments/assets/d72ea85a-7a8c-4f46-ab0d-9762c4777df2" width = "45%">
  <img width="400" height="400" alt="horizontal_rope" src="https://github.com/user-attachments/assets/71f2ccd4-bd5e-461d-a086-079a0ad4ff21" width = "45%">
</p>

| | |
|---|---|
| **Concepts** | Verlet Integration, Constraints, Real-time Simulation |
| **Context** | Introduction to C++ and Numerical Methods course |
| **Status** | Completed |


## Table of Contents

- [Implementation](#implementation)
- [Folder Structure](#folder-structure)
- [Building Instructions](#building-instructions)
- [References](#references)

## Implementation

## Folder Structure

Estructura acá

## Building Instructions

#### Windows building
All relevant libraries are found in /dependencies. It is necessary to download and configure CMake
(https://cmake.org/download/). Run CMake script and generate project of choice.

#### Linux/WSL building
It is necessary to have CMake, Git and the required packages: Using root (sudo) and type ```apt-get install libsoil-dev
libglm-dev libglew-dev libglfw3-dev```

### Build through CMake command line:
```
cd /path/to/Rope_simulation
mkdir build && cd build
cmake ..
make
```
## References
1. R. Badea, *[Owlree—Simulating a Rope (Games Series)](https://owlree.blog/posts/simulating-a-rope.html)*. Accessed: Apr. 4, 2024.

   

Final project for Introduction to C++ and Numerical Methods. GitHub repository: https://github.com/VelasquezE/Rope_simulation.

### General objective
Simulate a rope under the effect of gravity and the inner interactions between the segments. 

### Specific objectives
1. Install and get familiarize with the necessary libraries for rendering the rope with OpenGL
2. Visualize the system of particles as an static rope
3. Implement the Verlet integration method for updating the positions of the points that make up the rope
4. Implement the constraint between segments using the Jakobsen method
5. Visualize the movement of the rope using OpenGL and allowing the interaction with the user


