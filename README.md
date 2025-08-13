# Multi-Image Real-Time Face Recognition

A Python-based real-time face recognition system that allows training each person with multiple images for improved accuracy.  
Built with [face_recognition](https://github.com/ageitgey/face_recognition) and OpenCV.

## Features

- Capture multiple training images per person via webcam.
- Automatically save encodings per person in separate folders.
- Real-time face detection and recognition.
- Adjustable tolerance threshold for recognition accuracy.
- Optional performance optimizations (frame scaling, skipping, HOG model).
- Easy-to-manage dataset structure:

## Structure
training_faces/
John/
john_1.jpg
john_2.jpg
Sarah/
sarah_1.jpg
sarah_2.jpg

encodings/
John/
john_1.npy
john_2.npy
Sarah/
sarah_1.npy
sarah_2.npy


## Requirements

- Python 3.7+
- [face_recognition](https://github.com/ageitgey/face_recognition)
- OpenCV (`cv2`)
- NumPy

Install dependencies:

pip install face_recognition opencv-python numpy


## Usage

1. Capture Images
***python main.py***

- Press c to capture a frame.
- Press r to restart capture for a new person.
- Press q to quit.

2. Process and Save Encodings

***process_and_save_encodings_per_person()***

3. Run Real-Time Recognition

***start_recognition()***

## Performance Tips
- Use model="hog" for faster detection on CPU.

- Downscale frames before processing (scale_factor = 0.25).

- Skip every other frame for smoother performance.
