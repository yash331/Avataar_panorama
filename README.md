# Avataar_panorama

All of the thing (result images) are in the ipynb file, with imgs for 5 different prompts. 
## Seam Tiling

### New loss function or circular padding
Incoherent images are due to lack of control over seams of the images, I thought of a apporach in which we can define a loss function(works as a feedback), which we concatenate image with itself and find gradient at the middle to observe the sharp transition, but as I have limited resources(colab) and no data so I couldn't train the whole model again.
But there exist circular padding option in SD pipeline which is very similar.

```math

L_{new\ }=\ L_{SD\ }+\sum_{n=0}^{img}\sum_{x=width-3}^{width+3}∇\left(I\left(x,y\right)\right)

```

## Depth Control
Generated image is then passed to a new pipe which takes prompt, image and depth_mask for the image, by fine-tuning strength, no of inference and controlnet scaling we can get better results. 
