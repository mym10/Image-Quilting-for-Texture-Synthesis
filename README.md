# Image Quilting for Texture Synthesis

## Introduction
Texture synthesis is the process of generating a larger image or texture based on a given smaller example, such that the new texture maintains the visual and structural properties of the original. The goal is to create a seamless and plausible expansion of the original sample.

Image quilting is a specific algorithm or method used for texture synthesis. It works by stitching together small patches of texture from the input image to create a larger output texture. The patches are carefully aligned to ensure smooth transitions between adjacent patches, minimizing visible seams.

---

## Overview
This code implements a texture synthesis technique using patch-based quilting based on the paper “Image Quilting for Texture Synthesis and Transfer” by Efros & Freeman. It allows the generation of larger textures or filling regions using small input texture patches. The synthesis can use:

1. **Random patch placement**
2. **Error minimization (overlap boundaries)**
3. **Optimal patch blending via min-cut paths**

---

## Evaluation of Different Algorithms

### Evaluation Metrics
**Overlap Error**
- **Description**: Quantifies the error in overlapping regions between patches.
- **Metric**: Computes the mean squared error (MSE) or sum of squared differences (SSD) in the overlap areas.

### Evaluation Table
| Method           | Key Idea                               | Speed      | Seam Quality | Complex Texture Handling |
|------------------|----------------------------------------|------------|--------------|--------------------------|
| Efros & Leung    | Pixel-by-pixel synthesis               | Slow       | Moderate     | Good                     |
| Efros & Freeman  | Patch-based quilting with boundary cuts| Moderate   | Good         | Moderate                 |
| Wei & Levoy      | Random patch-based synthesis           | Fast       | Moderate     | Moderate                 |
| Kwatra et al.    | Patch synthesis with graph cuts        | Slow       | Excellent    | Good                     |
| Liu & Lin        | Pyramid-based optimization             | Very slow  | Excellent    | Excellent                |

---

## References
1. [Efros & Freeman](https://people.eecs.berkeley.edu/~efros/research/quilting/quilting.pdf)
2. [Liu & Lin](https://www.cs.cmu.edu/~wclin/texture/texture03.pdf)

