# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a black image of size 100x600 pixels.


### Step2:

Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step3:
Show the image containing the text without axis labels.

### Step4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).


### Step5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.
## Step6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
DEVELOPED BY: CH.V.S.DINESH KUMAR

REG NO:212224040055

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```PY
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'SIVA DINESH', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```


# Create the structuring element
```PY
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


# Erode the image

```PY
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```


# Dilate the image
```PY
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```





## Output:

### Display the input Image
<img width="515" height="102" alt="download" src="https://github.com/user-attachments/assets/804337f6-3ee4-4c10-866c-179f544a9b85" />

### Display the structuring Image
<img width="600" height="100" alt="download" src="https://github.com/user-attachments/assets/f1c187ba-d1e1-48de-84ba-f634d5d1ad57" />


### Display the Eroded Image
<img width="515" height="102" alt="download" src="https://github.com/user-attachments/assets/5d0b5aa6-cda1-4b7f-ba63-2ee6ba6be093" />


### Display the Dilated Image
<img width="515" height="102" alt="download" src="https://github.com/user-attachments/assets/8a464881-2092-4868-bdab-2d0aa369accd" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
