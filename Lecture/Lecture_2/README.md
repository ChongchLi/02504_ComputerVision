## Learning Objective
After this lecture you should be able to:

### 1.explain the phenomelogical origin of lens distortion
> Lens distortion occurs due to the fact that the image formed by a lens does not perfectly match the ideal mathematical image. This is because light rays passing through the edges of a lens are bent more than those passing through the center, which causes the image to be distorted. There are two types of lens distortion, barrel distortion and pincushion distortion.

### 2.compensate for lens distortion in images
> There are various methods to compensate for lens distortion in images, including using correction algorithms based on polynomial models of the distortion, using look-up tables, or using machine learning methods. One common method is to model the distortion using a radial distortion model, where the distortion is represented as a polynomial function of the distance from the center of the image. This polynomial can then be inverted to correct the distorted image.

### 3.explain the phenomelogical origin of the pinhole camera parameters
> The pinhole camera parameters describe the geometric relationship between the world coordinate system and the camera coordinate system. These parameters include the intrinsic parameters, such as the focal length and principal point, and the extrinsic parameters, such as the camera orientation and position. The intrinsic parameters describe the mapping between the image plane and the world coordinate system, while the extrinsic parameters describe the location and orientation of the camera in the world.

### 4.derive the homography matrix
> A homography matrix is a 3x3 matrix that describes the mapping between two images of the same scene taken from different perspectives. This matrix can be used to project points from one image onto the other, align images, or perform image stitching. The homography matrix can be estimated using various methods, including direct linear transformation (DLT), RANSAC, or least squares fitting.

### 5.explain the use of homographies in computer vision
> Homographies are used extensively in computer vision for tasks such as image alignment, image stitching, and camera calibration. They allow us to project points from one image to another and align images that were captured from different viewpoints. This can be useful in a variety of applications, including augmented reality, panoramic image creation, and object tracking.

### 6.perform the linear estimation of a homography matrix
> To perform the linear estimation of a homography matrix, we need to have corresponding points in both images. These points can be found using feature detection and matching techniques. Once we have these corresponding points, we can use a linear least squares algorithm to estimate the homography matrix that maps one set of points to the other.

### 7.use singular value decomposition (SVD) to solve linear systems
> Singular Value Decomposition (SVD) is a method for solving linear systems that involves finding the eigenvalues and eigenvectors of a matrix. It is commonly used in computer vision to solve problems such as estimation of the homography matrix, or to perform matrix factorization for tasks such as image compression or denoising. In computer vision, SVD can be used to estimate the homography matrix by finding the matrix that best aligns two sets of corresponding points in two images.