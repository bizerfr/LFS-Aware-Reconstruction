# LFS-Aware Surface Reconstruction
Official implementation of LFS-Aware Surface Reconstruction from Unoriented 3D Point Clouds ([arxiv](https://arxiv.org/abs/2403.13924))
![](teaser/teaser.gif)

### Dependencies
- Boost
- Eigen3
- QT5
- CGAL5.6.1
- OpenMP

The local feature size (LFS) estimation is available on this [repository](https://github.com/bizerfr/cgal/tree/psp-lfs). 
We fork from the official [CGAL](https://github.com/CGAL/cgal) library, and implement a local feature size estimation package. The implementation is [here](https://github.com/CGAL/cgal/pull/8006/files).

To use the LFS package, install the CGAL dependencies and git clone our [customized CGAL branch](https://github.com/bizerfr/cgal/tree/psp-lfs). 
```
git clone https://github.com/bizerfr/cgal.git
cd cgal
git checkout psp-lfs
```
Then, replace the original CGAL path (```CGAL_DIR```) with our customized CGAL.
We provide two examples.
```
cd Point_set_processing_3/examples/Point_set_processing_3
mkdir build && cd build
cmake ..
make lfs_example_pointset && make lfs_example_tuple
```
Try on your own point cloud!

### Tips for Using the Toolbox
- When modifying parameters, be sure to re-run the corresponding steps that depend on them. For example, if you change any parameters related to Adaptive Meshing, you must also re-execute the following steps: Estimate_sample_facet_size, Lipschitz_continuity_smoothing_SFS, and Adaptive_meshing.
- Load_Polylines is used to load sharp feature curves, which should be stored in a separate file from the point cloud data.
- max_facet_size, min_facet_size_thickenss_ratio should be carefully tuned. Make sure that max_facet_size is larger than the min_facet_size determined by min_facet_size_thickness_ratio.


Full code will be released after the preprint is accepted.
