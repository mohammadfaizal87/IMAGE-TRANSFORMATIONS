# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:

Read the input image using cv2.imread() and store it in a variable for further processing

### Step3:

Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically.

5.Rotation rotates the image by a given angle.

### Step4:

Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.


## Program:
```python

Developed By: MOHAMMAD FAIZAL SK
Register Number: 212223240092

import cv2
import numpy as np
import matplotlib.pyplot as plt
image=cv2.imread("C:\\Users\\admin\\Downloads\\images.webp")
image.shape

 ## Display the image

plt.imshow(image[:,:,::-1])
plt.title("Original Image")
plt.show()


i)Image Translation

tx,ty=100,200
M_translation=np.float32([[1,0,tx],[0,1,ty]])
translated_image=cv2.warpAffine(image,M_translation, (773,519))
plt.imshow(translated_image[:,:,::-1])
plt.title("Translated Image")
plt.axis("on")
plt.show()

ii) Image Scaling

fx, fy = 5.0, 2.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  # Set title
plt.axis('off')



iii)Image shearing


shear_matrix = np.float32([[1, 0, 0], [0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  
plt.title("Sheared Image")  
plt.axis('off')


iv)Image Reflection


reflected_image = cv2.flip(image, 2)

plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  
plt.title("Reflected Image")  
plt.axis('off')

v)Image Rotation

(height, width) = image.shape[:2] 
angle = 45 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image")  
plt.axis('off')(height, width) == image.shape[:2] 
angle = 45 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image")  
plt.axis('off')




vi)Image Cropping


x, y, w, h = 200, 200, 400, 250 
cropped_image = image[y:y+h, x:x+w]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")  
plt.axis('off')


```
## Output:

## Original image

<img width="643" height="557" alt="image" src="https://github.com/user-attachments/assets/a4dd198c-992c-4380-b7af-ae930c199cec" />




### i)Image Translation


<img width="762" height="506" alt="image" src="https://github.com/user-attachments/assets/b5c2a135-65d0-4c27-be4c-f55bfc46c8e3" />




### ii) Image Scaling


<img width="717" height="338" alt="image" src="https://github.com/user-attachments/assets/c4409628-e254-4025-b74a-2e707070587a" />




### iii)Image shearing


<img width="725" height="565" alt="image" src="https://github.com/user-attachments/assets/2e0c49d6-f853-4ab6-9a0f-7ae0c8e764f8" />




### iv)Image Reflection


<img width="703" height="550" alt="image" src="https://github.com/user-attachments/assets/4f7cbd51-02e3-4a13-a879-fdfd0d9e809f" />





### v)Image Rotation


<img width="603" height="532" alt="image" src="https://github.com/user-attachments/assets/7fe50818-98ad-49f5-aeb6-9838e13ccf6f" />




### vi)Image Cropping


<img width="641" height="567" alt="image" src="https://github.com/user-attachments/assets/a665d0b8-1b45-440f-900b-10a9528cbbce" />




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
