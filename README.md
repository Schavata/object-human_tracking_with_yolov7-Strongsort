# Object and Human Tracking using YoloV7 and StrongSort
The project implements object tracking using YOLOv7 for detection and StrongSORT for tracking. It processes input from various sources like webcam, files, directories, or URLs. The system performs real-time inference, applies non-maximum suppression, and leverages motion compensation. It offers flexibility with adjustable thresholds and options for saving results.

## Deployment

To deploy this project we need to clone this repository

```bash
git clone https://github.com/Schavata/object-human_tracking_with_yolov7-Strongsort.git
```
To run the code perfectly we need to install requirements.txt file
```bash
pip install -r requirements.txt
```

And also make your pc has python3.12.0 and GPU since tracker need high computation


## Instructions for Testing or to run the file
change the source to test the different types of inputs.

```bash
python track.py --source 0 --yolo-weights weights/yolov7.pt --strong-sort-weights weights/osnet_x0_25_msmt17.pt --show-vid
                           img.jpg  # image
                           vid.mp4  # video
                           path/  # directory
                           path/*.jpg  # glob
                           'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                           'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```

To improve the detection speed and accuracy change the yoloweights and also yoloversions.

##output image
![ip](https://github.com/Schavata/object-human_tracking_with_yolov7-Strongsort/assets/168991292/c5c4d68d-c0fa-492a-a251-5bf60aa90e71)

## Google Colab Notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RIWsZAMhzEmrB0FEjO-iH4kIF0nZZ1Xw?usp=sharing)

## Key Features

- **Object Detection and Tracking:** Integration of YOLOv7 for object detection and StrongSORT for object tracking enables robust real-time tracking of objects.
  
- **Flexible Input Handling:** Supports various input sources including webcams, files, directories, and URLs, making it adaptable to different use cases and environments.
  
- **Customizable Parameters:** Users can adjust parameters such as confidence threshold, NMS threshold, and maximum detections per image, enabling fine-tuning for specific tracking scenarios.
  
- **Efficient Processing:** Optimizes processing by applying non-maximum suppression, motion compensation, and real-time inference, ensuring high-performance tracking capabilities.

## Model Conversions with `track.py`

To convert the YOLOv7 and StrongSORT models to different formats for use with the `track.py` script, follow these steps:

1. **YOLOv7 Model Conversion:**
   - Use the provided `export.py` script in the YOLOv7 repository to convert the YOLOv7 model to ONNX format.

2. **StrongSORT Model Conversion:**
   - Convert the StrongSORT model to the desired format compatible with the `track.py` script.

For detailed instructions and examples, refer to the respective documentation of YOLOv7 and StrongSORT repositories.

### Output
The code will generate tracked object results in the output directory.
## Results

### Tracking Video
[![Tracking Video](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)

Click the image to watch the tracking video.


### Troubleshooting
- If you encounter CUDA-related errors, ensure that CUDA and cuDNN are properly installed and configured.
- Make sure to specify the correct paths to the pre-trained models and input data.

### Example
For example, to track objects in a video file `input.mp4`, run:python track.py --source input.mp4 --yolo-weights weights/yolov7.pt --strong-sort-weights weights/osnet_x0_25_msmt17.pt

## Integrating `track.py` into Your Application

1. **Setup Environment**:
   - Ensure Python is installed.
   - Install dependencies using `pip install -r requirements.txt`.

2. **Download Pre-trained Models**:
   - Obtain pre-trained YOLO and StrongSORT weights.
   - Place weights in designated directories or specify paths in your app.

3. **Input Data**:
   - Decide input type: live video, recorded video, or image frames.

4. **Processing**:
   - Utilize `track.py` functions for object detection and tracking.

5. **Display Results**:
   - Visualize tracking outcomes, e.g., bounding boxes, object IDs.

6. **User Interface** (Optional):
   - Consider adding a GUI using libraries like Tkinter or PyQt.

7. **Testing and Deployment**:
   - Thoroughly test your app before deployment or distribution.
  












