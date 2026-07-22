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
- [Future work](#future-work)
- [References](#references)

## Implementation
<img width="281" height="311" alt="flow_diagram" src="https://github.com/user-attachments/assets/2702765d-5550-408e-b3ca-2ddb552eafd6" />
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<!-- Created with Inkscape (http://www.inkscape.org/) -->

<svg
   width="74.461838mm"
   height="82.338295mm"
   viewBox="0 0 74.461838 82.338295"
   version="1.1"
   id="svg1"
   inkscape:version="1.4.4 (dcaf3e7, 2026-05-05)"
   sodipodi:docname="flow_diagram.svg"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:svg="http://www.w3.org/2000/svg">
  <sodipodi:namedview
     id="namedview1"
     pagecolor="#ffffff"
     bordercolor="#000000"
     borderopacity="0.25"
     inkscape:showpageshadow="2"
     inkscape:pageopacity="0.0"
     inkscape:pagecheckerboard="0"
     inkscape:deskcolor="#d1d1d1"
     inkscape:document-units="mm"
     inkscape:zoom="1.3772587"
     inkscape:cx="146.30512"
     inkscape:cy="129.60528"
     inkscape:window-width="1920"
     inkscape:window-height="991"
     inkscape:window-x="-9"
     inkscape:window-y="-9"
     inkscape:window-maximized="1"
     inkscape:current-layer="layer1" />
  <defs
     id="defs1">
    <marker
       style="overflow:visible"
       id="ArrowWide"
       refX="0"
       refY="0"
       orient="auto-start-reverse"
       inkscape:stockid="Wide arrow"
       markerWidth="1"
       markerHeight="1"
       viewBox="0 0 1 1"
       inkscape:isstock="true"
       inkscape:collect="always"
       preserveAspectRatio="xMidYMid">
      <path
         style="fill:none;stroke:context-stroke;stroke-width:1;stroke-linecap:butt"
         d="M 3,-3 0,0 3,3"
         transform="rotate(180,0.125,0)"
         sodipodi:nodetypes="ccc"
         id="path1" />
    </marker>
    <inkscape:path-effect
       effect="bspline"
       id="path-effect3"
       is_visible="true"
       lpeversion="1.3"
       weight="33.333333"
       steps="2"
       helper_size="0"
       apply_no_weight="true"
       apply_with_weight="true"
       only_selected="false"
       uniform="false" />
    <rect
       x="66.799362"
       y="174.2592"
       width="193.13728"
       height="41.386559"
       id="rect1" />
    <rect
       x="66.799362"
       y="174.2592"
       width="193.13728"
       height="41.386559"
       id="rect1-5" />
    <rect
       x="66.799362"
       y="174.2592"
       width="193.13728"
       height="41.386559"
       id="rect1-5-5" />
    <marker
       style="overflow:visible"
       id="ArrowWide-2"
       refX="0"
       refY="0"
       orient="auto-start-reverse"
       inkscape:stockid="Wide arrow"
       markerWidth="1"
       markerHeight="1"
       viewBox="0 0 1 1"
       inkscape:isstock="true"
       inkscape:collect="always"
       preserveAspectRatio="xMidYMid">
      <path
         style="fill:none;stroke:context-stroke;stroke-width:1;stroke-linecap:butt"
         d="M 3,-3 0,0 3,3"
         transform="rotate(180,0.125,0)"
         sodipodi:nodetypes="ccc"
         id="path1-2" />
    </marker>
    <inkscape:path-effect
       effect="bspline"
       id="path-effect3-1"
       is_visible="true"
       lpeversion="1.3"
       weight="33.333333"
       steps="2"
       helper_size="0"
       apply_no_weight="true"
       apply_with_weight="true"
       only_selected="false"
       uniform="false" />
  </defs>
  <rect
     style="fill:#e6e6e6;fill-opacity:1;stroke:none;stroke-width:0.499999;stroke-miterlimit:3.5;stroke-dasharray:none"
     id="rect3"
     width="73.961838"
     height="81.838295"
     x="7.3001289"
     y="24.3978"
     transform="translate(-7.0501293,-24.147801)" />
  <g
     inkscape:label="Layer 1"
     inkscape:groupmode="layer"
     id="layer1"
     transform="translate(-7.0501294,-24.147801)">
    <text
       xml:space="preserve"
       transform="matrix(0.26458333,0,0,0.26458333,-0.73547404,-11.811855)"
       id="text1"
       style="font-size:16px;font-family:nunito;-inkscape-font-specification:nunito;text-align:center;writing-mode:lr-tb;direction:ltr;white-space:pre;shape-inside:url(#rect1);fill:#000000;stroke:#000000;stroke-width:0;stroke-miterlimit:3.5;stroke-dasharray:none"><tspan
         x="70.104126"
         y="188.119"
         id="tspan2">Create system of particles </tspan><tspan
         x="73.232147"
         y="208.119"
         id="tspan3">under the force of gravity</tspan></text>
    <text
       xml:space="preserve"
       transform="matrix(0.26458333,0,0,0.26458333,0.69359949,13.83096)"
       id="text1-7"
       style="font-size:16px;font-family:nunito;-inkscape-font-specification:nunito;text-align:center;writing-mode:lr-tb;direction:ltr;white-space:pre;shape-inside:url(#rect1-5);fill:#000000;stroke:#000000;stroke-width:0;stroke-miterlimit:3.5;stroke-dasharray:none"><tspan
         x="84.496109"
         y="188.119"
         id="tspan4">Update positions with </tspan><tspan
         x="100.89613"
         y="208.119"
         id="tspan5">Verlet integration</tspan></text>
    <rect
       style="fill:none;stroke:#000080;stroke-width:0.5;stroke-miterlimit:3.5;stroke-dasharray:none"
       id="rect2"
       width="52.638"
       height="13.831823"
       x="16.554306"
       y="32.565247" />
    <rect
       style="fill:none;stroke:#000080;stroke-width:0.5;stroke-miterlimit:3.5;stroke-dasharray:none"
       id="rect2-8"
       width="52.638"
       height="13.831823"
       x="16.673883"
       y="57.905624" />
    <text
       xml:space="preserve"
       transform="matrix(0.26458333,0,0,0.26458333,-0.09472662,38.959319)"
       id="text1-7-6"
       style="font-size:16px;font-family:nunito;-inkscape-font-specification:nunito;text-align:center;writing-mode:lr-tb;direction:ltr;white-space:pre;shape-inside:url(#rect1-5-5);fill:#000000;stroke:#000000;stroke-width:0;stroke-miterlimit:3.5;stroke-dasharray:none"><tspan
         x="75.184128"
         y="188.119"
         id="tspan6">Bound particles with the </tspan><tspan
         x="101.20815"
         y="208.119"
         id="tspan7">Jakobsen method</tspan></text>
    <rect
       style="fill:none;stroke:#000080;stroke-width:0.5;stroke-miterlimit:3.5;stroke-dasharray:none"
       id="rect2-8-4"
       width="52.638"
       height="13.831823"
       x="17.23032"
       y="82.841881" />
    <path
       style="fill:none;stroke:#000080;stroke-width:0.5;stroke-miterlimit:3.5;stroke-dasharray:none;marker-end:url(#ArrowWide)"
       d="m 40.727037,46.874514 c 0,3.714102 0,7.428201 0,11.142303"
       id="path3"
       inkscape:path-effect="#path-effect3"
       inkscape:original-d="m 40.727037,46.874514 c 0,3.714102 0,7.428201 0,11.142303"
       transform="matrix(1,0,0,0.91734315,1.728978,3.6823908)" />
    <path
       style="fill:none;stroke:#000080;stroke-width:0.5;stroke-miterlimit:3.5;stroke-dasharray:none;marker-end:url(#ArrowWide-2)"
       d="m 40.727037,46.874514 c 0,3.714102 0,7.428201 0,11.142303"
       id="path3-5"
       inkscape:path-effect="#path-effect3-1"
       inkscape:original-d="m 40.727037,46.874514 c 0,3.714102 0,7.428201 0,11.142303"
       transform="matrix(1,0,0,0.91734315,1.9601547,28.54425)" />
  </g>
</svg>


## Folder Structure

```text
Rope_simulation
├── dependencies/          # Third-party libraries (GLFW, GLAD, GLM, KHR)
├── src/
│   ├── physics/           # Rope physics and numerical integration
│   │   ├── constraints_JakobsenMethod.*
│   │   ├── systemDynamics.*
│   │   └── updatePositions_verletIntegration.*
│   │
│   ├── shaders/           # GLSL shader programs
│   │
│   ├── rendering.*        # Rendering pipeline and OpenGL drawing
│   ├── libraries.h        # External library includes
│   ├── glad.c             # OpenGL loader source
│   └── main.cpp           # Application entry point
│
├── CMakeLists.txt         # Build configuration
└── README.md
```

### Description

- **dependencies/** – Contains all third-party libraries required to build the project. No additional downloads are needed.

- **physics/** – Implements the rope simulation using Verlet integration and Jakobsen's constraint relaxation method.

- **shaders/** – GLSL vertex and fragment shaders used for rendering.

- **rendering.cpp / rendering.h** – Handles OpenGL rendering, drawing routines, and visualization.

- **main.cpp** – Initializes the application, creates the simulation, and manages the main loop.

- **CMakeLists.txt** – Defines the build configuration using CMake.

## Future work

## Building Instructions

#### Windows building
All relevant libraries are found in /dependencies. It is necessary to download and configure CMake
(https://cmake.org/download/). Run CMake script and generate project of choice.

#### Linux/WSL building
It is necessary to have CMake, Git and the required packages: Using root (sudo) and type ```apt-get install libsoil-dev
libglm-dev libglew-dev libglfw3-dev```

#### Build through CMake command line:
```
cd /path/to/Rope_simulation
mkdir build && cd build
cmake ..
make
```
## References
1. R. Badea, *[Owlree—Simulating a Rope (Games Series)](https://owlree.blog/posts/simulating-a-rope.html)*. Accessed: Apr. 4, 2024.
