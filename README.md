# Sorghum-Plant-Classification

## Dataset
Available on Kaggle : https://www.kaggle.com/competitions/sorghum-id-fgvc-9/data

## Training Parameters
1. Optimizer -> Adam
2. Learning Rate -> 2e-5
3. Epochs -> 10
4. dropout -> 0.5
5. Loss -> Focal Loss with penalty factor of 2
6. Models used -> Swin Transformer and Efficient Net B4

## Result

### Swin Transformer
![SwinT Focal](https://user-images.githubusercontent.com/45042726/161034604-b42265b3-8d2f-4509-b184-64b788badf89.jpg)
Swin Transformer trained for 10 epochs could achieve a test accuracy of 53%.

### EfficientNetB4
![eff net b4](https://user-images.githubusercontent.com/45042726/161035854-550be355-7f81-471e-96cf-ce1586d633ad.jpg)
Efficient Net trained for 10 epochs could achieve a test accuracy of 49%.

### Weights and Biases Chart Comparison
![Performance Comparison Chart](https://user-images.githubusercontent.com/45042726/161035988-1d08fd15-8d4e-46c7-ab51-a379133a8757.png)

## Observations
1. Since the dataset was highly imbalanced, use of Focal loss improved the performance of the model by increasing the test accuracy by 2%.
2. EfficientNet was tending to overfit the dataset. Hence performing poorly on the test set.

