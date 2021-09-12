# mmcv

ModuleNotFoundError: No module named 'mmcv._ext'

reference: https://github.com/open-mmlab/mmdetection/issues/3271

This error can be fixed by build the package from source.

```
pip uninstall mmcv mmcv-full
Install MMCV from source.
git clone https://github.com/open-mmlab/mmcv.git
cd mmcv
MMCV_WITH_OPS=1 python3 -m pip install -e .
```