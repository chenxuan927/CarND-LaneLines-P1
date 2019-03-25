# **Finding Lane Lines on the Road** 
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image01]: ./test_images/solidWhiteRight.jpg "solidWhiteRight"
[image02]: ./test_images/solidWhiteCurve.jpg "solidWhiteCurve"
[image03]: ./test_images/solidYellowCurve.jpg "solidYellowCurve"
[image04]: ./test_images/solidYellowCurve2.jpg "solidYellowCurve2"
[image05]: ./test_images/solidYellowLeft.jpg "solidYellowLeft"
[image06]: ./test_images/whiteCarLaneSwitch.jpg "whiteCarLaneSwitch"

[image07]: ./test_images_output/solidWhiteRight.jpg "solidWhiteRight"
[image08]: ./test_images_output/solidWhiteCurve.jpg "solidWhiteCurve"
[image09]: ./test_images_output/solidYellowCurve.jpg "solidYellowCurve"
[image10]: ./test_images_output/solidYellowCurve2.jpg "solidYellowCurve2"
[image11]: ./test_images_output/solidYellowLeft.jpg "solidYellowLeft"
[image12]: ./test_images_output/whiteCarLaneSwitch.jpg "whiteCarLaneSwitch"

[image13]: ./test_images_output/solidWhiteRight_GrayScale.jpg "solidWhiteRight_GrayScale"
[image14]: ./test_images_output/solidWhiteRight_GaussianBlur.jpg "solidWhiteRight_GaussianBlur"
[image15]: ./test_images_output/solidWhiteRight_Canny.jpg "solidWhiteRight_Canny"
[image16]: ./test_images_output/solidWhiteRight_RegionOfInterest.jpg "solidWhiteRight_RegionOfInterest"
[image17]: ./test_images_output/solidWhiteRight_Hough.jpg "solidWhiteRight_Hough"
[image18]: ./test_images_output/solidWhiteRight_Merge.jpg "solidWhiteRight_Merge"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of the following 5 steps.
- Apply the GrayScale transform and Gaussian smoothing
- Apply the Canny Transform
- Apply an image mask by defining the region of the interest
- Apply the Hough transform to return an image with hough lines draw
- Overlay the lines on the original photo

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...
- divide all lines to two groups, left lane line and right lane line, based on the line slope
- perform linear regression on both left line and right line group
- output the averaged left and right lane line

I list down each pipeline step for processing photo solidWhiteRight.jpg
- Original photo
![alt text][image01]
- After GrayScale Transform
![alt text][image13]
- After Gaussian Smoothing
![alt text][image14]
- After Canny Transform
![alt text][image15]
- After Image Mask by ROI
![alt text][image16]
- After Hough Transform
![alt text][image17]
- Merge Lines with Original Photo
![alt text][image18]

The pipeline result
- solidWhiteRight.jpg
![alt text][image01]![alt text][image07]
- solidWhiteCurve.jpg
![alt text][image02]![alt text][image08]
- solidYellowCurve.jpg
![alt text][image03]![alt text][image09]
- solidYellowCurve2.jpg
![alt text][image04]![alt text][image10]
- solidYellowLeft.jpg
![alt text][image05]![alt text][image11]
- whiteCarLaneSwitch.jpg
![alt text][image06]![alt text][image12]


### 2. Identify potential shortcomings with your current pipeline
- the current implementation assumes lane lines to be straight, which does not support curved lane line
- the fixed region of the interest only works for certain driving scenario, which is not applicable for other scenarios
- the parameters for canny and hough transform are adjusted and set manually, which is subjective and may not be optimal


### 3. Suggest possible improvements to your pipeline
- instead of using linear regression, a different approach should be used to support curved line
- define a cost function and use neural network to learn the optimal parameters for canny and hough transform
- enhance detection with tracking algoirthm to handle occlusion cases
