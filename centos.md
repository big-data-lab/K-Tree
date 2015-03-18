---
title: GDal Installation on CentOS/RHEL 6.x
layout: post
---

The most convenient way to install GDAL on CentOS/RHEL 6.x will be to use ELGIS repository. Please refer to their [web site](http://elgis.argeo.org/) for detailed installation instructions.

The GDAL version on ELGIS repository could cause dependency problems, so you might need to manually install a few packages.

    #rpm -ihv ftp://195.220.108.108/linux/centos/6.5/os/x86_64/Packages/mpich2-1.2.1-2.3.el6.x86_64.rpm
    #rpm -ihv ftp://195.220.108.108/linux/centos/6.5/os/x86_64/Packages/mpich2-devel-1.2.1-2.3.el6.x86_64.rpm
    #rpm -ihv ftp://195.220.108.108/linux/centos/6.5/os/x86_64/Packages/mpich2-1.2.1-2.3.el6.i686.rpm
    #rpm -ihv ftp://195.220.108.108/linux/centos/6.5/os/x86_64/Packages/mpich2-devel-1.2.1-2.3.el6.i686.rpm
    #rpm -ihv ftp://rpmfind.net/linux/epel/6/x86_64/libgeotiff-devel-1.2.5-6.el6.x86_64.rpm
    #rpm -ihv ftp://rpmfind.net/linux/epel/6/x86_64/libgeotiff-1.2.5-6.el6.x86_64.rpm


Also, library libarmadillo will be also needed, so

    #rpm -ihv http://proj.badc.rl.ac.uk/cedaservices/raw-attachment/ticket/670/armadillo-3.800.2-1.el6.x86_64.rpm

However, this might not be the end of story because the ELGIS's GDAL binary doesn't support BigTiff format.

If you try to process a BigTiff formated image, you might get an error message from GDAL library as follows:

    gdalinfo /a/path/to/bigtiff/file
    ERROR 4: This is a BigTIFF file.  BigTIFF is not supported by this  version of GDAL and libtiff.

In this case, the only solution is to install GDAL from scratch. After downloading and unzipping the latest version of GDAL (version 1.11.2 at the time of writing), run following command in the source path.

    ./configure --prefix=/usr --without-libtool --with-libtiff=internal --with-geotiff=internal --with-armadillo=yes
    make
    sudo make install
