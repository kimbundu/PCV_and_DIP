<html>
<body>

<h1>Introduction</h1>
<p>Current project contains several exercises in Photogrammetric Computer Vision and Digital Image Analysis, performed in C++ using OpenCV library. In order to launch an exercise, run the corresponding bat-file, which specifies arguments required for executable of every exercise.</p>

<h1>Panorama creation</h1>
<p>Creation of a panorama from 3 images. Three photos of the same planar object were taken using slightly different horizontal orientation of the camera. Program performs stitching of the left image to a center one and then stitching of the right image to the result. For every stitching operation user chooses 4 pairs of matching points. From image coordinates of these points homography in 2D is calculated and applied. Resulting image is stored on the disk. <br>
Input files: <br>
ph_left.jpg, ph_mid.jpg, ph_rig.jpg <br>
<img src = "panorama_creation/ph_left.jpg">
<img src = "panorama_creation/ph_mid.jpg">
<img src = "panorama_creation/ph_right.jpg">
Output file:  <br>
panorama.jpg  <br>
<img src = "panorama_creation/panorama.png">
</p>

<h1>Calculation of interior and exterior camera parameters</h1>

<p>Calculation of internal and external parameters of the image. User provides a txt-file with homogeneous 
spacial coordinates of points on the object (cube) and finds these points on the image of this object. <br> 
Input files: <br>  
points.jpg  <br>
<img src = "calc_camera_parameters/points.jpg"> <br>

points.txt  <br>
35 10 0  <br>
15 25 0  <br>
25 0 45  <br>
15 0 10  <br>
0 10 40  <br>
0 40 25  <br>

Output file:  <br>
result.txt  <br>

<h1>Epipolar lines</h1>

<p>Computation of epipolar lines on the images of the same object taken from different viewpoints. 
User chooses 8 pairs of matching points. Images with epipolar lines are shown and saved.  <br>

Input files:  <br>
krem1.jpg  <br> 
<img src = "epipolar_lines/krem1.JPG"> <br>

krem2.jpg  <br>  
<img src = "epipolar_lines/krem2.JPG"> <br>

Output files:  <br>
fst.png  <br> 
<img src = "epipolar_lines/fst.png"> <br>

snd.png   <br>
<img src = "epipolar_lines/snd.png"> <br>
</p>

<h1>Object in 3D</h1>

<p>Calculation of 3D euclidean coordinates of points of a 3D-object from known coordinates of these 
points on two images of this object. Input file bh.dat contains 
more than 1000 lines. Each line consists of x, y pixel coordinates of a point on the first 
image and x, y coordinates of the same point on the second image. Input file pp.dat contains 5 lines, each line consists of x, y pixel coordinates of a point on the first image, x, y coordinates 
of the same point on the second image and X, Y, Z coordinates of this point on the 3D object. 
Program calculates fundamental matrix and than sets projection matrix of one camera as known 
and calculates projection matrix of the second camera. Known projection matrices lead to 
linear triangulation. To upgrade described reconstruction from projective to euclidean, 
control points are used. Required 3D homography is calculated and applied to the whole 
point cloud. Result is a point cloud in euclidean coordinates.  <br>
Input files: <br>
bh.dat, pp.dat  <br>
Output files: <br>
projectiveReconstruction.asc, euclidianReconstruction.asc  <br>
</p>

<h1>Image restoration</h1>

<h1>Unsharp masking</h1>

</body>
</html>