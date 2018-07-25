# Build-VisionWorks--Library-And-Run-Sample
How to build VisionWorks library and run sample

https://developer.nvidia.com/embedded/visionworks

# Step 1

Flush NVIDIA JetsonTx2 go to flowing link
https://docs.nvidia.com/jetpack-l4t/index.html#jetpack/3.2.1/install.htm

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

```
# Step 3
```
## Native Compilation of Sample Applications and Demos ##

The only method you can use to build the sample applications and demos is a
native build on the target system.

Sources for all samples and demos are provided in the `libvisionworks-samples` package.
After the package installation, source code and make files are located in the
`/usr/share/visionworks/sources` directory. The directory is protected from changes,
so you need to copy its content to any directory with write access.
Here we use your home folder as an example.
All samples use `make` as a build tool.

    $ /usr/share/visionworks/sources/install-samples.sh ~/
    $ cd ~/VisionWorks-<ver>-Samples/
    $ make -j4 # add dbg=1 to make debug build

You can build an individual sample from its directory but the executable will
not be created there nor in a sub-directory. The executable is created in the same directory
as when all samples are built from the top-level directory.

## Running Samples and Demos ##

**Applies to:** ARM devices only. Start the X window manager:

    $ export DISPLAY=:0
    $ X -ac &
    $ blackbox $

Go to the samples directory:

    $ cd ~/VisionWorks-<ver>-Samples/sources/bin/[arch]/linux/release
    Or
    $ cd ~/VisionWorks-<ver>-Samples/bin/[arch]/linux/release

Run each sample of interest by using the name of the sample. For example, to run `nvx_demo_feature_tracker`, execute:

    $ ./nvx_demo_feature_tracker

```
# Step 4
```
## Native Compilation of Sample Application for visionworks-tracking ##

Sources for samples are provided in the `libvisionworks-tracking-dev` package.
After package installation, source code and make files are located at:

    /usr/share/visionworks-tracking/sources

The directory is write protected;
copy its contents to a directory with write access, such as your home directory.
Execute the following commands:

    $ /usr/share/visionworks-tracking/sources/install-samples.sh ~/
    $ cd ~/VisionWorks-Tracking-<ver>-Samples/
    $ make -j4 # add dbg=1 to make debug build

Where `<ver>` is the version of the VisionWorks Object Tracker sample.

## Running Samples ##

**Applies to:** Jetson devices only.

1. Start the X window manager:

        $ export DISPLAY=:0
        $ X -ac &
        $ blackbox

2. Navigate to the samples directory:

        $ cd ~/VisionWorks-Tracking-<ver>-Samples/sources/bin/<arch>/linux/release
        Or
        $ cd ~/VisionWorks-Tracking-<ver>-Samples/bin/<arch>/linux/release

    Where `<ver>` is the version of the VisionWorks Object Tracker sample and `arch` is
    platform architecture.

3. Execute the following command:

        $ ./nvx_sample_object_tracker

```
# Step 5
```
## Native Compilation of Sample Application for visionworks-sfm ##

Sources for samples are provided in the `libvisionworks-sfm-dev` package.
After package installation, source code and make files are located at:

    /usr/share/visionworks-sfm/sources

The directory is write protected;
copy its contents to a directory with write access, such as your home directory.
Execute the following commands:

    $ /usr/share/visionworks-sfm/sources/install-samples.sh ~/
    $ cd ~/VisionWorks-Sfm-<ver>-Samples/
    $ make -j4 # add dbg=1 to make debug build

Where `<ver>` is the version of the VisionWorks SFM sample.

## Running Samples ##

**Applies to:** Jetson devices only.

1. Start the X window manager:

        $ export DISPLAY=:0
        $ X -ac &
        $ blackbox

2. Navigate to the samples directory:

        $ cd ~/VisionWorks-Sfm-<ver>-Samples/sources/bin/<arch>/linux/release
        Or
        $ cd ~/VisionWorks-Sfm-<ver>-Samples/bin/<arch>/linux/release

    Where `<ver>` is the version of the VisionWorks SFM sample and `arch` is
    platform architecture.

3. Execute the following command:

        $ ./nvx_sample_sfm

```
