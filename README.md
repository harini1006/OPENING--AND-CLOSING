## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by: HARINI V
Register Number:212222230044
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ICE AGE', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image
![image](https://github.com/harini1006/OPENING--AND-CLOSING/assets/113497405/8a11b63f-a2e9-4293-8222-37beecf5fcfe)


#### Display the result of Opening

![image](https://github.com/harini1006/OPENING--AND-CLOSING/assets/113497405/07855dd0-1c8c-4f12-b2a9-6861d874a11d)

#### Display the result of Closing
![image](https://github.com/harini1006/OPENING--AND-CLOSING/assets/113497405/8292c4c1-92d7-436b-bd28-76d022660adb)



### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
