# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.
<br>
### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.
<br>

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically.

5.Rotation rotates the image by a given angle.
<br>

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.
<br>

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.
<br>

## Program:
Developed By: YUVARAM . S <br>
Register Number: 212224230315
```
i)Image Translation

rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')

ii) Image Scaling

scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)  # Scale by 1.5x
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')

iii)Image shearing

M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')

iv)Image Reflection

reflected_image = cv2.flip(image_rgb, 1)  # Horizontal reflection (flip along y-axis)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')

v)Image Rotation

M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')

vi)Image Cropping

cropped_image = image_rgb[50:300, 100:400]  # Crop a portion of the image
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```
## Output:
### i)Image Translation
<br>
<br>![image](https://github.com/user-attachments/assets/2b7354e1-7ce2-487c-a46d-d6c0a6116306)

<br>
<br>

### ii) Image Scaling
<br>
<br>![image](https://github.com/user-attachments/assets/b6722d61-1603-4aef-917f-bbd5697b0f84)

<br>
<br>


### iii)Image shearing
<br>
<br>![lion-3](https://github.com/user-attachments/assets/304fdd3b-cae4-4eb3-b034-096fc0b07a78)

<br>
<br>


### iv)Image Reflection
<br>
<br>
<br>![lion-4](https://github.com/user-attachments/assets/3665aa1e-4824-4a19-8014-2336c92c5885)

<br>



### v)Image Rotation
<br>
<br>![lion-5](https://github.com/user-attachments/assets/2f58fec5-0a80-4dfc-91c0-3d7617eda77c)

<br>
<br>



### vi)Image Cropping
<br>
<br>
<br>![lion-6](https://github.com/user-attachments/assets/2d2ae2cf-6227-47ac-8402-8ef2f38c1107)

<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
