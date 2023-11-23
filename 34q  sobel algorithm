import cv2
import numpy as np

def sobel_edge_detection(input_image):
    # Convert the input image to grayscale
    img_gray = cv2.cvtColor(input_image, cv2.COLOR_BGR2GRAY)

    # Apply Gaussian blur to reduce noise
    img_blur = cv2.GaussianBlur(img_gray, (3, 3), 0)

    # Apply Sobel edge detection in the x and y directions
    sobelx = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=0, ksize=5)
    sobely = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=0, dy=1, ksize=5)

    # Combine the x and y edge images
    sobelxy = cv2.addWeighted(sobelx, 0.5, sobely, 0.5, 0)

    # Display the original, Sobel X, Sobel Y, and combined Sobel images
    cv2.imshow('Original', input_image)
    cv2.imshow('Sobel X', sobelx)
    cv2.imshow('Sobel Y', sobely)
    cv2.imshow('Sobel X Y using Sobel() function', sobelxy)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Read the input image
input_image = cv2.imread("cv.png")

# Call the function to perform Sobel edge detection
sobel_edge_detection(input_image)
