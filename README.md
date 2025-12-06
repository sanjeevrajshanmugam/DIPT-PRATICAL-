# Saveetha Engineering College  
(Autonomous)  
Affiliated to Anna University, Chennai  

## UNIVERSITY LAB EXAMINATION

## **Subject:** 19AI406 - Digital Image Processing Laboratory

## **Date:** _06/12/2025__

## **Name of the Student:** __SANJEEV RAJ.S__

## **Register Number:** __212223220096__

## **Department:** __B.TECH.IT__   

# QUESTION (8)

# 1)

# Code :

```
# Import 
import cv2
import matplotlib.pyplot as plt
# Read the image using OpenCV
img = cv2.imread("checkerboard_color.png", cv2.IMREAD_GRAYSCALE)
sobel_x = cv2.Sobel(img, cv2.CV_64F, 1, 0, ksize=3)
sobel_y = cv2.Sobel(img, cv2.CV_64F, 0, 1, ksize=3)

# Convert to absolute values
sobel_x = cv2.convertScaleAbs(sobel_x)
sobel_y = cv2.convertScaleAbs(sobel_y)

# 3. Combine Sobel results
sobel_combined = cv2.addWeighted(sobel_x, 0.5, sobel_y, 0.5, 0)
# Display the image using Matplotlib
plt.figure(figsize=(8, 8))

plt.subplot(2, 2, 1)
plt.imshow(img, cmap='gray')
plt.title("Original Image")
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(sobel_x, cmap='gray')
plt.title("Sobel X")
plt.axis('off')

plt.subplot(2, 2, 3)
plt.imshow(sobel_y, cmap='gray')
plt.title("Sobel Y")
plt.axis('off')

plt.subplot(2, 2, 4)
plt.imshow(sobel_combined, cmap='gray')
plt.title("Combined Sobel")
plt.axis('off')

plt.tight_layout()
plt.show()

```

# Output

<img width="687" height="672" alt="image" src="https://github.com/user-attachments/assets/56d23005-d361-4a91-8703-79c8c376dda0" />

# 2)

# Code: 

```
import cv2
import matplotlib.pyplot as plt

# Read the image
img = cv2.imread("Large_Scaled_Forest_Lizard.jpg")

# 1. Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# 2. Apply Laplacian operator
laplacian = cv2.Laplacian(gray, cv2.CV_64F)
laplacian = cv2.convertScaleAbs(laplacian)

# 3. Display original and Laplacian output
plt.figure(figsize=(10, 5))

plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(laplacian, cmap='gray')
plt.title("Laplacian Output")
plt.axis('off')

plt.tight_layout()
plt.show()

```

# Output 

<img width="836" height="320" alt="image" src="https://github.com/user-attachments/assets/1e4f8a56-46a0-4dc6-bf94-7f9dfa6945a6" />

# 3)

# Code :

```
import cv2
import matplotlib.pyplot as plt

# 1. Read the image in grayscale
img = cv2.imread("butterfly.jpg", cv2.IMREAD_GRAYSCALE)

# 2. Apply Canny edge detection
canny = cv2.Canny(img, 100, 200)

# 3. Display original and Canny output
plt.figure(figsize=(10, 5))

plt.subplot(1, 2, 1)
plt.imshow(img, cmap='gray')
plt.title("Original Image")
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Image")
plt.axis('off')

plt.tight_layout()
plt.show()

```

# Output

<img width="832" height="307" alt="image" src="https://github.com/user-attachments/assets/dfcdff9c-6c8d-40a8-b773-bb90bca265a4" />


