### EX NO : 11
### DATE  : 03.06.2022
# <p align="center">Opening and Closing</p>


## AIM:
To implement Opening and Closing using Python and OpenCV.

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
Use Opening operation.
### Step 5:
Use Closing Operation.

<br/><br/><br/><br/><br/>

## PROGRAM:
```
/*
Developed by   : Fawziya A
Register Number: 212220230017
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,450),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Fawziya A',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

## OUTPUT:

### Display the input Image
![WhatsApp Image 2022-06-24 at 8 10 06 PM](https://user-images.githubusercontent.com/75235022/175562719-82739f06-631a-412c-b086-8bdd07ff2777.jpeg)

### Display the result of Opening
![WhatsApp Image 2022-06-24 at 8 27 54 PM](https://user-images.githubusercontent.com/75235022/175562744-a678a547-8b35-4575-a93c-d8e2e100c96a.jpeg)


### Display the result of Closing
![WhatsApp Image 2022-06-24 at 8 27 55 PM (1)](https://user-images.githubusercontent.com/75235022/175562764-3d9a93b3-5c8b-4dd5-9b91-4b3ad1c5eecb.jpeg)


## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
