# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
<br>
Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
<br>
Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
<br>
Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
<br>
Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step6:
<br>
Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step7:
<br>
Crop the image using cropped_img=input_img[20:150,60:230]

### Step8:
<br>
Display all the Transformed images and end the program.


## Program:
```python
Developed By: DHIVYA SHRI B
Register Number: 212221230009
import numpy as np
import cv2

i)Image Translation:
import matplotlib.pyplot as plt
inputImage=cv2.imread("jen.jpg")
inputImage=cv2.cvtColor(inputImage, cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(inputImage)
plt.show()
rows, cols, dim = inputImage.shape
M= np.float32([[1, 0, 100],
                [0, 1, 200],
                 [0, 0, 1]])
translatedImage =cv2.warpPerspective (inputImage, M, (cols, rows))
plt.imshow(translatedImage)
plt.show()




ii) Image Scaling:
import numpy as np
import cv2
import matplotlib.pyplot as plt
inputImage=cv2.imread("jenifer.jpg")
inputImage=cv2.cvtColor(inputImage, cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(inputImage)
plt.show()
rows, cols, dim = inputImage.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 1.8, 0],
                  [0, 0, 1]])
scaledImage=cv2.warpPerspective(inputImage, M, (cols * 2, rows * 2))
plt.imshow(scaledImage)
plt.show()




iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
inputImage=cv2.imread("jen2.jpg")
inputImage=cv2.cvtColor(inputImage, cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(inputImage)
plt.show()
rows, cols, dim = inputImage.shape
matrixX = np.float32([[1, 0.5, 0],
                      [0, 1 ,0],
                      [0, 0, 1]])

matrixY = np.float32([[1, 0, 0],
                      [0.5, 1, 0],
                      [0, 0, 1]])
shearedXaxis = cv2.warpPerspective (inputImage, matrixX, (int(cols * 1.5), int (rows * 1.5)))
shearedYaxis = cv2.warpPerspective (inputImage, matrixY, (int (cols * 1.5), int (rows * 1.5)))
plt.imshow(shearedXaxis)
plt.show()
plt.imshow(shearedYaxis)
plt.show()


iv)Image Reflection
import numpy as np
import cv2
import matplotlib.pyplot as plt
inputImage=cv2.imread("jen3.jpg")
inputImage=cv2.cvtColor(inputImage, cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(inputImage)
plt.show()
rows, cols, dim = inputImage.shape
matrixx=np.float32([[1, 0, 0],
                    [0,-1,rows],
                    [0,0,1]])
matrixy=np.float32([[-1, 0, cols],
                    [0,1,0],
                    [0,0,1]])
reflectedX=cv2.warpPerspective(inputImage, matrixx, (cols, rows))
reflectedY=cv2.warpPerspective(inputImage, matrixy, (cols, rows))
plt.imshow(reflectedY)
plt.show()


v)Image Rotation
angle=np.radians(45)
inputImage=cv2.imread("rachel.jpg")
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotatedImage = cv2.warpPerspective(inputImage,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotatedImage)
plt.show()


vi)Image Cropping
angle=np.radians(45)
inputImage=cv2.imread("friends.jpg")
CroppedImage= inputImage[80:600, 80:430]
plt.axis('off')
plt.imshow(CroppedImage)
plt.show()
```

## Output:
### i)Image Translation
<br>
<br>
<br>
<br>
![dip1](https://user-images.githubusercontent.com/94505585/230386557-254a6fb3-52df-4b0f-8877-1f61223da7ea.jpg)


### ii) Image Scaling
<br>
<br>
<br>
<br>
![dip2](https://user-images.githubusercontent.com/94505585/230386633-9176b833-ff1a-4f5e-8e08-59bd3b11d0c6.jpg)


### iii)Image shearing
<br>
<br>
<br>
<br>
![dip3](https://user-images.githubusercontent.com/94505585/230386694-2724b914-f9d9-4872-bd96-9e70610c121e.jpg)


### iv)Image Reflection
<br>
<br>
<br>
<br>
![dip4](https://user-images.githubusercontent.com/94505585/230386746-bafbde18-6b5b-4602-b13e-c66ce812fe7a.jpg)



### v)Image Rotation
<br>
<br>
<br>
<br>
![dip5](https://user-images.githubusercontent.com/94505585/230386823-10214299-45e5-4871-a01a-3ccb4274e638.jpg)



### vi)Image Cropping
<br>
<br>
<br>
<br>
![dip6](https://user-images.githubusercontent.com/94505585/230386836-15d34dbb-7e18-44d4-84e8-56439bb65134.jpg)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
