# Numpy Darknet: Make Darknet to support numpy array as input

To prevent us from maintaining a diverged repo, we make numpy support
as independent plugin w/o touching Darknet's source codes.

# How to Use

```
$ git clone https://github.com/mujahid-rahman/Numpy-Darknet
$ cd Numpy-Darknet
$ ./patch_darknet ../darknet
$ cd ../darknet
$ # Manual action: Prepare tiny-yolo model
$ # Manual action: Update Makefile configuration if needed
$ # Manual action: Install python3-numpy package if needed
$ make  # use -j <cpu-number> to speedup compilation
$ make -f Makefile.numpy
$ python3 darknet_npinput.py
```

# How to Release with darknet-numpy

Additional library, `libdarknet_numpy.so`, will be created. You need to
install it with `libdarknet.so` together.

# Example

Please refer to `darknet_npinput.py` and `darknet_npinput_rpi.py`.
