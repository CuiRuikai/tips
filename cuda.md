# CUDA Errors

## Error on make: 'cuda_runtime.h: No such file or directory'

reference: https://github.com/pjreddie/darknet/issues/553

Add cuda runtime to path


```
export CPATH=/usr/local/cuda-10.2/targets/x86_64-linux/include:$CPATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.2/targets/x86_64-linux/lib:$LD_LIBRARY_PATH
export PATH=/usr/local/cuda-10.2/bin:$PATH
```