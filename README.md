# Face-Generator-by-DCGAN

## Outcomes

<table border="0">
<tr>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/generation_animation2.gif" width="100%" />
    </td>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/CelebA_DCGAN_train_hist.png", width="100%" />
    </td>
</tr>
</table>

<table border="0">
<tr>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/CelebA_DCGAN_1.png" width="100%" />
    </td>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/CelebA_DCGAN_10.png" width="100%" />
    </td>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/CelebA_DCGAN_50.png" width="100%" />
    </td>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/CelebA_DCGAN_150.png" width="100%" />
    </td>
    <td>
    <img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/CelebA_DCGAN_300.png" width="100%" />
    </td>
</tr>
</table>

## Datasets
* Collecting Myself.
[Face_dataset](https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/input/data/face_dataset.7z)
 
## Model
### Optimizer(Adam)
 * Discriminator : learning rate = 0.00005, betas = (0.5, 0.999)
 * Generator : learning rate = 0.001, betas = (0.5, 0.999)
 
### DCGAN
<p align="center">
<img src="https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/image/dcgan.png" width="800" />
</p>
#### Generator
* Purpose : cheat Discriminator
* Input : Random Noise with Normal Distribution(0,1), shape(100) 
* Output : Image shape same as true face image, shape(64, 64, 3)

#### Discriminator
* Purpose : Distinguish image comes from Genertors and true image.
* Input : fake image generate by Generator + True Image, shape(64, 64, 3)
* Output : Probability if the image are true image or not. (1)

## Demo
[jupyter notebook](https://github.com/wewanadi/Face-Generator-by-DCGAN/blob/master/main.ipynb)

* Set CUDA to -1 for training without GPU.dc
