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
cv2.putText(img1,'SAEE' ,(5,70),font,4,(255),2,cv2.LINE_AA)


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
![image](https://github.com/user-attachments/assets/b2c4392f-8ee3-484a-90b0-8db77765dd2c)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/bc8a0330-ce34-494b-8902-9389360aba35)



### Display the Dilated Image
![image](https://github.com/user-attachments/assets/3fed6d51-6194-4a16-9562-03f0396badc5)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
