# ScanGAN360
Code and model for the paper "[ScanGAN360: A Generative Model of Realistic Scanpaths for 360º Images](http://webdiis.unizar.es/~danims/projects/vr-scanpaths.html)".

![Teaser](https://github.com/DaniMS-ZGZ/ScanGAN360/blob/main/img/vr-scanpaths.jpg)

## Requirements
This work was developed using:
```
* python 3.7.4
* pytorch 1.2.0
* cudatoolkit 10.0.30
* opencv 4.1.2
```
You can install an environment with all required dependencies using `scangan360.yml` file in Anaconda. 

## Inference
The current version of the repository includes a basic, yet functional version to generate scanpaths from a 360º image using the ScanGAN360 model.

### Usage
```
python main.py --mode inference 
```

This will read an image `image_path = "data/test.jpg"` and generate a set of scanpaths that will be saved in `path_to_save = "test/"`. You can modify both those paths, and the number of generated scanpaths `n_generated`. Each of the images will contain 25 different scanpaths.

## Training the model
Training is now available. [Updated June 15th]

```
python main.py --mode train 
```

Make sure you have correctly updated `utils.py`, including all the directories required. Also, check the `data` folder to download the required images and processed gaze data.

Checkpoints and models are saved periodically in the assigned folder.

## Installing Requirements 
conda create -n scangan360 python=3.7.4
conda install pytorch=1.2.0 torchvision=0.4.0 torchaudio cudatoolkit=10.0 -c pytorch
pip install opencv-python==4.1.2.30
pip install -r requirements.txt

// Download linux driver: https://www.nvidia.com/download/index.aspx?lang=en-us