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

##output videos
![ip](https://github.com/Schavata/object-human_tracking_with_yolov7-Strongsort/assets/168991292/c5c4d68d-c0fa-492a-a251-5bf60aa90e71)

## Google Colab Notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RIWsZAMhzEmrB0FEjO-iH4kIF0nZZ1Xw?usp=sharing)




