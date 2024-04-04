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

## Programs
## Developed by : Priyanka A
## Reg.No. 212222230113

### Original Image

![butterfly](https://github.com/PriyankaAnnadurai/EDGE-DETECTION/assets/118351569/12af889f-0bc1-4c18-a6b3-dd5f0cdb9d29)



### Convert image to grayscale and remove noise

```py
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("butterfly.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```py
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
**SOBEL Y AXIS :**
```py
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
**SOBEL XY AXIS :**
```py
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
### LAPLACIAN EDGE DETECTOR
```py
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
### CANNY EDGE DETECTOR
```py
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
#### Sobel X Axis Edge Detection

![image](https://github.com/PriyankaAnnadurai/EDGE-DETECTION/assets/118351569/2f7f7108-eaaf-4ca5-bf34-44b898d85df2)

#### Sobel Y Sxis Edge Detection 

![image](https://github.com/PriyankaAnnadurai/EDGE-DETECTION/assets/118351569/d2f12664-500a-44d2-b8ae-d7d5f6f366b2)


#### Sobel XY Sxis Edge Detection 

![image](https://github.com/PriyankaAnnadurai/EDGE-DETECTION/assets/118351569/a1c3aa0c-72be-40a1-9082-8f10b5ae2942)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/PriyankaAnnadurai/EDGE-DETECTION/assets/118351569/61d1147f-d097-4015-ae8a-47b55df8b1ee)


### CANNY EDGE DETECTOR

![image](https://github.com/PriyankaAnnadurai/EDGE-DETECTION/assets/118351569/ef91f6b2-c0d6-4b61-b766-ba40ff2e7352)

## Result:
### Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
