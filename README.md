
**Project Overview:**
This project demonstrates how to recognize human actions from a video using pose estimation techniques and OpenCV. The code processes a video, identifies human poses, and recognizes actions based on specific landmarks.

**Steps to Recreate the Project:**

1. **Import Libraries:**
   - Import the required libraries: `cv2`, `mediapipe`, and `numpy`.

2. **Initialize Pose Estimation:**
   - Initialize MediaPipe Pose model for pose estimation.
   - Set confidence thresholds for detection and tracking.

3. **Capture Video:**
   - Open the video file using `cv2.VideoCapture`.
   - Get frame dimensions using `get()` function.

4. **Create Video Writer:**
   - Create an output video writer using `cv2.VideoWriter`.
   - Specify codec, frame rate, and frame dimensions.

5. **Process Frames for Pose Estimation:**
   - Loop through video frames using `cap.isOpened()`.
   - Read each frame using `cap.read()`.

6. **Convert Color Format:**
   - Convert BGR frame to RGB using `cv2.cvtColor()`.

7. **Estimate Poses and Draw Landmarks:**
   - Process the frame with the Pose model using `pose.process()`.
   - Extract pose landmarks using `results.pose_landmarks`.
   - Draw bounding boxes around detected poses and pose keypoints using OpenCV functions.

9. **Recognize Actions:**
   - Define a dictionary of action classes and associated landmarks.
   - Iterate through actions and check if all required keypoints are visible.
   - If visible, store the detected actions.

10. **Annotate Frame with Detected Actions:**
   - Display detected actions on the video frame using `cv2.putText()`.

11. **Write Processed Frame to Output Video:**
    - Write the annotated frame to the output video using `out.write()`.

12. **Release Resources:**
    - Release the video capture and writer objects using `release()`.

13. **Process Output Video:**
    - Open the processed output video using `cv2.VideoCapture`.

14. **Recognize and Annotate Actions in Output Video:**
    - Similar to step 7, recognize actions from the processed output video frames.
    - Annotate the actions on the frames using `cv2.putText()`.

15. **Create Output Video File:**
    - Create an output video file for the annotated output video frames.

16. **Release Resources and Close Windows:**
    - Release the video capture, writer, and window objects using `release()` and `destroyAllWindows()`.

**Conclusion:**
This project demonstrates a step-by-step process for recognizing human actions using pose estimation and OpenCV.Videos can be uploaded and its action can be recognized if its present in the labels and it can also be modified for real time action recognition.
