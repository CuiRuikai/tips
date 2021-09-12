# python-pcl

## advice: Don't touch this horrible package
---

To install python-pcl, the package pcl 1.7.2 need to be installed before.

I did not find a source to install the package pcl 1.7.2 via package manager, but it can be installed from source following below steps:

    [+] reference: https://machineseez.blogspot.com/2017/06/installing-point-cloud-library-18-on.html
    [1] download its source from https://github.com/PointCloudLibrary/pcl/archive/refs/tags/pcl-1.7.2.zip
    [2] unzip it to pcl
    [3] mkdir build
    [4] cd build
    [5] cmake ..
    [6] make
    [7] sudo make install

Others:

    [+] build will fail
        [-] fix it by change return (plane_coeff_d_); to return (*plane_coeff_d_); in file segmentation/include/pcl/segmentation/plane_coefficient_comparator.h
        [-] reference: https://github.com/PointCloudLibrary/pcl/issues/2282
    [+] to build pcl, [VTK](https://vtk.org/) needs to be installed
        [-] wget https://www.vtk.org/files/release/9.0/VTK-9.0.1.tar.gz
        [-] tar -xf VTK-9.0.1.tar.gz
        [-] cd VTK-9.0.1
        [-] mkdir build
        [-] cd build
        [-] cmake ..
        [-] make
        [-] sudo make install
    [+] VTK-9.0.1
        [-] this version has dispatched OpenGL and relies on OpenGL2, but pcl 1.7.2 need OpenGL.
        [-] this issue has been solved by pcl 1.8.0
    [+] fail in the end

