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


```
DEVELOPED BY NAVEEN RAJA N R
REG NO 212222230093
## program 
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('PHOTO 1.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)

# Display results using Matplotlib
plt.figure(figsize=(12, 12))

# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

# Sobel Edge Detection
plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

# Laplacian Edge Detection
plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

# Canny Edge Detection

plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

# Show all results
plt.tight_layout()
plt.show()

```


## Output:

![Screenshot 2024-10-03 112256](https://github.com/user-attachments/assets/e3848efd-0228-4479-b9ee-7b8561b380f8)


### SOBEL EDGE DETECTOR

![Screenshot 2024-10-03 112309](https://github.com/user-attachments/assets/477e517f-3d4e-4a55-941f-aab9391b5dcc)

![output](./sobel.png)

### LAPLACIAN EDGE DETECTOR
![output](./laplacian.png)


![Screenshot 2024-10-03 112318](https://github.com/user-attachments/assets/d10aae4b-b9e8-4ac3-bbbf-022b287fb47c)


### CANNY EDGE DETECTOR
![output](./canny.png)

![Screenshot 2024-10-03 112327](https://github.com/user-attachments/assets/4d10120f-d60f-4659-bd61-2cc570578145)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors
