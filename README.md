# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```py
Developed by: Kanishka V S
Register Number: 212222230061
```
### Import the necessary packages
```py
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```py
img = np.zeros((100, 400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'APPEALING', (5, 70), font, 2, (255), 5, cv2.LINE_AA)
```
### Create the structuring element
```py
kernel = np.ones((7, 7), np.uint8)
```
### Use Opening operation
```py
imgOpening = cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
```
### Use Closing Operation
```py
imgClosing = cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
```
### Display Result:
```py
plt.imshow(img, cmap = 'gray')
plt.axis("off")

plt.imshow(imgOpening, cmap = 'gray')
plt.axis("off")

plt.imshow(imgClosing, cmap = 'gray')
plt.axis("off")
```

## Output:

### Display the input Image
![image](https://github.com/kanishka2305/OPENING--AND-CLOSING/assets/113497357/a6fcd0f7-9973-4204-9921-ff2dcc007f9e)


### Display the result of Opening
![image](https://github.com/kanishka2305/OPENING--AND-CLOSING/assets/113497357/006d9ba0-7293-4b25-b103-044fe5b673a7)


### Display the result of Closing
![image](https://github.com/kanishka2305/OPENING--AND-CLOSING/assets/113497357/ef20604c-be1f-45b0-9525-d5c0084402b0)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
