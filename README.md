# EXPERIMENT 03:COLOR CONVERSION
## AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.
## SOFTWARE REQUIRED:
Anaconda - Python 3.7
## ALGORITHM:
### Step 1:
Import cv2 and save and image as filename.jpg
### Step 2:
Use imread(filename, flags) to read the file.
### Step 3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
### Step 4:
Split and merge the image using cv2.split and cv2.merge commands.
### Step 5:
End the program and close the output image windows.

## PROGRAM:
```
Developed By: RITHIGA SRI.B
Register Number: 212221230083
```

```
#Reading and displaying original image:
import cv2
img=cv2.imread('image.jpg')
#Original image
cv2.imshow('Original Image',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```
# 1.CONVERT BGR AND RGB TO HSV AND GRAY:
#BGR2HSV
hsv_img=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsv_img1=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
gray_img=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
gray_img1=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```
# 2.CONVERT HSV TO RGB AND BGR:
#HSV TO RGB
rgb_img=cv2.cvtColor(hsv_img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV TO RGB',rgb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgr_img=cv2.cvtColor(hsv_img1,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV TO BGR',bgr_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

```
# 3.RGB AND BGR TO YCrCb:
#RGB to YCrCb
YCrCb_img=cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR TO YCrCb
YCrCb_img1=cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```
# 4.Split and merge RGB image:
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()
```

```
# 5.Split and merge HSV image
#Split:
hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
#Merge:
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
```

## OUTPUT:
### Original Image:  
![image](https://user-images.githubusercontent.com/93427256/227719238-b257a4b7-07b6-41e8-91d1-4e8939f5fa20.png)

### BGR and RGB to HSV and GRAY:  
### BGR TO HSV:    
![image](https://user-images.githubusercontent.com/93427256/227719418-7bdc6bf4-fea1-49ab-83f6-141416533241.png)
### RGB TO HSV:      
![image](https://user-images.githubusercontent.com/93427256/227719471-f9b37290-073c-4eb1-9986-33fefff9ee82.png)
### BGR TO GRAY:      
![image](https://user-images.githubusercontent.com/93427256/227719513-5f3548e8-3d3c-4936-81c3-8282dda62523.png)
### RGB TO GRAY:    
![image](https://user-images.githubusercontent.com/93427256/227719540-cba11cc5-207b-490c-bc2c-7eef77b145e0.png)

### HSV to RGB and BGR:  
### HSV TO RGB:    
![image](https://user-images.githubusercontent.com/93427256/227719792-0fe84cd9-3ddf-4035-846f-019e96bd41c4.png)
### HSV TO BGR:    
![image](https://user-images.githubusercontent.com/93427256/227719932-7087cb5e-640c-4022-b9fa-ec78e1f32ca3.png)

### RGB and BGR to YCrCb:  
### RGB TO YCrCb:    
![image](https://user-images.githubusercontent.com/93427256/227720265-320e2eca-a60c-461e-a5f6-a993bc63cce9.png)
### BGR TO YCrCb:    
![image](https://user-images.githubusercontent.com/93427256/227720290-f197dcee-6f5b-4226-8105-fdd258d1fc73.png)

### Split and merge RGB image:    
![image](https://user-images.githubusercontent.com/93427256/227720501-1ddd662a-e945-4816-94b2-c81a870c90d4.png)

### Split and merge HSV image:    
![image](https://user-images.githubusercontent.com/93427256/227720782-d8aa233a-091e-4e3b-afe9-2ad7d8be9816.png)


## RESULT:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
