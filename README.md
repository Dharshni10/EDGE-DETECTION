# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:
Import all the necessary modules for the program.

Step2:
Load a image using imread() from cv2 module.

Step3:
Convert the image to grayscale

Step4:
Using Sobel operator from cv2,detect the edges of the image.

Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### Name : Dharshni V M
### Register Number : 212223240029
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('img.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)  
sobel_edge = cv2.magnitude(sobel_x, sobel_y)

laplacian_edge = cv2.Laplacian(gray_image, cv2.CV_64F)

canny_edge = cv2.Canny(gray_image, 100, 200)

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)

sobel_edge = cv2.magnitude(sobel_x, sobel_y)

sobel_edge = cv2.convertScaleAbs(sobel_edge)

plt.figure(figsize=(8, 6))

plt.imshow(laplacian_edge, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')

plt.imshow(canny_edge, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')

plt.imshow(sobel_edge, cmap='gray')  
plt.title("Sobel Edge Detector")
plt.axis('off')

plt.tight_layout()
plt.show()
```
## Output:
### LAPLACIAN EDGE DETECTOR

![Laplacian](https://github.com/user-attachments/assets/0c6a6d0f-532e-4c05-806b-9a7cf2ad9b30)

### CANNY EDGE DETECTOR

![Canny](https://github.com/user-attachments/assets/bcd874e0-46c4-4f50-b99e-418b822dd8f6)

### SOBEL EDGE DETECTOR

![Sobel](https://github.com/user-attachments/assets/20d7c6bc-c22d-446a-a7d2-3bdbe0a6f466)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
