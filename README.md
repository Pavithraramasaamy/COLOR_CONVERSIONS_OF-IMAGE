# EX-01 Image color Conversions
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

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
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: PAVITHRA R
### Register Number: 212222230106


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
import cv2
image=cv2.imread('virat.jpeg')
cv2.imshow('Cricket',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![1](https://github.com/user-attachments/assets/62b92907-fd8f-4092-ac68-590dcb57c93c)


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("virat.jpeg")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('Cricket', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![2](https://github.com/user-attachments/assets/d66f0c04-9c06-4ebd-89de-6d184596a1b1)


2. Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("virat.jpeg")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('Cricket', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![3](https://github.com/user-attachments/assets/560ac909-2d48-483d-8629-9e0eafef28dc)


3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("virat.jpeg")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('Cricket', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![4](https://github.com/user-attachments/assets/d1c22a73-d893-4472-8a22-ebdaa82a34cd)


4.Add the text "Cricket" at the top-left corner of the image.
```
import cv2
image = cv2.imread("virat.jpeg")
image = cv2.resize(image, (400, 300))
text = "ViratKohli"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Cricket', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![5](https://github.com/user-attachments/assets/e802b3a2-1762-4901-89fc-dccb721129a7)

### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('virat.jpeg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![6](https://github.com/user-attachments/assets/c5671b9d-64ed-493d-88da-c6662acc159c)


(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('virat.jpeg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


![7](https://github.com/user-attachments/assets/712a1ab8-117f-47c6-9323-e26448ba6eb4)


(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('virat.jpeg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![8](https://github.com/user-attachments/assets/623910e0-cd89-4229-9bd2-f1a9f3061f0f)



(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('virat.jpeg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![9](https://github.com/user-attachments/assets/1c4517df-33c9-496c-8d07-9cf6fa1d8efa)



### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
import cv2
image = cv2.imread("virat.jpeg")
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![10](https://github.com/user-attachments/assets/bd83e39a-d997-4c54-a3e3-93c687d02dac)




(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('virat.jpeg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![11](https://github.com/user-attachments/assets/e5b15fd4-be22-4e56-9b82-34428bc8de59)



### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![12](https://github.com/user-attachments/assets/38726681-5c5a-4257-89a3-5203669aafae)



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('virat.jpeg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![13](https://github.com/user-attachments/assets/2686f81f-c0ba-469a-8102-dc5d9e7693d3)


### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("virat.jpeg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![14](https://github.com/user-attachments/assets/a69c3715-1d04-446e-b6ed-127090c38cb2)



(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("virat.jpeg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


![15](https://github.com/user-attachments/assets/34bc028b-ce7c-43ad-88f0-0eb4d395fff3)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("virat.jpeg")
img = cv2.resize(img,(300,200))
cv2.imwrite('dip.jpeg',img)
```

![16](https://github.com/user-attachments/assets/4b17ca01-5e4f-48e4-8655-d01f897526a7)


## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.

