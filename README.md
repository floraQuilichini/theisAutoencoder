# theisAutoencoder
this repository is a pytoch implementation (on jupyter notebook) of the autoencoder of Theis et al, 2017

In the attached jupyter notebook, some parts of the code are mandatory and other optional. 
Snippets from 1 to 6 are mandatory. Then, the snippets 7-8 can be skipped. This snippet -called incremental training- has been used to reproduce the 2-steps training mentionned in the paper. First step : incremental training where the weights of the latent vector are progressivelly enabled. Second step : global training where all the weights are optimized all together (the initialization of global training is the computed weights of incremental training). According to the authors (Theis et al), this training is more efficient than doing only the second step (from random initialization). But the users are free to omit the first part. In this case, they must comment the first fourth lines of snippet 9. Snippets 11-12 refer to test. The user is free to comment the parts he doesn't need (metric calculus, saving results). Snippet 13 also refers to test but this time, with the addition of a range coder in order to encode the symbols of the latent vector. This snippet is optional, but the user need to install first the rangecoder ( https://github.com/lucastheis/rangecoder ) in order to make it work. 
In the code, each time we need to refer to a file (to get or write data), the name of the file are explicitly written. The user can replace our file organization by its own. In our organization, all the additional repository are directly situated in the folder of the notebook. There are additional repositories : the "data" repository which contains the "flickr" and "kodak" images, the "model_parameters" repository to store the learned weights of the network, the "reconstructed" repository where to store the reconsrructed images and the "latent_vect_encoded" repository where the encoded-by-rangecoder latent vector is stored. 
