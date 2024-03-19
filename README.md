# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

### Step6:
Rotate the image using angle function.

## Program:
```
Developed By: GOKUL J
Register Number: 212222230038
```

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("dog.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```


ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dog.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```

iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dog.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dog.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dog.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dog.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```

## Output:
### i)Image Translation
![Screenshot 2024-03-19 113152](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/173a093f-eeef-4110-af32-03ae7298b8de)


### ii) Image Scaling
![Screenshot 2024-03-19 113225](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/1684fca9-1b86-4e40-80ba-72014121344d)



### iii)Image shearing
![Screenshot 2024-03-19 113301](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/d6e94697-9edb-4f55-8221-89c4ae1c87b4)
![Screenshot 2024-03-19 113319](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/ec59b110-a165-43db-b4d7-fc18301b9556)



### iv)Image Reflection
![Screenshot 2024-03-19 113414](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/da514add-7604-4deb-8e89-3424953aea4c)
![Screenshot 2024-03-19 113421](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/eae3cb1c-2ca6-457e-8fbe-6232724e09c8)





### v)Image Rotation
![Screenshot 2024-03-19 113501](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/be6205b3-4f2f-4b88-aa47-5b5d420aa6a2)
![Screenshot 2024-03-19 113508](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/cd359206-69c3-4234-a550-fa4428d7325c)




### vi)Image Cropping
![Screenshot 2024-03-19 113547](https://github.com/Gokul0117/IMAGE-TRANSFORMATIONS/assets/121165938/5c497bcc-a208-4fff-8bd1-17194aaaf49a)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
