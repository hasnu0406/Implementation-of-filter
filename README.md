# Implementation-of-filter
# HASNA MUBARAK AZEEM
# 212223240052
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1
Import the necessary libraries (cv2, numpy, matplotlib.pyplot) and read the input image using cv2.imread().
</br>
</br> 

### Step 2
Define the kernels for the filters, such as an averaging kernel for smoothing (e.g., a 5x5 matrix of ones divided by 25) and a Laplacian kernel for sharpening.
</br>
</br> 

### Step 3
Apply the smoothing filters to the original image using functions like cv2.filter2D() for the averaging filter, cv2.GaussianBlur() for Gaussian blur, and cv2.medianBlur() for median blur.
</br>
</br> 

### Step 4
Apply the sharpening filter using cv2.filter2D() with the Laplacian kernel, and then add this filtered output to the original image to create the final sharpened image.
</br>
</br> 

### Step 5
Display the original, smoothed, and sharpened images side-by-side using matplotlib.pyplot.imshow() and plt.subplot() for comparison.
</br>
</br> 

## Program
### Developed By   : HASNA MUBARAK AZEEM
### Register Number: 212223240052
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("hasna.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python


kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()



```
iii) Using Gaussian Filter
```Python



gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()

```
iv)Using Median Filter
```Python


median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python



kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

<img width="867" height="541" alt="image" src="https://github.com/user-attachments/assets/b6e4a797-0239-4633-93e2-a6218025e777" />



ii)Using Weighted Averaging Filter
<img width="789" height="499" alt="image" src="https://github.com/user-attachments/assets/5bf53341-47d9-4139-aa9d-3b340202fd0d" />


iii)Using GaussianBlur
<img width="782" height="500" alt="image" src="https://github.com/user-attachments/assets/49128dc0-3b9e-4c6c-924c-cf5a2bc5f015" />



iv) Using Median Filter
<img width="862" height="545" alt="image" src="https://github.com/user-attachments/assets/6b26e819-7541-4d46-911b-d6dc5161a1de" />




### 2. Sharpening Filters


i) Using Laplacian Kernal

<img width="787" height="511" alt="image" src="https://github.com/user-attachments/assets/e8678212-01d0-45e7-80e1-fd7f86874169" />



ii) Using Laplacian Operator

<img width="774" height="491" alt="image" src="https://github.com/user-attachments/assets/869841ff-eba3-4ff4-b134-2955b96c368a" />






## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
