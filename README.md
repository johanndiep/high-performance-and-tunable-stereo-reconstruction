# High-Performance and Tunable Stereo Reconstruction

This Gitlab repository contains the code for the "High-Performance and Tunable Stereo Reconstruction" project. It was developed in the context of the lecture "[3D Vision](https://www.cvg.ethz.ch/teaching/3dvision/2017/index.php)" taught by Prof. Andreas Geiger and Dr. Torsten Sattler.

## Context

Most mobile robots require fast computation of their immediate surroundings in order to perform fast and maneuverable tasks. Conventional stereo algorithms are not adapted for this kind of applications since they focus on reconstruction quality rather than run-time performance. Therefore, the high-performance and tunable stereo reconstruction method presented by Sudeep Pillai, Srikumar Ramalingam and John J. Leonard was implemented in this project. The algorithm provides the option to adjust the desired reconstruction quality, at the cost of a slower run-time performance. The result is a disparity image for each left and right frame pair.

## Installation
This installation was tested for Ubuntu 16.04 LTS. For other operating systems, changes or additional packages might be required. Two external libraries are used, which are included in this repository:

* [exFAST](http://www.ra.cs.uni-tuebingen.de/software/sparsestereo/welcome_e.html)
* [Triangle](https://www.cs.cmu.edu/~quake/triangle.html)

 
Furthermore, the following two libraries were used:

* [OpenCV 2.4.13](https://opencv.org/release/opencv-2-4-13/)
* [Boost](https://www.boost.org/) (tested with 1.58.0.1)

Additional libraries might be required, install on request.

## Dataset

Two KITTI datasets are used which should be contained in folders as:

* [Stereo Evaluation 2012](http://www.cvlibs.net/datasets/kitti/eval_stereo_flow.php?benchmark=stereo) in data/data_stereo_flow
* [Visual Odometry / SLAM Evaluation 2012](http://www.cvlibs.net/datasets/kitti/eval_odometry.php) (00 folder) in data/data_odometry_color

These two datasets can be toggled by changing the variable `int DATASET` in the main.cpp file.

## Compiling and Running

The code was already build on Ubuntu 16.04 using cmake. To run the pipeline, use the executable located at src/main.out. To build the code again, navigate into the src folder and use:

```console
$ cmake .
$ make
```

## Example: Disparity image and Pointcloud

![Diparity image](https://i.imgur.com/pxZun4s.png)
![Pointcloud](https://i.imgur.com/J49u0vP.png)


## Version

* 22. June 2017: Version 1.0, [Documentation](https://gitlab.com/jdiep/high-performance-and-tunable-stereo-reconstruction/tree/master/paper)

## Credential

The core of this work is based on the publication ["High-Performance and Tunable Stereo Reconstruction"](https://arxiv.org/pdf/1511.00758.pdf) by Sudeep Pillai, Srikumar Ramalingam and John J. Leonard.

## Authors

* Johann Diep (MSc Student Mechanical Engineering, ETH Zurich, jdiep@student.ethz.ch)
* Milan Schilling (MSc Student Robotics, Systems and Control, ETH Zurich, milansc@student.ethz.ch)
* Ian Stähli (MSc Student Robotics, Systems and Control, ETH Zurich, staehlii@student.ethz.ch)
