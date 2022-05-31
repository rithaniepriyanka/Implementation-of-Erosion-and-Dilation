# IMPLEMENTATION OF EROSION AND DILATION
## AIM:
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.

## PROGRAM:
```
/*
Developed by   : J . RITHANIEPRIYANKA
Register Number: 212220230039
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img1,'Rithu',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img1)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(img1,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(img1,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()
```
## OUTPUT:

### Display the input Image

![EXP10-A](https://user-images.githubusercontent.com/75235132/171091130-39cc7cd8-25a7-4607-8bf5-de17912e76c8.png)

### Display the Eroded Image

![EXP10-B](https://user-images.githubusercontent.com/75235132/171091139-db57f510-d1a4-403e-ada5-13f3cf9ee5c5.png)

### Display the Dilated Image

![EXP10-C](https://user-images.githubusercontent.com/75235132/171091157-125c6e1e-1ae9-4e6a-9655-e2c70509e754.png)

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
