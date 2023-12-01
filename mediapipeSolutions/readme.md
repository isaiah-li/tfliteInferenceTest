# mediapipe solutions sample

## pose tracking

###reference
![pose tracking](https://github.com/google/mediapipe/blob/master/docs/solutions/pose.md)

### 'cv2' has no attribute '_registerMatType 问题解决

* 降级 或 headless
```
pip install opencv-python == lower
pip install opencv-python-headless<4.3
```

* 升级
```
pip install --upgrade opencv-contrib-python
pip install --upgrade opencv-python
pip install --upgrade opencv-python-headless
```

### cv2.error: OpenCV(4.8.1) /io/opencv/modules/highgui/src/window.cpp:1255: error: (-2:Unspecified error) The function is not implemented. Rebuild the library with Windows, GTK+ 2.x or Cocoa support. If you are on Ubuntu or Debian, install libgtk2.0-dev and pkg-config, then re-run cmake or configure script in function 'cvNamedWindow'

```
pip uninstall opencv-python
pip uninstall opencv-contrib-python
 
pip install opencv-contrib-python
pip install opencv-python
```

* opencv-python: 只包含opencv库的主要模块. 一般不推荐安装.
* opencv-contrib-python: 包含主要模块和contrib模块, 功能基本完整, 推荐安装.
* opencv-python-headless: 和opencv-python一样, 但是没有GUI功能, 无外设系统可用.

