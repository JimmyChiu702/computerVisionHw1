# Computer Vision Homework 1 Report
## Training cycleGAN
### Code Modification
#### Problem
We encountered the following error:

`RuntimeError: input and target shapes do not match: input [1 x 1], target [1] at /pytorch/aten/src/THNN/generic/MSECriterion.c:12`

This error should be because of the different version of pyTorch
#### Solution
We change the target dimesion using `unsqueeze()` function.

For instence : 

original : 
`loss_GAN_A2B = criterion_GAN(pred_fake, target_real)`

modified : 
`loss_GAN_A2B = criterion_GAN(pred_fake, target_real.unsqueeze(0))`

### Current Progress
#### Rate of Completion: 36%
#### Screen Shot
![](https://i.imgur.com/tmcJxDc.png)

## Inference cycleGAN in Personal Image

## Compare with Other Method