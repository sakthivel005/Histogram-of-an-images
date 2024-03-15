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
# Developed By: SAKTHIVEL.R
# Register Number: 212222100044
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 gray_image = cv2.imread('gray image.jpg')
color_image = cv2.imread('color image.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()




# Equalized Image
import cv2
Gray_image=cv2.imread('gray image.jpg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()







```
## Output:
### Input Grayscale Image and Color Image
Gray image
![Screenshot 2024-03-15 094238](https://github.com/sakthivel005/Histogram-of-an-images/assets/120550359/8c016863-4387-40d6-87e4-e19541de9dcd)



Color image
![Screenshot 2024-03-15 094256](https://github.com/sakthivel005/Histogram-of-an-images/assets/120550359/a6d5c9bb-ae1f-46ee-bd53-5c4328363f69)



### Histogram of Grayscale Image and any channel of Color Image
 Grayscale Image
![Screenshot 2024-03-15 094316](https://github.com/sakthivel005/Histogram-of-an-images/assets/120550359/5135fb60-bb90-40d2-91fa-c30de41cae4b)

Color Image
![Screenshot 2024-03-15 094330](https://github.com/sakthivel005/Histogram-of-an-images/assets/120550359/573363e1-235a-4a7e-bc75-102f9d667947)


### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-15 094354](https://github.com/sakthivel005/Histogram-of-an-images/assets/120550359/9dcca49f-a4b9-49e1-bc79-ae8df162d626)

![Screenshot 2024-03-15 094419](https://github.com/sakthivel005/Histogram-of-an-images/assets/120550359/56e632cb-3ea5-4c31-a663-c675723dc363)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
