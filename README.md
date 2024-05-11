# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the resul

 
## Program:
```
NAME : BALAMURUGAN B
REG : 212222230016
```
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ATREIDES',(5,70), font,2,(255),5,cv2.LINE_AA)

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")

# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")

```
## Output:

### Display the input Image

![in10](https://github.com/BALA291/OPENING--AND-CLOSING/assets/120717501/0c4bc8d3-c57d-44c0-8c84-018b98d04a4e)

### Display the result of Opening

![in10i](https://github.com/BALA291/OPENING--AND-CLOSING/assets/120717501/80535630-02ea-45f2-abf9-d73d9586db88)

### Display the result of Closing

![in10ii](https://github.com/BALA291/OPENING--AND-CLOSING/assets/120717501/2be0baca-6a61-4615-b0bf-441f44cad039)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
