import cv2

# Load the pre-trained Haar cascade for face detection
face_cascade = cv2.CascadeClassifier("C:/Users/ameer/Desktop/Computer Vision/haarcascade_frontalface_default.xml")

# Read the input image
img = cv2.imread('face.jpeg')

# Convert the image to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Detect faces in the input image
faces = face_cascade.detectMultiScale(gray, 1.3, 5)

# Count the number of detected faces
num_faces = len(faces)

# Draw rectangles around the detected faces
for (x, y, w, h) in faces:
    cv2.rectangle(img, (x, y), (x+w, y+h), (0, 255, 0), 2)

# Display the image with detected faces and the number of faces
cv2.putText(img, f"Number of faces: {num_faces}", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 255), 2)
cv2.imshow('Detected Faces', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
