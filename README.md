# Lab 05 – Structure from Motion (SfM)

## Results
- **Feature Detection:** feature_detection.png , feature_detection,jpg
- **Feature Matches:** output_match.jpg
- **Camera Pose:** pose.txt
- **3D Reconstruction:** reconstruction.png
- **Bonus:** creative_output.png

## Reflection / Mini-Analysis
1. **Which detector gave denser coverage?**  
   SIFT gave denser coverage than AKAZE due to more keypoints in textured regions.

2. **Effect of crossCheck or ratio threshold on matches:**  
   Increasing crossCheck reduces matches but increases accuracy. Lower ratio threshold allows more matches with potential outliers.

3. **Fundamental Matrix (F) meaning:**  
   Represents epipolar geometry. Points in left image correspond to epipolar lines in right image.

4. **Translation vector (t) direction:**  
   Shows relative direction from camera 1 to camera 2; magnitude is up-to-scale.

5. **Flattened reconstruction meaning:**  
   Indicates small baseline or inaccurate calibration.

6. **SIFT stability:**  
   SIFT is robust to scale, rotation, and moderate viewpoint changes.

7. **Uncalibrated cameras:**  
   Unknown intrinsics add unknown scale & skew; bundle adjustment can refine 3D points later.

## Option A: Visual Story – Rotating 3D Reconstruction

I created a rotating 3D visualization of the reconstructed point cloud using Matplotlib's animation tools. 
The viewpoint rotates 360° around the scene to simulate a camera orbit, allowing a complete inspection of 
depth and spatial structure. This helps visualize occlusions and the relative positions of points more clearly.
