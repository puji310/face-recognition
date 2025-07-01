# 🎭 Face Recognition

Recognize and manipulate faces from Python or the command line with the world's simplest face recognition library.

Built using [dlib](http://dlib.net/)'s state-of-the-art face recognition technology with deep learning. The model achieves **99.38% accuracy** on the [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/) benchmark.

This library also provides a `face_recognition` command-line tool for performing face recognition tasks directly from a folder of images.

---

## 🚀 Features

- 📍 **Find faces** in pictures
- 👁 **Locate facial features** (eyes, nose, mouth, chin)
- 🧠 **Identify known faces** in new images
- 📷 **Real-time face recognition** with a webcam
- 🎨 Perform fun tasks like **digital makeup**
- 💻 Use from both **Python scripts** and the **command line**

---

## 📌 Example Use Cases

- **Security systems**: Identify and authenticate individuals from images or video feeds.
- **Photo tagging**: Automatically tag friends in pictures.
- **Robotics and IoT**: Detect and respond to known faces.
- **Interactive art projects**: Manipulate faces for creative effects.
- **Web applications**: Build facial login or profile recognition features.

---

## 💻 Sample Code

```python
import face_recognition

# Load known and unknown images
known_image = face_recognition.load_image_file("known.jpg")
unknown_image = face_recognition.load_image_file("unknown.jpg")

# Encode faces
known_encoding = face_recognition.face_encodings(known_image)[0]
unknown_encoding = face_recognition.face_encodings(unknown_image)[0]

# Compare faces
results = face_recognition.compare_faces([known_encoding], unknown_encoding)

if results[0]:
    print("Face matched!")
else:
    print("No match.")
