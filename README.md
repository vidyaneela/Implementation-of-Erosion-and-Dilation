# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:
```
Developed by : M Vidya Neela
Reg no : 212221230120
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
text_image = np.zeros((100,550),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"M.VIDYA NEELA",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Erode the image
```
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')
```
# Dilate the image
```
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')
```
## Output:

### Display the input Image

![image](https://github.com/vidyaneela/Implementation-of-Erosion-and-Dilation/assets/94169318/6c89a3f5-3599-4598-ac54-a2e364fb9002)


### Display the Eroded Image

![image](https://github.com/vidyaneela/Implementation-of-Erosion-and-Dilation/assets/94169318/3220e5db-6dac-490d-bb2e-d2652a197f87)


### Display the Dilated Image

![image](https://github.com/vidyaneela/Implementation-of-Erosion-and-Dilation/assets/94169318/549a2d85-ae30-4596-ae29-59de9be56518)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
