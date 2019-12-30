+++
# Date this page was created.
date = 2018-11-10T00:00:00
layout = "project"

# Project title.
title = "A Path Tracer"

# Project summary to display on homepage.
summary = """
 This is the curriculum project for CS285 Advanced Image Synthesis at UCSB.<br>
 I'm responsible for all the code and pipeline design
 """
 
image_preview = "img/Scene-Test5.ppm"

# Tags: can be used for filtering projects.
# Example: `tags = ["Computer Graphics", "Rendering"]`
tags = ["Computer Graphics","Rendering"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# [header]
# image = "featured.jpeg"

+++

# Overview
This is a Monte-Carlo rendering systems that supports global illumination, interpolating parameters, texture mapping, shaders, bounding volume hierarchy accelerating, and depth of field rendering<br>
I independently accomplish it under the guidance of Prof. Pradeep Sen <br>

The main workflow of the program is as follows: <br>
1. Implement a basic Whitted-style ray tracer. <br>
2. Improved it to support interpolating parameters, texture mapping, shaders.<br>
3. Accelerate the rendering of complex scene by optimize the sphere and triangle intersection routines and add acceleration data structures.
4. Improve it to support Monte-Carlo integration (pixel antialiasing by integrating with a box filter over the pixel footprint and depth of field by integrating over the aperture of the camera).
5. Add path tracing to support global illmination.

# Features
## Main Rendering Pipeline Design


# Test Scenes

![Test Scene 1](img/Scene2-Test5.ppm)
![Test Scene 2](img/Scene2-Test4.ppm)
![Test Scene 3](img/Scene-Test4.ppm)



