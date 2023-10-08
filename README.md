
# Great Barrier Reef Object Detection Model

Australia's stunningly beautiful Great Barrier Reef is the world’s largest coral reef and home to 1,500 species of fish, 400 species of corals, 130 species of sharks, rays, and a massive variety of other sea life.

Unfortunately, the reef is under threat, in part because of the overpopulation of one particular starfish – the coral-eating crown-of-thorns starfish (or COTS for short). Scientists, tourism operators and reef managers established a large-scale intervention program to control COTS outbreaks to ecologically sustainable levels, since COTS starfish are threatening Australia's Great Barrier Reef.

The object detection model will help researcher identify starfish in real-time and take well-informed action to protect the reef for future generations.
Underwater videos of coral reefs are used to train the model.

## Features

This model is trained using Yolov8 in order predict the presence and position of crown-of-thorns starfish in sequences of underwater images taken at various times and locations around the Great Barrier Reef. Predictions take the form of a bounding box together with a confidence score for each identified starfish. An image may contain zero or more starfish.

![image](https://github.com/jasmindc/object-detection-project/assets/67323439/f098ddba-6e4c-4f8e-bdd0-355e5ac7c12c)


## Installing

Code can be downloaded and it is ready to be run in different environments paying attention to used paths.

### Initial Configuration

Before running the model, make sure to download and upload input data from here (15 GB size) : https://www.kaggle.com/competitions/tensorflow-great-barrier-reef/data

Input used:

train/ - Folder containing training set photos of the form video_{video_id}/{video_frame_number}.jpg.

[train/test].csv - Metadata for the images. test.csv is not aviable.

train.csv fields:
  * video_id - ID number of the video the image was part of. The video ids are not meaningfully ordered.
  * video_frame - The frame number of the image within the video. Expect to see occasional gaps in the frame number from when the diver surfaced.
  * sequence - ID of a gap-free subset of a given video. The sequence ids are not meaningfully ordered.
  * sequence_frame - The frame number within a given sequence.
  * image_id - ID code for the image, in the format '{video_id}-{video_frame}'
  * annotations - The bounding boxes of any starfish detections in a string format that can be evaluated directly with Python. A bounding box is described by the pixel coordinate (x_min, y_min) of its upper left corner within the image together with its width and height in pixels.



## Developing

The model is not ready to deploy, here some further steps that can be taken:
* evaulation on actual test set (not available on Kaggle challange)
* develop user interface 


## Links
* to see code with outputs visit (Kaggle model code): https://www.kaggle.com/code/jasmindc/great-barrier-reef-object-detection?scriptVersionId=145616380
* Kaggle source for the challange: https://www.kaggle.com/competitions/tensorflow-great-barrier-reef/overview
* Yolov8 information: https://docs.ultralytics.com/


