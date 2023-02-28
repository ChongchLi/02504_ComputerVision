## Learning Objective
After this lecture you should be able to:

### 1. Derive and explain the epipolar line in computer vision
> The epipolar line is an important concept in computer vision that helps to determine the 3D structure of a scene from two or more 2D images. When two cameras are used to capture images of a scene, the epipolar line is the line of intersection between the plane of the image and the plane that passes through the camera center and a corresponding point in the other image.\
To derive the epipolar line, we need to start with the fundamental matrix, which describes the relationship between points in two images taken by two cameras. The fundamental matrix can be computed from corresponding points in the two images using various algorithms, such as the eight-point algorithm or RANSAC.\
Once we have the fundamental matrix, we can use it to compute the epipolar line for a point in one image. Given a point in one image, we can use the fundamental matrix to find the corresponding epipolar line in the other image. Specifically, the epipolar line is the line that passes through the point in the first image and is the image of the line passing through the corresponding point and the camera center of the second camera.\
The epipolar line is important because it helps to reduce the search space for finding corresponding points in two images. Instead of searching the entire image, we only need to search along the epipolar line to find the corresponding point. This significantly reduces the computational complexity of finding correspondences between two images.\
In summary, the epipolar line is the line of intersection between the plane of the image and the plane that passes through the camera center and a corresponding point in the other image. It is computed from the fundamental matrix and helps to reduce the search space for finding corresponding points in two images.

### 2. Derive and apply the fundamental matrix in computer vision
> The fundamental matrix is a mathematical concept in computer vision used to describe the relationship between two views of a scene in a stereo camera setup. The fundamental matrix can be used for various applications, such as stereo rectification, stereo matching, and camera calibration.\
Here's a brief overview of how to derive and apply the fundamental matrix:\
> 1. Image point correspondences: Given two images of the same scene, the first step is to find corresponding points between the two images. This can be done manually or automatically using feature extraction and matching techniques.\
> 2. Normalization: Next, the image points need to be normalized to improve the accuracy of the fundamental matrix estimation. This involves scaling and translating the points to a common coordinate system.\
> 3. Fundamental matrix estimation: Once the correspondences are normalized, the fundamental matrix can be estimated using various techniques, such as the eight-point algorithm, normalized eight-point algorithm, or RANSAC.\
> 4. Validation: After estimating the fundamental matrix, it needs to be validated to ensure that it satisfies certain properties, such as rank 2 and epipolar constraints.\
> 5. Application: Once the fundamental matrix is validated, it can be used for various applications, such as stereo rectification, stereo matching, and camera calibration.\

>In summary, the fundamental matrix is a powerful tool in computer vision for describing the relationship between two views of a scene in a stereo camera setup. It can be derived using image point correspondences, normalization, and estimation techniques, and can be applied for various tasks in computer vision.

### 3. Derive and apply the essential matrix in computer vision
> The pinhole camera parameters describe the geometric relationship between the world coordinate system and the camera coordinate system. These parameters include the intrinsic parameters, such as the focal length and principal point, and the extrinsic parameters, such as the camera orientation and position. The intrinsic parameters describe the mapping between the image plane and the world coordinate system, while the extrinsic parameters describe the location and orientation of the camera in the world.

### 4. Implement the linear algorithm for triangulation
> A homography matrix is a 3x3 matrix that describes the mapping between two images of the same scene taken from different perspectives. This matrix can be used to project points from one image onto the other, align images, or perform image stitching. The homography matrix can be estimated using various methods, including direct linear transformation (DLT), RANSAC, or least squares fitting.

### 5. Explain the pros and cons of using a linear algorithm
> Homographies are used extensively in computer vision for tasks such as image alignment, image stitching, and camera calibration. They allow us to project points from one image to another and align images that were captured from different viewpoints. This can be useful in a variety of applications, including augmented reality, panoramic image creation, and object tracking.
