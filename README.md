# License-Plate-Detection
This project demonstrates the use of TensorFlow Object Detection API to detect number plates (Indian) from vehicles

Dataset used: https://www.kaggle.com/dataturks/vehicle-number-plate-detection

## Files/Folders :
- DataSet : Contains images of the cars and the respective cropped number plates
- Data :This folder contains the following :
     - test_labels.csv & train_labels.csv: .csv files as required by the generate_tfrecord.py script
     - test.record & train.record: TFRecords files of testing and training sets respectively(needed for training our model TFOD API)
     - label_map.pbtxt: Contains the encodings of the dataset classes which,in this case, is 1: license_plate
     - ssd_mobilenet_v1_pets.config: Training and evaluation pipeline configuration file as needed by TFOD API(depends on what model you choose)
 - Output_folder :This folder contains the following :
     - Images: a few results
     - output_inference_graph.pb: Contains the inference graph in .pb , the model checkpoint and the SavedModel
     - tflite_output_inference_graph.pb: Contains the inference graph in .pb and .tflite formats for using on mobile devices

- Indian_Number_plates.json: Configuration file which contains image download paths and annotations (downloaded from kaggle)
- generate_tfrecord.py : for converting csv files to TFRecord
- preparing_data.ipynb: A notebook demonstrating the process of preparing the dataset(.csv files) and for creating TFRecords
- scripts.ipynb: contains all commands needed to train ,evaluate and save the model

## Demo Inference ( taken from tensorboard )
![Alt Text](https://github.com/harshita-555/Licence-Plate-Detection/blob/master/License_Plate_Detection/output_folder/Images/success_2.png)
![Alt Text](https://github.com/harshita-555/Licence-Plate-Detection/blob/master/License_Plate_Detection/output_folder/Images/success_3.png)
![Alt Text](https://github.com/harshita-555/Licence-Plate-Detection/blob/master/License_Plate_Detection/output_folder/Images/fail_1.png)



