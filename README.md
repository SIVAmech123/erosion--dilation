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
## Developed by: SIVAKUMAR R
## Register number: 212223230209
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'SIVAKUMAR R' ,(5,70),font,4,(255),2,cv2.LINE_AA)


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
![WhatsApp Image 2025-05-07 at 15 12 55_2414f95f](https://github.com/user-attachments/assets/bf6151af-35c0-4f67-b7a3-440ae30a6a2a)

### Display the Eroded Image

![WhatsApp Image 2025-05-07 at 15 13 10_1f1d7d71](https://github.com/user-attachments/assets/e64f822b-1a74-4c4c-a43f-97aa8d0a8a3c)

### Display the Dilated Image
![WhatsApp Image 2025-05-07 at 15 13 21_127cdbf2](https://github.com/user-attachments/assets/c2a497f0-ec91-41be-a70c-d2f9ebe5c089)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
