# PHBS_TQFML/Facial Keypoints Detection
## Team Members
王迪雅  Wang Diya  1701213099 <br>
王锦烽  Wang Jinfeng  1701213103 <br>
颜鹏  Yan Peng  1701213130 <br>
朱存正  Zhu Cunzheng  1701213170 <br>
## Project Description/ Goal
Detecting facial keypoints is a very challenging problem. Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions. Computer vision research has come a long way in addressing these difficulties, but there remain many opportunities for improvement. In this project, we are trying to predict keypoint positions on face images. <br>
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
We find the dataset from [Kaggle](https://www.kaggle.com/c/facial-keypoint-detection/data) and use the image information of training dataset to build our model. （The dataset is so large that we just upload the compressed file.)


## Methods
### Step1: Building good training sets and [data preprocessing](https://github.com/diyawang/PHBS_TQFML/blob/master/Project/Data_preprocessing.ipynb).<br>
（1）In all image pixel data, only the top 15% of the darkest point is retained. The remaining points are all turned to pure white.<br>
（2）Set the border to remove noise, leave only the features of the five facial features, and turn all the other points into pure white.<br>
![Image text](https://raw.githubusercontent.com/diyawang/PHBS_TQFML/55a2633520117aa37f840e7861a1444a2a81fc85/Project/data1.png)
<br>
（3）The image is divided into four parts along the midpoints of each side. Right upper part is used to analyze left eye and left upper part is used to analyze right eye.<br>
![Image text](https://raw.githubusercontent.com/diyawang/PHBS_TQFML/master/Project/data2.jpg)
### Step2: Features extraction.<br> 
First, we will focus on the area with only eye.<br>
（1）If the area has less than or equal to three black points, the coordinates of the uppermost, downmost, leftmost, and rightmost points are directly extracted.<br>
（2）If the area has more than three black points, the coordinates of the fourth uppermost, downmost, leftmost, and rightmost points are extracted.<br>
（3）Then extract the sum of the pixels of all black points in the area.<br>
（4）Calculate the median of the horizontal and vertical coordinates of all non-white points in the area for the left and right eyes.<br>
Ultimately, we obtained the ordinates of the four boundary points of the eyes in the two regions, the median of the coordinate of the non-white dots and sum of all non-white points, which contains 22 features in total.<br>
### Step3: Using [Decision Tree/Random Forest](https://github.com/diyawang/PHBS_TQFML/blob/master/Project/analysis.ipynb) to predict facial keypoints.<br> 
Each predicted keypoint is specified by an (x, y) real-valued pair in the space of pixel indices. There are 2 keypoints, which represent the following elements of the face:

Prediction | Description
-------------------|------------------------
left_eye_center_x | x-coordinate of the central point in the left eye
left_eye_center_y | y-coordinate of the central point in the left eye
right_eye_center_x | x-coordinate of the central point in the right eye
right_eye_center_y | x-coordinate of the central point in the right eye


### Step4: Obtaining our results and prediction.<br> 
We will fix the problem of overfitting. Also, we will figure out which model is better to predict the central points of both eyes through mean standard error.

## Conclusion
In this regression analysis, we find that Random Forest is a better model to predict the keypoints of both eyes through mean square error and its coefficient of determination is higher. <br>
The results of Decision Tree:<br>

Prediction | MSE | coefficient of determination
--------|------|-----
left_eye_center_x | 4.131 | 0.061
left_eye_center_y | 3.050 | 0.423
right_eye_center_x | 3.729 | 0.162
right_eye_center_y | 3.200 | 0.382

The results of Random Forest:<br>

Prediction | MSE | coefficient of determination
--------|------|-----
left_eye_center_x | 3.027 | 0.312
left_eye_center_y | 1.977 | 0.626
right_eye_center_x | 3.103 | 0.303
right_eye_center_y | 2.464 | 0.524

![Image text](https://raw.githubusercontent.com/diyawang/PHBS_TQFML/master/Project/sample_results.png)
The write points are the ture location. The red ones are the prediction of Decision Tree, while the blue ones are the prediction of Random Forest.
