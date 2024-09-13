
# Video Person Detection

This project demonstrates how to detect people in a video using the YOLO (You Only Look Once) object detection model with OpenCV in Python. The code processes each frame of the video to identify and highlight people with bounding boxes.

## Requirements

- Python 3.x
- OpenCV

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Dev-wael1/video-person-detection.git
   cd video-person-detection
   ```

2. **Install Dependencies**

   Install the required Python libraries using pip:

   ```bash
   pip install opencv-python opencv-python-headless
   ```

3. **Download YOLO Files**

   Download the YOLOv3 weights and configuration files from the [YOLO website](https://pjreddie.com/darknet/yolo/). Place these files in the project directory:

   - `yolov3.weights`
   - `yolov3.cfg`

   You may also need the `coco.names` file which contains the class labels. You can download it from [here](https://github.com/pjreddie/darknet/blob/master/data/coco.names).

## Usage

1. **Prepare Your Video**

   Place your video file in the project directory and rename it to `video.mp4`, or update the script to use your video's filename.

2. **Run the Detection Script**

   Execute the Python script to start processing the video:

   ```bash
   python detect_people.py
   ```

   The script will open a window displaying the video with detected people highlighted. Press `q` to exit the video window.

## Code Overview

- **Loading YOLO**: The script loads the YOLO model using pre-trained weights and configuration files.
- **Processing Video**: It reads frames from the video, applies YOLO object detection, and draws bounding boxes around detected people.
- **Non-max Suppression**: Reduces overlapping bounding boxes to ensure each detected person is only marked once.

## Troubleshooting

- Ensure that all required files (`yolov3.weights`, `yolov3.cfg`, `coco.names`, and the video file) are in the correct directory.
- Adjust the confidence threshold and non-max suppression parameters in the script as needed for better results.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- YOLO: https://pjreddie.com/darknet/yolo/
- OpenCV: https://opencv.org/
```
