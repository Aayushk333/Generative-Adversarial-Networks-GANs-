# DCGANs (Deep Convolutional Generative Adversarial Networks)

One of the most interesting parts of Generative Adversarial Networks is the design of the Generator network. The Generator network is able to take random noise and map it into images such that the discriminator cannot tell which images came from the dataset and which images came from the generator.

_This is a very interesting application of neural networks. Typically neural nets map input into a binary output, (1 or 0), maybe a regression output, (some real-valued number), or even multiple categorical outputs, (such as MNIST or CIFAR-10/100)._

There are the lines taken from a paper by __Alec Radford, Luke Metz, and Soumith Chintala that introduces deep convolutional GANs, whose basic structure we use in our generator__

_In recent years, supervised learning with convolutional networks (CNNs) has seen huge adoption in computer vision applications. Comparatively, unsupervised learning with CNNs has received less attention. In this work we hope to help bridge the gap between the success of CNNs for supervised learning and unsupervised learning. We introduce a class of CNNs called deep convolutional generative adversarial networks (DCGANs), that have certain architectural constraints, and demonstrate that they are a strong candidate for unsupervised learning. Training on various image datasets, we show convincing evidence that our deep convolutional adversarial pair learns a hierarchy of representations from object parts to scenes in both the generator and discriminator. Additionally, we use the learned features for novel tasks - demonstrating their applicability as general image representations_
