# How to Install TensorFlow 2 and OpenCV on a Raspberry Pi


Recommend to use 64-bit Raspberry Pi and Latest OS

### Open Ternimal

Check the OS
`cat /etc/os-release`
make sure that VERSION = "11 (bullseye)"

Update and Upgrade OS (skip if os is already updated)
`sudo apt update`
`sudo apt upgrade`

Check Python Version
`python3 -V`

Check Architechture
`uname -m`

Note thses two things (Python version and Architechture), this need to select tensorflow shell file

For python3 -V = "3.9" & uname -m ="aarch64"
>download_tensorflow-2.8.0-cp39-none-linux_aarch64_numpy1221.sh

Open Link (skip)
https://github.com/PINTO0309/Tensorflow-bin/blob/main/previous_versions/download_tensorflow-2.8.0-cp39-none-linux_aarch64_numpy1221.sh

Click on Raw and Copy URL (skip)
https://raw.githubusercontent.com/PINTO0309/Tensorflow-bin/main/previous_versions/download_tensorflow-2.8.0-cp39-none-linux_aarch64_numpy1221.sh

Go back to Terminal
`wget https://raw.githubusercontent.com/PINTO0309/Tensorflow-bin/main/previous_versions/download_tensorflow-2.8.0-cp39-none-linux_aarch64_numpy1221.sh`

To see Download File
`ls`

You will find the file

Make it executable
`sudo chmod +x download_tensorflow-2.8.0-cp39-none-linux_aarch64_numpy1221.sh`

Download .whl File
`./download_tensorflow-2.8.0-cp39-none-linux_aarch64_numpy1221.sh`

To see .whl File
`ls`

Uninstall TensorFlow if have installed any
`sudo pip uninstall tensorflow`
`pip3 uninstall  tensorflow`

Install tensorflow using .whl File
`pip3 install tensorflow-2.8.0-cp39-none-linux_aarch64.whl`

Check TensorFlow
>`python3`
`import tensorflow as tf`
`tf.__version__`
`quit()`

Install OpenCV
`pip3 install opencv-python`

Install picamera
`python3 -m pip install "picamera[array]"`

Check OpenCV
>`python3`
`import cv2`
`cv2.__version__`
`quit()`


ERROR 
Downgrade the protobuf package to 3.20.x or lower
`pip3 install protobuf==3.20.*`
RuntimeError: module compiled against API version 0xf but this version of numpy is 0xd
`pip3 install numpy --upgrade`


# Install Jupyter Notebook
`pip3 install jupyter`

PIL install
`sudo apt-get install python3-pil python3-pil.imagetk`
