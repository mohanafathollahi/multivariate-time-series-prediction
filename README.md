# multivariate-time-series-prediction
**Comparison between two state of the art methods in multivariate time series prediction for Panama electricity demand**<br>
In 2023, two different approaches for time series predictions have been introduced:<br>
-[Dlinea](https://arxiv.org/abs/2202.07125)<br>
-[PatchTST](https://arxiv.org/abs/2211.14730)<br>
In this article more detail about PatchTST has been provided and performance of these two approaches in [Panama Electricity Load Forecasting dataset](https://www.kaggle.com/datasets/pateljay731/panama-electricity-load-forecasting/data) will be compared.<br>
## Section 1: Introduction<br>
Traditional models like recurrent neural networks (RNNs) and long short-term memory (LSTM) networks often struggle with long-range dependencies and are computationally intensive due to their sequential processing nature. While transformers address these drawbacks by considering attention mechanisms. This mechanism allows models to focus on specific parts of the input data that are more relevant to the current task, rather than treating all parts of the input equally. Therefore, making it easier to model complex interactions that may get lost in traditional sequential models. Additionally, transformers process sequences in parallel, unlike RNNs and LSTMs, which process one step at a time. This speeds up training and makes the model more efficient. 

These methods have been implemented on 8 popular time series datasets and showd that PatchTST have better result.<br>
![test](Images/Channel_independence.png)
