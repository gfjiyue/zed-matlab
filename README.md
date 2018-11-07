# Stereolabs ZED - Matlab Integration for windows 10 

This sample shows how to use the ZED SDK functionalities within Matlab on my PC.


# Prerequisites

- Windows 10 64bits 
- NVIDIA GPU 
- CUDA 9.0 (https://developer.nvidia.com/cuda-90-download-archive)
- MS visual studio 2015 64bits
- Matlab 2018b
- cmake (https://cmake.org/download/)


# Procedures

## Step 1 Install ZED SDK

Download the ZED SDK cuda 9 version (https://www.stereolabs.com/developers/release/#sdkdownloads_anchor) and install.

## Step 2 Build mexZED

For detailed instructions, check out the "BUILD PROCEDURE" section in [documentation](https://www.stereolabs.com/documentation/integrations/matlab/getting-started.html).


## Step 3 Run the program in Matlab
In the Matlab directory, open the file `ZED_Camera.m` with Matlab and press run. Press any key to exit the program.

## Results

This sample is split into 3 parts, each of them shows a specific feature of the ZED SDK in Matlab.

1. `ZED_Camera.m` :

	In this part, we first initialize the ZED Camera and then retrieve both stereo images (Left and Right) as well as the depth data (32-bits float buffer) and the depth image normalized to 8-bits (grayscale). Then, with Matlab, we compute the depth histogram from the depth data values and display it.

	<img src="ZED_Camera.png" alt="Drawing" style="width: 600px;"/>

2. `ZED_Tracking.m` :

	This part shows how to get the positional tracking information. First, we initialize the ZED camera and the tracking, then we display the current left image as well as all the positions of the camera.

	<img src="ZED_Tracking.png" alt="Drawing" style="width: 600px;"/>

3. `ZED_PointCloud.m` :

	This part shows how to initialize the ZED camera and retrieve for each frame the current point cloud (X,Y,Z) of the scene. Then we use the mesh function of Matlab to display it.

	<img src="ZED_PointCloud.png" alt="Drawing" style="width: 600px;"/>

### Limitations
**This sample application is not designed to run in real time**
