# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and read the original image.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Find reflection of image.

### Step 6:
Rotate the image.

### Step 7:
Crop the image.

## Program:
### Developed By: R ARUNRAJ
### Register Number: 212220230004
```python
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input= cv2.imread("tower.jpg")
input= cv2.cvtColor(input,cv2.COLOR_BGR2RGB)
cv2.imshow('Input',input)
plt.imshow(input)
cv2.waitKey(0)
plt.axis("on")
rows,cols,dim=input.shape
translation_matrix=np.float32(([1,0,100],[0,1,200],[0,0,1]))
translated_img=cv2.warpPerspective(input,translation_matrix,(cols,rows))
plt.axis("off")
plt.imshow(translated_img)

ii) Image Scaling
scaling_matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input,scaling_matrix,(cols,rows))
plt.axis("off")
plt.imshow(scaled_img)

iii)Image shearing
shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
sheared_img=cv2.warpPerspective(input,shearing_matrix,(cols*2,int(rows*1.5)))
plt.axis("off")
plt.imshow(sheared_img)

iv)Image Reflection
reflection_matrix_col=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_col=cv2.warpPerspective(input,reflection_matrix_col,(cols,int(rows)))
plt.axis("off")
plt.imshow(reflected_img_col)
reflection_matrix_row=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_row=cv2.warpPerspective(input,reflection_matrix_row,(cols,int(rows)))
plt.axis("off")
plt.imshow(reflected_img_row)

v)Image Rotation
rotation_angle=np.radians(10)
rotation_matrix=np.float32([[np.cos(rotation_angle),-np.sin(rotation_angle),0],
                                [np.sin(rotation_angle),np.cos(rotation_angle),0],
                                [0,0,1]])
rotated_img=cv2.warpPerspective(input,rotation_matrix,(cols,(rows)))
plt.axis("off")
plt.imshow(rotated_img)

vi)Image Cropping
cropped_img=input[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_img)
```
## Output:
### i)Image Translation
<img src="https://user-images.githubusercontent.com/75235747/166108596-853bafb0-149d-4c0d-929d-0a8852b1b163.JPG" width="600">
<img src="https://user-images.githubusercontent.com/75235747/166108602-71299ef3-8352-4a9f-a7f8-e46856c968de.JPG" width="600">

### ii) Image Scaling
<img src="https://user-images.githubusercontent.com/75235747/166108627-b6124f3e-9103-4d22-bfee-bb7139a9128f.JPG" width="600">

### iii)Image shearing
<img src="https://user-images.githubusercontent.com/75235747/166108660-cbaee4d8-17e8-4a09-84af-17ba767c98a9.JPG" width="600">

### iv)Image Reflection
<img src="https://user-images.githubusercontent.com/75235747/166108684-1448fc5b-84f0-4958-aee1-0d95fa5168d9.JPG" width="600">
<img src="https://user-images.githubusercontent.com/75235747/166108725-0974dc60-03d5-4d55-a5aa-df19630d59c7.JPG" width="600">

### v)Image Rotation
<img src="https://user-images.githubusercontent.com/75235747/166108806-50318075-9694-499d-9d6f-e529561fda26.JPG" width="600">

### vi)Image Cropping
<img src="https://user-images.githubusercontent.com/75235747/166108819-05f46977-cc04-47de-9ce3-c91dabc9357e.JPG" width="500">

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
