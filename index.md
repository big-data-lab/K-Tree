---
title: K-Tree Clustering and Searching Algorithm for Big Spatial Data
layout: post
---
Here, we provide a collection of [K-tree](http://eprints.qut.edu.au/16976/1/k-tree.pdf) related clustering libraries and programs specifically designed to handle big spatial data. The K-tree is a "tree-structured clustering algorithm" - first published in a [paper](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=889418&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D889418) authored by Shlomo Geva @[QUT](http://www.qut.edu.au)  (Queensland University of Technology). The K-tree was built for scalability and within minutes can cluster millions of objects into hundreds to thousands of clusters on a standard ‘off-the-shelf’ workstation (cost $5K-$10K). Searching the clusters is even faster, taking only a fraction of a second for a collection of this size. We believe that no other solution is able to perform at such a large scale on affordable hardware. To refer to the K-tree clustering in your research work, please cite: 

<cite>Geva, Shlomo. "K-tree: a height balanced tree structured vector quantizer." Neural Networks for Signal Processing X, 2000. Proceedings of the 2000 IEEE Signal Processing Society Workshop. Vol. 1. IEEE, 2000.</cite>

The version of K-Tree software in this repository was derived and forked from [LMW-tree](https://github.com/cmdevries/LMW-tree).  which was developed by Chris De Vries and Lance De Vine based on the original work by Shlomo Geva. De Vries and De Vine applied the K-tree to the big data domain and used it to cluster and search the [ClueWeb dataset](http://www.lemurproject.org/clueweb12.php/) – the world’s largest research-focussed text dataset. For K-tree algorithm and its related publications please refer to the archived [K-tree Website@sf.net](http://ktree.sf.net).

After seeing K-tree's powerful ability in clustering big data it has now been applied to cluster and search spatial information. It has currently been applied to satellite images of Australia from NASA’s Landsat 5 and 7 archives; however, it can theoretically be used for any type of spatial information. The K-tree is able to identify patterns in the dataset and locate areas that are similar to each other, for example, identifying remaining salt from an evaporated salt lake. When applied to a time series it can identifying patterns in land use change, for example, land clearing. By doing so, the K-tree can be a useful tool for aiding environmental management.

Below are the detailed information regarding K-tree clustering software compiling and usages:
Setting up the K-Tree
- [Working environment](environment)
- [Compiling the K-tree](building)
How to se the K-tree
- [On-Disk K-tree](on-disk-ktree)
- [List of K-Tree programs and their usages](list)
Other examples
- [More satellite image samples](sample-images)

Currently, this repository is maintained by Alan Woodley and Eric Tang ([@DrEricTang](https://twitter.com/DrEricTang)). It has partially been supported by the [Cooperative Research Centre for Spatial Information (CRCSI)](http://www.crcsi.com.au) . Satellite images have been provided as supplied from [Geoscience Australia](http://www.ga.gov.au/) under a Creative Commons Licence. 










