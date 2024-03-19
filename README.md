# LFS-Aware Surface Reconstruction
Official implementation of LFS-Aware Surface Reconstruction from Unoriented 3D Point Clouds ([arxiv](https://arxiv.org/))
![](teaser/teaser.gif)

### Dependencies
- Boost
- Eigen3
- QT5
- CGAL
- OpenMP

The local feature size (LFS) estimation is available on this [repository](https://github.com/bizerfr/cgal/tree/psp-lfs). 
We fork from the official [CGAL library](https://github.com/CGAL/cgal), and implement a local feature size estimation package. The implementation is [here](https://github.com/CGAL/cgal/pull/8006/files).

To use the LFS package, install the CGAL dependencies and git clone our own [branch](https://github.com/bizerfr/cgal/tree/psp-lfs). 
```
git clone https://github.com/bizerfr/cgal/tree/psp-lfs
```
We provide two examples.
```
cd cgal/Point_set_processing_3/examples/Point_set_processing_3
mkdir build && cd build
cmake ..
make lfs_example_pointset && make lfs_example_tuple
```
Try on your point cloud!

Full code will be released after the preprint is accepted somewhere.
