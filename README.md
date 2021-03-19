# tf2.0-cv2-kivy-on-ubuntu20.04-arm64-RP4
Setting up tensorflow 2.0, Kivy and OpenCV on Ubuntu 20.04 server and Raspberry Pi 4 (arm64)


# Step 1: Download Ubuntu Server 20.04.2 LTS
link: https://ubuntu.com/download/raspberry-pi

Note: Do not download the Ubuntu 20.10 desktop or server version as it does not suppport tensorflow at the moment. You must download and use Ubuntu 20.04 for the Raspberry Pi.

In bash run:

`$ source step0_setup.sh`




# Step 2: Install TensorFlow 2.2

In bash run:

`$ source step1_install_tensorflow_quick.sh`

Given that Ubuntu 20.04 comes with Python 3.8, we need to install Python 3.7 and also make Python 3.7 the default python version. The bash script takes care of all this. We are using Python 3.7 because that wheel is provided for ARM64 hardware with Tensorflow 2.4.0.


Then to check if it has installed:
```
$ python
>>> import tensorflow at tf
>>> tf.__version__

```




===
To install Kivy:
https://kivy.org/doc/stable/installation/installation-linux.html#linux-ppa

$ sudo add-apt-repository ppa:kivy-team/kivy
$ sudo apt-get update
$ sudo apt install libsdl2-dev libsdl2-image-dev libsdl2-mixer-dev libsdl2-ttf-dev

Then this:
$ sudo apt-get install python3-kivy
$ sudo apt-get install kivy-examples

Or this:
$ python -m pip install kivy[base] kivy_examples

Not sure which one worked.

====

https://vielmetti.typepad.com/logbook/2021/02/getting-tensorflow-running-on-arm64.html

https://qengineering.eu/install-tensorflow-2.2.0-on-raspberry-64-os.html

===
To isntall tensorflow
https://www.tensorflow.org/lite/guide/build_rpi

$ sudo apt-get install build-essential
$ git clone https://github.com/tensorflow/tensorflow.git tensorflow_src
$ sudo apt install curl
$ cd tensorflow_src && ./tensorflow/lite/tools/make/download_dependencies.sh


====

pip install imutils
pip install numpy


===

create a python virtual environment:
>> python3 -m venv wb

start that virtual environment:
>> source wb/bin/activiate

