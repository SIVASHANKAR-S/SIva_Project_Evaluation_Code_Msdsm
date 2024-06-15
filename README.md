# MSDSM Project Evaluation Code

This code repo contains various models and their application codes. Different models trained with QAT + Edge Complied + Retrained.

It must have Raspberry Pi hardware to test to check its performance and evaluations.

You can test this code across Raspberry Pi 3 & 4. This code base does not support Raspberry Pi 5 because of different Arm-based compilations. Raise request for code  for testing in Raspberry Pi 5.

The development code is not intended for the general public.


All model drive link: [Link](https://drive.google.com/file/d/1OJJylNon3eJGoeiXVJRU5yNQRklPqTW8/view?usp=drive_link)


### Image Classification Models
```
inception_v1_224_quant_edgetpu.tflite, imagenet_labels.txt
inception_v2_224_quant_edgetpu.tflite, imagenet_labels.txt
inception_v3_299_quant_edgetpu.tflite, imagenet_labels.txt
inception_v4_299_quant_edgetpu.tflite, imagenet_labels.txt
mobilenet_v1_1.0_224_quant_edgetpu.tflite, imagenet_labels.txt
mobilenet_v2_1.0_224_quant_edgetpu.tflite, imagenet_labels.txt

mobilenet_v2_1.0_224_inat_bird_quant_edgetpu.tflite, inat_bird_labels.txt
mobilenet_v2_1.0_224_inat_insect_quant_edgetpu.tflite, inat_insect_labels.txt
mobilenet_v2_1.0_224_inat_plant_quant_edgetpu.tflite, inat_plant_labels.txt
```

### Object Detection Models
```
mobilenet_ssd_v1_coco_quant_postprocess_edgetpu.tflite, coco_labels.txt
mobilenet_ssd_v2_coco_quant_postprocess_edgetpu.tflite, coco_labels.txt
mobilenet_ssd_v2_face_quant_postprocess_edgetpu.tflite, coco_labels.txt
```

All you need is a Raspberry Pi and a Picamera or a USB Camera to run this project.

## Configure your Raspberry Pi to Run this Project
Download this repo on your Raspberry Pi and run the bash script "install.sh" using command ```sudo sh install.sh```.
This bash script will download all the necessary packages/libraries required for this project. Also, the all the Models and the source code will be downloaded automatically and placed in the correct path. <br>
It would be best if you waited patiently as the script can take upto 20 minutes (depending on your internet speed) to complete the task.

The script performs the following actions on your Raspberry Pi automatically:- 

- Update & upgrade Raspberry Pi OS
- Install Apache Webserver and PHP
- Install Tensorflow Lite and Google Coral USB Accelerator Libraries
- Install OpenCV
- Download pre-trained Models from Google Coral repository
- Download the model_garden source code 
- Move the models and code to the desired location in your Raspberry Pi and set permissions.

## How to run the code
Open the terminal in Raspberry Pi and type the following commands:-
```
cd /vars/www/html/Siva_Project_models_evaluation

python3 app.py
```


- check the ip of your Raspberry Pi using command ```hostname -I```
- For example, if it is 192.168.1.12, then using any Laptop/mobile open a browser and type the following URL:-<br>
```
192.168.1.12/Siva_Project_models_evaluation
```



Now, you should start seeing the camera video with overlays on the Web GUI.
You can switch between the various models using the buttons provided on Web GUI. Based on your selection the respective model along with its label file gets loaded in the background during run time itself. This allows you to quickly change the models and appreciate the inferencing speeds<br>
"# SIva_Project_Evaluation_Code_Msdsm" 
