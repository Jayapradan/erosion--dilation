# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
## Developed by: M jayapradan
## Register number: 212224240061
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'m jayapradan' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```

## Output:

### Display the input Image


![WhatsApp Image 2025-05-25 at 21 14 13_01a94f9f](https://github.com/user-attachments/assets/6f24cf04-f3bd-4608-9cca-79ff0943a1ea)



### Display the Eroded Image

![WhatsApp Image 2025-05-25 at 21 14 09_069072ad](https://github.com/user-attachments/assets/167a4b2c-274e-4e52-b402-7e6243fcec9c)


### Display the Dilated Image

![WhatsApp Image 2025-05-25 at 21 14 06_b3ffe335](https://github.com/user-attachments/assets/daee4b43-c372-45ca-a05f-2ed1b1e625a4)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
