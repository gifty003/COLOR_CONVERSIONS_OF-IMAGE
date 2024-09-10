# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
	Draw a line from the top-left to the bottom-right of the image.
	Draw a circle at the center of the image.
	Draw a rectangle around a specific region of interest in the image.
	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
	Convert the image from RGB to HSV and display it.
	Convert the image from RGB to GRAY and display it.
	Convert the image from RGB to YCrCb and display it.
	Convert the HSV image back to RGB and display it.

### Step4:
	Access and print the value of the pixel at coordinates (100, 100).
	Modify the color of the pixel at (200, 200) to white.

### Step5:
	Resize the original image to half its size and display it.
### Step6:
	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
	Flip the original image horizontally and display it.
	Flip the original image vertically and display it.
### Step8:
	Save the final modified image to your local directory.
```
Developed By: GIFTSON RAJARATHINAM N
Register Number: 212222233002
```
# Program:

### 1)Read and Display an Image

```Python
import cv2
image=cv2.imread('loki leo.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
 

### OUTPUT:

![Screenshot 2024-09-10 112109](https://github.com/user-attachments/assets/f62a4047-0501-4078-a6f4-8cad53804b4b)



 

### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
import cv2
img = cv2.imread("loki leo.jpg")
img=cv2.resize(img,(600,800))
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:

![Screenshot 2024-09-10 112212](https://github.com/user-attachments/assets/c2c7fa57-3a9c-4d4b-a265-6ec59d3a848c)




 
### ii)Draw Shapes and Add Text
```Python
import cv2

# Load the image
img = cv2.imread("loki leo.jpg")
img1=cv2.resize(img,(600,800))


# Get the dimensions of the image
height, width, _ = img1.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img1, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:

![Screenshot 2024-09-10 112301](https://github.com/user-attachments/assets/24948fe4-2d65-4884-b88d-ff2a6ff2c028)



      
### iii)Draw a rectangle around a specific region of interest in the image.
```Python

import cv2

img = cv2.imread("loki leo.jpg")
img1=cv2.resize(img,(600,800))
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img1,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 <br>
 <br>

### OUTPUT:

![Screenshot 2024-09-10 112342](https://github.com/user-attachments/assets/de945430-ee4c-4d16-b7a3-db076c8c5e70)




      
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
import cv2

# Load the image
img = cv2.imread("loki leo.jpg")
img1=cv2.resize(img,(600,800))


# Define the text to be added and its position
text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img1, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>

    
### OUTPUT:

![Screenshot 2024-09-10 112415](https://github.com/user-attachments/assets/d562147f-d89d-42ca-95cb-147dcc5c0b4c)




### 3)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```Python
import cv2
img = cv2.imread('loki leo.jpg',1)

img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### OUTPUT:

![Screenshot 2024-09-10 112523](https://github.com/user-attachments/assets/c0263cae-f1f2-4f8d-a16f-f328fa8c4f85)


#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('loki leo.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:

![Screenshot 2024-09-10 112638](https://github.com/user-attachments/assets/9f1a5532-7b7a-4f05-af60-fcdf1fb6fdf3)


#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('loki leo.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:

![Screenshot 2024-09-10 112724](https://github.com/user-attachments/assets/44058a8f-bfef-4b30-8ef8-9ab66367aca0)


#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('loki leo.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:

![Screenshot 2024-09-10 112828](https://github.com/user-attachments/assets/c20aa391-5fd4-4a32-b29a-9a4e91c27d17)


## 4. Access and Manipulate Image Pixels:
```Python
import cv2

# Load and resize the image
img = cv2.imread('loki leo.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-10 113015](https://github.com/user-attachments/assets/27f2d262-cbcb-47d6-a8e2-f522f30035c6)



![Screenshot 2024-09-10 113034](https://github.com/user-attachments/assets/2e0bbc1e-a750-4b6d-9762-82760a4f0249)



## 5. Image Resizing:
```Python
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:

![Screenshot 2024-09-10 113212](https://github.com/user-attachments/assets/625d0ed5-5bea-4bcd-926f-aa866e92dae3)


## 6.Image Cropping:
```Python
import cv2

# Load the image
image1=cv2.imread('loki leo.jpg',1)
img1=cv2.resize(image1,(600,800))

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:

![Screenshot 2024-09-10 113336](https://github.com/user-attachments/assets/58dcbe99-f964-4c4f-9198-659093c2488b)



## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python


import cv2

img = cv2.imread("loki leo.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:

![Screenshot 2024-09-10 113433](https://github.com/user-attachments/assets/055c0c6a-8410-4c6d-b4e8-dca0a677a0cd)



#### ii.)Flip the original image vertically and display it.

```Python
import cv2

img = cv2.imread("loki leo.jpg")
img1=cv2.resize(img,(600,800))
img = cv2.resize(img1,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:

![Screenshot 2024-09-10 113611](https://github.com/user-attachments/assets/341fc8b6-b9d5-4821-b9c4-2c2f760fda19)


## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread("loki leo.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('lokesh1.jpg',img)
```
<br>
<br>

### Output:

![Screenshot 2024-09-10 113754](https://github.com/user-attachments/assets/34f5fd3e-1412-41a1-8dc9-e4f3c75fd261)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.


