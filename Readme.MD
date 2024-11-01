# Setup Instructions

### Open folder in vscode

You will be prompted to install extensions; install them.

### Edit CMakePresets.json

Build settings are in `CMakePresets.json`.  The important path is
`FORTRAN_BASEPATH` which should be set to the base path of the fortran compiler.  
Note that you must also set this in the `PATH` section:

![alt text](image-7.png)

### Configure cmake
Open the CMakeTools tab:

![alt text](image-1.png)

Select debug preset

![alt text](image-2.png)

### Add source files
Open `CMakeLists.txt`
You can add executables with `add_executable`, e.g.

![alt text](image-5.png)

## Building
Press f7, or click here:

![alt text](image-3.png)

Binaries will be build in `build/debug` or `build/release` depending 
on the build configuration.

## Debugging
Open Debugging tab

![alt text](image-4.png)

Select "Debug Target":

![alt text](image-6.png)

