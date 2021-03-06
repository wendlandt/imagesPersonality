# Texture Module

This module calculates the gray-level cooccurence matrix (GLCM) for each image
and calculates texture features based off of that. To better understand how the
GLCM works, refer to the helpful tutorial at
http://www.fp.ucalgary.ca/mhallbey/tutorial.htm.

## Contents
- **textureFeatures.py**: script that takes either an image (or a directory path)
	and outputs a CSV file containing texture metrics

## Dependencies
- Python's numpy library (http://www.numpy.org/)
- Python's scikit-image library (http://scikit-image.org/)
- Python Image Library (http://www.pythonware.com/products/pil/)

## Quick Start
In bash:
```
$ python textureFeatures.py someDirectory/myImage.jpg
$ python textureFeatures.py someDirectory
```

The textureFeatures script takes one argument, either the full path of a single
image or the path to a directory containing only images.

## Output
Results will be stored in features_texture.csv, which has the following headers:
file, contrast, correlation, energy, homogeneity

	file - name of file without extension (or path)
	contrast - the contrast metric for the image
	correlation - the correlation metric for the image
	energy - the energy metric for the image
	homogeneity - the homogeneity metric for the image

## Timing
3m,22s for approximately 7765 images
