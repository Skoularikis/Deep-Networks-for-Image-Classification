# Deep Networks for Image Classification

<strong><em>Exploring very deep convolutional networks based on VGG, ResNet, GoogLeNet principles.</em></strong>

## Summary
Implementation of both the original models - VGG16, ResNet18, Inception v1 - and respective alternative versions on MNIST and CIFAR10 datasets. The comparison between these six models indicate that the "improved" versions slightly outperform their vanilla counterparts.

For the avid reader, an extensive six page paper is also compiled, describing models' principles, training process and experimental results on the aforementioned datasets.

### Technologies Used:
Python, Pytorch, Matplotlib, Pandas, Scikit-Learn


#### Improtant Notes:
<ul>
<li>Due to time and hardware restrictions, all images were resized the size of 64 x 64. </li>
<li>Necessary changes (e.g changed the input of the first convolution layer to 1, accounting for grayscale images) were introduced to allow the networks' training.  </li> 
<li>Altered training process - Label smoothing, weight decay, multi-step learning rate scheduler, momentum - </li>
<li>Augmented existing data depending on the dataset of choice.</li>
</ul>

#### Overview of changes in VGG16
<ul>
<li>Added batch normalization layers between each convolution layer and before their activation layer.</li>
<li>Changed VGG's original implementation Adaptive Average Pooling layer with an 5 x 5 Adaptive Max Pooling layer. </li>
<li>Initialized network layers' weights and biases from an appropriate distribution.</li>
</ul>

#### Overview of changes in ResNet18
<ul>
<li>Replaced the original large 7 x 7 convolution layer by a stack of 3 x 3 convolutions.</li>
<li>Added batch normalization layers to the aforementioned stack between each convolution layer and before their activation layer.</li>
<li>Introduced a dropout layer with a minor dropout ratio before the linear classifier</li>
<li>Initialized network layers' weights and biases from an appropriate distribution.</li>
</ul>

#### Overview of changes in Inception v1
<ul>
<li>Replaced the original 7 x 7 convolution layer by a stack of 3 x 3 convolutions, inspired by VGG's findings.</li>
</ul>

## Installation Process

Clone repository (e.g with https)

``
git clone https://github.com/Skoularikis/Deep-Networks-for-Image-Classification.git
``

Providing conda is installed locally you can create env from file(environment.yaml):

``conda env create --file environment.yaml``

Activate env: 

``conda activate skoularikis_deep_networks_env``

To make development easier jupyter-lab has been installed.



## Known Issues
Due to known issues with loading notebooks on Github you can check the entire repository's content online on [nbviewer](https://nbviewer.jupyter.org/github/Skoularikis/Deep-Networks-for-Image-Classification/tree/main/)


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


## License
[MIT](https://choosealicense.com/licenses/mit/)
