# Homework3-MNIST-Fashion-MNIST
all files for the homework 3 programs

Acknowledgements:
•	Tensorflow tutorial - https://www.tensorflow.org/tutorials/generative/dcgan
•	Marianna Linhares Monterio’s Github - https://github.com/mari-linhares/DeepLearning/tree/master/GAN-fashion-MNIST

Procedure:
A Generative Adversarial Network (known from here on out as a GAN) is a type of neural network model that uses itself to train and improve both its detecting and deceptive abilities. The Discriminator is made and trained to accept data, either training data or generated, and tell the difference between the two. The Generator makes these fake images and trains to get the fake to look as close to real data as possible with the goal of fooling the Discriminator. This method of training makes the GAN very popular these days as it has the ability to train itself and be widely applicable in various real-world situations. In this project a DCGAN was used to train the basic MNIST dataset. To create the DCGAN I followed the tensorflow tutorial and grabbed the data using keras. I ran the initial program at 50 epochs, but upon seeing the result, ran an additional 25. To see if the image improved significantly. 

Summary:
The original results of the run with just 50 epochs showed great improvement in the generator. The numbers went from unidentifiable blobs, to more handwritten looking numbers. Some did also resemble letters, but they all had well defined shapes.
Main body/findings:
For this project I used the tensorflow website’s tutorial for the GAN as a base to understand and program the DCGAN. The environment of the program was Pycharm using python3.7, tensorflow 2.0, and anaconda3. I started off building the program by introducing the data creating the batch size’s to be run and creating the generator. The generator had an input layer, two hidden layers, and an output layer. A leaky ReLu was added as a penalty to the model and random noise was further added to the system to add a more unpredictable nature. The discriminator was built the same as the generator but without the noise and ReLu. 
Next I imported a cross entropy function from keras and used in in both the discriminator and generator to predict the loss. The training loop was then defined and the way the image would be visualized after each epoch was finished. Next the function for the model was built and set to run and the image set to print. 
The DCGAN took a few hours to run and produced 50 pictures, one for each epoch, showing incremental improvement over time. After 50 epochs the images were still very low quality compared to the dataset, but were much more similar than when the program started.

This homework’s goal was to make a DCGAN and have it train so that the discriminator would eventually be able to imitate the training data properly. In the end the generator’s imitation skills improved greatly, but with only 50 iterations it did not yet manage to duplicate the original dataset.
