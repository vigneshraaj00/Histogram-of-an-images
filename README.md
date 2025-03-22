# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: vignesh raaj S
# Register Number: 212223230239
import cv2
import numpy as np
import matplotlib.pyplot as plt

gray_image = cv2.imread('EX03.png', cv2.IMREAD_GRAYSCALE)

plt.title("Grayscale Image")
plt.imshow(gray_image, cmap='gray')
plt.axis('off')

plt.title("Histogram of Grayscale Image")
plt.hist(gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 255)
plt.tight_layout()
plt.show()

equalized_gray_image = cv2.equalizeHist(gray_image)

plt.title("Histogram of Equalized Grayscale Image")
plt.hist(equalized_gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 255)

plt.title("Enhanced Grayscale Image")
plt.imshow(equalized_gray_image, cmap='gray')
plt.axis('off')

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2025-03-22 153643](https://github.com/user-attachments/assets/5938202a-87fd-4ffd-9a33-5e63b1dfb492)
![Screenshot 2025-03-22 153724](https://github.com/user-attachments/assets/b23655cc-118b-4f71-93c5-276f0c1b5851)





### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2025-03-22 153802](https://github.com/user-attachments/assets/f5015ac1-8e6d-4ba0-a45b-67dbbab56de8)
![Screenshot 2025-03-22 153839](https://github.com/user-attachments/assets/5d44d4f5-226b-4e88-bcca-aef015e35090)





### Histogram Equalization of Grayscale Image.
![Screenshot 2025-03-22 153944](https://github.com/user-attachments/assets/39430edb-6b44-444c-b7f0-78227b31d557)
![Screenshot 2025-03-22 154025](https://github.com/user-attachments/assets/d513a700-425a-413f-9590-94b7b6e8dc06)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
