# Computing Images to Display on OLED and SLM

This folder demonstrates the computation needed for 1 static 3D scene for Split-Lohmann Display.

The inputs to the pipeline are two images, one RGB image in uint8, and a grayscale depth map image in uint8.

The outputs to the two displays are three images, the warpped RGB image in uint8, the warpped depth image in uint8, and the warpped and computed phase mask image in uint8.

Note that what we actually need and show on the two displays (the display code is not included), OLED and SLM, are:
- the warpped RGB image, and 
- the warpped and computed phase mask image.

All codes are in python.

### Requirements
`python 3.6` or above, `numpy`, `skimage`, `opencv`

### Usage
Run in this folder
```sh
python compute.py
```

`compute.py` is a script that takes an input texture map (color, png or jpg) and an input diopter map (grayscale, png or jpg) and computes the texture image to display on the oled and the phase mask to display on the slm. It saves the output texture map, diopter map, and phase mask to `output_folder`.

To change input images, change the file names at line 153 and 154.

To change parameters, change the desired parameter values in `params.py`.

To change the homography matrix, modify line 165 to the desired homography matrix.
