---
date: 2023
layout: syllabus
title: Grid Maps
permalink: /2d-benchmarks/grid-maps
---

<a>**Descriptions:**&nbsp;</a>
<a href='{{ site.baseurl }}/2d-benchmarks/grid-maps/gppc-2013/'><button class='button syllabus'>GPPC 2013</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/2d-benchmarks/grid-maps/gppc-2014/'><button class='button syllabus'>GPPC 2014</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/2d-benchmarks/grid-maps/iron-harvest/'><button class='button syllabus'>Iron Harvest</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/2d-benchmarks/grid-maps/local/'><button class='button syllabus'>Local</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='{{ site.baseurl }}/2d-benchmarks/grid-maps/movingai/'><button class='button syllabus'>MovingAI</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<a>**Downloads:**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a>
<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/gppc-2013/'><button class='button benchmarks'>GPPC 2013</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/gppc-2014/'><button class='button benchmarks'>GPPC 2014</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/iron-harvest/'><button class='button benchmarks'>Iron Harvest</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/local/'><button class='button benchmarks'>Local</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/movingai/'><button class='button benchmarks'>MovingAI</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

Here you can find a series of currently available grid-map benchmarks for 3D pathfinding. Grid maps are collections of unit square grids with uniform costs.
Several of these data sets are developed by other labs, whereas others are produced and hosted here. These banchmarks come from a variety of synthetic and real domains.

With this website, we aim to provide an overarching gateway for easy navigation between these various domains and to facilitate convenient attribution for each benchmark data set. We further aim to enable clear comparisons between various works in the literature on these benchmarks through clear version control and documentation.

## The Grid-Based Path Planning Competition (GPPC): 2013

<div class="fullwidth">

 **Num. of Maps** | **Total Num. of Instances**
--|---
 132 | 1,740,660
</div>

<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/gppc-2013/'><button class='button benchmarks'>Get the Benchmarks!</button></a>


(Mirror) Benchmarks from the 2013 Grid-based Path Planning Competition.

## The Grid-Based Path Planning Competition (GPPC): 2014

<div class="fullwidth">

 **Maps** | **Num. of Maps** | **Total Num. of Instances**
--|---|---
 Starcraft | 11 | 29,970
 Dragon Age: Origins | 27 | 44,414
 Dragon Age 2 | 57 | 54,360
 Mazes | 18 | 145,976
 Random | 18 | 32,228
 Rooms | 18 | 27,130
 Total | 132 | 347,868
</div>

<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/gppc-2014/'><button class='button benchmarks'>Get the Benchmarks!</button></a>

(Mirror) Benchmarks from the 2014 Grid-based Path Planning Competition.

## The Iron Harvest Benchmarks

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances** 
--|---|---
 35 | 2,000 | 70,000
</div>

<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/grid-maps/iron-harvest/'><button class='button benchmarks'>Iron Harvest</button></a>

Home of the Iron Harvest benchmarks. Using data from Iron Harvest, a recent real-time strategy game, we provide 35 distinct maps and 70,000 associated problem instances. Each map has three different representations: navigation mesh, obstacle map and grid. There are 2,000 co-feasible instances per map which allow comparisons across the different representations. We describe the benchmark, our instance generation approach and provide experimental results for some currently leading grid-based and mesh-based path planners.

## The Local Benchmarks

(Mirror) Benchmarks from the [HOG2 pathfinding library](https://github.com/nathansttt/hog2), a pathfinding library due to Nathan Sturtevant. HOG2 (Hierarchical Open Graph 2) is a collection of classes and a tile-based simulator which are designed as a simple model of RTS and other clocked simulation environments. For more on HOG please visit that project's repository.

## The MovingAI Benchmarks

(Mirror) Benchmarks from Nathan Sturtevant's [MovingAI repository](https://www.movingai.com/benchmarks/grids.html). The benchmarks in this directory are due to Nathan Sturtevant and mirrored from his repository at movingai.com. Several different variants of these problems have appeared over the years. The ones available here are all Version 2 (ca. 2018).

If you find these benchmarks useful for your research, please cite the following paper:

@article{sturtevant2012benchmarks, title={Benchmarks for Grid-Based Pathfinding}, author={Sturtevant, N.}, journal={Transactions on Computational Intelligence and AI in Games}, volume={4}, number={2}, pages={144 -- 148}, year={2012}, url = {http://web.cs.du.edu/~sturtevant/papers/benchmarks.pdf}, }