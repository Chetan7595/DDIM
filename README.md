# DDIM Pytorch
DDIM ([Denoising Diffusion Implicit Models](https://arxiv.org/abs/2010.02502)).

---
## Installation
This code work fine in the python version ```3.12.7```.
Install required modules by following command.
```
pip install -r requirements.txt
```

---


### Training

- Cifar10 (64 dimension)
```commandline
python train.py -c ./config/cifar10.yaml
```
- Cifar10 (128 dimension)
```commandline
python train.py -c ./config/cifar10_128dim.yaml
```
- CelebA-HQ

```commandline
python train.py -c ./config/celeba_hq_256.yaml
```

### Inference

- Cifar10 (64 dimension)
```commandline
python inference.py -c ./config/inference/cifar10.yaml -l /path_to_cifar10_64dim.pt/cifar10_64dim.pt
```
- Cifar10 (128 dimension)
```commandline
python inference.py -c ./config/inference/cifar10_128dim.yaml -l /path_to_cifar10_128dim.pt/cifar10_128dim.pt
```
- CelebA-HQ
  Download the dataset from the google drive link and save this according to below file system
- DDIM
    - /config
    - /src
    - /images_README
    - inference.py
    - train.py
    ...
    - /data (make the directory if you don't have it)
        - /celeba_hq_256
            - 00000.jpg
            - 00001.jpg
            ...
    
```

```commandline
python inference.py -c ./config/inference/celeba_hq_256.yaml -l /path_to_celeba_hq_256.pt/celeba_hq_256.pt
```

### Path

- After running the train command it will create an folder ```results```. For the cifar10 64-dim and cifar10 128-dim it will create an folder inside the ```results``` folder ```cifar10```. From which it we can get the ```.pt``` file. Same scenerio goes for celeba-hq.
- Replace these paths to get the inference.
