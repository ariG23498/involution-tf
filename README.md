# involution-tf
TensorFlow implementation of [Involution: Inverting the Inherence of Convolution for Visual Recognition](https://arxiv.org/abs/2103.06255). In this reporsitory you will find a `jupyter notebook` that houses the `involution` layer. 

# Convolution
![Conv](https://user-images.githubusercontent.com/36856589/120093172-1171d680-c136-11eb-966f-f6e6d6b8dd0a.jpeg)

# Involution
![Invo](https://user-images.githubusercontent.com/36856589/120093680-73800b00-c139-11eb-9c00-4da8c6a8bfc1.jpeg)

# Thoughts
I have also tried training a [classifier on CIFAR10](https://www.tensorflow.org/tutorials/images/cnn) from scratch wtih `convolutions` and `involutions`. The loss plots, accuracy plots and the size of the models are quite astonishing. While convs outperform invs, we need to keep in mind the amount of parameters for invs.
```
Convolutions:
Total params: 319,178
Trainable params: 319,178
Non-trainable params: 0
```
![image](https://user-images.githubusercontent.com/36856589/120099313-658db280-c158-11eb-8c1e-4e2f20a79ca1.png)
![image](https://user-images.githubusercontent.com/36856589/120099315-69213980-c158-11eb-8b97-d1a1bb0827b1.png)

```
Involutions:
Total params: 13,080
Trainable params: 13,074
Non-trainable params: 6
```
![image](https://user-images.githubusercontent.com/36856589/120099327-79d1af80-c158-11eb-8268-dd51ecf5a368.png)
![image](https://user-images.githubusercontent.com/36856589/120099331-7d653680-c158-11eb-9fe6-472f8fe20a45.png)



# Visualization of the activations
Below is the activation outputs from the involution kernels. We can observe that, involutions indeed is spatial-specific and channel-agnostic.
![image](https://user-images.githubusercontent.com/36856589/120099344-8950f880-c158-11eb-9a21-c3d34bc2b987.png)

# Citation
```
@misc{li2021involution,
      title={Involution: Inverting the Inherence of Convolution for Visual Recognition}, 
      author={Duo Li and Jie Hu and Changhu Wang and Xiangtai Li and Qi She and Lei Zhu and Tong Zhang and Qifeng Chen},
      year={2021},
      eprint={2103.06255},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
