# Pan/tilt face tracking with a Raspberry Pi + NCS
*This project using the NCS with openvino and ServoBlaster to drive*
multiple servos via the GPIO pins
to face tracking 
## Installation Python Libraries:
* Picamera -[[Installation]](https://picamera.readthedocs.io/en/release-1.13/install.html)
* OpenVINO
* Numpy

## Things needed:
* A raspberry pi 3B
* A Neural Compute Stick - (NCS)
* A pan/tilt bracket - (3D print)
* Two Servos - (SG90)
* A GPIO expansion board
* Pi Camera or USB Webcam

## Install the OpenVINO™ Toolkit for Raspbian* OS Package
### METHOD 1:
* #### Run this script [./Install_openvino.sh](https://github.com/yehengchen/FaceTracking-RPI3-NCS/blob/master/Install_openvino.sh)
*This script provides all instructions on install the OpenVINO™ toolkit package for Raspbian* OS*
### METHOD 2:
* #### The following steps will be covered:[[guide]](https://github.com/yehengchen/NCS2-OpenVINO)
*This guide provides step-by-step instructions on how to install the OpenVINO™ toolkit for Raspbian* OS*

## Getting Started:
### Install and start multiple servos:
    git clone git@github.com:yehengchen/FaceTracking-RPI3-NCS.git
    cd FaceTracking-RPI3-NCS/ServoBlaster/user
    sudo ./servod
    
### Testing multiple servos:
    echo 0=+10 > /dev/servoblaster
    echo 1=+10 > /dev/servoblaster

### Testing Picamera:
    raspistill -o image.jpg

### Run face tracking:
    python3 pi_NCS_face_traking.py

    
## Reference:
[PiBits-ServoBlaster](https://github.com/richardghirst/PiBits/tree/master/ServoBlaster)
