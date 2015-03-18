---
title: K-Tree Programs
layout: post
---

####KTree Indexer

kindex [options] image_files

	k-tree options:

	          -out                         out_file
	          -distance                    distance
	          -xw                          x_window__size
	          -yw                          y_window_size
	          -maxiter                     maxiter
	          -result                      result_size
	          -order                       order
	          -nb                          number_of_bits
	          -nf                          number_of_fields
	          -nts                         number_of_timesteps
	          -wz                          window_size

	Other options:
	          -index index_file            same the index file with name "index_file"
	          -print [tree:stats]          print the tree info
	                                       tree - the whole tree
	                                       stats - the tree stats
	          -fm[:sample number]          fm - fit memory, so needs sampling the data first when the input data is way too big


####KTree Console

	$kconsole
	Current working directory: /home/tangl3/workspace/lmw-tree
	>help
	help     print help information
	load     rebuild ktree from index file 'ktree.index'
	write    save ktree index
	build /a/path/to/file/or/directory ...
	         build ktree with input
	search [vege|saltlake|b1,b2,b3,b4,b5,b6...]
	         search k-tree
	plot     display search resultsquit     quit ktree console
	>build images/big_small_dir/big_small_output_1.tif
	Loading file images/big_small_dir/big_small_output_1.tif with id 0
	Finished loading images/big_small_dir/big_small_output_1.tif (duration 25 milliseconds)
	Finished building images/big_small_dir/big_small_output_1.tif (duration 0 seconds)
	windowSize 1
	numBits 16 quantize 0 doTimeSeries 0
	Running KTree
	Building KTree of order 100 with maxiter 10 and update delay 1
	KTree initialised
	Adding vectors with 1 items
	Tree levels: 1 in 0s
	Tree levels: 2 in 0s
	Time to add vectors 3806877ms

	Finished inserting ...
	Number of objects: 96000
	Level count: 3
	Cluster count level 1: 12
	Cluster count level 2: 969
	RMSE: 0.0684653

	Cluster count: 969
	done calculate object count
	 3.814985s wall, 3.810000s user + 0.000000s system = 3.810000s CPU (99.9%)
	finished writing out
	>print
	Number of objects: 96000
	Level count: 3
	Cluster count level 1: 12
	Cluster count level 2: 969
	RMSE: 0.0684653
	>load images/saltlakek.index
	k-tree loaded (0s)
	>search saltlake
	search query 3615 4620 5190 5350 3100 1710
	full query 3615 4620 5190 5350 3100 1710
	Search max distance 2050 full Max distance 2050
        >plot

![Salt Lake Search Results](../img/salt-lake-search-results.png  "Salt Lake Search Results")

####KTree Restore

	ktree-restore [options] ktree_index

	Available options:
	          -help                        show help information
	          -print [tree:stats]          print the tree info
	                                       tree - the whole tree
	                                       stats - the tree stats
	          -search [vege|saltlake|v1,v2,v3,v4,v5,v6
	                                      search the tree
