# EX-6 EDGE-DETECTION
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
## PROGRAM:
```
DEVELOPED BY: Santhosh U
REGISTER NUMBER: 212222240092
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("Edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![Output1](https://github.com/SanthoshUthiraKumar/EDGE-DETECTION/assets/119477975/8128da40-a746-4334-b918-efe5dd459e5d)

### SOBEL EDGE DETECTOR:
![Output2](https://github.com/SanthoshUthiraKumar/EDGE-DETECTION/assets/119477975/b0b8b79a-4c29-46d4-960d-03225ed0e3c1)

![Output3](https://github.com/SanthoshUthiraKumar/EDGE-DETECTION/assets/119477975/bb8dd05b-8fb8-47bb-ba7a-006610471055)

![Output4](https://github.com/SanthoshUthiraKumar/EDGE-DETECTION/assets/119477975/becb34eb-6e59-4d67-9913-e2a00ec724c5)

### LAPLACIAN EDGE DETECTOR
![Output5](https://github.com/SanthoshUthiraKumar/EDGE-DETECTION/assets/119477975/e75c7af8-2674-4957-a779-791668f6fb5e)

### CANNY EDGE DETECTOR
![Output6](https://github.com/SanthoshUthiraKumar/EDGE-DETECTION/assets/119477975/5ee21ac5-aba3-4661-9db3-c08125622798)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
