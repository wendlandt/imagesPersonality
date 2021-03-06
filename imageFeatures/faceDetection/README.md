# Face Detection Module

This module loads the number of images and counts the number of faces in each image using a CNN.

## Contents
- **faceDetection.py**: script to do face detection
- **detections_count.py**: script to count face detections
- Python 2.7 (doesn't work in Python 3)

## Dependencies
- This module is dependent on the doppia code found at https://bitbucket.org/rodrigob/doppia. Before running any of this code, please make sure that this code base is installed.
- Images can't be too big. Resizing everything to 700x700 (or smaller) works well. To resize, use ImageMagick: convert file.jpg -resize 700x700 file.jpg.

## Quick Start
First check that the paths to the data are set correctly in faceDetection.sh. Also, make sure that $OBJECTS_DETECTION_PATH/output exists and is empty.

Then, in bash:
```
$ ./faceDetection.sh (This will do all the detecting work and save all of the output in /home/wenlaura/local/doppia/src/applications/objects_detection/output. It will also read the results from the output folder and pipe them through the python script counting the faces)
```

## Output
Results will be in a text file located at $OBJECTS_DETECTION_TOOL/results.txt.

## Errors
Note: If you get the error "python: command not found", make sure that the path on line 86 of the faceDetections.h is correct (module load python-anaconda2, then type "which python" to determine the correct path).

Note: Errors might happen during the face detection process. You can find the errors my looking at the output and searching for "Could not find the input file." This error usually happens when a picture fails to exist (it usually isn't a problem).

## References
Mathias, Markus, et al. "Face detection without bells and whistles." Computer Vision–ECCV 2014. Springer International Publishing, 2014. 720-735.
