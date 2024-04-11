# Avataar_panorama

Incoherent images are due to lack of control over seams of the images, I thought of a apporach in which we can define a loss function(works as a feedback), which we concatenate image with itself and find gradient at the middle to observe the sharp transition, but as I have limited resources(colab) and no data so I couldn't train the whole model again.
But there exist circular padding option in SD pipeline which is very similar.
