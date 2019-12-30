+++
# Date this page was created.
date = 2018-11-10T00:00:00
layout = "project"

# Project title.
title = "A Unity3D Billiards Game"

# Project summary to display on homepage.
summary = """
 This is the curriculum project at UESTC.<br>
 I'm responsible for all the code and game design
 """
 
image_preview = "img/Scene-Test5.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["Game Development", "Unity3D"]`
tags = ["Game Development","Unity3D"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# [header]
# image = "img/Scene-Test5.jpg"

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

![Test Scene 1](img/Scene2-Test5.jpg)
![Test Scene 2](img/Scene-Test3.jpg)
![Test Scene 3](img/DepthOfField.jpg)



