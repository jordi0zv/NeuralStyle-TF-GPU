# NeuralStyle-TF-GPU

Neural Style Transfer (NST) is a technique in machine learning and compute vision that allows the fusion of two images: One representing the content and the other the style. The result is a new image (generated image) that combines the content structure with the artistic features of the style image.

This project implements NST using Tensorflow with GPU acceleration via CUDA, leveraging the VGG19 pre-trained model for feature extraction.

## Table of Contents
- [Features](#features)
- [Dependencies](#dependencies)
- [Project Structure](#project-structure)
- [Results](#results)
- [How to Run the Application](#how-to-run-the-application)
- [References](#references)


## Features
- **Tensorflow GPU Acceleration:** Uses Tensorflow and CUDA for optimal training speed.
- **VGG19 Pre-trained Model:** Employs a modified VGG19 model for effective content and style extraction.
- **Noise Initialization:** Starts with content image and noisy for enhanced stylization effects.

## Dependencies
This project was made with the following main dependencies/configuration:
- **Python** version **3.10**
- **CUDA** version **11.2**
- **cuDNN** version **8.1**

## Project Structure
```bash 
.
├── generated_images/              # Images generated by neural style 
├── images/                        # Images: content and style images to use 
├── pretrained_model/              # VGG19 model without Top
├── Neural-Style-Transfer.ipybn    # Main application logic in jupyter (more explained) Neural Style Transfer
├── Neural-Style.py                # Python version of jupyter version
...
```

## Results

Below are some example results produced by this neural style transfer project. Each output image combines the content of one image with the style of another:

- With around 3000 iterations

| Content Image | Style Image | Generated Image |
|----------|----------|----------|
| <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/images/claude_monet.jpg" alt="Content Image 1" width="400" height="400"> | <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/images/drop-of-water.jpg" alt="Style Image 1" width="400" height="400"> | <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/generated_images/water_monet.jpg" alt="Result Image 1" width="400" height="400"> |

- With around 1000 iterations

| Content Image | Style Image | Generated Image |
|----------|----------|----------|
| <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/images/claude_monet.jpg" alt="Content Image 1" width="400" height="400"> | <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/images/drop-of-water.jpg" alt="Style Image 1" width="400" height="400"> | <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/generated_images/water_monet.jpg" alt="Result Image 1" width="400" height="400"> |

- With around x iterations

| Content Image | Style Image | Generated Image |
|----------|----------|----------|
| <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/images/claude_monet.jpg" alt="Content Image 1" width="400" height="400"> | <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/images/drop-of-water.jpg" alt="Style Image 1" width="400" height="400"> | <img src="https://github.com/Jordi17z/NeuralStyle-TF-GPU/blob/main/generated_images/water_monet.jpg" alt="Result Image 1" width="400" height="400"> |

## How to Run the Application

- **Option 1:** With jupyter.
- **Option 2:** Using the python script. Place your content and style images in the images/ directory.
Run the main script (example):
```bash
python .\Neural-Style.py --content images/mona_lisa.jpg --style images/stone_style.jpg --output stone_lisa
```

## References
- Although Tensorflow functions automatically makes use of CUDA acceleration, however you can do a quick read on gpu and tensorflow usage here like i did: [https://www.tensorflow.org/guide/gpu].
- Obviously the Neural Style Transfer paper which introduce the concept and methodology [https://arxiv.org/abs/1508.06576].
- Youtube videos for better understanding such as [https://youtu.be/gzQxnZDePko?si=2PjyzVVdznNExlFY]. (here you have a different implementation).
