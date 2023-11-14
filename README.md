# Image-Acquisition-from-Web-Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
<br>
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
 Import the cv2 and numpy package.
<br>

### Step 2:
Read the Video frame using the cv2.VideoCapture(0)
<br>

### Step 3:
Write the image using imwrite().
<br>

### Step 4:
Display the frame using the imshow().
<br>

### Step 5:
Divide the frame into halves and assign the smaller frame
<br>
### Step 6:
Rotate the frame using the cv2.rotate().
<br>

## Program:

### Developed By: SASIDEVI V
### Register No: 212222230136

## i) Write the frame as JPG file
``` Python
import cv2
obj = cv2.VideoCapture(0)
while(True):
    cap,frame = obj.read()
    cv2.imshow('video.jpg',frame)
    cv2.imwrite("purse.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
obj.release()
```
## ii) Display the video
``` Python
import cv2
img = cv2.VideoCapture(0)
while(True):
    imagee,frame = img.read()
    cv2.imshow('SASIDEVI 212222230136',frame)
    cv2.imwrite("NewPicture.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
img.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
``` Python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('SASIDEVI 212222230136',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
``` Python
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2] = smaller_frame 
    image[:height//2, width//2:] = smaller_frame
    image[height//2:, width//2:] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    cv2.imshow('SASIDEVI 212222230136', image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
## Output

### i) Write the frame as JPG image

![image](https://github.com/SASIDEVIvenaram/Image-Acquisition-from-Web-Cameraa/assets/118707332/56716fbe-1bd0-4e94-b8e0-1957341ab2a0)




### ii) Display the video

![image](https://github.com/SASIDEVIvenaram/Image-Acquisition-from-Web-Cameraa/assets/118707332/aed89225-b0d2-466b-b609-689b1114e219)



### iii) Display the video by resizing the window


![image](https://github.com/SASIDEVIvenaram/Image-Acquisition-from-Web-Cameraa/assets/118707332/6e4d1678-a9a8-4b96-a624-a1355b2c4236)




### iv) Rotate and display the video

![image](https://github.com/SASIDEVIvenaram/Image-Acquisition-from-Web-Cameraa/assets/118707332/fa626521-2ab5-4e30-bf9d-31bc2327cc82)





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
