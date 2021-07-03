+++
# Date this page was created.
date = 2018-11-10T00:00:00
layout = "project"

# Project title.
title = "Course Project：A Path Tracing Render System"

# Project summary to display on homepage.
summary = """
 This is a curriculum project in CS285 Advanced Image Synthesis at UCSB.<br>
 I'm responsible for all the C++ code and pipeline design
 """
 
image_preview = "img/Scene-Test5.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["Computer Graphics", "Rendering"]`
tags = ["Computer Graphics","Rendering"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# [header]
# image = "img/Scene-Test5.jpg"

+++

# Overview
This is a Monte-Carlo rendering system that supports global illumination, interpolating parameters, texture mapping, bounding volume hierarchy accelerating, and depth of field effected rendering, etc..<br>
I independently accomplished it under the guidance of Prof. Pradeep Sen. <br>

The main workflow of the program is as follows: <br>
1. Implement a basic Whitted-style ray tracer. <br>
2. Improved it to support interpolating parameters, texture mapping, shaders.<br>
3. Accelerate the rendering of complex scenes by optimize the sphere and triangle intersection routines and add acceleration data structures.
4. Improve it to support Monte-Carlo integration (pixel antialiasing by integrating with a box filter over the pixel footprint and depth of field by integrating over the aperture of the camera).
5. Add path tracing to support global illumination.

# Features
## Ray Tracing

The first step of this system is to implement a basic Whitted-style ray tracer. Features like reflection, refraction, and shadowing are supported.
![Reflections & Shadows](img/Scene-Test5.jpg)
![Reflections & Refractions](img/Scene-Test2.jpg)

Then, I Improved it to support more shaders, such as texture mapping and interpolating parameters.
![Shaders](img/Shaders.jpg)

To render complex scenes, I added a heuristic bounding volume hierarchy (BVH) to store the primitives in an efficient manner. Also, I optimize the sphere and triangle intersection routines. In most scenes, the speed of rendering has been accelerated by more than 50x.
![Test Scene 1](img/BVH.jpg)
A complex scene rendered within 2 minutes:
![Test Scene 1](img/Scene2-Test5.jpg)

Now, it is the time to implement path tracing!

## Monte-Carlo integration & Path Tracing

To support pixel antialiasing, I implemented a box filter over the pixel footprint and depth of field by integrating over the aperture of the camera illustrated as follows:
![Antialiasing1](img/Antialiasing1.jpg)

As for the depth-of-field effect, I simulated an imaginary thin lens with a fixed aperture to produce a nice depth-of-field effect, where some objects will be sharp but others blurry.
![DepthOfField1](img/DepthOfField1.jpg)

Original scene:
![Test Scene 1](img/Scene2-Test4.jpg)

Depth-of-field effected scene:
![Test Scene 1](img/DepthOfField.jpg)

Now, here is the most important part! 
A basic Monte-Carlo estimater was implemented to sample radiance of the hemisphere.
![Test Scene 1](img/PathTracing.jpg)
By integrating the radiance coming from the hemisphere, we could estimate the radiance of indirect illumination. So far, we can get the global illuminated scenes as follows.
![Test Scene 1](img/PathTracing2.jpg)

## Final thesis

Also, I added a basic volumetic scattering effect estimater in this path tracer and wrote a final paper in SIGGRAPH tamplate which discussed principles of volumetic rendering and path tracing.

![Test Scene 1](img/Final1.jpg)
![Test Scene 1](img/Final2.jpg)
![Test Scene 1](img/Final3.jpg)
![Test Scene 1](img/Final4.jpg)
![Test Scene 1](img/Final5.jpg)

For more information and source code: https://github.com/XiangmingKA/PathTracer
![Test Scene 1](img/Scene-Test4.jpg)

