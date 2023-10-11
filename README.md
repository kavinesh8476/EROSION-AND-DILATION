# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).
<br>
### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.
<br>

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.
<br>

### Step4:
Display the eroded image using cv2.imshow.
<br>

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
<br>

## Program:
```
Developed by:Kavinesh M
Register Number:212222230064
```
### Import the necessary packages
``` Python
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"Kavinesh-M",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


### Erode the image
```python
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("Kavinesh-212222230064",image_erode)
cv2.waitKey(0)
```
### Dilate the image
```python
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("Kavinesh-212222230064",image_dilatel)
cv2.waitKey(0)
```
## Output:

### Display the input Image
<br>

![image](https://github.com/kavinesh8476/EROSION-AND-DILATION/assets/118466561/7944836f-6e67-47cc-81cf-57f9280ecd90)

<br>

### Display the Eroded Image
<br>

![image](https://github.com/kavinesh8476/EROSION-AND-DILATION/assets/118466561/5a5c3af3-6977-4f60-9c4e-c07fcca30f2f)

<br>


### Display the Dilated Image
<br>

![image](https://github.com/kavinesh8476/EROSION-AND-DILATION/assets/118466561/3459129f-4e55-471e-a4e6-3ca90f468229)

<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
