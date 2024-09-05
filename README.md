# multivariate-time-series-prediction
**Comparison between two state of the art methods in multivariate time series prediction for Panama electricity demand**<br>
In 2023, two different approaches for time series predictions have been introduced:<br>
-[Dlinea](https://arxiv.org/abs/2202.07125)<br>
-[PatchTST](https://arxiv.org/abs/2211.14730)<br>
In this article more detail about PatchTST has been provided and performance of these two approaches in [Panama Electricity Load Forecasting dataset](https://www.kaggle.com/datasets/pateljay731/panama-electricity-load-forecasting/data) will be compared.<br>
## Section 1: Introduction<br>
Traditional models like recurrent neural networks (RNNs) and long short-term memory (LSTM) networks often struggle with long-range dependencies and are computationally intensive due to their sequential processing nature. While transformers address these drawbacks by considering attention mechanisms. This mechanism allows models to focus on specific parts of the input data that are more relevant to the current task, rather than treating all parts of the input equally. Therefore, making it easier to model complex interactions that may get lost in traditional sequential models. Additionally, transformers process sequences in parallel, unlike RNNs and LSTMs, which process one step at a time. This speeds up training and makes the model more efficient.<br>
In recent years, some variations of transformers have been introduced to predict multivariate time series such as Informer (Zhou et al., 2021), Autoformer (Wu et al., 2021), and FEDformer (Zhou et al., 2022). In 2023, another study claimed the effectiveness of transformers and pointed to some drawbacks of it in time series forecasting. This drawback refers to the permutation-invariant feature of self attention which disregards the order of elements. Although various positional encoding techniques can help retain some order information, temporal information loss remains unavoidable when self-attention is applied on top of them.<br>
This limitation is generally not critical for tasks like natural language processing (NLP), where the overall meaning of a sentence remains largely intact even if the word order is altered. However, in time series analysis, where the data lacks inherent semantic meaning, the primary focus is on capturing the temporal dynamics between consecutive points. 
In this context, the order of the data is essential and plays a critical role in accurately modeling temporal patterns. In this study a simple linear model LTSF-Linear, Dlinear,  could get better results compared to other transformer methods.
After that another variant of the transformer called the PatchTST could solve the limitations of previous transformer approaches and beat the Dlinear model.<br>
In below the main idea behind PatchTST approach have been provided:<br>
1. Chanel independence<br>
Data set converted from multivariate to univariate. In another word the data which has m*n dimensions converted to m vectors of 1*n dimensions. This process called channel independence means that input token only contains information from a single channel or feature.






These methods have been implemented on 8 popular time series datasets and showd that PatchTST have better result.<br>
![test](Images/Channel_independence.png)
