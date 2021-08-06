**Instruction for collision avoidance**

Need to set Speed gain = 0.09, Sterring gain = 0.03

*1. Not using TensorRT, worse perfomance*
1. Run data_collection.ipynb and follow the promps for data collection. (My own data 120 pictures are in dataset.zip)
2. Run train_model.ipynb to get best_model.pth
3. Run live_demo.ipynb for collision avoidance

*2. Using TensorRT, better perfomance since utilize the NVIDIA GPU more*
1. Run data_collection.ipynb and follow the promps for data collection. (My own data 120 pictures are in dataset.zip)
2. Run train_model_resnet18.ipynb to get best_model.resnet18.pth
3. Run live_demo_resnet18_build_trt.ipynb to get best_model_trt.pth
4. Run live_demo_resnet18_trt.ipynb

**I run both demos and verfied the second one that used TensorRT have better performance !**
