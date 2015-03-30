---
title: K-Tree Clustering
layout: post
---

The K-Tree clustering software is a collection [K-tree](http://eprints.qut.edu.au/16976/1/k-tree.pdf) related clustering libraries and programs. K-tree itself is a "tree structured clustering algorithm" which was first published on a [paper](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=889418&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D889418) authored by Shlomo Geva @[QUT](http://www.qut.edu.au) (Queensland University of Technology). To refer K-tree clustering in your research work, please cite:  

<cite>Geva, Shlomo. "K-tree: a height balanced tree structured vector quantizer." Neural Networks for Signal Processing X, 2000. Proceedings of the 2000 IEEE Signal Processing Society Workshop. Vol. 1. IEEE, 2000.</cite>

The version of K-Tree software in this repository was derived and forked from [LMW-tree](https://github.com/cmdevries/LMW-tree) which was developed by Chris de Vries and Lance De Vine who re-wrote the K-tree library based on the original work by S. Geva. For K-tree algorithm and its related publications, please refer to the archived [K-tree Website@sf.net](http://ktree.sf.net) for more information.

After seeing K-tree's powerful ability in clustering big data when it was used in the research work on [ClueWeb data](http://www.lemurproject.org/clueweb12.php/), it is now further utilised to cluster satellite images to help with solving environment related problems. So we have developed an image clustering tool to assist classifying earth surface such as vegetation, forest, farm land, salt lake etc. 

####Salt Lake
![Salt Lake](img/saltlake.png =200x  "Salt Lake")


With the help and support from environmental scientists and government agencies, there are other possibilities we can also look at:

1.     Crop type and yield classification
2.     Land cover change monitoring
3.     Gullies classification in landscape
4.     Hierarchical classification of segmented imagery for vegetation
5.     Others

Below are the detailed information regarding K-Tree clustering software compiling and usages:

- [Working environment](environment)
- [Building K-Tree](building)
- [On-Disk K-tree](on-disk-ktree)
- [List of K-Tree programs and their usages](list)
- [More satellite image samples](sample-images)

Currently, this repository is maintained by Alan Woodley and Eric Tang ([@DrEricTang](https://twitter.com/DrEricTang)).
