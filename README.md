VideoDeepFakeDetection

Application that detects the originality of video files with artificial intelligence.

## Setup Environment

```bash
# Make sure your PIP is up to date
pip install -U pip wheel setuptools

# Install required dependencies
pip install -r requirements.txt
```

## Application

- You can run the file named [main.py](main.py).
- Running on http://127.0.0.1:5000


![295173513-fd979490-00d4-4172-a850-d0a4b6e4ba76](https://github.com/infernotlc/Video-DeepFake-Detection/assets/70065773/a387dcc1-362f-4e31-92cc-da2c1e5e1a89)


- Load your video(.mp4) file and test whether the file is real or not.



![295174687-a085bb6d-19fe-4631-a5b0-344c46cf876f](https://github.com/infernotlc/Video-DeepFake-Detection/assets/70065773/3d2f85e4-4945-4e06-853d-8fa943ec5fea)


## Overview

1- The video file is opened, and various video properties such as fps, width, and height are obtained.

2- Face detection is performed using **MTCNN (Multi-Task Cascaded Convolutional Networks)**.

3- The detected face is transformed into a feature vector using a pre-trained **Inception Resnet V1 model (InceptionResnetV1)**.

4- A comparison is made with the face in the previous frame, and a similarity score is calculated.

5- Similarity scores below a certain threshold are considered as indicative of a deepfake.

6- If deepfakes are detected in a consecutive number of frames, it is marked as a deepfake, and a frame is added to the video.

7- Processed frames are written to an output video file.



## License

Our project is licensed under the [MIT License](LICENSE).
