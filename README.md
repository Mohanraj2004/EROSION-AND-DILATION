##  EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>


### Step2:
Create the text image using cv2.putText.
<br>

### Step3:
Then create the structuring image for dilation/erosion.
<br>

### Step4:
Apply erosion and dilation using plt.erode and plt.dilate.
<br>

### Step5:
Plot the images using plt.imshow.
<br>

 
## Program:


# Import the necessary packages:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```



# Create the Text using cv2.putText:
```
image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"JEEVAGOWTHAM S",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```



# Create the structuring element:
```
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```



# Erode the image:
```
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
```




# Dilate the image:
```
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```





## Output:

### Display the input Image:
![Screenshot 2023-10-14 225841](https://github.com/Mohanraj2004/EROSION-AND-DILATION/assets/132890483/a47b933f-89db-4f26-877e-9ee62bd77e00)



<br>
<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image:
![Screenshot 2023-10-14 225936](https://github.com/Mohanraj2004/EROSION-AND-DILATION/assets/132890483/95620306-2b71-42a2-ab11-41f4969e2299)

<br>
<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image:


![Screenshot 2023-10-14 230020](https://github.com/Mohanraj2004/EROSION-AND-DILATION/assets/132890483/9b7080a8-2aba-42f6-8836-5aafd7dd3a67)

<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
