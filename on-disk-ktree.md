---
title: On Disk K-Tree
layout: post
---

The size of the dataset that can be clustered for the in-memory K-tree is limited by the size of computer memory, which on most systems limits the dataset size to about 10-20 Terabytes. However, the on-disk K-tree preforms clustering on disk rather than in memory thereby, dramatically increasing the size of the dataset that can be clustered.


/****************************************************************************************************************

 the k-tree index file

 HEADER    EXTRAS        INTERNAL NODES                      LEAF NODES
 =========|===========|====================================|==================================================================
 =========|FileList...|KeyAddressKeyAddressKeyAddress......|PixelKeyPixelKeyPixelKeyPixelKeyPixelKeyPixelKeyPixelKeyPixelKey..
 internal node address = header size + (internal node size x internal node order)
 leaf node address = header size + internal nodes size + (leaf node size x leaf node order)


 ****************************************************************************************************************/
