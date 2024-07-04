# Volcano 3d rendering system
## Texture Mapping Unit
Texture Mapping is a way of adding realism to a 3D model by defining high-frequency detail, surface texture, or color information on the model. In this process, a 2D surface, also called a "Texture Map", is wrapped around a 3D model. This process is also called as diffuse mapping.

![Overview of texture mapping process](img/texture_mapping.jpg)

### The Basics of Texture Mapping
The idea is simple enough. Let's say you have a model of a house. What if it had window "panes" that were transparent, so you could see what's inside? 

Texture mapping is what achieves the kind of realistic quality required. Instead of just being plain white, the windows could be transparent with a glass-like texture. That way, what's inside the room can be seen through the window instead of what looks like nothing at all.

Texture mapping technique is not only useful for 3D modeling, but for 3D rendering as well:
- Textures can provide information on how 3D objects should look, how light reflects off of them, and how they should appear under certain conditions. This texture map data can be used on any 3D object, including people, buildings, landscapes, or anything that normally has a surface.
- Textures can also be added or subtracted to provide more detail or hide features you don't want the public to see.
- Textures can help 3D models look more 3D and less 2D.

### Texture Compression
Texture compression has been proposed to reduce memory bandwidth. The basic idea
is to use compression on the texture images. The aim is to save memory bandwidth
without degrading the generated image quality too much. 
There are a few requirements for efficient texture compression in mobile devices.
A fixed compression rate is required for straightforward address computations, and the
number of indirect look-ups for the compression should be limited. Then, decompression should be fast and easytoimplementin hardwareto keepthe pipelinelatency short.

#### ETC1 Compressed Texture Image Formats
The compression technique used in this project is called Ericsson Texture Comperssion. The texture is described as a number of 4×4 pixel blocks. If the texture (or a particular mip-level) is smaller than 4 pixels in any dimension (such as a 2×2 or a 8×1 texture), the texture is found in the upper left part of the block(s), and the rest of the pixels are not used. For instance, a texture of size 4×2 will be placed in the upper half of a 4×4 block, and the lower half of the pixels in the block will not be accessed.


