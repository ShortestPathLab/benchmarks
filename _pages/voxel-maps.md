---
date: 2023
layout: syllabus
title: Voxel Maps
permalink: /3d-benchmarks/voxel-maps
---

<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/descent/'><button class='button syllabus'>Descent</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/industrial-plants/'><button class='button syllabus'>Industrial Plants</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/sandstone/'><button class='button syllabus'>Sandstone</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/warframe/'><button class='button syllabus'>Warframe</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/descent/'><button class='button benchmarks'>Descent</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/industrial-plants/'><button class='button benchmarks'>Industrial Plants</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/sandstone/'><button class='button benchmarks'>Sandstone</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/3d-benchmarks/voxel-maps/warframe/'><button type='button' class='benchmarks'>Warframe</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<br>
Here you can find a series of currently available voxel-world benchmarks for 3D pathfinding. A *voxel* is a unit size volume element, essentially the 3D equivalent to a unit cell in a 2D grid. One of these data sets, the **Warframe** benchmarks, is developed by [MovingAI](https://movingai.com/) and was the first to appear in the literature. The other three voxel benchmarks were constructed as part of our own work in order to help bridge-the-gap between the varied motivations of practitioners (drone navigation, pipe routing, video games) and the domains of available problems (aerial video game traversal).

In particular, we have developed the **Sandstone**, **Descent**, and **Industrial Plant** data sets, using advanced methods of problem generation to select only a small, but comprehensive set of problems from across the entire distribution fo difficulty. We present each of these problem instances along with useful metrics in an informed order of increasing difficulty, allowing users to quickly identify performance indicators and to reach more nuanced conclusions.

While we focus here only on *voxel* gridmaps due to their nice properties and high solution quality (i.e. small detours from the true path distance), there are of course many other ways to represent and search in 3D space. These open several other doors and come with their own interesting problems. In the future, we would like to expand this section to include other such benchmarks such as using Sparse Voxel Octrees. For the meantime, however, the below sections detail the four currently available voxel-world benchmarks in the literature, which allow us to begin investigating the wide open area of 3D search.


## Descent Benchmarks

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
--|---|---|---|----
 30 | 2,000 | 60,000 | 478M | 10M
</div>

This benchmark is derived from in-game levels from Descent, a video game developed by Parallax Software and released by Interplay Productions in 1995. It is recognised as the earliest FPS to feature entirely true-3D graphics, and is now open source. Descent is well-suited for search as each level has been designed specifically for 3D maneuverability and traversal; featuring rooms and branching corridors.

We adapt the 27 in-game levels and 3 secret levels into 30 voxel maps (one for each level) with 2,000 instances each, for a total of 60,000 problem instances.

Problem instances are generated solely from the internal traversable region which corresponds to the in-game playable area. The interior region of the original level remains one contiguous, enclosed region, and accounts only for a small proportion of the total size of the map.

For more information, and if you are using these benchmark problems, please cite the following paper to reference the benchmark sets:

@article{nobes2023voxels, title={Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants}, author={Thomas K. Nobes and Daniel D. Harabor and Michael Wybrow and Stuart D.C. Walsh}, journal={The 16th International Symposium on Combinatorial Search (SoCS)}, volume={16}, number={1}, pages={}, year={2023}, url = {https://ojs.aaai.org/index.php/SOCS/article/view/27283 } }


## Industrial Plant Benchmarks

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
--|---|---|---|----
 5 | 2,000 | 10,000 | 227M | 208M
</div>

This benchmark is designed to mimic industrial plant design and pipe routing problems. Using real data from chemical processing plants, we construct voxel maps that feature layouts composed of many types and scales of equipment modules, safety and engineering zones, support units, and more. We construct geometry at 10cm resolution which produces map sizes of hundreds of millions of voxels.

The benchmark consists of five unique plant layouts with 2,000 routing problems each for a total of 10,000 problem instances. Instances are generated by choosing at random start and target locations from among those voxels immediately adjacent to the surfaces of equipment modules. This simulates routing pipes between two fixed attachment points on corresponding modules. To better match the problems to valid routing scenarios, we exclude several areas such as safety or truck access zones, interiors of racks, and many miscellaneous equipment parts such as equipment skirts (lower supports for large vessels) from potential start/target points.

For more information, and if you are using these benchmark problems, please cite the following paper to reference the benchmark sets:

@article{nobes2023voxels, title={Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants}, author={Thomas K. Nobes and Daniel D. Harabor and Michael Wybrow and Stuart D.C. Walsh}, journal={The 16th International Symposium on Combinatorial Search (SoCS)}, volume={16}, number={1}, pages={}, year={2023}, url={https://ojs.aaai.org/index.php/SOCS/article/view/27283 } }


## Sandstone Benchmarks

<<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
--|---|---|---|----
 11 | 2,000 | 22,000 | 64M | 13M
</div>

This benchmark is derived from X-ray tomographic computed images (XRCT) of natural sandstone samples. The samples include Bandera Gray, Parker, Kirby, Bandera Brown, Berea, Berea Sister Gray (BSG), Berea Upper Gray (BUG), Castlegate, Buff Berea (BB), Leopard and Bentheimer sandstones.

We use binary images of the connected pore space, treating the sandstone itself as an obstacle, and the permeable pore space as traversable terrain. Traversable voxels compose a single connected region, assuming a 6-connected neighbourhood.

We define 11 maps with 2,000 pathfinding instances each, for a total of 22,000 problems. The pore-space geometry is characterised by winding narrow corridors and natural nonsymmetric shapes resulting in an environment reminiscent of random grid maps.

For more information, and if you are using these benchmark problems, please cite the following paper to reference the benchmark sets:

@article{nobes2023voxels, title={Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants}, author={Thomas K. Nobes and Daniel D. Harabor and Michael Wybrow and Stuart D.C. Walsh}, journal={The 16th International Symposium on Combinatorial Search (SoCS)}, volume={16}, number={1}, pages={}, year={2023}, url = {https://ojs.aaai.org/index.php/SOCS/article/view/27283 } }


## Warframe Benchmarks

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances**  | **Avg. Map Size (Voxels)** | **Avg. Traversible Size (Voxels)**
--|---|---|---|----
  44 | 10,000 | 440,000 | 159M | 158M
</div>

The benchmarks in this directory are due to Nathan Sturtevant and are mirrored from his repository at MovingAI.com(https://movingai.com/benchmarks/voxels.html). The ones available here are all Version 1 (ca. 2018).

Digital Extremes, a games company in London, Ontario, Canada has made voxel data freely available from their game Warframe to start a new repository of 3D voxel grids. (Pixels are picture elements; voxels are volume elements)

If you find these benchmarks useful for your research, please cite the following paper:

@article{brewer2018voxels, title={Benchmarks for Pathfinding in 3D Voxel Space}, author={Daniel Brewer and Nathan R. Sturtevant}, journal={Symposium on Combinatorial Search (SoCS)}, year={2018} }
