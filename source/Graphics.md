# Graphics

## Graphics Concepts

### References
- Tomas Akenine-Möller, Eric Haines, Naty Hoffman. "Real Time Rendering" (website and book) [realtimerendering.com](http://www.realtimerendering.com/).

#### Instanced Rendering
https://www.opengl.org/wiki/Vertex_Rendering#Instancing
http://ogldev.atspace.co.uk/www/tutorial33/tutorial33.html 
http://learnopengl.com/#!Advanced-OpenGL/Instancing

#### Texel
https://en.wikipedia.org/wiki/Texel_\(graphics\)

#### Tessellation
https://www.opengl.org/wiki/Tessellation

#### Surface and Swapchain
https://msdn.microsoft.com/en-us/library/windows/desktop/bb219683\(v=vs.85\).aspx

#### Uniform Buffer
http://www.geeks3d.com/20140704/gpu-buffers-introduction-to-opengl-3-1-uniform-buffers-objects/

#### GPU Pipeline
- A trip through the Graphics Pipeline 2011: 
  https://fgiesen.wordpress.com/2011/07/09/a-trip-through-the-graphics-pipeline-2011-index/
- Render Hell 2.0: 
  https://simonschreibt.de/gat/renderhell/
- Life of a triangle - NVIDIA's logical pipeline
  http://pixeljetstream.blogspot.kr/2015/02/life-of-triangle-nvidias-logical.html

Graphics API
------------
### Khronos Vulkan
#### Training
https://www.youtube.com/watch?v=EX1RKhlOYmY

#### References
- [A Brief Overview Of Vulkan API](http://www.toptal.com/api-developers/a-brief-overview-of-vulkan-api) 
- [Vulkan Programming Resources List @ Geeks3D](http://www.geeks3d.com/20160205/vulkan-programming-resources-list/)
- https://github.com/jcoder58/VulkanResources

#### Game Engines Using Vulkan
1. libretro/RetroArch
2. OpenTK (planned)

#### Topics
- [Vulkan Shader Resource Binding](https://developer.nvidia.com/vulkan-shader-resource-binding)

### Khronos OpenGL/ES/WebGL
#### OpenGL API Reference
- Jorge Rodríguez' OpenGL API Documentation [docs.GL](http://docs.gl/)
- https://www.opengl.org/sdk/docs/man4/

#### OpenGL Tutorials
- LearnOpenGL.com
- [Anton's OpenGL 4 Tutorials](http://antongerdelan.net/opengl/)

#### Open Source Implementation
- Mesa
- [Google Ion](https://github.com/google/ion)

### Microsoft DirectX 11/12
[Programming Guide](https://msdn.microsoft.com/en-us//library/windows/desktop/dn899121\(v=vs.85\).aspx)

### Apple Metal/SceneKit/SpriteKit
[Programming Guide](https://developer.apple.com/library/ios/documentation/Miscellaneous/Conceptual/MetalProgrammingGuide/Introduction/Introduction.html)

API Comparison
--------------

|          | Mantle | Vulkan | DirectX 12 | Metal |
|----------|--------|--------|------------|-------|
| Command  | cmd buf & queque | cmd buf & queque | cmd lists | cmd buf & queque |
| Resource Types | Image, Memory, View, Sampler | Buffer, Image, View, Sampler  |  Texture, Buffer, View, Sampler | MTLBuffer & MTLTexture |
| Shader Binding | Descriptor set, Dynamic memory view | Descriptor set | Descriptor table | ? |
| Memory   | GPU Memory heap, mem object | | | | 
| Rendering | | | | |
| Compute  | | | | |

Graphics SDKs and Tools
-----------------------
### Imagination PowerVR
  - [PowerVR SDK & Framework](https://community.imgtec.com/developers/powervr/)
    * Open Source [GitHub Repositories](https://github.com/powervr-graphics)

### Qualcomm Adreno

### ARM Mali

### Nvidia GameWorks

### AMD ?

### Debugging Tools
- [RenderDoc](https://github.com/baldurk/renderdoc)
