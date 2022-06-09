# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the required packages. 
### Step2:
Create the input image. 
### Step3:
Create the structuring element. 

### Step4:
Apply opening operation. 
### Step5:
Apply closing operation. 
<br>

 
## Program:

``` Python
# Import necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
im=cv2.putText(img1,' SANATH ',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Input Image",im)
# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))
# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
cv2.imshow("Opening Image",image1)
# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
cv2.imshow("Closing Image",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:

### Display the input Image
![](input.png)
### Display the result of Opening
![](opening.png)

### Display the result of Closing
![](closing.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
