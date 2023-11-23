import cv2
import numpy as np

def create_white_image_with_circle():
    # Get size of the image from the user
    width = int(input("Enter the width of the image: "))
    height = int(input("Enter the height of the image: "))

    # Create a white image of the specified size
    img = np.ones((height, width, 3), np.uint8) * 255

    # Draw a circle on the image
    center_coordinates = (width // 2, height // 2)  # Center of the image
    radius = min(width, height) // 4  # Radius of the circle
    color = (0, 0, 0)  # BGR color format (blue, green, red)
    thickness = 2  # Thickness of the circle outline

    cv2.circle(img, center_coordinates, radius, color, thickness)

    # Display the image
    cv2.imshow("White Image with Circle", img)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Call the function to create the white image with a circle
create_white_image_with_circle()
