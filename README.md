# EXP-1-Image-Handling-and-Pixel-Transformations-Using-OpenCV
# AIM:
Write a Python program using OpenCV that performs the following tasks:

Read and Display an Image.
Adjust the brightness of an image.
Modify the image contrast.
Generate a third image using bitwise operations.
Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)
# Algorithm:
Step 1:
Load an image from your local directory and display it.

Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.
Display the original, brighter, and darker images.

Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).
Display the original, lower contrast, and higher contrast images.

Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

# Program Developed By:
**Name:**HARISH M

Register Number: 212224110021

# Ex. No. 01
1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```PY
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('fly.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis') 
plt.title("Original Image")
plt.axis('off')  
plt.show()
2. Print the image width, height & Channel.
image = cv2.imread('fly.png')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
3. Display the image using matplotlib imshow().
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 10)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
4. Save the image as a PNG file using OpenCV imwrite().
image = cv2.imread('fly.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
5. Read the saved image above as a color image using cv2.cvtColor().
circle_img = cv2.circle(img_rgb,(100,150),100,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
6. Display the Colour image using matplotlib imshow() & Print the image width, height & channel.
image = cv2.imread('fly.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "OpenCV Drawing butterfly", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10) 
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
7. Crop the image to extract any specific (Eagle alone) object from the image.
image = cv2.imread('fly.png')
mage_rgb = cv2.cvtCoilor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
8. Resize the image up by a factor of 2x.
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
9. Flip the cropped/resized image horizontally.
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
10. Read in the image ('Apollo-11-launch.jpg').
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
11. Add the following text to the dark area at the bottom of the image (centered on the image):
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
12. Draw a magenta rectangle that encompasses the launch tower and the rocket.
image[100:300, 100:300] = [255, 255, 255] 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
13. Display the final annotated image.
image = cv2.imread('fly.png')
image.shape
14. Read the image ('Boy.jpg').
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
15. Adjust the brightness of the image.
image = cv2.imread('fly.png') 
image.shape
roi = image[50:250, 50:250]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
16. Create brighter and darker images.
img_brighter = cv2.add(img, matrix)
img_darker = cv2.subtract(img, matrix)
# YOUR CODE HERE
17. Display the images (Original Image, Darker Image, Brighter Image).
image = cv2.imread('fly.png') 
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
18. Modify the image contrast.
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
# Output:
<img width="525" height="513" alt="image" src="https://github.com/user-attachments/assets/1bdd9114-0ea0-4477-8090-b982c130ced0" />
<img width="521" height="512" alt="image" src="https://github.com/user-attachments/assets/6edf4a76-2cee-48b1-a432-fdada132576b" />
<img width="520" height="510" alt="image" src="https://github.com/user-attachments/assets/7a68f71e-158b-4a6b-9491-bc90c2282e73" />
<img width="516" height="507" alt="image" src="https://github.com/user-attachments/assets/a262608c-8008-4bff-8ea3-3ad2fc75ef42" />
<img width="607" height="552" alt="image" src="https://github.com/user-attachments/assets/307c3f9f-fa70-4fad-8661-8e63427a3531" />
<img width="640" height="535" alt="image" src="https://github.com/user-attachments/assets/71e50af0-957f-48a4-bbbb-5f463c9a974d" />
<img width="641" height="535" alt="image" src="https://github.com/user-attachments/assets/f3fa87d4-684b-43bd-ad9a-bdfd881928b8" />
<img width="585" height="527" alt="image" src="https://github.com/user-attachments/assets/e0711423-4300-4c7c-a674-8d343b90f8c8" />
<img width="518" height="507" alt="image" src="https://github.com/user-attachments/assets/9045e968-28d6-4fcd-b433-87378adc450f" />
<img width="520" height="512" alt="image" src="https://github.com/user-attachments/assets/4dfccaad-7672-4d62-aeae-555378acbd2f" />
<img width="517" height="506" alt="image" src="https://github.com/user-attachments/assets/24fae04b-4405-40b9-ae6e-3b2b2f379854" />
<img width="608" height="507" alt="image" src="https://github.com/user-attachments/assets/157ed9c2-8148-4fdb-8bf7-213e205855ba" />
<img width="537" height="508" alt="image" src="https://github.com/user-attachments/assets/c311b613-35b4-42d5-b199-0629d928c1ec" />
<img width="515" height="510" alt="image" src="https://github.com/user-attachments/assets/c360571b-251f-47a9-864b-9cdc5cb4f1c0" />
<img width="512" height="491" alt="image" src="https://github.com/user-attachments/assets/a1a9c698-beb0-43b1-8ae7-62c1e604d4a3" />

# Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.
