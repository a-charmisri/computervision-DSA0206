import cv2

# Load the pre-trained Haar cascade for face detection
face_cascade = cv2.CascadeClassifier("C:/Users/ameer/Desktop/Computer Vision/haarcascade_frontalface_default.xml")

# Load the pre-trained Haar cascade for eye detection
eye_cascade = cv2.CascadeClassifier("C:/Users/ameer/Desktop/Computer Vision/haarcascade_eye.xml")

# Read the input image
img = cv2.imread("eye.jpeg")

# Convert the image to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Detect faces in the input image
faces = face_cascade.detectMultiScale(gray, 1.3, 5)

# Iterate through the detected faces and detect eyes within the face boundaries
for (x, y, w, h) in faces:
    roi_gray = gray[y:y+h, x:x+w]
    roi_color = img[y:y+h, x:x+w]

    # Detect eyes within the face area
    eyes = eye_cascade.detectMultiScale(roi_gray)

    # Draw rectangles around the detected eyes
    for (ex, ey, ew, eh) in eyes:
        cv2.rectangle(roi_color, (ex, ey), (ex+ew, ey+eh), (0, 255, 0), 2)

# Display the image with detected eyes
cv2.imshow('Detected Eyes', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
