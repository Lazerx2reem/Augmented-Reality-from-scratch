# Augmented-Reality-from-scratch
Building an AR system using Python and OpenCV from scratch

we want to project in a screen a 3D model of a figure whose position and orientation matches the position and orientation of some predefined flat surface. Furthermore, we want to do it in real time, so that if the surface changes its position or orientation the projected model does so accordingly.

We will try to use **homography** transformation (surface image (2D) to the target image (2D)) to achieve this.

We should then apply this transformation to our 3D model and draw it on the screen.

Steps:

1. Recognize the reference flat surface.

2. Estimate the homography.

3. Derive from the homography the transformation from the reference surface coordinate system to the target image coordinate system.

4. Project our 3D model in the image (pixel space) and draw it.

Since this is a real time application, it would have been better to implement a tracking technique and not just plain recognition

Once we have identified the reference surface in the current frame and have a set of valid matches we can proceed to estimate the homography between both images.

Since we have already found a set of matches between both images we can certainly find directly by any of the existing methods an homogeneous transformation that performs the mapping.