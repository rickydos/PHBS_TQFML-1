# PHBS_TQFML/Facial Keypoints Detection
王迪雅 Wang Diya 1701213099 <br>
王锦烽 Wang Jinfeng 1701213103 <br>
颜鹏 Yan Peng 1701213130 <br>
朱存正 Zhu Cunzheng 1701213170 <br>
## Project Description
Detecting facial keypoints is a very challenging problem. Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions. Computer vision research has come a long way in addressing these difficulties, but there remain many opportunities for improvement. In this project, we are trying to predict keypoint positions on face images. <br>
See the [Proposal]
## Features
Each predicted keypoint is specified by an (x, y) real-valued pair in the space of pixel indices. There are 15 keypoints, which represent the following elements of the face:<br>
Features | Description
---------|------
left_eye_center_x |x-coordinate of central 
left_eye_center_y |
right_eye_center_x |
right_eye_center_y |
left_eye_inner_corner_x |
left_eye_inner_corner_y |
left_eye_outer_corner_x |
left_eye_outer_corner_y |
right_eye_inner_corner_x |
right_eye_inner_corner_y |
right_eye_outer_corner_x |
right_eye_outer_corner_y |
left_eyebrow_inner_end_x |
left_eyebrow_inner_end_y |
left_eyebrow_outer_end_x |
left_eyebrow_outer_end_y |
right_eyebrow_inner_end_x |
right_eyebrow_inner_end_y |
right_eyebrow_outer_end_x |
right_eyebrow_outer_end_y |
nose_tip_xnose_tip_y |
mouth_left_corner_x |
mouth_left_corner_y |
mouth_right_corner_x |
mouth_right_corner_y |
mouth_center_top_lip_x |
mouth_center_top_lip_y |
mouth_center_bottom_lip_x |
mouth_center_bottom_lip_y |

## Methods
Step1: Building good training sets and data preprocessing.                                      
Step2: Dimensionality reduction to figure out the best features.<br> 
Step3: Using Preceptron/Logistic Regression/(Kernel) SVM/Decision Tree/Random Forest/KNN/Majority Voting to predict the competitiveness of a bank.<br> 
Step4: Using holdout cross-validation and k-fold cross-validation to select the best model for our predictions.<br> 
Step5: Obtaining our results and the accuracy of our prediction.<br> 
## Data soures
We use annual data of 35 emerging countries in Eastern and Central Europe, Latin America and Asia during the period of 2001-2014 from Bankscope Database, which contains the financial information of most banks in the world, provides us most of the bank-level data. Bankscope Database is also the most frequently cited database in many early works. We also collected macroeconomic data of each country from EIU Countrydata, which provides macroeconomic and historical data for more than 200 countries and regions.
