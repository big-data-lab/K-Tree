---
title: On Disk K-Tree
layout: post
---

As in-memory K-tree is limited by the size of computer memory, we only can cluster the data that can be fit into the memory. So we implement on-disk K-tree which allow clustering on disk rather than in memory thereby, dramatically increasing the size of the dataset that can be classify.



/****************************************************************************************************************

 the k-tree index file

 HEADER    EXTRAS        INTERNAL NODES                      LEAF NODES
 =========|===========|====================================|==================================================================
 =========|FileList...|KeyAddressKeyAddressKeyAddress......|PixelKeyPixelKeyPixelKeyPixelKeyPixelKeyPixelKeyPixelKeyPixelKey..
 internal node address = header size + (internal node size x internal node order)
 leaf node address = header size + internal nodes size + (leaf node size x leaf node order)


 ****************************************************************************************************************/