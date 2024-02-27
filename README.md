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

### OUTPUT 

![Uploading 307217437-701c00d5-76d0-4a10-a74f-0ba58420a05a.png…]()



### v)Cut and paste portion of image
<br>
<br>

### vi) BGR and RGB to HSV and GRAY
<br>
<br>

### vii) HSV to RGB and BGR
<br>
<br>

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







