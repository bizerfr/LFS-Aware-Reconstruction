# LFS-Aware Surface Reconstruction
Official implementation of LFS-Aware Surface Reconstruction from Unoriented 3D Point Clouds ([arxiv](https://arxiv.org/abs/2403.13924))
![](teaser/teaser.gif)

### Dependencies
- Boost
- Eigen3
- QT5
- CGAL
- OpenMP

The local feature size (LFS) estimation is available on this [repository](https://github.com/bizerfr/cgal/tree/psp-lfs). 
We fork from the official [CGAL](https://github.com/CGAL/cgal) library, and implement a local feature size estimation package. The implementation is [here](https://github.com/CGAL/cgal/pull/8006/files).

To use the LFS package, install the CGAL dependencies and git clone our [customized CGAL branch](https://github.com/bizerfr/cgal/tree/psp-lfs). 
```
git clone https://github.com/bizerfr/cgal.git
cd cgal
git checkout psp-lfs
```
We provide two examples.
```
cd Point_set_processing_3/examples/Point_set_processing_3
mkdir build && cd build
cmake ..
make lfs_example_pointset && make lfs_example_tuple
```
Try on your own point cloud!

Full code will be released after the preprint is accepted.
