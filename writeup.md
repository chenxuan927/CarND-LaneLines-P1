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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image01]
![alt text][image02]
![alt text][image03]
![alt text][image04]
![alt text][image05]
![alt text][image06]


![alt text][image07]
![alt text][image08]
![alt text][image09]
![alt text][image10]
![alt text][image11]
![alt text][image12]

![alt text][image13]
![alt text][image14]
![alt text][image15]
![alt text][image16]
![alt text][image17]
![alt text][image18]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...