# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import All The Necessary Modules. 

### Step2
Using Averaging Filter Smoothen the given image

### Step3
Using the Weighted Averaging Filter Smoothen the given Image.

### Step4

Using the Gaussian Filter Smoothen the given Image.

### Step5
Using the Median Filter Smoothen the given Image.

### Step 6
Using the Laplacian Kernel Filter Sharpen the given Image.

### Step 7
Using the Laplacian Operator Filter Sharpen the given Image.

## Program:
### Developed By   : Ritika S
### Register Number: 212221240046
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('img.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')



```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('img.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')




```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('img.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')





```

iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('img.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
median=cv2.medianBlur(src=image2, ksize=11)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('img.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1, kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')




```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('img.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
new_image = cv2.Laplacian(image2, cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')




```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
![Output](![img6](https://user-images.githubusercontent.com/93427238/169300851-96ba0532-df14-4ca5-ad13-e830460b3917.png)


ii) Using Weighted Averaging Filter
</br>
![Output](![img1](https://user-images.githubusercontent.com/93427238/169300939-6d4334ee-06a0-4dbc-8f26-9280b418a9c5.png)

</br>

iii) Using Gaussian Filter
</br>
![Output](![img2](https://user-images.githubusercontent.com/93427238/169301045-0ac44cbc-aba7-4ae2-91cf-ee8b09d95802.png)

</br>

iv) Using Median Filter
</br>
![Output](![img3](https://user-images.githubusercontent.com/93427238/169301126-11975743-d9c3-499d-b55f-53d40799b800.png)

</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
![Output](![img4](https://user-images.githubusercontent.com/93427238/169301222-08f76768-b007-4921-a30a-777f27fece3f.png)

</br>

ii) Using Laplacian Operator
</br>
![Output](![img5](https://user-images.githubusercontent.com/93427238/169301305-fcd0b1fc-c5b6-4e72-af11-113017053bfb.png)

</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
