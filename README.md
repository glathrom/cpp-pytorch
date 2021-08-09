# C++ Pytorch Example 

## Installing the Library

This is the example shown in https://pytorch.org/cppdocs/installing.html#support with a few details added.

Since I am using the [YouCompleteMe](https://github.com/ycm-core/YouCompleteMe) addon it is necessary to give the location of the `torch.h` file.
This is done by adding command
```python
'-isystem', '<absolut path to libtorch>/include',
'-isystem', '<absolute path to libtorch>/include/torch/csrc/api/include'
```

## Building

When entering the build directory it is necessary to add a `CMAKE_PREFIX_PATH` to the `cmake` command:
```
> cmake -DCMAKE_PREFIX_PATH=<absolute path to the libtorch directory> ..
```
