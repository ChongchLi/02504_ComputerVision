## Learning Objective
After this lecture you should be able to:
### 1.explain homogeneous coordinates

> Homogeneous coordinates are an extension of Euclidean coordinates used in computer vision and graphics to represent points and vectors in a space with one extra dimension. In homogeneous coordinates, points and vectors are represented as (x, y, z, w), where the last component, w, is used to represent the scale of the point or vector. The use of homogeneous coordinates allows for more elegant mathematical formulations of transformations such as translations, rotations, and scaling.


### 2.convert to and from homogeneous coordinates

> To convert from Euclidean coordinates to homogeneous coordinates, we simply add a w component equal to 1. For example, a point (x, y) in Euclidean coordinates would become (x, y, 1) in homogeneous coordinates. To convert from homogeneous coordinates to Euclidean coordinates, we divide the x, y, and z components by the w component. For example, a point (x, y, z, w) in homogeneous coordinates would become (x/w, y/w, z/w) in Euclidean coordinates.

### 3.perform relevant coordinate transformations

> Coordinate transformations in homogeneous coordinates can be performed using matrices. For example, a translation can be represented as a 3x3 matrix that maps a point (x, y, w) to a new point (x', y', w'). Similarly, a rotation can be represented as a 3x3 matrix that maps a point (x, y, w) to a new point (x', y', w'). By combining these matrices, we can perform more complex transformations such as projective transformations.

### 4.explain the pinhole camera model

> The pinhole camera model is a mathematical model that describes how a camera maps 3D points in the world to 2D points in an image. In this model, a camera is represented as a pinhole, or a single point, through which light passes to form an image on a 2D image plane. The camera has intrinsic parameters, such as the focal length and the principal point, that describe the mapping from 3D to 2D, and extrinsic parameters, such as the camera position and orientation, that describe the location of the camera in the world. By combining the intrinsic and extrinsic parameters, we can map 3D points in the world to 2D points in an image and vice versa.