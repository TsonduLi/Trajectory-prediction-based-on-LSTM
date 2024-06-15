# Vehicle Trajectory Prediction in Autonomous Driving Systems

## Overview
This is a course project of ME343: Machine Learning for Computational Engineering, it focuses on predicting the future trajectory of vehicles, which is a crucial aspect of autonomous driving systems. It aims to forecast the future path of vehicles based on their historical and current states, enhancing path planning, collision avoidance, and overall safety and efficiency.

## Technical Challenge
The primary challenge lies in accurately predicting future vehicle trajectories with high accuracy and low latency, considering the non-linear and dynamic nature of vehicle movements, environmental influences, and real-time decision-making requirements.

## Approach
We utilize Long Short-Term Memory (LSTM) networks for their effectiveness in sequence prediction tasks, especially for handling the temporal dependencies in vehicle movements. The model inputs a sequence of past vehicle states (position, velocity, heading) and outputs a sequence predicting future positions.

## Code Implementation
The Python notebook and Wandb link for the project can be found [here](https://api.wandb.ai/links/zhiyuanl925/6nro4ox1).

## Dataset
The project uses the Argoverse 2 Motion Forecasting Dataset, focusing on vehicle trajectory data, including position, velocity, and heading, grouped by unique track IDs. The LSTM model's sequence length is set to 5, with data normalization performed using MinMaxScaler.

## Results
The model demonstrates a decrease in training/validation loss and relative error over training epochs. Optimal parameters were identified as batch size = 32, hidden layer size = 128, and learning rate = 0.0005.

## Limitations and Future Work
The model may struggle with erratic movements and could benefit from integrating more environmental data or employing advanced models such as encoder-decoder transformers. Further hyperparameter tuning and training with a broader data set could also enhance performance.

## References
1. Hochreiter, S., & Schmidhuber, J. (1997). Long Short-Term Memory. Neural Computation, 9(8), 1735-1780.
2. Rumelhart, D. E., Hinton, G. E., & Williams, R. J. (1986). Learning representations by back-propagating errors. Nature, 323(6088), 533-536.
