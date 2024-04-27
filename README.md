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
``` Python
Developed by : HARISH G
Register Number : 212222243001
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Django',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![Screenshot 2024-04-27 131043](https://github.com/Harish2404lll/erosion--dilation/assets/141472096/2abb3c98-9d3f-4f82-8a48-cf746d58460a)


### Display the Eroded Image
![Screenshot 2024-04-27 131054](https://github.com/Harish2404lll/erosion--dilation/assets/141472096/88baf16a-557d-4670-9bdd-ce4eb7a5a856)


### Display the Dilated Image
![Screenshot 2024-04-27 131423](https://github.com/Harish2404lll/erosion--dilation/assets/141472096/0b518eaf-384b-4d73-ac05-f0de4e97e1f9)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
