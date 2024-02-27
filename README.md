![307217437-701c00d5-76d0-4a10-a74f-0ba58420a05a](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/445279eb-78bc-4479-93c4-ade81ddb5f9d)# COLOR_CONVERSIONS_OF-IMAGE
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
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image

    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

### OUTPUT

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/46b97dc0-2f8d-4dde-9e61-0be6bf5fcab7)


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

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/29a58fd7-6d7f-4ffb-82d6-ef3fcefe62b3)


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

![image](https://github.com/Sangavi-suresh/COLOR_CONVERSIONS_OF-IMAGE/assets/118541861/1c8bdacc-990d-4ddf-adfa-abd950bad17a)

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





### viii) RGB and BGR to YCrCb
<br>
<br>

### ix) Split and merge RGB Image
<br>
<br>

### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







