# Parametric Stereo for Multi-Pose Face Recognition and 3D-Face Modeling

## Information

- [Sauce](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.226.4819&rep=rep1&type=pdf)

## Authors

- Rik Fransens,
- Christoph Strecha,
- Luc Van Gool

- PSI ESAT-KUL
- Leuven, Belgium

## Abstract

- **Face modeling and recognition** from a pair of calibrated **stereo cameras**

# Introduction

## Zhao et al Taxonomy [16]

### Face recognition from still images

1. Holistic matching methods
2. Feature based or structural matching methods
3. Hybrid of the above two

## Holistic matching

- Input = Visual content of the **complete face** region
- Extracts a **low-dimensional feature vector** and compares it to stored examples.

### Examples

- PCA-based **Eigenfaces** technique [14,11].
- **Fisherfaces** [2].
- **ICA**-based representations [1].

## Feature or structural matching

- The **position and appearance of local features** like eyes, nose, etc. are determined
- feature vector is built from above descriptors

### Example

- Elastic Bunch Graph Matching system [15] - uses **wavelet jets** to encode local appearance

## Hybrid

- Use both local and global descriptors

### Examples

- Modular **Eigenfaces** approach [12]
- Flexible Appearance Model [10] which uses an ASM-model [8] to encode shape, and PCA to encode image intensities.

## Major challenge

Creating a system that is **invariant** to **Illumination** & **Pose**

### Illumination invariant

- Approaches are based on Illumination Cone

### Pose invariant

- Most principled approaches makes use of 3D morphable face models

## Multi-camera approach

- Addresses the problems of illumination and pose variation.
- **2 calibrated cameras** used, algorithm computes a **3D-shape and texture** representation of the face
- These representations are parametrized by the **linear shape and texture coefficients** of a 3D-morphable face model

## 3D shape of face

- Rather then computing dense depth map, and then approximating the face related part
- We **directly fit** morphable 3D model to the set of stereo-images, hence the name parametric stereo
- This greatly reduces the degrees of freedom (DOFs) in the depth-from-stereo problem from 1 DOF per pixel to no. of shape parameters of the 3D-model + 6 (DOF of global R & T)
- Next, the **texture from both images** are mapped onto the vertices of the 3D-model
- This shape and pose free texture is described in terms of the **linear texture model** of the 3D-morphable model
- [Blanz and Vetter, 3D face model from single image](https://www.youtube.com/watch?v=nice6NYb_WA)
