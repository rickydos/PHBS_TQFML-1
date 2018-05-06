# PHBS_TQFML/Facial Keypoints Detection
王迪雅 Wang Diya 1701213099 <br>
王锦烽 Wang Jinfeng 1701213103 <br>
颜鹏 Yan Peng 1701213130 <br>
朱存正 Zhu Cunzheng 1701213170 <br>
## Project Description
Detecting facial keypoints is a very challenging problem. Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions. Computer vision research has come a long way in addressing these difficulties, but there remain many opportunities for improvement. In this project, we are trying to predict keypoint positions on face images. <br>
See the [Proposal]
## Features
Each predicted keypoint is specified by an (x, y) real-valued pair in the space of pixel indices. There are 15 keypoints, which represent the following elements of the face:

Features | Description
-------------------|------------------------
left_eye_center_x | x-coordinate of the central point in the left eye
left_eye_center_y | y-coordinate of the central point in the left eye
right_eye_center_x | x-coordinate of the central point in the right eye
right_eye_center_y | x-coordinate of the central point in the right eye
left_eye_inner_corner_x | x-coordinate of the rightmost point in the left eye
left_eye_inner_corner_y | y-coordinate of the rightmost point in the left eye
left_eye_outer_corner_x | x-coordinate of the leftmost point in the left eye
left_eye_outer_corner_y | y-coordinate of the leftmost point in the left eye
right_eye_inner_corner_x | x-coordinate of the leftmost point in the right eye
right_eye_inner_corner_y | y-coordinate of the leftmost point in the right eye
right_eye_outer_corner_x | x-coordinate of the rightmost point in the right eye
right_eye_outer_corner_y | y-coordinate of the rightmost point in the right eye
nose_tip_x | x-coordinate of the central point in the nose tip 
nose_tip_y | y-coordinate of the central point in the nose tip

## Data soures
We find the dataset from [Kaggle](https://www.kaggle.com/c/facial-keypoint-detection/data) and use the training dataset to build our model.

## Methods
Step1: Building good training sets and data preprocessing.                                      
Step2: Dimensionality reduction to figure out the best features.<br> 
Step3: Using Preceptron/Logistic Regression/(Kernel) SVM/Decision Tree/Random Forest/KNN/Majority Voting to predict the competitiveness of a bank.<br> 
Step4: Using holdout cross-validation and k-fold cross-validation to select the best model for our predictions.<br> 
Step5: Obtaining our results and the accuracy of our prediction.<br> 

