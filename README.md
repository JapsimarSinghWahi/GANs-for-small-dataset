# GANs-for-small-dataset
DC Gans Implementaion for Small Dataset (Lunar Dataset)

Machine learning with insufficient datasets is a proof of concept that aims towards generating
synthetic images from a sparse dataset. The objective was to implement various flavors of Generative
Adversarial Networks (GANs) and generate a comparative analysis for the quality of synthetically
generated images. Various image augmentation techniques coupled with different neural net
architectures were implemented to improve the image quality and attempt to make a generalized
model that can accommodate various datasets of different shapes and sizes. The generated images
from these implementations were used to train a U-net classifier model and compared the results
with a baseline model of artist’s renders to analyze the usability of the synthetic images. The
algorithm with the most promising results was exposed to different amounts of real images and the
corresponding generated images were examined. We aim to quantify the effects on generated images
with respect to the available amount of real images.


Deep Convolutional GAN (DCGAN), that uses a set of constraints on the architectural topology of
Convolutional GANs that make them stable to train in most settings. DCGAN is one of the popular
and successful network designs for GAN. It mainly composes of convolution layers without max
pooling or fully connected layers. It uses convolutional stride and transposed convolution for the
downsampling and the upsampling. The figure below is the network design for the generator. The
simplicity of DCGAN contributes to its success. It uses CNN as a feature extractor.[1]
Deep Convolutional GANS has the following architecture guidelines which we followed –
1. Replace any pooling layers with strided convolutions (discriminator) and fractional strided
convolutions (generator).
2. Use batchnorm in both the generator and the discriminator.
3. Remove fully connected hidden layers for deeper architectures.

3

4. Use ReLU activation in generator for all layers except for the output, which uses Tanh.
5. Use LeakyReLU activation in the discriminator for all layers.



