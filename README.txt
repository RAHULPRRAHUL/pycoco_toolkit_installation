Discussion:
https://github.com/matterport/Mask_RCNN/issues/6

https://github.com/waspinator/pycococreator

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
