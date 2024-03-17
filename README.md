# Histogram-of-an-images :
## Aim :
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
### Developed By:  MAMTHA I
### Register Number: 212222230076

```python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("bird.jpg")
color_image = cv2.imread("flower.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()


import numpy as np
import cv2
Gray_image = cv2.imread("bird.jpg")
Color_image = cv2.imread("flower.jpg")
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
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)


import cv2
gray_image = cv2.imread("bird.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()







```
## Output:
### Input Grayscale Image and Color Image :
![1](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/8ca7d368-167a-4b78-bfac-e48359ff76ab)![2](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/ba14cca6-f542-4e63-b738-02873de93df6)




### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-17 124108](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/29222bea-1794-4c6d-8697-24bff9fdff0f)![Screenshot 2024-03-17 124115](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/0cd37002-38b0-4515-8129-cd7c6f29537c)


![Screenshot 2024-03-17 124124](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/6016f5dc-3ee2-408e-986a-f38914e23207)![Screenshot 2024-03-17 124132](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/7a3d6b81-2f82-49f2-b6ca-2efefcfffc04)



### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-17 123623](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/ad6fb91a-e381-4cd5-93c7-34f1cbce0599)![Screenshot 2024-03-17 123637](https://github.com/Mamthaiyappaprabu/Histogram-of-an-images/assets/119393563/37a5985c-f528-4351-bc5a-c2be556217d1)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
