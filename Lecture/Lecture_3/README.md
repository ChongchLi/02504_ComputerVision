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
Here's a brief overview of how to derive and apply the fundamental matrix:
> 1. Image point correspondences: Given two images of the same scene, the first step is to find corresponding points between the two images. This can be done manually or automatically using feature extraction and matching techniques.
> 2. Normalization: Next, the image points need to be normalized to improve the accuracy of the fundamental matrix estimation. This involves scaling and translating the points to a common coordinate system.
> 3. Fundamental matrix estimation: Once the correspondences are normalized, the fundamental matrix can be estimated using various techniques, such as the eight-point algorithm, normalized eight-point algorithm, or RANSAC.
> 4. Validation: After estimating the fundamental matrix, it needs to be validated to ensure that it satisfies certain properties, such as rank 2 and epipolar constraints.
> 5. Application: Once the fundamental matrix is validated, it can be used for various applications, such as stereo rectification, stereo matching, and camera calibration.

>In summary, the fundamental matrix is a powerful tool in computer vision for describing the relationship between two views of a scene in a stereo camera setup. It can be derived using image point correspondences, normalization, and estimation techniques, and can be applied for various tasks in computer vision.

### 3. Derive and apply the essential matrix in computer vision
> The essential matrix is a mathematical concept in computer vision used to describe the geometric relationship between two views of a scene, such as the cameras capturing the views. The essential matrix is a 3x3 matrix that encapsulates the rotation and translation between the two camera views. Here's a brief overview of how to derive and apply the essential matrix:\
> 1. Image point correspondences: Given two images of the same scene, the first step is to find corresponding points between the two images. This can be done manually or automatically using feature extraction and matching techniques.
> 2. Calibration: Before estimating the essential matrix, the camera intrinsics need to be calibrated. This involves finding the camera's intrinsic parameters, such as the focal length and principal point.
> 3. Essential matrix estimation: Once the image correspondences and camera intrinsics are known, the essential matrix can be estimated using various techniques, such as the eight-point algorithm or the five-point algorithm.
> 4. Validation: After estimating the essential matrix, it needs to be validated to ensure that it satisfies certain properties, such as rank 2 and the epipolar constraint.
> 5. Decomposition: Once the essential matrix is validated, it can be decomposed into the relative rotation and translation between the two camera views using singular value decomposition (SVD).
> 6. Triangulation: Once the relative pose between the two camera views is known, the 3D positions of the scene points can be triangulated using the image correspondences.

> In summary, the essential matrix is a powerful tool in computer vision for describing the geometric relationship between two camera views capturing the same scene. It can be derived using image point correspondences, camera calibration, and estimation techniques, and can be applied for various tasks such as camera localization, 3D reconstruction, and visual odometry.

### 4. Implement the linear algorithm for triangulation
> Triangulation is a process of determining the 3D position of a point in space using multiple views of the same point from different camera perspectives. The linear algorithm for triangulation is a simple method to compute the 3D position of a point from two or more image correspondences. Here's an overview of how to implement the linear algorithm for triangulation:
> 1. Image correspondences: Given two or more images of the same scene, the first step is to identify corresponding points between the images.
> 2. Camera projection matrices: Next, the projection matrices of the cameras capturing the images need to be obtained. The projection matrix describes how a 3D point in space is projected onto a 2D image plane.
> 3. Linear system: Once the correspondences and camera projection matrices are known, a linear system can be constructed. The linear system is formed by stacking the equation for each correspondence pair. The equation relates the 2D image coordinates to the 3D world coordinates and the camera projection matrix.
> 4. Solve for the 3D point: The linear system can be solved using techniques such as singular value decomposition (SVD) to obtain the 3D position of the point in space.
> 5. Homogeneous coordinates: The 3D point is represented in homogeneous coordinates, which means that a scalar multiple of the point can represent the same point. Therefore, the 3D point needs to be normalized by dividing by the last element of the homogeneous vector.

> In summary, the linear algorithm for triangulation is a simple method to compute the 3D position of a point in space from two or more image correspondences. It involves identifying correspondences, obtaining the camera projection matrices, constructing a linear system, solving for the 3D point, and normalizing the result to homogeneous coordinates. The method can be extended to handle multiple points and multiple cameras.

### 5. Explain the pros and cons of using a linear algorithm
> The linear algorithm for triangulation is a simple and fast method to compute the 3D position of a point in space from two or more image correspondences. However, it has both pros and cons, which are as follows:

> Pros:
> 1. Simplicity: The linear algorithm is easy to implement and understand. It involves only basic linear algebraic operations and can be applied to a wide range of problems.
> 2. Speed: The linear algorithm is computationally efficient compared to other methods that involve non-linear optimization or iterative techniques. The solution can be obtained in real-time for real-world applications.
> 3. Robustness: The linear algorithm can handle noisy and outlier correspondences. It can tolerate errors in the input data and still provide reasonable results.

> Cons:
> 1. Accuracy: The linear algorithm is less accurate than non-linear techniques, such as the iterative algorithm, which can converge to a better solution by refining the initial estimate. The linear algorithm can lead to large errors in the presence of noise, uncertainty, and outliers.
> 2. Limited constraints: The linear algorithm relies on a few constraints, such as the image correspondences and camera projection matrices. It does not take into account other factors, such as lens distortion, camera calibration errors, and lighting variations.
> 3. Ambiguity: The linear algorithm can have multiple solutions, especially when the number of correspondences is small or the point is close to the camera. The ambiguity can lead to incorrect solutions or an under-constrained problem.

> In summary, the linear algorithm for triangulation is a simple and fast method that can provide a quick estimate of the 3D position of a point in space. However, it has limitations in terms of accuracy, robustness, and ambiguity, which need to be taken into account in real-world applications. The choice of algorithm depends on the specific problem requirements and constraints.
