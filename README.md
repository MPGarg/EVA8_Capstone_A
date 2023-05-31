# EVA8_Capstone_A

## Problem Statement

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/6819c494-43b9-463c-ba5c-4b1f6c653fb7)

## Solution Approach

ControlNet training done on fusing/fill50k dataset using stable diffusion V1.5 . It was trained for 1 epoch for 50,000 images. During this training there was hint of being trained but model was not able to converge.

Here are the validation images at completion of 1 epoch.

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/49ef86ac-0274-4b4a-8774-403e720f272d)

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/8455579f-9565-431e-972c-6e7388203984)

## Custom Dataset

Custom dataset was created using Flower images. Images were converted to Canny Image and Text was generated using BLIP. 

Dataset was hosted on HuggingFace: https://huggingface.co/datasets/MadhurGarg/Flowers and used for training purpose.

Training was done in 2 parts. Initially it was executed for 4 epochs (gradient_accumulation_steps = 2) and results were stored. Trained weights were further worked on in 10 more epochs (gradient_accumulation_steps = 1).

Model Prediction after initial run of 4 epochs:

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/9cc60b77-e75a-4584-a5c0-62eb8e7d0fcf)

Model is not able to perform well and need to be trained further.

It was trained on 10 futher epochs and at nearly 1000 more steps it starts showing sign of convergence.

Validation images at step 1000:

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/36890a78-7e13-4188-8ac8-a04f37c0b2c7)

At 1800 steps it was nearly trained:

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/2c25d085-5362-4e25-8309-75a2734d3c46)

At finish of training model predicted following images:

![image](https://github.com/MPGarg/EVA8_Capstone_A/assets/120099863/5364938b-0756-4cf1-b03e-de8342fd609c)

Model Link in Hugging Face: https://huggingface.co/MadhurGarg/ControlNet_Flowers2
