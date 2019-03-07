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

### Training Progress
#### Rate of Completion: 36%
#### Screen Shot
![](https://i.imgur.com/F8MjvCe.png)


## Inference cycleGAN in Personal Image
### Summer to winter
**Image1:**
![](https://i.imgur.com/2pChSaD.png)

**Image2:**
![](https://i.imgur.com/fnyF3jL.png)

**Image3:**
![](https://i.imgur.com/jgJTBdY.png)

**Image4:**
![](https://i.imgur.com/udtP6CN.png)

**Image5:**
![](https://i.imgur.com/hwlIwxS.png)

### Winter to summer
**Image1:**
![](https://i.imgur.com/KSfFxmQ.png)

**Image2:**
![](https://i.imgur.com/3OK3JHa.png)

**Image3:**
![](https://i.imgur.com/8Uin4jL.png)

**Image4:**
![](https://i.imgur.com/s4Nq2uX.png)

**Image5:**
![](https://i.imgur.com/rcNfHCu.png)


## Compare with Other Method
We use *Linear Color Transfer* as a comparison.

### Linear Color Transfer
https://github.com/ProGamerGov/Neural-Tools?fbclid=IwAR2aYbkqf-AAZuietcQMgraFMuzSxJaHbz54CJqb841rHCpgaP-0PitWqpU

### Original Images:
**Image 1:**
![](https://i.imgur.com/nIzljSE.jpg)

**Image 2:**
![](https://i.imgur.com/4EQgvtk.jpg)

**Image 3:**
![](https://i.imgur.com/0Y9L1lx.jpg)

**Image 4:**
![](https://i.imgur.com/cfNZ7x6.jpg)

### Result Images (cycleGAN vs Linear Color Transfer):
**Image 1:**
cycleGAN
![](https://i.imgur.com/dA6v9pk.png)
linear color transfer
![](https://i.imgur.com/7OefFkB.png)

**Image 2:**
cycleGAN
![](https://i.imgur.com/itCdb6R.png)
linear color transfer
![](https://i.imgur.com/Uu2sZc3.png)

**Image 3:**
cycleGAN
![](https://i.imgur.com/F5EWyzN.png)
linea color transfer
![](https://i.imgur.com/2tqwF5s.png)

**Image 4:**
cycleGAN
![](https://i.imgur.com/TcYB87C.png)
linear color transfer
![](https://i.imgur.com/Dwf6Z7U.png)