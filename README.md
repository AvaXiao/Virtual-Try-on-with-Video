# Virtual-Try-on-with-Video
Traditional virtual try on can only output one picture, in other words, we can only get the generated image with the original pose of the input image. How can we generate images with different poses?

We developed a virtual try-on system. Besides accepting one cloth image and one target person image, our system also needs a short skeleton video of posing. Then we will generate a video of the target person wearing the target cloth with the same posing. 

During the process, we mainly have three contributions:
Combine virtual try on model with pose transfer model to implement multi-poses virtual try on.
Refine the original virtual try on model with GAN to improve the quality of generated images.
Find a more comprehensive dataset to train models which improve the generate quality notability.
