import cv2
import numpy as np

def create_image_with_boxes(size):
    # Create a white image of the specified size
    white_image = np.full((size, size, 3), 255, dtype=np.uint8)

    # Calculate the size of the colored boxes
    box_size = size // 10

    # Create black, blue, green, and red boxes on each corner of the image
    white_image[0:box_size, 0:box_size] = [0, 0, 0]  # Black box in the top-left corner
    white_image[0:box_size, size - box_size:size] = [255, 0, 0]  # Blue box in the top-right corner
    white_image[size - box_size:size, 0:box_size] = [0, 255, 0]  # Green box in the bottom-left corner
    white_image[size - box_size:size, size - box_size:size] = [0, 0, 255]  # Red box in the bottom-right corner

    # Display the image
    cv2.imshow('Image with Boxes', white_image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Call the function with the desired size (e.g., 400)
create_image_with_boxes(400)
