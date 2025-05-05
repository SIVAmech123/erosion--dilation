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
## Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
## Register number: 212223230208
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'VENKATA SAI' ,(5,70),font,4,(255),2,cv2.LINE_AA)


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
![WhatsApp Image 2025-05-05 at 09 38 37_318464b3](https://github.com/user-attachments/assets/5a671d86-8878-4bee-a9b3-43dbeb75ce7a)


### Display the Eroded Image
![WhatsApp Image 2025-05-05 at 09 38 36_a8df6637](https://github.com/user-attachments/assets/4275205a-3fbf-40bf-9003-20c662c67d67)


### Display the Dilated Image
![WhatsApp Image 2025-05-05 at 09 38 36_856be539](https://github.com/user-attachments/assets/4e9b0f4e-030e-4588-9688-01c709c9c139)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
