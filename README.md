# beat-PD

## Introduction
This repo is used for beat-PD challenge: https://www.synapse.org/?fbclid=IwAR2iNoMYb-paEWaIyqyOuD0hwaYCkh6N4X5WBArJe7bezWY1bSANKjvdX0s#!Synapse:syn20825169/wiki/596118

## Method DecisionTree
1. 02/03/2020
- Extract Features of [First 2s and Last 2s, Maximum and Minimum Widths, Nearest zeros values] of record.
- MSE of "on_off": 2.66839378238342
- Conclusion: Failure

## Method CNN - LSTM -FC
1. 02/03/2020
- Filename: "Model_1_MSE_1.439"
- Model: 

``` 
Conv2d(in_channels=1, out_channels=64, kernel_size=(10, 3), stride=(1, 1), padding=(1,1)) 
ReLU
Conv2d(in_channels=64, out_channels=128, kernel_size=(5, 3), stride=(5, 3))
ReLU
LSTM(input_size = 1, hidden_size = 1, num_layers=1)
Linear(self.128, num_classes)
```

- Loss Function: CrossEntropy().
- Optimizer: Adam().
- Training: Stochastic Gradient Descent.
- MSE of "dyskinesia": 1.439.
- Conclusion: It seem good, but I need < 1.1

2. 04/03/2020
- Filename: "Model_2_MSE_1.442"
- Model, LossFunc, Optimizer: same with Model_1
- Training: Mini Batch Gradient Descent
- MSE of "dyskinesia": 1.442
- Conclusion: It's not good.

3. 04/03/2020
- Filename: "Model_3"
- Model: same with Model_1
- Loss Function: MSELoss()
- Optimizer: Adam()
- Training: Mini batch
- MSE
- Conclusion


