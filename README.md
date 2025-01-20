**Configured For MacOS**

python version 3.10.0
Best in Conda Environment

**Libraries**
**pip3 install tensorflow-macos==2.13.0**

if doesnt install other libraries, try these too
pip3 install tensorflow-metal==1.1.0
pip3 install keras==2.13.1
pip3 install torch (version 2.5.0)
pip3 install numpy (version1.24.3)

might need these libraries
ultralytics (version 8.3.63)


**!!!Replace example.pt with the .pt file you want to convert. Put all your models in yolov5/weights folder**
To verify can be converted to TensorFlow Keras model
python3 yolov5/models/tf.py --weights yolov5/weights/example.pt 

The actual conversion, delete the (saved model folder generated) and the tflite file should appear in the same weights folder
python3 yolov5/export.py --weights yolov5/weights/example.pt --include tflite 
