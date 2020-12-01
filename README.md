# Virtual-Try-on-with-Video
Traditional virtual try on can only output one picture, in other words, we can only get the generated image with the original pose of the input image. How can we generate images with different poses?

We developed a virtual try-on system. Besides accepting one cloth image and one target person image, our system also needs a short skeleton video of posing. Then we will generate a video of the target person wearing the target cloth with the same posing. 

## Pose transferm
This is the [Pose-Guided Person Image Animation](https://github.com/RenYurui/Global-Flow-Local-Attention/blob/master/PERSON_IMAGE_ANIMATION.md) task from [Global-Flow-Local-Attention](https://github.com/RenYurui/Global-Flow-Local-Attention). We use its pretrained model to generate target pose video.

If you want to generate your owm video, you should extract skeleton from your video with [alpha pose](https://github.com/MVIG-SJTU/AlphaPose) first. 

Examples:
Demo using `FastPose` model.
``` bash
./scripts/inference.sh configs/coco/resnet/256x192_res50_lr1e-3_1x.yaml pretrained_models/fast_res50_256x192.pth ${VIDEO_NAME}
```
We provide "coco_2_openpose_pose_tansform.py" to tranform the outputs of alpha pose to be openpose format since Motion Extraction Net deals with openpose format skeletons.

The next step is using Motion Extraction Net to preprocess dirty skeletons. Assuming that you want to smooth the skeleton sequences of the fashion data set, you can use the following code:
