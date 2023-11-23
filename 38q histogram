import cv2
import matplotlib.pyplot as plt

def analyze_histogram(input_image):
    # Convert the input image to grayscale
    gray_image = cv2.cvtColor(input_image, cv2.COLOR_BGR2GRAY)

    # Calculate the histogram using OpenCV
    hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

    # Plot the histogram
    plt.hist(hist, bins="auto")
    plt.xlabel("Pixel Intensity")
    plt.ylabel("Number of Pixels")
    plt.title("Histogram of Image")

    # Show the plot
    plt.show()

# Read the input image
input_image = cv2.imread("cv.png")

# Call the function to analyze the histogram of the input image
analyze_histogram(input_image)
