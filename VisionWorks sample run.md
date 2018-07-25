# VisionWorks--Library-Run-Sample

```
https://developer.nvidia.com/embedded/visionworks
```
# Step 1
```
Flush NVIDIA JetsonTx2 go to flowing link
https://docs.nvidia.com/jetpack-l4t/index.html#jetpack/3.2.1/install.htm
```
# Step 2
```
The following table shows various directories where the VisionWorks packages are
located after installation.

________________________________________________________________________________
Package Name      : libvisionworks
Installed location: /usr/lib
Description       : Main package with pre-built shared libraries.
________________________________________________________________________________
Package Name      : libvisionworks-dev
Installed location: /usr/include
                    /usr/lib
                    /usr/lib/pkgconfig
                    /usr/share/visionworks/cmake
Description       : Development package with headers, supplementary CMake and
                    package config files.
________________________________________________________________________________
Package Name      : libvisionworks-samples
Installed location: /usr/share/visionworks/sources
Description       : Source code for samples, demos, and NVXIO.
________________________________________________________________________________
Package Name      : libvisionworks-docs
Installed location: /usr/share/visionworks/docs
Description       : Documentation package for this release of VisionWorks.
________________________________________________________________________________

If missing package then flush JetsonTx2 properly
```
# Step 3
```
## Native Compilation of Sample Applications and Demos ##

    $ /usr/share/visionworks/sources/install-samples.sh ~/
    $ cd ~/VisionWorks-<ver>-Samples/
    $ make -j4 # add dbg=1 to make debug build

## Running Samples and Demos ##

Go to the samples directory:

    $ cd ~/VisionWorks-<ver>-Samples/sources/bin/[arch]/linux/release
    Or
    $ cd ~/VisionWorks-<ver>-Samples/bin/[arch]/linux/release
    
    Where `<ver>` is the version of the VisionWorks Object Tracker sample and `arch` is
    platform architecture.

## Running Samples ##

    $ ./nvx_demo_feature_tracker

```
# Step 4
```
## Native Compilation of Sample Application for visionworks-tracking ##

Execute the following commands:

    $ /usr/share/visionworks-tracking/sources/install-samples.sh ~/
    $ cd ~/VisionWorks-Tracking-<ver>-Samples/
    $ make -j4 # add dbg=1 to make debug build


## Running Samples ##

1. Navigate to the samples directory:

        $ cd ~/VisionWorks-Tracking-<ver>-Samples/sources/bin/<arch>/linux/release
        Or
        $ cd ~/VisionWorks-Tracking-<ver>-Samples/bin/<arch>/linux/release

   
2. Execute the following command:

        $ ./nvx_sample_object_tracker

```
# Step 5
```
## Native Compilation of Sample Application for visionworks-sfm ##

Execute the following commands:

    $ /usr/share/visionworks-sfm/sources/install-samples.sh ~/
    $ cd ~/VisionWorks-Sfm-<ver>-Samples/
    $ make -j4 # add dbg=1 to make debug build

## Running Samples ##

1. Navigate to the samples directory:

        $ cd ~/VisionWorks-Sfm-<ver>-Samples/sources/bin/<arch>/linux/release
        Or
        $ cd ~/VisionWorks-Sfm-<ver>-Samples/bin/<arch>/linux/release

2. Execute the following command:

        $ ./nvx_sample_sfm

```
