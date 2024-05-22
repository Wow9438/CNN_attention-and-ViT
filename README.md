We are given a data set of size 10000 images of 10 classes to train a neural network inorder to classify the train image data set.

In case of first approach I had used Vanilla CNN with some self attention layers embedded in between CNN layers in order to get dependencies on itself

In case of second approach I had used ViT (Vision Transformer Link: https://arxiv.org/pdf/2010.11929 ) , It's completely based on Transformer Architecture with No CNN's in it.Intially Image is patchified i.e; divided into patches based on the patch size and then a class token concatenated with patchified image along column,let us call this an embedding
Later Position encoding is performed to the embedding ,i.e; input to the transformer is total_embedding = positional_embedding + embedding and Transormer architecture is nothing but Multi-headed Self Attention Layers with Layer Norms and Linear layers and at final layer i.e; input to the final linear layer is the last column of the total_embedding i.e; column of the class token since it encodes all the information of the image. 
