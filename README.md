# CS6220-group-3-class-project
Adapted from https://colab.research.google.com/drive/1vLDuyInQF1_liK5B57KktAaXqKZd9h5Q?usp=sharing

From sanmesh: https://docs.google.com/document/d/1SoxOGzWRvyrBa-HIDbG5a58zAIBUguxS/edit 

## Overview

Runs age detection on faces within a given image. Once a face has been classified, a number of different saliency maps are computed for each face and saved locally. 

The saliency maps are generated by computing the pixel gradients of the input with respect to the probability that the face is a certain age range. These gradients are then transformed vis transformation functions defined in saliency.py. 

## How to run 

One can install the requirements in requirements.txt by running `python -m pip -r requirements.txt`

Put input images in ./input folder 

Run  `python saliency.py`

See output in ./output

Output is formatted like so:

```
./output
    ->Images
    -> Predicted Image
    -> faces (one folder for each face)
        -> greyscale face
        -> transformations
            -> predicted age range saliency map
            -> other age range saliency maps
```

