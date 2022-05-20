# Thresholding of Images
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
<br>Load the necessary packages.

### Step2:
<br>Read the Image and convert to grayscale.

### Step3:
<br>Use Global thresholding to segment the image.

### Step4:
<br>Use Adaptive thresholding to segment the image.

### Step5:
<br>Use Otsu's method to segment the image.

### Step 6:
<br>Display the results.

## Program
```
DEVELOPED BY :VEERAMALAI S
REG NO :212220230056
```
```python
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale
image=cv2.imread("1.jpg",1)
image=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray=cv2.imread("1.jpg",0)

# Use Global thresholding to segment the image
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)

# Use Adaptive thresholding to segment the image
thresh_img7=cv2.adaptive Threshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptive Threshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)

# Use Otsu's method to segment the image 
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)

# Display the results
titles=["Gray Image","Threshold Image (Binary)","Threshold Image (Binary Inverse)","Threshold Image (To Zero)"
       ,"Threshold Image (To Zero-Inverse)","Threshold Image (Truncate)","Otsu","Adaptive Threshold (Mean)","Adaptive Threshold (Gaussian)"]
images=[image_gray,thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,thresh_img6,thresh_img7,thresh_img8]
for i in range(0,9):
    plt.figure(figsize=(10,10))
    plt.subplot(1,2,1)
    plt.title("Original Image")
    plt.imshow(image)
    plt.axis("off")
    plt.subplot(1,2,2)
    plt.title(titles[i])
    plt.imshow(cv2.cvtColor(images[i],cv2.COLOR_BGR2RGB))
    plt.axis("off")
    plt.show()
```
## Output

### Original Image
<br>![eretrf](https://user-images.githubusercontent.com/75234790/169492667-ffe82dfb-170b-4c9d-9cd2-a37130cc90e7.png)

<br>
<br>
<br>
<br>

### Global Thresholding
<br>![dfg](https://user-images.githubusercontent.com/75234790/169492694-be4b6c4d-7024-4ca1-ab2a-78b55ffb833b.png)

<br>
<br>
<br>
<br>

### Adaptive Thresholding
<br>![dfgh](https://user-images.githubusercontent.com/75234790/169492716-1fb6e1de-4d4d-4501-ad51-baa2186bcc3d.png)

<br>
<br>
<br>
<br>

### Optimum Global Thesholding using Otsu's Method
<br>![jhgfhjgkhgjfhcgx](https://user-images.githubusercontent.com/75234790/169492735-6055b955-0019-4482-ba53-c5ea57b56d06.png)

<br>
<br>
<br>
<br>


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.

