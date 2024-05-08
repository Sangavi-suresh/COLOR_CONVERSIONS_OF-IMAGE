# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: SANGAVI SURESH
### Register Number:  212222230130


## Output:

### i) Read and display the image

    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

### OUTPUT

![308425963-f92cce43-70c6-4df3-b7ba-1be6e7677cce](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/760af16a-cbb5-4146-af49-3d912ebd3718)


### ii)Write the image

    import cv2
    image=cv2.imread('images.jpg',0)
    cv2.imwrite('natural.jpg',image)

### OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/0469e549-2130-4f5b-ae98-9ae7a25c64ac)


### iii)Shape of the Image

    import cv2
    image=cv2.imread('images.jpg',1)
    print(image.shape)

###  OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/ad69e405-1f96-4b0a-933a-c548bf8d514a)


### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### OUTPUT 

![308426138-478d4be2-9c38-47d3-ba4b-854a80686c49](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/adac1b23-6cf4-4213-ae30-56aff3f6b818)



### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('images.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('natural',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
### OUTPUT

![308426200-762947c3-a5c4-4135-8450-9cd8cedcb063](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/b776b11e-600b-47a0-b106-0775908ebe8a)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('images.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/b328331c-a2f7-4b35-b77d-482552d28fd2)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/0a643231-0519-4217-8e74-6feded114557)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/4b9326dc-1343-418b-8a90-c1d3d51faf2c)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/8533b3bb-a62a-4916-80a8-562bd412a035)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/7b200a5e-f9be-41b3-acc6-3854c7c16d59)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/e816abb7-ca10-4500-9d78-2011ac8d126d)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/5dbb8777-b706-482b-95d7-3edf6b6cd3d4)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/f87fe894-a67a-4769-9160-92e882af48bb)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/ff5f46b2-65ed-466d-878d-c3d9c867221b)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/fc3140a8-edbf-424a-bb42-3d52f7549d0f)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/fd1ac8b2-72f0-4b6b-ab8a-19c0c5e02956)


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('images.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT
![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/7202f7a6-3235-4a40-98fb-cbca61404de6)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/d6e714bc-fec7-4337-8e1f-9bd1331d8cd8)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/ffea9028-43ae-408a-9e51-bf9fd937da78)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/9b4aeb30-e837-447f-a6bd-d2464ba59627)

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("images.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/daebecff-e02d-4660-ab5a-ba6e75a2a9ed)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/10f31d28-a179-4dd3-96f3-75fd2d195c5f)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/0fa5ba4d-10c3-460c-b632-ed823cd840bd)

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/67f81c4a-2190-4026-a284-248b566e23a6)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







