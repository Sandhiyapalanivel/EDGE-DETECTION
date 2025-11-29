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
### Original Image
```Python
#Developed by : SANDHIYA P
#Register No: 212223230183
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('bird.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')




```
### SOBEL EDGE DETECTOR
```Python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

### LAPLACIAN EDGE DETECTOR
```Python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```Python

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
### ORIGINAL IMAGE 

![Screenshot 2025-04-24 140027](https://github.com/user-attachments/assets/3c5c534d-8bc6-46cd-a20c-90d04f0b6ca1)

### SOBEL EDGE DETECTOR
![Screenshot 2025-04-24 140033](https://github.com/user-attachments/assets/296302fb-b8f3-47af-9af9-4a89ca92c890)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2025-04-24 140033](https://github.com/user-attachments/assets/28c159ef-387a-4446-9a7c-b0a6e4be93ac)

### CANNY EDGE DETECTOR
![Screenshot 2025-04-24 140046](https://github.com/user-attachments/assets/f13ab133-8ef5-4e17-b39b-b13397f6a138)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
