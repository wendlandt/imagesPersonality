# Preprocessing Module

This module iterates through a directory, finds all of the images (the files starting with "file"), removes all of the non-images, and converts all of the images to 700x700 (necessary for face detection).

## Contents
- **preprocess.sh**: a script to preprocess all of the images in the dataset

## Dependencies
- ImageMagick (http://www.imagemagick.org/)

## Quick Start
Before using this, first make a copy of all of the original data and put it in a new folder (ie. data_preprocessed). This script will change that directory.

The directory must be organized as followed: each user has a separate folder in the directory, and in that user folder are all of the images for that user. The images are named file0 through file4.

Before running, open up preprocess.sh and make sure that the path is set correctly.

Then, in bash:	
```
$ ./preprocess.sh
```

## Output
This module will change the images inplace (it will not make a copy of them first).

## Timing
56m,49s for approximately 7765 images
