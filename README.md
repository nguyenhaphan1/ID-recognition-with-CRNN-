Recognize ID from VNID card using CRNN model

1. Clone the github [FLming](https://github.com/FLming/CRNN.tf2)

```
!git clone https://github.com/FLming/CRNN.tf2
```
2. Directory setup
```
|--/CRNN.tf2
|--/data
|--/runs/train
```

3. Data preparing

```
/data
|--/train
|  |--image1.jpg
|  |--image2.jpg
|  |--image3.jpg
|
|--/test
|  |--image4.jpg
|  |--image5.jpg
|
|--train_annotation.txt
|--test_annotation.txt
|
|--table.txt
```

4. train/test_annotation.txt (mjsynth format)
```
[path_to_image] [annotation]
Example: /data/train/image1.jpg 012345678910
```

5. Change the config file to coresponding directory setup (mjsynth.yml)
 <img src="[url](https://github.com/user-attachments/assets/eab2bafd-ca89-4655-9797-bfd90091fb51)" alt="mjsynth" width="300" height="300">
6. Train the model with custom dataset
```
!python CRNN.tf2/crnn/train.py --config mjsynth.yml --save_dir 'runs/train'
```
**Reference:**

CRNN: [FLming](https://github.com/FLming/CRNN.tf2)
