# Overview
Slang by the [Khronos Group](https://www.khronos.org/) streamlines shader compilation on different platform. Removing the requirement of a custom streamlined shader language for your game engine to likes of Unity, Unreal and Godot.

## Common features
- CLI for developer/engine-side integration - no performance hit on the end product.
- Compute shading
- Ray tracing core utilization
- Allow for modularization with "modules", similar to how `#include` works in GLSL.
- Already existing features like structs, macros and (un)scoped enums.

## Speed
Efficient and with fast compile times using features like precompilation using intermidiates (~30% speed up agains monolightic) <span style="font-size: 0.8em; color: gray;">According to this [video-presentation](https://www.youtube.com/watch?v=FCu8BiidI24) by Hai Nguyen from NVIDIA</span>

## Compatibility
It's backwards compatible with most shading languages (GLSL, HLSL, and more).
For that you use `-lang glsl` or `-lang hlsl`.

## Adoption
- Seamlesly supports Vulkan, OpenGL/ES, DX3D, Metal (beta), CUDA, CPU, PyTorch and WebGPU coming soon.
- Syntax is **very** similar to HLSL.

## Innovation
Function decorators that are used to specify entrypoints for different shaders (replaces `shader.vs`, `shader.fs`, `shader.gs`, `shader.compute`, etc.)
![alt text](entrypoints.png)
<span style="font-size: 0.8em; color: gray;">Source: "Slang in Vulkan" by The Khronos Group on [YouTube](https://youtu.be/FCu8BiidI24?si=ueXOJWalgvDG8Bn2&t=943).</span>

## Useful links
- [Slang website](https://shader-slang.com/)
- [Slang playground](https://shader-slang.com/slang-playground/)
- [Slang compiler by Khronos Group on GitHub](https://github.com/shader-slang/slang)
- [Official Press Release by Khronos Group](https://www.khronos.org/news/press/khronos-group-launches-slang-initiative-hosting-open-source-compiler-contributed-by-nvidia)

## Videos
"Slang in Vulkan" by The Khronos Group on YouTube.
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/FCu8BiidI24?si=arbEH5PzjKYtPqXw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
