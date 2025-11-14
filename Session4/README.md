# Assignment 4 
MNIST dataset with 99.4% accuracy with less than 20K params and under 20 epochs.
# Submitted by:
Smita Sasindran
Aayushee Mittal
Vishesh Sethi
Avneesh Nolkha

# Wev've used the following concepts/techniques/algorithms in the assignmnet:
-How many layers,
-MaxPooling,
-1x1 Convolutions,
-3x3 Convolutions,
-Receptive Field,
-SoftMax,
-Learning Rate,
-Kernels and how do we decide the number of kernels?
-Batch Normalization,
-Image Normalization,
-Position of MaxPooling,
-Concept of Transition Layers,
-Position of Transition Layer,
-DropOut
-When do we introduce DropOut, or when do we know we have some overfitting
-The distance of MaxPooling from Prediction,
-The distance of Batch Normalization from Prediction,
-When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)
-How do we know our network is not going well, comparatively, very early
-Batch Size, and effects of batch size

# Our network is as followed:

____________________________________________________________________
|             Block            |          Input        |       Output         |   Receptive Field    |
|___________________| ______________| ______________ |_________________|
Convolution Block 1  |   28x28x1          |      22x22x32     |         7x7                 |
|Transition Block 1     |   22x22x32        |      11x11x16     |        14x14              |
|Convolution Block 2 |   11x11x16        |      7x7x16         |        18x18              |
Convolution Block 3  |   7x7x16            |      5x5x16         |        22x22              |
| Average Pool Layer |   5x5x16            |      1x1x10         |        27 x 27            |
|___________________|______________ | _____________ | _________________ |

Droput - 0.1
BatchNorm - 16 & 32
Learning rate = 0.2
Momentum = 0.7
Optimizer - SGD
Conv Kernel - 3x3
Transition Kernel - 1x1
Max Pooling Kernel - 2x2
Padding = 0

Final Accuracy was 99.36 %
Achieved Accuracy of 99.44 in 12th epoch
