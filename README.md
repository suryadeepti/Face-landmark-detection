# Face-landmark-detection
Detect all landmarks of face like Eyes, Nose, Lips, Eyebrows.
Facial landmarks are used to localize and represent salient regions of the face, such as:
  Eyes
  Eyebrows
  Nose
  Mouth
  Jawline

Detecting facial landmarks is a subset of the shape prediction problem. Given an input image (and normally an ROI that specifies the object of interest), a shape predictor attempts to localize key points of interest along the shape.

In the context of facial landmarks, our goal is detect important facial structures on the face using shape prediction methods.

Detecting facial landmarks is therefore a two step process:

Step 1: Localize the face in the image.
Step 2: Detect the key facial structures on the face ROI.

We apply a pre-trained HOG + Linear SVM object detector specifically for the task of face detection.


Detecting facial landmarks in an image is a two step process:

First we must localize a face(s) in an image. This can be accomplished using a number of different techniques, but normally involve either Haar cascades or HOG + Linear SVM detectors (but any approach that produces a bounding box around the face will suffice).
Apply the shape predictor, specifically a facial landmark detector, to obtain the (x, y)-coordinates of the face regions in the face ROI.
Given these facial landmarks we can apply a number of computer vision techniques, including:

Face part extraction (i.e., nose, eyes, mouth, jawline, etc.)
Facial alignment
Head pose estimation
Face swapping
Blink detection
…and much more!
In next week’s blog post I’ll be demonstrating how to access each of the face parts individually and extract the eyes, eyebrows, nose, mouth, and jawline features simply by using a bit of NumPy array slicing magic.
