# OptiFlow: Lucas-Kanade Motion Analysis  

## 📌 Overview  
This project evaluates the **Lucas-Kanade optical flow method** by analyzing its performance under two different motion conditions:  
1. **Small Motion** (Simple Shift)  
2. **Large Motion** (Affine Transformation)  

By applying projective and affine transformations to images, we compare the estimated motion vectors from optical flow with the ground truth transformations to assess accuracy.  

## ✨ Features  
- **Manual Point Selection**: Interactive selection of corresponding points for projective transformation.  
- **Projective & Affine Transformations**: Warping images using transformation matrices.  
- **Lucas-Kanade Optical Flow**: Estimating motion vectors between original and transformed images.  
- **Error Analysis**: Computing displacement error and mean optical flow error.  
- **Visualizations**: Displaying ground truth motion vs. optical flow using motion vector plots.  

## 📂 Project Structure  
📦 OptiFlow
├── 📜 Capture_Points.py # Interactive point selection for projective transformation
├── 📜 Projective_Transform.py # Apply projective transformation to an image
├── 📜 Optical_Flow.py # Compute and visualize Lucas-Kanade optical flow
├── 📜 Affine_Transform.py # Apply affine transformation to an image
├── 📜 Error_Analysis.py # Compute optical flow error with ground truth
├── 📜 README.md # Project documentation
└── 📁 images # Folder for input images

perl
Copy code

## 🛠 Dependencies  
Ensure you have the following installed before running the project:  
```bash
pip install opencv-python numpy matplotlib
🚀 Usage
1️⃣ Run Projective Transformation
bash
Copy code
python Projective_Transform.py
Manually select four corresponding points in the original and transformed images.
Computes and applies a projective transformation matrix.
2️⃣ Run Lucas-Kanade Optical Flow
bash
Copy code
python Optical_Flow.py
Converts images to grayscale and detects feature points.
Applies Lucas-Kanade optical flow to estimate motion vectors.
Displays motion tracks comparing original vs. transformed image.
3️⃣ Evaluate Optical Flow Accuracy
bash
Copy code
python Error_Analysis.py
Computes the mean error between Lucas-Kanade estimated motion and ground truth.
Plots motion vectors for comparison.
4️⃣ Apply Affine Transformation
bash
Copy code
python Affine_Transform.py
Uses the first three selected points to compute an affine transformation.
Applies transformation and displays the result.
📊 Results
Motion Tracking: Lucas-Kanade optical flow successfully tracks small motions but struggles with larger affine transformations.
Error Analysis: Mean error quantifies deviation from ground truth, providing insight into optical flow limitations.
Visualization: Motion vectors illustrate differences between estimated and actual transformations.
📌 Future Improvements
Implement Pyramidal Lucas-Kanade for better performance on large motion.
Extend to real-world videos for practical motion tracking analysis.
Compare with Farneback Optical Flow for better accuracy evaluation.
