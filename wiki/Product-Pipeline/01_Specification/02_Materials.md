---
layout: default
nav_order: 2
has_children: false
permalink: /wiki/Product-Specification/Materials/
parent: Product Specification
grand_parent: Product Pipeline 
title: Materials




---




# Materials
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

<br>

> This section is closely related to "Textures". Information presented here may be relevant to both sections.
{: .note }

---

## Object structure
[custom callout colors]( /wiki/Product-Specification/Geometry/#geometry)
### 3DS Max

### Maya

### Blender

---

## Material Structure

<br>

All assets must have a maximum of two materials, for the two rendering types `opaque` and `transparent`.

> Where appropriate, transparent materials should be used on different objects from opaque (into as few objects as necessary to avoid artefacting), as the shader in-engine renders with `alpha blend` transparency. <br><br> Problems can occur if a transparent material is applied to a larger object where there is more complex intersecting geometry. This can result in artefacts where parts of the mesh render in the wrong order. Splitting the mesh into more objects can help, as the objects pivot should be sufficiently different for the engine to sort the rendering correctly.  
{: .note }

### 3DS Max

### Maya

### Blender

---

## Material Naming Convention

> All materials should start with the naming prefix "**m_**", followed by the products `UPC`. 
<br><br>
Products with transparency requires a total of two materials, where the second transparent material is named "m_UPC" followed by the suffix **"_t"**. 



| Type | Material Naming Example                    |
|:---|:-----------------------------|
|Opaque|**m_**888750194923   |
|Transparent|**m_**888750194923**_t** |



> Transparent materials always need an [**Alpha**]( /wiki/Product-Specification/Textures/#alpha) and [**Transmission map**]( /wiki/Product-Specification/Textures/#transmission), as well as the standard [**Diffuse**]( /wiki/Product-Specification/Textures/#diffuse) for opaque materials. 
{: .note }
 


---

## Material Type

<br>

---

### Standard

asdasd

---

### Transparent


