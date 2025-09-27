# Idea

Sub-surface scattering (SSS) is a key component in creating realistic materials like skin, wax, and other translucent objects.

<div style="display: flex; justify-content: center; align-items: center">
    <img src="local://preview_16fps.gif" style="margin: 2vw; max-width: 256px; width: 100%">
    <img src="local://screenshot_1.png" style="margin: 2vh; max-width: 256px; width: 100%">
</div>

## The problem

However, achieving this effect in real-time environments presents unique challenges. This article explores a novel approximation of sub-surface scattering designed specifically for real-time applications.

## Solution

The technique relies on transmission maps paired with a heavily modified implementation of the diffuse component of the classic Phong shading model. This approach effectively simulates the way light scatters beneath the surface of translucent materials while maintaining high performance, making it ideal for applications requiring real-time rendering, expensive and expansive scenes with many fragments taken up by foliage, realistic shading of in-game faces, etc.

## Key features

- **Real-time Capabilities:** This technique is optimized for real-time rendering, ensuring smooth performance even in resource-constrained environments.

- **Versatile Implementation:** A non-demanding implementation that boils down to a modification in the light processor of your engine's shader pipeline. (Specific to Godot Engine) Designed to work seamlessly with multiple rendering pipelines, including Forward+, Mobile, and Compatibility modes.

- **Minimal Overhead:** The approximation strikes a balance between visual fidelity and computational efficiency.

## Application
This solution may be of particular value to projects on such platforms or with such features:
- **Foliage & Skin:** Realistic and fast rendering of organic materials like skin or leaves for real-time environments.
- **VR/AR:** Given the incredible resolution that VR is rendered at makes it very important to optimize your fragment shaders as much as possible.
- **Mobile:** Tailored for compatibility with performance-sensitive platforms.

## Adoption

(Blender) Here is an example node layout of what a baking setup for a transmission-map may look like:

<img class="responsive-image" src="local://screenshot_0.png">

Here is the end result and what you should aim for if you have a different workflow.

<img class="responsive-image" src="local://sss_map_view.png">

## Example

An example implementation (Godot) in a shading language similar to GLSL is available [here](https://godotshaders.com/shader/performant-sss-sub-surface-scattering-approximation/).

## Useful links
- [Example implementation in Godot](https://godotshaders.com/shader/performant-sss-sub-surface-scattering-approximation/)
- [An Introduction To Real-Time Subsurface Scattering](https://therealmjp.github.io/posts/sss-intro/)