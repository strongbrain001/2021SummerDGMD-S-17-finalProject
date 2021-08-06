**Instruction for collision avoidance**

Need Xbox gamepad for data collection

Need to set speed gain = 0.09, Sterring = 0.02, Sterring KD = 0.07 for smooth run

*1. Not using TensorRT, worse perfomance

1. Run data_collection_gamepad.ipynb and follow the promps for data collection. (My own data 420 pictures are in road_following_dataset_xy_2021-07-26_13-33-12.zip)
2. Run train_model.ipynb to get best_steering_model_xy.pth
3. Run live_demo.ipynb for line following

*2. Using TensorRT, better perfomance since utilize the NVIDIA GPU more*

1. Run data_collection_gamepad.ipynb and follow the promps for data collection. (My own data 420 pictures are in road_following_dataset_xy_2021-07-26_13-33-12.zip)
2. Run train_mode.ipynb to get best_steering_model_xy.pth
3. Run live_demo_build_trt.ipynb to get best_steering_model_xy_trt.pth
4. Run live_demo_trt.ipynb

**I run both demos and verfied the second one that used TensorRT have better performance !**
