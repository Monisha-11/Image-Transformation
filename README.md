# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the required libraries and image for transformation.

### Step2:

Perform operations on the image like translaton, rotation and other.

### Step3:

Use the warpPerspective(image , matrix, (rows, columns)) function.

### Step4:

Plot the Image and Transformed Image on the graph using matplotlib for identifying changes.

### Step5:

Diifferent operations has been performed on the image.

## Program:
```python
Developed By: Monisha T
Register Number: 212221240029

i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread ("bookcover.jpg")
input_image = cv2. cvtColor (input_image, cv2. COLOR_BGR2RGB)
plt. axis('off')
plt.imshow(input_image)
plt. show()
rows, cols, dim = input_image.shape
M = np. float32([[1, 0, 300],[0, 1, 300],[0, 0, 1]])
translated_image = cv2.warpPerspective (input_image, M, (cols, rows))
plt.axis("off")
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
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

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
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

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation:

![output](./output1.png)


### ii) Image Scaling

![output](./output2.png)

### iii)Image shearing

![output](./output3.png)

### iv)Image Reflection

![output](./output4.png)


### v)Image Rotation

![output](./output5.png)


### vi)Image Cropping

![output](./output6.png)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
