# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. 

First covert the image from RBG to Grey followed by gaussian blur function and Canny to reduce the noise and edges detection.
Next I mask interested area and use Hough function to find lines in this area.
Lastly draw the lanes.

In order to draw a single line, slopes were compared and removed those with max deviation. Filtered until difference between slopes are less than 0.1. 
I used polyfit which return the slope after considering lines left behind. Hardcoded right bottom y-axis as image max height and y-axis for top lines are 310. 


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the region of interest is change. Currently the ROI is hardcoded.

Another shortcoming could be the code is not optimized and not easy to extend the code for further features development.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to optimize the code by removing hardcoded value and refactor the functions.

Another potential improvement could be to implement auto detection of ROI.
