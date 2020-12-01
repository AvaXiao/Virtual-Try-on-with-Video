# Virtual-Try-on-with-Video
Traditional virtual try on can only output one picture, in other words, we can only get the generated image with the original pose of the input image. How can we generate images with different poses?

We developed a virtual try-on system. Besides accepting one cloth image and one target person image, our system also needs a short skeleton video of posing. Then we will generate a video of the target person wearing the target cloth with the same posing. 

## Pose transferm
This is the [Pose-Guided Person Image Animation](https://github.com/RenYurui/Global-Flow-Local-Attention/blob/master/PERSON_IMAGE_ANIMATION.md) task from [Global-Flow-Local-Attention](https://github.com/RenYurui/Global-Flow-Local-Attention). We use its pretrained model to generate target pose video.
