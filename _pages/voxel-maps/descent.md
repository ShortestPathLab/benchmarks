---
date: 2023
layout: syllabus
title: Descent Benchmarks
permalink: /3d-benchmarks/voxel-maps/descent/
---

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
---|---|---|---|---
 30 | 2,000 | 60,000 | 478M | 10M
 
</div>

<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/voxel-maps/descent/'><button class='button benchmarks'>Get the Benchmarks!</button></a>

This benchmark is derived from in-game levels from Descent, a video game developed by Parallax Software and released by Interplay Productions in 1995. It is recognised as the earliest FPS to feature entirely true-3D graphics, and is now open source. Descent is well-suited for search as each level has been designed specifically for 3D maneuverability and traversal; featuring rooms and branching corridors.

We adapt the 27 in-game levels and 3 secret levels into 30 voxel maps (one for each level) with 2,000 instances each, for a total of 60,000 problem instances. A *voxel* is a unit size volume element, essentially the 3D equivalent to a unit cell in a 2D grid. *Voxel* gridmaps have nice properties and high solution quality (i.e. small detours from the true path distance).

Problem instances are generated solely from the internal traversable region which corresponds to the in-game playable area. The interior region of the original level remains one contiguous, enclosed region, and accounts only for a small proportion of the total size of the map.

We use advanced methods of problem generation to select only a small, but comprehensive set of problems from across the entire distribution fo difficulty. We present each of these problem instances along with useful metrics in an informed order of increasing difficulty, allowing users to quickly identify performance indicators and to reach more nuanced conclusions.

For more information, and if you are using these benchmark problems, please cite the following paper to reference the benchmark sets:

@article{nobes2023voxels,  
    title={Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants},  
    author={Thomas K. Nobes and Daniel D. Harabor and Michael Wybrow and Stuart D.C. Walsh},  
    journal={The 16th International Symposium on Combinatorial Search (SoCS)},  
    volume={16}, number={1}, pages={}, year={2023},  
    url = {https://ojs.aaai.org/index.php/SOCS/article/view/27283 }  
}