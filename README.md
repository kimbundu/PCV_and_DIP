## Introduction

Current project contains exercises in Photogrammetric Computer Vision, performed using OpenCV. 
Since exe-files require arguments (paths of used images and files), the fastest way to launch is run the corresponding bat-file.

## Panorama creation

Creation of a panorama from 3 images. User chooses 4 pairs of matching points for each pair of images, homography is calculated and applied.
Input files: ph_left.jpg, ph_mid.jpg, ph_rig.jpg  

Output file:  
panorama.jpg  
![text](/panorama_creation/panorama.png "panorama")

## Calculation of interior and exterior camera parameters 

Calculation of internal and external parameters of the image. User provides a txt-file with homogeneous 
spacial coordinates of points on the object (cube) and finds these points on the image of this object.  

Input files:  
points.jpg  
![text](/calc_camera_parameters/points.JPG "points")

points.txt  
35 10 0  
15 25 0  
25 0 45  
15 0 10  
0 10 40  
0 40 25  

Output file:  
result.txt  

## Epipolar lines

Computation of epipolar lines on the images of the same object taken from different viewpoints. 
User chooses 8 pairs of matching points. Images with epipolar lines are shown and saved.  

Input files:  
krem1.jpg  
![text](/epipolar_lines/krem1.JPG "krem1")  

krem2.jpg  
![text](/epipolar_lines/krem1.JPG "krem2")  

Output files:  
fst.png  
![text](/epipolar_lines/fst.png "first")  

snd.png   
![text](/epipolar_lines/snd.png "second")

## Object in 3D

Calculation of 3D euclidean coordinates of points of a 3D-object from known coordinates of these 
points on two images of this object. Input file bh.dat contains 
more than 1000 lines. Each line consists of x, y pixel coordinates of a point on the first 
image and x, y coordinates of the same point on the second image. Input file pp.dat contains 5 lines, each line consists of x, y pixel coordinates of a point on the first image, x, y coordinates 
of the same point on the second image and X, Y, Z coordinates of this point on the 3D object. 
Program calculates fundamental matrix and than sets projection matrix of one camera as known 
and calculates projection matrix of the second camera. Known projection matrices lead to 
linear triangulation. To upgrade described reconstruction from projective to euclidean, 
control points are used. Required 3D homography is calculated and applied to the whole 
point cloud. Result is a point cloud in euclidean coordinates.  

Input files: 
bh.dat, pp.dat  
Output files: 
projectiveReconstruction.asc, euclidianReconstruction.asc  

## Image restoration

## Unsharp masking

