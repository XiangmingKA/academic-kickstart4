+++
# Date this page was created.
date = 2018-11-10T00:00:00
layout = "project"

# Project title.
title = "Fabric Shading in Unity URP Shader Graph"

# Project summary to display on homepage.
summary = """
A comprehensive Shader-Graph-based fabric shading solution, extremely artist-friendly.<br>
I built the Master Node that implemented fabric BRDFs, anisotropy specular, and translucency, etc.. And I was responsible to build the Shader Graph nodes to support artists' work. I was responsible for the C# and HLSL coding, BRDFs research, Shader Graph nodes creation, and Demo creation using Substance Designer. 
 """
 
image_preview = "img/overview.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["Computer Graphics", "Rendering"]`
tags = ["Computer Graphics","Rendering"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# [header]
# image = "img/overview.png"

+++

# Overview
To give artists the flexibility to create various types of fiber while using different pipeline standards, we created this Shader-Graph-based fabric shading solution. While shading fibers in a physically based manner, we guaranteed that artists can use shader graphs to process their inputs. For instance, artists can choose the sources as the normal input--from normal maps, thread maps, or detail maps. We created the master node with two types of BRDF for silk-like and cotton-like fibers. Also, we implemented the commonly used features for fabric shading--translucency, anisotropic specular, and an extended two-sided rendering option. 

## Material Samples
![Cotton, Wool, Denim material samples](img/fabric_sample1.png)
![Linen and Velvet material samples](img/fabric_sample2.png)
![Silk, Shot Silk, Nylon material samples](img/fabric_sample3.png)

# Features
## Shader Graph Master Node
We extended the Shader Graph material type in URP. Added the "Fabric" option in the Graph Inspector, users can convert their Lit shader to our Fabric shader. 
![Material type option for Fabric](img/fabric_inspector.png)

To better mimic the surface feature of fiber, we implemented two types of BRDF--"Cotton: for rough fibers and "Silk" for smooth fibers in general. 

![Fabirc type options in Graph Inspector](img/fabric_type.png)

Two-sided rendering options were extended to support flipped-normal and mirrored-normal.
![Two-sided rendering options in Graph Inspector](img/fabric_twosided.png)


