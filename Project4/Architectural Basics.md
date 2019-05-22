 
How many layers- Depending on the type of the problem statement and the solution needed, the number of layers and in turn the network architecture needs to be decided. 

Receptive Field- While deciding the number of layers, we should ensure that the receptive field is close to the size of the image in question.

Kernels - the number of kernels is decided based on the explicivity needed and the hardware capabilities of the machine on which the solution will be deployed.

3x3 Convolutions - Is to be used to extract features from the images. Large number of 3x3 kernel will be better to extract as many features as possible in the early layers of the network.

MaxPooling- To be used when the number of parameters are increasing and reducing the size of image is unlikely to affect the performance of the network in extractign features. 

Position of MaxPooling-Maxpooling layers should be placed atleast 2 convolution layers away forom the input  to ensure that the network has extracted enough information.

The distance of MaxPooling from Prediction- Maxpooling layers should be placed atleast 2 convolution layers away from and output layer to ensure that the network doesnot lose information  by maxpooling when close to the prediction layer.

1x1 Convolutions- At some points in the network,where a certain combination of features generally go together(eg: eyes and eye brows generally go together) it would help to combine channels of information to make calculated prediction. It makes sense to combine the channels and carry them forward instead of taking them forward separately. In this sense, 1x1 convolution can help reduce the number of channels and in turn the parameters.

Concept and position of Transition Layers- maxpooling and 1x1 convolution togetehr constitutes the transition layer. It is generally placed between convolution blocks to break bottlenecks in the network architecture. This layer helps to significantly reduce number of parameters

SoftMax- gives stretched values for network prediction. Should not be used in applications where final predictions are crucial. Eg: in Medical diagnosis

Batch Size, and effects of batch size- Batch size should generally be more than the number of Epochs. The larger the batch size, faster the training

Number of Epochs and when to increase them- When learning rate is low, the network will need more number of epochs to hit therequired validation accuracy,

When to add validation checks- These checks need to added from the beginning of training so the performanc of the network can be observed early on in the training. 

How do we know our network is not going well, comparatively, very early- Enabling validation checks helps to predict the performance of the network by looking at the validation accuracy in the first couple of epochs.Comparing these values with the earlier iterations can help improving the network without having to wait till the end of training to improve it. 

Batch Normalization- Network can be improved by normalizing batches of images. 
The distance of Batch Normalization from Prediction-this should not be done too close to the prediction layer as vaulable information can be lost.
Image Normalization- Depending on the train and test data sets, image normalization can also be used to improve the accuracy of the network. 

When do we introduce DropOut, or when do we know we have some overfitting- When training accuracy is large and validation accuracy is falling behind, the netwrok is overfitting. The easiest was to prevent this is to add dropout. This layer will cause channels to be dropped randomly thus forcing the network to train harder.

Learning Rate - Used to set how fast the loss function can be minimized.

LR schedule and concept behind it- Optimum value for LR ensures that the global minima is hit graciously. 

Adam vs SGD- The choice between these two optimizers is subjective to the accuracy required and the type of network being built

When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)





