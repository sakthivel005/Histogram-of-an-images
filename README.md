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
```
# Developed By: SAKTHIVEL R 
# Register Number: 212222100044 
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("rose.jpg")
color_image = cv2.imread("rose.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("rose.jpg")
Color_image = cv2.imread("rose.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("rose.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```





## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-19 110656](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/47d99e12-5154-4d45-8aa4-4e7d88dcde12) ![Screenshot 2024-03-19 110646](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/35ccc03e-0235-4563-877b-51a52b5ec880)



### Histogram of Grayscale Image and any channel of Color Image
### Gray scale image
![Screenshot 2024-03-19 110936](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/fc69ba51-8f79-4180-a6cf-f2f91855f5c3)
![Screenshot 2024-03-19 110956](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/3b169b2b-ae62-4003-83bb-9fe053280058)

### color image
![Screenshot 2024-03-19 111039](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/d69c8d3b-63b9-4f16-9974-156785d369d2)
![Screenshot 2024-03-19 111049](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/bf9e4654-b473-4e58-8ea3-303e22c5605c)



### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-19 111140](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/d3570f97-6c61-47c3-b7d1-063cce684bb8) ![Screenshot 2024-03-19 111150](https://github.com/Gokul0117/Histogram-of-an-images/assets/121165938/c2dd52bb-d65f-402d-8973-b9de6bc4260d)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
