+++
# Date this page was created.
date = 2018-11-10T00:00:00
layout = "project"

# Project title.
title = "Advanced Character Rendering with Unity URP"

# Project summary to display on homepage.
summary = """
 Advanced character rendering subject at Unity Technologies, including Screen-Space Subsurface Scattering (5S), skin shading, and eye shading.<br>
 I'm fully responsible for the 5S render feature development, compute shader creation, physically-based skin shader and eye shader creation.
 """
 
image_preview = "img/overview.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["Computer Graphics", "Rendering"]`
tags = ["Computer Graphics","Rendering"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# [header]
# image = "img/Scene-Test5.jpg"

+++

# Overview
To achieve high fidelity character rendering, we implement multiple rendering techniques in Universal Render Pipeline, including a highly optimized screen-space subsurface scattering render feature, specialized PBR skin shader, and complicated eye shader that simulates refractions. All of these features are highly performance-optimized to support mobile and VR platforms.

<video src="./demo1.mp4" controls="controls" width="640" height="320" autoplay="autoplay">
Your browser does not support the video tag.
</video>

# Personal Contribution
## Screen-Space Subsurface Scattering

To render the subsurface scattering effect, I developed a Custom Render Feature to extend the Universal Render Pipeline. The specular and diffuse light contributions of the skin are stored separately in two textures and passed to the next render pass. A compute shader is implemented to calculate the final blurry scattered image using Burley’s normalized diffusion model.

We use the Diffusion Profile to control the subsurface scattering. I developed the supporting shader GUI and profile management system.

<video src="./demo2.mp4" controls="controls" width="640" height="320" autoplay="autoplay">
Your browser does not support the video tag.
</video>


## Physically Based Skin Shading

To shade the complicated skin structure, I implemented multiple shading features in the skin shader. Including using a specialized BRDF that has two specular lobes, detail maps that blends Albedo and Normal, color-bleeding AO, using powered AO as SO, etc.

<video src="./demo3.mp4" controls="controls" width="640" height="320" autoplay="autoplay">
Your browser does not support the video tag.
</video>

## Physically Based Eye Shading

In the eye shader, I implemented parallax mapping to simulate the refraction effect. AO and SO maps are supported to mimic the natural human structure. 

<video src="./demo4.mp4" controls="controls" width="640" height="320" autoplay="autoplay">
Your browser does not support the video tag.
</video>

