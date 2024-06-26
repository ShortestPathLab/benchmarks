---
date: 2023
layout: syllabus
title: Industrial Plant Benchmarks
permalink: /3d-benchmarks/voxel-maps/industrial-plants/
---

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
---|---|---|---|---
 5 | 2,000 | 10,000 | 227M | 208M
 
</div>

<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/voxel-maps/industrial-plants/'><button class='button benchmarks'>Get the Benchmarks!</button></a>

This benchmark is designed to mimic industrial plant design and pipe routing problems. Using real data from chemical processing plants, we construct voxel maps that feature layouts composed of many types and scales of equipment modules, safety and engineering zones, support units, and more. We construct geometry at 10cm resolution which produces map sizes of hundreds of millions of voxels. A *voxel* is a unit size volume element, essentially the 3D equivalent to a unit cell in a 2D grid. *Voxel* gridmaps have nice properties and high solution quality (i.e. small detours from the true path distance).

The benchmark consists of five unique plant layouts with 2,000 routing problems each for a total of 10,000 problem instances. Instances are generated by choosing at random start and target locations from among those voxels immediately adjacent to the surfaces of equipment modules. This simulates routing pipes between two fixed attachment points on corresponding modules. To better match the problems to valid routing scenarios, we exclude several areas such as safety or truck access zones, interiors of racks, and many miscellaneous equipment parts such as equipment skirts (lower supports for large vessels) from potential start/target points.

We use advanced methods of problem generation to select only a small, but comprehensive set of problems from across the entire distribution fo difficulty. We present each of these problem instances along with useful metrics in an informed order of increasing difficulty, allowing users to quickly identify performance indicators and to reach more nuanced conclusions.

For more information, and if you are using these benchmark problems, please cite the following paper to reference the benchmark sets:

@article{nobes2023voxels,  
    title={Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants},  
    author={Thomas K. Nobes and Daniel D. Harabor and Michael Wybrow and Stuart D.C. Walsh},  
    journal={The 16th International Symposium on Combinatorial Search (SoCS)},  
    volume={16}, number={1}, pages={}, year={2023},  
    url = {https://ojs.aaai.org/index.php/SOCS/article/view/27283 }  
}