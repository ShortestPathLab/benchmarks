---
date: 2023
layout: syllabus
title: Poly Maps
permalink: /2d-benchmarks/poly-maps/
---

<a href='{{ site.baseurl }}/2d-benchmarks/poly-maps/iron-harvest/'><button class='button syllabus'>Iron Harvest</button></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

A "Polygon Map" is a description of a 2D pathfinding environment where 
only the obstacles to be avoided are specified. This kind of input is
useful for a variety of algorithms, such as those based on Visibility Graphs.

### Polygon file format .poly

Details a set of polygons that cannot be traversed.  It contains two types:
enclosures where the Euclidean search happens on the interior of a polygon,
and obstacles where the Euclidean search must not intersect with.

The coordinate system has the x-axis increasing towards the right,
and the y-axis increasing upwards.

The format is provided below, elements in ``[]`` are variables
and ``<>`` are sub-format descriptions.

	polygon 1
	[enclosures-n:int] [obstacles-n:int]
	<polygon_desc>{ [enclosures-n] }
	<polygon_desc>{ [obstacles-n] }
	<topology_desc>?
	
	<polygon_desc>:
	[polygon-n:int] ([vertex-x:float] [vertex-y:float]) * [polygon-n]
	

The first line describe the number of enclosures ``[enclosures-n]`` present,
then the number of obstacles ``[obstacles-n]``.

The following ``[enclosures-n]`` lines provides details of all enclosures polygons,
each ``<polygon_desc>`` details the counter-clockwise orientated enclosure, using
1-based ID by order.

The following ``[obstacle-n]`` lines provides details of all obstacle polygons,
each ``<polygon_desc>`` details the clockwise orientated obstacles, using
1-based ID by order.

The ``<polygon_desc>`` details a polygon. ``[polygon-n]`` is the number of
vertices in this polygon, followed by ``[polygon-n]`` number of vertices ``(x,y)``
given by ``[vertex-x]`` and ``[vertex-y]``, no brackets.

An example of this format (with comments):

	polygon 1
	1 2
	4   0 0   10 0   10 10   0 10  # enclosure 1
	4   4 3   4 5   5 5   5 3  # obstacle 1, inside enclosure 1
	3   6 7   6 8   9 8  # obstacle 2, inside enclosure 2

## The Iron Harvest Benchmarks

<div class="fullwidth">

 **Num. of Maps** | **Instances per Map** | **Total Num. of Instances** 
---|---|---
 35 | 2,000 | 70,000
</div>

<a href='https://bitbucket.org/shortestpathlab/benchmarks/src/master/poly-maps/iron-harvest/'><button class='button benchmarks'>Iron Harvest</button></a>

Home of the Iron Harvest benchmarks. Using data from Iron Harvest, a recent real-time strategy game, we provide 35 distinct maps and 70,000 associated problem instances. Each map has three different representations: navigation mesh, obstacle map and grid. There are 2,000 co-feasible instances per map which allow comparisons across the different representations. We describe the benchmark, our instance generation approach and provide experimental results for some currently leading grid-based and mesh-based path planners.