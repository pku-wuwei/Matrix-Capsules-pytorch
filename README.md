# Matrix-Capsules-pytorch
This is a pytorch implementation of [Matrix Capsules with EM routing](https://openreview.net/pdf?id=HJWLfGWRb)

In ```Capsules.py```, there are two implemented classes: ```PrimaryCaps``` and ```ConvCaps```.
The ClassCapsules in the paper is actually a special case of ```ConvCaps``` with whole receptive field, transformation matrix sharing and Coordinate Addition.

In ```train.py```, I define a CapsNet in the paper using classes in ```Capsules.py```, and could be used to train a model for MNIST dataset.

## Train a small CapsNet on MNIST
```python train.py -batch_size=64 -use_cuda=True -lr=2e-2 -num_epochs=5 -r=3 -print_freq=5```

## Results
The test accuracy is around 99% after 5 epochs of training with a small Capsule of A,B,C,D,r = 64,8,16,16,1. More results on different configurations are welcomed.


## TODO
* using more matrix operation rather than ```for``` iteration in E-step of ```Capsules.py```.

