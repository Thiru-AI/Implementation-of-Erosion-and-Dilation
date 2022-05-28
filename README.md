# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>


### Step2:
Create the text image.
<br>

### Step3:
Create the structuring image for dilation/erosion.
<br>

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
<br>

### Step5:
Display the images.
<br>

 
## Program:

``` Python
# Import the necessary packages

import numpy as np 
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

img1=np.zeros((100,500),dtype= 'uint8') 
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'CRAZY_THIRU',(6,70),font,1.9,(455),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title("Original Image")
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

image_erode = cv2.erode(img1,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,cmap='gray')
plt.axis('off')


# Dilate the image

image_dilate = cv2.dilate(img1,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,cmap='gray')
plt.axis('off')



```
## Output:

### Display the input Image

![1](https://user-images.githubusercontent.com/94980741/170811934-eff8bacf-8107-40af-97f5-8521bafdc40b.png)


### Display the Eroded Image

![2](https://user-images.githubusercontent.com/94980741/170811958-7a155844-6c06-4eae-925f-a867bed3aeff.png)



### Display the Dilated Image

![3](https://user-images.githubusercontent.com/94980741/170811965-16a2703a-c969-4c4d-b5fd-bd37f1bd777a.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
