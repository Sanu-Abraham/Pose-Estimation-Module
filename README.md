# Pose Estimation Module using Mediapipe

This module provides a Python implementation of pose estimation using the Mediapipe library and OpenCV. It enables the estimation of human poses in images or video streams, allowing for applications such as fitness tracking, motion analysis, and more.

## Dependencies

The following dependencies are required to use the module:

- OpenCV
- Mediapipe

You can install these dependencies using pip:

```shell
pip install opencv-python mediapipe
```

## Usage

To use the Pose Estimation module, import it in your Python code:

```python
from pose_estimation import PoseEstimator
```

Then, create an instance of the `PoseEstimator` class with your desired configuration:

```python
estimator = PoseEstimator(mode=False, upperBodyOnly=False, smoothLandmarks=True, detectConf=0.5, trackConf=0.5)
```

You can adjust the parameters according to your specific requirements. Once the `PoseEstimator` object is created, you can call its methods to estimate poses in images or video frames.

For example, to estimate poses in a single image:

```python
import cv2

image = cv2.imread("image.jpg")
estimated_image = estimator.estimatePose(image)
pose_landmarks = estimator.getPosition(image)
# Process the estimated image and pose landmarks as needed
```

Refer to the script for more details and examples on how to use the `PoseEstimator` class.

## License

This module is licensed under the [MIT License](LICENSE).

## Acknowledgements

The pose estimation functionality in this module is based on the Mediapipe library, which provides the pose estimation model used for estimating human poses.
