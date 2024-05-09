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

## Program :

### Developed By : Hari Prasath. P
### Reg No : 212223230070

```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("duck.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## Sobel X axis
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
## Sobel Y axis
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
## Sobel XY axis
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
## Laplacian Edge Detector
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
## Canny Edge Detector
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

![Screenshot 2024-05-09 074705](https://github.com/Hari-Prasath-P-08/EDGE-DETECTION/assets/139455593/607368cf-9234-4c07-a7ff-87dbc363c41e)

![Screenshot 2024-05-09 074715](https://github.com/Hari-Prasath-P-08/EDGE-DETECTION/assets/139455593/e14b737f-f5a2-460f-a8f8-640d7fcc0633)

![Screenshot 2024-05-09 074728](https://github.com/Hari-Prasath-P-08/EDGE-DETECTION/assets/139455593/a4ad22fd-f8f9-4a9e-887f-6cb973fad358)

### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-05-09 074805](https://github.com/Hari-Prasath-P-08/EDGE-DETECTION/assets/139455593/4d1f4a33-e379-4a25-9788-f7ac2d60dc9a)

### CANNY EDGE DETECTOR

![Screenshot 2024-05-09 074813](https://github.com/Hari-Prasath-P-08/EDGE-DETECTION/assets/139455593/ed864a01-355c-4331-bbff-7f655bccb654)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
