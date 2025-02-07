# Motion Detection with OpenCV

This project implements a motion detection system using **OpenCV** and **Python**. The program captures video from a webcam, processes the frames to detect motion, and logs the timestamps when motion is detected.

## Features
- Captures live video using OpenCV
- Detects motion using frame differencing and contour detection
- Saves timestamps of motion events to a CSV file
- Displays processed frames in real-time

## Technologies Used
- Python 3
- OpenCV
- Pandas
- NumPy (optional, but recommended for performance optimization)

## Installation

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/yourusername/motion-detection-opencv.git
   cd motion-detection-opencv
   ```
2. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

## Usage

Run the script to start motion detection:
```sh
python motion_detector.py
```

### Controls
- **Press 'q'** to quit the program.

## How It Works
1. The program initializes the webcam and captures the first frame.
2. Each new frame is converted to grayscale and blurred to reduce noise.
3. The difference between the first frame and the current frame is computed.
4. A threshold is applied to highlight moving objects.
5. Contours are detected, and if an object is large enough, it is considered motion.
6. Timestamps of motion events are recorded and saved in `Times.csv`.

## Output
The program generates a CSV file (`Times.csv`) with the timestamps of detected motion:

| Start Time | End Time |
|------------|---------|
| 2025-02-07 10:15:30 | 2025-02-07 10:15:45 |
| 2025-02-07 10:20:12 | 2025-02-07 10:20:25 |

## Potential Improvements
- Implement email or SMS notifications when motion is detected
- Save recorded video clips of motion events
- Improve accuracy with background subtraction methods

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to contribute and improve this project!

