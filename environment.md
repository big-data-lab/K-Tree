---
title: Working Environment
layout: post
---

The K-Tree clustering software prefers *NIX working environment, but it should also work on other platforms such as Windows.


Hardware
========

In order to have decent clustering performance in term of accuracy, we need to cluster a large enough data set to produce a "converged" tree. To maintain such a big dynamic tree with constant node splitting, it requires all raw data have to be resided in memory. Therefore, to classify satellite images that cover large areas, we need a computer with huge amount of memory. For those lucky ones, with the help of a supercomputer that have [1.6 petabytes of memory](http://arstechnica.com/information-technology/2012/06/with-16-petaflops-and-1-6m-cores-doe-supercomputer-is-worlds-fastest/), building a big-enough-for-everything tree seems to be possible, however, not all researchers and application developers have the luxury to access such a supercomputer or the less powerful ones. So we simply use generic available high performance workstations provided by the major computer manufacturers for all our experiments.

Generally for big data clustering with K-tree, we recommend workstation with memory size no less than 256GB. With this size of memory, we would be able to build an in-memory K-tree for about 120 GeoTiff images with a resolution of 4000x4000 pixels each. As suggested by one of the computer manufacturers, a workstation with 2TB of memory should be available at the end of 2015.


Software
========

- Software dependencies

The K-tree library and programs relies on following third party libraries:

1.  [Boost](http://www.boost.org) (any up to date version)
2.  [Intel Theading Building Blocks](http://www.threadingbuildingblocks.org)
3.  [GDAL](http://www.gdal.org/)
4.  Java 8+ (optional) for a GUI tool plotting the k-tree search results

It is also required to use GCC 4.8+ or equivalents for K-Tree tool compiling.

- Third party libraries installation

###    GDAL<br/>
   For CentOS/RHEL/Oracle Linux users,   <br/>
        <pre><code>#yum install gdal*</code></pre>

   for Debian/Ubuntu/Linux Mints/Other Debian derivatives Linux users,
        <pre><code>$sudo apt-get install gdal*</code></pre>

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
