# Sorghum-Plant-Classification

## Dataset
Available on Kaggle : https://www.kaggle.com/competitions/sorghum-id-fgvc-9/data

## Result

### Swin Transformer

#### Training Parameters
1. Optimizer -> Adam
2. Learning Rate -> 2e-5
3. Epochs -> 10
4. dropout -> 0.5
5. Loss -> Focal Loss with penalty factor of 2

![SwinT Focal](https://user-images.githubusercontent.com/45042726/161034604-b42265b3-8d2f-4509-b184-64b788badf89.jpg)

Swin Transformer trained for 10 epochs could achieve a test accuracy of 53%.

### EfficientNetB4

#### Training Parameters
1. Optimizer -> Adam
2. Learning Rate -> 2e-5
3. Epochs -> 10
4. dropout -> 0.5
5. Loss -> Focal Loss with penalty factor of 2

![eff net b4](https://user-images.githubusercontent.com/45042726/161035854-550be355-7f81-471e-96cf-ce1586d633ad.jpg)

Efficient Net trained for 10 epochs could achieve a test accuracy of 49%.

### Weights and Biases Chart Comparison
![Performance Comparison Chart](https://user-images.githubusercontent.com/45042726/161035988-1d08fd15-8d4e-46c7-ab51-a379133a8757.png)

#### The models further were written in pytorch lightning module. Pytorch Lightning ensures efficient usage of the GPU, hence does not give CUDA memory exceeded error.

### EfficientNetB3

#### Training Parameters
1. Optimizer -> Adam
2. Learning Rate -> adaptive lr depending on the loss. Start with 1e-4.
3. Epochs -> 20
4. dropout -> 0.5
5. Loss -> Focal Loss with penalty factor of 2

![eff net b3](https://user-images.githubusercontent.com/45042726/161560275-29615bc7-5f83-4dde-8e89-e947c6eb706f.png)

Efficient Net B3 trained for 20 epochs could achieve a test accuracy of 80%.

## Observations
1. Since the dataset was highly imbalanced, use of Focal loss improved the performance of the model by increasing the test accuracy by 2%.
2. EfficientNet was tending to overfit the dataset with very less learning rate. Hence performing poorly on the test set.
3. Adaptive learning rate based on the loss and training for more number of epochs gave significant improvement in the testset prediction.

