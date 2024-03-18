# LFS-Aware Surface Reconstruction
official implementation of LFS-Aware Surface Reconstruction from Unoriented 3D Point Clouds ([arxiv](https://arxiv.org/))
![](teaser/teaser.gif)

### Dependencies
- Boost
- Eigen3
- QT5
- CGAL
- OpenMP

The local feature size (LFS) estimation is available on this [repository](https://github.com/bizerfr/cgal/tree/psp-lfs). 
We make a [pull request](https://github.com/CGAL/cgal/pull/8006) to the [CGAL](https://github.com/CGAL/cgal) repository. You can see the header file and examples files we add [here](https://github.com/CGAL/cgal/pull/8006/files).

To use the LFS package, install the dependencies and git clone our [branch](https://github.com/bizerfr/cgal/tree/psp-lfs). 
We provide two examples using our package.
```
cd cgal/Point_set_processing_3/examples/Point_set_processing_3
mkdir build && cd build
cmake ..
make lfs_example_pointset && make lfs_example_tuple
```
Try on your point cloud!

Full code will be released after the preprint is accepted somewhere.
