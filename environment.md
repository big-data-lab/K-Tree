---
title: Working Environment
layout: post
---

The K-tree software library has been written in C++. It has been tested on a *NIX working environment, but should also work on other platforms such as Windows. 

Hardware
========

K-tree has been designed to operate on affordable off-the-shelf workstations that cost between $5k and $10K. It has been tested on a server with 256GB memory, which allows for the equivalent of 2 billion pixels to be clustered (120 GeoTiff images from the Landsat 5 and 7 archives at 1 x 1 degree/4000 x 4000 pixel resolution). 

Software
========

- Compiling

It is recommended to use GCC 4.8+ or equivalents to compile the K-tree source code.

- Software dependencies

The K-tree library and programs relies on following third party libraries:

1.  [Boost](http://www.boost.org) (any up to date version)
2.  [Intel Theading Building Blocks](http://www.threadingbuildingblocks.org)
3.  [GDAL](http://www.gdal.org/)
4.  Java 8+ (optional) for a GUI tool plotting the k-tree search results

- Third party libraries installation

###    GDAL<br/>
   For CentOS/RHEL/Oracle Linux users,   <br/>
        <pre><code>#yum install gdal*</code></pre>

   for Debian/Ubuntu/Linux Mints/Other Debian derivatives Linux users,
        <pre><code>$sudo apt-get install gdal*</code></pre>
        
   If you are using CentOS/RHEL 6.0, please read the [GDAL installation guide for CentOS 6](../centos/).

###   TBB<br/>
   Please visit their [website](http://www.threadingbuildingblocks.org) to download the latest version, but sometimes their new version won't be compiled by the compiler. In this case, you might need to choose an achieved version such as [tbb42_20140601oss](https://www.threadingbuildingblocks.org/sites/default/files/software_releases/linux/tbb43_20150316oss_lin.tgz).
   After the installation, you will need put a line similar as the following in your shell environment file (eg. ~/.bashrc), or run it before compiling:
   <pre><code>source /opt/tbb/tbb42_20140601oss/bin/tbbvars.sh intel64</code></pre>

###    Boost<br/>
   In most Linux distributions, boost can be installed via system package management tool:
           <pre><code>#yum install boost*</code></pre>

   or,
        <pre><code>$sudo apt-get install boost*</code></pre>

   There are four particular boost libraries required:
        <pre><code>-lboost_system -lboost_thread -lboost_timer \
					-lboost_chrono -lboost_filesystem</code></pre>
