# PHBS_TQFML/Facial Keypoints Detection
王迪雅 Wang Diya 1701213099 <br>
王锦烽 Wang Jinfeng 1701213103 <br>
颜鹏 Yan Peng 1701213130 <br>
朱存正 Zhu Cunzheng 1701213170 <br>
## Project Description
Detecting facial keypoints is a very challenging problem. Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions. Computer vision research has come a long way in addressing these difficulties, but there remain many opportunities for improvement. In this project, we are trying to predict keypoint positions on face images. <br>
See the [Proposal]
## Features
The original data is the all image pixel data. We use the original 96 X 96 dataset to build up 11 features. Each feature is specified by an (x, y) real-valued pair in the space of pixel indices.

Feature |Description
-------|---------
SUM.L	|Sum of all non-white points in the left eye area
SUM.R	|Sum of all non-white points in the right eye area
Left.x.L |The x-coordinate of the leftmost black point in the left eye area
Left.x.R	|The x-coordinate of the leftmost black point in the right eye area
Right.x.L	|The x-coordinate of the rightmost black point in the left eye area
Right.x.R	|The x-coordinate of the rightmost black point in the right eye area
Top.x.L	|The x-coordinate of the uppermost black point in the left eye area
Top.x.R	|The x-coordinate of the uppermost black point in the right eye area
Bottom.x.L	|The x-coordinate of the downmost black point in the left eye area
Bottom.x.R	|The x-coordinate of the downmost black point in the right eye area
Med.x.L	|Median x-coordinate of all nonwhite points in the left eye area
Med.x.R	|Median x-coordinate of all nonwhite points in the right eye area
Left.y.L	|The y-coordinate of the leftmost black point in the left eye area
Left.y.R	|The y-coordinate of the leftmost black point in the right eye area
Right.y.L	|The y-coordinate of the rightmost black point in the left eye area
Right.y.R	|The y-coordinate of the rightmost black point in the right eye area
Top.y.L	|The y-coordinate of the uppermost black point in the left eye area
Top.y.R	|The y-coordinate of the uppermost black point in the right eye area
Bottom.y.L	|The y-coordinate of the downmost black point in the left eye area
Bottom.y.R	|The y-coordinate of the downmost black point in the right eye area
Med.y.L	|Median y-coordinate of all nonwhite points in the left eye area
Med.y.R	|Median y-coordinate of all nonwhite points in the right eye area

## Data sources
We find the dataset from [Kaggle](https://www.kaggle.com/c/facial-keypoint-detection/data) and use the image information of training dataset to build our model.


## Methods/ Goal
Step1: Building good training sets and data preprocessing.                                      
Step2: Dimensionality reduction to figure out the best features.<br> 
Step3: Using Preceptron/Logistic Regression/(Kernel) SVM/Decision Tree/Random Forest/KNN/Majority Voting to predict the competitiveness of a bank.<br> 
Step4: Using holdout cross-validation and k-fold cross-validation to select the best model for our predictions.<br> 
Step5: Obtaining our results and the accuracy of our prediction.<br> 


Each predicted keypoint is specified by an (x, y) real-valued pair in the space of pixel indices. There are 7 keypoints, which represent the following elements of the face:

Prediction | Description
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





