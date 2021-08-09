# C++ Pytorch Example 

## Installing the Library

This is the example shown in https://pytorch.org/cppdocs/installing.html#support with a few details added.

## Building

When entering the build directory it is necessary to add a `CMAKE_PREFIX_PATH` to the `cmake` command:
```
> cmake -DCMAKE_PREFIX_PATH=<absolute path to the libtorch directory> ..
```
