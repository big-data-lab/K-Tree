---
title: Building K-Tree Clustering Software
layout: post
---

After getting the working environment ready, we now can build the K-Tree programs.

Please go the K-Tree source directory:

For ***release*** build:

    make DEBUG=0
    
For ***debug*** build:

    make
    
GNU autotools can be used to create separate directories for the release build and debug build.

For ***release*** build:

	mkdir build/release -p
	cd build/release
	../../configure --prefix=/usr --libdir=/usr/lib64
	make
	sudo make install
    
For ***debug*** build:

	mkdir build/debug -p
	cd build/debug
	../../configure --prefix=/usr --libdir=/usr/lib64
	make
	
