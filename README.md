Brain MRI Tumor Classification and Explainability
I implement patch-based and full-image classification of MRI brain scans to detect tumors, by using ResNet50
Modifications
1. Patch Extraction
•
Updated to extract patches with image-level labels instead of patch-level labeling.
2. CNN Model
•
Replaced custom CNN with ResNet50 pretrained on ImageNet.
•
Added proper preprocessing
•
Fine-tuned fully connected layers on top of ResNet50.
•
Split the dataset into training and test sets.
3. Grad-CAM
•
Updated Grad-CAM to reference the last convolutional layer of ResNet50 (conv5_block3_out).
•
Corrected heatmap calculation and overlay visualization.
•
Added option to specifically test tumor images from the dataset.
4. Explainability
•
Added SHAP
•
Added LIME
Running
1.
Set paths for tumor and non-tumor images in TUMOR_DIR and NON_TUMOR_DIR.
