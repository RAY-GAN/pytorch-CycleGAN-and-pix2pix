!git clone https://github.com/RAY-GAN/pytorch-CycleGAN-and-pix2pix.git
\\ clone the repo


import os
os.chdir('pytorch-CycleGAN-and-pix2pix/')


!pip install -r requirements.txt
\\ install all the required API


!bash ./datasets/download_cyclegan_dataset.sh horse2zebra
\\down load the datasets for the horse2zebra translation


!python train.py --dataroot ./datasets/horse2zebra --name horse2zebra --model cycle_gan
\\ start the training process


!python test.py --dataroot datasets/horse2zebra/testA --name horse2zebra --model test
\\ start the testing process


\\ Make sure the dataroot is consistent with the desired datasets you want to train
\\ Check out the option files to further explore the possible flags for different training and test options



The majority of the codes are originated from https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix.git

I added custom dataset to the dataset folder: maskchange & animatedface.
