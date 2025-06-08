# myrepo
-----------------------------Dog vs Cat classifier----------------------------
In this Section we are implementing Convolution Neural Network(CNN) Classifier for Classifying dog and cat images. The Total number of images available for training is 20,000 and final testing is done on seperate 5,000 images.
Architecture Flow :
Input: 256x256x3
    |
[Conv2D 3x3, 32] -> 254x254x32
    |
[BatchNorm]
    |
[MaxPool 2x2] -> 127x127x32
    |
[Conv2D 3x3, 64] -> 125x125x64
    |
[BatchNorm]
    |
[MaxPool 2x2] -> 62x62x64
    |
[Conv2D 3x3, 128] -> 60x60x128
    |
[BatchNorm]
    |
[MaxPool 2x2] -> 30x30x128
    |
[Flatten] -> 115200
    |
[Dense 128]
    |
[Dropout]
    |
[Dense 64]
    |
[Dropout]
    |
[Dense 1]
    |
[Sigmoid]




