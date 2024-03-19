# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.
### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.
## Program:
### Developed By   :S.ANUSHARON
### Register Number:212222240010


### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/CAT.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
kernel = np.ones((11,11), np.float32)/121
image3 = cv2.filter2D(image2,-1, kernel)
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
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/CAT.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3 = cv2.filter2D(image2,-1, kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Origna`l')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('/content/CAT.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
image3 = cv2.GaussianBlur(src=image2, ksize=(11,11), sigmaX=0, sigmaY=0)

plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()
```

iv) Using Median Filter
```



import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('/content/CAT.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
median = cv2.medianBlur(src=image2, ksize=11)
plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('/content/CAT.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1,kernel3)

plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()





```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image1 = cv2.imread('/content/CAT.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB
new_image=cv2.Laplacian(image2,cv2.CV_64F)

plt.figure(figsize=(9, 9))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

plt.show()










```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![Screenshot 2024-03-19 114049](https://github.com/Anusharonselva/Implementation-of-filter/assets/119405600/919e5684-3e48-4922-beb0-3c69fb8114e5)

ii) Using Weighted Averaging Filter
![Screenshot 2024-03-19 114116](https://github.com/Anusharonselva/Implementation-of-filter/assets/119405600/5fb12593-2eac-4e64-a36f-e97749d8172d)

iii) Using Gaussian Filter
![Screenshot 2024-03-19 114138](https://github.com/Anusharonselva/Implementation-of-filter/assets/119405600/c9d096a5-0a61-4bbd-9508-41122f31295a)


iv) Using Median Filter
![Screenshot 2024-03-19 114159](https://github.com/Anusharonselva/Implementation-of-filter/assets/119405600/1d20a513-2a79-443d-aace-1ccd978069eb)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![Screenshot 2024-03-19 114222](https://github.com/Anusharonselva/Implementation-of-filter/assets/119405600/93348072-0770-48a6-8a9c-eb0991467dd2)

ii) Using Laplacian Operator
![Screenshot 2024-03-19 114241](https://github.com/Anusharonselva/Implementation-of-filter/assets/119405600/6c125c2a-4dba-4841-a8e3-37818e0854ea)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
