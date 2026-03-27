# FaceTrack Attendance System

A desktop attendance system built with Python, OpenCV, and Tkinter that uses face recognition to:

- register new users
- train a local recognition model
- mark attendance with date and time
- store attendance in CSV files

## Features

- GUI-based workflow using Tkinter
- Face image capture from webcam
- Local training with LBPH face recognizer
- Daily attendance file generation in CSV format
- Simple password protection for saving training profiles
- Live attendance table shown inside the app

## Tech Stack

- Python 3
- Tkinter for GUI
- OpenCV (opencv-contrib-python) for face detection and recognition
- NumPy, Pandas, Pillow
- CSV and datetime modules for data storage and timestamps

## Project Structure

```text
FaceTrack-Attendance-System/
├── main.py
├── haarcascade_frontalface_default.xml
├── Attendance/
├── StudentDetails/
│   └── StudentDetails.csv
├── TrainingImage/
└── TrainingImageLabel/
		├── psd.txt
		└── Trainner.yml
```

## Requirements

Install dependencies:

```bash
pip install opencv-contrib-python numpy pandas pillow
```

Notes:

- Tkinter is included with most standard Python installations on Windows.
- opencv-contrib-python is required because the project uses the face recognizer API.

## How To Run

1. Clone the repository.
2. Open a terminal in the project folder.
3. Install dependencies.
4. Start the app:

```bash
python main.py
```

## Usage Flow

1. Enter ID and Name.
2. Click Take Images to capture face samples.
3. Click Save Profile to train and save the model.
4. Click Take Attendance to start recognition and mark attendance.
5. Press q in the camera window to stop attendance capture.

## Data Files

- Registered students are stored in StudentDetails/StudentDetails.csv.
- Daily attendance is stored as Attendance/Attendance_DD-MM-YYYY.csv.
- Trained model is stored in TrainingImageLabel/Trainner.yml.

## Troubleshooting

- If the app says face recognizer is missing, install opencv-contrib-python instead of opencv-python.
- If the camera does not open, check webcam permissions and close other apps using the camera.
- If files are reported missing, confirm these exist:
	- haarcascade_frontalface_default.xml
	- TrainingImageLabel/ directory

## License

This project is licensed under the terms of the LICENSE file in this repository.
