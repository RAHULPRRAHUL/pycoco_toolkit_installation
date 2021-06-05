MS COCO API - http://mscoco.org/

Microsoft COCO is a large image dataset designed for object detection, segmentation, and caption generation. This package provides Matlab, Python, and Lua APIs that assists in loading, parsing, and visualizing the annotations in COCO. Please visit http://mscoco.org/ for more information on COCO, including for the data, paper, and tutorials. The exact format of the annotations is also described on the COCO website. The Matlab and Python APIs are complete, the Lua API provides only basic functionality.

In addition to this API, please download both the COCO images and annotations in order to run the demos and use the API. Both are available on the project website.
-Please download, unzip, and place the images in: coco/images/
-Please download and place the annotations in: coco/annotations/
For substantially more details on the API please see http://mscoco.org/dataset/#download.

After downloading the images and annotations, run the Matlab, Python, or Lua demos for example usage.

To install:
-For Matlab, add coco/MatlabApi to the Matlab path (OSX/Linux binaries provided)
-For Python, run "make" under coco/PythonAPI
-For Lua, run “luarocks make LuaAPI/rocks/coco-scm-1.rockspec” under coco/



###########################################################################


clone github repository:-

https://github.com/cocodataset/cocoapi

then edit the setup.py file in the coco/PythonAPI directory from this:-
extra_compile_args=['-Wno-cpp', '-Wno-unused-function', '-std=c99'],

to this:-
extra_compile_args=['-std=c99'],



When you run make under the PythonAPI folder, actually you run the command python setup.py build_ext --inplace, 
within which your default python(mostly python2) is called. 
So, just run the command python3 setup.py build_ext --inplace in the PythonAPI folder for python3. @asylbek27:-

python setup.py build_ext --inplace
