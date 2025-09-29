# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the required libraries.

### Step2:

Convert the image from BGR to RGB.

### Step3:

Apply the required filters for the image separately.

### Step4:

Plot the original and filtered image by using matplotlib.pyplot.

### Step5:

End the program.

## Program:
### Developed By   :SRISHANTH J
### Register Number: 212223240160
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("/content/DSC_0368 copy.jpg")
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
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```Python
median = cv2.medianBlur(image2, 13)
plt.imshow(cv2.cvtColor(median, cv2.COLOR_BGR2RGB))
plt.title("Median Blur")
plt.axis('off')
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

<img width="717" height="448" alt="image" src="https://github.com/user-attachments/assets/e8214a14-7169-434b-b5e2-b28cbac016ec" />



ii)Using Weighted Averaging Filter

<img width="308" height="411" alt="image" src="https://github.com/user-attachments/assets/05d8aaea-7b89-4b4c-a880-91fcafc8a90e" />



iii)Using Gaussian Filter

<img width="308" height="411" alt="image" src="https://github.com/user-attachments/assets/ff7abd14-fe18-43ae-a5cd-2e8634d30897" />

iv) Using Median Filter

<img width="308" height="411" alt="image" src="https://github.com/user-attachments/assets/8d1525e0-f2be-4b20-869c-49960199709e" />



### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

<img width="308" height="411" alt="image" src="https://github.com/user-attachments/assets/6a0d1246-047a-4577-a2d8-73907ca0f40e" />



ii) Using Laplacian Operator

<img width="308" height="411" alt="image" src="https://github.com/user-attachments/assets/043b4a81-4892-41f8-9221-650a1549efd9" />

## Result:

Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
