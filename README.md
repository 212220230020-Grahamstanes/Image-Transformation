# Image-Transformation
## AIM:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image using<br>
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])<br>
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 3:
Scale the image using<br>
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])<br>
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 4:
Shear the image using<br>
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])<br>
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 5:
Reflection of image can be achieved through the code<br>
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])<br>
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 6:
Rotate the image using<br>
angle=np.radians(45)<br>
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])<br>
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 7:
Crop the image using <br>
cropped_img=input_img[20:150,60:230]
### Step 8:
Display all the Transformed images.
## PROGRAM:
```python
Developed By: Graham stanes
Register Number: 212220230020
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("img.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
i)Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![image](https://user-images.githubusercontent.com/75235150/169488403-9458b4c5-72fe-4c3f-8d58-ae6c6b666492.png)


### ii) Image Scaling
![image](https://user-images.githubusercontent.com/75235150/169488440-28cb28b1-ca6d-4a04-8fbb-59197871610f.png)


### iii)Image shearing
![image](https://user-images.githubusercontent.com/75235150/169488466-ec64b7c5-58b2-439c-b9c3-19efb4ab3495.png)
![image](https://user-images.githubusercontent.com/75235150/169488483-7c552b06-ff9d-4d34-b00e-75533b5796ac.png)



### iv)Image Reflection
![image](https://user-images.githubusercontent.com/75235150/169488530-40c92d4a-669f-458c-833f-497ba77540d0.png)
![image](https://user-images.githubusercontent.com/75235150/169488550-e407c2a7-91e2-4806-89fb-2da28c797623.png)

### v)Image Rotation
![image](https://user-images.githubusercontent.com/75235150/169488584-c0e0a22d-59dc-45c4-8a05-1822302e44f2.png)



### vi)Image Cropping
!![image](https://user-images.githubusercontent.com/75235150/169488621-38fe5753-213d-45bb-b483-131e53326c72.png)


## RESULT: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
