# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
Create a text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Now Erode Nd Dilate the text image.

### Step5:
End the program.
 
## Program:

``` Python
# Import the necessary packages
import cv2
import matplotlib.pyplot as plt
import numpy as np

# Create the Text using cv2.putText
image1 = np.zeros((100,250), dtype = 'uint8')
image1 = cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_COMPLEX = 3
cv2.putText(image1,'Shakthi',(6,70), font, 2, (255,0,255),7,cv2.LINE_AA)

plt.figure()
plt.imshow(image1)
plt.title("original image")
plt.axis("off")
plt.show()

# Create the structuring element
kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(6,6))

# Erode the image
image_erode = cv2.erode(image1,kernel1)

plt.figure()
plt.imshow(image_erode)
plt.title("erosion")
plt.axis("off")
plt.show()

# Dilate the image
image_dilation = cv2.dilate(image1, kernel1)

plt.figure()
plt.imshow(image_dilation)
plt.title("dilation")
plt.axis("off")
plt.show()
```

## Output:

### Display the input Image
![](EX10-1.png)

### Display the Eroded Image
![](EX10-2.png)

### Display the Dilated Image
![](EX10-3.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.