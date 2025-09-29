# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### ORIGINAL IMAGE
```
NAME : Jothilakshmi Palani
REG NO : 212223110017


import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('melkin.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE
<img width="839" height="551" alt="image" src="https://github.com/user-attachments/assets/caa6d653-8ffe-486b-b78d-17be0bfd29ae" />




### SOBEL EDGE DETECTOR
<img width="731" height="545" alt="image" src="https://github.com/user-attachments/assets/49b55b16-b727-4e0a-8615-281ad8e4ea9c" />




### LAPLACIAN EDGE DETECTOR
<img width="740" height="542" alt="image" src="https://github.com/user-attachments/assets/a13f333d-3469-41a7-8a44-901ab2b8627f" />




### CANNY EDGE DETECTOR
<img width="751" height="549" alt="image" src="https://github.com/user-attachments/assets/b3223892-75d0-4415-b9a4-2c7f77edfc6c" />





## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
