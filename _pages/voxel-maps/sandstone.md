---
date: 2023
layout: syllabus
title: Sandstone Benchmarks
permalink: /3d-benchmarks/voxel-maps/sandstone
---

<<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
--|---|---|---|----
 11 | 2,000 | 22,000 | 64M | 13M
</div>

<br>
This benchmark is derived from X-ray tomographic computed images (XRCT) of natural sandstone samples. The samples include Bandera Gray, Parker, Kirby, Bandera Brown, Berea, Berea Sister Gray (BSG), Berea Upper Gray (BUG), Castlegate, Buff Berea (BB), Leopard and Bentheimer sandstones.

We use binary images of the connected pore space, treating the sandstone itself as an obstacle, and the permeable pore space as traversable terrain. Traversable voxels compose a single connected region, assuming a 6-connected neighbourhood. A *voxel* is a unit size volume element, essentially the 3D equivalent to a unit cell in a 2D grid. *Voxel* gridmaps have nice properties and high solution quality (i.e. small detours from the true path distance).

We define 11 maps with 2,000 pathfinding instances each, for a total of 22,000 problems. The pore-space geometry is characterised by winding narrow corridors and natural nonsymmetric shapes resulting in an environment reminiscent of random grid maps.

We use advanced methods of problem generation to select only a small, but comprehensive set of problems from across the entire distribution fo difficulty. We present each of these problem instances along with useful metrics in an informed order of increasing difficulty, allowing users to quickly identify performance indicators and to reach more nuanced conclusions.

For more information, and if you are using these benchmark problems, please cite the following paper to reference the benchmark sets:

@article{nobes2023voxels, title={Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants}, author={Thomas K. Nobes and Daniel D. Harabor and Michael Wybrow and Stuart D.C. Walsh}, journal={The 16th International Symposium on Combinatorial Search (SoCS)}, volume={16}, number={1}, pages={}, year={2023}, url = {https://ojs.aaai.org/index.php/SOCS/article/view/27283 } }
