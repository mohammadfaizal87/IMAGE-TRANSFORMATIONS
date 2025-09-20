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
<img width="623" height="437" alt="image" src="https://github.com/user-attachments/assets/3044fb4f-5f7d-439e-ba34-8e12773de293" />





### i)Image Translation


<img width="619" height="429" alt="image" src="https://github.com/user-attachments/assets/c058b5a9-d26f-45c8-94c0-aa693b4fe0ba" />





### ii) Image Scaling


<img width="620" height="174" alt="image" src="https://github.com/user-attachments/assets/39004e45-c69f-413b-9b29-32aa60ace356" />





### iii)Image shearing

<img width="616" height="431" alt="image" src="https://github.com/user-attachments/assets/097e131c-22e8-45fd-8ae1-34c4d82ad33c" />




### iv)Image Reflection


<img width="621" height="425" alt="image" src="https://github.com/user-attachments/assets/b44a35c5-3b2f-41da-9838-6f7acea1917d" />





### v)Image Rotation


<img width="462" height="463" alt="image" src="https://github.com/user-attachments/assets/1a9e8695-6358-4d0f-91c5-42bc48ed6d2b" />





### vi)Image Cropping

<img width="620" height="461" alt="image" src="https://github.com/user-attachments/assets/31ea3910-9199-42b1-96fb-2b51b177b111" />




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
