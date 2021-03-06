# Convolutional-Neural-Networks
`*` => means convolution in neural network and elementwise multiplication in python.

As the value of an image matrix moves towards zero or negative, the associated pixel gets darker. So, moving towards zero or negative one or so on exhibits darker shades while high values express brighter shades.

#### Suppose, we have an input matrix of shape (6x6) and the kernel(filter) applied is of the shape (3x3). Then the output matrix shape will be (4x4). The actual formula here: if input matrix is of shape (nxn) and kernel is of shape (fxf) then the output matrix will be of shape (n-f+1 x n-f+1).

#### If we introduce padding, p then the formula of the shape of output matrix will be (n+2p-f+1 x n+2p-f+1). f is usually odd. Because, it is easier to find whole number padding value using the following equation: n+2p-f+1 = n => 2p-f+1 = 0 => p = (f-1)/2. For instance, for (3x3) kernel or filter the padding will be 1, for (5x5) padding will be 2 and so on.

#### Padding is usually done to make the input matrix and the output matrix of the same shape.

#### Strided Convolution is done by hopping more than one space while performing convolution on a input matrix. The hopping amount is denoted by stride s. The formula for getting the output matrix shape through strided convolution is: (((n+2p-f)/s)+1 x ((n+2p-f)/s)+1); where s is stride. For instance, input matrix = (nxn) = (7x7), padding,p = 0, kernel(filter) = (fxf) = (3x3), stride,s = 2 then the output matrix shape = ((7+2.0-3)/2)+1 = 3; (3x3). If the output matrix shape is not an integer, then we have to round it down to the nearest integer.

n(subscript)c => n_c => number of channels (RGB)

Useful hyper-parameters for convolutional neural network are: filter shape, number of filters, stride, padding etc.

#### Stride implies the step size while moving the filter (kernel) or pooling layer over the original image. If we move on 1 column right and 1 row down with the kernel or pooling layer then stride, s = 1. Similarly, when we step with 2 columns right and 2 rows down, then stride, s = 2.

In case of an image shape such as: 32 x 32 x 3, the last dimension 3 usually denotes the color channel. In most cases the color channel is RGB (Red, Green and Blue) which implies three dimensional image.

As you go through the convolutional neural network build up process, the height and width of the input image (the first two dimensions) => n_H = 32 and n_W = 32 in the above case go down (decrease) and the color channel or the third dimension, n_C = 3 in the above case goes up (increases).

#### Keep in mind that each dimensional value is a parameter in neural network. Which implies to the notion that to learn each data point in an image or any form of input, you need to apply some weights to that data point. And each weight is a parameter. Which means for an image of shape 32 x 32 x 3, the image size is 3072 and so number of parameters will also be 3072 (in the form of weights).








































