# Autoencoders

Train an autoencoder (with CNN layers) to encode and decode an image. The input image will have noise added to it, the type of noise will be discussed below. Essentially, you’ll be training a denoising autoencoder. Then you’ll compare putting noise on an image from outside the dataset, which can be a custom photo you took (like trees, street, dogs in the street, cat, buildings, etc) or an image you chose from an online search and use it to test the auto encoder as follows:

     - Add noise to the image, and pass it through the autoencoder (the encoder should work as it was trained)
     - Pass the image as it is without noise through the encoder part, then add noise to the encoded vector, then decode it.
     - Apply point (1), (2) on 3 or more custom images (outside of the dataset) and show and compare the decoded images with the original.

----------------------------------------

<b>Dataset</b>

You are allowed to use any dataset as long as it satisfies the following:

      - Dataset consists of coloured images.
      - Dataset has at least 3 different background/scenery.
      - At least 100 different images for training.
      - Image size should be at least 128 or bigger (if possible, use at least size of 256 as minimum in width and height to have clear results)
      - The dataset can be a subset of any dataset.

----------------------------------------

<b>Noise</b>
  
The noise you’ll use is random noise sampled from any distribution, we suggest using the gaussian (normal) distribution in your noise generation for both the image and the encoded vector.
Just note that whatever distribution for the noise you’ll use, use it for both image and encoded vector.

----------------------------------------

<b>Autoencoder</b>

Try to not have too many layers (there is no limitation here), this is to save some computation time and avoid a bit of possible overfitting. Use whatever activations you see fit.
Train the autoencoder to encode a vector of size between 8-16 (a small) and 32-80 (a moderate size). So, you will need 2 auto encoders.
Save the autoencoders after training them.
Remember that the autoencoder is training on returning (image + noise) to (image)

----------------------------------------

- Train multiple autoencoder to encode vectors of size 8,16,32,64 (You can add more). And encode and decode a custom image.
- Apply PCA reduction and restoration on the same image, using the top 8, 16, 32, 64 (same as the above sizes) components.
- Compare the PCA restored images using different component sizes with the Encoded then decoded images using different autoencoder sizes. Show and compare the decoded and restored images and write what you observe.

