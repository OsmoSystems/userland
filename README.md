# OsmoSystems README
This is a fork of the raspberrypi/userland repo. It applies a small patch that results in the raspistill camera control program to control an LED (on BCM pin 5) to turn on and off in alignment with the start and end of image capture.

It was inspired by the snippet provided by [6by9](https://github.com/6by9) in this [forum post](https://www.raspberrypi.org/forums/viewtopic.php?t=165910)

# Original README
This repository contains the source code for the ARM side libraries used on Raspberry Pi.
These typically are installed in /opt/vc/lib and includes source for the ARM side code to interface to:
EGL, mmal, GLESv2, vcos, openmaxil, vchiq_arm, bcm_host, WFC, OpenVG.

Use buildme to build. It requires cmake to be installed and an ARM cross compiler. For 32-bit cross compilation it is set up to use this one:
https://github.com/raspberrypi/tools/tree/master/arm-bcm2708/gcc-linaro-arm-linux-gnueabihf-raspbian

Whilst 64-bit userspace is not officially supported, some of the libraries will work for it. To cross compile, install gcc-aarch64-linux-gnu and g++-aarch64-linux-gnu first. For both native and cross compiles, add the option ```--aarch64``` to the buildme command.

Note that this repository does not contain the source for the edidparser and vcdbg binaries due to licensing restrictions.
