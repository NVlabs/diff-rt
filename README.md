<!-- SPDX-FileCopyrightText: Copyright (c) 2023 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
SPDX-License-Identifier: LicenseRef-NvidiaProprietary

NVIDIA CORPORATION, its affiliates and licensors retain all intellectual
property and proprietary rights in and to this material, related
documentation and any modifications thereto. Any use, reproduction,
disclosure or distribution of this material and related documentation
without an express license agreement from NVIDIA CORPORATION or
its affiliates is strictly prohibited. -->

# Sionna RT: Differentiable Ray Tracing for Radio Propagation Modeling

This repository contains code to reproduce some of the results from the paper [Sionna RT: Differentiable Ray Tracing for Radio Propagation Modeling [A]](https://drive.google.com/file/d/1fTbTC6ogj9p8lPevvrFUu8tyOhsNArJm/view?usp=share_link) using the [Sionna&trade; link-level simulator [B]](https://nvlabs.github.io/sionna/).

## Abstract
Sionna&trade; is a GPU-accelerated open-source library for link-level simulations based on TensorFlow. Its latest release (v0.14) integrates a differentiable ray tracer (RT) for the simulation of radio wave propagation. This unique feature allows for the computation of gradients of the channel impulse response (or related quantities) with respect to many system  and environment parameters, such as material properties, antenna patterns, array geometries, as well as transmitter and receiver orientations and positions. In this paper, we outline the key components of Sionna RT and showcase several use-cases such as learning of radio materials and optimizing transmitter orientations through gradient descent. While ray tracing is a crucial tool for 6G research on topics like reconfigurable intelligent surfaces, integrated sensing and communications, as well as user localization, we believe that differentiable ray tracing is a key enabler for many novel and exciting research directions such as digital twins.

## Setup
Running this code requires [Sionna 0.14](https://nvlabs.github.io/sionna/) or later.
To run the notebooks on your machine, you also need [Jupyter](https://jupyter.org).
We recommend Ubuntu 20.04, Python 3.8, and TensorFlow 2.11.

## Structure of this repository

The repository contains the following notebooks:

* [Learning_Materials.ipynb](Learning_Materials.ipynb) : Demonstrates how electro-magnetic properties of objects in a scene can be learned by gradient descent.

* [Learning_Orientation.ipynb](Learning_Orientation.ipynb) : Demonstrates how the orientation of a transmitter can be optimized by gradient descent.

## References

[A] [J. Hoydis, F. Ait Aoudia, S. Cammerer, M. Nimier-David, N. Binder, G. Marcus, A. Keller, "Sionna RT: Differentiable Ray Tracing for Radio Propagation Modeling", Mar. 2023.](https://drive.google.com/file/d/1fTbTC6ogj9p8lPevvrFUu8tyOhsNArJm/view?usp=share_link)

[B] [J. Hoydis, S. Cammerer, F. Ait Aoudia, A. Vem, N. Binder, G. Marcus, A. Keller, "Sionna: An Open-Source Library for Next-Generation Physical Layer Research", Mar. 2022.](https://arxiv.org/abs/2203.11854)

## License and Citation

Copyright &copy; 2023, NVIDIA Corporation. All rights reserved.

This work is made available under the [NVIDIA License](LICENSE.txt).

If you use this software, please cite it as:
```bibtex
@article{sionna-rt,
    title = {{Sionna RT: Differentiable Ray Tracing for Radio Propagation Modeling}},
    author = {Hoydis, Jakob and {Ait Aoudia}, Fayçal and Cammerer, Sebastian and Nimier-David, Merlin and Binder, Nikolaus and Marcus, Guillermo and Keller, Alexander},
    year = {2023},
    month = MAR,
    journal = {arXiv preprint},
    online = {https://drive.google.com/file/d/1fTbTC6ogj9p8lPevvrFUu8tyOhsNArJm/view?usp=share_link}
}
```
