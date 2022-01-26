# vessel-segmentation

![outputs/Example.png](outputs/Example.png)

Left: Preprocessed input, Middle: Ground truth, Right: Prediction

### Summary
This repository contains code for a U-net model for vessel segmentation (Adapted from https://github.com/mitseng/RetinalVesselSegmentation) which is further used for ROP classification.

### Details
Training was done using a U-net based model on 64x64 random cropped patches with normalization, horizonatal and vertical flips and random rotate augmentions with batch size as 16 using weighted crossentropy loss(0.8, 0.2), SGD as optimised with learning rate 0.01 and momentum 0.9. Inference was done on the full image.

### Environment
**environment.yml** contains the dependencies for the conda environment.

### Training using db_train.csv: [Trained model will be stored in models/]
```
$ python3 main.py
```

### Evaluating using db_test.csv: [Outputs will be stored in outputs/]
```
$ python3 test.py
```

Authors:
1. Ashwin Vaswani
2. Praveer Singh
