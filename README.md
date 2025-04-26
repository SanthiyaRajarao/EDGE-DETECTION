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
```
Developed BY:SANtHIYA R
Reg No:212223230192


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('image.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)
sobel_combined = cv2.magnitude(sobel_x, sobel_y)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/755ad521-1415-41cf-9f3e-9b45db03c790)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/0ecb3d14-f6f1-4507-b5f0-c72134b224b9)


### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/50a665f5-e524-444e-b683-29b1c4b9e35f)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
