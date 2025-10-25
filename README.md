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
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

``` Python
# Import the necessary packages

# NAME: JAYADEV PALLINTI
# REG NO: 212223240058
import cv2
import numpy as np
from matplotlib import pyplot as plt


# Create the Text using cv2.putText

img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "JAYADEV PALLINTI", (5, 200), font, 2, (255), 6, cv2.LINE_AA)
from google.colab.patches import cv2_imshow
cv2_imshow(img2)


# Create the structuring element

kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))


# Use Opening operation

img_open = cv2.morphologyEx(img2, cv2.MORPH_OPEN, kernel2)
cv2_imshow(img_open)


# Use Closing Operation

img_close = cv2.morphologyEx(img2, cv2.MORPH_CLOSE, kernel1)
cv2_imshow(img_close)


```
## Output:

### Display the input Image
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/1a3feef1-810c-4e2a-b937-a272cc760a05" />


### Display the result of Opening
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/a8a01d7f-acd2-4791-b15c-c02efd3688af" />


### Display the result of Closing
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/f6a696ad-c98d-430d-8cf7-ab401ab9902f" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
