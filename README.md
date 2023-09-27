# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required packages for further process.

### Step 2:
Read the image and convert the bgr image to gray scale image.

### Step 3:
Use any filters for smoothing the image to reduse the noise.

### Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:
Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY : Dharmaraj S
REG NO : 212222240025
```
## Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("rose.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
# SOBEL X AXIS :
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
# SOBEL Y AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
# SOBEL XY AXIS :
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
# SOBEL X AXIS :

![1(a)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/c7d11a51-cbbf-42a1-8ab8-f2c8cb78c502)
![1(b)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/de4c402e-12fa-4d7d-b57e-c664478e4036)


# SOBEL Y AXIS :

![2(a)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/3f3d2639-2f49-47e3-8e90-e3b9e2a8872a)
![2(b)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/2182bec8-3225-45b1-ada6-41d9541679a4)


# SOBEL XY AXIS :

![3(a)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/1d08817f-0d4b-49d9-8628-46c853007b87)
![3(b)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/4f99f3a0-7ce2-4c64-9380-ad099630f851)

### LAPLACIAN EDGE DETECTOR

![4(a)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/7f55cc00-bf9f-434d-82e3-79aac4c2221c)
![4(b)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/a8ab7cb2-5280-487a-88e7-7548ce30a0ab)

### CANNY EDGE DETECTOR

![5(a)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/2943d63a-f8ff-4043-831d-482ac057d888)
![5(b)](https://github.com/dharmaraj-007/EDGEDETECTION/assets/119560386/fb9d415e-e61d-43c9-a18b-89f658c7f7aa)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
