#  YOLOv3-Object-Detection

##  Project Description

This project was completed during my **Data Science Internship at ITGust Sousse (June 2022 – July 2022)**. I worked with a pre-trained **YOLOv3 (You Only Look Once v3)** object detection model and applied it to various datasets for testing and analysis. The project also involved evaluating, fine-tuning, and implementing **real-time object detection** for images and videos to improve detection accuracy and usability.

## 🛠️ Features

* Utilized a pre-trained **YOLOv3** object detection model
* Applied the model to multiple datasets for object detection tasks
* Implemented **real-time object detection** for:

  * **Static images** using `yolo.py`
  * **Videos and webcam streams** using `yolo_video.py`
* Evaluated model performance using precision, recall, and mAP metrics
* Expand training with custom-labeled datasets

## 📚 Tools & Technologies Used

* **YOLOv3** (Darknet framework & pre-trained weights)
* **OpenCV**: for image processing, visualization, and real-time video feed
* **TensorFlow/Keras**: for additional fine-tuning steps
* **Python**: primary programming language

## ⚙️ Installation & Execution

1. **Clone YOLOv3 repository and set up environment**

   ```bash
   git clone https://github.com/nadammar/YOLOv3-Object-Detection.git
   cd YOLOv3-Object-Detection
   make
   ```

2. **Download pre-trained YOLOv3 weights and COCO class labels**

   ```bash
   wget https://pjreddie.com/media/files/yolov3.weights
   wget https://pjreddie.com/media/files/coco.names
   ```

3. **Run detection on a static image** using `yolo.py`

   ```bash
   python yolo.py --image images/<nom d'image>.jpg --yolo yolo-coco
   ```

   * `--image`: path to the input image
   * `--yolo`: base path to YOLO directory containing `yolov3.cfg`, `yolov3.weights`, and `coco.names`
   * `--confidence`: minimum probability to filter weak detections (default: 0.5)
   * `--threshold`: threshold for non-maxima suppression (default: 0.3)

4. **Run real-time object detection (video/webcam)** using `yolo_video.py`

   ```bash
   python yolo_video.py --input videos/<nom de video>.mp4 --output output/<nom de video>.avi --yolo yolo-coco
   ```

   * `--input`: path to the input video file or webcam index (e.g., `0`)
   * `--output`: path where the output video with detections will be saved
   * `--yolo`: base path to YOLO directory containing necessary files
   * `--confidence`: minimum probability to filter weak detections (default: 0.5)
   * `--threshold`: threshold for non-maxima suppression (default: 0.3)

## 📊 Sample Output

* Detected objects visualized with bounding boxes and confidence scores on images and video frames
* Real-time detection feed processed directly from webcam/video stream with detections saved to an output video file
* Performance evaluation metrics: **Precision**, **Recall**, **mAP**


## 👨‍💻 Author

Project developed by **Nada Ammar** during my **Data Science Internship at ITGust Sousse,Tunisia**.
